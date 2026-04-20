---
title: Metronome：OpenAI、Anthropic背后的计费平台，会是AI时代的Stripe吗？
publish_date: '2024-12-25'
publish_timestamp: 1735128200
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/rwapiYV2Vgm8SlhGZTPUDA
msgid: 1000000314
appmsgid: 2247510949
itemidx: 1
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzdCE42kiaicwUsVwD5fFXMibOqIrYXONAXqLJxHFXdicIgxGPxRwXqbnWUDnsA01A1eBic587MEdFaBbg/0?wx_fmt=jpeg
image_count: 38
archived_at: '2026-04-20T03:01:01+08:00'
---

[![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/001.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect)

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/002.png)

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/003.png)

作者：haozhen

编辑：penny

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/004.png)

企业计费平台作为企业运营的枢纽，不仅涉及费用计算，还深刻影响企业运营和现金流。随着**上云和 AI 这两大趋势推动按量计费模式，企业的定价策略和计费方式也更加动态复杂，给计费平台带来了机会。**

目前，计费平台尚未出现像 Salesforce、Stripe、Oracle 这样的行业 leader ，而计费的复杂性和专业性使其难以被上下游平台兼顾。**因此，计费平台成为软件生态中一个关键但尚未完全开发的领域，Metronome 是其中的重要玩家，OpenAI、Anthropic、Databricks，英伟达等都是其客户。**

Metronome 成立于 2019 年，为企业提供计费平台，可将客户销售等原始事件转化为计费指标输出，在 AI 驱动下收入获得了显著增长，每月要处理数百亿个事件，在账单运行期间每分钟要处理数十万张发票，去年 ARR 增长了 6 倍。在业务流程中，Metronome 上游是销售软件如 Salesforce，下游是财务，发票软件如 Stripe、Quickbooks 等。**在积累大量计费数据后，或许能从计费平台切入公司运营的其他环节。**

Metronome 两位创始人是 Scott Woody 和 Kevin Liu，之前的创业公司分别被 Dropbox 收购，在 Dropbox 体会到计费的复杂和费时。两人做了大量客户调研后决定解决这个痛点。

**虽然 Metronome 想象空间巨大，但计费领域玩家众多，竞争非常激烈。**Metronome 虽然在准确性上做得非常好，但若无法将大量一线数据积累到自己平台上进行产品迭代或者业务拓展，那可能会被努力转型的传统计费软件、向计费领域拓展的上下游软件、公司内部自建计费平台等对手吞并。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/005.png)

**💡**目录 **💡**

01 计费平台是企业运营的枢纽

02 Metronome 的产品

03 创始团队

04 经营情况

05 市场与竞争

06 Metronome 的优势与局限

07 融资与未来发展

**01.**

**计费平台是企业运营的枢纽**

目前，各家公司都将大量资源投入到自身产品的建设、推广等方面，而定价模式往往会被忽略。**但正如 Metronome 的创始人 Kevin Liu 所说，定价模式是可以改变一家公司市场地位的最重要杠杆之一。**

**产品定价模式的实施依赖于公司计费平台，计费平台联系着公司运营的许多方面，需要接收产品的使用、销售情况，比如合约签订、交易发生，并输出承诺付费金额、已履约金额等计费数据以供开立发票、更新看板等。SaaS 公司的产品从 building 到 GTM 等所有的环节都可能因为计费复杂性而出现延迟等变故。**

例如，过去手机运营商会根据用户通话时长和短信数量收费，而 T-Mobile 发现大多数用户最频繁联系的对象往往是他们的家人，因此首创了“家庭计划”（family plan）收费方式，鼓励用户将家人加入一个计划，家庭成员之间可以免费通话和发送短信。这种模式使得 T-Mobile 获得病毒式传播。但 T-Mobile 的竞争对手因为计费平台无法快速适应“家庭内免费通话和短信”的复杂计费需求，短期内无法推出类似计划，让 T-Mobile 成功抢占市场份额。

例如，Dropbox 在拓展日本市场时，由于内部计费平台的限制，无法单独为日本用户设置本地化的价格和语言版本，这种系统上的障碍使 Dropbox 推出新的本地化产品或价格策略等战略决策被迫延迟。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/006.png)

大部分公司的产品定价方式可以分成订阅制、买断制、企业自定义解决方案等，买断制和订阅制因易于理解，在 SaaS 行业早期发展时极大促进了产品销售。**但随着市场的发展变化，尤其是 AI 的发展，收费标准逐渐从 seats 转向用户使用价值，基于使用量的计费方式成为新的趋势，具体原因包括：**

**1. 产品成本结构随着云、AI 的发展而变化：**上云前，产品部署在用户的服务器上，运维成本是由用户的服务器承担，但上云后，云平台会按照使用量向公司收取费用；随着 AI 产品越来越受欢迎，而 AI 大模型一般根据 token 的量计算成本，因而越来越多的产品成本结构是按量计费，若收入也是按量计费则可以更好匹配产品成本。

**2. 用户需要更公平的定价模型：**基于 seats 的定价非常粗颗粒地衡量了用户如何使用公司产品，比如用户在购买了 seats 后，并不是每时每刻都需要使用产品，在不使用产品的时间内用户会产生“亏了”的主观感受。

**3. 公司产品不断地发展：**随着产品功能等的发展，定价会越来越复杂，买断制和订阅制需要不断修正购买条件或价格才能使收入增加，比如在推出产品新功能的时候，就需要考虑是将新功能加入已有的订阅套餐并提高套餐价格，还是新增一个订阅套餐供用户选择等等。而基于使用量的计费方式既可以让用户比较容易以较低的价格开始使用，又可以在用户深度使用的时候自然而然地增加收入。

但如 a16z 的投资人 Martin Casado 所说，**构建一个能够处理基于使用量计费的计费平台非常困难。**首先，处理大规模按量计费所需的数据是个不小的技术问题。其次，按量计费是一种相对较新的计费方式，设置新的计费方式通常需要编写大量代码。这两个问题结合在一起，意味着即使对于大型计费平台来说，推出按量计费平台也常常需要数月的时间。而且，随着业务的成熟，计费的复杂性会迅速增加，因为随着用户群和产品套件的增长，不仅数据量在增长，对数据连接的需求也呈指数级增长。**所以基于使用量计费的平台必须具有可扩展性并具有高准确性，且计费迭代的速度需要与产品迭代的速度相匹配。传统的计费平台已明显无法满足这些需求。**

综上所述，计费平台不仅是简单的计算费用，还影响着企业运营、现金流等诸多方面，在 AI 推动下，按量计费的兴起又给计费行业带来了全新的机遇和挑战。**相比销售和支付等环节，计费平台还没有形成一个类似 Salesforce、Stripe、Oracle 这样的领军公司，**领军企业可作为行业标杆，提升计费的规范性和行业效率，同时，计费平台的专业性和复杂性也使得计费平台目前很难由上下游环节兼顾。**因此企业计费平台处于软件生态中一个非常重要但未被充分开发的领域，这为创业公司 Metronome 提供了机会。**

**02.**

**Metronome 的产品**

**产品功能和用例**

**Metronome 提供了一个基于使用量的计费平台，可将输入的原始事件转化为计费指标输出，**公司技术团队无需花时间处理计费问题，业务团队又可以完全控制产品的定价方式。**创始人 Scott Woody 认为可以把 Metronome 想象成 Datadog，**主要解决了三个核心问题：第一，让客户在无需任何代码的前提下，几分钟就可以启动新的定价模型；第二，让计费平台为产品服务，Metronome 可以将计费数据从计费平台中取出，并输出到其他系统，比如成本控制系统；第三，计费等数据可以持续提供给公司来做决策，比如优化成本、收入预估。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/007.png)

**Metronome 可与 Stripe、AWS、Salesforce 等集成。在业务流程中，Metronome 上游是 Salesforce 等销售软件，下游是 Stripe、Quickbooks 等财务软件和数据平台。**例如，客户在 Salesforce 中完成定价，通过 Metronome 计费后，最终进入 Quickbooks，Metronome 也会自动将用户承诺的支付金额、购买产品的使用量以及被兑现的数据等传到 Salesforce 或 Metronome 内置的数据看板，来帮助团队及时发起追加销售、交叉销售等；例如，公司与用户发生交易后，在发票结算期结束时，Metronome 会自动在 Stripe 中创建相应的发票以收取付款。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/008.png)

**•  以 OpenAI 为例**

2021 年，OpenAI 意识到需要一个可扩展的计费基础设施，来匹配自身产品快速创新和增长。最初，OpenAI 使用的是内部开发的计费平台，这个平台依靠人工维护特定的程序脚本，需要手动处理很多工作，比如跟踪用户的使用情况、生成发票等。而且在定价管理上也非常耗时，无法迅速支持新产品的发布以及客户需求的拓展。OpenAI 收入运营高级经理 Lauren Workman 曾表示，在引入 Metronome 之前，调整价格或新增产品是一件非常耗时且繁琐的手动操作。OpenAI 应用工程团队负责人 Evan Morikawa 也认为内部的系统缺乏灵活性和自定义能力，无法支持基于使用量的定价模式或企业合同的复杂性。因此，OpenAI 需要一个全新的计费平台来支持产品发布等，并实现从编码脚本到自动计费的飞跃。由于 Metronome 易于部署且全面支持 OpenAI 的业务模式，所以 OpenAI 选择了与 Metronome 进行合作。

**Metronome 用了不到两周时间就完成了部署并投入运营，可以支持复杂的企业合同和自助式随用随付模式，并且能够跟上 OpenAI 每月多款产品的发布步伐。**Metronome 对于 OpenAI 的帮助具体包括：  

1. 引入 Metronome 之前，在 OpenAI 只有 1-1.5 万名用户的时候，当时工程师中有大约一半的人员需要负责计费，如今 OpenAI 用户数大幅增长，但在 Metronome 的帮助下，只有不到 10 位工程师负责计费。

2. 与 Metronome 合作之前，OpenAI 需要花费大约 6-8 周的时间才能推出新的定价模型，而接入 Metronome 之后只需要大约六分钟，这有助于 OpenAI 业务的快速变化。

3. 通过采用 Metronome，OpenAI 能够将工程资源从计费转移到核心产品开发。

4. Metronome 还显著简化了 OpenAI 的发票管理，收入运营团队之前需要每月花费数小时在 Excel 中管理发票，现在在 Metronome UI 中只需几分钟即可进行更改。

5. OpenAI 还利用 Metronome 的 API 为客户仪表板提供支持，客户可以在组织和个人层面跟踪每日使用情况情况。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/009.png)

**产品特点**

Metronome 计费平台的特点包括定价灵活、专业准确、易于使用。

**•  定价灵活**

1) Metronome 提供 Modular pricing engine（模块化定价引擎）和 Granular customer configuration（精细的用户配置），可自定义按使用量、seats 等不同的计费模式，以适应多样化的业务，避免计费错误。

2) 定价更新可以立即生效、将来生效或追溯生效。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/010.png)

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/011.png)

**•  专业准确**

1) **专业：**Metronome 专注于使用量计费，有专家称相比于 Salesforce，Metronome 是一个更适合审计、更符合法规要求的系统。

2) **准确：****按量计费最重要的就是准确性，客户会为了准确性付费，对于客户来说，知道自己没有因为错开账单等而损失数十万美元是非常重要的。**Metronome 的平台是 High throughput data platform（高吞吐量数据平台），可测量并存储所有原始收入相关的事件以支持当前和未来的定价，有极大规模的准确性和可靠。

3) **实时：**Metronome 提供 Embedded real-time data（嵌入式实时数据），可将实时使用情况和支出数据输出到业务系统。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/012.png)

•  **易于使用**

1) **集成性强：**Metronome 集成了大量的工作软件，从而能够在系统中容纳许多计费方案。Metronome 集成的软件种类可分成 Invoicing and accounting（如 Stripe）、Cloud marketplaces（如 AWS）、CRM（如 Saleforce）、Tax（如 Anrok） 和 Data export（如 Databricks、Snowflake、MySQL）这 5 类。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/013.png)

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/014.png)

2) **开箱即用：**官网的宣传语之一就是“World-class billing，out of the box”。有用户反馈 Metronome 启动成本较低，“开箱即用”做的很好。

**03.**

**创始团队**

**Metronome 创始人是 Scott Woody 和 Kevin Liu，两人之前的创业公司均成功被 Dropbox 收购。Kevin Liu 在采访中自述这一次创业非常慎重，**虽然两人早在 Dropbox 就共事并建立了深厚的友谊，二人仍花了数年时间通过共同讨论、实践和探索，来验证彼此是否适合作为创业合伙人。前期市场调研时，二人也做了充足的准备。为了更好地了解目标市场，Kevin Liu 与 Scott Woody 曾假扮斯坦福学生来进行实地调查，并设定目标——必须经历 50 次直接拒绝再考虑停止调研。在确立痛点时，Kevin Liu 和Scott Woody 也与数百家公司反复讨论了他们的计费需求才确定下 Metronome 的业务方向。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/015.png)

**•  Scott Woody（ Metronome CTO ➡️ CEO）**

Scott Woody 博士毕业于斯坦福大学商学院，曾于 2011 年创立 Foundry（Applicant Tracking System）。2013 年 Foundry 被 Dropbox 收购后，Scott Woody 也加入了 Dropbox 并担任 Engineer。Scott Woody 称 Metronome 的创业想法开始于自己在 Dropbox 的工作，他在 Dropbox 领导增长和货币化团队，需要发布一系列新产品的定价，每次更改价格都要花 3-6 个月，甚至 12 个月，才能生效，所以 2019 年他从 Dropbox 辞职并创立 Metronome，希望能帮助业务团队控制产品的定价。

**•  Kevin Liu（ Metronome CEO ➡️ Chairman）**

Kevin Liu 本科毕业于美国宾夕法尼亚大学沃顿商学院，曾于 2010 年创立 Predictive Edge 并担任 CEO，Predictive Edge 是斯坦福 StartX 创业社区的一部分，致力于电子商务产品的动态定价方法，以便营销人员发送给用户进行 A/B 测试。2014 年 Predictive Edge 被 Dropbox 收购后，Kevin Liu 也加入 Dropbox 担任 Enterprise Marketing，参与到 Dropbox 企业产品的早期营销工作中，2016 年离职后作为个人 investor 帮初创公司创始人进行融资、产品、GTM 和运营，更加深入了解到了企业定价的痛点，因此 2019 年创立 Metronome。

**04.**

**经营情况**

**•  商业模式**

官网显示具体定价需联系 Metronome，有新闻表示 Metronome 本身也采用了基于使用量的定价模式。另有专家称 Metronome 是按使用成本收费，还要支付额外的平台费和账单费，价格相对偏贵。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/016.png)

**•  收入**

得益于 AI 的大力发展，越来越多的公司从订阅制转向基于使用量的模式或两者的结合，Metronome 表示去年 ARR 增长了 6 倍，每天处理的事件数量突破了 10 亿，**每月需要处理数百亿个事件，在账单运行期间每分钟要处理数十万张发票。**

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/017.png)

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/018.png)

**•  客户群**

**24 年 6 月，Scott Woody 表示 Metronome 累计已有数亿使用者。目前客户既包括 OpenAI 和 Anthropic 等初创公司，也有 Databricks 和 Nvidia 等相对更大、更成熟的企业。**Metronome 的客户群体可以大致分成三类：

1）**目前使用传统方式计费，但希望转型为按量计费的客户，**比如数据转换工具 dbt，希望在现有业务模式中逐步引入按量计费；

2）**已使用按量计费，但自建系统存在瓶颈的客户，**比如 Confluent、Databricks，需要更高效、灵活的按量计费解决方案；

3）**大量 AI 相关公司，**比如 OpenAI、Anthropic、Anyscale、LangChain、Replicate 等。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/019.png)

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/020.png)

**创业初期，Metronome 的客户多为初创公司，从去年开始扩展到了更大的企业领域。**Metronome 甚至在还没有产出产品 demo 的时候就得到了第一批客户，Kevin Liu 认为是因为 Metronome 找准了客户痛点，并展示了高度的专业，从而赢得了客户的信任。**Metronome 价值观就是以客户为中心，相比之下 Metronome 并不太在意自己的成本，而是选择先满足客户的需求。**比如在和 OpenAI 合作的时候，OpenAI 会发送大量的数据给 Metronome，这让 Metronome 承担了很多成本，但 Kevin Liu 认为相比收入，更重要的是让 OpenAI 的业务保持连续，以及跟上 OpenAI 的业务拓展进程。

**05.**

**市场与竞争**

**按量计费的机遇与挑战**

**•  机遇**

如前文所述，随着 AI 的发展，按量计费逐渐流行。按量计费可以：

1）使得产品收益与云、AI 的成本对应；

2）给用户更公平的定价模型；

3）可以让用户比较容易开始使用产品，又可以随着用户使用的增长自然而然地增加收入。

除此之外，**还可以解决由于 AI 发展带来的人工需求减少而进一步导致用户所需 seats 减少的问题，即随着产品自动化的深入发展，尤其是AI的大力发展，产品越成功，用户所需的 seats 越少。**已经规模化使用按量计费的公司，比如 Snowflake，也证明按量计费的可行性。

有研究表明，目前基于使用量定价的 SaaS 产品自 2018 年以来一直呈上升趋势，但 2023 年按量计费的采用率同比略有下降。与此同时有 17 %公司正在积极测试基于使用量计费。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/021.png)

**•  挑战**

但按量计费也存在着挑战：

1）相比订阅制每月固定 seats 费用的支出，按量计费使得用户或公司无法精确预计费用开支，尤其是对于计划外支出较为敏感的群体。有研究表明，大多数按使用量计费的企业采用的是混合模式，而非纯粹按使用量计费， 尤其是小型企业。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/022.png)

2）按量收费需要对大量的使用数量进行计算，对于数据计算要求较高，对于计费平台的要求也随之增加。

3）虽然现实生活中已经存在电信公司流量计费、日常生活中水电收费等按量计费的方式，但相比订阅制，用户对于 SaaS 产品按量收费方式较为陌生。

4）虽然用户可以给自己的使用量设置上限来控制费用支出（这可能需要额外去搭建一个产品），但仍可能导致用户在使用的过程中较为“小心谨慎”。

5）适用的场景较为有限，通常只适用于业务单一或易于数据化的产品，比如邮件、短信发送次数等场景。

**竞争对手**

**在计费平台这个领域，客户除了关注实时性、成本等许多因素之外，最关注的就是准确性。如果计费不准确，那就需要报错、重新检查等操作，会延长客户的收费时间，影响公司现金流。因此能抓住准确性就能最大程度地占领市场和客户。**Metronome 的竞争对手可大致分成四类。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/023.png)

**•****传统计费软件，比如 Chargebee、Chargify、Zuora**

传统计费软件配置复杂，缺乏灵活定制化的能力，成本高昂。在宣传上，传统软件一般不会很大力度地对客户进行电话或者短信营销，但传统计费软件目前也在努力向新兴玩家学习。

以 Zuora 为例，Zuora 的计费平台通过云计算提供定价、计量、计费服务。Zuora 的功能和集成组件比 Metronome 更多，比如收入核算、CPQ（Configure, Price, Quote）、客户流失管理、多支付提供商集成等，但是 Zuora 在计费方面智能程度不如 Metronome，且 Zuora 月度结算的节奏太慢，不能实时反馈用户的使用情况。但有专家反馈 Zuora 产品的改进速度很快且非常显著，比如 Zuora 原先专注于订阅制计费并做得非常好，后来才转向基于使用量的计费，目前即使产品不如 Metronome，但已经可以提供按量计费的模型来满足用户的基础需求。

**•****上下游软件，比如 Stripe、NetSuite、Saleforce**

在业务层面，Metronome 的上下游软件包括 Stripe、NetSuite、Saleforce 等。这些企业的主营领域不在计费，因此在计费上往往不够灵活，目前一般与 Metronome 在流程上形成上下游的共存、互补局面。未来这些上下游的领头企业在寻求业务拓展的时候，可能会凭借资金、规模优势，创造出在计费上更完善的产品来取代 Metronome，或者会通过收购 Metronome 来填补功能空白。与此同时，Metronome 则希望从计费角度切入，让公司在 Metronome 平台上管理其他上下游软件，有专家认为公司已经花费了部署、自定义的时间让 Metronome 按照需要的方式工作，那一定会想让 Metronome 兼做一些上下游的事情来增大效益。

以 Stripe 为例，Stripe 专注于为企业提供支付服务。在计费上，Stripe 只提供了一组 API 供构建，明显不够灵活，而且目前若要在 Stripe 中做 Metronome 的计费工作，工作量会很大，但未来 Stripe 若从支付出发，向计费领域拓展业务，存在取代 Metronome 的可能性，Stripe 也有可能直接收购 Metronome。

**•** **其他初创公司产品，比如 Orb、M3ter**

计费领域的其他初创公司产品与 Metronome 有相似之处，但各家公司产品的功能侧重点、针对人群略有不同。

以 Orb 为例，Orb 致力于帮助企业自动处理各种计费任务，包括基于使用量计费、订阅模式或混合模式。Orb 与 Metronome 在用户体验、计费指标、设置计划等基本功能上有相似之处。但两家侧重有不同：

**1）目标用户：**Orb 更适合开发人员使用；Metronome 对于会计、销售和运营等非技术团队更加友好。

**2）商业模式：**Metronome 是按使用成本收费，还要支付额外的平台费和账单费；Orb 不会收取事件费用，但会收取平台费和账单费。有专家称，当考虑 10-12 个 SKU 时，使用 Metronome 的成本会是使用 Orb 的成本的 10 倍。

**3）业务重点：**Metronome 专注于发送更多的事件，拥有更多计费和合规性功能，能够理解地理位置，计费模式和数据导出也比 Orb 更成熟；Orb 关注如何节省成本。

**•** **公司自建软件**

对于初创公司或中小公司来说，几乎不会自建计费平台，因为对数据、人员、资源、时间要求太高。但大公司可能会出于费用考虑选择自建，因此 Metronome 需要提供更高性价比的产品。

**06.**

**Metronome 的**

**优势与局限**

**为什么看好？**

**•** **从计费平台切入，精准洞察 AI 产品计费趋势**

随着 AI 产品的普及，按量计费模式逐渐成为主流。**如创始人 Kevin Liu 所说，Metronome 可以视为是支持企业向按量计费模型过渡的理想工具，**能将实际发生的业务事件转化为结构化数据，从而方便分析与结算。在未来，Metronome 可能成为公司运营的核心枢纽，甚至有潜力作为按量计费领域的行业标杆，提升该领域的规范性与效率。

且 Metronome 在转化的过程中可积累大量有关用户如何使用产品的数据，可以为公司改进产品提供参考，为业务收入做预测，**即 Metronome 可以从计费平台切入，逐步渗透到公司运行的各个环节，实现在 Metronome 内部平台上管理公司的其他软件系统。**比如没有 Metronome 的时候，公司一般只能依靠 Saleforce 来展示收入预测，但用 Metronome 基于使用量计费后，Saleforce 不再是唯一的数据来源，且公司收入一般和用户使用量是直接挂钩，通过观测 Metronome 的数据可以更精确地定位问题，比如到底是哪一个环节的收入降低了。

**•** **立足准确性，跑通商业模式，在行业里获得先发优势**

**在计费平台领域，客户最关注的就是准确性，**Metronome 精准抓住了准确性。创始人 Kevin Liu 认为今天的 SaaS 产品有三个和以往不同的部分，分别是数据、计费和反馈。在数据上，特别是在计费速度快、有复杂的价格模型时，公司需要了解用户在产品内部做什么，Metronome 更像一家基础设施公司，直接与公司的事件流集成，可以实时调整信息并计算指标，使得公司始终知道客户使用产品的情况。在计费上，Kevin Liu 坚定立足准确性，不允许出现任何差错。在反馈上，Metronome 已经有复杂的集成，Metronome 会运行这些复杂的集成来实现用户端到端的工作，Metronome 会实时查看数据、计费、导出数据到客户的其他系统。

得益于极强的准确性等因素，Metronome 的收入和客户数都在不断增加，且获得了包括 OpenAI 在内的大量头部公司作为自己的标志性客户，证明 Metronome 的商业模式已经跑通，且可利用标志性客户来进一步增大 Metronome 在按量计费领域的市场占有率，巩固先发优势。

**•** **两位创始人在计费领域非常专业，已有成功创业的经验**

Metronome 的两位创始人 Scott Woody 和 Kevin Liu 在计费相关领域经验丰富。二人之前创立的 Foundry 和 Predictive Edge 均与数据跟踪、动态计费相关，二人在 Dropbox 的工作也涉及定价计费，在对按量计费的痛点把握上也非常专业。

二人在创立 Metronome 之前都有过成功的创业经历，经验较为丰富，人脉广阔。Kevin Liu 自述 Metronome 的天使投资人很多都是两位创始人在 Dropbox 认识的人和之前创立的公司的投资人返回来投资。两位创始人对此次创业非常慎重，准备得非常充分。除了前文所说的之外，Kevin Liu 对董事会成员的选择也非常认真，确定一个董事会成员都需要打 30 多次问询电话，这已远超出了行业平均数量。

**风险与局限**

**•** **按量计费场景有限，会降低 Metronome 天花板和利润空间**

虽然按量计费有很多订阅制没有的优势，但订阅制几乎可以在所有计费场景使用，而按量收费通常只适用于业务较为单一或易于数据化的产品，比如发送邮件、短信等发送成功的次数，手机流量消耗的数量，大模型 token 消耗的数量等等，这也是 Metronome 客户群体集中于 AI 或者数据领域的原因之一。若按量计费场景无法全面普及到 SaaS 产品的所有计费模式中，那按量计费的行业空间会降低，Metronome 的天花板也会降低。而且随着客户拓展，按量计费涉及的数据处理会越来越多、越来越复杂，会对 Metronome 的利润造成压力。虽然 Metronome 目前为了获得更大量的客户，并不太在意自己的成本，但若要持续地发展，利润仍然是需要考虑的重要因素。

**•** **上下游软件、传统软件等的竞争会挤压 Metronome 生存空间**

按使用量计费领域的玩家众多，产品替代性高，Metronome 虽然准确性做得非常好，有客户认为部署 Metronome 的回报率非常高，但也要适当兼顾性价比，已有客户因 Metronome 收费较贵而转向其他竞品。而且若Metronome 无法将一线的数据积累到自己的平台上进行产品的迭代或者业务的拓展，形成数据壁垒，那可能会被努力转型的传统计费软件、向计费领域拓展的上下游软件、公司内部自建计费平台等竞争对手所吞并。

**07.**

**融资与未来发展**

**融资**

2024 年 1 月 31 日，Metronome 宣布已在 B 轮融资中筹集了超过 4300 万美元，由 NEA 领投，a16z 和 General Catalyst 跟投。New Relic 和 Salesforce 前总裁 Hilarie Koplow-McAdams 加入董事会。至此，Metronome 的融资金额超过 7800 万美元。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/024.png)

**发展与建议**

**•** **Metronome 计划完善销售团队来更好服务客户**

在 2024 年 6 月的公开采访中，Scott Woody 特别强调自己在建立 GTM 团队，之前主要是由创始人主导的销售，现在计划在未来四个季度加速 GTM 团队建设。Scott Woody 还强调了设计的重要，他自述人们并不认为计费是一个有吸引力的设计领域，但他就是要改变这种现状。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/025.png)

**•****建议**

**产品建议：可以进一步提高产品的灵活性**

1. 有用户反馈目前 Metronome 中计费的变化不是自动化的，即当用户签约、续约、追加销售或者设定新价格时，所有更改都需要在 Metronome 手动进行，而在理想情况下，签署某项变更协议后，这些信息会立即自动在 Metronome 中更改。

2. 对于 Metronome 没有计费类型的场景，目前是不能直接输入到 Metronome 中，必须手动执行 SQL 查询来计算所有内容，可通过继续丰富计费类型来提高灵活性。

3. 目前 Metronome 只与美国主要支付提供商以及少数欧洲支付提供商合作，若要提高在国际化领域的灵活性，Metronome 需要与拉丁美洲、亚洲等支付提供商进行合作。

**业务建议：尽快利用现有优势建立数据壁垒**

1. Metronome 可以尽快将一线数据积累到自己的平台，来迭代自己的产品，或利用定价信息为不知道如何定价的公司提供咨询服务等来开拓业务，从而实现在 Metronome 内部为客户提供计费计划，进一步从计费平台切入公司运行的各个环节。

2. Metronome 有潜力成为一家独立的公司，也有可能被收购。

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/026.jpg)

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/027.jpg)

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/028.png)

排版：Doro

延伸阅读

[![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/029.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510898&idx=1&sn=3b4e8babc8aa2b71b5c5681534e8ff89&scene=21#wechat_redirect)

估值13亿美金，Clay 用 AI Agent 帮企业找客户

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/030.png)

[![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/031.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510837&idx=1&sn=0519e620d90fc536a0140aee9b1fce70&scene=21#wechat_redirect)

Bolt.new：AI Coding 领域的 Figma，2 个月实现近千万美元 ARR

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/032.png)

[![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/033.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510791&idx=1&sn=23c60bf34dac2f4906d897fc6b7863e1&scene=21#wechat_redirect)

Abridge：AI Scribe 成为 AI 医疗应用的最佳实践

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/034.png)

[![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/035.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510746&idx=1&sn=c12a07bb6dfb69d1180d029bbd7c55be&scene=21#wechat_redirect)

AI Coding 最全图谱：Agent 将如何颠覆软件

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/036.png)

[![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/037.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510708&idx=1&sn=b0845873a87e9a344ee23c221d922214&scene=21#wechat_redirect)

Sora V2 即将发布，AI Creativity 赛道有哪些机会？

![](../images/2024-12-25-metronome-openai-anthropicbei-hou-de-ji-fei-ping-tai-hui-shi/038.png)
