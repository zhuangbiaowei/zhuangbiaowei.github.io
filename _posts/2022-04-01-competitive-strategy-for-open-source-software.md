---
layout: post
title: "【翻译】开源软件的竞争战略"
date: 2022-04-01 16:31 +0800
categories: OpenSource Business
comments: true
---

论文来源：[Competitive Strategy for Open Source Software](https://doi.org/10.1287/mksc.1110.0669)

作者：
* Vineet Kumar ：哈佛大学哈佛商学院，波士顿，马萨诸塞州，02163，vkumar@hbs.edu
* Brett R. Gordon ：哥伦比亚大学商学院，纽约，纽约，10027，brgordon@columbia.edu
* Kannan Srinivasan ：卡内基梅隆大学泰珀商学院，宾夕法尼亚州匹兹堡，15213，kannans@andrew.cmu.edu。

---

商业开源软件（COSS）产品 —— 基于公开源代码的私人开发的软件 —— 代表了一个快速增长、价值数十亿美元的市场。开源软件市场竞争的一个独特方面是，许多开源许可证要求企业公开某些增强功能，这就刺激了企业搭上他人贡献的便车。这种做法提出了一些令人费解的问题。首先，如果竞争者可以免费使用这些贡献，那么企业为什么要进一步开发产品？第二，一个基于免费搭车的市场如何产生高质量的产品？第三，从公共政策的角度来看，强制分享改进的做法是提高还是降低了消费者剩余和行业利润？

为了解决这些问题，我们建立了一个开源软件公司之间的双边（two-sided）竞争模型。我们的模型包括：（1）两家公司在一个垂直差异化的市场中竞争，其中产品质量是公开与私有成分的混合；（2）一个开发者市场，公司在观察到他们对开源贡献的信号后雇用他们。我们证明，在均衡中支持搭便车行为，强制分享的设置可以产生高质量的产品，而且搭便车实际上可以增加消费者剩余和行业利润。

*关键词*：开源软件、产品战略、符号化、博弈论

*发布历史*：收到论文在 2009 年 10 月 12 日；接受论文在 2011 年 7 月 6 日；Eric Bradlow 担任本文的主编，John Zhang 担任副主编。

---

## 1. 绪论

随着开源软件不断改变行业的竞争格局，这个价值 5000 亿美元的软件市场正在经历一场重大变革（《经济学人》2009）。开源软件是通过公共合作建立的。源代码被公开发布，并允许其他人对其进行改进，这与传统的软件相比，企业对产品的源代码严加保护。[^1] 然而，开放源码不再只是作为专有软件的替代品--它正越来越多地被直接纳入广泛的商业产品中（Gartner Group 2008）。[^2]

商业开源软件（COSS）公司在增加更多的功能和提高公开可用的开源软件的可用性的基础上建立商业产品。管理开放源码许可证的条款规定了修改后的版本可以如何分发。[^3] 某些许可证要求开源软件公司向公众发布功能改进，而竞争公司可以将其纳入自己的产品。这样，企业就能搭上其他企业的顺风车，这种做法被微软首席执行官史蒂夫-鲍尔默称为“从知识产权意义上讲，它是附着在它所接触的一切事物上的癌症”（Fuller 2003）。

上面讨论的独特的制度安排提出了一些令人费解的问题。首先，如果竞争对手可以自由地将这些功能用于他们的产品，那么企业为什么要为其产品开发额外的功能呢？其次，技术专家指出，在一些案例中，开源软件产品与传统封闭源码软件公司生产的类似产品相当，甚至更好（Dedeke 2009）。在一个企业面临强烈的搭便车动机的市场中，如何生产出高质量的产品？第三，强制共享是否会导致更多功能的产生？第四，鲍尔默所描述的搭便车的“癌症”在什么时候可能会伤害企业和消费者？尽管开源软件行业的重要性日益增加，但现有的研究很少研究企业在这种新环境下的竞争策略。为了解决这些问题，我们将这个行业的独特方面纳入一个模型，并利用它来分析企业的竞争战略，以阐明这些经验性的困惑。

我们先简要介绍一下这个模型，然后更详细地讨论我们的主要结果。我们的模型有两个相互作用的市场：一个是由向消费者出售软件产品的 COSS 公司组成的产品市场，另一个是由公司雇用开发人员创造软件产品的开发者市场。

产品市场是一个由事先相同的软件公司组成的纵向差异化的双头垄断，他们选择产品质量和价格。一个产品的质量是两个组成部分的函数：功能和可用性。我们考虑两种受开源许可条款制约的产品市场互动。在私有功能市场中，企业可以自由使用任何开源功能，并将其纳入其软件产品，不受限制。相反，在共享功能市场下，企业开发的功能必须贡献给开放源码，因此每个企业也可以获得竞争者开发的公开可用功能。共享功能市场使每个公司都能免费搭乘其他公司的功能贡献。在这两种类型的产品市场中，可用性的改进都是私有的；无论何种许可，企业都不能获得竞争者的可用性组件。

在开发者市场上，企业雇用开发者为其产品创造更多的功能（特性）。然而，企业并不知道一个特定的开发者是否有适当的技能水平可以被雇用。开放源码为高技能的开发者提供了一种机制，通过向开放源码贡献功能，向企业发出他们的技能（类型）。开放源码的贡献为企业提供了一个关于开发者技能的可靠信号，因为潜在的雇主可以审查开发者的贡献（Leppamaki 和 Mustonen 2009）。这种贡献的动机与解释开发者的开源贡献的经济信号原理是一致的（Lerner 和 Tirole，2002）。

产品市场和开发者市场在均衡状态下的相互作用决定了开发者的工资、企业创造的开源软件的程度和通过开发者的信号传递，以及产品质量和价格。开发者的工资预期受到上文讨论的产品市场竞争结构的影响，并影响开发者对开源的激励。较高的预期工资会增加开放源码的功能贡献。更高的工资会影响企业开发更多的功能的决定，这对提供的工资有反馈作用。均衡的产品质量平衡了开发者对开源贡献的激励和企业对边际产品改进的支付意愿。因此，理解和模拟开源软件的创建对于理解开源软件公司的竞争性产品设计和定价策略至关重要。

我们展示了本节前面提出的难题是如何由 OSS 公司在产品和开发者市场上的竞争策略产生的，并且我们比较了模型在共享特征和私有特征上的均衡结果。市场的均衡结果。我们的主要结果，反映了这些困惑，如下。

首先，在共享功能市场中，我们发现在均衡中支持对功能的免费搭车：（事后）高质量的公司创造了额外的开源功能，而低质量的公司则没有。两家公司也都开发了一定程度的可用性。高质量的公司为开源做出了贡献，因为功能和可用性的互补性增加了可用性差异化的价值，而且两家公司都从质量差异化中获得了好处。低质量的公司贡献功能的动机较小，因为它可以搭高质量公司的便车，而且它的额外功能的边际价值较低，这与经验发现的高质量公司 Red Hat 为 Linux 贡献的代码明显多于竞争厂商的结论一致（Pal and Madanmohan 2002, Handy 2008）。第二，开发者市场上企业间的竞争减少，说明共享功能市场上的质量更高，再加上强制共享所产生的生产效率。第三，在更大的私人功能市场上，开源贡献可能会更高，因为开发者期望从企业间对其技能的激烈竞争中获得更高的工资，这增加了开发者对开源功能贡献的激励。第四，在搭便车的共享功能市场上，消费者和低质量的公司都明确地比在私人功能市场上要好。在某些条件下，高质量的公司也可能在共享功能市场上获得更高的利润。在免费搭车的情况下，消费者盈余会更高，因为价格竞争加剧，通过共同特征减少了产品的差异化。

尽管我们抓住了开源软件市场上最突出的竞争因素，但我们必须从几个有趣的问题中抽象出来，如自愿提供开放源码和多产品公司。我们的研究重点是给定一个特定的 COSS 市场的企业战略。我们在第 6 节中讨论了这些限制和对未来研究的想法。

我们的论文连接了两个不同的和以前独立的文献流，特别是在产品和开发者市场之间的相互联系的模型。产品市场模型是基于市场营销和工业组织中关于纵向差异化企业的战略产品开发的著名工作（Shaked 和 Sutton，1982 年，Moorthy，1988 年）。我们的设定的新颖之处在于公共产品和私人产品的结合，这也是 OSS 产品的一个独特方面，因此它对公司和在传统公司边界之外工作的个人社区共同创造产品的新兴文献做出了贡献（Ramaswamy 和 Gouillart，2010 年；Sawhney 等人，2005 年）。我们的工作也与最近几项关于开源的研究密切相关，但与之截然不同，这些研究考察了操作系统和应用程序的双面定价（Economides and Katsamakas 2006）以及开放和封闭源代码产品之间的动态竞争（Casadesus-Masanell and Ghemawat 2006）等问题。这两篇论文都没有探讨产品设计或开源企业之间的战略互动，我们的工作是对这两篇论文的补充，因为我们研究了基于开源并相互竞争的 COSS 产品。Leppamaki 和 Mustonen (2009) 假设了一个完美的开发者市场，忽略了质量的多维方面，并且没有探讨 COSS 企业之间的战略互动。Casadesus-Masanell 和 Llanes (2011) 考虑了一个公司将其软件作为开源发布的决定如何取决于竞争对手是使用开源还是专有商业模式。这个模型对应于 MySQL 的情况，而我们的模型更适合于 Linux 和 Red Hat。一个关键的区别是，我们市场的两面性使开放源代码的创造成为内生的。另一个区别是，在我们的模型中，企业是基于开发者贡献的现有开放源代码来构建软件的。因此，企业无法决定许可证的条款。我们把企业内生地选择是否在一个或多个开放源码市场运作的可能性留给未来的研究。

第二类文献有助于理解开发者为何对开源软件做出贡献。该文献区分了内在动机（包括利他主义、使用价值和类似因素）和外在动机（由市场因素、开发者地位和潜在工资驱动），它发现外在因素在开发者的贡献决定中起着重要作用（Roberts 等人，2006）。Hars 和 Ou（2002）使用对开发者的直接调查为信号传递提供了支持，Fershtman 和 Gandal（2007）表明，当许可证更倾向于商业化的时候，开发者的贡献更大。Lerner 和 Tirole(2002) 在一篇评论文章中认为，许多证据与经济信号传递的动机是一致的。[^4] 基于这项工作，我们在 Spence(1973) 的基础上，将开发者市场表述为个人传递信号以展示不可观察的技能（或能力）。我们将 Spence 的模型扩展到包括两种类型的信号溢出：开发者-公司和公司-公司的溢出。现在我们提供一个关于开源产业的广泛概述，以更好地理解我们研究的背景。

## 2. 开放源码产业

开放源码运动在 20 世纪 90 年代获得了突出的地位，它是一个由专家开发者组成的小型社区，他们将其程序的源代码（或蓝图）免费提供给任何人使用和构建。开源软件的增长非常迅速：市场研究机构 IDC（2009）估计，到 2013 年，这个市场的直接收入将增长到 81 亿美元，年复合增长率为 22%。此外，开源软件正越来越多地被用作商业软件的一部分。大型技术公司，如 IBM、Sun Microsystems 和 HewlettPackard，早已认识到开源的重要性，并推出了数十亿美元的开源计划。[^5]

消费者发现，免费提供的开源软件缺乏可用性，需要大量的专业知识才能有效使用（Lakhani 和 von Hippel，2003 年）。开源软件公司通过增加功能（或特性）和可用性来增加开放源码的价值，这是整个软件质量的两个不同方面：

1. *功能*：提供新的或增强的功能，扩展软件的基本操作。例如，与开源的 OpenOffice 相比，Sun 公司的 StarOffice 套件具有额外的功能，提供对不同文档格式的兼容性和支持。

2. *可用性和支持服务*：提高用户有效使用产品现有功能的能力。可用性的增强通常采取非软件服务的形式，如在线帮助、技术援助、文档、包装和其他支持服务。[^6]

这些有助于软件质量的功能和可用性维度之间的区别已经被 ISO 等标准组织所认可和量化（Abran 等人，2003；Jung 等人，2004）。一个直观的思考方式是，专家用户能够有效地使用功能复杂、可用性低的软件，但普通用户的生产力却随着软件的可用性而提高。例如，对比电子表格软件的专家用户使用自定义宏来完成复杂任务的能力与普通用户通过菜单驱动的界面与软件的互动。这种区别在我们的模型制定中起到了关键作用，我们还结合了这样一个事实，即创造功能被认为是一种高技能的工作。从事可用性工作的开发人员，也就是所谓的可用性工程师，通常不从事开源软件的工作，除非被公司雇用，这与众所周知的开源项目缺乏可用性的情况是一致的（Lakhani 和 von Hippel 2003）。

许多公司已经采用了 COS 模式，COS 产品现在涵盖了广泛的应用，从生产力套件到商业智能再到客户关系管理。[^7] 行业专家清楚地认识到，建立在开放源码上是一个重要的商业战略（Goldman 和 Gabriel 2005, Riehle 2007）。COSS 公司的一个典型例子是红帽公司。该公司免费提供的 Linux 开源软件的商业版本，旨在简化和扩展 Linux 操作系统的管理和行政。红帽 Linux 在 GNU 通用公共许可证下运行，这意味着红帽公司必须公开提供它对 Linux 的任何功能贡献，但可以保留任何可用性增强的隐私。红帽公司对 Linux 内核、Linux X Windows 系统、GNU 编译器集等做出了重大贡献，所有这些都在 Linux 的许可下公开（Pal and Madanmohan 2002, Handy 2008）。红帽公司为购买其商业产品的客户提供额外的服务，如大量的文档、安装和维护以及支持计划。

因此，企业可以在开放源码的基础上进行建设，而许可证的条款规定了开源软件企业是可以将其功能保密还是必须将其公开。我们在下面的模型中讨论这一区别。

## 3. 模式——私人和共享特征市场

我们建立了一个由事先相同的公司组成的双头垄断模型，它们在两个独立但相互关联的市场中竞争：第一个是产品市场，消费者购买公司生产的软件；第二个是开发者市场，公司在其中竞争开发者。

图 1 详细说明了我们模型中的阶段顺序，其中包括私人特征和共享特征市场。阶段 0、1、3 和 4 对两种类型的产品市场都是共同的，而阶段$$2^P$$只存在于私有功能市场，阶段$$ 2^S_a $$和$$ 2^S_b $$只存在于共享功能市场。在第一阶段，开发者选择是否对开源功能做出贡献以及贡献的多少，以表明他们的技能水平。在私有功能市场中，企业同时观察到开发者的信号，并在阶段$$ 2^P $$中做出工资报价和所有产品开发决策。在共享功能市场中，企业观察开发者的信号，并在阶段$$ 2^S_a $$中做出工资报价和唯一的功能开发决策，然后他们在阶段$$ 2^S_b $$中选择开发多少可用性和复制多少功能给他们的竞争对手。在第三阶段，企业在观察了产品质量后制定价格，在第四阶段，消费者在观察了所有质量和价格后做出购买决定。表 1 总结了我们模型的符号，区分了模型中的外生模型基元和内生结果。

![](/assets/img/cs-oss-01.png)

图 1 模型中各阶段的顺序

|符号|定义|
|------|----------|
|市场类型 P,S　　　　|分别代表私人特征和共享特征市场的上标|
|模型要素　　　　||
|　　M|市场规模、异质性|
|　　$$ C_L,C_H $$|每种类型的开发者向开源贡献一个功能的成本|
|　　$$ C_s $$|开发一个单位的可用性的成本|
|　　$$ \eta_H (=\eta),\eta_L $$|高类型和低类型开发者的生产率分别为|
|均衡战略和结果||
|　　$$ p_j, q_j $$|j 公司产品的价格和质量，分别为|
|　　$$ f_j, s_j $$|j 公司雇用的开发人员数量和可用性投资，分别为|
|　　$$ F_j $$|公司 j 的产品的特征数量|
|　　$$ F_0 $$|由于开发者的贡献而产生的开放源码功能的数量|
|　　$$ e_L, e_H $$|低类型和高类型开发者对开放源码的贡献分别为|
|　　W(e)|开发者市场的工资，与 $$ e \in \{ e_L, e_H \} $$|

表 1 模型中主要结构的记号

### 3.1. 产品市场

消费者要么选择从某个 OSS 公司购买一个单位的软件，要么不购买产品，在这种情况下，他们得到的归一化效用为 0。消费者对质量的偏好是异质的，一个以 $$\theta$$ 为指数的消费者对质量为 q、价格为 p 的软件产品的效用为

$$ u(q;\theta) = \theta q - p. $$

消费者对质量的边际估价是均匀分布的，$$ \theta ～ U[0, M] $$，而它的实现值决定了消费者更喜欢哪种产品。M 是市场规模或异质性参数，数值越大表示消费者对质量的评价越分散。请注意，消费者的质量被固定为 1。

软件产品的质量 *q* 取决于其功能水平 F 和可用性 s。我们遵循行业惯例，认为这些维度是相互排斥的（Boehm 1981, Pressman 2004）。质量是由生产函数定义的：

$$ q = Q(F, s). $$

一个软件产品的功能定义了该产品可以帮助完成的一系列任务，而可用性是指消费者使用该产品的功能的难易程度。消费者既重视更多的功能，也重视更高的可用性。然而，丰富的功能可能会创造出一个过于复杂的产品，而消费者可能无法利用所有的功能而没有可用性。反之，高水平的可用性与大量的功能结合在一起更有利。[^8] 因此，我们将质量的这两个维度建模为（不完全）互补，这意味着

$$ {\partial^2Q \over \partial s \partial F} > 0. $$

捕捉到这种互补性并且在特征和可用性方面都是凹的简单函数形式是 Cobb-Douglas，$$Q(F,s)=(F \cdot s)^{1/4}$$，为了方便起见，我们使用这个函数。上述消费者偏好和产品质量的表述对所有市场都是通用的。图 2 说明了产品市场的结构：上层板块描述了私有特性市场，在这个市场中，两家公司最初都能从开源社区获得$$F_0$$的特性，下层板块描述了共享特性市场，公司将他们开发的任何特性贡献给开源。[^9] 公司$$j \in \{ 1, 2 \}$$通过雇佣$$f_j$$功能开发者和选择$$s_j$$的可用性水平来决定其产品质量，我们将公司 1 表示为总体质量较高的公司，在不损失一般性的情况下让$$q_1 > q_2$$。开发者的技能水平或生产力各不相同，$$\eta \in \{ \eta_L , \eta_H \}$$，一个开发者在被雇佣时能生产$$\eta$$单位的功能。共享特征市场和私人特征市场的关键区别在于对产品质量的表述。在上图中，私人功能市场中的公司将开放源码的功能和仅他们自己开发的功能纳入他们的产品。相比之下，下图中的共享功能市场显示，企业必须将其开发的任何功能回馈给开放源码，这些功能随后可能成为两家企业产品的一部分。

![](/assets/img/cs-oss-02.PNG)

图 2 产品市场。私人和共享功能的比较

在私有特征市场中，企业 j 的产品有$$F_j=(F_0+ \eta f_j)$$特征。在共享特征市场中，企业决定从其竞争者那里复制多少特征，用阶段$$2^S_b$$中的$$\delta \in [0, 1]$$表示。因此，产品中的特征数量为$$F_j=(F_0 + \eta f_j + \eta \delta_j f_{-j})$$。

在这两个市场中，每个公司 j 还将产品的可用性发展到 $$s_j$$ 水平，使产品的功能对消费者来说更容易。公司 j 的产品的整体质量取决于功能是私有的（P）还是共享的（S）：

$$ q^P_j = Q(F_j, s_j) = [(F_0 + \eta f_j)s_j]^{1/4}, $$ and
$$ q^S_j = Q(F_j, s_j) = [(F_0 + \eta f_j + \eta \delta_j f_{-j})s_j]^{1/4} $$.

这两种情况下的生产成本都包括支付给开发人员的工资 *w*，以创建功能和提高可用性，每单位成本为 $$c_s$$。[^10] 总的固定生产成本 $$C(f, s)$$ 是功能开发成本和可用性创造成本的总和，并给出 $$C(f, s) = w \cdot f + c_s \cdot s$$。

### 3.2. 开发者市场

开发人员是异质性分布的，要么是高技能（高类型），要么是低技能（低类型）。贡献于开放源码的成本根据开发者的类型而不同。 为了贡献 *e* 特征，高类型产生的成本为 $$c_H \cdot e$$，低类型产生的成本为 $$c_L \cdot e$$，$$c_H < c_L$$ 表示高类型面临较低的成本。[^11] 高类型的开发者有一个保留选项 $$\gamma ～ \psi ( \cdot )$$，其累积分布函数为 $$\Psi ( \cdot )$$，支持范围为 $$[\underline{R}, \bar{R}]$$，其中 $$0≤ \underline{R} < \bar{R}$$。[^12] 这个选项代表了开发者从她目前的工作中获得的效用，只有当新的工资报价超过 *r* 和信号成本时，她才会接受。请注意，开发者在两个方面是异质的：他们（离散的）技能水平和他们（连续的）保留工资。 

在信号成功地揭示了开发者的类型或技能水平后，开发者可以选择 COSS 公司，或外部市场。高技能开发者的外部市场之所以存在，是因为成功为开源项目做出贡献所需的技能可以在许多市场上得到有用的应用。例如，一个为 Linux 开放源码项目做出贡献的开发者可以收到甲骨文等公司的邀请，而甲骨文并不是 Linux 市场上的主要竞争者。我们通过外部需求 $$D(w)$$ 来捕捉开发者通过对开源项目的贡献所能发出的软件技能的具体程度。一个低的外部需求表明所发出的技能是非常具体的，而一个高的外部需求则表明相反。因此，外部需求 $$D(w)$$ 是市场工资的函数，并且只在它通过创造对高技能开发者的额外需求来源而影响工资的意义上影响市场结果。请注意，外部市场对没有发出信号的开发者没有需求，因为他们的技能水平是不确定的。

图 3 显示了开发者市场及其与产品市场的联系。这些数字与图 1 中概述的博弈阶段相对应。开发者根据市场形成对工资的预期，并对开放源码做出贡献，向企业发出他们的技能水平的信号（阶段 1 ）。这些贡献是可以公开观察到的，企业利用这些贡献来评估开发者的技能，并向开发者提供工资（阶段 $$2^P$$ 和 $$2^S_a$$ ）。[^13] 企业同时雇用开发者，并在此过程中选择产品的功能水平。

![](/assets/img/cs-oss-03.png)

图 3 开发者市场

低类型的开发者可能试图伪装成高类型的开发者来说服公司雇用他们。开放源码项目的看门人会筛选出低质量的代码，并决定接受哪些提交的代码，这意味着高类型开发者的贡献成本较低（Bagozzi 和 Dholakia，2006）。为了简化我们的论述，我们做了两个假设：低类型的开发者有保留选项 $$R_L≥0$$，他们在被雇佣时对 COSS 公司没有生产力；即 $$\eta_L=0$$。这些假设使得雇用低类型的人无利可图。[^14]

如果企业能够观察到开发者的技能水平，他们就会以这种观察为基础来确定工资。然而，当工资是不可观察的时候，它取决于对开源 *e* 的贡献，表示为$$w(e)$$。贡献 *e* 功能的 $$t \in \{L, H\}$$ 类型的开发者获得 $$u_t(w,e)=w(e) - c_t e$$，她的最佳贡献水平为

$$
\begin{aligned}
&{e_t = \underset{e}{\arg \ max} \ w(e) - c_t e,}
&
& (1)
\end{aligned}
$$

受制于激励相容性（IC）和个人理性（IR）条件：

$$
\begin{aligned}
{\begin{aligned}
&(IC_H): w(e_H) - c_H ≥ w(e_L) -  C_H e_L, \\\\
&(IR_H): w(e_H) - c_H e_H ≥ r, \\\\
&(IC_L): w(e_L) - c_L e_L ≥ w(e_H) - c_L e_H, \\\\
&(IR_L): w(e_L) - c_L e_L ≥ 0.
\end{aligned}}
&
& (2)
\end{aligned}
$$

为了确保分离，高类型的开发者必须认为付出高水平的努力（$$IC_H$$）是激励相容的，并且与她的保留选择（$$IR_H$$）相比，必须得到足够的补偿来为 COSS 企业工作。低类型的开发者必须发现模仿高类型的开发者（$$IC_L$$）是非常昂贵的。低类型的 IR 约束是很容易满足的。企业不认为在他们的类型被可信地揭示后，以任何正工资雇用低类型的开发者是最佳的。当低类型开发者没有贡献时，$$IC_L$$ 中的条件就会减少到 $$0≥w(e)-c_L e_H$$。在高类型的开发者中，那些保留值低于阈值 $$r≤w(e_H)-c_H e_H$$ 的开发者会选择发出信号，而其他保留值较高的开发者，$$r>w(e_H)-c_H e_H$$ 则不会发出信号。因此，发出信号的高类型开发者的数量是 $$f_0^H =\Psi (w(e_H) - c_H e_H)$$。

这个条件描述了企业或外部市场可供雇用的开发者的供应。给定一个任意的工资 *w*，第一阶段可用的开源功能的初始水平，$$F_0(w)$$，是开发者的数量和他们的贡献的函数：

$$
\begin{aligned}
&{F_0(w) = f_0 e_H = \Psi(w(e_H) - c_H e_H ) eH.}
&
& (3)
\end{aligned}
$$

尽管 IR 和 IC 条件是必要的，但它们并不足以决定工资，工资取决于产品市场和开发者市场之间的互动，它们分别制约着开发者的需求和供应。

### 3.3. 讨论和比较

我们将目前的设置与 Spence 的典型模型（1973）进行比较，在该模型中，工人通过教育投资向完全竞争的企业市场发出信号，并获取所有的剩余。在我们的模型中，开发者对开源功能的贡献是对寻求雇佣高技能开发者的 COSS 公司的信号。我们在两个主要方面建立了 Spence，从而使该模型适用于更广泛的环境。首先，我们的模型考虑了一个不完全竞争的、垂直差异化的双头垄断，在这个双头垄断中，公司赚取正的利润--类型内的开发者异质性和开发者的不同边际生产力意味着公司只根据最后一个功能对他们的边际价值来提供工资。因此，消费者对质量的边际价值递减使企业和开发者都能赚取盈余。

第二，信号贡献有两种类型的溢出效应：开发者对公司的溢出和公司对公司的溢出。在开发者对企业的溢出效应中，开发者在第一阶段的贡献可以替代企业的功能贡献。由于信号的作用，开发者对开源的贡献越多，企业对他们的竞争就越不激烈，这就起到了减少工资的作用。在共享功能市场上，企业与企业之间会发生溢出效应，因为每个企业的功能贡献都可以提供给竞争者。因此，企业对开发者人才的竞争不那么激烈，因为企业意识到他们可以完全利用其竞争对手开发的功能。

相比之下，Spence（1973）的教育信号传递模型既没有考虑不完全竞争，也没有考虑我们所构想的那种溢出效应。在我们的模型中，开发者的信号传递不仅影响到该开发者的效用和雇佣他的 OSS 公司，而且还关键性地改变了市场中 OSS 公司之间的战略互动，我们认为本文是第一个研究信号传递环境中包括战略溢出效应的重要方面。这些相互冲突的激励措施在产品市场和开发者市场之间建立了关键而独特的联系，接下来我们将分析这些市场中相互联系的均衡的特性。

## 4. 平衡分析

我们通过逆向归纳法分析模型的子博弈完全均衡，从消费者的选择和第三阶段的定价子博弈开始。然后，我们转向 $$2^P$$ 或 $$2^S_a / 2^S_b$$ 阶段的产品开发决策，最后转向第一阶段的开发者信号博弈。对我们的分析并不重要的中间结果在电子附录中以定理的形式出现（可作为在线版本的一部分，可在 [http://mktsci.pubs.informs.org/](http://mktsci.pubs.informs.org/) 查看）。

### 4.1. 定价均衡

第三阶段的定价子博弈适用于产品市场的所有情况，它在很大程度上借用了 Moorthy（1988）的观点。我们将消费者 $$\theta_{12}$$ 定义为对公司 1 和公司 2 的产品无动于衷，因此，所有对质量有较高价值的消费者，即 $$\theta > \theta_{12}$$ ，都会选择公司 1 的产品。$$\theta_{12}$$ 由冷漠条件决定，$$\theta_{12} \cdot q_1 - p_1 = \theta_{12} \cdot q_2 - p_2$$。同样，我们定义消费者 $$\theta_{20}$$，他在购买公司 2 的产品和不购买任何产品之间是无所谓的，这样 $$\theta_{20} q_2 - p_2 = 0$$。请注意，所有消费者 $$\theta$$，使 $$\theta_{20} < \theta < \theta_{12}$$ 选择购买公司 2 的产品，而不是公司 1 的产品或不购买的选择。然后，各公司的市场份额被确定为

$$m_1 = {1 \over M} (M - \theta_{12}) = {1 \over M} (M - { {p_1 - p_2} \over {q_1 - q_2} }), and$$

$$m_2 = {1 \over M} (\theta_{12} - \theta_{20}) = {1 \over M} ({ {p_1 - p_2} \over {q_1 - q_2} } - {p_2 \over q_2}).$$

收入由上述市场份额和价格决定，企业制定价格以实现收入最大化，导致最佳价格水平成为两个企业产品质量水平的函数：

$$p^*_1 = \underset{p1}{\arg max} (M -{ {p_1-p_2} \over {q_1 - q_2} }) p_1, and$$

$$p^*_2 = \underset{p2}{\arg max} ({ {p_1-p_2} \over {q_1 - q_2} } - {p_2 \over q_2}) p_2.$$

每个企业的最优价格是对另一个企业设定的价格的最佳反应，并取决于两个产品的质量水平，而最优收入仅是企业选择的产品质量水平的函数。

在这个阶段，我们注意到，公司的收入、价格。和消费者盈余都只表示为 产品质量水平和市场规模的函数 规模的函数。接下来，我们描述了产品设计的特点 关于功能和可用性，我们评估 这对产品质量有什么影响。

### 4.2. 产品质量均衡

企业通过雇佣开发人员和进行可用性投资来确定其产品特征，这两者都有助于提高产品质量。产品战略子博弈开始于私有特性市场的 $$2^P$$ 阶段和共享特性市场的 $$2^S_a$$ 阶段。我们描述了在工资（ $$w$$ ）和免费提供的开源功能（ $$F_0$$ ）的情况下，COSS 公司的部分均衡行为。利润函数是通过将功能和可用性水平代入收入函数并考虑开发成本而得出的。

在私人市场的 $$2^P$$ 阶段和在共享功能市场的 $$2^S_a$$ 和 $$2^S_b$$ 阶段，子博弈的解决需要企业从战略上确定功能和可用性的最佳组合，这反过来又决定了整体质量。在共享功能市场中，搭便车的可能性导致了产品差异化的减少和价格竞争的加剧，因此不清楚在均衡状态下是否有公司会对功能做出贡献，或者每个公司是否会发现搭便车在其竞争者的贡献上更有利可图。

**命题 1（产品市场均衡）** 由 $$F_0$$ 初始开源特征产生的产品策略均衡，并且企业 $$j\in\{1, 2\}$$ 根据产品质量进行区分，其特征是特征水平、可用性和整体质量，取决于市场类型：

|私有|共享|
|------|----------|
|$$s^P_j = \pi^S_j M^2  \sqrt{\eta \over {c_s}^3 w},$$|$$s^P_j = \psi^Q_j M^2  \sqrt{\eta \over {c_s}^3 w},$$|
|$$f^P_j = \pi^F_j M^2  \sqrt{\eta \over c_s w^3} - {F_0 \over \eta},$$|$${\begin{aligned} &f^S_1 = \psi^F_1 M^2  \sqrt{\eta \over c_s w^3} - {F_0 \over \eta}, \\ &f^S_2 = 0, \end{aligned}} $$|
|$$q^P_j = \pi^Q_j M \sqrt{\eta \over c_s w},$$|$$q^S_j = \psi^Q_j M \sqrt{\eta \over c_s w}.$$|

在共享特征市场中，每个公司都完全复制其竞争对手的特征。竞争者的特征，因此，$$\delta_1 = \delta_2 = 1$$。

用于私人功能市场的常数 $$\pi^S$$、$$\pi^F$$ 和 $$\pi^Q$$ 以及用于共享功能市场的常数 $$\psi^S$$、$$\psi^F$$ 和 $$\psi^Q$$ 在电子附录中定义。

这里有几个要点需要注意。首先，在私有功能市场上，除了从开放源码获得的 $$F_0$$ 功能外，两家公司都创造了一些功能。$$F_0$$ 的增加导致企业减少他们开发的功能数量，因为开放源码的功能是一种替代品。我们发现，企业更多地在成本较低的质量维度上对其产品进行区分，这意味着如果功能的生产成本较低，企业将更多地在功能上进行区分，$$(f_1 - f_2 > s_1 - s_2)$$。

第二，共享特征市场阶段 $$2^S_b$$ 的含义是，两家公司都完全复制竞争对手的特征。部分复制的策略似乎是最佳的，因为它将创造更多的产品差异化。为了理解这个结果背后的直觉，请分别考虑每个公司的激励机制。对于高质量的公司来说，复制更多的产品总是更受欢迎，因为这样做可以提高公司自身的质量和公司之间的质量差异化程度 $$(q_1-q_2)$$。对于低质量的公司来说，复制会增加其自身的质量，但会减少质量的差异化。然而，当质量水平相差足够大时，质量提高的正面效应支配了差异化减少的负面效应。低质量的公司完全复制高质量公司的特征，因此，为了达到一定的质量水平，在可用性方面的投资较少。

我们发现，只有高质量的公司开发的功能超出了开发者贡献的开源功能 F0。低质量的公司则完全搭上了高质量公司提供的功能。为什么高质量的公司会开发出一个积极的功能？这个直觉来自于这样一个事实：质量维度是互补的，这意味着消费者对可用性的边际效用随着功能水平的提高而增加。尽管特征并不直接有助于产品质量的区分，但它们确实放大了企业间可用性差异的影响。请注意，低质量的公司在可用性方面的投资比高质量的公司少，而高质量的公司开发功能是为了提高产品的差异化程度，而这种差异化是由拥有较高可用性的产品所导致的。因此，来自可用性的差异化的增加使得创造降低竞争强度的特征是值得的。

上述共享功能市场的产品市场结果对开发者市场有一个关键的影响，我们在下一节中研究：只有高类型的公司雇用开发者，因为低类型的公司不开发功能 $$(f_2=0)$$，而且只有外部市场为发出信号的开发者提供了一个替代品。

### 4.3. 开发者市场平衡

工资影响企业对开发者的需求，影响愿意发出信号的开发者的数量，也影响他们在第一阶段对开放源码的贡献水平。均衡工资必须平衡企业对开发者的需求和愿意通过信号进入市场的开发者的供应。我们重点关注高类型和低类型开发者对开源软件做出不同贡献的分离均衡。

对于信号传递博弈中的分离均衡，我们确定了工资的条件，即导致一些高类型的开发者做出积极的贡献，并确保低类型的开发者不会发现模仿他们是有利可图的。下面的结果提供了工资和开源贡献方面的最小成本分离（LCS）均衡的必要条件。与最低成本分离均衡相对应的贡献和信念，包括满足直觉标准的均衡外信念（Cho and Kreps 1987），有助于确定一个独特的均衡，我们将进一步关注这个均衡。[^15]

**命题 2（开发者市场分离均衡）** 在 LCS 均衡中，对开源做出贡献的高类型开发者的数量和每个开发者贡献的功能数量都随着工资的增加而增加。

请注意，这一结果与产品市场的类型无关。两类开发者的缴费决定决定了分离所需的最低缴费额；$$e^{LCS}(w) = w/c_L$$。工资越高，低类型的开发者就越有动力去伪装成高类型的开发者，因此后者必须贡献更多的功能，使前者伪装起来没有吸引力。具有低保留或外部选择权的高技能开发者，即 $$r<r^{LCS}(w)=w-c_H e^{LCS}(w)=w(w-c_H/c_L)$$，选择发出信号，意味着发出信号的高类型开发者的数量为 $$f^{LCS}_0 = \Psi (r^{LCS}) = \Psi (w - c_H e^{LCS}(w))$$。因此，随着工资的增加，那些认为对开放源码的贡献与他们目前的保留选择相比相对更有吸引力的高类型开发者的数量也会增加。

第一阶段产生的开源特性的数量是发出信号的开发者数量与每个开发者的贡献的乘积，$$F^{LCS}_0(w) = f^{LCS}_0 e^{LCS} (w) = (w/c_L) \Psi (w(1-c_H/c_L))$$。这一结果使我们能够关注决定 $$F_0$$ 的（预期）工资水平。我们把注意力进一步限制在 LCS 均衡结果上，并去掉 LCS 的上标。

## 5. 市场互动和比较

在前面的结果中，我们分别考察了涉及企业和消费者的产品市场竞争，以及涉及企业和开发者的开发者市场。我们将整个市场的这两方面整合起来，以了解私人功能和共享功能市场的竞争性产品策略。市场之间的关键联系是开发者的工资，它决定了有多少功能被生产出来以纳入产品中。

均衡工资 $$w^P$$ 或 $$w^S$$ 等于由企业需求和对开发者的外部需求 D4w5 形成的对开发者的总体需求，以及宁愿发出信号也要保留选择的开发者的总供给。我们把私人特征市场的超额需求函数 $$\xi^P$$ 和工资为 w 的开发者共享特征市场的超额需求函数 $$\xi^S$$ 表示为

$$ \begin{aligned}
& &\xi^P(w) = &D(w) + M^2 \sqrt{\eta \over {c_s w^3} } D(\pi^F_1 + \pi^F_2) & & &\\\\ 
& & &-2 {w \over c_L} \Psi(w [1 - {c_H \over c_L} ]) - \Psi (w [1 - {c_H \over c_L} ]),\\\\
& &\xi^S(w) = & \underbrace {D(w)}_{External \ demand} \\\\
& & & + \underbrace {M^2 \sqrt{\eta \over c_s w^3} \psi^F_1 - {w \over c_L} \Psi (w [1 - {c_H \over c_L}])}_{COSS \ demand D = f_1 + f_2} \\\\
& & & - \underbrace{\Psi (w -  [1 - {c_H \over c_L}])}_{Developers' signaling}. & & (4)
\end{aligned}$$

将过剩需求等同于 0，决定了两种情况下的均衡工资。低于这个工资水平，为开源做出贡献的高类型开发者就会比企业愿意雇用的要少，而高于这个工资水平，更多的开发者就会倾向于做出贡献而不是企业愿意雇用。因此，均衡工资的作用是平衡开发者和企业的信号激励，我们研究了它与市场规模、信号成本和生产可用性的成本之间的比较静态。私有特征和共有特征市场的隐含方程 $$\xi^P(w^P)=0$$ 或 $$\xi^S(w^S)=0$$ 分别决定了均衡工资 $$w^P$$ 或 $$w^S$$。

**命题 3（工资）** 以下属性 对均衡工资来说是成立的。

(i) 共享特征市场上的工资低于 在私人特征市场上，$$w^S < w^P$$。

(ii) 在两个市场中，w 都满足以下属性：w 在市场规模 $$(\delta w / \delta M > 0)$$、信号成本 $$(\delta w / \delta c_H > 0)$$ 和技能水平 $$(\delta w / \delta \eta > 0)$$ 中是增加的；在可用性成本 $$(\delta w / \delta c_s < 0)$$ 中是减少的。

在 (i) 中，我们发现在共享功能市场中，由于企业之间的免费搭车，均衡工资较低。我们从命题 1 中发现，在共享功能市场上，$$f_2=0$$ 与支付给开发者的工资无关，公司 2 选择完全自由搭车，复制公司 1 的功能。自由搭车的效应减少了企业间在开发者市场上的竞争，导致开发者工资的降低，这反过来又导致第一阶段产生的开源功能减少。

检查 (ii) 中的比较统计学，我们发现工资随着市场规模 M 的增加而增加，因为更大的市场会使企业在创造更高质量的产品方面进行更多的投资，而企业之间的竞争会促使工资上升。当生产可用性的成本较低时，工资也较高，因为低的 $$c_s$$ 允许企业在可用性方面进行更多的投资。较高的可用性水平提高了互补性特征对消费者的价值，企业在特征方面的投资增加，从而提高了开发者的工资。当信号传递对高类型的开发者来说是昂贵的时候，更少的人发出信号，更多的人选择他们的保留选项，导致更少的开源功能，这种减少的供应提高了工资。

我们接下来研究开放源码功能的提供，这是专家用户以及政策制定者和开放源码项目的初始创建者所关心的，他们可能会寻求最大化公开可用的功能数量。

**命题 4（开源的创造）** 当市场规模大，高类型开发者的信号成本低时，在私有功能市场下，开源功能的创造要比共享功能市场高。

在共享特征市场中，两家公司不仅可以获得高类型开发者对开源的贡献，还可以获得高质量公司开发的特征。相比之下，私有功能市场允许企业将其功能保持在私有状态，只留下对功能的信号贡献作为开放源码，导致我们预期开放源码的功能较少。然而，当消费者市场很大时，生产更高质量的产品具有更大的价值，企业在私人功能市场上对开发者的竞争更加激烈。这种效应提高了高类型开发者与低类型开发者分离的动机。当分离相对容易时（$$c_H$$ 与 $$c_L$$ 相比较小），更多的高类型开发者进入市场，更多的开发者为开放源码功能作出贡献。

开源功能的水平，加上坚定的决定，影响到整体的产品质量，我们把注意力转向这个问题。

**命题 5（产品质量）** 对比这些市场，我们发现以下情况。

(i) 私人特征市场提供最低的质量水平。

(ii) 对于小的市场规模和低的信号成本，私有功能市场提供了最高质量的产品。

(iii) 共享功能市场的可用性比率 s1/s2 总是比私人功能市场的大，而私人功能市场下的功能比率 f1/f2 更大。私人功能市场的质量差异化比率 q1/q2 的捕获量比共享功能市场的要高。

在共享功能市场上，低质量公司的质量总是更高，因为该公司能够免费搭上高质量公司提供的功能。即使低质量公司开发的可用性水平低于私人功能市场，这一效应也是成立的，而且它与模型参数无关，如市场规模或信号传递成本。

产品市场类型对高质量公司的质量水平的影响更加微妙：它取决于市场规模、信号传递成本和开发可用性的成本。如果工资相同，私人特征市场将提供最高质量的产品。然而，回顾一下，$$w^P>w^S$$，当企业之间对开发者的竞争没有那么激烈时，工资之间的差异是最接近的。对开发者的竞争降低可能是由于市场机会较小。当市场规模较大时，对开发者的需求上升，开发高质量产品的成本和均衡工资也会增加。这些工资效应对私有功能市场比对共享功能市场更强，高质量公司选择的质量水平在共享功能市场上可能变得更高。当高类型开发者的信号传递成本较高时，这也导致了竞争的加剧，放大了企业之间在私人功能市场上对开发者的竞争。

可用性的边际效益随着功能的公共贡献水平的提高而增加，这意味着开发者发出的更多信号会增加企业开发可用性的动机。在共享功能市场上，企业在可用性上的差异化更大，因为这是唯一的差异化手段，但这种差异化不足以克服两种产品具有相同水平的功能的事实，因此共享功能市场上的质量差异化更低。

接下来，我们评估消费者和企业在两个市场上获得的剩余水平 和企业在两个市场上获得的剩余。

**命题 6（利润和消费者盈余）** 我们研究了盈余的创造和在企业和消费者之间的分配情况。我们发现，在企业和消费者之间创造和分配盈余

(i) 在共享特征市场下，高质量的公司可以获得更高的利润。

(ii) 在所有市场条件下，共享特征市场的消费者剩余都高于私人特征市场。

高质量的公司可能会有更高的利润，因为更大的外部需求会诱发广泛的开发者对开源的贡献，这增加了开发者-公司的溢出效应，但减少了公司-公司的溢出效应（对功能的免费搭乘）。在这种情况下，高质量的公司在共享功能市场下可以做得更好。

(ii) 中的消费者剩余结果令人惊讶地具有普遍性和反直觉性：企业对开发者竞争的减少增加了对消费者的剩余。其理由是，企业开发的产品中使用的信号（开源功能）的效用，以及由于低质量企业对功能的搭便车而导致的开发者市场竞争的减少，都有利于消费者。因此，与鲍尔默的观点相反，即强制性共享许可是一个“附着在自己身上的癌症”，我们发现这样的要求可能对消费者和公司都有利。

## 6. 结论、局限性与进一步的工作

商业化的开源软件市场正在迅速增长，并对常规软件市场产生了许多战略影响（《经济学人》2009）。企业利用开源的能力改变了产品设计的决策，这比产品的组成部分完全是专有的标准设置要多。我们构建了一个商业开源市场的双边模型，其中企业在产品和开发者市场中竞争。开发者为开放源码做出贡献，向企业传递他们的技能水平，这决定了企业可用于其产品的开放源码水平。企业雇佣开发者来建造他们的产品，然后他们在一个垂直差异化的市场上为消费者竞争。我们比较了两种常见的开放源代码许可证下的均衡结果。我们相信我们的框架可以帮助营销学者理解一个具有重大概念差异的领域，它对竞争性的营销策略有很大的影响，并且首先决定了创造的公共产品的数量。未来的工作可以探讨一些领域，比如企业选择采用哪种许可证，以及是否同时在多个开源市场上运作。

我们的模型有助于合理地解释在行业中观察到的一些困惑，例如为什么红帽公司对 Linux 的贡献明显多于其他公司，以及为什么强制共享的市场实际上比专有市场能产生更高质量的产品。我们表明，企业之间强制分享功能贡献实际上可以提高利润和消费者剩余，与企业可以私下进行适当投资的市场相比，在一个可以搭便车的市场中，企业可以生产更高质量的产品。我们的模型还扩展了先前关于就业市场信号传递的工作（Spence 1973），包括两种类型的溢出效应：开发者-公司和公司-公司，并且我们证明了公司和消费者如何从这些溢出效应中受益。

像往常一样，在正式模型的背景下进行这样的分析，需要做出许多简化的假设和抽象，我们在这里讨论，我们评估了几个维度，目前的论文可以沿着这些维度扩展。

首先，我们在本文中研究的市场结构并不是与开放源码相关的所有市场类型的详尽清单，其中包括企业开发专有软件并自愿发布源代码的情况--例如，MySQL，一个数据库产品，发布其源代码并允许用户为非商业目的修改它，但对商业应用需要协商许可协议。

第二，企业面临着各种“市场进入”类型的决策，包括是否进入特定的市场，这可能取决于企业的资源、经验和能力，我们的模型并没有捕捉到，但这将是进一步研究的有趣方面。一个公司可能面临着进入许多开源市场之一的选择（例如，私有功能与共享功能市场）；它应该进入哪个市场？如果这些市场是不同的，并且公司忽略了其竞争对手的进入决定，那么本文的模型将分别适用于每个市场环境。

第三，在多产品或前瞻性的环境中，企业对开放源码做出贡献的动机更为复杂。一个多产品公司可能对开放源码做出贡献的原因是，这种贡献可以削弱另一个市场的竞争对手。这一理论意味着，IBM 对 Linux 的贡献，或 Sun 对 OpenOffice 的贡献，背后的一个动机可能是希望减少微软的市场支配地位（和收入），使每个公司能够更有效地竞争。

第四，我们对开源产品的任何横向差异化进行了抽象。公司可能开发的软件不是通用的，而是针对特定的利基用户的。例如，某些版本的 Linux 针对嵌入式或移动设备市场，其重点可能是低功耗的计算，而不是获得高功率的功能。

总之，建立在开放源码上的软件市场正在迅速增长，最近随着谷歌安卓操作系统的发布，开放源码已经跃升为移动计算平台。在移动市场上，硬件制造商生产基于安卓系统的智能手机，并在一个与我们模型中的共享功能市场非常相似的环境中发布源代码。我们的设定自然延伸到评估和理解手机市场中制造商之间的竞争。总的来说，我们预计开源市场将在未来吸引研究人员的极大关注，他们希望研究这个行业中产品设计、定价和公司战略的独特方面。

## 7. 电子伴侣

本文的电子版配套资料可作为在线版本的一部分，可在 [http://mktsci.pubs.informs.org/](http://mktsci.pubs.informs.org/)。

## 鸣谢

作者感谢 Anthony Dukes、Oded Koenigsberg、斯坦福大学、芝加哥大学、密歇根大学、德克萨斯大学达拉斯分校、蒙特利尔高等商学院 3GTM 会议、K 和长江商学院营销研究论坛的研讨会参与者的意见。任何其余的错误 是他们自己的。

## References

* Abran, A., A. Khelifi, W. Suryn, A. Seffah. 2003. Usability meanings and interpretations in ISO standards. Software Quality J. 11(4) 325–338.
* Bagozzi, R. P., U. M. Dholakia. 2006. Open source software user communities: A study of participation in Linux user groups. Management Sci. 52(7) 1099–1115.
* Boehm, B. W. 1981. Software Engineering Economics. Prentice-Hall, Englewood Cliffs, NJ. Casadesus-Masanell, R., P. Ghemawat. 2006. Dynamic mixed duopoly: A model motivated by * Linux vs. Windows. Management Sci. 52(7) 1072–1084.
* Casadesus-Masanell, R., G. Llanes. 2011. Mixed source. Management Sci. 57(7) 1212–1230.
* Cho, I. K., D. M. Kreps. 1987. Signaling games and stable equilibria. Quart. J. Econom. 102(2) 179–221.
* Dedeke, A. 2009. Is Linux better than Windows software? IEEE Software 26(3) 103–104.
* Economides, N., E. Katsamakas. 2006. Two-sided competition of proprietary vs. open source technology platforms and the implications for the software industry. Management Sci. 52(7) 1057–1071.
* Economist, The. 2009. Open-source software in the recession: Born free. (May 28) http://www.economist.com/node/13743278.
* Fershtman, C., N. Gandal. 2007. Open source software: Motivation and restrictive licensing. Internat. Econom. Econom. Policy 4(2) 209–225.
* Fuller, T. 2003. How Microsoft warded off rival. New York Times (May 15) http://www.nytimes.com/2003/05/15/technology/15SOFT.html.
* Gartner Group. 2008. Gartner highlights key predictions for It organisations and users in 2008 and beyond. Press release (January 31), Egham, UK. http://www.gartner.com/it/page.jsp?id=593207.
* Goldman, R., R. P. Gabriel. 2005. Innovation Happens Elsewhere: Open Source as Business Strategy, 1st ed. Morgan Kaufmann, San Francisco.
* Handy, A. 2008. Red Hat tops list of corporate Linux code contributors. Software Development Times (September 18) http://www.sdtimes.com/link/32870.
* Hars, A., S. Ou. 2002. Working for free? Motivations for participating in open-source projects. Internat. J. Electronic Commerce 6(3) 25–39.
* IDC. 2009. Worldwide open source services 2009–2013 forecast. Report, IDC, Framingham, MA.
* InfoWorld. 2000. Open-source platforms: IBM invests almost $1 billion in Linux. (December 18) 16.
* Jung, H. W., S. G. Kim, C. S. Chung. 2004. Measuring software product quality: A survey of ISO/IEC 9126. IEEE Software 21(5) 88–92.
* Lakhani, K. R., E. von Hippel. 2003. How open source software works: “Free” user-to-user assistance. Res. Policy 32(6) 923–943.
* Laurent, L. S. 2004. Understand Open Source and Free Software Licencing. O’Reilly, Cambridge, MA.
* Leppamaki, M., M. Mustonen. 2009. Skill signalling with product market externality. Econom. J. 119(539) 1130–1142.
* Lerner, J., J. Tirole. 2002. Some simple economics of open source. J. Indust. Econom. 50(2) 197–234.
* Moorthy, K. S. 1988. Product and price competition in a duopoly. Marketing Sci. 7(2) 141–168.
* Pal, N., T. R. Madanmohan. 2002. Competing on open source: Strategies and practise. Working paper, Massachusetts Institute of Technology, Cambridge. http://opensource.mit.edu/online_papers.php.
* Pressman, R. B. 2004. Software Engineering: A Practitioner’s Approach. McGraw-Hill, New York.
* Ramaswamy, V., F. Gouillart. 2010. The Power of Co-Creation: Build It with Them to Boost Growth, Productivity, and Profits. Free Press, New York.
* Riehle, D. 2007. The economic motivation of open source software: Stakeholder perspectives. Computer 40(4) 25–32.
* Roberts, J. A., I. Hann, S. A. Slaughter. 2006. Understanding the motivations, participation, and performance of open source software developers: A longitudinal study of the Apache projects. Management Sci. 52(7) 984–999.
* Sawhney, M., G. Verona, E. Prandelli. 2005. Collaborating to create: The Internet as a platform for customer engagement in product innovation. J. Interactive Marketing 19(4) 1–15.
* Shaked, A., J. Sutton. 1982. Relaxing price competition through product differentiation. Rev. Econom. Stud. 49(1) 3–13.
* Spence, M. 1973. Job market signaling. Quart. J. Econom. 87(3) 355–374.
* Thompson, D. V., R. W. Hamilton, R. T. Rust. 2005. Feature fatigue: When product capabilities become too much of a good thing. J. Marketing Res. 42(4) 431–442.

---

[^1]: 开源软件应与其他两种形式的免费软件相区别。一些公司免费提供他们的软件（“免费软件”），但不提供源代码（例如，Adobe Reader）。另一种形式是自愿开放源代码，即企业发布源代码，但对其使用和再分配有严格的限制。我们不考虑这些情况，因为所涉及的战略问题与开源软件公司所面临的问题有很大不同。

[^2]: 开源软件的流行例子包括 Linux 操作系统、Firefox 浏览器、OpenOffice、Apache 网络服务器、SugarCRM 和 MySQL 等等。参见 http://www.sourceforge.net，了解基于网络的开放源码应用程序库。

[^3]: 我们重点讨论两类最常见的、与 OSS 行业相关的许可证：GPL (http://www.gnu.org/licenses/licenses.html#GPL) 和 BSD (http://www.opensource.org/licenses/bsd-license.php)。更多讨论见 Laurent（2004）。

[^4]: 关于轶事，可以在 http://www.odesk.com/blog/2008/02/open-source-work-as-a-portfolio/ 和 http://blogs.techrepublic.com.com/opensource/?p=821 （2011 年 3 月 11 日访问）找到两个恰当的例子。

[^5]: 参见 InfoWorld (2000).

[^6]: 可用性也可以包括软件代码或附加程序，使界面更容易使用。

[^7]: 基于开源的商业应用的详尽清单可以在维基百科上找到；http://en.wikipedia.org/wiki/Commercial_open_source_applications（2011 年 3 月 11 日访问）。

[^8]:  一般来说，消费者不会从功能水平和可用性之间明显不平衡的产品中获益。Thompson 等人（2005）表明，购买过于复杂的产品的消费者会面临 "功能疲劳"，提高可用性可以帮助消费者有效地利用这些功能。

[^9]: $$F_0$$ 在平衡状态下通过开发者的信号传递来确定（在本节后面讨论）。

[^10]: 我们专注于功能开发者的劳动力市场，因为创造新的功能是一种更加专业和具有挑战性的技能，而将可用性建模为外生的，则更加现实。

[^11]: 尽管为了说明问题，我们认为所有的功能都是等价的，但即使开发者贡献的功能在 “质量”上是不一样的，我们的结果也是成立的。关于这种情况的证明，可向作者索取。

[^12]: 对于我们的结果，不需要对 $$\Psi$$ 的函数形式作进一步的假设。我们在描述中使用一般形式，因为它有助于提出和解释不同的效果。

[^13]: 企业的工资报价与开发者的信念，在平衡的情况下是一致的。

[^14]: 我们只要求在均衡工资下，企业因雇用一个增量的低类型开发者而增加的边际利润足够低。如果$$\eta_L>0$$，但仍然低到足以让企业发现不向他们提供正工资是有利可图的，那么这个条件就可以满足。

[^15]: 信号模型通常允许有多种均衡，我们使用直观标准来完善 "不合理 "的均衡。在我们的语境中，最小成本指的是在每个现行工资下所需的最小分离。这种对均衡外信念的提纯要求任何观察到的对均衡路径的偏离都更有可能来自于能从偏离中获得最大利益的类型。