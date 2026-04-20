---
title: Anyscale：Databricks 创始人再下场，ML 领域最值得期待的公司？
publish_date: '2022-12-28'
publish_timestamp: 1672230427
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/lKaEJsRkKnRkdDE9C2uOiQ
msgid: 1000000155
appmsgid: 2247499563
itemidx: 1
digest: 手握相同剧本的 Anyscale 能否复制下一个 Databricks？
cover: https://mmbiz.qpic.cn/mmbiz_jpg/3tHNibnJ2jgw62gr4jjJZYbKhrprtPsPwnH0Z90L2c8DYHWyxMC2omw9dLLh8JXHtTTPXfYxLXe8huFw49F21fw/0?wx_fmt=jpeg
image_count: 21
archived_at: '2026-04-20T00:03:27+08:00'
---

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/001.gif)

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/002.png)

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/003.png)

作者：Kefei

编辑：penny

排版：Lydia

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/004.png)

2013 年，UC Berkeley 的 7 位学者创立了著名的数据与人工智能公司 Databricks，Databricks 是云计算趋势下最成功的 data infra 公司之一，2022 年 8 月收入超过 10 亿美元，最新估值达到 380 亿美金，成为一级市场的超级独角兽。在 Databricks 创始团队中，有一位名叫 Ion Stoica 的教授。2019 年，Ion 带着 Berkeley 的另外两名学生 Robert Nishihara 和 Philipp Moritz 再次创立了一家新的初创企业——Anyscale。

**带着 Databricks 的光环和相似的剧本，Anyscale 一经成立就获得了大量的关注和期待。****Anyscale 是一个机器学习分布式计算平台，基于开源框架 Ray 进行设计。**Ray 同样出自 Anyscale 团队之手，Anyscale 与 Ray 的关系就像 Databricks 与 Spark，最近大火的 ChatGPT 就是基于 Ray 的框架训练。Ray 目前在 Github 上有 2.3 万个 stars，4 千多次 forks，以及 760 多位 contributors。

2021 年 12 月，Anyscale 完成了 1 亿美元的 C 轮融资，估值达到 10 亿美元，投资者包括 a16z、Addition、NEA、Intel 等。今年 8 月，Addition 和 Intel 又共同牵头追加了新一轮 9,900 万美元投资。

我们认为，**Anyscale 的高估值主要得益于团队和技术的优越性，但从产品成熟度和商业化角度看，公司仍十分早期。**从需求端看，机器学习分布式计算是否必要？典型应用场景有哪些？机器学习 scalability 的需求有多大？何时爆发？这些关键问题目前没有人能给出有信心的预判。从供给端看，Ray 尚未成为行业标准，Anyscale 的商业化产品也暂时未找到 Product/Market Fit，商业价值仍不清晰。

不过，鉴于 Ion 丰富的成功创业经历、优越的技术实力、深厚的行业资源以及吸引人才的能力，我们有理由相信他能够带领 Anyscale 在 AI/ML 时代复制 Databricks 的传奇。

**🦄️ 活动预告**

**【****Anyscale****主题闭门讨论会】**

**围绕 Anyscale，海外独角兽将在近期组织一场小型线上闭门讨论，邀请对 Anyscale 有研究洞见的朋友一起探索和讨论。如果您对我们的活动感兴趣，欢迎填写问卷！我们会对问卷结果进行筛选后和您联系。**

**· 讨论主题：**Anyscale 的未来与挑战

**· 活动形式：**线上闭门讨论（20 人以内）

**· 活动时间：**具体时间报名成功后通知

**· 报名方式：**填写问卷

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 Anyscale 与分布式计算

02 产品：新一代分布式计算平台

03 Databricks 明星创始人再下场

04 市场与竞争

05 核心判断

**01.**

**Anyscale与分布式**

**计算**

**公司简介**

Anyscale 于 2019 年成立，是一个基于 Ray 构建的分布式计算平台。Ray 是一个开源的分布式计算框架，可以将 AI/ML 和 Python 的 workload 从单机拓展至多台计算机上，从而提高 workload 的运行效率。

Anyscale 是开源项目 Ray 背后的商业化产品及公司，Anyscale 与 Ray 的关系就像 Databricks 与 Spark。并且，Anyscale 与 Databricks 都出自同一个实验室——UC Berkeley 的 RISELab（AMPLab），且出自同一位教授之手——Ion Stoica。就像 2013 年带着一批学生创立 Databricks 一样，Ion 在 6 年后又带着另一批学生创立了 Anyscale，这也是 Anyscale 一成立就备受瞩目的原因。

除了 Ion 之外，公司创始团队成员还包括 CEO Robert Nishihara 和 CTO Philipp Moritz，他们都是 Berkeley RISELab 的博士毕业生。Ray 目前在 Github 上有 2.3 万个 stars，4 千多次 forks，以及 760 多位 contributors。

Anyscale 在去年 12 月完成了 1 亿美元的 C 轮融资，估值达到 10 亿美元，投资者包括 a16z、Addition、NEA、Intel 等。今年 8 月，Addition 和 Intel 又共同牵头追加了新一轮 9,900 万美元的投资。

**分布式计算**

分布式计算通俗理解就是指把一个规模庞大的计算问题分成若干部分，并分配给多台计算机进行处理，最后再把这些计算结果综合起来得到最终结果。分布式计算的两大优势为可扩展性和可靠性。

**· 可扩展性：**随着工作负载的增加，分布式计算可以通过向系统添加额外的节点来扩展至非常大的规模，让系统可以在不牺牲性能的同时，处理更大规模的数据和需求。

**· 可靠性：**分布式计算能最大限度地减少系统停机或中断时间，快速地处理故障。这是因为分布式计算系统将计算问题分配给多个节点处理，当一个节点出现问题时，系统其余节点仍可继续运行。

**为什么需要分布式计算？**

**· 数据量指数级增长**

在美国，每一家公司都是数据公司，数据指导实践的观念深入人心，这也造就了 data infra 公司的成功。随着越来越多企业利用数据这个杠杆，数据量急剧增加，到了 AI/ML 时代，数据量更是呈指数级增长。庞大的数据需要大量的计算资源，普通单机无法在一个令人满意的时间内完成任务，需要靠超级计算机来完成，但超级计算机的造价和维护十分昂贵。采用分布式计算可以将数据分布到不同的机器，不仅能效率提升，成本也得到控制。

**· 企业重视机器学习效率**

人工智能与机器学习被越来越多企业视为战略级方向和核心竞争力，企业对人工智能与机器学习项目的开发速度和运行效率有了更高的要求。

**02.**

**产品：新一代分布式计算平台**

Anyscale 的产品定位是一个分布式计算应用平台。分布式计算一直以来都是业界难题，需要依靠高水平的 IT 开发人员手动分配资源，还要处理并发的问题，既复杂又耗时，具体的操作流程和工具长期以来没有统一的行业标准。

而 Anyscale 在做的事就是探索分布式计算的标准化流程，并将其抽象成简单易用的产品，使更多从事 AI/ML 的人，如数据科学家和机器学习工程师等等，都能在不依靠高水平 IT 人员的情况下，独立完成分布式计算。在 Anyscale 的环境中，开发人员不需要关心资源分配问题，Anyscale 会自动完成资源分配和并发执行。Anyscale 的出现降低了对开发人员的技术水平要求，为开发人员缩短计算时间，提高工作效率。

Anyscale 的分布式计算平台在开源分布式框架 Ray 之上建立。Anyscale 内部习惯将其开源产品称为 Ray，将商业化产品称为 Anyscale。

**Ray**

Ray 是一个开源分布式计算框架，开发者可以通过 Ray 来扩展 AI/ML 和 Python 应用，建立和管理计算机集群。

Ray 由一个核心的分布式计算架构（Ray Core）和一个用于简化 ML 计算的工具库（Ray AIR）组成，工具库包含了针对 Data、Train 等多个环节的工具和服务。

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/005.png)

**· Ray Data：**分布式数据预处理

**· Ray Train：**分布式训练

**· Ray Tune：**超参数调优

**· Ray Serve：**可扩展和可编程的服务

**· Ray RLlib：**可扩展的强化学习

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/006.png)

从位置上看，Ray 并不位于传统机器学习的 workflow 上，它在更底层的位置，负责扩展和加速 ML 各个环节的 workload。Ludwig、TensorFlow、PyTorch 等 AI/ML 框架可以在 Ray 之上运行。此外，Ray 可以在任意机器、集群、云、Kubernetes 上运行。

**Anyscale**

Anyscale 是基于 Ray 的云托管平台，也是公司的商业化产品。Anyscale 在 Ray 的基础上添加了不少 features 和服务，如可观测性、访问控制等等，目前还在探索数据安全等 value-add。

**与 Ray 相比，Anyscale 的一大优势在于它是一个集成了众多机器学习工具和平台的开发环境，AI/ML 项目的整个生命周期都可以在 Anyscale 一个平台上完成，实现从开发到生产的无缝衔接。**并且，客户若使用 Anyscale，就不需要内部自建团队去搭建和维护分布式计算系统，既方便又减少了一定的人力成本。

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/007.png)

公司与一众领先企业共同打磨产品，Microsoft、Amazon、Nvidia、Intel、IBM、Uber、OpenAI、蚂蚁、字节等 AI/ML 水平极高的公司都在使用 Ray 进行机器学习工作。Anyscale 已有付费客户，但大多数公司仍使用开源的 Ray，未给商业化产品付费。

**03****.**

**Databricks 明星创始人再下场**

团队是 Anyscale 刚成立就备受关注的核心因素，Anyscale 创始团队来自 UC Berkeley RISE 实验室，联合创始人包括 Ion Stoica、Robert Nishihara（CEO）、Philipp Moritz（CTO）。Ion 是团队的灵魂人物。

**· Ion Stoica**

Ion Stoica，UC Berkeley 计算机科学系教授，RISE 实验室首席研究员，他最有名的代表作是 Spark 和 Databricks，Ion 是 Spark 的联合发起者，也是 Databricks 的联合创始人兼执行主席。

事实上，Anyscale 是 Ion 的第三个创业项目。2006 年，Ion 与 Hui Zhang 创立 Conviva，Ion 担任 CTO。Conviva 致力于人工智能视频分析技术的开发，为客户提供视频分发服务，以及针对视频传播渠道、观看人群、收视体验等方面的实时监测、分析和优化。Conviva 获得了 Foundatin Capital、NEA、GGV 等投资机构的支持。

2013 年，Ion 与 UC Berkeley 的 6 位学者共同创立了著名的数据与人工智能公司 Databricks，Databricks 是基于云计算趋势下最成功的 data infra 公司之一。Databricks 基于开源项目 Spark 进行开发，成功将 Spark 推向市场，并成为大数据处理的行业标准。同时，Databricks 的商业化十分成功，2022 年 8 月收入超过 10 亿美元，当前估值 380 亿美金。

除了两家创业公司，Ion 还曾领导了两个备受瞩目的开源项目：Apache Mesos 和 Tachyon。其中，Mesos 曾一度大受市场追捧，Mesos 发布于 2009 年，是一个开源的分布式计算框架，由 Berkeley AMPLab 开发。2010 年，Twitter 使用 Mesos 成功解决了频繁宕机的问题，Mesos 也因此受到关注。不过，随着云计算的普及和以云为核心的容器化基础设施项目的迅速崛起，如 Kubernetes，基于传统技术架构的 Mesos 逐渐暴露出许多问题。2019 年 5 月，Twitter 宣布其基础设施将从 Mesos 全面转向 Kubernetes，Mesos 黯然离场。

Ion 目前领导着 UC Berkeley 的 Sky Computing 实验室，他们在 2021 年发表了一篇论文，From Cloud Computing to Sky Computing，旨在探索下一代云计算。他们近期还发布了开源的机器学习框架 SkyPilot，基于 SkyPilot，用户可以在任何云上运行 ML 工作负载。

**·****Robert Nishihara 和 Philipp Moritz**

其他两位成员 CEO Robert Nishihara 和 CTO Philipp Moritz 是 Ion 的学生，技术能力极强。公司员工评价 Robert 是一位思想很 sharp、野心很大、执行力很强的 CEO，整体评价较高。

**04.**

**市场与竞争**

**市场**

Anyscale 位于机器学习分布式计算赛道，早期从强化学习场景切入，后拓展至传统机器学习领域，包括数据摄取及处理、超参数调整、模型服务等等。但从技术层面和用户使用情况看，Ray 在强化学习场景中表现更为突出，在传统机器学习领域则没有明显优势。

以下是 Ray 的标杆客户的应用情况：

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/008.png)

从用户使用情况可以看出，Ray/Anyscale 尚未在某一特定场景成为行业标准，它现在更像是一个技术或框架，尚未找到足够 sharp 的需求和场景进行产品化，商业化处在极其早期的阶段，难以准确估算市场规模和企业价值。

**竞争**

Anyscale 面临的竞争主要来自 Databricks（Spark）和三大云厂商。

**1. Databricks（Spark）**

Spark 同样是一个分布式计算框架，被广泛应用于大数据处理。

**与 Spark 相比，Ray 的优势体现在：**

**· Ray 具备更好的容错性，拥有更高的计算效率**

一个建立在 Spark 上的 ML 框架，当它的一个工作节点运行失败后，Spark 的所有节点都会停止工作，计算只能重新开始；而如果 ML 框架建立在 Ray 上，一个节点停止工作时，Ray 的其他工作节点还可以正常工作。

**· Ray 更加底层，兼容性更强**

根据用户访谈，PySpark 的一个弱点是所有编程必须在 MapReduce 范式中完成。而 Ray 是一个非常底层的计算框架，一般的机器学习框架都可以在其上运行。这一特性使得 Ray 可以和不同的机器学习库集成，因此，Ray 不会将开发人员束缚在任何特定的范式里。

**与 Spark 相比，Ray 的劣势是：**

**· 渗透率低**

Ray 开源于 2018 年，是一个年轻的产品，团队在未来会进行频繁的功能开发，这意味着用户需要频繁地维护他们的代码。对比 Spark 等出现时间更长的分布式计算框架，Ray 拥有的网络资源更少。用户在使用 Spark 的过程中遇到问题时，可以轻易从互联网上搜索得到解决方案，但是 Ray 的用户就未必能够从互联网上获取更多有用信息。

另外，Ray 在传统机器学习场景的渗透率不高，已经采用 Spark 的公司在相当长的一段时间内不会抛弃 Spark 而选择 Ray。

**· 数据处理能力不及 Spark**

根据用户反馈，目前 Ray 在数据处理领域还无法与 Spark 竞争。事实上，很多公司会用 Spark 做 ML 前端的数据处理，而将 ML 的中间环节交给 Ray。从这里也可以看出，不论是 Spark 还是 Ray，目前都没有成为 AI/ML 领域的通用 infra，未来两者的竞争关系将会长期存在。

**2. 云厂商**

AWS，Azure，GCP 三大云厂商都有自己的分布式计算框架，这些计算框架与 Ray 构成直接竞争关系，给 Anyscale 带来一定的竞争压力。

**05.**

**核心判断**

**成功要素**

**1.****连续成功创业经验**

团队是 Anyscale 当前的最大亮点。Ion 是一位连续成功创业者，另外两位核心成员 Robert Nishihara 和 Philipp Moritz 是非常 smart 的年轻人。Anyscale 和 Databricks 一样，都起源于实验室，从开源项目起家，试图成为行业标准，并完成从开源到商业化的转变，路径几乎完全相似。Databricks 从 2013 年成立至今，踩过不少坑也绕过不少路，Ion 作为 Databricks 的联合创始人，可以帮助 Anyscale 避开 Databricks 此前踩过的坑，许多经验可以复用。

例如，Anyscale 在早期就将公司拆成两个独立的团队，一个团队负责开源产品 Ray，另一个团队负责闭源产品 Anyscale，开源团队的重心在于技术实力的提升、社区的搭建和运营等等，而闭源团队则更专注于产品力和商业化，这很显然复制了 Databricks 的做法，而这是 Databricks 花了几年时间才探索出来的经验与方法。

**2. 技术实力强劲**

技术水平也是 Anyscale 的核心竞争力。在我们调研访谈过程中，所有拥有技术背景的专家和开发人员都表示 Ray 和 Anyscale 产品背后的技术非常强，无论是从论文层面看还是从代码层面看，团队的技术实力都让他们感觉非常惊喜，这也给 Anyscale 带来一定的壁垒。此外，Anyscale 的客户和竞对都表示，Ray 比 Spark 更适合做 ML，Ray 能够与 ML 相关的框架更好地契合、以及打通工作流，与 Spark 相比，Ray 更 AI/ML-native。

**3. 人才和行业资源丰富**

由于超强的团队和技术实力，Anyscale 吸引了大量人才加入。Anyscale 部分员工表示，他们此前错过了 Databricks，不想再错过下一个大机会。Anyscale 招聘门槛较高，招聘流程繁琐冗长，薪资也低于大厂和同类创业公司的平均水平，但依然有大量的人才想加入。他们认为，Anyscale 团队技术实力强劲，且 Ion 这么多年来持续探索行业难题，提出了许多具有开创性意义的解决方案，即使未来 Anyscale 商业化遇到很大挑战，在个人成长方面依然有很大的收获。

此外，Anyscale 的行业资源也十分丰富，公司成立之初就获得顶级投资人 Ben Horowitz 的支持，Microsoft、Amazon、OpenAI、ByteDance 等全球领先企业与 Anyscale 团队保持十分紧密的联系，共同帮助 Anyscale 打磨产品，定期针对技术、产品、行业、战略等问题展开讨论，为 Anyscale 提供建议和反馈。与此同时，Anyscale 团队也为上述公司在探索人工智能与机器学习框架、分布式计算等方面提供不少帮助。

**4. 行业标准尚未形成，Anyscale 机会大**

分布式计算已不是新课题，但随着应用场景不断变化，分布式计算框架也需要随之演变。在经历了将近 10 年的发展，Spark 已成为大数据处理的分布式计算的行业标准，但随着场景切换到人工智能与机器学习，Spark 的局限性正逐渐暴露出来，AI/ML 时代的分布式计算标准尚未形成，而目前来看，Anyscale 是最有潜力、也是呼声最高的行业标准制定者。

**风险**

**1. 刚需程度**

Anyscale 在机器学习系统中处在相对底层的位置，并不在传统 workflow 上，换句话说，企业在进行机器学习工作时，有 Ray 更好，没有也不会影响项目的顺利开展，Ray 对于机器学习工作是一个锦上添花的存在，因此我们会对其刚需程度与必要性存疑。

锦上添花的工具在经济周期到来时会暴露出脆弱性，当经济下行，企业削减预算，企业将根据产品刚需程度从弱到强依次放弃产品。刚需程度弱的产品受周期影响较大。

此外，与其他架构相比，Ray 主要在强化学习领域表现出色，在传统机器学习领域则没有明显优势，因此从应用场景来看，需求也存在一定的局限性。

**2. 行业 timing**

**Databricks 之所以能够做到 10 亿美金的收入规模，成功实现商业化，除了把握住云的趋势外，很大程度是因为大数据处理到了需求全面爆发的时点。**Databricks 不仅被技术领先的科技企业所采用，更是破圈至传统领域，如金融、能源、医疗等。传统领域客户有以下特征：1. 资金充裕，付费能力强；2. 行业竞争充分，付费意愿强；3. 技术水平不高，有外采或外包技术产品的需求，付费意愿强。Databricks 的大额订单大多来自此类企业，而背后的核心条件是，此类企业有大数据处理需求。

因此，行业需求爆发时点同样是 Anyscale 商业化能否成功的关键因素。机器学习分布式计算的需求有多大？何时达到爆发时点？这些关键问题目前没有人能给出有信心的预判。但积极信号是，AIGC 对计算性能要求很高，对分布式机器学习有极大的推动，OpenAI 的 ChatGPT 正是在 Ray 上进行训练。而消极信号是，并非所有 ML workload 都需要高性能、高扩展性，性能和成本之间也需要平衡。

**3. 商业价值尚不清晰**

Anyscale 目前商业化路径尚不清晰，商业化产品与开源产品相比 value-add 也不显著，从用户留存表现看，产品力仍有待加强。例如，有用户反馈，开发人员目前无法得知数据被 Anyscale 传输到何处进行计算，这使得一些对数据安全性要求高的公司没有成为 Anyscale 的付费用户。

根据我们对 Ray 现有用户的调研也发现，许多标杆用户未来并没有计划为 Anysclae 付费，使用 Ray 只是为了学习和借鉴它的技术，帮助企业内部自建计算框架和机器学习架构。

**4. 没有数据留存，迁移成本低**

Anyscale 是一个轻量级的解决方案，开发人员只需要添加几行代码就可以把现有的代码转化为 Ray 代码。并且，Ray 只进行数据计算，没有数据留存。这些特点都代表着用户弃用 Ray、转向其他解决方案的迁移成本很低。

**建议**

鉴于 Ion 丰富的成功创业经历、优越的技术实力、深厚的行业资源以及吸引人才的能力，我们有理由相信他能够带领 Anyscale 在 AI/ML 时代复制 Databricks 的传奇。

一家 Infra 公司的成功，通常需要经历以下 4 个阶段：

1. 由于行业、趋势、场景的变化，新的需求出现，这个时候有需求但没有标准化产品，大型企业尤其是科技公司便在企业内部自建团队，靠几名高技术水平开发者从 0 到 1 手动搭建产品和框架，并在后续自主维护。

2. 技术和解决方案在实验室或企业内部运行一段时间后，开始有人试图抽象出相对通用的框架和产品，并向市场发布，有开源产品、也有闭源产品，但此时还没有形成行业标准。

3. 随着需求的增长，越来越多的客户使用和筛选各类产品，经过一段时间的市场检验，最终收敛到 1-2 款产品，行业标准形成。

4. 成为行业标准的产品和公司将基于现有的技术和产品，提供更多更有价值的功能和服务，提升产品和商业化能力，在商业化方面取得成功。

Anyscale 目前尚处在第 2 个阶段，公司已抽象出相对通用的框架和产品，但行业标准尚未形成，从投资角度看，此时入场风险较高。

我们也可以参考 Databricks 的成功经验去观察 Anyscale 的进展。Databricks 的成功可以大致概括为以下 2 个阶段：

1. 开源 Spark 成为行业标准。

2. Databricks 成功找到商业化产品的核心应用场景和 Product/Market Fit。当用户购买 Databricks 产品的 ROI 比使用“开源架构+内部自建团队”的方案更高时，用户开始为 Databricks 付费。

鉴于 Anyscale 技术和团队的优越性，以及其成为行业标准制定者的巨大潜力，建议持续跟踪项目和行业进展，关注行业收敛情况和公司商业化发展情况。

**特别感谢**

感谢李雨婷对本次研究的贡献。

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/009.png)

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/010.png)

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/011.png)

延伸阅读

[![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/012.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247499259&idx=1&sn=7f96988b91bbe25fbf896a782b0ff823&chksm=ce9b4265f9eccb735b42b4f43d7dbb11c89792df8b6b85ff81846c8be3c97ffd6a4e8eb1854b&scene=21#wechat_redirect)

Carta：估值85亿美元的资管工具，目标成为一级市场的纳斯达克

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/013.png)

‍‍[![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/014.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247498632&idx=1&sn=0227cec29558739f6e139446c446a8f9&chksm=ce9b4416f9eccd00de8b63097b6c613d41b2473fce4e2a9d52cdae10a0451135692c802cb9c7&scene=21#wechat_redirect)‍‍

Cresta：销售和客服的实时 AI 导师

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/015.png)

[![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/016.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247497830&idx=1&sn=cff092d2be0ff776661916344c4fbe6b&chksm=ce9b47f8f9ecceee1d41cfbbabde207bb7b137060c8336691c8845d274aae570490e0cc6f362&scene=21#wechat_redirect)

ICONIQ Growth：顶流富豪家办，SaaS隐形之王

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/017.png)

[![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/018.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247496770&idx=1&sn=95ad1010608a454a675b653f8676b2df&chksm=ce9b4bdcf9ecc2ca8bc42e379cb479b3cccad5d7cc70d829f4ea4c80818aa3af2002168e41ab&scene=21#wechat_redirect)

加息阴霾下，如何抄底美股优质SaaS 公司？｜拾象DAO Insight

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/019.png)

[![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/020.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247496196&idx=1&sn=670c90a6c1be8e7e93dcd00a87859d04&chksm=ce9b4d9af9ecc48c29c22ea7c6f3762cc920c7daaf68742b766e56e15ea3de4d9f4224ebd251&scene=21#wechat_redirect)

dbt：数据行业新物种，估值42亿美金的数据转换工具

![](../images/2022-12-28-anyscale-databricks-chuang-shi-ren-zai-xia-chang-ml-ling-yu/021.png)
