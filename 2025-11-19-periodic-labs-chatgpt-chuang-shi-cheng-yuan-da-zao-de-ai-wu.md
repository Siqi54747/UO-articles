---
title: Periodic Labs：ChatGPT 创始成员打造的 AI 物理学家，让 Agent 在现实实验中学习
publish_date: '2025-11-19'
publish_timestamp: 1763553600
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/cvibAn3nLMDwpfZ3hubM7g
msgid: 1000000458
appmsgid: 2247519510
itemidx: 1
digest: 尽管奖励函数的设计在数字任务上有很大提高，但科学研究仍依赖现实实验反馈
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgwB1qarVZpsUMAfIQibsOicddooyXjBGYqpZZVB3YJql0UyicW9eVLDCbRpiaEomSuufzeDMMgiaTgeXwQ/0?wx_fmt=jpeg
image_count: 29
archived_at: '2026-04-20T04:46:59+08:00'
---

[![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1)

作者：Ivy、Haozhen

今天，Gemini 3 正式发布，在多项基准测试中登顶：在“Humanity’s Last Exam”中成绩约为 37.5% （此前最高约为 26.5%）；在 ARC-AGI-2 中成绩约 31.1%（Gemini 2.5 成绩约 4.9%）。Gemini 3 再次展示了 LLM 在推理与多模态理解上的快速跃升，LLM 已成为通用智能研究的前沿。

可当将 LLM 应用于解决现实世界中的物理和化学问题时，传统的 AI 训练模式却暴露出了明显局限：过度依赖互联网数据，缺乏真实实验的迭代与反馈，难以支撑科学发现所需的高精度推理。Periodic Labs 因此诞生。

Periodic Labs 由 ChatGPT co‑creator Liam Fedus 和 DeepMind 材料科学负责人 Ekin Dogus Cubuk 创立，目标是打造能自主设计并执行现实实验的 “AI 物理学家”。团队从高温超导和磁性材料切入，希望为未来的科学超级智能（scientific superintelligence）奠定基础。

团队的核心思路是将 LLM、模拟（simulation）与高通量实验（experiment）紧密结合。通过自建实验室，团队能生成高质量实验数据，并以物理规律驱动的奖励函数取代传统数字评分器，让 agent 能像科学家一样从实验迭代中学习。今年 9 月，Periodic Labs 完成 3 亿美元种子轮融资。

本文结合了团队最新访谈和公开信息，拆解了 Periodic Labs 的技术壁垒、团队背景，以及他们是如何通过“AI 物理学家”重塑 AI 在科学研究中的传统角色。

**01.**

**Periodic Labs 是什么？**

Periodic Labs 是一家前沿 AI 研究实验室，希望能利用 LLM 加速物理学和化学领域的研究与开发。他们的目标是构建一个能够自主设计并执行现实世界实验的“AI 物理学家”。这种能力的潜在应用领域非常广泛，包括先进制造、材料科学、化学工程以及任何需要在物理世界进行研发的产业链。比如，如果能在实验中发现一种能在 200 Kelvin 条件下工作的超导体，将会重塑人类对宇宙的认知。

团队认为，实验（experiment）、模拟（simulation）和 LLM 的紧密结合是至关重要的，为此，他们正在搭建一个能够产生高通量、高质量实验数据的物理实验室，从而可以让三者共同迭代。此外，团队还设计了基于物理规律的奖励函数，取代传统依赖数学或代码评分器的奖励方式，使模型能够从真实实验结果中获得更可靠的学习反馈。

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/002.png)

**现实实验是 AI 物理学家的核心环节**

Periodic Labs 认为，在逻辑学和数学之后，物理学将成为 LLM 下一阶段的重要探索方向。尤其是那些与人类生活联系更紧密、处于量子力学（quantum mechanics）能量尺度的研究领域，例如凝聚态物理（Condensed Matter physics）、材料科学和化学。

“量子力学能量尺度”指的是只有在原子、分子、电子等微观层面、以量子力学才能准确描述的典型能量范围，例如电子能级差、化学键能、晶格振动能等。换句话说，它就是微观物理过程所涉及的能量量级，远低于核反应或高能物理的能量范围。

而要让 LLM 真正成为面向量子力学的基础模型，关键在于让模型具备科学研究所需的迭代能力。但目前的模型还无法做到这一点，因为科学本质上需要依赖不断循环的模拟、理论计算和实验。如果模型无法像人类研究者那样在迭代过程中进步，它就无法真正“发现”科学。因此，必须让 LLM 学会科学探究的方法，而这一点只能通过真实的物理实验来实现，而不能仅依赖模拟。

以 ChatGPT 为例，早期的 ChatGPT 使用标准的 RLHF 训练，主要依靠监督数据和基于人类偏好的奖励函数进行优化。然而，当时的奖励函数更强调“像一个友好的助手”，而忽略了“数学正确性”或“代码有效性”。因此早期模型的数学能力并不好。因此，如果缺乏针对目标任务的真实反馈信号，奖励函数就无法有效引导模型朝正确方向优化。

尽管目前奖励函数的设计已经取得了显著进展，但这些进步主要还是体现在数字任务、互联网数据处理和论文分析上，也就是说训练 ChatGPT 等模型的技术只是在数字世界中取得了巨大进步，但科学研究仍依赖于现实世界的实验反馈。因此，Periodic Labs 希望把实验纳入模型的迭代循环中，让实验结果直接成为 AI agent 的奖励信号和优化依据。

目前 Periodic Labs 正在建设的首个实验室就是一个用于粉末合成（powder synthesis）的实验室，机器人可以在其中混合、加热粉末，从而可以发现新的超导体、磁体等关键材料。这种方法简单、廉价且适合机器人执行，核心方法就是量子力学。

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/003.png)

总的来说，Periodic Labs 认为，科学研究本质上是一个依赖不断试验与反馈的迭代过程，只有具备实际动手能力，才能真正取得进展。因此，在 Periodic Labs 的体系中，一切成果都以最终实验结果为核心衡量标准：

**•**  在高温超导研究中，只要能突破目前环境压力下 135 Kelvin 的纪录，就能证明方法有效。

这里的“纪录”指的是目前在环境压力（ambient pressure）条件下实现的最高超导转变温度 135 K，这是高温超导研究中被科学界广泛认可的公开最高值。

**•**  在更应用导向的场景中，评价依据则是材料的具体性能，如延展性、韧性或强度。系统能否依据基础科学发现以及航天、国防、半导体等行业的需求，发现并制造出具备特定目标特性的材料，是判断团队是否成功的最终标准。

但需要注意的是，虽然 Periodic Labs 重视现实实验，但同时，团队也会借助物理模拟工具和机器学习方法来预测材料属性，来提高研发效率。此外，Periodic Labs 还将 agent 所调用的工具视为由其他神经网络或 agent 组成的模块集合，这样的模块化方式既提升了开发效率，也避免了重复构建已有能力。

**发展路线图：从高温超导切入 AI 物理学家**

Periodic Labs 非常相信 AI scaling laws，但也指出这一原则只有在直接服务于他们真正关心的目标时才有意义，也就是推动科学发展，尤其是物理领域的研究与开发。

目前高温超导性和磁性是 Periodic Labs 的重点研究领域，团队选择这两个领域是因为这些问题本身具有高度复杂性和挑战性。

以高温超导为例，团队将超导性作为最先攻克的方向的原因主要有三个：

1、从哲学层面看，如果能发现一类在 200K 实现超导的材料，将会深刻改变人类对宇宙和量子效应的理解。

2、从技术角度看，超导性是一种相变（phase transition），临界温度主要由晶体的基本性质决定，对缺陷或微观结构等难以模拟的细节具有较强的鲁棒性，因此是一个易于验证、技术上可行的切入点。

3、最重要的一点是，虽然团队以高温超导为核心目标，但他们在实现这个目标前需要完成一系列前置任务，包括自主合成、自动表征，以及利用 LLM 进行材料模拟和分析，这其中的每一步技术突破都将推动他们向最终的科学超级智能（scientific superintelligence）迈进。这就类似于 DeepMind 和 OpenAI 要通过层层任务推进 AGI，Periodic Labs 也将这些领域视为通向科学超级智能的必要阶段或者中转站，而不是与目标无关的支线任务。

自主合成指的是自我管理的合成过程，它无需持续的人工干预就能设计、执行、监控和调整实验条件来制造新材料或化合物。

自主表征指的是一个自动化、智能化的过程，用于对合成的材料进行分析和测量，从而确定材料的结构、组成和关键属性。

总的来说，高温超导是一个能够凝聚物理学界共识的基础性难题，Periodic Labs 认为，只有在至少一个领域完成从理论到实验的完整循环，他们才能真正摆脱停留在论文和教科书层面的局限，更进一步朝“AI 科学家”的目标迈进。

**商业化路径：成为研究人员的 Copilot**

尽管高温超导性是非常好的北极星指标，但 Periodic Labs 深刻明白技术路线和商业路径必须相互匹配。为了确保公司在推进科学的同时具备可持续性，他们需要一条能够在中期实现商业可行性的路径，也就是在先进工业中，充当工程师与研究人员的 Copilot。

就像前沿 AI 实验室用 AI coding 提升了软件工程的效率一样，Periodic Labs 也希望为航天、国防、半导体等高度依赖材料与物理迭代的行业提供智能化工具。这些行业虽然拥有庞大的科研预算，但始终缺乏能高效进行物理学领域迭代的数字化工具。Periodic Labs 能够显著加速这些团队的研发流程，缩短迭代周期，并最终推动他们更快取得研究进展。

在将成果部署到航天、国防、先进制造等行业时，考虑到这些行业一方面正在探索自身的 AI 路线，另一方面又普遍面临技术更新缓慢和专业知识流失的问题，Periodic Labs 采用的是“登陆并扩张”（land and expand）的策略。

“登陆并扩张”（land and expand）指企业先以一个小而明确的切入点进入客户体系（land），在证明价值后再逐步扩大使用范围与合作深度（expand）。

也就是说，Periodic Labs 的部署方式不是要求客户彻底重构生产线，而是先找出企业内部最突出的瓶颈和最关键的问题，并将这些具体需求映射到 Periodic Labs 的系统能力上，以此向客户展示自身技术能显著加速问题解决的效果。在具体操作上，Periodic Labs 会先与客户共同界定清晰、可评估的问题范围，然后围绕客户最关心的任务进行优化，进一步找到企业内部最有推动力的团队和最紧迫的需求，并将这些需求与 Periodic Labs 最先进的技术能力结合起来。

**02.**

**团队背景**

**创始人**

Periodic Labs 的创始人是 Liam Fedus 和 Ekin Dogus Cubuk。 两人在 Google Brain 相识并共事，之后分别加入 ChatGPT 和 DeepMind。

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/004.png)

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/005.png)

Liam Fedus 和 Ekin Dogus Cubuk 的工作经历

**•****Liam Fedus**

Liam Fedus 是蒙特利尔大学（MILA）计算机科学博士生，主要研究方向为生成模型和 RL。和大多数 ML 研究员一样，他也是物理学背景出身，先后在 MIT 和加州大学取得物理学学士和硕士学位，研究方向包括监督学习、无监督学习和 RL，研究目标是构建稳健可靠的算法。

作为 ChatGPT 的共同创建者（co‑creator），他最初在专注于数据和评估的 RL 团队工作，之后领导了 post training 研究团队，他在将 OpenAI 研究成果转化为可实际使用的 ChatGPT 产品方面发挥了重要作用。在担任 OpenAI post training 团队的 VP of Research 期间，他负责领导团队监督 AI 模型在初始训练后的优化这一关键环节，从而使模型成为安全、一致、可全球部署的产品。

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/006.png)

**•****Ekin Dogus Cubuk**

Ekin Dogus Cubuk 先后在 Swarthmore College、Harvard、Stanford 求学，2017 年获得了 Stanford 材料学的博士后学位。在 Harvard 读博期间，他的研究方向为原子系统的结构复杂性，涵盖从无序固体到催化表面等领域，主要运用密度泛函理论和机器学习方法研究无序固体和电池材料的物理性质。他在 2017 年加入 Google DeepMind，工作了八年时间，是材料科学与化学研究负责人。这期间，他主要研究大型神经网络的扩展性和域外泛化特性，以及它们在清洁能源和信息处理等材料发现领域的应用。

**团队建设**

Periodic Labs 团队的研究人员大致可以分成三类：ML 背景的科学家、物理学或者化学背景的科学家、具有复合背景的科学家。团队认为，让前两类科学家紧密协作至关重要，关键结合点在于要帮助物理学家和化学家理解应该如何指导 LLM 对物理和化学问题进行推理。

目前，团队正在评估哪些步骤应纳入模型的 pre-training 和 RL 训练中，以教会 LLM 对量子力学等物理系统进行推理。同时，LLM 研究人员也在学习物理学的知识、相关模拟工具以及研究目标。

在团队氛围上，团队内部提倡“没有愚蠢的问题”（no stupid questions culture），鼓励物理学家、化学家和 ML 专家进行跨学科交流。团队发现，计算机科学家（computer scientists）常常以类似 API 的思维方式来处理问题，这有助于将科学家的陈述转化为明确的输入、输出和目标。这种跨界人才在团队沟通中发挥着关键作用，他们连接了纯粹的 ML 或 LLM 专家、实验主义者和模拟专家，通过翻译和连接不同群体的信息，使得信息可以在团队内流转。

以 API 的方式思考问题是指将一个复杂的过程或功能格式化，定义清晰的边界、输入、处理逻辑和输出。

在具体形式上，团队通过每周教学会议，让成员互相分享各自领域的知识，例如 RL 循环、数据清理以及科学发展史等。这些内部知识交流不仅服务于团队希望实现的超导性目标，也提升了 Periodic Labs 在客户项目中应用 LLM 的能力。因为团队发现，客户在阅读文献、进行模拟、计算和实验等流程上的操作方式，与 AI Agent 在团队内部的工作流程高度相似，因此内部培训直接增强了服务客户的效率。

**团队成员**

目前，Periodic Labs 团队总共约有 30 人。对于研究人员来说，Periodic Labs 研究人员的特质与 OpenAI、Anthropic、DeepMind 等前沿 AI 实验室高度相似，但团队认为，最关键的区别在于：他们是否真正认同“加速科学”这一使命。根据目前公开的信息，Periodic Labs 研究人员情况具体如下：

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/007.png)

**•**团队中 ML 或 AI 背景的研究人员

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/008.png)

**•**团队中物理或化学背景的研究人员

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/009.png)

**•** 团队中有复合背景的研究人员

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/010.png)

值得一提的是，Periodic Labs 表示公司在招聘时其实并不要求候选人必须具有物理或化学的高等学位。团队认为，当代科学知识庞大而细碎，即使是顶尖物理学家也会有难以覆盖的知识空白，所以没有物理背景的新人与顶尖专家之间的差距并不像看上去那么大。尤其在发现新超导体这类高度复杂的任务中，协作是当代科学进步的必然要求，因为没有任何个人能够同时全面掌握化学、物理、合成和表征等所有环节。

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/011.png)

因此，Periodic Labs 对理想候选人的核心期待包括：

1、具有深度好奇心，真正渴望在更深层次上理解 ML 和科学；

2、具有使命驱动力，将“加速科学”视为宏伟目标；

3、务实且严谨，以解决方案为导向，能快速达成目标；

4、在 ML、实验或模拟这三个维度中的某个维度上达到顶尖水平；

5、具有强烈的紧迫感，公司的目标是尽快实现 LLM 在科学改进方面的突破，而不是等待十年再突破。

此外，Periodic Labs 非常重视与学术界的联系，因为许多模拟工具和新颖的合成方法都是在学术界开发出来的，而且学术界还能让公司更好地了解关键的科学分析任务、思维方式以及基础技能原语（primitives），从而弥补业界在这些方面的不足。为了深化和学术界的联系，Periodic Labs 采取了两项主要举措：

1、成立了一个涵盖超导性、凝聚态化学、高通量 DFT（密度泛函理论）等专业知识的顾问委员会；

2、启动资助计划，支持学术界进行那些不适合工业界、但与 LLM Agent 在合成、材料发现、物理建模方面相关的研究。

**03.**

**融资情况**

2025 年 9 月，Periodic Labs 完成了 3 亿美元的种子轮融资，本轮由 Andreessen Horowitz（a16z）领投，其他投资者包括 Felicis、DST Global、NVIDIA、 Accel 和一些个人投资者。根据公开报道，在完成融资前，Periodic Labs 的估值达到了 10 亿美元，也有新闻表示最高达到了 15 亿美元，这笔交易是近期 scientific AI 领域规模最大的投资之一。

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/012.png)

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/013.png)

**04.**

**行业痛点**

在访谈中，团队提到，在用 AI 推动物理学研究的过程中，主要存在三个行业痛点：

**•** 痛点一：如何解决数据问题？

当前主流 AI 实验室普遍相信 scaling law，认为只要持续扩大算力和数据规模，就能最终解决物理学难题。Periodic Labs 表示这种规律虽然在经验上成立，但关键问题还是在于：“Y 轴究竟代表什么？”以及“模型的测试分布与真实的物理问题是否一致？”

Y 轴代表模型的性能指标，此处强调，即使模型在某个特定 Y 轴上不断取得更高的测试成绩，这个指标本身也未必等同于解决物理学或材料科学问题的真实能力。

具体来说，如果模型主要基于互联网信息进行 pre-training，那么它接触到的只是互联网的典型数据分布。这样的训练方式虽然能提升模型在域内（in domain）任务上的表现，但面对物理学中那些域外（out of domain）或分布外（out of distribution）的问题，性能提升的斜率可能非常小，也就是改进速度缓慢，甚至可能毫无用处。

例如，一个善于编程的模型，即便拥有大量互联网数据和反馈循环，也无法用这些知识去治愈癌症，因为模型缺乏在癌症领域进行完整迭代所需的实验数据与专业知识。

但即使在域内，AI 模型的性能也高度依赖训练数据的质量，当前高质量数据的获取仍有很大困难：

1、科学文献中关于某些物理性质的数据数值往往相差好几个数量级，质量参差不齐，存在显著的不确定性。只有通过亲自开展实验，才能获得可靠的数据并校正这些偏差。如果模型仅依赖这些嘈杂的文献数据进行训练，最终只会复制现有的错误与偏差，而无法推动对物理或化学的更深层理解。

2、某些关键的实验数据，例如形成焓数据或超导性相关的高质量数据，根本无法公开获得，或者能得到的数据往往污染严重，不能用来训练 ML 模型。

3、科学界通常缺乏负面结果的发表，导致公开的研究大多只展示成功案例。但在构建有效的科学模型时，一条明确的负面结果同样是极其重要的学习信号。

**•** 痛点二：如何实现模拟的自动化？

当前，客户最迫切希望解决的问题之一就是模拟（simulations）的自动化，包括自动化开发过程中的关键工具、处理格式匹配等基础问题，以便将模拟结果顺畅地接入材料设计管线。

**•** 痛点三：现有方法过度依赖检索

在实际研究中，许多公司仍主要依赖检索（retrieval）等轻量级方法。Periodic Labs 认为，更有效的路径应当是通过 pre-training 和 mid training，将关键知识直接写入模型的权重中。然而，当前的监督训练效率较低，模型的表现仍类似于 ChatGPT 的早期阶段，难以把分散的知识系统化地整合成一个或一组统一的模型。因此，Periodic Labs 主张采用高算力强化学习（high-compute RL）作为更可行的解决方案。

需要注意的是，在 Periodic Labs 的解决方案中，mid training 的原子单位（atomic unit）包括各类知识形式，从晶体结构（crystal structures）等底层物理描述，到“如何制造某种材料”这类高层语义，都需要统一整合到模型中。只有让模拟数据与实验数据在分布上连贯相接，模型才能具备更强的泛化能力，最终成长为真正理解物理和化学的专家。

Mid training 是指介于 pre-training 和 post training 之间的一个训练阶段，指在 pre-training 和 post training 之间注入大量新的、以前不存在的知识，可以用于解决模型知识截止（knowledge cut off，指的是模型在训练完成时所能获取的知识范围会停在某个时间点，之后新出现的事实、数据或研究进展，模型无法自动知道）或获取实时知识的问题。

**05.**

**为什么过去做不成 AI 物理实验室？**

团队认为，以前没有人能真正建成 AI 物理实验室的原因主要有两个：

首先，这一方向所需的技术高度复杂，对团队专业度有非常高的要求。Periodic Labs 之所以能在此时推进，是因为 Periodic Labs 团队在 LLM、实验和模拟三大核心支柱上都汇聚了顶尖人才。具体来说，团队认为目前专业知识是非常分散的，因此他们在每个支柱下都寻求细分领域的专家：

**•** 实验领域包括凝聚态化学、凝聚态物理、自动化、设施操作；

**•** 模拟领域包括理论物理、编程模拟；

**•** LLM 领域包括中期训练（mid training）、RL、基础设施（infra）。

其次，实现 AI 物理实验室所需的关键 AI 技术仅在过去几年才出现，而模型训练所依赖的实验与模拟数据又主要掌握在少数工业企业手中，这些企业通常对近期 AI 技术缺乏深入理解，因此在此之前，没有团队能够真正完成这项工作。

**06.**

**市场竞争**

虽然过去没有团队能实现 AI 物理实验室，但目前 Periodic Labs 的宏观战略其实与 Radical AI 有相似之处，两家公司都认为现有文献缺乏高质量的实验数据来训练科学的基础模型，因此它们都筹集了大量资金来构建 AI 物理实验室，目标是 AI 生成的假设能够直接连接到现实世界的实验中，利用现实实验的反馈作为强化学习信号，最终让模型学会一种贴近科学推理过程的“科学直觉”（scientific intuition）。

除了初创公司，AI4M 领域也有大公司入局。比如 2023 年，DeepMind 发布了 GNoME，可以识别用于材料开发的新晶体，2023- 2024 年，微软先后推出了 MatterGen 和 MatterSim，这两款工具都是专门为材料发现而设计的。

**Radical AI**

Radical AI 成立于 2025 年初，希望能通过将 AI、工程学、物理理论与应用研究相结合，重塑材料的设计、开发与发现流程。今年 7 月，公司完成了由 RTX Ventures、NVIDIA 等投资方参与的 5500 万美元种子轮融资。

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/014.png)

公司构建了一个由 AI 驱动的材料研发闭环系统，用于加速材料的发现与开发。这个系统结合了高通量分子量子力学方法、由原子预测建模和生成方法组成的 AI 引擎以及具有自动化化学合成和表征功能的全自动驾驶实验室。整个“材料飞轮”由四个环节构成：

1、预测：利用先进的原子级和生成模型，从数十亿种材料组合中筛选出结构与物性最具潜力的候选者

2、优化：结合计算、自适应实验和主动学习，对候选材料的化学合成路径进行持续优化

3、自动化：通过高效率的机器人实验室执行材料的合成与表征，实验速度超过人工效率

4、反馈：数据会被重新输入回预测引擎中，从而形成闭环

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/015.png)

2025 年 4 月，公司发布了 TorchSim，这是一款下一代 PyTorch 原生原子模拟引擎，这个引擎在原子模拟方面实现了显著提速：相比 ASE （Atomic Simulation Environment） 快了 100 倍，比 DFT （密度泛函理论） 快 1 亿倍。

在访谈中，Periodic Labs 表示，虽然两家战略相似，但在研究材料的具体方向上还是存在差异：

**•** 今年 8 月，Radical AI 宣布了与美国空军的合同，专注开发用于高超音速飞行的高熵合金；

**•** Periodic Labs 将发现高温超导体作为北极星目标，并将通过实现自主合成（autonomous synthesis）和自主表征（autonomous characterization）等路径来实现。

2025 年 8 月，Radical AI 获得了美国空军（DAF）下属 AFWERX 的一份 D2P2（Direct-to-Phase II）合同，合同金额约为 120 万美元。该合同目的是为了应对高超音速飞行条件下的极端环境，Radical AI 将协助开发新型高熵合金（HEAs），以提升材料的热机械性能，满足美国空军对先进合金的需求。

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/016.png)

排版：傅一诺

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/017.png)

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/018.png)

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/019.png)

延伸阅读

[![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/020.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247519468&idx=1&sn=7966d04995a859f4a138abc1d676c7f2&scene=21#wechat_redirect)

Snowflake CEO 复盘：为什么 LLM 时代企业需要一个 AI Data Cloud？

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/021.png)

[![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/022.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247519409&idx=1&sn=ff433823fb92ddc4ba0e9aa55966952c&scene=21#wechat_redirect)

AI Bubble 深度讨论：万亿美元 CapEx，Dark GPU，广告电商如何带飞 AI｜Best Ideas

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/023.png)

[![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/024.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247519321&idx=1&sn=fc53c50e23296ab6d3504468e80f0785&scene=21#wechat_redirect)

Leogra AI：BVP 投资的欧洲版 Harvey，给每位律师配一位协作 Copilot

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/025.png)

[![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/026.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247519279&idx=1&sn=38988fa076d39737e15c66ac03ef725b&scene=21#wechat_redirect)

对谈 Sora 核心团队：Sora 其实是一个社交产品，视频生成模型会带来科研突破

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/027.png)

[![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/028.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247519240&idx=1&sn=30efcbe447c20697b48ae09291da43cf&scene=21#wechat_redirect)

联手 OpenAI 发布 ACP，Stripe 是如何思考 Agent 支付的？

![](../images/2025-11-19-periodic-labs-chatgpt-chuang-shi-cheng-yuan-da-zao-de-ai-wu/029.png)
