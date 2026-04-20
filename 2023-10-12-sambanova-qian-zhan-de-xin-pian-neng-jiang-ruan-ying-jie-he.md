---
title: Sambanova：前瞻的芯片能匠，软硬结合抢滩企业LLM Serving
publish_date: '2023-10-12'
publish_timestamp: 1697112000
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/wanA5oF-YhstHgwiNgj0ng
msgid: 1000000225
appmsgid: 2247504914
itemidx: 1
digest: 提前两年布局大模型
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzXBBooNCKESiahRpbxIwlAA7WvaPuwemOEECdAyalyEnGEr2lUql2qdj61PrYPIwkYaV9kS1AqLZg/0?wx_fmt=jpeg
image_count: 38
archived_at: '2026-04-20T01:38:33+08:00'
---

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/001.gif)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/002.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/003.jpg)

作者：NCL

编辑：Siqi

排版：Gisele

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/004.png)

将 LLM 的能力和业务场景相结合、利用 LLM 把企业积累的结构化和给结构化数据转化成业务价值是市场对于 LLM 保持兴奋的重要原因。当 OpenAI 在今年 2 月推出 Foundry 时，一度被外界解读为 OpenAI 将发力企业级市场的信号，但因为聚焦于模型能力的提升、多模态以及计算资源有限等主客观因素，OpenAI 在企业级市场动作并没有外界预期的那样激进，其他闭源模型公司也有类似特征。与此同时，过去半年开源模型社区的繁荣则成为企业级模型服务的新动力，AWS 和 HuggingFace 的联盟就是一类代表。

Sambanova 是这个领域中的独特玩家。它萌芽于创新芯片架构，由 3 位芯片和 AI/ML 领域的行业传奇人物共同创立，他们在芯片、AI/ML 技术路径上的前瞻性让 Sambanova 早在 2020 年 GPT-3 刚一发布后就决定押注于 GPT 技术路径，并成功开发出了拥有创新架构的芯片产品 RDA。RDA 能够**根据不同的 AI/ML 任务动态地重新配置硬件资源和数据流，极大程度提高了硬件的通用性，从而能适应 AI/ML 领域的快速发展。**在今年 9 月发布的 SN40L 则进一步针对大模型进行优化，有望成为 Serving LLM （Continual Pre-training、Finetune 和 Inference）性价比最高的设备。

但作为初创团队和 NVIDIA 或 AMD 直接竞争科技巨头们的计算资源预算几乎不可能。因此，在 RDA 芯片基础上，Sambanova 也推出了自己的软件服务，为非科技企业客户进行模型咨询和 fine-tune，进而搭建出一套软硬件产品。Sambanova CEO 也表示，这套软硬件一体的产品 Sambanova Suite 的目标用户是 Global 2000 企业。

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 核心判断

02 行业背景

03 产品

04 团队

05 发展战略

06 争议与挑战

07 融资历史

**01.**

**核心判断**

1. **企业级应用是 LLM 的重要场景，像企业开始****使用** **SaaS 软件、云一样，围绕****企业** **LLM** **的需要****也能诞生一批重要公司****，而头部模型公司尚未在企业级市场中形成垄断优势、企业应用 LLM 的需求分层等则为创业团队提供了机会空间**。以头部模型公司 OpenAI 为例，由于当下由于顶尖模型的竞争加剧，以及 OpenAI 对微软的产品线的深度整合计划，我们认为 OpenAI 暂时没有多余的算力资源投入到企业级产品线中，这恰好是 Sambanova 等团队的窗口机会。此外，开源模型（如LLAMA-2 和 Falcon-180B）和顶尖闭源模型之间虽然存在差异但已经可以满足企业业务需求，企业用户在模型选择的偏好上不执着于闭源模型，也让 Sambanova 能将重心放在 LLM Serving 上。
2. **Sambanova 的三位****创始人****分别是****芯片和 AI/ML 领域****的****传奇人物，****在****软硬件技术路径上****有着极强的前瞻性获得成功****：**CEO Rodrigo Liang 曾是 Sun Microsystems（太阳微电子）芯片部门的资深负责人 ，创始人之一的 Kunle Olukotun 则是多核处理器奠基人 ，另外一位创始人则是积极活跃在各大 ML/AI/LLM 社区的意见领袖以及连续成功创业者 Christopher Ré。Sambanova 公司内部承接了大量 Sun Microsystems 的芯片部门的员工，虽然是一家创业团队但已经从上至下拥有充足的芯片开发经验和供应链管理能力，过去两年中，围绕大模型技术路线和对应的产品线，团队也培养了数十名 LLM 模型工程师，已在 Serving 环节的服务部署上搭建了先发优势，近期，团队也开始从 GCP 和 AWS 引入云计算关键高管，希望能降低客户的使用门槛。
3. **公司在 2020 年就预见了 GPT 等超大模型的爆火，也因此提前布局、成为** **LLM 初创公司里最早能拿出全套自研软硬件解决方案的****团队****。**在 2020 年，团队在自己的初代芯片设计中就预见性地向 GPT 倾斜、开始走超大内存路线，并在在同年开始组建 LLM 训练专家小组，2021 年 11 月份就开发出了第一个完整解决方案。而今年 9 月发布的 SN40L 则已经为上万亿参数的 MoE 模型做好准备，有望成为提供 LLM Serving 环节（Fine-tune 和 Inference）性价比最高的服务器。在开源模型不被顶尖模型甩下的前提下，公司已比众多竞争对手在服务中大型传统企业的综合能力上积累了 1-2 年的先发优势。
4. **无论是芯片还是软硬件解决方案都获得了客户和市场的认同：**公司硬件的主要客户为三家知名的国家实验室，分别是 Lawrence Livermore National Lab（美国），Argonne National Lab（美国），RIKEN Center（日本），而在软硬件一体的产品线上，公司已经成功进入到非科技大型企业市场，其中就包括 OTP Bank 和 Accenture，并且 Accenture 将帮助公司接触到更多的传统企业，CEO Rodrigo Liang 认为 Sambanova 的长期目标是服务 Global 2000 的大型企业。
5. **开源闭源模型能力****格局****、Serving 环节竞争对手****众多以及当** **GPU 算力短缺缓解****后 OpenAI 等头部模型玩家在 LLM Serving 上的投入是公司要面对的竞争****。**一旦闭源模型对开源模型形成碾压性优势，相当一部分企业客户会因为模型能力被虹吸至头部模型，LLM 企业级服务市场格局因此发生变化，仅依赖开源模型会十分被动，晋以来；开源模型 Serving 是一个竞争激烈且高度同质化的赛道，除了 AWS 和 Huggingface 以及 Databricks 和 MosaicML 两大联盟外，还有 OctoML 等许多初创公司，竞争激烈将意味着市场和利润空间或将面临严峻挑战；而一旦 OpenAI 获取了足够的 GPU 算力，配合上微软的企业客户渠道，Sambanova 的市场空间将显著收缩；Sambanova 以 on-prem 的服务实施对于技术支持团队门槛很高，当公司进入业务扩张期会带来人才供给挑战。

**02.**

**行业背景**

OpenAI 对 GPT 模型的不断迭代优化（包括 Scaling、Instruct-Tunning 和 RLHF）赋予了其多项令人瞩目的能力，使得它在几乎所有传统的自然语言处理（NLP）任务中都表现出色。随着 LLM 时代在去年末正式开启，以及**未来多模态（包括图片和视频信息）的加入，能够理解结构化和非结构化数据的 LLM 大概率会替代许多软件工具，越来越多的企业也已经开始尝试引入 LLM 以挖掘出更多数据业务价值。**

但客观来说，对于绝大多数企业客户而言，现阶段的以 GPT 为代表的大模型在企业级市场仍有诸多无法被满足的痛点，要真正和企业业务耦合、创造价值还需要相当考虑到以下几方面问题。而 OpenAI 以及其他头部模型公司目前因为更多专注于模型能力提升，无论是考虑到激烈的模型能力竞争、还是有限的算力资源都无法投入开发精力在短期内进行解决。

• **软硬件结合的难度高：**大模型的服务器集群和训练过程是一个费时耗力的系统工程，非科技公司几乎无法自主搭建和运维迭代。即使是 Anthropic 这样拥有行业顶尖专家的团队，在早期仍花费了半年以上的时间搭建软硬件 Infra，更不要说传统企业内部的 IT 部门，保守预计整个过程可能需要 2 年以上。对于金融、零售、医药等大型非科技企业而言，让它们从硬件底层开始搭建一套 LLM 显然会导致高昂的摸索成本，这也是历史上这类企业在技术需求上普遍喜欢找技术咨询公司的原因。随着模型和数据集的不断增大，模型的复杂性也在增加，这还将进一步增加了模型调整和训练的难度。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/005.jpg)

•**共用模型难确保数据隐私：**ChatGPT 目前是所有人共享相同的模型，这也导致出现不少严重的隐私问题。比如三星员工将公司源代码和会议纪要放入 Prompt 后，这个信息将可以被 OpenAI 合法获取。此外， ChatGPT 的聊天历史数据库也在 3 月份发生过权限混乱 Bug，不少用户可以看到其他用户的历史聊天。在隐私的考量下，许多传统巨头（JP Morgan、高盛、三星等）严令禁止员工在工作中使用 ChatGPT，但他们又将需要大语言模型提供的效率提升，如何在保证隐私的前提下在把业务和大模型相结合已经是一个普遍需求。

• **企业的个性化需求满足：**长期来看，给予大模型个性将是 ToB 模型公司最重要的功能之一，本质上企业需要让模型更能够理解自己的业务，除了不同行业间的区分外，即使是在同一领域，不同企业因为业务特性、客户构成等细节上也存在差异，例如主张 PLG 策略和大客户策略对应的市场推广内容风格就完全不同。比如，Adobe CTO 创立的 Typeface 主张为每个企业客户提供个性化的模型，不仅能倾向采用用户的偏好色系和产品图片，也能根据用户的历史文案口吻，生成更个性化的文案。企业的个性化需求也决定了现阶段 GPT 等闭源模型无法和业务结合得特别彻底。

• **自主掌控信息的时效性：**当下 GPT3.5 和 GPT4 的数据都只截至到 21 年 9 月，显然当下的通用大模型显然无法做到高频地更新信息。但落地到企业实际业务中，许多信息需求都是有时效性的，尤其是在金融和科技行业。但是在企业自主掌握模型后，可以将公司最新的研报等信息喂入。

• **模型可审计性和所有权归属界定：**可审计性指的是能看到模型的 Weights 和训练数据集，因为企业客户要规避侵权和偏见等问题，所以对于模型可审计性有需求，但显然这些都属于 OpenAI 的商业机密，几乎不会共享给客户。所有权则是确保在学习了内部资料的模型能掌控在企业自己的计算中心里，不会被 Azure 等云计算厂商长期绑定（Vendor Lock-in），避免未来被天价收费。**所有权也一定程度影响了投资人对公司的技术壁垒预期**，比如 Salesforce 利用好以往积累的数据来训练自研模型后，对于 OpenAI 依赖的减少显著改善了其市场地位。

除了闭源模型的特性本身和企业实际需求之间的摩擦外，GPU-Centric 的计算单元设计本身也为 LLM 的应用带来挑战，如内存带宽不足、可扩展性受限、性价比较低，以及软硬件迭代周期矛盾等问题。而这些也正是拥有深厚芯片设计背景的 Sambanova 团队在当时看到的机会。

具体来说：

1. **内存迭代和算力升级之间的失衡带来算力浪费：在过去 20 年里，内存读写带宽的提升幅度是计算性能提升的 1/3000，导致 GPT 或推荐系统中的算力使用率不高。**如下图中展示的那样，内存读写带宽用了二十年提升了 30 倍，算力性能却在同期里提升了 90000 倍。这使得 GPU 中的计算单元经常要等待内存拿取所需的数据，比如有博主在用单张 A100 在没有进行内存优化时训练 GPT-2 时，受限于内存读取效率，算力使用效率只有 35.7%。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/006.jpg)

*内存读写带宽用了二十年提升了 30 倍，算力性能却在同期里提升了 90000 倍。*

2. **不断读写数据带来的算力利用率低：另一个导致计算效率不高的原因是传统冯诺依曼架构中的缺陷，数据在计算单元和内存单元之间读写的读写频率过高，这使得读写带宽不高的情况进一步恶化。**传统冯诺依曼架构（如下左图）下，数据要不断地在计算单元和内存单元之间读写。比如计算矩阵乘法中，计算单元通常是将矩阵先拆小后分而治之（如下右图），从中可以推测出过程中反复读写的频次是极高的。这在内存带宽已严重不足的背景下，进一步恶化了计算单元的利用率。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/007.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/008.png)

3. **具有较高读写速率的 HBM 方案受限于制造和安装复杂性，拓展能力弱，仍未解决内存和计算资源错配的问题：尽管 HBM 相较于 DDR 内存有高带宽、低能耗等优势，但却丧失了更换灵活性。**HBM 的设计下，内存需要用 Silicon Interposer（一种特殊材料） 和计算芯片连接，基本这意味着 HBM 内存的配置直接由制造环节决定、后期无法灵活更换。灵活性的缺失导致芯片厂商必须提前预判市场需求，而模型的高频迭代以及多模态功能的加入让预测变得几乎不可能，**这必将导致内存和计算资源的错配**。比如 AMD 最新推出的 MI300X 加大了先前发布的 MI300A 中的内存容量，优化后的计算内存比让产品比 Nvidia 的 H100 在 LLM 市场里更具性价比。**此外，错配的另一个原因是 HBM 的制造和安装有更复杂的技术要求，导致 HBM 可扩展能力远小于 DDR**。当前 GPU 最大能配置的 HBM 内存容量为 192 GB，但如果采用 DDR 内存则轻松能上 TB 级别的容量，不过这样的代价是对于内存读写密集型算法（比如 GPT 和推荐系统）会运行的特别慢，因为 DDR 内存的带宽通常只有 HBM 的 1/10 左右。

4. **LLM 参数量的骤升让 GPU 集群 TCO（总体拥有成本） 极高**：尽管在 MoE/LoRA/Quantization 等技术应用下，训练模型的成本有明显的下降，但是上万亿参数的 LLM 仍需要极大的内存空间，比如 1.8 TB 的 GPT-4 被爆（来自 SemiAnalysis）采用了 128 张 A100 的集群进行推理，（以 $1/hour/A100 计算，这是市场上最便宜的长期预定价格）需要企业每年为此支付 1121 万美元。更夸张的是，若企业需要经常 Finetune 甚至 Continual Pre-training 模型，则需要上千张 A100，每年的花销将达到上亿。换言之，**HBM 带来的性能提升是以极高的 TCO（总体拥有成本）作为代价的，而 LLM 参数量的骤升让这个问题快速显现并恶化。**

5. **硬件和软件迭代周期之间的矛盾让专用 ASIC 芯片方案失效**：LLM 和 Diffusion 模型的大浪下，科技巨头们如微软选择专有ASIC 芯片作为对应方案，ASIC 的优点在于其在特定任务上的高效性和低能耗，然而，其设计和制造周期之长，使其难以跟上 AI 算法的更新速度，例如即便像 NVIDIA 这样的垄断巨头，也仅能将芯片的迭代周期维持在两年一次，但这在日新月异的 AIGC 算法前显然不够，MoE 和多模态等新技术的加入将让现在根据 ChatGPT 设计的 ASIC 难以满足。

基于以上 LLM 在软件和硬件上所面临的问题，Sambanova 自 2020 年开始便将公司重心收敛到 LLM 上，并在 2021 年 9 月份便落地了整套产品。

**03.**

**产品**

SambaNova 的核心产品其创新架构芯片，该芯片的诞生源于团队对 GPT 以及大模型押注，但拥有丰富经验的团队自创立之初便意识到，**对于芯片公司而言，找到正确的技术路线和持久的计算场景，都是其能否在激烈的市场竞争中立足的关键因素**。据 Omdia Market Radar：Top AI Hardware Startups 报告统计，2018 年以来，风险投资在 25 家芯片公司中投入了 60 亿美元，但目前仍活跃在市场上的只有不到 5 家。即使是业界巨头，Intel 也因为在过去十年中误判技术路线和目标市场，导致其地位逐渐下滑。

现阶段，SambaNova 的产品是一套软硬件结合的全栈（full-stack）方案，Sambanova GPT Suite，它能够为非科技公司在其业务场景整合包括 GPT 在内的 LLM 服务 ，在最新一代芯片 SN40 的发布中，CEO Rodrigo Liang 表示，Sambanova 的目标是服务于 Global 2000 中的企业。

**硬件**

Reconfigurable Dataflow Unit (RDU)

**RDU 是 SambaNova 在 2020 年推出的芯片产品，能为多种 AI/ML 算法提供通用的加速，其最核心的创新在于使用了极为灵活的 Reconfiguarable Dataflow 架构，这一架构能够根据不同的 AI/ML 任务动态地重新配置硬件资源和数据流，从而允许开发者根据需求高自由度地撰写 Complier，极大程度提高了硬件的通用性，从而能适应 AI/ML 领域的快速发展。**

GPT-3 系列的发布Sambanova 在 2020 年便将团队重心放在针对 GPT 技术路线的软硬件优化上，不仅为其设计了 Dataflow 以加速训练和推理，并且也在今年 9 月发布第四代产品 **SN40L，L 代表专为大模型优化：SN40L 的设计中引入了三级内存的设计，内存高达 1.5 T的内存，可以支持 25.6 万个token的序列长度，SN40L 有望成为 Serving LLM （Continual Pre-training、Finetune 和 Inference）性价比最高的设备。**

SambaNova RDU 的芯片结构相当复杂（如下图），该结构被命名为 **Reconfiguarable Dataflow Accelerator**，其中的组件包括：

• Pattern Compute Unit （PCU）：计算单元；

• Pattern Memory Unit （PMU） ：由 SRAM 制成的内存单元；

• Switch：负责高效连接 PCU 和 PMU；

• Address Generator Units （AGU） 和 Coalescing Units （CU） ：共同负责连接电脑的其他部分，比如 off-chip 的 DRAM 内存、硬盘或网卡等资源。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/009.png)

**RDU 最核心的创新在于引入了 Reconfiguarable Dataflow 的概念，它允许用户能够根据不同 AI 算法定制自己的数据流水线（dataflow）。**我们可以通过下面两个例子来感受 Reconfiguarable Dataflow  的高效和通用性：

• **简单的卷积神经网络（CNN，常用于计算机视觉场景）**：下图为 Sambanova 的工程师为一个简单的 CNN 设计了一条 Dataflow，可以看到芯片从 DDR 内存单次读取样本后，就能在片上完成完整的计算过程，避免多次读写 DDR。而对于这样小型的 CNN，片上不同的计算单元还能同时处理不同的样本，就像工厂里的流水线。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/010.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/011.png)

• **GPT 解码器中的 Feed Forward Neural Network：**SambaNova 的工程师们参考 GPT-3 13B 的参数设置重新训练了一个 GPT，在根据 GPT 的结构设计对应流水线后，在 RDU 上的训练速率上成功比 A100 快了 4.5 倍。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/012.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/013.png)

*（具体论文参考：TRAINING LARGE LANGUAGE MODELS EFFICIENTLY WITH SPARSITY AND DATAFLOW）*

下图中展示了传统架构和 Dataflow 架构在处理 GPT Decoder的 Feed Forward Neural Network 时的区别，其中蓝框表明是存储在 SRAM 上。他们最大的区别是对于 HBM/DDR Memory 的读取次数，Dataflow 的合理运用将有效减少内存读写的浪费。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/014.png)

**除 Dataflow 外，最新一代芯片 RDU SN40L 的设计还加入了520MB SRAM (300 TB/s)、64GB HBM3 (3 TB/s) 和1.5 TB DDR5 (0.3 TB/s)三级内存方案，基于这一设计我们预估 Sambanova 能将计算集群的总拥有成本（TCO）降至 GPU 的 1/25（下文会进行详细分析），也让 RDU 有机会成为 Serving（包括 Fine-tune 和 Inference ） LLM 环节中最高性价比的服务器。**

三级内存方案指：

• **520MB SRAM (300 TB/s):** 在芯片中四处分布的 PMU 由高性能且昂贵的 SRAM 制成，单片 SN40L RDU 中包含着 640 MB 的 SRAM，能提供 300TB/s 的总带宽。作为比较，单片 H100 上的 SRAM 为 50MB ，我们推测其总带宽应预计不会超过 50TB/s。

• **64GB HBM3 (3 TB/s)：**SN40L 将 RDU 和 HBM3 内存封装在了一起，从而能够获得接近 H100 的内存速率，化解了前代芯片的弱势。

• **1.5 TB DDR5 (0.3 TB/s)：****Sambanova 基于对 LLM 模型市场的预判，一直要求团队把 RDU 最大内存容量推至极限。**CTO Kunle 早在 2019年就预测到未来模型将会变得极大，所以在推出第一代芯片时， Kunle 就强力推动工程团队支持 1.5TB 的 DDR。

作为对比， Coreweave HGX H100 服务器里，通常由 8 张 H100 共享 1-2TB 的 DDR5 内存，总带宽在 300 GB/s，意味着平均每张 H100 有 256 GB 的 DDR5 内存和 37.5 GB/s 每秒的带宽，**远少于单张 RDU 所能读取的内存容量和带宽。**

如下为 RDU 和 NVIDIA Datacenter Chip 一些指标的对比：

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/015.png)

*注：RDU SN30 基本是将两个 SN20 用 TSMC 的技术拼接形成的，类似 Apple M1 和 M1 Pro。*

**Dataflow 和三级内存的设计组合有能力缓解我们在前面提到的当前 GPU-Centric 的问题：**

1. **Dataflow 和三级内存的深度优化将允许计算单元等待时间更少。**算力使用效率低的主要原因是计算单元要等本地内存和远距离内存的读写。三级内存的引入能让用户根据内容的常用程度依次的分布在 SRAM、HBM 和 DDR 上，从而**不仅避免不必要的读写操作，DDR 的大容量也降低了读写远距离内存的需求**。Dataflow 则允许用户将计算结果直接用在流程的下一步中，而在传统架构下计算结果通常会写回内存，而在下一步中需要再次读取，造成严重的资源浪费。

2. **远超行业均值的 SRAM 容量减少了读写数据的频率**。RDU 拥有 520MB 的 SRAM，远超 H100 的 50MB。更大的 SRAM 能节省从 HBM/DDR 读写的次数，从而降低启动读写时的总延时。

3. **DDR 和 HBM 的混用既确保了性能，也保留了一定的可扩展性**。在 SN40L 之前的产品中，Sambanova 为确保 RDU 服务器能容纳近万亿参数的 LLM，不得不以内存性能作为代价采用大容量的 DDR。而在 SN40L 的设计中，将 HBM 置于 SRAM 和 DDR 之间作为性能缓冲将明显缓解这一问题。

4. **RDU 针对 DDR 的优化能数量级降低计算集群 TCO（总体拥有成本）** 。由于单片 RDU 能支持 1.5TB 的 DDR，也意味着一台由 8 个RDU 组成的服务器就能放下 12 TB 的参数，对应着大概 5 万亿参数量的 LLM，如果换成 A100 则需要 150 张 A100 80G，既 20台服务器左右，考虑到其中浪费的互联系统和 CPU 配套设施，**Sambanova 预估能将成本降至 GPU 的 1/25。大内存的设计还可以有效避免了片间通讯的研发成本和难度**。因为基本解决了存算单元之间的错配，所以 RDU 服务器基本不太需要成百上千个 RDU 之间的通讯。不过， RDU 仍旧能够提供对 RMDA over Ethernet/Infiniband 通讯协议的支持，最大支持为 400Gb/s  ，根据我们的了解，RDU已经验证能够支持千卡规模的计算集群，所以在互联方面已基本追平行业平均水平。

5. **Dataflow 和三级内存方案允许用户针对场景深度优化。**我们在上面提到，硬件的冗长迭代周期和高企的迭代成本让市面上大部分 ASIC 公司难以跟上软件算法的高频迭代。RDU 因为支持 Dataflow 加上最新一代的三级内存方案则给予 Complier 极大的硬件调度自由度，能够灵活的根据各种 AI/ML 算法定制优化方案。**对于用户而言，Dataflow 的设计能让 Complier 指导 RDU 适应最新的算法，用户完全能将硬件的研发预算转移到 Complier 的开发团队上，缓解软硬件迭代周期的矛盾；对于 SambaNova 来说，RDU 的硬件研发成本能够在多个 AI/ML 场景下被摊平，再通过为多个客户开发 Complier 来赚取长期服务费。**

这样创新的架构将能极大加速科研机构内的一些 CV/NLP 的算法侧的实践，也因此 RDU 的最早一批客户由国家实验室、国家科研机构等构成。我们将在后文中展开这些客户和用例。

**软件**

SambaNovaGPT

**芯片行业仅靠技术创新远远不足以生存，还需要辅以合理的 GTM 策略，对于 SambaNova 来说，团队在 2022 年推出的 SambaNova GPTSuite 就是让 RDU 有机会从科研机构走向更大的企业级市场的存在，进而触及传统企业的 IT 预算****，成为企业级 LLM 的重要基础设施。**

首先，需要强调的是，**GPT 对于 SambaNova 来说是一次历史机遇**。对于 SambanNova 自身来说，开发团队从 2020 年起就将精力集中在 GPT 这单一算法上，持续在技术和产品上积累优势，站在外部机遇视角下，GPT 的强大不仅能侵蚀传统 NLP 场景，也能满足以往无法实现的长尾需求。

**SambaNova 在 2020 年 3 月就训练了一个 100B 参数的模型 ONE**，尽管当时还没有收敛到 GPT 技术路线上，**但也算是正确地选择了大参数和语言生成的路线**，在后来看到 GPT-3 惊人的表现后，团队就决心转向 GPT 路线。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/016.png)

*SambaNova 在 2020 年 3 月就训练了一个 100B 参数的模型 ONE*

**2021 年 11 月，SambaNova 为匈牙利 OTP Bank 开发了一个完整的软硬件方案 SambaNovaGPT，一个针对匈牙利语定制的 13B 参数 LLM。**这款模型的客户是 OTP Bank 和匈牙利科技部，OTP 将用其辅助移动端银行应用的运营事务，而科技部则鼓励其他匈牙利的大学、SMB 使用这项创新的技术。

💡

**我们推测，OTP Bank 的模型仅有 13B 的主要原因有两点：**

• 匈牙利语的语料库远小于英语，所以小参数量的模型就已足够得到充分训练；

• 客户的需求比较固定，只可以用一些精心定制的例子来为模型 Fine-tune 就能获得不错的效果；

**受 OTP Bank 合作的启发，SambaNova 在 2022 年 3 月推出了面向企业和政府客户的 SambaNovaGPT Suite，是一个软硬件一体的企业级大模型解决方案，也是 SambaNova 目前的主力产品。**首先团队会协助客户选取最合适的模型，再由硬件团队根据模型、训练数据和访问量大小决定需要多大的服务器。然后等模型团队会结合企业客户需求在服务器上训练好模型后，再将设备安装到客户的机房中。除了 On-prem 外，为降低用户的使用门槛，我们预计公司将推出云服务平台，我们将在后文展开。目前阶段 Sambanova Suite 的服务方式是除了 On-prem 外，我们预计，为降低用户的使用门槛，公司会推出云服务平台，我们将在后文展开。

在模型的选择上，因为 RDA 的灵活性，Sambanova 目前能够支持包括 GPT、Claude、Llama 等各类闭源和开源模型，Sambanova 也推出了自己的模型 （SN GPT 和 BLOOMChat），在具体实践中，Sambanova 的 LLM 工程师团队会结合企业需求和偏好进行模型的最终选择。

选定好模型后，将企业数据用以 Fine-tune 模型（如下图），这样就可个性化模型并提高生成准确度。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/017.png)

还有一些客户会要求开发一些更易用的软件，比如下图是公司做的一个和 PDF 内容问答的 Demo（如下图）。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/018.png)

结合公司的一些产品 Demo ，我们可以看到，其主推的是模型大小为 13B，也会支持 Automatic Speech Recognition 的模型，从而能用在客服场景中。比如公司正在帮助客户解决以下商业场景：

• 在客服人员的通话中给予一些选项和话术上的辅导，并从客户交谈中挖掘信息；

• 帮助企业处理大量的文本数据，从海量的文档中提取有价值的信息，提高工作效率。

此外，由于 NLP 的技术路线目前已收敛至 GPT 上，这使得 SambaNova 团队能集中精力针对 GPT 进行开发。其中包括：

•**硬件：**在最新一代 RDU SN40L 中采用三级内存方案，不然在训练大模型时需要额外攻关片间互联技术。

• **Complier：**团队中的 Venkat Srinivasan 为 GPT 13B 大小的模型定制 Dataflow，从而达到 A100 的 4.5x 的训练效率。

• **LLM 算法：**团队先后开发了 SN GPT（13B），BLOOMChat（176B） 等模型，是 LLM 开源社区的重要力量。

其中，BloomChat 是公司对 Bloom 进行对话风格的指令微调后所得到的多语种对话模型，有着不俗的性能和社区声量。由 50 个左右的志愿者进行的上千条偏好选择（包含 6 种语言）中，BloomChat 和 GPT-4 被选择的次数比是 45：55（下左图），而和其他开源模型对比时，用户更偏好 BloomChat 结果的占比是碾压的 66%（下右图）。但是社区内也有用户反馈模型在代码和安全性上有较大问题，代码能力可能是因为 Bloom 模型本身的训练语料中代码成分较少或质量不高，而安全性则说明 SambaNova 团队在 Alignment 能力上离一线的 OpenAI 和 Anthropic 有一定差距。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/019.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/020.png)

**CV and**

**Recommender System**

在 LLM 之前，SambaNova 也曾看好 CV 和 Recommender System 在企业内部的应用，但是因为需求和算法的碎片化，SambaNova 自身很难在积累算法和产品上的优势，所以公司内部只有少量的 CV 专家仍在支持国家实验室的科研问题，在商业场景下难以找到客户，这里我们不做展开。

**04.**

**团队**

SambaNova 的团队是我们关注这家公司的原因之一，在了解几位核心创始人的背景后，我们也更能理解其产品理念和发展战略。SambaNova  由 3 位行业传奇创立，并拥有一位拥有深厚企业和政府人脉、丰富经验的产品经理，早在 2020 年，公司就开始建立一支专注于 GPT 相关工作的模型工程师团队，目前这个模型训练团队已经发展到二三十人的规模。**为了顺应传统企业向云计算转变的大势，SambaNova 最近从 AWS 和 GCP引入了云计算领域的 Infra 和销售主管，我们因此推测 Sambanova 未来将会推出针对企业的大模型云服务。**

**Rodrigo Liang**

**- CEO & Co-founder**

**Rodrigo Liang 是一名资历深厚的芯片工程师，也有着丰厚的企业 IT 系统的 know-how 和人脉资源。**Liang 曾在 Afara Websystems 担任 VP of Engineering，Afara 是 Sambanova 现任 CTO Kunle Olukotun 在 2001 年创办的公司，Liang 是 Afara 当时最好的工程师，他主导开发的 Niagara 架构芯片（用于网页服务器）成功在 2002 年吸引来了 Sun Microsystems 的 3000 万美元收购要约（此前 Afara 只有 Seed 轮），并凭借优异的性能让 Sun 砍掉内部自研的 Honeybee 系列芯片， Liang 加入 Sun 后担任了 Sun 的多线程芯片部门 VP。2010 年， Sun 被 Oracle 收购后，Liang 加入担任 SPARC 芯片部门的 VP，推动了 Oracle 和 IBM 在企业级服务器的硬件能力升级。

Sun Microsystems 曾是 IBM 最大的竞争对手，也主导开发了 JAVA 语言。其主营业务为卖芯片和服务器为主，辅以操作系统、数据库和开发语言等软件配套。2000 年左右，Sun Microsystems  的市值曾高达 2000 亿美元，但因为忽视市场销售和运营等原因，逐渐走向没落，最终在 2009 年被 Oracle 以 74 亿美元收购。

**Liang 的背景让 SambaNova 的商业模式与大多数芯片创业公司不同：并不直接售卖芯片，而是像 Oracle、Sun Microsystems 以及 iIBM 一样向企业销售软硬件整合的解决方案。**在 Sun 和 Oracle 的工作经历让 Liang 知道，**软硬件整合对技术能力不强、数据安全要求高的传统企业（如制造业或金融业）有着显著的吸引力。****再加上每年向传统巨头收取技术服务费，我们认为这一商业模型将有助于 SambaNova 在竞争激烈的芯片行业中长久生存下来**，因为对于一个只有 200 人的小团队来说，和 NVIDIA 或 AMD 竞争科技巨头的预算（比如 Meta 内部的计算集群）几乎是不可能的。

**Kunle Olukotun**

**- Chief Technologist & Co-founder**

**Kunle Olukotun 是多核芯片理论的奠基人之一，摩尔定律能在 2006 年后没有失灵正是因为 CPU 从追求单核心性能到追求多核心协同工作。**他目前仍在斯坦福担任 CS 和 EE 的教授，每年也能指导四五篇 ML Complier 优化和 RDU 在不同 ML 场景下应用的论文，确保 RDU 能持续在最前沿的科研工作中持续找到场景。

Olukotun 曾是 Afara WebSystems 的创始人，他利用自己的前沿科研成果开发了多核多线程芯片，后来为 Sun Microsystem 设计了 UltraSPARC T1 的芯片架构，**在当时全球 Web Serving 服务器芯片里遥遥领先，比最好的 Intel 同类芯片快了 7 倍。**

在 2008 年，Olukotun 辞去了 Sun 的工作后重返 Standford，组织并主导了 Pervasive Parallelism Laboratory 和 Data Analytics for What’s Next （DAWN） Lab，前者注重软硬件结合的并行计算，后者注重数据分析等早年 AI/ML 的研究，也在这里结识了另一位 Co-founder Christopher Ré。

**Christopher Ré**

**- Co-founder**

**Christopher Re 在公司主要负责前沿的 AI 算法研究，为公司指明前沿的学术方向，也带来学界和开源社区的的合作。**

**Ré 是 Standford AI Lab 的助理教授，不仅有着出色学术成就，同时也是一位成功创业者。**Ré 凭借 2011 年发布的 Hogwild （一种流行的分布式梯度下降算法，有 2500 左右的 Citation）而逐渐变得知名，目前也持续在 Lab 里指导着 AI/ML PhD，每年负责 30-50 篇的论文。其中包括 10 亿美元估值的 Snorkel 初创团队就是 Christopher Ré 的学生。此外，Ré 曾创办过一家数据挖掘公司 Lattice，仅在一轮天使轮后就被 Apple 以两亿美元收购。

**Ré 也是知名的大模型社区 Hazy Research的意见领袖，指导着 Standford AI/ML PHD 活跃运营 Hazy Research，并协助 SambaNova 获得学界和开源社区的合作。**除了学术研究外，Ré 也热衷于对 AI 的安全、社区、壁垒或竞争格局等角度发表自己的看法，在和自己的 PHD 学生的帮助下，运营着 Hazy Research 博客。此外，这个博客经常和 Hugging Face、Together 等知名开源社区互动，最近也为公司带来和 MosaicML、Together 的合作。

**Marshall Choy**

**- VP of Product & Go-to-Market**

**Marshall Choy 是一名出色的 ToB/G 服务器的产品经理和销售主管，公司几乎所有的大客户资源都是他推动的。**

Choy 从 1998 年起就在 Sun Microsystem 担任产品经理，当该公司被 Oracle 收购后，他继续担任企业级服务器的产品经理，不过更加强调硬件与 Oracle Database 和软件的集成，并开始积累 Go-to-Market 的人脉网络。在 2018 年加入了 SambaNova 后，先后带来了 LLNL、ANL、OTP Bank 和近期日本的 RIKEN Center 等客户。此外，由于 Oracle 和 Accenture 是企业 IT 的战略合作伙伴， Choy 则利用先前的资源促成了 Accenture 和 SambaNova 形成企业 AI 的战略合作伙伴。

除去上面四位重要人物外，**公司还吸纳了大量曾在 Sun Microsystem 和 Oracle 主持 SPARC 处理器的主管和工程师**，涉及领域从上游的芯片架构、设计和编译器优化，到中游的测试、生产和供应链管控，再到下游的企业服务器集群、企业应用和 ML/AI 算法工程师。

公司在 2020 年发布了第一代芯片之后，就开始组建一个专门负责训练 GPT 模型的项目团队，目前预计该团队有二三十名模型工程师。他们的日常工作除了根据客户的需求调整模型之外，也会学习开源社区的前沿技术和参与学术讨论，同时与一些社区进行合作以共同训练模型。然而，由于公司内部还有大量的芯片工程师，这两个团队会频繁地进行交叉合作，共同探索和撰写关于 RDU 在各个领域的加速方法，以试图扩大 RDU 的应用范围。

**今年四月， SambaNova 更从 AWS 和 GCP 分别挖来了 Richard Halkett 和 Danner Stodolsky，分别负责搭建更成熟的销售团队和云计算平台**。Richard Halkett 曾在 AWS 担任了 6 年的云计算创新业务主管，更早前曾在思科担任全球销售部门的主管，十分契合 SambaNova 创新性的 ML/AI 业务销售；而 Danner Stodolsky 则先后在 Google Youtube 和 GCP 担任 VP of Engineer，预计二者的加入是 SambaNova 为搭建云计算服务进行准备。

**05.**

**发展战略**

**AI For Science**

**SambaNova 的硬件产品最早也是目前最重要的客户群体是国家实验室，公司基本只要为客户提供硬件和一些通用的软件，并不太需要做一些 Dataflow 定制化的工作，可以说是一个“钱多事少”的生意。**其中，公司和 Lawrence Livermore National Laboratory、 Argonne National Laboratory 和 RIKEN Center 的合作较为紧密。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/021.png)

Lawrence Livermore National Laboratory（LLNL） 是公司最早的合作伙伴，这家国家实验室有着全球第 6 的超算 Sierra，每年能从美国能源部拿到 5000 万美元的预算，其中 4-5 百万美元会花在计算资源上。RDU 在 LLNL 主要被用来辅助 Corona 超算集群，进行 Cognitive Simulations，这种模拟试图使用超大规模的神经网络来替代硬核的物理公式计算，所以这将需要处理百万计甚至数十亿的神经元。此外，他们也利用 RDU 极大的 SRAM 来进行一些小模型的推理，能获得远超 GPU 架构下的效率。

Argonne National Laboratory 也是一个早期客户，这家国家实验室有着全球第一的超算 Aurora，每年能从美国能源部拿到 6 亿美元的预算，其中有 1.6 亿美元会花在计算资源上。这家实验室偏好支持多个芯片初创公司，有着一个计算资源平台 ALCF AI 供科研人员申请调用，平台上有 Cerebras、Graphcore、Groq 、 Habana 和 SambaNova。RDU 主要被用在中微子物理、癌症预测和新药发现学等复杂的科研场景中，所以 Argonne 在 2022 年和 Samabnova 续签了多年的合同。Argonne 和 SambaNova 的研究员合作开发了 RDU dataflow for GNN 后，获得了 1.5-2x 的加速。

RIKEN Center 是 2023 年 3 月签下的新客户，这家实验室是日本最富盛名 ML/AI 研究所，有着当今全球第三的超算 Fugaku，每年的花销预算大概有 7 亿美元，其中有 1.25 亿美元会花在计算资源上。RIKEN 的科研人员将会在 RDU 运行复杂的 CV 算法，用来处理超清的 3D 图片。

**企业 LLM 战略转变**

**不少企业的 LLM 战略正在从分发切换到自研，这意味将有大量中型模型的训练需求。**比如，Salesforce 的 EinsteinGPT 和 Notion AI 在早期只是将 GPT3.5 和 Claude 嵌入到用户的工作流中，Salesforce 作为分发模型的角色。但最近两个月， EinsteinGPT 已逐渐在一些场景下混用了自研 LLM，从而使得自己地位进一步抬升。也有一些 LLM 应用开发者先用 GPT-4 为用户生成高质量回答，再用这些高质量数据去 Fine-tune 开源模型，最终在一些固定场景下能以极低的成本获得近似的效果。

此外，**模型的智能能力并不是企业客户决策的最重要标准**。Hugging Face 和 SambaNova 的模型工程师总结了其客户选择模型的规律：他们通常会在**一开始使用 OpenAI 来探索业务中能嵌入 LLM 的场景，但是后面会逐渐因为成本、数据安全、自主掌控技术、用户授权复杂、OpenAI API 功能贫瘠等问题，转而使用开源模型或从头自研新模型**。这时他们便会找到 Hugging Face 或是 Sambanova 这类公司寻求咨询和帮助。

**在市场时机上，OpenAI 中短期内更倾向探索智能极限，内部 80% 的算力仍用在 Training，SambaNova 可以趁现在主攻大模型的 ToB Serving。**受 Google Bard、 Anthropic 和 Inflection 的激烈竞争影响，并且由于 OpenAI 吸纳的人才主要还是模型训练的工程师，OpenAI 的人才和算力资源更倾向 Training 端。由于 ToB Serving 通常比 ToC Serving 所占用的算力资源更多，所以为保证模型竞争力的 OpenAI 还没法切换公司重心到 ToB Serving 上。SambaNova 可以抓住这两三年的窗口期，梳理开源社区在各个模型训练的技巧，为企业客户提供咨询和 Serving。

**OpenAI/Anthropic 的旗舰模型预计将长期闭源，难以允许企业私有化部署，而采用开源模型的 SambaNova 将可直接将软硬件整体放入客户的机房，提供最高级别的个性化、数据安全、模型所有权等企业需求。**OpenAI 和微软近期签下了奔驰，但 GPT 的模型仍在 Azure 云上运行，意味着 Azure 难以为类似奔驰这样的大客户做私有化部署，而奔驰将无法个性化模型，且会被 Azure 长期 Vendor lock-in，也有可能会遇上大模型带来的新云安全问题。而 SambaNova 由于将会采用开源模型，可以将软硬一体的解决方案放入客户的机房，不需要担心模型权重泄露，也能够提供最高级别的个性化、数据安全、模型所有权等企业需求。

**是否允许私有化部署将直接导致客源的差异化，SambaNova 对于数据安全有极端追求且技术要求不高的金融和制造业很有吸引力：**

• 这些领域通常有大量的专属词汇和特殊的语法体系，也会对处事流程和对话方式有严苛的要求，所以他们是急需个性化/垂直化的场景；

• 与此同时，由于行业的敏感性和对客户的保密条款，这些行业的客户愿意放弃一部分的能力来追求数据隐私；

• 最后，这些客户通常内部的技术能力不强，更倾向直接向埃森哲这类咨询公司外包完整的技术方案，而不是像 Salesforce/Notion 这些科技新贵一样既想要从 Azure 拿到能力最强的模型，又希望自己的技术团队对其改造后留有一部分的自主权。

**我们认为现在 SambaNova 和 OpenAI 的差异化竞争角度足够明显，在开源模型的能力还可以的前提下，配合 Accenture 吃下一部分 Global 2000 企业的成功率可观。**

**Open Source Gang**

**开源社区的协作和巨头的搅局策略正在显著着提升开源社区的模型能力和声量，随着优质开源模型不断涌现、市场上模型供给足够丰富和多元，Sambanova 有机会更全面地满足客户需求，团队在学习并熟知模型训练各个环节的优质项目后，能够更全面深入地为客户提供咨询和 Serving 服务。**

OpenAI 的模型训练方法是上百人和数万张 GPU 用数年的实验才试探出的工程经验，不计其数的小技巧积微成著才有了今天 GPT-4 的卓越表现，这个过程中，OpenAI 也在各个环节培养了行业第一批优质人才。只要 OpenAI 的人才流失不严重，那么以 SambaNova 的工程师人数和算力规模，将很难不被 OpenAI 的未来模型甩下。但这并不意味着 SambaNova 无法做好企业模型：

• **开源社区模型能力**

正如我们在LLM迷思中提到，多个开源社区通过合作推出了可商用的 OpenLLAMA 13B，其性能在 22 个测评指标中和原始 LLAMA 13B 性能相近。随着链路的打通和分工的明确，**我们相信开源社区的模型能力将会在未来一两年内会有超出预期的表现。**此外，SambaNova 在今年三月也和 Together 与 Hazy Research 合作了 OpenChatKit 项目，自己也下场微调了 BLOOM 模型，为算力短缺的开源社区贡献了千亿参数级别的多语种对话大模型。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/022.png)

**• 巨头的搅局策略**

当前开源社区模型能力较为突出的当属 Meta 的 LLAMA 和中东财团支持的 Falcon。虽然他们在技术工程的初期积累相对较少，但他们显然想通过支持和协助开源社区来提升自身的知名度并获取技术援助，并试图搅乱 Google 和微软的战略布局。

TII 的 Falcon-180B 和 Meta 的 LLAMA-2 已在多项指标上接近了 GPT-3.5，而用各个场景下的数据进行 Fine-tune 后不仅能媲美 GPT Fine-tune 后的效果，并且降低了成本又保证了数据隐私。当免费和顶尖 LLM 只差半代的共识形成后，不少用户便倾向于基于开源模型自研。

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/023.png)

这时候 Sambanova 不仅能依靠 SN40L 为客户省下百卡规模的计算集群成本，又已经有两三年 Servng 企业客户的经验，节省他们在 Fine-tune、Evaluation 和部署的 MLOPs 上的学习成本。

**模型云服务**

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/024.jpg)

**Sambanova 在 4 月份分别从 AWS 和 GCP 挖来了其重要的管理层 Richard Halkett 和 Danner Stodolsky，大概率将推出云服务。**Richard Halkett 曾是 AWS 的创新部门主管，而 Danner Stodolsky 则是谷歌 Youtube、Ads 和 GCP 等多个重要部门的工程 VP。回顾 SambaNova 以往的商业策略，以及 RDU 的复杂性，我们预测这个云平台将并非简单地按需提供 RDU，而是它将允许客户从 Hugging Face 等模型平台中选择合适的开源模型，提供一个用户友好的界面，让客户能够利用自己的数据进行模型的微调。最后，底层的支持则是 SambaNova 的 RDU，以及一些较通用的编译器 (Complier)。

这个全新的平台预期将大幅降低 RDU 的使用门槛，更引入了开源模型的灵活性和适应性。通过提供友好的用户界面，它将帮助那些入门级的用户（比如一些小金融机构和制造公司等）更容易地定制和应用复杂的模型，以满足他们具体的业务需求。此外，客户尝试 RDU 和模型后效果不错，可以联系 Sambanova 团队定制专用的编译器来追求极致性能，或是直接购买服务器来进一步降低成本。

我们预期，SambaNova 的这一举措将有力地推动其业务发展，特别是能更高效地配合 Accenture 满足高频且复杂的企业需求。

**06.**

**争议与挑战**

1. **仅用开源模型将面临众多竞争对手：**

**Sambanova 将依靠开源社区的 Base Model 给客户做后续的定制化服务，但这将意味着市场上任何一个拥有一定技术能力的团队都有可能成为他们的竞争者。**眼下，许多初创公司都担忧 OpenAI 的强大模型能力将在未来向 B 端市场转型后对他们形成压倒性的竞争优势，这使得这些初创公司在建立团队和吸引投资者方面面临着挑战。像是 Sambanova 和 Hugging Face 这类先前都有不错的融资额和市场地位的公司，应该**抓住初创公司不敢做，OpenAI 没来做的市场时机，努力抓住客户并打磨产品**。否则等市场已达成 OpenAI 无法甩开开源模型的共识，就会因为公司没有明显（客源/成本/产品/团队熟练度）壁垒，因市场的内卷而逐渐失去盈利能力。

然而，LLM Serving市场依然具备诱人的潜力，吸引了一众巨头和顶尖创业者的布局。不仅有 AWS 和 Huggingface，还有Databricks 和 MosaicML 等两大联盟，以及像 OctoML 和 Modular 等初创公司。前两大巨头联盟拥有充足的算力、人才和技术储备，而后两个初创公司则凭借强大的技术团队和执行力在行业内具备了相当的吸引力和竞争力。

**这是一场关乎市场机遇、技术产品优势和客户忠诚度的竞赛，任何一环的失误都可能导致竞争地位的丧失。我们认为，Sambanova 整合软硬件以及面向传统企业客户的策略在一定程度上避免了直接竞争，也有机会在早期就抓住更有价值的大型企业客户，在市场上获得先发优势。**

2. **ChatGPT 隐私和个性化问题将逐渐被解决**

尽管外部认为 OpenAI 目前仍把大量人才和算力放在 Training 上，也因此留给一些企业级 LLM 服务的机会给到其他团队，但考虑到 ChatGPT 团队（ToC Serving）的内部优先级和重视程度还是很高的。我们认为 OpenAI 现在已经在产品的隐私和个性化问题上取得了初步进展：在用户条款中明确表示不会利用用户数据进行训练，这使得大部分用户对隐私问题的担忧有所缓解；也将在近期放出 Profile 功能，这将使用户能够进行一定程度的个性化设置。

3. **算力紧缺缓解导致 OpenAI 提前转向 ToB Serving 市场**

尽管当前 OpenAI 并没有冗余的算力资源为算力占用更高的 B 端用户做私有化模型等产品，但预计到年底，随着 AMD MI300 和 Google TPUv5 的大规模上市，算力紧缺的情况有望得到显著缓解。MI300/TPUv5 因采用和 H100 不同的制程和技术方案等原因，也不用和 NVIDIA 抢 TSMC 4nm 的产能，其成本和售价大概率会比 H100 低，预计能在 Serving 环节有不错的性价比表现。

考虑到 Azure 当下已经初步尝试为奔驰等传统巨头做 ChatGPT 的简单整合，可能在年底就会利用 AMD 的芯片为企业客户做私有化部署等更能保障隐私的举措，这将使 Sambanova 面临紧迫的时间压力。

**07.**

**融资历史**

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/025.png)

**Reference**

https://sambanova.ai

https://iscaconf.org/isca2018/docs/Kunle-ISCA-Keynote-2018.pdf

https://sambanova.ai/wp-content/uploads/2021/04/SambaNova\_Accelerated-Computing-with-a-Reconfigurable-Dataflow-Architecture\_Whitepaper\_English.pdf

https://www.eetimes.com/podcasts/the-future-of-llms-compute-democratization-and-open-source-models/

https://www.servethehome.com/SambaNova-sn10-rdu-at-hot-chips-33/

https://www.engineering.com/story/hard-times-for-ai-chip-startups

https://www.nextplatform.com/2023/09/20/sambanova-tackles-generative-ai-with-new-chip-and-new-approach/

https://www.techtarget.com/searchenterpriseai/news/366552594/SambaNova-AI-launches-new-chip-the-SN40L

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/026.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/027.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/028.png)

延伸阅读

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/029.png)

Synthesia: AI Avatar的PMF样本，像PPT一样做视频

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/030.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/031.png)

GenAI云计算百亿角斗场，算力之外的错位博弈

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/032.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/033.png)

11Labs：声音模态能否突围OpenAI？

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/034.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/035.png)

“AI版YC”创始人：我们要如何跨越AI Hype Cycle？

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/036.png)

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/037.png)

Jan Leike：OpenAI将如何在4年内实现超级对齐？

![](../images/2023-10-12-sambanova-qian-zhan-de-xin-pian-neng-jiang-ruan-ying-jie-he/038.png)
