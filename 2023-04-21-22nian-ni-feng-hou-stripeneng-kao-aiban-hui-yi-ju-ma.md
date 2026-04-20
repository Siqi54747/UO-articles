---
title: 22年逆风后，Stripe能靠AI扳回一局吗？
publish_date: '2023-04-21'
publish_timestamp: 1682079473
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/WOEZPNnZo2Vip71SLAdmsw
msgid: 1000000192
appmsgid: 2247501768
itemidx: 1
digest: Collison兄弟因为自己的天马行空亲手错过了Stripe的最佳结局。
cover: https://mmbiz.qpic.cn/mmbiz_jpg/3tHNibnJ2jgydlib7xhGbiaHIdh6kNUo3H4ibaRkKicjickB7T9Lod0yzOOibg7XSNT0U4ib78NhMtV6yAmRentzXAzy6Q/0?wx_fmt=jpeg
image_count: 25
archived_at: '2026-04-20T01:01:58+08:00'
---

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/001.gif)

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/002.png)

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/003.png)

作者、编辑：程天一

排版：Ziyu

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/004.png)

Stripe 现在是一家估值 500 亿美元的公司。

疫情来了之后，Stripe 其实一直是大赢家。它是疫情期间现金储备最充裕的公司，因为 Will Gaybrick 迅速在 20 年 4 月帮助 Stripe 以 360 亿美元估值从 a16z、General Catalyst 和 Sequoia 那里募了 6 亿，这让 Stripe 顺利度过了疫情，又按 950 亿美元融了一轮，更激进地投入了软件套件以及国际化扩张，在过去 3 年实现了 6000 亿美元的 Net New TPV。

Collison 兄弟为 Stripe 规划的远大目标是成为一家万亿美元级别的公司，所以它需要做软件、重构内部基础设施、扩大支付处理的基本盘、增加相匹配的员工人数……**但是他们忽略的前提是，宏观环境不可能一直顺风顺水 —— Stripe 本希望在 22 年跨过万亿 TPV 的大门，但是由于宏观环境和数字经济客户们经营上的逆风，它最终只做到了 8000 亿美元出头，烧了 5 亿美元的净现金只带来了 26% 的增长，Rule of 40 是不及格的 11%。**

某种程度上，Stripe 亲手错过了最佳结局，它应该像 Airbnb 那样在 2020 年上市。Airbnb 的创始人听从了 Bill Gurley 的 push，而 Collison 兄弟则为自己的过度自信和天马行空付出了代价。它的员工们面临着 RSU 到期而公司还没有 IPO 的困境，Stripe 不得不自降估值募集超过 40 亿美元以帮助大家度过这种局面。

我们在上个季度对于 [**Stripe 当前的处境做了深度的追踪和分析**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247491549&idx=1&sn=425fccb5c05707d1fede32fffaa8157d&chksm=ce98a043f9ef295516575028dc5d6cd3723375bea84f5edc0e748d2b0e46970cecd8e5e57d2c&scene=21#wechat_redirect)，而它也保持了去年开启的传统，发布了 2022 年度 Update。结合 The Information 对它泄露的融资 Deck 的报道，**我们可以使用纯公开信息将拾象内部的 Update Memo 进行脱敏并开源分享出来，以帮助我们的读者对这个全球最大的 Fintech 独角兽的现状有更深入的了解。**

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 泄露的融资 Deck

02 Devil's Advocate

03 否极泰来

**01.**

**泄露的融资 Deck**

**22 年概况**

通过 Stripe 泄露的融资 Deck（由 The Information 发布）和官方发布的 2022 年度信息，读者们可以一窥它在 2022 年的经营状况：

• 8170 亿美元 TPV，同比增长 26%，刨除汇率逆风同比增长 29%；

• 32 亿美元扣除资损前的净收入，同比增长 25%；

• 28 亿美元扣除欺诈资损后的净收入，同比增长 18%；

• 2.8 亿美元支付以外的软件及服务收入，同比增长接近 80%，占总收入的 9%；

• 110+ 个年 TPV 10 亿美元以上的大型企业客户；

• 全年推出了 244 全新的用户功能和 336 个 API 更新；

• 25% 交易量来自非美国客户；

• EBITDA 由盈转亏，22 年烧掉了 5 亿美元现金。

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/005.png)

*Source - The Information*

**核心业务进展**

这部分业务主要指 Stripe 产品线中的 Stripe Payments 和 Connect，即跟支付处理强相关、贡献主要收入的业务，其 TPV 和收入增长主要由以下几个因素驱动，抛开宏观逆风，其实都仍然靠谱：

• **有机增长**：随着已有客户自身的增长而自发增长，Stripe 的大多数 Cohort 表现稳定；

• **通过降低创业成本和复杂性来增加新企业的创建速度**：Stripe 继续保持着对创业公司客户群的高渗透率，享受它们业务增长的红利，并且能维持高的 Take Rate，专门服务公司成立的 Stripe Altas 产品在 22 年的客户数相较 19 年增长了 155%；

• **帮助大型企业适应互联网经济**：Stripe 从 19 年发力以来持续赢得全球大型企业客户，目前能贡献 10 亿美元以上年交易量的客户有超 110 个，每年贡献 100 万美元以上净收入的客户接近 400 个，典型的客户包括 Amazon、PGA、丰田、MAN 和 Maersk 等；

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/006.png)

• **支付在全球范围内的障碍**：尽管目前北美仍然占据 Stripe 70% 以上的 TPV，但是欧洲、亚太和拉美以更高的增速在增长，而且这些地区的综合 take rate 更高。

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/007.png)

*Source - The Information*

**创新业务情况**

这部分业务打包起来贡献了 2.8 亿美元收入的软件及服务收入，体量小，但是长远看相比支付业务其实毛利更高，是 Stripe 未来回报的关键非共识之一，目前的进展是：

• Stripe Issuing 这块儿业务从 18 年启动，可以帮助客户发行实体或虚拟的借记卡，并且通过 Interchange 分成来获得收入，但目前体量还比较小，TPV 是 Marqeta（目前市值从颠覆的 200 亿美元跌到 23 亿美元）的 1/10，不过增速非常快；

• Billing、Invoicing、Revenue Recognition、Sigma、Tax 在内的一系列套件是全村的希望，也是 Stripe overhire 在产研上重兵投入的领域；

• 鉴于对手都拥有自己的双边网络，比如 PayPal 可以作为收单商服务商家也可以作为钱包服务用户，Square 同时拥有 Cash App 和 Afterpay，Klarna、Affirm 也都有端来承载和持续运营用户，Link 是 Stripe 构建商家和用户双边网络的重要布局。它的业务形态是收银台，能保存并自动填充客户的付款和运输信息。

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/008.png)

**02.**

**Devil's Advocate**

从成长期投资视角看，*catching the falling knife* 是件危险的事情。Adyen 仍然是 Stripe 最好的锚，它 TPV 跟 Stripe 差距不大，收入体量在 Stripe 的 1/2 左右，但是 EBITDA Margin 在 50% 以上并且增速保持在 30%，目前它的市值徘徊在 ~400 亿美元。因此 500 亿美元的 Stripe 还缺乏足够的吸引力，我们起码要看 400-450 亿美元区间的机会。下面的内容可以帮助我们客观认知 Stripe 现状：

**崩坏的 Rule of 40**

Stripe 是疫情期间现金储备最充裕的公司，因为 Will Gaybrick 迅速在 20 年 4 月帮助 Stripe 以 360 亿美元估值从 a16z、General Catalyst 和 Sequoia 那里募了 6 亿，这让 Stripe 顺利度过了疫情，并且在过去 3 年实现了 6000 亿美元的 Net New TPV。

但与此同时整个组织规模迅速膨胀，Stripe 的员工总数从疫情前的 2000 人变成 2022 年的 8000 人，让 Stripe 的 GMV/Employee 从跟 Adyen 接近缩水至其 40% 的水平。这种缺乏效率的扩张让 Stripe 的自由现金流从 21 年的正 4.6 亿美元变成 22 年的 5.5 亿美元亏损。

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/009.png)

*Source - All In Podcast*

从基本的 Rule of 40（一家标准的软件公司起码收入增长和 FCF Margin 相加应该等于或超过 40%）角度看，Stripe 已经是一家被玩坏的公司，它有 23% 的增长，但是 FCF Margin 按净收入口径算是 -17%，固定汇率调整后的 Rule of 40 也只有 11%，处于软件公司的后 25% 分位。

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/010.png)

*Source - a16z Growth Metrics Benchmark*

拉出来类似画像的公司看，如果 Stripe 在 20 年上了市，今年这个业绩的 downside 结局就是 Twilio 在 22 年的剧本。Rule of 40 在这个区间的公司的 ARR Multiple 平均数有 5.4x，中位数是 5.5x，也就是说 Stripe 的 downside 大致在 150-200 亿美元。

从这个 downside 的思维出发，我们如果按 400-450 亿美元的估值考虑进入，接受的前提是：

1. 透支了 1 年的增长；

2. 相信管理层能够在 24 年扭转 Rule of 40 的表现，即收入增长仍然维持在 20% 区间，但是 FCF Margin 大幅改善。

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/011.png)

**绝望的融资和死亡螺旋**

根据我们和硅谷朋友的交流，在和 Stripe 关系没那么亲密的硅谷 Fintech 投资人心中：**Stripe 亲手错过了最佳结局，它应该像 Airbnb 那样在 2020 年上市。**Airbnb 的创始人听从了 Bill Gurley 的 push，而 Collison 兄弟则为自己的过度自信和天马行空付出了代价。

**Stripe 目前陷入的是典型的两难局面（或者说是死亡螺旋）：**

• Stripe 发出了大量的 RSU 来激励员工，有 1 万名前任和现任员工持有 RSU，它们的解禁期通常是 7 年或公司 IPO，当 RSU 到期完成归属，员工们需要纳税，但又无法出售自己的股份；

• Stripe 似乎在推进 IPO，但是鉴于资本市场的冰冷，这有可能无法成功；

• Stripe 目前通过额外募集资金来帮助员工处理这一局面，它需要在 22 年上半年募集 20 亿美元，并且在 24 年底之前募集 40 亿美元；

• 但是目前每个人都缺乏流动性，这个筹集过程一定不会平稳，这导致 Stripe 可能需要不断调低估值并且带来更大的股份流失。

在 550 亿美元融资遇到挑战的情况下，Stripe 目前已经将估值调低至 500 亿美元。从这个死亡螺旋的逻辑和市场的反应来看，这不是老股价格在未来一段时间的终点。

**分心的管理层**

我们相信企业家的经营能力不来自媒体的吹捧，而是“行胜于言”。Collison 兄弟仍然值得敬佩，但是他们在过去两年的某些经营事故让我们的信心有些许流失：

**1. Bolt 创始人的暴论影响了 Stripe 的 VC moat。**

Bolt 的创始人 Ryan Breslow 在 22 年 1 月发布了长文指责 Stripe 和 YC 是“黑帮老大”，使用各种可以想象到的手段阻止竞争对手取得成功。我们无法具体估计这个事件的影响，但 Ryan 的帖子在 Twitter 和 Hacker News 上引发了巨大的讨论，这毫无疑问为 Stripe 的品牌带来了巨大的损害。坦诚来说，VC moat 对于 Stripe 的生意非常重要，如果 YC 和红杉等机构在未来潜移默化地走向“避险”，这将严重影响 Stripe 对于下一波科技创新的垄断。

**2.****John 和 Patrick 是创始人，但可能已经不是创业者。**

Collison 兄弟仍然是 Stripe 的灵魂人物，他们是创始人，但已经不是严格意义上的创业者。John Collison 在 21 年 6 月花 2000 万欧元在爱尔兰购置了庄园，Patrick Collison 一直对支付之外的领域有过度的好奇心，他在 21 年 12 月成立了 Arc Institute 为科学研究做贡献。随着 Stripe 向欧洲扩张，Collison 兄弟将更多时间花在了故乡爱尔兰，而不是公司总部所在的硅谷。

**3. 22 年的过度扩张、overhire 和管理层动荡。**

22 年的 Stripe 和 19 年的 Bytedance 有点像，它过度急促地试图同步扩展各类软件，同时延续全球扩张，但区别是 Bytedance 的家底更厚，而 Stripe 的现金在亏损面前捉襟见肘。在此之外，Stripe 的高管团队也在 22 年异常动荡，安全主管 Niels Provos 在 3 月辞职，本来同意加入担任金融服务总裁的 James Phillips 也临时拒了 offer，它现任的 CFO Dhivya Suryadervara 也在 23 年 2 月宣布即将离开。

总体而言，Collison 兄弟仍然是出色的创始人和管理者，但是我们应该意识到他们远非完美，并且成熟度可能和 Frank Slootman 这样的管理者有差距。他们比  Frank Slootman 要酷得多，但是这有隐患。

**03****.**

**否极泰来**

尽管有 devil's advocate 中的诸多问题，但 Stripe 仍有其独特的意义，硅谷独角兽的形象代言人、第三大估值的独角兽、支付和软件的完美组合。如果你要建一个独角兽 Index Fund，缺少 Stripe 将使它不完整。

**我们的 Thesis 没有破裂**

我们原来的 thesis 没有变化，公司 Deck 里的一些信息也可以继续验证我们原来的判断：

**1. 现代化收单商势不可挡，而 Stripe 有独特的竞争力。**

Stripe 的 win rate 相较 21 年初有很大提升，只有不到 10% 的单子是输给了竞争对手。Checkout.com 的 US Commerce Head 在客户访谈中也提到，尽管他们在美国的头号竞争对手是 Stripe，但是 90% 单子都是替换更落后的传统收单商，而不是现代化收单商的直接竞争。

**2. 全球创新看美国，美国创新看硅谷，Stripe 垄断了最优质的创新公司！！！**

Stripe 过去的成功是抓住了 Instacart、DoorDash、Lyft、Shopify 等公司，跟它们一路成长。在最近 Generative AI 的趋势下，Stripe 又是明显的赢家，最头部的模型和应用都使用 Stripe 来收单。如果能有下一个 Shopify 的 TPV 同等量级的公司出现，Stripe 是最有可能服务这个公司的收单商。

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/012.png)

Annual Letter 里有一段原话是：

（年 TPV 10 亿美元以上客户数量）其中一部分扩张是由于成熟的巨头企业，但大部分不是。在  Stripe 工作的乐趣之一就是与初创企业合作，帮助他们实现快速成功。这 100 多家行业领袖中，超过一半的企业在 Stripe 平台上实现了 10 倍的收入增长，超过四分之一的企业实现了 100 倍的增长。许多现在众所周知的公司，如 Instacart、Substack 和 DoorDash（最初命名为“Palo Alto Delivery”），从一创立就使用 Stripe 来收单。

Stripe 的 take rate 相较 Adyen 优势明显。在 10 亿美元以上 TPV 客户占比达到 60% 以上的基础上，Stripe 的 take rate 基本没有明显变化。（这一点有些不确定性，因为我们正听说有大客户在和 Stripe 重新谈判定价）。

**AI 大潮中的不错站位**

就像我在上面指出的，**Stripe 在创新创业客群仍然拥有绝对的统治力。**

从 Midjourney、Jasper 到 ChatGPT Plus，最创新和最优质的 AI 公司都在使用 Stripe 收单。不同于 Shopify、Instacart 的那个年代，现在的 Stripe 还拥有 Billing、Invoicing、Revenue Recognition、Sigma、Tax 这套软件产品，能为 AI 初创公司们提供全套的收入管理软件和相关流程的自动化能力，跟它们财务堆栈的耦合程度更深了。

此外，Stripe 可能是跟 OpenAI 关系最亲密的公司之一，OpenAI 的联合创始人及现在的 President Greg Brockman 是 Stripe 的首任 CTO，15 年离职时被 Patrick Collison 介绍给了 Sam Altman，才有了后面 OpenAI 这摊子事儿。

现在 Stripe 和 OpenAI 已经有非常深度的合作：

**• OpenAI 全套产品使用 Stripe 付费：**ChatGPT Plugs 和 DALL.E 都使用 Stripe 接受全球客户的付款、管理订阅、提供定价表、计算销售税、报账和打击欺诈；

**• Stripe 成为 GPT-4 的深度用户：**Stripe 是 GPT-4 推出时预测试的重要客户，公开发布了使用 GPT-4 对支持文档进行问答以及检测 Discord 社区欺诈的 Show Case，同时 Stripe 内部还开发了一套 AI 应用构建平台，方便每个员工基于 LLM 的能力构建 AI 智能应用。

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/013.png)

**公司有明确的转盈计划**

从 topline 的角度看，Stripe 增速放缓，但是放在 22 年的环境里绝对不算特别差的，要知道 PayPal 的 TPV 已经到了负增长的程度。

在 Annual Letter 中，管理层的解释是：

建立在 Stripe 平台上的企业总共处理了超过 8170 亿美元的交易额，比去年增长了 26% 。虽然不太准确，但是与之相关的电子商务（交易量大盘）去年增长了 7% 。

不过鉴于资本市场对于增长和盈利偏好的改变，后面我们观察 Stripe 的经营重点一定是 bottom line，Stripe 也有比较明确的盈利改善规划，将 22 年的 -2% 经调整 EBITDA 在 24 年起码扭转到 21 年的 19% 水平，具体包括：

• 继续优化 headcount：抓手是组织架构调整和可能的进一步裁员；

• 营销和销售费用的优化：让 GTM 团队更精简；

• 研发提效，并且让全球基础设施的成本随着 TPV 增长逐渐被摊薄；

• 通过自动化等方式优化其他费用支出。

整体方案比较 actionable，所以如同上文所说，我们的 u have to believe 是：**管理层能够执行这个计划，在 24 年扭转 Rule of 40 的表现，即收入增长仍然维持在 20% 区间，但是 FCF Margin 大幅改善。**

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/014.png)

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/015.png)

延伸阅读

[![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/016.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247498171&idx=1&sn=237435c25b79c9018606bf395aa1c913&chksm=ce9b4625f9eccf331dc8ae958c0850a888060a7221d53d52746d74ceec910c294607c9352d38&scene=21#wechat_redirect)

诞生5家Fintech上市公司后，拉美能跑出自己的Plaid吗？

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/017.png)

[![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/018.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247493023&idx=1&sn=b0f0ec7fe34adebc0f7b762082c63bf6&chksm=ce9b5a01f9ecd3175cdd75e4ce440fd5147e257d11e14628ba1b4affa9d2f8db2fb2482d72cb&scene=21#wechat_redirect)

大回调中，融了千亿美金的FinTech独角兽们过得还好吗？

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/019.png)

[![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/020.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247492447&idx=1&sn=67842faeab698d55789029da523851c3&chksm=ce9b5cc1f9ecd5d758b00a8d3485e65e06430dd73b4d74bc121be24ed988940db742a2ad8470&scene=21#wechat_redirect)

估值34亿美元，MoonPay是PayPal for Web3吗?

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/021.png)

[![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/022.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247491673&idx=1&sn=9743dc817572bad1747b4fbaf64c1295&chksm=ce9b5fc7f9ecd6d1360056c7833adc67ccdc2f15f0379edaebe70ad9899f8278ce33aa16e802&scene=21#wechat_redirect)

数字资产托管：诞生多个独角兽，Crypto与传统金融的交汇处

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/023.png)

[![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/024.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247491292&idx=1&sn=8b7e5f04ceb6a6b00ca63a7e63b8f541&chksm=ce98a142f9ef2854cda89ec977ff0290843455d2afd593d3d23614edf2275f6efbf31a912414&scene=21#wechat_redirect)

FTX重注、吸金30亿美元，非洲会诞生下一个Stripe吗？

![](../images/2023-04-21-22nian-ni-feng-hou-stripeneng-kao-aiban-hui-yi-ju-ma/025.png)
