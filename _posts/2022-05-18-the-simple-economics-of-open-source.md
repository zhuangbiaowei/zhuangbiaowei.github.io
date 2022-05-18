---
layout: post
title: "【翻译】开源的简单经济学"
date: 2022-05-18 15:18 +0800
categories: OpenSource Economics
comments: true
---
```
Josh Lerner
Jean Tirole  
Working Paper 7600
http://www.nber.org/papers/w7600
NATIONAL BUREAU OF ECONOMIC RESEARCH
1050 Massachusetts Avenue
Cambridge, MA 02138
March 2000
```

The assistance of the Harvard Business School’s California Research Center, and Chris Darwall in particular, was instrumental in the development of the case studies and is gratefully acknowledged. We also thank a number of practitioners—especially Eric Allman, Mike Balma, Brian Behlendorf, Keith Bostic, Tim O’Reilly, and Ben Passarelli—for their willingness to generously spend time discussing the open source movement. Jacques Crémer, Bernard Salanié, and Rob Merges provided helpful comments. Harvard Business School’s Division of Research provided financial support. The Institut D'Economie Industrielle receives research grants from a number of corporate sponsors, including Microsoft Corporation. All opinions and errors, however, remain our own.

哈佛商学院加州研究中心，特别是 Chris Darwall 的协助，对案例研究的发展起到了重要作用，在此表示感谢。我们也感谢一些从业者，特别是 Eric Allman、Mike Balma、Brian Behlendorf、Keith Bostic、Tim O'Reilly 和 Ben Passarelli，感谢他们愿意花时间来讨论开源运动的问题。Jacques Crémer、Bernard Salanié和 Rob Merges 提供了有益的评论。哈佛商学院的研究部提供了财政支持。工业经济研究所从一些企业赞助商那里获得研究资助，包括微软公司。然而，所有的意见和错误都是我们自己的。

# ABSTRACT / 摘要

There has been a recent surge of interest in open source software development, which involves developers at many different locations and organizations sharing code to develop and refine programs. To an economist, the behavior of individual programmers and commercial companies engaged in open source projects is initially startling. This paper makes a preliminary exploration of the economics of open source software. We highlight the extent to which labor economics, especially the literature on “career concerns,” can explain many of these projects’ features. Aspects of the future of open source development process, however, remain somewhat difficult to predict with “offthe-shelf” economic models.

最近，人们对开放源码软件开发的兴趣大增，这涉及到许多不同地点和组织的开发人员共享代码来开发和完善程序。对于一个经济学家来说，参与开源项目的个人程序员和商业公司的行为最初是令人吃惊的。本文对开放源码软件的经济学进行了初步探索。我们强调劳动经济学，特别是关于 "职业关注 "的文献，可以在多大程度上解释这些项目的特点。然而，开放源码开发过程中的某些方面仍然难以用 "现成的 "经济模型来预测。

# 1. Introduction / 介绍

Over the past two years, there has been a surge of interest in open source software development. Interest in this process, which involves software developers at many different locations and organizations sharing code to develop and refine software programs, has been spurred by three factors:

在过去的两年里，人们对开放源代码软件开发的兴趣激增。对这一过程的兴趣，包括许多不同地点和组织的软件开发人员共享代码，以开发和完善软件程序，是由三个因素刺激的：

* The rapid diffusion of open source software. A number of open source products, such as the Apache web server, dominate their product categories. In the personal computer operating system market, International Data Corporation estimates that the open source program Linux has between seven to twenty-one million users worldwide, with a 200% annual growth rate. Many observers believe it represents a leading potential challenger to Microsoft Windows in this important market segment.
* 开源软件的迅速普及。一些开放源码产品，如 Apache 网络服务器，在其产品类别中占主导地位。在个人电脑操作系统市场，国际数据公司估计，开放源码程序 Linux 在全球拥有 700 万至 2100 万用户，年增长率为 200%。许多观察家认为，在这个重要的市场领域，它代表了对微软视窗系统的一个领先的潜在挑战者。
* The significant capital investments in open source projects. Over the past two years, numerous major corporations, including Hewlett Packard, IBM, and Sun, have launched projects to develop and use open source software. Meanwhile, a number of companies specializing in commercializing Linux, such as Red Hat and VA Linux, have completed initial public offerings, and other open source companies such as Cobalt Networks, Collab.Net, Scriptics, and Sendmail have received venture capital financing.
* 对开放源码项目的大量资本投资。在过去的两年里，许多大公司，包括惠普、IBM 和 Sun，都启动了开发和使用开源软件的项目。同时，一些专门从事 Linux 商业化的公司，如 Red Hat 和 VA Linux，已经完成了首次公开募股，其他开源公司如 Cobalt Networks、Collab.Net、Scriptics 和 Sendmail 也获得了风险投资。
* The new organization structure. The collaborative nature of open source software development has been hailed in the business and technical press as an important organizational innovation.
* 新的组织结构。开放源码软件开发的协作性质已被商业和技术媒体誉为重要的组织创新。

Yet to an economist, the behavior of individual programmers and commercial companies engaged in open source processes is startling. Consider these quotations by two leaders of the open source community:

然而对一个经济学家来说，参与开源进程的个别程序员和商业公司的行为是令人吃惊的。考虑一下开放源码社区两位领导人的这些语录：

> The idea that the proprietary software social system—the system that says you are not allowed to share or change software—is unsocial, that it is unethical, that it is simply wrong may come as a surprise to some people. But what else can we say about a system based on dividing the public and keeping users helpless? [Stallman, 1999]
>
> 专有软件社会体系--说你不允许分享或改变软件的体系--是不社会的，是不道德的，是完全错误的，这种想法可能会让一些人感到惊讶。但是，对于一个建立在分裂公众和让用户无助的基础上的系统，我们还能说什么呢？[Stallman, 1999]
>
> The “utility function” Linux hackers is maximizing is not classically economic, but is the intangible of their own ego satisfaction and reputation among other hackers. [Parenthetical comment deleted] Voluntary cultures that work this way are actually not uncommon; one other in which I have long participated is science fiction fandom, which unlike hackerdom explicitly recognizes “egoboo” (the enhancement of one’s reputation among other fans) [Raymond, 1999b].
>
> Linux 黑客所追求的 "效用函数 "并不是经典的经济函数，而是他们自己的自我满足和在其他黑客中的声誉这种无形的东西。【亲笔评论删除】以这种方式运作的自愿文化实际上并不罕见；我长期参与的另一种文化是科幻小说迷，它与黑客王国不同，明确承认 "自我感觉良好"（在其他粉丝中提高自己的声誉）[Raymond, 1999b]。

It is not initially clear how these claims relate to the traditional view of the innovative process in the economics literature. Why should thousands of top-notch programmers contribute freely to the provision of a public good? Any explanation based on altruism[^1] only goes so far. While users in less developed countries undoubtedly benefit from access to free software, many beneficiaries are well-to-do individuals or Fortune 500 companies. Furthermore, altruism has not played a major role in other industries, so it would have to be explained why individuals in the software industry are more altruistic than others.

最初并不清楚这些主张与经济学文献中关于创新过程的传统观点有何关系。为什么成千上万的顶级程序员要为提供公共产品而无偿贡献呢？任何基于利他主义的解释 [^1] 都只能到此为止。虽然欠发达国家的用户无疑会从免费软件的使用中受益，但许多受益者是富裕的个人或财富 500 强公司。此外，利他主义在其他行业并没有发挥重要作用，所以必须解释为什么软件行业的个人比其他人更利他。

This paper seeks to address this puzzle, by making a preliminary exploration of the economics of open source software. Reflecting the early stage of the field’s development, we do not seek to develop new theoretical frameworks or to statistically analyze large samples. Rather, we focus on three “mini-cases” of particular projects: Apache, Perl, and Sendmail.[^2] We seek to draw some initial conclusions about the key economic patterns that underlie the open source development of software. We find that much can be explained by reference to economic frameworks. We highlight the extent to which frameworks of labor economics, and in particular the literature on “career concerns,” can explain many of the features of open source projects.

本文试图通过对开源软件的经济学进行初步探索来解决这一难题。为了反映该领域的早期发展阶段，我们并不寻求开发新的理论框架或对大型样本进行统计分析。相反，我们专注于三个特定项目的 "小案例"。Apache、Perl 和 Sendmail[^2]。我们试图得出一些关于支撑开源软件发展的关键经济模式的初步结论。我们发现，很多东西可以通过参考经济框架来解释。我们强调劳动经济学的框架，特别是关于 "职业关注 "的文献，可以在多大程度上解释开放源码项目的特点。

At the same time, we acknowledge that aspects of the future of open source development process remain somewhat difficult to predict with “off-the-shelf” economic models. In the final section of this paper, we highlight a number of puzzles that the movement poses. It is our hope that this section will have itself an “open source” nature: that it will stimulate research by other economic researchers as well.

同时，我们承认，开源开发过程的未来的某些方面仍然难以用 "现成的 "经济模型来预测。在本文的最后一节，我们强调了该运动所带来的一些困惑。我们希望这一节本身具有 "开源 "的性质：它也能刺激其他经济研究者的研究。

Finally, it is important to acknowledge the relationship with the earlier literature on technological innovation. The open source development process is somewhat reminiscent of the type of “user-driven innovation” seen in many other industries. Among other examples, Rosenberg’s [1976] studies of the machine tool industry and von Hippel’s [1988] of scientific instruments have highlighted the role that sophisticated users can play in accelerating technological progress. In many instances, solutions developed by particular users for individual problems have become more general solutions for wide classes of users. But as we shall argue below, certain aspects of the open source process—especially the extent to which contributors’ work is recognized and rewarded—are quite distinct from earlier settings.

最后，必须承认与早期技术创新文献的关系。开放源码的开发过程有点让人想起在许多其他行业看到的 "用户驱动的创新 "类型。在其他例子中，Rosenberg[1976] 对机床行业的研究和 von Hippel[1988] 对科学仪器的研究都强调了复杂的用户在加速技术进步中的作用。在许多情况下，由特定用户为个别问题开发的解决方案已经成为广泛类别用户的更普遍的解决方案。但正如我们将在下面论证的那样，开放源码过程的某些方面--特别是贡献者的工作被认可和奖励的程度--与早期的环境截然不同。

# 2. The Nature of Open Source Software / 开源软件的性质

While media attention to the phenomenon of open source software has been recent, the basic behaviors are much older in their origins. There has long been a tradition of sharing and cooperation in software development. But in recent years, both the scale and formalization of the activity have expanded dramatically with the widespread diffusion of the Internet.[^3] In the discussion below, we will highlight three distinct eras of cooperative software development.

虽然媒体对开源软件现象的关注是最近的事，但其基本行为的起源却要早得多。长期以来，在软件开发中一直存在着分享和合作的传统。但近年来，随着互联网的广泛传播，这种活动的规模和正规化程度都有了很大的提高 [^3]。在下面的讨论中，我们将强调合作软件开发的三个不同时代。

## 2.1 The first era: early 1960s to the early 1980s.  / 第一个时代：60 年代初至 80 年代初

Many of the key aspects of the computer operating systems and the Internet were developed in academic settings such as Berkeley and MIT during the 1960s and 1970s, as well as in central corporate research facilities where researchers had a great deal of autonomy (such as Bell Labs and Xerox’s Palo Alto Research Center). In these years, the sharing by programmers in different organizations of basic operating code of computer programs—the source code—was commonplace.[^4]

20 世纪 60 年代和 70 年代，计算机操作系统和互联网的许多关键方面是在学术环境中开发的，如伯克利和麻省理工学院，以及在研究人员有很大自主权的中央企业研究机构（如贝尔实验室和施乐公司的帕洛阿尔托研究中心）。在这些年里，不同机构的程序员共享计算机程序的基本操作代码--源代码--是很常见的。[^4]

Many of the cooperative development efforts in the 1970s focused on the development of an operating system that could run on multiple computer platforms. The most successful examples, the Unix operating system and the C language used for developing Unix applications, were originally developed at AT&T’s Bell Laboratories. The software was then installed across institutions, being transferred freely or for a nominal charge. Many of the sites where the software was installed made further innovations, which were in turn shared with others. The process of sharing code was greatly accelerated with the diffusion of Usenet, a computer network begun in 1979 to link together the Unix programming community. As the number of sites grew rapidly (e.g., from 3 in 1979 to 400 in 1982), the ability of programmers in university and corporate settings to rapidly share technologies was considerably enhanced.

20 世纪 70 年代的许多合作开发工作集中在开发一个可以在多个计算机平台上运行的操作系统。最成功的例子是 Unix 操作系统和用于开发 Unix 应用程序的 C 语言，最初是在 AT&T 的贝尔实验室开发的。然后，该软件被安装在各机构中，被免费转让或收取象征性的费用。许多安装了该软件的地方进行了进一步的创新，而这些创新又与其他人分享。分享代码的过程随着 Usenet 的传播而大大加快，Usenet 是一个始于 1979 年的计算机网络，将 Unix 编程社区联系起来。随着网站数量的迅速增加（例如，从 1979 年的 3 个增加到 1982 年的 400 个），大学和企业环境中的程序员迅速分享技术的能力得到了极大的提高。

These cooperative software development projects were undertaken on a highly informal basis. Typically no effort to delineate property rights or to restrict reuse of the software were made. This informality proved to be problematic in the early 1980s, when AT&T began enforcing its (purported) intellectual property rights related to Unix.

这些合作软件开发项目是在非常非正式的基础上进行的。通常情况下，没有努力去划分产权或限制软件的再利用。这种非正式性在 20 世纪 80 年代初被证明是有问题的，当时 AT&T 开始执行其与 Unix 有关的（所谓的）知识产权。

## 2.2 The second era: early 1980s to the early 1990s. / 第二个时代：80 年代初至 90 年代初

In response to these threats of litigation, the first efforts to formalize the ground rules behind the cooperative software development process emerged. This ushered in the second era of cooperative software development. The critical institution during this period was the Free Software Foundation, begun by Richard Stallman of the MIT Artificial Intelligence Laboratory in 1983. The foundation sought to develop and disseminate a wide variety of software without cost.

为了应对这些诉讼的威胁，出现了第一批将合作软件开发过程背后的基本规则正式化的努力。这开创了合作开发软件的第二个时代。这一时期的关键机构是自由软件基金会，由麻省理工学院人工智能实验室的 Richard Stallman 于 1983 年开始。该基金会试图开发和传播各种各样的软件，而不收取任何费用。

One important innovation introduced by the Free Software Foundation was a formal licensing procedure that aimed to preclude the commercialization of cooperatively developed software. In exchange for being able to use and modify the GNU software (as it was known), users had to agree to make the source code freely available (or at a nominal cost). As part of the General Public License (GPL, also known as “copylefting”), the user had to also agree not to impose licensing restrictions on others. Furthermore, all enhancements to the code—and even code that intermingled the cooperatively developed software with that developed separately—had to be licensed on the same terms. It is these contractual terms that distinguish open source software from shareware (where the binary files but not the underlying source code are made freely available, possibly for a trial period only) and public-domain software (where no restrictions are placed on subsequent users of the source code).[^5]

自由软件基金会引入的一项重要创新是一个正式的许可程序，旨在排除合作开发的软件的商业化。为了换取使用和修改 GNU 软件（正如它所知道的那样），用户必须同意免费提供源代码（或以名义成本）。作为通用公共许可证（GPL）的一部分，用户还必须同意不对他人施加许可限制。此外，所有对代码的改进，甚至是将合作开发的软件与单独开发的软件混合在一起的代码，都必须按照相同的条款进行许可。正是这些合同条款将开放源码软件与共享软件（免费提供二进制文件，但不提供基本的源代码，可能只提供试用期）和公共领域软件（对源代码的后续用户没有限制）区分开来。[^5]

This project, as well as contemporaneous efforts, also developed a number of important organizational features. In particular, these projects employed a model where contributions from many developers were accepted (and frequently publicly disseminated or posted). The right to modify the official version of the program, however, was confined to a smaller subset of individuals closely involved with the project, or in some cases, an individual leader. In some cases, the project’s founder (or his designated successor) served as the leader; in others, leadership rotated between various key contributors.

这个项目，以及同时代的努力，也发展了一些重要的组织特征。特别是，这些项目采用了一种模式，即接受许多开发者的贡献（并经常公开传播或张贴）。然而，修改程序的官方版本的权利只限于与项目密切相关的一小部分人，或者在某些情况下，只限于个别领导人。在某些情况下，项目的创始人（或他指定的继任者）担任领导；在其他情况下，领导权在不同的关键贡献者之间轮换。

## 2.3 The third era: early 1990s to today. / 第三个时代：90 年代初到今天

The widespread diffusion of Internet access in the early 1990s led to a dramatic acceleration of open source activity. The volume of contributions and diversity of contributors expanded sharply, and numerous new open source projects emerged, most notably Linux (a variant of the UNIX operating system developed by Linus Torvalds in 1991). As discussed in detail below, interactions between commercial companies and the open source community also became commonplace in the 1990s.

20 世纪 90 年代初，互联网接入的广泛传播导致了开放源码活动的急剧加速。贡献的数量和贡献者的多样性急剧扩大，出现了许多新的开放源码项目，最引人注目的是 Linux（由 Linus Torvalds 在 1991 年开发的 UNIX 操作系统的变种）。正如下面详细讨论的那样，商业公司和开放源码社区之间的互动在 90 年代也变得很普遍。

Another innovation during this period was the proliferation of alternative approaches to licensing cooperatively developed software. During the 1980s, the GPL was the dominant licensing arrangement for cooperatively developed software. This changed considerably during the 1990s. In particular, Debian, an organization set up to disseminate Linux, developed the “Debian Social Contract” in 1995. This agreement allowed licensees greater flexibility in using the program, including the right to bundle the cooperatively developed software with proprietary code. This more flexible licensing arrangement was adopted in early 1997 by a number of individuals involved in cooperative software development, and was subsequently known as the “Open Source Definition.” As the authors explained:

这一时期的另一个创新是，合作开发的软件许可的替代方法激增。在 20 世纪 80 年代，GPL 是合作开发软件的主要许可安排。这种情况在 20 世纪 90 年代发生了很大的变化。特别是，Debian，一个为传播 Linux 而成立的组织，在 1995 年制定了 "Debian 社会契约"。该协议允许被许可人在使用该程序时有更大的灵活性，包括将合作开发的软件与专有代码捆绑在一起的权利。这种更灵活的许可安排在 1997 年初被一些参与合作软件开发的人采用，随后被称为 "开放源代码定义"。正如作者所解释的那样：

> License Must Not Contaminate Other Software. The license must not place restrictions on other software that is distributed along with the licensed software. For example, the license must not insist that all other programs distributed on the same medium must be open-source software. Rationale: Distributors of open-source software have the right to make their own choices about their own software [Open Source Initiative, 1999].
> 
> 许可证不得污染其他软件。许可证不得对与授权软件一起发布的其他软件施加限制。例如，许可证不得坚持要求在同一媒介上分发的所有其他程序必须是开源软件。理由是。开源软件的发行者有权对自己的软件做出自己的选择 [Open Source Initiative, 1999]。

Unlike the General Public License, this new license is not “viral”: it does not “infect” all code that was bundled with the software with the requirement that it be covered under the license agreement as well.

与通用公共许可证不同，这个新的许可证不是 "病毒式 "的：它不会 "感染 "所有与软件捆绑在一起的代码，要求它们也被纳入许可证协议。

The past few years have seen unprecedented growth of open source software. At the same time, the movement has faced a number of challenges. We will highlight two of these here: the “forking” of projects (the development of competing variations) and the development of products for high-end users.

在过去的几年里，开源软件得到了空前的发展。同时，这一运动也面临着一些挑战。我们将在此强调其中的两个：项目的 "分叉"（开发相互竞争的变体）和为高端用户开发的产品。

One issue that has emerged in a number of open source projects is the potential for programs splintering into various variants. In some cases, passionate disputes over product design have led to the splintering of open source projects into different variants. Examples of such splintering are the Berkeley Unix program and Sendmail during the late 1980s.

在一些开源项目中出现的一个问题是程序有可能分裂成各种变体。在某些情况下，对产品设计的激烈争论导致了开放源码项目分裂成不同的变体。这种分裂的例子有 Berkeley Unix 程序和 1980 年代末的 Sendmail。

Another challenge has been the apparently lesser emphasis on documentation and support, user interfaces,[^6] and backward compatibility found in at least some open source projects. The relative technological features of software developed in open source and traditional environments are a matter of passionate discussion. Some members of the community believe that this production method dominates traditional software development in all respects. But many open source advocates argue that open source software tends to be geared to the more sophisticated users.[^7] This point is made colorfully by one open source developer:

另一个挑战是，至少在一些开放源码项目中发现，对文档和支持、用户界面 [^6] 和向后兼容性的重视程度显然较低。在开放源码和传统环境下开发的软件的相对技术特征是一个热烈讨论的问题。一些社区成员认为，这种生产方式在各方面都主导了传统的软件开发。但许多开放源码的倡导者认为，开放源码软件往往是面向更复杂的用户的 [^7]。一位开放源码的开发者对这一点做了生动的说明：

> [I]n every release cycle Microsoft always listens to its most ignorant customers. This is the key to dumbing down each release cycle of software for further assaulting the non-personal computing population. Linux and OS/2 developers, on the other hand, tend to listen to their smartest customers… The good that Microsoft does in bringing computers to non-users is outdone by the curse that they bring on experienced users [Nadeau, 1999]. 
>
> [在] 每个发布周期中，微软总是听从其最无知的客户的意见。这是每个软件发布周期的关键，以进一步攻击非个人的计算机人口。另一方面，Linux 和 OS/2 的开发者倾向于听取他们最聪明的客户的意见。..... 微软在把计算机带给非用户方面所做的好事被他们带给有经验的用户的诅咒所超越了 [Nadeau, 1999]。 

Certainly, the greatest diffusion of open source projects appears to be in settings where the end users are sophisticated, such as the Apache server installed by systems administrators. In these cases, users are apparently more willing to tolerate the lack of detailed documentation or easy-to-understand user interfaces in exchange for the cost savings and the possibility of modifying the source code themselves. In several projects, such as Sendmail, project administrators chose to abandon backward compatibility in the interests of preserving program simplicity. One of the rationales for this decision was that administrators using the Sendmail system were responsive to announcements that these changes would be taking place, and rapidly upgraded their systems. In a number of commercial software projects, it has been noted, these types of rapid responses are not as common. Once again, this reflects the greater sophistication and awareness of the users of open source software.

当然，开放源码项目的最大传播似乎是在终端用户很复杂的情况下，如系统管理员安装的 Apache 服务器。在这些情况下，用户显然更愿意容忍缺乏详细的文档或易于理解的用户界面，以换取成本的节约和自己修改源代码的可能性。在一些项目中，例如 Sendmail，项目管理员为了维护程序的简单性，选择了放弃向后兼容。这个决定的理由之一是，使用 Sendmail 系统的管理员对这些变化的公告做出了反应，并迅速升级了他们的系统。在一些商业软件项目中，人们注意到，这些类型的快速反应并不常见。这再次反映了开放源码软件用户的复杂性和意识的提高。

The debate about the ability of open source software to accommodate high-end users' needs has direct implications for the choice of license. The recent popularity of more liberal licenses such as the Debian Social Contract and the Open Source Definition and the concomitant decline of the GNU license are related to the rise in the “pragmatists’” influence. These individuals believe that allowing proprietary code and for-profit activities in segments that would otherwise be poorly served by the open-source community will provide the movement with its best chance for success.

关于开源软件能否满足高端用户需求的争论，直接影响到许可证的选择。最近比较自由的许可证，如 Debian Social Contract 和 Open Source Definition 的流行，以及随之而来的 GNU 许可证的衰落，都与 "实用主义者 "的影响力上升有关。这些人认为，允许专有代码和营利性活动出现在那些本来对开源社区服务很差的领域，将为该运动提供最佳成功机会。

# 3. The Origins of the Three Programs / 三个项目的起源

Each of the three case studies was developed through the review of printed materials and interviews (as well as those posted on various web sites) and face-to-face meetings with one or more key participants in the development effort. In addition, we held a number of conversations with knowledgeable observers of the open source movement. In Sections 4 and 5, we will frequently draw on examples from the three cases. Nonetheless, we felt it would be helpful to first provide a brief overview of the three development projects.

这三个案例研究中的每一个都是通过审查印刷材料和采访（以及在各种网站上发布的材料），以及与开发工作中的一个或多个关键参与者进行面对面的会谈而形成的。此外，我们还与开源运动的有识之士进行了多次对话。在第 4 节和第 5 节中，我们将经常借鉴这三个案例的例子。尽管如此，我们认为首先对这三个开发项目做一个简单的概述是有帮助的。

## 3.1 Apache

The development of Apache began in 1994. Brian Behlendorf, then 21, had the responsibility for operating one of the first commercial Internet servers in the country, that powering Wired magazine’s HotWired web site. This server, like most others in the country, was at the time running the Unix-based software written at the National Center for Supercomputer Applications (NCSA) at the University of Illinois. (The only competitive product at the time was the server developed at the joint European particle physics research facility CERN.) The NCSA had distributed its source code freely and had a development group actively involved in refining the code in consultation with the pioneering users. As Behlendorf and other users wrote emendations, or “patches,” for the NCSA server, they would post them as well to mailing lists of individuals interested in Internet technology.

Apache 的开发始于 1994 年。当时 21 岁的 Brian Behlendorf 负责操作国内最早的商业互联网服务器之一，该服务器为《连线》杂志的 HotWired 网站提供动力。这台服务器和国内其他大多数服务器一样，当时正在运行伊利诺伊大学国家超级计算机应用中心（NCSA）编写的基于 Unix 的软件。（当时唯一有竞争力的产品是欧洲粒子物理学联合研究机构 CERN 开发的服务器）。NCSA 免费发布了它的源代码，并有一个开发小组积极地参与到与先锋用户的协商中，完善代码。当 Behlendorf 和其他用户为 NCSA 的服务器写了一些修正，或称 "补丁 "时，他们也会把它们发布到对互联网技术感兴趣的个人的邮件列表中。

Behlendorf and a number of other users, however, encountered increasing frustrations in getting the NCSA staff to respond to their suggestions. (During this time, a number of the NCSA staff had departed to begin Netscape, and the University was in the process of negotiating a series of licenses of its software with commercial companies.) As a result, he and six other pioneering developers decided to establish a mailing list to collect and integrate the patches to the NCSA server software. They agreed that the process would be a collegial one. While a large number of individuals would be able to suggest changes, only a smaller set would be able to actually make changes to the physical code. In August 1995, the group released Apache 0.8, which represented a substantial departure from earlier approaches. A particular area of revision was the Application Program Interface (API), which allowed the development of Apache features to be very “modular.” This step enabled programmers to make contributions to particular areas without affecting other aspects of the programs.

然而，Behlendorf 和其他一些用户在让 NCSA 的工作人员回应他们的建议时遇到了越来越多的挫折。（在这期间，NCSA 的一些工作人员已经离开，开始了 Netscape 的工作，而大学也正在与商业公司就其软件的一系列许可进行谈判）。因此，他和其他六个先锋开发者决定建立一个邮件列表，以收集和整合 NCSA 服务器软件的补丁。他们一致认为，这个过程将是一个集体的过程。虽然有很多人能够提出修改建议，但只有少数人能够真正对物理代码进行修改。1995 年 8 月，该小组发布了 Apache 0.8，这代表了与早期方法的巨大差异。一个特别的修订领域是应用程序接口（API），它允许 Apache 功能的开发非常 "模块化"。这一步骤使程序员能够在不影响程序其他方面的情况下对特定领域做出贡献。

The diffusion of Apache has been quite dramatic. Periodic surveys by Netcraft show that the share of publicly observable Web servers (i.e., those not behind firewalls) running Apache rose from 31% in April 1996 to 44% in June 1997 to 55% in September 1999.[^8] In 1999, the Apache Software Foundation was established to oversee the development and diffusion of the program. The current status of Apache, as well as the other two open source projects that we focused on, is summarized in Table 1.

阿帕奇的普及是相当引人注目的。Netcraft 的定期调查显示，运行 Apache 的可公开观察的网络服务器（即那些不在防火墙后面的服务器）的份额从 1996 年 4 月的 31%上升到 1997 年 6 月的 44%，到 1999 年 9 月的 55%[^8]。1999 年，Apache 软件基金会成立，负责监督该计划的发展和推广。表 1 总结了 Apache 以及我们关注的其他两个开放源码项目的现状。

![](/assets/img/table_1.png)

## 3.2 Perl

Perl, or the Practical Extraction and Reporting Language, was created by Larry Wall in 1987. Wall, a programmer with Burroughs (a computer mainframe manufacturer now part of Unisys) had already written a number of widely adopted software programs. These included a program for reading postings on on-line newsgroups and a program that enabled users to readily update old source code with new patches.

Perl，即实用提取和报告语言，是由拉里-沃尔在 1987 年创建的。Wall 是 Burroughs（一家计算机主机制造商，现在是 Unisys 的一部分）的一名程序员，他已经编写了许多被广泛采用的软件程序。这些程序包括一个用于阅读在线新闻组的帖子的程序和一个使用户能够随时用新的补丁更新旧的源代码的程序。

The specific genesis of Perl was the large number of repetitive system administration tasks that Wall was asked to undertake while at Burroughs. In particular, Wall was required to synchronize and generate reports on two Unix-based computers as part of a project that Burroughs was undertaking for the U.S. National Security Agency. He realized that there was a need for a program language that was somewhere between the Unix shell language and the C language (suitable for developing complex programming applications). The Perl language sought to enable programmers to rapidly undertake a wide variety of system administration tasks. The program was first introduced in 1987 via the Internet. It has become widely accepted as a language for developing scripts for Apache web servers, and is incorporated in a number of other programs.

Perl 的具体起源是 Wall 在 Burroughs 工作期间被要求承担大量的重复性系统管理任务。特别是，作为 Burroughs 为美国国家安全局进行的一个项目的一部分，Wall 被要求在两台基于 Unix 的计算机上同步和生成报告。他意识到，需要一种介于 Unix shell 语言和 C 语言（适合开发复杂的编程应用）之间的程序语言。Perl 语言试图使程序员能够迅速承担各种系统管理任务。该程序于 1987 年通过互联网首次推出。它已被广泛接受为开发 Apache 网络服务器脚本的语言，并被纳入其他一些程序中。

Perl is administered on a rotating basis: the ten to twenty programmers (the number fluctuates over time) who have been most actively involved in the program take turns managing different aspects of the project. Wall himself has joined the staff of O’Reilly & Associates, a publisher specializing in manuals documenting open source programs. While he is no longer actively contributing to the programming, he remains active in managing the project.

Perl 的管理是轮流进行的：十到二十个最积极参加项目的程序员（人数随时间变化）轮流管理项目的不同方面。沃尔本人已经加入了 O'Reilly & Associates 的工作人员，这是一家专门出版开放源代码程序文档的出版社。虽然他不再积极为编程做贡献，但他仍然积极管理该项目。

Two efforts to establish a Perl-related foundation have foundered. The Perl Institute had been intended to ensure that less glamorous tasks, such as documentation, were undertaken, in order to enhance the long-run growth of Perl. The failure of these efforts may have reflected more about the specifics of the individual personalities involved than the prospects of the program itself.

建立一个与 Perl 有关的基金会的两次努力都失败了。Perl 研究所的目的是为了确保不那么吸引人的工作，比如说文档，以促进 Perl 的长期发展。这些努力的失败可能更多地反映了有关个人的具体情况，而不是项目本身的前景。

## 3.3 Sendmail

Sendmail was originally developed in the late 1970s by Eric Allman, a graduate student in computer science at the University of California at Berkeley. As part of his responsibilities, Allman worked on a variety of software development and system administration tasks at Berkeley.

Sendmail 最初是由 Eric Allman 在 70 年代末开发的，他是加州大学伯克利分校的计算机科学研究生。作为他职责的一部分，Allman 在伯克利从事各种软件开发和系统管理任务。

One of the major challenges that Allman faced was the incompatibility of the two major computer networks on campus. The approximately one dozen Unix-based computers had been originally connected through “BerkNet,” a locally developed program that provided continuous interconnection. These computers, in turn connected to those on other campuses through telephone lines, using the UUCP protocol (Unix-toUnix Copy Protocol). Finally, the Arpanet, the direct predecessor to the Internet, was introduced on the Berkeley campus around this time. Each of the networks used a different communications protocol: for instance, each person had multiple e-mail addresses, depending on the network from which the message was sent. To cope with this problem, Allman developed in 1979 a program called “Delivermail,” which provided a way to greatly simplify the addressing problem. In an emendated form that allowed it to address a large number of domains, it was released two years later as “Sendmail.” 

Allman 面临的主要挑战之一是校园内两个主要计算机网络的不兼容。大约十几台基于 Unix 的计算机最初是通过 "BerkNet "连接的，这是一个本地开发的程序，提供连续的互连。这些计算机又通过电话线与其他校园的计算机连接，使用 UUCP 协议（Unix-to-Unix 复制协议）。最后，Arpanet，互联网的直接前身，大约在这个时候被引入伯克利校园。每个网络都使用不同的通信协议：例如，每个人都有多个电子邮件地址，这取决于信息是从哪个网络发出的。为了解决这个问题，Allman 在 1979 年开发了一个名为 "Delivermail "的程序，它提供了一个大大简化寻址问题的方法。在一个允许它处理大量域名的修正形式中，它在两年后作为 "Sendmail "发布。

Sendmail was soon adopted as the standard method of routing e-mail on the Arpanet. As the network grew, however, its limitations became increasingly apparent. A variety of enhanced versions of Sendmail were released in the 1980s and early 1990s which were incompatible with each other—in the argot of the open source community, the development of the program “forked.” In 1993, Allman, who had returned to working at Berkeley after being employed at a number of software firms, undertook a wholesale rewrite of Sendmail. The development was sufficiently successful that the incompatible versions were largely abandoned in favor of the new version. By 1998, it was estimated that 80% of all e-mail traffic was sent by Sendmail.

Sendmail 很快就被采纳为 Arpanet 上路由电子邮件的标准方法。然而，随着网络的发展，它的局限性变得越来越明显。在 20 世纪 80 年代和 90 年代初，Sendmail 的各种增强版本被发布，但它们彼此不兼容--用开放源码社区的说法，程序的发展是 "分叉 "的。1993 年，Allman 在受雇于一些软件公司后回到伯克利工作，他对 Sendmail 进行了全面重写。这项开发工作非常成功，以至于不兼容的版本在很大程度上被放弃，而改用新的版本。到 1998 年，据估计 80%的电子邮件流量是由 Sendmail 发送的。

In 1997, Allman established Sendmail, Inc. The company, which has been financed by a leading venture capital group Benchmark Capital, is seeking to sell Sendmail-related software enhancements (such as more user-friendly interfaces) and services. At the same time, the company seeks to encourage the continuing development of the software on an open source basis. For instance, Sendmail, Inc. employs two engineers who work almost full time on contributions to the open source program, which is run by the non-profit Sendmail Consortium.

1997 年，Allman 成立了 Sendmail 公司。该公司得到了领先的风险投资集团 Benchmark Capital 的资助，正在寻求销售与 Sendmail 相关的软件改进（如更多的用户友好界面）和服务。同时，该公司试图鼓励在开放源码的基础上继续开发该软件。例如，Sendmail 公司雇用了两名工程师，他们几乎全职从事对开放源码计划的贡献，该计划由非营利性的 Sendmail 联盟管理。

# 4. What Does Economic Theory Tell Us about Open Source? / 经济理论对开源有什么启示？

## 4.1 What motivates programmers? Theory / 是什么激励了程序员？理论

A programmer participates in a project, whether commercial or open source, only if she derives a net benefit (broadly defined) from engaging in the activity. The net benefit is equal to the immediate payoff (current benefit minus current cost) plus the delayed payoff.

一个程序员参与一个项目，无论是商业项目还是开源项目，只有当她从参与活动中获得净收益（广义上的定义）时才会参与。净收益等于即时回报（当前收益减去当前成本）加上延迟的回报。

A programmer working on a software development project incurs a variety of immediate benefits and costs. First, the programmer receives monetary compensation if she is working for a commercial firm. Second, the programmer may be fixing a bug or customizing a program for her own benefit (as well as, in the case of an open source process, for the benefit of others.) Third, the programmer incurs an opportunity cost of her time. While she is working on this project, she is unable to engage in another programming activity. The actual cost of this time depends on how enjoyable the work is.

一个从事软件开发项目的程序员会产生各种直接的利益和成本。首先，如果程序员为一个商业公司工作，她会得到金钱上的补偿。第二，程序员可能是为了自己的利益（以及在开放源码的情况下，为了其他人的利益）修复一个错误或定制一个程序。第三，程序员产生了她时间的机会成本。当她在这个项目上工作时，她无法从事其他的编程活动。这个时间的实际成本取决于工作的愉快程度。

The delayed reward covers two distinct, although hard-to-distinguish, incentives. The career concern incentive refers to future job offers, shares in commercial open sourcebased companies,[^9] or future access to the venture capital market. The ego gratification incentive stems from a desire for peer recognition. Probably most programmers respond to both incentives. There are some differences between the two. The programmer mainly preoccupied by peer recognition may shun future monetary rewards, and may also want to signal her talent to a slightly different audience than those motivated by career concerns. From an economic perspective, however, the incentives are similar in most respects. We will group the career concern incentive and the ego gratification incentive under a single heading: the signaling incentive.

延迟奖励涵盖了两个不同的，尽管难以区分的激励。对事业的关注激励指的是未来的工作机会、基于开放源码的商业公司的股份 [^9]、或未来进入风险投资市场的机会。自我满足的激励源于对同行认可的渴望。可能大多数程序员对这两种激励都有反应。两者之间也有一些区别。主要关注同行认可的程序员可能会回避未来的金钱回报，也可能想向那些出于职业考虑的人发出她的才能的信号，这与那些人的动机略有不同。然而，从经济角度来看，这些激励措施在大多数方面是相似的。我们将把职业关注激励和自我满足激励归为一个标题：信号传递激励。

Economic theory [e.g., Holmström, 1999] suggests that this signaling incentive is stronger,

经济理论 [例如，Holmström，1999] 表明，这种信号激励更强，

```
a) the more visible the performance to the relevant audience (peers, labor market, venture capital community),
b) the higher the impact of effort on performance, and
c) the more informative the performance about talent.

a) 绩效对相关受众（同行、劳动力市场、风险资本界）的影响越大。
b) 努力对业绩的影响越大，以及
c) 绩效对人才的信息量越大。
```

The first condition gives rise to what economists call “strategic complementarities.” To have an “audience,” programmers will want to work on software projects that will attract a large number of other programmers. This suggests the possibility of multiple equilibria. The same project may attract few programmers because programmers expect that other programmers will not be interested; or it may flourish as programmers (rationally) have faith in the project.

第一个条件产生了经济学家所说的 "战略互补性"。为了拥有一个 "听众"，程序员会希望从事能够吸引大量其他程序员的软件项目。这表明存在多种均衡的可能性。同一个项目可能会吸引很少的程序员，因为程序员预期其他程序员不会感兴趣；或者它可能会蓬勃发展，因为程序员（理性地）对这个项目有信心。

The same point applies to forking in a given open source project. Open source processes are in this respect quite similar to academic research. The latter is well known to exhibit fads. Fields are completely neglected for years, while others with apparently no superior intrinsic interest attract large numbers of researchers. Fads in academia are frowned upon for their inefficient impact on the allocation of research. It should not be ignored, however, that fads also have benefits. A fad can create a strong signaling incentive: researchers working in a popular area may be highly motivated to produce a high-quality work, since they can be confident that a large audience will examine their work.

这一点也适用于某个开源项目中的分叉。开源过程在这方面与学术研究相当相似。后者是众所周知的，它表现出流行趋势。多年来，一些领域被完全忽视，而另一些领域显然没有卓越的内在兴趣，却吸引了大量的研究人员。学术界的风潮因其对研究分配的低效影响而被人诟病。然而，不应忽视的是，流行也有好处。流行可以创造一个强大的信号激励：在一个受欢迎的领域工作的研究人员可能会有很大的动力去完成高质量的工作，因为他们可以相信有很多人将会研究他们的工作。

## 4.2 Comparison between open source and closed source programming incentives. / 开放源码和封闭源码编程激励机制之间的比较

To compare programmers' incentives in the open source and proprietary settings, we need to examine how the fundamental features of the two environments shape the incentives just reviewed. We will first consider the relative short-term rewards, and then turn to the deferred compensation.

为了比较程序员在开源和专有环境中的激励机制，我们需要研究这两种环境的基本特征是如何形成刚才所回顾的激励机制的。我们将首先考虑相对的短期回报，然后再考虑递延报酬的问题。

Commercial projects have an edge on the current-compensation dimension because the proprietary nature of the code generates income. This makes it privately worthwhile for private companies to offer salaries.[^10] This contention is the old argument in economics that the prospect of profit encourages investment, which is used, for instance, to justify the awarding of patents to encourage invention.

商业项目在目前的报酬方面有优势，因为代码的专有性质产生了收入。这使得私人公司在私人方面值得提供工资 [^10]。这一论点是经济学中的一个古老的论点，即利润的前景鼓励投资，例如，它被用来证明授予专利以鼓励发明的合理性。

By way of contrast, an open source project may well lower the cost for the programmer, for two reasons:

作为对比，一个开放源码项目很可能降低程序员的成本，原因有二：

i) “Alumni effect”: Because the code is freely available to all, it can be used in schools and universities for learning purposes; so it is already familiar to programmers. This reduces their cost of programming for UNIX, for example.[^11]

ii) Customization and bug-fixing benefîts: The cost of contributing to an open source project is lower if the activity brings about a private benefit (bug fixing, customization) for the programmer and her firm. Note again that this factor of cost reduction is directly linked to the openness of the source code.

i) "校友效应"。因为代码是免费提供给所有人的，它可以在学校和大学里用于学习；所以它已经为程序员所熟悉。这减少了他们对 UNIX 的编程成本，例如。[^11]

ii) 定制和修复错误的好处。如果这项活动为程序员和她的公司带来了私人利益（修复错误，定制），那么对开源项目的贡献成本就会降低。请注意，这个成本降低的因素是与源代码的开放性直接相关的。

Let us now turn to the delayed reward (signaling incentive) component. In this respect too, the open source process has some benefits over the closed source approach. As we noted, signaling incentives are stronger, the more visible the performance and the more attributable the performance to a given individual. Signaling incentives therefore may be stronger in the open source mode for three reasons:

现在让我们来谈谈延迟奖励（信号激励）部分。在这方面，开放源码的过程也比封闭源码的方法有一些好处。正如我们所指出的，信号激励越强，业绩就越明显，业绩就越能归属于某个人。因此，在开放源码模式下，信号激励可能更强，原因有三：

i) Better performance measurement: Outsiders can only observe inexactly the functionality and/or quality of individual elements of a typical commercially developed program, as they are unable to observe the proprietary source code. By way of contrast, in an open source project, the outsiders are able to see not only what the contribution of each individual was and whether that component “worked,” but also whether the task was hard, if the problem was addressed in a clever way, whether the code can be useful for other programming tasks in the future, and so forth.

ii) Full initiative: The open source programmer is her own boss and takes full responsibility for the success of a subproject. In a hierarchical commercial firm, however, the programmer's performance depends on her supervisor's interference, advice, etc. Economic theory would predict that the programmer's performance is more precisely measured in the former case.

iii) Greater fluidity: It may be argued that the labor market is more fluid in an open source environment. Programmers are likely to have less idiosyncratic, or firmspecific, human capital that limits shifting one’s efforts to a new program or work environment. (Since many elements of the source code are shared across open source projects, more of the knowledge they have accumulated can be transferred to the new environment).

i) 更好的性能测量。外人只能不准确地观察典型的商业开发的程序的个别元素的功能和/或质量，因为他们无法观察专有的源代码。作为对比，在一个开放源码项目中，外部人员不仅能够看到每个人的贡献是什么，以及该组件是否 "工作"，而且还能看到任务是否困难，是否以巧妙的方式解决了问题，代码是否能在未来对其他编程任务有用，等等。

ii) 充分的主动性。开源程序员是她自己的老板，对一个子项目的成功承担全部责任。然而，在一个等级森严的商业公司里，程序员的表现取决于她的上司的干预和建议等。经济理论预测，在前一种情况下，程序员的表现会得到更精确的衡量。

iii) 更大的流动性：可以说劳动力市场在开放源码环境中更具有流动性。程序员可能有较少的特异性或公司特定的人力资本，限制了他们将自己的努力转移到一个新的程序或工作环境中。（由于源代码的许多元素是在开放源码项目中共享的，他们所积累的更多知识可以转移到新的环境中）。

These theoretical arguments also provide insights as to who is more likely to contribute and what tasks are best suited to open source projects. Sophisticated users derive direct benefits when they customize or fix a bug in open source software.[^12] A second category of potential contributors consists of individuals with strong signaling incentives; these may use open source software as a port of entry. For instance, open source processes may give a talented system administrator at a small academic institution (who is also a user!) a unique opportunity to signal her talent to peers, prospective employers, and the venture capital community.[^13]

这些理论论据也为谁更有可能做出贡献以及哪些任务最适合开源项目提供了启示 [^12]。第二类潜在的贡献者包括具有强烈信号激励的个人；他们可以把开放源码软件作为一个入口。例如，开放源码过程可能会给一个小型学术机构的天才系统管理员（他也是一个用户！）一个独特的机会，向同行、未来的雇主和风险投资界展示她的才能。[^13]

As to the tasks that may appeal to the open source community, one would expect that tasks such as those related to the operating systems and programming languages, whose natural audience is the community of programmers, would give rise to strong signaling incentives. By way of contrast, tasks aiming at helping the much-less-sophisticated end user—e.g., documentation, design of easy-to-use interfaces, technical support, and insuring backward compatibility—usually provide lower signaling incentives.[^14]

至于那些可能对开放源码社区有吸引力的任务，人们期望那些与操作系统和编程语言有关的任务，其自然听众是程序员社区，会产生强烈的信号激励。相比之下，旨在帮助不那么复杂的终端用户的任务--例如，文档、设计易于使用的界面、技术支持和确保向后兼容--通常会提供较低的信号激励。[^14]

## 4.3 Evidence on individual incentives / 关于个人奖励的证据

A considerable amount of evidence is consistent with an economic perspective.

相当多的证据与经济观点是一致的。 

First, user benefits are key to a number of open source projects. One of the origins of the free software movement was Stallman's inability to improve a printer program because Xerox refused to release the source code. In each of the three scenarios described in section 3, the project founders were motivated by information technology problems that they had encountered in their day-to-day work. For instance, in the case of Apache, the initial set of contributors was almost entirely system administrators who were struggling with the same types of problems as Behlendorf. In each case, the initial release was “runnable and testable”: it provided a potential, even if imperfect, solution to a problem that was vexing considerable numbers of data processing professionals.

首先，用户利益是一些开源项目的关键。自由软件运动的起源之一是 Stallman 无法改进一个打印机程序，因为施乐公司拒绝发布源代码。在第 3 节所述的三种情况中，项目创始人都是由他们在日常工作中遇到的信息技术问题所激发的。例如，在 Apache 的案例中，最初的贡献者几乎都是系统管理员，他们与 Behlendorf 一样，都在为同样类型的问题而奋斗。在每个案例中，最初的版本都是 "可运行和可测试的"：它为困扰大量数据处理专业人员的问题提供了一个潜在的，即使是不完美的解决方案。

Second, it is clear that giving credit to authors is essential in the open source movement. This principle is included as part of the nine key requirements in the “Open Source Definition” [Open Source Initiative, 1999]. This point is also emphasized by Raymond [1999b], who points out “surreptitiously filing someone’s name off a project is, in cultural context, one of the ultimate crimes.”

第二，很明显，在开放源码运动中，给作者以荣誉是至关重要的。这一原则被列为 "开源定义"[Open Source Initiative, 1999] 中的九个关键要求之一。雷蒙德 [1999b] 也强调了这一点，他指出 "在文化背景下，偷偷摸摸地将某人的名字从项目中移除是终极犯罪之一"。

Finally, the reputational benefits that accrue from successful contributions to open source projects appear to have real effects on the developers. This is acknowledged within the open source community itself. For instance, Raymond [1999b] notes three primary benefits that accrue to successful contributors of open source projects “good reputation among one’s peers, attention and cooperation from others, … [and] higher status [in the] … exchange economy.” Thus, while some of benefits conferred from participation in open source projects may be less concrete in nature, there also appear be quite tangible—if delayed—rewards.

最后，对开放源码项目的成功贡献所带来的声誉好处似乎对开发者有真正的影响。这一点在开放源码社区本身也得到了承认。例如，Raymond[1999b] 指出，开源项目的成功贡献者有三个主要好处："在同行中的良好声誉，来自他人的关注和合作，...[和] 更高的地位 [在] 交换经济中"。因此，虽然参与开放源码项目所带来的一些好处在本质上可能不那么具体，但似乎也有相当具体的回报，尽管是延迟的回报。

The Apache project provides a good illustration of these observations. The project makes a point of recognizing all contributors on its web site, even those who simply identify a problem without proposing a solution. Similarly, the organization highlights its most committed contributors, who have the ultimate control over the project’s evolution. Moreover, it appears that many of the skilled Apache programmers have benefited materially from their association with the organization. Numerous contributors have been hired into Apache development groups within companies such as IBM, become involved in process-oriented companies such as Collab.Net which seek to make open source projects more feasible (see below), or else moved into other Internet tools companies in ways that were facilitated by their expertise and relationships built up during the open source movement. Meanwhile, many of the new contributors are already employed by corporations, and working on Apache development as part of their regular assignments.

Apache 项目为这些观察提供了一个很好的说明。该项目在其网站上强调对所有贡献者的认可，即使是那些仅仅发现问题而没有提出解决方案的人。同样地，该组织也强调其最坚定的贡献者，他们对项目的发展有最终的控制权。此外，许多熟练的 Apache 程序员似乎已经从他们与该组织的联系中获得了实质性的好处。许多贡献者被雇用到 IBM 等公司的 Apache 开发组，参与到 Collab.Net 等以流程为导向的公司中，这些公司试图使开放源码项目更加可行（见下文），或者以他们在开放源码运动中建立的专业知识和关系促进的方式进入其他互联网工具公司。同时，许多新的贡献者已经受雇于公司，并将 Apache 的开发作为他们常规工作的一部分。

There is also substantial evidence that open source work may be a good stepping stone for securing access to venture capital. For example, the founders of Sun, Netscape, and Red Hat had signaled their talent in the open source world. In Table 2, we summarize some of the subsequent commercial roles played by individuals active in the open source movement.

还有大量证据表明，开放源码工作可能是确保获得风险资本的良好垫脚石。例如，Sun 公司、Netscape 公司和 Red Hat 公司的创始人都曾在开放源码世界中显示出他们的才能。在表 2 中，我们总结了一些活跃在开放源码运动中的个人后来所扮演的商业角色。

![](/assets/img/table_2.png)

## 4.4 Leadership, organization and governance / 领导、组织与治理

A successful open source project also requires a credible leader or leadership, and an organization consistent with the nature of the process.

一个成功的开源项目还需要一个或多个可靠的领导，以及一个与该过程性质相一致的组织。 

Although the leader is often at the origin a user who attempts to solve a particular program, the leader over time performs less and less programming. The leader must (a) provide a vision, (b) make sure that the overall project is divided into much smaller and well-defined tasks (“modules”) that individuals can tackle independently from other tasks, (c) attract other programmers, and, last but not least, (d) “keep the project together” (prevent it from forking or being abandoned).

尽管领导者在开始时往往是一个试图解决特定程序的用户，但随着时间的推移，领导者进行的编程越来越少。领导必须 (a) 提供一个愿景，(b) 确保整个项目被划分为更小的、定义明确的任务（"模块"），个人可以独立于其他任务来处理，(c) 吸引其他程序员，最后但并非最不重要的是，(d) "保持项目在一起"（防止它分叉或被遗弃）。

The initial leader must assemble a critical mass of code to which the programming community can react. Enough work must be done to show that the project is doable and has merit. At the same time, to attract additional programmers, it may be important that the leader does not perform too much of the job on his own and leaves challenging programming problems to others.[^15] Indeed, programmers will initially be reluctant to join a project whose leadership qualities are yet untested unless they identify an exciting challenge. Another reason why programmers are easier to attract at an early stage is that, if successful, the project will keep attracting a large number of programmers in the future, making early contributions very visible.

最初的领导者必须组装一个临界质量的代码，使编程社区能够作出反应。必须做足够多的工作来证明这个项目是可行的，而且是有价值的。同时，为了吸引更多的程序员，重要的是领导者不要自己做太多的工作，而把具有挑战性的编程问题留给其他人 [^15]。事实上，程序员最初会不愿意加入一个领导素质尚未得到检验的项目，除非他们发现了一个令人兴奋的挑战。在早期阶段比较容易吸引程序员的另一个原因是，如果成功的话，该项目在未来会不断吸引大量的程序员，使早期的贡献非常明显。

Consistent with this argument, it is interesting to note that each of the three cases described above appeared to pose challenging programming problems. When the initial release of each of these open source programs was made, considerable programming problems were unresolved. The promise that the project was not near a “dead end,” but rather would continue to attract ongoing participation from programmers in the years to come, appears to be an important aspect of its appeal. In this respect, Linux is perhaps the quintessential example. The initial Linux operating system was quite minimal, on the order of a few tens of thousands of lines of code. In Torvalds’ initial postings in which he sought to generate interest in Linux, he explicitly highlighted the extent to which the version would require creative programming in order to achieve full functionality.

与这一论点相一致的是，值得注意的是，上述三个案例中的每一个似乎都提出了挑战性的编程问题。当这些开放源码程序中的每一个最初发布时，相当多的编程问题都没有得到解决。该项目没有接近 "死胡同"，而是在未来几年继续吸引程序员的持续参与，这种承诺似乎是其吸引力的一个重要方面。在这方面，Linux 也许是最典型的例子。最初的 Linux 操作系统是相当小的，只有几万行的代码。在 Torvalds 最初的帖子中，他试图引起人们对 Linux 的兴趣，他明确强调该版本需要创造性的编程以实现全部功能的程度。

Another important determinant of project success appears to be the nature of its leadership. In some respects, the governance structures of open source projects are quite different. In a number of instances, such as Linux, there is an undisputed leader. While certain aspects are delegated to others, a strong centralization of authority characterizes these projects. In other cases, such as Apache, a committee will resolve the disputes by voting or a consensus process. At the same time, leaders of open source projects share some common features. Most leaders are the programmers who developed the initial code for the project (or made another important contribution early in the project's development). While many no longer make programming contributions, having moved on to broader project management tasks, the individuals that we talked to believed that the initial experience was important in establishing credibility to manage the project. The splintering of the Berkeley-derived Unix development programs has been attributed in part to the absence of a single credible leader.

项目成功的另一个重要决定因素似乎是其领导的性质。在某些方面，开放源码项目的管理结构是相当不同的。在一些情况下，如 Linux，有一个无可争议的领导者。虽然某些方面被委托给其他人，但这些项目的特点是权力的集中化。在其他情况下，如 Apache，一个委员会将通过投票或共识过程来解决争端。同时，开放源码项目的领导者有一些共同的特点。大多数领导者是为项目开发最初代码的程序员（或在项目发展的早期做出了其他重要贡献）。虽然许多人不再做编程贡献，而是转向更广泛的项目管理任务，但我们交谈过的人认为，最初的经验对建立管理项目的可信度很重要。伯克利衍生的 Unix 开发项目的分裂，部分归因于缺乏一个可靠的领导者。

But what does the leadership of an open source project do? It might appear at first sight that the unconstrained, quasi-anarchistic nature of the open source process leaves little scope for a leadership. This, however, is incorrect. First, as we have already indicated, the leadership sets a vision. If the leader is credible and/or the vision is compelling, this vision helps coordinate expectations. Second, even though participants are free to take the project where they want as long as they release the modified code, acceptance by the leadership of a modification or addition provides some certification as to the quality of the latter and its integration/compatibility with the overall project.

但是，一个开源项目的领导层是做什么的？乍看起来，开放源码过程的无约束、准无政府主义的性质给领导层留下的空间很小。然而，这是不正确的。首先，正如我们已经指出的，领导层设定了一个愿景。如果领导是可信的，或者愿景是令人信服的，这个愿景有助于协调期望。第二，即使参与者可以自由地把项目带到他们想要的地方，只要他们发布修改后的代码，领导层对修改或增加的内容的接受，为后者的质量和它与整个项目的整合/兼容提供了一些证明。

As discussed by Max Weber [1968], some attributes underlie a successful leadership.[^16] First, the programmers must trust the leadership: that is, they must believe that the leader's objectives are sufficiently congruent with theirs and not polluted by ego-driven, commercial, or political biases. For instance, the leadership must be willing to accept improvements on their merits even though they do not fit the leader's original blueprint.

正如马克斯-韦伯（Max Weber）[1968] 所讨论的，一些属性是成功领导的基础 [^16]。首先，程序员必须信任领导：也就是说，他们必须相信领导的目标与他们的目标足够一致，而不是被自我驱动、商业或政治偏见所污染。例如，领导层必须愿意接受有价值的改进，即使它们不符合领导层的原始蓝图。

Trust in the leadership is also key to the prevention of forking. While there are natural forces against forking (the loss of economies of scale due to the creation of smaller communities, the hesitations of programmers in complementary segments to port to multiple versions, and the stigma attached to the existence of a conflict), other factors may encourage forking. User-developers may have conflicting interests as to the evolution of the technology. Ego (signaling) concerns may also prevent a faction from admitting that another approach is more promising, or simply from accepting that it may socially be preferable to have one group join the other's efforts even if no clear winner has emerged. The presence of a charismatic (i.e., trusted) leader is likely to substantially reduce the probability of forking in two ways. First, indecisive programmers are likely to rally behind the leadership's preferred alternative. Second, the dissenting faction may not have an obvious leader of its own.

对领导层的信任也是防止分叉的关键。虽然有反对分叉的自然力量（由于创建较小的社区而导致的规模经济的损失，互补部分的程序员对移植到多个版本的犹豫不决，以及存在冲突的耻辱感），但其他因素可能鼓励分叉。用户和开发者在技术的发展上可能有利益冲突。对自我（信号）的关注也可能阻止一个派别承认另一种方法更有前途，或者干脆不接受即使没有明显的赢家出现，让一个团体加入另一个团体的努力可能在社会上更可取。一个有魅力的（即被信任的）领导者的存在，可能会在两个方面大大降低分叉的概率。首先，优柔寡断的程序员可能会团结在领导层的首选方案后面。第二，持反对意见的派别可能没有自己的明显的领导者。

A good leadership should also clearly communicate its goals and evaluation procedures. Indeed, the open source organizations go to considerable efforts to make the nature of their decision making process transparent: the process by which the operating committee reviews new software proposals is frequently posted and all postings archived. For instance, on the Apache web site, it is explained how proposed changes to the program are reviewed by the program’s governing body, whose membership is largely based on contributions to the project. (Any significant change requires at least three “yes” votes—and no vetoes—by these key decision-makers.)

一个好的领导层也应该清楚地传达其目标和评估程序。事实上，开放源码组织在使其决策过程的性质透明化方面做出了相当大的努力：运营委员会审查新软件提案的过程经常被公布，并且所有的帖子都被存档。例如，在 Apache 网站上，它解释了对该计划的修改建议是如何由该计划的管理机构审查的，该机构的成员主要是基于对项目的贡献。（任何重大的改变都需要这些关键的决策者至少投出三张 "同意 "票--没有否决票）。

# 5. Commercial Software Companies' Reactions to the Open Source Movement / 商业软件公司对开放源代码运动的反应  

This section examines the interface between open and closed source software development. Challenged by the successes of the open source movement, the commercial software corporations may employ one of the following two strategies. The first is to emulate some incentive features of open source processes in a distinctively closed source environment. Another is to try to mix open and closed source processes to get the best of both worlds.

本节探讨了开放源码和封闭源码软件开发之间的接口。在开放源码运动成功的挑战下，商业软件公司可能采用以下两种策略之一。第一种是在一个独特的封闭源码环境中模仿开放源码过程的一些激励性特征。另一种是尝试混合开放和封闭源代码的过程，以获得两个世界的最佳效果。

## 5.1 Why don't corporations duplicate the open source incentives? / 为什么企业不复制开放源代码的激励措施？ 

As we already noted, owners of proprietary code are not able to enjoy the benefits of getting free programmer training in schools and universities (the alumni effect); nor can they easily allow users to modify their code and customize it without jeopardizing intellectual property rights. Similarly, and for the reasons developed in section 4, commercial companies will never be able to duplicate the visibility of performance reached in the open source world.

正如我们已经指出的，专有代码的所有者不能享受在学校和大学里获得免费的程序员培训的好处（校友效应）；他们也不能轻易地允许用户修改他们的代码和定制，而不损害知识产权。同样，由于第 4 节所阐述的原因，商业公司将永远无法复制在开放源码世界中达到的性能可见度。

In contrast, they can to some extent duplicate some of the signaling incentives of the open source world. Indeed, a number of commercial software companies (e.g., video game companies, Qualcomm for the Eudora email program) list people who have developed the software. It is an interesting question why others do not. To be certain, commercial companies do not like their key employees to become highly visible, lest they be hired away by competitors.[^17] But, to a large extent, firms also realize that this very visibility enables them to attract talented individuals and provides a powerful incentive to existing employees.

相比之下，他们在某种程度上可以复制开放源代码世界的一些信号激励。事实上，一些商业软件公司（如视频游戏公司、Eudora 电子邮件程序的高通公司）列出了开发该软件的人。这是一个有趣的问题，为什么其他公司不这样做呢？可以肯定的是，商业公司不希望他们的关键员工变得非常引人注目，以免他们被竞争对手雇用 [^17]。但是，在很大程度上，公司也意识到，这种能见度使他们能够吸引有才能的人，并为现有的员工提供强有力的激励。

Another area in which software companies might try to emulate open source development is the promotion of widespread code sharing within the company. This may enable them to reduce code duplication and to broaden a programmer's audience. Interestingly, existing organizational forms may preclude the adoption of open source systems within commercial software firms. An internal Microsoft document on open source [Valloppillil, 1998] describes a number of pressures that limit the implementation of features of open source development within Microsoft. Most importantly, each software development group appears to be largely autonomous. Software routines developed by one group are not shared with others. In some instances, the groups seek to prevent being broken up by not documenting a large number of program features. These organizational attributes, the document suggests, lead to very complex and interdependent programs that do not lend themselves to development in a “compartmentalized” manner nor to widespread sharing of source code.[^18]

软件公司可能试图模仿开放源码开发的另一个领域是促进公司内部广泛的代码共享。这可以使他们减少代码的重复，并扩大程序员的受众范围。有趣的是，现有的组织形式可能会阻碍商业软件公司采用开放源代码系统。一份关于开放源代码的微软内部文件 [Valloppillil, 1998] 描述了一些限制在微软内部实施开放源代码开发功能的压力。最重要的是，每个软件开发小组似乎基本上是自治的。由一个小组开发的软件程序不会与其他小组共享。在某些情况下，这些小组试图通过不记录大量的程序功能来防止被拆散。该文件指出，这些组织属性导致了非常复杂和相互依赖的程序，不适合以 "分割 "的方式开发，也不适合广泛分享源代码。[^18]

## 5.2 The commercial software companies' open source strategies. / 商业软件公司的开源战略

As should be expected, many commercial companies have elaborated strategies to capitalize on the open source movement. In a nutshell, they expect to benefit from their expertise in some segment whose demand is boosted by the success of a complementary open source program. While improvements in the open source software are not appropriable, commercial companies can benefit indirectly in a complementary proprietary segment.[^19]

正如可以预料的那样，许多商业公司已经制定了战略来利用开源运动。简而言之，他们希望从他们在某些领域的专长中获益，而这些领域的需求又因互补的开放源码项目的成功而增加。虽然开放源码软件的改进是不可取的，但商业公司可以在一个补充性的专有领域间接受益。[^19]

One such strategy is straightforward. It consists of commercially providing complementary services and products that are not supplied efficiently by the open source community. Red Hat and VA Linux for example, exemplify this “reactive” strategy.[^20]

这样的策略之一是直截了当的。它包括以商业方式提供开放源码社区不能有效提供的补充服务和产品。例如，红帽和 VA Linux 就是这种 "反应式 "战略的典范。[^20]

A “reactive” commercial company may still want to encourage and subsidize the open source movement, for example by allocating a few programmers to the open source project.[^21] Red Hat will make more money on support if Linux is successful. Similarly, if logic semiconductors and operating systems for personal computers are complements, one can show by a revealed preference argument that Intel’s profits will increase if Linux (which unlike Windows is free) takes over the PC operating system market. Similarly, Sun may benefit if Microsoft's position is weakened. Oracle may wish to port its database products to a Linux environment in order to lessen its dependence on Sun's Solaris operating system. Because firms do not capture all the benefits of the investments, the free-rider problem often discussed in the economics of innovation should apply here as well. Subsidies by commercial companies for open source projects should remain limited unless the potential beneficiaries succeed in organizing a consortium (which will limit the free-riding problem).

一个 "被动 "的商业公司可能仍然希望鼓励和补贴开源运动，例如，为开源项目分配几个程序员 [^21]。如果 Linux 获得成功，Red Hat 将在支持方面赚取更多的钱。同样，如果逻辑半导体和个人电脑的操作系统是互补的，人们可以通过显露的偏好论证表明，如果 Linux（与 Windows 不同的是免费的）占领了个人电脑操作系统市场，英特尔的利润将会增加。同样地，如果微软的地位被削弱，Sun 公司也会受益。甲骨文公司可能希望将其数据库产品移植到 Linux 环境中，以减少其对 Sun 公司 Solaris 操作系统的依赖性。由于企业不能获得所有的投资收益，创新经济学中经常讨论的搭便车问题在这里也应该适用。商业公司对开源项目的补贴应该是有限的，除非潜在的受益者成功地组织了一个财团（这将限制搭便车的问题）。

A second strategy is to take a more proactive role in the development of open source software. Companies can release existing proprietary code and create some governance structure for the resulting open source process. For example, Hewlett-Packard recently released its Spectrum Object Model-Linker open source in order to help the Linux community port Linux to Hewlett Packard's RISC architecture. They can even (though probably less likely) encourage “ex nihilo” development of new pieces of open source software. This is similar to the strategy of giving away the razor (the released code) to sell more razor blades (the related consulting services that HP will provide).

第二种策略是在开放源码软件的开发中发挥更积极的作用。公司可以发布现有的专有代码，并为由此产生的开放源码过程创建一些管理结构。例如，惠普公司最近发布了它的 Spectrum Object Model-Linker 开放源代码，以帮助 Linux 社区将 Linux 移植到惠普公司的 RISC 架构上。他们甚至可以（虽然可能不太可能）鼓励 "凭空 "开发新的开源软件。这类似于赠送剃刀（发布的代码）以销售更多剃刀片（惠普将提供的相关咨询服务）的策略。

Various efforts by corporations selling proprietary software products to develop additional products through an open source approach have been undertaken. One of the most visible of these efforts was Netscape’s 1998 decision to make “Mozilla,” a portion of its browser source code, freely available. This effort has been so far relatively unsuccessful. Indeed, the Mozilla effort only received approximately two dozen postings by outside developers. Perhaps (and we can only conjecture here), the launching failed because it occurred too late (many exciting tasks had already been completed). It is also likely that Netscape did not adopt the right governance structure. Leadership by a commercial entity may not internalize enough of the objectives of the open source community. In particular, a corporation may not be able to credibly commit to keeping all source code in the public domain and to adequately highlighting important contributions.[^22]

销售专利软件产品的公司已经做出各种努力，通过开放源代码的方式开发更多的产品。这些努力中最引人注目的是网景公司 1998 年决定免费提供 "Mozilla"，即其浏览器源代码的一部分。到目前为止，这一努力还相对不成功。事实上，Mozilla 的努力只收到了外部开发者的大约二十几个帖子。也许（我们在此只能猜测），启动失败是因为它发生得太晚了（许多令人振奋的任务已经完成）。也有可能是网景没有采用正确的管理结构。一个商业实体的领导可能没有将开放源码社区的目标充分内部化。特别是，一个公司可能无法令人信服地承诺将所有的源代码保留在公共领域，并充分强调重要的贡献。[^22]

In this light, it is tempting to interpret the creation of organizations such as Collab.Net as efforts to certify corporate open source development programs, just as investment banks and venture capitalists play a certification role for new firms. Collab.Net, a new venture funded by the venture capital group Benchmark Partners, will organize open source projects for corporations who wish to develop part of their software in this manner. Collab.net will receive fees for its online marketplace (SourceXchange, through which corporations will contact open source developers), for preparing contracts, for helping select and monitor developers, and for settling disputes. Hewlett Packard released the core of its E-speak technology (which enable brokering capabilities) to open source[^23] and posted six projects related to this technology.

有鉴于此，很容易将 Collab.Net 等组织的建立解释为对企业开放源码开发项目进行认证的努力，就像投资银行和风险资本家对新公司发挥认证作用一样。Collab.Net 是一家由风险资本集团 Benchmark Partners 资助的新企业，它将为那些希望以这种方式开发部分软件的企业组织开放源码项目。Collab.net 将为其在线市场（SourceXchange，企业将通过它与开源开发者联系）、准备合同、帮助选择和监督开发者以及解决争端而收取费用。惠普公司将其 E-speak 技术的核心（实现了中介功能）发布为开放源码 [^23]，并公布了与该技术有关的六个项目。

Hewlett Packard's management of the open source process seems consistent with Dessein [1999]. Dessein shows that a principal with formal control rights over an agent's activity in general gains by delegating his control rights to an intermediary with preferences or incentives that are intermediate between his and the agent's. The partial alignment of the intermediary's preferences with the agent's fosters trust and boosts the agent's initiative, ultimately offsetting the partial loss of control for the principal. In the case of Collab.net, the congruence with the open source developers is obtained through the employment of visible open source developers (for example, the president and chief technical officer is Brian Behlendorf, one of the cofounders of the Apache project) and the involvement of O'Reilly, a technical book publisher with strong ties to the open source community.

惠普公司对开源过程的管理似乎与 Dessein[1999] 一致。Dessein 表明，一个对代理人的活动拥有正式控制权的委托人一般会通过将他的控制权委托给一个具有介于他和代理人之间的偏好或激励的中间人而获得收益。中间人的偏好与代理人的偏好部分一致，促进了信任，提高了代理人的主动性，最终抵消了委托人控制权的部分损失。在 Collab.net 的案例中，与开源开发者的一致性是通过雇佣可见的开源开发者（例如，总裁和首席技术官是 Brian Behlendorf，Apache 项目的共同创始人之一）和 O'Reilly 的参与来实现的，O'Reilly 是一家与开源社区有密切联系的技术书籍出版商。

When can it be advantageous for a commercial company to release proprietary code under an open source license? The first condition is, as we have noted, that the company expects to thereby boost its profit on a complementary segment. A second is that the increase in profit in the proprietary complementary segment offsets any profit that would have been made in the primary segment, had it not been converted to open source. Thus, the temptation to go open source is particularly strong when the company is too small to compete commercially in the primary segment or when it is lagging behind the leader and about to become extinct in that segment.[^24]

对于一个商业公司来说，什么时候在开放源码许可证下发布专有代码才是有利的呢？第一个条件是，正如我们所指出的，公司期望因此而提高其在补充部分的利润。第二个条件是，在专有补充部分的利润增长抵消了在主要部分的任何利润，如果它没有被转换为开放源代码的话。因此，当公司规模太小，无法在主要领域进行商业竞争时，或者当它落后于领先者，即将在该领域灭绝时，开放源代码的诱惑力就特别大。[^24]

## 5.3 Can commercial activities pollute the open source process? / 商业活动能否污染开放源码进程？ 

The flexible open source license allows for the coexistence of open and closed source code. While it represents in our view (and in that of many open source participants) a reasonable compromise, it is not without hazards.

灵活的开放源码许可允许开放和封闭源码的共存。虽然在我们看来（也是许多开放源码参与者的看法），这代表了一种合理的妥协，但它也不是没有危险的。

First, the open source project may be “hijacked” by a participant who builds a valuable module and then offers proprietary APIs to which application developers start writing. The innovator has then built a platform that appropriates some of the benefits of the project. To be certain, open source participants might then be outraged, but it is unclear whether this would suffice to prevent the hijacking. The open source community would then be as powerless as the commercial owner of a platform above which a “middleware” producer superimposes a new platform.[^25]

首先，开源项目可能被一个参与者 "劫持"，他建立了一个有价值的模块，然后提供专有的 API，应用程序开发人员开始编写。这样，创新者就建立了一个平台，侵占了项目的一些好处。可以肯定的是，开放源码的参与者可能会被激怒，但不清楚这是否足以阻止劫持行为。这样一来，开源社区就会像平台的商业拥有者一样无能为力，而 "中间件 "生产者则在上面叠加了一个新平台。[^25]

Second, the coexistence of commercial activities may alter the programmers' incentives. To understand why it may be useful to make an analogy with academia (despite some differences between the academic research and open source development processes).

第二，商业活动的并存可能会改变程序员的动机。为了理解原因，与学术界做个类比可能是有用的（尽管学术研究和开放源码开发过程之间有一些差异）。

To put our reflections in perspective, let us first argue against the view that one should prevent academic research from being polluted by outside activities. We believe that these outside activities—e.g., for an economist, work with firms and financial intermediaries and participation in the public policy process; for an engineer, consulting with large firms and part-time work in start-ups—provides a useful two-way transfer of knowledge between practical matters and fundamental research. They also provide academics who desire it with (instantaneous and intertemporal) job diversification and thereby increase the attractiveness of academia. Yet, like many researchers, we are concerned that these outside activities may pollute the research process and make it less attractive. There are several reasons for this.

为了正确看待我们的思考，首先让我们反对这样的观点：我们应该防止学术研究受到外部活动的污染。我们认为，这些外部活动--例如，对经济学家来说，与企业和金融中介机构合作并参与公共政策进程；对工程师来说，为大公司提供咨询并在创业公司兼职--提供了实际事务和基础研究之间有用的双向知识转移。它们还为有此愿望的学者提供（即时和跨时空的）工作多样化，从而增加学术界的吸引力。然而，和许多研究人员一样，我们担心这些外部活动会污染研究过程，使其失去吸引力。这有几个原因。

First, a field may be deprived of some of its best minds if they neglect fundamental research and pursue applied, specific-purpose projects rather than broader, generalpurpose innovations. The field may lose some of its allure as an exciting intellectual environment in which new insights accrue at a rapid pace and a large community that avidly reads about the latest developments.

首先，如果一个领域忽视了基础研究，而追求应用的、特定目的的项目，而不是更广泛的、通用的创新，那么这个领域可能会被剥夺一些最优秀的人才。该领域可能会失去其作为一个令人兴奋的知识环境的一些诱惑力，在这个环境中，新的见解会以很快的速度积累起来，并有一个热衷于阅读最新发展的庞大社区。

Second, the academic process may lose some of its integrity. The high-powered incentives provided by outside activities may induce researchers to sell off some of the long-term reputational capital in the academic community. This happens for instance when a researcher puts his intellectual weight behind a dubious idea, directs students excessively to his or her start-up or consulting firm, rejects papers submitted to scientific journals simply because they do not mesh with the views espoused in the outside activity, or stops freely exchanging knowledge. To be certain, some of these behaviors are already motivated by purely academic incentives. Our point is simply that these may be exacerbated by the presence of powerful outside incentives, and by the shortening of the relationships that results from the move of academics to other communities.

第二，学术过程可能会失去一些完整性。外部活动提供的高权力激励可能会诱使研究人员出卖在学术界的一些长期声誉资本。例如，当一个研究人员把他的智力支持放在一个可疑的想法上，把学生过度地引导到他或她的创业公司或咨询公司，拒绝提交给科学杂志的论文，仅仅因为它们与外部活动中所支持的观点不一致，或者停止自由交流知识，就会发生这种情况。可以肯定的是，这些行为中的一些已经被纯粹的学术动机所驱使。我们的观点是，这些行为可能会因为强大的外部激励因素的存在而加剧，也会因为学术界向其他社区的转移而导致关系的缩短而加剧。

While it is too early to tell, some of these same issues may appear in the open source world. Programmers working on an open source project may be tempted to stop interacting and contributing freely if they think they have an idea for a module that might yield a huge commercial payoff. Too many programmers may start focusing on the commercial side, making the open source process less exciting

虽然现在判断还为时过早，但这些问题中的一些也可能出现在开放源码世界。在一个开源项目上工作的程序员可能会受到诱惑，如果他们认为他们有一个可能产生巨大商业回报的模块的想法，就会停止互动和自由贡献。太多的程序员可能会开始专注于商业方面，从而使开源过程变得不那么令人兴奋。

# 6. What are the Open Economic Questions about Open Source? / 关于开源的公开经济问题有哪些？

There are many other issues posed by open source development that do not lend themselves as neatly to conventional economic frameworks. This section will highlight a number of these as suggestions for future work.

开放源码发展带来的许多其他问题并不像传统的经济框架那样整齐划一。本节将强调其中一些问题，作为对未来工作的建议。

To what extent will reliance on breaking software projects into distinct modules serve to limit the effectiveness of open source? The success of an open source project is dependent on the ability to break the project into distinct components. Without an ability to parcel out work in different areas to programming teams who need little contact with one another, the effort is likely to be unmanageable. Some observers argue that the underlying Unix architecture lent itself well to the ability to break development tasks into distinct components. It may be that as new open source projects move beyond their Unix origins and encounter new programming challenges, the ability to break projects into distinct units will be less possible. But recent developments in computer science and programming languages (e.g., object-oriented programming) have encouraged further modularization, and may facilitate future open source projects.

依靠将软件项目分成不同的模块，在多大程度上会限制开源的有效性？一个开放源码项目的成功取决于将项目分成不同组件的能力。如果没有能力将不同领域的工作分配给不需要相互接触的编程团队，那么工作就可能无法管理。一些观察家认为，底层的 Unix 架构很适合将开发任务分解成不同的组件的能力。可能随着新的开源项目超越其 Unix 的起源并遇到新的编程挑战，将项目分成不同的单元的能力将不太可能。但最近计算机科学和编程语言的发展（例如，面向对象的编程）鼓励了进一步的模块化，并可能促进未来的开源项目。

Can the management of open source projects accommodate the increasing number of contributors? The frequency and quality of contributions to each of the open source projects studied appears to be highly skewed, with a few individuals (or at most a few dozen) accounting for a disproportionate amount of the contributions, with most programmers making just one or two submissions. Many contributors to Sendmail, for instance, are students, who use the open source project as part of their software engineering training. These claims are corroborated by the assessment of over 4000 contributions to a Linux development site by Dempsey, et al. [1999], who conclude that developers of more than two Linux applications, while accounting for only 9% of the overall sample, account for over 38% of the total contributions. If large numbers of lowquality contributions are becoming increasingly common, there may be substantial management challenges in the future.[^26] In this setting, sorting though the large number of software submissions of varying quality is likely to be an increasingly onerous task, one that will swamp the efforts of a volunteer staff. One possibility is the model being adapted by Sendmail, where professional employees of the for-profit firm manage the open source submissions (as well as making their own contribution). But in general, the extent to which individual open source projects can accommodate substantial growth in contributors remains an open question. (At the same time, it must be acknowledged that the same skewness of output is also observed among programmers employed in commercial software development facilities [e.g., see Brooks, 1975].)

开源项目的管理能否适应越来越多的贡献者？在所研究的每个开源项目中，贡献者的频率和质量似乎是高度倾斜的，少数人（或最多几十人）占了不成比例的贡献量，而大多数程序员只提交了一到两次。例如，Sendmail 的许多贡献者是学生，他们把这个开源项目作为他们软件工程培训的一部分。Dempsey 等人 [1999] 对一个 Linux 开发网站的 4000 多份贡献的评估证实了这些说法，他们的结论是：两个以上的 Linux 应用程序的开发者虽然只占整个样本的 9%，但却占了总贡献的 38%以上。如果大量低质量的贡献变得越来越普遍，那么未来可能会有大量的管理挑战 [^26]。在这种情况下，对大量质量参差不齐的软件提交进行分类，可能是一项越来越繁重的任务，这将淹没志愿工作人员的努力。一种可能性是 Sendmail 所采用的模式，即由营利性公司的专业员工来管理开放源码的提交（以及做出自己的贡献）。但总的来说，单个开源项目能在多大程度上适应贡献者的大幅增长仍然是一个开放的问题。（同时，我们必须承认，在商业软件开发设施中雇用的程序员中也观察到了同样的产出偏斜现象 [例如，见 Brooks, 1975]）。

To what extent do open source projects have a greater or shorter effective life span than traditional projects? One of the arguments offered by open source advocates is that because their source code is publicly available, and at least some contributions will continue to be made, its software will have a longer duration. (Many software products by commercial vendors are abandoned or no longer upgraded after the developer is acquired or liquidated, or even when the company develops a new product to replace the old program.) But another argument is that the nature of incentives being offered open source developers—which as discussed above, lead them to work on highly visible projects—might lead to a “too early” abandonment of projects that experience a relative loss in popularity. An example is the XEmacs project, an open source project to create a graphical environment with multiple “windows” that originated at Stanford. Once this development effort encountered an initial decline in popularity, many of the open source developers appeared to move onto alternative projects.

开源项目在多大程度上比传统项目有更大或更短的有效寿命？开放源码倡导者提供的一个论据是，因为他们的源代码是公开的，至少有一些贡献会继续进行，所以它的软件会有更长的持续时间。（许多商业供应商的软件产品在开发商被收购或清算后，甚至在公司开发新产品以取代旧程序时，就被放弃或不再升级）。但另一个论点是，提供给开放源码开发者的激励措施的性质--如上所述，导致他们在高度引人注目的项目上工作--可能会导致 "过早 "放弃那些经历了相对的人气下降的项目。一个例子是 XEmacs 项目，这是一个源于斯坦福大学的开源项目，旨在创建一个具有多个 "窗口 "的图形环境。一旦这个开发工作遇到了最初的人气下降，许多开放源码的开发者似乎就转向了其他项目。

Our ability to answer confidently these and related questions is likely to increase as the open source movement itself grows and evolves. At the same time, it is heartening to us how much of open source activities can be understood within existing economic frameworks, despite the presence of claims to the contrary. The literature on “career concerns” provides a lens through which the structure of open source projects, the role of contributors, and the movement’s ongoing evolution can be viewed.

随着开源运动本身的发展和演变，我们自信地回答这些问题和相关问题的能力可能会提高。同时，尽管存在着与之相反的说法，但开放源码活动有多少可以在现有的经济框架内得到理解，这让我们感到振奋。关于 "职业关注 "的文献提供了一个视角，通过这个视角可以看到开放源码项目的结构、贡献者的作用以及该运动的持续演变。

[^1]: The media like to portray the open source community as wanting to help mankind, as it makes a good story. Many open source advocates put limited emphasis on this explanation. 媒体喜欢把开源社区描绘成想要帮助人类，因为这是个好故事。许多开源倡导者对这种解释的强调是有限的。
[^2]: These are summarized in Darwall and Lerner [2000].  这些都在 Darwall 和 Lerner[2000] 中进行了总结。
[^3]: This history is of necessity highly abbreviated. For more detailed treatments, see Browne [1999], DiBona, Ockman, and Stone [1999], Gomulkiewicz [1999], Levy [1984], and Raymond [1999a].  这段历史必然是高度简略的。更详细的论述，见 Browne [1999], DiBona, Ockman, and Stone [1999], Gomulkiewicz [1999], Levy [1984], and Raymond [1999a].  
[^4]: Programmers write source code using languages such as Basic, C, and Java. By way of contrast, most commercial software vendors only provide users with object, or binary, code. This is the sequence of 0s and 1s that directly communicates with the computer, but which is difficult for programmers to interpret or modify. When the source code is made available to other firms by commercial developers, it is typically licensed under very restrictive conditions. 程序员使用 Basic、C 和 Java 等语言编写源代码。作为对比，大多数商业软件供应商只向用户提供对象或二进制代码。这是与计算机直接通信的 0 和 1 的序列，但程序员很难解释或修改。当商业开发商将源代码提供给其他公司时，通常是在非常严格的条件下授权。
[^5]: It should be noted, however, that some projects, such as the Berkeley Software Distribution (BSD) effort, did take alternative approaches during the 1980s. The BSD license is much less constraining than the GPL: anyone can modify the program and redistribute it for a fee without making the source code freely available. In this way, it was a continuation of the university-based tradition of the 1960s and 1970s.  然而，应该指出的是，一些项目，如伯克利软件发行（BSD）的努力，在 20 世纪 80 年代确实采取了其他方法。BSD 许可证的限制比 GPL 要少得多：任何人都可以修改程序并有偿重新发布，而不需要免费提供源代码。在这方面，它是 1960 年代和 1970 年代基于大学的传统的延续。
[^6]: Two main open source projects (GNOME and KDE) are meant to remedy Linux's handicap on the desktop (mouse and windows interfaces). 两个主要的开源项目（GNOME 和 KDE）是为了弥补 Linux 在桌面上的缺陷（鼠标和窗口界面）。
[^7]: For example, Torvalds [1999] argues that the Linux model works best with developer-type software. Ghosh [1999] views the open source process as a large repeated game process of give-and-take among developer-users (the “cooking pot” model). 例如，Torvalds[1999] 认为 Linux 模式在开发者类型的软件中效果最好。Ghosh[1999] 认为开放源码过程是开发者-用户之间的大型重复博弈过程（"煮锅 "模式）。
[^8]: A complication is introduced by the fact that firewall-protected servers may be quite different in nature. For instance, a survey of both protected and unprotected servers in the summer of 1996 by Zoma Research concluded that open source server programs, including Apache, accounted for only 7% of all installations, far less than the contemporaneous Netcraft estimate. 受防火墙保护的服务器在性质上可能有很大的不同，这就带来了一个复杂的问题。例如，1996 年夏天，Zoma Research 对受保护和不受保护的服务器进行了调查，结论是包括 Apache 在内的开放源码服务器程序只占所有安装量的 7%，远远低于 Netcraft 同期的估计。
[^9]: Linus Torvalds and others have been awarded shares in Linux-based companies that went public. Most certainly, these rewards were unexpected and did not affect the motivation of open source programmers. If this practice becomes “institutionalized,” such rewards will in the future be expected and therefore impact the motivation of open source leaders. Linus Torvalds 和其他人在上市的基于 Linux 的公司中获得了股份。最肯定的是，这些奖励是出乎意料的，并没有影响开放源码程序员的积极性。如果这种做法变得 "制度化"，这种奖励在未来就会被预期，从而影响到开放源代码领导者的积极性。
[^10]: To be certain, commercial firms (e.g., Netscape, Sun, O'Reilly, Transmeta) supporting open source projects are also able to compensate programmers, because they indirectly benefit financially from these projects. Similarly, the government and not-for-profit corporations have done some subsidizing of open source projects. Still, there should be an edge for commercial companies. 可以肯定的是，支持开源项目的商业公司（如 Netscape、Sun、O'Reilly、Transmeta）也能够对程序员进行补偿，因为他们间接地从这些项目中获得经济利益。同样，政府和非营利性公司也对开放源码项目进行了一些补贴。不过，商业公司还是应该有一个优势。
[^11]: While we are here interested in private incentives to participate, note that this complementarity between apprenticeship and projects is socially beneficial. The social benefits might not increase linearly with open source market share, however, since the competing open source projects may end up competing for attention in the same common pool of students. 虽然我们在这里对参与的私人激励感兴趣，但请注意，学徒制和项目之间的这种互补性是有社会效益的。然而，社会效益可能不会随着开源市场份额的增加而线性增长，因为相互竞争的开源项目最终可能会在同一个共同的学生库中争夺注意力。
[^12]: A standard argument in favor of open source processes is their massive parallel debugging. Typically, commercial software firms can only ask users to point at problems: beta testers do not fix the bugs, they just report them. It is also interesting to note that many commercial companies do not discourage their employees from working on open source projects. In many cases where companies encourage such involvement, programmers use open source tools to fix problems. Johnson [1999] builds a model of open source production by a community of user-developers. There is one software program or module to be developed, which is a public good for the potential developers. Each of the potential developers has a private cost of working on the project and a private value of using it; both of which are private information. Johnson shows that the probability that the innovation is made need not increase with the number of developers, as free-riding is stronger when the number of potential developers increases. 支持开放源码进程的一个标准论点是它们的大规模并行调试。通常情况下，商业软件公司只能要求用户指出问题：β测试者不修复错误，他们只是报告它们。同样有趣的是，许多商业公司并不阻止他们的员工参与开放源代码项目的工作。在许多公司鼓励这种参与的情况下，程序员使用开放源码工具来修复问题。Johnson[1999] 建立了一个由用户-开发者组成的社区的开放源码生产模型。有一个待开发的软件程序或模块，这对潜在的开发者来说是一个公共物品。每个潜在的开发者都有在该项目上工作的私人成本和使用它的私人价值；这两者都是私人信息。约翰逊表明，创新的概率不需要随着开发者数量的增加而增加，因为当潜在开发者的数量增加时，搭便车的情况更严重。
[^13]: An argument often heard in the open source community is that people participate in open source projects because programming is fun and because they want to be “part of a team.” While this argument may contain a grain of truth, it is puzzling as it stands; for, it is not clear why programmers who are part of a commercial team could not enjoy the same intellectual challenges and the same team interaction as those engaged in open source development. The argument may reflect the ability of programmers to use participation in open source projects to overcome labor market rigidities that make signaling in other ways problematic. 在开源社区经常听到的一个论点是，人们参与开源项目是因为编程很有趣，因为他们想成为 "团队的一部分"。虽然这个论点可能包含一丝真理，但它是令人费解的；因为，不清楚为什么作为商业团队一部分的程序员不能像从事开源开发的程序员那样享受同样的智力挑战和同样的团队互动。这个论点可能反映了程序员有能力利用参与开放源码项目来克服劳动力市场的僵化，而这种僵化使得以其他方式打信号成为问题。
[^14]: Valloppillil [1998] further argues that reaching commercial grade quality often involves unglamorous work on power management, management infrastructure, wizards, etc., that makes it unlikely to attract open source developers. Valloppillil[1998] 进一步认为，达到商业级别的质量往往涉及到电源管理、管理基础设施、向导等不光彩的工作，这使得它不可能吸引开源开发者。
[^15]: E.g., Valloppillil’s [1998] discussion of the Mozilla release.  例如，Valloppillil 的 [1998] 关于 Mozilla 发布的讨论。
[^16]: See also Hermalin [1998]. 另见 Hermalin [1998]。
[^17]: For instance, concerns about the “poaching” of key employees was one of the reasons cited for Steve Jobs’ recent decision to cease giving credit to key programmers in Apple products [Claymon, 1999].  例如，对 "挖走 "关键员工的担忧是史蒂夫-乔布斯最近决定停止在苹果产品中对关键程序员给予奖励的原因之一 [Claymon, 1999]。
[^18]: Cusamano and Selby [1995], however, document a number of management institutions at Microsoft that attempt to limit these pressures. 然而，Cusamano 和 Selby[1995] 记录了微软公司一些试图限制这些压力的管理制度。
[^19]: Another motivation for commercial companies to interface with the open source world may be public relations. We do not view this as a permanent strategy, however, as programmers and consumers presumably cannot be so easily fooled over an extended period. Similarly, firms may temporarily encourage programmers to participate in open source projects to learn about the strengths and weaknesses of this development approach. 商业公司与开放源代码世界对接的另一个动机可能是公共关系。然而，我们不认为这是一个永久性的策略，因为程序员和消费者不可能在很长一段时间内如此容易被愚弄。同样，公司可以暂时鼓励程序员参与开源项目，以了解这种开发方式的优势和劣势。
[^20]: Red Hat provides support for Linux-based products, while VA Linux provides hardware products optimized for the Linux environment. In December 1999, their market capitalizations were $17 and $10 billion respectively. 红帽公司为基于 Linux 的产品提供支持，而 VA Linux 则提供为 Linux 环境优化的硬件产品。1999 年 12 月，它们的市值分别为 170 亿美元和 100 亿美元。
[^21]: Of course, these programmers also increase the company's “absorptive capacity” and help the company with the development of the proprietary segment.  当然，这些程序员也增加了公司的 "吸收能力"，并帮助公司发展专有部分。 
[^22]: For instance, in the Mozilla project, Netscape’s unwillingness to make large amounts of browser code public was seen as an indication of its questionable commitment to the open source process. In addition, Netscape’s initial insistence on the licensing terms that allowed the corporation to relicense the software developed in the open source project on a proprietary basis was viewed as problematic [Hamerly, Paquin, and Walton, 1999]. The licensing terms however may not have been the hindering factor, since the terms of the final license are even stricter than those of the GPL. 例如，在 Mozilla 项目中，网景公司不愿意公开大量的浏览器代码，这被认为是它对开放源码过程的承诺值得怀疑的表现。此外，网景公司最初坚持的许可条款允许该公司在专有基础上重新许可在开放源码项目中开发的软件，这被认为是有问题的 [Hamerly, Paquin, and Walton, 1999]。然而，许可条款可能不是阻碍因素，因为最终许可的条款甚至比 GPL 的条款更严格。
[^23]: Some of the E-speak code remains proprietary to Hewlett Packard; so will some applications and utilities developed in the future. It should also be noted that HP can profit by providing services to E-speak users, which, while not proprietary, should be an arena in which HP has a natural advantage. 一些 E-speak 代码仍然是惠普公司的专利；未来开发的一些应用程序和实用程序也将如此。还应注意的是，惠普可以通过向 E-speak 用户提供服务而获利，这虽然不是专利，但应该是惠普具有天然优势的领域。
[^24]: See, for example, the discussion of SGI’s open source strategy in Taschek [1999]. 例如，见 Taschek [1999] 中对 SGI 的开放源码战略的讨论。  
[^25]: The increasing number of software patents being granted by the U.S. Patent and Trademark Office provide another avenue through which such a “hijacking” might occur. In a number of cases, industry observers have alleged that patent examiners—not being very familiar with the unpatented “prior art” of earlier software code—have granted unreasonably broad patents, in some cases giving the applicant rights to software that was originally developed through open source processes. 美国专利和商标局授予的越来越多的软件专利提供了另一个可能发生这种 "劫持 "的途径。在一些案例中，行业观察家声称，专利审查员--对早期软件代码中未获专利的 "现有技术 "并不十分熟悉--已经授予了不合理的宽泛专利，在某些情况下，申请人获得了最初通过开放源代码程序开发的软件的权利。
[^26]: Linus Torvalds has succeeded in overseeing the Linux process by delegating to trusted lieutenants who themselves have sub-delegated. 莱纳斯-托瓦兹（Linus Torvalds）通过授权给自己信任的副手，而这些副手自己又转授权，成功地监督了 Linux 进程。
