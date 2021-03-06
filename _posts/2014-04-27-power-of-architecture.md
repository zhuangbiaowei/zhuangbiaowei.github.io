﻿---
layout: post
title:  "架构的力量"
date:   2014-04-27 12:01
categories: Thinking IT
---

<a href="http://book.douban.com/subject/20445258/"><img src="https://img9.doubanio.com/view/subject/s/public/s24642460.jpg" style="width:30%;"></a>

<a href="http://book.douban.com/subject/1186899/"><img src="https://img9.doubanio.com/view/subject/s/public/s1218861.jpg" style="width:30%;"></a>

最近看了两本书，这两本书当然大有不同，一本书专注于分析软件设计，尤其是架构设计的书；而另一本则是在分析互联网领域的法律与创新的关系问题。

两本都是好书，都值得分别为他们写一篇读书心得，只是这里想谈谈的是两本书中，相通的部分——「架构的力量」。

- 端对端原则

在《思想的未来》中，作者回顾了互联网的架构设计思想：
「这一原则是由网络设计者Jerome Saltzer、David Clark、David P.Reed在1981年首次提出的，被称为端对端(end-to-end argument, e2e)，用以指导网络设计者们开发网络协议及应用程序。」
「端对端原则认为，网络的智能不应当放在网络内，而应当位于网络的端点，即网络内的计算机只是履行应用程序所需的基本功能，而一些特殊功能应由网络边缘的计算机来实现。」
「据RFC 1958所述，虽然因特网社区中许多成员会认为因特网不存在架构，但是，社区成员普遍相信，因特网的目标是连通性，工具是因特网协议，智能位于端对端而不是隐藏与网络之中。网络的任务是尽可能灵活有效地传输数据包，而其他的一切都应该靠边站。」

由这样的架构原则，作者总结出了三个要点：「应用程序在网络边缘的计算机上执行，任何种类的应用都可以立即被运行；网络没有为任何特定应用程序做优化设计，对于任何创新都是开放的；由于网络平台的中立性，网络无法做到歧视某种特定的新设计。」

**在我看来：互联网最初的设计者，因为足够谦逊，所以对于「平台将会如何被使用」未做任何假设，他们的架构仅仅专注于最为简单的目标，而这也是互联网取得如今这样巨大成就的根本原因。**

- 不要尝试预测未来

在《简洁之美》中，作者极力向读者阐述：架构设计简洁的价值，因为随着时间的不断增长，软件的研发成本的绝大部分，会产生于后期维护的阶段。越是简洁的架构，就越是能够为今后的维护，节约大笔费用。

另外一个值得注意的事实是：「程序员犯的最常见也是最严重的错误，就是在其实不知道未来的时候，去预测未来。」

而作者给出的策略是：「最安全的情况是，完全不尝试预测未来，所有的设计决策都应当根据当前确切知道的信息来做。」

**在我看来，当年的互联网设计者，就是那种最伟大的程序员/设计师，他们未做任何假设，仅仅专注于解决信息传输的需求。**

- 一个可能的误区

不去尝试预测未来，根据当前确切知道的信息来做。这样的逻辑，可能会让人偷懒。
1. 「啊，我们这就开始干吧！」
2. 「我们不要做太多的假设！(不必想那些设计的事情)」

**架构是存在的，设计是需要的，需求要尽可能的去搜集与分析。在做到这三个要点之后，才能谈及「不要假设」，「不要过度设计」。在此之前，还是不要放松为好。**

**架构是有力量的，简洁的架构，往往会产生的惊人的力量。当然，「无架构设计」不在其列。**