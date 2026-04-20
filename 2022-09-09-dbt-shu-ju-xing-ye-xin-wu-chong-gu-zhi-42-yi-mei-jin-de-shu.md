---
title: dbt：数据行业新物种，估值 42 亿美金的数据转换工具
publish_date: '2022-09-09'
publish_timestamp: 1662721200
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/Bj-b7XHRvR8X-3dyEmEBcg
msgid: 1000000121
appmsgid: 2247496196
itemidx: 1
digest: 世界重新关注 SQL 作为数据行业核心语言的重要地位。
cover: https://mmbiz.qpic.cn/mmbiz_jpg/3tHNibnJ2jgyXsa4gduagCTyicxt3ul3yeBCWvUVfamEicYTRiaDqcicsXfI5hmBgr0PZ79DfCiawtK9L0FMhMJWkk1A/0?wx_fmt=jpeg
image_count: 20
archived_at: '2026-04-19T23:29:43+08:00'
---

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/001.gif)

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/002.png)

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/003.png)

**作者：Kefei**

**编辑：Penny**

**排版：Elena**

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/004.png)

**随着以 Snowflake 为代表的云数据仓库的崛起，世界重新关注 SQL 作为数据行业核心语言的关键地位**，以 SQL 为核心的数据工具重新受到重视，dbt 就是其中之一。

**dbt 是数据转换工具，核心功能是把用户的代码编译为可以在数据仓库执行的 SQL 语言，帮助用户在数据仓库中转换数据**。在此之前，数据转换需要通过其他更加复杂的语言才能实现，而大部分数据分析师只掌握 SQL，他们必须依靠数据工程师来完成数据转换工作。随着 dbt 及一系列基于 SQL 开发的数据处理工具的出现，数据分析师可以独立完成从数据处理到数据分析的全流程工作。

**dbt 是新一代 Data Stack 的重要组成部分，常与 Snowflake、Fivetran、Looker 等产品结合使用。dbt 产品简单易用，且拥有一个充满活力的社区，具备优秀开源产品所具备的两大特性。此外，dbt 没有直接竞争对手，是其所在领域唯一的主流解决方案。**

dbt 是数据行业新类别的定义者，推动了一个新兴职位的出现——分析工程师（Analytics Engineer）。**2021 年，要求掌握 dbt 应用的分析工程师岗位数量较 2020 年增长了 3 倍。目前 dbt Community Slack 用户已超过 25,000 人，共有 9,000 家企业的员工使用了 dbt Core（开源版本），付费企业 1,800 家，付费用户在过去一年增长了 2 倍，ARR 增长了 6 倍。这些都足以证明 dbt 的价值和影响力**。

然而，从投资和企业发展角度看，dbt 仍存在一些问题：天花板较低；商业化产品尚未实现 Product/Market Fit。天花板较低主要受 dbt 客单价影响，dbt 与 Snowflake 客群高度重合，但客单价仅为 Snowflake 的大约 1/30。我们认为，dbt 若想提高天花板，可以尝试调整定价模型以及扩展产品矩阵，同时也要加强团队的商业化能力。

**毋庸置疑，dbt 是现代 Data Stack 中一个独特的存在，具有较高的价值，并且人们是真心喜欢它。我们认为 dbt 是一家值得持续关注的公司。**

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 dbt 解决什么问题？

02 从 ETL 到 ELT

03 dbt 业务与成长性

04 dbt 为什么值得我们关注？

05 结论与建议

**01.**

**dbt 解决什么问题？**

企业中的数据从多方而来，常见的数据源包括数据库、文档、表格、Web 等。**由于数据来源分散、数据质量参差以及指标定义和业务属性不一致，在有效利用数据之前，需要对数据进行 ETL（Extract, Transform, Load）/ELT，使数据从原始状态达到可使用状态，以便用于分析、可视化、建模等等。dbt 解决的就是 ETL/ELT 里 “T” 的问题，即数据转换**。

**数据转换是指将数据从一种格式/结构转换为另一种格式/结构的过程，是 ETL/ELT 中最重要的环节**。数据转换过程包含以下几个步骤：

- **清理数据**：解决数据缺失和数据不一致的问题
- **规范数据**：将数据格式化
- **删除重复数据**：删除冗余的数据
- **检验**：系统报告低质量数据、异常数据
- **排序**：将数据分类排序

**在企业里，这些工作通常由数据工程师（Data Engineer）来完成，当数据达到可使用状态后，数据分析师（Data Analyst）可以开始对数据进行分析，获得有价值的洞见。**

通常情况下，1 位数据工程师所能处理的数据量可支撑 2-3 位数据分析师的分析需求，然而，数据工程师与数据分析师的数量相差悬殊，在实际工作中，数据分析师的需求很难被完全满足。即使可以被满足，为每 2-3 位数据分析师配备 1 位数据工程师也不合理。

此外，数据工程师与数据分析师独立作业，两边的信息是孤立的，带来较大的沟通成本，影响工作效率。数据工程师对业务的理解不如数据分析师透彻，数据分析师不熟悉各类数据集的细微差别，并且，由于对指标的定义和计算方法有所不同，分析师经常重写同事已经写过的语句，导致组织决策速度降低，决策质量下降。

**因此，ETL/ELT 工作由数据工程师来完成并不是最佳选择，最佳方案是，让数据分析师自己完成 ETL/ELT 的工作。**

但在现有的工具下，数据分析师无法独立完成 ETL/ELT 工作，因为 ETL/ELT 需要复杂的编程语言，而大部分数据分析师仅掌握 SQL语言。因此，若想让数据分析师自主完成 ETL/ELT 只有两种方法，第一是数据分析师都去学习复杂编程语言，这显然不现实；第二种方法是，让 ETL/ELT 能够在 SQL 语言下完成，**这就是 dbt 在做的事**。

**dbt 是一个帮助数据分析师完成数据转换的工具。有了 dbt 之后，数据分析师可以通过编写 SQL 语句、低门槛转换数据，不再需要依赖数据工程师，独立解决数据转换问题**。ETL/ELT 中的“E”和“L”也已经实现“SQL 化”，“E”和“L”部分由 Fivetran、Airbyte 等公司来完成，这里不过多阐述。

**02.**

**从 ETL 到 ELT**

**作为数据转换工具，dbt 的核心功能是把用户的代码编译为可以在数据仓库执行的 SQL 语言，帮助用户在数据仓库中转换数据。dbt 是新一代 Data Stack 的重要组成部分，常与 Snowflake、Fivetran、Looker 等产品结合使用。**

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/005.png)

- **云数据仓库成为数据分析领域的中心平台，数据处理方式由 ETL 变成 ELT**

传统数据处理方式是“ETL”，即提取数据后，先完成数据转换，再将转换好的数据加载到数据仓库中，**但随着 Snowflake、Redshift、BigQuery 等云数据仓库重要性不断增强，他们逐渐成为数据分析领域的中心平台，新一代 Data Stack 出现，衍生出围绕数据仓库操作和处理数据的需求，即数据首先进入数仓，再进行数据转换，数据处理方式由 ETL 向 ELT 转变**。

在 ELT 中，首先使用 Fivetran 等工具，从数据源提取数据，加载到云数据仓库，然后再用 dbt 将数据转换为分析所需要的格式。ELT 比传统的 ETL 更灵活、更简便。

此外，由于云数据仓库将计算和存储分离，以及数据仓库的性能和可扩展性不断增强，围绕数据仓库处理数据成为可能。**dbt 的兴起很大程度受益于云数据仓库的繁荣，甚至可以说 dbt 是云数据仓库生态企业**。

- **Snowflake 等云数据仓库的崛起让世界重新重视 SQL 的核心地位**

SQL 是数据库的“母语”。然而，自 Hadoop 出现以来，人们将工作负载从数据仓库转移到新奇的数据湖中，2010 年开源的 Spark 成为数据湖的标准语言。**Hadoop 和 Spark 的成功吸引了许多关注，但值得注意的是，即使在 Hadoop 的全盛时期，大部分数据转换工作依然是通过 HiveQL 来完成，而 HiveQL 是 SQL 的“衍生品”。**

**近几年，随着以 Snowflake 为代表的、以 SQL 为核心的云数据仓库的崛起，世界重新重视 SQL 作为数据行业核心语言的地位。**

此外，数据行业的一大痛点是，不是每位潜在数据消费者都能独立为自己服务，使用门槛限制了数据工具的推广和商业化前景。由于 SQL 的使用门槛较低，人们在尝试使用其他语言后，重新回归 SQL 使用者的行列，长期来看，使用 SQL 的人的数量也远远大于使用其他语言的人的数量。**因此，以 SQL 为核心意味着更多的人可以独立消费和使用数据，意味着更大的市场空间**。

**03.**

**dbt 业务与成长性**

**dbt 由两个基本组件组成：编译器和运行器**。用户在文本编辑器中编写 dbt 代码，从命令行调用 dbt。dbt 将所有代码编译成 SQL，并针对配置的数据仓库执行这些代码。

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/006.png)

**不过，dbt 的目标不仅限于成为一个 SQL 转换库，而是希望能够为用户提供强大的工具来构建和共享转换模型及成果**。因此，dbt 设置了包管理器，包管理器类似一个共享平台，用户可以在管理器内发布 dbt 代码存储库，其他人可以直接引用存储库里的内容。dbt 将数据分析师从工具使用者变成工具开发者。

根据用户访谈，除了基本功能“数据转换”外，包管理器也深受用户喜爱。一位来自 GitLab 的数据分析师谈到：**“通过使用 dbt，一旦定义了一个数据转换过程，代码就将存储在 dbt 内部，你可以在此基础上随时进行修改和迭代。dbt 还支持同行评审机制。”**

另一位数据分析师也表示**：****“使用 dbt 的时，感觉自己就像软件工程师一样，用自己喜欢的语言写代码，并且可以把它们上传到 GitHub 上，你会得到同行的点评和反馈，并且可以直接在上面操作和修改。我们现在还没有看到这个工具有什么大的缺点，一旦我们或别人建立了一个模型或管道，我们可以重复使用，极大程度避免了重复工作。它提供了一个定义标准的工具，每个人都可以重复使用这些标准。”**

除此之外，dbt 还提供数据模型、数据测试、数据文档等功能。

- **数据模型：是指将数据模块化存储**。一方面方便用户清晰表达项目结构，让团队更好地理解用户所做的工作；另一方面数据以模块化的方式存储，方便日后调试自己或别人写的代码和模型。

- **数据测试：是指帮助团队检测数据，提高数据质量**。dbt 在以下四个阶段验证数据质量：源数据；构建模型；部署模型；浏览模型及代码。还可以测试源数据所在的位置。
- **数据文档**：如记录“ARR 是如何定义的”以及这些指标所依赖的源数据等等，帮助回答有关数据集的日常问题，让团队成员对数据的理解保持在同一层面，方便团队协作。

dbt 基于以下信念进行开发：

1. **代码是复杂分析逻辑的最佳表达形式；**
2. **数据分析师应该像软件开发者一样使用类似的工作方法和工具；**
3. **关键数据分析基础设施应该由其真正的用户来控制和使用；**
4. **分析代码本身——不仅仅是分析工具——将越来越多地开源。**

这些信念也构成了今天我们所看到的产品。

**dbt 的企业用户包括 Canva、GitLab、HubSpot 等，使用人群主要是数据工程师、数据分析师和数据科学家，事实上还有一类因 dbt 而产生的群体——分析工程师，我们稍后会对此进行介绍。**

从商业化层面看，dbt 分为个人版、团队版、企业版。其中，个人版永久免费，团队版的价格为每月 50 美元 per seat，企业版则基于企业每年所需要的席位以及其他附加的功能和服务进行个性化定价。

同时，dbt 也将 dbt Core 开源，想要在本地或企业内部 IT 架构上运行 dbt 的工程师可以自行部署。

在过去的 2021 年，dbt 达成了许多 milestones：

1. **社群**：dbt 在 Slack 的用户社区 dbt Community Slack 的用户已超过 25,000 人，在 8 个国家拥有 12 个 Meetup 团体。
2. **客户**：目前共有 9,000 家企业的员工使用了 dbt Core（开源版本），付费企业有 1,800 家，付费用户在过去一年增长了 2 倍，ARR 增长了 6 倍。
3. **合作伙伴**：2021 年，dbt 的战略合作伙伴数量增长 2 倍。
4. **新用例**：dbt Cloud API 当前可支持超过 25 个企业应用程序。
5. **团队**：团队从 2021 年初的 50 人扩大到 200 人，扩大了 4 倍。

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/007.png)

*Weekly Active dbt Projects*

各项指标都足以证明 dbt Core 已完成 Product/Market Fit 的验证，进入高速增长阶段。但从收入规模及用户反馈看，dbt 的付费产品离 PMF 或许还有一段距离。

**04.**

**dbt 为什么值得我们关注？**

**1. dbt 是数据行业新类别的定义者**

dbt 解决的实际上是数据分析师与数据工程师之间的 gap，即只会 SQL 的数据分析师无法自己完成数据工程工作，而数据工程师对业务的理解和洞察较弱。**dbt 的诞生使一类职能介于数据分析师与数据工程师之间的新兴群体出现——分析工程师（Analytics Engineer）**。

**分析工程师的工作就是用 SQL 语言独立构建数据管道和数据模型，完成原本只能由数据工程师或数据科学家来完成的数据准备工作。**

对于工具定义工作岗位，很多人会猜测究竟是真需求还是公司为了体现其价值而创造出来的伪需求。但通过在各大招聘网站爬取的数据显示，**仅 2021 年一年，要求掌握 dbt 应用的分析工程师的岗位数量就增长了 3 倍。我们认为这足以客观证明 dbt 的实际价值和影响力**。

**2. dbt 具备优秀开源公司所具备的特征**

**dbt 产品简单易用，交互友好，摩擦较小，能有效解决问题**。易用性一方面体现在用户能用 SQL 语言而不是其他复杂的语言实现数据转换，另一方面体现在产品设计、交互等方面。并且 dbt 教学视频丰富，用户可以很快学会并上手使用。

**除了极强的产品力外，dbt 拥有一个充满活力的社区，对于 bottom up 模式的开源产品而言，这是极其重要的。dbt 在 Slack 上的社区拥有超过 2.5 万活跃用户，他们分布在 8 个国家和地区，且参与度极高，社区成员的贡献和反馈让 dbt 产品变得越来越好。**

事实上，dbt 社区早期和其他开源社区一样，只是早期产品使用者交流和反馈的渠道。随着 HubSpot、Casper 等公司开始尝试使用 dbt，他们的员工开始加入 dbt 的 Slack 社区。**这给 dbt 社区带来两个好处，一是大公司使用产品的员工数量更多，当他们从这些公司离职后，将 dbt 带到更多的公司；另一方面，大公司员工素质相对更高，眼界更开阔，他们将话题从如何使用 dbt 延伸到关于现代 Data Stack 的讨论，将 dbt 社区变成有名的数据论坛，其中一些用户还主动组建了当地 dbt 团建小组，dbt 在硅谷、纽约、伦敦、悉尼等城市建立了具有影响力的社区**。

dbt 每年也会召开 Coalesce 会议，举办线上活动，不断吸引新的社区成员。除此之外，dbt 社区用户还自发在 Substack 或其他渠道分享关于 dbt 和分析工程的文章和播客，dbt 也推出一项将新用户带入社区的活动 dbt Learn，dbt Learn 也为现有用户提供专业的知识和服务。

强大的社区让 dbt 在融资前没有投入一分销售和营销费用，公司完全自然增长，这也足以看出 dbt 产品的优越以及用户的忠诚和喜爱。

**一款简单好用的产品和一个充满活力的社区，可以说，dbt 具备优秀开源产品所具备的两大特性。**

**3. 值得 bet 的创始人**

dbt 创始人 Tristan Handy 非常优秀。2013 年初，Tristan 加入 RJMetrics（后被 Magento 收购），担任营销 VP。2015 年，Tristan 在 RJ 领导了一个名叫 Stitch 的项目，Stitch 后来被分拆，作为一个独立业务运营。

2016 年，Tristan 从 RJ 辞职，创办 Fishtown Analytics。FA 起初是一家分析咨询公司，帮助初创企业进行业务分析。与此同时，FA 内部还在运营一个名为 dbt（data building tool，数据构建工具）的开源产品。由于 dbt 大受欢迎，很快变成了 Fishtown Analytics 的核心业务，**Fishtown Analytics 也于 2021 年 6 月正式更名为 dbt Labs。**

Tristan Handy 有写 blog 的习惯，经常通过文字分享自己对 dbt 以及数据行业的思考和洞见。Tristan 曾多次在 blog 上分享自己对现代 Data Stack 的发展趋势的看法，以及 dbt 的重要决策及决策背后的思考，包括 dbt 为什么不支持 Python，为什么设定如此低的价格，为什么不从 enterprise 客户切入等等。

Tristan 还不定期在 blog 复盘 dbt 的发展情况，并制定未来发展计划。通过高管访谈，我们了解到 Tristan 每个阶段都会为 dbt 设定明确的目标，并且几乎都能实现，我们认为这非常了不起。

**同时，Tristan 非常 ambitious，对自己的人生以及 dbt 的未来有很高的要求和期待。熟悉 Tristan 的投资人和公司高管表示，Tristan 似乎每一秒钟都在思考如何将 dbt 变成一家伟大的公司，包括吃饭、走路以及陪伴家人旅行的时候。**

Tristan 在 dbt 完成 C 轮融资后也谈到：“我在想如何在这个星球上度过我的时间？我的墓碑上可以写些什么？如果我对这些问题中的任何一个的回答是‘赚很多钱’，那么你可能正在阅读一篇关于 Fishtown Analytics 是如何被高价收购的文章。但我真的无法想象做出这样的决定。此次融资的原因与 dbt 未被收购的原因相同，那就是——保持独立。”

**对于 dbt 未来会成为一家什么样的公司，Tristan 表示：“*****I want to create a smithy（铁匠铺）.*****” 当用户想要任何数据处理工具，都可以在 dbt 找到，即买即用**。显然，Tristan 所畅想的 dbt 的未来远不止我们今天所看到的一个小工具这么简单。

**4. 良好的竞争环境，绝对的竞争优势**

除 dbt 外，市场上的 ELT 工具还包括 Airflow、Fivetran、AWS Glue、Dataform、Matillion、Panoply 等等。**但事实上，如果我们聚焦到数据转换，dbt 可以说是没有直接的竞争对手，是客户的第一（唯一）选择**。

**不过，有两类公司未来有可能成为 dbt 的竞争对手，第一类是 Fivetran、Airbyte 等公司，它们负责 ELT 里的 “E” 和 “L”，未来有较大可能介入“T”，把 ELT 全流程都覆盖。第二类潜在竞对是 Snowflake、Databricks 和三大云厂商的数据仓库平台。**

**市场对 dbt 的需求很大程度基于数据仓库的繁荣，把 dbt 称作数据仓库生态企业一点也不过分，既然如此，数据仓库平台也可以开发自己的 ELT 工具以取代外部工具，或选择与其他 ELT 公司合作**。这些都是 dbt 未来可能面临的竞争和挑战，但就目前来看，并没有任何能对 dbt 构成威胁的数据转换工具，竞争环境相对良好，dbt 也具备绝对的竞争优势。

**05.**

**结论与建议**

**dbt 增长驱动因素包括：云数据仓库的成熟，SaaS 和数据生态的繁荣以及多云并进所需的数据转换和迁移**。其中，云数据仓库的成熟是最关键因素，Fivetran + dbt + Snowflake 是目前最常见的组合，dbt 也可以说是 Snowflake 生态企业。既然是 Snowflake 生态企业，timing 便不是核心问题，生态已相对 ready，Snowflake 生态也是未来 5-10 年 data infra 最好的生态之一。

**关键问题在于市场大小和产品刚需程度**。根据用户访谈，我们了解到 dbt 的主要用户与 Snowflake 的客户基本一致，但由于 dbt 提供免费的开源版本，付费用户数量远远小于 Snowflake。并且我们的一大 concern 是，dbt 付费用户 ARPU 值较低，且目前没有看到增长的可能性，这也与 dbt 定价过低、不太科学的定价模型有一定关系。多位用户提到，他们平均每年在 dbt 的支出大约为 1 万美元，部分用户则只有几千美元的年支出，几乎是整个 Data Stack 的最低支出水平，而这些用户每年在 Snowflake 的支出都高达到 10-60 万美金。

除此之外，dbt 并非刚需产品。当用户被问到“如果削减预算，你会先放弃 Data Stack 中的哪款产品”的时候，dbt 通常被排在前面或中间，而 Snowflake 则排在最后。

由此我们可以通过与云数据仓库市场规模进行对比，算出 dbt 潜在收入规模，以及 dbt 未来市场价值。根据 Maximize Market Research，2021 年全球云数据仓库市场规模约为 260 亿美元，预计到 2027 年达到 478 亿美元。根据 dbt 与 Snowflake ARPU 值的倍数关系（约 30 倍），即使 dbt 是该领域唯一的 player，成长空间依然有限。

出于市场对 Snowflake 生态预期的看好，dbt 估值/市值或可享受较高溢价，因此我们也可以和 Snowflake 市值进行对比。Snowflake 上市后，市值最高突破千亿美金，市场回调时市值也有 400 多亿美金。由于 dbt 和 Snowflake 的客群高度相似，客单价相差大约 30 倍，倘若在当前条件下预测 dbt 未来市值，保守估计只有 30-50 亿美金。考虑到 dbt 的刚需程度与 Snowflake 不同，实际付费客户也比 Snowflake 要少得多，因此还需在 30-50 亿美金的基础上打些折扣。然而，dbt D 轮估值已达到 42 亿美元，我们认为该估值与其实际价值相比并不便宜。

**不过，无论是 dbt 还是云数据仓库，渗透率依然很低，增长并未停止，几十亿美金的规模未必就是上限。且 dbt 除了在 Snowflake 被广泛应用之外，目前有向其他云数据仓库（RedShift, BigQuery…）以及DataLake/LakeHouse（Databricks）渗透的趋势。并且从产品和团队来看，dbt 确实拥有一款 killer 级产品，目前来看没有直接竞争对手。**

**综合来看，无论是市场成熟度还是产品和团队的优越性，dbt 都是现阶段比较稳妥的投资，但由于市场较小，且依附于云数据仓库生态，目前来看没有成为平台的可能性，因此只能算是一个稳稳的 6 分标的，不是一个 9-10 分标的**。dbt 和云数据仓库正处于高速增长阶段，从增量和市场预期来看，依然有较大的投资价值，但需要同时关注 Snowflake 等云数据仓库生态的增长情况。dbt 未来能成为多大的公司，很大程度取决于云数仓生态的成长性。

**dbt 若想扩大收入规模，提升天花板，我们认为可以从以下三个方面进行尝试**：

1. **尽快完成商业化产品的 Product/Market Fit 验证，加强团队商业化能力。**
2. **调整定价模型**。dbt 目前采用 per seat 的定价模式，这在一定程度上限制了 dbt 的未来收入规模。由于数据量的增长远快于使用数据的人的增长，因此从长远来看，data infra 产品采用 usage-based pricing model 或许是更好的选择。
3. **在完成商业化产品的 Product/Market Fit 验证后，可考虑切入 ELT 的其他两个环节，即 “E” 和 “L” 环节。未来还可根据产品的关联性，逐渐切入云数据仓库生态的其他领域。**

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/008.png)

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/009.png)

**Reference**

https://www.getdbt.com/blog/next-layer-of-the-modern-data-stack/

https://www.youtube.com/watch?v=3Fb\_o7NuERQ

https://podcasts.apple.com/ve/podcast/tristan-handy-the-work-behind-the-data-work/id1504567418?i=1000565843110

https://www.youtube.com/watch?v=rP-b5s\_72l8

https://www.getdbt.com/blog/what-are-the-steps-tools-in-setting-up-a-modern-saas-based-bi-infrastructure/

https://www.youtube.com/watch?v=1Zj8gTLdf5s

https://www.getdbt.com/blog/what-exactly-is-dbt/

https://www.getdbt.com/blog/pricing-vision-fit/

https://www.getdbt.com/blog/future-of-the-modern-data-stack/

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/010.png)

延伸阅读

[![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/011.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247492893&idx=1&sn=c13a9db1932ab01ce38ef582ecc08eb0&chksm=ce9b5a83f9ecd395e8652f9fa79234050734c46a2f9761ee86117c08b67a1f6f3820b60f7494&scene=21#wechat_redirect)

Cohesity：企业数据备份领域的 iPhone，用“超融合”唤醒沉睡数据

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/012.png)

[![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/013.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485500&idx=1&sn=a81b7c5c3d2c277015b82bd08650e4fe&chksm=ce98b7a2f9ef3eb49a1fbcd4e18f3b36ddba140f32afd996b17e5cc0ab2abb17d662fc358cb2&scene=21#wechat_redirect)

HashiCorp：企业上云的桥梁，云计算领域的Shopify

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/014.png)

[![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/015.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247488600&idx=1&sn=c909b3fbad3b129452f40c3975fe4b4f&chksm=ce98abc6f9ef22d0989fe304822b0da1cda08ff31e6507775ddb2c48e194c1767dc6bdc92901&scene=21#wechat_redirect)

Fivetran：云计算时代的数据管道，估值56亿美金的行业创新者

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/016.png)

[![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/017.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247492594&idx=1&sn=ca6e8791338863d251e0551c89d0dafe&chksm=ce9b5c6cf9ecd57a81ccd501d301d31de91f0d4bc384a3ebf8b02aff38f9afd70fd4f5eff437&scene=21#wechat_redirect)

Grafana：SpaceX的数据监测利器，云原生领域的Tableau

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/018.png)

[![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/019.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485849&idx=1&sn=bf5f2c7e329aa529a396e5972836d3ab&chksm=ce98b607f9ef3f11228620a8b1d9bb5cc14f9f3398c7560dd52e08bcc632855a5492eaf33fae&scene=21#wechat_redirect)

CryptoPunks：NFT领域的蒙娜丽莎？销售额已超10亿美元

![](../images/2022-09-09-dbt-shu-ju-xing-ye-xin-wu-chong-gu-zhi-42-yi-mei-jin-de-shu/020.png)
