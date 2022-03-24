---
layout: post
title: "【翻译】开源促进会没有赢得 Neo4j 诉 PureThink 案的胜利"
date: 2022-03-25 13:51 +0800
categories: OpenSource Law
comments: true
---

翻译来源：[The Open Source Initiative Did Not Win Neo4j v. PureThink](https://writing.kemitchell.com/2022/03/17/OSI-Neo4j-PureThink.html)


**everywhere it looks, OSI sees itself, and in triumph**

**无论在哪里，OSI 都能看到自己，并取得胜利**

The Open Source Initiative's blog post on the Neo4j appeal is self-serving, misleading, and wrong. Again.

开放源码促进会关于 Neo4j 上诉的博文是为自己服务的，误导性的，而且是错误的。咱们再来仔细看看。

OSI claims:

OSI 声称：

> The court only confirmed what we already know — that "open source" is a term of art for software that has been licensed under a specific type of license, and whether a license is an OSI-approved license is a critically important factor in user adoption of the software.

> 法院只是证实了我们已经知道的事实 -- “开放源代码”是一个术语，指的是在特定类型的许可证下获得许可的软件，而许可证是否是 OSI 批准的许可证是用户采用软件的一个至关重要的因素。

No it didn't.

不，它没有。

The court didn't legally decide anything about the meaning of "open source". It didn't define any new terms of art legal-system-wide. It didn't even make precedent. The first page of its decision says "NOT FOR PUBLICATION" at the top and "This disposition is not appropriate for publication and is not precedent except as provided by Ninth Circuit Rule 36-3" at the bottom.

法院没有从法律上决定任何关于“开源”的含义。它并没有在整个法律系统中定义任何新的艺术术语。它甚至没有创造先例。其裁决的第一页顶部写着“不供发表”，底部写着“除第九巡回法庭规则 36-3 规定的情况外，本处理意见不适合发表，也不是先例”。

But even if the appeals court had made precedent, there's nothing in its decision about OSI. Here's the appellate court disposition. Here's the trial court order. Search them for "Open Source Initiative". You won't find it. Neither trial court nor appeals court even mentioned OSI, OSI approval, any license list, or any trademark on the term.

但即使上诉法院做出了先例，其裁决中也没有关于 OSI 的内容。这是上诉法院的处理意见。这里是审判法庭的命令。在其中搜索“OSI”。你不会找到它。无论是初审法院还是上诉法院，甚至都没有提到 OSI、OSI 的批准、任何许可清单，或任何关于这个词的商标。

The relevant bit from the appeals court is here:

上诉法院的相关内容在此：

> Defendants' representation that ONgDB is a "free and open-source" version of Neo4j(R) EE was literally false, because Section 7 of the Sweden Software License only permits a downstream licensee to remove "further restrictions" added by an upstream licensee to the original work.

> 被告声称 ONgDB 是 Neo4j(R)EE 的“免费和开源”版本，这在字面上是错误的，因为瑞典软件许可证第 7 条只允许下游被许可人删除上游被许可人对原始作品添加的“进一步限制”。

If that seems like a strange way to decide if something's free and open source, that's because it is. But it's the way that matters in this lawsuit, because it's the way the lawyers agreed to argue the point. The trial court judge followed their lead:

如果这看起来像一个奇怪的方式来决定一个东西是否是自由和开源的，那是因为它就是这样的。但在这场诉讼中，这是最重要的方式，因为这是律师们同意争论的方式。初审法院的法官跟随他们的思路：

> …Plaintiffs argue that Defendants' representations that ONgDB is "free and open source" is false because "the Neo4j Sweden Software License did not permit Defendants to remove the commercial restrictions imposed by the Commons Clause." The parties agree that the truth or falsity of Defendants' statements hinge on "the interpretation of Section 7 [of the Neo4j Sweden Software License], and GFI's right to remove the Commons Clause from the Neo4j Sweden Software License." Cross-Motion at 30; see also Plaintiff's Reply at 18 ("Defendants do not dispute that their marketing of ONgDB as 'free and open source' Neo4j(R) EE is primarily based on their (mis)interpretation of the Neo4j Sweden Software License and the form AGPLE upon which it was based.")

> 原告认为，被告关于 ONgDB 是“自由和开源”的陈述是错误的，因为“Neo4j 瑞典软件许可证不允许被告删除共享条款所施加的商业限制。”双方同意，被告陈述的真实性或虚假性取决于“对【Neo4j 瑞典软件许可证】第 7 条的解释，以及 GFI 从 Neo4j 瑞典软件许可证中删除共享条款的权利。” 反方动议，第 30 页；另见原告第 18 页的答复 ("被告对他们将 ONgDB 推销为'免费和开源'的 Neo4j(R) EE 主要是基于他们对 Neo4j 瑞典软件许可的（错误）解释以及作为其基础的 AGPLE 形式没有异议。"）

The actually interesting part of this whole kerfuffle is that the trial court decided PureThink could not rip Commons Clause out of the LICENSE file:

这场风波中真正有趣的部分是，审判法庭决定 PureThink 不能从 LICENSE 文件中删除 Commons 条款：

> Defendants argue that there is a reasonable interpretation of the Neo4j Sweden Software License that permits licensees, like GFI or Defendants, to remove the Commons Clause and redistribute the software under the standardized AGPL license. Cross-Motion at 27–30. The court disagrees.

> 被告认为，对 Neo4j 瑞典软件许可证有一个合理的解释，即允许被许可人，如 GFI 或被告，删除 Commons 条款，并根据标准化的 AGPL 许可证重新发布软件。反方动议在 27-30 页。法院不同意。

Since "could or couldn't remove Commons Clause" is how the parties agreed to argue whether the "free and open source" claims were true or false, and the court decided PureThink couldn't remove the Commons Clause, which it did, the claims about ONgDB were false. In the context of this lawsuit, ONgDB wasn't "free and open source" because PureThink removed Commons Clause from AGPL. Think about that. Check the "False Statement" section, starting on page 23.

由于“能否删除 Commons 条款”是双方同意争论“自由和开放源码”的说法是真的还是假的，而法院裁定 PureThink 不能删除 Commons 条款，而它确实这样做了，所以关于 ONgDB 的说法是假的。在这起诉讼中，ONgDB 不是“自由和开放源码”，因为 PureThink 从 AGPL 中删除了 Commons 条款。想想这个问题。请看第 23 页开始的“虚假声明”部分。

OSI's blog post gets this exactly wrong. They want to see a court holding that Neo4j's release wasn't open source because they added Commons Clause to AGPL. What they got is a court saying that taking Commons Clause away from AGPL made claims about being open source false claims. But OSI sees what it wants to see:

OSI 的博文完全搞错了这一点。他们希望看到法院认定 Neo4j 的发布不是开源的，因为他们在 AGPL 中加入了 Commons 条款。他们得到的是一个法院说，从 AGPL 中拿走 Commons 条款使得关于开源的说法成为虚假的说法。但 OSI 看到了它想看到的东西：

> But adding the non-free Commons Clause created a different license such that the software could not be characterized as "open source" and doing so in these circumstances was unlawful false advertising.

> 但是，加入非自由共享条款就形成了一种不同的许可，使该软件不能被定性为“开放源码”，在这种情况下这样做是非法的虚假宣传。

When we actually look at the way the trial court understood "open source", it's the opposite. The court took the original Neo4j release as open source "meaning that the source code was available to the public on GitHub pursuant to the GNU General Public License version 3". Later on, Neo4j added Commons Clause. But that was still "open source" as the court saw it:

当我们实际看一下初审法院对“开放源代码”的理解时，情况正好相反。法院将最初的 Neo4j 版本视为开源，“意味着根据 GNU 通用公共许可证第三版，源代码在 GitHub 上向公众提供”。后来，Neo4j 增加了 Commons 条款。但在法院看来，这仍然是“开放源代码”。

> In May 2018, Plaintiffs released Neo4j EE version 3.4, which they continued to offer under an open source license; however, they replaced the AGPL with a stricter license, which included the terms from the AGPLv3 and additional restrictions provided by the Commons Clause.

> 2018 年 5 月，原告发布了 Neo4j EE 3.4 版本，他们继续以开源许可的方式提供；但是，他们用更严格的许可取代了 AGPL，其中包括 AGPLv3 的条款和 Commons 条款提供的额外限制。

It's only when Neo4j went to a commercial license exclusively that the court marks the end of open source release:

只是当 Neo4j 完全转为商业许可时，法院才标志着开源发布的结束。

> In November 2018, Plaintiffs released Neo4j EE version 3.5 under a commercial license only. From that point on, Plaintiffs were no longer providing Neo4j EE on an open source basis.

> 2018 年 11 月，原告仅在商业许可下发布了 Neo4j EE 3.5 版本。从那时起，原告不再以开放源代码的方式提供 Neo4j EE。

Is the real headline here "Federal Court Holds AGPL Plus Commons Clause is Open Source"? Hell, no. The court's language isn't deciding anything about what "open source" means globally. It's just reciting the framing of facts accepted by parties to this lawsuit. Within that framing, Neo4j under AGPLv3 plus Commons Clause was open source. It was removing the Commons Clause that made the problem, because that's how lawyers on both sides argued it. Maybe that's incongruous with the wider, parallel debate ongoing in industry. That debate didn't factor in court.

这里真正的标题是“联邦法院认为 AGPL 加上共享条款是开放源码”吗？见鬼，不是。法院的语言并没有对“开源”在全球范围内的含义做出任何决定。它只是回顾了这起诉讼中各方所接受的事实框架。在这个框架内，AGPLv3 和 Commons 条款下的 Neo4j 是开源的。移除共享条款才是问题所在，因为双方的律师都是这样争论的。也许这与工业界正在进行的更广泛的、平行的辩论不相协调。那场辩论在法庭上并不存在。

Trial courts don't care, of themselves, what "open source" means. They don't care about how you or I or OSI people feel about it. They won't waste scarce time they do not have entertaining definitional politics. They won't blow a well scoped lawsuit out into a sprawling debate about a marketing bauble. It's not their job to settle our mailing list scores.

审判法庭本身并不关心“开源”意味着什么。他们并不关心你、我或 OSI 的人对它的感受。他们不会浪费稀缺的时间来处理定义的政治问题。他们不会把一个范围很广的诉讼吹成一个关于营销小玩意的漫无边际的辩论。他们的工作不是解决我们的邮件列表的问题。

Trial courts deal with just as much detail as they need to get lawsuits resolved. Here, that meant grappling with the rather narrow question of whether AGPLv3 section 7, which allows removal of "additional restrictions", lets downstreamers remove Commons Clause. The trial court found that it does not. The appeals court didn't overturn that finding. This is a legal decision that could potential apply outside the specific context. And a pretty interesting one at that. On GPL interpretation. Not on what counts as "open source".

审判法庭在解决诉讼时需要处理尽可能多的细节。在这里，这意味着要处理一个相当狭窄的问题，即 AGPLv3 第 7 条允许删除“额外限制”，是否允许下游者删除 Commons 条款。初审法院认为它不允许。上诉法院并没有推翻这一结论。这是一个有可能在特定背景之外适用的法律决定。而且是一个相当有趣的决定。关于 GPL 的解释。而不是关于什么是“开放源码”。

Why, why, why does all this need to be said?

为什么，为什么，为什么需要说这一切呢？

Despite contrary evidence, hackers still take OSI as it presents itself—as a technocratic, dispassionate source of authoritative legal guidance "for the community". In their defense, that's how I took it, too, until I studied law and paid attention. "Activists" drive OSI. They hold the bullhorn. Lawyers—my colleagues—don't post things like this. They read court opinions carefully.

尽管有相反的证据，黑客们仍然认为 OSI 是一个技术官僚的、冷静的、“为社区”提供权威法律指导的来源。在他们的辩护中，我也是这样认为的，直到我学习法律并注意到。“积极分子”推动 OSI。他们拿着牛角号。律师--我的同事--不会发布这样的东西。他们仔细阅读法庭意见。

All of this takes me back to 2017. The ICO plague was rampant. Coin Center, the main booster mouthpiece, was hocking all manner of dubious posts on how securities regulations somehow did not apply to blockchain. They did apply, and lawyers said so. But people saw what they wanted to see, repeated what they wanted to hear, invoked the "magic words" they were told would protect them — "utility token!" — and got themselves and others into a lot of unnecessary trouble.

所有这些都让我回到了 2017 年。ICO 的瘟疫很猖獗。币安中心，这个主要的助推器喉舌，正在兜售各种可疑的帖子，说证券法规如何在某种程度上不适用于区块链。他们确实适用，律师也这么说。但人们看到了他们想看到的东西，重复了他们想听到的东西，引用了他们被告知会保护他们的“神奇词汇”--“实用代币！”--并使自己和其他人陷入了许多不必要的麻烦。

The boosters got what they wanted.

There was a cost, but they didn’t pay it.

Reader, beware.

推动者们得到了他们想要的东西。

这是有代价的，但他们没有付出代价。

读者们，请注意！