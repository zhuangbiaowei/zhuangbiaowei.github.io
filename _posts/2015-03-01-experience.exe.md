---
layout: post
title:  "experience.exe"
date:   2015-03-01 22:38
categories: Thinking IT
tags: Cloud
comments: true
---

一个只有程序员才能立刻理解的笑话：「中国的法律是txt格式的，西方的法律是exe格式的。」当然，这个笑话相当片面（废话），但是却可以成一个很好的引子，引出今天的话题：「什么才算是可以被执行的经验？」

## 一、先来谈谈，什么样的经验是txt格式的

在stackoverflow，有大量的问题，是这种格式：「在XX平台上，我想跑XX和XX和XX，怎么搞？」、或者「我在安装/运行XX的时候，系统报错，说是找不到XX，怎么办？」

这些问题，通常有其他老手已经碰到过了。于是，有某个好心人，在下面答复一番，读到这段说明的新手，再照此操作一番。

如果顺利的话，自然就OK了。如果搞出其他的问题，只怕还要再来追加提问。

## 二、再来谈谈，什么样的经验是可执行的

所有的开源项目，都包含了宝贵的经验，而且一旦编译(动态语言只需要配置一下)成功，就是可执行的了。

当然，编译与配置，同样需要经验。configure脚本与Makefile、Rake脚本，就是这种编译类经验的可执行版本。而Gemfile、requirement.txt、package.json之类的文件则是配置类经验的可执行版本。

这些当然都是极好的，但是却又远远不够。我们依然需要阅读install文档，依然有各种坑需要去踩。

## 三、曾经的一个设想：dependency.io

大概在去年6~7月份的时候，我曾经有过一个设想，主要也是受到了brew的启发：如果有某种机制，能够解决任意平台、任意语言、任意情况下的各种依赖问题，那应该可以大大的解放开发者吧。如果每个人都能够将自己的一点经验分享出来，再汇集到一起，世界一定会变得更加美好吧。

但是，在略微思考之后，就发现要解决这个问题，实在是太复杂了。
* 一个系统要正常运行，考虑到不同的操作系统、平台与版本，需要正确的配置一堆组件
* 一个组件需要考虑其版本、依赖平台以及获取方式，还有它所要依赖的其他组件
* 最简单的办法自然是apt-get，但是有时候必须考虑从源代码编译，甚至在特定平台版本之下，需要打上某些patch，才能正确编译
* 也许在某个平台下，就是无法编译、安装成功的，这个在知识库里也应该有「结论」
* 在一切都已经在我的机器上安装完成之后，还需要正确的配置，将他们组合起来
* 如果在我的机器里，需要并存一个组件的几个不同版本，如何避开冲突，也是一场噩梦
* 以上的这一切，需要一个层层递进的依赖关系，以及一个足够灵活的数据格式

最后，我放弃了这个项目！当然，类似的事情，还有人一直在做：[Chef & Cookbook](https://supermarket.chef.io/cookbooks-directory)

## 四、重型的解决方案

在我们的项目组里，有一个非常笨重，但却有效的办法：派一位「死士」先在一台干净的虚拟机上，把所有的依赖问题解决，完成各种配置，最后将虚拟机复制N份，给每个开发人员使用。

多年以前的vagrant+box+virtualbox，其实就是这样一种方案的略微方便一些的版本。

为什么说这样的方案是「重型」的？虚拟机的大小是几百M；启动时间至少几十秒；一台虚拟机至少占用几百M甚至几个G的内存；当然还有高昂的CPU计算资源消耗；如果这一切都仅仅是为了解决复杂的依赖关系，那也太奢侈了。

## 五、容器——一个足够好的折中方案

基于容器，我们可以获得一个个基本上近似于干净、相互隔离的「操作系统」，在此基础上的配置与依赖关系，可以通过足够简单的方式来描述。

而另一方面，由于容器的大小、启动时间、占用内存、消耗CPU都大大的低于基于虚拟机的重型方案，这就使得在一台机器上，同时启动成百上千个容器实例，也不在话下。

这种优势对于运维的好处先按下不表，这里先讨论其对于经验梳理的意义：原本在一台虚拟机里，我们需要配置N个不同的组件，以及组件之间的相关配置，要将其组成在一起，使其能够顺利工作，复杂度是惊人的。现在，我们可以将工作分为两部分：每个组件的依赖描述，以及组件之间的组合配置关系。

举一个简单的例子：[cookbook gitlab](https://github.com/atomic-penguin/cookbook-gitlab) 与 [docker gitlab](https://github.com/sameersbn/docker-gitlab)

这两个项目，就是两种不同思路与技术平台的产物，同样是为了描述「安装并运行Gitlab」的经验，复杂度大概会相差10倍。在docker模式下，我们只需要阅读Dockerfile与fig.yml两个文件，大约50+行，就能够搞明白了。而在Chef模式下，我们至少得阅读recipes目录下的三个文件，大约500+行吧......

另外一件docker做得特别靠谱的事情，是建立了简单好用的[Docker Hub](https://registry.hub.docker.com/)，这使得创建、分享、学习各种经验，变得更加容易了。

### 题外话

另外一个值得关注的社区，是[wercker](http://wercker.com/)，这个社区也在以[boxes](https://app.wercker.com/#explore/boxes)与[steps](https://app.wercker.com/#explore/steps)的方式，在努力构造更加容易分享和执行的经验。 

## 六、从经验描述的角度来看dockerfile与fig.yml

如果扯远一点的话，我们可以看到几种不同的描述经验的格式，广义的来看，无非是某种DSL而已。

* 顺序执行式：当我需要做一些事情，按照顺序1，2，3这样做下去。
* 加上IF/ELSE/FOR/WHILE的顺序执行式：在顺序执行的基础上，做一些条件与分支判断，通过循环在减少一些重复代码，然后就差不多了。
* Makefile/Rake风格：一件事情，可以分解为多个task，每个task可能存在前置依赖的task，整个任务可以被分解为层层依赖的一堆task。
* Config/YAML/XML风格：这是较为死板的一种模式，甚至几乎称不上是描述经验的DSL，而是将各种配置参数，以较为方便阅读的格式写出来而已。

目前的Dockerfile，与fig.yml（升级为docker compose之后，变成docker-compose.yml了），可以说都相当简陋。缺乏许多重要的特性。目前只能算是堪堪够用，却远不能称之为好用。

* docker build无法带参数，一个Dockerfile只能build出一个结果。假设两个非常接近的image，我也只能写两Dockerfile；
* docker compose同样无法带参数，我不能使用同一个yml配置文件，或者启动developement模式、或者启动production模式；
* 构造容器与组件的很多经验，实际上需要写在这两个文件之外，以某种魔法的形式，在不知不觉中被引入容器；

## 七、针对未来的一些猜想

* 在dockerfile与fig.yml复杂起来之后，新一轮的DRY式改良，应该会再次出现，函数、参数、模板、include之类的语法也可能会被引入。
* 如果我们将dockerfile看做是一个用来build docker镜像的底层脚本，说不定可以创造某种更加高级的DSL，用来编译生成出最终的Dockerfile。
* 如果将来容器大行其道，可以被执行的经验越来越多，分享与交流经验的社区越做yue好，只怕stackoverflow，会渐渐的衰落吧。
