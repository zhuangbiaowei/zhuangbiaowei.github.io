---
layout: post
title: 在软件领域，所有的商业模式都与开源有关
date: 2023-04-04 17:19 +0800
tags: OpenSource Business
comments: true
---
最近开源社的公众号连续转发了几篇文章：《开源商业模式是个伪命题》[^1]、《开源商业模式是不是伪命题？》[^2]、《开源不是商业模式》[^3]。我也一时技痒，打算参与这个讨论。

我的立论，开宗明义第一句话就是：“**在软件领域，所有的商业模式都与开源有关**”。

## 什么是商业模式？

虽然有很多关于商业模式的讨论，但是究其本质，商业的考虑无非两部分：如何控制成本，如何赚取收益。最终达到的效果，是成本降低，收益提高，利润最大化。

从商业，到商业模式，其实就是一套可以被总结出来的“打法”。这样的办法，你可以用来控制成本，我学会了，也能用来控制成本。一种巧妙的推广手段，你可以低成本获客，我也可以用来低成本获客。

以下内容来自维基百科，《商业模式》九个要素的参考模型[^4]：

* 价值主张（Value Proposition）：即公司通过其产品和服务所能向消费者提供的价值。价值主张确认了公司对消费者的实用意义。
* 消费者目标群体（Target Customer Segments）：即公司所瞄准的消费者群体。这些群体具有某些共性，从而使公司能够（针对这些共性）创造价值。定义消费者群体的过程也被称为市场划分（Market Segmentation）。
* 分销渠道（Distribution Channels）：即公司用来接触消费者的各种途径。这里阐述了公司如何开拓市场。它涉及到公司的市场和分销策略。
* 客户关系（Customer Relationships）：即公司同其消费者群体之间所建立的联系。我们所说的客户关系管理（Customer Relationship Management）即与此相关。
* 价值配置（Value Configurations）：即资源和活动的配置。
* 核心能力（Core Capabilities）：即公司执行其商业模式所需的能力和资格。
* 合作伙伴网络（Partner Network）：即公司同其他公司之间为有效地提供价值并实现其商业化而形成的合作关系网络。这也描述了公司的商业联盟（Business Alliances）范围。
* 成本结构（Cost Structure）：即所使用的工具和方法的货币描述。
* 收入模型（Revenue Model）：即公司通过各种收入流（Revenue Flow）来创造财富的途径。

其实在我看来，最重要的就是最后两条：**成本结构与收入模型**。

## 软件领域的商业模式，为啥都与开源有关？

之前的几篇文章，因为忽略了**商业模式，不等于收入模型，还与成本结构有关**，所以才会争论来争论去。一旦考虑到成本结构，我就试问一句：现在还有哪个商业软件，不包含开源成分吗？

当然，这样的忽略，也并不是从以上几位作者开始的，我之前翻译的一篇维基百科上的词条《开源软件的商业模式》[^5]，也是在强调：通过采用各类商业模式，解决如何用开源软件赚钱的问题。

一旦我们同时考虑降低成本，扩大收益这两个目标，对于开源商业模式的讨论，格局就打开了。

## 使用开源与对外开源，到底有什么区别？

从成本的角度来看，我们最终商用的软件，其中总是会包含一定比例的开源成分。至于那个开源的成分，最初是人家开源，我们使用。还是我们先闭源开发，然后再开源出去。其实区别不大。

当然了，如果细细的分解，还是有些差别的。

* 对外开源
  * 社区运营成本
  * 开源安全成本
* 使用开源
  * 开源合规成本
  * 开源安全成本

在成本之外，还有一个区别是确实存在的：使用开源的情况下，要想掌控开源软件的发展方向，会相当困难。而在对外开源的情况下，相对会容易一些。当然，这本质上还是一个投入成本的问题：如果企业投入开源的成本，大于外部参与者投入的成本，又想借力，又想掌控，这就很困难了。

| 外部参与比例 | &nbsp;高&nbsp; | &nbsp;低&nbsp; |
| ---- | ---- | ---- |
| 成本 | 低 | 高 |
| 掌控力 | 弱 | 强 |
| 盈利潜力 | 低 | 高 |

## 开源的商业模式，其实质是什么？

在我的另一篇文章《什么是开源？》[^6]中，我提到了开源空间（Open Source Space）是一个边界封闭，内部开放的空间。现实世界的约束，商业规则的约束，就是这个开源空间的边界。

![商业模式示意图](/assets/img/oss-bm.png)

我们可以这么设想，在开源空间之中，Bit流动的阻力为0。也就是说，这个空间应该重新命名为自由开源空间（Free/Open Source Space）。在这个空间范围内，是赚不到钱的。这也就是为什么我们会觉得：开源商业模式是一个伪命题的原因。

但是，在这个空间的边界，我们可以设计一个合理的斜坡，从完全开放到完全封闭，从完全免费到各种收费策略。本质上就是利用封闭与开放之间的落差赚钱。

## 开源商业模式为啥步履维艰？

既然是一个斜坡，当然存在不同的斜率。作为自由开源空间的受益者，当然希望这个斜坡越缓越好。而一个商业企业，为了自身的生存，总得赚取足够的利润。这其中的利益博弈与话语权的博弈，礼物文化、奉献精神、用善行换取地位、用流量换来风投，总总纠缠，都是因此而起。

![商业模式示意图-2](/assets/img/oss-bm-2.png)

上图所示，是一个大概的开放状态与商业收益的关系。

* 闭门造车：在现在这个时代，还想所有的代码都自己从0开始写的公司，是不可能有利润的，软件都卖不出去
* 利润空间：随着开放程度的提高，成本降低，收益提高（因为开放性，使得获客成本，支撑成本，交易成本都不断下降）
* 活雷锋：太过于开放，以至于用户根本无需付费，就能用得很好了

从商业上来说，我们应该追求的，就是橘黄色箭头，指向的那个利润最高点！

## 总结

现在几乎所有的行业，都会转型成为软件企业。所有的软件企业，都必须思考开源相关的成本与利润（商业模式）问题。因此，开源商业模式，当然不是一个伪命题，而是一个需要“动态调整开源边界决策”的问题。

---

[^1]: [https://mp.weixin.qq.com/s/xrI-RDlr6DPs8ZBrqM9sdA](https://mp.weixin.qq.com/s/xrI-RDlr6DPs8ZBrqM9sdA)
[^2]: [https://mp.weixin.qq.com/s/P_GjDvRhZoncBmGW0RTRvA](https://mp.weixin.qq.com/s/P_GjDvRhZoncBmGW0RTRvA)
[^3]: [https://mp.weixin.qq.com/s/gBIIZfdDZe1gW5w7kPM1kw](https://mp.weixin.qq.com/s/gBIIZfdDZe1gW5w7kPM1kw)
[^4]: [https://zh.wikipedia.org/wiki/%E5%95%86%E4%B8%9A%E6%A8%A1%E5%BC%8F](https://zh.wikipedia.org/wiki/%E5%95%86%E4%B8%9A%E6%A8%A1%E5%BC%8F)
[^5]: [开源软件的商业模式](/opensource/business/2022/03/13/business-models-for-open-source-software.html)
[^6]: [什么是开源？](/2023/03/30/what-is-open-source.html)
