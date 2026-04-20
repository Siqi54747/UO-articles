---
title: AGI 路线图第二阶段：游戏即模型训练｜AGIX PM Notes
publish_date: '2025-10-13'
publish_timestamp: 1760356800
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/NIDKik_6xiggG5xSDIQEAQ
msgid: 1000000434
appmsgid: 2247518628
itemidx: 1
digest: 游戏为 agent 提供了一个可操作环境
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzq8YMlsI1hycJhex6ktuia9FnK120kDibco3RDH4YHVZCGQRXoKucZDhnAcvuv7HXVUHtcBk36TdKA/0?wx_fmt=jpeg
image_count: 17
archived_at: '2026-04-20T04:32:55+08:00'
---

[![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/002.png)

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/003.png)

[AGIX 指数](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=3570724992708624387&scene=21#wechat_redirect)诞生于我们对“如何捕获 AGI 时代 beta 和 alphas”这一问题的深度思考。毫无疑问，AGI 代表了未来 20 年最重要的科技范式转换，会像互联网那样重塑了人类社会的运行方式，我们希望 AGIX 成为衡量这一新科技范式的重要指标，如同 Nasdaq100 之于互联网时代。

「AGIX PM Notes」是我们对 AGI 进程的思考记录，希望通过学习 Warren Buffett、Ray Dalio、Howard Marks 等传奇投资者们的分享精神，与所有 AGIX builders 一同见证并参与这场史无前例的技术革命。

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/004.png)

**PM Notes**

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/005.svg)

**游戏即训练**

作者：Max

在我们自己的 AI 投资框架中，很早就有一个 AI 落地的“路线图”。尽管 ChatGPT 诞生已经过去了 3 年，这个“路线图”仍然只进行到了第一阶段，即 AI for Productivity。AI 的应用虽然百花齐放，但无论 coding，writing，document generation 还是 ChatGPT 本身，都仍然只是一个生产力工具。生产力可以横向继续拓展到需要创意、人类智力的各个数字化领域，图片，视频，音乐，AI 作为辅助的能力会变得越来越强，生产力工具的属性和价值也越来越明确。而第二阶段，我们当时定义了 Gaming as Training， 游戏即训练。

游戏看似和模型训练相距甚远，但无论是 OpenAI 早期的 Dota 2 项目，还是 Elon Musk xAI 近期招兵买马通过开发或利用游戏环境进一步训练旗下 AI 模型 Grok，均预示着游戏在 AI 训练中的重要角色和位置。原因很简单：

1. 游戏是一个 agent 的可操作的环境，在这里环境里，状态、动作、结果都可以被记录和复现，环境也支持高频且低成本的试错与自博弈。

2. 这个环境还有明确的规则和 ground truth，并且所有的感知是为了实现该目标而服务的，这就破除了视频相较于语言压缩率更低的问题。

3. 这个环境还能让人类 in the loop，通过与 agent 互动和协同来共同完成任务。

通过这三个重要因素，游戏就有可能成为训练 agent 不可多得的理想环境，AI agent 通过不断和环境的交互来进行学习。未来也有可能通过游戏产品化的方式实现游戏即训练，也即不断在其中收集更多人和 AI 互动协作完成任务的数据，尤其是与人协同、博弈与沟通的数据，而非目前仅是聊天机器人这么一个 AI 的最初级形态。

我们在之前提到过人类学习的方式和直觉是模拟，通过心理模拟或者想象预测可能的未来，并据此调整动作和行为。一些研究也通过让机器人能够高效地“想象”隐状态空间中自主规划行动，学会了一系列技能。

Google 从 2019 年开始的 Dreamer 研究给我们提供了一个重要的观察线索。

Dreamer v1 在 2019 年首次提出让 agent 在隐状态空间中进行“想象”， 通过隐状态空间动力模型来预测未来、规划行为。Agent 本身对于环境未知的，通过学习这个环境模型，而非在定义好的环境规则内进行规划和搜索（AlphaZero），agent 通过有模型强化学习（Model-based RL）实现了完成复杂任务的高性能，被视为通用 AI 的潜在路径突破点。随后 Dreamer v2 第一次把 Dreamer 隐空间模型方法扩展到难度极高的 Atari 环境，用纯世界模型方式达到人类水平，且超过单卡顶级无模型基线。Dreamer v3 突破了泛化性能。

当大部分强化学习算法可以直接应用于类似其开发时设定目标相似的任务时（例如玩电子游戏的 agent 的算法和下围棋的 agent 算法显著不同），通用性面临很大的问题。尤其当我们想把已有的强化学习算法应用到全新的任务，例如从控制电子游戏的算法无缝应用到机器人控制，就需要大量的工作、专业知识和计算资源来调整算法的超参数。Dreamer v3 在使用固定超参数的情况下，在广泛领域中超越了专用专家算法，使强化学习能够更容易地应用于新问题，也即具有了所谓的“泛化”能力。它依然依靠隐状态空间世界模型的思路，为 agent 提供丰富的感知能力和想象未来的能力。并通过评估网络（critic）对每个结果的价值进行判断，行为网络（actor）选择动作以达到最佳结果。

Dreamer v3 实现了在 Minecraft 中不依靠人类标注数据，开箱即用自主完成收集钻石的能力（难点在于稀疏奖励，探索困难以及长时间跨度和开放世界），为后续从互联网视频中教会 agent 世界知识，以及通过跨领域学习单一世界模型让 agent 能够逐步建立起更通用的知识和能力。

9 月公布的 Dreamer v4 更进一步，仅用未经标注的离线视频数据集获取大部分知识，而无需在游戏里进行互动学习。当我们与未完全训练好的机器人模型进行物理世界交互的时候，处理机器人损坏和安全问题往往是重要考量。通过这种离线数据集以及用“想象”来学习的方式，就不再有类似的担忧。而同样来自 Google 的 Genie 3 这种依靠 diffusion transformer 架构的视频模型，在学习物体之间相互作用的精确度方面还是有很大局限性，同时也非常消耗算力，进一步降低了其实用性。Dreamer v4 尽管使用的数据量比 OpenAI 的 video pretraining 离线 agent 少 100 倍，但性能有大幅提升，并且在算力上，实现了在单块 H100 GPU 上的实时推理。

我们可以预见类似的方法实时应用在 Computer Use 等等用例中，通过一个大量的电脑使用数据集（用稀疏奖励进行标注，很多公司都在积极的准备类似的数据集）和一个大型模型来完成训练。Dreamer 的方法也可以使得在数百万个不同场景中训练机器人执行任务成为可能，而无需在现实世界中手动搭建这些场景，也不用在训练过程中处理机器人损坏的问题。

更重要的是，它也许能真正开启多模态原始数据训练通用 agent 的范式。也即过去多模态数据中，很难判断什么是真正相关的信息，也就无法像通过语言这种高度压缩的信息一样来训练一个模型完成任务。但当在游戏或机器人模型中，agent 带着完成某个任务的目标去观察世界时，这种关注点会重构多模态数据的焦点，而这个能力能够更有效地利用多模态数据中的信号。类似 Dreamer 论文中的隐状态空间动力模型，它又何尝不是一种为完成任务而发展出来的模态，而这个模态会超越单纯的图像或文本的狭隘定义。

**01.**

**本周市场总结**

**对冲基金在 AI 与零售板块回补空仓，美日买盘主导市场**

在过去的一周中，对冲基金持续增持全球股票，资金流向从新兴市场转向发达市场，其中北美和日本表现最为突出。

在北美市场，买盘主要来自空头回补。多方反馈显示，各策略中空头仓位承压，促使基金进行回补。这导致美股多空基金（L/S）整体杠杆小幅下降，最新总杠杆为 212%，较一周前的 214%略低，但仍接近历史高位。净杠杆保持周环比持平，为 57%，位于过去 12 个月及 3 年期的第 97 百分位。值得注意的是，这部分稳定来自基金同时减持部分多头仓位，从而拉低了总杠杆。

北美市场的买盘几乎完全由 TMT 板块带动，若剔除 TMT，对冲基金在该地区将呈净卖出。TMT 内部买盘广泛，亏损科技（MSXXUPT，上周涨 5.5%）为平台上最受青睐的主题，买盘由空头回补及部分加仓共同推动。基金亦增持与 AI 相关的半导体和软件板块，但两者仓位分化显著：AI 半导体净敞口位于 100 百分位高点，而软件仅处于自 2020 年以来的第 12 百分位。

此外，对冲基金回补了在热门零售股（MSXXRFLO 指数成分股）上的空头头寸。散户持续强劲买入该板块，自 8 月初以来该指数累计上涨约 38%，基金因此被迫大幅回补空仓。

在 AI 强势股与零售热门股的双重买盘推动下，对冲基金整体成为动能（Momentum）因子的净买方。当前仓位已升至近一年上四分位，虽未达到极端水平，但基金对高动能因子的曝险正快速增加。值得注意的是，这一趋势多源于市值变化（持有的高动能股票继续上涨推高净敞口）。

另一方面，对冲基金在本周减持了生物科技、能源（尤其天然气相关企业）及生活必需品板块。从因子角度看，基金净卖出“质量”（Quality）因子，主要由低质量股票的买盘推动。

日本市场的买入力度居全球之首，与年初至今最大单周买盘规模持平。除指数产品外，基金亦增持了 TMT（半导体）及金融（银行）板块。买盘来自多空基金与宏观基金的共同推动。从地区视角看，各区域基金普遍偏向买入。

除日本外的亚洲市场交易较为平淡，中国与台湾均录得小幅净买入。然而，美股上市的中概互联网板块仍遭显著净卖出，该板块净敞口仍处于历史低位。

欧洲市场资金流平稳，对冲基金买入生活必需品与公用事业，卖出医药、奢侈品及银行板块。

**全球主要股指下跌，对冲基金延续正回报**

AGIX 本周下跌 1.51%，跌幅小于主要三大指数：标普 500 下跌 2.79%、纳斯达克 100 下跌 3.00%、道琼斯下跌 2.60%。

在业绩方面，对冲基金整体继续录得正回报。全球基金月度迄今（MTD）上涨 50 个基点，美国多空基金上涨 0.8%。欧洲与亚洲基金本月亦录得约 0.5%至 1%的涨幅。

自年初以来，全球对冲基金平均收益为 +10.2%，美国多空基金为 +11.2%。

**02.**

**AI Alphas**

**Nvidia（NVDA）股价创历史新高，美国批准向阿联酋出口芯片并上调目标价：分析称“这不是泡沫”**

Nvidia 股价上周四上涨约 1.8%，创下历史新高。彭博社报道称，美国政府已批准向阿联酋出口价值数十亿美元的 Nvidia 芯片。

据报道，美国商务部在阿联酋承诺加强对美投资后，向 Nvidia 发放了出口许可证。这是自特朗普就任总统以来，Nvidia 首次获准向阿联酋出口 AI 芯片。

此举紧随特朗普年初访阿时宣布的 AI 基础设施项目“Stargate UAE”。该项目于 5 月公布，计划在阿布扎比建设 5 吉瓦特数据中心，由 OpenAI 与 Oracle 共同运营，基础设施由 Cisco 与 Nvidia 提供。

特朗普政府与阿联酋、沙特的 AI 合作为 Nvidia 打开了新的海外市场。尽管美国政府此前短暂禁止向中国销售 Nvidia 芯片，但随后以分享中国地区营收为条件暂时放宽限制——这一罕见安排仍未最终落实。同时，据悉中国现已禁止科技企业采购 Nvidia 芯片。

**Google（GOOGL）推出 Gemini Enterprise，对标 Microsoft （MSFT）与 OpenAI**

Google 推出面向企业的新产品“Gemini Enterprise”，旨在与微软的 AI 办公服务展开竞争，同时实现其 AI 投资的商业化。

Gemini Enterprise Standard 与 Plus 版每位用户每月 30 美元，Business 版为每位用户每月 21 美元。该平台可让企业用户在单一界面中使用 Gemini 进行企业数据分析与 AI 代理操作，直接对标 Microsoft 365 Copilot。

**Tesla（TSLA）因手部与手臂设计问题暂停 Optimus 机器人量产**

据 *TechSpot*报道，Tesla 暂时中止了 Optimus 的推出，同时重新设计机械结构，尤其是前臂和手部。公司已生产数百个部分完成的机器人主体，目前尚未完成，以便工程师专注于解决技术瓶颈。

三个月前，The Information 报道，这些问题导致装配和零件采购全面暂停，Tesla 机器人部门正在重新设计相关部件。手臂与手部是 Optimus 最复杂的部分，需要精细的运动控制、扭矩精度和热管理，超出 Tesla 现有设计能力。

据悉，工程师在耐久性测试中遇到可靠性问题，包括电机过热、抓握力不足以及关节频繁故障。Elon Musk 公开承认 Optimus 上肢仍是技术难题，但强调暂停是暂时的，旨在提升长期可靠性。

**Amazon（AMZN）推出新版 AI 代理工具，挑战 ChatGPT 与 Copilot**

Amazon 正推出其主力企业人工智能工具的更新版本，意在进一步抢占自动化办公软件市场份额。

Amazon Web Services 上周四宣布推出“Quick Suite”，这是一款能够分析销售数据、生成报告或总结网页内容的聊天机器人与 AI 代理组合。AWS 营销主管 Julia White 表示，现有使用 18 个月前推出的“Q Business”软件的客户，将被鼓励迁移至这一新平台。

**Salesforce（CRM）推出 Agentforce IT Service，对标 ServiceNow（NOW）**

Salesforce 推出了 Agentforce IT Service，一款新的 IT 服务管理（ITSM）平台，意在挑战 ServiceNow 在该领域的主导地位。这标志着云巨头进一步布局企业 IT 运营，基于其现有 Service Cloud 平台。

该平台高度依赖 AI，采用多 Agent 系统分析历史工单、实时识别问题根源并建议解决方案，将 IT 支持从传统工单转向对话式、预测性服务。平台与 Salesforce Data Cloud、Slack 及 Teams 深度集成，实现工具间无缝工作流，降低集成复杂度。

**Tempus（TEM）入选 ARPA-H ADAPT 项目，提供 CRO 与测试服务，推进精准癌症治疗**

Tempus AI 宣布，其被美国卫生与公共服务部下属的高级研究项目局 ARPA-H 选中，为 ADAPT（Advanced Analysis for Precision Cancer Therapy）项目提供测试及合同研究组织（CRO）服务。

ADAPT 项目旨在通过利用生物标志物开发适应性治疗策略来改善癌症治疗，初期聚焦非小细胞肺癌、乳腺癌和结直肠癌，最终目标为提升患者生存率。

**CoreWeave（CRWV）推出 Serverless RL，使强化学习对 AI 开发更普及**

CoreWeave 推出 Serverless RL，这是首个公开的全托管强化学习（RL）平台，使开发者无需复杂基础设施即可大规模训练 AI 代理。

Serverless RL 整合了 CoreWeave 的 AI 云基础设施及近期收购的 OpenPipe 与 Weights & Biases 工具。平台支持多 GPU 扩展，仅需 Weights & Biases 账户和 API 密钥即可快速部署。通过在集群中多路并行训练，训练速度提升约 1.4 倍，成本较本地 H100 GPU 环境降低约 40%，模型质量不受影响。

该平台降低了企业使用 RL 的门槛，促进 AI 代理持续优化和客户体验提升。早期采用者包括 SquadStack.ai 和 QA Wolf。CoreWeave 此举凸显其推进 AI 基础设施并提供可扩展解决方案的承诺。

**Roblox（RBLX）股价评级上调至中性，用户增长推动**

MoffettNathanson 将 Roblox 评级从“卖出”上调至“中性”，原因是平台上病毒式体验推动用户指标爆发式增长。过去一年，Roblox 股价涨幅超过 200%，其中近六个月涨幅达 120%。

研究公司指出，虽然对 Roblox 估值仍存疑问，但用户活跃度显著改善促使评级上调。公司市值 873 亿美元，营收同比增长 27%，虽未盈利仍交易于高估值倍数。

**Bernstein 上调 Datadog（DDOG）目标价至 170 美元，看好云使用趋势**

Bernstein 将 Datadog 目标价从 147 美元上调至 170 美元，维持“跑赢大盘”评级。公司观察到 Datadog 在夏季回调后反弹，第二季度基础营收（剔除 AI）可能加速增长。

**03.**

**ETF 101**

**ETF 如何复制（Replicate）指数？**

ETF（交易型指数基金）的一个核心承诺就是：你持有的 ETF 能够跟踪某个指数的表现。但“跟踪”不是靠猜的，而是靠工程化的“复制”方法。不同的 ETF 可能采用不同的复制方式，这将直接影响它的成本、偏差（tracking difference / tracking error）、风险特性等。因此，理解 ETF 的复制机制，对选 ETF、理解其优劣非常关键。

**一、ETF 复制指数的基本思路**

“复制指数”在本质上是把指数的组成、权重、收益特征，用一种可操作的方式在 ETF 资产组合中实现。指数本身只是规则或公式（哪些股票、各自权重、调整方式），并不是真实资产；ETF 要做的，是选择一组资产 + 交易策略，使得其组合表现尽量接近那个指数。

在理想状态下，我们希望：

**•**ETF 的回报率 ≈ 指数的回报率

**•**ETF 的跟踪误差（回报差异的波动）尽可能小

**•**ETF 的运作成本 / 交易成本 / 结构风险 要控制得相对较低

不同的市场、资产类别、指数复杂度，决定了完整复制（全复制）并不总是可行或最优，因此出现了几种折中或替代方法。

常见的复制方式可以归为五类，以下分别介绍它们的原理、优缺点与适用场景。

**二、复制方法及其优劣对比**

下面是几种主流的 ETF 复制方式：

1. 物理复制（Physical Replication）：即 ETF 直接买入指数中的标的股票或债券（完全复制或抽样复制）；

2. 完全复制（Full Replication）：即在物理复制中最“纯粹”的版本：买入指数中每一个成分、按其权重完全复制；

3. 抽样 / 优化复制（Sampling / Optimization）：即在物理复制中一种折中方式，只选取部分代表性标的组合（抽样）或通过模型优化（优化复制）；

4. 合成复制（Synthetic Replication / Swap-based）：即ETF 不直接买入指数成分，而是通过与对手方签订掉期（swap），使 ETF 获得指数表现；ETF 自身可能持有一组流动性好的“抵押资产”作为担保；

5. 混合复制（Hybrid / Physical + Synthetic）：即在同一个 ETF 中同时运用物理复制和合成复制的组合策略。

这几种方式并非孤立、互斥，许多 ETF 会针对其目标指数的特性做折中或混合策略。

**三、如何理解不同复制方式对 ETF 效率的影响？**

复制方式会对 ETF 的跟踪误差、跟踪差异、费用、风险等产生重要影响。下面是几个关键考虑点和比较：

**跟踪误差 / 跟踪差异**

**•**物理全复制在理想情况下能够实现最低的跟踪误差（理论上最接近指数），因为组合与指数重合度最高。

**•**抽样 / 优化复制可能因样本选择、权重偏差等引入额外偏差，使得跟踪误差 / 跟踪差异略高。

**•**合成复制在某些情境下能够较好地压低跟踪误差，尤其是在难以物理复制的资产类别（例如跨国、流动性差市场、商品类）中。

**•**然而，合成复制带来的对手方信用风险或合约条款的不利因素，也可能在极端环境下导致较大偏离。

**费用与成本**

**•**物理复制（尤其全复制）因买卖成本、管理成本、交易摩擦等费用较高。

**•**抽样 / 优化复制可以通过减少持仓数量或选择更流动成分来降低交易成本。

**•**合成复制可能在某些市场通过掉期结构降低买卖成本、规避流动性瓶颈，但需要支付合约费或收益差价。

**•**综合来看，低成本、高稳定性的复制方式对于被动 ETF 投资者尤为重要。

**透明度、结构风险与信任**

**•**物理复制方式透明度高，投资者可以清楚看到 ETF 的持仓和结构。

**•** 合成复制方式透明度较低，结构依赖合同、对手方、条款等，投资者需要信任管理方与合约对手方的信用与履约能力。

**极端市场行为**

在市场极端波动、流动性危机或对手方压力阶段，复制方式的表现可能出现较大差异：

**•** 抽样 / 优化复制在极端行情中可能放大偏差，因为样本可能无法有效覆盖全指数的波动。

**•** 合成复制在对手方出现问题、信贷市场踩踏、合约条款冲击时可能遭遇较大不利影响。

**•** 全复制如果流动性严重枯竭或交易成本暴涨，也可能因买卖困难而偏离。

因此，选 ETF 时不能只看“复制方式”一个因素，而是要结合费用、规模、流动性、历史跟踪表现、极端阶段表现等综合考量。

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/006.png)

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/007.png)

排版：夏悦涵

延伸阅读

[![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/008.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518581&idx=1&sn=19aa9f21427f7a9d9b20ca0bf480ac0a&scene=21#wechat_redirect)

深度讨论 Online Learning ：99 条思考读懂 LLM 下一个核心范式｜Best Ideas

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/009.png)

[![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/010.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518502&idx=1&sn=2930195ac8478084ca8d8770c08a4dd1&scene=21#wechat_redirect)

经验时代的 Scaling Law｜AGIX PM Notes

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/011.png)

[![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/012.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518470&idx=1&sn=21efdd5f223ca848235c6d9ce65472b9&scene=21#wechat_redirect)

深度讨论 Pulse：OpenAI 超越 Google之路的开始 ｜Best Ideas

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/013.png)

[![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/014.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518426&idx=1&sn=523497b9f61a5b0c3fc4614ec5cd842f&scene=21#wechat_redirect)

AI X 用户研究：能并行千场访谈的“超级研究员”，正重塑产品决策的未来

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/015.png)

[![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/016.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518339&idx=1&sn=98990578287f19823437707618ddff0e&scene=21#wechat_redirect)

Notion、Stripe 都在用的 Agent 监控，Braintrust 会是 AI-native 的 Datadog 吗？

![](../images/2025-10-13-agi-lu-xian-tu-di-er-jie-duan-you-xi-ji-mo-xing-xun-lian-pm/017.png)
