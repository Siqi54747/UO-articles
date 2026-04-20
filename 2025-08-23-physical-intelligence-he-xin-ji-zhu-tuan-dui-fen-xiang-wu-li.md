---
title: Physical Intelligence 核心技术团队分享：物理世界的“Vibe Coding”如何实现？
publish_date: '2025-08-23'
publish_timestamp: 1755950400
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/ctKUfpbSQyWAjs9BY-yAww
msgid: 1000000408
appmsgid: 2247517278
itemidx: 1
digest: 用知识绝缘（Knowledge Insulation）机制重构模型训练流程
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgyiacq5HNy0luWzxibVhD1OjNzpOIt7PxsMtEt2IKkraiaaV0taDIVamyuGdB1tJK2KVDXmVW3MibgJdw/0?wx_fmt=jpeg
image_count: 30
archived_at: '2026-04-20T04:13:23+08:00'
---

[![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100&scene=21#wechat_redirect)

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/002.jpg)

编译：shiling、haozhen

编辑：Siqi

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/003.png)

通用机器人是 AGI 从数字世界走向物理世界的重要路径，而在 AI robotcis 这个主题下，Physical Intelligence 无疑是最具技术深度和研究影响力的团队之一。今年 4 月，PI 以 π₀ 为基础，新发布了一个在开放世界具有泛化能力的 VLA 模型 π₀.₅，PI 表示 π₀.₅ 在一些未知环境中，依然能够展现出与在原始训练环境相近的表现。

那么，从技术视角看，VLA 与 LLM、VLM 之间究竟是什么关系？为了实现通用机器人大脑，PI 是怎么从零构建数据管线的？PI 新提出的“知识绝缘（Knowledge Insulation）”机制到底又是如何运行的？

这篇文章是 Physical Intelligence 核心技术团队对机器人过去和当下技术路径的解读，并分享了 PI 在数据采集、算法设计以及 multi-robot 通用模型领域的前沿技术探索：

**•** VLM 在 LLM 基础上拓展了视觉感知能力，而 VLA 是 VLM 在机器人领域的进一步应用；

**•** PI 团队几乎从头搭建了整个数据引擎，而且通过实验，PI 证明了提高数据的多样性是提升机器人泛化的关键路径；

**•** 为了解决传统模型训练的缺点，PI 提出了“知识绝缘（Knowledge Insulation）”机制，创新性地重构了训练流程；

**•** 在开放世界部署机器人的三大难题分别是数据缺口、性能不稳健和硬件平台迁移非常复杂；

**•** 未来，PI 希望能推动软硬件的深度融合，用户可以设计和定制硬件，实现“物理世界的 vibe coding”。

……

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/004.png)

**01.**

**VLA 是 VLM 在机器人领域的应用**

如今，机器人虽然在工业等结构化生产线上已取得巨大成功，但在家庭、办公室、公共空间等开放场景中，它们的灵活性和智能水平依然远不及人类，因此我们必须进一步扩展 LLM 的能力空间。

**•****VLM 在 LLM 基础上拓展了视觉感知能力**

视觉-语言模型（Visual-Language Model， VLM）是一类结合视觉和语言信息的多模态模型，能够理解并生成与图像内容相关的自然语言描述，或者根据文本 prompt 进行图像分析。与 LLM 相比，VLM 在语言理解能力的基础上新整合了视觉信息，不仅能处理纯文本输入，还能处理和生成涉及视觉内容的复杂信息。

对大多数 researcher 来说，VLM 的训练流程已经比较完善了。具体来说，VLM 以图像和文本为输入，通过预训练的 Transformer 架构，结合 prompt 自回归地生成文本输出。常规训练流程通常是在获得一个 pre-training 模型后，再从互联网上抓取通用数据，并辅以少量与特定任务相关的数据进行补充，再在大规模集群上进行微调，最后借助现成的推理与部署工具将模型部署到云端。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/005.png)

VLM 架构

**•****VLA 的目标是直接输出机器人动作指令**

VLM 让机器能够理解和生成自然语言描述，**但与其他领域对模型的需求相比，机器人领域的需求存在根本差异**。因为机器人不仅要理解场景，更需生成精确的动作指令，实时驱动机械执行复杂任务。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/006.png)

VLM 处理图像与文本指令的基本原理

视觉-语言-动作模型（Visual-Language-Action，VLA）本质上是 VLM 在机器人领域的应用。它不仅能接收图像和文本输入，还会整合机器人当前的状态信息，例如关节角度和机械臂位置。**它的目标不再是生成对场景的语言描述，而是直接输出控制机器人的动作指令。**这一转变带来极大的工程挑战，因为机器人动作需要保持高频率、低延迟、连续且精确的控制，这与传统文本生成模型在处理连续动作序列的需求存在本质差异。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/007.png)

VLA 架构

**过去三年，多模态 LLM 和 VLM 已经从最初的对话系统，逐步发展为融合视觉编码、强化学习等的多模态推理系统，在编码辅助、内容创作等任务中表现出色。**

而 VLA 的发展路径与 VLM 类似，但起步稍晚。以 RT-2 为例，早期的多模态语言模型已经开始引入视觉编码器，一些模型甚至专门针对机器人任务进行训练。虽然这些模型主要作为概念验证的原型存在，但它们已经能够在熟悉的环境中，指挥机器人完成多样的物体抓取任务。尽管有机器人数据量不足的限制，这些尝试仍然极大地激发了业界对于通用机器人智能的关注和期待。

**RT-2（Robotic Transformer 2）**是 Google Research 推出的 VLA 模型，是基于 VLM 架构进行扩展的，训练数据来源包括网页图文、机器人执行示例以及其他多模态数据。

到了 2024 年下半年，一些针对机器人操作的多模态模型进一步出现，行业内也相继推出 Gemini for Robotics、NVIDIA GR00T 等方案，但这些系统仍主要属于概念验证或早期示范阶段。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/008.png)

VLMs 与 VLAs 技术演进

**02.**

**机器人的智能发展：能力、泛化和性能**

**PI 团队的核心理念是，如果一件事能被人类远程遥控完成，那么模型大概率也能学会。**这个想法源自早期对 PR2 机器人的观察。尽管 PR2 的硬件在当时非常先进，但 PR2 的自主决策能力有限，仍然需要依赖人类远程控制或预设任务规划。

**PR2 机器人（Personal Robot 2）**是由 Willow Garage 开发的一款服务机器人，因为具有开放平台的设计以及丰富的软件生态系统（如 ROS 机器人操作系统），所以被广泛用于机器人研究和开发领域。

PR2 机器人远程操作示例

这一事实让 PI 团队更加坚信，**机器人技术发展的核心阻碍并不在于硬件性能，而在于如何赋予机器人像人类一样的智能，让机器人能够准确感知复杂环境、理解多模态信息、灵活规划并稳健执行动作。**PI 的目标就是打造基于视觉、语言和动作的统一模型，赋予机器人和人类相似的能力。

为了实现这一目标，PI 基于 VLA 进行了相关研究。2024 年下半年，PI 发布了首款 multi-robot 通用模型 π₀，这个模型具备在多种机器人平台上执行复杂任务的能力。Physical Intelligence 研究科学家 Jost Tobias Springenberg 评价这个模型是当时最灵巧、最具实用性的 multi-robot 通用模型之一，并已经开源。π₀ 还在架构上进行了优化，使用了 diffusion model 来生成高频率动作，来满足机器人对实时性和响应速度的要求。

π₀ 执行复杂任务示例

**PI 认为，机器人的智能发展可以从三个方面理解：能力（Capability）、泛化（Generalization）和性能（Performance）。**

**能力（Capability）指的是机器人是否能够完成以前从未实现过的复杂任务。**早期机器人大多只能做重复的工业流水线操作，难以应对日常生活中复杂多变的场景，比如折叠衣服、组装盒子或整理桌面等。

随着 π₀ 的发布，PI 团队在多种平台上演示了机器人可以完成多步骤操作任务的能力。在实际测试中，机器人表现出了接近人类的灵活应对能力，比如执行出现偏差时会主动调整，甚至多次尝试直到结果令人满意。这种表现与传统依赖预设路径运行的机器人完全不同，也印证了团队的观点：凡是远程操控能完成的事，模型同样可以通过学习来实现。

然而，能力本身还不足以支撑机器人走向实用化。如果机器人只能在训练过的环境中工作，那么机器人的实际价值将大打折扣。因此，**第二个方面是泛化（Generalization），即在完全陌生、未见过的环境中依然能够正确执行任务。**

**当机器人具备了能力与泛化后，剩下的最大挑战就是性能（Performance）。**

PI 联合创始人兼 CEO Karol Hausman 认为，当前模型仍处于“演示就绪（demo ready）”而非“部署就绪（deployment ready）”的阶段。尽管能力和泛化方面都取得了显著进展，现阶段机器人更多还是停留在演示层面，失败的情况仍然频繁出现。

而性能的提升不仅意味着需要更高的任务成功率，还包括稳定性、速度和鲁棒性。例如，在衣物折叠实验中，机器人可能动作缓慢、偶尔出错，但往往能通过自我纠正最终完成一整堆衣物的折叠工作。这种“犯错—修正—坚持直到成功”的过程，使得机器人更接近人类的工作方式，而不再是传统机器人“一旦出错就彻底失败”的机械模式。

但性能的提升并不能单纯依赖数据规模的堆积。Hausman 强调，要让机器人真正达到人类级别的性能，需要新的算法和新的思路，而不仅仅是更多的数据或更大的模型。这意味着未来的突破可能会来自于训练范式、决策机制和系统设计的创新。

**因此，对于 PI 团队而言，下一阶段的重点在于探索模型能力如何随数据多样性的增加而提升。**基于这一方向，团队开发了具备开放世界泛化（open world generalization）的 VLA 模型 PI 0.5（π₀.₅），目标是让机器人在跨任务、跨环境、跨平台的条件下实现稳定而可靠的泛化。目前已有初步结果显示，π₀.₅ 在一些未知环境中，依然能够维持与原始训练环境相近的表现。

π₀.₅ 完成任务示例

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/009.png)

π₀.₅ 协同训练数据框架

值得一提的是，在众多潜在应用场景中，家庭环境被选为 PI 模型的首个重点落地方向。这一选择是基于以下考量：

**•****环境高度复杂：**家庭物品丰富多样，空间结构复杂多变，人机交互频繁且复杂，这是对机器人智能的极限考验；

**•****需求非常明确：**家庭对于自动化家务的需求非常旺盛，比如衣物折叠、地面清洁、物品归置等，市场潜力巨大；

**•****数据采集便利：**可以通过家庭用户反馈及远程操控进行数据积累，来让模型持续获得多样化场景数据，进一步提升泛化和鲁棒性；

因此，PI 能够利用家庭场景的丰富数据和明确需求，将模型从实验室验证阶段快速推进到真实环境进行部署。

**03.**

**PI 如何重构通用机器人模型研发模式？**

**PI 从零构建机器人数据管线**

**Physical Intelligence 在机器人数据收集与模型训练方面采取了从零开始的系统性设计。**目前市场上没有现成的解决方案能够同时满足高鲁棒性和高灵巧性的需求，因此 PI 团队几乎从头搭建了整个数据引擎，目标是在短时间内让机器人具备初步的自主操作能力，同时为未来几年的规模化扩展奠定基础。

实际经验表明，数据管线的搭建和运行是整个流程中最关键的部分之一。团队超过一半的工作都集中在数据系统的构建、数据的有效收集，以及数据质量的保障上。

具体来说，团队设计了一套可以动态扩展的任务集合，用来检验目前能够完成的动作，比如叠衣服、买杂货等。人类操作员可以通过专门设计的运行环境和远程控制系统操控机器人。操作员借助引导臂，让机器臂模仿自己的动作，然后有专门的软件将操作员的动作转换为机器臂末端的控制信号。通过这种方式，机器人不仅能展现复杂且细致的操作，也能收集到高质量的数据用于训练。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/010.png)

PI 从 0 到 1 构建数据引擎来驱动机器人学习

整个数据采集过程由一个云端系统统一管理，这个系统能够实时监控任务执行情况，并动态安排数据采集和标注工作。标注完成后，数据被存入大数据桶，再根据训练需求进行筛选，投入模型训练流程。训练完成后，模型能够掌握执行任务所需的策略，并展现一定程度的自主规划与执行能力。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/011.png)

屏幕上的每个小方块代表某位操作员在某个周二执行的具体任务

通过这套方法，数据采集取得了显著进展。项目初期，市场上最大规模的公开数据集是 Open Cross Embodiment 数据集，约包含 3800 小时的机器人操作数据，这些数据主要来源于全球多家机器人研究实验室中的静态场景。

Open Cross Embodiment 数据集中的静态场景指的是在固定环境中进行机器人操作，如机器臂在实验台或受控空间内完成抓取、搬运等任务，这些场景的环境结构和摆放往往相对单一，缺乏真实生活场景的复杂动态变化。

而 PI 团队在运行自己的这套自主数据采集的流程六个月后，就累计收集了约 1 万小时的机器人操作的片段，涵盖了数十个不同的家庭环境和数百类任务，例如折叠衬衫、物品搬运和整理等。这些数据相比之前更贴近真实生活场景，任务类型也更丰富多样。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/012.png)

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/013.png)

滑动查看 PI 自主采集数据流程

再过了六个月之后，团队不仅在静态环境（如固定厨房、卧室的操作场景）中积累了更多数据，也开始借助移动操控系统进行大规模数据采集。移动操控系统指的是搭载在移动底盘上的机器人臂，能够在更大空间内灵活移动和操作，捕捉动态变化的环境数据。这一阶段采集的数据不仅任务范围显著扩展，还大幅提升了数据的多样性，具体体现在：

**•****环境多样性：**涵盖了数百种不同的场景，包括不同户型的厨房、卧室、客厅等，不同环境中的家具布局、光照、物品种类和摆放都有差异；

**•****动态变化：**相比早期静态实验环境，移动操控系统能捕捉到环境中物体被移动、人与机器人的交互等动态过程；

**•****任务复杂度：**从简单抓取扩展到折叠衣物、整理物品、搬运等更加复杂、细致的日常生活操作。

数据规模和多样性的提升使得机器人可以在多任务、多环境、多平台条件下表现出更强的自主执行能力和灵活性。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/014.png)

机器人在多样场景中规模化数据训练后提升了任务自主执行能力

特别的是，为了进一步验证泛化的来源，团队在保持训练样本总量不变的前提下，分别在不同类型的家庭环境中进行训练，再让模型在一个从未接触过的家庭中进行测试。结果发现，训练所覆盖的家庭越多，模型在新环境中的表现越好，甚至优于专门在该环境中训练过的模型。这一发现证明了，**提高数据的多样性是提升机器人泛化的关键路径。**

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/015.png)

训练场景越多，模型在开放世界的泛化能力越强

**“知识绝缘机制”重构训练流程**

除了在机器人数据采集上进行了系统性设计，PI 团队还在模型算法架构上实现了模块化升级。新模型采用了多模态融合的设计，能够更有效地整合视觉、语言与动作信息，实现更精准的环境感知与任务理解。而且在数据方面，模型不仅使用了静态和移动机器人操作的多样数据，还融合了网络图文、目标检测和带语言注释的交互数据。

这些改进都让模型训练成为了一个难题，因为传统的训练方案存在明显的两难：如果直接用 diffusion model 训练主干网络，会存在削弱模型理解图像和文字能力的风险，同时模型的训练速度也会比较缓慢；如果仅用机器人数据进行微调，最后泛化能力又会效果不好。

**灾难性遗忘（catastrophic forgetting）**指神经网络在持续学习新任务时，由于在面对新任务时有参数更新，模型在旧任务上学到的知识会被快速覆盖或丢失的现象。在多模态或机器人学习中，如果模型在 pre-training 阶段学会了较强的视觉和语言理解能力，但在后续用动作数据进行训练时没有妥善设计训练策略，就可能导致模型“遗忘”原有的语义理解能力，从而只能执行低层控制而缺乏高层任务理解。

为解决这一问题，**PI 的研究团队提出了“知识绝缘（Knowledge Insulation）”机制，创新性地重构了训练流程：**

**•** 首先，将连续动作序列离散化为 text-like tokens，使主干网络可以使用由自然语言处理的训练范式；

**•** 其次，在接入 Action Expert 扩散模块时截断梯度回传，保护主干网络免受扩散损失（diffusion loss）的干扰。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/016.png)

PI “知识绝缘”机制相关论文

这个方法不仅避免了 Action Expert 扩散模块对主干网络参数的冲击，还使模型的训练速度提升了 10 倍，使 π₀.₅ 在零样本任务中的表现与微调模型不差上下，同时还保持原有的泛化能力。

具体来说，π₀.₅ 使用的架构以 pre-training 的 Transformer 为核心，并拓展出一个 Action Expert Transformer 子模块。主干网络负责感知和理解场景语义，既能预测场景中的潜在问题，也能将人类的高层指令分解为可执行的子任务，例如将“清理我的卧室”解析为“拾起枕头”等具体动作。Action Expert Transformer 则接收主干网络的中间结果，并以更高频率运行，结合 diffusion model 和流匹配目标生成连续、平滑的控制动作，实现从语义到物理执行的高效衔接。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/017.png)

π₀.₅ 数据架构

此外，研究团队还提出了软硬件解耦战略，将智能软件作为系统核心，从而降低对特定机器人硬件的依赖。通过打造高度可移植、可复用的软件模型，系统能够快速适配多种机器人平台，大幅提升了模型在实际部署中的灵活性与效率。

**04.**

**在开放世界部署机器人的三大难题**

虽然 PI 对数据采集、模型架构和训练等方面做了一系列的改进，但在开放世界中部署机器人，依然面临着三大核心难题。

**•** **数据缺口**

**VLM 可以依赖海量公开的图文数据进行快速迭代，但机器人操作所需的数据远不如网络文本那样丰富与开放。**不同于自动驾驶在封闭道路中的“感知—避障”逻辑，机器人操作需要实际物理接触，在无人干预下，任务难度是呈指数级增长的。因为每次接触都可能产生一系列不确定性，例如物体变形、摩擦系数变化或受扰动等非线性效应，问题复杂度远远超过单纯的路径规划。

**而且数据的稀缺不仅在数量上，更在质量上。**收集大量错误数据对机器人的行为改进没有帮助，**因此我们需要获取正确的数据，也就是包含物理交互闭环反馈的时序数据**，例如机械臂施力与布料形变之间的对应关系。由于缺乏类似互联网这种通用数据源，在机器人领域，收集真实且有效的交互数据不仅门槛高，成本也极为昂贵。

**•****性能不稳健**

Karol Hausman 及部分团队成员认为，**目前机器人 VLA 面临的最大挑战是性能的稳健性，也就是如何真正“演示就绪（demo ready）”走向“部署就绪（deployment ready）”。**

这个问题不是仅仅扩大参数规模或增加数据量就能直接解决的，更需要在算法和架构上实现突破。尽管在现阶段，机器人在执行任务时仍会出现错误，但它们已经展现出了类似人类的适应能力，能够通过“试错-修正”的方式自我调整，并进行多次尝试直至完成任务，这使得机器人的行为更贴近真实的人类操作。

目前，虽然我们可以在 VLM 的基础上构建 VLA 模型，但机器人执行任务时，对动作指令的频率与延迟方面的要求极高，同时还必须具备应对物理扰动和感知不确定性的能力。π₀ 在开源后已经完成了跨领域迁移验证，例如无人机的空中抓取和手术机器人的精细操作，**但要实现商业化部署，仍需解决动作执行的时序错位问题。**

因为目前机器人在执行任务时通常会先获得一次观测结果，再进行推理，但推理过程往往需要数百毫秒，在此期间模型会假设环境静止不变，但现实世界是动态的，当新的动作预测生成时，环境状态可能已经发生改变，从而导致执行偏差。

为应对这一挑战，Kevin Zakka 提出了一种类似图像修复（image inpainting）的方法。类似 diffusion models 在图像中填补缺失区域，在机器人场景下，模型可以将已执行的动作视为“已知动作”（known actions），尚未执行的部分则视为“缺失区域”（masked regions），并根据这些信息对未来的行动轨迹进行补全和修正。这种方式无需重新训练主模型，属于纯粹的算法改进。换句话说，机器人在执行当前动作块的同时，可以并行计算并修复后续轨迹，从而提升整体稳健性。不过，Kevin 也强调，如果未来能显著提升推理速度，延迟带来的问题将从根本上得到缓解。

Kevin Zakka 是 U.C. Berkeley Robot Learning Lab 的博士生，导师是 Pieter Abbeel ，目前关注于全身控制（humanoid control）、数据先验（data priors）与仿真等领域。

**•****硬件平台迁移非常复杂**

**Tobias 认为真正制约大规模商业化和应用落地的，并非性能稳健性本身，而是跨硬件平台的迁移与泛化。**不同的机器人硬件在控制协议、感知系统和执行机制上差异巨大，缺乏统一接口层，导致通用模型的跨平台迁移非常复杂且成本很高。

Hausman 也指出，虽然目前硬件的机电一体化和传感技术已有很大进步，但早期的机器人 demo 就已经表明了硬件其实已经完全具备完成复杂任务的能力了，如前文所述，真正缺失的是具备类人智能的算法和模型。智能不足导致机器人在面对复杂、多变的现实环境时难以自主适应和决策，进而成为行业发展的主要阻碍。

因此，如果要在短时间内将机器人大规模推向实际应用，比如实现一年内落地上千台设备，**有一个重要前提就是同一个模型能够适配多种硬件平台，而无需针对每一种设备进行繁琐的个性化调整。**

一个典型案例是 PI 需要在远离办公地点的地方部署一台咖啡机器人。PI 此前从未接触过这款硬件设备，模型也没有针对这个机器人硬件进行过定制化训练，但它依然能够自主制作一杯咖啡。

这个挑战的复杂性也是远远超过自动驾驶的。后者多在封闭环境中训练强化学习模型，目标清晰、路径明确。而机器人任务，比如清理厨房，往往涉及多个非结构化子目标，且机器人本身的体态、控制方式和传感系统是高度异构的，**这些差异决定了机器人通用智能的研发不能照搬自动驾驶的技术路径，而必须重新设计任务表达和系统架构。**

目前还没有成熟的标准方案能够将这类大型机器人模型灵活部署到不同环境中，例如机器人本地或设备端。由于缺乏可直接使用的通用解决方案，多场景、多设备部署依然处于探索阶段。

**05.**

**未来可能会出现“机器人模型即服务”**

对于上述的三大难题，PI 在未来 1–2 年时间里，选择将重点放在了突破性能瓶颈这一问题上。

同时为减少对特定任务微调的依赖，PI 正在通过一系列算法改进，研发通用的任务“配方”，一旦这个“配方”实现，那么用户在获得基础模型后，就不再需要额外对模型做 post-training 就可以直接部署了。

PI 已经构建了一个覆盖多场景、多任务的标准化评估体系，希望能通过统一的 benchmark 来量化模型性能，确保算法和模型在不同环境下的表现都是稳定可靠的。PI 还通过与硬件厂商合作，希望能优化软硬件整体系统的性能，解决机器人在不同平台上部署时的适配和性能问题。

这个评估体系由 Physical Intelligence 为 π₀ 开发。这一体系的核心目标不仅是统计单一任务的成功率，而是在跨场景（不同家庭环境、不同物体组合）和跨任务（清理、折叠、搬运、组装等）下全面衡量模型的泛化表现。PI 通过开放 benchmark 的形式，将评估标准嵌入实际数据集与任务接口，使研究者和开发者能够在相同条件下运行 π₀ 或衍生模型，从而实现可重复、可比较的量化评估。

**未来，团队希望构建一个通用且可定制的机器人智能生态，让不同类型的机器人都能执行多样化的任务。**类比 LLM 的发展，PI 希望打造一个智能平台，在这个平台上，用户可以通过自然语言发布命令或做少量示范，就能直接引导机器人完成复杂操作，从而降低机器人使用门槛，提高交互效率。

**PI 还希望能推动软硬件的深度融合，用户可以设计和定制硬件，同时像写程序一样向机器人注入智能算法。这种方式被称为“物理世界的 vibe coding”**，能够让机器人智能的开发和迭代更灵活、更高效。通过这种设计，PI 希望打造一个开放协作的生态系统，让开发者、企业、硬件厂商和用户共同推动机器人技术的发展，实现机器人在实际生活和工作中的应用。

如果上述这些目标都能实现并推广开来，将会对机器人产业和日常生活产生影响。PI 认为，未来 5-10 年，在家庭中，具备通用智能能力的家庭机器人可能可以普及，它们可以完成叠衣服、清洁、整理物品等任务，提高生活便利性。在工业领域，PI 的技术可以让机器人快速适应多变的生产线，提升制造效率和柔性生产能力。

**这还可能催生新的商业模式——“机器人模型即服务”（RMaaS）**，通过云端和本地部署的智能平台，为企业和个人提供定制化机器人解决方案。

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/018.png)

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/019.png)

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/020.png)

排版：范诗翎

延伸阅读

[![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/021.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517203&idx=1&sn=1444daf92341aadaeee873f0a7479c53&scene=21#wechat_redirect)

拾象 AGI 观察：LLM 路线分化，AI 产品的非技术壁垒，Agent“保鲜窗口期”

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/022.png)

[![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/023.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517002&idx=1&sn=2d057443bcfc87ad9ea30507b4de0089&scene=21#wechat_redirect)

软件行业“快时尚化”背后的经济学 ｜ AGIX PM Notes

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/024.png)

[![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/025.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247516804&idx=1&sn=d58cb33ce44f2f896b4a5b33d68991a8&scene=21#wechat_redirect)

竞购 Chrome，正面竞争 OpenAI，Perplexity 为什么要做 AI 浏览器？

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/026.png)

[![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/027.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247516757&idx=1&sn=9f99d92639525ca5a31d034a30a17749&scene=21#wechat_redirect)

对谈 Memories.ai 创始人 Shawn: 给 AI 做一套“视觉海马体”｜Best Minds

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/028.png)

[![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/029.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247516719&idx=1&sn=302c937188de1b79c78192713d0006a6&scene=21#wechat_redirect)

GPT-5 不是技术新范式，是 OpenAI 加速产品化的战略拐点

![](../images/2025-08-23-physical-intelligence-he-xin-ji-zhu-tuan-dui-fen-xiang-wu-li/030.png)
