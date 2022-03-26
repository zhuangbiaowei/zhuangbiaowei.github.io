---
layout: post
title: 【翻译】开源的“抗议软件”伤害了开源
date: 2022-03-26 16:09 +0800
categories: OpenSource Protestware
comments: true
---

翻译来源：[Open source ‘protestware’ harms Open Source 2022-03-24 05:31](https://opensource.org/blog/open-source-protestware-harms-open-source)

作者：[smaffulli](https://opensource.org/blog/82319)

本周是普京对乌克兰的战争开始后的第一个月。我们当时就表明了 [OSI 的立场](https://opensource.org/newsletter/OSI-mar-2022) —— OSI 谴责俄罗斯军队在普京的指挥下对乌克兰的攻击，但有一个新的发展，直接影响到开源社区，它需要一个新的评论。

新的进展是，愤怒的维护者已经开始向少数开放源码库添加代码，以抗议战争。当部署时，这种“[抗议软件](https://www.technologyreview.com/2022/03/21/1047489/activists-are-targeting-russians-with-open-source-protestware)”表达了维护者对俄罗斯政府入侵乌克兰的反对。大多数抗议软件在运行时只是显示反战或支持乌克兰的信息。这是一种非暴力的、创造性的抗议形式，可能是有效的。

但是，至少在一个案例中 —— node-ipc 包中的 peacenotwar 模块 —— 这个更新破坏了 npm 开发者的代码，旨在抹去存储在俄罗斯和白俄罗斯的数据。在 3 月 16 日关于恶意代码的[博文](https://snyk.io/blog/peacenotwar-malicious-npm-node-ipc-package-vulnerability/)中，Snyk 公司的 Liran Tal 说："这一安全事件涉及一个维护者破坏磁盘上的文件的破坏性行为，以及他们试图以不同形式隐藏和重述这种蓄意破坏行为"。

Gerald Benischke 在 3 月 16 日的[博文](https://beny23.github.io/posts/on_weaponisation_of_open_source/)中所说的“开源武器化”是不分青红皂白的，它造成的**附带损害**损害了开发者和运营商的工作，仅仅是因为他们有一个俄罗斯分配的 IP 地址。它对和平缔造者和战争贩子的伤害一样大 —— 即使是使用 VPN 来反对入侵的道德黑客也可能遭受附带损害。

可以理解的是，这已经引起了愤怒。我们也有这种愤怒。抗议是言论自由的一个重要因素，应该得到保护。开放性和包容性是开源文化的基石，而开源社区的工具是为全球访问和参与而设计的。总的来说，开源文化和工具 —— 问题追踪、信息传递系统、资源库 —— 提供了一个独特的信号渠道，可以绕过暴君为掌握权力而施加的审查制度。

与其说是恶意软件，不如说是利用提交日志中的信息来发送反宣传信息，并发布追踪器，在俄罗斯境内分享乌克兰在俄罗斯军队手中真正发生的事情的准确消息，这是两种明显的可能性。开源社区有很多渠道可以发挥创意，而不会伤害到每个碰巧加载更新的人。

我们鼓励社区成员以创新和明智的方式利用开源的自由和工具，让俄罗斯公民了解强加给乌克兰公民的现实伤害，并支持乌克兰境内的、以及支持乌克兰的人道主义和救济工作。

从长远来看，这种武器化很可能就像是向风中吐痰。破坏开源项目的坏处远远超过任何可能的好处，而且这种反作用力最终会损害负责的项目和贡献者。推而广之，所有的开放源码都会受到伤害。使用你的权力，是的，但要明智地使用它。