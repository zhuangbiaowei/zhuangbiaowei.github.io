---
layout: post
title: "翻译与评述《后开放零成本许可证》"
date: 2024-03-12 13:58 +0800
tags: OpenSource License
comments: true
---

**特别感谢：赵云虎律师帮我审阅了翻译的初稿，并提出了很多专业的修改意见，详情请参见[commit diff](https://github.com/zhuangbiaowei/zhuangbiaowei.github.io/commit/92fc102bc96e31774886f5e76943b2df5448ef4a)**

---

4 天前，著名的 [Bruce Perens](https://perens.com/about-bruce-perens/) 发表了一篇新的博客，标题是《[Post-Open License: First Draft](https://perens.com/2024/03/08/post-open-license-first-draft/)》。作为开源运动的创始人之一，开源定义（OSD）的撰写人，在今年 1 月的一篇专访《[专访开源先锋 Bruce Perens：后开源、许可证、AI](https://linux.cn/article-16524-1.html)》中，他就已经提到，自己正在开发一种新的许可证。Perens 提到，开源社区需要解决几个紧迫的问题。

* 我们现在的许可证已无法满足需求
* 开源完全未能服务于普通人
* 他所描述的“后开源”，比开源稍微复杂一些。它将明确企业与开发者的关系，以确保企业为所获得的利益支付合理的费用。对于个人和非营利机构，仍可免费使用，而且只需一个许可证即可。

现在，我们终于能够看到全文了。

借助 ChatGPT 的帮助，我快速阅读了这个协议，并打算与一些朋友讨论，然后在翻译的基础上，略作评述，也希望与更多朋友，一起讨论。

【Post-Open】，在 Linux.cn 的网站翻译中，称之为“后开源”，而我会称之为“后开放”，因为如果是后开源，应该是【Post-OpenSource】才对。

---

【原文】POST OPEN ZERO-COST LICENSE 0.01, March 2024.

【译文】后开放零成本许可证 0.01 版，2024 年 3 月。

【原文】

**1. PRELUDE**

**1.1 HOW TO USE THIS TEXT ON YOUR OWN WORK.**

If you wish to apply these terms to your own work, you must first enter into the POST-OPEN OPERATING AGREEMENT, which gives permission to use this copyrighted text.

【译文】

**1. 前言**

**1.1 如何将本文应用于您自己的作品。**

如果您希望将这些条款应用于您自己的作品，您必须首先签订《**后开放运营协议**》，该协议许可使用此受版权保护的文本。

【译注】POST-OPEN OPERATING，是一个需要被定义的概念。

【原文】

**1.2 COPYRIGHT OF THIS TEXT**

Copyright (C) 2024 POST-OPEN ADMINISTRATION. All rights reserved. The section on ARBITRATION originates with the American Arbitration Association and we do not claim copyright upon it.

【译文】

**1.2 本文的版权**

版权所有 (C) 2024 **后开放管理机构**。保留所有权利。关于**仲裁**的部分起源于美国仲裁协会，我们对此不主张版权。

【译注】POST-OPEN ADMINISTRATION，是一个需要被定义的概念。

【原文】

**1.3 ADVISORY SECTIONS**

Text contained within square brackets ("[" and "]") is advisory in nature and not part of these terms. These terms shall not be invalidated or otherwise impaired if advisory sections are incorrect or become out-of-date. [This is an example of an advisory section.]

【译文】

**1.3 建议章节**

放在方括号（“[”和“]”）内的文本是建议性质的，并不构成这些条款的一部分。如果建议章节错误或过时，这些条款不应被视为无效或以其他方式受到损害。[这是一个建议章节的例子。]

【原文】

**1.4 THE CONTACT.txt FILE**

The identity of the LICENSOR and the means of contacting them should appear in the file "CONTACT.txt" where the SOURCE CODE is stored. This file may also contain caveats regarding the work, declarations of PUBLIC INTERFACES, statements regarding the source and status of some portions of the work (for example, that the developer disclaims copyright to that portion), and other information that may effect your rights.

【译文】

**1.4 CONTACT.txt 文件**

**许可方**的身份及其联系方式应当出现在存储**源代码**的 “CONTACT.txt” 文件中。该文件还可以包含关于作品的警告、公共接口的声明、关于作品某些部分的来源和状态的声明（例如，开发者声明放弃该部分的版权），以及可能影响您权利的其他信息。

【原文】

**1.5 DRAFT NATURE OF THIS DOCUMENT**

This is a DRAFT version of the POST-OPEN ZERO-COST LICENSE 0.01 . [If you don't like these terms, contact the LICENSOR for a different license.]

WARNING: These terms are not the product of an attorney, and that's a particularly bad practice - the way a judge would enforce (or decline to enforce) these terms is unpredictable, and they may let down the developer who attempts to enforce them in court. Apply these terms to your work at your own risk. [We intend to release a version that is the product of a competent attorney.]

【译文】

**1.5 本文档的草案性质**

这是**后开放零成本许可证** 0.01 的**草案**版本。[如果您不喜欢这些条款，请联系**许可方**以获取不同的许可证。]

**警告**：这些条款不是由律师制定的，这是一个特别糟糕的做法——法官如何执行（或拒绝执行）这些条款是不可预测的，它们可能会让尝试在法庭上执行这些条款的开发者失望。将这些条款应用于您的作品需自担风险。[我们打算发布一个由合格律师制定的版本。]

【原文】

**2. DEFINITIONS**

References to defined terms are rendered in all-capital lettering, for example: "TERMINATION". When a defined term appears in lower-case, it refers to the general usage of that word rather than the defined form, for example "WORK" refers specifically to the work placed under these terms by the LICENSOR, and a "work" may be the WORK or another one. Some words in these terms appear as all-capital simply as part of of common parlance, for example "A" and "HTTP".

【译文】

**2. 定义**

对定义术语的引用以全部大写字母呈现，例如：“TERMINATION”（**终止**）。当一个定义术语以小写出现时，它指的是该词的一般用途，而非定义形式，例如“WORK”（**作品**）特指由**许可方**根据这些条款发布的作品，而一个“work”可能是该作品或另一个作品。这些条款中的一些词语以全部大写形式出现，仅作为常用语的一部分，例如“A”和“HTTP”。

【译注】在中文翻译中，术语会以加粗方式展现。

【原文】

2.1 The POST-OPEN ADMINISTRATION is the entity which, through the POST-OPEN OPERATING AGREEMENT with all of the LICENSORS of works in the POST-OPEN COLLECTION, may represent any of those LICENSORS in any controversy or claim arising out of or related to these terms and its other agreements and processes. The POST-OPEN ADMINISTRATION may bring suit or enforce other law on behalf of the LICENSOR.

【译文】

2.1 **后开放管理机构**是一个实体，通过与所有**后开放系列**中作品的**许可方**签订的**后开放运营协议**，可以代表任何这些**许可方**在与这些条款及其其他协议和流程相关的任何争议或索赔中。**后开放管理机构**可代表**许可方**提起诉讼或执行其他法律。

【译注】**后开放管理机构**相当于是创设了一个站在所有（采纳了Post-Open License的）开源作者背后的支持方。但是，在这个文本里，并没有出现**后开放运营协议**的具体内容或链接指向。

【原文】

2.2 The POST-OPEN ZERO-COST CONTRACT is these same terms, with the addition of clear and recorded consent by the licensee. [To enter into it, see https://postopen.org/zero-contract/ ]

【译文】

2.2 **后开放零成本合同**是这些相同的条款，加上被许可人的明确和记录在案的同意。[请访问 [https://postopen.org/zero-contract/](https://postopen.org/zero-contract/) ]

【译注】这个网站尚未开放，但是感觉一种不必要的“外部依赖性”

【原文】

2.3 The POST-OPEN PAID CONTRACT is a separate agreement which grants additional rights not provided by these terms. [To enter into it, see https://postopen.org/paid-contract/ ]

【译文】

2.3 **后开放付费合同**是一份单独的协议，它授予这些条款未提供的附加权利。[请访问 [https://postopen.org/paid-contract/](https://postopen.org/paid-contract/) ]

【译注】同上

【原文】

2.4 The POST-OPEN INFRINGEMENT PROCESS is the process by which an infringing entity cures an infringement and comes back into compliance without litigation.  Uncooperative infringers are, of course, subject to litigation, blocking of imports, simple and punitive damages, and other prosecution. [To participate in the POST-OPEN INFRINGEMENT PROCESS, see https::/postopen.org/infringement/ ]

【译文】

2.4 **后开放侵权处理流程**是一个过程，通过该过程，侵权实体治愈侵权并在不进行诉讼的情况下恢复合规。当然，不合作的侵权者将面临诉讼、进口阻止、简单和惩罚性赔偿以及其他起诉。[要参与**后开放侵权处理流程**，请访问 [https://postopen.org/infringement/](https://postopen.org/infringement/) ]

【译注】同上

【原文】

2.5 YOU are the legal entity exercising RESTRICTED RIGHTS under these terms and any other legal entities that YOU have more than 5% ownership of or equivalent control without ownership. YOUR is the possessive or adjective form of YOU.

【译文】

2.5 **您**是在这些条款下行使**受限权利**的法律实体，以及**您**拥有超过5%所有权或相当的非所有权控制权的其他法律实体。“**您的**”是“**您**”的所有格或形容词形式。

【原文】

2.6 A MACHINE LEARNING MODEL is a computational program or device that makes use of data to inflence its future logical operations, with or without inclusion of that data textually or in any recognizable form. Other names for MACHINE LEARNING MODEL are artificial intelligence (abbreviated AI), and large language model.

【译文】

2.6 **机器学习模型**是一种计算程序或设备，它使用数据影响其未来的逻辑操作，无论是否包含该数据的文本或任何可识别形式。**机器学习模型**的其他名称包括人工智能（简称 AI）和大型语言模型。

【原文】

2.7 To TRAIN is to input data to a MACHINE LEARNING MODEL or for the purpose of producing or improving a MACHINE LEARNING MODEL. TRAINED is the past tense of TRAIN.

【译文】

2.7 **训练**是向**机器学习模型**输入数据，或为了产生或改进一个**机器学习模型**的目的。**训练过**的是**训练**的过去时。

【原文】

2.8 AGGREGATION is the storage of multiple works on a storage medium for the purpose of permitting access to the indivual works for the purpose of transferring them to another medium, for example computer memory or another storage medium; or the provision of those works via a method of access, for example a web site, for the purpose of transferring the indivdual works to another medium.

【译文】

2.8 **聚合**是将多个作品存储在一个存储介质上，以便允许访问个别作品以将它们转移到另一个介质，例如计算机内存或另一个存储介质；或通过一种访问方法提供这些作品，例如一个网站提供这些作品，从而将这些单独的作品转移到另一个介质上。

【原文】

2.9 The WORK is the computer program, data, or other information to which these terms are applied by the LICENSOR, any derivative of the WORK under copyright or moral rights law, any transformation of the WORK (for example, compilation, text processing, non-literal copying), and any work combining or incorporating the WORK other than AGGREGTION, whether or not such combining or incorporation is considered derivative under copyright law or moral rights law. For example: a compiled program; a modified program; a program, system or device containing the WORK; a program produced by connecting another program and the WORK together except through a PUBLIC INTERFACE; a program that executes the WORK as a separate program to do some of its processing; a version of the WORK translated to a different computer language; a version of the texts of the WORK translated to another human language; or a MACHINE LEARNING MODEL TRAINED with the SOURCE CODE or any transformation of the WORK are all considered to be the WORK.

【译文】

2.9 **作品**是指**许可方**适用这些条款的计算机程序、数据或其他信息，任何根据版权或精神权利法的**作品**的衍生品，**作品**的任何转换（例如，编译、文本处理、非字面复制），以及除了**聚合**以外合并或纳入**作品**的任何作品，无论此类合并或纳入是否在版权法或精神权利法下被视为衍生作品。例如：编译后的程序；修改后的程序；包含**作品**的程序、系统或设备；除通过**公共接口**外，将另一个程序和**作品**连接在一起产生的程序；将**作品**作为单独程序进行部分处理的方式予以执行的程序；将**作品**翻译成不同计算机语言的版本；将**作品**的文本翻译成另一种人类语言的版本；或用**源代码**或作品的任何转换训练的**机器学习模型**，都被视为**作品**。

【原文】

2.10 COMPILATION is the creation of an executable form of the WORK from SOURCE CODE. COMPILATION generally involves multiple tools, for example a compiler, an assembler, and a linker. COMPILATON may include the use of conditional compilation facilities provided by the developers of the WORK, and configuration of the options of the aforementioned tools.

【译文】

2.10 **编译**是从**源代码**创建**作品**的可执行形式的过程。**编译**通常涉及多个工具，例如编译器、汇编器和链接器。**编译**可能包括使用**作品**开发者提供的条件编译设施，以及配置上述工具的选项。

【原文】

2.11 A PUBLIC INTERFACE is an interface that is part of a fundamental purpose of the work to provide services to other works without those works becoming MODIFICATIONS, or causing the combination of works. For example, the HTTP interface of a web browser, or the system call interface of an operating system kernel. The fundamental nature of the interface within the work is important, a developer may not unilaterally add a PUBLIC INTERFACE to an existing program or remove such an interface without the agreement of the other LICENSORS. The simple existence of an API does not automatically make that API a PUBLIC INTERFACE. PUBLIC INTERFACES means one or  more of a PUBLIC INTERFACE. [Where it could be unclear, the declaration of a public interface, or that a particular interface is not a public interface, may be stated in the CONTACT.txt file.]

【译文】

2.11 **公共接口**是作品的一部分，其基本目的是向其他作品提供服务，而不使这些作品被**修改**，或导致作品的组合。例如，网络浏览器的HTTP接口，或操作系统内核的系统调用接口。接口在作品中的基本性质很重要，开发者不能单方面向现有程序添加**公共接口**或在没有其他**许可方**同意的情况下移除此类接口。一个API的简单存在并不自动使该API成为**公共接口**。**公共接口(复数)**指的是一个或多个**公共接口**。[在可能不清楚的情况下，公共接口的声明，或特定接口不是公共接口的声明，可以在CONTACT.txt文件中说明。]

【原文】

2.12 MODIFICATION is:

* a) Any alteration or transformation of the WORK other than COMPILATION.
* b) The combination or inclusion of the WORK or any portion of it with another work other than through a PUBLIC INTERFACE or AGGREGATION, such that the two works are combined into a single program or application, regardless of the means of such combination or inclusion or or not such combination or inclusion is considered the creation of a derivative work under copyright and moral rights law. For example, dynamic linking, or the provision of a program through any interface that is integrated into a second program, such that the functionality of the first program is added to the combination of both programs. AGGREGATION is not MODIFCATION.

【译文】

2.12 **修改**是：

* a) 除**编译**外，对**作品**的任何改变或转换。
* b) 将**作品**或其任何部分与另一作品结合或包含在一起，除非通过**公共接口**或**聚合**，使得两个作品合并成一个单一程序或应用，无论此种结合或包含的手段如何，或者此种结合或包含是否在版权和精神权利法下被认为形成衍生作品。例如，动态链接，或通过任何集成到第二个程序中的接口提供程序，使得第一个程序的功能被添加到两个程序的组合中。**聚合**不是**修改**。

【原文】

2.13 RESTRICTED RIGHTS are the exercise of any rights regarding the WORK that are protected by copyright, patent, or moral rights law, and additionally any acts which are specifically restricted by these terms. RESTRICTED RIGHTS include (but are not limited to) ephemeral or other copying, reading or examining the WORK other than to read these terms and the CONTACT.txt file, use, redistribution, modification, performance of the WORK, TRAINING of a MACHINE LEARNING MODEL with SOURCE CODE or any transformation of the WORK, and exercise of any of the aforestated rights or acts upon a MACHINE LEARNING MODEL TRAINED thusly.

【译文】

2.13 **受限权利**是对受版权、专利或精神权利法保护的**作品**行使的任何权利，以及这些条款明确限制的任何行为。**受限权利**包括（但不限于）临时或其他复制，阅读或检查作品（除了阅读这些条款和CONTACT.txt文件之外），使用、再分发、修改、执行作品、用**源代码**或作品的任何转换形式**训练****机器学习模型**，以及对于以这种方式**训练**的**机器学习模型**行使上述任何权利或行为。

【原文】

2.14 PROTECTING JURISDICTIONS are those that provide legal protection of RESTRICTED RIGHTS regarding the work, except that they are not required to protect patents. Along with all of the usual copyright and/or moral rights protections, they must protect the copyright or moral rights of works used to used to TRAIN a MACHINE LEARNING MODEL. At this writing, (March, 2024) the POST-OPEN ADMINISTRATION asserts that the nation of Japan is not a PROTECTING JURISDICTION due to the lack of protection of works used to TRAIN a MACHINE LEARNING MODEL.

【译文】

2.14 **司法保护辖区**是对作品的有关**受限权利**提供法律保护的地区，但它们不需要保护专利。除了所有通常的版权和/或道德权利保护之外，它们还必须保护用于**训练****机器学习模型**的作品的版权或道德权利。截至本文撰写时（2024年3月），**后开放管理机构**声称，由于缺乏保护用于**训练****机器学习模型**的作品，日本国不是一个**司法保护辖区**。

【原文】

2.15 The LICENSOR is the legal entity which owns the WORK, and which applies these terms to it. LICENSORS means one or more LICENSOR. Most works in the POST-OPEN COLLECTION will be the product of many real persons, and businesses, and organizations, who may license it directly or through another legal entity.

【译文】

2.15 **许可方**是拥有**作品**并将这些条款应用于它的法律实体。**许可方(复数)**意味着一个或多个**许可方**。**后开放系列**中的大多数作品将是许多自然人、企业和组织的产品，他们可以直接或通过另一个法律实体进行许可。

【原文】

2.17 SOURCE CODE is the human-readable, unobfuscated and preferred form of a work for modification. In the case of a compiled or interpreted computer language, this would be the language used as input to the compiler or interpreter.

【译文】

2.17 **源代码**是作品的人类可读、无歧义且首选的便于修改的形式。在编译或解释的计算机语言的情况下，这将是用作编译器或解释器输入的语言。

【译注】 2.16 在原文中就缺失了

【原文】

2.18 PUBLIC RELEASE is the publication of the SOURCE CODE of the WORK or a MODIFICATION in a public site on the internet, licensed under these terms, where it is expected to be permanently and reliably available worldwide for download without any permission or legal agreement in addition to these terms. One example, at this writing, would be a public repository on "github.com". [The most common practical form of PUBLIC RELEASE at this writing is contribution of a modification to a project via the "pull" mechanism of public "git" repository.]

【译文】

2.18 **公开发布**是指在互联网的公开网站上发布**作品**或**修改**的**源代码**，并在这些条款下许可，期望它能在全球范围内永久且可靠地供人下载，无需除这些条款之外的任何许可或法律协议。在本文撰写时的一个例子，将是“github.com”上的一个公共存储库。[目前最常见的**公开发布**实践形式是通过公共“git”仓库的“pull”机制向项目贡献修改。]

【原文】

2.19 The POST-OPEN COLLECTION is all works that have been placed under these terms by LICENSORS who have entered into the POST-OPEN OPERATING AGREEMENT, and for which PUBLIC RELEASE has been performed.

【译文】

2.19 **后开放系列**是指那些已签订**后开放运营协议**的**许可方**按照这些条款放置的所有作品，并且已进行了**公开发布**。

【原文】

2.20 TERMINATION immediately discontinues YOUR GRANT OF RIGHTS to all works in the POST-OPEN COLLECTION, including (but not limited to) the WORK, but all other terms contine to apply and YOUR consent to these terms survives TERMINATION. TERMINATION is never ended automatically, or simply by the cure of the condition causing TERMINATION. YOU must take a specific action to cure TERMINATION, such as entering into one of the contracts that allows the condition that previously caused TERMINATION (the POST-OPEN ZERO-COST CONTRACT or the POST-OPEN PAID CONTRACT), or by participating in the POST-OPEN INFRINGEMENT PROCESS. TERMINATES is the act or past-tense of TERMINATION.

【译文】

2.20 **终止**立即结束**您**对**后开放系列**中所有作品的**权利授予**，包括（但不限于）**作品**，但所有其他条款继续适用，且**您**对这些条款的同意在**终止**后仍然有效。**终止**从不会自动结束，或仅仅通过纠正导致**终止**的条件而结束。**您**必须采取特定行动来纠正**终止**，例如签订允许先前导致**终止**的条件的其中一份合同（**后开放零成本合同**或**后开放付费合同**），或参与**后开放侵权处理流程**。**终止**是**终止**的行为或过去时。

【原文】

**3. CONDITIONS**

**3.1 ZERO-COST CONDITIONS**

TERMINATION occurs when any of the conditions in the following list apply to YOU and YOU have not already entered into the POST-OPEN ZERO-COST CONTRACT. If YOU wish to continue to exercise RESTRICTED RIGHTS after one of these conditions applies, YOU may enter into the POST-OPEN ZERO-COST CONTRACT. [Which is a version of these same terms with the addition of clear and recorded consent by the licensee.]

*  a) You exercise RESTRICTED RIGHTS outside of a PROTECTING JURISDICTION.

【译文】

**3. 条件**

**3.1 零成本条件**

当以下列表中的任何条件适用于**您**且**您**尚未签订**后开放零成本合同**时，将发生**终止**。如果在其中一种情况适用后**您**希望继续行使**受限权利**，**您**可以签订**后开放零成本合同**。[这是这些相同条款的一个版本，增加了被许可人的明确和记录在案的同意。]

* a) **您**在**司法保护辖区**之外行使**受限权利**。

【原文】

**3.2 PAID CONDITIONS**

TERMINATION occurs when any of the conditions in the following list apply to YOU. If YOU wish to continue to exercise RESTRICTED RIGHTS, YOU may enter into the POST-OPEN PAID CONTRACT. [Which is a separate agreement that gives permission to perform the stated actions, in exchange for annual payment and an annual disclosure requirement.]

* a) The end-user revenue through all legal entities in which YOU have ownership exceeding 5% or equivalent control without ownership exceeds USD$5 Million anually. End-user revenue is all money or other value collected from customers, including the financial value equivalent of any non-monetary remuneration such as barter or the grant of rights or privileges.
* b) You provide, for remuneration, any work in the POST-OPEN COLLECTION to others, other than PERSONAL USE, or perform that provision at the order of another legal entity that receives remuneration for it. This includes (but is not limited to) provision of the work as a service; or inclusion of the work in a product that is sold, for example software that is sold or sale of a device containing the WORK.
* c) You make MODIFICATIONS to any WORK in the POST-OPEN COLLECTION without performing one of these actions (you may perform both):
    * I)  You enter into the POST-OPEN OPERATING AGREEMENT and make a PUBLIC RELEASE of the MODIFICATION.
    * II) You enter into the POST-OPEN PAID CONTRACT.

【译文】

**3.2 付费条件**

当以下列表中的任何条件适用于**您**时，将发生**终止**。如果**您**希望继续行使**受限权利**，您可以签订**后开放付费合同**。[这是一个单独的协议，允许执行规定的行动，以换取年度支付和年度披露要求。]

* a)  通过**您**拥有超过5%所有权或等效无所有权控制的所有法律实体，最终用户收入年度超过500万美元。最终用户收入是从客户收集的所有金钱或其他价值，包括任何非货币报酬的财务价值等价物，如易货或权利或特权的授予。
* b)  除了个人使用外，**您**为**他人**提供**后开放系列**中的任何作品以获取报酬，或者按另一个获得报酬的法律实体的命令执行该提供。这包括（但不限于）以服务形式提供作品；或将作品包含在出售的产品中，例如出售的软件或包含**作品**的设备的销售。
* c)  您对**后开放系列**中的任何**作品**进行**修改**，未执行以下行动之一（您可以执行两者）：
    * I)  您签订**后开放运营协议**并进行**修改**的**公开发布**。
    * II) 您签订**后开放付费合同**。

【译注】本质上类似于双许可（Dual-License）

【原文】

**3.3 TERMINATION CONDITIONS**

TERMINATION occurs if any of the conditions in the following list apply to you.

【译文】

**3.3 终止条件**

如果以下列表中的任何条件适用于您，则会发生**终止**。

【原文】

a) You perform any action prohibited by these terms, breach this contract, or infringe RESTRICTED RIGHTS of any work in the POST-OPEN COLLECTION.

【译文】

a) 您执行这些条款禁止的任何行为，违反此合约，或侵犯**后开放系列**中任何作品的**受限权利**。

【译注】结成了一个保护同盟，一个都不能被侵犯。

【原文】

b) You bring suit or other enforcement for patent infringement regarding any work in the POST-OPEN COLLECTION or cause, fund or join such a suit or enforcement.

【译文】

b) 您对后开放系列中的任何作品提起专利侵权诉讼或进行其他执法，或导致、资助或加入此类诉讼或执法。

【原文】

c) YOU further restrict the rights granted in these terms, YOU add any terms to these terms, or YOU make separate terms which change the effect of these terms. For example, you enter into a contract with users which includes a punitive action if they redistribute security information regarding a work in the POST-OPEN COLLECTION or MODIFICATIONS of such a work intended to cure or mitigate a security issue.

【译文】

c) **您**进一步限制这些条款中授予的权利，**您**添加任何条款到这些条款中，或**您**制定单独的条款改变这些条款的效果。例如，您与用户签订合约，如果他们重新分发有关**后开放系列**中作品或旨在纠正或减轻安全问题的该作品的**修改**的安全信息，则包含惩罚性行动。

【原文】

d) You cause the any work in the POST-OPEN COLLECTION to potentially become subject to export control laws (for example the US ITAR and EAR) by exercising RESTRICTED RIGHTS for military, defense, or weaponization purposes; by requesting or participating in support or services regarding any work in the POST-OPEN COLLECTION for military, defense, or weaponization purposes, or by making a MODIFICATION of any work in the POST-OPEN COLLECTION for military, defense, or weaponization purposes.

【译文】

d) 由于您出于军事、防御或武器化目的行使**受限权利**；请求或参与与**后开放系列**中任何作品的军事、防御或武器化目的相关的支持或服务；或出于军事、防御或武器化目的**修改****后开放系列**中的任何作品，您导致**后开放系列**中的任何作品可能受到出口控制法律（例如美国的ITAR和EAR）的约束。

【译注】这一条看起来违背了“OSD中的非歧视性条款”，但在事实上，却有利于作品被更大范围的使用。


【原文】

e) YOU deliberately do not report security-related information regarding the any work in the POST-OPEN COLLECTION to the LICENSOR and the POST-OPEN ADMINISTRATION as soon as possible, or YOU create an agreement with terms restricting any other party from making such a report, except in the case that you are legally restricted from making such a disclosure by a direct order of your government (rather than a private agreement such as an NDA), and then only as long as such a restriction applies. [Please see https://postopen.org/security/ to make a report to the POST-OPEN ADMINISTRATION and the LICENSOR.]

For example, if YOU are a company or other entity that provides security services, and you disclose security information about the WORK to your customers and affiliates without also disclosing it to the POST-OPEN ADMINISTRATION and the LICENSOR before then or at the same time, you violate these terms and TERMINATION occurs.

【译文】

e) **您**故意不尽快向**许可方**和**后开放管理机构**报告**后开放系列**中任何作品的与安全相关的信息，或者**您**创建一个协议，其条款限制任何其他方进行此类报告，除非您因直接受到政府命令（而不是私人协议如保密协议）而法律上被禁止进行此类披露，在此情况下，只有当此类限制适用时才是如此。[请访问 [https://postopen.org/security/](https://postopen.org/security/) 向**后开放管理机构**和**许可方**报告。]

例如，如果**您**是一家提供安全服务的公司或其他实体，并且您在之前或同时没有向**后开放管理机构**和**许可方**披露有关**作品**的安全信息，而仅向您的客户和关联方披露，则您违反了这些条款，**终止**发生。

【原文】

f) You train a MACHINE LEARNING MODEL with the SOURCE CODE or any transformation of a work within the POST-OPEN COLLECTION, or exercise any rights protected by copyight, patent, or moral rights law regarding a MACHINE LEARNING MODEL TRAINED with the text of a work within the POST-OPEN COLLECTION. These would include (but are not limited to) use, copying, or redistribution of such a model; exercise of the same rights on the behalf of others; or having those rights exercised on YOUR behalf.

【译文】

f) 您使用**后开放系列**内的**源代码**或任何作品的转换训练**机器学习模型**，或行使受版权、专利或精神权利法保护的关于以**后开放系列**内的作品文本**训练**的**机器学习模型**的任何权利。这些将包括（但不限于）使用、复制或重新分发此类模型；代表他人行使相同的权利；或让这些权利在**您**的代表下被行使。

【译注】看来是为了封堵GitHub Copilot的行为

【原文】

g) YOU are unresponsive for more than 60 days to enforcement-related communications of the POST-OPEN ADMINISTRATION regarding these terms or one of these agreements if you have entered into it: the POST-OPEN ZERO-COST CONTRACT, the POST-OPEN PAID CONTRACT, or the POST-OPEN OPERATING AGREEMENT.

【译文】

g) 如果**您**已经签订如下的其中一个合同：**后开放零成本合同**、**后开放付费合同**或**后开放运营协议**，您对**后开放管理机构**关于这些条款或其中一个协议的与执法相关的通信超过60天天没有响应。

【原文】

**4. TERMS**

These terms include this entire document, including (but not limited to) the DEFINITIONS and PRELUDE, except for the ADVISORY SECTIONS.

【译文】

**4. 条款**

这些条款包括本整个文档，包括（但不限于）定义和序言，但咨询部分除外。

【原文】

4.1 REQUIREMENT TO LICENSE

You must license the WORK if YOU exercise RESTRICTED RIGHTS, even the right to read or examine the WORK, or if another legal entity exercises RESTRICTED RIGHTS on YOUR behalf, for example a software-as-a-service business which provides servers that execute the WORK for YOU. You may license the WORK via these terms, or by executing the POST-OPEN ZERO-COST CONTRACT or the POST-OPEN PAID CONTRACT.

At your option, you may enter into the POST-OPEN ZERO-COST CONTRACT at any time. This provides you a executed contract with these same terms, and consent by YOU and the POST-OPEN ADMINISTRATION, which may be more convenient to your business or legal process.

【译文】

**4.1 许可要求**

如果**您**行使**受限权利**，即使是阅读或检查**作品**的权利，或者如果另一个法律实体代表**您**行使**受限权利**，例如为**您**执行**作品**的 SaaS 业务，您必须对**作品**进行许可。您可以通过这些条款进行许可，或通过执行**后开放零成本合同**或**后开放付费合同**进行许可。

您可以选择随时签订**后开放零成本合同**。这为**您**提供了一个与这些相同条款的执行合同，并得到**您**和**后开放管理机构**的同意，这可能更便于您的业务或法律流程。

【原文】

4.2 RIGHTS RESTRICTION

No exercise of RESTRICTED RIGHTS, including (but not restricted to) ephemeral copying, is permitted except under these terms or by entering into the POST-OPEN ZERO-COST CONTRACT, the POST-OPEN PAID CONTRACT, or the POST-OPEN OPERATING AGREEMENT, as applicable.

【译文】

**4.2 权利限制**

除非根据这些条款或通过进入**后开放零成本合同**、**后开放付费合同**或**后开放运营协议**（视情况而定），否则不允许行使**受限权利**，包括（但不限于）瞬时复制。

【原文】

4.3 NO WARRANTY, REQUIREMENT FOR INDEMNIFICATION

To the extent permissible by law, no warranties are applicable to the WORK, even warranties of usability or fitness for use. You agree to indemnify the LICENSOR and the POST-OPEN ADMINISTRATION regarding any hazard or liability caused by YOUR use of the WORK, including (but not limited to) damages to you and others, penalties or fines levied by government, and prosecution of patent infringement resulting from YOUR exercise of RESTRICTED RIGHTS. If such liability is of concern to YOU, you are advised to purchase insurance to protect YOU from it. [The POST-OPEN ADMINISTRATION does not offer such insurance at this time.]

【译文】

**4.3 无保证，赔偿要求**

在法律允许的范围内，对**作品**不适用任何保证，即使是适用性或适宜性的保证。您同意就您使用**作品**引起的任何风险或责任，包括（但不限于）对**您**和他人的损害、政府征收的罚款或罚金以及由于您行使**受限权利**而导致的专利侵权诉讼，对**许可方**和**后开放管理机构**进行赔偿。如果**您**对此类责任感到担忧，建议**您**购买保险以保护自己。[目前**后开放管理机构**不提供此类保险。]

【原文】

4.4 ASSERTION OF PRESENCE OF DEFECTS, NO RESPONSIBILITY TO REPORT OR CURE

There are defects in the WORK, both known and unknown, including (but not limited to) ones with a potential effect upon security or privacy of the user, and ones that could conceivably cause damage to life or property. It is not technically or economically possible to produce a work free of defects within the state of the art at this time. The LICENSOR and the POST-OPEN ADMINISTRATION may operate a defect reporting system, but decline responsibility to report, repair, or cure defects under these terms, to the extent permissible by law. Such serivces may be available through a paid support contract.

【译文】

**4.4 声明存在缺陷，无报告或纠正责任**

**作品**存在已知和未知的缺陷，包括（但不限于）可能影响用户安全或隐私的缺陷，以及可能导致对生命或财产造成损害的缺陷。在目前的技术水平下，生产一个无缺陷的作品在技术上或经济上是不可能的。**许可方**和**后开放管理机构**可能运行一个缺陷报告系统，但在法律允许的范围内拒绝报告、修复或纠正缺陷的责任。此类服务可能通过付费支持合同获得。

【原文】

4.5 ASSERTION OF THE POSSIBILITY OF PATENT CLAIMS

The WORK may be considered to come under one or more existing patent claims, regardless of the validity or enforcibility of such claims. A complete patent search and the development of an understanding of what patents are actually valid or enforcible is not technically or economically possible. The liability for such claims is entirely yours, and the LICENSOR and the POST-OPEN ADMINISTRATION deny any such liability, including to YOU. If such liability is of concern to YOU, YOU are advised to purchase insurance to protect you from it.

【译文】

**4.5 声明可能存在专利索赔的可能性**

**作品**可能被视为落入一个或多个现有专利索赔之下，不论这些索赔的有效性或可执行性如何。完全进行专利搜索并了解哪些专利实际有效或可执行在技术上或经济上是不可能的。对于此类索赔的责任完全由**您**承担，**许可方**和**后开放管理机构**拒绝承担任何此类责任，包括对**您**的责任。如果**您**对此类责任感到担忧，建议**您**购买保险以保护自己。

【原文】

4.6 MODIFICATION

MODIFICATION of the WORK with PUBLIC RELEASE requires entry into the POST-OPEN OPERATING AGREEMENT. If YOU wish to make MODIFICATIONS without PUBLIC RELEASE, YOU must enter into the POST-OPEN PAID CONTRACT. You may enter into both and make modifications under each as appropriate. If YOU perform MODIFICATION without entering into the POST-OPEN OPERATING AGREEMENT or the POST-OPEN PAID CONTRACT, TERMINATION occurs.

Producers of significant MODIFICATIONS and new works are advised that if YOU make PUBLIC RELEASE and enter into the POST-OPEN OPERATING AGREEMENT, the POST-OPEN ADMINISTRATION may pay you with part of the revenue collected under the POST-OPEN PAID CONTRACT. Thus, there is a financial incentive for all parties to publish their modifications and increase the size and functionality of the POST-OPEN COLLECTION.

Modifications that are made available via PUBLIC RELEASE are more likely to be maintained as part of the overall project, while private modifications must be brought up to sync with every public release if you wish to use the features and bug fixes in that release, and this will be a continuing expense.

【译文】

**4.6 修改**

带有公开发布的**作品**的**修改**需要签订**后开放运营协议**。如果**您**希望在不进行**公开发布**的情况下进行修改，**您**必须签订**后开放付费合同**。您可以同时签订这两个合同，并根据情况进行修改。如果您在不签订**后开放运营协议**或**后开放付费合同**的情况下进行**修改**，则发生**终止**。

对于重大**修改**和新作品的制作者，建议如果**您**进行**公开发布**并签订**后开放运营协议**，**后开放管理机构**可能会用**后开放付费合同**收到的部分收入支付给您。因此，发布修改并增加**后开放系列**的规模和功能对所有方都有财务激励。

通过**公开发布**提供的**修改**更有可能作为整个项目的一部分得到维护，而私人修改必须与每次公开发布同步更新，如果您希望使用该发布中的功能和错误修复，则这将是一个持续的费用。

【译注】最后其实再次强调了上游优先的原则

【原文】

4.7 CONSENT AND AGREEMENT

This is a contract between YOU, the LICENSOR, and the POST-OPEN ADMINISTRATION. Exercise of any RESTRICTED RIGHTS indicates YOUR consent to these terms. YOU may explicitly indicate your consent by entering into the POST-OPEN ZERO-COST CONTRACT, but your consent is indicated whether or not you do so.

If YOU are a government, nation, or soverign power, you agree to comply with the law and these terms as they would apply to real persons in your jurisdiction. You specifically consent to allow and commit to respond to any lawsuit by the LICENSOR or the POST-OPEN ADMINISTRATION.

If YOU are more than one legal entity, each individual entity which exercises RESTRICTED RIGHTS must enter into these terms, the POST-OPEN ZERO-COST LICENSE, or the POST-OPEN PAID LICENSE.

YOU agree to comply with these terms regardless of the status of the WORK under copyright, moral rights, or patent law. Where the law grants YOU a right and these terms prohibit it, these terms shall prevail to the extent permitted by law. YOU agree not to exercise RESTRICTED RIGHTS outside of these terms. You agree not to TRAIN a MACHINE LEARNING MODEL with the information of any work in the POST-OPEN COLLECTION. You agree not to perform ephemeral copying with the purpose of TRAINING such a model.

【译文】

**4.7 同意和协议**

这是**您**、**许可方**和**后开放管理机构**之间的合同。行使任何**受限权利**表明**您**同意这些条款。**您**可以通过签订**后开放零成本合同**明确表示您的同意，但无论您是否这样做，您的同意都已经表达了。

如果**您**是政府、国家或主权力量，您同意遵守法律和这些条款，就像它们适用于您管辖范围内的自然人一样。您特别同意允许并承诺响应**许可方**或**后开放管理机构**提起的任何诉讼。

如果**您**是不止一个法律实体，每个行使**受限权利**的单独实体必须签订这些条款、**后开放零成本许可**或**后开放付费许可**。

不论**作品**在版权、道德权利或专利法下的状态如何，**您**同意遵守这些条款。当法律赋予**您**一项权利而这些条款禁止它时，这些条款在法律允许的范围内将占上风。**您**同意不在这些条款之外行使**受限权利**。**您**同意不使用**后开放系列**中任何作品的信息**训练****机器学习模型**。您同意不进行瞬时复制以**训练**此类模型的目的。

【原文】

4.8 NO RIGHT TO RELICENSE

This agreement directly is between the LICENSOR, the POST-OPEN ADMINISTRATION, and YOU. When you convey a copy of the WORK to another party, or run the work as a service on behalf of another party, you must give them a copy of these terms and inform them that the WORK is covered by these terms. These terms then apply directly between them, the LICENSOR, and the POST-OPEN ADMINISTRATION.

【译文】

**4.8 无权再许可**

本协议直接涉及**许可方**、**后开放管理机构**和**您**。当您向另一方转让**作品**的副本，或代表另一方运行作品作为服务时，您必须给他们一份这些条款的副本，并通知他们作品受这些条款约束。这些条款然后直接适用于他们、**许可方**和**后开放管理机构**之间。

【原文】

4.9 PUBLIC INTERFACES

YOU agree to connect the WORK to software which is not under these terms only through its PUBLIC INTERFACES. YOU agree that an API present in the WORK which is not declared a PUBLIC INTERFACE is not permissible for use for connecting to programs that are not under these terms.

【译文】

**4.9 公共接口**

**您**同意只通过其**公共接口**将**作品**连接到不受这些条款约束的软件。**您**同意，在**作品**中存在的API如果未声明为**公共接口**，则不允许用于连接到不受这些条款约束的程序。

【原文】

4.11 NO CIRCUMVENTION

YOU agree not to employ legal or technical strategies with the main purpose of circumventing the effect of these terms. For example, creating a legal entity for the purpose of entering into these terms while insulating another legal entity from these terms; or creating a technical means of linking a program in the POST-OPEN COLLECTION to a second program which is not under these terms, without that second program being considered part of the WORK.

【译文】

**4.11 禁止规避**

**您**同意不采用法律或技术策略，其主要目的是规避这些条款的效果。例如，创建一个法律实体目的是为了签订这些条款，同时使另一个法律实体免受这些条款的约束；或创建一个技术手段将**后开放系列**中的程序链接到第二个不受这些条款约束的程序，而不将该第二程序视为**作品**的一部分。

【译注】4.10 在原文中就缺失了

【原文】

4.12 GRANT OF RIGHTS

In consideration of your consent to the entirety of these terms: as long as TERMINATION has not occured, you are granted the right to exercise RESTRICTED RIGHTS other than MODIFICATION, including (but not restricted to) use and redistribution of the WORK and exercise of patent claims of the LICENSOR and the POST-OPEN ADMINISTRATION necessary to exercise RESTRICTED RIGHTS other than MODIFICATION under these terms.

【译文】

**4.12 授予权利**

考虑到您对这些条款的全部同意：只要未发生**终止**，您将被授予除修改以外的行使**受限权利**的权利，包括（但不限于）使用和重新分发作品以及行使**许可方**和**后开放管理机构**的专利索赔，这些专利索赔对行使这些条款下的除**修改**以外的***受限权利***是必要的。

【原文】

4.13 CONDITIONS FOR TERMINATION

At the moment that the PAID CONDITIONS, ZERO-COST CONDITIONS, or TERMINATION CONDITIONS apply to YOU, TERMINATION occurs. You may then, as applicable, enter into the POST OPEN ZERO-COST CONTRACT, the POST-OPEN PAID CONTRACT, or YOU may contact the POST-OPEN ADMINISTRATION regarding curing an infringement under the POST-OPEN INFRINGEMENT PROCESS. Please pre-emptively enter into the aforementioned agreements before such a situation arises.

【译文】

**4.13 终止条件**

一旦**付费条件**、**零成本条件**或**终止条件**适用于**您**，**终止**就会发生。然后，根据适用情况，您可以签订**后开放零成本合同**、**后开放付费合同**，或**您**可以联系**后开放管理机构**关于在**后开放侵权处理流程**下纠正侵权。请在此类情况发生之前预先签订上述协议。

【原文】

4.14 SEVERABILITY

If a court should strike any of these terms or find them unenforcible, the minimum possible text is struck and the remainder of these terms survive.

【译文】

**4.14 可分割性**

如果法院裁定这些条款的任何部分无效或不可执行，将尽可能少地删除文本，并且这些条款的其余部分仍然有效。

【原文】

4.15 ACCEPTANCE OF THE POST-OPEN ADMINISTRATION AS A PARTY TO ANY DISPUTE

YOU accept that the POST-OPEN ADMINISTRATION has the right to represent the LICENSOR in any controversy or claim arising out of or relating to these terms.

【译文】

**4.15 接受后开放管理机构作为任何争议的一方**

**您**接受**后开放管理机构**有权代表**许可方**处理因这些条款产生或与这些条款相关的任何争议或索赔。

【原文】

4.16 ARBITRATION

Any controversy or claim arising out of or relating to these terms, or the breach thereof, shall be settled by arbitration administered by the American Arbitration Association if the parties are all within the United States, or the International Centre for Dispute Resolution in the case that a party to the dispute is external to the United States, in accordance with the Commercial Arbitration Rules and/or other appropriate rules of those organizations. Judgment on the award rendered by the arbitrator(s) may be entered in any court having jurisdiction thereof. YOU and all parties to these terms consent
to the use of computer videoconferencing or telephone conferencing, rather than personal appearance, for the operation of arbitration and any court session.

【译文】

**4.16 仲裁**

由这些条款或其违反引起的任何争议或索赔，如果当事方都在美国内，应由美国仲裁协会管理进行仲裁，或如果争议方位于美国外，则由国际争议解决中心进行仲裁，按照这些组织的商业仲裁规则和/或其他适当规则进行。仲裁员的裁决可以在有管辖权的任何法院进入判决。您和所有这些条款的方同意使用计算机视频会议或电话会议而不是亲自出现，用于仲裁和任何法庭会议的运作。

【原文】

4.17 REVISION OF THESE TERMS

During the present DRAFT terms period, changes to these terms published as a revised DRAFT by the POST-OPEN ADMINISTRATION are effective immediately and superscede the terms previously issued.

After the first publication of a FINAL version of these terms, the following terms apply:

The POST-OPEN ADMINISTRATION may publish revised versions of these terms. Revised terms will remain substantially similar to these ones, and may include changes only to:

* a) Correct errors and ambiguities.
* b) Avoid loopholes that have come into use.
* c) Respond to findings of courts which server some of the terms or interpret some of the terms unfavorably.
* d) Respond to new law or law newly enforced upon any party to these terms.
* e) Respond to changes in technology (for example, this text responds to the rise of MACHINE LEARNING MODELS and TRAINING of such, terms which were not included in classical Open Source licenses). 
* f) Respond to changes in monetary value: for example, a change in the real value of the stated amount of end-user revenue requiring that YOU join into the POST-OPEN PAID CONTRACT, or a change in the nation or other entity for which that value is defined: (for example, a change from USD to a presently-theoretical stable global currency).

When changes to these terms are published as FINAL revised terms by the POST-OPEN ADMINISTRATION (rather than a DRAFT), YOU may, at your discretion, immediately apply the new terms, or you may continue to apply these terms to works already in your use for no more than one year from the publication of the revised terms. If you begin to use another work in the collection, the new terms apply to it immediately. [This allows the licensee time for legal evaluation of the new terms and to make decisions regarding their use of the POST-OPEN COLLECTION.]

【译文】

**4.17 这些条款的修订**

在当前**草案**条款期间，**后开放管理机构**发布的这些条款的修订**草案**立即生效，并取代之前发布的条款。

在这些条款的第一个**最终**版本发布后，适用以下条款：

**后开放管理机构**可以发布这些条款的修订版本。修订后的条款将与这些条款大体相似，并且只可能包括以下变更：

* a) 更正错误和歧义。
* b) 避免已经开始使用的漏洞。
* c) 响应一些法院对条款的服务或不利解释的发现。
* d) 响应对这些条款的任何一方新施加的新法律或新执行的法律。
* e) 响应技术变化（例如，本文响应**机器学习模型**的兴起及其**训练**，这些术语不包括在传统开源许可中）。
* f) 响应货币价值变化：例如，更改要求您加入**后开放付费合同**的最终用户收入声明金额的实际价值，或更改定义该价值的国家或其他实体：（例如，从美元更改为目前理论上的稳定全球货币）。

当**后开放管理机构**以**最终**修订条款（而非**草案**）形式发布这些条款的变更时，**您**可以自行决定立即适用新条款，或者您可以继续对已在您使用中的作品适用这些条款，但最多不超过从修订条款发布之日起的一年。如果您开始使用系列中的另一个作品，则新条款立即对其适用。[这允许被许可人时间进行新条款的法律评估，并就他们使用**后开放系列**的决策进行决定。]

【译后记】

* 可以发现，这个草稿，的确还是非常“潦草”的。
* **后开放管理机构**及其系列的合同，是一个野心勃勃的策划，不确定是否能够成功。
* 以上的构想本身是有价值的，但是也许以开源基金会（或者开源基金会的联盟）作为载体来推行，或更加有可行性。