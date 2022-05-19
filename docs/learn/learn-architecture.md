---
id: learn-architecture
title: Architecture
sidebar_label: Architecture
description: 了解Polkadot构造的关键组件。
keywords: [polkadot, 组件, 构造]
slug: ../learn-architecture
---
> 
> 原文链接：[https://wiki.polkadot.network/docs/learn-nft](https://wiki.polkadot.network/docs/learn-architecture) ，中文翻译：Sherise
> 
Polkadot是一个具有共享安全性和互用性的异构多链（Multichain）。

# 组件

## 中继链

中继链是Polkadot的中心链。Polkadot上所有的所有校验器都被标记在DOT的中继链上，并对中继链进行验证。中继链由为数不多的交易类型组成，这些交易类型包括与治理机制交互的方式、平行链拍卖和参与NPoS。中继链具有故意设置的最小化功能——例如，不支持智能合约。中继链的主要责任是协调整个系统，包括平行链；其他特定的工作则被委托给平行链，两者有不同的部署方式和功能。

## [平行链](learn-parachains.md) 和 [平行线程](learn-parathreads.md) 值槽

Polkadot可以支持多个执行值槽。这些值槽就像计算机处理器上的核心（例如，现代笔记本电脑的处理器可能有八个核心），这些核心中的每一个一次可以运行一个进程。Polkadot允许这些值槽使用平行链和平行进程这两种订阅模式。平行链有一个专门用于链条的值槽（核心），就像一个不断运行的进程。平行线程则是在一个组中共享值槽，因此更像是需要唤醒且运行频率较低的进程。

整个Polkadot网络中发生的大部分计算，会由被委托处理各种用例的特定平行链或平行线程实现。除了要求平行链必须能够生成被分配到的校验器实现验证的证明之外，Polkadot对平行链不做任何限制。这个证明验证了平行链的状态转换。部分平行链可能专用于特定的应用程序，而另一部分平行链可能专注于特定的功能，如智能合约、隐私或可扩展性；然而，其他平行链可能是试验性的架构，本质上不一定是区块链。

Polkadot提供许多方法，确保平行链在特定时间范围内的值槽。平行线程是线程池的一部分，这个池子共享值槽以及必胜的独立区块拍卖。平行线程和平行链具有相同的API，但它们之间的区别是基于经济层面上的：平行链需要在租赁值槽期间持有DOT，而平行线程则是按区块付费。平行线程可以变成平行链，反之亦然。

### [共享安全性](learn-security.md)

连接到Polkadot中继链的平行链们，都享有中继链的安全性。Polkadot在中继链和所有连接的平行链之间具有共享状态。如果由于某些原因，中继链必须状态回退，那么所有的平行链也将跟着回退。这是为了确保整个制度的有效性能持久存在，没有任何单独部分可以被入侵篡改。

共享状态，可以保证使用Polkadot平行链时的信任假设仅为中继链校验器集的信任假设，而不是其他假设。拥有大量押注的支持，中继链上的校验器理论上是安全的，平行链应该也会从这种安全性中受益。

## 互用性

### [跨共识消息格式（XCM）](learn-crosschain)

XCM是跨共识消息的简称，它是一种格式，而不是一种协议。格式不假定接收方或发送方的共识机制，它只关心消息必须采用的格式。XCM格式是平行链能够相互通信的方式。与XCMP（即“跨链消息传递协议”的缩写）不同的是，XCM是可被交付的成果，而XCMP是交付机制。了解更多关于XCM的知识，最好方法是阅读[规范](https://github.com/paritytech/xcm-format)。

### [区块链桥](learn-bridges.md)

区块链桥，是一种允许任意数据从一个网络传输到另一个网络的连接方式。各种链可以通过区块链桥进行互操作，但也可以作为具有不同协议、规则和治理模型的独立链存在。在Polkadot中，区块链桥可连接到中继链，并通过由[排序器](#collators)维护的Polkadot共识机制进行保护。

通过区块链桥，Polkadot可以连接Web 3.0的未来，因为作为隔离状态链[安全稳健]的通信渠道，区块链桥是Polkadot互操作性体系结构的基础。

# 主要角色

## 校验器（Validators）

如果[校验器](../general/glossary.md#validator)被选入校验集，则会在中继链上产生区块。它们也接受来自校验器的有效状态转换的证据；作为回报，它们将获得押注奖励。

## 提名器（Nominators）

[提名器](../general/glossary.md#nominator)将它们的押注绑定到特定的校验器上，以帮助押注进入激活状态下的验证器集，从而为链生成区块。作为回报，提名器通常会从校验器那里获得一部分押注奖励。

## 排序器（Collators）

[排序器](../general/glossary.md#collator)是平行链和中继链上的完整节点。他们收集平行链事务，并为中继链上的校验器生成状态转换证明。它们还可以使用XCMP发送和接收来自其他平行链的消息。

---

## 白板系列

有关Polkadot架构的视频讲解，请参考W3F研究员阿利斯泰尔·斯图尔特的白板采访视频：

<iframe width="560" height="315" src="https://www.youtube.com/embed/xBfC6uTjvbM" frameBorder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowFullScreen></iframe>
