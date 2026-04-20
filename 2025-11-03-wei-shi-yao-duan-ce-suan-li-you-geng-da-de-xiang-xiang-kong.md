---
title: 为什么端侧算力有更大的想象空间？｜AGIX PM Notes
publish_date: '2025-11-03'
publish_timestamp: 1762171200
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/jzmPUPiAss707Sn0qLpotw
msgid: 1000000449
appmsgid: 2247519139
itemidx: 1
digest: 数据能否快速喂饱 GPU，而不是喂饱算力本身
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxFic5NktA2sJ9jpZyC1DibUDbicwyWafJTS3D2V3KUianwOGe2a7elPBFicF2XoTHuRhRaibyvuD2Vo1qw/0?wx_fmt=jpeg
image_count: 17
archived_at: '2026-04-20T04:41:42+08:00'
---

[![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/002.png)

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/003.png)

[AGIX 指数](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=3570724992708624387&scene=21#wechat_redirect)诞生于我们对“如何捕获 AGI 时代 beta 和 alphas”这一问题的深度思考。毫无疑问，AGI 代表了未来 20 年最重要的科技范式转换，会像互联网那样重塑了人类社会的运行方式，我们希望 AGIX 成为衡量这一新科技范式的重要指标，如同 Nasdaq100 之于互联网时代。

「AGIX PM Notes」是我们对 AGI 进程的思考记录，希望通过学习 Warren Buffett、Ray Dalio、Howard Marks 等传奇投资者们的分享精神，与所有 AGIX builders 一同见证并参与这场史无前例的技术革命。

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/004.png)

**PM Notes**

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/005.svg)

**Edge that Come to the Center**

作者：Max

当智能无比廉价和商品化之后，什么才是最有价值的，答案其实从来不只是模型本身。

最贵的总是瓶颈的部分，从 AI 产业爆发开始，大家的焦点集中在算力，所以有了英伟达的巨大爆发。因为原子总是比比特慢，软件复制的速度远远超过芯片蚀刻的速度。紧接着 Satya 在 BG2 的 podcast 谈到，微软当前最大的问题不是芯片供应，而是缺乏足够的电力和物理空间来安装和运行所有 AI GPU。他指出，实际上微软手里有不少 AI 芯片因为没有地方插、没有足够 power，甚至只能暂时闲置。Satya 强调，目前不是芯片不够用，而是“没有足够的‘warm shell’（能立刻布置 GPU 的可用数据中心空间）”去扩展算力，这直接限制了 AI 业务的规模和增长速度。所以我们看到了电力，能源和数据中心空间相关的公司的热炒。

最近，市场持续聚焦“内存瓶颈”，主要因为 AI 算力升级过程中，内存（尤其是高带宽内存 HBM）已经成为限制模型训练与推理效率的关键硬件短板。随着大模型参数规模、上下文窗口持续膨胀，在实际推理阶段，对内存容量和带宽的需求远高于以往 GPU 计算。“内存墙”现象凸显，大量 GPU 算力被闲置，核心瓶颈变成：数据能否快速喂饱 GPU，而不是算力本身。

Sandisk 的 HBF 技术尝试用闪存做“准主存/内存级存储”，解决 HBM 容量瓶颈，并通过新架构赋予闪存更高带宽、低延迟，能承载部分“热数据”外延分布式推理需求，有效补充 HBM 不足。Seagate 的 HAMR 硬盘聚焦“冷数据”，由于训练语料库、历史推理结果、日志归档等场景，产生“冷数据”大量堆积，需要强大而便宜的大盘来集中管理和召回。以上都是瓶颈导致的暴涨。 继续往前推演，如果数据中心空间也解决了，我们有了云端超强的计算能力，行业的瓶颈是什么？

黄仁勋在 DC GTC 期间宣布，英伟达已经与通信设备巨头诺基亚达成深度战略合作。诺基亚将在其未来基站系统中集成 NVIDIA ARC 解决方案，该平台将赋能机器人精准操控与高精度气象预测等关键应用。英伟达还计划将其商用级 AI-RAN 产品整合至诺基亚领先的无线接入网（RAN）组合中，使通信服务商能够在英伟达平台上部署 AI 原生的 5G-Advanced 和 6G 网络。

通过这种合作，我们大概可以窥测，下一个瓶颈显然来自于一个端侧 AI 的未来：一方面如何加强用户端侧的算力，保障更低的延迟，无论在 2B 例如医疗、金融和自动化等领域的实时决策辅助，还是个人用户的编程“心流”、娱乐交互的沉浸程度还是保障自动驾驶、机器人的安全可靠。另一方面是用户侧和云端的带宽和连接，通过架构上的创新例如 AI-RAN 实现更适应和支持 AI 原生应用的通信能力，打破“云独大”格局，支持本地实时 AI 推理和决策。也具备了更高速的数据传输、更高的流量承载效率、超低时延、以及动态按需适配各类复杂 AI 与实时业务场景的能力。

为什么端侧的算力有更大的想象空间和必要性？

Andrej Karpathy 在反驳 Sutton 的文章里谈到，动物（比如马）的智能和目前人工智能模型以及人类智能有本质区别，其中之一就是生物智能具备“边缘计算”能力，不是所有能力都需要通过大脑统一处理。比如反射和本能，这些处理在身体的神经网络“边缘”完成，马可以在受惊时迅速逃跑、完成复杂的运动协调，这往往靠的是进化内置的本能，而不是意识驱动的决策。这种机制与技术上的边缘计算类似：数据和响应在离传感器最近的位置处理，减少延迟和能耗。

马斯克在 Joe Rogan Podcast 上谈到，边缘节点处理本地推理并与服务器协作不是可选的。这是唯一在架构上可行的前进路径。如果我们按照他习惯的第一性原理去思考：业界一般按照运营级 4K 流媒体每路约 25-50 Mbps 带宽需求进行设计。按照较保守的 25 Mbps/用户和 2023 年 997 Tbps（即 997,000,000 Mbps）海底光缆总带宽来算，理论最大同时 4K 流用户约为 39,880,000（约 4000 万），但这是理想物理极限，并未考虑各级骨干、地区网络瓶颈和流量交互冗余等实际因素。而这个用户量级远不能支撑目前的 ChatGPT 用户体量，更不要提类似微信这样的超级 APP 用户量级。所以完全由服务器端进行渲染和计算将需要不切实际的数据传输率，可能超出现有全球带宽容量，所以端侧 AI 的这部分感知和计算让互联网和云去处理是不现实的。

在模型侧，我们也在向着更小更节能的方式不断推进，这符合物理原则。能量转移过程总是以“作用量最小”的路径进行，而最节能的过程总是最小化无用能量损耗与熵增。例如过去微调模型，我们需要大量的算力。而 Thinking Machines 团队最新成果显示，他们用 on-policy distillation 将小模型在数学推理等复杂任务上的性能推到接近 32B 参数大模型，同时训练步数减少 7-10 倍，FLOPs 和 GPU 小时数减少 9-30 倍，综合训练效率提升达 50-100 倍。

英伟达作为行业最高全局视角的中心，已经开始通过和通信基础设施公司例如诺基亚的合作，在布局下一个端侧和 AI 原生网络架构的未来，当然仍然是以英伟达的计算芯片为核心。Nokia 正把最新 AI-RAN 方案完全迁移到这个愿景上，目标就是实现“每一个基站都是一个本地 AI 数据中心”，而只有能效极高的小模型才能跑通规模化商用场景。当然无论马斯克的未来还是黄仁勋的未来，端侧无疑都是下一步需要重点关注的核心。

**01.**

**上周市场总结**

**美股创历史新高下方向性风险下降，TMT 与 AI 主题承压，欧洲出现净买入**

上周全球股票市场成交放量，美股指数再创新高之际，全球对冲基金却转为净卖出，卖盘集中在美国股市。美国多空基金成为削减方向性风险的主力：一方面加空、另一方面也是少数同时减多的一类，主导了对美股的总体净卖出；而其他策略端小幅增多为主。行业上，资金撤出集中在持仓更拥挤的 TMT 口袋，特别是广义 AI 主题（Broad AI）、七巨头在财报后的相关篮子、AI Tech Beneficiaries 以及 AI Power 等，此前净敞口已基本回到近 12 个月峰值水平，因此成为本轮减配重心；同时，10 月上旬刚明显降空的板块再度被“加压”做空，尤以无盈利科技与高空头占比篮子为代表。

与之相对，资金在医疗保健与可选消费上转为净买入，且这两大板块的净仓位均接近谷底水平，工业与材料亦见温和买盘，整体呈现自拥挤龙头外向更分散资产扩散的早期迹象，但大盘科技与 AI 仍是投资组合中的最大权重。从季节性看，10 月下旬至 11 月上旬通常是美国多空基金为年末降总杠杆的起点，而在净杠杆仍靠近 12 个月高位、空头端明显变轻的背景下，过去一周在多头侧观察到的减仓，具有延续至随后几周的可能。区域维度，欧洲成为唯一净买入的地区，增量主要来自加多，且集中在医疗保健与金融；从集中度看，欧洲长仓集中度自短期低点明显回升至近一年第 31 百分位。亚太方面，名义规模较为平静：资金继续卖中买台，日本小幅净卖出。

杠杆结构方面，美国多空基金净杠杆降至 56%（环比 -2pct，长期分位 76%），总杠杆回落至 213%（环比 -2pct，长期分位 99%）；欧洲净杠杆升至 49%（环比 +2pct），总杠杆 170%（环比 -2pct）；亚洲净杠杆 71%（环比 +2pct），总杠杆 141%（环比 +1pct）。整体而言，全球资金在美股创新高背景下继续降低方向性风险，但节奏以结构性、拥挤度导向的再平衡为主。

**全球对冲基金表现稳健分化，美股 L/S 小幅回撤，拥挤多头相对空头年内超额延续**

绩效层面，尽管美股大盘走强并叠加因子波动，上周全球基金总体抗住冲击：截至 10 月 30 日，全球平均基金上周上涨约 14 个基点，但美国多空基金上周跌约 10 个基点，其中周四单日约 -50 个基点，主要来自超大盘科技回落；月度来看，全球基金本月上涨约 71 个基点，仅捕捉 MSCI 涨幅（+2.1%）的一部分，美国多空基金月内 +93 个基点，略低于该组 10 月份大部分时间所维持的净杠杆水平（中高 50 区间）；年初以来，全球平均基金 +10.4%，美国多空基金 +11.4%，对比 S&P 500 +17.2%。

欧洲与亚洲分化：欧洲平均基金本月仅 +60 个基点，显著落后同期 SXXP +3.1%；亚洲基金本月 +1.2%，其中中概/中国多空基金 +2.2%（对比 MSCI Asia Pacific +3.8%）；年内欧洲 +9.7%，亚洲 +14.8%，中国多空基金以 +22.4% 领跑各大群体。拥挤度方面，北美 Top 50 多头相对空头上周超额约 +2.0%，月内约 +3.7%，年内约 +20.4%；分地区看，北美上周多减空利差约 +1.96%，欧洲约 +1.96%，亚洲约 +1.27%，均跑赢各自基准，显示在龙头回调与再平衡环境下，拥挤多头的累计优势仍在但边际扩张趋缓。

**02.**

**AI Alphas**

**亚马逊（AMZN）计划裁减约 3 万个企业职位，创下近年来最大规模**

据路透社报道，亚马逊计划自上周二起裁减约 30,000 个企业职位，这将是该公司自 2023 年以来规模最大的一次裁员行动。此次裁员将波及人力资源、设备与服务、运营等多个部门。这一数字超过了 2022 年末开始的 27,000 人裁员规模。近年来亚马逊已在多个部门进行小规模裁员，今年 1 月曾在通讯与可持续发展部门削减少量岗位。CNBC 报道指出，亚马逊 CEO 安迪·贾西在内部备忘录中明确表示，随着公司加速部署 AI 智能体，未来对企业职位的需求将持续减少。该举措反映了亚马逊在人工智能技术规模化应用背景下，对组织架构进行的战略性调整。

**澳大利亚监管机构起诉微软（MSFT）未及时告知 Microsoft 365 Copilot 涨价选项**

澳大利亚竞争与消费者委员会（ACCC）已对微软公司提起诉讼，指控其在向 Microsoft 365 生产力套件部署人工智能功能时存在误导消费者行为。监管机构指出，微软在向个人和家庭版订阅用户推出 Copilot AI 助手并分别上调价格 45%和 29%后，未能明确告知 270 万澳大利亚自动续订用户可以选择不含 Copilot 的经典版本以维持原价。ACCC 主席 Gina Cass-Gottlieb 强调，微软的通信方式剥夺了消费者做出知情选择的权利。诉讼还揭露用户必须启动订阅取消流程才能访问更便宜的经典版本。若被判违反竞争法，微软可能面临相关期间调整后营业额 30%的罚款。微软回应称将详细审查指控，并承诺与监管机构建设性合作。此次诉讼是微软 365 套件近期面临的又一监管挑战，去年欧盟曾就其捆绑 Teams 行为认定违反反垄断规则。

**苹果（AAPL）、微软（MSFT）市值双双突破 4 万亿美元**

科技巨头苹果与微软市值双双突破 4 万亿美元大关，创下资本市场里程碑。苹果首次跻身 4 万亿美元俱乐部，成为继英伟达和微软之后第三家达成此成就的企业。其股价飙升得益于 iPhone 17 系列超预期的市场表现，公司将于 10 月 30 日公布 2025 财年第四季度财报。微软则凭借与 OpenAI 的新合作协议重返 4 万亿美元市值，其 Azure 云服务因提供 OpenAI 大模型及算力需求持续增长。微软披露对 OpenAI 约 27%的持股估值达 1350 亿美元。与此同时，谷歌母公司 Alphabet 以 3.25 万亿美元市值逼近这一历史性门槛，反映出人工智能浪潮对科技巨头估值的强劲拉动。

**Super Teacher 推动 AI 普惠小学辅导，确定性系统提升准确性，技术创新受谷歌（GOOGL）前高管加持**

教育科技初创公司 Super Teacher 正在通过 AI 技术推动小学辅导普及化，其开发的 AI 辅导应用月费仅 15 美元，远低于传统辅导数百至数千美元的费用。该公司由前谷歌产品经理兼教育工作者 Tim Novikoff 创立，目前已吸引约 2 万户家庭注册，并在纽约、新泽西和夏威夷的公立学校投入使用。Super Teacher 采用确定性系统而非大型语言模型生成内容，确保答案准确性，避免 LLM 可能出现的错误。作为 TechCrunch Disrupt 2025 创业竞技场 Top 20 决赛入围者，该公司计划将服务扩展至更多年级，并与更多学区合作。Novikoff 强调 AI 辅导是教师可用的工具而非替代品，其使命是让私人辅导民主化。

**英伟达（NVDA）GTC 华盛顿大会聚焦 AI 基础设施实践，微软（MSFT）、思科（CSCO）等巨头共论产业转型**

英伟达在华盛顿 GTC 大会上展示了其在 AI 基础设施领域的持续领先地位。公司凭借 CUDA 软件平台构建了强大的技术护城河，将 GPU 转化为完整计算平台，并通过合作伙伴生态系统巩固竞争优势。分析师指出，英伟达季度营收达 47 亿美元，年增长率保持在 50%，验证了企业客户对 AI 基础设施的强劲需求。超大规模客户如 OpenAI 正在通过采用更高效的英伟达基础设施来优化运营成本，实现“花得更多、省得更多”的经济效益。大会聚焦于 AI 工厂的实际部署，涵盖推理集群、数据管道和网络架构等关键环节，与会专家将讨论混合供应商策略、容量规划等实操议题。包括 Northrop Grumman、Cisco Systems 等企业高管将分享部署经验，彰显英伟达在推动 AI 从技术概念向产业实践转化的核心作用。

**亚马逊（AMZN）为 Anthropic 打造的 110 亿美元 Project Rainier 数据中心园区正式启用**

亚马逊云科技（AWS）正式启用位于印第安纳州、耗资 110 亿美元的 Project Rainier 数据中心园区，该设施专为 AI 公司 Anthropic 设计，将运行其人工智能模型的训练和推理工作负载。目前园区已部署 7 栋建筑，容纳近 50 万颗 AWS Trainium2 芯片，预计到年底将超过 100 万颗。AWS 计划进一步建设 23 栋建筑，使园区总容量超过 2.2 吉瓦。亚马逊自 2024 年初已向 Anthropic 投资 80 亿美元，后者不仅使用 AWS 基础设施运行核心工作负载，还为 AWS 的 AI 基础设施优化提供技术支持。AWS Trainium2 处理器采用定制设计的 NeuronCore-v3 核心架构，通过 NeuronLink 互连技术实现高效数据传输。AWS 预计年底推出新一代 Trainium3 加速器，性能将提升四倍。这一大规模基础设施部署旨在帮助 Anthropic 与 OpenAI 竞争，后者计划部署 33 吉瓦数据中心容量，并采用英伟达、AMD 的 GPU 及自研 AI 芯片。

**AMD（AMD）推进软件定义 AI 工厂战略，通过 ROCm 软件栈重塑数据中心架构**

AMD 正积极推进软件定义 AI 工厂战略，通过构建全栈计算平台重新定义数据中心架构。公司副总裁 Anush Elangovan 在 theCUBE + NYSE Wired 活动上透露，AMD 已将战略重心从硬件代际交付转向软件层开发，其开源的 ROCm 软件栈成为核心支撑，可在 EPYC 处理器、Instinct GPU 和 Pensando 网卡上创建标准化计算层。技术突破体现在新推出的 Helios 机架级超级计算机，单机架集成 72 个 MI450 GPU，提供 1.4 exaFLOPs 的 FP8 算力，配备 31TB HBM4 内存和 19Tb/s 带宽，支持吉瓦级部署。这种软硬件深度融合的架构将可靠性、安全性内置于平台底层，通过开放生态吸引开发者参与创新，为从超大规模云到边缘设备的全场景 AI 工作负载提供支撑。

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/006.png)

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/007.png)

排版：夏悦涵

延伸阅读

[![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/008.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247519112&idx=1&sn=562af823af24b984bc3c0242c389caa8&scene=21#wechat_redirect)

Coatue 最新报告：复盘 400 年、 30+ 次泡沫，我们离 AI 泡沫还很远

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/009.png)

[![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/010.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247519023&idx=1&sn=54a12b29668ca5b99582d8d4b931125f&scene=21#wechat_redirect)

领投 Ilya 新公司，13 年净 IRR 33%，Greenoaks 的科技投资哲学

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/011.png)

[![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/012.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518893&idx=1&sn=d97353a4eaff11bf3a12a3712ca328db&scene=21#wechat_redirect)

RL 是新的 Fine-Tuning

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/013.png)

[![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/014.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518860&idx=1&sn=033bb7b4db2d36c742d68acaf4218dd0&scene=21#wechat_redirect)

SemiAnalysis 创始人解析万亿美元 AI 竞争：算力是 AI 世界的货币，Nvidia 是“中央银行”

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/015.png)

[![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518822&idx=1&sn=d6b378e1e41e739fe132926b3cd4565f&scene=21#wechat_redirect)

告别 260 亿美元低效投入，HappyRobot 为物流业配置 “AI 调度员”

![](../images/2025-11-03-wei-shi-yao-duan-ce-suan-li-you-geng-da-de-xiang-xiang-kong/017.png)
