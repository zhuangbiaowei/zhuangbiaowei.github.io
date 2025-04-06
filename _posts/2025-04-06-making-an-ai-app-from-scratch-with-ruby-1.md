---
layout: post
title: 用Ruby从头做一个AI Agent应用 -- Smart Prompt
date: 2025-04-06 11:59 +0800
tags: OpenSource Ruby AI Agent
comments: true
---
这是一篇系列文章，描述我如何使用Ruby语言，从头构建一个AI Agent的应用，真的（几乎）是从头构建，因为Ruby语言在LLM这个生态中，简直就是一穷二白，啥也没有。

我的底层依赖只有两个：

* [ruby-openai](https://github.com/alexrudall/ruby-openai)
* ollama-ai（后来发现，这个几乎也可以不用，只需要OpenAI兼容，基本上就行了）

其他的，基本上都得靠自己。

开源地址：[smart_prompt](https://github.com/zhuangbiaowei/smart_prompt)

## 第一部分： Smart Prompt

为啥要做一个`Smart Prompt`，而不是直接使用`ruby-openai`？因为我感觉原生的SDK不够灵活，我希望添加以下功能：

### 模板化的提示词

* 调用代码

```ruby
prompt :summarize, { text: params[:text] }
```

* summarize.erb

```erb
Please organize and output the results of the following request in a more complete and comprehensive manner:
<%= text %>
```

在使用提示词时，通过传入参数，能够调用一个`erb`模板文件，而在这个模板文件里，我们可以用上所有的ERB语法。

### 随意切换供应商

```ruby
use "deepseek"
model "deepseek-chat"
...
send_msg
...
model "deepseek-reasoner"
...
send_msg
...
use "SiliconFlow"
model "deepseek-ai/DeepSeek-V3"
...
send_msg
```

### 用DSL来写一个Worker

Ruby语言最好的地方，就是我们可以设计自己的DSL，所以我们可以用更加舒服的方式来写一个调用各种大模型，完成特定任务的`worker`。

```ruby
require "smart_prompt"

SmartPrompt.define_worker :smart_bot do
  use "SiliconFlow"
  model "Qwen/QwQ-32B"
  sys_msg "你是一个聪明的智能助手。"
  prompt :summarize, { text: params[:text] }
  send_msg
end

engine = SmartPrompt::Engine.new("./config/llm_config.yml")
result = engine.call_worker(:smart_bot, {text: "关于结构化的提示词，你有哪些好的建议？"})
puts result
```

当然，既然是DSL，我们还可以这么改写：

```ruby
require "smart_prompt"

SmartPrompt.define_worker :smart_bot do
  use params[:provider]
  model params[:model]
  sys_msg "你是一个聪明的智能助手。"
  prompt :summarize, { text: params[:text] }
  send_msg
end

engine = SmartPrompt::Engine.new("./config/config.yml")
result = engine.call_worker(:smart_bot, {text: "关于结构化的提示词，你有哪些好的建议？", provider: "deepseek", model: "deepseek-chat"})
puts result
result = engine.call_worker(:smart_bot, {text: "关于结构化的提示词，你有哪些好的建议？", provider: "SiliconFlow", model: "deepseek-ai/DeepSeek-V3"})
puts result
```

### 如何配置？

一看就懂的配置：`config.yml`

```yaml
adapters:
  openai: OpenAIAdapter
llms:
  SiliconFlow:
    adapter: openai
    url: https://api.siliconflow.cn/v1/
    api_key: ENV["APIKey"]
    default_model: Qwen/Qwen2.5-7B-Instruct
  ollama:
    adapter: openai
    url: http://localhost:11434/
    default_model: deepseek-r1
  deepseek:
    adapter: openai
    url: https://api.deepseek.com
    api_key: ENV["DSKEY"]
    default_model: deepseek-reasoner
logger_file: ./log/log.txt
worker_path: "./workers"
template_path: "./templates"
```

### 如何获取流式信息？

```ruby
require "smart_prompt"
engine = SmartPrompt::Engine.new("./config/config.yml")
engine.call_worker_by_stream(:smart_bot, { text: text }) do |chunk, _bytesize|
    if chunk.dig("choices", 0, "delta", "reasoning_content")
        puts "reasoning_content: " + chunk.dig("choices", 0, "delta", "reasoning_content")
    end
    if chunk.dig("choices", 0, "delta", "content")
        puts "content: " + chunk.dig("choices", 0, "delta", "content")
    end
end
```

### 如何保持多轮对话？如何重新开始？

```ruby
require "smart_prompt"
engine = SmartPrompt::Engine.new("./config/llm_config.yml")
result = engine.call_worker(:smart_bot, {text: "张聪明的父亲名叫张老实，张老实只有一个儿子。", with_history: true})
puts result
result = engine.call_worker(:smart_bot, {text: "张老实的儿子叫什么名字？", with_history: true})
puts result
```

```ruby
#清除对话历史
require "smart_prompt"
engine = SmartPrompt::Engine.new("./config/llm_config.yml")
engine.clear_history_messages
```

## 后续内容

* 用Ruby从头做一个AI Agent应用 -- Smart Agent （一个支持Function Calling与MCP的Agent框架）
* 用Ruby从头做一个AI Agent应用 -- RubyRich （一个纯Ruby编写的仿Python框架）
* 用Ruby从头做一个AI Agent应用 -- SmartResearch （一个真实、有用的研究助手）

#### 敬请期待