---
title: 企业数据“LLM ready”与“小Palantir”们的崛起 ｜ AGIX PM Notes
publish_date: '2025-09-01'
publish_timestamp: 1756729213
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/2-DL8V9-6xbc26jtydiKRA
msgid: 1000000412
appmsgid: 2247517552
itemidx: 1
digest: 数据没有“AI-ready” 是目前 AI 落地的最大障碍
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxK9NoWdShfL2kwxIVNVP3VeO2QmRsKXkZZJicInpjQh2n3UZfM3H8MD6Vsf3icM5AfDX8Kj83iaiauFw/0?wx_fmt=jpeg
image_count: 17
archived_at: '2026-04-20T04:17:01+08:00'
---

[![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/002.png)

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/003.png)

[AGIX](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=3570724992708624387#wechat_redirect)诞生于我们对“如何捕获 AGI 时代 beta 和 alphas”这一问题的深度思考。毫无疑问，AGI 代表了未来 20 年最重要的科技范式转换，会像互联网那样重塑了人类社会的运行方式，我们希望 AGIX 成为衡量这一新科技范式的重要指标，如同 Nasdaq100 之于互联网时代。

「AGIX PM Notes」是我们对 AGI 进程的思考记录，希望通过学习 Warren Buffett、Ray Dalio、Howard Marks 等传奇投资者们的分享精神，与所有 AGIX builders 一同见证并参与这场史无前例的技术革命。

**PM Notes**

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/004.svg)

**How to get “LLM ready”？**

作者：Max

今年三月 GTC 的热潮里，似乎每个人都在寻找能够解锁金矿的钥匙。RL（强化学习）、Agentic AI，似乎每一个词都对应着一个几十倍上百倍估值暴涨潜力的创业公司，和新的造富神话。如果共识真能造福，可能经济周期就不应该存在了。

热潮之外，有一类创业公司像个异类。不需要大量融资，A 轮的钱还没花完就已经实现盈亏平衡，投资人因为毛利率偏低或规模化挑战对其不屑一顾，认为它们配不上"几周内 ARR 破千万"的 AI 速度神话。他们的位置特别像早期的 Palantir。

这些公司往往由前 Palantir 员工创办，进而掌握了这一轮服务拉动增长的衣钵，比如 Distyl.ai 的 CEO Arjun Prakash，曾在 Palantir 负责销售、Snorkel AI 负责数据新产品，正是这种深厚的贴合企业数据和落地端的技术经验让他们能够看到真正的痛点。然而，这样的背景和实际的商业成果在当前的投资环境中似乎并不被看重。就像创始人 Alex Karp 在 2025 年给股东的信中坦言："公司快速增长之前，公司和团队承受了外界多年的嘲笑和冷遇，连一些投资人都'轻描淡写、态度冷淡'，我们被视为异类（outcast）。"

这样的异类恰恰为我们揭示了目前 AI 的真实发展阶段——**我们仍处于准备阶段**。这次生成式 AI 的关键能力是决策负担的卸载（offload）或增强（enhancement），而决策需要数据支撑。

数据没有准备就绪是目前 AI 落地的最大障碍，**更深层的问题在于企业流程的 AI 原生化转型**。传统的 AI 部署往往停留在表面——用 AI 工具替换人工操作，但企业流程本身并未发生根本变化。真正的 AI 落地需要将整个组织的知识和流程转换为"AI 原生原语"（AI-native primitives），这是一个远比简单的工具替换更复杂的系统工程。

Distyl.ai 的实践揭示了这种转型的复杂性：企业需要建立完整的反馈循环——从领域专家的知识提取，到 AI 系统的实时监控，再到基于反馈的持续改进。这不是一次性的技术部署，而是需要企业文化、流程和技术架构的系统性重构。

从 Distyl.ai 的实践中，我们可以总结出数据准备的三个关键维度：

**第一，数据基础设施（Data Infrastructure）**。各类结构的数据需要能被 AI Agent 调用和处理，这要求建立统一、高效的数据管道和存储体系。Distyl.ai 的专有"Distillery Platform"正是这一理念的体现，能够量身定制 AI 解决方案，快速而可靠地集成到企业现有流程中。

**第二，知识蒸馏（Distillation）**。需要把过去的大量经验知识和手工技艺变成可量化的数据，或者将工作流程数字化。Distyl.ai 在这方面的突破性贡献是将组织知识转化为 AI 驱动的工作流程、提示和模式——关键是这些可以由领域专家（SMEs）在无需技术技能的情况下进行精炼和调整。

这个过程包含五个关键层级：

**•****组织知识转化：**将企业的隐性知识转换为 AI 可理解的工作流、提示和架构

**•****系统可观测性：**跟踪多组件系统中的每个输入、输出和决策点，提供 AI 操作的详细审计轨迹

**•****Agent 评估与安全护栏：**在多个层级（系统、组件和 LLM 任务）评估 AI 系统性能，使用测试套件确保可靠性和正确性

**•****反馈集成：**为 AI 决策提供详细的审计轨迹，并集成反馈循环进行实时精炼，为后期 RL 准备数据

**•****企业级可靠性与安全：**通过 RBAC、多租户和审计轨迹确保 AI 工作流满足企业级安全、合规和治理要求

**第三，仿真模拟（Simulation）**。像 Palantir 的 Ontology 一样，把企业变成数字孪生（Digital Twin），将企业视为一个正在运行的有状态软件系统，每一个业务动作都成为一个可追踪的事件（Event）。Distyl.ai 的核心创新在于让 AI Agent 能够编排和执行可审计的流程——从 SOP/数据/工具转换为 AI 原生原语，SMEs 提供生成工作流的反馈，AI Agent 利用反馈来精炼和更新流程，最终 AI Agent 编排并执行可审计的工作流。这种闭环系统确保了 AI 决策的透明性和可追溯性，这正是企业级 AI 应用的核心要求。

本周我们也看到了 Snowflake、MongoDB 等数据基础设施股票的大涨，这并非偶然。**高价值的 AI 应用不会停留在回答问题层面，它们要改变现实世界的状态，把"洞察转化为行动"。**为了使用 AI，让企业达到 Enterprise LLM Ready，需要企业数据正在两个层面汇聚：用于捕获新鲜信号的流式数据骨干网，以及具有互操作性存储与治理能力的统一数据云。这与 Confluent 和 Snowflake 所强调的平台架构图完全一致。

**实时流处理的关键角色**正在显现。Confluent 的 Kafka+Flink 架构不仅提供了数据流的基础设施，更重要的是推出了"Streaming Agents"概念——让 AI 代理能够持续监控、推理并基于实时数据流采取行动。这种能力的重要性在于它具备可重放性（Replayability），企业可以安全地在生产环境中测试 AI 决策而不产生实际副作用。Confluent 的 Flink ARR 在 2025 年上半年的两个季度中增长了约 3 倍，其 Kafka 数据流现在能无缝化为 Apache Iceberg 表，实现“流转湖仓”一体的数据分析架构。这意味着远期来看，Kafka 可作为企业运营所有实时数据的统一入口，支撑设备、产线、用户行为等生产和运营实体的实时数据流采集与聚合，将物理世界的行为流（传感器、日志、交易等）桥接到流+湖仓分析视图，让仿真和数字孪生不仅有“实时”也能有“历史回溯”。叠加生成式 AI 的决策强化特性，将现代企业运营带入一个新的层次。

**同时，代理性 AI（Agentic AI）依赖于四个核心循环：推理（Reasoning）、记忆（RAG/向量检索）、规划（Planning）以及与企业数据相连的执行（Execution）。**

这四个环节缺一不可，它们都建立在坚实的数据基础设施之上。尤其是，企业正在标准化开放湖仓表格格式来为 AI 提供共享治理——Snowflake 的 Open Catalog 管理 Apache Iceberg，而 Confluent 的 Tableflow 将 Kafka 流物化为 Iceberg/Delta，以及 Databricks 的 Unity Catalog，就是一个统一治理框架，用于同时管理结构化数据、非结构化数据和 AI 模型资产，且内置了 AI 驱动的文档、发现和优化能力，从而消除了定制 ETL 的需求。

随着 AI 从试验项目走向生产环境，可观测性和安全性也会成为企业关注的焦点，在数据准备阶段之后，以可观测性为代表的过程治理就显现出其重要性。Datadog 的 LLM 可观测性平台正在填补技术监控的空白，提供端到端的追踪、内置的质量/安全评估、A/B 测试框架以及 AI 代理控制台。

但过程治理更 AI 原生的表达可能是： **决策透明性与可追溯性**：每个 AI 决策都必须有完整的审计轨迹，从输入数据到中间推理步骤，再到最终输出，全程可追溯。

****•**专家-AI 协作的反馈机制：**领域专家可以实时查看 AI 生成的工作流，提供反馈并进行调整，这种人在回路（Human-in-the-loop）的设计确保了 AI 决策与业务实际需求的一致性。

****•**多层级的评估与护栏系统：**不同于传统的二元评估，企业需要在系统级、组件级和任务级分别设置评估标准和安全护栏，形成立体的质量保证体系。

在 AI 的准备阶段，为企业提供流动性强、治理能力强、分析能力丰富的数据底座至关重要。毕竟，再强大的 AI 模型，离开了高质量、结构化、实时更新的数据支撑，也只能是空中楼阁。而那些被市场暂时忽视的"异类"，或许正是下一轮 AI 浪潮的真正受益者。

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/005.png)

**01.**

**本周市场总结**

**科技板块为上周唯一净卖出板块**

本周对冲基金整体仍为全球股票的净买方，但各地区的买入力度有限。按区域来看，买盘主要集中在北美股票（名义金额与相对规模均居首），其次是欧洲和日本；亚洲（不含日本）则是唯一呈现净卖出的区域。

北美市场方面，买盘来自小幅加仓的多头头寸，而空头活动相对平淡。按行业分，资金主要流入工业（地面运输与机械）、通信服务（互动媒体）、必需消费品（药品及综合零售、食品分销）及金融（大型多元化银行与支付）。

科技板块则是唯一显著被净卖出的板块，其中半导体、IT 服务和电子设备均位列卖出较多的行业。因子层面流向同样温和，没有因子出现超过 ±0.5 标准差的买入或卖出。尽管买入力度有限，美国股票多空基金净杠杆环比仍上升约 6%，主要受上周五杰克逊霍尔会议后的市场反应推动。当前净杠杆已回升至 55%，处于长期历史的 70 分位以上，且在过去 12 个月的 95 分位水平。

其他地区方面，欧洲是唯一出现较为明显买盘的区域，主要来自小幅多头加仓。与北美相反，欧洲科技是本周推动净买入的核心，软件及半导体贡献居前。其他受到净买盘关注的行业包括欧洲防务、欧洲银行及欧洲奢侈品。值得注意的是，尽管欧洲动量因子出现回调，但并未观察到该因子卖出增加，唯一被显著卖出的因子是规模因子（Size）。

在亚洲（不含日本），对冲基金转为卖方，此前两周在中国市场的买盘明显放缓，同时加大了区域内空头配置，主要集中于中国可选消费和中国科技，来自亚洲和美国的基金均有贡献。

**全球股市普遍向上，AGIX 表现优异**

业绩表现方面，本周对冲基金整体跑赢基准指数，主要得益于北美地区多头与空头的相对表现。AGIX 本周上涨 1.99%，大幅跑赢三大指数：S&P 500（0.33%），QQQ（0.01%），DowJones（0.58%）。

北美拥挤多头的回报较拥挤空头高出约 3.3%，相对标普 500 的超额收益主要来自多头端。

平均来看，全球基金本周上涨约 25 个基点，优于 MSCI 仅约 13 个基点的涨幅；全球多空基金则上涨约 40 个基点。美洲多空基金录得约 40 个基点涨幅，捕捉了标普本周约 55 个基点涨幅的较大部分。

其他地区方面，欧洲与亚洲多空基金平均分别上涨 30 个基点和 60 个基点，尽管欧元区 STOXX 600 与 MSCI 亚太指数当周录得下跌。随着本月强劲收官，平均全球对冲基金在 8 月底已上涨 1.7%，年内累积收益达 7.1%。按区域分拆，美洲多空基金年内上涨 7.6%；欧洲与亚洲多空基金则表现更佳，均录得 11.6%的年内涨幅。

**02.**

**AI Alphas**

**NVIDIA （NVDA） 公布 2026 财年第二季度业绩**

NVIDIA 公布截至 7 月 27 日的 2026 财年第二季度业绩，营收 467 亿美元，环比增长 6%，同比增长 56%。其 Blackwell 数据中心收入环比增长 17%。本季度未向中国客户销售 H20 芯片，但释放了 1.8 亿美元此前预留库存，并向境外客户实现约 6.5 亿美元的 H20 销售。GAAP 毛利率为 72.4%，非 GAAP 毛利率 72.7%。摊薄每股收益分别为 1.08 美元和 1.05 美元，若不计库存释放及相关税务影响，则为 1.04 美元。

**Apple （AAPL） 股价因新品预期与强劲业绩交投活跃**

8 月 27 日，苹果成交量达 3130 万股，显著高于近期水平。市场将交投活跃归因于新品发布传闻及第三财季强劲业绩。公司截至 6 月 28 日的季度营收达 940 亿美元，同比增长近 10%，高于预期 50 亿美元。每股收益 1.57 美元，超出市场预测。iPhone 收入同比增长 13.5%至 445.8 亿美元，Mac 销售 80.5 亿美元亦超出预期。iPad 收入 65.8 亿美元略低于预估，可穿戴收入降至 74 亿美元，而服务收入稳步上升至 274.2 亿美元。整体毛利率 46.5%，略高于分析师预期。结果显示苹果在科技行业面临逆风之际仍具韧性。

**AI 研究员正在离开 Meta（META）Superintelligence Lab**

在 Meta 宣布成立 Superintelligence Lab 仅两个月后，已有数名 AI 研究员从该实验室辞职。

首先，Avi Verma 和 Ethan Knight 已从 Superintelligence Lab 辞职，并返回其旧东家 OpenAI。另一位引人注目的离职者是 Rishabh Agarwal，这位前 Google DeepMind 研究员被 Meta 挖角，传闻年薪高达 100 万美元。他于 4 月加入 Meta，但在 8 月 25 日宣布，这是他在该实验室的最后一周。

此外，两位知情人士向 TechCrunch 透露，Scale AI 的前 CEO Alexandar Wang 为协助管理 MSL 而从 Scale AI 带来的至少一名前高管——Scale AI 前生成式 AI 产品与运营高级副总裁 Ruben Mayer——在加入 Meta 仅两个月后也已离职。

**Microsoft （MSFT） 启动自研 AI 模型测试，减少对 OpenAI 依赖**

微软宣布启动自研 AI 模型“MAI-1”的公开测试，以增强其面向消费者的 Copilot 助手功能。该模型正在 LMArena 网站上接受用户评价，并将在未来数周内应用于 Copilot 部分文本场景，以便收集反馈并改进性能。微软长期依赖 OpenAI 的模型，此举显示其正努力构建自主的 AI 能力。

**Palantir （PLTR） 与富士通合作在日本扩张，推动 AIP 普及**

8 月 5 日，Palantir 与富士通日本公司签署授权协议，将其 AIP 平台纳入富士通的“Uvance”框架，并于 8 月 19 日正式公布。通过该协议，富士通可向日本企业客户分销 Palantir 的生成式 AI 解决方案。此次合作强化了 Palantir 在亚洲的布局，使 AIP 成为富士通企业解决方案的核心层。富士通计划将 AI 驱动的流程引入金融、物流、制造等行业，以抓住日本 AI 采用率上两位数增长的机遇。Palantir 则可借助富士通的客户网络，拓展在应用型 AI 领域的商业化渠道。

**Google（GOOGL） 在弗吉尼亚追加 90 亿美元投资，强化 AI 和云基础设施**

彭博社 8 月 28 日报道，Google 将在 2026 年前向弗吉尼亚州投资 90 亿美元，用于扩建云与 AI 基础设施。计划包括在 Chesterfield 县建设新数据中心，并扩展 Loudoun 和 Prince William 县的设施，进一步巩固北弗吉尼亚作为全美数据中心枢纽的地位。微软（MSFT）、亚马逊（AMZN）和 Meta（META）此前亦宣布类似的数十亿美元投资，竞争加速。Meta 更被传将在路易斯安那投入约 500 亿美元建设数据中心。Google 还承诺提供 10 亿美元，为弗吉尼亚州学生一年使用其 AI Pro 方案的机会。此类投资不仅反映出 AI 算力需求的持续增长，也符合美国推动本土科技产业发展的政策方向。

7 日，瑞银分析师 John Hodulik 重申对 AppLovin 的“买入”评级，并将目标价定为 540.00 美元。此次评级重申是在公司公布二季度业绩后做出的，业绩超出华尔街预期，并对本期销售额给出更高指引。瑞银将公司 2026 财年的 EBITDA 预期上调至 61.8 亿美元，高于华尔街普遍预期的 56.5 亿美元。这一调整主要得益于二、三季度游戏相关业务表现好于预期。该机构对 AppLovin 分阶段推出其自助式网页广告平台的计划持乐观态度。该平台将于今年 10 月启动，首先向基于推荐的广告客户开放，并计划在 2026 年上半年向所有客户全面开放，这有助于降低中期网页广告收入增长的风险。

**Samsara （IOT） 获分析师支持，产品采用与订阅收入加速**

TD Cowen 分析师 Derrick Wood 重申对 Samsara 的买入评级，指出其产品采用和订阅增长势头强劲，年经常性收入（ARR）持续上升，资产标签等功能的普及提升了平台在多个行业的价值。RBC 资本也维持买评级，进一步增强了投资者信心。Samsara 正在扩展 AI 驱动的“连接运营”平台，将车辆、设备和设施数据整合，用于提升安全性、效率和运营可视化。

**03.**

**ETF 101**

**投资大师们是如何看待 ETF 的？**

当谈到投资，很少有人的话语像沃伦·巴菲特和查理·芒格那样被奉为金科玉律。这两位价值投资大师对 ETF 的看法，对普通投资者有着重要的指导意义。那么，他们究竟如何看待 ETF 这一投资工具呢？

**巴菲特的指数投资之路**

**巴菲特虽然以精选个股著称，但他对普通投资者的建议却出人意料地简单：投资低成本指数基金。**

早在 1996 年，巴菲特就在伯克希尔的股东信中写道：“大多数投资者，无论是机构还是个人，都会发现最佳投资方式是一只成本极低的 S&P 500 指数基金。”

这一观点在 2007 年更是得到了实践验证。当年，巴菲特与对冲基金管理公司 Protégé Partners 打赌：在 10 年内，S&P 500 指数基金的表现将优于精心挑选的五只对冲基金。结果如何？到 2017 年底，S&P 500 指数基金累计回报约 125.8%，而对冲基金组合仅有 36.3%。

巴菲特赢得这场赌局的核心原因在于：低成本。高额管理费和业绩提成严重侵蚀了对冲基金的实际回报，而低成本的指数 ETF 则将更多收益留给了投资者。

**芒格对 ETF 的警示与认可**

与巴菲特相比，芒格对某些 ETF 产品持更为谨慎的态度。他曾明确警告投资者远离复杂的 ETF 产品，特别是杠杆 ETF 和反向 ETF。在 2013 年的一次采访中，芒格表示：“一般个人投资者最好对期权、做空股票、三倍反向做空 ETF、结构性票据和可变年金等一些金融工具保持谨慎。简单一些总没错，至少可以降低成本。”

然而，对于传统的、低成本的指数 ETF，芒格与巴菲特持相似观点，认为这是大多数普通投资者的理性选择。

**价值投资理念与 ETF 的契合点**

乍看之下，巴菲特和芒格推崇的价值投资似乎与被动的 ETF 投资背道而驰，但深入分析会发现二者有着共通之处：

**•**长期持有：价值投资强调长期持有优质资产，而非频繁交易。ETF 正是为长期投资设计的工具。

**•**低成本：巴菲特反复强调成本对长期回报的侵蚀作用。低成本 ETF 正是对这一理念的最佳实践。

**•** 分散风险：虽然巴菲特本人偏好集中投资，但他建议普通投资者通过指数基金分散风险。

**•** 避免自我膨胀：芒格常说："认识自己的能力圈至关重要。"对于不具备专业选股能力的投资者，ETF 是更为谦逊和理性的选择。

**从大师观点中获取的实用建议**

基于巴菲特和芒格的观点，普通投资者可以采纳以下 ETF 投资策略：

**•** 选择费率极低的宽基指数 ETF 作为投资组合的核心

**•**避开复杂的结构性 ETF 产品，特别是杠杆 ETF 和反向 ETF

**•** 采取长期持有策略，避免频繁交易

**•** 定期投资，利用复利效应和美元成本平均法

巴菲特和芒格虽然以个股投资成名，但他们对 ETF 的认可恰恰体现了价值投资的本质：理性、克制和对长期价值的追求。对普通投资者而言，遵循这些大师的建议，选择适合自己的 ETF 产品，或许是通往投资成功的更为稳妥的道路。

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/006.png)

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/007.png)

排版：夏悦涵

延伸阅读

[![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/008.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517523&idx=1&sn=49485604220ec400efe1bff17ecdfb7c&scene=21#wechat_redirect)

AI 叙事重塑科技投资，市场 Hype 中如何识别真正的 AI Winners？｜AGIX 年度回顾

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/009.png)

[![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/010.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517480&idx=1&sn=3f682da7c82b1483a6b3c1674c459e8f&scene=21#wechat_redirect)

8 个月营收提高 4 倍，n8n 为什么是 AI Agent 最受欢迎的搭建平台？

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/011.png)

[![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/012.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517328&idx=1&sn=6bc1fea7dc6c863197dcb584023cd89b&scene=21#wechat_redirect)

LLM 商业化猜想：OpenAI 会走向 Google 的商业化之路吗？｜AGIX PM Notes

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/013.png)

[![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/014.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517278&idx=1&sn=c94e50d20f18c33d7a78635e15c7a36f&scene=21#wechat_redirect)

Physical Intelligence 核心技术团队分享：物理世界的“Vibe Coding”如何实现？

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/015.png)

[![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517203&idx=1&sn=1444daf92341aadaeee873f0a7479c53&scene=21#wechat_redirect)

拾象 AGI 观察：LLM 路线分化，AI 产品的非技术壁垒，Agent“保鲜窗口期”

![](../images/2025-09-01-qi-ye-shu-ju-llm-ready-yu-xiao-palantir-men-de-jue-qi-agix/017.png)
