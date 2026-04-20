---
title: H100 供需分析：芯片战争将持续多久？
publish_date: '2023-08-08'
publish_timestamp: 1691495975
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/arwikTbqsGv8hBb4aqaXMA
msgid: 1000000214
appmsgid: 2247503594
itemidx: 1
digest: GPU 的短缺可能会持续到 2024 年。
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxSPicxRibqUftUiarg1Mst4hIYUh2SzSuzF1qTQiaIxw32Gh1IrgFOicpSXXPn9dYDFA3HskEhsCQduZg/0?wx_fmt=jpeg
image_count: 25
archived_at: '2026-04-20T01:25:27+08:00'
---

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/001.gif)

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/002.png)

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/003.png)

作者：Clay Pascal

编译：wenli， Lavida， yunhao

推荐人：Cage， Huaiwei

排版：Scout

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/004.png)

[**大模型的突破是以硬件算力和云计算能力的提升作为土壤的**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501716&idx=1&sn=5422dbcec1099d7a0cc9df87d18941c6&chksm=ce9b780af9ecf11c6ee9a7743d0ee7a50eba3e36baa28fba92891d5b94db93dec391d0b70c27&scene=21#wechat_redirect)**，被视为 GPU “核弹”的 NVIDIA H100 正面临有史以来最严重的缺货。Sam Altman 就直接表示，GPU 的短缺限制了 OpenAI 在微调、专用容量、32K 上下文窗口、多模态等方面的技术升级速度。**

本文编译自  GPU Utils，作者主要从供需两个视角的分析探讨了 GPU（尤其是 NVIDIA H100）会持续多久。

需求视角下，NVIDIA H100 毋庸置疑是训练大模型的刚需，根据估算，**目前市场上对 H100 的需求在 43.2 万张左右，若按每张约 3.5 万美元计算，这是相当于总价值约为 150 亿美元的 GPU**，这 43.2 万的数字尚未包括像字节跳动（TikTok）、百度和腾讯这样需要大量 H800 的企业。

站在供给侧，H100 的短缺直接受限于台积电产能，且短期内， NVIDIA 并没有其他可选择的芯片工厂。因为出货量有限， NVIDIA  对于如何分配这些 GPU 也有自己的策略，对于 NVIDIA 来说，如何保证这些有限的 GPU 流向 AI 黑马而非 Google、微软、AWS 这些潜在竞争者相当重要。

这场围绕着 H100 的 AI 军火竞赛要持续多久？答案尚不明朗。虽然 NVIDIA 表示下半年会增加供给，但目前看来 GPU 的短缺可能会持续到 2024 年。

围绕着 H100 的短缺，接下来市场上或许会进入一种“恶性循环”：稀缺性导致 GPU 容量被视为 AI 公司的护城河，从而导致了更多的 GPU 囤积，而这又进一步加剧了 GPU 的稀缺。

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 背景

02 H100 的需求分析

03 H100 供给侧分析

04 如何获得 H100

05 总结

**01.**

**背景**

直到 2023 年 8 月，人工智能领域的发展一直受到 GPU 供应瓶颈的制约。

“人工智能热潮被低估的原因之一是 GPU/TPU 短缺。GPU 和 TPU 的短缺限制了产品推广速度和模型训练进度，但这些限制很隐蔽。我们看到的主要是 NVIDIA 的股价飙升，而非研发进度受限。当供需达到平衡时，情况会有所好转。

—— Adam D'Angelo，Quora、Poe.com 首席执行官，前 Facebook 首席技术官

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/005.png)

*这些是对 GPU 供需和人工智能最重要的 CEO 和公司*

Sam Altman 则表示，GPU 的短缺限制了 OpenAI 的项目进展，例如微调、专用容量、32K 上下文窗口、多模态等。

小型和大型云提供商的大规模 H100 集群容量即将消耗殆尽。

“每个人都希望 NVIDIA 能生产更多的 A/H100”。

—— 来自云提供商执行人员的信息

“由于当下 GPU 短缺的情况，对 OpenAI 来说，使用我们产品的人越少， 对我们反而越好”；

“如果大家因为我们缺乏足够 GPU 而减少对 OpenAI 产品的使用，我们实际上会很高兴”。

—— Sam Altman，OpenAI  首席执行官

Sam Altman 这句话一方面巧妙地展现了 OpenAI 的产品已经深受全球用户的喜欢，但同时也说明了另外一个事实，即 OpenAI 确实需要更多的 GPU 来进一步推广、升级其功能。

Azure 和微软方面也面临类似情况，有匿名人士提到：

• 公司内部正在限制员工使用 GPU，大家必须像 20 世纪 70 年代的大学生为了使用电脑那样排队申请算力。从我的角度来看，OpenAI 当下正在吸走所有 GPU 资源；

• 今年 6 月，微软和 CoreWeave 的合作本质上是为了增强微软的 GPU/算力供给。

**CoreWeave ：**

云算力服务供应商，据 CoreWeave 官网宣传，他们的服务比传统云计算厂商便宜 80%。2023 年 4 月，CoreWeave 获得 NVIDIA 的 B 轮投资，并获得了大量 H100 新卡，6 月，微软也与 CoreWeave 签订协议，微软会在未来数年内投资数十亿美元，用于云计算基础设施建设。

7 月，CoreWeave 推出了与 NVIDIA 合作打造的世界上最快的 AI 超级计算机项目，以及 Inflection AI 使用支持 MLPerf 提交的基础设施在 CoreWeave Cloud 上创建世界上最复杂的大型语言模型之一。此外，CoreWeave 利用手中的 NVIDIA H100 加速卡作为抵押，于 8 月宣布完成 23 亿美元的债务融资。

总结来说， H100 GPU 的供应已经相当短缺。甚至有传言说，**Azure 和 GCP 的容量实际上已经用完，AWS 的容量也快用尽。**

而之所以短缺，是因为 NVIDIA 给到这些云供应商的 H100 GPU 供给也就这么多，随着 NVIDIA 的 H100 GPU 产量无法满足需求，这些云供应商可以提供的算力自然也开始出现短缺。

**如果要理解算力瓶颈，可以围绕以下几个问题展开：**

• 造成这种情况的具体原因有哪些？:

- 需求量有多大？如哪些领域的人工智能需求量增加相对迅速；

- 供应量有多大？NVIDIA 等 GPU 生产商的产能是否足够满足需求；

• 这种短缺情况会持续多久？GPU 的供需何时会逐渐达到平衡点？

• 有哪些方式可以有效缓解这种短缺局面？

*欢迎关注**海外独角兽**视频号*

*获取最前沿的科技行业资讯*

**02.**

**H100 的需求分析**

**从需求端分析算力瓶颈的关键问题：**

1. 具体来说，人们想购买却难以买到的是什么？

2. 目前市场上对  GPU 的需求有多大？

3. 为什么企业更偏好 NVIDIA H100 而不是采用不同的 GPU ？

4. 目前市场上的 GPU 有哪些类型？

5. 企业能够在哪里买到 GPU ？它们的价格如何？

**H100 的需求方都是谁？**

**对 H100 或 A100 的需求量在 1,000 个以上的企业：**

• **训练 LLM 的初创公司：**

OpenAI（通过 Azure 获得）、Anthropic、Inflection（通过 Azure 和 CoreWeave）、Mistral AI；

• **云服务提供商（CSPs）：**

除了 Azure、GCP、AWS 三巨头外，还有 Oracle，以及 CoreWeave、Lambda 这样的 GPU 云供应商；

• **其他科技巨头：**

例如 Tesla （**拾象注：**原作者在此处未提及的 Meta、Apple 等巨头也对 GPU 存有大量需求，Google 主要使用 TPU 处理计算，对 H100 的需求主要是 Google Cloud Platform）。

除了上述企业外，如果企业需要对 LLM 进行大量微调，也需要储备至少 100 张以上的 H100 或 A100。

对于采用私有云（CoreWeave、Lambda）的公司、以及 H100 存量在几百到上千的公司来说，它们面临的几乎主要都是 LLM 和一些扩散模型（ Diffusion Model ）方面的工作。有些公司选择对现有模型进行微调，但更多 AI 领域的初创公司正在从 0 开始构建自己的新的大模型。**这些公司和私有云服务商签订的合同金额通常在在 1,000 万至 5,000 万美元之间，合同期为 3 年，并使用几百到几千个 GPU。**

对于那些只使用少量按需的 H100 GPU 的公司来说，与 LLM 相关的任务占据了他们 GPU 用量的大头，LLM 对 GPU 的使用率可能超过了 50%。

当前，私有云正受到企业的青睐，尽管这些企业通常会选择默认的大型云服务提供商，但他们也面临被淘汰的风险。

**• 大型人工智能实验室更受限于推理任务还是训练任务？**

这个问题取决于他们的产品吸引力有多大。也就是说，公司的产品吸引力对决定资源分配非常重要，在资源有限的情况下，推理和训练的优先级往往各有侧重。Sam Altman 的观点是，如果一定要做选择的话，OpenAI 更倾向于增强推理能力，但目前 OpenAI 在这两方面都受到了限制。

**为什么 H100 是训练 LLM 的刚需**

目前市场上大部分使用的是 NVIDIA H100 GPU。这是因为在 LLM 的推理和训练方面，H100 GPU 的速度是最快的，也具有最佳的推理性价比。具体来说，大部分企业选择使用 8-GPU HGX H100 SXM 服务器。

根据我的分析，相同的工作，H100 在成本方面更具优势。如果可以找到二手设备，V100 GPU 是一个不错的选择，但这通常是不可能的。

—— 某匿名人士

在推理方面，我们发现 A10G GPU 已经绰绰有余，而且便宜得多。

—— 某私有云高管

我们注意到了 Falcon 40b 和 llama2 70b 这两个模型也正在被大量使用，在这两个模型的使用中，这种说法就不再准确了。因此，互联速度对推理任务非常重要。

—— （另一位）私有云高管

**Falcon 40b ：**

Falcon 是具有 400 亿参数的基础大语言模型，Falcon 40b 旨在使用更少的训练计算能力达到更优的效果，该模型仅占 GPT-3 训练计算的 75%、Chinchilla 的 40% 以及 PaLM-62B 训练的 80%。2023 年 5 月 25 日，阿联酋技术创新研究所宣布将 Falcon 9 开源，供研究和商业使用，发布后一度登上 Hugging Face 开源 LLM 榜首。

**• LLM 创业团队的共同需求是什么？**

**对于 LLM 创业公司，在 LLM 训练上，它们往往会选择配备 3.2Tb/s InfiniBand 的 H100 GPU。虽然在训练环节，几乎所有人都偏好 H100，但在推理环节，这些企业则更看重性价比，即每美元创造的性能。**

与 A100 相比，H100 GPU 的每美元性能仍然存在一些问题，但 H100 之所以依旧更受青睐，是因为它们更好的拓展性，以及更快的训练时间，而速度/压缩启动、训练或改进模型的时间对于初创公司来说是至关重要的。

“对于多节点训练，他们都要求使用带有 InfiniBand 网络的 A100 或 H100 GPU。我们观察到唯一的非 A/H100 要求是用于推理，其工作负载是单 GPU 或单节点”。

—— 某私有云高管

**影响 LLM 训练的因素主要有：**

**• 内存带宽：**面对大量从内存加载数据的情况，更高的内存带宽可以加速数据加载；

**• 模型计算力（FLOPS，floating point operations per second）：**张量内核或等效矩阵乘法单元，主要影响的是计算速度；

**• 高速缓存和高速缓存延迟：**高速缓存可以暂存数据以重复访问，对性能影响显著；

**• 附加功能：**如 FP8 （8 位浮点数） 等，低精度数值格式可加速训练和推理；

**• 计算性能：**与 GPU CUDA 内核数量相关，主要影响的是可并行执行的任务数目；

**• 互连速度：**如 InfiniBand 等快速节点间互联带宽，该因素会影响分布式训练速度。

**H100 之所以比 A100 更受青睐，部分原因在于 H100 具有更低的缓存延迟和 FP8 计算能力。**

H100 确实是首选，因为它的效率高达 A100 的 3 倍，但成本仅为 A100 的 1.5 - 2 倍。如何考虑到整个系统的成本，H100 的每美元性能也要高得多，如果考虑系统性能，每美元性能可能要高出 4-5 倍。

—— 某深度学习研究员

**数值精度为何如此重要？**

低精度浮点数能够提升训练和推理速度，如 FP16 比 FP32 低一半内存占用量，并在计算速度上比 FP32 快三倍。在 LLM 训练过程中，为保证速度和精度的均衡，会使用混合精度、自适应精度等方法对大语言模型进行加速，因而多种精度支持对大语言模型训练是重要考量之一。Google 提出了 BFP16 数值格式，扩大了数值范围的同时，降低了精度，也比 FP 32 的性能要好。

**• 除了 GPU 之外， LLM 训练和运营中还有哪些成本环节？**

**目前 GPU 是整个 LLM 训练基础设施中最昂贵的配件，但其他方面的成本也不低，同样对 LLM 的训练和运营成本产生影响：**

1. 系统内存和 NVMe 固态硬盘价格昂贵：大模型需要大量的高速内存和高速固态硬盘来缓存和加载数据，这两种组件的价格都很高；

2. 高速网络成本高昂：如 InfiniBand 这样的高速网络 （用于节点间通信） 价格非常昂贵，大型、分布式训练尤甚。

运行一个群集的总成本中，**10%-15% 可能用于电力和托管，两者之间大致平分。电力成本包含电力、数据中心建筑成本、土地成本和员工等，约为 5%-8%；托管成本包含土地、建筑、员工等，约为 5%-10%。**

我们主要考量的是网络和可靠的数据中心。由于网络限制和不可靠的硬件，AWS 并不适合。

—— 深度学习研究员

**• GPUDirect 技术在 LLM 训练中提供了什么样的帮助？**

**NVIDIA 推出的 GPUDirect 虽然并非 LLM 训练中的必需，但也能对性能有所帮助：**

GPUDirect 技术可以提高性能， 但未必是一个超临界的差异。这主要取决于你的系统瓶颈在哪里。对于某些架构/软件实现来说，系统瓶颈不一定在于网络。**但如果是网络，GPUDirect 能够使性能提高 10%-20%，这对于昂贵的训练运行成本来说是相当可观的数字。**

尽管如此，GPUDirect RDMA 现在已经无处不在，其受欢迎程度几乎不言而喻。我认为，对于非 Infiniband 网络，GPUDirect 的支持力度较弱，但大多数为神经网络训练而优化的 GPU 集群都有 Infiniband 网络/卡。对性能影响更大的因素可能是 NVLink，因为它比 Infiniband 更罕见，但它也只有在你采用特定的并行化策略时才至关重要。

因此，强大的网络和 GPUDirect 等功能可以让那些不够成熟的软件开箱即用。但如果考虑成本或原有的基础设施，GPUDirect 并非严格要求。

—— 某深度学习研究员

**GPUDirect：**

NVIDIA 推出的名为 GPUDirect 存储（GPUDirect Storage）的数据传输技术，主要用于加快位在各种存储的数据传输到 GPU 内存的速度，可以将带宽增加至原本的 2 到 8 倍，并且还能降低端到端的延迟，达 3.8 倍。 过去将数据从存储器载入到 GPU，都是由 CPU 负责，这会大大限制硬件性能。

数据从 NVMe 磁盘传输到 GPU 內存的标准路径，是使用系统內存中的回弹缓存（Bounce Buffer），即额外的数据拷贝。GPUDirect 存储技术的核心是避免使用回弹缓存以减少额外的数据副本，并使用直接內存存取引擎（Direct Memory Access，DMA）将数据直接放到 GPU 内存中。

**为什么  LLM 公司不能使用 AMD 的 GPU？**

某私有云公司的高管表示，购买 AMD GPU 从理论上是可行的，但设备从购买到实际真正运转都需要一定时间，即便只是 2 个月左右的开发和调试时间都意味着比竞争对手更晚进入市场。也因此，CUDA 是英伟达目前的护城河。

MosaicML 的一篇研究中则提到，AMD GPU 同样也适用于大模型训练任务。他们对基于 PyTorch 的简单训练任务进行了实验，相较于在 NVIDIA 上运行，无需进行任何代码修改。作者表明，只要代码库是基于 PyTorch 构建的，那么可以直接在 AMD 上使用，无需额外的适配。未来，作者计划将在更大规模计算集群上验证 AMD 系统的性能表现。

与此同时，也有观点认为，考虑到一个模型训练的成本接近 3 亿美元，所以没有人会冒险去大规模依赖 AMD 或其他初创公司的芯片，尤其是当芯片需求在 1 万张以上的数量级时。

一位半导体行业的退休人士也提到，AMD 的供货情况也并不乐观，台积电 CoWoS 的产能已经被 NVIDIA 吸走了，所以，虽然 MI250 也许是一个可行的替代方案，但同样很难获得。

**H100 VS A100：**

**NVIDIA A100：**

NVIDIA V100 的升级，相较于 V100，A100 的性能提升了 20 倍，非常适合于 AI 、数据分析等任务。A100 由 540 亿个晶体管组成，集成了第三代 Tensor 核心，并具有针对稀疏矩阵运算的加速功能，对于 AI 推理和训练来说特别有用。此外，采用 NVIDIA NVLink 互连技术可以将多个 A100 GPU 用于更大的 AI 推理工作负载。

**NVIDIA H100：**

A100 的下一代产品，是最新款的、针对大模型专门优化过的芯片。它基于 Hopper 架构，使用台积电 5nm 定制版本制程（4N）打造，单张芯片包含 800 亿晶体管。具体来说，NVIDIA 提出了 Transformer Engine，集成了多种精度计算和 Transformer 神经网络动态处理能力，使得 H100 GPU 能够大大缩短模型训练时间。基于 H100，NVIDIA 还推出了机器学习工作站、超级计算机等一系列产品，如 8 张 H100 和 4 个 NVLink 结合组成一个巨型 GPU——DGX H100。

相较于 A100，H100 的 16 位推理速度快约 3.5 倍，16 位的训练速度快约 2.3 倍。

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/006.jpg)

*A100 与 H100 速度对比*

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/007.png)

*H100 Training MoE*

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/008.jpg)

*H100 Speedup At Scale*

大多数人倾向于购买 H100 用于模型训练和推理，而将 A100 主要用于模型推理。但是也有人可能会考虑以下几个因素：

**• 成本：**H100 较 A100 更昂贵；

**• 容量：**A100 和 H100 在计算能力和内存不同；

**• 使用新硬件：**采用 H100 需要在软件和工作流上做相应调整；

**• 风险：**设置 H100 存在更多未知风险；

**• 软件已优化：**有的软件已经针对 A100 进行了优化。

总的来说， 尽管 H100 的性能更高，但有些时候选择 A100 也十分合理，**这使得是否从 A100 升级到 H100 不是一个简单决策，需要考量到很多因素。**

事实上，A100 将在几年后成为今天的 V100。考虑到性能限制，我认为现在几乎没有谁会在 V100 上训练 LLM。但 V100 仍被用于推理和其他任务。同样的，随着越来越多的人工智能公司转向 H100 来训练新模型，A100 的价格可能会下降，但对 A100 需求始终存在，尤其是在推理方面。

—— 私有云执行官

我认为，由于一些获得巨额融资的初创公司终将倒闭，可能导致市场上又出现大量 A100 。

—— （另一位）私有云执行官

不过随着时间的推移， **人们会将 A100 用于越来越多的推理任务， 而不再用于训练最新、更大型的模型。**而 V100 的性能已经无法支持大型模型的训练， 高显存显卡更适合大机型，因此尖端团队更青睐 H100 或 A100。

不使用 V100 的主要原因是缺少 brainfloat16（bfloat16， BF16）数据类型。没有这种数据类型，就很难轻松地训练模型。OPT 和 BLOOM 性能不佳的主要原因就是没有这种数据类型（OPT 是在 float16 中训练的，BLOOM 的原型设计主要是在 FP16 中完成的，这就无法将数据推广到在 BF16 中完成的训练运行）。

—— 深度学习研究员

**• Nvida 的 GPU H100、GH200、DGX GH200、HGX H100 和 DGX H100 之间的区别？**

• H100 = 1x H100 GPU；

• HGX H100 = NVIDIA 服务器参照平台。OEM 厂商用于构建 4 GPU 或 8 GPU 服务器，由 Supermicro 等第三方 OEM 制造；

• DGX H100 =  NVIDIA 官方 H100 服务器，配备 8x H100，NVIDIA 是其唯一供应商；

• GH200 = 1x H100 GPU 加上 1x Grace CPU；

• DGX GH200 = 256x GH200，将于 2023 年底上市，可能仅由 NVIDIA 供应；

*欢迎关注**海外独角兽**视频号*

*获取最前沿的科技行业资讯*

• 针对大型云计算公司的 MGX。

其中，大多数公司选择购买 8-GPU HGX H100，而非 DGX H100 或 4-GPU HGX H100 服务器。

**这些 GPU 分别的成本如何？**

1x DGX H100 （SXM） 配备 8x H100 GPU 的价格为 46 万美元，其中包括所需的支持服务等，约 10 万美元。Startups 可以获得 Inception 折扣，折扣约为 5 万美元，最多可用于 8x DGX H100 盒子，共计 64 个 H100。

GPU 具体规格如下：

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/009.png)

*DGX H100 规格*

1x HGX H100 （SXM） 配备 8x H100 GPU 的价格在 30 万至 38 万美元之间，具体价格取决于规格（网络、存储、内存、CPU）以及销售商的利润和支持水平。如果规格与 DGX H100 完全相同，则企业可能需要支付较高的价格，即 36 万至 38 万美元（包括支持费用）。

1x HGX H100（PCIe）配备 8x H100 GPU，包括支持费用在内约为 30 万美元，具体价格取决于规格。

PCIe 卡的市场价格约在 3 万至 3.2 万美元之间。

SXM 显卡并不作为单卡销售，因此很难给出定价。一般只作为 4GPU 和 8GPU 服务器销售。

市场上大约 70-80% 的需求是 SXM H100，其余的是 PCIe H100。SXM 部分的需求呈上升趋势，因为前几个月只有 PCIe 卡可用。鉴于大多数公司购买的是 8GPU HGX H100（SXM），包括其他服务器组件在内，每 8 个 H100 的大致花费为 36 万至 38 万美元。

DGX GH200 包含 256x GH200，而每个 GH200 包含 1x H100 GPU 和 1x Grace CPU。根据估算，DGX GH200 的成本可能在 1500 万 - 2500 万 美元之间。

**市场对 GPU 的需求到底是多少？**

• GPT-4 的训练可能是在 1,0000 至 2,5000 张 A100 基础上完成的；

• Meta 大约有 2,1000 张 A100，Tesla 大约有 7000 张 A100，Stability AI 大约有 5000 张 A100；

• Falcon 40B 的训练是在 384 张 A100 上进行的；

• Inflection 在其 GPT-3.5 等效模型中使用了 3500 张 H100。

到 12 月，我们将有 2.2 万个 GPU 投入使用，而目前投入使用的设备也已远远超过 3500 张。

—— Inflection AI 首席执行官 Mustafa Suleyman

**根据 Elon Musk 的说法，GPT-5 的训练可能会用到 3-5 万张 H100。**Morgan Stanley 在 2023 年 2 月提出过，GPT-5 将使用 2.5 万个 GPU，并且他们在当时也提出 GPT-5 已经投入训练中，不过 Sam Altman 随后在今年 5 月否认了这一点，表示 OpenAI 并未进行 GPT-5 的训练，所以 Morgan Stanley 的信息或许并不准确。

GCP 大约有 2.5 万张 H100，Azure 可能有 1- 4 万张 H100。甲骨文 （Oracle）的情况应该类似。此外，Azure 的大部分容量将被供应至 OpenAI。

CoreWeave 大约保有 3.5 至 4 万个 H100 ，但这是根据订单情况得出的，而非实际情况。

**Startup 订购了多少张 H100？**如果用于 LLM 微调任务，通常订购几十或几百张；若用于 LLM 训练，则需要数千张。

**LLM 领域内的公司可能需要多少 H100？**

• OpenAI 可能需要 5 万个，Inflection 需要 2.4 万个，Meta 可能要 2.5 万个（也有说法认为 Meta 实际上要 10 万或更多）；

• 大型云服务商，如 Azure、Google Cloud、AWS 和 Oracle 可能各需要 3 万；

• 私有云服务商，如 Lambda 和 CoreWeave 以及其他私有云可能加起来共需要 10 万；

• Anthropic、Helsing、Mistral、Character 可能各需要 1 万。

上面的数字都是估算和猜测，其中有些可能是被重复计算的，例如租用云的客户。**总体上，按照目前的测算，H100 的数量约为 43.2 万张，若按每张约 3.5 万美元计算，这就是总量价值约 150 亿美元的 GPU。此外，这 43.2 万的数字尚未包括像字节跳动（TikTok）、百度和腾讯这样需要大量 H800 的中国公司。**

此外，一些金融公司也在部署从数百到数千张规模不等的 A100 /H100 ：如 Jane Street、JP Morgan、Two Sigma 和 Citadel。

**这与 NVIDIA 数据中心收入相比如何？**2023 年 2 月至 4 月，NVIDIA 数据中心收入为 42.8 亿美元。2023 年 5 月 25 日至 7 月，数据中心收入可能在 80 亿美元左右。**这主要是基于以下假设：NVIDIA 对该季度收入指引较高，主要原因是数据中心业务的收入增加，而非其他业务领域的收入增加。**

因此，供应短缺情况可能需要一段时间才能缓解。但有可能算力短缺的情况被夸大了，首先，大部分公司都不是立刻购买所有自己需求的 H100，而是逐步升级；此外，NVIDIA 也正在积极提升产能。

整个市场上拥有 40 万张 H100 并非遥不可及，尤其是考虑到现在每个人都在大量部署 4 或 5 位数 H100 的情况。

—— 某私有云高管

**总结**

• 大多数大型 CSP（Azure、AWS、GCP 和 Oracle）和私有云（CoreWeave、Lambda 和其他各种云）更希望获得更多的 H100 GPU，而不仅仅是能够访问它们，大多数大型人工智能产品公司也追求更多的 H100 GPU。

• 一般来说，这些公司需要配备 SXM 卡的 8GPU HGX H100 机箱。根据规格和支持情况，每台 8GPU 服务器的成本大约在 300 到 400 万美元之间。可能会有对数十万个 H100 GPU 的过剩需求，这部分总价值超过 150 亿美元；

• 在供应有限的情况下，NVIDIA 完全可以通过提高价格来找到一个市场均衡价格，并且在某种程度上也确实这样做了。总而言之，最终决定如何分配 H100 GPU ，取决于 NVIDIA 自身更倾向于将其分配给哪些客户。

**03.**

**H100 供给侧分析**

**来自 TSMC 的瓶颈**

H100s 是由 TSMC（台积电）生产的， **NVIDIA 能否选择其他芯片工厂生产更多的 H100 呢？至少现在这种可能尚未出现。**

NVIDIA 过去曾与三星有过合作，但三星还不能满足他们对尖端 GPU 的需求，所以目前英伟达只能使用台积电生产的 H100s GPU 和其他 5nm GPU 。**也许在未来，NVIDIA 会与英特尔合作，或者继续与三星在相关技术上合作，但短期内这两种情况都不会发生，因而也不会对 H100 的供应紧张情况有所缓解。**

台积电（TSMC）的 5 纳米（N5）技术在 2020 年进入量产。N5 技术是 TSMC 的第二种 EUV 工艺技术，提供了比之前的 N7 技术更快的速度和更低的功耗。此外，TSMC 还计划推出 4 纳米（N4）技术，它是 N5 技术的增强版本，将进一步提升性能和功耗，并计划于 2022 年开始量产。

H100 是基于 TSMC 4N 工艺生产的，4N 属于 5nm 系列中的增强型 5nm，而非真正的 4nm 工艺。**除了 NVIDIA，Apple 也在使用这个技术，但他们已主要转向 N3，并保留了大部分 N3 容量。**另外，高通和 AMD 是 N5 系列的大客户。

A100 使用的是台积电的 N7 工艺。

7纳米（N7 ）是台积电 2019 年投入量产的制程节点。在 N7 基础上，台积电还推出了N7+工艺，即采用 EUV（极紫外光刻）的 7nm 制造工艺，把晶体管密度提升了15%~20% 同时降低芯片功耗。

一般情况下，前端制程容量（Fab Capacity）会提前 12 个月以上就被规划好。有观点指出，TSMC 和其大客户会共同计划下一年的生产需求，因此当下 H100 的供给短缺一定程度上是因为 TSMC 和 NVIDIA 在前一年对今年 H100 需求的错误判断。

**前端制程容量（Fab Capacity）：**

在半导体芯片工艺流程中，Fab 为 FABRICATION（加工，制造）的简称，Fab Capacity 可以认为是产能容量。

另据消息，H100 从开始生产到可以出售给客户（生产、包装和测试完毕）一般需要 6 个月，不过这个情况有待得到证实。

一位半导体行业退休专业人员指出，晶圆产能并非台积电的瓶颈，真正的瓶颈其实在于前面提到的 CoWoS（三维堆叠）。

**CoWoS （Chip on wafer on Substrate，三维堆叠）：**

是台积电的一种 2.5 D的整合生产技术，先将芯片通过 CoW（Chip on Wafer）的封装制程连接至硅晶圆，再把 CoW 芯片与基板（Substrate）连接，整合成 CoWoS。

根据 DigiTimes 的报道，TSMC 已经开始扩充自己的 CoWoS 产能，计划在 2023 年底前将 CoWoS 产能从每月 8,000 片晶圆提升至 11,000 片，并在 2024 年底之前增加到每月 14,500 至 16,600 片左右。NVIDIA、Amazon、博通、Cisco 和赛灵思等主要科技巨头都增加了对 TSMC 先进 CoWoS 封装的需求。

**H100 内存**

**内存类型（Memory Bype）、内存总线宽度（Memory Bus Width）和内存时钟速度（Memory Clock Speed）共同影响了 GPU 的内存带宽。**作为 GPU 架构的一部分，NVIDIA 设计了 H100 的总线宽度和时钟速度。H100 SXM 上主要使用 HBM3 内存， H100 PCIe 上，主要使用 HBM2e。

HBM 很难生产，供给也非常有限，因此生产 HBM 是一场噩梦。但是一旦生产出了 HBM，其他部分的设计将变得简单。

—— 某 Deepl Learning 研究员

**内存类型、内存总线宽度和内存时钟速度是计算机内存的三个重要指标。**

**内存总线宽度：**

指的是内存模块与主板之间的数据传输通道的宽度，较宽的内存总线宽度可以提供更大的数据通路，从而提高内存与处理器之间的数据传输速度。

**内存时钟速度：**

指的是内存模块的工作时钟频率，较高的内存时钟速度意味着内存可以更快地进行读写操作，提供更高的数据传输速度。

**HBM（High Bandwidth Memory）：**

是一种高带宽内存技术，用于在图形处理器（GPU）和其他高性能计算设备中提供快速的内存访问速度。传统的图形卡和计算设备使用的内存技术通常是基于 GDDR（Graphics Double Data Rate）的设计，它在性能和功耗之间存在一定的平衡。而 HBM 技术通过在 GPU 芯片上放置内存堆栈，以及通过高速垂直连接（TSVs）将多个 DRAM 芯片堆叠在一起，实现了更高的带宽和更低的功耗。

对于 HBM3 内存，NVIDIA 可能全部或者主要使用 SK Hynix。目前并不确定 NVIDIA 的 H100 是否使用了三星的内存，但可以确定的是，NVIDIA 目前没有使用美光的内存。

就 HBM3 而言，一般来说，SK Hynix 的产量最大，随后是三星，第三名的美光和前两者的产量差距较大。看起来，SK Hynix 已经提高了产量，但 NVIDIA 仍希望他们生产更多，而三星和美光还没有成功提高产量。

**制造 GPU 时还会用到什么？**

此外，GPU 的生产还会涉及到很多金属材料及零部件，这些环节原料的短缺也带来引发 GPU 的供给瓶颈，例如：

**• 金属和化学品：**包括铜、钽、金、铝、镍、锡、铟和钯等硅（类金属）等，这些金属和化学品被用于生产的各个阶段，从硅晶圆的制造到 GPU 的最终组装，例如硅、稀土等；

**• 组件和封装材料：**例如基板、焊球和焊线 、散热化合物等，它们被用来完成 GPU 各个部件的组装和链接，对 GPU 的运行至关重要；

**• 能源消耗：**在 GPU 芯片的制造过程中，由于使用了高精度的机械设备，因此需要大量的电力。

**NVIDIA 如何解决 H100 短缺？**

NVIDIA 方面透露他们将在今年下半年增加供应量，NVIDIA CFO 在财报会上表示公司正在全力解决供给问题，但除此之外，他们没有传达更多信息，也没有任何具体的和 H100 相关的数字。

“我们正在努力解决本季度的供应问题，但我们也已经为下半年采购了大量库存。”

“我们相信，下半年的供应量将大大超过上半年。”

—— 英伟达首席财务官科莱特-克雷斯（Colette Kress）在 2023 年 2 月至 4 月财报电话会议上的发言

某私有云公司高管认为，**接下来市场上可能会出现一种恶性循环，即，稀缺性导致 GPU 容量被视为 AI 公司的护城河，从而导致了更多的 GPU 囤积，而这又进一步加剧了 GPU 的稀缺。**

根据历史上 NVIDIA 推出不同架构的间隔时间，H100 的下一代机型可能要到 2024 年底（2024 年中到 2025 年初）才会发布。在此之前，H100 将会一直是 NVIDIA GPU 的 Top 级产品（GH200 和 DGX GH200 不算，它们不是纯 GPU，都使用 H100 作为 GPU）。

此外，预期未来也会有更大显存的 120GB 版本。

**04.**

**如何获得 H100**

**H100 的卖家**

戴尔、HPE、联想、超微（Supermicro）和广达（Quanta）等原始设备制造商（OEMs）都在销售 H100 和 HGX H100，而订购 InfiniBand 需要通过 NVIDIA  Mellanox 完成。

**Mellanox** 是 全球 InfiniBand 主要供应商之一，2015 年，Mellanox 在全球 IB 市场上的占有率达到80%。2019 年，NVIDIA 以每股 125 美元的价格收购了 Mellanox，总交易价值达约 69 亿美元。这项收购使 NVIDIA 能够进一步扩展在高性能计算和数据中心领域的市场份额，并且加强了 NVIDIA 在 AI 领域的竞争力。

通过整合 Mellanox 的高速互连技术和 NVIDIA 的 GPU 加速器，NVIDIA 能够为数据中心提供更高带宽和更低延迟的解决方案。Mellanox 之外，IB 领域另一家供应商 QLogic 的 IB 技术在 2012 年被英特尔公司出资收购。

CoreWeave 和 Lambda 等 GPU 云从 OEM 那里购买 GPU，然后再租给 Startup。超大规模的云厂商（Azure、GCP、AWS、甲骨文）能够更直接地与 NVIDIA 合作购买，但他们有时候也会和 OEM 合作。

对于 DGX，也要通过 OEM 完成购买。客户虽然可以和 NVIDIA 沟通采购需求，但购买则是通过 OEM ，而非直接向 NVIDIA 下采购订单。

交付时间上，8 GPU HGX 服务器的交付时间非常糟糕，而 4 GPU HGX 服务器的交付时间还不错，但现实是每个人都想要 8 GPU 服务器。

**• 从下单到部署 H100 需要多久？**

部署是一个分阶段的过程。比如说一个 5000 GPU 的订单，他们可能会在 4-5 个月内获得 2,000 或 4,000 GPU 的访问权限，然后在 6 个月左右获得剩余的 GPU 的访问权限。

**对于 Startup，如果要购买 GPU，并不是从 OEM 或者经销商那里下订单**，他们一般会选择 Oracle 等公有云服务，或向 Lambda 和 CoreWeave 等私有云租用访问权，或向 FluidStack 等与 OEM 和数据中心合作的提供商租用访问权。

**• 企业应该自建数据中心还是主机托管？**

对于建立数据中心，需要考虑的因素包括建立数据中心的时间、是否拥有硬件方面的人才和经验，以及资本投入规模。

租用和托管服务器要容易得多。如果你想建立自己的数据中心，就必须铺设一条暗光纤线路到你所在的位置，以连接互联网，光纤的造价是每公里 1 万美元。在互联网繁荣时期，大部分基础设施已经建成并支付了费用。现在，您只需租用即可，而且相当便宜。

—— 某私有云高管

选择租用或自建数据中心并为一个非此即彼的决策，企业根据实际需求，可以有以下不同选择：

1. 按需云：纯粹使用云服务进行租赁；

2. 预留云；

3. 主机托管（购买服务器，与提供商合作托管和管理服务器）；

4. 自助托管（自己购买和托管服务器）。

大多数需要大量 H100 的 Startup 会选择预留云或主机托管。

**企业如何选择云服务公司？**

有观点认为，Oracle 的基础设施可靠性不如三大云，但它愿意在客户技术支持上花更多时间。有私有云公司从业者表示， 100% 会有对基于 Oracle 的服务一大批不满意的客户，也有其他公司 CEO 认为 Oracle 的联网能力更强。

**一般来说，Startup 会选择在服务支持、价格和容量方面综合实力最强的公司。**

几个大型云服务公司之间的主要区别在于：

**• 网络：**AWS 和 Google Cloud 采用 InfiniBand 的速度较慢，因为它们有自己的方法，不过大多数寻求大型 A100/H100 集群的初创公司都在寻求 InfiniBand；

**• 可用性：**例如，Azure 的 H100 算力大部分被 OpenAI 所使用，这就意味着可供其他客户使用的算力可能并不多。

**虽然还没有事实依据，但有猜测认为，NVIDIA 更倾向于为那些没有开发竞争性机器学习芯片的云服务商优先分配 GPU 供给。**目前所有三大云服务商都在开发自己的机器学习芯片，但 AWS 和 Google 的 NVIDIA 替代产品已经上市，并抢走了 NVIDIA 的一些市场份额。因而也引发了一些市场猜测，认为 NVIDIA 之所以更愿意和 Oracel 合作就是因为这点。

一些大型云公司的价格比其他云更优惠。正如一位私有云执行官所指出的，“例如，AWS/AZURE 上的 A100 比 GCP 要贵得多。”

Oracle 告诉我，今年晚些时候他们将有 “数以万计的 H100”投入使用。但在定价方面，他们比其他公司都要高。他们没有给我 H100 的定价，但对于 A100 80GB，他们给我的报价接近 4 美元/小时，这比 GCP 的报价高出近 2 倍，而且是在相同的功耗和投入的情况下。

—— 匿名人士

较小的云在定价方面更有优势，除非在某些情况下，其中一个大型云公司可能会进行奇怪的交易来换取股权。

所以综合来看， 就和 NVIDIA 的合作亲密度而言，Oracle 和 Azure > GCP 和 AWS，不过这一点只是猜测。

甲骨文率先推出了 A100s，并与英伟达合作托管了基于英伟达的集群，英伟达也是 Azure 的客户。

**• 哪种大型云公司的网络性能最好？**

Azure、CoreWeave 和 Lambda 都使用 InfiniBand。Oracle 的网络性能很好，达到 3200 Gbps，但使用的是以太网而不是 InfiniBand，对于高参数 LLM 训练等使用情况下，可能比 IB 慢 15-20% 左右。AWS 和 GCP 的网络没有那么好。

**• 目前企业是如何选择云服务的？**

一份面向 15 家企业的统计数据显示，所有被调研的 15 家企业都会选择 AWS、GCP 或 Azure，其中并没有 Oracle 。

大多数企业倾向于使用现有的云。但对于创业团队来说，他们的选择则更基于现实：哪家可以提供算力，就会选择哪家。

**• 关于 DGX Cloud、NVIDIA 正在与谁合作？**

“英伟达正与领先的云服务提供商合作托管 DGX 云基础架构，首先从甲骨文云基础架构开始”——与英伟达进行销售，但通过现有的云提供商进行租赁（首先与甲骨文合作 ，然后是 Azure，之后是 Google Cloud，没有与 AWS 合作）。

NVIDIA  CEO 黄仁勋在 NVIDIA 的财报电话会议上说过 “理想的组合是 10% 的 NVIDIA DGX 云和 90% 的 CSP 云”。

**• 云服务巨头们的 H100 时间表：**

CoreWeave 是最早的一家。作为 CoreWeave 的投资人，并且大概率为了加强大型云公司之间的竞争，NVIDIA 最早为 CoreWeave 完成交付。

其他云服务公司的 H100 时间表如下：

• Azure 于 3 月 13 日宣布 H100 可供预览；

• 甲骨文于 3 月 21 日宣布限量供应 H100；

• Lambda Labs 于 3 月 21 日宣布将于 4 月初推出 H100；

• AWS 于 3 月 21 日宣布 H100 将在几周后开始预览；

• Google Cloud 于 5 月 10 日宣布开始 H100 私有预览。

**• 不同公司分别在使用哪些云服务？**

• OpenAI: Azure

• Inflection:  Azure 和 CoreWeave

• Anthropic: AWS 和 Google Cloud

• Cohere：AWS 和 Google Cloud

• Hugging Face: AWS

• Stability AI: CoreWeave 和 AWS

• Character.ai: Google Cloud

• X.ai：甲骨文

• NVIDIA: Azure

**如何获得更多的 GPU 配额？**

最终的瓶颈在于是否可以从 NVIDIA 方面获得算力分配。

**• NVIDIA 是如何选择客户的？**

NVIDIA 通常会给每个客户都分配一定的 GPU ，而这一过程中 **NVIDIA 最关心的是“终端客户是谁”，举例来说，Azure 说 “我们想购买一万张 H100 来支持 Inflection”，与 Azure 说 “我们为 Azure 购买一万张 H100” 对应的结果是不同的。**如果 NVIDIA 对某个特定的终端客户感兴趣，那么云公司就有可能获得额外的 GPU 配额。所以，NVIDIA 很希望尽可能了解终端客户是谁，他们会更倾向于大企业或拥有强大背书的初创公司。

是的，情况看起来就是这样。英伟达喜欢为 AI startups 提供 GPU 的使用权（其中许多公司与英伟达关系密切）。英伟达投资的 AI 公司 Inflection 正在 CoreWeave 上测试一个巨大的 H100 集群。

—— 某私有云执行官

*欢迎关注**海外独角兽**视频号*

*获取最前沿的科技行业资讯*

如果某个云公司给 NVIDIA 带来了一个终端客户，并表示他们准备购买一定数量级的 H100，且 NVIDIA 对该终端客户感兴趣，NVIDIA 一般就会给予一定配额，这实际上会提高 NVIDIA 分配给该云公司的总容量，因为这部分配额是独立于 NVIDIA 最初给到该云公司配额之外。

NVIDIA 向私有云分配大容量的情况比较特殊：**CoreWeave 拥有比 GCP 更多的 H100。NVIDIA 不愿意将大量资源分配给那些试图与其直接竞争的公司（AWS Inferentia 和 Tranium、Google TPUs、Azure Project Athena）。**

但归根结底，如果你向 NVIDIA 提交采购订单和资金，承诺更大的交易和更多的前期资金，并表明你的低风险状况，那么你一定会获得比别人更多的 GPU 配额。

**05.**

**总结**

即便如 Sam Altman 所说，“使用大模型的时代即将结束”，但目前我们仍然受到 GPU 的限制。一方面，像 OpenAI 这类公司，已经拥有 ChatGPT 这种极佳 PMF 的产品，但因为受限于 GPU 所以需要大量采买算力，另一方面，也有不少团队在为未来参与 LLM 的可能性而囤积 GPU，不论他们是否有可能创造出 ChatGPT 这样的产品。

但毫无疑问，NVIDIA 的话语权不会动摇。

**现阶段 PMF 做得最好的 LLM 产品是 ChatGPT，以下以 ChatGPT 为例来说明 GPU 为什么短缺：**

1. 因为 ChatGPT 深受用户喜爱，它的 ARR（年度经常性收入）有可能超过 5 亿美元；

2. ChatGPT 在 GPT-4 和 GPT-3.5 的 API 之上运行；

3. GPT-4 和 GPT-3.5 的 API 需要 GPU 才能运行，并且需要大量 GPU，OpenAI 希望为 ChatGPT 及其 API  发布更多功能，但受限于 GPU 的数量而无法实现；

4. OpenAI 通过微软（Azure） 购买了大量 NVIDIA GPU；

5. 为了制造 H100 SXM GPU，NVIDIA 使用台积电进行制造，并使用台积电的 CoWoS 封装技术和主要来自 SK Hynix 的 HBM3。

除了 OpenAI，市场上还有很多公司都在训练自己的大模型，先抛开 LLM 当中存在有多少泡沫存在、最终又有多大概率出现 PMF 的产品，但总体上 LLM 竞赛已经推高了市场对 GPU 的需求。此外，还有一些公司即使暂时还不需要 GPU，但由于担心未来，所以他们也会开始提前储备。因此，这就有点像**“对供应短缺的预期加重了供应短缺”**。

所以，推高 GPU 需求的另外一股力量是哪些希望在创建新的 LLMs、或者在未来参与 AI 的企业公司：

1. 大模型重要性已经成为一种共识：如果是成熟企业，则希望在自己的数据上训练 LLM 并寄希望其带来更多商业价值；作为初创公司，则希望建立自己的 LLM 并转化为商业价值。而 GPU 是用来训练大模型的刚需；

2. 这些企业和大型云厂商（Azure、Google Cloud、AWS）的沟通，试图来获得足够的的 H100；

3. 在此过程中，他们发现云厂商也没有足量的 H100 进行分配，并且一些云厂商的网络配置也存在瑕疵，于是，CoreWeave、Oracle、Lambda 和 FluidStack 也成为，与此同时如果他们想自己购买 GPU 并拥有它们，也许他们还会与 OEM 和 NVIDIA 讨论；

4. 最终，他们获得了大量 GPU；

5. 现在，他们正在尝试让自己的产品与市场相匹配；

6. 如果还不清楚的话，这条路并不好走——请记住，OpenAI 是在更小的模型上实现产品与市场的契合，然后再将其放大。但是，现在要实现产品与市场的匹配，你必须比 OpenAI 的模型更适合你的用户的使用案例，因此在一开始时你需要比 OpenAI 更多的 GPU。

**至少到 2023 年底，对于要部署数百或数千的 H100 的企业都会面临短缺问题，也许到 2023 年底，情况会更加明朗，但目前看来，GPU 的短缺可能会持续到 2024 年。**

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/010.jpg)

*GPU 供需之旅*

**Reference**

https://www.youtube.com/watch?v=nxbZVH9kLao&t=35s

https://humanloop.com/blog/openai-plans

Comment from a custom LLMs-for-enterprises startup founder

Message from an exec at a cloud provider

https://www.youtube.com/watch?v=TO0J2Yw7usM

Conversations with execs at cloud companies and GPU providers

https://www.tomshardware.com/news/more-details-about-elon-musk-ai-project-emerge

https://azure.microsoft.com/en-us/blog/azure-previews-powerful-and-scalable-virtual-machine-series-to-accelerate-generative-ai/

https://inflection.ai/NVIDIA-coreweave-mlperf

Tesla Q1 2023 (covers Jan 1 2023 to Mar 31 2023) earnings call

https://llm-utils.org/OpenAI+Interviews/Sam+Altman+interviewed+by+Patrick+Collison+-+Transcript+(May+9%2C+2023)

https://timdettmers.com/2023/01/30/which-gpu-for-deep-learning/

https://www.mosaicml.com/blog/mpt-30b

https://resources.NVIDIA.com/en-us-dgx-systems/ai-enterprise-dgx

https://resources.NVIDIA.com/en-us-grace-cpu/grace-hopper-superchip

https://resources.NVIDIA.com/en-us-dgx-gh200/NVIDIA-dgx-gh200-datasheet-web-us

https://llm-utils.org/DGX+GH200+Stats+and+Release+Date

A comment from an exec at a cloud company

A guesstimate ballpark from an exec at a cloud company

https://www.fierceelectronics.com/sensors/chatgpt-runs-10k-NVIDIA-training-gpus-potential-thousands-more

https://www.stateof.ai/compute

https://huggingface.co/tiiuae/falcon-40b

https://inflection.ai/NVIDIA-coreweave-mlperf

https://inflection.ai/inflection-ai-announces-1-3-billion-of-funding

https://NVIDIAnews.NVIDIA.com/news/NVIDIA-announces-financial-results-for-first-quarter-fiscal-2024

https://fuse.wikichip.org/news/6439/tsmc-extends-its-5nm-family-with-a-new-enhanced-performance-n4p-node/, https://pr.tsmc.com/english/news/2874

https://developer.NVIDIA.com/blog/NVIDIA-ampere-architecture-in-depth/

https://developer.NVIDIA.com/blog/NVIDIA-hopper-architecture-in-depth/ ︎

https://www.NVIDIA.com/content/dam/en-zz/Solutions/gtcs22/data-center/h100/PB-11133-001\_v01.pdf

https://www.NVIDIA.com/en-us/data-center/products/certified-systems/

https://llm-utils.org/Building+your+own+GPU+cluster

https://NVIDIAnews.NVIDIA.com/news/NVIDIA-launches-dgx-cloud-giving-every-enterprise-instant-access-to-ai-supercomputer-from-a-browser

https://www.reuters.com/technology/amazons-cloud-unit-is-considering-amds-new-ai-chips-2023-06-14/

https://www.businesswire.com/news/home/20230321005245/en/CoreWeave-Announces-NovelAI-as-Among-the-First-to-Have-NVIDIA-HGX-H100-GPUs-Online

https://azure.microsoft.com/en-us/blog/azure-previews-powerful-and-scalable-virtual-machine-series-to-accelerate-generative-ai/

https://blogs.oracle.com/cloud-infrastructure/post/limited-availability-oci-compute-NVIDIA-h100

https://lambdalabs.com/blog/lambda-cloud-adding-NVIDIA-h100-tensor-core-gpus-in-early-april

https://NVIDIAnews.NVIDIA.com/news/aws-and-NVIDIA-collaborate-on-next-generation-infrastructure-for-training-large-machine-learning-models-and-building-generative-ai-applications

https://cloud.google.com/blog/products/compute/introducing-a3-supercomputers-with-NVIDIA-h100-gpus

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/011.png)

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/012.png)

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/013.png)

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/014.png)

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/015.png)

延伸阅读

[![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/016.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503539&idx=1&sn=b3c54e6cadd70072269ac1a7478988d4&chksm=ce9b712df9ecf83bd5a5b465311ed483a4a4a554e9b1f5dece94621dee4451b748f3e9d0e8a3&scene=21#wechat_redirect)

Harvey：OpenAI投资的法律Copilot，最适合LLM落地的垂直行业

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/017.png)

[![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/018.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503488&idx=1&sn=24bf3cef8b6d859e0b3d4607dc3235b3&chksm=ce9b711ef9ecf808c248dbde533b37b47ced78cdabc4d25b31e96d7fbbab265029d00af377bf&scene=21#wechat_redirect)

拾象硅谷见闻系列：生产力 SaaS 如何应对 AI 的颠覆？

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/019.png)

[![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/020.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503441&idx=1&sn=19397a87b3993ccd6f85fcfcc872d13f&chksm=ce9b71cff9ecf8d919696795beea88ba25056c52262bd5b43e278fa34ec6927fbb118dfff3f8&scene=21#wechat_redirect)

Covariant：OpenAI Mafia创业，为机器人开发AI大脑

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/021.png)

[![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/022.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503355&idx=1&sn=587f9d2354699b5531e797c9c5f3b157&chksm=ce9b7265f9ecfb73a213f324904851a4bde4223cf9728b28ccbe289ea7969c9eebe596da4787&scene=21#wechat_redirect)

拾象实践：为了理解AI-Native，我们做了几款AI应用

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/023.png)

[![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/024.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503155&idx=1&sn=ce93d9e4476ca641d2c5f1283d4ef563&chksm=ce9b72adf9ecfbbbc90a551840965531cb8174620b4bbc31a6d03489c70bf3e611a3cca64bf6&scene=21#wechat_redirect)

Perplexity AI，比Google Bard和Bing Chat更靠谱的问答引擎

![](../images/2023-08-08-h100-gong-xu-fen-xi-xin-pian-zhan-zheng-jiang-chi-xu-duo-jiu/025.png)
