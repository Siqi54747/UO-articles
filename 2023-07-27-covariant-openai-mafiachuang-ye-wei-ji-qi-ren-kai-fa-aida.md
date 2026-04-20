---
title: Covariant：OpenAI Mafia创业，为机器人开发AI大脑
publish_date: '2023-07-27'
publish_timestamp: 1690459200
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/0E0qI6qsk-rYl-vTaY15gg
msgid: 1000000211
appmsgid: 2247503441
itemidx: 1
digest: 拥有 AI 大脑的机械臂如何与现实世界交互？
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgyeTuXbQlMdhhzcwgZzWOfs5NEPskicicy5mKZTPwNSGaKmRZKy9TrddnYFNTZZS5N65Zr8wia00icW1w/0?wx_fmt=jpeg
image_count: 34
archived_at: '2026-04-20T01:22:03+08:00'
---

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/001.gif)

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/002.png)

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/003.png)

作者：Kefei、Haozhen

排版：Scout

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/004.png)

随着过去几年电商渗透率快速提升，仓储、物流场景对效率、自动化的需求不断增强。Pick and Place 是仓储和物流系统中非常重要的一环，将其进行自动化是提升物流效率的核心，我们看到越来越多的 Pick and Place Robot 被部署在仓储和物流场景中。

**将 Deep Learning 应用于 Pick and Place Robot 也是行业关键变量之一。**在应用 Deep Learning 以前，Pick and Place Robot 通过获取特定物品的 3D 模型进行拣选，该方法的局限性在于机器人很难拾取此前没有建模和编码的新物品，且在部署到实际场景时，需要针对特定物品手动调整算法，过程非常复杂且低效。因此，基于传统方法，Pick and Place Robot 只能在结构化的场景中进行，无法 scale 到复杂场景。加入 Deep Learning 算法后，机器人不需要针对特定对象进行建模，而是通过大规模数据的训练，机器人可以从自身经验中学习，完成更新、更广泛的任务。

Covariant 就是在 Deep Learning 这波浪潮中起来的一家将 AI 技术应用到机器人领域的公司。Covariant 于 2017 年成立，创始团队成员分别是 UC Berkeley 教授 Pieter Abbeel 和他的三位学生 Peter Chen、Rocky Duan 和 Tianhao Zhang。**其中，Pieter Abbeel、Peter 和 Rocky 三人在创立 Covariant 之前，都曾在 OpenAI 工作。**Pieter Abbeel 教授是 AI 和机器人领域非常重要的人物，是将深度强化学习应用在机器人领域的先驱。

公司核心产品是 Covariant Brain，即一个通用的 AI 系统，在计算机视觉层面已经能够做到较好的通用性和可靠性。Covariant Brain 可以适配到不同硬件中，与下游硬件厂商或集成商一同为客户提供服务。同时，Covariant 也在开发自己的硬件，提供端到端的解决方案。**Covariant 目前从仓储和物流的 pick and place 场景切入，公司长期愿景是研发出可以使机器人适用于各类场景、完成各类任务的通用的 foundation model。**

**机器人的 foundation model 是我们非常期待看到的，如果能够实现，在家庭和商业场景中都将产生巨大的价值。**但目前仍有很多困难的问题需要解决，比如 Covariant 选择切入的 manipulation 环节如何实现泛化就是学术界目前重点关注但尚未解决的问题，除此之外还有许多系统化、工程化、商业化方面的问题。本文也针对这些问题进行了讨论。

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 什么是 Covariant

02 团队与创业故事

03 竞争与客户视角

04 关键问题讨论

**01.**

**什么是 Covariant**

**产品**

Covariant 是一家将 AI 技术应用到机器人领域的公司，公司于 2017 年成立，核心产品是 Covariant Brain，即一个通用的 AI 平台，**建立在预训练模型之上，机器人可以自主学习，以适应各种环境的变化，完成各类任务。**Covariant 目前从仓储和物流场景的 Pick and Place Robot 切入，公司长期愿景是开发出可以使机器人适用于各类场景、完成各类任务的通用 AI 系统。

**Covariant Brain 有如下特点：**

**• 通用 AI 平台**

Covariant Brain 可以让机器人从自身的经验中学习，抓取各类物品，例如机器人既可以抓取服装、杂货等商品，也可以抓取包含了多种类型物品的板条箱。无论物品的形状、大小或包装如何，都能保证一定的准确率和稳定性。Covariant Brain 还可以实现跨多个设施、实现多个用例的自动化。**Covariant Brain 核心是一套软件系统，适配不同的硬件，也可以适应客户现有的系统和上下游流程。**

**• 预训练**

Covariant 的训练数据来自于机器人与现实世界的交互，Covariant Brain 基于来自世界各地的机器人的数百万条经过筛选的数据进行预训练。

**• 可以适应物品的变化**

Covariant Brain 通过向所有联网机器人学习来不断改进，使得 Covariant Brain 能够适应 SKU 和商品的变化。

**应用场景**

**Covariant 从仓储和物流场景的 Pick and Place Robot 切入**，具体应用包括订单履行、包裹分拣和分割、按灯拣选、卸垛、感应等。

**1. Robotic Putwall**

批量拣选和退货处理的自动分拣（Automated sortation for batch-picking and returns processing operations）：Covariant 的 AI 机器人可自主对混合 SKU 的容器进行物品分拣。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/005.gif)

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/006.gif)

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/007.gif)

*Source：Covariant 官网*

**2. Robotic Induction**

自动感应到单元分拣机、袋式分拣机、自动导向车和自动装袋机（Automated induction onto unit sorters,  pocket sorters,  AMRs,  and auto-baggers）：机器人自主将物品投入单元分拣机、袋式分拣机、自动导向车和自动装袋机等设备，机器人可以自动执行重复的手动流程。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/008.gif)

*Source：Covariant 官网*

**3. Goods-to-Person Picking**

机器人从存储、穿梭车、自动导向车和其他自动化仓储与检索系统中进行拣选（Robotic picking from cube storage, shuttles, AMRs, and other ASRS）：机器人可以将传统的货到人系统转变为自动化的货到机器人系统。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/009.gif)

*Source：Covariant 官网*

**4. Robotic Kitting**

用于联合包装、配餐和订阅服务的自动化组装（Automated assembly for co-packing,  meal kitting,  and subscription services）：机器人自动从装了食品等的袋子中挑选物品并将其放入外发箱、垃圾箱或袋子中。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/010.gif)

*Source：Covariant 官网*

**5. Robotic Depalletization**

将混合 SKU 的托盘自动卸垛到传送带上（Automated depalletization of mixed-SKU pallets onto a conveyor）：将会减轻工人的压力，确保存储和拣选区域按时补充并最大限度地提高吞吐量。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/011.gif)

*Source：Covariant 官网*

**客户**

Covariant 现有客户包括 Fortna、Knapp、ABB、Bastian 等仓库集成商和物流公司。

例如，全球最大的纯合同物流提供商 GXO 部署了 Covariant 驱动的 KNAPP Pocket Sorter Induction 来对服装进行分类；Radial 部署了机器人 Putwall 来实现自动化分拣并提高设施吞吐量；美国最大的药品分销商 McKesson 部署了由 Covariant 驱动的 KNAPP Pick-it-Easy 机器人；Otto Group 与 Covariant 建立了长期战略关系，在 Otto 集团的履约中心将部署一百多个 AI 机器人来处理订单拣选过程。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/012.png)

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/013.png)

*Source：Covariant 官网*

**02.**

**团队与创业故事**

**团队**

Covariant 创始团队有四名成员，分别是 UC Berkeley 的教授 Pieter Abbeel 和他的三位博士生 Peter Chen、Rocky Duan 和 Tianhao Zhang。其中，Pieter Abbeel、Peter Chen 和 Rocky Duan 三人在创立 Covariant 之前，都曾在 OpenAI 工作。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/014.png)

*从左到右分别是 Rocky Duan、Tianhao Zhang、*

*Pieter Abbeel 和 Peter Chen*

*Source：Covariant 官网*

Pieter Abbeel 教授是 AI 和机器人领域的重要人物，是将深度强化学习应用在机器人的先驱。Pieter Abbeel 现为 UC Berkeley Electrical Engineering and Computer Sciences 的教授，研究领域包括 AI、CIR(Control, Intelligent Systems, and Robotics) 和机器学习，研究中心有 BAIR (Berkeley Artificial Intelligence Research Lab)、BDD (Berkeley Deep Drive)、Cal-MR (Center for Automation and Learning for Medical Robotics)、CHAI (Center for Human Compatible Artificial Intelligence) 和 CPAR (CITRIS People and Robots)。**Pieter Abbeel 教授最富盛名的是在 AI、机器人和强化学习等方面的领先研究。**他推动了深度模仿学习（deep imitation learning），深度无监督学习（deep unsupervised learning），迁移学习（transfer learning），元学习（meta-learning）和学习学习（learning to learn) 等领域的进步。

Pieter 于 1977 年出生在比利时安特卫普，2000 年获得比利时鲁汶大学电气工程学士和硕士学位，并在斯坦福大学获得计算机科学博士学位，他师从吴恩达，在 2008 年完成博士学位后成为 UC Berkeley 电气工程与计算机科学系的助理教授，之后创立了伯克利机器人学习实验室（Berkeley Robot Learning Lab）。2016 年到 2017 年，Abbeel 加入 OpenAI，并发表了大量关于强化学习、机器人学习和无监督学习的文章。同时在 2016 年，他成为 Berkeley 人工智能研究实验室 (BAIR) 的联合主任，2017 年成为 Berkeley 的终身教授。

**Pieter 认为 AI 和构建智能系统的结合点就是机器人。**2010 年，他研发了一款能够叠衣服的机器人，因此闻名学术界。2012 年，Geoffrey Hinton 和他的学生在图像识别上的突破激发了 Pieter “所有事物都可以完全被学习”的想法。2021 年 Pieter 获得 ACM 计算奖（ACM Prize in Computing），ACM 提到：**“Pieter 率先教会机器人从人类演示中学习（学徒学习）和通过自己的反复试错学习（强化学习），这为下一代机器人技术奠定了基础。”**

Pieter 除了于 2017 年联合创立 Covariant 之外，2014 年与 UCB 的 Arjun Singh、Sergey Karayev、Ibrahim Awwal 共同创立了 Gradescope ，专注于使用 AI 帮助教师对作业和考试进行评分，目前被全球 500 多家大学使用，该公司于 2018 年被 TurnItIn 收购。他还创立了 Berkeley Open Arms，聚焦于低成本、高性能的 7 自由度机器人手臂，该公司已获得 Berkeley Blue Robot 项目的知识产权许可。2021 年，他加入了投资 AI 初创公司的 AIX Ventures 作为投资合伙人。在此之外，他还主持了每周播客 Robot Brains，采访 AI 和机器人领域的科学家、创业者和投资人。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/015.png)

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/016.png)

*Source：Pieter Abbeel 个人主页、Linkedin*

除 Pieter Abbeel 教授外，Covariant 还有以下 3 位创始团队成员：

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/017.png)

**创业故事**

Covariant 的创业起源于 Peter 与 Rocky 在 Berkeley 的一次聚会。当时团队刚刚发表了一篇强化学习领域的论文，Peter 认为强化学习缩小了 AI 机器人能做的事与人所能做的事之间的差距，但下一步需要从一个非常务实的维度考虑问题，比如机器人需要操纵的对象是什么，需要以什么样的精度和周期来做，环境变化是什么，机器人类型是什么，硬件类型是什么等等。**Peter 认识到学术界的抽象追求和客户实际问题之间存在差距，这也是他们创立 Covariant 的原因之一，Covariant 希望把最好的 AI 科学家带到需要解决的特定问题上。**之后团队花费了很长时间走访不同的行业做调研，包括制造业、物流业、农业、餐厅、回收中心等等，最后从市场需求出发选择了仓储和物流领域。

在仓储和物流领域，Covariant 关注 manipulation 环节，即 AI 如何操纵所有进入仓库或者配送中心的物品，**实际上意味着需要 AI 可以操纵世界上存在的每一件物品。**Peter 认为由于世界上物品种类的多样性，尝试去解决操纵问题非常有趣且没有捷径，如果操纵问题能够解决，AI 机器人的大部分问题都能够解决，这也是 Covariant 聚焦于操纵问题作为 AI 机器人进入世界的入口的原因。Covariant 团队坚信即使有不同的操纵用例存在，但实际上可以通过建立同一个 AI 系统来解决所有挑战，**因为这些挑战的核心是相同的，都是理解世界上有什么东西，东西在哪里，以及如何更好地操纵等等。**

Peter 在采访中曾言改进机器人有两种方法，一种方法可以视为类似改进机器人大脑结构，另一种方法则可以视为让机器人的大脑经验变得更好。让机器人从人类的操作中获得数据和经验就是经验积累的部分，**但机器人必须要有一个有足够能力吸收数据的大脑结构，这也是 Covariant 所关注的重点。**Covariant 的研究团队在过去几年中取得的研究突破和进展都属于改善大脑结构本身的范畴。而 Rocky 认为要解决机器人问题仅仅开发和改进算法是不够的，**更重要的是需要获得足够多的、正确的数据。**同时在学术环境中能够接触到的真实数据有限，**AI 机器人必须能够在商业环境中大规模地部署移动设备，才能形成真实数据的闭环，这也是团队决定创立 Covariant 的关键原因。**

2017 年，Pieter Abbeel、Peter Chen、Rocky Duan 和 Tianhao Zhang 联合创立了 Covariant 来推动机器人的发展，Covariant 从仓储和物流领域切入，力求建立通用的 AI 平台来解决所有场景的操纵问题。

**融资**

2023 年 4 月 Covariant 宣布在 C 轮融资中额外筹集 7,500 万美元，这是对 2021 年 7 月 8,000 万美元的 C 轮融资的进一步补充，目前 Covariant 的融资总额已达 2.22 亿美元。本轮融资由 Radical Ventures 和 Index Ventures 领投，CPP Investments 和 Amplify Partners 跟投。此外，这一轮融资还有新的投资者 Gates Frontier Holdings、AIX Ventures 和 Northgate Capital 加入。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/018.png)

在 Covariant 的投资人列表中，还有一群在 AI 方面有着杰出成就的科学家，如 Jeff Dean、李飞飞、Geoffrey Hinton、Yann LeCun 等等。

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/019.png)

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/020.png)

*来源：Covariant 官网*

**03.**

**竞争与客户视角**

**Amazon**

Amazon 是 Covariant 主要竞争对手之一，在技术与场景方面与 Covariant 十分相似。

**• Robin 机械臂：**

2021 年，Amazon 推出一款名为“ Robin ”的机械臂，专门负责处理较轻的包裹。Robin 可以计算如何识别、移动和分类通过传送带呈现的可能彼此叠放的包裹，并抓取包裹、旋转并扫描以了解目的地的邮政编码，对卸垛机起到了补充作用。

**• Cardinal 机械臂：**

2022 年 6 月，Amazon 推出 Robin 迭代版的 Cardinal。Cardinal 可以举起和移动重达 50 磅的包裹，也可以准确读取包裹标签，将单一包裹挑出来放在 GoCart 中。Amazon 目标是 2024 年在所有物流中心部署该技术。

**• Sparrow 机械臂：**

2022 年 11 月，Amazon 推出 Sparrow 货物装箱拣选机械臂，这是 Amazon 仓库中的第一个可以检测、选择和处理库存中单个产品的机器人系统。利用计算机视觉和 AI，Sparrow 可以识别和处理数百万件物品，且 Sparrow 不再局限于方正的物品形状，可以直接处理形状、大小各异的物品，比如可以抓取日化用品、玩具等，但对于松散或复杂的包装，Sparrow 处理起来仍然有困难。

**尽管技术与场景十分相似，但 Amazon 不一定与 Covariant 形成直接竞争关系，而有可能成为供应商与客户的关系，据了解，Coviariant 也正在接触 Amazon，希望能够在 Amazon 的仓库部署一定数量的机械臂，但是让 Amazon 开放自己的场景给外部供应商有一定难度。**

**其他竞争对手**

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/021.png)

上述列举的竞争对手为仍在进行 AI 研发投入、仓储和物流场景的机械臂厂商。不过，Covariant 的竞争对手不止上述公司，下游集成商也是强劲的竞争对手，包括 ABB、Dematic、AutoStore、FANUC、KUKA 等。

根据客户访谈发现，即使 Covariant 可以直接向客户出售他们的产品，但很多客户的仓库里本来已经有了其他的自动化或数字化系统，如自动存储和检索系统，或一个从 SAP 购买的完整的仓库管理系统，又或是从 Dematic、KNAPP 等大型自动化公司采购的控制系统。在这种情况下，客户更希望和原有系统开发商或集成商谈采购方案，且更加信任集成商的方案以及集成商对上游供应商的选择和背书。**此时，Covariant 与下游集成商就成为了竞合关系。**

竞争是指 Covariant 本可以独立将自己的产品出售给客户，但由于客户和集成商沟通的意愿更强，对集成商信任度更高，从而导致 Covariant 变成二级供应商，议价权和品牌影响力受到影响。合作是指，实际上此现象较为常见，因此选择与集成商合作或许能带来更多的客户和订单。

除了以上两类竞对，如果从技术路线和 Covariant 的愿景出发，希望做机器人的 foundation model，那么竞对还包括 Google、Tesla、Nvidia、Meta 等。

以上从 3 个维度分析了 Covariant 的竞争对手，每类竞争对手均为不同类型的企业。但如果我们从客户角度出发，通过客户访谈我们发现客户在选择供应商时最不关心的是技术路线，最关心的是以下两个方面：

**• 效果**

效果是客户在选择供应商时最关心的问题。有客户表示：“我们不关心机器人的名字，机器人的品牌，机器人的技术路线，它能否把工作做好，这是最重要的。” 我们可以**将效果细化为精确度和可靠性**，如果机械臂操纵的精确程度不足够高，需要人为干预，则会影响整个业务逻辑，营运成本无法控制。而如果可靠性不够强，则有可能捡错或损坏包裹或物品，同样带来额外的成本。

此外，目前 Pick and Place 场景有个技术卡点在于机械臂无法精确地将产品放置在盒子的特定位置，或将其排列整齐，因此对于部分物品如易碎物品，还需要进一步人工手动进行摆放和包装。

**• ROI**

ROI 也是客户关注的主要因素。生产力提升多少、成本下降多少、是否能算得过来账，都是客户重点考虑的因素。客户通常从机器相比于人工作业时间的延长、工作效率的提升、以及一台机器能替代多少人等角度进行计算。但要注意的是，当机器人 AI 能力不足够强，可靠性无法得到保证的时候，运维成本将增加，这里的运维成本更多是指运维人员的人力成本，运维人员的成本通常比物流和仓库里普通工人的成本高。**因此，在某些时候，机器看似减少了人力，实际上减少的是低成本的人力，高成本的人力反而变多了。**

除此之外，一些细节也会影响 ROI，如机器人的占地面积应该尽可能小，任何一个系统或一台机器放在仓库里就意味着剩余的可存储的空间变小，收入变少。用户非常在意这些细节，而根据用户反馈，Covariant 团队对场景的理解和细节的把握很深入。

**04.**

**关键问题讨论**

**1. AI 泛化能力突破的 timing？研发投入与企业自身造血能力的权衡？**

Covariant 团队表示，公司的最终愿景是开发出能够用于商业和家庭场景的、从 manipulation 环节延伸至其他各环节的通用的机器人 foundation model，但这在今天的学术界依然是一个难题，若想实现此愿景需要一定的时间、大量的研发投入以及更多顶尖的人才。

即使只看 Covariant 目前切入的 manipulation 一个维度，**manipulation 能力的泛化目前是机器人学面临的最难解的问题之一**。目前学术界普遍认同的一种相对主流的方法是 manipulation 的泛化可以通过收集足够多的数据实现，但基于此方法，我们依然会遇到一些问题，比如收集哪些数据？什么是高质量的数据？各类数据的配比分别为多少？这里面有非常多的 tricks，就像训练 LLM 一样，是一项实验工程，需要非常多的时间和资源投入。**另一方面，公司所选择的路线、收集数据的方法等等也会对成本和 timing 产生很大影响。**

利润丰厚、资源丰富的大厂或许不需要考虑上述问题，但对于创业公司而言，可能会面临企业研发投入与企业现金流之间的权衡或妥协。

此外，目前 AI 机器人公司的财务模型很难打正，由于今天的 AI 技术仍无法使机器人达到 99.9%（甚至需要更高）的通用性，长尾问题不断出现，导致运营成本居高不下，拖垮了财务模型。有的客户甚至因为长尾问题而需要改变业务逻辑。

许多机器人公司都从一个美好的通用机器人愿景开始，追求极致的 AI 能力和极致的硬件能力，但最终都不得不陷入极致的专业化和结构化的解决方案中，只有这样客户的 ROI 才能打正，客户才会采购产品，企业才能生存下去。

因此，对 AI 技术发展的追踪和 timing 的判断十分关键。目前业界对 manipulation 能力泛化的 timing 判断分歧较大，没有相对统一和收敛的答案，我们只能保持关注。

**2. 机器人大脑是否可以独立存在？软件厂商是否需要拥有硬件能力？**

在个人电脑时代，有苹果这样软硬件一体的公司，也有微软这样靠操作系统占据巨大市场的公司。在机器人的世界里，独立的机器人大脑或机器人操作系统能否独立存在，能否与不同硬件适配，从商业角度看能否有独立的市场等一系列问题也是我们在研究机器人 foundation model 时十分关注的问题。通过研究 Covariant，我们目前得到的结论是**机器人软件厂商最好也需要有硬件实力，一方面，拥有端到端的、一体化的能力可以离客户更近，另一方面，仅有软件实力在商业和数据反馈上会受到较大限制。**

仅有软件实力的厂商在商业上无非采取两种模式，一是与下游的集成商合作，这是目前比较主流的形式；二是直接为终端客户开放 API，适配到客户当前拥有的硬件设备中。

**第一种方式会遇到的问题包括：**

• 传统集成商的硬件设备不擅长处理 AI 所能处理的复杂行为。

• 产品、核心客户、商业模式不同，导致传统集成商对于销售带有 AI 属性的设备的动力不足。传统集成商出售的产品数量众多，客户多为传统客户，因此客户可选择的范围广，对应到每个上游供应商和品牌商的采购概率就会变小。另一方面，传统客户对 AI 的采用程度不高。因此会导致一个现象，有的集成商一年卖出几千台设备，但几千台设备中仅有大约 50 台是带有 AI 能力的设备，50 台中或许又仅有 10 台设备选用了某家软件供应商的系统。

• 部分资金或技术实力较强的集成商会在内部孵化自己的 AI 团队，进而减少外部采购的需求。

而第二种方式的问题在于，该方案对客户而言有一定门槛，需要客户自身对 AI 有较强的理解，和较强的使用 AI 的能力，否则合作起来很困难，后续运营中也容易出现较多客户无法解决的运营问题，带来较大的运营成本。

**Reference**

https://www.youtube.com/watch?v=UfNftHnYAYk

https://www.youtube.com/watch?v=QhDLHWR04Rk

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/022.jpg)

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/023.png)

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/024.png)

延伸阅读

[![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/025.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503355&idx=1&sn=587f9d2354699b5531e797c9c5f3b157&chksm=ce9b7265f9ecfb73a213f324904851a4bde4223cf9728b28ccbe289ea7969c9eebe596da4787&scene=21#wechat_redirect)

拾象实践：为了理解AI-Native，我们做了几款AI应用

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/026.png)

[![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/027.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503155&idx=1&sn=ce93d9e4476ca641d2c5f1283d4ef563&chksm=ce9b72adf9ecfbbbc90a551840965531cb8174620b4bbc31a6d03489c70bf3e611a3cca64bf6&scene=21#wechat_redirect)

Perplexity AI，比Google Bard和Bing Chat更靠谱的问答引擎

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/028.png)

[![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/029.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503042&idx=1&sn=64c30e9be599064b90f8b57891ab1f9d&chksm=ce9b735cf9ecfa4a2c3fb60d4de31d02b52ce15406eb2feab41854d3749ae305abdd4cf4cee7&scene=21#wechat_redirect)

OpenAI基金首批投资赛道，Kick是下一代ERP雏形？

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/030.png)

[![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/031.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502793&idx=1&sn=f4ab1b8b4b063bfa992f8238cba93f7e&chksm=ce9b7457f9ecfd41b163ec2c3658d961de85bedf111865a6e4af0be9516a35d8db40a5fba207&scene=21#wechat_redirect)

GPT-4 的“秘密”：MoE、参数量、训练成本和推理设计

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/032.png)

[![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/033.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502724&idx=1&sn=3d3eea620abbb46f09dc3b7440ac36be&chksm=ce9b741af9ecfd0c595c2dff9a1190affb8d015361c355e0fb9dc975eff63dff93aa12308d84&scene=21#wechat_redirect)

AI Agents大爆发：软件2.0雏形初现，OpenAI的下一步

![](../images/2023-07-27-covariant-openai-mafiachuang-ye-wei-ji-qi-ren-kai-fa-aida/034.png)
