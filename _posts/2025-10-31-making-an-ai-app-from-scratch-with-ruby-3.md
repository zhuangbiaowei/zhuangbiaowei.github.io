---
layout: post
title: 用Ruby从头做一个AI Agent应用 -- SmartResearch （一个真实、有用的研究助手）
date: 2025-10-31 16:00 +0800
tags: OpenSource Ruby AI Agent Research
comments: true
---

这是一篇系列文章，描述我如何使用Ruby语言，从头构建一个AI Agent的应用。在前两篇中，我们分别介绍了[Smart Prompt](/2025/04/06/making-an-ai-app-from-scratch-with-ruby-1.html)和[Smart Agent](/2025/04/23/making-an-ai-app-from-scratch-with-ruby-2.html)，现在终于来到了这个系列的最终章：**SmartResearch**，一个真正实用、能够帮助进行学术研究和知识管理的AI助手。

开源地址：[SmartResearch](https://github.com/zhuangbiaowei/SmartResearch)

## 第三部分：SmartResearch - 学习与思考的循环（CoLT）

SmartResearch不仅仅是一个AI对话工具，它实现了一个完整的**学习与思考循环（Chain of Learning & Thinking, CoLT）**：

```
[思考] → [搜索] → [学习] → [存储] → [重复]
```

这个自增强循环让AI能够持续积累知识、自适应推理，并不断改进。

### 三模式应用系统

SmartResearch运行在TUI（终端用户界面）中，通过F键切换三种操作模式：

- **F2 - 交流与探索模式**：交互式研究和问答，带自主搜索规划
- **F3 - 知识库模式**：文档管理、下载、标记和基于向量的检索
- **F4 - 创作模式**：基于积累的知识生成大纲和撰写文章

### 核心架构：建立在SmartAgent之上

SmartResearch建立在之前介绍的SmartAgent框架之上，提供了完整的Agent系统：

```ruby
# 在agents/smart_search.rb中定义的搜索Agent
SmartAgent.define :smart_search do
  question = params[:text]
  result = call_worker(:pre_search, params, with_tools: true, with_history: true)

  if result.call_tools
    call_tools(result)
    params[:text] = "请输出一份搜索规划"
    result = call_worker(:pre_search, params, with_tools: true, with_history: true)
  end

  params[:text] = result.content
  result = call_worker(:smart_search, params, with_tools: true, with_history: true)

  if result.call_tools
    call_tools(result)
  end

  params[:text] = question
  result = call_worker(:summary, params, with_tools: false, with_history: true)

  result.content
end
```

### 知识存储系统

SmartResearch使用PostgreSQL + pgvector扩展来存储和管理知识：

- **ResearchTopic**：顶层研究主题
- **SourceDocument**：网页、PDF、DOCX文件
- **SourceSection**：内容块（最大4000字符，100字符重叠）
- **Embedding**：向量嵌入用于语义搜索（1024维）
- **Tag**：层次化标记系统，包含类型标签和内容标签

内容首先按Markdown标题分割，然后按最大字符数分块，每个块都会被嵌入和标记。

### 内容处理管道

1. **用户在F2模式提问**
2. **`pre_search`工作器分析范围并生成搜索计划**
3. **`smart_search`工作器使用工具执行搜索**
4. **结果存储为SourceDocuments（内容为"null"占位符）**
5. **在F3模式使用`dall`命令下载完整内容**
6. **内容被分块、嵌入、标记并链接到研究主题**
7. **在F4模式，向量搜索检索相关内容用于文章写作**

### 分块策略

内容首先按Markdown标题分割，然后按max_chars（默认4000）分块，各块之间保留100字符的重叠：

```ruby
def chunk_content(content, max_chars = 4000)
  # 如果内容长度小于max_chars，则整篇返回
  return [content] if content.length <= max_chars

  # 按照markdown的语法分段
  chunks = split_by_markdown_headers(content, max_chars)

  # 如果按markdown分段后仍然有超过max_chars的块，则进一步分片
  final_chunks = []
  chunks.each do |chunk|
    if chunk.length <= max_chars
      final_chunks << chunk
    else
      # 按max_chars大小分片，且各片之间保留100的重叠内容
      final_chunks += split_with_overlap(chunk, max_chars, 100)
    end
  end

  final_chunks
end
```

### F3知识库命令

在F3模式下，你可以使用以下命令：

- `l` / `list`：列出所有研究主题
- `l [num]`：列出主题ID下的文档
- `ll [num]`：显示文档内容和标签
- `d [num]`：下载文档ID的完整内容
- `d [url]`：下载并保存新URL
- `dd [num]`：下载主题ID下的所有文档
- `dall`：下载所有不完整的文档
- `ask [question]`：使用向量搜索查询知识库
- `del [num]`：删除文档及其所有关系

### F4写作命令

在F4模式下，你可以使用以下命令：

- `outline [topic]`：生成文章大纲 → `reports/outline.json`
- `outline`：显示当前大纲
- `outline [discussion]`：基于反馈修改现有大纲
- `del`：删除outline.json
- `write_all` / `wa`：从大纲写完整文章 → `reports/`
- `rewrite [chapter_id] [instructions]`：重写特定章节
- `format`：清理和去重脚注

### 流式显示

TUI使用回调进行实时显示：

```ruby
agent.on_reasoning do |reasoning_content|
  print reasoning_content.dig("choices", 0, "delta", "reasoning_content")
  print "\n" if reasoning_content.dig("choices", 0, "finish_reason") == "stop"
end

agent.on_content do |content|
  print content.dig("choices", 0, "delta", "content")
  print "\n" if content.dig("choices", 0, "finish_reason") == "stop"
end

agent.on_tool_call do |msg|
  puts msg
end
```

### MCP服务器集成

SmartResearch集成了多个MCP服务器：

- **opendigger.rb**：开源项目指标分析
- **all_in_one.rb**：通用研究工具包
- **amap.rb**：位置/地图服务

每个MCP服务器都是一个Ruby类，定义了SmartAgent可以调用的工具。

### 配置系统

SmartResearch使用分层配置：

- **`config/llm_config.yml`**：SmartPrompt引擎配置（LLM适配器、API密钥、工作器/模板路径）
- **`config/agent.yml`**：SmartAgent引擎配置（代理/工具/MCP路径、日志记录）
- **`lib/database.rb`**：数据库连接字符串

### 实际使用示例

让我们看看SmartResearch如何帮助进行实际研究：

1. **启动应用**：
```bash
./bin/smart_research
```

2. **在F2模式提问**：
```
请帮我研究一下Ruby在AI领域的应用现状
```

3. **系统自动**：
   - 分析问题范围
   - 生成搜索计划
   - 执行搜索并保存结果
   - 提供初步总结

4. **在F3模式下载内容**：
```
dall
```

5. **在F4模式生成文章**：
```
outline Ruby在AI领域的应用现状
write_all
```

### 为什么选择Ruby？

正如前两篇文章提到的，Ruby在LLM生态中确实"一穷二白"，但这正是挑战所在。通过SmartResearch，我们证明了：

1. **Ruby可以构建复杂的AI应用**
2. **DSL设计让代码更优雅**
3. **TUI界面提供优秀的用户体验**
4. **完整的Agent系统可以处理复杂任务**

### 技术栈总结

- **RubyRich**：提供TUI组件和事件处理
- **SmartPrompt Engine**：管理LLM交互、历史记录和工作器调用
- **SmartAgent Engine**：提供代理定义、工具调用和MCP集成
- **Better Prompt**：提示优化系统
- **Sequel ORM**：数据库抽象

### 外部依赖

- **markitdown**：Python工具，用于将各种格式转换为Markdown
- **PostgreSQL + pgvector**：向量相似性搜索
- **SQLite3**：Better Prompt提示优化数据库
- **MCP Servers**：基于Node.js的工具

## 结语

通过这个系列，我们展示了如何从零开始，用Ruby语言构建一个完整的AI Agent应用生态系统：

1. **Smart Prompt**：基础的大模型调用和模板系统
2. **Smart Agent**：增强的Agent框架，支持工具调用和MCP
3. **SmartResearch**：实用的研究助手，实现学习与思考循环

SmartResearch不仅仅是一个技术演示，它是一个真正有用的工具，能够帮助研究人员、学生和任何需要系统化知识管理的人。它证明了Ruby语言在AI领域的潜力，以及"从零开始"构建复杂系统的可行性。

希望这个系列对你有所启发，也欢迎你参与SmartResearch的开发，共同探索AI Agent的更多可能性！

---

*本系列文章到此结束，感谢阅读！*