---
title: Weight & Biases：大模型军备竞赛的受益者，AI领域的Datadog
publish_date: '2023-03-03'
publish_timestamp: 1677844970
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/USxOJ7WUhvMHYmuB2-feUQ
msgid: 1000000176
appmsgid: 2247500649
itemidx: 1
digest: 模型实验管理 + 模型监控，是 AI/ML 领域 Datadog 级别的生态位。
cover: https://mmbiz.qpic.cn/mmbiz_jpg/3tHNibnJ2jgy23ibgAXoa8AdqXrWF9ib8GiccAc1xj67f7NUR2mkMT0ykms5Nkic42HtA6QJTkwVL1ES5bASox1VZwA/0?wx_fmt=jpeg
image_count: 33
archived_at: '2026-04-20T00:42:02+08:00'
---

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/001.gif)

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/002.png)

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/003.png)

作者：Kefei，Haihan

编辑：penny

排版：Lydia

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/004.png)

**模型训练是实验科学，是通过反复试错、迭代、求解的过程。AI/ML 科学家在训练模型时，往往要经历无数次的修改和迭代，如果将这其中的过程和经验记录下来，是一件非常有意义的事。**一方面可以了解模型训练进度、资源使用情况、训练过程中遇到的问题、以及如何解决问题等等，另一方面也可以和团队共享经验，共同协作完成模型搭建。基于此需求，模型实验管理工具应运而生，Weights & Biases 是该领域最具代表性的公司。

Weights & Biases 于 2017 年成立，由 CrowdFlower 创始人 Lukas Biewald 和 Chris van Pelt 以及前 Google 工程师 Shawn Lewis 联合创办。目前，**W****eights & Biases 聚焦在模型实验管理环节，未来有可能切入下游的模型监控领域。公司增长迅速，2022 年 ARR 增长 150%，****当前****已达到几千万美金，且 NDR 非常高，从增长到留存表现都非常优异。**

**Weights & Biases** **的价值在大模型中更加****显著****。**大模型训练的复杂程度和资源消耗程度使大模型企业对模型实验管理工具的需求激增，作为模型实验管理赛道的 top 1，Weights & Biases 是大模型企业的首选。OpenAI、DeepMind、Facebook AI Research、Midjourney、Stability、Nvidia、Microsoft 等公司均为 Weights & Biases 的客户。**OpenAI 使用 Weights** **&** **Biases 跟踪了 2,000 多个项目、数百万次实验和数百万名团队成员的模型版本。****而 Weights & Biases 的创立灵感也来源于 Lukas 在 OpenAI 的一次实习经历。**

**未来 3-5 年内，****Weights & Biases** **将持续享受大模型军备竞赛带来的红利，保持高速增长。但长期看，模型实验管理市场规模有限，如果想要有所突破，切入下游的模型监控环节是必要选择。**当 Apps 数量变多，我们需要 APM 工具，需要 Datadog；当 data 数量变多，我们需要 Data Observability 工具，需要 Grafana；如果我们假设未来模型变得很重要或模型数量变多，那么我们一定会需要模型实验管理、模型监控工具。并且现在 90% 的模型还没有被训练出来，训练出来的模型中 90% 还没有被投入生产，未来还有很大增长空间。

**模型实验管理 + 模型监控，是 AI/ML 领域 Datadog 级别的生态位，有机会诞生出 AI/ML 时代的 Datadog，而** **Weights & Biases** **被赋予最高期待。**

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 市场

02 产品与商业模式

03 团队

04 竞争

05 成功要素与风险

06 结论

07 融资历史

08 访谈纪要

**01.**

**市场**

一个模型的生产和部署往往不是一蹴而就的，需要经过多次修改和迭代，这样就会出现一个问题：**工程师难以保证下一次的修改一定是正确的，也难以保证下一版一定比上一版好。因此模型的版本管理变得十分重要。**试想如果模型版本不能被妥善管理，一旦修改错误无法返回上一版本或前面的某一版本，技术人员便将面临从头开始重新建模的困境。重现模型不仅造成了大量时间的浪费，也是对技术人员记忆力的巨大考验。

此外，IBM 首席 AI 科学家 Deborban Leff 曾表示，超过 87% 的 AI/ML 项目并未投入生产，主要原因是：1/ 数据存储位置、格式的多样性导致收集、清洗数据所付出的时间成本太高；2/ 团队协作的缺失。

**针对模型版本管理和团队协作两个痛点，Weights & Biases 应运而生——以模型实验管理环节为重点，**延伸至对数据准备、模型训练和模型部署的全生命周期的管理，为技术人员提供追踪模型版本、检验模型性能的功能，帮助其选择最优版本的模型进行上线，在团队协作和保证模型可复现性上发挥重要作用。

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/005.png)

当前，AI/ML 技术解决方案正被越来越多的企业和研究机构广泛接受和使用，MLOps 尤其是偏下游的环节正处于起步阶段，未来仍有较大增长空间。我们对模型实验管理市场规模测算如下：

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/006.png)

**据测算，全球模型实验管理市场规模预计在 2027 年达到 43 亿美元。**

**02.**

**产品与商业模式**

**Weights and Biases 是一个机器学习平台，核心产品是模型实验管理工具。**用户可以管理其机器学习项目，例如实验跟踪、数据集版本控制和模型管理，重点是协作、可重复性、可追溯性和透明度。Weights and Biases 应用行业分布广泛，覆盖自动驾驶汽车、医疗保健与生命科学、科学研究、通讯、媒体和娱乐以及公共部门等多个领域。

Weights and Biases 目标用户为机器学习从业者、研究机构、企业。以个人和团队用户为主，目前累计用户数已达到 50 多万，这些用户分布在 700 多家公司。**OpenAI 也使用 Weights and Biases 追踪了 2,000 多个项目、数百万次实验和数百万名团队成员的模型版本。**

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/007.png)

**模型版本与实验管理**

**用户可以在 Weights and Biases 以可视化的形式跟踪所有机器学习实验，可以在 web 或移动设备上查看模型的最新训练进度和结果，并能够通过使用协作托管功能，在团队间进行模型调整。**除此之外，用户还可以将实验文件和数据集如：超参数、模型权重，样本测试预测等直接保存到 Weights and Biases 或自己的存储空间中，方便以后对模型的重现，便于团队间的项目移交、协作。在自动对记录数据集进行版本化的同时，Weights and Biases 会在后台自动比较数据间的差异，保留最佳性能模型的检查点，确定最佳模型，删除重复数据，节约存储空间。**Weights and Biases 的实验追踪管理能够对用户的 CPU 和 GPU 使用情况进行监控，对相关指标进行实时可视化，以及识别模型训练过程中的表现和遇到的问题，提高资源的使用效率。**

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/008.png)

**协作空间**

这一项针对共享和跨团队协作的功能，用户可以在此界面分享和展示机器学习项目。传统的项目分享通常为屏幕截图或杂乱无章的笔记，但是在 Weights and Biases，用户可以将项目进展、介绍与结果以图表、笔记和动态实验的形式进行分享，邀请协作者对自己的项目进行编辑和实时评论。

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/009.png)

**可视化看板**

Weights and Biases 为分析和理解机器学习结果提供了一套交互式可视化和仪表盘，包括直方图、散点图和性能指标，并提供结构化分析。

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/010.png)

**超参数调优**

Weights and Biases 能够对超参数进行扫描，并带有默认可视化效果，使用者不用编写自定义代码，即可通过图表对机器学习实验进行直观的比较，最终使用 Weights and Biases 的输出结果为模型训练选择最佳超参数值。

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/011.png)

**模型部署**

模型部署提供了将机器学习模型部署到生产中的各类工具，在每个生命周期阶段集中管理所有模型版本，并能与 AWS 和 GCP 等云平台整合。

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/012.png)

Weights and Biases 有 3 种定价模式：个人版、团队版和企业版。

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/013.png)

我们从团队版定价可以看出，对于一个 10 人的 ML 团队，若购买基础版产品且不超过基本使用量，则每年花费 $600-1,800。我们也通过客户访谈得知，部分客户采购企业版产品，每年花费大约为 5-20 万美金。**因此目前来看，Weights & Biases 占企业预算金额并不高。**

**03****.**

**团队**

Weights and Biases 于 2017 年成立，由 CrowdFlower 创始人 Lukas Biewald 和 Chris van Pelt 以及前 Google 工程师 Shawn Lewis 联合创办。

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/014.png)

在创办 Weights and Biases 之前，Lukas Biewald 和 Chris van Pelt 就共同创立了 CrowdFlower ，数据标注公司 Figure Eight 的前身，该公司后来以 4.28 亿美元的价格被 Appen 收购。Shawn 有着 4 年 Google 软件工程师的工作经历，2011 年曾创立 Beep Networks，一家开发并提供云连接无线传感器的公司，由于市场竞争激烈于 2014 年宣布倒闭。

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/015.png)

**Weights and Biases 的创立灵感来源于 Lukas Biewald 在 OpenAI 的一次实习经历。**在工作中，Lukas 发现很多机器学习研究人员所使用的工具已经过时了，很大程度影响了工作效率和模型质量，由此产生研发一款方便 AI/ML 团队协同的工具，帮助他们更好地构建模型的想法。

**04.**

**竞争**

**1. 竞对类型一：模型实验管理创业公司**

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/016.png)

**2. 竞对类型二：模型监控创业公司**

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/017.png)

**3. 竞对类型三：成熟企业 ML 平台**

Google Vertex AI、AWS SageMaker、Databricks MLflow…

**• Comet vs. Weights & Biases**

**Comet 是 Weights & Biases 的主要竞争对手。Comet 产品与 Weights & Biases 高度重合，两者的核心区别在于主要客群不同，Comet 主要面向 enterprise 客户，而 Weights & Biases 更多面向个人用户或团队用户。**Comet 目前以服务超 150 家客户，包括 Uber、Shopify、Ancestry、Cepsa、Etsy 等，ARR 在 2021 年实现 5 倍增长。Comet 与 AWS SageMaker、Google Vertex AI、New Relic、TensorFlow 等平台合作紧密。Comet 对个人用户、学术团体、早期创业公司免费。

与 Weights & Biases 相比，Comet 的企业级功能更丰富。但 Comet 团队执行力不如 Weights & Biases，响应速度较慢，对客户需求和反馈也没有引起足够重视。早期，Comet 产品功能比 Weights & Biases 更完善，但 Weights & Biases 后来无论是产品丰富度、产品易用性还是用户体验都反超 Comet。**因此，在创业公司中，梯队相对清晰，Weights & Biases 有较大的领先优势。**

**• Vertex AI / SageMaker vs. Weights & Biases**

Google Vertex AI 与 AWS SageMaker 仍是用户在选择机器学习工具时绕不开的两大平台。在模型试验管理环节，选择 Google Vertex AI 的人更多。Google Vertex AI 的优势在于集成了市场上的其他产品，用户切换工具方便。此外，由于 enterprise 客户有安全审查要求，如果产品都在同一个平台只需审查一次，若使用其他平台的产品则需要再审查一次，如果一个产品的独特性不显著，用户将为了方便使用大平台提供的工具。

**• 模型实验管理 vs. 模型监控**

**模型试验管理聚焦于模型训练阶段，模型监控则聚焦于模型上线后的监控，两者是上下游关系。**不过，两者只是所处的环节和阶段不同，但都是对模型和资源进行监控，因此产品形态差异不大。此外，两个环节的市场总盘子都不足够大，**长期来看，两个环节的供应商大概率要切入对方的领域，因此，Arise、Arthur 等模型管理公司长期来看也是 Weights & Biases 的竞争对手。**

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/018.png)

**05.**

**成功要素与风险**

**成功要素**

**1. 重要赛道 & 重要位置**

AI/ML 在未来 10 年的重要性无须反复提及，我们希望挖掘出 AI infra 链条上所有重要环节、重要位置，而 Weights & Biases 所在的模型实验管理是我们认为相对重要的一个环节。**当 Apps 数量变多，我们需要 APM（Application Performance Management）工具，我们需要 Datadog；当 data 数量变多，我们需要 Data Observability 工具，我们需要 Grafana；如果我们假设未来模型变得很重要或模型数量变多，那么我们一定会需要模型实验管理、模型监控工具，最终跑出来的可能是 Weights & Biases。**

**2. 产品价值显著，易用性好，受用户喜爱**

**模型实验管理在 AI/ML 工作中价值体现较明显，如果没有 Weights & Biases，工作会变得混乱，尤其是团队间协作，模型在哪、训练进度如何、结果怎么样、结果是如何得到的、资源调用情况如何等等，都需要依靠 Weights & Biases 来追踪和查看。**Weights & Biases 提供了较高的价值。除此之外，Weights & Biases 的产品易用性和用户体验做得很好，深受用户喜爱，口口相传，NPS 为 9-10 分。有用户表示，没有用 Weights & Biases 的人只可能是没听说过此类产品的人，如果用户知道有这样一款产品存在，一定会瞬间爱上它。

**3. 客户质量高，增长和留存数据乐观**

**Weights & Biases ARR 在几千万美金量级，ARR 去年同比增长 150%，增长迅速，NDR 也超过 150%，商业化表现佳。**NDR 高是因为有数据沉淀，模型实验管理工具就像用户的笔记本，知识和项目情况沉淀在笔记本中，如果笔记本页数无限大，用户将没有动力更换笔记本。

Weights & Biases 客户包括 OpenAI、DeepMind、Facebook AI Research、Midjourney、Stability、Nvidia、Microsoft、Lyft 等等，许多客户为大模型或 Generative AI 公司。**大模型对算力需求大、成本高，Weights & Biases 能够为大模型及大模型之上的应用层企业可视化资源的使用情况，充分享受到大模型与 Generative AI 的红利。**

**4. 团队 Marketing 能力强、执行力强**

**Weights & Biases 在品牌塑造、PR、marketing 方面非常强，**文章、播客、社区、研讨会等应有尽有，还发布了类似 Kaggle 的榜单。Weights & Biases CEO 与核心团队也非常活跃，出现在各大论坛和会议，包括业界的活动与高校的活动。有用户表示：“他们可能是我见过最高调的供应商”。

**强大的品牌与市场营销能力对于实验管理工具赛道而言十分重要，**因为即使产品与产品之间在交互设计、用户体验等方面有一定差距，但单从价值来看，每款产品提供的价值差异并不大。再加上模型实验管理工具就像笔记本，用户更换的动力不大。因此更早地触达用户、更快获取更多用户很关键。模型实验管理赛道是占坑逻辑，早期占的坑越多，留给对手的机会就越少，因此有很强的 marketing 能力对于 Weights & Biases 而言是一个极大的优势。

此外，Weights & Biases 团队的执行力很强，他们能及时根据用户反馈调整产品，并在用户提出问题和需求时快速响应，使得用户体验很好，产品迭代速度也很快。许多用户表示，早期决定与 Weights & Biases 合作很大程度是因为 **Weights & Biases 团队永远给人一种“极度渴望合作且十分靠谱”的感觉。**

**风险**

**1. 天花板不够高**

从目前测算结果来看，2027 年 Weights & Biases 所在的赛道潜在市场空间仅为 43 亿美元，规模较小。并且，Weights & Biases 占企业预算并不高，根据调研结果，5 人 ML 团队每年在 Weights & Biases 花费 5-10 万美金，10 人 ML 团队每年花费 15-20 万美金。

另一方面，由于 Weights & Biases 主要针对个人或团队用户，而非 enterprise 客户，Weights & Biases 提供企业级解决方案的能力较弱，产品中也缺少企业级 feature。早期针对 C 端或 SMB 客户起量较快，但后期如果无法突破此边界拿到 enterprise 客户的订单，则有可能很快遇到天花板。

**不过大模型这波趋势起来之后，该情况有所好转，大模型训练的复杂程度以及对资源的消耗程度，都使模型实验管理和监控变得更加重要，Weights & Biases 也成功拿下了多家大模型公司和 Generative AI 企业的订单。**长期看，更大的需求不在训练端，而在推理端，如果 Weights & Biases 能成功切入模型上线后的模型监控环节，天花板将有质的提升。

**2. 刚需程度不足，迁移成本低**

尽管模型实验管理工具有数据沉淀，用户没有更换其他解决方案的动力，**但假设 Weights & Biases 明天就消失，用户表示不会对业务产生任何影响，这是因为 Weights & Biases 目前切入的领域主要在离线环境，而非与业务紧密结合的在线环境。这也表明了 Weights & Biases 价值虽显著，但刚需程度不足。**

有位用户用了个比喻解释该问题，Weights & Biases 只是个笔记本，它记录项目情况，但不存储用于模型训练的数据，它不是课本，也不是考试中的答卷，如果笔记本弄丢了，再买一本新的，并根据记忆和现有的模型把此前的笔记补上就行，不会产生太大影响。此外，假设用户想要更换供应商，只需要 3-5 天就能迁移完成，迁移成本不高，企业若自建一套系统，也只需要 3-4 个月时间。

**06.**

**结论**

**Upside：Datadog for AI/ML？**

除此之外，我们认为 Weights & Biases 团队能力较强，但不够 visionary，不够坚定。

正如成功要素部分所说，当 Apps 数量变多，我们需要 Datadog；当 data 数量变多，我们需要 Grafana；如果我们假设未来模型变得很重要或模型数量变多，那么我们一定会需要模型监测、模型管理工具。竞争部分也提到，模型监测与模型管理两个环节的供应商未来大概率会互切，进入对方的领域，两个环节未来将由相同的供应商负责。因此，**Weights & Biases 的 upside 的假设是，Weights & Biases 成功从模型实验管理切入到模型监控环节，甚至切入工作流的更多环节，或像 Datadog 一样成功扩大了产品数量。**

**Downside：被收购**

**Weights & Biases 在 AI infra 卡位较好，价值显著，产品易用性好，深受用户喜爱。**Weights & Biases 对用户而言有很大的价值在于方便协作、提升模型训练效率、可视化资源使用情况等等，对 AI/ML 的 adoption 速度提升有很大帮助，利好上游的硬件厂商和云平台，**对于上游厂商而言，Weights & Biases 是好的并购标的，Nvidia 也于 2022 年 5 月对 Weights & Biases 进行了战略投资。因此我们对 Weights & Biases 的 downside 并不担心。**

**当前判断**

**基于当前情况，我们的判断是 Weights & Biases 今年 2023 年 ARR 超过 1 亿美金，2027 年预计在模型试验管理 43 亿美金的市场中占据 10% 的市场份额，即 2027 年 ARR ~ 4.3 亿美金（仅指模型实验管理环节，不包括模型监控环节）。长期看，Weights & Biases 要做到 10 亿美金 ARR 应该还需要 8-10 年，同时也不排除有被收购的可能性。****一句话总结，短期将保持高速增长，长期有挑战。**

**判断依据如下：**

**1. 短期受大模型军备竞赛红利影响，保持高速增长。**

大模型训练的复杂程度和资源消耗程度使大模型企业对模型实验管理工具的需求激增，作为模型实验管理赛道的 top 1，Weights & Biases 是大模型生态企业的首选。并且借着大模型的东风，Weights & Biases 开始切入 enterprise 客户，客户群体由原来的个人或团体客户扩展至 enterprise 客户。因此我们认为 Weights & Biases 短期内将保持高速增长。

**2. 长期来看，由于 Weights & Biases 当前所切的市场空间有限，在大模型军备竞赛红利过去后，增长会面临一定挑战。**

即使 Weights & Biases 借着大模型打开了 enterprise 市场，但模型实验管理本身聚焦在训练侧，而参与模型训练的面向的只有少数顶级的研究员和工程师，即使在 enterprise 企业也是如此，也就是说 Weights & Biases 看似打开了 enterprise 市场，但客群与此前的主要用户如高校研究员、个人用户等等差异不大，有一定量的提升，但不是质的提升。且顶级研究员的数量不会快速扩张，模型实验管理的市场空间相对较小，因此 Weights & Biases 长期发展依然有挑战。

**3. 如果想在长期有所突破，切入下游的模型监控环节是必要的选择。**

就像上文所说的模型上线后、在实际生产环境中监控模型是更大的市场和机会。更理想的情况是切入更多的工作流环节。我们认为 Weights & Biases 切入模型监控环节成功的概率不小，因为目前该环节玩家不具备超强的竞争力，Weights & Biases 切入相对容易，但也要看团队的野心和意愿。

此外，**APM 公司是在 app 生态非常成熟之后才跑出来，Data Observability 工具也是在 data stack 相对完善、data 生态非常繁荣之后需求量才大增，而 AI/ML 行业才刚刚起步，尤其是大模型，因此我们判断现在是模型实验管理需求爆发的时点，而距离模型监控需求爆发的时点仍有 5-8 年。**并且横向切入其他环节，扩产品线，并非容易之事，Datadog 靠此策略取得成功，但大多数公司都无法突破舒适区。

4. 我们认为 Weights & Biases 有可能被收购的原因是：1/ Weights & Biases 产品价值显著，但产品相对较薄；2/ 对上游硬件和云厂商有战略协同意义；3/ 团队能力较强，但不够 visionary、不够 aggressive。

**07.**

**融资历史**

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/019.png)

**08.**

**访谈纪要**

**1. Customer A**

我们核心的 ML 团队、完全专注于机器学习的目前不到 10 人。机器学习过程中的两大挑战是：1/ 如何以可扩展的方式有效、快速、轻松地部署模型；2/ 模型注册表，包括模型版本管理、模型全生命周期监控等等。在我看来，Weights & Biases 在做的实验追踪很大价值在于员工之间的知识共享，避免一些重复性工作。W&B 目前在支付方面有些问题。我之前在另一家公司工作的时候，试图让 Weights & Biases 成为我们的供应商，但我们不能使用 cloud 版本，只能 on-prem 部署，而 on-prem 版本的定价远高于 cloud 版本，因此我们最终没有选择采购 Weights & Biases。

**2. Customer B**

Weights & Biases 与 Comet 的区别在于，Weights & Biases 更倾向于面向学术界进行销售，客户多为研究人员，而 Comet 则更多与初创企业或大公司接触，面向金融或传统农业领域。这从他们举办的研讨会主题也能看出来，Weights & Biases 通常会深入讨论技术、学术性话题，包括 AI/ML 方向的最新研究成果等等，而能够欣赏这些东西的通常是学术界研究员或行业内实验室的研究员。

**3. Customer C**

我们做深度学习，需要对与训练这些模型相关的所有指标进行监测，很多东西需要追踪和查看，Weights & Biases 是一个非常详细的深度学习日志系统，在使用 Weights & Biases 之前，人们只能将模型日志保存在电子表格或其他文档中。有了 Weights & Biases，你可以将日志插入代码中，且透明度大大提高，它记录了你在训练模型过程中发生的每一件事，而不是一个独立的、不一定有意义的电子表格或文件。

我们在使用 Weights & Biases 前，也评估了 Comet，但我们发现 Weights & Biases 团队的响应速度更快，他们看起来更愿意与我们合作，更愿意为我们提供额外的支持。所以我们选择了 Weights & Biases。

实际上，Weights & Biases 的核心产品比 Comet 要好得多，使用 Weights & Biases 是非常容易的，直接、容易理解。假设我们有 5 个人在研究同一个模型，如果没有 Weights & Biases 将是非常困难的，你的团队会陷入混乱。我们是 20 人的团队，每年在 Weights & Biases 花费 20 万美金。但如果 Weights & Biases 提价 3 倍我们依然会买，如果没有 Weights & Biases 我们的工作将会受到影响。我认为任何做深度学习的人，如果他们没有使用 Weights & Biases，唯一可能的原因是他们不知道这个工具的存在。

**4. Customer D**

我认为 MLOps 的最大价值在上游，尤其是数据部分，如何为你的模型获取训练数据，我认为这可能是最有价值的地方。Weights & Biases 虽然也是其中一个关键环节，但它们所覆盖的价值范围更窄，客单价我猜是 5 万美元以下。相比之下，我们现在在 AWS 上的花费大约是每年 2,500 万美元，在 Scale 的花费也有每年 200-250 万美元。

**5. Customer E**

对我来说，Weights & Biases 就像一个虚拟的笔记本，数据科学家们以前都有一个笔记本或电子表格，用于追踪所有的实验，但现在有了 Weights & Biases，Weights & Biases 就是一个非常好的数据科学家协作平台。但由于数据安全，我们不希望我们的信息和数据被 Weights & Biases 吸收，因此到了规矩较严格的新公司后，我就没有再用 Weights & Biases。

当你想用模型来解决业务问题时，可以进行一些实验，类似原型设计，Weights & Biases 主要切入的环节为训练阶段的模型实验管理。如果我们把模型带入生产环境，模型同样需要被监控，这个环节有其他玩家，但我认为 Weights & Biases 也想进入这个市场。Weights & Biases 有很好的品牌识别度，被大家看作是一个很酷的品牌，他们确实在社区运营方面投入较大。如果满分 10 分，我会给 Weights & Biases 打 8 分，它是一个非常好的产品，也是一个非常简单的产品。

**6. Customer F**

我们尝试过 Databricks 的 MLflow，它也有模型实验管理工具，且是免费提供，Azure ML 也有一个模型追踪系统，但我们仍然需要 Weights & Biases，因为他们的功能差距非常大。Weights & Biases 可以横向整合，切入越来越多的工作流，类似 Databricks 的做法。他们起步很好，在模型追踪、可观测性、日志等方面都比其他人做得好，这是一个相当坚实的基础。我在使用过程中遇到问题、提出问题，他们对反馈意见的接受度很高，且每次都会帮我解决这些问题。

Weights & Biases 有一个社区，里面有大量的思维碰撞，有播客、教程、论坛等等，这些内容没有在宣传 Weights & Biases，仅限于学术讨论，但实际上为 Weights & Biases 塑造了很好的品牌形象。

**7. Customer G**

我们公司有 250 名 AI 或数据科学家，使用 Weights & Biases 的有 15-20 人，主要集中在模型和算法团队。很难将 Weights & Biases 与其他工具进行比较，每个工具都在一个特定的领域很突出，重点不同。如果满分 10 分，我会给 Weights & Biases 打 9 分。

**8. Customer H**

我们用 Weights & Biases 主要是因为方便，如果没有 Weights & Biases，我们也能自己写一套工具，大概需要 4 个月时间。但问题在于，我们自己写的产品使用体验可能没有那么好，可能无法吸引其他团队使用，进而没有达到协作的效果。我认为 Weights & Biases 没有直接的竞争对手。就目前而言，Weights & Biases 处在一个有利的位置，因为他们已经在这方面投入了很多时间，作为一个工具，Weights & Biases 显然领先于其他竞争对手。

**9. Customer I**

我在机器视觉团队，整个部门有 15 个人。我们的实验追踪主要依靠 AWS 和 Weights & Biases，AWS 用于共享文档，用于协作，而 Weights & Biases 用于比较模型。我们是 Weights & Biases 的早期使用者，我们整个部门都在处理大量的数据，这是我们工作中最耗时的部分之一，另一个耗时的事情是寻找模型中的问题，以及调试模型。因此我认为拥有一个可以大大减少此类工作时间的工具是非常重要的。

**10. Customer J**

我们公司的数据科学与机器学习团队有 12 人，4 人负责 infra，4 人负责数据质量，3 人负责研发。过去一年，我一直试图说服老板使用 Weights & Biases 或 Neptune。Weights & Biases 现在是一家 branding 很好的公司，我过去经常使用它，认为它是最好的，我喜欢它的许多功能，但我认为它的定价已经相当高了，在我们公司所处的阶段，可能需要更便宜的产品。

此外，Weights & Biases 很多功能对我们来说不是特别有用，我想也许 Neptune 会更适合我们。我们希望 Weights & Biases 有一个定价选项，可以自己选择想要的功能和产品，而不是按一整个 package 卖。我想，我现在会建议公司用一个开源软件，或采购 Neptune，因为它很便宜。

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/020.png)

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/021.png)

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/022.png)

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/023.png)

延伸阅读

[![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/024.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247500575&idx=1&sn=5c113c85a79cc8bc58d15fb2d4ace921&chksm=ce9b7c81f9ecf597d9041598d4637b4fbfcfa1e90f7e32e6d59c8c0d1bc00417e91b5a3d478f&scene=21#wechat_redirect)

拾象云安全投资图谱：Wiz最快达到1亿美元ARR的来龙去脉

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/025.png)

[![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/026.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247500097&idx=1&sn=fc9f6e843e83a73b656dac06a7c8def9&chksm=ce9b7edff9ecf7c965e38f3bd3b4f827f5c813e6bccd70ec85ebd6227d0679e83cc99efa794c&scene=21#wechat_redirect)

Webflow：40亿美金估值的无代码建站SaaS，能否跨越下个技术周期？

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/027.png)

[![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/028.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247499707&idx=1&sn=35e5225593b44f2eefeb0e43ba56405f&chksm=ce9b4025f9ecc9338ab35d290bd72066a99281ac0b9870c6d51799c2e478d8a6b9e30842e9d6&scene=21#wechat_redirect)

Rippling：HR领域的Salesforce，将分裂的HCM再度平台化

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/029.png)

[![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/030.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247499819&idx=1&sn=f3cf42a225d459dcc861d338ccb15abe&chksm=ce9b7fb5f9ecf6a3b668e8700ec3d0894bd9c6faff41aa4e5ba369afafe3d701765a0b8c8739&scene=21#wechat_redirect)

Retool：重塑现代企业的1/3，为SaaS装上乐高底座

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/031.png)

[![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/032.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247499602&idx=1&sn=43da7f386a31e9990702c38514c28bf4&chksm=ce9b40ccf9ecc9dac7ef54c7afb31509eea25c06afecab4093acc3bc5df48c7565cd25513ac7&scene=21#wechat_redirect)

Universal API：第三方集成的高速公路，SaaS割裂现状的破局之道

![](../images/2023-03-03-weight-biases-da-mo-xing-jun-bei-jing-sai-de-shou-yi-zhe-yu/033.png)
