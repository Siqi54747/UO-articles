---
title: Agent 重构互联网，谁将受益于线上内容的“帕累托效应”？｜AGIX PM Notes
publish_date: '2025-09-08'
publish_timestamp: 1757332800
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/OB3g1n4Gq0tN0I1gY8OX5g
msgid: 1000000414
appmsgid: 2247517695
itemidx: 1
digest: Reddit、 X 等内容平台也可以看成一个垂类索引数据库
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgyzpAJG2aubf2QCv5qdwCUFxTxc8N7v8HMbibXYIUm8rl31RzGlCrXshMwdWFyLPiarZ0ibqibEj4qJMQ/0?wx_fmt=jpeg
image_count: 17
archived_at: '2026-04-20T04:18:35+08:00'
---

[![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1)

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/002.png)

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/003.png)

AGIX 诞生于我们对“如何捕获 AGI 时代 beta 和 alphas”这一问题的深度思考。毫无疑问，AGI 代表了未来 20 年最重要的科技范式转换，会像互联网那样重塑了人类社会的运行方式，我们希望 AGIX 成为衡量这一新科技范式的重要指标，如同 Nasdaq100 之于互联网时代。

「AGIX PM Notes」是我们对 AGI 进程的思考记录，希望通过学习 Warren Buffett、Ray Dalio、Howard Marks 等传奇投资者们的分享精神，与所有 AGIX builders 一同见证并参与这场史无前例的技术革命。

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/004.png)

**PM Notes**

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/005.svg)

**AI 时代的 “80-20” 问题**

作者：Max

在本周 Google 垄断案的法律文件中，Duckduckgo 这种小型的搜索公司在作证中提到：谷歌索引的规模使其相对于现有的小型搜索公司拥有关键的竞争优势。对于 Duckduckgo 或者 ChatGPT 等新进入的竞争者，建立一个搜索索引（Index），导致能够回答 80%的查询问题，在资本投入的强度上较大，但是短到中期是可以实现的。但困难的是剩余的 20%的长尾查询，其非常具有挑战性，要求索引能够包含非常具体且晦涩的来源。因此法庭主张，Google 应该向合格竞争对手开放对谷歌搜索索引的访问，帮助解决 “80–20” 的问题。

通过披露每个网页的唯一文档 ID（DocID，标记出重复页面）、DocID 对应的 URL 映射、该 URL 首次被发现时间、最后一次抓取时间、垃圾信息评分（spam score）以及设备类型标记（区分桌面或移动），法院认为**强制披露这些数据是弥补谷歌排他协议造成竞争伤害的合理且相称的方法。**

**共享的索引信息极具价值，有助于缩小规模差距。** 通过获取这套数据，竞争者将“更快地建立起一个**在规模、实时性和有用性上都足够强大的搜索索引**”。例如，OpenAI 表示这些数据能让其**更快速地构建自身索引并提升产品质量**，苹果的 Eddy Cue 认为，数据披露将**加速竞争对手打造更大规模的索引数据库**，DuckDuckGo 创始人则称这将“**快速启动**”任何竞争对手大规模索引构建。

对于目前市场上的竞争者（如 Perplexity 等），这些数据同样是**宝贵的“情报”**。他们可以交叉对比自身索引，发现漏收录的重要网站或内容领域，从而迅速补全短板。尤其是在移动搜索、最新内容和垃圾内容筛除等方面，谷歌的数据可以帮助竞争者**弥补经验和数据不足**，提供更接近谷歌水准的用户体验。随之而来，搜索市场可能出现**更为多元化的格局**，谷歌一家独大的局面有所缓解。当然二级市场的重点仍然是关注 Google 免于分拆 Chrome 以及仍然能够得到苹果每年的天价付款，但行业格局已经在慢慢改变。

首先，搜索会否变得更去中心化，不同于以往一个巨头来提供互联网的基础设施，各类中小竞争者都可以来参与和分担？例如基于 Google 开放的索引，垂类的竞争者是否将通过垂直搜索，企业/行业自有知识库等，来维护**行业级“主索引”**。**并通过协议互联，将泛用搜索变为“路由层”**。监管对索引共享的推动，可能加速了这种“多源召回 和统一编排”架构的落地。

从另外一个角度看这个问题，Reddit、 X 等内容平台也可以看成一个垂类索引数据库，而他们已经成为了生成新的高质量 token 的工厂。如果把 Reddit 的 Token 数量和 New York Times 全部 context 的 Token 数量加起来，会发现两者在数量级上大致相当，但 Reddit 得到的（关注/使用）却是它的七倍。因为无论纽约时报还是华尔街日报，新闻 token 的熵往往大同小异，然而实际上正是那些本地的、独特的、有差异化的内容最有价值。而 AI 的编排和 reasoning 能力，恰恰是促进这部分长尾或颗粒度更细的信息更有效变现或者和需求更紧密无缝耦合的重要催化剂。这里的“长尾”因为搜索引擎的路由化，反而被激励或奖励开放，并且释放出了更高的价值。

而有了高颗粒度的供应和需求，是否就需要有相应的经济机制的建立来交换价值，尤其考虑到 Indexing 半开放后，Google 从内容的“守门员”一定程度上变为内容的数据基础设施服务商，各类答案引擎都可以基于统一数据做自己擅长的 Ranking/Answering。

Cloudflare 就在思考这个问题。在和 Perplexity 的 bot 攻防中展露了他们的野心。2025 年 6 月，Cloudflare 上线了“pay per crawl”服务，允许网站向 AI 公司收取爬取内容的费用，默认屏蔽绝大多数 AI 爬虫，需获得许可后方可访问。Cloudflare 的主张是，传统互联网内容商业模式（Google 为代表）一直依赖“流量”来实现各方价值交换。创作者免费上传内容，Google 为创作者带来曝光和流量，进而变现（通常是广告）。而 AI 让这个价值循环被破坏了，进而也会破坏为互联网贡献免费内容的动力。

Cloudflare 尝试**作为中立做市商**：Cloudflare 可以为 AI 内容索引、付费抓取（Pay-per-crawl）、数据“token”交易等提供底层交易撮合。比如 AI 公司想抓取内容，内容原作者想标价、限流或分成，Cloudflare 能够作为“内容 API/Token 流量的做市平台”来保障透明和公平。这样的话，内容生产者可以设定抓取/引用价格，AI 答案引擎（如 OpenAI、Perplexity）通过 Cloudflare 完成准入、计费、清算分成。这样既防止滥用/灌水，也让优质内容获得可持续收入。Cloudflare 有强大的分发、计量、结算、API 限速和身份认证等能力，天然契合“内容市场”和数据商品化的场景。

但同时，我们也应该警惕 Cloudflare 谋求成为新的数据寻租层，可能更好的方式是向 Crypto 市场的交易机制学习。Pay-per-crawl/token 无法解决数据质量的问题，就像在各个号称高质量的数据源前架起收费站，而最终发现数据质量根本不值得去爬取。反而是 Crypto 的 Gas Fee 有借鉴之处，当一个数据源的质量越高，愿意来爬取的 Bot 或 Agent 就会越多，可以通过“拥堵费”的形式，让真正高质量的内容得到市场的激励。

在信息的 80-20 以外，商品和服务层面都有可能展开 80-20 的重构。**80%标品**可能会被聊天分发“基础设施化”。例如任何有对话能力的聊天入口都可以成为标品的**分发器**，把独立站与平台货源动态拼装进入对话，压缩传统电商在这部分的 take rate；尤其是由于单轮推荐位稀缺（1–5 个），排序会自然偏向“高点击/低退货/强口碑”的头部 SKU。而 **20%长尾**则从“库存驱动”转向“UGC/AGC 驱动”：创作者与小商家提交“可生产的描述”（prompt＋BOM/打样文件），由按需制造与小批量履约承接，可能形成“微品牌—微社群—微供应链”的自洽飞轮。

在服务层面，**80%标准化软件**会被模型原生能力吞并为“免安装的功能层”。真正产生溢价的是那 20%定制化：每个客户利用 AI 的变成能力而进行软件定制化，企业也可以将自身流程与数据映射成可复用的配方/脚本（recipes）与“数字孪生”，进行运营软件化，由 AI 将通用基座组合成每家企业独有的 Micro-SaaS；软件不会迎来快时尚时代，而是乐高时代。这些模块可以像 UGC 一样被发布、交易与复合，平台提供可审计执行环境（微隔离 / micro-VM）、观测与结算，并按结果/节省的人工时分润。由此，服务行业的“长尾”从人力外包变为知识与流程的可交易资产，持续复利。

在 AI 分发与路由化之后，“80%”会被做成低摩擦、可互操作的公共底座；“20%”则演化为**高颗粒度、可质押、可复用**的 UGC/AGC 商品与配方市场。我们也期待看到越来越多的组合公司按类似的思路进行业务演进。

**01.**

**本周市场总结**

**北美与欧洲活跃度上升，中国需求放缓**

夏季最后几个月的买盘在九月初似乎暂停，基金略微转向小幅抛售股票。但更值得注意的是，总体交易活跃度明显上升，主要由欧洲和北美股票驱动，基金在投资组合中增加了多头和空头敞口。在收益方面，尽管全球股指仅录得小幅上涨，基金收益却更为平淡。平均全球对冲基金本周截至周四仅上涨约 8 个基点，美洲 L/S 基金仅上涨约 4 个基点。其他地区基金收益同样温和，欧州基金平均上涨约 1 个基点，而亚洲基金则下跌约 10 个基点。

从资金流向来看，北美为净卖出最多的地区，但规模极小（仅约 0.2 z-score 卖出事件）。在行业层面，金融板块抛售居前，其次为科技和房地产——ETF 同样呈净卖出，显示基金在指数级对冲方面大幅加仓。从更细分的行业角度来看，软件行业净卖出居首，其次为 HMO、银行、保险及住宅建设——值得注意的是，相较于其在美国股指中的权重，软件板块的看空仓位仍为近年来最高水平，近期基金抛售进一步加速。

另一方面，基金继续加仓工业板块，与八月的买入趋势一致。工业板块的买入主要来源于多头增加，几乎所有子行业本周均呈净买入（唯一例外为机械行业）。此外，能源（综合油气、勘探生产）、日用品（分销零售、饮料）和通信服务（互动媒体与服务）同样呈净买入。从因子角度看，流向略显温和，但我们观察到基金偏好买入“质量”和“大盘”因子，同时抛售“流动性”因子。

在其他地区，净流向整体较弱，欧洲、亚太（日本除外）和日本均无地区出现超过 0.1 z-score 的买卖。三地中，欧洲股票的总加仓幅度最大，而亚太整体流动相对温和。欧洲板块净流向同样平淡，但对欧股科技板块的买入需求仍较强，而房地产则呈明显看空态势。欧股科技板块中，软件与半导体均呈净买入，与八月下半月的需求趋势一致。在亚太地区，中国市场（尤其 A 股）的强劲买盘在过去 3-4 个月后本周明显放缓，甚至出现卖出。这些抛售主要来自此前需求最旺的板块——工业、医疗和金融。H 股的增仓兴趣有限，且规模不大（周环比略低于 1 z-score）。日本市场交易活跃度轻微，无论总量还是净流向均低迷。基金小幅买入公用事业、非必需消费和科技板块，同时抛售工业和通信服务。

**对冲基金表现优异，AGIX 大幅跑赢美股主要指数**

从表现来看，本周对冲基金相对主要指数表现良好，主要得益于北美拥挤多头及部分空头的收益贡献。AGIX 上涨 2.76%，明显跑赢三大美股指数：S&P 500 上涨 1.03%，QQQ 上涨 1.85%，道琼斯上涨 1.03%。在北美，拥挤多头对超额收益贡献明显，最拥挤多头较最拥挤空头超额约 1.2%，推动了相对收益的重要部分。

盈利方面，平均全球基金本周收益约 35 个基点，调整 beta 后超过标普 500 约 103 个基点的涨幅；全球 L/S 基金收益接近 50 个基点。地区层面，美洲 L/S 基金约获 40 个基点，欧洲 L/S 基金约获 30 个基点，亚洲 L/S 基金约获 45 个基点，尽管各区域指数表现不一。凭借本周的强势表现，平均全球基金本月迄今收益为 +1.8%，年初至今收益为 +8.5%。按地区拆分，美洲 L/S 基金年初至今 +7.9%，欧洲 L/S 基金 +11.8%，亚洲 L/S 基金 +12.4%。

**02.**

**AI Alphas**

**谷歌反垄断案结果出炉：法院不强制谷歌出售 Chrome 浏览器，Alphabet（GOOGL）股价飙升**

周三，Alphabet 股价上涨超过 8%，此前美国哥伦比亚特区联邦地方法院法官 Amit Mehta 于周二晚间裁定，谷歌无需出售其 Chrome 浏览器，称剥离业务“不恰当”。这是一起具有里程碑意义的反垄断案件。Mehta 法官的裁决指出，谷歌需要共享帮助其维持搜索垄断地位的数据，但避免了可能的最严厉惩罚措施。

裁决还允许谷歌继续向“分销合作伙伴支付费用，以预安装或安装 Google 搜索、Chrome 或 GenAI 产品”。这意味着谷歌可以继续每年向苹果 （AAPL） 支付约 200 亿美元，以换取苹果在 Safari 浏览器和 Siri 中使用 Google 搜索作为默认搜索引擎。受此利好消息影响，苹果股价周三上涨近 3%。

**OpenAI 预计到 2029 年现金消耗 1150 亿美元**

据 The Information 周五报道，OpenAI 大幅上调其到 2029 年的现金消耗预期至 1150 亿美元，以支持其流行 ChatGPT 聊天机器人背后的人工智能技术。这一预测比此前预期高出 800 亿美元。该报道未透露消息来源。OpenAI 作为全球最大的云服务器租赁方之一，预计今年现金消耗将超过 80 亿美元，比年初预期高出约 15 亿美元。

为控制迅速上升的成本，OpenAI 将寻求开发自有数据中心服务器芯片和设施。据 Financial Times 报道，OpenAI 将于明年与美国半导体巨头 Broadcom （AVGO） 合作生产首款人工智能芯片，并计划内部使用，而非面向客户销售。

此外，OpenAI 在 7 月加深与 Oracle （ORCL） 的合作，计划建设 4.5 GW 数据中心容量，延续其“星际之门（Stargate）”项目（总投资可达 5000 亿美元、容量 10 GW），该项目还包括日本科技投资者软银集团。OpenAI 还将新增 Google Cloud 为计算能力供应商。The Information 表示，公司明年现金消耗将翻倍至超过 170 亿美元，比此前预期高出 100 亿美元，2027 年为 350 亿美元，2028 年为 450 亿美元。

**AGIX 覆盖公司 AppLovin（APP） 将被纳入 S&P 500 指数**

美国广告技术公司 AppLovin 和线上证券交易平台 Robinhood Markets 的股价在上周五盘后交易中均上涨约 7%。此前，S&P 500 宣布，两家公司将被纳入 S&P 500 指数。

根据 S&P 的声明，这一调整将在 9 月 22 日开盘前生效。届时，AppLovin 将取代 MarketAxess Holdings，而 Robinhood 将取代 Caesars Entertainment。

**受益于 Q3 出色表现及 OpenAI 合作，分析师上调 Broadcom （AVGO） 目标价**

9 月 4 日，Broadcom 公布 2025 财年第三季度财报。公司营收同比增长 22%，达到 159.5 亿美元。Broadcom 总裁兼 CEO Hock Tan 预计下一季度 AI 半导体营收将达到 62 亿美元。

Broadcom 与 OpenAI 签署了一项 100 亿美元合作协议。在财报电话会议中，Tan 表示公司与 OpenAI 达成协议，为其构建 AI 加速器。该客户承诺基于 Broadcom XPU 订购超过 100 亿美元的 AI 机架。虽然 Broadcom 未透露客户身份，但 Financial Time 确认该新客户为 OpenAI。

**Samsara （IOT） 财报超预期，股价上涨 17.4%**

Samsara 连续第三日上涨，周五股价飙升 17.44%，收于 42.09 美元，原因是财报表现亮眼，并上调全年增长预期。财报显示，公司净亏损从去年同期的 4961 万美元缩小至 1680 万美元，同比下降 66%。营收同比增长 30.49%，达到 3.9148 亿美元。

受此影响，Samsara 将全年营收增长预期上调至 15.74 亿至 15.78 亿美元，高于此前预期的 15.47 亿至 15.55 亿美元，同比增长约 26%。

**Microsoft （MSFT） 表示红海海底光缆中断影响 Azure 云服务**

Microsoft 周六表示，由于红海多条海底光缆中断，Azure 用户可能面临延迟增加。公司在 Azure 系统更新状态中称，用户在中东交通路由上可能会出现服务中断。

为应对中断，Azure 已通过备用网络路径重定向流量，网络交通未受影响。Azure 是全球第二大云服务提供商，仅次于亚马逊 AWS。

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/006.png)

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/007.png)

排版：傅一诺

延伸阅读

[![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/008.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517618&idx=1&sn=8ef705bde94b9aed8e1dee764a89479a&scene=21#wechat_redirect)

Temporal：Nvidia、OpenAI 都在用，为什么 Agent 还需要专门的长程任务工具？

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/009.png)

[![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/010.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517552&idx=1&sn=0fcc3988e2c9ed1aacc24cf678f91571&scene=21#wechat_redirect)

企业数据“LLM ready”与“小Palantir”们的崛起 ｜ AGIX PM Notes

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/011.png)

[![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/012.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517523&idx=1&sn=49485604220ec400efe1bff17ecdfb7c&scene=21#wechat_redirect)

AI 叙事重塑科技投资，市场 Hype 中如何识别真正的 AI Winners？｜AGIX 年度回顾

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/013.png)

[![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/014.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517480&idx=1&sn=3f682da7c82b1483a6b3c1674c459e8f&scene=21#wechat_redirect)

8 个月营收提高 4 倍，n8n 为什么是 AI Agent 最受欢迎的搭建平台？

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/015.png)

[![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517328&idx=1&sn=6bc1fea7dc6c863197dcb584023cd89b&scene=21#wechat_redirect)

LLM 商业化猜想：OpenAI 会走向 Google 的商业化之路吗？｜AGIX PM Notes

![](../images/2025-09-08-agent-zhong-gou-hu-lian-wang-shui-jiang-shou-yi-yu-xian-nei/017.png)
