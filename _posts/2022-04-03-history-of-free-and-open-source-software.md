---
layout: post
title: "【翻译】自由和开源软件的历史"
date: 2022-04-03 20:46 +0800
categories: OpenSource History
comments: true
---

在维基百科上找到一个英文词条 [History of free and open-source software](https://en.wikipedia.org/wiki/History_of_free_and_open-source_software) ，因为无法登录编辑，只能先借助 DeepL 翻译在自己的博客上，以后有机会再转过去。

---

在 20 世纪 50 年代和 60 年代，计算机操作软件和编译器是作为购买硬件的一部分交付的，没有单独的费用。当时，源代码，即软件的人类可读形式，通常与软件一起分发，提供修复错误或增加新功能的能力。 [^1] 大学是计算技术的早期采用者。按照知识共享的学术原则，大学开发的许多修改都是公开共享的，并涌现出一些组织来促进共享。随着大规模操作系统的成熟，允许对操作软件进行修改的组织越来越少，最终这些操作系统被禁止修改。然而，实用程序和其他附加功能的应用程序仍然被共享，新的组织已经形成，以促进软件的共享。

## 1. 软件前的共享技术

自由分享技术信息的概念早在计算机之前就存在了。例如，在汽车发展的早期，有一家企业拥有最初由 George B. Selden 申请的双循环汽油发动机专利的权利。通过控制这项专利，他们能够垄断这个行业，迫使汽车制造商遵守他们的要求，否则就会面临诉讼。1911 年，独立汽车制造商亨利-福特赢得了对塞尔登专利的挑战。结果是，塞尔登专利几乎变得一文不值，一个新的协会（最终成为机动车制造商协会）成立了。新协会在所有美国汽车制造商之间制定了一项交叉许可协议：尽管每个公司都会开发技术并申请专利，但这些专利在所有制造商之间公开共享，没有任何金钱交换。到美国参加第二次世界大战时，92 项福特专利和 515 项其他公司的专利正在这些制造商之间共享，没有任何金钱交换（或诉讼）。[^2]

## 2. 20 世纪 80 年代前的自由软件

在 20 世纪 50 年代到 60 年代，几乎所有的软件都是由学术界和企业研究人员合作生产的，通常作为公共领域的软件共享。因此，它通常是在学术领域长期建立的开放和合作原则下发布的，本身并不被视为一种商品。这种公共行为后来成为所谓的黑客文化（这个词在开源程序员中具有积极的含义）的核心要素。此时，源代码，即软件的人类可读形式，通常与软件的机器代码一起分发，因为用户经常自己修改软件，因为不修改就不能在不同的硬件或操作系统上运行，也可以修复错误或增加新的功能。[^3][^4] 自由和开源软件的第一个例子被认为是 A-2 系统，1953 年由 Remington Rand 的 UNIVAC 部门开发，[^5] 它与源代码一起发布给客户。[^6] 后来，几乎所有的 IBM 大型机软件也都分发了源代码。诸如 IBM 701 的用户组，称为 SHARE，以及数字设备公司（DEC）的用户组，称为 DECUS，都是为了促进软件的交流而成立。SHARE 操作系统最初由通用汽车公司开发，由 SHARE 为 IBM 709 和 7090 计算机分发。一些大学的计算机实验室甚至制定了一项政策，要求所有安装在计算机上的程序都必须带有已公布的源代码文件。[^7]

1969 年，高级研究计划局网络（ARPANET），一个横跨大陆的高速计算机网络被建成。该网络（后来被互联网所取代）简化了软件代码的交流。[^3]

一些在 1970 年代开发的自由软件继续被开发和使用，如 TeX（由 Donald Knuth 开发）[^8] 和 SPICE。[^9]

### 2.1. 自由软件的最初衰退

到 20 世纪 60 年代末，变化正在到来：随着操作系统和编程语言编译器的发展，软件生产成本相对于硬件来说正在急剧增加。一个不断发展的软件产业正在与硬件制造商的捆绑式软件产品竞争（捆绑式产品的成本包含在硬件成本中），租赁的机器需要软件支持，但却没有为软件提供收入，一些客户能够更好地满足自己的需求，[^10] 不希望制造商的软件成本与硬件产品成本捆绑在一起。在 1969 年 1 月 17 日提起的美国对 IBM 的反垄断诉讼中，美国政府指控捆绑式软件是反竞争的。[^11] 虽然有些软件仍然是免费的，但有越来越多的软件只在限制性许可下出售。

在 1970 年代早期，AT&T 免费向政府和学术研究人员分发了早期版本的 Unix，但这些版本并不允许重新发布或分发修改过的版本，因此不是现代意义上的自由软件。在 20 世纪 80 年代初 Unix 变得更加普及之后，AT&T 停止了免费分发，并对系统补丁收费。由于切换到另一个架构是相当困难的，大多数研究人员都支付了商业许可证。

在 1974 年美国版权作品新技术使用委员会（CONTU）决定“计算机程序，只要体现了作者的原创，就是适当的版权主题”之前，软件并不被认为是可版权的。 [^12][^13] 因此，软件没有附加许可证，而是作为公共领域的软件共享，通常带有源代码。CONTU 的判决加上后来的法院判决，如 1983 年苹果诉富兰克林案中的目标代码，使计算机程序获得了文学作品的版权地位，并开始了软件的许可和收缩包装的封闭式软件商业模式。[^14]

在 20 世纪 70 年代末和 80 年代初，计算机供应商和纯软件公司开始例行收取软件许可费，将软件作为“程序产品”进行营销，并通过版权、商标和租赁合同对新的软件开发施加法律限制，现在这些软件被视为资产。1976 年，比尔-盖茨写了一篇题为“致业余爱好者的公开信”的文章，其中他对业余爱好者广泛分享微软的产品 Altair BASIC 而不支付其许可费表示失望。1979 年，当 AT&T 公司决定通过出售 Unix 系统获利时，开始强制执行其许可证。 [^15] 在 1983 年 2 月 8 日的一封公告信中，IBM 开始执行一项政策，即不再随购买的软件分发源代码。[^16][^17]

为了增加收入，一个普遍的趋势是开始不再分发源代码（容易被程序员阅读），而只分发从源代码编译出来的可执行机器代码。有一个人对这种新做法感到特别痛苦，他就是理查德-斯塔尔曼。他担心自己不能再研究或进一步修改最初由他人编写的程序。Stallman 认为这种做法在道德上是错误的。作为回应，他在 1983 年创立了 GNU 项目，以便人们可以只使用自由软件来使用计算机。[^1] 他在 1985 年成立了一个非营利组织--自由软件基金会，以便更正式地组织该项目。他发明了 copyleft，一种保护受版权保护的作品的“自由”状态的法律机制，并在 GNU 通用公共许可证中加以实施。Copyleft 许可证允许作者授予用户一些权利（包括在不进一步收费的情况下使用作品的权利，以及获得、研究和修改程序完整的相应源代码的权利），但要求衍生品保持在相同的许可证或没有任何额外限制的许可证下。由于衍生品包括与其他原始程序的组合，下游作者被阻止将最初的作品变成专有软件，并被邀请为 copyleft 公共资源做出贡献。[^3] 后来，其他人开发了这种许可证的变体。

## 3. 20 世纪 80 年代和 90 年代

### 3.1. 非正式的软件共享继续进行

然而，仍有一些人希望与其他程序员和/或用户免费分享他们的源代码，他们当时被称为“业余爱好者”和“黑客”。[^18] 在互联网的引入和广泛的公众使用之前，有几种可供选择的方式，包括在计算机杂志（如 Dr. Dobb's Journal, Creative Computing, SoftSide, Compute! [^19] 虽然仍有版权，但雅达利 8 位家庭系统软件的关键组件的注释源代码在大众市场书籍中出版，包括《雅达利 BASIC 源码书》[^20] （雅达利 BASIC 的完整源代码）和《雅达利 DOS 内部》（雅达利 DOS 的完整源代码）。[^21]

#### 3.1.1. SHARE 程序库

SHARE 用户组，成立于 1955 年，开始收集和分发自由软件。SHARE 第一个有记录的分发日期是 1955 年 10 月 17 日。[^22] “SHARE 计划图书馆机构”（SPLA）分发信息和软件，特别是磁带。

#### 3.1.2. DECUS 磁带

在 20 世纪 80 年代早期，所谓的 DECUS 磁带 [^23] 是一个为 DEC 设备的用户传输免费软件的世界性系统。操作系统通常是专有软件，但许多工具，如 TECO 编辑器、Runoff 文本格式化器或 List 文件列表工具等被开发出来，使用户的生活更容易，并在 DECUS 磁带上分发。这些实用程序包使 DEC 受益，有时将它们纳入他们专有操作系统的新版本中。甚至编译器也可以被分发，例如 Ratfor（和 Ratfiv）帮助研究人员从 Fortran 编码转向结构化编程（抑制 GO TO 语句）。1981 年的 Decus 磁带可能是最具创新性的，它带来了劳伦斯伯克利实验室软件工具虚拟操作系统，允许用户在 DEC 16 位 PDP-11s 和 32 位 VAXs 上使用类似 Unix 的系统，在 VMS 操作系统下运行。它类似于目前 Windows 的 cygwin 系统。二进制文件和库经常被分发，但用户通常倾向于从源代码进行编译。

#### 3.1.3. 1980 年代的在线软件共享社区

在 20 世纪 80 年代，与自由软件运动平行，带源代码的软件在 BBS 网络上被分享。这有时是一种需要；用 BASIC 和其他解释语言编写的软件只能以源代码的形式发布，而且大部分是免费软件。当用户开始收集这些源代码，并建立专门讨论其修改的板块时，这就是一个事实上的开源系统。

其中一个最明显的例子是最常用的 BBS 系统和网络之一，WWIV，最初由 Wayne Bell 用 BASIC 开发。一种“修改”他的软件并分发修改的文化如此广泛地发展起来，以至于当该软件首先被移植到 Pascal，然后被移植到 C++时，它的源代码继续被分发到注册用户，他们会分享修改并编译他们自己版本的软件。这可能有助于它成为一个占主导地位的系统和网络，尽管它不在 Fidonet 的保护伞下，而 Fidonet 是许多其他 BBS 制作者所共享的。

同时，20 世纪 80 年代初 Usenet 和 UUCPNet 的出现进一步连接了编程社区，并为程序员提供了一种更简单的方式来分享他们的软件和贡献于其他人编写的软件。[^24]

### 3.2. 自由软件运动的发起

1983 年，Richard Stallman 发起了 GNU 项目，旨在编写一个不受源代码使用限制的完整操作系统。促使这一点的具体事件包括：一个恼人的打印机因为源代码被扣留而无法修复。[^25] Stallman 还在 1985 年发表了 GNU 宣言，概述了 GNU 项目的目的并解释了自由软件的重要性。GNU 项目及其宣言的另一个可能的灵感是 Stallman 和 Symbolics, Inc. 之间关于 MIT 对 Symbolics 对其 Lisp 机器的更新的访问权的分歧，该机器是基于 MIT 的代码。[^26] 在启动后不久，他 [^18] 使用现有的术语“自由软件”，并成立了自由软件基金会来推广这一概念。《自由软件定义》于 1986 年 2 月出版。

1989 年，GNU 通用公共许可证的第一个版本发布。[^27] 1991 年发布了稍微更新的第二版。1989 年，一些 GNU 开发者成立了 Cygnus Solutions 公司。[^28] GNU 项目的内核（后来被称为 “GNU Hurd”）不断被推迟，但大多数其他组件都在 1991 年之前完成。其中一些，特别是 GNU 编译器集，已经成为市场的领导者。GNU Debugger 和 GNU Emacs 也取得了显著的成功。

### 3.3. Linux (1991 年至今）

由 Linus Torvalds 发起的 Linux 内核于 1991 年作为可自由修改的源代码发布。该许可证不是自由软件许可证，但在 1992 年 2 月的 0.12 版本中，Torvalds 以 GNU 通用公共许可证重新许可了该项目。[^29] 与 Unix 一样，Torvalds 的内核吸引了志愿程序员的注意。

在这之前，GNU 项目没有内核意味着不存在完整的自由软件操作系统。Torvalds 内核的开发弥补了这最后的空白。几乎完成的 GNU 操作系统和 Linux 内核的结合，形成了第一个完整的自由软件操作系统。

在 Linux 发行版中，由 Ian Murdock 于 1993 年开始的 Debian GNU/Linux 值得注意的是，它明确地致力于 GNU 和 FSF 的自由软件原则。Debian 开发者的原则在蝶变社会契约中得到了体现。从一开始，Debian 项目就与自由软件基金会有密切的联系，事实上，在 1994-1995 年间，它曾被自由软件基金会赞助过一年。1997 年，前 Debian 项目负责人 Bruce Perens 也帮助创立了 Software in the Public Interest，一个为各种自由软件项目提供资金和支持的非营利组织。[^30]

自 1996 年以来，Linux 内核包含了专有的许可组件，因此它不再是完全的自由软件。[^31] 因此，拉丁美洲自由软件基金会在 2008 年发布了 Linux-内核的修改版本，称为 Linux-libre，其中所有专有和非自由组件被删除。

许多企业提供基于 Linux 的定制产品，或发行版，并提供商业支持。命名仍然是有争议的。将整个系统简单地称为“Linux”是常见的用法。然而，自由软件基金会和许多其他组织主张使用“GNU/Linux”这一术语，说它是整个操作系统的一个更准确的名称。[^32]

20 世纪 90 年代和 2000 年，Linux 在企业和政府中的应用越来越多。至少在英语世界中，Ubuntu 及其衍生产品成为了一个相对流行的 Linux 发行版群体。

### 3.4. FreeBSD(1993 年至今）

1993 年，当 USL 诉 BSDi 的诉讼案庭外和解后，FreeBSD 和 NetBSD（都源自 386BSD) 作为自由软件被发布。1995 年，OpenBSD 从 NetBSD 分叉出来。2004 年，Dragonfly BSD 从 FreeBSD 分叉出来。

### 3.5 网络时代 (1990 年代末）

在 90 年代中后期，当许多基于网站的公司开始起步时，自由软件成为网络服务器的流行选择。Apache HTTP 服务器成为使用最多的网络服务器软件，这个称号到 2015 年仍然保持着。[^33] 以 Linux 内核为基础，Apache 提供网络服务，MySQL 数据库引擎用于数据存储，PHP 编程语言用于提供动态网页的通用“堆栈”软件为基础的系统被称为 LAMP 系统。实际上，在 PHP 之前的编程语言是 Perl，它在 20 世纪 90 年代中期和后期主导着网络。网络表格是通过用 Perl 编写的通用网关接口脚本在服务器端处理的。

### 3.6 开放源码的推出

1997 年，Eric S. Raymond 发表了《大教堂与集市》，对黑客社区和自由软件原则进行了反思性分析。这篇论文在 1998 年初受到了极大的关注，也是促使网景通信公司将其流行的网景通讯器互联网套件作为自由软件发布的因素之一。[^34]

网景公司的行为促使雷蒙德和其他人研究如何将自由软件的原则和好处带到商业软件行业。他们的结论是，自由软件基金会的社会行动主义对像网景这样的公司没有吸引力，并寻找一种方法来重塑自由软件运动的品牌，以强调共享源代码的商业潜力。[^35]

自由软件运动中的一些人在一次战略会议 [^36] 上采用了“开放源码”的标签，该会议在加利福尼亚的帕洛阿尔托举行，是对网景公司 1998 年 1 月宣布发布 Navigator 的源代码的反应。参加会议的人包括提出“开放源码”的 Christine Peterson、[^1] Todd Anderson、Larry Augustin、Jon Hall、Sam Ockman、Michael Tiemann 和 Eric S. Raymond。在接下来的一周里，雷蒙德和其他人致力于传播这个词。Linus Torvalds 在第二天进行了一次重要的制裁。菲尔-休斯在 Linux 杂志上提供了一个讲坛。自由软件运动的先驱 Richard Stallman 曾想采用这个词，但他改变了主意。[^36] 那些采用这个词的人利用 Navigator 源代码发布前的机会，将自己从“自由软件”这个词的意识形态和对抗性含义中解放出来。网景公司以网景公共许可证和后来的 Mozilla 公共许可证发布了其源代码。[^37]

这个词在 1998 年 4 月由技术出版商 Tim O'Reilly 组织的一次活动中得到了极大的推动。该活动最初名为“自由软件峰会”，后来被命名为“开源峰会”，[^38] 该活动聚集了许多最重要的自由和开源项目的领导人，包括 Linus Torvalds、Larry Wall、Brian Behlendorf、Eric Allman、Guido van Rossum、Michael Tiemann、Paul Vixie、Netscape 的 Jamie Zawinski 和 Eric Raymond。在那次会议上，有人提出了自由软件这一名称所引起的混乱。Tiemann 主张用“sourceware”作为新的术语，而 Raymond 则主张用“open source”。参加会议的开发人员进行了投票，并在当晚的新闻发布会上宣布了获胜者。五天后，雷蒙德首次公开呼吁自由软件社区采用新的术语。[^39] 此后不久，开放源码组织成立。[^1][^36] 根据开放源码组织的说法，理查德-塔尔曼最初曾对采用开放源码术语的想法进行过调侃。[^40] 但由于开源术语的巨大成功埋没了 Stallman 的自由软件术语及其关于社会价值和计算机用户自由的信息，[^41][^42][^43] 后来 Stallman 和他的 FSF 强烈反对 OSI 的做法和术语。[^44] 由于 Stallman 拒绝“open source”一词，FOSS 生态系统在其术语上出现分歧；另见自由软件的替代术语。例如，2002 年的一项自由软件开发者调查显示，32.6%的人将自己与开放源码软件联系在一起，48%的人与自由软件联系在一起，19.4%的人介于两者之间或未作决定。[^45] 然而，Stallman 仍然坚持认为，每个术语的使用者都是反对专利软件的盟友。

2000 年 10 月 13 日，Sun Microsystems 公司在 GNU Lesser General Public License 下将 StarOffice 办公套件作为自由软件发布。这个自由软件版本被重新命名为 OpenOffice.org，并与 StarOffice 共存。

到 20 世纪 90 年代末，在网络泡沫和开源软件驱动的 Web 2.0 背景下“开源”一词在公共媒体 [^46] 中获得了很大的吸引力，并被软件行业所接受。

## 4. 桌面 (1984 年至今）

X 窗口系统创建于 1984 年，并在 1990 年代中期成为桌面自由软件操作系统中事实上的标准窗口系统。X 作为一个服务器运行，负责代表客户（即单个软件应用程序）与图形硬件进行通信。它提供了一些有用的服务，如为同一显示器提供多个虚拟桌面，并在网络上传输视觉数据，以便可以远程访问一个桌面。

最初，用户或系统管理员用 X 和可用的窗口管理器（为应用程序窗口添加标准控件；X 本身不做这个）、寻呼机、码头和其他软件组装他们自己的环境。虽然 X 可以在没有窗口管理器的情况下操作，但有一个窗口管理器可以大大增加便利性和易用性。

20 世纪 90 年代出现了两个关键的自由软件操作系统的“重量级”桌面环境，被广泛采用。KDE 和 GNOME。KDE 是由 Matthias Ettrich 在 1996 年创立的。当时，他被 UNIX 应用程序的用户界面的不一致性所困扰。他提出了一个新的桌面环境。他还想使这个桌面易于使用。他最初的 Usenet 帖子激发了很多人的兴趣。[^47]

Ettrich 选择在 KDE 项目中使用 Qt 工具箱。当时，Qt 并没有使用自由软件许可证。GNU 项目的成员开始关注使用这样一个工具包来建立一个自由软件的桌面环境。1997 年 8 月，两个项目被启动以回应 KDE：Harmony 工具包（Qt 库的免费替代品）和 GNOME（没有 Qt 的不同桌面，完全建立在自由软件之上）。[^48] GTK+被选为 GNOME 的基础，取代了 Qt 工具包。

1998 年 11 月，Qt 工具包在自由/开源的 Q 公共许可证（QPL）下被授权，但关于与 GNU 通用公共许可证（GPL）的兼容性的争论仍在继续。2000 年 9 月，Trolltech 公司除了 QPL 之外，还在 GPL 下提供了 Unix 版的 Qt 库，这消除了自由软件基金会的担忧。此后，KDE 被拆分为 KDE Plasma Workspaces（一个桌面环境）和 KDE Software Compilation（一个包括桌面环境的更广泛的软件集）。

KDE 和 GNOME 现在都参加了 freedesktop.org，这是一个在 2000 年发起的标准化 Unix 桌面互操作性的努力，尽管它们之间仍然存在着竞争。[^49]

自 2000 年以来，为 X 编写的软件几乎总是使用一些写在 X 之上的部件工具包，如 Qt 或 GTK。

2010 年，Canonical 发布了 Unity 的第一个版本，取代了之前 Ubuntu 的默认桌面环境，即 GNOME。这种向新的、正在开发中的桌面环境和用户界面的改变最初在 Ubuntu 用户中引起了一些争议。

2011 年，GNOME 3 问世了，它在很大程度上抛弃了桌面隐喻，而采用了更加面向移动的界面。随之而来的争议导致 Debian 考虑在 Debian 7 上默认使用 Xfce 环境。几个独立项目开始继续维护 GNOME 2 的代码。

Fedora 没有采用 Unity，保留了其现有的 GNOME、KDE 和 LXDE 的选择，GNOME 是默认的，因此 Red Hat Enterprise Linux（Fedora 作为其“初始测试场”）也没有采用 Unity。有兴趣的第三方开发者对 Ubuntu 进行了分叉，保留了 GNOME，抛弃了 Unity。2017 年 3 月，Ubuntu 宣布它将在未来的版本中放弃 Unity，转而采用 GNOME 3，并停止开发基于 Unity 的智能手机和平板电脑。[^50][^51]

当谷歌建立了基于 Linux 的安卓操作系统，主要用于手机和平板设备时，它用特制的 SurfaceFlinger 取代了 X。

开源开发者也批评 X 已经过时，在其协议和库中携带了许多未使用的或过于复杂的元素，同时缺少现代功能，如合成、屏幕保护程序和窗口管理器提供的功能。[^52] 由于这些原因，已经或正在进行一些尝试来取代 X，包括：

* Y 窗口系统，到 2006 年已经停止了开发 [^53] 。
* Wayland 项目，开始于 2008 年。
* Mir 项目，由 Canonical Ltd. 于 2013 年启动，旨在为 Ubuntu 制作一个替代的窗口系统。

## 5. 微软、SCO 和其他攻击 (1998-2014)

随着自由软件变得越来越流行，微软等行业现任者开始把它看作是一个严重的威胁。这一点在 1998 年泄露的一份文件中得到了体现，该文件被微软证实是真实的，被称为“万圣节文件”。

史蒂夫-鲍尔默曾经把 GPL 比作“癌症”，但后来不再使用这个比喻。事实上，微软已经软化了它对开放源代码的公开立场，开放源代码已经成为微软 Windows 生态系统的一个重要组成部分。然而，与此同时，在幕后，微软的行动对开源社区也不那么有利了。

### 5.1. SCO 诉 IBM 和相关的不良宣传（2003 年至今）

2003 年，一家名为 SCO 的专有 Unix 供应商和前 Linux 发行商声称，Unix 的知识产权被不适当地复制到 Linux 内核中，并起诉了 IBM，声称它对此负有责任。一些相关的诉讼和反诉讼接踵而至，有些来自 SCO，有些来自其他起诉 SCO 的人。然而，SCO 的指控缺乏具体内容，虽然一些媒体报道说它们是可信的，但 SCO 的许多批评者认为这些指控充其量也是非常可疑的。

在 SCO 诉 IBM 一案的过程中，人们发现，不仅 SCO 多年来一直在 GPL 下发布 Linux 内核，并继续这样做（从而使任何索赔在法律上难以成立），而且 SCO 甚至不拥有它所主张的许多 Unix 代码的版权，也无权代表推定的所有者 Novell 对它们提出起诉。

尽管 SCO 的首席执行官达尔-麦克布赖德向媒体提出了许多关于不适当的侵占的疯狂和破坏性的主张，其中许多后来被证明是虚假的，或者即使是真实的，也与法律无关。

博客 Groklaw 是对 SCO 的索赔和相关事件的最法证的审查者之一，多年来通过报道这些材料获得了知名度。

在 SCO 诉 IBM 及其他各种法庭案件中，SCO 遭受了一次又一次的失败，并在 2007 年申请了破产保护。然而，尽管法院发现 SCO 并不拥有版权（见上文），而且 SCO 喜欢打官司的首席执行官 Darl McBride 不再管理公司，负责 SCO 破产的破产管理人决定继续进行他声称与 SCO 诉 IBM 的诉讼有关的一些部分。他显然有能力这样做，因为在 SCO 诉 IBM 一案中，SCO 的主要律师事务所在一开始就签署了一份协议，无论案件完成需要多长时间，都将以固定金额代表 SCO。

2004 年，亚历克西斯-德-托克维尔研究所（ADTI）宣布打算出版一本名为《萨米兹达特》的书。以及其他关于开放源代码“来源”的问题，表明 Linux 内核是基于从 Unix 窃取的代码，实质上是用这样的论点：不可能相信 Linus Torvalds 能产生像 Linux 内核这样复杂的东西。这本书从未出版，因为它受到了广泛的批评和嘲弄，包括据称为该书接受采访的人。后来发现，其中一些人从来没有接受过采访，而且 ADTI 也没有试图联系 Linus Torvalds，或者向他提出这些指控，让他做出回应。微软试图为这一事件划清界限，说这是一个“分心”。

许多人怀疑这些针对 Linux 内核的法律和恐惧、不确定性和怀疑（FUD）的攻击，有些或全部是微软暗中安排的，尽管这从未被证实。然而，ADTI 和 SCO 都得到了微软的资助。

### 5.2. 欧盟委员会诉微软 (2004-2007)

2004 年，欧盟委员会认定微软在工作组软件市场的互操作性方面存在反竞争行为。微软曾在 2001 年解决了美国诉微软一案，该案指控微软非法滥用其垄断权力，强迫计算机制造商预装 IE 浏览器。

委员会要求微软提供其工作组协议的全部文件，以允许竞争者与其工作组软件进行互操作，并对微软的不遵守行为每天处以 150 万欧元的罚款。该委员会有管辖权，因为微软在欧洲销售有关软件。

微软在试图通过欧盟法院对该决定提出上诉失败后，最终遵守了该要求，制作了大量的详细文件。

Samba 项目作为微软在工作组软件市场上仅存的竞争对手，是这些文件的主要受益者。

### 5.3. ISO OOXML 的争论（2008 年至今）

2008 年，国际标准化组织将微软的 Office Open XML 公布为国际标准，这关键性地意味着它，以及微软的 Office，可以在法律或政策规定使用开放标准的项目中使用。对标准化过程的批评者，包括参与该过程本身的 ISO 国家委员会的一些成员，指称该过程中存在违规和违反程序的情况，并认为 ISO 不应该批准 OOXML 作为标准，因为它参考了未记录的微软 Office 行为。

截至 2012 年，OOXML 没有正确的开源实现，这验证了批评者关于 OOXML 难以实现和规范性不足的言论。目前，谷歌还不能将 Office 文档正确地转换为其专有的 Google Docs 格式。这表明 OOXML 不是一个真正的开放标准，而是一个描述微软 Office 的部分文件，而且只涉及某些文件格式。

### 5.4. 微软对开源的贡献和对相关项目的收购

2006 年，微软推出了 CodePlex 开放源代码托管网站，为针对微软平台的开放源代码开发者提供托管。2009 年 7 月，微软甚至对 Linux 内核开放了一些支持 Hyper-V 的补丁，因为 GNU 通用公共许可证要求他们这样做，[^54][^55] 并将它们贡献给主线内核。请注意，Hyper-V 本身并不是开源的。微软的 F#编译器，创建于 2002 年，也已经在 Apache 许可下作为开源发布。F#编译器是一个商业产品，因为它已经被纳入了微软的 Visual Studio，而 Visual Studio 不是开源的。

多年来，微软代表经常在各种开源和 Linux 会议上露面。

2012 年，微软成立了一个名为微软开放技术公司的子公司，目的是通过参与开源标准，弥合微软专有技术和非微软技术之间的差距。[^56] 这个子公司后来被折回微软，因为微软在开源和非 Windows 平台上的立场变得更加有利。

2016 年 1 月，微软在 MIT 许可下将 Chakra 作为开放源代码发布；代码可在 GitHub 上获得。[^57]

随着公司开始认可更多的开源软件，微软对开源的立场也发生了转变。2016 年，微软前首席执行官史蒂夫-巴尔默（Steve Balmer）已经收回了他关于 Linux 是恶性癌症的声明。[^58] 2017 年，该公司成为 Linux 基金会的白金级支持者。到了 2018 年，在收购 GitHub 前不久，微软在那里为开源项目做出贡献的付费员工数量居于榜首。[^59] 虽然微软可能赞同也可能不赞同自由软件的原始理念，但数据显示，它确实在战略上赞同开源。

批评者指出，2019 年 3 月，微软就 2013 年的一份专利合同起诉了富士康的子公司；[^60] 2013 年，微软曾宣布与富士康达成专利协议，与富士康使用基于 Linux 的 Android 和 Chrome OS 有关。[^61]

## 6. 开源和编程语言

今天使用的绝大多数编程语言都有一个免费的软件实现。

自 20 世纪 90 年代以来，以开源编译器和/或解释器的形式发布主要的新编程语言已经成为常态，而不是例外。例子包括 1991 年的 Python，1995 年的 Ruby 和 2003 年的 Scala。近来，最明显的例外是 Java、ActionScript、C#和苹果的 Swift，直到 2.2 版都是专有的。大部分都开发了部分兼容的开源实现，就 Java 而言，主要的开源实现现在已经非常接近于商业版本。

### 6.1. Java

自 1996 年首次公开发布以来，Java 平台一直没有开放源代码，尽管 Java 运行时的源代码部分被包含在 Java 开发工具包（JDK）中，据称是在“保密”的基础上，尽管在大多数国家公众都可以免费下载。后来，Sun 公司扩大了这种“机密”源代码的访问范围，通过一个单独的程序将 Java 运行时环境的全部源代码开放给公众，后来还提供了 Java 编译器 javac 的源代码。Sun 还向 Blackdown Java 项目秘密提供了 JDK 源代码，该项目是一个志愿者的集合，他们将 JDK 的早期版本移植到 Linux 上，或者在 Sun 的 JDK 的 Linux 端口上进行改进。然而，这一切都不是开源的，因为在所有情况下，未经 Sun 公司许可的修改和再分配都是被禁止的。Sun 当时表示，他们关注的是如何防止 Java 平台的分叉。

然而，几个独立的 Java 平台的部分重新实现已经被创建，其中许多是由开源社区创建的，如 GNU Compiler for Java（GCJ）。太阳公司从未对任何一个开放源码克隆项目提起过诉讼。值得注意的是，GCJ 在支持自由软件的发行版上给 Java 带来了不好的用户体验，如 Fedora 和 Ubuntu，它们当时将 GCJ 作为它们的 Java 实现。如何用 Sun JDK 取代 GCJ 是用户经常问到的问题，因为 GCJ 是一个不完整的实现，不兼容且有错误。

2006 年，Jonathan I. Schwartz 成为 Sun Microsystems 的 CEO，并表明了他对开源的承诺。2007 年 5 月 8 日，Sun Microsystems 在 GNU 通用公共许可证下将 Java 开发工具包作为 OpenJDK 发布。部分类库（4%）不能作为开源发布，因为它们是由其他方授权的，并作为二进制插件包含在内。正因为如此，在 2007 年 6 月，Red Hat 推出了 IcedTea，用 GNU Classpath 实现的等价物来解决这些受保护的组件。自从发布以来，大部分的负担已经解决了，只剩下音频引擎代码和颜色管理系统（后者将使用 Little CMS 来解决）。

## 7. 分布式版本控制 (2001 年至今）

第一个开源的分布式修订控制系统（DVCS）是 2001 年的“tla”（后来改名为 GNU arch）；然而，它和它的后继者“baz”和“bzr”（Bazaar）从未变得非常流行，GNU arch 也被停止了，尽管 Bazaar 仍在继续，并被 Canonical 使用。

然而，其他 DVCS 项目如雨后春笋般涌现，一些项目开始得到大量采用。

### 7.1. Git (2005 年至今）

Git 是最流行的 DVCS，创建于 2005 年。[^62] 一些 Linux 内核的开发者开始使用一个名为 BitKeeper 的专有 DVCS，特别是 Linux 创始人 Linus Torvalds，尽管其他一些内核开发者由于其专有性质而从未使用过它。当 Andrew Tridgell 开始对 BitKeeper 进行逆向工程，目的是制作一个能够提供与商业版本相同功能的开源工具时，Linux 内核开发涉及一些专有软件的不寻常情况“出现了”。BitMover，开发 BitKeeper 的公司，作为回应，在 2005 年取消了它给予某些内核开发者的特殊免费许可。

由于 BitKeeper 许可证的取消，Linus Torvalds 决定编写自己的 DVCS，称为 git，因为他认为现有的开源 DVCS 都不适合他作为内核维护者的特殊需要（这就是他首先采用 BitKeeper 的原因）。其他一些开发者迅速加入并帮助他，随着时间的推移，git 从一个相对简单的“愚蠢的内容跟踪器”（一些开发者在此基础上开发了“porcelain”扩展）成长为今天复杂而强大的 DVCS。然而，Torvalds 不再亲自维护 git；多年来，它一直由 Junio Hamano 维护，并不断收到许多开发者的贡献。

git 等开源 DVCS 的日益普及，以及后来 DVCS 托管网站的出现，其中最受欢迎的是 GitHub（成立于 2008 年），进一步降低了参与自由软件项目的障碍。有了 GitHub 这样的网站，潜在的贡献者不再需要做一些事情，比如寻找源代码仓库的 URL（它可能在每个网站的不同地方，或者有时隐藏在 README 文件或开发者文档中），或者研究如何生成一个补丁，如果有必要的话，还要订阅正确的邮件列表，以便他们的补丁邮件能够到达正确的人手中。贡献者可以简单地一键分叉自己的仓库副本，当他们的改动准备好了，就从相应的分支发出拉动请求。GitHub 已经成为世界上最受欢迎的开源软件托管网站，再加上分叉的便利性和分叉的可见性，使得它成为贡献者进行大大小小修改的热门方式。

## 8. 最近的发展

虽然版权是自由软件作者用来确保其软件符合许可证要求的主要法律机制，但其他机制，如立法、软件专利和商标也有用途。为了应对专利和 DMCA 的法律问题，自由软件基金会在 2007 年发布了 GNU 公共许可证的第三版，其中明确提到了 DMCA 的数字版权管理（DRM）条款和专利权。

在 GNU GPLv3 制定之后，作为 GNU 系统许多部分的版权持有人，如 GNU 编译器集合（GCC）软件，FSF 将大部分 GNU 程序的许可证从 GPLv2 更新到 GPLv3。苹果公司是 GCC 的用户，也是 DRM 和专利的重度使用者，它决定将其 Xcode IDE 中的编译器从 GCC 换成 Clang，这是另一个 FOSS 的编译器，[^63] 但它是在一个允许性的许可之下。[^64] LWN 推测，苹果的部分动机是希望避免 GPLv3。[^65]

最近的兼并影响了主要的开源软件。太阳微系统公司（Sun）在 2008 年收购了流行的开源 MySQL 数据库的所有者 MySQL AB。[^66]

甲骨文公司又于 2010 年 1 月收购了 Sun，获得了他们的版权、专利和商标。这使甲骨文成为最受欢迎的专有数据库和最受欢迎的开源数据库（MySQL）的所有者。甲骨文试图将开源的 MySQL 数据库商业化，引起了自由软件社区的关注。[^67] 部分是为了应对 MySQL 未来的不确定性，自由软件社区将该项目分叉到甲骨文控制之外的新数据库系统。这些系统包括 MariaDB、Percona 和 Drizzle。[^68] 所有这些都有独特的名称；它们是不同的项目，不能使用 MySQL 这个商标名称。[^69]

### 8.1. 安卓 (2008 年至今）

2008 年 9 月，谷歌发布了第一个版本的安卓系统，这是一个新的智能手机操作系统，作为开放源码（一些有时但不总是与安卓系统捆绑的谷歌应用程序不是开放源码）。最初，该操作系统由谷歌免费赠送，并被许多手机制造商踊跃采用；谷歌后来收购了摩托罗拉移动，生产自己的“香草”安卓手机和平板电脑，同时继续允许其他制造商使用安卓。现在，安卓是世界上最流行的移动平台。[^70]

由于安卓系统是基于 Linux 内核，这意味着 Linux 现在是移动平台（通过安卓系统）和超级计算机的主导内核，[^71] 也是服务器操作系统的关键角色。

#### 8.1.1. 甲骨文诉谷歌

2010 年 8 月，甲骨文起诉谷歌，称其在 Android 中使用的 Java 侵犯了甲骨文的版权和专利。甲骨文诉谷歌的初次审判于 2012 年 5 月结束，认定谷歌没有侵犯甲骨文的专利权，审判法官裁定谷歌使用的 Java 应用编程接口（API）的结构不具有版权。陪审团认为谷歌做出了微不足道的（“de minimis”）版权侵权行为，但双方约定谷歌将不支付赔偿金，因为它是如此微不足道。[^72] 然而，甲骨文向联邦巡回法院提出上诉，谷歌就字面复制索赔提出了交叉上诉。[^73] 联邦巡回法院裁定，谷歌承认的微小版权侵权行为并非微不足道，并将合理使用问题送回初审法官重新审议。2016 年，该案被重新审理，陪审团以合理使用为由，认定谷歌胜诉。

### 8.2. Chromium OS (2009 年至今）

直到最近，Linux 仍然是一个相对不常见的台式机和笔记本电脑的操作系统选择。然而，谷歌的 Chromebooks，运行 Chrome OS，本质上是一个瘦客户端，已经占据了美国 300 美元以下笔记本电脑市场的 20-25%。[^74] Chrome OS 是由开源的 Chromium OS 构建的，它是基于 Linux 的，就像商业化手机上的 Android 版本是由 Android 的开源版本构建的一样。

## 9. 外部链接

*   Elmer-Dewitt, Philip (30 July 1984). [Software Is for Sharing](https://web.archive.org/web/20070930122050/http://www.time.com/time/magazine/article/0,9171,926733,00.html), _Time_.
*   [Richard Stallman speaking about free software and the GNU project in 1986](https://www.gnu.org/philosophy/stallman-kth.html), Sweden
*   [David A. Wheeler on the history of free software](http://www.dwheeler.com/oss_fs_why.html#history), from his "Look at the numbers!" paper
*   [The Daemon, the GNU, and the Penguin](http://www.groklaw.net/staticpages/index.php?page=20051013231901859), by Peter Salus
*   [Documents about the BSD lawsuit that lead to 386BSD and then FreeBSD](http://cm.bell-labs.com/cm/cs/who/dmr/bsdi/bsdisuit.html)
*   [_Open Sources: Voices from the Open Source Revolution_](http://www.oreilly.com/catalog/opensources/book/toc.html) (January 1999)
*   [The history of Cygnus solutions](https://web.archive.org/web/20171022105307/http://www.toad.com/gnu/cygnus/index.html), the largest free software company of the early 90s
*   [LWN.net's 1998–2008 timeline part 1](https://lwn.net/Articles/264402/) ([part 2](https://lwn.net/Articles/264980/), [3](https://lwn.net/Articles/265577/), [4](https://lwn.net/Articles/266358/), [5](https://lwn.net/Articles/268407/), [6](https://lwn.net/Articles/269276/))
*   [A Brief History of FreeBSD](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/history.html), by Jordan Hubbard
*   [UNESCO Free Software Portal](http://www.unesco.org/webworld/portal_freesoft/open_history.shtml)
*   [Infinite Hands](http://infinite-hands.draketo.de/), a free licensed folk song about the history of free software.

## 10. 参考文献

[^1]: VM Brasseur (2018). [Forge your Future with Open Source](https://archive.org/details/isbn_9781680503012). Pragmatic Programmers. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier)) [978-1-68050-301-2](https://en.wikipedia.org/wiki/Special:BookSources/978-1-68050-301-2).

[^2]: James J. Flink (1977). The Car Culture. MIT Press. ISBN [978-0-262-56015-3](https://en.wikipedia.org/wiki/Special:BookSources/978-0-262-56015-3).

[^3]: Hippel, Eric von; Krogh, Georg von (1 April 2003). ["Open Source Software and the "Private-Collective" Innovation Model: Issues for Organization Science"](https://dspace.mit.edu/bitstream/1721.1/66145/1/SSRN-id1410789.pdf) (PDF). Organization Science. 14 (2): 209–223. [doi](https://en.wikipedia.org/wiki/Doi_(identifier)):[10.1287/orsc.14.2.209.14992](https://doi.org/10.1287%2Forsc.14.2.209.14992). [hdl](https://en.wikipedia.org/wiki/Hdl_(identifier)):[1721.1/66145](https://hdl.handle.net/1721.1%2F66145). [ISSN](https://en.wikipedia.org/wiki/ISSN_(identifier)) [1047-7039](https://www.worldcat.org/issn/1047-7039).

[^4]: ["IBM 7090/7094 Page"](https://web.archive.org/web/20150827134534/http://www.cozx.com/~dpitts/ibm7090.html). Archived from [the original](http://www.cozx.com/~dpitts/ibm7090.html) on 27 August 2015. Retrieved 11 August 2015.

[^5]: Ceruzzi, Paul (1998). [A History of Modern Computing](https://archive.org/details/historyofmodernc00ceru). The MIT Press. ISBN [9780262032551](https://en.wikipedia.org/wiki/Special:BookSources/9780262032551).

[^6]: ["Heresy & Heretical Open Source: A Heretic's Perspective"](http://www.infoq.com/presentations/Heretical-Open-Source). [Archived](https://web.archive.org/web/20121014192441/http://www.infoq.com/presentations/Heretical-Open-Source) from the original on 14 October 2012. Retrieved 16 November 2012.

[^7]: Sam Williams. Free as in Freedom: Richard Stallman's Crusade for Free Software. ["Chapter 1: For Want of a Printer"](http://www.oreilly.com/openbook/freedom/ch01.html) [Archived](https://web.archive.org/web/20150910145624/http://www.oreilly.com/openbook/freedom/ch01.html) 10 September 2015 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine). 2002.

[^8]: Gaudeul, Alexia (2007). "Do Open Source Developers Respond to Competition? The LATEX Case Study". Review of Network Economics. 6 (2). doi:[10.2202/1446-9022.1119](https://doi.org/10.2202%2F1446-9022.1119). ISSN [1446-9022](https://www.worldcat.org/issn/1446-9022). S2CID [201097782](https://api.semanticscholar.org/CorpusID:201097782).

[^9]: ["A brief history of spice"](https://web.archive.org/web/20070523080617/http://www.ecircuitcenter.com/SpiceTopics/History.htm). Archived from [the original](http://www.ecircuitcenter.com/SpiceTopics/History.htm) on 23 May 2007. Retrieved 18 June 2007.

[^10]: Fisher, Franklin M.; McKie, James W.; Mancke, Richard B. (1983). IBM and the U.S. Data Processing Industry: An Economic History. Praeger. ISBN [978-0-03-063059-0](https://en.wikipedia.org/wiki/Special:BookSources/978-0-03-063059-0).page 176

[^11]: Fisher. op.cit.

[^12]: [Apple Computer, Inc. v. Franklin Computer Corporation Puts the Byte Back into Copyright Protection for Computer Programs](http://digitalcommons.law.ggu.edu/cgi/viewcontent.cgi?article=1344&context=ggulrev) [Archived](https://web.archive.org/web/20170507231059/http://digitalcommons.law.ggu.edu/cgi/viewcontent.cgi?article=1344&context=ggulrev) 7 May 2017 at the Wayback Machine in Golden Gate University Law Review Volume 14, Issue 2, Article 3 by Jan L. Nussbaum (January 1984)

[^13]: Lemley, Menell, Merges and Samuelson. Software and Internet Law, p. 34.

[^14]: Landley, Rob (23 May 2009). ["notes-2009"](http://landley.net/notes-2009.html). landley.net. [Archived](https://web.archive.org/web/20170904111501/http://landley.net/notes-2009.html) from the original on 4 September 2017. Retrieved 2 December 2015. So if [open source](https://en.wikipedia.org/wiki/Open-source_software) used to be the norm back in the 1960s and 70s, how did this _change_? Where did [proprietary software](https://en.wikipedia.org/wiki/Proprietary_software) come from, and when, and how? How did [Richard Stallman](https://en.wikipedia.org/wiki/Richard_Stallman)'s little utopia at the [MIT AI lab](https://en.wikipedia.org/wiki/MIT_AI_lab) crumble and force him out into the wilderness to try to rebuild it? Two things changed in the early 80s: the exponentially growing installed base of microcomputer hardware reached critical mass around 1980, and a legal decision altered copyright law to cover binaries in 1983."

[^15]: [Weber, Steven](https://en.wikipedia.org/wiki/Steven_Weber_(professor)) (2004). [The Success of Open Source](https://web.archive.org/web/20090927011950/http://polisci.berkeley.edu/faculty/bio/permanent/Weber,S/). Cambridge, MA: [Harvard University Press](https://en.wikipedia.org/wiki/Harvard_University_Press). pp. 38–44. ISBN [978-0-674-01858-7](https://en.wikipedia.org/wiki/Special:BookSources/978-0-674-01858-7). Archived from [the original](http://www.polisci.berkeley.edu/Faculty/bio/permanent/Weber,S/) on 27 September 2009.

[^16]: IBM Corporation (8 February 1983). ["DISTRIBUTION OF IBM LICENSED PROGRAMS AND LICENSED PROGRAM MATERIALS AND MODIFIED AGREEMENT FOR IBM LICENSED PROGRAMS"](http://landley.net/history/mirror/ibm/oco.html). [Archived](https://web.archive.org/web/20170904075121/http://landley.net/history/mirror/ibm/oco.html) from the original on 4 September 2017. Retrieved 24 March 2017.

[^17]: Gallant, John (18 March 1985). ["IBM policy draws fire – Users say source code rules hamper change"](https://books.google.com/books?id=4Wgmey4obagC&q=1983object-only+model+IBM&pg=PA8). [Computerworld](https://en.wikipedia.org/wiki/Computerworld). Retrieved 27 December 2015. While IBM's policy of withholding source code for selected software products has already marked its second anniversary, users are only now beginning to cope with the impact of that decision. But whether or not the advent of object-code-only products has affected their day-to-day DP operations, some users remain angry about IBM's decision. Announced in February 1983, IBM's object-code-only policy has been applied to a growing list of Big Blue system software products

[^18]: Shea, Tom (23 June 1983). ["Free software – Free software is a junkyard of software spare parts"](https://books.google.com/books?id=yy8EAAAAMBAJ&q=us+government+public+domain+software&pg=PA31). [InfoWorld](https://en.wikipedia.org/wiki/InfoWorld). Retrieved 10 February 2016.

[^19]: Ahl, David. ["David H. Ahl biography from Who's Who in America"](http://www.swapmeetdave.com/Ahl/DHAbio.htm). [Archived](https://web.archive.org/web/20150924131314/http://www.swapmeetdave.com/Ahl/DHAbio.htm) from the original on 24 September 2015. Retrieved 23 November 2009.

[^20]: Wilkinson, Bill (1983). [The Atari BASIC Source Book](https://archive.org/details/ataribooks-the-atari-basic-source-book). COMPUTE! Books. ISBN [9780942386158](https://en.wikipedia.org/wiki/Special:BookSources/9780942386158). [Archived](https://web.archive.org/web/20130119010453/http://archive.org/details/ataribooks-the-atari-basic-source-book) from the original on 19 January 2013. Retrieved 2 October 2017.

[^21]: Wilkinson, Bill (1982). ["Inside Atari DOS"](http://atariarchives.org/iad/). COMPUTE! Books. [Archived](https://web.archive.org/web/20171002120523/http://atariarchives.org/iad/) from the original on 2 October 2017. Retrieved 2 October 2017.

[^22]: Norman, Jeremy. ["SHARE, The First Computer Users' Group, is Founded (1955)"](http://www.historyofinformation.com/expanded.php?id=4805). HistofyofInformation.com. [Archived](https://web.archive.org/web/20170411125236/http://historyofinformation.com/expanded.php?id=4805) from the original on 11 April 2017. Retrieved 24 March 2017.

[^23]: ["The DECUS tapes"](http://www.ibiblio.org/pub/academic/computer-science/history/pdp-11/rsx/decus/). [Archived](https://web.archive.org/web/20121228220557/http://www.ibiblio.org/pub/academic/computer-science/history/pdp-11/rsx/decus/) from the original on 28 December 2012. Retrieved 9 May 2013.

[^24]: DiBona, C., et al. Open Sources 2.0. O'Reilly, ISBN [0-596-00802-3](https://en.wikipedia.org/wiki/Special:BookSources/0-596-00802-3).

[^25]: ["Talk transcript where Stallman tells the printer story"](https://www.gnu.org/events/rms-nyu-2001-transcript.txt). [Archived](https://web.archive.org/web/20140318074756/http://www.gnu.org/events/rms-nyu-2001-transcript.txt) from the original on 18 March 2014. Retrieved 18 April 2014.

[^26]: ["Transcript of Richard Stallman's Speech, 28 Oct 2002, at the International Lisp Conference"](https://www.gnu.org/gnu/rms-lisp.html). GNU Project. 28 October 2002. [Archived](https://web.archive.org/web/20140416180457/https://www.gnu.org/gnu/rms-lisp.html) from the original on 16 April 2014. Retrieved 21 December 2008.

[^27]: ["GNU General Public License v1.0"](https://www.gnu.org/licenses/old-licenses/gpl-1.0.txt). [Archived](https://web.archive.org/web/20140221032723/http://www.gnu.org/licenses/old-licenses/gpl-1.0.txt) from the original on 21 February 2014. Retrieved 18 April 2014.

[^28]: Michael Tiemann (29 March 1999). ["Future of Cygnus Solutions, An Entrepreneur's Account"](http://www.oreilly.com/catalog/opensources/book/tiemans.html). [Archived](https://web.archive.org/web/20070610003451/http://www.oreilly.com/catalog/opensources/book/tiemans.html) from the original on 10 June 2007. Retrieved 18 June 2007.

[^29]: ["Release notes for Linux kernel 0.12"](https://www.kernel.org/pub/linux/kernel/Historic/old-versions/RELNOTES-0.12). [Archived](https://web.archive.org/web/20070819045030/http://www.kernel.org/pub/linux/kernel/Historic/old-versions/RELNOTES-0.12) from the original on 19 August 2007. Retrieved 25 July 2016.

[^30]: ["A Brief History of Debian"](http://www.debian.org/doc/manuals/project-history/ch-detailed.en.html). [Archived](https://www.webcitation.org/69LfEYDhG?url=http://www.debian.org/doc/manuals/project-history/ch-detailed.en.html) from the original on 22 July 2012. Retrieved 11 February 2008.

[^31]: [Take your freedom back, with Linux-2.6.33-libre](http://www.fsfla.org/svnwiki/anuncio/2010-03-Linux-2.6.33-libre.en) [Archived](https://web.archive.org/web/20121219081431/http://www.fsfla.org/svnwiki/anuncio/2010-03-Linux-2.6.33-libre.en) 19 December 2012 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine) FSFLA, 2010.

[^32]: ["Linux and GNU – GNU Project – Free Software Foundation"](https://www.gnu.org/gnu/linux-and-gnu.html). Gnu.org. 20 May 2013. [Archived](https://web.archive.org/web/20170319145123/http://www.gnu.org/gnu/linux-and-gnu.html) from the original on 19 March 2017. Retrieved 2 October 2013.

[^33]: ["January 2015 Web Server Survey"](https://web.archive.org/web/20160119190846/http://news.netcraft.com/archives/2015/01/15/january-2015-web-server-survey.html). Netcraft. Archived from [the original](http://news.netcraft.com/archives/2015/01/15/january-2015-web-server-survey.html) on 19 January 2016. Retrieved 3 February 2016.

[^34]: Kelty, Christpher M. (2008). ["The Cultural Significance of free Software – Two Bits"](https://web.archive.org/web/20160304070704/http://twobits.net/pub/Kelty-TwoBits.pdf) (PDF). [Duke University](https://en.wikipedia.org/wiki/Duke_University) press – durham and london. p. 99. Archived from [the original](http://twobits.net/pub/Kelty-TwoBits.pdf) (PDF) on 4 March 2016. Retrieved 17 February 2016.

[^35]: [Karl Fogel](https://en.wikipedia.org/wiki/Karl_Fogel) (2016). ["Producing Open Source Software – How to Run a Successful Free Software Project"](http://producingoss.com/en/introduction.html#free-vs-open-source). O'Reilly Media. [Archived](https://web.archive.org/web/20160420192933/http://producingoss.com/en/introduction.html#free-vs-open-source) from the original on 20 April 2016. Retrieved 11 April 2016.

[^36]:[Tiemann, Michael](https://en.wikipedia.org/wiki/Michael_Tiemann) (19 September 2006). ["History of the OSI"](https://web.archive.org/web/20021001164015/http://www.opensource.org/docs/history.php). [Open Source Initiative](https://en.wikipedia.org/wiki/Open_Source_Initiative). Archived from [the original](http://www.opensource.org/history) on 1 October 2002. Retrieved 23 August 2008.

[^37]: Muffatto, Moreno (2006). Open Source: A Multidisciplinary Approach. Imperial College Press. ISBN [978-1-86094-665-3](https://en.wikipedia.org/wiki/Special:BookSources/978-1-86094-665-3).

[^38]: [Open Source Summit](http://linuxgazette.net/issue28/rossum.html) [Archived](https://web.archive.org/web/20131229053622/http://linuxgazette.net/issue28/rossum.html) 29 December 2013 at the Wayback Machine Linux Gazette. 1998.

[^39]: [Eric S. Raymond](https://en.wikipedia.org/wiki/Eric_S._Raymond "Eric S. Raymond"). ["Goodbye, 'free software'; hello, 'open source'"](http://www.catb.org/~esr/open-source.html). catb.org. [Archived](https://www.webcitation.org/617oVjlKk?url=http://www.catb.org/~esr/open-source.html) from the original on 22 August 2011. Retrieved 11 August 2015.

[^40]: [Tiemann, Michael](https://en.wikipedia.org/wiki/Michael_Tiemann) (19 September 2006). ["History of the OSI"](https://web.archive.org/web/20021001164015/http://www.opensource.org/docs/history.php). [Open Source Initiative](https://en.wikipedia.org/wiki/Open_Source_Initiative). Archived from [the original](http://www.opensource.org/docs/history.php) on 1 October 2002. Retrieved 23 August 2008.

[^41]: Leander Kahney (5 March 1999). ["Linux's Forgotten Man – You have to feel for Richard Stallman"](https://web.archive.org/web/20010622041610/http://www.wired.com/news/technology/0%2C1282%2C18291%2C00.html). [Wired](https://en.wikipedia.org/wiki/Wired_(magazine)). Archived from [the original](https://www.wired.com/news/technology/0,1282,18291,00.html) on 22 June 2001.

[^42]: ["Toronto Star: Freedom's Forgotten Prophet (Richard Stallman)"](http://www.linuxtoday.com/infrastructure/2000101000421OSCY). _Linux Today_. 10 October 2000. [Archived](https://web.archive.org/web/20160417104602/http://www.linuxtoday.com/infrastructure/2000101000421OSCY) from the original on 17 April 2016. Retrieved 25 March 2016.

[^43]: [Nikolai Bezroukov](https://en.wikipedia.org/wiki/Nikolai_Bezroukov) (1 November 2014). ["Portraits of Open Source Pioneers – Part IV. Prophet"](http://www.softpanorama.org/People/Stallman/prophet.shtml#Linux_schism). [Archived](https://web.archive.org/web/20160410122520/http://softpanorama.org/People/Stallman/prophet.shtml#Linux_schism) from the original on 10 April 2016. Retrieved 25 March 2016.

[^44]: Richard Stallman. ["Why Open Source Misses the Point"](https://www.gnu.org/philosophy/open-source-misses-the-point.html). [Archived](https://web.archive.org/web/20110804231811/http://www.gnu.org/philosophy/open-source-misses-the-point.html) from the original on 4 August 2011. Retrieved 18 April 2014.

[^45]: [Rishab Aiyer Ghosh](https://en.wikipedia.org/wiki/Rishab_Aiyer_Ghosh) et al (2002).["Free/Libre and Open Source Software: Survey and Study FLOSS Deliverable D18: FINAL REPORT – Part IV: Survey of Developers"](https://web.archive.org/web/20090913045502/http://www.infonomics.nl/FLOSS/report/Final4.htm). Archived from the original on 13 September 2009.

[^46]: Brian Fitzgerald, Pär J. Ågerfalk (2005). [The Mysteries of Open Source Software: Black and White and Red All Over](https://www.computer.org/csdl/proceedings/hicss/2005/2268/07/22680196a.pdf) [Archived](https://web.archive.org/web/20160405134050/https://www.computer.org/csdl/proceedings/hicss/2005/2268/07/22680196a.pdf) 5 April 2016 at the Wayback Machine [University of Limerick](https://en.wikipedia.org/wiki/University_of_Limerick), Ireland. "Open Source software (OSS) has attracted enormous media and research attention since the term was coined in February 1998."

[^47]: Ettrich, Matthias (14 October 1996). ["New Project: Kool Desktop Environment (KDE)"](https://groups.google.com/group/de.comp.os.linux.misc/msg/cb4b2d67ffc3ffce). [Newsgroup](/wiki/Usenet_newsgroup "Usenet newsgroup"): [de.comp.os.linux.misc](news:de.comp.os.linux.misc). [Usenet:](https://en.wikipedia.org/wiki/Usenet_(identifier)) [53tkvv$b4j@newsserv.zdv.uni-tuebingen.de](news:53tkvv$b4j@newsserv.zdv.uni-tuebingen.de). [Archived](https://web.archive.org/web/20130530054434/http://groups.google.com/group/de.comp.os.linux.misc/msg/cb4b2d67ffc3ffce) from the original on 30 May 2013. Retrieved 29 December 2006.

[^48]: Richard Stallman (5 September 2000). ["Stallman on Qt, the GPL, KDE, and GNOME"](http://linuxtoday.com/news_story.php3?ltsn=2000-09-05-001-21-OP-LF-KE). [Archived](https://web.archive.org/web/20090122070916/http://www.linuxtoday.com/news_story.php3?ltsn=2000-09-05-001-21-OP-LF-KE) from the original on 22 January 2009. Retrieved 9 September 2005.

[^49]: ["A tale of two desktops"](http://www.pcauthority.com.au/Feature/79378,a-tale-of-two-desktops.aspx). _PC & Tech Authority_. [Archived](https://web.archive.org/web/20150704093709/http://www.pcauthority.com.au/Feature/79378,a-tale-of-two-desktops.aspx) from the original on 4 July 2015. Retrieved 11 August 2015.

[^50]: Shuttleworth, Mark (5 April 2017). ["Growing Ubuntu for cloud and IoT, rather than phone and convergence"](https://web.archive.org/web/20170507225729/https://insights.ubuntu.com/2017/04/05/growing-ubuntu-for-cloud-and-iot-rather-than-phone-and-convergence). _[Canonical Ltd.](https://en.wikipedia.org/wiki/Canonical_Ltd.)_ Archived from [the original](https://insights.ubuntu.com/2017/04/05/growing-ubuntu-for-cloud-and-iot-rather-than-phone-and-convergence/) on 7 May 2017. Retrieved 5 April 2017.

[^51]: ["Ubuntu To Abandon Unity 8, Switch Back To GNOME"](http://phoronix.com/scan.php?page=news_item&px=Ubuntu-Dropping-Unity). [Phoronix.com](https://en.wikipedia.org/wiki/Phoronix.com). [Archived](https://web.archive.org/web/20170516161705/http://www.phoronix.com/scan.php?page=news_item&px=Ubuntu-Dropping-Unity) from the original on 16 May 2017. Retrieved 6 April 2017.

[^52]: ["The Wayland Situation: Facts About X vs. Wayland – Phoronix"](https://www.phoronix.com/scan.php?page=article&item=x_wayland_situation). [Archived](https://web.archive.org/web/20150924091609/http://www.phoronix.com/scan.php?page=article&item=x_wayland_situation) from the original on 24 September 2015. Retrieved 11 August 2015.

[^53]: ["Post on y-devel by Brandon Black"](https://web.archive.org/web/20060924165154/http://www.y-windows.org/pipermail/y-devel/2006-January/001977.html). 3 January 2006. Archived from [the original](http://www.y-windows.org/pipermail/y-devel/2006-January/001977.html) on 24 September 2006. Retrieved 14 May 2017.

[^54]: Gavin Clarke (23 July 2009). ["Microsoft opened Linux-driver code after 'violating' GPL"](https://www.theregister.co.uk/2009/07/23/microsoft_hyperv_gpl_violation/). The Register. [Archived](https://web.archive.org/web/20131004230535/http://www.theregister.co.uk/2009/07/23/microsoft_hyperv_gpl_violation/) from the original on 4 October 2013. Retrieved 6 September 2013.

[^55]: ["GNU General Public License"](https://www.gnu.org/licenses/gpl.html). [Archived](https://web.archive.org/web/20140418021611/http://www.gnu.org/licenses/gpl.html) from the original on 18 April 2014. Retrieved 18 April 2014.

[^56]: Ovide, Shira (16 April 2012). ["Microsoft Dips Further into Open-Source Software"](https://www.wsj.com/articles/SB10001424052702304432704577347783238850756). _[The Wall Street Journal](https://en.wikipedia.org//wiki/The_Wall_Street_Journal)_. [Archived](https://web.archive.org/web/20150210214357/http://www.wsj.com/articles/SB10001424052702304432704577347783238850756) from the original on 10 February 2015. Retrieved 17 April 2012.

[^57]: ["ChakraCore GitHub repository is now open"](https://blogs.windows.com/msedgedev/2016/01/13/chakracore-now-open/). 13 January 2016. [Archived](https://web.archive.org/web/20160130180037/https://blogs.windows.com/msedgedev/2016/01/13/chakracore-now-open/) from the original on 30 January 2016. Retrieved 22 January 2016.

[^58]: ["Ballmer: I may have called Linux a cancer but now I love it"](https://www.zdnet.com/article/ballmer-i-may-have-called-linux-a-cancer-but-now-i-love-it/).

[^59]: Asay, Matt (7 February 2018). ["Who really contributes to open source"](https://www.infoworld.com/article/3253948/who-really-contributes-to-open-source.html). _InfoWorld_. Retrieved 8 June 2020.

[^60]: ["Foxconn rejects Microsoft patent lawsuit, says never had to pay royalties"](https://www.reuters.com/article/us-foxconn-microsoft-idUSKBN1QT0D9). [Reuters](https://en.wikipedia.org/wiki/Reuters). 19 March 2019. Retrieved 8 June 2020.

[^61]: ["Microsoft and Foxconn Parent Hon Hai Sign Patent Agreement For Android and Chrome Devices - Stories"](https://news.microsoft.com/2013/04/17/microsoft-and-foxconn-parent-hon-hai-sign-patent-agreement-for-android-and-chrome-devices/). _microsoft.com_. 16 April 2013. [Archived](https://web.archive.org/web/20190330124348/https://news.microsoft.com/2013/04/17/microsoft-and-foxconn-parent-hon-hai-sign-patent-agreement-for-android-and-chrome-devices/) from the original on 30 March 2019. Retrieved 8 June 2020.

[^62]: ["SCM Ranking, Q3 2013"](https://web.archive.org/web/20130928180246/http://beta.gitgear.com/why_git/SCM_Ranking_2013Q3_F1.pdf) (PDF). Switch-Gears. Archived from [the original](http://beta.gitgear.com/why_git/SCM_Ranking_2013Q3_F1.pdf) (PDF) on 28 September 2013. Retrieved 22 September 2013.

[^63]: Brockmeier, Joe. ["Apple's Selective Contributions to GCC"](https://lwn.net/Articles/405417/). [Archived](https://web.archive.org/web/20111117002647/http://lwn.net/Articles/405417/) from the original on 17 November 2011. Retrieved 23 October 2011.

[^64]: ["LLVM Developer Policy"](https://web.archive.org/web/20121113204817/http://www.llvm.org/docs/DeveloperPolicy.html#license). LLVM. Archived from [the original](http://llvm.org/docs/DeveloperPolicy.html#license) on 13 November 2012. Retrieved 19 November 2012.

[^65]: Holwerda, Thom. ["Apple Ditches SAMBA in Favour of Homegrown Replacement"](http://www.osnews.com/story/24572/). [Archived](https://web.archive.org/web/20120114142006/http://www.osnews.com/story/24572/) from the original on 14 January 2012. Retrieved 23 October 2011.

[^66]: ["Sun to Acquire MySQL"](https://web.archive.org/web/20080117192218/http://www.mysql.com/news-and-events/sun-to-acquire-mysql.html). MySQL AB. Archived from [the original](http://mysql.com/news-and-events/sun-to-acquire-mysql.html) on 17 January 2008. Retrieved 16 January 2008.

[^67]: Thomson, Iain. ["Oracle offers commercial extensions to MySQL"](https://www.theregister.co.uk/2011/09/16/oracle_commercial_extensions_mysql/). [Archived](https://web.archive.org/web/20111023204950/http://www.theregister.co.uk/2011/09/16/oracle_commercial_extensions_mysql/) from the original on 23 October 2011. Retrieved 23 October 2011.

[^68]: Samson, Ted. ["Non-Oracle MySQL fork deemed ready for prime time"](https://web.archive.org/web/20111109094334/http://www.infoworld.com/d/open-source-software/non-oracle-mysql-fork-deemed-ready-prime-time-853). Archived from [the original](http://www.infoworld.com/d/open-source-software/non-oracle-mysql-fork-deemed-ready-prime-time-853) on 9 November 2011. Retrieved 23 October 2011.

[^69]: Nelson, Russell. ["Open Source, MySQL, and trademarks"](http://www.opensource.org/node/496). [Archived](https://web.archive.org/web/20111021095017/http://opensource.org/node/496) from the original on 21 October 2011. Retrieved 23 October 2011.

[^70]: ["Android, the world's most popular mobile platform"](https://developer.android.com/about/index.html). [Archived](https://web.archive.org/web/20130922035131/http://developer.android.com/about/index.html) from the original on 22 September 2013. Retrieved 6 September 2013.

[^71]: Steven J. Vaughan-Nichols (29 July 2013). ["20 great years of Linux and supercomputers"](https://www.zdnet.com/20-great-years-of-linux-and-supercomputers-7000018681/). [ZDNet](https://en.wikipedia.org/wiki/ZDNet). [Archived](https://web.archive.org/web/20130823182003/http://www.zdnet.com/20-great-years-of-linux-and-supercomputers-7000018681/) from the original on 23 August 2013. Retrieved 6 September 2013.

[^72]: Niccolai, James (20 June 2012). ["Oracle agrees to 'zero' damages in Google lawsuit, eyes appeal"](http://www.computerworld.com/s/article/9228298/Oracle_agrees_to_zero_damages_in_Google_lawsuit_eyes_appeal). [Archived](https://web.archive.org/web/20121117001109/http://www.computerworld.com/s/article/9228298/Oracle_agrees_to_zero_damages_in_Google_lawsuit_eyes_appeal) from the original on 17 November 2012. Retrieved 23 June 2012.

[^73]: Jones, Pamela (5 October 2012). ["Oracle and Google File Appeals"](https://web.archive.org/web/20121201130542/http://www.groklaw.net/articlebasic.php?story=20121005082638280). Groklaw. Archived from [the original](http://www.groklaw.net/articlebasic.php?story=20121005082638280) on 1 December 2012. Retrieved 17 November 2012.

[^74]: Williams, Rhiannon (11 July 2013). ["Google Chromebook sales soar in face of PC decline"](https://www.telegraph.co.uk/technology/google/10173494/Google-Chromebook-sales-soar-in-face-of-PC-decline.html). _[The Daily Telegraph](https://en.wikipedia.org//wiki/The_Daily_Telegraph)_. [Archived](https://web.archive.org/web/20130925104825/http://www.telegraph.co.uk/technology/google/10173494/Google-Chromebook-sales-soar-in-face-of-PC-decline.html) from the original on 25 September 2013. Retrieved 3 September 2013.
