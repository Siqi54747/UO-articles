---
title: 10 万卡集群：通往 AGI 的新门票
publish_date: '2024-07-17'
publish_timestamp: 1721217870
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/3VoCKTcxp_FRUsFH-UHbPQ
msgid: 1000000270
appmsgid: 2247508533
itemidx: 1
digest: 10万卡集群正在成为美国大模型公司的标配
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgwS7rxwlOLt6SzZFibAOFq6UIqGWTmGIAmhL1UhEj3V6SoyFX4wgPzlIEBPXicfDnCZ2KJ1tXZq9yWA/0?wx_fmt=jpeg
image_count: 52
archived_at: '2026-04-20T02:22:16+08:00'
---

[![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/001.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect")

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/002.png)

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/003.png)

作者：Dylan Patel，Daniel Nishball

编译：Lavida

编辑：penny，NCL

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/004.png)

10 万卡集群正在成为美国大模型公司的标配。

为了捕捉 AGI 大基建浪潮中的 beta 机会和价值流向，拾象发布了 AI 时代的纳斯达克指数， [**AGIX Index**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&chksm=ce9b60bbf9ece9ad6b7028fd2aa90e43dba20a6a92f9202cdd88b806dd9a18f3e0e17ce7e8e1&scene=21#wechat_redirect)。**在文章中我们讨论过，AI 行业正处于“硬件投入—infra 建设—应用爆发”这三个阶段的初期，因此，硬件和 infra 是 AGIX Index 目前重点覆盖的板块。**

新一轮 10 万卡集群竞赛再次证明，**AGI 的基建投入仍然如火如荼地进行**——马斯克高调宣布为 xAI 建设 10 万卡集群，OpenAI/Microsoft、Anthropic/AWS、Meta 等大型 AI 公司也在加紧 10 万卡集群建设，每个集群在服务器硬件上的支出已经超过 40 亿美元。但一个 10 万 H100 集群的建设涉及复杂的技术和运营挑战，远不是砸钱就能解决的问题。

大模型训练的本质是把数据通过算力转换成智能。在 AGI 竞赛中，如果 GPU 是核弹，数据中心就是核武器库。**作为新一代计算单元，数据中心决定了芯片是否能转化成算力，**支持模型实现“跳变式跨越”。

在这样的竞赛中，既涉及到电力能源挑战、并行计算、网络拓扑方案、可靠性等各种挑战，也涉及到各环节的头部公司，[**AGIX Index**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&chksm=ce9b60bbf9ece9ad6b7028fd2aa90e43dba20a6a92f9202cdd88b806dd9a18f3e0e17ce7e8e1&scene=21#wechat_redirect) 中的代表公司**英伟达、博通、TSMC、MRVL、SK Hynix、VRT**等仍在大基建浪潮的尖端。

本文编译自 SemiAnalysis 对 10 万 H100 集群建设的技术分析，延续我们对**[数据中心互联的研究](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507950&idx=1&sn=64c3d23960ec8e4cf91dccdece8aa4e1&scene=21#wechat_redirect)**，本文将继续聚焦英伟达、博通为代表的硬件公司如何构建大型 AI 训练集群。

💡 目录 💡

      01 数据中心的电力问题

      02 并行计算的方式

      03 超级 AI 算力集群的网络设计

      04 可靠性和数据恢复

      05 网络交换机技术对比

      06 CAPEX：BOM 成本计算

      07 机架布局和平面图优化

GPT-4 发布之后，一直存在一种声音认为 AI 发展低于预期，模型能力没有明显跃升，**主****要原因就是目前还没任何一家 AI Lab 能够大幅增加在单一模型上投入的计算量。**目前市面上已发布的模型在训练计算量上基本都是 GPT-4 水平（～2e25 次 FLOPS），Gemini Ultra、Nemotron 340B 和 Llama 3-405B 的 FLOPS 都和 GPT-4 相似甚至更高，但因为有些架构不够先进，导致最终没有解锁新的能力。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/005.png)

Source: SemiAnalysis Estimates

**虽然 OpenAI 的计算资源更多，但他们主要把这些资源用来开发 GPT-4 Turbo 和 GPT-4o 这种规模更小、过度训练且推理成本更低的模型，并且 OpenAI 也承认前不久才开始训练下一代能力更强的模型。**AI Timeline 的下一个里程碑将是训练出数万亿参数的多模态 Transformer，让模型具备处理大量视频、图像、音频和文本数据的能力。目前还没有人能完成这项任务，但各大公司正在积极扩张。OpenAI/Microsoft、xAI 和 Meta 等大型 Al Labs 正在展开 10 万 GPU 集群建设的争夺赛，这些单个训练集群仅服务器资本支出就超过 40 亿美元，还受限于数据中心容量和电力供应能力。**一个 10 万 GPU 的集群需要超过 150MW 的数据中心容量，一年的消耗就是 1.59TWh（15.9 亿度电），约等于 15 万个家庭一年的用电量。**按$0.078/Kwh 的单价来计算，一个 10 万卡集群每年光在电力这一项上的支出就高达 1.239 亿美元。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/006.png)

Source: SemiAnalysis, US EIA

以下数据可以更直观地展示一个 10 万 GPU 集群的算力：

•**OpenAI 训练 GPT-4 时用了大概 2 万张 A100，**BF16 浮点运算量大概是 2.5×10²⁵ FLOP（2150 万 ExaFLOP），训练时间是 90-100 天，峰值吞吐量只有 6.28 BF16 ExaFLOP/秒。

• 一个 10 万 H100 集群的峰值吞吐量会达到 198 FP8 ExaFLOP/秒 或 99 FP16 ExaFLOP/秒，**从峰值理论上来说，这个数值是 2 万张 A100 GPU 集群训练时最大 FLOPS 的 31.5 倍。**

\* 拾象注：Exa 表示 10¹⁸ ，所以 1 ExaFLOP = 10¹⁸ FLOPs

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/007.png)

Source: Nvidia, SemiAnalysis 

AI labs 用 H100 训练万亿参数的模型时，能够实现高达 35%的 FP8 MFU 和 40%的 FP16 MFU。MFU（Model Full Utilization，模型浮点运算利用率）是在考虑到成本和各种限制因素后，衡量峰值潜力 FLOPS 的有效吞吐量和利用率的标准，这些因素包括功率限制、通信不稳定、数据丢失后重新计算、拖慢进度的任务和低效核心程序等等。**一个 10 万张 H100 的集群用 FP8 做 GPT-4 的训练，只需要四天。如果一个 10 万 H100 集群持续运行 100 天，可以实现大概 6×10²⁶（6 亿 ExaFLOP）的有效 FP8 模型 FLOP。但如果硬件可靠性较差，就会显著降低 MFU。**

**01.**

**数据中心的电力问题**

为了支持服务器、存储设备、网络设备这些核心 IT 设备，一个 10 万 H100 集群所需的功耗大约是 150MW（兆瓦）。**虽然单个 GPU 的功率只有 700W，但每个 H100 服务器内还有 CPU、NIC（网络接口卡）、PSU（电源供应单元）等等部件，所以每个 GPU 还要额外消耗大概 575W。**除了 H100，集群内还需要一系列存储服务器、网络交换机、CPU 节点、光模块等等，这些设备会额外再占用大概 10% 的 IT 功耗。**作为对比，美国最大的国家实验室超级计算机 El Capitan 只需要 30MW 的关键 IT 电力，大概只有一个 10 万 H100 集群功耗的 1/5。**

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/008.png)

超级计算机 El Capitan，

部署在美国劳伦斯利弗莫尔国家实验室（LLNL）

电力方面一个很大的问题是，至今还没有任何单个数据中心大楼能够承载 150MW 的电力需求，所以 10 万 GPU 集群一般都是一个园区，而不是单一建筑。由于没有合适的设施，xAI 甚至要把田纳西州 Memphis 的一家废弃旧工厂改造成数据中心来解决电力供应问题。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/009.jpg)

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/010.jpg)

xAI 在田纳西州 Memphis 建设中的数据中心，

世界上最大的超级计算机园区

Source: xAI

因为整个园区内的服务器需要通过光纤收发器来联网，而传输的距离越长，光纤收发器成本就越高，成本就会在无形中增加：

• “多模”SR（短距离）和 AOC（有源光缆）光模块传输距离约为 50 米；

• “单模”DR 和 FR 收发器传输信号距离在 500 米 - 2000 米 之间，可靠性较高，但成本可能是“多模”SR（短距离）和 AOC（有源光缆）光模块的 2.5 倍；

• 园区级别的 800G 相干光收发器的传输距离超过 2000 米，但价格也是普通光模块的 10 倍以上，一般在 $1800。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/011.png)

多模光纤（Multimode Fiber）和单模光纤（Single Mode Fiber）在结构和光信号传播方式上的区别

小型的 H100 集群通常会用平面或者近平面这样交换层数比较少的网络设计，只需要通过一两层交换机，用多模收发器（multi-mode transceiver）把所有 GPU 以 400G 的速率进行互联。但是大型 GPU 集群必须增加更多的交换机，光纤成本会非常高，网络拓扑结构会因为供应商技术、workload 以及 capex 有很大不同。

**我们可以把每个数据中心大楼都看作一个计算岛（compute island），岛内会包含一个或多个计算舱（computer pod）；不同计算岛之间用远距离光收发器来实现互连，计算舱之间则通过廉价的铜缆或多模光模块来连接。**下图中有 4 个计算岛，这些岛内部有高带宽连接，但岛间的带宽比较低。在一个数据中心内提供 155MW 的电力是非常困难的，但 Microsoft、Meta、Google、Amazon、ByteDance、xAI、Oracle 等等超过 15 家大厂都在扩建数据中心，这些中心未来很可能有足够的空间容纳 AI 服务器和网络设备。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/012.png)

Source: SemiAnalysis 

不同的客户会基于各种原因选择不同的网络拓扑结构，包括数据传输 infra、成本、可维护性、电力、电流以及任务量等等。有些客户选择了 Broadcom Tomahawk 5，有些客户仍然坚持用 InfiniBand，还有一些选择了 NVIDIA 的 Spectrum-X，下文中我们会深入分析他们做出这种选择的原因。

**02.**

**并行计算的方式**

在深入探讨网络设计、拓扑结构、可靠性问题以及检查点（checkpointing）的策略之前，我们先简要回顾一下万亿参数训练中使用的三种并行方式：**数据并行（Data Parallelism）、张量并行（Tensor Parallelism）和流水线并行（Pipeline Parallelism）。**

**数据并行**

数据并行是最简单的并行形式，其中每个 GPU 都有模型权重的完整副本，并接收数据的不同子集。这种类型的并行通信需求最低，因为只需要在 GPU 间传递梯度数据。但**数据并行需要每个 GPU 都有足够的内存来存储整个模型的权重、激活值、优化器状态（optimizerstate）。对于像 GPT-4 这样的 1.8 万亿参数模型，仅仅是模型权重和优化器状态在训练时就需要高达 10.8TB 的内存。**

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/013.png)

Source: ColossalAI

**张量并行**

为了克服这些内存限制，可以使用张量并行技术。在张量并行中，每一层的工作和模型权重分布在多个 GPU 上，一般会覆盖全部隐藏层。中间的工作会通过在自注意力机制（self-attention）、前馈网络（feed forward network）和层归一化（layer normalizations）等计算中多次跨设备的归约（all-reduction）来交换，这就需要高带宽和非常低的延迟。**在张量并行的模式下，所有参与的 GPU 都会协同工作，共同构成一个大型 GPU。这种方式可以将整个计算任务分解为多个部分（即张量并行等级），从而减少每个 GPU 需要处理的数据量和消耗的内存。**例如，现在通常在 NVLink 上使用 8 个张量并行等级，相当于每个 GPU 使用的内存减少到原来的 1/8。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/014.png)

Source: Accelerating Pytorch Training

**流水线并行**

单个 GPU 内存有限的问题还可以用流水线并行解决。在流水线并行中，每个 GPU 只负责模型前向计算的一环，并仅计算这一环中的层，然后再把中间结果传递给下一个 GPU。因为流水线并行等级的数量减少了，所需的内存量也减少了。流水线并行对通信量有较大的需求，但相比张量并行还是要小。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/015.png)

Source: Colossal AI

**3D 并行**

为了最大化 MFU，公司通常会结合以上三种并行形式，形成 3D 并行，分布大概是：

• H100 服务器内的多个 GPU 间用张量并行；

• 岛内的节点间用流水线并行；

• 岛间用数据并行，因为数据并行通信量最低，并且岛间的网络连接比较慢。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/016.png)

Source: Optimus-CC

全存储数据并行（FSDP，Fully Sharded Data Parallel）技术通常会在小规模 GPU 集群上用来处理非常大型的模型，但在实际应用中却很少 work，本身也存在不兼容的问题。

**03.**

**超级 AI 算力集群的网络设计**

**拓扑结构**

AI 算力集群的网络设计需要考虑数据并行的方案。如果每个 GPU 都用 Fat-Tree 拓扑结构，并以最大带宽来连接，成本会非常高，因为中间涉及到 4 层交换，每增加一层网络，所需的光器件成本也会大幅上升。因此，没有人会为大型 GPU 集群部署完整的 Fat-Tree 架构。相反，他们会创建有完整 Fat-Tree 架构的计算岛，并在这些岛间用较低带宽互联。实现这一点有很多方法，但**大多数公司会对网络顶层进行带宽的过度订阅（oversubscribe），即在网络的顶层，分配给岛屿之间连接的带宽会超过实际可用的带宽。**

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/017.png)

Fat Tree（k=4）架构示意

下图是 Meta 上一代的 GPU 集群架构，最多可以达到 3.2 万卡。总共有 8 个计算岛，岛间有全速的 Fat-Tree 带宽，然后在顶层有另一层交换，收敛比（即 over subscription，过度订阅比率）为 7:1，也就是说岛间的网络连接速度比岛内的网络连接慢 7 倍。**但在实际操作中这种降速对性能影响并不大，因为通常不是所有的服务器都会用最大带宽来通信，可以在保证局部高性能的同时，降低整体网络架构的复杂性和成本。**

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/018.png)

Source: Meta

**InfiniBand和前端以太网的****混合架构**

GPU 部署有多种网络：前端网络、后端网络和扩展网络（NVLink）。某些情况可能会在每个网络上用到不同的并行方案，NVLink 网络的速度可能是唯一能够满足张量并行需求的网络。后端网络通常可以轻松处理大多数其他类型的并行，但如果存在过度订阅的情况，通常只能用于数据并行。还有些人甚至没有在顶层带宽过度订阅的集群架构，他们反而是把流量从后端网络转移到前端网络，来避免带宽的瓶颈。

一家大型科技公司在多个 InfiniBand 计算岛之间用了前端以太网进行模型训练，这是因为前端网络的成本要低得多，还可以利用园区内现有的网络在大楼和区域路由间通信。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/019.png)

Source: SemiAnalysis

不过由于采用了MoE等稀疏技术，模型大小增长得更快，前端网络需要处理的通信量也在增加，前端网络的带宽最终可能跟后端网络的带宽差不了多少，所以必须仔细权衡优化，否则最终可能两种方案的网络成本趋同。

Google 的做法是专门设计了一种叫做 ICI（Inter Chiplet Interconnect）的前端网络架构，用来支持大规模 TPU Pod 训练。这种架构最多只能支持 8960 个芯片，并且在 64 个 TPU 水冷机架之间要用昂贵的 800G 光器件和光路交换机连接。因为这种在扩展规模上的局限性，Google 必须通过增强 TPU 的前端网络来弥补，让它的表现比大多数 GPU 前端网络都更强大。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/020.png)

Source: Google at MLSys24 

如果要用前端网络来进行分布式训练，那就必须在不同的岛间进行**全局 all-reduce**，具体操作包括：

1. **本地 reduce-scatter：**首先，每个舱或岛内部用 InfiniBand 或 ICI 网络进行规约-分散（reduce-scatter），这样每个 GPU/TPU 都会拥有梯度的一部分总和。

2. **跨舱 all-reduce：**用前端以太网在不同舱之间传输和汇总数据。

3. **舱级 all-gather：**在每个舱内部再次收集和整合数据，确保每个节点都获得完整的数据。

前端网络还要负责加载数据。随着多模态图像和视频训练数据的增加，前端网络需求未来也会有指数级增长。在这种情况下，加载大型视频文件和执行 all-reduce 操作会争夺前端网络带宽，因此必须在二者间做合理分配。如果存储网络流量不规则，还会增加滞后问题，导致整个 all-reduce 操作变慢，没办法做可预测的建模。

另一种替代方案是用 4 个层级的 InfiniBand 网络，收敛比是 7:1，这类网络有 4 个舱，每个舱内有 24576 个 H100，采用 3 层级的非阻塞网络系统。**相比前端网络，****InfiniBand 网络更容易扩展带宽，灵活性会更高，只需在 A 大楼和 B 大楼的交换机之间增加更多的光纤收发器即可，这比给集群中每个机箱的前端网络做 NIC 升级（例如从 100G 升级到 200G 等）要容易得多。**

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/021.png)

Source: SemiAnalysis 

这种网络相对来说也更加稳定，因为前端网络可以专门负责加载数据和检查点，后端网络则可以专注 GPU 到 GPU 的通信，这样也更好解决落后节点问题。但它最大的缺点就是需要各种额外的交换机和光模块，所以价格极贵。

**Rail Optimized vs Middle of Rack**

有些集群为了让网络更好维护和管理，同时尽量用小于 3 米的铜缆和小于 50 米的多模光纤来增加稳定性，会选择放弃 NVIDIA 推荐的 Rail Optimized 设计，采用机柜中部（Middle of Rack）设计。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/022.png)

Source: Huawei

💡

根据交换机在数据中心机房机柜上的部署位置，一般分为**机柜顶部（Top of Rack）， 机柜中部（Middle of Rack）或机柜底部（Bottom of Rack）**。其中的机柜中部（Middle of Rack）是指在数据中心内将设备安装在服务器机柜的中间位置。这种安装方式可以优化空气流通和散热效率，平衡机柜重量，方便维护，并改善电缆管理，经常用在关键设备的安装，比如交换机、路由器和存储设备，来提高数据中心的整体效率和可靠性。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/023.jpg)

Source: Nvidia

Rail Optimized 技术可以让每个 H100 连接到 8 个不同的 leaf switch，而不是全部连接到同一个机架中部的交换机，这样每个 GPU 只需要通过 1 个交换机跳转就能和更远距离的 GPU 通信。All-to-All 集体通信在 MoE 模型里用得非常频繁，交换机的跳数少了，通信路径的长度更短，就能更好提高现实世界中 All-to-All 集体通信的性能。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/024.png)

Source: Crusoe

**Rail Optimized 的缺点在于必须连接到不同的 Leaf Switch，这些交换机的距离不一，每次连接都要跨越不同的距离，所以必须用更贵的光纤来连接。但在 Middle of Rack 的情况下，交换机可以放在同一个机柜里，可以用更短距离的连接方式，比如直连电缆（DAC）和有源电缆（AEC），这些电缆一般都更便宜。**另外交换机与 Spine Switch 之间的距离超过 50 米时，就必须用单模光纤收发器，因为它能支持更远的距离。

如果使用了 Rail Optimized 之外的设计，就可以用廉价的 DAC 替换 98304 个光纤收发器，来连接 GPU 和 Leaf Switch，也就是说整个网络中会有 25-33% 的连接是铜缆，这样可以显著降低成本。如下面的机柜图所示，在 Rail Optimized 中，Leaf Switch 会在机柜的中间位置，这样每个 GPU 都可以用 DAC 铜缆直接连接到 Leaf Switch。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/025.png)

Non-rail optimized middle of rack

Source: SemiAnalysis

**相比光纤来说，DAC 铜缆散热更好，省电又便宜，可靠性也更高，所以出现网络连接中断（flapping）和故障的几率就更低，而这些都是光纤高速互连运行中的大问题。**比如说 Quantum-2 IB 脊交换机如果用 DAC 铜缆的话功耗是 747W，但用多模光纤收发器时功耗会飙到 1500W。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/026.png)

Rail optimized end of row

Source: SemiAnalysis

另外，对于数据中心的技术人员来说，Rail Optimized 设计的初始布线会非常耗时，因为每个链路两端的距离有 50 米，而且还不在同一个机架上。相比之下，Middle of Rack 的 Leaf Switch 与所有 GPU 都在同一个机架上，甚至还可以在集成工厂环境中测试计算节点到 Leaf Switch 的链路，方便更好地提前发现和解决问题，减少现场部署时的风险。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/027.png)

Rail-Optimzed Network 的 End of Row 水冷散热

Source: SemiAnalysis

**04.**

**可靠性和数据恢复**

**可靠性是限制模型训练的关键问题**

**目前模型训练都需要多个计算单元同时工作，系统中的任何一个故障都可能影响整体训练过程，因此可靠性成为了大型集群最重要的运维关注点之一。**最常见的可靠性问题包括 GPU HBM ECC Error、GPU 驱动程序卡住、光收发器故障、NIC 过热，以及节点不断报错和故障等等。

数据中心为了保持训练的连续性，尽量减少故障恢复的平均时间，必须在现场保留热备节点（hot spare nodes）和冷备用组件（cold spare components）。当发生故障时，不能马上就停止整个训练，而是要赶紧换上激活好的备用节点继续训练。

**一般来说重启能解决大部分故障，但并不能解决全部问题。实操来说，技术人员经常要亲自去检查和更换设备，如果比较幸运的话，可能几个小时能修复好，但很多情况下需要好几天才能让节点重新运行。**虽然从理论上讲这些损坏的节点有可用的 FLOPS 能力，但实际上这些节点和备用的热节点并没有参与到模型训练中，也没有为模型训练作出贡献。

在训练过程中，模型需要频繁地将模型的 checkpoint 保存到 CPU 内存或 NAND SSD 中，避免发生 HBM ECC 等等错误。一旦出现了报错，就必须从较慢的存储层重新加载模型权重和优化器，然后再重启训练。这个过程可以用到像 Oobleck 这样的容错训练技术，提供由用户级别应用程序驱动的方法来应对 GPU 和网络故障。

**但是频繁保存 checkpoint 和使用容错训练技术会影响系统的整体 MFU，因为过程中整个集群要不断地暂停，不断把当前权重保存到持久内存或 CPU 内存中。**一般来说每 100 次迭代只保存一次检查点，也就是说在发生故障时最多可能丢失 99 步的有效工作。在一个 10 万集群中，如果每次迭代需要 2 秒钟，那么在第 99 次迭代发生故障时，就会损失多达 229 个 GPU 天的工作量（一个 GPU 天代表一个 GPU 运行 24 小时）。

另一种故障恢复方法是让备用节点通过后端网络只用 RDMA（远程直接内存访问）从其他 GPU 复制权重，也是大多数大型 AI Labs 在用的故障修复方法。后端 GPU 网络大概是 400Gbps，每个 GPU 有 80GB 的 HBM 内存，复制权重大约需要 1.6 秒。用这种方法的话，最多只会丢失 1 步操作（因为会有更多的 GPU HBM 保存有最新的权重副本），所以最后只会丢失相当于 2.3 个 GPU 天的计算量，另外还要再加上从其他 GPU 的 HBM 内存 RDMA 复制权重所需的 1.85 个 GPU 天。

checkpoint 重启本身可以说是又慢又麻烦，十分低效，但许多小型公司仍然在坚持用它来处理所有故障，主要是因为它操作起来更简单。如果是直接进行内存重建而不是 checkpoint 重启，可以给整体集群运行的 MFU 提高好几个百分点。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/028.png)

Source: Meta

**InfiniBand/RoCE 链路故障**

**各种报错中有一个最常见的问题是InfiniBand/RoCE 链路故障。**虽然每个 NIC 到 Leaf Switch 链路的平均故障间隔时间是 5 年，但因为光模块数量非常多，对于一个全新的、正常工作的集群来说，第一次作业失败仅仅在 26.28 分钟内就会发生。如果不通过内存重构进行故障恢复，那么在一个 10 万 GPU 的集群中，因为光器件故障，重启要花的时间甚至可能会超过训练模型的时间。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/029.png)

Source: SemiAnalysis 

**目前每个 GPU 都会通过 PCIe 交换机直接连到一个 ConnectX-7 NIC，这种设计没有备用路径，在网络架构层面完全没有容错能力，所以必须在训练代码中添加处理故障的逻辑，这就直接增加了整个代码库的复杂程度。现在对于 NVIDIA 和 AMD GPU 的网络结构来说，这是一个关键问题，因为这种设计对单点故障非常敏感，即便是只有一个 NIC 失败，连接到它的卡也没有其他路径和其他 GPU 通信。**现在 LLM 基本在节点内都用的是张量并行，需要所有节点之间能够高效通信，所以即使一个网卡、一个收发器或一个 GPU 失败，整个服务器都会被当作是宕机不可用。

**各大 Lab 都在努力让网络能够重新配置，让节点不那么脆弱。解决这个问题是非常必要的，因为只要一个 GPU 故障或一根光纤故障，整个 GB200 NVL72 就会瘫痪。而一个 GB200 NVL72 有 72 个 GPU，价值数百万美元。如果这样的系统瘫痪，影响和损失要比一个几十万美元的 8 GPU 服务器宕掉严重得多。**

NVIDIA 已经意识到这个问题的严重性，并且增加了一个专门的引擎用于 RAS（reliability， availability and serviceability）的维护。RAS 通过分析卡的数据，例如温度、恢复的 ECC 重试次数、时钟速度、电压，可以预测芯片可能出现的故障，并且提醒数据中心的技术人员，这样就可以人为地主动维护。举例来说，技术人员可以提前调整风扇速度配置文件，加快风扇转速，增强散热效果；或者在计划的维护时间段内，暂时下线服务器，进行更详细的物理检查和维护工作。此外，在开始训练作业之前，每个芯片的 RAS 引擎都会执行全面的自检，比如运行已知结果的矩阵乘法，检测静默数据损坏（SDC）等等。

**Cedar-7**

Microsoft/OpenAI 等为了优化成本进行了另一种尝试：在每个服务器都用 Cedar Fever-7 网络模块，而不是 8 个 PCIe 外形的 ConnectX-7 网络卡。Cedar Fever 模块的主要优点是只需要 4 个 OSFP 插槽，而不是 8 个，这种配置允许在计算节点端用双端口 2x400G 收发器，而不只是在交换机端使用，因此可以把连接到 Leaf Switch 的光模块数量从每个 H100 节点的 8 个减少到 4 个。连接 GPU 到 Leaf Switch 的总计算节点端光模块数量也从 98304 减少到 49152。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/030.png)

Source: Nvidia 

因为 GPU 到 Leaf Switch 的链路数量减少了一半，我们可以更好地预测首次故障的时间。根据估算，每个双端口 2x400G 链路的平均故障间隔时间是 4 年（单端口 400G 链路是 5 年），这样一来，首次出故障的估算时间会延后到 42.05 分钟，比没有使用 Cedar-7 模块时的 26.28 分钟要好得多。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/031.png)

Source: ServeTheHome

**05.**

**网络交换机技术对比**

**Spectrum-X NVIDIA**

现在市场上有一个 10 万 H100 集群在建中，预计年底前会投入运营，这个集群使用的就是 NVIDIA Spectrum-X 以太网。

Spectrum-X 在大型网络中相比 InfiniBand 有很多优势，除了性能和可靠性更好外，成本也更低。Spectrum-X 以太网的 SN5600 交换机有 128 个 400G 端口，而 InfiniBand NDR Quantum-2 交换机只有 64 个 400G 端口，还有博通的 Tomahawk 5 交换机 ASIC 也支持 128 个 400G 端口，所以这一代 InfiniBand 的劣势非常明显。

一个完全互联的 10 万节点集群可以设计为 3 层架构，如果用 4 层架构，那么所需的收发器数量会是原来的 1.33 倍。由于 Quantum-2 交换机的端口容量较低，在 10 万 H100 集群中，完全互联的 GPU 最多只能有 65536 个。但是下一代 InfiniBand 交换机 Quantum-X800 会通过 144 个 800G 端口来解决这个问题。从数字“144”可以看出，这是为 NVL72 和 NVL36 系统设计的，在 B200 或 B100 集群中应该应用不会很多。虽然 Spectrum-X 不需要 4 层结构可以节省一些成本，但缺点是仍然需要从 Nvidia LinkX 产品线买高价光模块，因为其他光模块可能不兼容，或者得不到 Nvidia 的验证。

**Spectrum-X 相对于其他供应商的主要优势在于，用 Spectrum-X 可以得到 NVIDIA 自家通信库（如 NCCL）的一级支持，并且 Jensen 会把 Spectrum-X 的用户放到新产品线的首批客户队列里。但如果使用博通的 Tomahawk 5 芯片，要想实现最大吞吐量，就需要大量的内部工程努力来优化网络与 NCCL 的配合。**

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/032.png)

Source: SemiAnalysis

以太网相比 InfiniBand 的缺点是不支持 SHARP 网络内归约，而网络内归约可以通过在网络交换机上进行求和操作，减少每个 GPU 需要发送和处理的数据量，从而理论上把网络带宽提高 2 倍。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/033.png)

Source: Nvidia

此外，在第一代 400G Spectrum-X 中，NVIDIA 用了 Bluefield-3 来代替 ConnectX-7 作为临时的方案，这也是 Spectrum 的一个劣势。不过我们预计在未来的几代产品中， ConnectX-8 能和 800G Spectrum-X 完美配合。对于超大规模的数据中心来说，Bluefield-3 比 ConnectX-7 卡要贵 300 美元 ASP 左右，而且还要多耗费 50W 的电力，导致每个节点都需要额外的 400W 电力，这会降低整个训练服务器的“每皮焦耳智能（intelligence per picojoule）”。在相同网络架构的前提下，用 Spectrum X 的设备相比 Broadcom Tomahawk 5 需要额外的 5MW 电力来支持 10 万 GPU 的部署。

**Broadcom Tomahawk 5**

为了避免支付 NVIDIA 产品的高额费用，很多公司会选择使用基于 Broadcom Tomahawk 5 的交换机。每个基于 Tomahawk 5 的交换机都有和 Spectrum-X SN5600 交换机相同的 128 个 400G 端口，并且如果公司有优秀的网络工程师，是能够实现类似性能的。而且需要用到的光收发器和铜缆都是通用的，可以从任何地方的任何一家供应商买到，混合搭配使用。

大多数客户会直接和 ODM 合作，比如和 Celestica 合作使用基于 Broadcom 的交换机 ASIC，或者与 Innolight 和 Eoptolink 合作进行光模块的生产。计算下来交换机和通用光模块的成本，Tomahawk 5 与 Nvidia InfiniBand 相比要便宜得多，与 Nvidia Spectrum-X 相比也同样更有价格优势。

使用 Tomahawk 5 交换机的一个缺点是，需要有足够的工程能力来修补和优化 NCCL 通信集合。NCCL 通信集合在初始状态下仅针对 NVIDIA 的 Spectrum-X 和 InfiniBand 进行了优化，也只对他们开箱即用。

好在如果建一个 10 万卡集群的预算有 40 亿美元，那是有足够的工程能力来修补 NCCL 和编写优化程序的。当然，软件开发仍然是件很困难的事，NVIDIA 始终保持着技术领先，但总体上来说，每个超大规模企业都会进行这些优化，并最终从 InfiniBand 转向其他方案。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/034.png)

Source: SemiAnalysis

**06.**

**CAPEX:**

**BOM 成本计算**

每个 10 万 H100 集群的总投资（capex）大概是 40 亿美元，根据所选择的网络类型有所不同，SemiAnalysis 提供的 4 种方案包括：

1. **4 层 InfiniBand 网络**：包括 32768 个 GPU 岛，Rail Optimized 设计，收敛比 7:1

2. **3 层 Spectrum-X 网络：**包括 32768 个 GPU 岛，Rail Optimized 设计，收敛比 7:1

3. **3 层 InfiniBand 网络：**包括 24576 个 GPU 岛，Non-Rail Optimized 设计，用前端网络做岛间连接

4. **3 层 Broadcom Tomahawk 5 以太网网络：**包括 32768 个 GPU 岛，Rail Optimized 设计，收敛比为 7:1

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/035.png)

Source: SemiAnalysis

从上图可以看出：

• 4 层 InfiniBand 网络比其他方案要贵 1.3-1.6 倍，因此未来不会有公司继续用大型 InfiniBand 网络。

• 3 层 InfiniBand 网络可行，但严重降低了并行方案的灵活性。

• Spectrum X 可以提供更大的岛，并增加岛间互联的带宽，成本也和其他方案差不多，但致命缺点是需要更多电力。

**基于 Broadcom Tomahawk 5 的 32k-GPU 集群，再加上顶层 7:1 的收敛比，是目前公认最具成本效益的方案，也是很多公司采用的网络设计方案，它提供了最高的性能与 TCO（Total Cost of Ownership，总拥有成本）比，避免支付给 NVIDIA 高额费用。**Broadcom Tomahawk 5 的解决方案已经被包括 Meta 在内的多家公司采用，并且推出的时间比 NVIDIA 的 Spectrum-X 更早。

**07.**

**机架布局和平面图优化**

在整个数据中心的设计中，优化机架布局也是很重要的，要尽可能高效地使用铜缆和多模光纤。下图是采用 Rail Optimized 设计的 Spectrum-X / Tomahawk 5 32k 集群平面图。从图中可以看到，为了优化光纤使用，有些行的 Leaf Switch 并没有放在同一行，这种设计主要为了能优化使用 50 米多模光纤。如果将多模光模块放置在行的末端，中间的 Spine Switch 就会超出 50 米的有效距离，导致无法连接。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/036.png)

使用 Rail Optimized 的

 Spectrum-X / Tomahawk 5 32k 集群平面图

Source: SemiAnalysis

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/037.png)

Source: SemiAnalysis

注：在这个 10 万节点集群在建的 4 栋大楼中，

有 3 栋已建成

在这个 Microsoft 的开发集群中，每个机架支持高达 40kW 的功率密度，每个机架内容纳 4 个 H100 节点。这个 infra 的布线设置非常独特，铜缆（特别是每行末端的粗黑缆）用于机架内交换机之间的连接。相比之下，从 H100 到 Leaf Switch 的连接则是使用多模 AOC 光纤，可以通过蓝色缆线识别。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/038.png)

Source: Microsoft

总的来说，NVIDIA 还是 10 万 H100 集群的最大赢家，因为流向 NVIDIA 的收入构成了整个 BOM 的大头。未来预计 Broadcom 将在几乎所有超大规模计算集群中占据主导地位，networking 收入将持续增长。NVIDIA 也将继续保持增长势头，因为很多新兴云服务厂商、国家和企业都将选择 NVIDIA 的参考设计。

本文内容仅为研究分享，不作为投资建议。

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/039.png)

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/040.png)

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/041.png)

排版：Doro

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/042.jpg)

延伸阅读

[![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/043.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508357&idx=1&sn=e00726dddc2ea74111fecb8faee23c86&chksm=ce9b1e1bf9ec970d937685132547a0f18157ae704ff581e97c05bf36136602f37ff44d84fb87&scene=21#wechat_redirect)

通用机器人是 AI 时代的新 "iPhone" 吗？

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/044.png)

[![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/045.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508283&idx=1&sn=1a096e4d2f545784a749b1cc018a6043&chksm=ce9b1ea5f9ec97b3f0272d4ad0b58ada6db7fbca8013cd67269eaf5946145a26d090eeb6ba15&scene=21#wechat_redirect)

专访 LanceDB 创始人：多模态 AI 需要下一代数据基建

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/046.png)

[![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/047.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508115&idx=1&sn=3a897e184295128abbe124f8db6524b4&chksm=ce9b1f0df9ec961b90749b66452bb56cc9ac6fbf328b9149a377698299fa27e985a83e0dfab5&scene=21#wechat_redirect)

Kore.ai：LLM能否为AI客服带来新一轮洗牌与机遇

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/048.png)

[![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/049.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508064&idx=1&sn=1f60f9c685f92ca914c2d4a128f83880&chksm=ce9b1ffef9ec96e8f15c7f7ea91ecea5ae6509dcdc32c804b41f1ad167471c80f51771f7ef83&scene=21#wechat_redirect)

为什么 AGI 应用还没有大爆发？

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/050.png)

[![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/051.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507950&idx=1&sn=64c3d23960ec8e4cf91dccdece8aa4e1&chksm=ce9b6070f9ece96648ed9da6b2d4953fe2b8897629285b688253fa2e4a72473a7747d91baa74&scene=21#wechat_redirect)

互联：让数据中心成为新一代计算单元

![](../images/2024-07-17-10-mo-qia-ji-qun-tong-wang-agi-de-xin-men-piao/052.png)
