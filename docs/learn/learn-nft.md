> 原文链接：https://wiki.polkadot.network/docs/learn-nft
> 
> 翻译：Sherise

---
id: learn-nft
title: NFTs
sidebar_label: NFTs
description: 对Polkadot生态系统中NFT场景的解释。
keywords: [NFT, 不可替代代币, NFT 2.0]
slug: ../learn-nft
---

本页是对NFT以及波卡网络中各种NFT方法的总览。

**预见混乱（Expect Chaos）。**

## 可替代性

NFT意为*不可替代代币*。可替代性，指的是组织内部的互换能力。从理论上讲，一张20美元的钞票在商店里总是值20美元，而且与任何其他20美元纸币的价值相当。然而，它不能与1美元或100美元的钞票(在组织之外)互换。

这就好比宝可梦的喷火龙卡牌不可与杰尼龟卡牌进行互换，但是不同版本的喷火龙卡牌之间是可以互换的。

可替代性是一种范围——对一部分人来说可以替代的东西，对其他人可能就不是。现实中，宝可梦卡牌是不可替代资产的典型例子，它比美元钞票更具可互换性，因为钞票都有一个可能对政府机构很重要的唯一序列号。但宝可梦卡牌并没有序列号[1]。

![](<https://www.investopedia.com/thmb/Nr-RLORu5CX_lIWZfLmV5X0eIrc=/613x345/smart/filters:no_upscale()/Clipboard01-d20f6eb9351e4f36a46e11fd87b53b2d.jpg>)

此外，如果玩家只是在乎角色的外观，那么游戏中像紫色魔剑这样的数字道具，或许可以置换另一把外观相似的剑。但如果另一把剑有不同的功能，并且会影响玩家即将开启的冒险的结果的话，那么外观相似的剑绝对是不可替换的。

考虑到这一点，对NFT最简单的解释是，**NFT是一系列任意的、基于项目的、不可互换的数据，可以通过加密的方式证明属于某人**。这些数据可以是任何东西，例如演唱会门票、出席证明、简单的词汇、虚拟化身、虚拟世界中的地块、音频剪辑、房屋契约、抵押贷款等等。

---

## NFT标准

通用区块链，本质并不是为了阐释NFT的概念而构建的。它只是对自己的原生代币有天然的感知，并持续优化；但是建立在链上这样的实现，本质上是一种 "侵入"。

例如，以太坊是一个通用区块链，它没有内置“代币”(可替换或不可替换)的概念。以太坊中的代币，本质上是由各种用户界面以*特定方式*解释和读取的信息电子表格。这样的阅读方式被称为*标准*。

可能您听的最多的可替代代币标准是ERC20，而最广泛的NFT标准是ERC721，紧随其后的是ERC1155。必须定义这些标准的缺点是，它们总是指示如何以某种方式阅读电子表格，假装以某种方式提供信息，但根据定义，这种方式不能被优化。因此，即使在网络通畅的好日子里，与任何EVM链上的NFT进行交互也会花费几美元；但在2021年，以太坊上每次交互（转移、造币、出售）的平均成本约为100美元。

这可以防止超出当前以太坊上*收集数字灰尘类NFT*热潮的案例——例如个人资料照片，“看一次然后被丢弃”的生成艺术，[ENS](ens)地址以及[出勤证明徽章](https://poap.xyz/)等。

#### 典型的 [以太坊上的NFT](https://opensea.io/assets/0x2127fe7ffce4380459cced92f2d4793f3af094a4/12598)

![](../assets/nft/samurai.png)

为了便于比较，我们可以将这些称为NFT 1.0：静态NFT，几乎完全是基于图像的收藏品，稀有程度各不相同。

---

## NFTs 2.0：Polkadot和Kusama的NFT

这是Polkadot的技术闪耀之处，也是NFTs 2.0发挥作用的地方。

通过允许[异构的特定分片](learn-parachains.md)存在 ，构建者可以针对复杂的NFT用例进行原生优化，而无需权衡在其他环境与系统交互时低下的效率及高昂的代价。

在Polkadot生态系统中，存在以下NFT解决方案，并正在开发中：

### 独特网络（Unique Network）

[独特网络（Unique Network）](https://unique.network/)，是NFT特定的区块链，提供创新功能如：赞助交易，捆绑可替代代币与不可替代代币，以及为获得部分所有权将NFT拆分为可替换代币。

到目前为止，独特网络（Unique Network）已经推出了两个NFT项目：作为[Hackusama](https://hackusama.devpost.com/)的一部分的SubstRapunks，以及最近在[Polkadot Decoded](https://decoded.polkadot.network/)期间作为一项推广活动的Cherobricks。他们目前正在运营与Kusama相连的betanet，这些NFT已经可以在上面交易。

#### 来自[Unqnft.io](https://unqnft.io)的NFT [2]

![](https://unique.network/local/templates/unique/static/images/content/chel-400.jpg)


用户可以将KSM发送到他们的独特网络（Unique Network）托管帐户，在那里进行交易，然后将赚取或剩余的KSM发回。

独特网络（Unique Network）旨在使他们的市场技术具有开源性和白标友好性。从理论上讲，使用Unique的技术，可以为您的项目轻松建立一个新的市场。独特网络（Unique Network）的目标是成为Polkadot上的平行链，而Quartz是他们在Kusama的对手。

*独特网络（Unique Network）与RMRK密切合作（见下文）。*

### RMRK

[RMRK](https://rmrk.app)是一种“侵入”，是在Kusama中继链之上的强制标准。由于Kusama旨在轻量级地处理与其连接的各种平行链，因此它没有任何其他类似原生NFT或智能合约的复杂链逻辑。然而，由于市场需求和Kusama的“混乱”性质，RMRK团队决定采用比特币的[“染色币(colored coins)”](https://en.bitcoin.it/wiki/Colored_Coins)方法，在Kusama链上实现NFT涂鸦。

RMRK标准是一套用于解释Kusama上称为“备注（remarks）”的特殊涂鸦的规则范式，它可通过任何Substrate链中的核心`系统` pallet进行访问。

RMRK团队刚刚发布了该协议的2.0版本，这是一套“NFT乐高（NFT legos）”基础组件，当它们组合在一起时，允许构建者在没有智能合约的情况下构建任意复杂的NFT系统。


#### NFT乐高

1. NFT可以拥有其他NFT，NFT可以装配其他NFT进行视觉变化
2. NFT可以（根据环境和资源优先级）拥有多个资源
3. NFT在发现价格和社会机制时，可以产生链上表情（情绪反应）
4. NFT有条件渲染（例如，如果蒙娜丽莎得到50个😘亲吻表情符号，她就会脸红）
5. NFT可以由社区通过可替代的持有者代币（NFT的细分）进行管理

即将到来的的3.0版本（于2022年第一季度发布），将是融合所有RMRK 2.0逻辑的pallet和智能合约（EVM）版本；它会集成到合作伙伴链中，并可在数十个链中低价且轻松地传送不可替代代币。

#### 来自[Kanaria](https://kanaria.rmrk.app)的NFT

![](../assets/nft/kanaria.png)

```note 多资源型NFT

多资源型NFT（GIF的状态，和SVG组合型动态NFT可合二为一）也可从它的“库存”中装备其他NFT。

```

RMRK团队正在与独特网络（Unique Network）密切合作。RMRK的逻辑和技术将以runtime升级（FRAME pallets）的形式部署在唯一网络上。

基于RMRK的NFT有以下两个市场，在其中已有数百个项目启动：

- [Singular](https://singular.rmrk.app)，官方市场
- [Kodadot](https://kodadot.xyz)，第三方市场

此外，可以在[Kanaria](https://kanaria.rmrk.app)平台上访问和测试具有可组合、嵌套、多资源NFT的RMRK 2.0功能。

有关RMRK的完整介绍，详见[RMRK的视频解说](https://url.rmrk.app/rmrkcc)，[Kanaria(RMRK 2)的视频解说](https://url.rmrk.app/kanariacc)，以及[说明文档](https://docs.rmrk.app)。

### 无限性

作为以太坊ERC1155标准的作者以及Enjin Wallet和Unity插件的创造者，[Enjin](https://enjin.io)领头实现了NFT在3D游戏中的轻松部署。Efinity是一个NFT桥接链，将于2022年在Kusama和Polkadot上线。

他们计划建立一个*平行代币*，这不仅将成为Polkadot生态系统中不同平行链之间代币迁移的标准，也将成为进出Etherum和其他EVM系统的标准。

### Moonbeam

[Moonbeam](https://moonbeam.network)和在Kusama上与之对应的MoonRiver，都是使用Etherum RPC端点的完整EVM部署。

这意味着提供给其他EVM链的整个工具包(如HardHat、Remix、Truffle、MetamASK等堆栈)可供MoonRiver/MoonBeam用户和开发人员使用，这使其在吸引现有用户群方面有明显的领先优势。

数十个备受瞩目的团队正在Moonriver/Moonbeam上推出（或重新推出）他们的产品，然而，必须注意的是，Moonbeam是EVM链，因此在NFT的定制化和功能丰富性方面将受到与任何其他EVM链相同的限制。

然而，一个值得注意的优势是，MoonRiver/MoonBeam仍然是Substrate链，这意味着仍然可以将定制pallet集成到runtime中，使链runtime层面的NFT特定优化成一种可靠方法，以保持工具的EVM兼容性，同时优化丰富NFT的存储和交互。

### Uniques

Uniques是部署在公共利益平行链Statemint上的[FRAME pallet](https://github.com/paritytech/substrate/tree/master/frame/uniques)。它实现了最基本的NFT类型——引用一些元数据的数据记录。这些元数据的引用在冻结之前是可变的，因此NFT及其类别（派生的实体）是可变的，除非发行者特别说明是不可变的。

Uniques故意采取了一种非常简单的方法，使Statemint链成为可替代和不可替代间的简单持衡链。

可以在[RMRK的Single Platform](https://singular.rmrk.app)上，将右上角菜单从Kusama切换到Statemine，查看Uniques NFT并与之交互。

![](../assets/nft/nft-statemine.png)

还可以通过[Statemine的Extrinsics选项卡](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fkusama-statemine-rpc.paritytech.net#/extrinsics)直接与交互：

![](../assets/nft/uniques.png)

**更多的用户界面已经在开发中**。

---

## 桥接

桥接Substrate链和EVM链需要付出很大的努力，但这是NFT行业非常需要的功能。合并收集者和客户群具有重要意义，因此多个项目都致力于实现这一点。

除了RMRK（使用[XCMP](learn-cross-consensus.md)原生的Substrate到Substrate的无缝远程传输）和Efinity（平行代币）外，还有以下工作正在进行中：

- **MyNFT**: 一个EVM到EVM的桥接工作。
- **RMRK <-> EVM** 简化桥: 在RMRK黑客马拉松期间开发的桥，用于将[RMRK hackathon](https://rmrk.devpost.com)移植到EVM链上的简化IOU中，主要部署将于2022年11月在MoonRiver上进行。
- **RMRK <-> EVM** 完整桥:EVM版本的 RMRK 2.0 应在2021年12月准备就绪，这意味着完全迁移 RMRK 2.0 NFT 从  RMRK（Kusama）到 MoonRiver（和其他EVM）将成为可能。

### 参考

- [1]: [Investopedia](https://www.investopedia.com/terms/l/liars-poker.asp)；
- [2]: [Unique Network's Chelobrick](https://unique.network/blog/chelobricks-making-waves-with-10-000-substrate-based-nfts/)
