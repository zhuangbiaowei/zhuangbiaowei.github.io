﻿---
layout: post
title:  "Java社群该向Ruby on Rails学习些什么？"
date:   2014-04-26 08:58
categories: Thinking IT
tags: OpenSource
comments: true
---


软件开发者是分社群的，大多数时候都是按照语言来划分大的派别，门派不同的人，很少相互交流——跟那种用XXX的有什么好说的？越是这门语言足够的自给自足，越是懒得看别的语言的东西。作为一个次新兴语言，Java社群已经足够封闭了。自己内部热闹非凡，新技术、新名词、新战争、新领袖层出不穷，哪里有空去理会Java以外的世界？

可是最近的事情有点奇怪了，Java社群在非常热烈的讨论另外一个语言的项目“Ruby on Rails”！这是什么东西？

CSDN的Java频道出了一篇文章：“[最美的MVC,ORM方案原来在别处–Ruby on Rails](http://blog.csdn.net/calvinxiu/article/details/358390)”！

是不是很令人惊讶？这么长他人自己灭自己威风的事情，咱们Java社群的人可是从来没干过的。

我当时也看了这篇文章，第一反应就是无动于衷，我还跟同事讲：“现在年纪大了，早就没有学新语言的冲动了 Smile ”

后来呢？偶然的机会我下载了一份PDF，下载地址是：

[Ruby on Rails实践](http://bbs.csdn.net/topics/70342450)

然后就看起来了。

多好的介绍啊！简单，清晰，准确，有诱惑力！于是我下载了Ruby，One-Click就安装完成了，然后在DOS窗口下输入了一条命令：

gem install rails –remote

就安装了Ruby on Rails。

再输入一条命令：

rails mybook

就建立我的第一个Web应用项目。

再输入一条命令：

ruby mybook\script\server

就启动了WEB Server。在浏览器里，就看到了初始的Welcome页面！

再说两个数字：
一个Web Server需要8行代码。
一个CRUD需要1行代码。

我的浅尝到此为止，但是留下的印象确实无比深刻！

为什么Java社群里那么多开源项目，“成百上千的Framework”，没有一个有这么方便？注意，我只说方便！

方便才是硬道理！这个道理，Java社群里也有人懂的，比如Hibernate的作者Gavin King就说：“10分钟之内把Hibernate跑起来”。Good，但是，一个包含Hibernate的Web应用要跑起来，需要多少时间？

一个流行的架构“WebWork+Spring+Hibernate”，加在一起的一个最简单demo，需要多少时间才能跑起来？等等，还没有选定WebServer呢！

再有，为什么不是iBaits呢？为什么不是Pico呢？为什么不是Velocity呢？为什么不是……

有人也许会说：“ruby社群只是发展得比java晚，所以现在只有这么一个拿得出手的东西，咱们java的好东西太多了，所以选起来累一些。”

但是，问题在于，Java社群里的那么多好东西，怎么就没有一个有RoR那么方便呢？

java社群必须认真反思了！我们究竟在追求什么？
“美感”
“架构”
“灵活性”
“健壮性”
“先进性”
“规范性”
“设计模式”

那么“易学性”和“易用性”呢？难道我们开发新的框架，不是为了减少程序员的劳动吗？

看到人家做出来的东西，总感觉有不足之处，然后呢？
自己另外做一个。然后呢？还有人又做了第三个，第四个。。。。

其实我们不需要那么多“富有创意”的项目，只要有几个能用的，顺手的就好了。如何才能改变Java社群的这种现状呢？

思考中…

原文写于：2005年05月27日

后记：这就是我最早接触Ruby & Rails的记录了。至今未悔...
