---
layout: post
title:  "试译：开源项目成功的十条准则"
date:   2015-10-06 22:00
categories: Thinking IT
tags: OpenSource
---

原文：[Ten Rules for Open Source Success](http://hintjens.com/blog:95)

## 《开源项目成功的十条准则》

**Everyone wants it, lots of people try it, yet doing it is mostly painful and irritating. I’m speaking about free software aka open source. Today I’m going to summarize 30 years of coding experience in ten management-proof bullet points.**

**每个人都想去做，也有很多人跃跃欲试，但是真做起来却常常会令人痛苦和愤怒——我说的是自由软件，或者更宽泛一些的开源软件。今天我要将自己30年来的开发经验，总结为开源软件的十条成功法则。**

    庄表伟：每个人都需要它，很多人跃跃欲试，但是干起来却往往会令人痛苦或者愤怒。
    我在谈论的是自由软件（开源软件）。
    今天，以我30年来的开发经验，我想要总结以下10条经营要点：

    余晟：每个人都想去做开源，也有很多人尝试了，但是真正去做却常常收获痛苦和恼怒。
    我所说的这回事是自由软件，或者叫开源软件。
    今天我要总结自己30年来的开发经验，归纳为十条经得起实践检验的准则。

    魏永明：所有人需要它，很多人尝试它，但做起来却常常是痛苦的甚至会令人不快——
    我说的是自由软件，或者更宽泛一些的开源软件。
    今天，我将把本人三十年的编码经验总结为开源软件的十条成功法则。

    八刀：今天我将把我三十年的开发经验囊括在以下十点。

**1、People Before Code**

**1、人比代码重要**

**This is the Golden Rule, taught to me by Isabel Drost-Fromm. Build community, not software. Without community your code will solve the wrong problems. It will be abandoned, ignored, and will die. Collect people and give them space to work together. Give them good challenges. Stop writing code yourself.**

**这是一条黄金法则，是Isabel Drost-Fromm【注1】教给我的。我们要建立的是社区而不是软件。没有社区，你的代码就会用来解决错误的问题。然后这些代码会被抛弃、忽略，最后死去。正确的做法是把人集结起来，给他们协同工作的空间，给他们充分的挑战。切记不要亲手来写代码！**

注1：Isabel Drost-Fromm是Apache软件基金会的成员，Apache Mahout的创立者之一。

    庄表伟：这是一条黄金法则，是Isabel Drost-Fromm教给我的。
    建立社区而非软件，没有社区，你的代码将会去解决错误的问题。
    然后它将会被抛弃、忽略，最后死去。将人汇集起来，给他协同工作的空间，
    给他们足够好的挑战，停止自己写代码！

    余晟：这是金科玉律，是Isabel Drost-Fromm教给我。
    我们要建立的是社区而不是软件。没有社区，你的代码就会用来解决错误的问题。
    然后这些代码会被抛弃、忽略，最后死去。正确的做法是把人集结起来，给他们协同工作的空间，
    给他们充分的挑战。切记不要亲手来写代码！

    Holm：..他们足够好的挑战，停止自己写代码！断句有问题，读起来像“让他们停写”

**2、Use a Share-Alike License**

**2、使用“以相同方式共享”的许可证**

    庄表伟：2、使用‘以相同方式共享’型许可证

    余晟：2、使用‘以相同方式共享’的许可证

**Share-alike is the seat belt of open source. You can boast about how you don’t need it, until you have a bad accident. Then you will either find your face smeared on the wall, or have light bruising. Don’t become a smear. Use share-alike. If GPL/LGPL is too political for you, use MPLv2.**

**“以相同方式共享”是开源的安全带。在遇到严重的事故之前，你大可吹嘘自己完全不需要它。一旦出现事故，你就会发现自己满脸污垢，或者‘轻微擦伤’，不要成为一个“伤员”。使用“以相同方式共享”的许可证吧，如果你觉得GPL/LGPL太过于政治化，那就用MPLv2。**

    庄表伟：‘以相同方式共享’是开源的安全带，你可以吹嘘自己是如何的不需要它，直到你碰到糟糕的‘意外’。
    然后你会发现自己头撞南墙，或者‘轻微擦伤’，不要成为一个‘伤员’。
    用‘以相同方式共享’型许可证吧，
    如果你觉得GPL/LGPL太过于政治化，那就用MPLv2。

    余晟：‘以相同方式共享’是开源的安全带。在遇到严重的事故之前，你大可吹嘘自己完全不需要它。
    一旦出现事故，你就会发现自己满脸污垢，或者还有轻微擦伤。你应当避免把自己搞砸，
    你应该使用‘以相同方式共享’的许可证吧。
    如果觉得GPL/LGPL太过于政治化，那就用MPLv2。

**3、Use an Zero-Consensus Process**

**3、使用一个无需达成共识的协作流程**

    八刀：零共识

**Seeking upfront consensus is like waiting for the ideal life partner. It is kind of crazy. Github killed upfront consensus with their fork/pull-request flow, so you’ve no excuse in 2015. Accept patches like Wikipedia accepts edits. Merge first, fix later, and discuss out of band. Do all work on master. Don’t make people wait. You’ll get consensus, after the fact.**

**寻求事前的共识就像是在等待理想的人生伴侣，这简直就是疯狂。借助fork/pull-request这种模式，Github已经干掉了事前共识，所以在2015年的今天你没有任何借口坚持事前共识。你应当像维基百科那样接受修改。先合并，再修复，同时单独讨论。所有工作应当在master分支上进行，不应当让大家等待。有了既成事实，共识会随之而来。**

    庄表伟：寻求前期的共识就像是在等待理想的人生伴侣，这简直就是疯狂。
    借助fork/pull-request这种模式，Github已经干掉了前期共识，
    所以在2015年的今天，你没有任何借口。例如像维基百科那样接受修改。
    先合并，再修复，然后附带进行讨论。在master分支上做所有的工作，不要让人等待。
    事实上，你会逐渐得到共识的。

    八刀：这听起来有点疯狂

    余晟：寻求事前共识就像是在等待理想的人生伴侣，这很疯狂。
    借助fork/pull-request这种模式，Github已经干掉了事前共识，
    所以在2015年的今天你没有任何借口坚持事前共识。你应当像维基百科那样接受修改。
    先合并，再修复，同时单独讨论。所有工作应当在master分支上进行，不应当让大家等待。
    有了既成事实，共识会随之而来。

    刘天栋：然后扩大进行体制外讨论。先上车，后补票，你会逐渐得到共识的。

    Holm：寻求前期的共识：预先达成的共识；事实上，你会逐渐得到共识的：最终，你能获得事实的共识。

**4、Problem, then Solution**

**4、首先是问题，然后才是解决方案**

    庄表伟：4、首先是问题，然后才是解决方案

    余晟：4、问题优先，然后才是解决方案

**Educate yourself and others to focus on problems not features. Every patch must be a minimal solution to a solid problem. Embrace experiments and wild ideas. Help people to not blow up the lab. Collect good solutions and throw away the bad ones. Embrace failure, at all levels. It is a necessary part of the learning process.**

**教育自己和其他人，聚焦于问题而非功能特性。每一个补丁都必须是解决某个实际问题的最小化的解决方案。勇于尝试，勇于接受疯狂的想法。你还需要帮助他人，确保他们干的事情不会导致实验室的爆炸。收集好的解决方案，抛弃那些糟糕的方案。在各个层面上都应当宽容失败。这是学习过程中不可缺少的一部分。**

    庄表伟：教育自己和其他人，聚焦于问题而非功能特性。
    每一个补丁都必须是解决某个实际问题的最小化的解决方案。
    勇于尝试，勇于接受疯狂的想法，确保实验室不会被炸掉。收集好的解决方案，抛弃那些坏的。
    在所有的层面上，拥抱失败。这是学习过程中不可缺少的一部分。

    余晟：你必须教育自己和他人，集中关注问题，而不是功能特性。
    所有补丁都应当是解决某个实际问题的最小化解决方案。
    你应当勇于尝试，勇于接受疯狂的想法。你还需要帮助他人，确保他们干的事情不会导致实验室的爆炸。
    请收集好的解决方案，抛弃那些糟糕的方案。
    在各个层面上都应当宽容失败。这是学习过程中不可缺少的一部分。

    Holm：…疯狂的想法，确保实验室不会被炸掉…：断句有问题。

**5、Contracts Before Internals**

**5、首先约定，然后再完成内部实现**

    庄表伟：5、首先约定，然后再完成内部实现

    余晟：5、约定优先，然后完成内部实现

**Be aggressive about documenting contracts (APIs and protocols) and testing them. Use CI testing on all public contracts. Code coverage is irrelevant. Code documentation is irrelevant. All that matters is what contracts the code implements, and how well it does that.**

**要积极地记录约定（API与协议）并加以测试。要使用持续集成工具测试所有的公开约定。代码覆盖率是无关紧要的，代码文档也是无关紧要的。真正重要的是代码实现了哪些约定，以及它们是如何实现的。**

    庄表伟：要积极的记录约定（API与协议）并测试它们。使用CI工具测试所有的公开约定。
    代码覆盖率是无关紧要的，代码文档是无关紧要的。
    一切的关键都在与约定的代码实现，以及他们是如何实现的。

    刘天栋：…一切的关键都在于代码如何实现约定，以及他们是如何良好地实现的。

    余晟：要积极地记录约定（API与协议）并加以测试。要使用持续集成工具测试所有的公开约定。
    代码覆盖率是无关紧要的，代码文档也是无关紧要的。
    真正重要的是代码实现了哪些约定，以及它们是如何实现的。

**6、Promote From Within**

**6、从内部提拔**

**Promote contributors to maintainers, and maintainers to owners. Do this smoothly, easily, and without fear. Keep final authority to ban bad actors. Encourage people to start their own projects, especially to build on, or compete, with existing projects. Remove power from people who are not earning it on a daily basis.**

**将贡献者提拔为维护者，将维护者提拔为负责人。以流畅、轻松且无畏地方式来做。保留干掉‘害群之马’的最终权力。鼓励大家开始自己的项目，尤其是基于已有项目，或者与已有项目竞争的项目。每天持之以恒地检视并剥夺那些不再贡献者的权力。**

    庄表伟：将贡献者提拔为维护者，将维护者提拔为负责人。
    这样做起来，将会顺利、轻松并且免于恐惧。保留干掉‘老鼠屎’的最终权力。
    鼓励人们开始自己的项目，尤其是基于已有项目，或者与之竞争的项目。
    剥夺那些不再每日贡献者的权力。

    刘天栋：…以流畅、轻松而无畏地方式来做。…每天持之以恒地检视并剥夺那些不再贡献者的权力。

    余晟：维护者应当从贡献者中提拔出来，负责人应当从维护者中提拔出来。
    整个过程应当会平稳、轻松，而不应当有任何担忧。你需要保留干掉‘害群之马’的最终权威。
    还需要鼓励大家开始自己的项目，尤其是基于已有项目的项目，或者与已有项目竞争的项目。
    对于那些不能每日做出贡献的人，应当剥夺他们的权力。

**7、Write Down the Rules**

**7、将规则写下来**

    余晟：7、明文记录规则

**As you develop your rules, write them down so people can learn them. Actually, don’t even bother. Just use the C4.1 rules we already designed for ZeroMQ, and simplify them if you want to.**

**当你制定规则时，请将他们写下来，以便人们可以了解他们。事实上，你甚至都不需要亲自动手——如果你愿意，可以直接套用我们为ZeroMQ制定的规则C4.1，再按需简化。**

    庄表伟：当你制定规则时，将他们写下来，以便人们可以了解他们。
    这样一点都不麻烦。如果你愿意的话，可以直接使用我们为ZeroMQ制定的规则，再加以简化。

    刘天栋：更简单的办法是，如果你愿意的话，可以直接使用我们为ZeroMQ制定的规则C4.1…

    余晟：当你制定规则时，请将它们写下来，以便人们可以了解他们。
    事实上，你甚至都不需要亲自动手——如果你愿意，可以直接套用我们为ZeroMQ制定的规则C4.1，
    再按需简化。

**8、Enforce the Rules Fairly**

**8、公平地执行规则**

**Use your power to enforce rules, not bully others into your “vision” of the project’s direction. Above all, obey the rules yourself. Nothing is worse than a clique of maintainers who act special while blocking patches because “they don’t like them.” OK, that’s exaggeration. Many things are much worse. Still, the clique thing will harm a project.**

**用你的权力去执行规则，但不要强迫别人认同你对于项目发展方向的“愿景”。最要紧的是，你自己必须遵守规则。最糟糕的事情莫过于维护者自己形成了小圈子，仅仅因为“不喜欢”就拒绝其他人的补丁。好吧，这样说有点夸张了。不过，很多情况其实更加糟糕。还是那句话，小圈子对项目是有害的。**

    庄表伟：用你的权力去执行规则，但不要强迫别人遵循你对于项目发展方向的“愿景”。
    首先，自己就要遵守规则。没有什么比一个维护者的小圈子，仅仅因为“他们不喜欢”就拒绝补丁，
    更加糟糕的事情了。好吧，这样有些夸张了。
    不过，有些事情会更糟糕。总之，小圈子会伤害一个项目。

    余晟：用你的权力去执行规则，而不要强迫别人认同你对于项目发展方向的“愿景”。
    最要紧的是，你自己必须遵守规则。最糟糕的事情莫过于维护者自己形成了小圈子，
    仅仅因为“不喜欢”就拒绝其他人的补丁。好吧，这样说有点夸张了。
    不过，很多情况其实更加糟糕。还是那句话，小圈子对项目是有害的。

**9、Aim For the Cloud**

**9、以“云”为目标**

    庄表伟：以云为目标

    刘天栋：以集思广益为目标

**Aim for a cloud of small, independent, self-organizing, competing projects. Be intolerant of large projects. By “large” I mean a project that has more than 2-3 core minds working on it. Don’t use fancy dependencies like submodules. Let people pick and choose the projects they want to put together. It’s economics 101.**

**以小型的、独立的、自组织的、竞争性的（一群可以自由协作的）项目为目标，（市场）不能容忍大项目。所谓“大”，我的意思是一个项目包含了2~3个核心想法。要拒绝子模组那样花哨的依赖关系。让大家去挑选，并将他们选择的项目放到一起（工作）。这是经济学的常识。**

    庄表伟：以小型的、独立的、自组织的、竞争性的（可以在云中部署的）项目为目标，
    （市场）不能容忍大项目。所谓“大”，我的意思是一个项目包含了2~3个核心想法。
    不要用那些花哨的类似于子模组那样的依赖。让人们去挑选，并将他们选择的项目放到一起（工作）。
    这是经济学的基本常识。

    刘天栋：以一群小型的、独立的、自组织的、竞争性的项目为目标，不要容忍大项目。
    所谓“大”，我的意思是一个项目包含了2~3个核心大拿，
    让人们自己去挑选并揉和他们选择的项目。

    余晟：开源项目应当以小型的、独立的、自组织的、竞争性的（可以在云中部署的）项目为目标。
    对于大项目，应当坚决避免姑息。所谓“大”，我的意思是包含了2~3个核心想法的项目。
    要拒绝子模块那样花哨的依赖关系。让大家去挑选，去把自己选择的项目放到一起。
    这是经济学的常识。

**10、Be Happy and Pleasant**

**10、开心愉快最重要**

**Maybe you noticed that “be innovative” isn’t anywhere on my list. It’s probably point 11 or 12. Anyhow, cultivate a positive and pleasant mood in your community. There are no stupid questions. There are no stupid people. There are a few bad actors, who mostly stay away when the rules are clear. And everyone else is valuable and welcome like a guest who has traveled far to see us.**

**也许你注意到了，“创新”并不在我的建议列表中。它很可能排在第11或12点。总之，你需要在你的社区里培养一种积极的、愉快的氛围。愚蠢的问题，愚蠢的人都应当被踢出去。就算有“老鼠屎”，也会在清楚的规范下自动消失。剩下的人是则有价值的，我们欢迎有朋自远方来。**

    庄表伟：也许你注意到了，“创新”并不在我的建议列表中。他很可能在第11或12点。
    总之，在你的社区里培养一种积极的、愉快的氛围，没有愚蠢的问题，也没有愚蠢的人。
    就算有‘老鼠屎’，也会在违反规则时被清理掉。
    其余的人是有价值的，我们欢迎他们像游客一样，远远的看着我们。

    刘天栋：就算有“老鼠屎”，也会在清楚的规范下自动消失…我们欢迎有朋自远方来。

    余晟：也许你注意到了，“创新”并不在我的建议列表中。它很可能排在第11或12点。
    总之，你需要在你的社区里培养一种积极的、愉快的氛围。愚蠢的问题，愚蠢的人都应当被踢出去。
    就算有‘捣蛋鬼’，也会在因为违规被清理掉。
    剩下的人是则有价值的，应当像对待远到的客人那样欢迎他们。

ps.  第一次试着翻译，求各位朋友帮忙指正，多谢了！

pps. 在诸多朋友的帮助下，再修订了一遍，有了不少自己的思考，仅仅是反映在了译文之中，没有一一说明，见谅。

ppps. 徐定翔给了我一个非常好的建议：“我通常是译完隔天不看英文读一遍译文。把不符合中文表达习惯的部分润色一下。” 谢谢！

关于作者：[Pieter Hintjens](https://en.wikipedia.org/wiki/Pieter_Hintjens)

Pieter Hintjens（1962年12月3日-2016年10月4日）是比利时软件开发者、作家，也是自由信息基础设施基金会（FFII）（一个反对软件专利的协会）的前任主席。2007年，他被《知识产权管理》杂志提名为 "知识产权领域最有影响力的50人 "之一。

Hintjens于1962年出生于刚果，在东非长大。

Hintjens曾担任iMatix公司的首席执行官和首席软件设计师，该公司生产免费软件应用程序，如ZeroMQ高性能消息库、OpenAMQ AMQP消息服务、Libero、GSL代码生成器和Xitami网络服务器。

他积极参与开放标准的制定，是高级消息队列协议（AMQP）的原创者，数字标准组织的创始人，RestMS网络消息协议的编辑[8]RestMS采用Hintjens等人2008年为数字标准组织开发的点对点、共享相似、分支和合并模型（COSS）进行开发。

在2010年2月之前，他一直担任wikidot.com的CEO，该公司是发展最快的维基托管服务之一。

2010年，Hintjens被诊断出患有胆管癌，并成功通过手术切除。然而，2016年4月，它又复发了，他被诊断为末期胆管癌。2016年10月4日，Hintjens自愿接受了安乐死。