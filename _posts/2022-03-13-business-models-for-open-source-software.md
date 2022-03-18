---
layout: post
title: 【翻译】开源软件的商业模式
date: 2022-03-13 10:35 +0800
categories: OpenSource Business
comments: true
---

**本文的翻译，得到阿法兔同学的大力帮助，非常感谢。欢迎订阅他的微信公众号“阿法兔研究笔记”**

在维基百科上找到一个英文词条 [Business models for open-source software](https://en.wikipedia.org/wiki/Business_models_for_open-source_software) ，因为无法登录编辑，只能先借助 DeepL 翻译在自己的博客上，以后有机会再转过去。

# Business models for open-source software / 开源软件的商业模式

Companies whose business centers on the development of open-source software employ a variety of business models to solve the challenge of how to make money providing software that is by definition licensed free of charge. Each of these business strategies rests on the premise that users of open-source technologies are willing to purchase additional software features under proprietary licenses, or purchase other services or elements of value that complement the open-source software that is core to the business. This additional value can be, but not limited to, enterprise-grade features and up-time guarantees (often via a [service-level agreement](https://en.wikipedia.org/wiki/Service-level_agreement)) to satisfy business or compliance requirements, performance and efficiency gains by features not yet available in the open source version, legal protection (e.g., indemnification from copyright or patent infringement), or professional support/training/consulting that are typical of proprietary software applications.

以开发开源软件为核心业务的公司，通过采用各类商业模式，解决如何用开源软件赚钱的问题（因为通常开源软件的定义是 Free，免费许可的）。每一种商业策略都建立在这样一个前提上：开源技术的用户，愿意在专有许可证的要求下，购买额外的软件功能，或者购买其他服务或有价值的部分，作为对开源业务核心的补充。购买的额外的价值包括但不限于：企业级服务和功能、通过服务级别协议对运行时间的保证。还有为了满足业务合规性要求，通过开源版本尚未提供的功能，提高性能和效率，法律保护（例如，对版权或专利侵权的赔偿），或专业支持/培训/咨询，等同于常见的专利软件应用场景。

Historically, these business models started in the late 1990s and early 2000s as "[dual-licensing](https://en.wikipedia.org/wiki/Multi-licensing)" models, for example [MySQL](https://en.wikipedia.org/wiki/MySQL),[^1] and have matured over time to include many variations, as described in the sections below.  Pure dual licensing models are not uncommon, as a more nuanced business approach to open source software businesses has developed. Many of these variations are referred to an ["open core" model](https://en.wikipedia.org/wiki/Open-core_model), where the companies develop both open source software elements and other elements of value for a combined product.

从历史上看，这些商业模式始于 20 世纪 90 年代末和 21 世纪初的“双重许可” 模式，例如 MySQL，[^1] 随着时间的推移，而逐渐发展成熟，当然它也发生了一些变化，会在后面的部分进行阐述。 纯粹的双许可模式相对常见，对开源软件企业来说，已经形成了一种更细致的商业模式。其中许多变种，被称作“开放核心（open core）”模式，即公司同时开发开放源码软件元素和其他价值元素的组合产品。

A variety of open-source compatible business approaches have gained prominence in recent years, as illustrated and tracked by the Commercial Open Source Software Index (COSSI),[^2] a list of commercial open source companies that have reached at least US$100 million in revenue. Notable examples include [open core](https://en.wikipedia.org/wiki/Open-core_model) (sometimes referred to as [dual licensing](https://en.wikipedia.org/wiki/Dual_licensing) or [multi-licensing](https://en.wikipedia.org/wiki/Multi-licensing)), [software as a service](https://en.wikipedia.org/wiki/Software_as_a_service) (not charging for the software but for the tooling and platform to consume the software as a service often via subscription), [freemium](https://en.wikipedia.org/wiki/Freemium), donation-based funding, [crowdfunding](https://en.wikipedia.org/wiki/Crowdfunding), and [crowdsourcing](https://en.wikipedia.org/wiki/Crowdsourcing).

近年来，各类能与开源兼容的商业模式已逐步得到了重视，正如商业开源软件指数（COSSI）[^2] 所记载的，名单上的商业开源公司的收入至少达到 1 亿美元。值得注意的案例，包括开放核心（有时被称为双重许可或多重许可）、软件即服务（不是对软件收费，而是对工具和平台收费，以消费软件作为服务，通常通过订阅）、免费、基于捐赠的资金、众筹和众包模式。

There are several different types of business models for making profit using open-source software (OSS) or funding the creation and ongoing development and maintenance. Below are a list of current existing and legal commercial business models approaches in context of open-source software and open-source licenses.[^3] The acceptance of these approaches varies; some of these approaches are recommended (like open core and selling services), others are accepted, while still others are considered controversial or even unethical by the open-source community. The underlying objective of these business models is to harness the size and international scope of the open-source community (typically more than an order of magnitude larger than what would be achieved with closed-source software equivalents) for a sustainable commercial venture. The vast majority of commercial open-source companies experience a conversion ratio (as measured by the percentage of downloaders who buy something) well below 1%, so low-cost and highly-scalable marketing and sales functions are key to these firms' profitability.[^4]

几种不同类型的商业模式均可以通过开源软件（OSS）盈利，或者为开源的持续开发、维护提供资金。以下是目前在开源软件和开源许可证背景下，目前合规的商业模式。[^3] 这些模式的接受程度各不相同；其中一些被广泛推荐和接受（如开放核心和销售服务），还有一些在开源社区中是有争议的，甚至经常被认为是不道德的。这些商业模式的目标是利用开源社区的规模和国际范围（通常比闭源软件的同等规模大一个数量级以上）来实现可持续的商业调整。绝大多数商业性的开源公司的转化率（以购买东西的下载者的百分比衡量）远远低于 1%，因此，公司的盈利关键，就是低成本和高度可扩展的营销和销售环节。[^4]

## Not selling code / 不出售代码

### Professional services / 专业服务

Open-source software can also be commercialized from selling [services](https://en.wikipedia.org/wiki/Service_(economics)), such as training, [technical support](https://en.wikipedia.org/wiki/Technical_support), or [consulting](https://en.wikipedia.org/wiki/Information_technology_consulting), rather than the software itself.[^5][^6]

开源软件可以通过销售服务来实现商业化，比如培训、技术支持或咨询。[^5][^6]

Another possibility is offering open-source software in [source code](https://en.wikipedia.org/wiki/Source_code) form only, while providing [executable](https://en.wikipedia.org/wiki/Executable) binaries to paying customers only, offering the commercial service of [compiling](https://en.wikipedia.org/wiki/Compiling) and [packaging](https://en.wikipedia.org/wiki/Package_(package_management_system)) of the software. Also, providing goods like physical [installation media](https://en.wikipedia.org/wiki/Data_storage_device) (e.g., [DVDs](https://en.wikipedia.org/wiki/DVD)) can be a commercial service.

另一种模式是单纯提供源代码形式的开源软件，而仅向付费客户提供可执行的二进制文件，包括软件的编译和包装等商业服务。另外，提供实物安装媒介（如 DVD）等商品，也可以视作一种商业服务。

Open-source companies using this business model successfully are, for instance RedHat,[^7] IBM, SUSE, Hortonworks (for Apache Hadoop), Chef, and Percona (for open-source database software).

成功使用这种商业模式的开源公司有，例如 RedHat、[^7] IBM、SUSE、Hortonworks（用于 Apache Hadoop）、Chef 和 Percona（用于开源数据库软件）。

### Branded merchandise / 品牌商品

Some open-source organizations such as the Mozilla Foundation[8] and the Wikimedia Foundation[9] sell branded merchandise articles like [t-shirts](https://en.wikipedia.org/wiki/T-shirt) and coffee mugs. This can be also seen as an additional service provided to the [user community](https://en.wikipedia.org/wiki/User_community).

一些开源组织，如 Mozilla 基金会 [^8] 和维基媒体基金会 [^9]，出售品牌商品文章，如 T 恤衫和咖啡杯。这也可以看作是提供给用户社区的额外服务。

### Software as a service / 软件即服务

Selling [subscriptions](https://en.wikipedia.org/wiki/Subscription_business_model) for online accounts and server access to customers is one way of adding value to open-source software. Another way is combining desktop software with a service, called [software plus services](https://en.wikipedia.org/wiki/Software_plus_services). Most open core companies that use this approach also provide the software in a fashion suitable for [on-premises](https://en.wikipedia.org/wiki/On-premises_software), do-it-yourself deployment. To some customers, however, there is significant value in a "plug and play" hosted product. Open source businesses that use this model often cater to small and medium enterprises who do not have the technology resources to run the software. Providing [cloud computing](https://en.wikipedia.org/wiki/Cloud_computing) services or [software as a service](https://en.wikipedia.org/wiki/Software_as_a_service) (SaaS) without the release of the open-source software is not an open source deployment.

向客户出售订阅制在线账户和服务器访问权限，是增加开源软件价值的一种方式。另一种方式是将桌面软件与服务相结合，称为软件加服务。大多数采用这种商业模式的开放核心公司，以适合内部部署、自己动手的方式提供软件。然而，对一些客户来说，“即插即用”的托管产品具有重要价值，应用这种模式的开源企业会迎合了那些没有技术资源来运行软件的中小型企业，只提供云计算服务或软件即服务（SaaS），而不发布开源软件，不进行开源部署。

The FSF called the server-side use-case without release of the source-code the "ASP loophole in the GPLv2" and encourage therefore the use of the Affero General Public License which plugged this hole in 2002.[^10][^11] In 2007 the FSF contemplated including the special provision of AGPLv1 into GPLv3 but ultimately decided to keep the licenses separate.[^12]

FSF 称，不释放源代码的服务器端使用情况为 “GPLv2 中的 ASP 漏洞”，因此鼓励使用 AGPL ，该许可证在 2002 年堵住了这个漏洞。[^10][^11] 2007 年，FSF 考虑将 AGPLv1 的特殊条款纳入 GPLv3，但最终决定将许可证分开。[^12]

### Voluntary donations / 自愿捐款

**Main article: [Donationware](https://en.wikipedia.org/wiki/Donationware) / 主条目：捐赠软件**

There were experiments by Independent developers to fund development of open-source software donation-driven directly by the users, e.g. with the [Illumination Software Creator](https://en.wikipedia.org/wiki/Illumination_Software_Creator) in 2012.[^13] Since 2011, [SourceForge](https://en.wikipedia.org/wiki/SourceForge) allows users to donate to hosted projects that opted to accept donations, which is enabled via [PayPal](https://en.wikipedia.org/wiki/PayPal).[^14]

独立开发者曾尝试过由用户直接捐赠驱动的开源软件的开发，例如 2012 年的 Illumination Software Creator。[^13] 自 2011 年起，SourceForge 允许用户捐赠给选择接受捐赠的托管项目，可以通过 PayPal 等支付手段完成。[^14]

Larger donation campaigns also exist. In 2004 the [Mozilla Foundation](https://en.wikipedia.org/wiki/Mozilla_Foundation) carried out a fundraising campaign to support the launch of the [Firefox](https://en.wikipedia.org/wiki/Firefox) 1.0 [web browser](https://en.wikipedia.org/wiki/Web_browser). It placed a two-page ad in the December 16 edition of [The New York Times](https://en.wikipedia.org/wiki/The_New_York_Times) listing the names of the thousands who had donated.[^15][^16]

大规模捐赠活动也是存在的。2004 年，Mozilla 基金会开展了一次众筹活动，以支持 Firefox 1.0 网络浏览器的推出，12 月 16 日的《纽约时报》上刊登了两页广告，列出了数千名捐款者的名字。[^15][^16]

In May 2019, [GitHub](https://en.wikipedia.org/wiki/GitHub), a Git-based software repository hosting, management and collaboration platform owned by Microsoft, launched a Sponsors program that allows people who support certain open source projects hosted on GitHub to donate money to developers who contribute and maintain the project.[^17]

2019 年 5 月，微软旗下的基于 Git 的软件库托管、管理和协作平台 GitHub 推出了一项赞助计划，允许支持 GitHub 上托管的某些开源项目的人，向贡献和维护项目的开发者直接捐赠资金。[^17]

### Crowdsourcing / 众包

[Crowdsourcing](https://en.wikipedia.org/wiki/Crowdsourcing) is a type of participative online activity in which an individual, an institution, a nonprofit organization, or company proposes to a group of individuals of varying knowledge, heterogeneity, and number, the voluntary undertaking of a task via a flexible open call. The undertaking of the task, of variable complexity and modularity, and in which the crowd should participate, bringing their work, money, knowledge and/or experience, always entails mutual benefit. The user will receive the satisfaction of a given type of need, be it economic, social recognition, self-esteem, or the development of individual skills, while the crowdsourcer will obtain and use to their advantage that which the user has brought to the venture, whose form will depend on the type of activity undertaken. Caveats in pursuing a Crowdsourcing strategy are to induce a substantial market model or incentive, and care has to be taken that the whole thing doesn't end up in an open source anarchy of adware and spyware plagiates, with a lot of broken solutions, started by people who just wanted to try it out, then gave up early, and a few winners. Popular examples for Crowdsourcing are [Linux](https://en.wikipedia.org/wiki/Linux), [Google Android](https://en.wikipedia.org/wiki/Google_android), the [Pirate Party](https://en.wikipedia.org/wiki/Pirate_Party) movement, and Wikipedia.

众包是一种参与模式的在线活动，在此类活动中，个人、机构、非营利组织或公司向一群具有不同知识、异质性和数量的个人提议，通过灵活的公开呼吁，自愿承担某项任务。任务的承担，具有各种程度的复杂性和模块化，大家参与其中，反之给参与者带来工作、金钱、知识和/或经验，这种模式蕴含着互利的思维。用户特定需求可以得到满足，无论是经济、社会认可、自尊，还是个人技能的发展，而众包商将获得并利用用户为风险投资带来的优势，其形式将取决于所进行的活动类型。追求众包战略的注意事项是，要主导一个实质性的市场模式或激励措施，并且要注意整个事情不会以广告软件和间谍软件的无政府状态而告终，有很多并不成功的解决方案，这些解决方案是由那些只是想尝试一下，然后提前放弃的人开始的，还有一些赢家。众包的流行例子是 Linux、谷歌安卓、海盗党运动和维基百科。

## Selling users / 销售用户

### Partnership with funding organizations / 与筹资组织的伙伴关系

Other financial situations include partnerships with other companies. [Governments](https://en.wikipedia.org/wiki/Governments), [universities](https://en.wikipedia.org/wiki/Universities), companies, and non-governmental organizations may develop internally or hire a contractor for custom in-house modifications, then release that code under an open-source license. Some organizations support the development of open-source software by [grants](https://en.wikipedia.org/wiki/Grant_(money)) or [stipends](https://en.wikipedia.org/wiki/Stipend), like [Google's](https://en.wikipedia.org/wiki/Google) [Summer of Code](https://en.wikipedia.org/wiki/Summer_of_Code) initiative founded in 2005.[^18]

财务状况包括与其他公司的伙伴关系。政府、大学、公司和非政府组织，可以在内部开发或雇用承包商进行内部转向定制和修改，然后在开源许可证下，发布这些代码。一些组织通过赠款或津贴来支持开源软件的开发，比如 2005 年成立的谷歌的 "代码之夏 "计划。[^18]

### Advertising-supported software / 广告支持的软件

In order to commercialize FOSS (free and open-source software), many companies (including [Google](https://en.wikipedia.org/wiki/Google), [Mozilla](https://en.wikipedia.org/wiki/Mozilla), and [Canonical](https://en.wikipedia.org/wiki/Canonical_Ltd)) have moved towards an [economic model](https://en.wikipedia.org/wiki/Economic_model) of [advertising-supported software](https://en.wikipedia.org/wiki/Advertising-supported_software). For instance, the open-source application [AdBlock Plus](https://en.wikipedia.org/wiki/AdBlock_Plus) gets paid by Google for letting [whitelisted](https://en.wikipedia.org/wiki/Whitelist) Acceptable Ads bypassing the browser ad remover.[^19] As another example is [SourceForge](https://en.wikipedia.org/wiki/SourceForge), an open-source project service provider, has the revenue model of advertising banner sales on their website. In 2006, SourceForge reported quarterly takings of $6.5 million[^20] and $23 million in 2009.[^21]

为了使 FOSS（自由和开源软件）商业化，许多公司（包括谷歌、Mozilla 和 Canonical）已经转向以广告支持软件的经济模式。例如，开源应用程序 AdBlock Plus 因让白名单上的可接受广告绕过浏览器广告去除器而获得谷歌的报酬。[^19] 另一个例子是开源项目服务提供商 SourceForge，它的官方网站上存在广告横幅销售的收入模式。2006 年，SourceForge 报告的季度收入为 650 万美元 [^20] ，2009 年为 2300 万美元。[^21]

## Pre-selling code / 预售代码

### Bounty driven development / 赏金驱动的开发

**Main article: [Open-source bounty](https://en.wikipedia.org/wiki/Open-source_bounty) / 主条目：开源赏金**

The users of a particular software artifact may come together and pool money into an [open-source bounty](https://en.wikipedia.org/wiki/Open-source_bounty) for the implementation of a desired feature or functionality. Offering [bounties](https://en.wikipedia.org/wiki/Bounty_(reward)) as funding has existed for some time. For instance, [Bountysource](https://en.wikipedia.org/wiki/Bountysource) is a web platform which has offered this funding model for open source software since 2003.

某个特定软件产品的用户会可以聚集在一起，为实现所需的特性或功能而集资，提供开源赏金。赏金提供的模式已经存在一段时间了。例如，网络平台 Bountysource，从 2003 年开始为开源软件提供这种模式。

Another bounty source is companies or foundations that set up bounty programs for implemented features or bugfixes in open-source software relevant to them. For instance, [Mozilla](https://en.wikipedia.org/wiki/Mozilla_Foundation) has been paying and funding freelance open-source programmers for [security bug](https://en.wikipedia.org/wiki/Security_bug) hunting and fixing since 2004.[^22][^23][^24]

另一个赏金来源，是公司或基金会为与他们相关的开源软件中，已实现的功能或错误修复设立赏金计划。例如，Mozilla 公司自 2004 年以来一直在支付和资助自由职业的开源程序员进行安全漏洞的寻找和修复。[^22][^23][^24]

### Pre-order/crowdfunding/reverse-bounty model / 预购/众筹/反向赏金模式

A newer funding opportunity for open-source software projects is [crowdfunding](https://en.wikipedia.org/wiki/Crowdfunding), which shares similarities with the [pre-order](https://en.wikipedia.org/wiki/Pre-order) or [Praenumeration](https://en.wikipedia.org/wiki/Praenumeration) business model, as well as the reverse bounty model, typically organized over web platforms like [Kickstarter](https://en.wikipedia.org/wiki/Kickstarter),[^25] [Indiegogo](https://en.wikipedia.org/wiki/Indiegogo),[^26] or [Bountysource](https://en.wikipedia.org/wiki/Bountysource)[^27] (see also [comparison of crowd funding services](https://en.wikipedia.org/wiki/Comparison_of_crowd_funding_services)). One example is the successfully funded Indiegogo campaign in 2013 by Australian programmer Timothy Arceri, who offered to implement an [OpenGL](https://en.wikipedia.org/wiki/OpenGL) 4.3 extension for the [Mesa](https://en.wikipedia.org/wiki/Mesa_(computer_graphics)) library in two weeks for $2,500.[^26] Arceri delivered the OpenGL extension code which was promptly merged upstream, and he later continued his efforts on Mesa with successive crowdfunding campaigns.[^28] Later, he found work as an employee in this domain with [Collabora](https://en.wikipedia.org/wiki/Collabora) and in 2017 with [Valve](https://en.wikipedia.org/wiki/Valve_Corporation).[^29] Another example is the June 2013 [crowdfunding](https://en.wikipedia.org/wiki/Crowdfunding) on [Kickstarter](https://en.wikipedia.org/wiki/Kickstarter)[^30][^31] of the [open source video game](https://en.wikipedia.org/wiki/Open_source_video_game) [Cataclysm: Dark Days Ahead](https://en.wikipedia.org/wiki/Cataclysm:_Dark_Days_Ahead) which raised the payment of a full-time developer for 3.5 months. [Patreon](https://en.wikipedia.org/wiki/Patreon) funding has also become an effective option, as the service gives the option to pay out each month to creators, many of whom intend to develop free and open-source software.[^32]

开源软件项目另一个模式是众筹，与预购或预定商业模式以及反向赏金模式有相似之处，通常会在 Kickstarter、[^25] Indiegogo、[^26] 或 Bountysource[^27] 等网络平台上进行（另见众筹服务的比较）。其中一个例子是澳大利亚程序员 Timothy Arceri 在 2013 年成功资助了 Indiegogo 活动，他提出，要在两周内为 Mesa 库实现 OpenGL 4.3 扩展，价格为 2500 美元。[^26] Arceri 交付的 OpenGL 扩展代码很快被合并到上游，接着他通过连续的众筹活动继续他在 Mesa 的工作。 [^28] 后来，他在 Collabora 找到了这个领域的工作，2017 年又在 Valve 找到了工作。[^29] 另一个例子是 2013 年 6 月在 Kickstarter[^30][^31] 上众筹的开源视频游戏 Cataclysm。Dark Days Ahead，筹集了一个全职开发者 3.5 个月的报酬。在 Patreon 平台上众筹也成为一种行之有效的选择，Patreon 可以让用户选择每月向开源创作者支付款项。[^32]

## Selling intellectual property / 出售知识产权

### Dual-licensing or Open Core / 双重许可或开放核心

**Main articles: [Open-core model](https://en.wikipedia.org/wiki/Open-core_model) and [Multi-licensing](https://en.wikipedia.org/wiki/Multi-licensing) / 主条目：开放核心模式和多重许可**

In a [dual licensing](https://en.wikipedia.org/wiki/Multi-licensing) model, the vendor develops software and offers it under an [open-source license](https://en.wikipedia.org/wiki/Open-source_license) but also under separate proprietary license terms. The proprietary version can be licensed to finance the continued development of the free open-source version.[^33] Customers may prefer a no-cost and open-source edition for testing, evaluation, proof of concept development, and small scale deployment. If the customer wishes to deploy the software at scale, or in proprietary distributed products, the customer then negotiates for a commercial license to an enterprise edition. Further, customers will learn of open-source software in a company's portfolio and offerings but generate business in other proprietary products and solutions, including commercial [technical support](https://en.wikipedia.org/wiki/Technical_support) contracts and services. A popular example is [Oracle](https://en.wikipedia.org/wiki/Oracle_Corporation)'s [MySQL](https://en.wikipedia.org/wiki/MySQL) [database](https://en.wikipedia.org/wiki/Database) which is dual-licensed under a commercial proprietary license and also under the [GPLv2](https://en.wikipedia.org/wiki/GPLv2).[^34] Another example is the [Sleepycat License](https://en.wikipedia.org/wiki/Sleepycat_License). [Flask](https://en.wikipedia.org/wiki/Flask_(web_framework)) developer Armin Ronacher stated that the [AGPLv3](https://en.wikipedia.org/wiki/Affero_General_Public_License) was a "terrible success" as "vehicle for dual commercial licensing" and noted that [MongoDB](https://en.wikipedia.org/wiki/MongoDB), [RethinkDB](https://en.wikipedia.org/wiki/RethinkDB), [OpenERP](https://en.wikipedia.org/wiki/OpenERP), [SugarCRM](https://en.wikipedia.org/wiki/SugarCRM) as well as [WURFL](https://en.wikipedia.org/wiki/WURFL) utilizing the license for this purpose.[^35]

在双重许可模式中，供应商开发的软件在开源许可下提供，但也在单独的专有许可条款下提供。专有版本可以通过授权，来资助免费开源版本的持续开发。[^33] 客户可能更喜欢无成本的开源版本，用于测试、评估、概念验证开发和小规模部署。如果客户希望大规模部署该开源软件，或在专有的分布式产品中部署，客户就会协商获得企业版的商业许可。此外，客户会在公司的产品组合和产品中了解到开源软件，但在其他专有产品和解决方案中运行业务，包括商业技术支持合同和服务。一个流行的例子是甲骨文的 MySQL 数据库，它在商业专有许可证和 GPLv2[^34] 下有双重许可证。Flask 的开发者 Armin Ronacher 说，AGPLv3 作为“双重商业许可的工具”是一个“巨大的成功”，并指出 MongoDB、RethinkDB、OpenERP、SugarCRM 以及 WURFL 都在为此目的而利用该许可。[^35]

Dual license products are generally sold as a "community version" and an "enterprise version." In a pure dual licensing model, as was common before 2010, these versions are identical but available under a choice of licensing terms. Added proprietary software may help customers analyze data, or more efficiently deploy the software on their infrastructure or platform. Examples include the IBM proprietary Linux software, where IBM contributes to the Linux open-source ecosystem, but it builds and delivers (to IBM's paying customers) [database software](https://en.wikipedia.org/wiki/Database_software), [middleware](https://en.wikipedia.org/wiki/Middleware), and other software that runs on top of the open-source core. Other examples of proprietary products built on open-source software include [Red Hat Enterprise Linux](https://en.wikipedia.org/wiki/Red_Hat_Enterprise_Linux) and [Cloudera](https://en.wikipedia.org/wiki/Cloudera)'s [Apache Hadoop](https://en.wikipedia.org/wiki/Apache_Hadoop)-based software.

双许可证产品通常以“社区版”和“企业版”的形式出售。在一个纯粹的双授权模式中，就像 2010 年之前常见的那样，这些版本是相同的，但可以选择授权条款。增加的专有软件可以帮助客户分析数据，或更有效地在其基础设施或平台上部署软件。例子包括 IBM 专有的 Linux 软件，IBM 为 Linux 开源生态系统做出了贡献，但它建立并提供（给 IBM 的付费客户）数据库软件、中间件和其他在开源核心之上运行的软件。其他建立在开源软件上的专有产品的例子包括红帽企业 Linux 和 Cloudera 的基于 Apache Hadoop 的软件。

### Selling certificates and use of trademark / 销售证书和商标的使用

**Main article: [Franchising](https://en.wikipedia.org/wiki/Franchising) / 主条目：特许经营**

Another financing approach is innovated by [Moodle](https://en.wikipedia.org/wiki/Moodle), an open source [learning management system](https://en.wikipedia.org/wiki/Learning_management_system) and community platform.[^36][^37] The business model revolves around a network of commercial partners[^38] who are certified and therefore authorised to use the Moodle [name](https://en.wikipedia.org/wiki/Trademark) and [logo](https://en.wikipedia.org/wiki/Logo),[^39] and in turn provide a proportion of revenue to the Moodle Trust, which funds core development.[^40]

另一种融资方式是由开源学习管理系统和社区平台 Moodle 进行的创新。[^36][^37] 它的商业模式围绕着一个商业伙伴网络 [^38]，可以通过认证，继而被授权使用 Moodle 的名称和标志，[^39] 反过来又向 Moodle 信托基金提供一部分收入，为核心开发工作提供资金。[^40]

### Re-licensing under a proprietary license / 在专利许可下重新许可

If a software product uses only own software and open-source software under a [permissive free software licence](https://en.wikipedia.org/wiki/Permissive_free_software_licence), a company can re-license the resulting software product under a proprietary license and sell the product without the source code or [software freedoms](https://en.wikipedia.org/wiki/The_Free_Software_Definition).[^41] For instance, [Apple Inc](https://en.wikipedia.org/wiki/Apple_Inc.). is an avid user of this approach by using source code and software from open-source projects. For example, the [BSD Unix](https://en.wikipedia.org/wiki/Berkeley_Software_Distribution) operating system kernel (under the [BSD license](https://en.wikipedia.org/wiki/BSD_license)) was used in [Apple](https://en.wikipedia.org/wiki/Apple_Inc.)'s [Mac](https://en.wikipedia.org/wiki/Macintosh) PCs that were sold as proprietary products.[^42]

如果某个软件产品只使用自己的软件和自由软件许可下的开源软件，公司可以在专有许可下重新许可所产生的软件产品，并在没有源代码或软件自由的情况下销售该产品。[^41] 例如，苹果公司是这种方法的狂热使用者，它使用开源项目的源代码和软件。例如，BSD Unix 操作系统的内核（在 BSD 许可下）被用于苹果公司的 Mac 电脑中，而这些电脑是作为专利产品出售的。[^42]

## Selling proprietary additives / 销售专有附件

### Selling optional proprietary extensions / 销售可选的专有扩展

**Main article: Open-core model / 主词条：开放核心模式**

Some companies sell proprietary but optional extensions, modules, [plugins](https://en.wikipedia.org/wiki/Plug-in_(computing)) or [add-ons](https://en.wikipedia.org/wiki/Browser_extension) to an open-source software product. This approach is a variant of the [freemium](https://en.wikipedia.org/wiki/Freemium) business model. The proprietary software may be intended to let customers get more value out of their data, infrastructure, or platform, e.g., operate their infrastructure/platform more effectively and efficiently, manage it better, or secure it better. Examples include the [IBM proprietary Linux software](https://en.wikipedia.org/wiki/Linux_Technology_Center), where IBM contributes to the Linux open-source ecosystem, but it builds and delivers (to IBM's paying customers) [database software](https://en.wikipedia.org/wiki/Database_software), [middleware](https://en.wikipedia.org/wiki/Middleware), and other software that runs on top of the open-source core. Other examples of proprietary products built on open-source software include [Red Hat Enterprise Linux](https://en.wikipedia.org/wiki/Red_Hat_Enterprise_Linux) and [Cloudera](https://en.wikipedia.org/wiki/Cloudera)'s [Apache Hadoop](https://en.wikipedia.org/wiki/Apache_Hadoop)-based software. Some companies appear to re-invest a portion of their financial profits from the sale of proprietary software back into the open source infrastructure.[^43]

一些公司在开源软件产品上销售专有但可选择的扩展、模块、插件或附加组件。这种方法是免费商业模式的一个变体。专有软件是为了让客户从数据、基础设施或平台中获得更多的价值，例如，更有效地操作其基础设施/平台，更好地管理它，或更好地保护它。例子包括 IBM 专有的 Linux 软件，IBM 为 Linux 开源生态系统做出了贡献，但它建立并提供（给 IBM 的付费客户）数据库软件、中间件和其他在开源核心之上运行的软件。其他建立在开源软件上的专有产品的例子包括红帽企业 Linux 和 Cloudera 公司基于 Apache Hadoop 的软件。一些公司似乎将其出售专有软件的部分经济利润重新投入到开源基础设施中。[^43]

The approach can be problematic with many open source licenses ("not license conform") if not carried out with sufficient care. For instance, mixing proprietary code and open-source licensed code in [statically linked libraries](https://en.wikipedia.org/wiki/Statically_linked_library)[^44] or compiling all source code together in a software product might violate open-source licenses, while keeping them separated by interfaces and [dynamic-link libraries](https://en.wikipedia.org/wiki/Dynamic-link_library) would adhere to license conform.

不过如果不够谨慎，这种方法可能会对许多开源许可证产生问题（“不符合许可证”）。例如，在静态链接库 [^44] 中混合专有代码和开源许可代码，或者在软件产品中一起编译所有的源代码，可能会违反开源许可，而通过接口和动态链接库将它们分开，则符合许可的要求。

### Selling required proprietary parts of a software product / 销售软件产品所需的专有部分

A variant of the approach above is the keeping of required data content (for instance a video game's audio, graphic, and other art assets) of a software product proprietary while making the software's source code open-source. While this approach is completely legitimate and compatible with most open-source licenses, customers have to buy the content to have a complete and working software product.[^45] Restrictive licenses can then be applied on the content, which prevents the redistribution or re-selling of the complete software product. Examples for open-source developed software are Kot-in-Action Creative Artel video game Steel Storm, engine GPLv2 licensed while the artwork is CC-BY-NC-SA 3.0 licensed,[^46] and Frogatto & Friends with an own developed open-source engine[^47] and commercialization via the copyrighted game assets[^48] for iPhone, BlackBerry and MacOS.[^49]

上述方法的一个变种是将软件产品所需的数据内容（例如视频游戏的音频、图形和其他艺术资产）保留为专利，同时将软件的源代码开放。虽然这种方法是完全合法的，并与大多数开源许可证兼容，但客户必须购买这些内容才能拥有一个完整的、可运行的软件产品。[^45] 然后可以在内容上应用限制性许可证，防止重新分配或重新销售完整的软件产品。开源软件的例子有 Kot-in-Action Creative Artel 视频游戏《钢铁风暴》，引擎是 GPLv2 许可的，而作品是 CC-BY-NC-SA 3.0 [^46] 许可的，还有 Frogatto & Friends，有自己开发的开源引擎 [^47]，通过 iPhone、黑莓和 MacOS 的版权游戏资产 [^48] 进行商业化。[^49]

Other examples are Arx Fatalis (by Arkane Studios)[^50] and Catacomb 3-D (by Flat Rock Software)[^51] with source code opened to the public delayed after release, while copyrighted assets and binaries are still sold on gog.com as digital distribution.[^52]

其他的例子有 Arx Fatalis（Arkane Studios）[^50] 和 Catacomb 3-D（Flat Rock Software）[^51]，源代码在发布后延迟向公众开放，而有版权的资产和二进制文件仍在 gog.com 上作为数字发行出售。[^52]

Doing so conforms with the FSF and Richard Stallman, who stated that for art or entertainment the software freedoms are not required or important.[^53]

这样做符合 FSF 和 Richard Stallman 的观点，他表示，对于艺术或娱乐来说，软件自由不是必须的，也没有那么重要。[^53]

The similar product bundling of an open-source software product with hardware which prevents users from running modified versions of the software is called tivoization and is legal with most open-source licenses except GPLv3, which explicitly prohibits this use-case.[^54]

将开源软件产品与硬件捆绑在一起，防止用户运行软件的修改版本，这种类似的产品被称为 tivoization，除了 GPLv3 明确禁止这种使用情况外，大多数开源许可证都是合法的。[^54]

### Selling proprietary update systems / 销售专有更新系统

Another variant of the approach above, mainly use for data-intensive, data-centric software programs, is the keeping of all versions of the software under a free and open-source software license, but refraining from providing [update](https://en.wikipedia.org/wiki/Software_update) scripts from a n to an n+1 version. Users can still deploy and run the open source software. However, any update to the next version requires either exporting the data, reinstalling the new version, then reimporting the data to the new version, or subscribing to the proprietary update system, or studying the two versions and recreating the scripts from scratch.

上述方法的另一个变种，主要用于数据密集型、以数据为中心的软件程序，是将软件的所有版本保持在自由和开源软件许可之下，但不提供从 n 到 n+1 版本的更新脚本。用户仍然可以部署和运行该开源软件。然而，任何更新到下一个版本的工作都需要导出数据，重新安装新的版本，然后重新导入数据到新的版本，或者订阅专有的更新系统，或者研究两个版本并从头开始重新创建脚本。

This practice does not conform with the [free software principles](https://en.wikipedia.org/wiki/Software_Freedom) as espoused by the FSF. Richard Stallman condemns this practice and names it "diachronically trapped software".[^55]

这种做法不符合 FSF 所倡导的自由软件原则。Richard Stallman 谴责这种做法，并将其命名为 "不合时宜的陷阱软件"。

### Selling without proprietary license / 在没有所有权许可的情况下进行销售

All of the above methods follows from the traditional approach in the selling software, where Software is licensed for installation and execution on a user- or customer-supplied infrastructure. In the classic software product business, revenues typically originate from selling software upgrades to the customer. Hovewer, it's also practicing selling exactly the same programs or add-ons but without proprietary licensing. For example, applications like ardour,[^56] radium[^57] or fritzing[^58] it's completely free software on GPL license but there is a fee to get the official binary, often bundled with tech support or the privileges of attracting developers' attention to adding new functionalities to the program.

上述所有方法都来自于销售软件的传统方法，即软件被授权在用户或客户提供的基础设施上安装和执行。在传统的软件产品业务中，收入通常来自于向客户销售软件升级。但是，它也在实践中销售完全相同的程序或附加组件，但没有专有许可。例如，像 ardour[^56]、radium[^57] 或 fritzing[^58] 这样的应用程序是完全基于 GPL 许可的免费软件，但要获得官方二进制文件则需要付费，通常会捆绑技术支持或吸引开发者注意为程序添加新功能的特权。

This practice does conform with the free software principles as espoused by the FSF.[^59]

这种做法确实符合 FSF 所倡导的自由软件原则。[^59]

## Other / 其他

### Obfuscation of source code / 源代码的模糊化

An approach to allow commercialization under some open-source licenses while still protecting crucial business secrets, intellectual property and technical know-how is obfuscation of source code. This approach was used in several cases, for instance by Nvidia in their open-source graphic card device drivers.[^60] This practice is used to get the open-source-friendly propaganda without bearing the inconveniences. There has been debate in the free-software/open-source community on whether it is illegal to skirt copyleft software licenses by releasing source code in obfuscated form, such as in cases in which the author is less willing to make the source code available. The general consensus was that while unethical, it was not considered a violation.

有一种方法是混淆源代码，这是在某些开源许可证下，可以允许商业化，同时也能保护关键的商业秘密、知识产权和技术的诀窍。这种方法在某些情况下会被应用，例如 Nvidia 在他们的开源图形卡设备驱动程序中使用。[^60] 这种做法被用来获得有利于开源的宣传，而不需要承担麻烦。自由软件/开源社区一直在争论，通过发布混淆形式的源代码来规避版权软件许可是否违法，例如在作者不太愿意提供源代码的情况下。普遍的共识是，虽然不道德，但不会被认为是违规。

The Free Software Foundation is against this practice.[^61] The GNU General Public License since version 2 has defined "source code" as "the preferred form of the work for making modifications to it." This is intended to prevent the release of obfuscated source code.[^62]

自由软件基金会反对这种做法。[^61] GPL 自第二版起将 "源代码 "定义为 "对其进行修改的作品的首选形式"。这是为了防止发布混淆的源代码。[^62]

### Delayed open-sourcing / 延迟开放源代码

Some companies provide the latest version available only to paying customers. A vendor [forks](https://en.wikipedia.org/wiki/Fork_(software_development)) a non-[copyleft](https://en.wikipedia.org/wiki/Copyleft) software project then adds closed-source additions to it and sells the resulting software. After a fixed time period the [patches](https://en.wikipedia.org/wiki/Patch_(computing)) are released back [upstream](https://en.wikipedia.org/wiki/Upstream_(software_development)) under the same license as the rest of the codebase. This business model is called version lagging or time delaying.[^43][^63]

有些公司只向付费客户提供最新版本。一个供应商将一个非盗版的软件项目分叉，然后在其中加入闭源的补充内容，并出售由此产生的软件。在一个固定的时间段后，这些补丁在与代码库的其他部分相同的许可下被释放回上游。这种商业模式被称为版本滞后或时间延迟。[^43][^63]

For instance, 2016 the [MariaDB Corporation](https://en.wikipedia.org/wiki/MariaDB_Corporation) created for business compatible "delayed open-sourcing" the [source-available](https://en.wikipedia.org/wiki/Source-available) Business source license (BSL) which automatically [relicenses](https://en.wikipedia.org/wiki/Relicensing) after three years to the [FOSS](https://en.wikipedia.org/wiki/Free_and_open-source_software) GPL.[^64][^65] This approach guarantees licensees that they have source code access (e.g. for [code audits](https://en.wikipedia.org/wiki/Code_audit)), are not locked into a [closed platform](https://en.wikipedia.org/wiki/Closed_platform), or suffer from [planned obsolescence](https://en.wikipedia.org/wiki/Planned_obsolescence), while for the software developer a time-limited exclusive commercialization is possible.[^64] In 2017 followed version 1.1, revised with feedback also from [Bruce Perens](https://en.wikipedia.org/wiki/Bruce_Perens).[^66][^67]

例如，2016 年 MariaDB 公司为商业兼容的“延迟开源”创建了可获得源代码的商业源代码许可证（BSL），该许可证在三年后自动重新授权给 FOSS GPL。[^64][^65] 这种方法保证了被许可人对源代码的访问权（例如用于代码审计），且不会被锁定在一个封闭的平台上，也不会受到计划的被淘汰而造成的影响，而对软件开发者来说，可以进行有时限的独家商业化。[^64] 2017 年的 1.1 版，在布鲁斯-佩伦斯的反馈下进行了修订。[^66][^67]

However, this approach works only with own software or [permissive licensed](https://en.wikipedia.org/wiki/Permissive_free_software_licence) code parts, as there is no copyleft FOSS license available which allows the time delayed opening of the source code after distributing or selling of a software product.

然而，这种方法只适用于自己的软件或许可的代码部分，因为没有允许在分发或销售软件产品后延迟开放源代码的版权自由软件许可。

### Open sourcing on end-of-life / 生命周期结束时开源

**See also: [List of commercial software with available source code](https://en.wikipedia.org/wiki/List_of_commercial_software_with_available_source_code) and [List of commercial video games with available source code](https://en.wikipedia.org/wiki/List_of_commercial_video_games_with_available_source_code)**
**参见：具有可用源代码的商业软件列表和具有可用源代码的商业视频游戏列表**

An extreme variant of "delayed open-sourcing" is a business practice popularized by [id Software](https://en.wikipedia.org/wiki/Id_Software)[^68][^69] and [3D Realms](https://en.wikipedia.org/wiki/3D_Realms),[^70][^71] which released several software products under a [free software license](https://en.wikipedia.org/wiki/Free_software_license) after a long proprietary commercialization time period and the [return of investment](https://en.wikipedia.org/wiki/Return_of_investment) was achieved. The motivation of companies following this practice of releasing the source code when a software reaches the commercial [end-of-life](https://en.wikipedia.org/wiki/End-of-life_(product)), is to prevent that their software becomes unsupported [Abandonware](https://en.wikipedia.org/wiki/Abandonware) or even get lost due to [digital obsolescence](https://en.wikipedia.org/wiki/Digital_obsolescence).[^72] This gives the [user communities](https://en.wikipedia.org/wiki/User_community) the chance to continue development and support of the software product themselves as an open-source software project.[^73] Many examples from the [video game](https://en.wikipedia.org/wiki/Video_game) domain are in the [list of commercial video games with later released source code](https://en.wikipedia.org/wiki/List_of_commercial_video_games_with_later_released_source_code).

“延迟开放源代码”的极端变体之一，是由 id Software[^68][^69] 和 3D Realms[^70][^71] 推广的一种商业模式，这种模式在实现漫长的专有商业化周期和投资回报后，以自由软件许可证的形式发布了几个软件产品。遵循这种做法的公司，在软件的商业寿命终结时，发布源代码的动机主要是为了防止软件成为不受支持的废弃软件，甚至因数字过时而丢失。[^72] 这就使得用户群体，可以有机会作为一个开源软件项目继续开发和支持软件产品。[^73] 很多商业视频游戏领域存在许多例子，都是在生命周期结束后发布源代码。

Popular non-game software examples are the [Netscape Communicator](https://en.wikipedia.org/wiki/Netscape_Communicator) which was open-sourced in 1998[^74][^75] and [Sun Microsystems](https://en.wikipedia.org/wiki/Sun_Microsystems)'s [office suite](https://en.wikipedia.org/wiki/Office_suite), [StarOffice](https://en.wikipedia.org/wiki/StarOffice), which was released in October 2000 at its commercial end of life.[76] Both releases made foundational contributions to now prominent open-source projects, namely [Mozilla Firefox](https://en.wikipedia.org/wiki/Mozilla_Firefox) and [OpenOffice.org](https://en.wikipedia.org/wiki/OpenOffice.org)/[LibreOffice](https://en.wikipedia.org/wiki/LibreOffice).

常见的一个非游戏软件的例子是 1998 年开源的 Netscape Communicator[^74][^75] 和 Sun Microsystems 的办公套件 StarOffice，StarOffice 于 2000 年 10 月在其商业寿命结束时发布源代码。[^76] 这两个版本都为现在著名的开源项目做出了基础性贡献，即 Mozilla Firefox 和 OpenOffice.org/LibreOffice。

## Funding / 资助

Unlike proprietary off-the-shelf software that come with restrictive licenses, open-source software is distributed freely, through the web and in physical media. Because creators cannot require each user to pay a license fee to fund development this way, a number of alternative development funding models have emerged.

与带有限制性许可证的现成专利软件不同，开源软件是通过网络和媒体免费发布的。因为构建者无法要求每个用户支付许可费来资助这种开发方式，所以出现了一些可替代的开发资助模式。

An example of those funding models is when bespoke software is developed as a consulting project for one or more customers who request it. These customers pay developers to have this software developed according to their own needs and they could also closely direct the developers' work. If both parties agree, the resulting software could then be publicly released with an open-source license in order to allow subsequent adoption by other parties. That agreement could reduce the costs paid by the clients while the original developers (or independent consultants) can then charge for training, installation, [technical support](https://en.wikipedia.org/wiki/Technical_support), or further customization if and when more interested customers would choose to use it after the initial release.

这类资助模式的一个例子：定制软件是作为一个咨询项目，为特有需求的特定客户群体开发的。这些客户付钱给开发者，根据自己的需要开发这个软件，客户也可以密切指导开发者的工作。如果双方都同意，所开发的软件就可以用开放源码许可证公开发布，以允许其他各方随后采用。该协议可以减少客户支付的费用，而原始开发者（或独立顾问）可以收取培训、安装、技术支持或进一步定制的费用，如果有更多感兴趣的客户在最初发布后选择使用它的话。

There also exist [stipends](https://en.wikipedia.org/wiki/Stipend) to support the development of open source software, such as [Google](https://en.wikipedia.org/wiki/Google)'s [Summer of Code](https://en.wikipedia.org/wiki/Summer_of_Code)[^18] and [Outreachy](https://en.wikipedia.org/wiki/Outreachy).[^77]

也有支持开发开源软件的津贴，如谷歌的 "代码之夏（Summer of Code）"[^18] 和 Outreachy。[^77]

Another approach to funding is to provide the software freely, but sell licenses to proprietary add-ons such as data libraries. For instance, an open-source [CAD](https://en.wikipedia.org/wiki/Computer-aided_design) program may require parts libraries which are sold on a subscription or flat-fee basis. Open-source software can also promote the sale of specialized hardware that it interoperates with, some example cases being the [Asterisk](https://en.wikipedia.org/wiki/Asterisk_(PBX)) telephony software developed by PC-telephony hardware manufacturer [Digium](https://en.wikipedia.org/wiki/Digium) and the [Robot Operating System](https://en.wikipedia.org/wiki/Robot_Operating_System) (ROS) robotics platform by Willow Garage and Stanford AI Labs. Many open source software projects have begun as research projects within universities, as personal projects of students or professors, or as tools to aid scientific research. The influence of universities and research institutions on open-source shows in the number of projects named after their host institutions, such as [BSD Unix](https://en.wikipedia.org/wiki/BSD_Unix), [CMU Common Lisp](https://en.wikipedia.org/wiki/CMU_Common_Lisp), or the [NCSA HTTPd](https://en.wikipedia.org/wiki/NCSA_HTTPd) which evolved into [Apache](https://en.wikipedia.org/wiki/Apache_Web_server).

另一种筹资方式是免费提供软件，但是可以出售数据库等专有附加组件的许可证。例如，一个开放源码的 CAD 程序可能需要零件库，这些零件库是以订阅或统一收费的方式出售。开源软件也可以促进与之互操作的专门硬件的销售，一些例子是由 PC 电话硬件制造商 Digium 开发的 Asterisk 电话软件和 Willow Garage 和 Stanford AI Labs 开发的机器人操作系统（ROS）机器人平台。许多开源软件项目都是作为大学内部的研究项目（学生或教授的个人项目）、或作为帮助科学研究的工具而开始。大学和研究机构对开源的影响体现在以其所在机构命名的项目数量上，如 BSD Unix、CMU Common Lisp 或演变为 Apache 的 NCSA HTTPd。

Companies may employ developers to work on open-source projects that are useful to the company's infrastructure: in this case, it is developed not as a product to be sold but as a sort of shared public utility. A local bug-fix or solution to a software problem, written by a developer either at a company's request or to make his/her own job easier, can be released as an open-source contribution without costing the company anything.[^78] A larger project such as the Linux kernel may have contributors from dozens of companies which use and depend upon it, as well as hobbyist and research developers.

公司可以雇用工程师从事对公司础设施有用的开源项目：在这种情况下，它不是作为一种产品来销售，而是作为一种共享的公共设施来开发。开发者根据公司的要求，或为了简化自己的工作，而去编写的局部错误修复或软件问题的解决方案，可以作为开放源码的贡献而发布，而不会给公司带来任何损失。[^78] 像 Linux 内核这样的大型项目可能有来自几十家使用和依赖它的公司的贡献者，以及业余爱好者和研究开发人员。

A new funding approach for open-source projects is [crowdfunding](https://en.wikipedia.org/wiki/Crowdfunding), organized over web platforms like [Kickstarter](https://en.wikipedia.org/wiki/Kickstarter), [Indiegogo](https://en.wikipedia.org/wiki/Indiegogo), or [Bountysource](https://en.wikipedia.org/wiki/Bountysource).[27]

开源项目的一种新的筹资方式是众筹，通过 Kickstarter、Indiegogo 或 Bountysource 等网络平台组织。[^27]

## Challenges / 挑战

[Open-source software](https://en.wikipedia.org/wiki/Open-source_software) can be sold and used in general [commercially](https://en.wikipedia.org/wiki/Commerce). Also, commercial open-source applications have been a part of the [software industry](https://en.wikipedia.org/wiki/Software_industry) for some time.[^79][^80] While commercialization or funding of open-source software projects is possible, it is considered challenging.[81]

开源软件可以在一般情况下进行商业化销售和使用。另外，商业化的开源应用，已经成为软件行业的一部分。[^79][^80] 虽然开源软件项目的商业化或融资是可行的，但还是具有一定的挑战性。[^81]

Since several [open-source licenses](https://en.wikipedia.org/wiki/Open-source_license) stipulate that authors of derivative works must distribute them under an open-source ([copyleft](https://en.wikipedia.org/wiki/Copyleft)) license, ISVs and VARs have to develop new legal and technical mechanisms to foster their commercial goals,[^3] as many traditional mechanisms are not directly applicable anymore.

一些开源许可证规定，衍生作品的作者必须在开源（copyleft）许可证下发布这些作品，ISV 和 VAR 必须开发新的法律和技术机制来促进其商业目标，[^3] 而许多传统机制不再直接适用。

Traditional business wisdom suggests that a company's methods, assets, and intellectual properties should remain concealed from market competitors ([trade secret](https://en.wikipedia.org/wiki/Trade_secret)) as long as possible to maximize the profitable commercialization time of a new product.[^82] Open-source software development minimizes the effectiveness of this tactic; development of the product is usually performed in view of the public, allowing competing projects or clones to incorporate new features or improvements as soon as the public code repository is updated, as permitted by most open-source licenses. Also in the computer hardware domain, a hardware producer who provides free and open software drivers reveals the knowledge about hardware implementation details to competitors, who might use this knowledge to catch up.

从传统的商业角度来看，一个公司的方法、资产和知识产权，应尽可能地对市场上的竞争者保持隐蔽（因为是商业秘密），从而最大限度地延长新产品的商业化盈利时间。[^82] 开源软件的开发，将这种策略的有效性降到最低；也就是说，产品的开发通常是在公众面前进行的，允许竞争项目或克隆人在公共代码库更新时立即加入新的功能或改进，这是大多数开源许可证所允许的。同样在计算机硬件领域，一个提供免费开放软件驱动程序的硬件生产商将有关硬件实施细节的知识透露给竞争对手，后者可能利用这些知识进行赶超。

Therefore, there is considerable debate about whether vendors can make a sustainable business from an open-source strategy. In terms of a traditional software company, this is probably the wrong question to ask. Looking at the landscape of open source applications, many of the larger ones are sponsored (and largely written) by system companies such as IBM who may not have an objective of software license revenues. Other software companies, such as Oracle and Google, have sponsored or delivered significant open-source code bases. These firms' motivation tends to be more strategic, in the sense that they are trying to change the rules of a marketplace and reduce the influence of vendors such as Microsoft. Smaller vendors doing open-source work may be less concerned with immediate revenue growth than developing a large and loyal community, which may be the basis of a corporate valuation at merger time.

因此，对于供应商是否能从开源战略中获得可持续的业务，存在相对比较大的争论。就传统软件公司而言，这可能是一个错误的问题。纵观开放源码应用程序的格局，许多较大的应用程序是由系统公司（如 IBM）赞助的（主要编写方），这些公司可能没有软件许可收入的目标。其他软件公司，如甲骨文和谷歌，已经赞助或提供了重要的开源代码库。这些公司的动机往往更具战略性，因为他们试图改变市场的规则，减少微软等厂商的影响。从事开放源码工作的小型供应商可能不太关心眼前的收入增长，而关心发展一个庞大而忠诚的社区，这可能是合并时企业估值的基础。

## FOSS and economy / 自由软件和经济

**Main article: [Open-source economics](https://en.wikipedia.org/wiki/Open-source_economics) / 主词条：开源经济学**

According to [Yochai Benkler](https://en.wikipedia.org/wiki/Yochai_Benkler), the Berkman Professor for Entrepreneurial Legal Studies at [Harvard Law School](https://en.wikipedia.org/wiki/Harvard_Law_School), free software is the most visible part of a new economy of [commons-based peer production](https://en.wikipedia.org/wiki/Commons-based_peer_production) of information, knowledge, and culture. As examples, he cites a variety of FOSS projects, including both free software and open source.[^83]

根据哈佛大学法学院伯克曼创业法律研究教授 Yochai Benkler 的说法，自由软件是基于公地的信息、知识和文化同行生产的新经济中最明显的部分，他列举了各种包括自由软件和开放源代码的自由软件项目。[^83]

This new economy is already under development. In order to commercialize FOSS, many companies, [Google](https://en.wikipedia.org/wiki/Google) being the most successful, are moving towards an [economic model](https://en.wikipedia.org/wiki/Economic_model) of [advertising-supported software](https://en.wikipedia.org/wiki/Advertising-supported_software). In such a model, the only way to increase revenue is to make the advertising more valuable. [Facebook](https://en.wikipedia.org/wiki/Facebook) has recently come under fire for using novel user tracking methods to accomplish this.[^84]

这种新经济已经在发展之中。为了使自由软件商业化，许多公司（谷歌是最成功的）正在向广告支持的软件经济模式发展。在这种模式下，增加收入的唯一途径是使广告更有价值。Facebook 最近因使用新的用户跟踪方法来实现这一目标而受到批评。[^84]

This new economy is not without alternatives. Apple's [App Stores](https://en.wikipedia.org/wiki/App_Store_(iOS)) have proven very popular with both users and developers. The Free Software Foundation considers Apple's App Stores to be [incompatible](https://en.wikipedia.org/wiki/License_compatibility) with its GPL and complained that Apple was infringing on the GPL with its [iTunes](https://en.wikipedia.org/wiki/ITunes) terms of use.[^85] Rather than change those terms to comply with the GPL, Apple removed the GPL-licensed products from its App Stores.[^86] The authors of VLC, one of the GPL-licensed programs at the center of those complaints, recently began the process to switch from the GPL to the [LGPL](https://en.wikipedia.org/wiki/LGPL) and [MPL](https://en.wikipedia.org/wiki/Mozilla_Public_License).[^87][^88]

这种新经济并非没有替代方案。事实证明，苹果的应用程序商店在用户和开发者中都非常受欢迎。自由软件基金会认为苹果的应用程序商店与它的 GPL 不兼容，认为苹果的 iTunes 使用条款侵犯了 GPL。[^85] 苹果公司没有改变这些条款以符合 GPL 的规定，而是将 GPL 授权的产品从其应用程序商店中删除。[^86] VLC 的作者是这些投诉的中心的 GPL 许可程序之一，最近开始从 GPL 转向 LGPL 和 MPL 的过程。[^87][^88]

## Examples / 案例

**Main article: [List of commercial open-source applications and services](https://en.wikipedia.org/wiki/List_of_commercial_open-source_applications_and_services) / 主词条：商业开放源码应用程序和服务清单**

Much of the Internet runs on open-source software tools and utilities such as Linux, Apache, MySQL, and PHP, known as the LAMP stack for web servers. Using open source appeals to software developers for three main reasons: low or no cost, access to source code they can tailor themselves, and a shared community that ensures a generally robust code base, with quick fixes for new issues.

许多互联网都运行在开源软件工具和实用程序上，如 Linux、Apache、MySQL 和 PHP，被称为网络服务器的 LAMP 堆栈。使用开源软件吸引软件开发者的主要原因有三个：尽可能的零成本或者低成本，获得可以自己定制的源代码，以及参与共享的社区，确保一个普遍强大的代码基础，并且快速修复新问题。

Despite doing much business in proprietary software, some companies like Oracle Corporation and IBM participated in developing free and open-source software to deter from monopolies and take a portion of market share for themselves. See Commercial open-source applications for the list of current commercial open-source offerings. Netscape's actions were an example of this, and thus Mozilla Firefox has become more popular, getting market share from Internet Explorer.

尽管在专有软件方面做了很多生意，但一些公司，如甲骨文公司和 IBM，还是参与了自由和开放源码软件的开发，以防止垄断，并为自己争取一部分市场份额。目前的商业开放源码产品清单见商业开放源码应用程序。网景公司的行为就是一个例子，因此，Mozilla Firefox 变得更加流行，从 IE 浏览器那里得到了市场份额。

* Active Agenda is offered for free, but requires all extensions to be shared back with the world community. The project sells a "Non-Reciprocal Private License" to anyone * interested in keeping module extensions private.
* Adobe Systems offers Flex for free, while selling the Flash Builder IDE.
* Apple Inc. offers Darwin for free, while selling Mac OS X.
* Asterisk, digital electronics hardware controlled by open-source software
* Codeweavers sells CrossOver commercially, deriving it from the free Wine project they also back.
* Canonical Ltd. offers Ubuntu for free, while they sell commercial technical support contracts.
* Cloudera's Apache Hadoop-based software.
* Francisco Burzi offers PHP-Nuke for free, but the latest version is offered commercially.
* IBM proprietary Linux software, where IBM delivers database software, middleware and other software.
* Ingres is offered for free, but services and support are offered as a subscription. The Ingres Icebreaker Appliance is also offered as a commercial database appliance.
* id Software releases their legacy game engines under the GPL, while retaining proprietary ownership on their latest incarnation.
* Mozilla Foundation have a partnership with Google and other companies which provides revenue for inclusion of search engines in Mozilla Firefox.
* MySQL is offered for free, but with the enterprise version includes support and additional features.
* SUSE offers openSUSE for free through the openSUSE Project, while selling SUSE Linux Enterprise (SLE).
* OpenSearchServer offers its community edition on SourceForge and an enterprise edition with professional services to enterprises with a paid license
* Oracle - VirtualBox is free and open to anyone, but the VirtualBox extension pack can only be used for free at home, thus requiring payment from business users
* OWASP Foundation is a professional community of open-source developers focused on raising visible for software security.
* Red Hat sells support subscriptions for Red Hat Enterprise Linux (RHEL) which is an enterprise distribution periodically forked from the community-developed Fedora.
* Sourcefire offers Snort for free, while selling Sourcefire 3D.
* Sun Microsystems (acquired by Oracle in 2010) once offered OpenOffice.org for free, while selling StarOffice
* Untangle provides its Lite Package for free, while selling its Standard and Premium Packages by subscription
* Zend Technologies offers Zend Server CE and Laminas for free, but sells Zend Server with support and additional features.

## Further reading / 延伸阅读

* Popp, Karl Michael (2015). "Open Source Business Models". Open Source Best Practices.
* Koenig, John (2004). "Seven Open Source Business Strategies for Commercial Advantage" (PDF). Riseforth. Archived from the original (PDF) on 2017-01-12. Retrieved 2014-10-18.
* Wheeler, David A. (14 June 2011). "Free-Libre / Open Source Software (FLOSS) is Commercial Software" (published 27 December 2006).
* "Selling Free Software". Free Software Foundation. 18 November 2016.
* Perens, Bruce (3 October 2005). "The emerging economic paradigm of Open Source". First Monday (2). doi:10.5210/fm.v0i0.1470.
* Raya, Amadeu Albós; Martínez, Lluís Bru; Monsalve, Irene Fernández (September 2010). "Economic aspects and business models of Free Software" (PDF). Archived (PDF) from the original on 27 May 2016.
* Chang, Victor; Mills, Hugo; Newhouse, Steven (27 March 2014). "From Open Source to long-term sustainability: Review of Business Models and Case studies". University of Southampton (published 20 June 2007).
* Fink, Martin (2003). The Business and Economics of Linux and Open Source. Prentice Hall Professional. ISBN 9780130476777.
* Dornan, Andy (2 January 2008). "The Five Open Source Business Models". InformationWeek.
* Golden, Bernard (2005). "2: Open Source Business Models". Succeeding with Open Source. Boston: Addison-Wesley Professional. ISBN 9780321268532.
* Tapscott, Don; Williams, Anthony D. (December 2006). Wikinomics: How Mass Collaboration Changes Everything. Portfolio. ISBN 9781591841388.

## References / 参考链接

[^1]: ["MySQL :: Commercial License for OEMs, ISVs and VARs"](https://www.mysql.com/about/legal/licensing/oem/). www.mysql.com. Retrieved 2019-09-11.
[^2]: ["COSSI: $100M+ Revenue Commercial Open-Source Software Company Index"](https://docs.google.com/spreadsheets/d/17nKMpi_Dh5slCqzLSFBoWMxNvWiwt2R-t4e_l7LPLhU/edit?usp=embed_facebook). Google Docs. Retrieved 2019-08-28.
[^3]: Popp, Dr. Karl Michael (2015). Best Practices for commercial use of open source software. Norderstedt, Germany: Books on Demand. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier)) [978-3738619096](https://en.wikipedia.org/wiki/Special:BookSources/978-3738619096).
[^4]: Riehle, Dirk. ["The Single-Vendor Commercial Open Source Business Model"](https://www.researchgate.net/publication/220385101). Researchgate. Retrieved 19 September 2021.
[^5]: Germain, Jack M. (5 November 2013). ["FOSS in the Enterprise: To Pay or Not to Pay?"](http://www.linuxinsider.com/story/79341.html). LinuxInsider. ECT News Network, Inc. Retrieved 18 June 2016.
[^6]: Rubens, Paul (13 February 2013). ["6 Reasons to Pay for Open Source Software"](http://www.cio.com/article/2388344/open-source-tools/6-reasons-to-pay-for-open-source-software.html). CIO. [CXO Media, Inc](https://en.wikipedia.org/wiki/CXO_Media,_Inc.). Retrieved 18 June 2016. Open source software is free to download, modify and use, but that doesn't mean it's not worth paying for sometimes. If you're using open source software in a commercial, enterprise capacity, here are six reasons why you should pay for free software."
[^7]: McMillan, Robert (28 March 2012). ["Red Hat Becomes Open Source's First $1 Billion Baby"](https://www.wired.com/2012/03/red-hat/). [Wired](https://en.wikipedia.org/wiki/Wired_(website)). Retrieved 18 June 2016. Other companies have made big money selling Linux — Intel, IBM, Dell, and others have used it as a way to sell hardware and support services — but Red Hat has managed the tricky business of building a software platform that big businesses will pay for.
[^8]: Markham, Gervase (16 March 2004). ["Mozilla Foundation Open Letter Orders Unofficial Mozilla Merchandise Sellers to Stop, Legal Action Hinted"](http://www.mozillazine.org/articles/article4484.html). MozillaZine. Retrieved 18 June 2016.
[^9]: ["Wikipedia Store"](https://store.wikimedia.org/). Wikimedia Foundation. 2016. Retrieved 18 June 2016.
[^10]: ["Licenses"](https://www.gnu.org/licenses/index.html). GNU Project. Free Software Foundation. The GNU Affero General Public License. Retrieved 18 June 2016. We recommend that people consider using the GNU AGPL for any software which will commonly be run over a network.
[^11]: Tiemann, Michael (7 June 2007). ["GNU Affero GPL version 3 and the "ASP loophole""](https://opensource.org/node/152). [Open Source Initiative](https://en.wikipedia.org/wiki/Open_Source_Initiative). Retrieved 18 June 2016.
[^12]: ["Frequently Asked Questions about the GNU Licenses"](https://www.gnu.org/licenses/gpl-faq.html#SeparateAffero). GNU Project. [Free Software Foundation](https://en.wikipedia.org/wiki/Free_Software_Foundation). 26 May 2016. Why did you decide to write the GNU Affero GPLv3 as a separate license?. Retrieved 18 June 2016.
[^13]: Sneddon, Joey-Elijah (2012-06-01). ["Will You Help Change The Way Open-Source Apps are Funded?"](http://www.omgubuntu.co.uk/2012/06/help-linux-tycoon-more-go-open-source). OMGUbuntu. Retrieved 2013-08-08. Lunduke is pledging to open-source and distribute his portfolio of hitherto paid software – which includes the Linux distro management simulator Linux Tycoon - for free, under the GPL, if he can reach a donation-driven funding goal of $4000/m. Reaching this goal, Lunduke says, 'will provide proof for others, who would also like to move their software businesses to be open source, that it is doable.'
[^14]: Naramore, Elizabeth (4 March 2011). ["SourceForge.net Donation System"](https://sourceforge.net/p/forge/documentation/Donations/?version=1). [SourceForge](https://en.wikipedia.org/wiki/SourceForge). Slashdot Media. Retrieved 16 October 2017.
[^15]: Mozilla Foundation (December 15, 2004). ["Mozilla Foundation Places Two-Page Advocacy Ad in The New York Times"](https://www-archive.mozilla.org/press/mozilla-2004-12-15.html). Retrieved June 15, 2010.
[^16]: Marson, Ingrid (2004-12-16). ["New York Times runs Firefox ad"](http://news.cnet.com/New-York-Times-runs-Firefox-ad/2100-1032_3-5493774.html). cnet.com. Retrieved 2013-08-12. Fans of the Mozilla Foundation's Firefox browser who funded an advertisement in The New York Times will finally get to see their names in print on Thursday.
[^17]: Tung, Liam. ["GitHub will now let you back your favourite open source developers"](https://www.zdnet.com/article/github-will-now-let-you-back-your-favourite-open-source-developers/). ZDNet. Retrieved 2019-08-26.
[^18]: Byfield, Bruce (21 September 2005). ["Google's Summer of Code concludes"](https://www.linux.com/news/googles-summer-code-concludes). linux.com. Retrieved 18 June 2016. DiBona said that the SOC was designed to benefit everyone involved in it. Students had the chance to work on real projects, rather than academic ones, and to get paid while gaining experience and making contacts. FOSS projects benefited from getting new code and having the chance to recruit new developers.
[^19]: Callaham, John (2013-06-06). ["Report: Google paying AdBlock Plus to not block Google's ads"](https://www.neowin.net/news/report-google-paying-adblock-plus-to-not-block-google039s-ads). [neowin](https://en.wikipedia.org/wiki/Neowin).com. Retrieved 2013-08-13. Google is paying money to Eyeo, the company behind AdBlock Plus, so that its ads get through the browser ad remover.
[^20]: Hunt, Katherine (2007-05-24). ["Sourceforge quarterly profit surges as revenue rises"](http://www.marketwatch.com/story/sourceforge-quarterly-profit-surges-as-revenue-rises). marketwatch.com. Retrieved 2013-08-13. Software Corp., late Thursday reported third-quarter net earnings of $6.49 million, or 9 cents a share, up from $997,000, or 2 cents a share, during the year-ago period. Pro forma earnings from continuing operations were $2.1 million, or 3 cents a share, compared with $1.2 million, or 2 cents a share, last year. The Fremont, Calif.-based maker of computer servers and storage systems said revenue for the three months ended April 30 rose to $10.3 million from $7.9 million. Analysts, on average, had forecast a per-share profit of 2 cents on revenue of $12 million."
[^21]: ["SourceForge Reports Second Quarter Fiscal 2009 Financial Results"](https://web.archive.org/web/20150603170625/http://ir.corp.sourceforge.com/phoenix.zhtml?c=82629&p=irol-newsArticle&ID=1260642&highlight=). Archived from the original on 2015-06-03.
[^22]: Leyden, John (2004-08-03), [Mozilla to pay bounty on bugs](http://www.securityfocus.com/news/9255), [The Register](https://en.wikipedia.org/wiki/The_Register), retrieved 2013-08-10
[^23]: Evers, Joris (July 25, 2005). ["Offering a bounty for security bugs"](http://news.cnet.com/2100-7350_3-5802411.html). [CNET](https://en.wikipedia.org/wiki/CNET). [CBS Interactive](https://en.wikipedia.org/wiki/CBS_Interactive). Retrieved 12 August 2007.
[^24]: ["Mozilla Foundation Announces Security Bug Bounty Program"](https://blog.mozilla.org/press/2004/08/mozilla-foundation-announces-security-bug-bounty-program/). [Mozilla Foundation]. Mountain View, California. August 2, 2004. Retrieved 2013-08-10.
[^25]: Lunduke, Bryan (2013-08-07). ["Open source gets its own crowd-funding site, with bounties included - Bountysource is the crowd-funding site the open source community has been waiting for"](http://www.networkworld.com/community/blog/open-source-gets-its-own-crowd-funding-site-bounties-included). networkworld.com. Retrieved 2013-08-10. Many open source projects (from phones to programming tools) have taken to crowd-funding sites (such as Kickstarter and indiegogo) in order to raise the cash needed for large-scale development. And, in some cases, this has worked out quite well.
[^26]: Arceri, Timothy (2013-07-26). ["Help improve OpenGL support for the Linux Graphics Drivers"](http://www.indiegogo.com/projects/help-improve-opengl-support-for-the-linux-graphics-drivers). [Indiegogo](https://en.wikipedia.org/wiki/Indiegogo). Retrieved 2013-08-11. Helping fund the time for me to become a Mesa contributor and document the experience to make it easier for others to understand where to start with the Mesa codebase. Many people have brought up the idea of crowd sourcing open source driver development. This is a small scale experiment to see if it could actually work."
[^27]: ["Bountysource Raises $1.1 Million for the First Crowdfunding Platform for Open-Source Software Projects"](https://finance.yahoo.com/news/bountysource-raises-1-1-million-130000440.html). Yahoo Finance. Marketwired. 16 July 2013. Retrieved 18 June 2016.
[^28]: Larabel, Michael (12 November 2013). ["Crowd-Funding Is Back For Another Mesa Extension"](https://www.phoronix.com/scan.php?page=news_item&px=MTUxMTQ). [Phoronix](https://en.wikipedia.org/wiki/Phoronix).
[^29]: Larabel, Michael (14 February 2017). ["Valve Has Another Linux Graphics Driver Developer Working On Open-Source AMD"](https://www.phoronix.com/scan.php?page=news_item&px=Arceri-Joined-Valve). [Phoronix](https://en.wikipedia.org/wiki/Phoronix).
[^30]: ["Cataclysm: Dark Days Ahead - Dedicated Developer"](http://www.kickstarter.com/projects/568375735/cataclysm-dark-days-ahead-dedicated-developer/). [Kickstarter](https://en.wikipedia.org/wiki/Kickstarter). 22 June 2013.
[^31]: ["Multipocalyptic Roguelike Cataclysm: Dark Days Ahead Turns To Kickstarter"](https://web.archive.org/web/20140401001904/http://indiestatik.com/2013/06/22/cataclysm-dda-kickstarter/). Archived from [the original](http://indiestatik.com/2013/06/22/cataclysm-dda-kickstarter/) on 2014-04-01.
[^32]: Marchant, Julie. ["Julie Marchant is creating libre video games"](https://www.patreon.com/onpon4). [Patreon](https://en.wikipedia.org/wiki/Patreon).
[^33]: Solatan, Jean (2011). Advances in software economics: A reader on business models and Partner Ecosystems in the software industry. Norderstedt, Germany: BOD. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier)) [978-3-8448-0405-8](https://en.wikipedia.org/wiki/Special:BookSources/978-3-8448-0405-8).
[^34]: ["Commercial License for OEMs, ISVs and VARs"](http://www.mysql.com/about/legal/licensing/oem/#5). MySQL.com. Oracle. July 2010. Q4: What is Oracle's dual license model for MySQL software?. Retrieved 18 June 2016. Oracle makes its MySQL database server and MySQL Client Libraries available under both the GPL and a commercial license. As a result, developers who use or distribute open source applications under the GPL can use the GPL-licensed MySQL software, and OEMs, ISVs and VARs that do not want to combine or distribute the MySQL software with their own commercial software under a GPL license can purchase a commercial license."
[^35]: Ronacher, Armin (23 July 2013). ["Licensing in a Post Copyright World"](http://lucumr.pocoo.org/2013/7/23/licensing/). Armin Ronacher's Thoughts and Writings. What Changed in 2007. Retrieved 18 June 2016. The AGPLv3 was a terrible success, especially among the startup community that found the perfect base license to make dual licensing with a commercial license feasible. MongoDB, RethinkDB, OpenERP, SugarCRM as well as WURFL all now utilize the AGPLv3 as a vehicle for dual commercial licensing. The AGPLv3 makes that generally easy to accomplish as the original copyright author has the rights to make a commercial license possible but nobody who receives the sourcecode itself through the APLv3 inherits that right. I am not sure if that was the intended use of the license, but that's at least what it's definitely being used for now."
[^36]: Gartner, Samantha (6 October 2014). ["Moodle will always be an open source project"](https://opensource.com/education/14/10/open-access-learning-moodle). opensource.com. Retrieved 18 June 2016.
[^37]: Dougiamas, Martin (22 January 2014). ["Moodle: a case study in sustainability"](http://oss-watch.ac.uk/resources/cs-moodle). OSS Watch. University of Oxford (published 5 June 2007). Retrieved 18 June 2016.
[^38]: ["How do the Moodle Partners work?"](https://web.archive.org/web/20140722023159/http://moodle.com/partners/about/). Moodle. 2012. Archived from [the original](http://moodle.com/partners/about/) on 22 July 2014. Retrieved 18 June 2016.
[^39]: ["The Moodle Trademark"](https://moodle.com/trademarks/). Moodle. 2016. Retrieved 18 June 2016.
[^40]: Kolowich, Steve (27 March 2012). ["Blackboard's Open-Source Pivot"](http://www.insidehighered.com/news/2012/03/27/blackboard-buys-moodlerooms-creates-open-source-division). Inside Higher Ed. Retrieved 18 June 2016.
[^41]: Montague, Bruce (2013-11-13). ["Why you should use a BSD style license for your Open Source Project - GPL Advantages and Disadvantages"](http://www.freebsd.org/doc/en_US.ISO8859-1/articles/bsdl-gpl/article.html). [FreeBSD](https://en.wikipedia.org/wiki/FreeBSD). Retrieved 2015-11-28. In contrast to the GPL, which is designed to prevent the proprietary commercialization of Open Source code, the BSD license places minimal restrictions on future behavior. This allows BSD code to remain Open Source or become integrated into commercial solutions, as a project's or company's needs change. In other words, the BSD license does not become a legal time-bomb at any point in the development process. In addition, since the BSD license does not come with the legal complexity of the GPL or LGPL licenses, it allows developers and companies to spend their time creating and promoting good code rather than worrying if that code violates licensing."
[^42]: Oram, Andy (2011-08-26). ["How Free Software Contributed to the Success of Steve Jobs and Apple"](http://radar.oreilly.com/2011/08/how-free-software-contributed.html). radar.oreilly.com. Retrieved 2013-08-10. the BSD license allowed Apple to keep its changes proprietary"
[^43]: Olson, Mike (13 November 2013). [Opportunities Abound in the Big Data Space](http://ecorner.stanford.edu/videos/3223/Opportunities-Abound-in-the-Big-Data-Space-Entire-Talk). Stanford eCorner. Stanford University.
[^44]: Hustvedt, Eskild (2009-02-08). ["Our new way to meet the LGPL"](https://web.archive.org/web/20090220234542/http://blog.linuxgamepublishing.com/2009/02/08/our-new-way-to-meet-the-lgpl/). Archived from [the original](http://blog.linuxgamepublishing.com/2009/02/08/our-new-way-to-meet-the-lgpl/) on 2009-02-20. Retrieved 2011-03-09. You can use a special keyword $ORIGIN to say 'relative to the actual location of the executable'. Suddenly we found we could use -rpath $ORIGIN/lib and it worked. The game was loading the correct libraries, and so was stable and portable, but was also now completely in the spirit of the LGPL as well as the letter!"
[^45]: ["TTimo/doom3.gpl"](https://github.com/TTimo/doom3.gpl). [GitHub](https://en.wikipedia.org/wiki/GitHub). 2012-04-07. Retrieved 2013-08-10. "Doom 3 GPL source release [...] This source release does not contain any game data, the game data is still covered by the original EULA and must be obeyed as usual."
[^46]: ["STEEL STORM EPISODE 1 LIMITED USER SOFTWARE LICENSE AGREEMENT"](http://www.steel-storm.com/ss_license.html). steel-storm.com. Retrieved 2013-08-10. "For the purpose of this Agreement, the Art Assets include pk3 archive inside of 'steelstorm/gamedata/' folder that contain two-dimensional and three-dimensional works of graphic art, photographs, prints and art reproductions, maps, charts, diagrams, models, and technical drawings, sound effects and musical arrangements, documentation and tutorial videos, and are licensed under Attribution-NonCommercial-ShareAlike 3.0 Unported license. The Engine, which includes Windows, Linux and Mac binaries, and the Engine's source code, are licensed under GNU GPL v2 license."
[^47]: Simpson, Kristina (2015-04-26). ["LICENCE"](https://github.com/anura-engine/anura/blob/trunk/LICENSE). anura-engine - GitHub. Retrieved 2015-10-10.
[^48]: frogatto (15 April 2020). ["License"](https://github.com/frogatto/frogatto/blob/master/LICENSE). [GitHub](https://en.wikipedia.org/wiki/GitHub). "CC-BY 3.0 LICENSE [...] assets under copyright"
[^49]: Gabovitch, Iwan (22 April 2011). "Humble Indie Bundle's Source Releases". "Another game which is commercial (on iDevices) and has FOSS code and closed art [...] is Frogatto."
[^50]: Nick (2011-01-14). ["Arx Fatalis source code, patch released!"](http://bethblog.com/index.php/2011/01/14/arx-fatalis-source-code-patch-released/). bethblog.com. Retrieved 2011-08-10.
[^51]: Larabel, Michael (6 June 2014). ["id Software's Softdisk Open-Sources Some Really Old Games"](https://www.phoronix.com/scan.php?page=news_item&px=MTcxMjM). [Phoronix](https://en.wikipedia.org/wiki/Phoronix).
[^52]: Ohle, Tom (4 December 2008). ["Straight out of the Dungeon, Arx Fatalis invades GOG.com"](http://www.develop-online.net/press-releases/straight-out-of-the-dungeon-arx-fatalis-invades-gog-com/0129540). Develop-Online.net (Press release). [Warsaw](https://en.wikipedia.org/wiki/Warsaw), [Poland](https://en.wikipedia.org/wiki/Poland).
[^53]: Stallman, Richard (2012). ["On-line education is using a flawed Creative Commons license"](http://stallman.org/articles/online-education.html). stallman.org. Retrieved 2013-08-10. "In my view, nonfree licenses that permit sharing are ok for works of art/entertainment, or that present some party's viewpoint (such as this article itself). Those works aren't meant for doing a practical job, so the argument about the users' control does not apply. Thus, I do not object if they are published with the CC-BY-NC-ND license, which allows only noncommercial redistribution of exact copies."
[^54]: ["Activities - FSFE"](https://fsfe.org/activities/activities.html). FSFE - Free Software Foundation Europe.
[^55]: ["gnu.org"](https://www.gnu.org/philosophy/when-free-depends-on-nonfree.en.html). www.gnu.org. Retrieved 2017-11-10.
[^56]: ["ardour"](https://ardour.org/download.html).
[^57]: ["radium"](http://users.notam02.no/~kjetism/radium/download.php).
[^58]: ["fritzing"](https://fritzing.org/download/).
[^59]: ["Frequently Asked Questions about the GNU Licenses"](https://www.gnu.org/licenses/gpl-faq.en.html#DoesTheGPLAllowMoney).
[^60]: [Larabel, Michael](https://en.wikipedia.org/wiki/Michael_Larabel) (26 March 2010). ["NVIDIA Drops Their Open-Source Driver, Refers Users To VESA Driver"](https://www.phoronix.com/scan.php?page=article&item=nvidia_kills_nv&num=1). Phoronix. "The xf86-video-nv driver has been around that provides very basic 2D acceleration and a crippled set of features besides that (no proper RandR 1.2/1.3, KMS, power management, etc.) while the code has also been obfuscated to try to protect their intellectual property."
[^61]: ["What is free software?"](https://www.gnu.org/philosophy/free-sw.html). [Free Software Foundation](https://en.wikipedia.org/wiki/Free_Software_Foundation). "Obfuscated "source code" is not real source code and does not count as source code."
[^62]: ["Reasoning behind the "preferred form" language in the GPL"](https://lwn.net/Articles/431651/). lwn.net. 2011-03-07. Retrieved 2013-08-19.
[^63]: Sprewell (29 April 2010). ["Towards A Real Business Model For Open-Source Software"](https://www.phoronix.com/scan.php?page=article&item=sprewell_licensing&num=1). [Phoronix](https://en.wikipedia.org/wiki/Phoronix).
[^64]: Martin, Alexander J (24 August 2016). ["MySQL daddy Widenius: Open-source religion won't feed MariaDB"](https://www.theregister.co.uk/2016/08/24/monty_interview/). [The Register](https://en.wikipedia.org/wiki/The_Register).
[^65]: [Phipps, Simon](https://en.wikipedia.org/wiki/Simon_Phipps_(programmer)) (19 August 2016). ["Uproar: MariaDB Corp. veers away from open source"](https://www.infoworld.com/article/3109213/open-source-tools/open-source-uproar-as-mariadb-goes-commercial.html). [InfoWorld](https://en.wikipedia.org/wiki/InfoWorld).
[^66]: [sl-1-1](https://perens.com/2017/02/14/bsl-1-1/) on perens.com (2017-02-14)
[^67]: [releasing-bsl-11](https://mariadb.com/resources/blog/releasing-bsl-11) on mariadb.com by Kaj Arnö (2017)
[^68]: ["id Software releases Doom 3 source code"](http://www.h-online.com/open/news/item/id-Software-releases-Doom-3-source-code-1383572.html). The H Open. 23 November 2011. [Archived](https://web.archive.org/web/20131208041324/http://www.h-online.com/open/news/item/id-Software-releases-Doom-3-source-code-1383572.html) from the original on 8 December 2013.
[^69]: Spencer, Spanner (24 March 2009). ["id Software makes iPhone Wolfenstein open source"](http://www.pocketgamer.co.uk/r/iPhone/Wolfenstein+3D+Classic/news.asp?c=12324). PocketGamer.co.uk.
[^70]: Siegler, Joe (1 April 2005). ["Shadow Warrior Source Code Released"](http://legacy.3drealms.com/news/2005/04/shadow_warrior_12.html). [3D Realms](https://en.wikipedia.org/wiki/3D_Realms).
[^71]: ["Games"](http://legacy.3drealms.com/games.html). [3D Realms](https://en.wikipedia.org/wiki/3D_Realms). "Selected games have had their source code released by us. These games are: Duke Nukem 3D, Shadow Warrior, Rise of the Triad, Word Whiz, Beyond the Titanic, Supernova, & Kroz. You can obtain these from our downloads page."
[^72]: Andersen, John (2011-01-27). ["Where Games Go To Sleep: The Game Preservation Crisis, Part 1"](http://www.gamasutra.com/view/feature/6271/where_games_go_to_sleep_the_game_.php?print=1). [Gamasutra](https://en.wikipedia.org/wiki/Gamasutra). Retrieved 2013-01-10. "The existence of decaying technology, disorganization, and poor storage could in theory put a video game to sleep permanently – never to be played again. Troubling admissions have surfaced over the years concerning video game preservation. When questions concerning re-releases of certain game titles are brought up during interviews with developers, for example, these developers would reveal issues of game production material being lost or destroyed. Certain game titles could not see a re-release due to various issues. One story began to circulate of source code being lost altogether for a well-known RPG, preventing its re-release on a new console."
[^73]: Bell, John (2009-10-01). ["Opening the Source of Art"](https://web.archive.org/web/20140330084636/http://timreview.ca/article/294). Technology Innovation Management Review. Archived from [the original](http://timreview.ca/article/294) on 2014-03-30. Retrieved 2013-08-09. "[...]that no further patches to the title would be forthcoming. The community was predictably upset. Instead of giving up on the game, users decided that if Activision wasn't going to fix the bugs, they would. They wanted to save the game by getting Activision to open the source so it could be kept alive beyond the point where Activision lost interest. With some help from members of the development team that were active on fan forums, they were eventually able to convince Activision to release Call to Power II's source code in October of 2003."
[^74]: ["NETSCAPE ANNOUNCES PLANS TO MAKE NEXT-GENERATION COMMUNICATOR SOURCE CODE AVAILABLE FREE ON THE NET"](https://web.archive.org/web/20070401072854/http://wp.netscape.com/newsref/pr/newsrelease558.html). [Netscape Communications Corporation](https://en.wikipedia.org/wiki/Netscape_Communications_Corporation). 1998-01-22. Archived from [the original](http://wp.netscape.com/newsref/pr/newsrelease558.html) on 2007-04-01. Retrieved 2013-08-08. "BOLD MOVE TO HARNESS CREATIVE POWER OF THOUSANDS OF INTERNET DEVELOPERS; COMPANY MAKES NETSCAPE NAVIGATOR AND COMMUNICATOR 4.0 IMMEDIATELY FREE FOR ALL USERS, SEEDING MARKET FOR ENTERPRISE AND NETCENTER BUSINESSES"
[^75]: ["MOUNTAIN VIEW, Calif., April 1 /PRNewswire/ -- Netscape Communications and open source developers are celebrating the first anniversary, March 31, 1999, of the release of Netscape's browser source code to mozilla.org"](http://www.prnewswire.com/news-releases/netscape-celebrates-first-anniversary-of-open-source-software-release-to-mozillaorg-73806207.html). [Netscape Communications](https://en.wikipedia.org/wiki/Netscape_Communications). 1999-03-31. Retrieved 2013-01-10. [...] The organization that manages open source developers working on the next generation of Netscape's browser and communication software. This event marked a historical milestone for the Internet as Netscape became the first major commercial software company to open its source code, a trend that has since been followed by several other corporations. Since the code was first published on the Internet, thousands of individuals and organizations have downloaded it and made hundreds of contributions to the software. Mozilla.org is now celebrating this one-year anniversary with a party Thursday night in San Francisco.
[^76]: Proffitt, Brian (2000-10-13). ["StarOffice Code Released in Largest Open Source Project"](https://web.archive.org/web/20131016014106/http://www.linuxtoday.com/developer/2000101300221NWDTSW). linuxtoday.com. Archived from [the original](http://www.linuxtoday.com/developer/2000101300221NWDTSW) on 2013-10-16. Retrieved 2013-01-10. "Sun's joint effort with CollabNet kicked into high gear on the OpenOffice Web site at 5 a.m. PST this morning with the release of much of the source code for the upcoming 6.0 version of StarOffice. According to Sun, this release of 9 million lines of code under GPL is the beginning of the largest open source software project ever."
[^77]: ["Outreachy | Internships Supporting Diversity in Tech"](https://www.outreachy.org/). www.outreachy.org. Retrieved 2019-11-28.
[^78]: Holtgrewe, Ursula (March 2004). ["Articulating the Speed(s) of the Internet: The Case of Open Source/Free Software"](http://www.ssoar.info/ssoar/handle/document/12259). [Time & Society](https://en.wikipedia.org/wiki/Time_%26_Society). 13: 129–146. [doi](https://en.wikipedia.org/wiki/Doi_(identifier)):[10.1177/0961463X04040750](https://doi.org/10.1177%2F0961463X04040750). [S2CID](https://en.wikipedia.org/wiki/S2CID_(identifier)) [61327593](https://api.semanticscholar.org/CorpusID:61327593).
[^79]: Popp, Dr. Karl Michael; Meyer, Ralf (2010). [Profit from Software Ecosystems: Business Models, Ecosystems and Partnerships in the Software Industry](https://books.google.com/books?id=i1VGDLCMyKAC). Norderstedt, Germany: Books on Demand. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier)) [9783839169834](https://en.wikipedia.org/wiki/Special:BookSources/9783839169834).
[^80]: Wheeler, David A. (February 2009). ["F/LOSS is Commercial Software"](http://timreview.ca/article/229). Technology Innovation Management Review. Talent First Network. Retrieved 18 June 2016.
[^81]: Stallman, Richard (11 March 2012). [Richard Stallman (S20E10)](https://www.youtube.com/watch?v=radmjL5OIaA&t=0h53m46s) (Podcast). The Linux Action Show. [Jupiter Broadcasting](https://en.wikipedia.org/wiki/Jupiter_Broadcasting). Event occurs at 0:53:46. Retrieved 18 June 2016. "I'm not going to claim that I got a way to make it easier to raise money to pay people who write free software. We all know, that to some extent there are ways to do that, but we all know that they are limited, they are not as broad as we would like."
[^82]: Donovan, S. (6 August 2002). "Patent, copyright and trade secret protection for software". IEEE Potentials (published 1994). 13 (3): 20. [doi](https://en.wikipedia.org/wiki/Doi_(identifier)):[10.1109/45.310923](https://doi.org/10.1109%2F45.310923). [ISSN](https://en.wikipedia.org/wiki/ISSN_(identifier)) [0278-6648](https://www.worldcat.org/issn/0278-6648). [S2CID](https://en.wikipedia.org/wiki/S2CID_(identifier)) [19873766](https://api.semanticscholar.org/CorpusID:19873766). "Essentially there are only three ways to protect computer software under the law: patent it, register a copyright for it, or keep it as a trade secret."
[^83]: Benkler, Yochai (April 2003). ["Freedom in the Commons: Towards a Political Economy of Information"](https://web.archive.org/web/20110306041013/https://www.law.duke.edu/shell/cite.pl?52+Duke+L.+J.+1245+pdf). Duke Law Journal. 52 (6). Archived from [the original](http://www.law.duke.edu/shell/cite.pl?52+Duke+L.+J.+1245+pdf) on 2011-03-06. Retrieved 2013-09-16.
[^84]: ElBoghdady, Dina; Tsukayama, Hayley (2011-09-30). ["Facebook tracking prompts calls for FTC investigation"](https://www.washingtonpost.com/business/economy/facebook-tracking-prompts-calls-for-ftc-investigation/2011/09/29/gIQAVdsP8K_story.html). [The Washington Post](https://en.wikipedia.org/wiki/The_Washington_Post). Retrieved 23 October 2011.
[^85]: Cheng, Jacqui (10 January 2011). ["VLC for iOS vanishes 2 months after eruption of GPL dispute"](https://arstechnica.com/gadgets/2011/01/vlc-for-ios-vanishes-2-months-after-eruption-of-gpl-dispute/). [Ars Technica](https://en.wikipedia.org/wiki/Ars_Technica).
[^86]: Vaughan-Nichols, Steven. ["No GPL Apps for Apple's App Store"](https://www.zdnet.com/blog/open-source/no-gpl-apps-for-apples-app-store/8046). [ZDNet](https://en.wikipedia.org/wiki/ZDNet). Retrieved 23 October 2011.
[^87]: ["Changing the VLC engine license to LGPL"](http://www.videolan.org/press/lgpl.html). Retrieved 23 October 2011.
[^88]: Johnston, Casey (18 July 2013). ["VLC media player returns to the iOS App Store after 30-month hiatus"](https://arstechnica.com/gadgets/2013/07/vlc-media-player-returns-to-the-ios-app-store-after-30-month-hiatus/). [Ars Technica](https://en.wikipedia.org/wiki/Ars_Technica). Retrieved 10 October 2013.