---
title: Agentic Enterprise：生成式软件重新定义企业形态｜AGIX PM Notes
publish_date: '2025-09-22'
publish_timestamp: 1758537146
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/jf-PZIUwrp4deBbqBah1KQ
msgid: 1000000424
appmsgid: 2247518173
itemidx: 1
digest: 企业数据是最好的 RL 环境
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgwyuia0iaQWibJ8oicZW1ADllbwbWBCmnFoaS2MJp8KzAvgibmmibiajDPSLugmjBVg0aMdRhG5st64KJB7Q/0?wx_fmt=jpeg
image_count: 18
archived_at: '2026-04-20T04:25:47+08:00'
---

[![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/002.png)

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/003.png)

[AGIX](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=3570724992708624387&scene=21#wechat_redirect) 指数诞生于我们对“如何捕获 AGI 时代 beta 和 alphas”这一问题的深度思考。毫无疑问，AGI 代表了未来 20 年最重要的科技范式转换，会像互联网那样重塑了人类社会的运行方式，我们希望 AGIX 成为衡量这一新科技范式的重要指标，如同 Nasdaq100 之于互联网时代。

「AGIX PM Notes」是我们对 AGI 进程的思考记录，希望通过学习 Warren Buffett、Ray Dalio、Howard Marks 等传奇投资者们的分享精神，与所有 AGIX builders 一同见证并参与这场史无前例的技术革命。

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/004.png)

**PM Notes**

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/005.svg)

**Agentic Enterprise**

作者：Max

软件正在从静态的代码集合演化为能够持续学习和自我优化的“Living Software”。这种转变的核心在于建立一个可扩展的环境，能够捕获用户信号、转换为奖励、启动训练任务并将模型快速重新部署到生产环境，从而实现软件的自我改进。

传统软件通常是静态发布、功能固定的代码集合，而“Living Software”则能根据用户反馈不断进化。在编程助手工具 Cursor 的 Tab 补全功能中，我们看到了这一理念的实践：Cursor 引入在线强化学习（Online RL）对代码自动补全模型进行持续优化。通过实时采集开发者对代码建议的接受/拒绝反馈作为奖励信号，通过策略梯度方法调整模型，让模型逐渐避免产生低质量建议。效果是显著的——升级后的 Tab 模型建议数量减少了21%，但建议的接受率提升了28%。Keen Technology 的 Khurram Javed 评价，这是业界首次大规模展示实时强化学习优势的成功案例，模型只要有用户使用就能无限适应下去。

在构建“Living Software”的架构时，一个更为根本的问题浮现：在这个[“经验时代”（Era of Experience）](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512336&idx=1&sn=f149c8f599f037377f0e75a0111a9c7d&scene=21#wechat_redirect)，高质量的环境可能比算法本身更重要。换言之，AI 模型比拼的是参数规模和算法效率，但同时也比拼的是它所汲取经验的环境质量。正如 Elon Musk 反复强调的，“真实世界才是唯一重要的奖励信号”。

企业或组织正成为“Living Software”理想的训练环境。而且有点反直觉的是，不完全是模型能力决定了经验时代的胜负，在“Living Software”时代，B2B 业务拓展（销售、合作）能力可能比单纯的AI算法能力更为重要。

最高质量的训练环境掌握在企业手中，而获取这些环境的访问权更像一个商业问题而非技术问题。再先进的模型架构，如果无法说服企业让你接入他们的核心业务流程、获取真实反馈数据，你的 AI 系统就只能在次优环境中“学习”。

反之，如果能打入顶级企业场景，哪怕只是为咨询公司生成 PPT 这样的用例提供AI支持，其训练得到的能力密度也远高于面向普通消费者的琐碎场景。伟大的技术往往诞生于最高要求的用例：在最苛刻环境中通过反复试错脱颖而出，这本身也是一种更高质量的强化学习环境。由此可以预见，谁能拿下企业场景，让自己的 AI 代理在真实业务中学习，谁就能建立难以超越的竞争壁垒。

同时，训练范式的转移也为这种未来奠定了技术基础。过去模型发展“大即是好”的思路已走向瓶颈。GPT-5 不再是一味追求一个巨无霸模型处理所有请求，而是根据任务难度在不同规模的模型间智能路由。GPT-5 Codex 更进一步，其核心设计包括自动“推理时长”调整：简单请求快速完成，复杂任务则让模型“思考”更久，进行深度代码分析和多轮自动迭代。这种变长推理方式（“adaptive thinking duration”）是在模型内部通过训练形成的，不是通过一个单独的“外部路由器”实现显式模型切换。

而“体验时代”也是“AI 部署”（AI deployment）时代，预训练大模型固然重要，但更关键的是将智能做成有用的产品来建立价值数十亿或数万亿美元的公司，并且在真实应用场景下做实现模型/产品的持续学习。而这么做的成本也在持续降低，根据 DeepSeek 在 Nature 上发布的论文，R1的模型只用了 $294,000 美金的训练成本。成本的断崖式下降意味着：

第一，软件公司都会选择训练自己的模型，而基于 API 的大模型商业模式会遇到极大的挑战。例如 Stripe 也训练了全球第一个为支付而建的基础模型。Stripe 目前处理超过 1 万亿美元的年支付量，86% 的卡片此前已被 Stripe 见过，这为其基础模型提供了独特的数据优势 。该模型现已部署到整个 Stripe 支付套件中，为授权、欺诈检测、交易争议等领域带来新的性能提升 。

第二，数据资源和经验回放（trajectory replay）将成为核心竞争点。企业有望不断累积和复用自有业务数据，包括人与 AI 交互的轨迹、业务流程日志等。这种数据飞轮一旦建立，后来的竞争者将难以复制同样的效果，因为真正宝贵的是多年沉淀下来的隐性知识。我们可以想象一个不远的将来，每家公司都拥有属于自己的专用大模型，通过持续的在线学习和周期性的参数更新，时刻优化着企业的决策和流程。

在业务前台或产品本身被模型“学习”的同时，企业运营的流程也可以提取蕴含的业务逻辑和决策模式，用 AI 予以自动化。往往企业工作流是历史路径依赖的产物：受到当时技术工具、组织结构、沟通手段乃至管理者认知的限制，许多流程是当时的局部最优，并非全局最优，甚至从来没有再迭代过。而 AI 系统则没有这些桎梏。面对复杂的流程组合，AI 可以尝试人类难以想象的方案，从中发掘隐藏的高效路径。

未来企业形态，可能正如 Mercor 联合创始人 Brendan Foody 所言，将类似于一个“强化学习环境机”。人类不再重复性劳动，而是一次性创造知识、教会 AI，然后让AI 代理去大规模复制和执行。企业扩张不再线性依赖于人力增长，而更取决于能否把关键流程数字化、模型化，通过训练“AI 员工”来实现指数级的可复制性和规模化。在这样的图景下，人类角色也发生转变——员工变成了 AI 的教练和反馈提供者，新工作的重点在于设计环境、设定奖励、监督 AI 表现。这与工业革命催生出新的职业类别如机器操作工类似，只不过这次新涌现的角色将是“AI 训练师”、“流程设计师”等等。

总之，Agentic Enterprise 不仅仅是技术上的概念，更是未来企业组织形态的一次跃迁。那些率先拥抱“Living Software”理念、善用真实环境塑造 AI、敢于重塑自身流程的公司，将引领下一个时代的商业版图。

**01.**

**本周市场总结**

**对冲基金继续在美国以外的半导体板块加码，美国小盘股遭抛售**

在市场聚焦美联储下调 25 个基点利率的背景下，对冲基金的资金流动相较股市的持续反弹显得不那么积极。对冲基金小幅净买入全球股票，规模相当于约 0.4z 的周度事件，且大部分买入力度来自日本以外的亚洲市场。至于北美市场，多空两端的资金流相对平淡，但在小盘股反弹的背景下，内部仍有明显的板块轮动。

更深入来看，北美地区对冲基金最终成为净买方，推高了整体净杠杆至 57%，这是自 2022 年初以来的最高水平（仅在 2024 年初夏的短暂时期曾触及类似水平）。

总杠杆仍保持高位，不过在美股轮动过程中，并未观察到大规模的减仓动作。多数单一行业呈现净卖出，其中科技板块领跌——半导体成为美国市场中被卖出最多的行业。不过值得注意的是，在该板块表现强劲后，对冲基金于周四转而买入。

TMT 其他子板块表现分化，硬件最终净买入，而软件则净卖出。除科技外，对冲基金一周内还减持了公用事业与房地产。买入力度主要集中在必需消费品及医疗保健（医药与生物科技）。

此外，ETF 空头回补也在一定程度上抵消了净卖出倾向，因股市整体持续走高。因子层面上，对冲基金延续近期趋势，继续向更偏向防御的组合倾斜，显著买入质量因子与规模因子。

美国以外的买入力度更强，主要由日本以外的亚洲市场驱动。韩国成为对冲基金买入的核心市场，中国与台湾也有所贡献。三国的交易焦点集中在 AI 相关板块，半导体与硬件位列净买入最多的行业，电商亦受到青睐。主要流向集中于新增多头头寸，其中对韩国 AI 受益股的敞口创下追踪数据以来最高水平，而台湾半导体的净敞口也处于高位。在欧洲，对冲基金亦录得小幅净买入，其中半导体同样贡献最大。此外，软件与奢侈品亦受到增持，国防、机械、电气设备等主题亦是买入亮点。

**AGIX 周上涨幅度平均超三大指数两倍以上，全球对冲基金稳步上涨，美洲多空基金在 9 月反弹中表现突出**

本周 AGIX 上涨 3.11%，跑赢三大指数：标普 500 +0.74%、QQQ +1.30%、道琼斯 +0.94%。对冲基金整体表现方面，全球平均基金本周上涨 50 个基点，捕捉到 MSCI 上涨 75 个基点中的相对较高比例。美洲地区的多空基金更是跑赢标普，本周上涨 105 个基点，而标普同期涨幅为 74 个基点。按月度来看，全球平均基金上涨 1.7%，MSCI 上涨 3%；年初至今，全球基金上涨接近 9%。美洲多空基金本月平均上涨 2.2%，年初至今上涨 10.4%。其他地区方面，欧洲与亚洲的多空基金本周均录得接近 30 个基点的涨幅。欧洲多空基金本月上涨 1.3%，年初至今上涨 10%；亚洲基金本月上涨 3%，年初至今上涨 15.5%，主要受益于近期中国市场反弹。

**02.**

**AI Alphas**

**Nvidia （NVDA） 投资 Intel （INTC）50 亿美元**

Intel 在上周四（9 月 18 日）股价大幅上涨，创下历史新高。Nvidia 将出资 50 亿美元并与 Intel 合作开发 AI 基础设施与个人计算机产品后，大量买入 Intel 股票。盘中一度触及 52 周高点 32.38 美元，最终收于 30.57 美元，上涨 22.77%。

Nvidia 在声明中表示，公司以每股 23.28 美元收购 Intel 股票，总额 50 亿美元。交易需满足监管审批等惯常交割条件。此次投资同时伴随两家公司承诺共同开发多代数据中心与 PC 定制产品，加速超大规模、企业级及消费级市场的应用与工作负载。

此外，Intel 与 Nvidia 还将通过 NVLink 技术无缝衔接各自架构，结合 Nvidia 的 AI 与加速计算优势和 Intel 的 CPU 技术及 x86 生态系统，为客户提供先进解决方案。

在数据中心领域，Intel 将为 Nvidia 打造定制 x86 CPU，后者将其整合至自家 AI 基础设施平台并推向市场。在个人计算领域，Intel Corp。 将开发并销售整合 Nvidia RTX GPU chiplet 的 x86 SoC。新一代 x86 RTX SoC 将支持对 CPU 与 GPU 高度整合有强烈需求的多种 PC。

**OpenAI 计划五年投入 1000 亿美元租用备用服务器**

据 The Information 上周五（9 月 19 日）报道，OpenAI 计划未来五年花费约 1000 亿美元，从云服务商处租用备用服务器。这笔投入是在该公司此前预计至 2030 年将为云服务器租赁支出 3500 亿美元基础上的新增部分。

报道称，考虑到备用服务器在内，OpenAI 平均每年将为服务器租赁花费约 850 亿美元。公司高管在与股东的讨论中表示，这些备用服务器具备“可变现性”，未来有助于带来额外收入，不论是通过科研突破还是产品使用激增。

OpenAI 此前预计至 2029 年现金消耗将达到约 1.15 万亿美元，以支持其大规模 AI 模型的开发。

**Alphabet （GOOGL） 宣布在英国投资 50 亿英镑并新建数据中心**

据路透社上周二（9 月 16 日）报道， Google 将在英国投资 50 亿英镑（约 68 亿美元），时机恰逢美国总统 Donald Trump 访问该国。此次访问预计将促成多项新商业交易与合作。

Google 同时宣布将在伦敦附近建设一座新数据中心，以满足 Google Cloud、Search、Maps 以及 Workspace 等 AI 服务快速增长的需求。

**Oracle （ORCL） 与 Meta （META） 商谈 200 亿美元云计算协议**

据路透社上周五（9 月 19 日）援引知情人士消息，Oracle 正与 Meta 洽谈一份规模约 200 亿美元的多年期云计算协议。这一合作将为 Meta 的 AI 模型训练与部署提供算力支持，补充其现有的云计算供应商。

该潜在交易消息传出一周前，华尔街日报报道称 OpenAI 已与 Oracle 签署合同，在未来五年采购约 3000 亿美元算力，成为有史以来规模最大的云服务合同之一。

Oracle 近年来已与 Amazon、Alphabet 与 Microsoft 建立合作，使其云客户可在原生服务基础上运行 Oracle Cloud Infrastructure。相关合作收入在第一季度增长超过 16 倍。

公司上周宣布签署四份数十亿美元的合同。随着 OpenAI 与 xAI 等企业积极扩展算力储备以保持 AI 竞赛领先，Oracle 预计未来几个月还将新增多位百亿美元级客户，并称其 OCI 业务预订收入将在未来超过 5000 亿美元。

**CoreWeave （CRWV） 获 Nvidia （NVDA） 63 亿美元订单**

上周一（9 月 15 日），CoreWeave 股价上涨近 8%。公司披露与 Nvidia 签订了一份 63 亿美元的订单合同，其中 Nvidia 承诺至 2032 年 4 月前收购任何未售出的算力容量。该交易凸显 CoreWeave 对 Nvidia GPU 的深度依赖，也进一步巩固双方战略合作关系。Nvidia 目前持有 CRWV 约 7% 股份。

尽管 CoreWeave 仍处于亏损状态，但营收正稳步增长。随着 OpenAI 等大客户支持的数十亿美元级合同落地，市场普遍预期 CRWV 股票仍具上升空间。

**Meta （META） 在 Connect 大会发布新款智能眼镜**

Meta 在年度 Connect 大会上发布了新一代智能眼镜。首席执行官 Mark Zuckerberg 公布公司首款面向消费者的智能眼镜。这款产品在公司内部代号为 “Hypernova”，对外预计以 “Celeste” 推出。眼镜右侧镜片内置小型显示屏，可显示通知等基础功能。

新产品功能不及去年展示的 “Orion” 原型，后者曾被 Zuckerberg 称为“通往未来的时光机”。Meta 计划在 2027 年正式推出 Orion。

**03.**

**ETF 101**

**ETF 101：如何理解 ETF 的流动性？**

对于想要投资 ETF 的投资者来说，“流动性”常被提到，却常常被误解。理解 ETF 的流动性，不仅能帮助你更好地选 ETF，也能在买卖之中减少成本与风险。下面我们来一步步拆解。

**什么是流动性？**

**•**流动性指的是一个资产在希望的时间内、以一个合理价格被买卖的难易程度。

**•**对于 ETF 来说，流动性强意味着你可以在交易所里迅速买入或卖出，不用大幅降低价格，也不用等太久。

**为什么这很重要？**

**•** 如果流动性差：想卖 ETF 时可能要降价才能找到买家，或者形成“买卖价差”（bid-ask spread）大，成本提高。

**•**流动性强的 ETF 更安全、交易成本也低，对于普通投资者来说更放心。

**常见误区：成交量与规模是不是流动性的全部**

误区 1：成交量 = 流动性

虽然成交量大通常是流动性好的一个信号，但成交量只是“过去或历史上成交的量”。它并不一定代表你在某一天、某个时间点能以合理价格成交大额交易，仅看成交量可能“只看到冰山一角”。

误区 2：资产规模越大流动性越好

这也是常被认为成立的观点——通常规模大的 ETF 确实更受人关注，投资者多。但规模大并不自动保证在某些时间里交易活跃或者买卖价差小。规模只是一个参考指标之一。

**ETF 的流动性有哪些组成部分？如何全面评估？**

要全面理解 ETF 的流动性，不只看成交量或规模，最好从多个维度来观察。以下是关键组成部分和可用指标：

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/006.png)

**一个具体例子说明：隐含流动性 vs 表面成交量**

假设某只 ETF 的隐含流动性大约为 6,149 万份额，折合港币约 4.5 亿港币／日，而其在交易所屏幕上看到的日成交量只有 75.9 万股。如果只看成交量，你可能低估了它可以支持的交易规模，误以为流动性很低。

**投资者在选 ETF 时应该怎么做：实用建议**

基于上述理解，以下是普通投资者在选 ETF 或在买卖 ETF 时可以采用的一些实用步骤／思考方式：

1. 先看你关心的标的／策略

如果你选的是比较冷门的细分主题、行业或是某些定制指数类产品，本身标的资产流动性可能就比大盘类弱。

2. 查 ETF 的成交量与换手率

用你的证券／行情软件看这只 ETF 最近几个月的日均成交量、换手率；看成交量有没有很多零星波动／是否稳定。

3. 观察盘口（买卖委托）情况

开盘、中午、收盘时段，买卖价格间隔（点差）如何／挂单厚度如何。

4. 看折溢价与 IOPV（或 NAV）

知道 ETF 的净资产值／参考净值，并比较与市场价格是否经常偏离以及偏离程度。

5. 了解 ETF 的“创建赎回机制” & 发行人的支持度

好的 ETF 发行人通常有强大的资本市场支持、流动性提供者网络、透明披露标的。这样在你进行大额交易或市场波动时更有保障。

6. 不要单纯追求成交量大或规模大

虽然这是正面的因素，但关键是看这些指标配合买卖成本、折溢价、盘口结构等是否良好。

**风险提示与注意事项**

**•** 即使流动性好的 ETF，也有可能在市场极端情况下（如重大新闻、市场恐慌、资金流出快速）出现买卖困难或折溢价扩大。

**•** 对于大额交易者（机构或个人打算一次性买／卖很多），可能无法完全通过二级市场成交，需要考虑分批交易或调动一级市场机制。

**•** ETF 内部的标的资产如果跨市场／跨币种，可能涉及货币风险、结算时间、市场规则差异，这些也会影响实际流动性。

**总结**

ETF 的流动性不只看成交量，也不只看规模；还要看标的资产的流动性、买卖盘口情况、折溢价情况、市场结构（做市商、一级市场机制）等。

理解这些，能帮助你在选 ETF 的时候更有把握，也能在买卖 ETF 的时候减少隐性成本，保护自己的投资收益。

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/007.png)

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/008.png)

排版：夏悦涵

延伸阅读

[![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/009.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518145&idx=1&sn=c4603e0ee1c1a45a0bcd4c1eafd4e016&scene=21#wechat_redirect)

Stripe x Cursor，硅谷两代“金童”对谈: 未来5年IDE里将不再是代码

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/010.png)

[![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/011.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518120&idx=1&sn=6f4e7c983c66e5a5c2b84be206ab223e&scene=21#wechat_redirect)

超越 Prompt 和 RAG，「上下文工程」成了 Agent 核心胜负手

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/012.png)

[![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/013.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518031&idx=1&sn=bb6cada95f0ffbb951f6bdcc21663afa&scene=21#wechat_redirect)

一半美国医生都在用的AI产品，OpenEvidence 是医疗界的 Bloomberg

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/014.png)

[![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/015.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517863&idx=1&sn=ebf449b114d7325f15247ad28ddddd61&scene=21#wechat_redirect)

Vibe Working：AI Coding 泛化的终局想象｜AGIX PM Notes

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/016.png)

[![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/017.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517781&idx=1&sn=22cb82ed020d508c26cb0be9187300ee&scene=21#wechat_redirect)

Cloudflare 的 AI 新叙事：线上内容“做市商”，Agent 互联网流量基建

![](../images/2025-09-22-agentic-enterprise-sheng-cheng-shi-ruan-jian-zhong-xin-ding/018.png)
