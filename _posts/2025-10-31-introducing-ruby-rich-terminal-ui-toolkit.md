---
layout: post
title: SmartResearch的底座 -- RubyRich （纯Ruby编写的终端UI工具包）
date: 2025-10-31 10:00 +0800
tags: OpenSource Ruby AI Agent TUI Terminal
comments: true
---

在前三篇文章中，我们介绍了[Smart Prompt](/2025/04/06/making-an-ai-app-from-scratch-with-ruby-1.html)、[Smart Agent](/2025/04/23/making-an-ai-app-from-scratch-with-ruby-2.html)和[SmartResearch](/2025/10/31/making-an-ai-app-from-scratch-with-ruby-3.html)这三个AI应用组件。今天，我们要深入探讨支撑这些应用的核心基础设施——**RubyRich**，一个纯Ruby编写的终端用户界面（TUI）工具包。

开源地址：[ruby_rich](https://github.com/zhuangbiaowei/ruby_rich)

## 什么是RubyRich？

RubyRich是一个受Python [Rich](https://github.com/Textualize/rich)库启发的Ruby终端UI工具包，它提供了优雅的格式化、高级布局和专业级的终端输出能力。在Ruby的LLM生态"一穷二白"的背景下，RubyRich填补了终端界面开发的空白。

### 为什么需要RubyRich？

在构建SmartResearch这样的AI应用时，我们面临一个关键问题：**如何为用户提供直观、美观的交互界面？** 传统的命令行界面过于简陋，而Web界面又过于复杂。TUI（终端用户界面）成为了完美的解决方案，但Ruby生态中缺乏成熟的TUI库。

这就是RubyRich诞生的原因——为Ruby开发者提供构建专业级终端应用的工具。

## 核心特性

### 🎨 丰富的标记语言

RubyRich提供直观的`[bold red]text[/bold red]`语法，让文本格式化变得简单优雅：

```ruby
require 'ruby_rich'

# 基础颜色和样式
puts RubyRich::RichText.markup("[red]错误信息[/red]")
puts RubyRich::RichText.markup("[bold]重要文本[/bold]")
puts RubyRich::RichText.markup("[italic blue]样式文本[/italic blue]")

# 组合样式
puts RubyRich::RichText.markup("[bold red]严重警告！[/bold red]")
```

### 🖥️ 语法高亮

内置支持200+编程语言的语法高亮：

```ruby
# 自动语言检测
puts RubyRich.syntax("def hello; puts 'world'; end")

# 显式指定语言
python_code = "def fibonacci(n):\n    return n if n <= 1 else fibonacci(n-1) + fibonacci(n-2)"
puts RubyRich.syntax(python_code, 'python')
```

### 📄 Markdown渲染

完整的Markdown支持，针对终端输出进行优化：

```ruby
markdown_text = <<~MARKDOWN
# 项目文档

## 特性
- **富文本格式化**
- *语法高亮*
- `代码块`

### 代码示例
```ruby
puts "Hello, Ruby Rich!"
```

> 这是一个引用块

[访问我们的网站](https://example.com)
MARKDOWN

puts RubyRich.markdown(markdown_text)
```

### 🌳 树形结构显示

美观的层次化数据可视化：

```ruby
# 手动构建树
树 = RubyRich.tree("我的项目")
源码 = 树.add("src")
源码.add("main.rb")
源码.add("utils.rb")
树.add("README.md")

# 从文件路径构建
路径 = ["app/models/user.rb", "app/views/users/index.html", "config/routes.rb"]
文件树 = RubyRich::Tree.from_paths(路径, "Rails应用")
```

### 📊 增强表格

自动扩展的表格，支持丰富的格式化：

```ruby
# 表格中的富内容
table = RubyRich::Table.new(headers: ["功能", "状态", "备注"])
table.add_row([
  RubyRich::RichText.markup("[cyan]语法高亮[/cyan]"),
  RubyRich::RichText.markup("[green]✅ 完成[/green]"),
  "支持200+语言"
])
table.add_row([
  RubyRich::RichText.markup("[cyan]Markdown渲染[/cyan]"),
  RubyRich::RichText.markup("[yellow]🚧 测试版[/yellow]"),
  "完整CommonMark支持"
])

puts table.render
```

### 🧩 面板布局

创建嵌套布局，支持边框和样式：

```ruby
# 创建面板布局
layout = RubyRich::Layout.new(width: 80, height: 20)

# 添加面板
header = layout.add_panel("header", width: 80, height: 3, position: :top)
content = layout.add_panel("content", width: 60, height: 15, position: :left)
sidebar = layout.add_panel("sidebar", width: 20, height: 15, position: :right)
footer = layout.add_panel("footer", width: 80, height: 2, position: :bottom)

# 设置面板内容
header.content = "RubyRich - 终端UI工具包"
content.content = "这里是主要内容区域..."
sidebar.content = "这里是侧边栏..."
footer.content = "底部信息"

puts layout.render
```

### 📋 多列布局

专业的报纸风格列格式化：

```ruby
layout = RubyRich.columns(total_width: 80)

# 添加不同配置的列
左列 = layout.add_column(title: "新闻", align: :left)
右列 = layout.add_column(title: "更新", align: :right)

左列.add("突发：Ruby Rich 2.0发布！")
左列.add("新功能包括高级布局")
右列.add("性能提升300%")
右列.add("内存使用减少50%")

puts layout.render(show_headers: true, show_borders: true)
```

### 🚦 状态指示器

全面的状态符号和进度跟踪：

```ruby
# 基础状态指示器
puts RubyRich.status(:success)     # ✅ 成功
puts RubyRich.status(:error)       # ❌ 错误
puts RubyRich.status(:warning)     # ⚠️ 警告
puts RubyRich.status(:info)        # ℹ️ 信息

# 系统状态
puts RubyRich.status(:online)      # 🟢 在线
puts RubyRich.status(:offline)     # 🔴 离线
puts RubyRich.status(:maintenance) # 🔧 维护

# 状态面板
board = RubyRich::Status::StatusBoard.new(width: 50)
board.add_item("Web服务器", :online, description: "Nginx运行在80端口")
board.add_item("数据库", :warning, description: "高连接数")
board.add_item("缓存", :error, description: "Redis连接失败")
puts board.render
```

### 📈 高级进度条

多种样式、ETA、速率计算和多进度支持：

```ruby
# 带细节的基础进度条
bar = RubyRich::ProgressBar.new(
  1000,
  width: 40,
  title: "处理中",
  show_percentage: true,
  show_rate: true,
  show_eta: true
)

bar.start
1000.times { |i| bar.advance(1); sleep(0.01) }
bar.finish(message: "✅ 处理完成！")

# 不同样式
styles = [:default, :blocks, :arrows, :dots, :line]
styles.each do |style|
  bar = RubyRich::ProgressBar.new(50, style: style, title: style.to_s)
  # ... 进度 ...
end

# 多个进度条
multi = RubyRich::ProgressBar::MultiProgress.new
bar1 = multi.add("文件1", 100)
bar2 = multi.add("文件2", 100)
bar3 = multi.add("文件3", 100)
multi.start
# ... 分别更新进度条 ...
multi.finish_all
```

## 在SmartResearch中的应用

在SmartResearch中，RubyRich扮演了至关重要的角色：

### F2模式 - 交流与探索

```ruby
# 在F2模式下显示AI思考过程
agent.on_reasoning do |reasoning_content|
  print reasoning_content.dig("choices", 0, "delta", "reasoning_content")
  print "\n" if reasoning_content.dig("choices", 0, "finish_reason") == "stop"
end

agent.on_content do |content|
  print content.dig("choices", 0, "delta", "content")
  print "\n" if content.dig("choices", 0, "finish_reason") == "stop"
end
```

### F3模式 - 知识库管理

使用RubyRich的表格和树形结构来显示文档列表、标签系统和搜索结果：

```ruby
# 显示研究主题列表
table = RubyRich::Table.new(headers: ["ID", "主题", "文档数", "创建时间"])
ResearchTopic.all.each do |topic|
  table.add_row([
    topic.id,
    topic.name,
    topic.source_documents.count,
    topic.created_at.strftime("%Y-%m-%d")
  ])
end
puts table.render
```

### F4模式 - 文章创作

使用多列布局来显示大纲和写作进度：

```ruby
# 显示文章大纲
layout = RubyRich.columns(total_width: 80)
outline_col = layout.add_column(title: "大纲", align: :left)
progress_col = layout.add_column(title: "进度", align: :right)

outline_data.each do |section|
  outline_col.add("#{section.level}. #{section.title}")
  progress_col.add("#{section.progress}% 完成")
end

puts layout.render
```

## 技术架构

### 依赖库

RubyRich建立在几个优秀的Ruby库之上：

- **rouge** - 语法高亮引擎
- **tty-cursor** - 终端光标控制
- **tty-screen** - 终端屏幕信息
- **redcarpet** - Markdown解析
- **unicode-display_width** - Unicode字符宽度计算

### 模块设计

RubyRich采用模块化设计，每个功能都有独立的模块：

```
lib/ruby_rich/
├── ansi_code.rb      # ANSI转义码处理
├── columns.rb        # 多列布局
├── console.rb        # 控制台主类
├── dialog.rb         # 对话框
├── layout.rb         # 布局系统
├── live.rb           # 实时更新
├── markdown.rb       # Markdown渲染
├── panel.rb          # 面板组件
├── print.rb          # 打印工具
├── progress_bar.rb   # 进度条
├── status.rb         # 状态指示器
├── syntax.rb         # 语法高亮
├── table.rb          # 表格
├── text.rb           # 富文本
├── tree.rb           # 树形结构
└── version.rb        # 版本信息
```

## 性能优化

RubyRich针对性能进行了优化：

- **快速处理** - 每秒处理10,000+标记元素
- **高效渲染** - 毫秒级渲染大型表格（1000+行）
- **内存优化** - 高效的对象管理，内存占用小
- **线程安全** - 支持并发操作

## 安装和使用

### 安装

添加到Gemfile：
```ruby
gem 'ruby_rich'
```

或直接安装：
```bash
gem install ruby_rich
```

### 快速开始

```ruby
require 'ruby_rich'

# 富文本标记语言
puts RubyRich::RichText.markup("[bold green]成功！[/bold green] 任务完成。")

# 语法高亮
code = "def hello\n  puts 'world'\nend"
puts RubyRich.syntax(code, 'ruby')

# Markdown渲染
markdown = "# 标题\n\n这是**粗体**文本。"
puts RubyRich.markdown(markdown)

# 树形结构
tree = RubyRich.tree("项目")
tree.add("src").add("main.rb")
tree.add("README.md")
puts tree.render

# 状态指示器
puts RubyRich.status(:success, text: "所有系统运行正常")
puts RubyRich.status(:warning, text: "检测到高内存使用")

# 增强进度条
RubyRich::ProgressBar.with_progress(100, title: "处理中", show_rate: true) do |bar|
  100.times { |i| bar.advance(1); sleep(0.01) }
end
```

## 主题和自定义

RubyRich支持完全的自定义：

```ruby
# 自定义主题设置
RubyRich::RichText.set_theme({
  primary: { color: :blue, bold: true },
  secondary: { color: :cyan },
  accent: { color: :yellow, bold: true }
})

# 使用主题样式
text = RubyRich::RichText.new("重要消息", style: :primary)
puts text.render

# 自定义进度条样式
RubyRich::ProgressBar::STYLES[:custom] = {
  filled: '▓', empty: '░', prefix: '⟨', suffix: '⟩'
}
```

## 在AI生态中的价值

RubyRich不仅仅是一个TUI工具包，它在Ruby的AI生态中扮演着关键角色：

### 填补生态空白

在Python生态中，有Rich、Textual等成熟的TUI库，而Ruby生态中一直缺乏类似工具。RubyRich填补了这一空白，让Ruby开发者能够构建专业的终端AI应用。

### 提升用户体验

通过美观的界面、实时更新和丰富的交互元素，RubyRich显著提升了AI应用的用户体验。用户不再需要面对枯燥的命令行输出，而是可以享受流畅、直观的交互过程。

### 促进AI应用开发

有了RubyRich，开发者可以更专注于AI算法的实现，而不需要花费大量时间在界面开发上。这大大降低了构建复杂AI应用的门槛。

## 实际应用案例

### SmartResearch

如前所述，SmartResearch是RubyRich最典型的应用案例。它展示了如何用RubyRich构建一个功能完整的AI研究助手：

- **三模式界面** - F2交流、F3知识库、F4创作
- **实时显示** - AI思考过程、工具调用、搜索结果
- **数据可视化** - 文档树、状态面板、进度跟踪

### 其他潜在应用

RubyRich还可以用于：

- **AI对话系统** - 构建类似ChatGPT的终端界面
- **数据监控面板** - 实时显示系统状态和指标
- **开发工具** - 代码审查、测试报告、部署监控
- **教育应用** - 交互式学习工具

## 结语

RubyRich代表了Ruby在AI领域的一个重要里程碑。它证明了：

1. **Ruby可以构建专业的TUI应用** - 不逊色于Python生态
2. **优雅的DSL设计** - Ruby的元编程能力让代码更简洁
3. **完整的组件系统** - 从基础文本到复杂布局的全覆盖
4. **实际应用价值** - 已经在SmartResearch等项目中验证

通过RubyRich，我们看到了Ruby在AI领域的巨大潜力。它不仅仅是"能用"，而是能够构建出**美观、高效、专业**的AI应用。

随着Ruby生态的不断完善，我们有理由相信，Ruby将在AI领域占据一席之地。而RubyRich，正是这一征程中的重要基石。

---

*欢迎参与RubyRich的开发，共同推动Ruby在AI领域的发展！*

**相关链接：**
- [SmartResearch项目](https://github.com/zhuangbiaowei/SmartResearch)
- [SmartAgent框架](https://github.com/zhuangbiaowei/smart_agent)
- [SmartPrompt引擎](https://github.com/zhuangbiaowei/smart_prompt)