---
title: 互联：让数据中心成为新一代计算单元
publish_date: '2024-06-21'
publish_timestamp: 1718976710
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/Sqfk6ytKLDKdogrOf9wwMg
msgid: 1000000263
appmsgid: 2247507950
itemidx: 1
digest: Datacenter is the new compute unit.
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgwVlJ3Dh5xrW0KibymicWFu8jJuHLdFVOdlfOnOyERwUiciaj5qxm5XRDgicorfbciaw20vicBQM0TiaqAAOg/0?wx_fmt=jpeg
image_count: 52
archived_at: '2026-04-20T02:17:26+08:00'
---

[![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/001.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect")

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/002.png)

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/003.jpg)

作者：NCL

编辑：Siqi

排版：Doro

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/004.png)

Datacenter is the new compute unit.这是英伟达对于计算系统拓展的愿景：未来数据中心将取代单个芯片，成为计算系统的基本单元，而数据中心也会像芯片一样持续迭代计算能力，不断优化性能和能效。

如同芯片依赖架构和制程工艺创新从而实现性能升级一样，高速、高带宽、低延迟的互联解决方案对于数据中心规模化计算也十分关键。

与此同时，算力规模已成为模型 Scaling 的主要瓶颈，比如 NV 在 GTC 上也只能最多将 3.2 万张 H100 组成集群，以满足 GPT-5 的训练需求。为了实现 GPT-6 ，探索10 倍级下一代数据中心成为共识。下一代超大规模集群也让“互联”升级成为一个相当现实的需求，因此，我们认为从下一代模型的计算需求出发，互联也一定是投资的关键主题。

硬件是拾象 [**AGIX Index（Bloomberg Ticker：SOLEAGIX）**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&chksm=ce9b60bbf9ece9ad6b7028fd2aa90e43dba20a6a92f9202cdd88b806dd9a18f3e0e17ce7e8e1&scene=21#wechat_redirect)的重要组成板块，在 AGI 大基建时期的当下，硬件环节的公司既是推动 AGI timeline 的关键力量，也一定能够 catch 到最多价值。本篇内容是我们对数据中心互联的主题研究，通过对各个互联环节的细颗粒度拆解，来厘清互联的现状、趋势和关键机会。

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 关键结论

02 为什么关注互联

03 互联环节的技术趋势

04 下一代互联关键：Chip-to-Chip

05 服务器层级的互联

06 NV 的垄断优势将在互联环节延续

07 重要公司

**01.**

**关键结论**

**1. 互联环节是计算中心除了计算芯片之外的第二大 Capex，并且随着 datacenter 规模的提升，互联成本的占比也会增加。**以 Meta 的 24k-GPU 计算集群为例，Compute 部分成本为 68.2%，而互联占到了 23.9%，而在 100k-GPU 的情况下，互联则占到了 26.1%，计算芯片的占比为 66.3%。

**2.****Nvidia 在互联环节同样享有强势位置。在下一代超大规模计算中心建设中，Nvidia 不仅会享受到 GPU 需求爆发的受益，也会因为对 NVLink 的提前布局捕获互联环节的果实。**NV 不仅能和 TSMC 共同实现最快的 Die-to-Die 互联，还拥有最全面的互联产业的覆盖，不仅在 Switch 层面既能用 NV Quantum-X800 将集群规模扩大到数十万以上，从而让 InfiniBand  架构在与 RoCE 的竞争中有明显优势，也能靠 Spectrum 产品线凭借针对 LLM 的 NCCL 算法库，统治 RoCE Switch 市场。

**3.****Die-to-Die 和 Chip-to-Chip 是下一代互联升级过程中的关键技术创新，也是创业公司的主要机会。**我们已经看到 [Ayar Labs](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502183&idx=1&sn=6c02066bceb1b1df73c94cbdf5126ed4&chksm=ce9b76f9f9ecffef376df6b8795abe2af4a28efbc647293e288ab7c2fccb1672aea5c3f0e353&scene=21#wechat_redirect)、Xconn 等公司拿出了成熟的设计方案、甚至已经进入流片环节，对于大公司而言，这类公司也是它们的潜在收购标的。而在其他互联环节，更多则是常规技术路径升级，存量头部公司拥有极大优势，适合通过二级投资来捕获行业增长的 beta。

**4. Google 和 Broadcom 的联盟最有机会挑战 Nvidia 。**Nvdia 在单卡性能、系统构建和生态兼容性上都有明显优势，GB200 的出现极大削弱了其他玩家单点突破的可能，只有拥有完整的大内存系统才能形成竞争。在只有 Fat-tree 互联架构难以继续扩展，且 NV 探索的 Dragonfly 架构受阻的情况下，Google 和 Broadcom 的组合才有可能凭借多年在 Torus 的积累反超 NV。对于一级市场而言，由于大多数一级计算芯片公司在互联和系统构建上研发较弱，而一级的互联芯片公司也很难找到计算芯片来落地，导致一级 LLM 芯片投资愈发困难。

5. 对于二级公司， 除了 Nvidia、Google 和 Broadcom 三家明显优胜者外，值得关注的公司还有：

•   光模块环节：Coherent、Innolight、Marvell

•   交换机环节：Arista

•  线材：Amphenol（铜）、Credo（铜）、Coherent（光）

在一级市场上，主要有  Enfabrica 和 Xconn，做光模块的 Ayar Labs 和 Celestial AI 等公司值得关注。

**02.**

**为什么关注互联**

互联是数据中心除了计算芯片之外的第二大 Capex，我们以 Meta 的 24k-GPU 计算集群为例进行估算，Compute 部分成本为 68.2%，而互联占到了 23.9%，剩余部分则是存储、电力等。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/005.png)

要实现下一代 10X 算力的计算集群规模扩容，目前有两条路径：

1）在现有的 Fat-Tree 互联架构下扩容单交换机接口数，

2）探索新的互联架构，例如 Dragonfly 架构。

**在目前的 Fat-tree 网络架构下，RDMA 组网的集群最大 GPU 数取决于旗舰 Switch 的接口数。**现阶段，旗舰交换机有 64 个接口，不考虑延迟和阻塞问题的情况下，三层 Fat-Tree 架构将最多支持 (32x32x64=)65536 个 GPU 组成计算集群，不过因为 Oversubscription Ratio（过度订阅比，即某个网络链路的带宽与所连接终端设备带宽的比值）的原因，目前 Nvidia 也只能做到 3.2 万个 GPU 进行稳定运行 LLM 训练。

NV Quantum-X800 的推出一定程度上缓解了扩容焦虑，作为 B200 同代产品， NV Quantum-X800 提供了 144 个800G 接口，这意味着，基于 NV Quantum-X800 的**两层网络最大组网 GPU 将会是：72x144=10656，三层网络最大组网 GPU 数为：72x72x144=767232**，但是 RoCE 阵营预计在接下来两三年内仍局限于 64 个接口，IB 在训练场景的优势和份额将会扩大。

在切换网络架构上，Dragonfly 被认为是 Fat-free 的下一代架构。Dragonfly 定义了层次化的网络结构，能够灵活扩展节点数，并保证通讯的低延迟。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/006.jpg)

和 Fat-Tree 比，Dragonfly 的架构也会更适合 MoE 架构，因为 Dragonfly 架构下局部节点的通讯效率更高，也因此能带来更高的算力利用率，同时，在相同节点数的网络中，Dragonfly 需要更少的互联设备，从而带来成本和能耗上的优势。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/007.png)

不过，Dragonfly 的架构还处于探索阶段，有消息称，NVIDIA 正在探索 Dragonfly 架构下所需的网络配件。预计2027 年以后才会有产品推出。

因此，为了适配下一代模型训练，扩容仍是数据中心的升级方向。在这一背景下，首先，更多 GPU、更远距离通信的特性对互联性能提出了更高要求，其次，因为计算架构的原因，互联设备的需求增速高于集群规模的增速的， GPU 增加一系列带来的收发器、Switch 等互联设备的需求。如下图：

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/008.png)

如果我们以 Meta 24k-GPU 计算中心的 Capex 推演，在 100k-GPU 数据中心中，互联的 Capex 占比变成了 26.1%，提升了 2%+。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/009.png)

**03.**

**互联环节的技术趋势**

带来计算中心互联升级的还有技术侧的变化。提升互联与宽带的升级的关键技术有 CXL（Compute Express Link）、和 CPO（Coherent Processor Optic） ，二者交汇有望成为下一代计算中心的主要变革。

1. HBM 为 GPU和 ASIC 提供高带宽内存，高带宽能够支持模型训练和推理中的大规模并行计算，HBM 虽然提供了高带宽，但当前的内存容量有限；

2. CXL 可以将大容量 DRAM 资源共享给加速器，从而扩展 HBM 的有效容量。

3. CPO 作为光互连技术能够提供更高带宽、更低延迟的CPU-加速器、加速器-内存链路。

HBM、CXL 和 CPO 单点技术的突破都在为下一代计算中心和互联升级，当三者能够有机结合时，数据中心架构会被重构。

**CXL**

CXL 由 Intel 和 AMD 在 2019 年提出，它是对上一代计算机硬件传输协议 PCIe 的升级，能够让各个计算机部件（计算芯片、内存、硬盘和互联设备等）之间进行高速数据传输，让它们更好的协同工作。

CXL 之于 PCIe 的升级主要体现在：不仅可以提供 PCIe 的传输功能，还支持组网，从而增强了各个设备间的内存共享和互操作性，还降低了设备间的响应延迟、提升了数据传输带宽，更重要的是，CXL 协议下允许对服务器的每一个部件都分解并池化，CXL 所具备的内存池化能力也是 CXL 替代 PCIe 过程中最值得期待的变革性应用。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/010.png)

在服务器的通讯主要依赖于 PCIe Switch。GPU 能从 CPU 获取指令和内存数据，并通过 NIC 与其他 GPU 进行协作，随着 GPU 数量的增长，对 PCIeCXL  的需求也会相应递增，

在常见的服务器中，这样的通讯主要依赖 PCIe Switch，GPU 能从从 CPU 获取指令和内存数据，从 NIC 和数万张 GPU 进行协作。PCIe/CXL Switch 将在未来 3-5 年内以 30% 左右的 CAGR 从 8 亿美元扩展到 32 亿美元左右，目前中高端市场由博通全面垄断，由前博通部门主管所创立的 Xconn 计划在 25 年开始大规模量产，Xconn 在实现领先的性能的同时又能提供一定的性价比优势，作为创业团队也会在 CXL 环节威胁博通的市场地位。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/011.png)

**CPO**

CPO（Coherent Processor Optic）是一种基于光学互联技术的高速芯片间互联接口规范，CPO 的核心是通过硅光子学技术将传统互联接口集成到光学芯片上，用硅片来构建光子收发器里的所有组件，不仅从原材料角度对传统设计中的不同元件材料进行替代、整合，制作上也复用了成熟的 CPU 制造工艺，这些都有效降低了光模块（Optical Module）的成本。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/012.png)

凭借能耗和可扩展性优势，光学元件（Optics）已经在 Sever-to-Server 的互联上得到应用，例如 Meta 的 VP of Infra 就透露过， Meta 内部的 AI 训练服务器集群已基本采用 Optics，在 NVIDIA 的设计中，有望在 NVLink 6.0-7.0 时实现从电信号向光信号的转化。

伴随对计算提升，Chip-to-Chip 互联环节同样存在光学元件替换传统铜线通讯的需求，但对 Optics 的体积和成本提出了更进一步的要求，硅光子学的成熟成功解决了这部分问题，预计会成为 Chip-to-Chip 互联的主流解决方案。

**04.**

**下一代互联关键：Chip-to-Chip**

芯片层的互联涵盖了  Die-to-Die 和 Chip-to-Chip 两部分，其中，Die 间互联解决的是单颗芯片内不同 Die 之间的互联，例如，是计算芯片公司主要的迭代路径。Chip-to-Chip 则解决的是单个服务器节点内的不同独立芯片之间互联需求。

**Die-to-Die**

Die-to-Die 能够让不同的单独的硅芯片直接连接起来，从而在这些硅片之间它们快速共享数据、提升计算性能、降低延迟。Die 间互联已经成为计算芯片公司主要的迭代路径。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/013.png)

现阶段， Die-to-Die 互联主要依赖 TSMC 迭代 CoWos 来升级 2.5D 封装。TSMC COWOS 的目前年收入大概在 40 亿美元，市场预期 CoWos 未来会保持 50% 以上的 CAGR，预计未来会是很大的赛道。不过也有市场观点认为，TSMC 不太可能在落后制程上做过多 Capex 投入，这可能会带来 CoWos 长期产能不足的风险。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/014.jpg)

而在 3D 封装层面，目前 TSMC 和 Intel 只提供了概念性的技术展示，除了巨头外，我们也关注到例如 Whalechip 这样的早期团队在做类似尝试，并且技术方案更为激进。TSMC 的 3D 封装最多做到 2 层，但 Whalechip 可以做到 3 层，所以在目前巨头没有明显客户、技术和产能的明显优势下，类似于 Whalechip  这样的初创公司有机会通过自己的产品声量获得一定市场份额、甚至成为巨头公司的收购标的。

**Chip-to-Chip**

Chip 间互联主要涵盖的是 CPU、GPU 和 Network Interface Card（NIC）之间的互联，现阶段，片间互联环节的主流技术路径包括了 PCIe（Peripheral Component Interconnect Express）、NVLink-C2C和Google的TPU ICI（Inter-Chip Interconnect）。

**LLM 热潮带来对算力需求的升级，算力的可扩展性（Scalability）也成为芯片公司的重要竞争指标，NVIDIA 凭借 NVLink 在模型训练市场占据了领先优势，也驱动计算中心的互联架构的变化。**

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/015.png)

**•   NVLink**

由于 NVIDIA 不满于 PCIe 的弱性能和过慢的迭代速度，自己研发了 NVLink-C2C 来性能互联。

NVLink 协议之所能比传统 Ethernet 协议更快，根本原因是砍掉了 Server-to-Server 架构下的复杂网络功能，例如端到端重试、自适应路由和数据包重新排序等，并将 CUDA 和 NVLink 协议结合，从而实现了极高带宽和能耗的互联性能。例如 B100 采用的 NVLink C2C 速率已能做到 1.8TB/s，是 PCIEv5 128GB/s 的 14 倍左右。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/016.png)

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/017.png)

Nvidia 在在这个环节的超前布局也迫使博通的 PCIE Switch 和谷歌 TPU ICI 去追求更极致的性能，甚至采用或收购初创公司的前沿技术实现追赶。

**•   Google ICI**

Google TPU 则采用了和 Braodcom 合研的 ICI 系统，可以看到，同张主板上的 4 片 TPU 通过光缆进行互联，TPU v5p 的互联速率高达 600GB/s，是 PCIEv5 128GB/s 的 5 倍左右。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/018.png)

Broadcom 所提供业界领先的 HBM PHY 和 SerDes IP 是 Google 选择 Braodcom 的重要原因，但 TPUv6 预计将采用独立的互联芯片，类似于 Ayar Labs 所提供的技术方案，以追求更极致的互联性能，但其目前正在考量多个替代方案的性能和兼容性。

**05.**

**服务器层级的互联**

和芯片环节的互联相比，服务器级别的互联更多是在存量方案上的升级。

**Tray-to-Tray**

Tray 间互联指的是完成同一个机架内多台服务器的互联，在这一环节，主要用的产品有 Leaf Switch 和 NIC（Network Interface Card，网络接口卡）。

在 Datacenter 规模扩大过程中，服务器数量的增加一定会带来 NIC 的增长，作为连接计算设备的 NIC 成为刚需，每台服务器都需要一个或多个 NIC，Leaf Switch 的需求则来自超大 datacenter 内更高的带宽和更低的延迟通信需求。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/019.png)

•   **Tray-to-Tray NIC**

每个机架（Rack）通常会配备 2-8 个 RDMA 网卡，帮助 GPU 高效接入到数万卡集群参与大规模并行计算任务。NVIDIA Mellanox 的 ConnextX-800G 是目前性能最好的网卡，能够支持 800Gbps的数据传输速率，因为和 Ethernet 相比， Infiniband 能提供更低的延迟和更高的数据吞吐量，更适配于海量数据传输的高性能计算和数据中心场景。

在超大规模的计算集群中，每个 Rack 都可以看作一个中小规模的 GPU 集群，这些 GPU 之间也需要通过高速互联技术进行数据交换。为了追求极限性能，NVIDIA 为 500 张 GPU 以下规模的中小集群研发的 NVLink 就可以运用到 Rack 内的互联上。

NVLink 是专门用于 GPU 链接的高宽带互联，支持高达1.8TB/s的传输速率。和传统的PCIe接口相比，NVLink 可以实现更高的带宽和更低的延迟。

为了追求极限性能，NVIDIA 为 500 张 GPU 以下规模的中小集群研发了 NVLink，能实现 1.8TB/s 的互联。在超大规模的计算集群中，每个 Rack 都可以看作一个中小规模的 GPU 集群，这些 GPU 之间也需要通过高速互联技术进行数据交换，二NVLink在单个服务器主板上连接多个GPU，从而在机架内实现高效互联。

通过下图我们可以看到，每块服务器主板上有两个 NVLink 接口（红圈位置）：

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/020.png)

在 Cable 的选择上，因为 Rack 中 GPU 之间的通讯距离并不远，所以通常会采用成本更低的铜缆作为 ，而这些铜缆也会自带接口，因此并不需要光收发器（通常一个 800G 的光收发器需要 $1800），所以 CSP 们会尽可能的使用铜缆，因为成本明显更低。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/021.jpg)

Digital-to-Analog Converter

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/022.jpg)

Active Electrical Cable with Copper conductors

•   **Leaf Switch**

Leaf Switch是一种机架（Rack）级交换机，主要用于将同一机架内的多台服务器通过高速网络互联起来。它可以与服务器的 NIC 对接，从而组成机架内部的高速网络。

在 RoCE和 IB 的组网技术路径下，Leaf Switch 是必不可少的关键组件。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/023.png)

•   **NVSwithch**

为了增强中小规模 GPU 集群内部的高速互联，Nvidia 也推出了NVSwitch交换芯片。NVSwitch 可以被集成在高端GPU 内部，作为单个服务器节点内部配备多个 GPU 时的高速互联方案，实现同一服务器（Server）节点内所有 GPU 之间的超宽直连。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/024.png)

每台配备 8 个 GPU 的 Server 节点，通过NVSwitch可实现高达 14.4TB/s 的 GPU内部总互联带宽。而在标准机架内，通常可以部署 72 个 GPU，为了将这 72 个 GPU 高效互联，就需要在机架中心部署 9 台NVSwitch，并通过密密麻麻的NVLink铜线缆将它们连接起来,构建起类似于“GPU集群内网络”的拓扑。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/025.png)

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/026.png)

**但 NVSwitch 提供的还只是 GPU 的 server内部直连，但在更高层级上，为了完成整个机架内所有节点之间的高性能互联，仍需要 Leaf Switch 来完成。**因此，NVSwitch 和 Leaf Switch 的组合是异构计算环境中端到端的高性能网络的刚需。

**Rack-to-Rack**

不同 Rack 之间的互联现阶段基本只能依赖光收发器和光缆进行传输。通常距离越长的发信器价格和功耗越高，所以会尽可能选取合适的设备。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/027.png)

机架（Rack）间互联是通过 Spine Switch 将 Leaf Switch 链接来完成的。在顶级 AI 训练集群中为了确保互联性能，Spine Switch 和  Leaf Switch 都会使用同款旗舰机型。通常情况下，RDMA 网络中 Spine switch 和 Leaf switch 支持的接口数量对集群的最大 GPU 数量规模有着直接的关系和制约作用。因此，Spine 和 Leaf switch 技术的迭代和性能提升，对于建构件下一下一代超大规模 GPU 集群变得很关键。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/028.png)

在传统的 RoCE/IB 架构下，在每个机架最上方都会有一台叫做 ToR （Top of Rack） 交换机，可以将机架内的服务器进行互联。

同时，随着计算中心规模的扩大，各个 Rack 间物理距离也在不断拉长，当 rack 之间的距离超过电缆的有效传输距离时，Rack-to-Rack 的远距离高速互联就需要利用光纤来实现。**因此，在下一代大规模数据中心的搭建中，光收发器和足够长的光缆将成为必不可少的组件。**

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/029.png)

**•****Rack-to-Rack Switch**

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/030.png)

因为 Spine Switch（二层网络架构中是 Core Switch）需要负责连接下层Leaf Switch，Spine 和 Core Switch 就需要提供更多端口数量来保证支持连接多个 Leaf Switch，从尺寸和端口密度来看，Spine 和 Core 交换机也就比 Leaf Switch 更大。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/031.png)

•   **通常情况下，RDMA 组网的集群最大 GPU 数和集群中旗舰 Switch 的接口数相关。**

H100 同代的 NV Quantum-2 Switch 是 Nvidia 面向 Leaf Switch 推出的旗舰机型，有 64 个400G 接口，它首先能支持 32 张 GPU 以 400G 组成第一层网络，剩下的 32 个接口将以 400G 去与 Spine Switch 互联。

为了尽可能组成最大的集群，每个 Leaf Switch 只会和一个 Spine Switch 做一次连接，也就是说单台 Spine Switch 最多能和 64 台 Spine Switch 互联，也就是**两层网络最大能由（32x64=） 2048 台 GPU 组成，三层网络能由 （32x32x64=）65536 台 GPU 组成。**

**B100 同代的 NV Quantum-X800 有 144 个 800G 的接口，两层网络最大能由（72x144=）10656 张 GPU 组成，三层网络能由（72x72x144）=767232 张 GPU 组成。**

上面计算得出的是理想状态下 GPU 集群最大规模，而在实际操作中，为避免互联过于拥挤导致高频阻塞，还需要考虑到 Oversubscription Ratio（过度订阅比，即某个网络链路的带宽与所连接终端设备带宽的比值），行业常用的 Oversubscription Ratio 是 3：1 或是 4：1。

例如，对于连接了 32 个GPU节点的Leaf Switch ，为满足 4:1 的 Oversubscription Ratio 就需要使用 8 到 10 个 400Gbps 端口与每台 Spine Swithc相连，从确保足够的带宽、避免网络拥堵。

不过，由于 GPU 价格昂贵，工程师们通常也会在软件层面安排好数据流的延迟问题，尽可能地扩大集群规模，并保证每张卡的效率。

•   **Google OCS**

除了传统的电子交换方式，谷歌和博通也为TPU 互连网络研发了基于 OCS (光电路交换)的新型光互连架构。

OCS 是利用微机电系统(MEMS)技术制造的可动态调节角度的微小镜子阵列，通过调节每个微镜的角度来切换光信号的传输路径，进而实现光信号的交换和互连。这种设计不仅具有带宽巨大的优势，而且允许TPU互连网络在Fat Tree和Torus等不同拓扑结构间灵活切换,降低了网络迭代和运行成本。目前，OCS可支持8960个TPU单元以600Gbps的速率实现全互连。作为对比，基于IB(InfiniBand)的电子互连最多可支持 3,2768 个 GPU 以 100Gbps的速率互连，而基于 NVLink 的 GPU 直连方案则能支持最多 576 个 GPU 以 1800Gbps 的高速率互连。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/032.png)

•   **关键组件：NIC、Transceiver、Cable**

下面分别是 NIC、Transceivers、AEC 和 AOC。Rack-to-Rack 因为距离限制通常会使用光缆，但也有不少公司为了成本考量使用 AEC。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/033.png)

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/034.jpg)

目前并没有这些不同距离设备的详细拆分，但是预计主要集中在 DR 以下。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/035.png)

**Cluster-to-Cluster**

集群（Cluster） 间的互联实现主要需要使用极远距离的 Transceivers， 对其他环节的设备的影响并不大。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/036.png)

跨集群训练需要 Intercluster logical interfaces（LIF），其中，上市公司 NETAPP 很擅长这个，但是它们开发的是存储的跨云读写，并不确定对 GenAI 的影响。

**06.**

**NV 的垄断优势将在互联环节延续**

根据 LightCounting 统计，LLM 在 2023 年的普及让 IB Switch 的份额得到了跃升，并有机会在未来 5 年内和 RoCE 平分 AI Server 市场。考虑到 RoCE 下的 Ethernet Switch 需求中还包含着大量传统数据中心业务，所以**在纯 LLM workload 下，IB 的份额优势相当明显。**

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/037.png)

从目前 Nvida 所规划的技术路线上看，我更倾向于认为 NVLink+IB 的技术优势和市场份额在未来 2-3 年内持续扩大。

首先，**IB Switch 的接口数比 RoCE 有明显优势，这也意味着在训练集群拓展上有更大规模优势。**如前文所述，考虑到新一代 IB switch 将接口数从 64 个提升至 144 个，训练集群的规模能扩大 10 倍左右，而由于 RoCE 阵营在两三年内并无法做到类似的技术，所以 GPT-6 等下一代模型的训练预计都将使用 IB Switch。

**使用 NVLink 的推理集群在推理旗舰模型时有明显的性能和性价比优势，RoCE 则不太会被用在推理集群中。**在推理集群中，NVLink 和 NVSwitch 的组合凭借比 RoCE 和 IB 强十几倍的通讯速率，将 72 张 GPU 的内存互联起来，这样的大内存系统能允许更多的模型/数据/用户请求并行运算，从而达到数十倍的吞吐量、能耗比和性价比，这是 IB/RoCE 都无法企及的。**我们预计未来的推理需求将由类似 GB200 的大内存集群用来满足旗舰模型，由大内存单卡（如 B200 或 ASIC）来推理开源模型，并不太会拉动 IB 和 RoCE 的需求。**

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/038.png)

**NVLink 和 IB/RoCE 的协同通讯（Rail-optimzed Network）将巩固 NV 生态的性能优势。**Rail-optimzed Network 指的是当一 GPU 的通讯渠道拥堵时，可以将信息通过 NVLink/NVSwitch 传至同一服务器内的空闲 GPU，再传送给目标 GPU。这样的网络架构将让 NV 的交换机始终比同代的交换机保持性能优势，也有助于 NV GPU 比同代 ASIC 保持互联性能上的领先。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/039.png)

总的来说，尽管市场预计 Nvidia 未来几年在推理芯片的市占比将逐步下滑，主要是因为未来单卡便可独立推理中小模型，但是这并不影响互联环节的竞争格局，因为未来将只有高端模型的推理需要互联，而 NVLink 目前只有 TPU ICI 这个对手，考虑到目前 LLM 基于 TPU 所做的生态和优化远不及 NV，我们认为 NV 的垄断优势将延续。

**07.**

**重要公司**

**Private Companies**

•   **Ayar Labs**

海外独角兽曾经对 [Ayar Labs](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502183&idx=1&sn=6c02066bceb1b1df73c94cbdf5126ed4&chksm=ce9b76f9f9ecffef376df6b8795abe2af4a28efbc647293e288ab7c2fccb1672aea5c3f0e353&scene=21#wechat_redirect) 进行过深入分析，作为片间通讯光模块（CPO）的代表公司，Ayar Labs 通过和 Switch Chip 或 GPU 一起封装，从而解决片间通讯的带宽、延迟、距离和能耗问题。

Google TPU v6 也在尝试类似的技术，并正在测试多家 Vendors 和他们主计算片的兼容性，由于主片由博通设计，所以可知这些 Vendors 中并不包含博通；此外，博通的 Tomahawk 5 交换芯片已采用了 CPO 技术，在延迟和能耗表现上有明显提升。

**•   Celestial AI**

Celestial AI 和 Ayar Labs 一样都是做片间通讯的光模块产品，但不同于 Ayar Labs 选择和 Switch Chip 或 GPU 共同封装，Celestial AI 选择的方案是放置于 HBM 旁，让 GPU/ASIC 能远距离进行 HBM 读写。Celestial AI 已经获得了 AMD 的投资，但和 Ayar Labs 比，Celestial AI 的产品成熟度还较低。

•   **Enfabrica**

Enfabrica 是将 RoCE 和 CXL 结合，推出针对的 LLM 的交换机，既能为 AI Server 扩充内存容量并提升内存利用率，又能优化 CXL 和 RoCE 网卡的通讯效率，降低延迟。这将同时冲击博通的 RoCE 和 PCIe Switch Chip 产品线，因为客户可能会更倾向安装简化的网络设备。

•   **Xconn**

Xconn 定位于做最高端的 CXL Switch Chip，目前已设计出全球首款 PCIE5.0 和 CXL 2.0 Switch Chip，这两款并有着最优秀的总交换带宽、延迟表现和能耗比表现，预计能构建最大容量的内存池，为数据中心降本增效。Xconn 的产品比博通的旗舰芯片高 50% 的总互联带宽，更低的延迟和能耗表现，有机会抢夺博通在 CXL Swith Chip 的市场。

**Public Companies**

对于二级公司，除了 Nvidia、Google 和 Broadcom 在这三家有明显优势的公司外，值得关注的公司还有：

•   **Coherent****（COHR）**

主做光模块和光器件的公司，其子公司 Finisar 为 NV 光模块的最大供应商，几十年来都是全球最大、技术最领先的光器件供应商。

•   **Marvell****（MRVL）**

作为是一家全能的半导体公司，Marvell 不仅有行业绝对领先的光器件 DSP，在光模块领域也达成了不错的销售规模，更是接下了 AWS AI ASIC ( Trainium 和 Inferentia ) 和 Google ARM CPU 的设计订单。

•   **中际旭创** **（688389:CH）**

中国市场迅速崛起的光模块公司，根据 Lightcounting 排名，中际旭创和 Coherent 并列排名第一，是 NV 光模块的第二大供应商，凭借国内的需求优势，让其业绩不逊于 Coherent。

**•   Arista Networks****（ANET）**

一家行业领先的交换机公司，它用博通的交换机芯片为客户的各个使用场景（云计算、高频交易或 AI）设计并组装企业数据中心的交换机，再配其自主研发的操作系统 EOS，能够为大型科技公司、金融机构、云服务提供商提供针对性的云网络搭建。

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/040.png)

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/041.png)

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/042.jpg)

延伸阅读

[![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/043.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&chksm=ce9b60bbf9ece9ad6b7028fd2aa90e43dba20a6a92f9202cdd88b806dd9a18f3e0e17ce7e8e1&scene=21#wechat_redirect)

拾象AGIX指数发布：AI 时代的纳斯达克100

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/044.png)

[![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/045.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507542&idx=1&sn=9f8e8d83d2571b209f11a2d9e11bc236&chksm=ce9b61c8f9ece8dee01b9c8f59a9528934d68a9dc02a199ae5647c4dc5be4ad0bf980093b6c3&scene=21#wechat_redirect)

OpenAI联创：RLHF是超级智能的秘密武器

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/046.png)

[![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/047.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507279&idx=1&sn=a7a90282361bbdbc8885a1a44b583ada&chksm=ce9b62d1f9ecebc7b1f96c18e33e24831ca173ffebe7ca9741e9c1a6a5b0a4e80c06183d3ed0&scene=21#wechat_redirect)

AGI马拉松与大基建

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/048.png)

[![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/049.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507251&idx=1&sn=105fc33689a0a07bfa2e1131b01cc2c5&chksm=ce9b62adf9ecebbb6a4c14e42839183445e1ed7ed1f5ab735cccf51632dc74b571011210b2bb&scene=21#wechat_redirect)

Writer：企业级全栈式文字生成平台，如何对抗ChatGPT冲击？

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/050.png)

[![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/051.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507175&idx=1&sn=008f2c5a35d22397ce9fbd56b75c0d55&chksm=ce9b6379f9ecea6fef95aec53b614fe8d3f8137bbfdef2198bf451edbf8751e861b930627a37&scene=21#wechat_redirect)

Suno AI：音乐生成迎来MidJourney时刻，Suno能否挑战Spotify？

![](../images/2024-06-21-hu-lian-rang-shu-ju-zhong-xin-cheng-wei-xin-yi-dai-ji-suan/052.png)
