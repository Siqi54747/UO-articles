---
title: Celestia：模块化区块链的星辰大海
publish_date: '2022-09-30'
publish_timestamp: 1664535627
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/GR-24AZ7a0XmlRC8ZFR38Q
msgid: 1000000127
appmsgid: 2247496661
itemidx: 1
digest: 模块化区块链可能是通往多链世界的最佳路径。
cover: https://mmbiz.qpic.cn/mmbiz_jpg/3tHNibnJ2jgzrtnyfic2Xfw0DlCmGt556iaSMVxQunk0ib2fcUpD6iaMad63NH2QjuMOibRlXXaVKT7G9G7GRd3yic97g/0?wx_fmt=jpeg
image_count: 45
archived_at: '2026-04-19T23:34:59+08:00'
---

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/001.gif)

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/002.png)

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/003.png)

**作者：Jessie**

**排版：Elena**

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/004.png)

单体区块链需要每个节点执行每笔交易，其本质上是不可扩展的。因此，多链世界不可避免，我们认为模块化区块链（modular blockchain）可能是通往多链世界的最佳路径。

**Celestia 是第一个真正的模块化区块链，其愿景是将 Cosmos 的主权互操作区域（zones）和以 rollup 为中心的以太坊结合起来，共享安全性。**它通过将执行与共识分开，并引入数据可用性采样（data availability sampling）来进行扩展，有望支持更广阔的潜在用户需求，同时保持验证的成本相对稳定，为用户带来更好的性能。

如果将区块链重新想象成一个模块化的堆栈，那么 Celestia 的意义不止于可扩展性。它的独特优势包括信任最小化的桥、主权 rollup、有效的资源定价、更简单的治理、更轻松的链上部署、灵活的虚拟机等等。

**Celestia 向主权 rollup 提供数据可用性与共识安全服务，它将自己比作“区块链领域的 AWS”，其收入来源也主要依赖于主权 rollup 支付的服务费用，以及部分 MEV。不过我们也不无疑虑：其价格更加低廉的区块服务究竟能为 Celestia 带来多少利润？毕竟这类 toB 业务也很难产生网络效应。**

另外，虽然 Celestia 有模块化区块链领域最强悍的创始团队，但以太坊分片计划，即 Danksharding 也计划拆分出单独的数据可用性层，新兴的 Celestia 终究难以与经过千锤百炼的以太坊匹敌。

不过我们相信，**未来的区块链世界将会呈现“一超多强”的局面**，以太坊绝不可能是区块链世界中唯一的模块化区块链，Celestia 仍旧是一个值得期待的玩家，**作为第一个专门的 DA 层，Celestia 比其他公链做的更少，但也许获得的更多。**

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 背景：区块链的模块化趋势

02 团队与资本支持

03 Celestia 的工作原理：解耦执行

04 Celestia 如何扩展？

05 Celestia 可以带来多大的扩展性？

06 Celestia 的优势

07 Celestia 的商业模式

08 市场竞争与路线图

09 未来的挑战

**01.**

**背景：区块链的模块化趋势**

如果我们把一条公链比喻成一家餐厅，那么毫无疑问，原始的以太坊就像一个既要烧菜、又要传菜、还要收银和打扫卫生的“全能选手”——它提供了一个统一的 DA、共识、结算和执行层。然而即便该“全能选手”再能干，随着来用餐的顾客越来越多，餐厅也会不堪重负，能服务的顾客始终很有限。

面对这样的困境，明智的餐厅老板都会选择再雇佣新的雇员，帮助分担一部分职能，因而有了 **Layer2 —— rollup 进行执行，以太坊负责 DA、共识和结算，从而减轻以太坊的负担。由此，我们看到了区块链呈现模块化的趋势，就像一家顾客越来越多的餐厅，也必须有厨师、服务员、收银员、清洁工等多种角色。而一条公链可以分为以下四个模块：**

- 数据可用性（DA）—— 确保 rollup 区块头后面的交易数据已经被发布，并且可供使用，以便任何人都可以重新创建状态
- 共识 —— 至少就交易及其排序达成共识
- 结算 —— 验证/仲裁证明和协调跨链资产转移、信息传递
- 执行 —— 确定哪些交易是有效的，并更新链上状态

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/005.png)

除了以太坊 rollups，以太坊分片、Cosmos Zones、Polkadot Parachains、Avalanche Subnets、Near's Chunks 和 Algorand Co-Chains 都是模块化区块链的探索实践，但这些模块化设计在如何处理**跨模块的安全方面**有很大不同：像 Avalanche、Cosmos 和 Algorand 这样的 Multi-chain hubs 最适合自身独立的模块确保安全性，而 Ethereum、Polkadot、Near 和 Celestia 这样的模块则采用共享（shared）或继承（inherit）的方式确保安全。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/006.png)

**目前最具吸引力的是以太坊和 Cosmos 生态。**以太坊设想了一个以 rollup 为中心的未来，虽然 rollup 比 Layer1 灵活性更低，但它们可以彼此共享安全性。而 Cosmos 是由一群应用于特定程序的 zones 组成的区块链互联网，比 rollups 更便宜、更灵活，但它们不能完全共享安全性，有些安全性不好的链很可能被篡改交易历史。这时，需要共享安全性来避免这种情况。

**如果我们既想要保持灵活性与低成本，又想要可靠的安全性，如何兼得呢？**创新者 Celestia 横空出世，它结合了这两个生态的精华，**将 Cosmos 的主权互操作区域（zones）与以 rollup 为中心、并共享安全性的以太坊结合起来，使用 Celestia 作为数据可用性层，无法被篡改和重组，所有交易的历史都被记录在 Celestia 的区块中。**

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/007.png)

为了便于我们理解 **DA（即 data availability，数据可用性）**，我们可以做这样一个类比，你往 Google Drive 上传了一张照片，第二天，你想把这张照片给朋友看。你问 Google：“你能给我看看我昨天上传的照片吗？”

如果 Google 回答说：“我可以使用它，我可以给你看那张照片。”然后只是给你发送一张从照片上剪下来的脸作为证明。你一定会觉得很困惑，你想要下载你的照片，而不是从 Google 那里证明他们有你的照片。

**这个在生活中近乎“荒诞”的场景，恰恰可以生动地阐释数据可用性层执行的核心功能。**我们只是想要看到那张脸作为证明，证明链上数据是可用的，并不想从 DA 层那里下载所有的数据。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/008.png)

**02.**

**团队与资本支持**

**团队介绍**

Celestia 团队背景相当亮眼，由优秀的区块链扩容领域的学者、研究人员和工程师组成，此前在区块链扩容领域均有着丰富的工作或创业经验。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/009.png)

CEO Mustafa 是伦敦大学计算机科学的博士，专业研究区块链扩容问题。他曾联合创立了区块链扩容平台 Chainspace，后被 Facebook 收购。他也是欺诈证明的发明者，曾于 2018 年作为第一作者与 Vitalik 发表论文《欺诈与数据可用性证明》。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/010.png)

CTO Ismail 曾在 Tendermint（Cosmos 母公司）、Interchain Foundation、Google 等公司担任软件工程师，具有丰富的区块链技术经验。CRO John 是多伦多大学计算机工程的博士，曾担任 ConsenSys 的研究员和工程师，后来联合创立了 Optimistic Rollup 解决方案 Fuel Labs。COO Nick 拥有斯坦福大学的硕士学位，此前曾是公链 Harmony 的联合创始人。

其顾问团队的阵容也相当豪华，包括 IBC 的联合创始人 **Zaki Manian，Tendermint 的联合创始人和 Cosmos 的联合创始人 Ethan Buchman 等**。

不过存在一个值得质疑的点是，CRO John Adler 还是他联合创立的 Fuel Labs 的核心贡献者，并致力于将其转型为模块化区块链的执行层，**虽然和 Celestia 可能存在业务联动，但我们仍不免担忧，这对于 Celestia 的创业是否是严重的分心**。

**融资情况**

2021 年 3 月，Celestia 完成 150 万美元的种子轮融资，由 Binance Labs 领投，其他投资方有：Interchain Foundation、Maven 11、KR1、Signature Ventures、Divergence Ventures、Dokia Capital、P2P Capital、Tokonomy、Cryptium Labs、Michael Ng、Simon Johnson、Michael Youssefmir 和 Ramsey Khoury。

**2021 年 12 月，团队又融资 273 万美元。据市场信息，Celestia 的估值迄今至少达 20 亿美金。暂时并未发行代币。**

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/011.png)

**03.**

**Celestia 的工作原理：解耦执行**

Celestia 会接收到来自它之上的主权 rollup 打包的交易，并通过共识协议 Tendermint 来排序交易。**与其他区块链不同的是，Celestia 不会质疑这些交易的有效性，也不负责执行它们**。Celestia “平等”对待所有交易，只要交易支付了必要的费用，它就会接受这些交易，将它们排序并在链上广播。

💡

注 1：根据 Celestia Blog，如果一个 rollup 有自己的结算层来决定分叉的规范链和交易的有效性规则，那么该 rollup 就是主权的。

注 2:有效性用于确定哪些交易是有效的，而共识使节点就有效交易的顺序达成一致。

而在 Celestia 之上的主权 rollup 可以通过 Merkle 证明，验证 rollup 传过来的交易数据在 Celestia 的数据可用性层已经被打包和排序。主权 rollup 节点会执行交易来计算他们的状态（例如，确定每个人的账户余额），**如果有任何交易被 rollup 节点认为是无效的，则不会处理这些交易。**

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/012.png)

只要 Celestia 的历史保持不变，运行相同有效性规则的 rollup 节点就可以计算出相同的状态，主权 rollups 所需的，只是这些经过排序的交易及其共享的历史已经达成共识。

**04.**

**Celestia 如何扩展？**

解耦执行的明显优势在于，不需要每个人都执行所有交易，节点可以自由执行与其 app 相关的交易。例如，游戏 app 的节点不必执行与 DeFi app 相关的交易。

**尽管如此，解耦执行的可扩展性优势仍然有限，因为它们牺牲了可组合性**。假如两个 app 想要相互交换一些 token，就需要计算两个 app 的状态，节点必须执行与两者相关的交易。事实上，随着新 app 加入这些交互，要执行的交易数量一定会增加。如果所有 apps 都想相互交互，我们将回到单体链（monolithic chain），每个人都要下载并执行所有交易。

那么 Celestia 如何实现无可匹敌的可扩展性，将执行与共识解耦与可扩展性又有什么关系呢？

**可扩展性瓶颈**

**可扩展性通常被描述为“增加交易数量而不增加验证链的成本”**。为了了解可扩展性瓶颈在哪里，我们简要回顾一下区块链是如何得到验证的。

在一条区块链中，共识节点（验证者、矿工等）生成区块，然后向全网广播。全节点通过下载和执行其中的所有交易来验证交易，相比之下，由于用于搭建轻节点的设备性能一般比较差，轻节点（99% 的用户）无法验证这些区块的交易，而只能跟踪区块头（区块中包含的数据摘要）。因此，轻节点的安全保障要比全节点低得多，它们默认共识是诚实的，但显然这不可能。

**而性能更好的全节点会对整个区块中的交易进行验证，恶意共识无法欺骗全节点接受无效区块**，因为它们会注意到无效的交易（例如用于双花的 tx 或无效的 mint），停止跟随该条链。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/013.png)

区块链领域的可扩展性瓶颈被称为**状态膨胀（state bloat）**。随着更多交易的发生，区块链的状态（执行交易所需的信息）会增长，对带宽以及计算力要求也越大，对节点性能要求增加，也就导致符合条件的节点越来越少，**少数全节点成了网络的中心，全节点串通作恶的可能性变大，给网络带来中心化风险，安全性变差。**

**由于大多数链都重视去中心化，因此他们希望全节点能在消费级硬件上运行，所以会控制区块/ gas 的大小来限制其状态增长的速度，这就是造成区块链可扩展性瓶颈的原因。**

**欺诈证明和有效性证明**

**欺诈/有效性证明的发明打破了这一可扩展性瓶颈**，它们让轻节点可以验证区块中的交易是有效的，具备与全节点几乎相同的安全保证，同时消耗更少的资源。

下面是一个简化的欺诈证明示例。在欺诈证明中，全节点为轻节点提供足够的数据，以便它们自主识别无效交易，该证明的第一步要求全节点向轻节点显示，特定数据（例如，声称无效的 tx）属于某一个区块体（block body）。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/014.png)

通过使用 Merkle Tree，全节点可以向轻节点证明特定交易包含在块中，而无需他们下载整个区块的内容。

然而，虽然证明**包含 tx** 很容易，但证明 **tx 不存在**则很难。**麻烦的是，证明 tx 不存在与证明包含 tx 对于使欺诈/有效性证明有效运转，同样重要。**

**数据可用性问题**

**为了让全节点生成欺诈/有效性证明，它们必须能够计算状态 —— 账户余额、合约代码等**，这需要全节点来下载和执行所有交易。但是，如果恶意共识发布了区块头（block headers），但在区块体（block body）中扣押（withholds）了一些 tx 怎么办？

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/015.png)

在这样的攻击场景下，全节点很容易注意到区块体（body）中的数据丢失，因此拒绝跟随链。但是，仅下载区块头的轻节点将继续跟随它，因为它们不会注意到任何差异。

***数据可用性是欺诈证明和有效性证明的先决条件***

如果无法访问完整数据，诚实的全节点无法生成欺诈/有效性证明。**一旦发生了数据扣押攻击，轻节点却不会注意到问题所在，无意中和全节点分叉**。数据可用性问题是一个非常微妙的问题，因为**证明 tx 不存在的唯一方法是下载所有 tx**，这正是轻节点由于资源限制而做不到的事情。

**我们可以类比这样一个“暗室实验”**：如下图的漫画所示，一个黑暗的房间里有一个公告板。首先，区块生产者（block producer）进入房间，并在公告板上写了一些信息。然后作为验证者的你带着手电筒进入房间，手电筒的光束很窄，而且电量不足，所以你只能读懂公告板上极少数明显位置的文字。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/016.png)

你的任务是**确保该公告板上的信息是可用的**，这有些棘手，因为存在两种可能性：要么生产者表现诚实，写下完整的文件信息；要么生产者行为不端，遗漏了一些信息，使整个文件不可用。**但你的手电筒电量不足，无法检查公告板的每个位置，通过只在几个地方检查公告板，你无法区分前面所说的这两种情况，因此，你不能可靠地检查整个区块的数据可用性，我们需要一种新的方法。**

***Celestia 解决了数据可用性问题***

让我们看看 Celestia 如何解决这个问题，前文我们提到 Celestia 并不关心交易的有效性，它真正关心的是区块生产者是否已经完全发布了区块头（headers）背后的数据。

**使 Celestia 具有极强可扩展性的原因在于，这种可用性规则可以由资源有限的轻节点自主执行**，通过数据可用性抽样(data availability sampling）来完成。

**数据可用性抽样 (Data Availability Sampling，DAS)**

DAS 依赖于一种数据保护技术，称为纠删码（erasure coding）。由于对这种编码进行解码后，即便是非常小的数据碎片，仍旧可以从中恢复原始数据，所以只需要下载该区块的一小部分，就可以以非常高的概率检查出一个区块的所有数据是否已经发布。

**这里有一个非常简单的数学思考过程，如果你想理解 Celestia 的数据可用性抽样过程，请保持耐心，我保证，这部分内容的难度不会超过小学水平。**

纠删码对原始数据有不同的压缩比，这里我们假设压缩比为 2：1，假如有一个 1 MB 大小的区块，对其进行纠删编码后，将一个大的区块分成许多个小的 chunks，并将整个区块“扩展” 2 MB，其中额外的 1 MB 是特殊的数据。如果被编码后的区块中有任何字节丢失，由于纠删码的存在，你可以轻松恢复这些字节。即便有多达 1 MB 的区块数据丢失，你也可以恢复整个区块，但超过 1 MB，就无法再恢复整个区块。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/017.png)

**就像光盘遭遇一些划痕，仍旧可以完整读取内容，但是如果大面积损毁、超过一定比例，则无法正常播放影片。所以一个恶意生产者想使区块不可用，即便他只扣押了很少的数据，但被编码之后，也会变成扣押 50% 以上的 chunks***（至于为什么编码后就会变成扣押 50% 以上的 chunks，这里涉及复杂的多项式，不再展开，如果对这部分的数学原理感兴趣，欢迎加文末作者微信交流）*。

这就变得非常容易检测，因为网络中只可能有两种区块生产者，诚实的区块生产者和恶意的区块生产者。如果一个网络中，全是诚实的区块生产者，那么轻节点可以顺利下载所有的 chunks；如果网络中存在恶意的区块生产者，那么轻节点每次下载 chunks，至少有 50% 以上的概率会无法成功下载。**这也就意味着，一旦存在无法下载的 chunks，那么我们就可以判断，网络中存在恶意节点**。

现在假设这样一种情况，网络中存在恶意区块生产者，这也就意味着 50% 以上的 chunks 都无法下载。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/018.png)

轻节点对这些 chunks 进行随机抽样，第一次抽到可以下载的 chunk 概率会小于 50%，接着再抽样，连续两次抽到可以下载的 chunk 概率至多不会超过 ，连续三次抽到可以下载的 chunks 概率至多不会超过 **...... 无限随机抽样下去，可以一直抽到可以下载的 chunks 的概率至多不会超过  —— 而这个概率接近于 0，这也就意味着，在有恶意区块生产者的网络中，轻节点会错误认为整个区块数据可用的概率为 0。**

**好了，数学学习的部分到这里结束**，实际上，数据可用性证明的全部细节比这更复杂，并且依赖于其他的假设，比如对网络中轻节点的最小数量有要求，这样才能有足够的轻节点发出样本请求，从而共同恢复整个区块。

**“恢复”的过程很类似于我们常用的 BT（BitTorrent）种子下载**，BitTorrent 是最早的去中心化文件共享协议，不同的对等方拥有不同的文件片段，下载者将自己已有的文件信息分享给网络中其他人，并交换自己没有的部分，这种情况下，下载同一份文件的人越多，下载速度就越快。

**回到我们上面提及的暗室实验**：现在我们不要求区块生产者在公告板上写下原始文件，而是要求它把文件切成许多小的数据块，对它们进行纠删编码，并将被编码的数据块写到公告板上。

接下来，我们考虑这两种情况：要么生产者表现得很诚实，写下了所有的数据块；**要么生产者行为不端，想让文件不可用。**

所以，如果要让文件不可用，区块生产者也只能写下一部分的数据块，这也就意味着，大量的数据块将被丢失，**这样才能保证无法恢复至原始数据**。这会造成这样的结果——我们将会看到一个大半空缺的公告板。而一个数据可用的公告板，大部分位置都是满的。

**这种差异变得很容易区分**——你可以在公告板上进行随机抽样，只要发现一个数据块是空的，那么文件不可用，经过多次抽样检测，你会判断错误的概率趋近于 0。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/019.png)

总而言之，由于轻节点只需要采样少量尺寸极小的 chunks，就可以确认数据是否可用，如果检测到任何无效交易，特定的执行层就可以拒绝执行。但无效的交易数据仍旧会保存在 Celestia 上。

**05.**

**Celestia 可以带来多大的扩展性？**

关于可扩展性，有两个主要因素限制 Celestia 的 DA 吞吐量：

1. 可以采样多少数据
2. 轻节点采样的区块头大小

**首先来看第一个因素。采样的数据越多，就可以为更大的数据量提供可用性保证，但 Celestia 的数据可用性采样（DAS）使任何单个终端用户需要采样的数据量始终是一个可控的大小。虽然单个节点容量受限，但由于 DAS 可以由资源有限的终端用户执行，甚至智能手机也可以参与采样过程，因此，大量轻节点可以加入采样。**

而且 Celestia 只提供数据可用性而不做状态执行，所以区块产量（block production）可以更高，并且每个区块有更多的空间，区块变得更大、可以采样的数据更多、带来更高的 tps。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/020.png)

*Celestia 团队的当前估计*

**采样节点的数量**与用户需求有关，**Celestia 的区块空间供应是关于需求的函数**，这意味着， 与单体链不同，Celestia 可以**随着用户需求的增长提供低廉而稳定的费用**。

**接下来我们来看第二个因素，轻节点采样的区块头大小与区块大小的平方根成正比，区块头越大，对轻节点的带宽要求就越高**。因此，为了获得与全节点相同的安全性，轻节点需要付出 O(√n) 带宽成本，其中 n 是区块大小。虽然这可能看起来是一个限制因素，但随着时间的推移，增加的资源需求可能会被网络带宽的改进所抵消。

另外，**如果平均轻节点的带宽容量增长 X，Celestia 的 DA 吞吐量可以安全地增长 X^2**。而尼尔森的互联网带宽定律指出，互联网用户的带宽连接速度每 21 个月带宽速率将增长一倍。因此，Celestia 将大大受益于网络带宽的指数级改进，有望满足**潜在用户需求，同时保持验证成本相对稳定**。

**06.**

**Celestia 的优势**

模块化区块链的优势不止于可扩展性，我们接下来会介绍 Celestia 的 8 个独特优势，尽管短期内这些特性不一定能显著发挥出来。

***1.自主权（Self Sovereignty）***

目前的 rollups 就像以太坊的婴儿链（baby chains），他们将区块头发布在以太坊上，欺诈/有效性证明在链上执行，因此，它们的状态由以太坊上的一系列智能合约决定。

Celestia 上的 rollups 运作模式完全不同，它对其存储的数据没有任何感知，并将所有解释权和执行权留给 rollups，这些 rollups 就像是目前大多数 L1 区块链那样运行。

**因此，Celestia 上的 rollups 本质上是拥有自己主权的区块链。在 L1 区块链中，有争议的硬分叉通常被认为是非常危险的，因为分叉链最终会削弱其安全性。**因此，通常不惜一切代价避免分叉，从而扼杀创新性。

**Celestia 首次为 rollups 带来了分叉的能力，而无需担心安全性减弱。**这是因为所有分叉最终都将使用相同的 DA 层，不会放弃 Celestia 共识层的安全优势。想象一下，如果区块链从一开始就以这样的方式运行，比特币区块大小的争论或以太坊 DAO 分叉会变得多么顺利。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/021.jpg)

***2.灵活性***

Celestia 不做执行的特性也将加快 VM 领域的创新。随着 Starkware、LLVM、MoveVM、CosmWasm、FuelVM 的出现，我们相信 VMs 可以在执行的各个方面进行创新，支持的操作、数据库结构、交易格式、软件语言等，将更加适用于特定用例，并实现最佳性能。

***3.轻松部署***

**让区块链部署变得更容易一直是不变的趋势**。早期，没有 PoW 硬件就无法启动去中心化网络，最终通过引入 PoS 消除了瓶颈，成熟的开发者工具（如 Cosmos SDK）使发布新区块链变得更加容易。然而，尽管取得了进步，PoS 共识的成本仍然很高。而其他的创新者 Polkadot 平行链的部署成本很高，以太坊 rollups 的运营成本很高。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/022.png)

**Celestia 是这一趋势的下一个演变**。Celestia 团队正在使用 Optimint 的 Cosmos SDK 实施 ORU 规范。该工具支持部署任何链，无需开发人员担心共识的开销或昂贵的部署/运营费用，可以在几秒钟内部署新的链，用户从第一天起就可以安全地与它们交互。

***4.高效的资源定价***

以太坊计划在未来几年分阶段展开其分片计划，rollup 只能用这些数据分片来发布数据。随着基础层的数据容量增加，这自然会导致更便宜的 rollup 费用。然而，这并不意味着以太坊放弃其在 L1 上的状态执行环境。

要在以太坊上运行一个 rollup 节点，还必须执行与以太坊的 L1 有关的状态。然而，以太坊已经有一个“巨大”的状态，执行成本高昂。更糟糕的是，用于限制 L1 状态大小的 gas fee 也用于计算 rollups 的历史数据。因此，只要 L1 上出现活动高峰，所有 rollups 的费用都会随之增加。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/023.png)

而在 Celestia 中，状态增长和历史数据被完全分开处理。Celestia 的区块空间只存储历史 rollup 数据，这些数据以字节为单位进行结算，所有状态执行都由它们自己独立单元中的 rollups 计量。由于活动受制于不同的费用市场，一个执行环境中的活动高峰不会破坏另一个执行环境中的用户体验。

举个例子，如果一个 Celestia 版本的 ENS 只是想要一个结算证明和转移代币的地方，它不需要将证明发布到一个通用的执行环境、并为之支付过多成本，无需与通用执行环境中的 DeFi 项目竞争却无法捕获任何价值。

***5.信任最小化的桥***

从广义上讲，桥有两种形式，受信任的桥（trusted bridges）和信任最小化的桥（trust minimized bridges）。**信任最小化的桥更加安全，但条件也更为严苛，需要：**

1. 相同的 DA 保证
2. 一种解释彼此欺诈/有效性证明的方式

常见的 L1 之间不满足“共享 DA”这一条件，所以它们之间不能形成信任最小化的桥。他们依靠彼此的共识进行通信，这必然意味着降低安全性。而 Celestia 与以太坊一样，rollup 以最小化信任的方式与 DA 层进行通信，保证了较好的安全性。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/024.png)

***6.最低限度的治理***

区块链治理很慢，改进提案通常需要多年的社会协调才能实施。虽然这是安全所需要的，但它显著减慢了区块链领域的开发节奏。

模块化区块链为区块链治理提供了一种更好的方式，其中执行层可以独立快速地采取行动，而共识层可以保持稳定。

EIP 的历史上很大一部分提案与执行功能和性能有关。它们通常涉及诸如操作定价、添加新操作码、定义 token 标准等内容。

在模块化区块链堆栈中，这些讨论将仅涉及各个执行层的参与者，不会渗透到共识层。

***7.去中心化区块验证，而非生产***

**Vitalik 在 Endgame 一文中指出 —— “区块生产是中心化的，区块验证是无须信任且高度去中心化的，仍然可以防止审查。” 这意味着，去中心化最重要的因素是区块验证而不是生产**，只要一小部分共识节点的行为可以被大量参与者审计，我们依然可以信任区块链。

同样，虽然 Celestia 对区块生产者的资源要求很高，但对验证者的资源要求较低，从而实现了高度去中心化、抗审查的网络。

***8.简洁性***

明确识别区块链的可扩展性瓶颈对 Celestia 团队做出最简洁的设计选择有巨大帮助。虽然以太坊在其分片路线图的最后实施了 DAS，但 Celestia 选择不走过于复杂的共识分片路线。同样，Celestia 没有实施新奇的共识协议，而是选择使用具有成熟工具和广泛的开发人员/验证者支持的 Tendermint。**我们认为这些设计选择将使 Celestia 脱颖而出，并且在 Celestia 进入市场时大受欢迎。**

**07.**

**Celestia 的商业模式**

以太坊和 Celestia 社区的许多人认为 DA 最终会有巨大的价值。来自以太坊基金会的研究员 Dankrad Feist 在和 Celestia co-founder John Adler 对谈的播客中表达了他的观点：

*“资产......需要从一些......产生收益的手段中获得安全。我相信最有价值的资产将只在数据的可用性上，区块空间（block space）将成为去中心化经济中最有价值的资产。”*

Celestia 对 rollups 而言是更便宜、更快捷的数据可用性 L1（data-availability L1），rollups 将越来越多地使用它来达成共识和数据可用性。因此，Celestia 做的是**向 rollps 出售区块空间（blockspace）**的生意。

Celestia 的收入来源有 2 个：**交易费（transaction fees）和最大可提取价值（MEV）**。

***交易费用（Transaction fees）***

**Celestia 将自己描述为区块链领域的“AWS”，这样描述道，“Celestia 之于去中心化 apps，就如同云计算之于传统互联网**。”像 AWS 这样的云服务使得用户在共享服务器的虚拟机上部署网页，而 Celestia 允许用户在共享一个共识层的链上部署 Dapps。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/025.png)

作为一种 B2B 业务，向 Celestia 支付交易费用的将是 rollups，而不是直接的用户。Celestia 计划实施类似于 EIP-1559 的燃烧机制，将交易费用分成两部分：

- 动态的基础费用。这部分费用会随着网络拥堵而增加，它们会被燃烧，算作协议收入。
- 给 Celestia 验证者节点的小费，让他们优先处理某些交易（当然这些交易已经经过 rollup 打包）。这笔费用由 rollup 支付给验证者（validator）。

验证者通过验证区块来赚取 Celestia coins，随着更大规模的采用，烧掉的 coins 会超过发行量，这将造成货币通缩。要成为 Celestia 验证者，必须质押 Celestia coin，如果被检测到违规行为，这些 coins 会被罚没。Celestia coins 除了要用来支付交易费用，还会有人想要质押 Celestia coin 成为验证者，因而 Celestia coin 会越来越有价值。

***MEV***

Maximal Extractable Value 是矿工/验证者的次要收入来源，用户可以向验证者支付额外的金额，让他们的交易被优先处理，这种“贿赂”没有上限。大多数情况下，用户希望确保他们的交易是区块中的第一个，以防止抢跑（front-running）。有时候恰恰相反，用户可能会付钱给验证者对 mempool 中有的交易进行抢跑（front-run）或“三明治攻击”。

💡

注：mempool，等待被添加到区块中的交易集合

Celestia 也会发生这种情况，rollups 希望自己的一批交易在另一个批交易之前被打包到区块中，因此他们会“贿赂”验证者，这种“贿赂”既可以用 Celestia coin 支付，也可以用验证者愿意接受的任何其他货币。

如果 Celestia 团队为这一过程创建 Priority Gas Auction（PGA）机制，那么 MEV 很可能是以 Celestia coin 支付的，支付的费用其中一部分会被燃烧，这将为 Celestia coin 持有者带来更多价值。即使“贿赂”以另一种货币结算，赚取这些“贿赂”的激励也会增加验证者的供应，从而增加抵押 Celestia coin 的需求。这两种情况都会促进 Celestia coin 的价值提升。

在常规的 L1 区块上，MEV bot 可以针对单个交易提取价值，而 Celestia 处理的是捆绑交易（bundled transactions），每个区块的可提取价值会更低。

**因此，Celestia 网络可以赚取这两部分收入来源的总和：基本交易费和 MEV 中的一部分。**

**08.**

**市场竞争与路线图**

**用户数据**

Celestia 于 2022 年 3 月 25 日发布了 Mamaki Testnet，约有 1000 个节点参与测试，活跃节点约 150，由于当前 Mamaki 测试网没有激励，所以参与人数不多。推特上已有 6.1 万关注者，Discord 群聊社区中有 3.5 万成员。

**竞争格局**

***Avail***

Avail 是 Polygon 团队于去年 6 月宣布推出的一个通用的、可扩展的、以数据可用性为中心的区块链，适用于独立链、侧链和链外扩展解决方案。

Avail 使用 Kate 多项式承诺来创建一个二维数据可用性方案，避免欺诈证明，不需要诚实的多数假设，并且不依赖诚实的全节点来获得数据可用。

Celestia 的联合创始人 Mustafa Al-Bassam 在 twitter 上称 Polygon Avail 的介绍几乎逐字复制了他在 2019 年介绍 LazyLedger（Celestia 的前身）文章。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/026.png)

针对 Mustafa Al-Bassam 关于 Polygon Avail 涉嫌抄袭的指责，Polygon 团队回应称，介绍文字的雷同是营销和内容团队的失误，**实际上 Avail 与 Celestia 是两个不同的架构，主要区别在于 Avail 基于 Kate 承诺，而 Celestia 基于欺诈证明，因此技术层面上存在实质性的区别**，不过仍因营销和内容团队的失误对 Celestia 及其社区表示歉意。

**Celestia 和 Avail 都有其优势和劣势**。Celestia 实现起来比较简单，但由于其纠删码和轻节点采样数据的规模较大，因此需要的**通信带宽略高**。Avail 涉及相对复杂的加密实现，**难度稍大**，它的优点是纠删码尺寸小，轻节点采样的数据量小，带宽要求低。目前 Avail 已发布测试版，具体竞争格局，还有待一段时间观察。但 Celestia 无论是从市场先发优势还是技术正统性上，都处于领先地位。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/027.png)

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/028.png)

***以太坊分片：Danksharding***

**我们对 Celestia 最大担忧在于，Celestia 的机会只在以太坊分片计划完成之前的这段窗口期。**Danksharding 比当前的 rollup 和 validum 都更加合理：它将 DA 拆分为单独的层，比 rollup 更有效；但仍然在链上，比 validum 更高的安全性。

这样做的好处是通过减少验证者的工作量（仅验证一小部分 DA 而不是全部）在大区块的情况下保持验证者的可靠性，这导致每秒交易量更高，验证所有交易的成本更低。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/029.png)

Celestia 与以太坊升级的 DA 分片相似之处在于，rollups 都继承一个基础层的安全性，而不同之处在于以下两个方面：

1. Celestia 不在基础层执行任何有意义的状态变更，而升级后的以太坊则仍需要在基础层执行。这将使 Celestia 上的主权 rollups 免于高度波动的基础层费用，而在状态频繁变动的以太坊上，token 销售、NFT 空投或高收益耕种的机会都可能导致需求大规模激增，gas fee 飙升。Celestia 的 rollups 在安全性方面消耗相同的原始数据存储资源，并且仅用于安全性，这使得主权 rollup fees 主要与该特定 rollup 的使用绑定，而不是和基础层。
2. DA 证明的一个关键特性就是，参与节点越多，算力多，共同合作可承担的工作越多，可以存储的数据也就更多。这意味着由于 Celestia 有更多的轻节点参与 DA 层的采样工作，区块的尺寸就可以变得更大，吞吐量更高。理论上 Celestia 的吞吐量可以比升级后的以太坊 DA 层更大，但纸面的 tps 毫无意义，我们仍需要静待两者的开发速度与具体实现。

**Roadmap**

Celestia 第一个公共测试网于 2022 年第二季度推出，该测试网旨在发展和稳定验证者社区。它还将允许在 Celestia 之上构建 dApp 和 Rollup 的首次实验。测试网将持续几个月，并将为 2023 年第一季度的 Celestia 激励测试网奠定基础。

主网上线为 2023 年第二季度，该网络将包括开发人员和节点运营商能够获得奖励的任务和挑战。激励性测试网将与计划于 2022 年第四季度末的主网具有近乎相同的功能。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/030.png)

**09.**

**未来的挑战**

Celestia 正在开创一种全新的区块链设计。虽然我们相信这是一个优于现有解决方案的模型，**但它仍然存在一些挑战**：

**1. DA 网络的不稳定性**。正如我们上文提到的那样，Celestia 的区块大小随着网络中数据采样节点的数量而增加，然而，数据采样的过程并不具备抵抗**女巫攻击（Sybil-resistant）**的能力。因此，没有确切的方法来确定网络中真实节点的数量，区块的大小也就无法确定，DA 网络的吞吐量也就是不确定的。而女巫攻击也可能造成恶意共识，从而破坏整个网络。另外，参与采样的节点并不受到直接的奖励，只有隐性激励——维持网络的稳定，它们可以获得更多收益。直接激励不足也可能导致网络的不稳定性。

💡

注：Sybil Attack，女巫攻击，是指一个人可以伪造多个身份运行多个伪装节点，对整个网络造成攻击。Sybil Resistant 就是对女巫攻击有抵抗能力。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/031.png)

**2. 不做执行的专用 DA 层网络冷启动困难**。与其他区块链不同，Celestia 依赖其他执行链来启动用户活动，因此，Celestia 的初始用例之一 Celestiums 将用作以太坊上 Validiums（类似于 rollups）的链下 DA 解决方案。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/032.png)

另一个项目是 Cevmos，这是一个带有内置 EVM 的 Cosmos SDK 链，专门用于 rollup 结算。Cevmos 上的 rollups 会将他们的数据发布到 Cevmos，然后再将其发布到 Celestia。就像今天的以太坊一样，Cevmos 将作为结算层执行 rollups 证明。Cevmos 的目标是允许以太坊 rollups 在 Celestia 上直接发布，而无需更改其代码库。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/033.png)

**3. Celestia 原生代币的实用性存在限制**。像其他 L1 公链一样，Celestia 的原生代币将通过对 Celestia 区块空间的需求来积累价值，然而，与大多数链不同，由于 Celestia 不做状态执行，其代币在 DeFi 和其他垂直领域作为流动性来源的效用将受到一定限制。

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/034.png)

**特别感谢**

Suning @Foresight Ventures、Xinning、Junchen、Alan、JFLam

**Reference**

https://members.delphidigital.io/reports/pay-attention-to-celestia

https://members.delphidigital.io/reports/l1-vs-l2-entering-the-endgame/

https://celestia.org/resources/reading-list/

https://medium.com/@Jon\_Charbonneau/celestia-the-foundation-of-a-modular-blockchain-world-95900fe2cfb0

https://medium.com/@Jon\_Charbonneau/why-modular-app-specific-blockchains-are-the-future-79652e5c75ec

https://coinmarketcap.com/alexandria/article/what-is-data-availability

https://blog.celestia.org/clusters/

https://rpubs.com/Ramshreyas/celestia

https://blog.celestia.org/introducing-modular-fellows/

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/035.png)

延伸阅读

[![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/036.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247493248&idx=1&sn=63fd70c440e8d48da996f52475933f86&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247493248&idx=1&sn=63fd70c440e8d48da996f52475933f86&scene=21#wechat_redirect")

StarkWare：以太坊扩容最佳团队，80 亿美元高估了吗？

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/037.png)

[![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/038.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485924&idx=1&sn=68b05ae1dd48023582b50d1e403d8689&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485924&idx=1&sn=68b05ae1dd48023582b50d1e403d8689&scene=21#wechat_redirect")

Solana：以太坊的挑战者，要建立区块链领域的纳斯达克

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/039.png)

[![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/040.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247488708&idx=1&sn=e3031c4ebb1cd1968c632177102e0dc3&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247488708&idx=1&sn=e3031c4ebb1cd1968c632177102e0dc3&scene=21#wechat_redirect")

Terra：区块链领域的支付宝，破壁加密世界和传统商业

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/041.png)

[![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/042.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485264&idx=1&sn=aabb62635b2598b0ad535801d9c270cd&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485264&idx=1&sn=aabb62635b2598b0ad535801d9c270cd&scene=21#wechat_redirect")

单月收入超过3亿美金，Axie Infinity的无限可能

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/043.png)

[![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/044.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247490151&idx=1&sn=33d791f4e5e0aef693c912cac78ad612&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247490151&idx=1&sn=33d791f4e5e0aef693c912cac78ad612&scene=21#wechat_redirect")

Paradigm：凭实力完美抄底比特币，新范式投资的登顶之路

![](../images/2022-09-30-celestia-mo-kuai-hua-qu-kuai-lian-de-xing-chen-da-hai/045.png)
