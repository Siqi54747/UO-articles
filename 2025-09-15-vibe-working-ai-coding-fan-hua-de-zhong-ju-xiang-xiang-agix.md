---
title: Vibe Working：AI Coding 泛化的终局想象 ｜AGIX PM Notes
publish_date: '2025-09-15'
publish_timestamp: 1757937600
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/3bKMrDP8vamhFPmaoKH5Fg
msgid: 1000000418
appmsgid: 2247517863
itemidx: 1
digest: AGIX 持续大幅度跑赢美股主要指数，上周上涨 3.15%
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgwoygU0dk2Gad6dRFOVDQMY8CQibkGwfztf3wIV2OccSVpdNbGQZUbSrnf0RHgmoc62W4hZ9JMnoMg/0?wx_fmt=jpeg
image_count: 19
archived_at: '2026-04-20T04:21:53+08:00'
---

[![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/002.png)

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/003.png)

[AGIX](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=3570724992708624387&scene=21#wechat_redirect)指数诞生于我们对“如何捕获 AGI 时代 beta 和 alphas”这一问题的深度思考。毫无疑问，AGI 代表了未来 20 年最重要的科技范式转换，会像互联网那样重塑了人类社会的运行方式，我们希望 AGIX 成为衡量这一新科技范式的重要指标，如同 Nasdaq100 之于互联网时代。

「AGIX PM Notes」是我们对 AGI 进程的思考记录，希望通过学习 Warren Buffett、Ray Dalio、Howard Marks 等传奇投资者们的分享精神，与所有 AGIX builders 一同见证并参与这场史无前例的技术革命。

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/004.png)

**PM Notes**

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/005.svg)

**Vibe Working**

作者：Max

“Vibe working”最早用于 AI 驱动的软件开发，强调用自然语言描述目标，把目标和上下文输给 AI，结果自动产出可用代码。但代码之所以可以 Vibe 是指针对结果的 prompting 而非针对过程的 prompting。正是因为过程无论多少步骤，都可以最终收敛到一个单一结果上，也即代码可执行与否。

我们可以想象一个棋盘，它的规则是固定的，每一个操作都能立即得到反馈。在编程中，这个“棋盘”就是可控的开发环境。我们给出明确的目标和上下文，比如“我要实现一个用户登录功能”。接下来，编译器、测试、部署这一整套流程提供了一种确定性：代码要么通过，要么失败，结果一目了然。

在 Vibe working 能否成立的讨论中还有另外两个前提，一是可追溯的上下文。所有的依赖关系、工具链、外部资源都清晰可控，可以随时回溯到任何一个版本。二是低延迟的反馈。测试结果能迅速告诉你，你的代码是否正确。

而如果想把“vibe working”从代码世界推广到更广阔的开放环境，比如日常办公、市场营销甚至物流管理，可能这个环境和工作流本身也必须“API 化”。

简单来说，就是让环境的状态变得可读。它需要有可判定性（Determinism）：比如任务是否足够明确？即使输入有细微变化，结果也能保持稳定，并且有清晰的验收标准。还需要有稳定可追溯的上下文（Context）：完成任务所需的一切——数据、权限、依赖关系——是否都能被追踪和回溯？以及可控执行（Actuation）：操作是否标准化、可回滚。

这一切都指向了两个方向，1）代码化的工作流管理，2）作为企业 Context 的数字孪生。

工作流管理方面，市场上已经有不少现成的产品和方案。在非上市公司领域，上一代公司 Zapier， 和 AI Agent 协作管理的 n8n 都是典型代表。典型的工作流比如，每天早上 8:00，检查我当天的电子邮件和日程，只筛选出那些有公司外部参与者的会议，然后在线搜索这些人的资料，接着做个总结，然后把总结发到我的飞书上。你只需将这段话输入并作为提示给 Zapier 中的 Agent，它就会正确选择工具，在后台构建流程，给你一个摘要，然后允许你连接这些工具。随着人与工具的聊天交互趋势的演进，人们会越来越普遍地期望所有工具和所有软件工具都能让他们只需输入或只需说出想要实现的目标。工具会回复，“这是我创建的工作流，我们来测试一下，看看是否有效。”

这个过程完全抽象了软件过去构建的各类界面和模块，不代表那些执行模块被取代了，而是在复杂功能之上抽象出了一个执行和规划层，用户不再需要学习上百个复杂按钮以及其功能，再自行构建和测试。

如果软件公司例如 Adobe 可以迅速把如何使用 Adobe 的成百上千个工作流 Agent 化，可能就能避免被图片生成模型颠覆的命运，这关乎执行能力，而非技术可行性。

n8n 的切入角度稍微不同，它更针对的是无人或自动化的工作流，面向的是更技术化的团队。尽管目前 Glean， Decagon， Sierra 也开始基于他们的单点功能切入工作流协同，例如将客服通话记录摘要到 Salesforce 或类似的基础操作；只是因为他们在单点功能上（客服等）释放了 AI 能够提供的最大价值和动能，所以他们从单点切入并尝试横向拓展到工作流自动化。有没有可能未来 AI 的最佳形态就是像 n8n 一样的工作流自动化原生，因为所有的单点功能都会被 AI 动力驱动，在之上做编排的能力，以及最不能忽视的，把人作为 Context 最重要一环 loop in 的能力，会超越目前的单点解决方案。类似一个“多态工具平台”，一个支持所有 AI Agent 和客户特定用例的智能工作流集成平台的抽象层，所有的 AI 用例都可以在此之上构建。

当然目前的此类工具还比较薄，比如在工作流作为一个事件被激发时，应该有自动的 RAG，自动的 Context engineering 等能力，同时应具备各个工作流节点连接多样外部数据来源（数据库等）的专业化能力。我们已经看到 MCP 这个协议的潜力，但 MCP 是从 Chatbot 为中心去思考问题，是把各类工具的能力向语言模型来暴露。

语言模型的问题是输出的非确定性，类似本周 Thinking Machine 公布的自己的研究，就算通过某种方法把输出的确定性一定程度上解决，又可能牺牲了其性能。可能正确的思路是，依赖类似 n8n 之类的确定性工作流平台作为代理能力的端到端流程的枢纽，把 Glean 等等这些单点解决方案作为 MCP Client 囊括进来。相当于把 Chatbot 从工作流的核心（大脑）的位置摘除出来，让位于确定性工作流编排平台，而 LLM 降级为作为一个辅助和它该有的 Infra 之一的位置。可能这也是语言天然的局限性，类似于我们无法用语言描述如何运营一个全球性的物流公司，变相说明了工作流，可视化和数字孪生的价值。

回到 Vibe working，目前类似自动化 Office 套件等的产品获得了较高关注，市场在欢呼 PPT，EXCEL 等软件可能被 LLM 的能力替代。但这里的误区可能还是我们的聚焦点，如果以 LLM 全能的视角来看这类工具，现有 PPT，Excel 的功能如何向语言模型进行暴露更为重要。所以我们看到这些文档生成产品，通过利用现有的开源 PPT 和 Excel Library，结合 LLM 的编程能力实现了初步的自动化文档生成、报告制作和数据可视化。

尤其是本周发布的 Claude File Creation，似乎离 Vibe Working 的实现咫尺之遥。但实际上 Claude 只是发布了一个 OpenAI 两年以前发布的 Code Interpreter，或者数据分析产品能力上和两年以前的 Julius.ai 并没有太大差异。通过在服务器端的沙箱中编写并执行自定义的 Python（和 Node.js）代码，并用它来处理和分析数据。通过 phython-pptx， openpyxl 等开源库，Claude 获得了创建简单文档的能力。

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/006.png)

就像 X 上这条评论中指出的一样，Coding Agent 迅速进步的核心是 dogfooding，产品开发者是自己就是第一批、也是最苛刻的用户。当他们用自己的产品来编写代码时，所有的痛点、不便、低效之处都会被第一时间感知到。通过自己试用，对错误进行分析分析然后流程化评估的闭环，使得产品团队能够以极高的效率，将真实世界的使用经验转化为模型能力的提升和产品功能的改进。

而 Vibe working 的问题是目前暂时无法闭环，如何定义一个好的 PPT 或者一个好的 Excel 财务模型，并没有像程序一样单一的“可执行”作为标准。这一过程和工作流自动化一样，可能解决的方法还是要按照以人为中心化的视角，或者工作流编排为中心的视角，结合模型的能力，通过 FDE 作为模型和客户之间重要的 workflow context builder，最后实现产品真正的可用性。而不是目前我们看到的，每个产品生成的 PPT 都是类似格式，千篇一律。

**01.**

**本周市场总结**

**全球市场延续涨势，亚洲与科技板块表现亮眼**

本周，美股三大指数齐创新高，受益于投资者对美联储 9 月降息的普遍预期。美国 8 月 CPI 同比升至 2.9%，显示通胀压力回升，而初请失业金人数升至 26.3 万，为 2021 年 10 月以来最高水平，就业市场趋弱。欧洲市场同样跟随上涨，Stoxx Europe 600 与 FTSE100 分别录得 +1.0% 与 +0.8%。中国市场投资情绪积极，恒生指数、国企指数和沪深 300 均录得显著涨幅，其中沪深 300 周四创下自 3 月以来最大单日升幅，主要受益于科技股反弹。但宏观数据仍显压力，8 月 PPI 连续第 35 个月下滑至 -2.9%，CPI 三个月来首次转负至 -0.4%。

投融资方面，亚洲地区大额交易活跃，新加坡 GIC 与阿布扎比投资局（ADIA）向 Vantage Data Centers 投资 16 亿美元；Bain Capital 将中国数据中心业务以 39 亿美元出售给中资财团。另类资管领域，Blackstone 推出 BXINFRA Lux 基础设施投资产品，进一步拓展欧洲、亚太和中东市场；Sagard 与 Baird 达成合作，后者收购少数股权以支持美国财富管理扩张。

截至 9 月 11 日，行业公司股价本周中位数涨幅为 +2.7%，估值水平维持在 2025E P/E 20.9x、2026E P/E 18.1x。摩根士丹利近期参与多项重要交易，包括 Bain Capital 39 亿美元出售 Chindata、阿里巴巴 32 亿美元可转债发行、中国太保 20 亿美元可转债发行、蔚来 10 亿美元增发，以及电装与小松金融分别 5 亿美元债券融资。整体来看，全球市场风险情绪维持积极，亚洲与科技相关资产表现突出。

**AGIX 持续大幅度跑赢美股主要指数**

从表现来看，AGIX 在过去一周上涨了 3.15%，显著跑赢三大美股指数：S&P 500 上涨 1.37%，QQQ 上涨 1.35%，道琼斯上涨 0.70%。这表明成长股与技术相关资产继续对基金超额收益形成支撑。

整体来看，基金在本周延续了对结构性机会的把握，相对主要指数取得正面表现。不同地区和策略的表现存在分化，但总体上，美洲与欧洲基金保持稳健，亚洲基金则受市场波动影响更为敏感。

**02.**

**AI Alphas**

**Nebius（NBIS）与 Microsoft（MSFT）签署 174 亿美元协议**

Nebius Group 上周一（9 月 8 日）表示，将在未来五年内向 Microsoft 提供 GPU 基础设施产能，合同价值 174 亿美元。消息公布后，公司股价盘后飙升逾 47%。

该协议凸显了高性能 AI 运算需求的激增。Microsoft 还可能在协议框架下追加采购，使合同总额接近 194 亿美元。Nebius 将从今年晚些时候起，为 Microsoft 提供来自新泽西州 Vineland 新数据中心的专用 GPU 产能。

**Microsoft（MSFT）引入 Anthropic 技术，部分替代 OpenAI**

据 The Information 报道，Microsoft 将为 Office 365 的部分 AI 功能采用 Anthropic 技术，这显示公司正在分散人工智能组合。

此前多年，Microsoft 一直依赖 OpenAI 为 Word、Excel、Outlook、PowerPoint 提供新功能。此次调整将结合 Anthropic 与 OpenAI 技术。开发者表示，在自动化 Excel 财务处理、根据指令生成 PowerPoint 演示文稿等方面，Anthropic 的最新模型优于 OpenAI。

同时，Microsoft 也在开发自有 AI 模型，并将 DeepSeek 模型整合至 Azure，以提升产能满足需求。

**Microsoft（MSFT）、OpenAI 达成非约束性协议，允许 OpenAI 重组**

Microsoft 与 OpenAI 周四表示，双方已签署非约束性协议，允许 OpenAI 重组为营利性公司。这标志着 ChatGPT 热潮中最重要的合作进入新阶段。

新的商业条款尚未披露，双方称正推进最终协议的磋商。OpenAI 希望通过更常见的治理架构融资并最终上市。

不过，重组仍需加州与特拉华州司法当局批准。若无法在年底前完成，公司可能失去数十亿美元的融资。

**美国拟对 Samsung（KRX: 005930）、Hynix（KRX: 000660）在华芯片供应实施年度审批**

知情人士称，美国拟要求 Samsung Electronics 和 SK Hynix 每年申请向中国工厂出口芯片制造材料和设备的许可。此举旨在替代拜登政府时期的豁免制度，避免对全球电子产业造成动荡。

此前的 VEU（验证终端用户）制度允许两家公司在履行安全与监控承诺后，持续向中国供应设备。新方案将改为每年审批具体数量的受限设备、零件和材料。

**Nvidia（NVDA）发布 Rubin CPX GPU，面向大规模 AI 应用**

Nvidia 周二在加州圣克拉拉的 AI Infra Summit 上推出新 GPU “Rubin CPX”，专为百万 token 级代码生成与视频生成应用设计。

该 GPU 将与 Vera CPU、Rubin GPU 组成 Vera Rubin NVL 144 CPX 平台，包含 144 个 GPU，性能较现有 BG300 NVL 72 系统提升 7.5 倍。

Nvidia 称，客户每投资 1 亿美元，可带来约 5 亿美元的 token 收入。Rubin CPX 将于 2026 年底上市。

**TSMC（TWSE:2330）8 月营收同比增长 34%，AI 需求支撑强劲**

台积电 8 月营收达新台币 3358 亿元（约 111 亿美元），同比增长 34%，显示全球 AI 芯片需求依然旺盛。市场预计第三季度整体营收增幅约 25%。

**FTC 启动对 Alphabet（GOOGL）、Meta（META）等 AI 聊天机器人的调查**

美国联邦贸易委员会（FTC）周四表示，已向 Alphabet、Meta、OpenAI 等提供 AI 聊天机器人的企业发出调查请求，关注其如何监控并减轻技术的负面影响。

FTC 希望了解相关企业如何通过聊天机器人实现营收、处理用户输入、生成回应。此前 Reuters 报道，Meta 内部政策允许聊天机器人与未成年人进行“浪漫性质的对话”，另有家庭因 ChatGPT 在青少年自杀事件中的角色起诉 OpenAI。

**Adobe（ADBE）上调业绩预期，AI 功能带来回报**

Adobe 公布强劲指引，预计截至 11 月的季度营收为 60.8 亿至 61.3 亿美元，高于市场预期。剔除部分项目后，每股利润为 5.35 至 5.40 美元。

CEO Shantanu Narayen 表示，AI 产品带来的年度经常性收入已超过 50 亿美元。消息公布后，公司股价盘后上涨约 4%，收于 350.55 美元。今年迄今股价累计下跌 21%。

**Micron（MU）股价上涨，Citi 上调目标价至 175 美元**

Micron Technology 股价上周四（9 月 11 日）盘前上涨 3.6%，此前 Citi 分析师 Christopher Danely 将目标价从 150 美元上调至 175 美元，并维持“买入”评级。

新目标价较当前水平有 25%的上涨空间。分析师预计，Micron 第四财季业绩符合预期，但对第一季度指引将大幅超出市场预期，因 DRAM 和 NAND 销售及定价提升。

Morgan Stanley 指出，AI NAND 市场到 2029 年预计占全球 NAND 市场 34%，总规模将增加 290 亿美元。

**03.**

**ETF 101**

**什么是 ETF 分红**

ETF（Exchange-Traded Fund，交易型指数基金）本质上是一个持有一篮子股票（或其它可分红资产）的基金。如果这些标的股票派发股息（dividend），ETF 本身就会收到这些股息。然后，ETF 管理公司会将这些收到的股息，以现金或额外份额的方式分派给 ETF 的持有人。

**分红是怎么计算和分配的**

以下是 ETF 分红从标的公司到投资者这个流程的大致步骤：

**1.标的公司支付股息：ETF 持有的某一家公司决定支付股息（例如季度股息或年度股息）；**

**2.ETF 收到这些股息：当股票在其除息日（ex-dividend date）之后派息，ETF 持有这些股票的份额就对应领取到这些股息；**

**3.基金汇总所有股息收入：ETF 管理机构会将其组合中所有股票派发的股息收入累积起来；**

**4.净额扣除相关费用与税费（如果有）：在分派给投资者之前，可能有一些费用、管理费、税收或其他开支需要从这部分股息中扣除；**

**5.向 ETF 持有者分派：基金会按照你持有 ETF 的份额比例，将这部分股息分配给你。分派通常是按比例（pro rata） 的方式进行，即如果你持有 ETF 的 1%，你将获得所有应派股息的 1%；**

**6.分派频率：多数 ETF 是季度分红，但也有可能是年度或月度，这取决于基金本身的政策。**

**分红对投资者的意义**

**1.现金流收入：如果是偏好收取现金流的投资者，ETF 的分红可以为投资组合提供定期的现金收入；**

**2.税务因素：分红可能被视为 “合格股息（qualified dividend）” 或 “非合格股息（non-qualified dividend）”，不同类别的分红在税务上处理方式不同。合格股息通常享有较低税率（类似资本利得税率），而非合格股息可能按普通收入税率征税；**

**3.再投资的可能：有些投资平台或 ETF 本身允许将分红再投资，即用收到的现金分红去买入更多的 ETF 份额。这样可以让复利效果发挥作用。**

**关于 ETF 分红的注意点**

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/007.jpg)

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/008.png)

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/009.png)

排版：夏悦涵

延伸阅读

[![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/010.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517781&idx=1&sn=22cb82ed020d508c26cb0be9187300ee&scene=21#wechat_redirect)

Cloudflare 的 AI 新叙事：线上内容“做市商”，Agent 互联网流量基建

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/011.png)

[![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/012.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517743&idx=1&sn=124cd41acb1263ba70c332934acbd675&scene=21#wechat_redirect)

对谈 Macaron 创始人陈锴杰：RL + Memory 让 Agent 成为用户专属的“哆啦 A 梦”｜Best Minds

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/013.png)

[![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/014.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517699&idx=1&sn=ef5aa2db9b3a876a1d6d3cad7741b5d3&scene=21#wechat_redirect)

AGI 投资清单：为什么这 30+ 美股公司值得关注？｜Best Ideas

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/015.png)

[![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517695&idx=1&sn=4d7a0eb4f798080cf5a634959d4070f0&scene=21#wechat_redirect)

Agent 重构互联网，谁将受益于线上内容的“帕累托效应”？｜AGIX PM Notes

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/017.png)

[![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/018.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517618&idx=1&sn=8ef705bde94b9aed8e1dee764a89479a&scene=21#wechat_redirect)

Temporal：Nvidia、OpenAI 都在用，为什么 Agent 还需要专门的长程任务工具？

![](../images/2025-09-15-vibe-working-ai-coding-fan-hua-de-zhong-ju-xiang-xiang-agix/019.png)
