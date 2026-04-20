---
title: 软件的新玩法：如何 Fork 一个技能库｜AGIX PM Notes
publish_date: '2025-10-27'
publish_timestamp: 1761566400
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/JqXOWaQxHdhXVVXmqP_vhg
msgid: 1000000444
appmsgid: 2247518919
itemidx: 1
digest: 功能即技能，技能即软件
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzCQEaAVy8szwgRC8OOcSha1UD6oib7O2Ejg1fPB7enibziciaBA8a9whjEJR9snH6Wicdokx9iaAyxHXBw/0?wx_fmt=jpeg
image_count: 17
archived_at: '2026-04-20T04:37:46+08:00'
---

[![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/002.png)

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/003.png)

[AGIX 指数](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=3570724992708624387&scene=21#wechat_redirect)诞生于我们对“如何捕获 AGI 时代 beta 和 alphas”这一问题的深度思考。毫无疑问，AGI 代表了未来 20 年最重要的科技范式转换，会像互联网那样重塑了人类社会的运行方式，我们希望 AGIX 成为衡量这一新科技范式的重要指标，如同 Nasdaq100 之于互联网时代。

「AGIX PM Notes」是我们对 AGI 进程的思考记录，希望通过学习 Warren Buffett、Ray Dalio、Howard Marks 等传奇投资者们的分享精神，与所有 AGIX builders 一同见证并参与这场史无前例的技术革命。

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/004.png)

**PM Notes**

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/005.svg)

**How To Fork a Software**

作者：Max

本周在看了 Claude Skills 的 PDF Skill.md 文件后，有一种奇特的感觉。所有传统软件上的菜单，比如 PDF 编辑软件中的添加水印，PDF 转文字，加密码保护等等常用功能都变成了 Markdown 文件，平铺直叙的在 Skill.md 中供 LLM 来阅读调用。我们究竟是从面向人的软件，向着面向机器的软件又前进了一步。目前的 Skills repo 已经包括了 Canva， Slack， Documents 等等模块。添加 Skills 的方式也非常像我们在 LLM 电脑上安装了一个程序，而这个“程序”完全是 In Context 的，和 LLM“系统”本身具有高度互感知和互操作的特性，或者说让 LLM 具备了一定的工具使用直觉。

在之前的 PM Notes 里我们提到过，传统的软件或者是 system of record 或者 system of engagement， 是一个拥有良好界面的数据库前端。软件商业模式的优势也来源于此，它得以几乎 0 边际成本的分发，因为软件本身基本是个“死”系统。但作为一个 system of intelligence，软件将会变成 living software， 是一个护城河建立在“学习”而非“代码”基础上的，能够自适应用户 Context 的 Ambient agent。Skills 紧密贴合了这个范式。我们来到了功能即技能，技能即软件的时代。

在传统软件之上加载一个 Agent layer，让过去的软件仍然是独立存在的软件但只不过更“智能”的方向可能是错的。而一个软件，重新消解成为面向 LLM 的 skill.md 文件，并且将需要调用的“功能”和“模块”更好的向着 LLM 来暴露的方式已经越来越显著。软件也需要越来越降级为更贴近 Infra 的存在，怎么保障核心功能的安全，稳定。而这种范式下，规模效应的作用会远大于个性化的设计和功能，会让软件的市场集中度越来越高，也许也会出现技能库共享与企业标准化带来的新型“智能基础设施”商业范式。

但应该怎么理解 Skills 是一个 Living Software 的范式？Claude Skills 本质上是一组可组合、可重复利用的小技能或推理模块，可理解为“不同 Constitution AI 的集合”或“不同原则模块”，被调用来完成复杂、多变的任务。想必熟悉 Claude 演进历史的朋友对 Constitutional AI 都不陌生。Constitutional AI 是 Anthropic 为 Claude 打造的训练方法，通过预定义的一套“原则”（Constitution）指导 Claude 的行为和输出。这些原则通常是安全、善良、诚实等抽象价值观，贯穿模型训练和推理环节，用于约束和监督大模型行为，类似“AI 版宪法”。 

而从强化学习的视角来看，RL 的一个关键挑战是为 LLMs 在可验证问题或人为规则之外的各类领域获得准确的奖励信号。高质量的奖励在特定领域主要来自具有明确条件的人为设计环境或来自可验证问题的手工规则，例如数学问题和编码任务。在通用领域，奖励生成更具挑战性，因为奖励标准更加多样且复杂，且通常没有明确的参考或真实答案。因此，通用奖励建模对于提升 LLMs 在更广泛应用中的表现至关重要，无论是从后训练的视角（例如大规模的强化学习），还是从推理的视角（例如由 RM 指导的搜索）。

对于通用领域，有些研究探索过采用原则来指导奖励生成以代替人工规则。而面向 LLMs 的原则最早在 Constitutional AI 中提出。传统 Constitutional AI 里，原则通常是"hand-crafted criteria"（完全由人规定），指导奖励模型或安全评估。假如有一种机制则允许模型自适应生成原则，而不是仅依赖人工输入。原则成为了奖励生成的一部分，能根据不同任务、数据分布自动调整和扩展。例如 Deepseek GRM 里的方法，模型每次生成一组原则，然后根据这些原则对 LLM 输出做评价，再通过 Pairwise（如投票、排序、加权）和 MetaRM 筛选低质量原则/技能，保留高效的原则，实现“技能库”的在线筛选和自举。

Claude Skills 里面的这些模块就有点像早期的 constitutional AI 以及刚才提到的“原则”。虽然 SPCT，Constitutional AI 这些方法目前主要在 RM/对齐研究，与 Claude Skills 的工程产品层尚处“可迁移/待结合”的阶段。往前看，Claude Skills 这种目前还是由人类设计和规定的“原则（Constitutions/skills）”，在理论上，模型也可以通过自生成原则，并和 Skills 库中的“规定原则”进行比较、配对（Pairwise），再利用 SPCT 等方法实现这些“技能”的在线学习和逐步进化。这时，就会出现我们畅想的 Living Software。

此外，MCP 当时的概念还是建立一种客户端/服务器关系，需要通过标准化协议来连接不同的数据源和工具。而 Claude Skills 则有“更近端、更受控的执行边界”，这种架构上的差异揭示了两种截然不同的软件演进路径。Claude Skills 的技能组装方式更像是软件的基因库，通过不断的变异、选择和进化来适应环境，而非传统软件那种固定的硬编码或者无可组合性的状态。

这也许就是"How to Fork a Software"的新答案：不再是复制代码仓库，而是 Fork 技能库（skill.md 文件）。当一个 PDF 编辑软件被"Fork"时，我们复制的不是 GUI 代码和底层逻辑，而是一组可被 LLM 理解和重组的技能描述。这些技能可以被任意组合、修改、扩展，就像乐高积木一样。更重要的是，这些被 Fork 的技能会在使用中持续进化。通过自生成原则和 SPCT 等方法，模型会自动筛选高效技能、淘汰低质量原则，实现技能库的自我优化。

**01.**

**本周市场总结**

**全球去杠杆延续，美国动能交易承压，科技与可选消费成主要调整方向**

上周全球股票市场延续两周前的去杠杆趋势（de-grossing），主要由北美市场主导。尽管主要股指继续温和上行，但因子层面波动明显，尤其是动能（Momentum）因子在美洲市场承压，成为本轮仓位调整的核心驱动。美国多空基金连续第二周出现总杠杆回落，周环比下降约 1 个百分点至 216%，但仍位于过去十年高位区间（历史 100 分位）；与此同时，净杠杆因空头回补上升 2 个百分点至 58%，触及近三年新高。

从仓位结构看，本轮调整以空头回补为主，部分伴随轻微的多头削减。行业层面，科技与可选消费成为主要调整方向。基金在科技板块中集中回补软件股，尤其是与人工智能相关的 AI 软件与 SaaS 公司，但在整体仓位偏高的背景下，增配意愿仍然有限。半导体板块中，Analog 类个股被显著减持，而 AI 赢家相关半导体股票则保持稳定。无盈利科技股继续遭到削减，显示投资者在高波动环境下对高风险资产的回避情绪仍强。可选消费中，餐饮与零售类公司受到更多卖压。医疗保健板块则分化明显，基金增持非商业化生物科技个股，同时削减制药与 HMO 曝险。

欧洲市场方面，上周整体呈现轻微净卖出，去杠杆节奏相较两周前明显放缓。仓位调整主要表现为空头回补与有限的多头削减，软件与奢侈品行业为回补重点，银行、矿业及防务板块出现一定规模的多头削减。当前欧洲市场的去杠杆仍处于早期阶段，未达到近年历史回调周期的幅度。亚洲市场整体保持谨慎，日本成为主要去杠杆来源，卖盘集中于科技与工业板块，而亚太（除日本）地区成交清淡，基金在台湾市场减持的同时，小幅加仓中国股票。

从杠杆结构来看，美国多空基金净杠杆上升至 58%，创近三年高点，而总杠杆虽略有下降但仍维持高位。欧洲与亚洲的杠杆水平变化有限，欧洲净杠杆环比上升 2 个百分点至 47%，亚洲持平于 68%。总体而言，全球基金继续削减方向性风险，但调整规模相对温和，尚未出现系统性去杠杆迹象。

**全球对冲基金表现稳健，美欧领跑，亚洲小幅回撤**

尽管因子波动加大，上周全球对冲基金整体表现稳健。截至 10 月 23 日，全球基金平均上涨约 50 个基点，收复两周前部分跌幅，表现与主要股指走势一致。美洲与欧洲基金分别上涨约 50–70 个基点，亚洲基金略有下跌约 30 个基点。月度来看，全球多空基金已转为正收益，月内上升约 20 个基点（MSCI ACWI +1%）。

年初以来，全球多空基金上涨约 9.6%，其中美洲地区表现领先，累计上涨 11.1%，欧洲上涨 9.4%，亚洲上涨10.5%。从行业与风格表现来看，动能与波动率因子仍承压，而成长与质量因子表现相对稳定。北美市场的空头回补推动净杠杆回升，同时改善了基金短期收益率；欧洲基金维持稳健节奏，受益于防务与奢侈品板块支撑；亚洲基金则因日本与中国市场波动而略有回撤。

从拥挤交易表现来看，北美 Top 50 多头相对空头上周超额收益持平（WTD 0%），年内累计收益约 15.7%；欧洲与亚洲分别为 25.8% 与 12.2%。这一结构显示全球资金在动能回调环境下继续保持高集中度，但资金流呈现谨慎态势，尤其在高波动板块中更倾向于减少方向性风险敞口。整体来看，对冲基金在动能调整阶段继续优化仓位，美国去杠杆主线延续，欧洲维持稳健，亚洲略显承压。

**02.**

**AI Alphas**

**Netflix 全面押注生成式 AI：提升制作效率，平衡创意与权益担忧**

在娱乐行业对生成式 AI 应用仍存分歧之际，Netflix 在最新季度财报中明确表态将全力押注 AI 技术。Netflix CEO Ted Sarandos 在业绩电话会议上强调，AI 不会自动造就优秀的故事讲述者，但能为创意人员提供更好的工具，提升影视内容的制作效率。该公司已在多部作品中实践 AI 应用：阿根廷剧集 *The Eternaut*使用 AI 生成建筑坍塌场景，*Happy Gilmore 2*利用 AI 实现角色年轻化效果，*Billionaires' Bunker*则将其用于服装和场景设计的预可视化。尽管行业对 AI 替代创意工作的担忧持续升温，特别是 OpenAI 发布 Sora 2 音视频生成模型后引发演员权益争议，Sarandos 向投资者保证 Netflix 不担心 AI 取代创造力。财报显示，Netflix 季度营收同比增长 17%至 115 亿美元，但未达公司预期。

**Anthropic 推出 Claude Code 网页版：面向订阅用户开放，年化收入超 5 亿美元**

Anthropic 上周一正式推出网页版 Claude Code，将其爆款 AI 编程助手从命令行界面扩展至浏览器环境。该产品现面向每月 20 美元 Pro 计划及 100-200 美元 Max 计划订阅用户开放，用户可通过 claude.ai 网站或 iOS 应用访问。自 5 月大规模推出以来，Claude Code 用户量增长 10 倍，年化收入贡献超 5 亿美元，成为当前最受欢迎的 AI 编程工具之一。产品经理 Cat Wu 透露，90%的 Claude Code 产品代码由公司 AI 模型自主编写，工程师角色正从编码者转向 AI 助手管理者。尽管面临微软 GitHub Copilot、Cursor、Google 和 OpenAI 等竞争对手的激烈角逐，Anthropic 仍持续推动 AI 编程代理发展，CEO Dario Amodei 预测 AI 即将为软件工程师编写 90%的代码。不过研究显示，部分工程师使用 AI 编程工具后效率反而降低，主要因等待 AI 响应及处理复杂代码库中的错误输出耗时增多。

**Oracle 发布 AI Database 26ai：数据库即 AI 引擎，一行 SQL 实现语义检索**

甲骨文公司正式发布 Oracle AI Database 26ai 版本，标志着其数据库产品全面转向 AI 原生架构。该版本在原有 23AI 版本基础上，通过季度补丁实现无缝升级，将 AI 能力深度集成至数据库全栈——包括事务处理、查询优化、应用开发及数据治理等核心层。新版本嵌入了 AI 向量技术、大语言模型集成及自动化检索增强生成功能，用户仅需单行 SQL 指令即可实现跨关系型、空间、文档、图数据等多模态数据的语义搜索与智能分析。技术架构上，甲骨文将隐私保护机制植入数据库底层，确保 AI 模型仅能访问终端用户授权数据，有效解决金融、医疗等敏感行业的合规需求。据数据库技术执行副总裁 Juan Loaiza 透露，本次升级涵盖超百项 AI 专项，通过统一 AI 架构显著降低企业多工具管理复杂度。

**AI 工厂全速推进：云算力大单、数据中心投资与并购潮并行**

尽管市场对 AI 泡沫的担忧日益加剧，AI 基础设施投资仍保持强劲增长态势。上周 Anthropic 与谷歌达成价值数十亿美元的云服务协议，获得百万 TPU 访问权限；Crusoe 融资 13 亿美元加速 AI 数据中心建设；Uniphore 从英伟达、Snowflake 等公司获得 2.6 亿美元投资。OpenAI、甲骨文和 Vantage 宣布在威斯康星州共同建设价值超 150 亿美元的数据中心园区。与此同时，Meta 裁减 600 名 AI 员工以精简超级智能实验室部门。高盛预测到 2027 年 AI 将颠覆就业市场并重构全球商业格局，而数百名 AI 专家联名呼吁暂停 AGI 研发。在网络安全领域，Veeam 以 17 亿美元收购 Securiti，Dataminr 以 2.9 亿美元收购 ThreatConnect，行业整合趋势持续。亚马逊展示将 AI 与机器人、智能眼镜融合的物流技术，强调增强而非取代人力。

**Vibes 上线后，Meta AI 日活跃达 270 万、下载量激增**

市场情报提供商 Similarweb 最新分析显示，Meta AI 移动应用在推出'Vibes'AI 视频功能后用户数据显著增长。截至 10 月 17 日，该应用在 iOS 和 Android 平台的日活跃用户激增至 270 万，较四周前的 77.5 万大幅提升。同时，每日新增下载量达到 30 万次，高于几周前的不足 20 万次，而去年同期日下载量仅为 4000 次。值得注意的是，在 Meta AI 用户增长 15.58%的同时，ChatGPT、Grok 和 Perplexity 等竞争对手的日活用户分别下降了 3.51%、7.35%和 2.29%。分析师认为，OpenAI 视频生成器 Sora 的邀请制访问限制可能促使部分用户转向体验 Meta AI 的替代方案。

**Google AI Studio 引入“氛围编程”：自然语言生成并一键部署应用**

Google 宣布在其 AI Studio 应用开发平台中集成“氛围编程”体验，通过自然语言提示快速生成功能性应用程序。本次更新新增应用画廊、模型选择器、秘密变量存储及模块化“超能力”功能，支持一键部署至 Google Cloud Run。此举被视为对 OpenAI 的 GPT-5-Codex、Anthropic 的 Claude Sonnet 4.5 及 Salesforce 的 Agentforce Vibes 等竞品的直接回应。业内推测 Google 即将发布 Gemini 3.0 大模型，匿名测试平台 LMArena 近期出现的“lithiumflow”和“orionmist”模型被指可能是其预发布版本。Google 云首席执行官 Thomas Kurian 强调公司坚持平台优先的 AI 战略，通过高度集成生态降低技术门槛。

**Adobe 推出 AI Foundry：企业可定制品牌化 Firefly 模型，合规输出更可控**

Adobe 正式推出 AI Foundry 服务，为企业客户提供定制化生成式 AI 模型创建能力。该服务基于 Firefly 基础大模型系列，通过"深度调优"技术将企业的知识产权和品牌资产直接整合到模型架构中，而非传统的微调方式。Adobe 生成式 AI 业务副总裁 Hannah Elsakr 强调，这种方法能确保输出内容高度符合品牌视觉识别系统，包括特定色调、字体和图像风格。服务采用按使用量计费模式，区别于传统的席位定价。Constellation Research 分析师 Liz Miller 指出，该方案特别适合迪士尼、Netflix 和派拉蒙等拥有多品牌体系的大型企业，能有效管理跨市场、多格式的大规模内容需求。Firefly 模型完全基于授权数据训练的特性，为企业规避了 AI 版权风险提供了保障。

**OpenAI 收购 Mac 平台 AI 界面 Sky：推进跨应用代理与桌面自动化**

OpenAI 上周四宣布已收购 Mac 电脑 AI 自然语言界面 Sky 的开发商 Software Applications。此次收购旨在将 OpenAI 技术深度嵌入以 Mac 为基础的消费者日常生活和企业运营中。Sky 是一款未公开上市的软件，能够实时查看用户屏幕内容并在应用程序中代为执行操作，涵盖写作、规划、编码等场景。值得注意的是，Sky 团队核心成员曾开发 Workflow 并将其出售给苹果，该技术后演变为系统功能“快捷指令”。尽管苹果计划明年推出 AI 增强版 Siri，并与 OpenAI 合作将部分查询转至 ChatGPT，但其注重隐私保护的策略可能延缓类 Sky 系统的屏幕监控功能开发。根据 Pitchbook 数据，被收购方曾融资 650 万美元，投资者包括 OpenAI CEO Sam Altman。本次交易由 ChatGPT 负责人 Nick Turley 和应用业务 CEO Fidji Simo 主导，并经 OpenAI 董事会批准。

**SAP Q3 业绩稳健：营收与利润增长，云收入小幅低于预期**

SAP SE 公布第三季度业绩显示，尽管云收入略低于预期，但整体表现强劲。总营收达 105.3 亿美元，同比增长 11%，符合分析师预期；运营利润增长 15%至 29.8 亿美元，净利润飙升 29%至 21.5 亿美元。调整后每股收益 1.84 美元，超出市场预期的 1.73 美元。核心云业务收入增长 27%至 61.3 亿美元，虽略低于 61.7 亿美元的预期，但已连续五个季度保持超 25%增长，占总营收比例从 51%提升至 58%。云 ERP 套件收入增长 31%至 53.3 亿美元，当前云积压订单增长 27%至 218.5 亿美元，预示未来订阅收入潜力。可预测收入占比提升至 87%，传统软件许可销售下降 43%。CEO Christian Klein 强调 AI 代理已全面融入业务流程，并引用 IDC 研究称 SAP 增速较市场整体快 10 个百分点。公司维持 2025 年增长展望，并将运营利润指引上调至原区间上限 119.5-123 亿美元。

**03.**

**ETF 101**

**ETF vs 指数基金：被动投资的双轨逻辑与选择艺术**

在被动投资成为主流的今天，ETF（交易型开放式指数基金）与传统指数基金共同构成了投资者追踪市场指数的两大基石。它们虽共享“跟踪指数”的基因，但在交易方式、成本构成和适用场景上存在根本性差异。理解这些差异，是投资者根据自身资金状况、交易习惯和投资目标，做出精准选择的决定性一步。

**一、ETF 与指数基金的本质区别**

**•**ETF：交易所内的“指数股票”。它在二级市场像股票一样实时交易，价格随供需瞬息万变，具备高流动性和灵活性。

**•**指数基金：按净值申赎的“场外工具”。它每天只以一个价格（收盘后计算的基金净值）完成一次申购或赎回，操作简单，更适合定期、定额的长期投资。

**二、核心差异的三重维度解析**

1. 交易机制：实时价格 vs 每日净值

**•**ETF 的盘中博弈：ETF 的价格在交易时间内持续波动，投资者可以随时响应市场变化进行买卖，甚至进行短线交易或套利。这种特性使其成为交易型工具。

**•**指数基金的“一日一价”：无论一天中市场如何起伏，投资者都只按下午三点收盘后确定的净值成交。这消除了日内择时的干扰，是定投和长期配置的理想模式。

2. 成本结构：显性费用 vs 潜在摩擦

**•**ETF 的成本透明性：主要成本是极低的管理费和交易时的券商佣金，通常没有申购赎回费。其独特的实物申赎机制也有助于控制跟踪误差，保持成本优势。

**•**指数基金的隐性成本：虽然管理费也较低，但通常高于同类 ETF。此外，申购费和赎回费（尤其在持有期较短时）是常见的成本陷阱，频繁操作会显著侵蚀收益。

3. 投资门槛与资金效率

**•**指数基金的普惠性：场外指数基金门槛极低，十元甚至一元即可起投，让小额资金也能轻松参与市场。

**•**ETF 的整手交易：在交易所按“手”买卖，入门资金取决于单份净值与整手倍数。对于资金量小的投资者，可选择单位净值较低的 ETF，或通过其场外“替代品”——ETF 联接基金来间接投资。

**三、选择策略：如何让工具匹配你的投资蓝图**

**•** 明确你的投资画像

1）如果你是交易者或希望灵活配置：需要盘中交易、行业轮动或希望成本极致透明，ETF 是你的不二之选。

2）如果你是长期定投者或追求省心省力：希望通过定期定额平滑成本、强制储蓄，且不愿被日内波动干扰，传统指数基金更具优势。

**•** 长期视角下的关键指标：对于长期持有而言，微小的费率差异在复利作用下会形成巨大收益差别。因此，在二者间选择时，总费率（管理费+托管费等） 和跟踪误差是比短期交易便利性更应优先考量的因素。

**•**利用互补性：两种工具并非互斥。完全可以在核心仓位上用指数基金进行长期定投，同时用少量资金通过 ETF 进行灵活的战术补充。

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/006.png)

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/007.png)

排版：夏悦涵

延伸阅读

[![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/008.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518893&idx=1&sn=d97353a4eaff11bf3a12a3712ca328db&scene=21#wechat_redirect)

RL 是新的 Fine-Tuning

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/009.png)

[![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/010.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518860&idx=1&sn=033bb7b4db2d36c742d68acaf4218dd0&scene=21#wechat_redirect)

SemiAnalysis 创始人解析万亿美元 AI 竞争：算力是 AI 世界的货币，Nvidia 是“中央银行”

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/011.png)

[![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/012.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518822&idx=1&sn=d6b378e1e41e739fe132926b3cd4565f&scene=21#wechat_redirect)

告别 260 亿美元低效投入，HappyRobot 为物流业配置 “AI 调度员”

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/013.png)

[![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/014.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518724&idx=1&sn=085e7c34d814da5741c9bf75d10de03a&scene=21#wechat_redirect)

GPT-5 核心成员详解 RL：Pre-training 只有和 RL 结合才能走向 AGI

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/015.png)

[![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518657&idx=1&sn=c5e5643910ca4c9669df786bc4d65280&scene=21#wechat_redirect)

Palantir 创始工程师深度分享：FDE 模式是 Agent 时代的 PMF 范式

![](../images/2025-10-27-ruan-jian-de-xin-wan-fa-ru-he-fork-yi-ge-ji-neng-ku-agix-pm/017.png)
