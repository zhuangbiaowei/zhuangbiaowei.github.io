---
layout: post
title: "Markdown.World 项目规划"
date: 2023-01-24 12:30 +0800
tags: OpenSource KnowledgeEngineering Markdown
comments: true
---

在 [上一篇文章](/2022/12/18/open-source-knowledge-engineering-for-emerging-areas.html) 中，我提到了自己在做的一些工作。后来又买了一个域名： [markdown.world](https://markdown.world)。

因此，想在这篇文章里，较为系统的阐述一下，这个项目的整体规划。

![](https://www.markdown.world/images/all_markdown_world.png)

## 一、围绕 Markdown 的整体架构

```
+-------------+   +-----------+   +---------------+   +----------------+
|  Markdown   |   |           |   |               |   |                |
|    File     +-->| Generator +-->+   HTML Site   +-->|  GitHub Pages  |
|    Tree     |   |           |   |               |   |                |
+-------------+   +-----------+   +---------------+   +----------------+
                        |                                      ^
                        |         +---------------+            |
                        +-------->|     Slide     |------------+
                        |         +---------------+
                        |
                        |         +--------------+
                        +-------->|   PDF/ePub   |
                                  +--------------+
```

### 1. Markdown 可以包含的各种内容类型

1. 基于 Obsidian 或 Logseq 等工具，创作的知识库
2. 基于 GitBook 或 MDBook 等工具，创作的书籍
3. 基于 Jekyll 或 Hugo 等工具，创作的博客
4. 其他主要基于 Markdown 格式的内容

### 2. Markdown 已经支持的各种扩展格式

1. 原生 Markdown 的基础格式： [https://daringfireball.net/projects/markdown/syntax](https://daringfireball.net/projects/markdown/syntax)
2. Github 扩展的格式： [GitHub Flavored Markdown Spec](https://github.github.com/gfm/)
3. 各种流程图工具 [mermaid](https://mermaid-js.github.io/mermaid/#/) 或 [flowcharts](http://flowchart.js.org/)
4. 数学公式 [MathJAX](https://www.mathjax.org/)
5. 基于``[[]]``的双向链接
6. 基于``(())``的站内引用

### 3. Markdown.World 计划支持的扩展格式

1. 将``(())``扩展为跨站引用
2. 可视化图表 [Apache ECharts](https://echarts.apache.org/zh/index.html)
3. TODO 列表
4. CodeRunner or CodePen
5. Manim

## 二、Generator 的内部架构

```
+--------+          +---------------+                                +---------------+
| Source |          |               |                                |               |
|   +    | -------> |  Load Config  |  --------------------------->  |  Render Site  |
| Config |          |               |                                |               |
+--------+          +-----------+---+                                +--A------------+
                                |                                       |
                          +-----V--------+                     +--------+------+
                          |              |                     |               |
                         /| Parse Source |                     |  Render Page  |
                        / |              |                     |               |
                       /  +------------+-+                     +--A------------+
                      /                |                          |
                     /                 |                          |
     +--------------V----+        +----V-----------+    +---------+------+
     |                   |        |                |    |                |
     |  Knowladge Graph  |        | Parse Markdown +--->| Render Element |
     |                   |        |                |    |                |
     +-------------------+        +----------------+    +----------------+
```

### 1. 基于 TOML 格式的配置文件

这个是受 mdbook 项目的启发，后来我也去了解了一下 [TOML](https://toml.io/en/) 格式，发现非常舒服，就应用在了更多地方。

* book.toml
* wiki.toml
* logseq.toml
* obsidian.toml
* blog.toml
* *.toml

各种配置文件，都大同小异，用于特定类型的站点输出配制。

### 2. 解析源文件

基于配制文件对于源文件的描述，解析源文件主要有两个方面的工作：

* 解析``[[]]``双向链接，建立知识图谱的数据集
* 解析每一个 Markdown 文件的头部元数据，获得 Metadata

### 3. 解析 Markdown 文件，并渲染各种扩展元素

基于配制文件的定义，从 Markdown 中解析出各种扩展元素，并分别渲染，例如上文 1.2、1.3 两节所提及的各种格式。

具体的渲染，有两种选择，可以是服务器端渲染，例如各种 Markdown 格式与扩展的 Markdown 格式。

也可以是浏览器渲染，例如 MathJAX 就是通过一个 JS 文件，在前端实时渲染的。

### 4. 基于模板，生成整个网站，或其他格式

这个我参考了 Jekyll 的用法，用上了 [Liquid](https://github.com/Shopify/liquid) 这样的模板引擎，感觉还是比较方便的。

## 三、项目规划

### 1. [markdown_site](https://github.com/markdown-world/markdown_site)

这是一个解读并生成整个基于 markdown 的站点的 gem 包，它依赖另一个 gem 包：markdown_extension

### 2. [markdown_extension](https://github.com/markdown-world/markdown_extension)

这是一个接续各种扩展的 markdown 文件的，并渲染生成的 gem 包。

### 3. 各种特定类型的模板项目

* [Logseq2Pages](https://github.com/markdown-world/Logseq2Pages)
    * 这是一个将 Logseq 的源文件，解析并生成静态网站的模板
* [wiki.md](https://github.com/markdown-world/wiki.md)
    * 如名称所示，这是一个 wiki，而且计划支持多语言
* [oss-book](https://github.com/kaiyuanshe/oss-book)
    * 这个目前还是基于 mdbook 所做的扩展，今后会统一到 markdown.world 之内
* [blog](https://github.com/markdown-world/blog)
    * 这个目前还只有规划，后续会扩展成一个 Blog 的模板，但是应该不会发展到与 Jekyll 或者 Hugo 竞争的复杂程度，主要是为了演示基于 Markdown 写作的各种可能性
* vscode-extension
    * 这个项目还没有开始，计划是做一个插件，方便在基于 Markdown 写作的过程中，引用其他 Markdown 站点的最新内容

## 总结

想法太多，精力、能力都不太够，只能慢慢做，也欢迎大家加入。