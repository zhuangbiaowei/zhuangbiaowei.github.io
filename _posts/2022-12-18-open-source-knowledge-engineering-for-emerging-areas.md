---
layout: post
title: 面向新兴领域的开源知识工程
date: 2022-12-18 10:21 +0800
tags: OpenSource KnowledgeEngineering
comments: true
---

## 从知识工程到知识图谱

根据《知识图谱标准化白皮书（2019）》介绍，知识工程相关的发展经历了以下几个阶段：

* 1955 年——1977 年，起源阶段
    * 引文网络分析开始成为一种研究当代科学发展脉络的常用方法
* 1977 年——2012 年，发展阶段
    * 1977 年，B.A. Feigenbaum 提出知识工程的概念
    * 1991 年，Niches 提出知识本体的概念
    * 1998 年，Tim Berners-Lee 提出语义网
    * 2022 年，机构知识库的概念被提出
* 2012 年——至今，繁荣阶段
    * 2012 年，谷歌提出 Google Knowledge Graph

在我想要构建**开源知识图谱**的过程中，学习了以上的这些信息，然后发现：不太适用。

## 新兴领域的知识工程

现代的知识图谱，追求的是在海量数据中，抽取概念、关系与各种属性，然后再将其表示出来。而对于像开源这样的领域，我们首先需要的是：协作建设。

而且，是以众包的方式，协作建设。当然，无论是 Wikipedia 还是 Wikidata，都是众包协作的典范，但是经过考察之后，我依然觉得，还是得自己打造一套知识工程所需的基础设施，然后再开始我想要的各种“建设”。

### 新兴领域知识工程的需求

* All Markdown
    * 支持 echarts
    * 支持 MetaData
    * 支持 [GFM](https://github.github.com/gfm/)
    * 支持 [MathJax](https://www.mathjax.org/)
    * 支持代码高亮
* 引用
    * [[]] 方式链接站内词条
    * (()) 方式引用站外信息
* 支持词条 -> 文章 -> 书籍 -> Slide 的展示
* All Hosting GitHub
    * 使用 GitHub Pages
    * 使用 Github Actions
    * 通过 Pull Request 协作

## 目前的成果

* [https://github.com/kaiyuanshe/oss-book](https://github.com/kaiyuanshe/oss-book)
    * 演示页面：[https://kaiyuanshe.cn/oss-book/](https://kaiyuanshe.cn/oss-book/)
    * 这是一本开源书籍，基于 [rust mdbook](https://github.com/rust-lang/mdBook)
    * 添加了一个 [mdbook-echarts](https://github.com/zhuangbiaowei/mdbook-echarts) 插件，可以集成 echarts
    * 添加了一个 citation.rb，可以引入其他 git 仓库里的 Markdown 内容
    * 集成了 [reveal.js](https://revealjs.com/)，可以直接在浏览器里演示
* [https://github.com/zhuangbiaowei/wiki.md](https://github.com/zhuangbiaowei/wiki.md)
    * 演示页面：[https://zhuangbiaowei.github.io/wiki.md/](https://zhuangbiaowei.github.io/wiki.md/)
    * 这是一个纯粹用 Markdown 格式渲染得到的 wiki
    * 支持 summary，以及 toml 格式的 metadata
* [https://kaiyuanshe.cn/oss-book/test.html](https://kaiyuanshe.cn/oss-book/test.html)
    * 这个是演示的关键，可以查看 [test.md](https://github.com/kaiyuanshe/oss-book/blob/main/src/test.md?plain=1)
    * ```((zbw:src/summary:5))``` 代表着引用 zbw 这个仓库的```src/summery.md```文件中的第 5 行，还可以引用整个文件，也可以引用从a到b的每一行
    * 在 [book.toml](https://github.com/kaiyuanshe/oss-book/blob/main/book.toml) 中，配置了可以被引用的仓库
    * 点击演示页面的引用，可以跳转回到实际的 markdown 文件，以及相应的行

## 后续工作

随着开源知识库与书籍的编写过程不断推进，我也会不断的改建这些基础设施，欢迎大家参与一起来开发。