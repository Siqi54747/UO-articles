---
title: GenAI云计算百亿角斗场，算力之外的错位博弈
publish_date: '2023-09-21'
publish_timestamp: 1695297867
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/LQVTShU5jXWPupNOC7XWHw
msgid: 1000000223
appmsgid: 2247504793
itemidx: 1
digest: 算力是LLM的“军火”，云计算公司是当下确定性最强的受益方。
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxQUPLlrxQ8P708E5N18MFQTQWcXa6Via8BXlrpclyAYwg25EicuJv3kj9Ic6qZibYNB7tok0lWVX4aA/0?wx_fmt=jpeg
image_count: 40
archived_at: '2026-04-20T01:35:49+08:00'
---

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/001.gif)

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/002.png)

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/003.png)

作者：NCL

编辑：Siqi

排版：Scout

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/004.png)

算力是 LLM 的“军火”，作为核心资源供给方的云计算公司是当下确定性最强的受益方。

对于Azure、Google Cloud Platform 和 AWS 三大云厂商而言， LLM 是他们新的角斗场：Azure 全力下注 OpenAI ，GCP 则凭借 TPU 的充沛算力以及 Vertex AI 的配套软件，为 Gemini、Anthropic 等大模型巨头提供低成本军火，还能大规模支持 GenAI 公司的模型部署，AWS 为了在 GenAI 浪潮下保住市场领先地位，先围绕着模型开源社区做适配和引流，再以充满诚意的价格成为多家模型公司的重要算力补充。

但由于 OpenAI（Azure）和 Gemini （GCP）日益紧张的竞争关系，Azure 和 GCP 它们逐渐推迟或减少了公开释出的 Datacenter GPU，这意味着不少中小型 GenAI 将更难以获取到足够的算力。

与此同时，为了确保 LLM 生态的多元繁荣保证以强化自身的市场议价权，NVIDIA 也先后重注 Coreweave 和 Lambda Labs 两家云计算初创公司，并通过芯片资源的支持让它们将当下最紧俏的战略资源输入市场。由 NVIDIA 所扶植的“新军”正在对云计算的“旧王们”发起挑战。

我们认为，随着 LLM 格局的变化，云计算领域的利益分配可能发生变化。因为各个云计算供应商在硬件、软件和商业化上的布局不同，他们所匹配到的客户特征、用户决策偏好以及在 LLM 发展的客户需求的差异，不同阶段中所能够捕获的价值也会发生变化，我们在本篇研究中会围绕这些板块进行细节对比，尝试寻找其中的投资机会。

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 研究背景

02 硬件对比

03 软件对比

04 商业化对比

**01.**

**研究背景**

模型企业的格局和云计算厂商的市场格局相关性极高：Azure 与 OpenAI 的紧密联姻使其成为 LLM 浪潮中最直接的受益者，Google 不仅自己下场做对标 OpenAI 的顶尖模型 Gemini，还通过股权投资与和 TPU 资源合作，战略布局了 Anthropic 和 Character.ai；Coreweave 则在早期就和 Inflection 紧密协作，博得了 NVIDIA 的关注和提携。

我们打算深入研究云计算公司的初衷是，作为核心资源供给方的云计算公司当下确定性最强的 LLM 受益方， LLM 团队的技术壁垒是通过消耗计算资源做实验积累的，而最终业绩也需要计算资源交付，那么他们的业绩增速大概率是高度正相关的，**当模型公司因被市场赋予高预期、享受超高估值倍数时，云计算公司享受到的这部分确定性收益是否已经 Value-in ？**

**此外，LLM 格局的变化也让云计算领域的利益分配可能发生变化，不同背景的 LLM 参与方因其业务性质、资金储备、对 LLM 的需求深度等，在云计算供应商选择上的决策偏好不同，目前被低估、或处于 Tier 2 的玩家有机会捕获更多价值。**例如，在考虑成本的情况下， 拥有自研芯片的 GCP 和定价较低的 Lambda Labs 或 Coreweave 更吸引到这类开发者的关注。

尽管目前的主流观点是 LLM 将最终收敛于两三家巨头，但在过去的半年时间里，开源模型和一些 SaaS 公司的自研 LLM 的努力让我们看到了格局多样化的可能性，比如，Meta 作为搅局者先后开源了 LLAMA 和 LLAMA 2，让开源社区初步追上了 GPT-3.5 水平。

**关于模型格局变动，我们认为存在以下几种可能性，一旦模型格局变化，进而云计算环节的利益分配也将被搅动，目前被低估的玩家有机会捕获更多价值：**

**• Hypothesis 1: 主要算力资源将从 Training 转向 Serving （包含 Fine-tune 和 Inference）：**

尽管目前模型厂商们的精力主要放在 Training，例如目前 OpenAI 将 80% 的算力放在 Training 环节，而其他竞对还处于 Serving 阶段的更早期，Serving 的算力占用更少。我们大胆预计，在 2025 年左右，模型公司在 Serving 上的算力投入将达到 50% ，这方面迁移将对硬件上（例如自研芯片和互联方案）和软件上（MLOPs 也将从 Training 环节切换到 Serving）都提出全新的要求，也意味着会有一部分订单转至更符合 Serving 需求的云计算供应商。

**• Hypothesis 2: 顶尖开源模型对 OpenAI GPT 能力差距缩短至半代，用户开始选择基于开源模型做个性化：**

TII 的 Falcon-180B 和 Meta 的 LLAMA-2 已在多项指标上接近了 GPT-3.5，而用各个场景下的数据进行 Fine-tune 后，不仅能媲美 GPT Fine-tune 后的效果，并且降低了成本又保证了数据隐私。当免费模型和顶尖 LLM 只差半代的共识形成后，一定会有用户出于成本和隐私等考量倾向于基于开源模型自研，为了进行 Fine-tuning，用户在硬件层面会对百卡规模的集群形成需求，软件角度，也会需要一整天 MLOps 来满足 Fine-tune、Evaluation 和部署等。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/005.png)

https://www.anyscale.com/blog/llama-2-is-about-as-factually-accurate-as-gpt-4-for-summaries-and-is-30x-cheaper?ref=promptengineering.org

**• Hypothesis 3 ：LLM 的场景从效率发散到娱乐，开发者的决策从 Performance Driven 转向 Cost Driven：**

目前市场上的三大模型 GPT-4、Bard、Claude-2 基本聚焦于文案写作、代码和搜索问答这类生产力场景，与此同时，也有 Inflection 和 Character.ai 这类在陪伴和娱乐场景下发力的模型。和生产力场景不同，娱乐场景因为用户量级带来更大 inference 需求，与此同时，这些用户的付费意愿和能力却不一定比生产力场景高，因此，**就像 Youtube 和 Netflix 多年在软硬件上深挖如何降低流媒体成本一样，当 LLM 场景从生产力向娱乐场景扩散， LLM 迎来自己的 mass adoption 时，开发者也一定会更看重性价比。**这时，自研芯片或定价较低的云计算公司会成为开发者首选。

💡

Youtube 不仅在硬件上推出了专用于视频编码的 VCU，使其计算效率上有了 20 倍的提升，还在软件上屡次革新了视频编码格式，在过去的15年间推出四代编码格式，最新的 AV1 能比流媒体行业较通用的 H.264 节省 50% 的带宽。Netflix 则将 Per-Title 和 Shot-based Encoding 技巧用来改善常用的 H.264 编码格式，让老旧的设备也能享受更好的画质。

**• Hypothesis 4 ：大部分 SaaS 公司将自研 LLM，以夯实技术积累并压低成本。**

**SaaS 公司的 LLM 策略正在从分发头部模型切换至自研，意味着将有大量中型模型的训练需求。**在 LLM 初期，我们观察到市场上的 SaaS 公司 embed LLM 的方式只是将 GPT 和 Claude 能力和用户使用产品的工作流进行融合，比如，Salesforce EinsteinGPT 、 Notion AI，本质上是对模型能力的分发。但最近两个月，则出现一些变化，例如，EinsteinGPT 开始在一些场景下混用了自研 LLM，也有一些 LLM 应用开发者选择 GPT-4 为用户生成高质量回答，再用这些高质量数据去 Fine-tune 开源模型，最终在一些固定场景下能以极低的成本获得近似的效果。

显然，**混用自研模型的方式将显著改善 SaaS 公司对 LLM 模型的依赖关系，他们也能为下游用户提供更好的隐私和定价。我们预计，未来 SaaS 公司自研 LLM 将成为一股风潮，大概率基于开源模型做各个场景下的 Fine-tuning，这类开发者通常没有足够的技术和人员去打通链条的每一个环节，所以拥有良好 MLOPs 和开源社区的导流将至关重要。**

**• Hypothesis 5：技术门槛较高的关键 MLOPs 配套会显著优化获客能力和用户黏性：**

LLM MLOPs 板块，企业的可选择空间比较大，例如内部自建、第三方应用，云计算厂商也会提供基础的 MLOPs，例如 AWS Sagemaker。对于云计算厂商来说，如果能在软件侧提供**工具链中技术门槛较高的环节，也有可能因此获得更高的用户粘性，例如 GCP 在 Kubernetes 上的积累可能会成为重要考量因素，因为并不是大部分技术人员都有能力扩展 Kubernetes 到 5000 Nodes 以上。**

总而言之，我们期待上述的五股趋势将多样化模型和云计算格局，而其中也必然孕育着巨大的投资机会。

接下来，我们会从硬件、软件、商业化和服务等角度详细比较各家云计算公司的优劣势。综合来看：

• GCP（Google Cloud Platform） 的均衡实力最强，无论是在 Training 还是 Serving 板块，GCP 都有能力在各个环节都稳定地排在前三；

• Azure 目前在 Training 环节优势明显，因为和 OpenAI 的强势绑定，Azure 最先享受到了 LLM 红利，但因为计算资源和服务精力都集中在 OpenAI 上，因而客户多元化受到挑战，也无法在 Serving 环节进行充分布局；

• AWS 因为重点布局了 Serving 环节，有可能在 3 年后迎来爆发，但跟谷歌相比，主要输在 GCP TPU 的算力规模和可用性远超于 AWS 的自研芯片。和 Oracle、Coreweave 和 Lambda 相比，AWS 的优势在于软件；

• Coreweave 则在硬件和服务优势环节中有不错的整体实力。

**下表中是我们对云计算供应商在不同环节的打分**（**拾象注：**这里打分的方式是如果在某一方面，AWS > Azure ≈ GCP > Oracle > Coreweave > Lambda，那么他们的评分会分别是 6，4.5，4.5，3，2，1 )，**但并未考虑各个模块之间的重要性权重，读者可以根据心中对行业阶段、环节重要性等指标推测出权重，以达到更准确的推断。**

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/006.png)

**02.**

**硬件对比**

**Datacenter GPU：**

**云计算公司在 NVIDIA 那里所享受到的 GPU 供应优先级比绝对数量更重要。**

由于 LLM 热潮引发的显卡短缺，NVIDIA 成为了模型公司与云计算公司竞相争取的合作伙伴，大家都希望能够在供货优先级上占得先机。但 **LLM 模型公司的格局也影响着 NVIDIA 的中长期利益和地位，对于 NVIDIA 而言，LLM 市场足够多元、利益分配相对分散一定好过头部收敛，因此，为了保证自身受益的可持续性，NVIDIA 不仅会在供货时会追问每家云计算厂商服务的具体模型公司，并且还会考虑 LLM 生态均衡性、自研芯片的竞争态势和客户体量等因素，从而初步决定了下面的优先级：Azure ≈ Coreweave > AWS ≈ Oracle Cloud Infrastructure > Lambda > GCP。**

接下来我们将详细解析这个顺序背后的考量：

**• Azure:**

**Azure 和 OpenAI 的高度绑定是双刃剑。**OpenAI 在 LLM 的强势影响力让之间的强绑定让它以极高确定性享受到 LLM ，但也正是这种强绑定让 Azure 在中长期面临 GPU 拥有量下降、可服务带宽受限带来的客户拓展压力。

Azure 对于 OpenAI 大胆且富有远见的巨额投资让其先于市场一步囤积起了充沛的 GPU 资源，其中 80-90% 被用来提供给 OpenAI 进行模型的实验和训练，剩下的正在用来进行模型 Serving 环节的尝试，比如支持数亿月活的 ChatGPT 和 （Azure） OpenAI API。这使得 Azure **几乎没有冗余的算力能提供给 OpenAI 以外的客户，**我们交流到的一些模型工程师表示，当他们去找 Azure 要 A100 Instance 时常被告知并没有足够的卡。所以，**除 OpenAI 以外的模型公司通常不会把 Azure 作为主要算力供应商**。

此外，虽然 LLM 让 NVIDIA 受益，但如果 OpenAI 垄断 LLM 市场后，NVIDIA 将会因下游客户单一反而失去了定价权，所以对于 NVIDIA 而言，**LLM 生态的均衡发展才能最大化 NVIDIA 的长期利益**，也因此，为了避免 H100 被 OpenAI/Azure 独占的情况发生，NVIDIA 更倾向于正在积极寻找并扶持其他的云计算公司。

**• CoreWeave:**

**Coreweave 凭借早期与 Inflection 合作获得极高供货优先级，有可能成为最早部署十万张 H100 的云计算公司。**Coreweave 在 2023 年初便找到 Inflection 为其提供小几千张 H100，这家模型公司在后来半年里快速成长为前五的 LLM 模型公司。NVIDIA 看中了这个组合中的巨大潜力，不仅先后向两家公司投资数亿美元，并通过抬高 Coreweave 的 H100 的供货优先级来为 Inflection 提供 22000 张 H100，Coreweave 在 H100 供给上的优势甚至也吸引到了 Azure 的合作，对于算力渴求的 Azure 也和 Coreweave 签下了微软数十亿美元的多年合同，按照官网 H100 的三年预定价格（每张 H100 每小时收取 2.23 美元）看，极有可能定下了 3-5 万张 H100。**我们认为 Coreweave 可能成为最早拥有十万张 H100 的云计算公司，但其未来的总数上限还取决于 Inflection 能够有机会在下一代模型竞争中的表现，或是能否押注到另一家重要客户。**

**• AWS :**

**AWS 在早期在 NVIDIA 的供货优先级中靠后，但随着 AWS 先后和 Anthropic、Hugging Face 和 Cohere 等头部模型公司建立合作，其供货优先级正在快速爬升，成为了 OpenAI 以外的大部分 LLM 模型公司主要算力来源。**

作为最大的云计算公司，AWS 的 A100 略少于激进的 Azure，但预计在 2023 年底，AWS 能有 2.5-3 万张 H100，其中，供公开使用的 EC2 P5 Instance 就宣称将有 2.2 万张 H100。

**由于 AWS 内部大量的自研硬件（例如 Inferentia、Trainium、EFA 等）会对 NVIDIA 的产品线形成威胁，在年初时也没有优质的 LLM 模型公司作为下游客户，所以 AWS 此前的供货优先级较低。**而随着 AI/ML/LLM 的重要程度在公司内部不断提高，且和 Anthropic/Hugging Face 的合作推进顺利，AWS 的市场地位和 GPU 供给正在快速改善。

**• Oracle:**

**Oracle Cloud Infrastructure （OCI） 和 NVIDIA 有很长一段密切合作的历史，因此也属于 NVIDIA 供货优先级靠前的云计算公司，OCI 的客户群体主要为愿意长期预定的企业级客户和中型 LLM 公司，比如 NVIDIA、Cohere 和 Adept。**Oracle 属于十分积极开发并销售 NVIDIA Datacenter GPU Instance 的云厂商，比如 Oracle 是四大云里面最早公开推出 A100 Instance，也较早地将 H100 Instance 卖给 Cohere 和 Adept。优质的下游客户渠道，配合上富有诚意的合作行为，让 NVIDIA 不仅将 Oracle 的供货优先级设在 Azure 和 Coreweave 后，更是将自己的 AI/ML 模型（NVIDIA DGX Cloud）托管在 OCI 的硬件 Infra 上。

**• Lambda Labs：**

**Lambda Labs 由于体量较小专注于 On-demand 的 AI Training 市场，试图捕获长尾的中型客户，公司因下游客户群体的多样化而获 NVIDIA 的扶植。**

Lambda Labs 面向的是市场中尚未被满足的长尾需求。**大量科研机构、SMB以及开源社区需要几百或一千张左右的 A100 或 H100 来进行一些 LLM 模型的尝试**，相对于比头部公司，这类型客户的特点订单的持续时间较短（On-demand 为主），中短期内需求量大，订单不确定性较高，但云计算大厂在 on-demand 定价并不友好。**Lambda 的优势在于定价足够友好。**

因此，面对短期内的 LLM 热潮，Lambda Labs 也陷入了供不应求的状态，它们**从 Oracle Cloud Infrastructure 长期租了小几千张的 A100，赚取 On-demand 和 Long-term Reserve 之间的差价利润。**

有消息称，NVIDIA 也将计划投资 Lambda Labs，我们猜测是出于布局并扶持开源社区的模型能力，拥有大量长尾需求的 Lambda Labs 也受到了投资，也因此，我们认为 Lambda Labds 的供货优先级也会得到提升。

💡

**Lambda Labs ：**2012 年创立，2016 年转型成为一家 GPU 云服务公司，业务模式和 Coreweave 类似。根据 The Information ， NVIDIA 也将计划投资 Lambda Labs 3 亿美元，投后估值 10 亿美元。

**• Google Cloud Platform:**

**谷歌在 LLM 和 TPU 上都有令 NVIDIA 忌惮的技术积累，也因此，出于钳制 GCP 或均衡行业发展的考量，NVIDIA 并没有给到 GCP 较高的供货优先级。但我们认为，Google 并不会因此被“卡脖子”，相反，外界一定程度上低估了谷歌内部 TPU 的利用率和算力规模。**

谷歌拥有自研的 Networking 方案 OCS （针对 TPU） 和 Titanium network adapter （for H100 Instance），这样的组合完全有能力满足训练早期的实验阶段、为客户个性化的 Fine-Tune 和最后的推理。尽管和 NVIDIA 的关系并不紧密，但是 TPU 的算力规模将在下一代 LLM 的训练早期让 Google 和 Anthropic 不会被 OpenAI 甩下，甚至能比 OpenAI 有更多的算力资源进行模型 Serving。

**Networking**

为了搭建能够支持万亿参数级别的大模型训练的计算集群，除了需要成千上万个 GPU 作为节点，还要依赖高速的网络。当各个节点计算完单次的梯度计算后，需要所有节点同步这些梯度值，而单次梯度同步的通信量就高达上百 GB 量级。**如果通信时间增大，即模型训练中通信时间占比提高，往往会导致 GPU 停止计算等待数据，这将造成整体集群的算力损失（如下图）。**

因此，提升整个集群的通信速度，降低模型训练中的通信时间占比对于模型训练而言也相当重要，站在客户角度，云计算供应商的通信设备也是重要考量因素。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/007.jpg)

*网络通信*

**工程师们通常会通过重构 GPU 通讯、优化集群内的通讯和组网架构两个路径来实现对 GPU 集群有效算力的充分挖掘 。不同路径下有不同解决方案，不同云计算厂商的方案选择也各有不同。**

**1. 用 RDMA  重构 GPU 通讯：**

**RDMA 是对 GPU 之间通讯路径的重构，允许 GPU 绕过 CPU 和繁多的传统通信协议直接访问另一 GPU 的显存数据，从而实现高带宽、低延迟和低资源占用的效果。**

具体来说，传统互联方式在硬件上（如左上半图）需要将 GPU 的数据复制到系统内存上，并要 CPU 对数据进行多次处理以符合复杂的通信协议（如左下半图），再传输到另一台服务器上进行类似的操作。**这个过程中，通讯带宽严重依赖、并受限于 CPU 的性能，并且多层的协议处理过程也让延迟极高。**RDMA 的则实现了让 GPU 能绕过 CPU 和另一个 GPU 直接高效通信，是对 GPU 之间的通讯路径和相关协议的重构（如下图右侧）。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/008.png)

**RDMA 的实现可以通过 Infiniband 或  Ethernet 协议，不同云计算公司的方案选择如下：**

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/009.png)

RDMA 最早由 Mallanox 公司在 Infiniband 协议上实现，但由于 RDMA over Infiniband 的定价权和技术版权被 Mallanox 独占，许多公司便开始尝试以类似的理念和技术在 Ethernet 协议上达到类似的效果，即现在的 RDMA over Converged Ethernet （RoCE）。

**Infiniband 最显著的优势是低延迟**，RoCE 的延迟通常在 200-250ns 左右，是 Infiniband 的 2 倍左右。

**RoCE 最显著的优势是价格合理和兼容性强**，主流的交换机厂商和云计算自研方案已形成充分竞争，用户能以合理的价格获得类似的带宽（在 LLM 场景下，RoCE 能实现 Infiniband 85-90% 的性能）。此外，这些高性能 Switch 未来也能被用在传统的数据中心业务中，良好的兼容性和极长的可用生命周期带来了较低的成本。

**目前来看，Infiniband 在模型训练阶段有优势，但推理环节将由 RoCE 主导。**

Infiniband 为让 GPU 绕过 CPU 从数据库或另一个 GPU 内存上读取数据，也设计了相应的软硬件方案，全面优化好了模型训练的整个闭环，凭借出色的低延迟表现让 RoCE 较难匹敌。

但考虑到 LLM 的通用性和即将加入的多模态，推理环节一定会涉及更多元的业务场景和天量的出入（数据中心的）请求，**这使得 Infiniband 的机器集群必须要将数据转换成 Ethernet 的协议格式，从而才能和外界的业务整合。模型训练的业务复杂度难以和推理的业务复杂度相比，导致运用更广的 Ethernet 协议和硬件将有极大的兼容性和成本优势，因为它们可以随时从训练环境被转用在各类推理环境中。**

**2.优化计算集群内部的通讯速率和组网架构**

**为了进一步提升训练集群的有效算力，网络带宽和组网架构也在其中扮演了很重要的角色。**行业通常的解决方案是：先通过 NVLINK 来解决单服务器内的通讯，再运用 RDMA 交换机来解决成百上千台服务器之间的通讯。

💡

**NIC**

NV ConnectX-7(400Gbps): Azure、Coreweave、Oracle、Lambda

In-House Solution: AWS EFAv2(400Gbps)、GCP Titanium Network Adapter(200Gbps)

**RDMA Type**

Infiniband: Azure、Coreweave

Ethernet: AWS、GCP、Oracle、Lambda

**Switch-to-Switch Connection**

800Gbps: Azure

400Gbps: AWS、Coreweave、Oracle、Lambda、GCP

**首先，NVLINK 和 NVSwitch 的组合为机内互联提供了无与伦比的性能，已经成为服务器标配，各大云计算厂商均配备和 GPU 同代的 NVLINK 来最大化服务器的性能表现。**下图展示了单个服务器内的互联方案是如何实现的。绿色线条部分即 NVLINK 和 NVSwitch 组合是如何为 GPU 之间提供高达 900GBps 通讯带宽的。

需要注意的是，**为了在更大的集群上远程访问内存，每张 GPU 还会再配备独立的 RDMA NIC，从而实现对不同服务器上内存的访问。**

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/010.png)

**对于云计算厂商，在解决完单个服务器通讯速率的问题之后，他们还要对计算集群中的成百上千台服务器之间的组网架构进行优化升级。**

目前行业比较常见的组网方案如下，这个方案能支持 16000 台服务器、对应 12.8 万张 GPU（**拾象注：**单台服务器内有 8 张 GPU）的互联。目前行业内比较通用的服务器带宽为 3200 Gbps（因为单台服务器内都有 8 张 GPU，每个 GPU 各有一个 400 Gbps 的 RDMA NIC）。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/011.png)

可以额外注意一下单位， NVLINK 所提供的 900 GBps = 7200 Gbps，是常见 RDMA NIC 的 18 倍。不过当前 NVSwitch 目前只最大支持 256 个 H100 互通，所以仍需要 RDMA NIC 来组建超大规模的计算集群，未来 NVSwitch 的迭代有望支持更大的服务器集群，可能将在 Inference 和 Serving （Fine-tune 和 RLHF） 环节有显著性能优势。

**事实上，Azure 为 OpenAI 打造的服务器集群已先一步在 Switch-to-Switch 之间用上了 800 Gbps 的设备，预计 AWS 将在年底跟上，而 GCP 可能会在明年年中前完成升级。**

有 Azure 的工程师表示， 800 Gbps 可能是 H100 集群的需求上限，因为当速率达到 1600 Gbps 时，HBM3 的内存读取速率将再次成为瓶颈。**如果大模型竞争加剧，不排除 AWS 和 GCP 不计成本地从 Broadcom、Marvell  手中获取顶尖的 RDMA 设备，以增强 H100 Instance 的性能和竞争优势。**其中 AWS 已基本决定要在年底前完成升级，Broadcom JERICHO3-AI 系列交换机极具竞争力。

**此外，AWS 和 GCP 内部的自研 NIC 将带来显著的成本控制能力，作为对比， Azure 仍主要采用 NVIDIA 所提供的完整方案。**AWS 和 GCP 推出的 H100 Instance 分别采用自研的 **E****FAv2 （400Gbps） 和 Titanium Network Adapter （200Gbps），其中 GCP Titanium 是第一代产品，所以其性能仍未跟上行业主流。**Azure、Coreweave、Oracle 和 Lambda，他们采用的方案应该是 NVIDIA 所提供 400Gbps 的 ConnectX-7，所以成本较高。

**Bare Metal Instances**

• Traditional Instances: AWS、GCP

• Bare Metal Instances: Oracle OCI、Coreweave、Azure、Lambda Labs

**传统 Instances 和 Bare Metal Instances 的主要区别在于利用率和性能的 Trade-off，LLM 模型公司是 Bare Metal 服务器的新一类目标客户群体。**

传统 Instances 设计中，云计算厂商为了提高设备利用率、最大化经济效益，通常允许一台服务器上运行多个虚拟机，以供多个客户按需共享一台服务器，为了更好管理多个虚拟机，云厂商开发了 Host OS、Hypervisor （下图中绿色虚线部分）等系统和软件层，但也因此牺牲了一部分服务器资源用来运行 Host OS、Hypervisor 。Bare Mental Instances 的设计中，较于传统 Instances 去掉了VM 层，从而实现了优于传统服务器的性能。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/012.png)

因为去掉了 VM，由于 Container 之间的多租户的安全性隔离难以做到 VM 那么彻底，导致 Bare Metal Instances 的用户只能以较高的价格独占服务器，这会使云计算厂商无法享受规模效应带来的成本优势，使其定价和 On-prem 相比没有明显优势，也无法像数据库或 SaaS 那样长期锁住客户，所以在早期，**云计算厂商先前并不会化较大精力和资源在这上面，只会主推一些 Database 场景下的机器以满足客户需求，因为只有数据库和服务器在同一个机房才能最小化延迟。**

但整体上看，**Bare Metal Instances 在 Training 环节更占优势，因为客户这时需要最大化珍贵的算力资源，而在 Serving 环节，由于业务复杂度、成本等考量，传统的 Instances 大概率才能满足各个客户的多样需求。**

**Oracle、GCP 和 Azure 先前都曾主推 Database 场景下的 Bare Metal Instance，后来 Oracle 和 Azure 比较重视 AI、ML 以及 HPC 场景下的 Bare Metal GPU Instance。**由于 Database 在性能、安全和硬件认证上有较严格的要求，尤其是 Oracle Database 只有在认证过的硬件上才能有完善的功能和性能，所以 Oracle、GCP 和 Azure 在 2019 年前就先后推出了各个版本数据库的 **Bare Metal Instance**。同年，HPC/ML 成为了云计算厂商重要的业务扩展方向，其中 Oracle 和 Azure 会着重营销他们的 Bare Metal Instance，以为客户提供最极致的性能。目前 Oracle 和 Azure 都有着大量传统公司（汽车）客户。

**AWS 则通过自研的 Nitro System，将 Hypervisor 引起的资源损耗降到小于 1%。**AWS Nitro System 主要由三个组件组成：Nitro Hypervisor、Nitro Security Chip 和 Nitro Cards。Nitro Card 承担了网络、存储和协调功能，从而释放了主机处理器资源。Nitro 安全芯片强化了硬件的信任度和系统启动的安全性。这样的设计允许 Hypervisor 中的网络、存储和安全模块被简化，从而获得了极致轻量化的 Hypervisor。

下图展示了 Nitro Hypervisor 能够在各种 HPC/ML/AI 场景下达到近似 Bare Metal 99%的性能**（Bare metal performance with the AWS Nitro System）**。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/013.png)

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/014.png)

**03.**

**软件对比**

**Kubernetes**

💡

**Google Kubernetes Engine：**云厂商中功能最丰富，自动化程度最高，性能最强的；

**AWS EKS ：**因市场占有率和 Hugging Face 的导流，是云厂商中被用的最多的，功能性上也覆盖的比较全面；

**Azure AKS ：**功能最基础，虽然 OpenAI 的集群有大量的自研 tricks，但这些 tricks 并没有被移植到 Azure。

Kubernetes 是训练和部署一个中大型模型（**拾象注：**这里的中大型模型可以粗略定义为参数量大于等于 LLAMA 2 70B）的关键组件，**GKE 让 GCP 对于中大型、有技术追求的企业更有吸引力**，因为他们通常偏好自己从头开发一个参数量可观的 LLM，或是对一个中大型开源模型（如 Falcon-180B）进行继续训练。

**由于 Kubernetes 的技术门槛和必要性远比 Monitroing 和实验管理等 MLOPs 更高，而中大型公司也有一些人手能搭建这些 MLOPs，所以他们在选择云计算公司时会更看重 Kubernetes 这类技术门槛更高的功能。**

Kubernetes 主要由两大部分组成：Control Plane 和 Data Plane（如下图），而云服务公司所提供的 Kubernetes 服务通常指的是代用户运行 Control Plane 部分，帮用户选择并部署合适的 Scheduler、API Server 等部件。近两年， GCP 和 AWS 开始尝试帮助客户管理 Data Plane 部分，为用户自动选择合适的硬件配置和软件版本来运日益复杂化的工作，这种服务被称为是 Serverless Kubernetes。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/015.png)

**在 LLM 场景下，客户通常对 Kubernetes 有以下需求：**

**• Upscale:**

**Google Kubernetes Engine 在 Upscaling 的 Node 上限和 Auto-scale 的精准度和可靠性上都远超竞争对手**，这里的差距主要在自研的 API Server、Scheduler 和 Control Manager 的技术壁垒上。这里的精准度指的是 GKE 在 Auto-scale 时能精确分析工作量的大小后配以合适大小的服务器，从而以尽可能低的成本满足用户需求。AWS 为跟上这项功能推出了 Karpenter 开源项目，而 Azure AKS 仍在使用 Kubernetes 的官方版本。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/016.png)

**• Node Self-healing:**

在 LLM 长达数月的训练过程中，由数千 Nodes 组成的集群中难免有一两台机器发生问题，这时需要 Control Manager 时刻检测各个集群是否发生错误，并将出错的服务器或 Container 进行重启，再将整个集群回载到上一个保存的 Checkpoint 继续训练。**Node Self-healing 是提高训练效率的关键因素，不过由于每家 LLM 训练流程上的不同，目前的 Node Self-healing 的智能程度还有待提高。GKE 和 Azure AKS 都提供 Node Self-healing，而 AWS EKS 并没有这项功能。**

**•****Auto Updates:**

GKE 在 Updates Kubernetes 时自动化程度最高，Azure AKS 覆盖的版本多于 AWS EKS。Azure AKS 和 AWS EKS 在升级 Control Plane 时需要一些人力决策才能完成升级，而 GKE 并不需要。

**• Monitor:**

在用户开箱即用时，GKE 提供了功能最全面的可视化界面；Azure AKS 也有不错的功能覆盖，有一些功能需要一些小设置才能使用；AWS EKS 所有的可视化功能都需要设置，用户需要学习文档和各种开源项目才能使用监测系统状态。

**• Serverless Kubernetes：**

参考云计算咨询公司 SAGA 的测评中，GKE 的 Autopilot 比 AWS EKS 的 Fargate 在设置时所需的复杂度更少，部署集群的速度更快，对于一些复杂功能的兼容性更好。Azure AKS 目前并没有推出 Serverless Kubernetes。

**ML/AI OPs**

MLOPs 通常涉及四大块：数据标注、模型构建、训练和微调模型、部署模型。其中，数据标注在 LLM 场景下暂时难以被软件标准化，更多还是依靠 Scale AI 那样重人力的方式，这里不展开讨论。此外，由于篇幅限制，这一板块只涉及 LLM 场景下的 MLOPs 比较。

**ML/AI OPs 中，AWS Sagemaker 是在所有云中对开发者流程覆盖最全面，和 LLM 开源社区合作最紧密，在开发者社群里心智和口碑是最好的**；GCP Vertex AI 在模型部署环节和可视化上有一些亮点超过了 AWS，但是在模型构建和训练环节和 AWS 差距较大；Azure 目前并没有将 OpenAI 内部 MLOPs 工具链上的优势转化到 AzureML 中，这可能是因为公司将优先级放在了对 GPT 系列的部署中，也可能是认为 LLM 模型终将收敛，面向中小开发者的 MLOPs 工具长期价值不大。

**AWS Sagemaker 在 ML/AI OPs 上的优势将让 AWS 对于中小开发者团队极有吸引力，因为较小的团队通常没有精力分散到各个环节的工具开发；Azure 和 GCP 则更注重辅助用户部署他们的独占模型，而在工具链上的开发并不深入。**

**模型构建**

模型构建分为 Studio/IDE、Training Container 和 Model Hub 三个环节的需求。整体上看，因为有和 Hugging Face 多年合作关系的背景，AWS 在该环节针对 SMB、中小团队和开源社区训练模型的能力积累很深，并且也能从 Hugging Face 获得不错的引流，但对于资深和顶尖 LLM 团队来说，这几家之间的差距并不明显，因为他们都有能力、并倾向于搭建内部的工作流 Infra。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/017.png)

**Studio/IDE:** 各家的差距并不明显。

**Training Container:** 训练容器里包含着训练过程中常用的 AI/ML 框架库、数据集和 Tokenizer，这些能为用户节省下大量训练前地环境配置工作。Hugging Face Training Deep Learning Container DLC 是业界比较通用的 Container，而他们和 Sagemaker 团队进一步合作开发了针对 AWS 优化的 Training DLC，能够整合上 SageMaker distributed training 库，能支持用户使用 AWS 最先进的 A100/H100 Instances。

**Model Hub:** AWS 因和 Hugging Face 有多年深度合作的历史，能从 Hugging Face 直接导流到 AWS Sagemaker 的网页操作界面（如下图）。也可以从 Sagemaker Python SDK 里输入想要模型的 model\_id （比如下面代码中的 "bigscience/bloomz-7b1”），就可以让用户的 AWS Instance 初步加载好 Pre-Trained Model，并进行训练。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/018.png)

```
from sagemaker.huggingface import HuggingFace    
# hyperparameters, which are passed into the training job   
hyperparameters ={  
   'model_id': "bigscience/bloomz-7b1",           # pre-trained model   
   'dataset_path': '/opt/ml/input/data/training', # path where sagemaker will save training dataset  
   'epochs': 3,                                   # number of training epochs     
   'per_device_train_batch_size': 1,                    # batch size for training    
   'lr': 2e-4,                                          # learning rate used during training   
}    
# create the Estimator   
huggingface_estimator = HuggingFace(  
     entry_point          = 'run_clm.py',      # train script    
     source_dir           = 'scripts',         # directory which includes all the files needed for training    
     instance_type        = 'ml.g5.2xlarge', # instances type used for the training job       
     instance_count       = 1,                 # the number of instances used for training    
     base_job_name        = job_name,          # the name of the training job     
     role                 = role,              # IAM role used in training job to access AWS resources, e.g. S3      
     volume_size          = 300,               # the size of the EBS volume in GB       
     transformers_version = '4.26',            # the transformers version used in the training job     
     pytorch_version      = '1.13',            # the pytorch_version version used in the training job    
     py_version           = 'py39',            # the python version used in the training job     hyperparameters      =  hyperparameters )
```

不过 AzureML 和 Vertex AI 用户可以用 Hugging Face 的 Transformer Package，也能下面代码中一样快速导入到 Azure 或 GCP Instance 上，但根据 Keshav Singh 的博客分享，这种实践方式总体的代码工程量会更多一些。

**训练和微调模型**

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/019.png)

**Distributed Training:**

• Sagemaker 将常见的通讯算法针对自研的网络硬件进行了整合和优化，能更快完成 Upscaling 需求，也有自己 Complier 能够在 Kernel 算法、Dataflow 和内存管控上深度优化。

• Azure 的方案则是深度整合了 Infiniband 设备的驱动，从而发挥出 NVIDIA 全家桶的完全性能。

• GCP 的优化方向是在多卡通信的算法上优化，但因为后续他们将这一技术开源，所以总体上优势并不明显。

• 在第三方服务商中，我们也看到不少客户反馈认为 MosaicML 的分布式训练能力碾压 Sagemaker，尤其是在更大的集群上训练时。

**Cost Reduction:**

• AWS 的 Spot VMs 的覆盖的机型更多，定价清晰， 算力冗余情况不清楚；

• Azure 因为将大部分资源用于支持 OpenAI，几乎没有 A100/H100 Instance 的冗余 Spot VMs；

• GCP 所提供的定价方案比较模糊，算力冗余情况不清楚。

**Experiment Management:**

• Sagemaker 和 Vertex AI 所提供的实验管理能力差距并不大，只是在最终可视化时 Sagemaker 在团队协作功能上略有优势。

• AzureML 中所收集的实验信息不够丰富，也没有一些基础可视化的功能直观地展现出来。

• 我们在客户访谈中还看到有相当一部分客户提到他们会通过 Weight and Biases 或 Databricks 来进行实验管理，因为云计算厂商收集和展现的实验信息不够全面和直观。

**Monitor & Visualization:**

• 首先，训练过程中的 Monitor 和 Visualization 主要涉及硬件状态、实验信息和训练数据信息。

• Sagemaker 对上面的三个部分全都覆盖到了，不过似乎没有为 LLM 场景下的做功能的增删（我们将在介绍第三方方案时展开），并且由用户抱怨 AWS 的报错能力不全面，连 Input 文件类型/数据结构弄错了都没报错；

• Azure 对于硬件和系统层面的监控和可视化与 AWS 类似，但是在对模型的实验信息和训练数据信息的监控和可视化仍处于测试阶段，目前 Azure 都不让用户放入生产环境中；

• Vertex AI 不仅覆盖了三种功能，并且也整合了 Tensorboard 的一部分功能来让用户快速分析模型特点，所以在模型可视化上是三家云厂商中整体最好的。

作为第三方工具的 Weight and Biases 则在可视化产品上远超于三大云，主要差距在于内置的基础可视化功能覆盖更全，在团队协作的功能（评价或是快速导出结果）上更领先，对于 LLM 每个环节的信息的记录和展示更细致。Arize 则除了基本的可视化功能外，更强调帮助用户找出 LLM 训练数据和生成结果的 Outliers，并且甚至将 GPT-4 嵌入在工作流中，让其对数据进行辅助分析。

**Pipelines:**

目前没有看到关于 Pipeline 的评价，我们推测是由于各家都是用开源方案针对自家方案进行改造，没有太多差异化。

**Version Control:**

三家云厂商的 Version Control 都大同小异，只是不少客户会用 Weight and Biases 的前端小设计（如下图）更直观的看到训练集和模型版本之间的关系，这样也能让用户更快找到所需的版本。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/020.png)

**模型部署**

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/021.png)

**Model Hub:**

AWS 和 Azure 都能直接从 Hugging Face 上导流到 Sagemaker 或 AzureML 的 Console 界面（如下图）。不过 AWS 和 Hugging Face Inference Endpoint 所覆盖的开源模型数量更多。除开源模型外， AWS 还支持用户选取 Anthropic、Cohere、AI21 Labs 的闭源模型。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/022.png)

GCP 的生态则更为封闭，基本只支持自研的 PaLM/Imagen/Codey 模型，配合上一些很古早的 BERT/T-FLAN 等开源模型，不过近期发布会上逐渐宣布了对 LLAMA2/Falcon 的支持，封闭的情况正在好转。

**Model Monitor (Predictions):**

部署阶段的 Model Monitor 主要涉及推理结果的偏差和飘移。比如 LLM 经常会有存在问题的的 Prompts 和 Responses。

在传统 ML/AI 业务中，Sagemaker 是三大云中最领先的，甚至从 Model Monitor 中专门拆出了 Clarify 产品，让用户更快速地发现 predictions 中的问题，但在 LLM 场景下，目前三大云均没有推出更针对的产品，让第三方公司能有时机建立壁垒。

Weight&Biases 提供了更直观的 prompt engineering 的界面 （如下一图），而 Arize 则靠独特的 Embedding 算法，让用户更直观的看到有问题的 Prompts/Responses （如下二图）。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/023.png)

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/024.jpg)

**Serverless API:**

三大云主要在独占模型、个性化、稳定性和安全性等角度进行差异化竞争。其中， **AWS 胜在各项能力均衡，Azure 胜在独占模型能力，GCP 胜在微调模型的技术手段多样。**具体来说：

AWS 目前独占了 Anthropic、AWS Titan、AI21 和 Cohere 的模型，并且用户能用自己的数据集 Fine-tune 来进行模型个性化，但目前 Severless API 还无法完成 LoRA/QLoRa 等高效 Fine-tune 的算法。此外， AWS 还提供各种企业级的安全功能，保证让用户的私有数据无法被模型公司获取。

Azure 的优势在于对最强模型公司 OpenAI 系列模型的独占，但客观限制也在于目前没有足够的算力支持大规模公开服务客户，只能提供优先试用权给部分客户，并且因为算力短缺的原因，Azure OpenAI Service 目前还不支持 **Fine-tune 等私有化模型的功能。**但总体上，Azure 能够支持、提供完整的企业级安全方案，其中为奔驰云服务的合作便是有力的证明。

GCP 的模型主要是自研的 PaLM、Imagen 和 Codey，并且支持用户用自己的数据集 Fine-Tune 来实现模型个性化，并且为语言和代码模型提供 LoRA、RLHF 等多样的微调技术，以及为文生图模型进行 Style and Subject tuning。谷歌也通过 LoRA 等 Parameter-Efficient Fine-tuning 技术配合上 GCP 以往的网络安全和权限管理工具，最大程度地保障了客户的数据安全。

**04.**

**商业化对比**

**硬件和运维成本**

**云计算的硬件和运维成本主要由硬件的折旧成本，电费和机房托管成本构成，目前看，单张长期 Reserve 的 H100 每小时成本在 1.5-1.7 美元左右，而 On-demand 的 H100 成本在 1.4 -1.6 美元左右。**

**单张 H100 （含下图中的配套设备）的每小时折旧成本为 1.15-1.29 美元左右，GPU 自身的折旧成本是服务器总成本的 70-75% 左右。**大部分客户通常会购买的 HGX H100 售价为 36 万美元左右，平均每张 H100 的价格为 4.5 万美元，不过有极少一些大客户能将单张 H100 （含配套设备）的价格压到 4 万美元左右。其中光 H100 自身的售价通常为 3- 3.2 万美元，这意味着 GPU 占服务器成本的 70-75% 左右。目前行业通常将 GPU 的可用周期算作四年，这意味着单张 H100 每小时的折旧成本为 1.15 - 1.29 美元。

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/025.jpg)

**单张长期 Reserve 的 H100 的每小时电费为 0.21-0.25 美元，而 On-demand 的 H100 每小时电费为 0.13-0.16 美元。**美国 Datacenter 的一度电（kWh）通常需要 0.17 - 0.21 美元，按照 HGX 满载时的 10.2 kWh 和 95% 的利用率假设计算，大概每张 H100 每小时需要 0.21 - 0.25 美元。对于 On-demand 机器的利用率通常在 60% 左右，这时每张 H100 每小时的电力成本为 0.13-0.16 美元。在实际使用中大概率会比这个数字略低一些。

此外，机房的托管成本主要包括机房租赁和维护人员的工资通常占总成本的 5-10%，由此推出**单张长期 Reserve 的 H100 每小时成本在 1.5-1.7 美元左右，而 On-demand 的 H100 每小时成本在 1.4 -1.6 美元左右。**

**由于只有 Azure 和 Coreweave 基本采用 Infiniband 全家桶，所以其他云计算公司会因采用了 RoCE 的方案成本略低些，而 AWS 和 GCP 因自研的网络设备能更低一些，这里因没有详细数据无法展开对比。**

**定价策略**

我们从下表中可以看出，AWS 通过设置较高的 On-demand Price 和较低的 Reserve Price 以吸引更多的长期用户；而 Azure 和 GCP 的定价则对短期用户的吸引力更大。Coreweave 和 Lambda 作为后期之秀，正以极低的定价从前四大云巨头中抢走份额。**不少用户表示，他们更喜欢 Coreweave 和 Lambda “所见即所得”的定价，和四大云交流时销售总会将 Sagemaker 或是数据库等其他业务打包贩卖，让用户几乎无法算清在 GPU Instances 上所花的实际定价，也让整个议价过程变得冗长。**

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/026.png)

*Source：各家官网*

基于对 H100 的成本分析，我们对几家已推出 H100 Instances 的云计算厂商的 Gross Margin 进行推测如下：

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/027.png)

其中 Lambda Labs 的 On-demand 和 3Y Reserve Price 价格比其他两家都要低，不过有客户反馈他们需要等待较久才能用上机器，并不能像 AWS 那样大部分时间都有可用机器。也就是说，**云厂商定价需要权衡价格和集群空闲率**，低价并不意味着用户体验肯定会更好，当用户无法及时 Upscale 时他们可能会考虑空闲率更高的厂商。

在 MLOPS 套件的收费上，只有综合实力最强的 AWS Sagemaker 是收费的，Azure ML 和 Vertex AI 目前则几乎不收费，只是方便用户更容易调用 Instances 以扩大需求。Sagamaker 的定价方式是在底层硬件的定价上提高 10-20% 左右，比如 ec2.p4d.24xlarge 的 On-demand 价格为 32.77 美元一小时，而包含 Sagemaker 的 ml.p4d.24xlarge 的价格为 37.69 美元，差价为 15% 左右。

**目标客群**

基于不同云计算的定价策略，我们也对他们各自想要主攻的客户对象进行推测：

**• AWS 是云计算公司中 LLM 客户分配最均衡的**

AWS 凭借 Hugging Face 的导流和在 Sagemaker 上的积累，让其有底气在 On-demand Pricing 上预留了较高的 Margin，是目前最有能力从开源 LLM 热潮中赚上一笔的。不过它们目前想着重发展长期预定的大客户，所以将长期预定的 Gross Margin 设置的比 Azure 和 GCP 更低，近日签下 Anthropic、Cohere、AI21 合作也说明战略已取得初步成功。

**• Azure 和 GCP 是云计算公司中客户分布最集中的**

目前从 Azure 和 GCP 上都比较难订到 A100，而 H100 则几乎没有。它们都坚定的看好自研大模型，优先将 H100 Instance 留给自用。如果有冗余算力，Azure 可能更倾向留给模型推理（ Azure OpenAI Service 或 Office Copilot ）来博取更高的利润率。GCP 除自研 Gemini 外还有 Anthropic 和 Character.ai，在客户分布上略好于 Azure。Azure 和 GCP 近日连连强调将要放出 H100 Instance 很有可能是为了讨好 NVIDIA，从而获得更高的供货优先级。

**• Oracle 偏好中大型企业级客户的 Reserve 订单**

据说 Oracle 的 H100 早已被 NVIDIA、 MosaicML、 Cohere 或 Adept 给订完了，所以迟迟没有公开推出 On-demand H100 Instance。这些订单的量级都在几千张左右，属于中大型模型公司的算力补充。

**• Coreweave 主要服务超大企业级客户的 Reserve 订单**

Coreweave 庞大的 H100 供应量和较合适的定价让其成为了超大型模型公司或云计算公司的主要长期算力来源，无论是 Azure 还是 Inflection 都是最头部的显卡需求方，其客户集中度略好于 Azure 和 GCP。

**• Lambda 偏好中大型企业级客户的 On-demand 订单**

有不少客户的需求是对开源 LLM 进行继续训练和 Fine-tune，所以它们通常会需要数百或小几千的 A100/H100 进行中短期训练，Lambda 便想以极低的 On-demand 价格吸引这部分用户，以好好利用它手中的近万张 A100/H100。这样的定价配合上适当的宣传，吸引来了众多开源社区和中大型企业级客户，他们需要等待冗长的队伍后才能用上机器，这使得 Lambda Labs 的 On-demand 利用率在 80-90% 以上，接近了 Reserve 的利用率，从而能够保证一定的盈利。

此外， Lambda Labs 也利用较高的 On-demand 利用率来实现长短期价格的套利：因为 Lambda Labs 的 A100 供不应求，于是便和 Oracle 以较低价格签订了一些长期 Reverse 的 A100 Instance，再以 On-demand 价格卖给新客户。不过如果未来 LLM 的需求集中到头部大模型公司的话， Lambda 这样的套利将面临亏损的风险。**这属于在竞争激烈的行业里用创新的定价策略找到了不错的市场地位。**

**服务对比**

在成本和定价分析基础上，我们可以对不同云计算厂商更适配的主要客群画像进行分析。我们可以从上文中推测出各大云的主要目标客群和特性：

客户集中度低：AWS、Lambda、Oracle

客户集中度高：Azure、GCP、Coreweave

这也形成了显著的用户体验上的差异。具体来说**，像是 AWS、Lambda 或 Oracle 这样客户集中度低的云计算公司会更容易遇上多租户（multi-tanents） 带来的问题，比如高峰负载、Upscaling 困难和客服响应周期长等。**

💡

**拾象注：**云计算的两面性在于，想要实现可观的盈利就必须要尽可能多的任务放在现有的主机上，然而这样做却会导致客户无法获取可能的最佳体验。

**AWS 既有全世界租户最多的机房，又需要负责部署丰富的头部 LLM 模型，还深度整合了日新月异的开源 LLM 生态，很容易在短期热点事件中难以处理高峰负载。**AWS US East N. Virginia （US EAST 1）  是全世界最拥挤的机房，只要这个机房出现严重宕机，半个互联网就下线了。比如在 2021 年 12 月份的宕机，让 Amazon、Meta、Disney、Netflix、Robinhood 和 Coinbase 同时无法使用。由于最新的 AWS H100 Instance P5 系列就主要部署在这个机房，而负责 LLM 模型 Serveless API 的 AWS Lambda 也在 2023 年 7 月刚宕机过，如果再配合上未来开源社区推出类似 LLAMA2 那样的爆款，AWS 的极限承压能力将迎来新的挑战。

**多租户的需求通常是难以预测和规划的，用户 Upscaling 的需求通常在 AWS 需要更久才能被响应。**由于 AWS 模型种类的复杂性，它很难估计哪个闭源或开源模型短期内的训练或推理需求的是否会骤升，这决定了内部 GPU 有多大比例要规划给 EC2 集群（训练需求）还是 AWS Lambda Endpoint（推理需求）。如果 EC2 集群未来的规划失误，会导致一些大客户的 Upscaling 需求需要数周，甚至数月才能满足。

一位来自 Bloomberg 的 AI 工程师分享，他曾在 AWS 扩展了他的训练集群，其中有一台机器的算力利用率十分不稳定，调查了几天才知道原来是 AWS 临时添加的那台机器因空间问题而放倾斜了，导致机箱散热风道不通畅，严重影响了性能。

**多租户的需求需要表单和大量邮件来沟通和统筹，AWS 的客服处理周期远长于 Coreweave 和 GCP。**不少用户抱怨在 AWS 遇上问题时需要填写冗长的表单，或是在邮件里写繁杂的技术记录，才能在 AWS 庞大的技术客服中找到技能对口的人员。而 Coreweave 则可以直接和客户建立 Slack 群高效沟通，也因为专精 LLM 场景的硬件问题而使得技术人员更精简，通常 AWS 两三天才能解决的问题 Coreweave 能在几个小时内解决。值得一提的是 GCP 响应速度较快，可能因为先前 ML/AI 场景下的客户集中度高，总数不多。

**Reference**

1. https://www.run.ai/blog/why-kubernetes-is-the-platform-for-genai

2. https://dev.to/thenjdevopsguy/aks-vs-eks-vs-gke-2459

3. https://komodor.com/blog/the-2022-managed-kubernetes-showdown-gke-vs-aks-vs-eks/

4.https://www.pluralsight.com/resources/blog/cloud/aks-vs-eks-vs-gke-managed-kubernetes-services-compared

5. https://aws.amazon.com/cn/blogs/machine-learning/training-large-language-models-on-amazon-sagemaker-best-practices/

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/028.png)

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/029.png)

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/030.png)

延伸阅读

[![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/031.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504471&idx=1&sn=108970a82e8ffba8b648fe3eea9eb523&chksm=ce9b6dc9f9ece4dfe52bdf89524c3b1adfef27277e996b7d012b0a95247b493a2d48bdef82b6&scene=21#wechat_redirect)

11Labs：声音模态能否突围OpenAI？

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/032.png)

[![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/033.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504325&idx=1&sn=df6825d20898422e34e457da93f9c5a4&chksm=ce9b6e5bf9ece74df300126e8dd04ccbaace58be7aca52ca78a89ff3e70729ebe9cfa4ebeaee&scene=21#wechat_redirect)

“AI版YC”创始人：我们要如何跨越AI Hype Cycle？

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/034.png)

[![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/035.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504292&idx=1&sn=84a5216c74f47cb2bf5c29ceebd6aca0&chksm=ce9b6e3af9ece72cf3ccf6ae375c64adf4664e4f250926286553950ebae529682ccda33eb800&scene=21#wechat_redirect)

Jan Leike：OpenAI将如何在4年内实现超级对齐？

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/036.png)

[![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/037.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504262&idx=1&sn=845508fbe7361e6caff51ec3c2a2fb33&chksm=ce9b6e18f9ece70edbeb112bc8a10784e18887061c93e269e2d12055c8e8cd5fc69947d56775&scene=21#wechat_redirect)

Luma AI会是3D领域的Midjourney吗？

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/038.png)

[![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/039.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504173&idx=1&sn=ea5f1900311aa117848c492b224efeb9&chksm=ce9b6eb3f9ece7a5fa2715ff5bcfb2b8872b481c809063144e086e7f789eebba3adfe94ea51e&scene=21#wechat_redirect)

Alkira：SD-WAN 先驱再创业，多云网络对 GenAI 关键吗？

![](../images/2023-09-21-genaiyun-ji-suan-bai-yi-jiao-dou-chang-suan-li-zhi-wai-de-bo/040.png)
