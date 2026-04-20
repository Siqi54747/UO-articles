---
title: Listen Labs：把用户研究“黑灯流水线”化，AI Agent 系统实现小时级洞察
publish_date: '2025-07-09'
publish_timestamp: 1752062400
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/gyzIxB41nSPVRRxR3t-gVg
msgid: 1000000386
appmsgid: 2247514798
itemidx: 1
digest: 和 1000 个用户聊完天再决策
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzSd75o8AwksGx7tfoibc9awtqXHbvRia5eYVWwEolt2jiauf2NkbUreicPRXXicz3uibD0FPgJq3n61iaiaw/0?wx_fmt=jpeg
image_count: 23
archived_at: '2026-04-20T03:58:16+08:00'
---

[![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/002.png)

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/003.png)

作者：Hongyu

编辑：penny

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/004.png)

Listen Labs 由两位哈佛校友 **Florian Juengermann** 与 **Alfred Wahlforss**在 2024 年底联合创立，并在 2025 年 4 月连获 Sequoia 领投的种子轮与 A 轮合计 2700 万美元融资，目标是打造一套能**自动招募受访者、主持上千场多语访谈、即时归档并复用洞察**的“AI 用户研究员”体系。

今年 2–5 月，Listen Labs 依次发布三项核心能力：1）**AI Interviewer**可同时主持上千场语音/视频深访并动态追问；2）**Insight Engine** 把转录、情绪与行为数据送入 GPT-4o 管线，几分钟生成主题聚类与可下载 PPT；3）**Research Warehouse** 将所有历史项目向量化存档，研究者可像 ChatGPT 一样对话检索并触发“一键再访谈”。

在 AI 赋能用户研究的两条主线中，一条是传统无主持可用性测试借助 LLM 做摘要与打标签；另一条则是 Listen Labs 所聚焦的**全流程自动化深访**——让 AI 主持人+ 用户访谈池（panel network）把“招募-访谈-分析-汇报”变成黑灯流水线，研究团队只需提出商业问题即可获得可执行洞察。

本文通过两位联合创始人的专访、公司网站披露及报道，详解了 Listen Labs 如何用多模型管线与并行计算实现小时级交付，以及为何在 AI 驱动的用户研究浪潮中，“数据仓库＋代理”将成为下一代产品决策操作系统。详细分析了其竞争态势以及呈现了其在**自动化完整性、LLM 深度、小时级交付**和**全球高质量面板**四个维度的竞争优势。但未来仍需在数据治理、面板多样性与方法论可信度上持续迭代。

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/005.png)

💡 目录 💡

   01 创业故事

   02 产品介绍

   03 核心价值

   04 竞争

   05 客户反馈

**01.**

**创业故事**

AI 的指数级发展正在重塑商业社会基础架构。结合数据科学方法与机器学习模型的协同进化，形成了多产业范式转型的技术临界点，为商业决策机制的革新创造了结构性机遇。

***Listen Labs 诞生于一次“只有三份访谈就要押注产品方向”的无奈——Alfred 与 Florian 用 AI 把深度定性研究的速度、规模和说服力，都提升了两个数量级，让“和一千个用户聊完天再决策”成为现实。***

在瑞典长大的**Alfred Wahlforss**还在本科阶段（KTH 计算机与商业专业）就创办了护士派遣平台 Bemlo，并一路把产品做到近 100 万美元年收入；随后他赴哈佛攻读数据科学硕士。在这一路上，他做过海量用户研究：用问卷去衡量功能、追踪品牌活动。但他很快发现——问卷能给出指标，却给不了“为什么”；而当他进行定性访谈时，往往聊完三个人就要拿去说服团队下注，这种样本量让决策既难以自信，也难以复现。

在哈佛，Alfred 认识了来自德国、曾获 IOI 奖牌和 ICPC 世界决赛资格的**Florian Juengermann**。Florian 先在特斯拉 Autopilot 团队做运动规划算法工程师，直接向 Elon 汇报，对“把技术推到极限”有近乎偏执的执念；两人都热衷快速验证产品假设，也都被“怎么把用户洞察做得既深又快”这个痛点反复折腾。

一次课余合作，他们两周内做出了一款 AI 头像生成应用，首日就涌入 2 万用户。为了搞清这些用户真正想要什么，他们临时写了一个小工具去自动发问、自动追问、再自动总结访谈内容——这正是 Listen Labs 最早的雏形。那次经历让两人意识到：如果 AI 能把深度访谈扩展到成百上千人，而分析和总结又在几小时内完成，传统市场调研的效率边界就会被彻底改写。

**2023 年，他们正式创立 Listen Labs。**平台用大型语言模型担任“主持人”，可以同时与上千名受访者展开富有同理心的对话；模型会根据实时回答动态追问，最后再把所有访谈自动聚类、提炼洞察，并生成易读的决策摘要和片段视频。短短两年，Listen Labs 已为微软、Canva 等客户完成超过 30 万场访谈，并先后获得红杉领投的种子轮和 A 轮融资、累计 2700 万美元。

**02.**

**产品介绍**

“Listen Labs 定位目标用户、开展访谈、分析反馈，并提供可执行的洞察结论——数小时内即可交付成果，周期缩短至传统调研的十分之一。”

Listen Labs 端到端 AI 研究系统覆盖从研究设计至洞察综合的全流程，核心阶段包括：**研究设计（Research Design，自动化生成研究框架与执行方案）、****目标招募（Target Recruitment，精准筛选特定研究人群数据库）、****AI 深度访谈（AI Interview，通过智能交互技术实施情境化访谈）、****洞察综合（Insight Synthesis，自动整合多维度数据形成结论）。**

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/006.png)

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/007.png)

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/008.png)

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/009.png)

滑动查看完整表格

**03.**

**核心价值**

Listen Labs 聚焦市场调研环节的核心痛点，通过自研 AI 访谈模型、全球面板与自动化分析管线，把原本“慢、贵、样本小”的定性研究升级为“深、快、省”的持续洞察流程，提升客户决策质量并持续创造商业价值。

**1.****聚焦市场调研环节的核心痛点**

客户研究市场体量庞大，单以软件巨头 Qualtrics 即获 120 亿美元估值可见一斑。据行业公开数据显示，财富 500 强企业平均每年在客户调研工具上的投入约 1000 万美元，在传统市场研究机构上的预算高达 1 亿美元，合计形成百亿美元级的支出规模。然而，现有服务提供方普遍存在技术落后、流程冗长等效率瓶颈，无法满足企业日益增长的快速洞察需求。

市场调研的核心环节——招募合适受访者、开展访谈、分析数据并生成报告——本质上仍是基础且重复的工作，但在传统模式下耗时高、成本重，难以同时保证数据质量与样本规模。这一痛点催生出对兼顾速度、质量和成本控制的下一代解决方案的强烈需求，为技术驱动型市场研究平台创造了显著机会。

**2.****通过自研 AI 访谈模型、全球面板与自动化分析管线，把原本“慢、贵、样本小”的定性研究升级为“深、快、省”的持续洞察流程**

Listen Labs 将大模型访谈、全球面板与自动化分析整合为一条端到端流程，可在数小时内完成原本需 6–8 周的定性研究：**平台一次可并行主持上千场语音或视频访谈，实时智能追问“为什么”，并依托自建的专家访谈语料对模型进行微调，确保对话深度与语义聚类准确率；**所有洞察都附带原句与音/视频引用，保证可追溯性。

其自带的参与者面板覆盖 200 多个国家、数百万预审用户，已为 Microsoft、Canva、Sony、UFC、BCG 等客户交付超过 30 万场深访。Sequoia 的对比实验显示，同规模研究 Listen Labs 的交付速度从“周级”缩短到“小时级”，且在 A/B 测试中表现最佳。

由于招募、主持、转录、翻译、编码和报告生成全部自动化，客户获得与传统咨询相当甚至更细的洞察，成本却显著降低；因此这个平台特别适用于**需求发现、概念/广告测试、可用性验证及全球品牌追踪等需要同时兼顾规模与深度的场景，**同时保留人类研究员在高阶综合分析中的关键作用，形成“更好-更快-更省”的新一代质性研究范式。

**3.****团队连续成功创业经验，商业模式快速验证，资本加持**

Alfred Wahlforss 自 2019 年创立北欧医疗人力匹配平台 Bemlo，2023 年又在出售 AI 头像应用 BeFake 后，与在哈佛攻读硕士期间结识的 Florian Juengermann 联合创办 Listen Labs。Wahlforss 还发起非营利计划 Snabbt（现 Velocity），资助瑞典青年赴硅谷实践。

Juengermann 曾是德国编程竞赛国家冠军，2019 年创办软件外包团队 XOrigin、2020 年推出图像搜索应用 Trendify，2022 年加入 Tesla Autopilot 负责运动规划，2023 年出任 Listen Labs CTO 并组建算法团队。

两位创始人通过多次小型产品试验积累技术与市场洞察，逐步滚动至更大赛道，呈现出“快速迭代—技术互补—资本驱动”的连续创业模式。Listen Labs 6 个月内达到 300 万美元 ARR，单月收入破 100 万美元；服务微软、Google、Anthropic 等头部客户并获红杉资本领投的 2700 万美元融资。

**4. 未来演进方向**

将 Listen Labs 由当前的早期访谈与分析工具升级为一个集成式“研究数据仓库＋AI 代理”平台：平台将沉淀全部历史研究数据，支持用户通过对话即时检索过往结论，并自动按关心的客群维度生成“合成用户”，推演其潜在回答；如果推演不足以满足需求，系统可一键发起新一轮定向访谈，迅速补充样本。

借助大模型技术，平台预计像编码领域的 AI Copilot 一样显著提升研究生产力，实现问题生成、招募、访谈、分析到报告的全流程自动化和民主化，同时保留专业研究人员在高级分析与策略洞见中的不可替代作用。

联合创始人相信，随着研究门槛降低、速度和成本优化，市场对高质量用户研究的需求将被进一步激发，未来的研究团队将由人机协同组成，研究岗位数量只增不减。

**04.**

**竞争**

用户体验（UX）研究软件市场涵盖用于收集、分析和解读用户反馈的工具与平台，为以用户为中心的设计和产品开发提供数据支持，以改进产品可用性和用户满意度；随着企业对用户导向策略关注度的提升，该类软件的市场需求整体呈增长态势。

全球 UX 研究软件市场目前仍处“亿级美元”体量：2024 年规模约 2.5–4.3 亿美元，并预计在 2032–2033 年增至约 10 亿美元左右，对应年复合增速 11–13%；增长主要受数字化转型、远程协作常态化及生成式 AI 在访谈分析中的渗透推动，而数据隐私合规和预算审查是限制企业快速扩张的关键因素。

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/010.jpg)

当 AI 主导的远程 UX／定性研究赛道的竞争主要围绕四条轴线展开：

**1. 受访者资源**

当前趋势是受访用户池从“量”走向“质+广”（多语种、身份核验、GDPR 合规），对早期公司有资金与时间密集型挑战。规模和覆盖度直接决定样本获取速度与代表性，例如 User Interviews 自称拥有逾 600 万名可验证受访者并可在数小时内完成匹配，Listen Labs 则凭借语音并行技术一次可启动上千场访谈、触达 200+国家参与者。

**2.****AI 分析深度与客观性**

行业目前尚缺乏统一客观评估指标，模型偏差、上下文截断、幻觉等问题需通过链路追溯和人工复核缓释。平台从简单转录升级到大模型驱动的主题聚类和自动洞察，如 UserTesting 在 2025 年全面推出 AI Insight Summary 以自动解析行为与语音数据。

**3.****使用流程设计**

交互设计越贴近产品、设计、营销等跨职能团队的日常工具（Figma、Jira、Slack），越能提升渗透率并降低学习曲线。工具能否把招募、访谈、分析到汇报无缝串成单一工作流决定落地门槛，Listen Labs 主打“一键追加样本＋自动 PPT”，而 Conveo 提供实时视频房间与动态追问来提升交互效率。

**4. 资本与扩张能力**

融资额直接影响面板扩张与模型训练节奏：Listen Labs 2025 年获 Sequoia 领投 2700 万美元种子＋A 轮，Outset.ai 同年完成 1700 万美元 Series A，Conveo 亦在 2024 年拿到 530 万美元种子轮。

在资金、面板和模型快速拉开差距的同时，行业仍面临隐私合规、模型偏差和受访者激励等共性挑战。

**主要趋势**包括：

1）行业龙头借规模经济持续并购整合，巩固纵向全链条优势；

2）AI 能力正覆盖招募、测试、分析与报告等环节并迭代升级；

3）数据合规、隐私保护与洞察保真度成为采购与合作前置条件；

4）各区域受本地法规及面板资源差异影响，竞争呈现显著地域化；

5）厂商通过区分大型企业、中小企业与初创等客户层级，推出差异化功能与定价方案以扩大渗透。

**主要竞争对手**

Global Growth Insight 的研究显示，全球 UX 研究软件市场高度集中，显现规模壁垒，全球前五大厂商市占率近 60%，其中 UserTesting 由于广泛的企业使用量和强大的平台功能，约有 26%的市场份额；UserZoom 捕获了近 21%的市场份额，该市场份额由其强大的远程测试和分析工具驱动。

**Listen Labs v.s. UserTesting v.s. UserZoom**

Listen Labs 全程 AI 自动化访谈与报告交付最快，UserTesting 人机结合加 AI 摘要获大型客户青睐但价格高，UserZoom 以企业级 ResearchOps 与量化分析见长却因学习曲线陡而受诟病。具体对比如下：

**产品形态**

• Listen Labs 是 AI 主持深度访谈+受访者招募+自动报告的一站式平台，完全由 AI 代替人工主持，可以数小时内生成主题、亮点剪辑和 PowerPoint 报告。

• UserTesting 是人机结合的访谈与可用性测试平台（moderated / un-moderated）。2023 年推出 UserTesting AI，在原有视频测试上增加自动摘要与趋势发现。

• UserZoom 是企业级 UX 研究套件，侧重远程无脚本任务、基准测试和行为分析，可以提供项目管理式 ResearchOps 流程。

**前端交互**

• Listen Labs：Web 仪表盘可以一键生成 “highlight reel”，访谈过程有实时字幕、可插入追问，可以多语言音调测试。

• UserTesting：有时间轴视图和实时聊天室，团队可共同标注、下载剪辑片段，客户端 App 支持移动端采样。

• UserZoom：有任务构建器和数据看板，可以和 Figma / Jira 集成，以表格和漏斗视图呈现量化指标。

**中 / 后端技术**

**•**Listen Labs：有自研 LLM 做语义聚类与情感分段，主持逻辑基于 GPT-4 级大模型并可动态追问，可以自动生成多格式报告。

• UserTesting：“AI Insight Summary” 以生成式 AI 自动提炼视频与行为数据，Feedback Engine 将 UserZoom 技术整合为趋势检测。

**•**UserZoom：统计引擎和 NLP 模块 “AI Themes” 快速标签化文本与言语记录，支持自动路径 / 热点分析。

**客户反馈（公开）**

**•**Listen Labs：1）微软、Google 内测称“小时级交付缩短研究周期”；2） Reddit 社区研究员评价称自动化、高效，但需验证问答深度。

**•**UserTesting：1）Wells Fargo、BT Group 等案例称 AI 摘要节省上百小时视频分析；2）Forrester Wave 2024 将其列为“领导者”，但部分用户反馈定价昂贵。

• UserZoom：1）企业评测称测调数据分析维度“更量化”；2）第三方对比文档指学习曲线陡峭，早期报告导出略繁琐。

**赛道分化：“一站式全流程自动化”平台 v.s.  AI+人协作”工具 v.s. 上游面板或补充分析功能**

AI 主导的 UX／定性研究赛道正分化为三类：

1）Listen Labs 与 Outset.ai 代表的“一站式全流程自动化”平台，以 GPT 级大模型主持访谈、生成多模态报告，强调数小时交付；

2）UserTesting、Conveo、Strella-AI 等“AI+人协作”工具，在视频访谈基础上叠加脚本生成、趋势洞察与 Query 检索，服务大型企业并追求深度分析；

3）User Interviews 与 Sago 则侧重受访者招募与数据管理，为前两类平台提供上游面板或补充分析功能。

整体市场竞争围绕自动化深度、交付速度与量化分析能力展开，头部玩家已获千万至亿美元级融资并吸引 Unilever、Google 等标杆客户。

重点企业对比如下：

**Listen Labs**

**•****定位 / 交付：**AI 主持深度访谈的一体化 SaaS（转录-主题归类-报告全自动）

**•****交互特点：**Web 仪表盘并行多场访谈，结果可导出摘要 / PPT

**•****技术要点：**语音识别+GPT 类大模型做深入追问与主题聚类

**• 客户状况：**官方称“数小时交付洞察”，具体客户名单未披露

**Motives**

**•****定位 / 交付：**AI 驱动定性研究平台，自动化访谈、分析与报告

• **交互特点：**研究者用 Web 控制台搭建项目，受访者视频 / 语音参与

**•****技术要点：**LLM 自动转录并生成主题剪辑片段

**•****客户状况：**聚焦品牌营销场景，未公布具体客户数量

**Conveo**

**•****定位 / 交付：**“AI 同事”式视频访谈平台，可自动生成研究方案并即时分析

**•** **交互特点：**实时房间支持动态追问，分析面板同步展示洞察

**•****技术要点：**多语言 ASR+GPT 模型，持续训练企业数据

**•** **客户状况：**宣称 Unilever、Google 等采用；已获 530 万美元种子轮融资

**Strella-AI**

**•****定位 / 交付：**AI+人协作研究工具，自动生成讨论指南并支持多语言偏差控制

**•****交互特点：**流程看板与实时 highlight reel，在线编辑脚本

**•****技术要点：**LLM 生成脚本+Query 引擎跨访谈检索，官方称分析时间缩短 90%

**•****客户状况：**示例客户包括保险科技公司 Root 等

**Outset.ai**

**•****定位 / 交付：**多模态 AI 主持研究平台，支持访谈与可用性测试

**•****交互特点：**可定制虚拟主持人 Persona，集 Figma 等原型工具

**•****技术要点：**自研多模态模型联合法行为视频、音频与交互事件

**•****客户状况：**2025 年完成 1.7 亿美元 A 轮融资，服务多家大型企业

**UserTesting**

**•****定位 / 交付：**企业级体验研究套件（并入 UserZoom 后覆盖量化 + 质性）

**•****交互特点：**多人协作空间+ “AI Insight Summary” 自动主题提炼

**•** **技术要点：**专利行为数据管线+GPT 驱动摘要模型

**•****客户状况：**覆盖财富 500 企业，官方未披露 AI 模块渗透率

**User Interviews**

**•****定位 / 交付：**招募与参与者 CRM 平台，维护 600 万+受访者面板

**•****交互特点：**“Hub” 项目看板 + API 向第三方研究工具供数

**•****技术要点：**匹配算法+身份核验模型，数据可与 Zapier 等 SaaS 联动

**•****客户状况：**官方着重面板规模和分析，暂不提供自动访谈 /分析功能

**Sago (QualBoard)**

**•****定位 / 交付：**传统质性平台转型数字社区，推出 Query AI 与 Multi-Video AI Summaries

**•****交互特点：**讨论板+虚拟焦点小组，Query AI 支持自然语言检索

**•****技术要点：**生成式 AI 跨视频摘要与快速查询

**•****客户状况：**服务 CPG、金融等垂直行业，官方宣称“提高分析效率”

Listen Labs 的显著优势在于**大规模并行语音访谈（官方宣称可“一人并行千场”）与自动生成 PowerPoint 报告**，并已获得 Sequoia 领投的 $27M 资金，为持续研发和面板扩张提供保障。

与之相比，**新创竞品**（Motives、Conveo、Strella-AI、Outset.ai）在访谈自动化与多模态分析等单点功能上各有亮点，但普遍仍处早期融资阶段，面板规模、数据仓库深度或企业集成度尚待时间验证。

**传统/成熟平台**（UserTesting、Sago）则凭既有客户群和数据资产在流程完整性与合规性上具优势，但工具学习曲线、成本与 AI 原生深度可能不及 Listen Labs。**User Interviews**专注招募环节，可为多方提供上游样本，构成 Listen Labs 潜在合作方而非核心功能竞争者。

**Motives**

**•**相对 Listen Labs 的优势：访谈后自动生成高亮视频片段与主题洞察，方便营销场景直接引用

**•**相对 Listen Labs 的劣势 / 风险点：未披露并行访谈规模和数据仓库规划；融资与客户数量公开信息有限，资源储备可能逊于 Listen Labs （已获$27M A 轮）

**Conveo**

**•**相对 Listen Labs 的优势：已获 Unilever、Google 等大型客户落地，验证企业级适用性；多语言视频访谈与实时分析

**•**相对 Listen Labs 的劣势 / 风险点：仅完成$5.3M Seed 轮，资金与团队规模小于 Listen Labs；尚未公开支持“干场并行”能力

**Strella-AI**

**•**相对 Listen Labs 的优势：AI 自动生成多语言讨论指南并宣布称可将分析时间缩短 90%；支持量化问题嵌入、偏差控制

**•**相对 Listen Labs 的劣势 / 风险点：客户案例与资金规模披露有限；未见自动 PPT 报告或研究数据信仓库功能，长期沉淀能力待验证

**Whyser**

• 相对 Listen Labs 的优势：异步 AI 语音/视频访谈减小排期摩擦，可通过 User Interviews API 快速招募样本，适合资源受限团队

• 相对 Listen Labs 的劣势 / 风险点：仍处早期测试阶段，主要在 Product Hunt 获得初步口碑；高阶分析与并行规模未公开，技术深度或受限

**Outset.ai**

• 相对 Listen Labs 的优势：早在 2023 年提出“AI-moderated interview”概念，获$17M Series A；支持多模态数据（视频、音频、交互事件）分析，并与 Figma 等原型集成

• 相对 Listen Labs 的劣势 / 风险点：团队仅 14 人，扩张与客户成功需要更多资源；并发能力与自动报告深度未公开，与 Listen Labs“干场并行+自动 PPT”定位不同

**UserTesting**

• 相对 Listen Labs 的优势：拥有庞大企业客户和专利行为数据管线，量化 + 质性全流程；AI Insight Summary 已商用

• 相对 Listen Labs 的劣势 / 风险点：平台复杂、价格和实施周期相对较高，中小团队入门门槛大 Listen Labs；AI 功能仍属增量插件而非全栈核心

**User Interviews**

• 相对 Listen Labs 的优势：600 万+受访者面板与身份核验，API 生态完善，可为 Listen Labs 这类工具提供上游流量

• 相对 Listen Labs 的劣势 / 风险点：仅做招募 CRM，不提供主持、分析与报告；若客户倾向“一站式”，需要再接入 Listen Labs 或其他分析工具

**Sago (QualBoard)**

• 相对 Listen Labs 的优势：数字社区 + 传统质性焦点组，2024 推出 Query AI 与多视频摘要，可服务长期社区研究

• 相对 Listen Labs 的劣势 / 风险点：平台历史包袱重，AI 功能为补丁式升级；自动主持、并行规模与 PPT 输出等能力不及 Listen Labs 的“AI 研究全栈”愿景

就**自动化完整性、LLM 深度、小时级交付**和**全球高质量面板**四个维度来看，Listen Labs 在“快速、大规模质性洞察”的细分场景具备明显先发优势，可帮助产品与市场团队在迭代周期内获取决策级用户反馈。

**1. 全链路自动化**

Listen Labs 亮点在于：1）单一平台覆盖招纳生成 → 全球招募 → AI 主持访谈 → 自动剪辑/报告；2）平台本身完成流程衔接，无需切换多款工具。

竞争对手常见做法是，大多数厂商在**单点**提供服务，比如 UserTesting 需在外部脚本编辑器编写任务；UserInterviews 仅做招募；Dovetail 专注资料库。

Listen Labs 的竞争优势来源于产品架构自带完整工作流，可直接嵌入产品迭代节奏，省去人工对接与导出导入步骤，减少人为错漏和总工时约 50–70%

**2.****AI 深度（LLM 驱动）**

Listen Labs 亮点在于：1）LLM 实时主持，能根据受访者回答**即时追问**，保持对话语义连贯性；2）自动生成文字摘要、主题聚类、剪辑“高光”视频及 PowerPoint 报告。

竞争对手常见做法是，热图/可用性测试类产品（Hotjar， Loop11）仅在行为数据层做 AI 摘要；传统访谈平台（Lookback， Userlytics）依赖人工主持、人工标注。

因此，Listen Labs 的竞争优势来源于，1）深度语义理解 + 生成式追问，使“质性洞察”可大规模复制；2）减少研究员在转录、编码、报告撰写环节的投入，节约 60–80%分析时间。

**3.****交付速度**

Listen Labs 亮点在于从提需求到交付成品**数小时，**官方案例显示可在 6–8 小时内完成，20+次深访并生成报告。

竞争对手常见速度是，UserTesting 专业服务交付约 1–14 天；Forsta/FocusVision 等传统供应商需**一至两周**完整报告。

所以 Listen Labs 的竞争优势在于可以快速反应适配**敏捷/CI CD** 迭代，在 A/B 上线或概念验证阶段能提供“决策当天就可用”的定性证据。

**4.****自有面板规模与质量控制**

Listen Labs 亮点在于：1）宣称接入**数百万**项画像受访者，覆盖 200+ 国家；2）内置**欺诈检测系统**，将无效样本率从行业平均 ～20% 降至近零；3）可按语言、职能、行业、人口统计及心理特征筛选。

竞争对手常见做法包括，1）部分 SaaS 工具需客户“Bring-Your-Own-Participants”；2）大面板厂商（UserTesting、Userlytics）虽规模大，但跨语言及 B2B 细分深度受限。

Listen Labs 优势来源于 **全球化覆盖 + 算法质控，并**兼顾“速度、范围、真实性”，这对早期出海产品、长尾垂直行业尤其重要。

但需要注意的是，Listen Labs 的价值兑现仍取决于：

• **算法透明度与合规体系**的进一步完善；

• 与**BI/产品分析**工具的深度集成，以稳固客户黏性；

• 持续投入**面板质量与多语种支持**，防止规模扩张削弱数据可信度。

若能在以上环节保持领先，Listen Labs 有望在用户研究软件赛道建立差异化护城河，并抵御传统巨头通过并购整合带来的竞争压力。

**05.**

**客户反馈**

**可公开查到的客户使用反馈**

**投资方 / 企业用户 Sequoia Capital：**Sequoia 既为投资方也是内部用户，称 Listen 能“在数小时内同时进行数千场访谈”，并能“触达 200 多个国家、数百万名参与者”。截至 2025 年 4 月，平台已累计完成 30 万+ 场访谈，服务 Microsoft、Canva、Chubbies 等客户。

**品牌客户示例 Chubbies：**Chubbies 案例指出，借助 Listen，青少年样本量提升 24 倍（从 5 人增至 120 人），缩短新品调研周期（具体时长未披露）。

**品牌客户示例 Canva：**Canva 表示通过 Listen 在“数小时内完成全球多语种访谈”，将原本须数日的流程压缩为“数分钟”级别。

**参与者社区 Redditr/ProlificAc：**多名受访者肯定界面友好、付款快（即刻或数小时内结算），负面反馈主要集中在报酬偏低、摄像头要求、筛选补偿不足；部分用户担忧收集过多个人信息（PII）。

**Product Hunt（公开评论）：**早期上架时获“自动化访谈节省时间”之类正面评论，但截至 2025 年 6 月页面尚无正式评分数据。

**综合观察**

**优势共识：**企业客户与投资方普遍肯定 Listen Labs 在**时效（从数周缩短至数小时）**与**规模（并行数千场深访）**上的显著提升，并认可自动生成 PPT 报告、视频高光等“一站式交付”的便利。

**量化成效：**案例显示可带来 20×以上的受众覆盖增长、50+场深访一周内交付等效率数据，对快速迭代产品及营销策略具有直接价值。

**质疑与改进点：**参与者端主要集中在**报酬标准**与**筛选补偿**；研究从业者则关注 **A****I 访谈提问质量、灵活追问与分析可靠性**。这些反馈提示 Listen Labs 需在激励机制、访谈脚本优化及结果可审计性上持续迭代，以巩固其“深度 + 速度”卖点并化解偏差隐忧。

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/011.png)

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/012.png)

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/013.png)

排版：范诗翎

延伸阅读

[![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/014.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514551&idx=1&sn=91311f46da4ed809525675f3991f7e24&scene=21#wechat_redirect)

Isomorphic Labs：DeepMind 创始人再创业，打造制药界的 TSMC

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/015.png)

[![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514519&idx=1&sn=2ffc31799808fe68c65557f25c97796f&scene=21#wechat_redirect)

“10x Cursor”开发体验， Claude Code 如何带来 AI Coding 的 L4 时刻？｜Best Ideas

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/017.png)

[![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/018.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514422&idx=1&sn=be5cceb8d96e2b9a300ca353d4c97d1c&scene=21#wechat_redirect)

Jack Clark: 美国 AI 政策的隐形推手，时代的良心还是囚徒？

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/019.png)

[![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/020.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514384&idx=1&sn=4150d9e5bc851d09a23f519b825521f3&scene=21#wechat_redirect)

Cluely：最具争议的 00 后 AI 创业者，用一款 “作弊神器”2 个月实现 600 万美金 ARR

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/021.png)

[![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/022.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514353&idx=1&sn=a2dfe3b5f7c67c2e3ea1b4eb03b26fb0&scene=21#wechat_redirect)

OpenAI 研究员 Noam Brown：Mid-training 是新的 pre-training

![](../images/2025-07-09-listen-labs-ba-yong-hu-yan-jiu-hei-deng-liu-shui-xian-hua-ai/023.png)
