---
title: 联手 OpenAI 发布 ACP，Stripe 是如何思考 Agent 支付的？
publish_date: '2025-11-06'
publish_timestamp: 1762432296
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/YsILMMbYO1p9cYDa65yerg
msgid: 1000000451
appmsgid: 2247519240
itemidx: 1
digest: ACP 本质是商家、agent 和消费者之间的一种“共享语言”
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgyt4HUhgyJZxtPgtrSeFBHR8ED3zO0j6XMSygAribQvIoxSfGWWAhAcHVNrBWTSFa8MLUgaicpjdg8Q/0?wx_fmt=jpeg
image_count: 25
archived_at: '2026-04-20T04:42:40+08:00'
---

[![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

编译：Haozhen、Ivy

当 agent 开始学会“消费”，支付世界也迎来了重构的时刻。

作为互联网支付重要基础设施，Stripe 当前最新估值高达 1060 亿美元，它每年需要处理约占全球 GDP 1.3% 的[交易量](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518145&idx=1&sn=c4603e0ee1c1a45a0bcd4c1eafd4e016&scene=21#wechat_redirect)，也因此，在 AI 时代，Stripe 成为包括 ChatGPT 在内的几乎所有 AI-native 玩家的支付首选。

今年 9 月，OpenAI 与 Stripe 联合推出了 Agentic Commerce Protocol（ACP），一个面向 agent 经济系统的开放商业标准，明确规定了商家应如何向 agent 展示商品、品牌形象与定价策略等，标志着 agent 不再只是信息中介，而将成为具备购买与支付能力的经济参与者，这更是从根本上重新定义了“谁在参与经济活动”这个命题。

为了更深入理解 Stripe 在这场浪潮中的战略布局，我们整理了 Emily Glassberg Sands 的最新访谈。作为 Stripe 的 Head of Data & AI，Emily 在访谈中分享了 ACP 的本质，Stripe 是如何通过 AI 提升市场效率和内部工作效率、推动全球 GDP 增长的，以及应该如何看待 AI 是否存在泡沫等问题。

**01.**

**ACP 是什么？**

**⾯向 Agent 的开放商业标准**

今年 9 月，Stripe 与 OpenAI 联合推出了 Agentic Commerce Protocol，简称 ACP。这是一个开放的共享标准，目的是解决“agent 代表人类购物”这一新兴场景中潜在的问题：越来越多的用户希望 AI 工具（比如 ChatGPT）可以直接购买商品或服务，但商家却缺乏一种标准化的方式来向这些 agent 展示自身产品的信息，同时 agent 也需要一个统一的接口来理解并访问这些信息。ACP 的诞生正是为了解决这一空白，为 agent、商家和消费者之间的高效交互建立基础。

这个协议的本质是一种“共享语言”，它清晰定义了商家应该如何向 agent 展示自身的商品、实时库存、品牌形象与定价策略。因此，遵循这一协议后，商家可以一次性将结构化的商品信息提供给所有兼容的 agent，不用再针对每个新平台进行定制化开发，显著降低了商家接入 agent 的门槛。同时，agent 开发者也能更高效地整合来自不同商家的数据，为用户提供更丰富、准确的购买建议与执行能力。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/002.png)

在产品战略上，Stripe 内部一致决定将 ACP 作为一种“协议”而非“产品”发布，这是因为目前客户、用户以及 AI 驱动的“买家 agent”正在以空前的速度改变商业互动方式。Emily 表示，全球商业生态需要一个开放的共享标准，而这个标准不一定要贴上 Stripe 的名字，ACP 的使命在于促进整个互联网商业生态的增长，而非单纯服务于 Stripe 自身或局限于 Stripe 的支付体系。

在协议设计上，Stripe 没有选择为 agent 提供一个直接持有资产的钱包（wallet），因为 ACP 的核心在于让企业能够以标准化的方式展示自己的产品、库存、价格和品牌信息，让 agent 能够理解或代表用户进行购买。也就是说，ACP 作为一种协议，本身独立于具体的支付和资金流动机制。随着市场和技术的发展，资金的流转方式可以不断演变，但 ACP 不用同步更新标准。ACP 关注的是“商业信息的表达和传递”，而支付机制决定的是“资金的流动方式”，两者相互独立，又相互补充。

目前，这个协议的潜力已在 ChatGPT 的“即时结账”（Instant Checkout）功能中得到初步验证。首批合作伙伴包括 Etsy、即将上线的百万级 Shopify 商家（比如美妆品牌 Glossier）以及 Salesforce 这样的 SaaS 巨头。更具标志性的是，沃尔玛和山姆会员店等大型零售商也已加入，这表明主流零售业已开始认可 agentic commerce 的趋势。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/003.png)

Stripe 认为在 agentic commerce 之下，支付方式不会局限于虚拟卡模式。稳定币、通用钱包等新型支付工具都有可能成为下一阶段的发展方向。同时，存储余额（Storage Balance）将在微交易领域发挥关键作用。例如，购买价值仅 5 美分或 10 美分的 AI 推理或内容服务的时候，传统卡片支付体系的效率非常低，而基于存储余额的模式能更高效地处理此类交易。随着 AI 之间的直接交互日益普遍，agent 对 agent 的支付预计将推动这一领域迈向新的前沿。

Stripe 的存储余额（Storage Balance） 是指商家在 Stripe 内部预先存放的一笔资金，可用于未来的付款或全球代发（Global Payouts），资金可从银行账户或 Stripe 收款余额转入，加快支付的执行速度。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/004.png)

在 Emily 看来，尽管 agent 领域有可能演变成一个“赢家通吃”的市场，但从效率与生态多样性的角度出发，更理想的结果是商家能够同时通过多个 agent 销售产品。

**两个组成部分：共享支付令牌和欺诈检测机制**

Emily 认为，ACP 不仅仅是商品信息标准化协议，还包含两个重要组成部分。

1. 共享支付令牌（Shared Payment Token）

共享支付令牌（Shared Payment Token）允许 agent 在不接触或存储用户敏感支付凭证的情况下，安全地代表用户完成支付，从而既保护隐私，又降低交易风险。

这是 Stripe 在支付执行层面开发的机制，这项技术关注“交易如何真正完成”，比如：

**•** 在 ChatGPT 的即时结账功能中，Stripe 提供了共享支付令牌作为后台机制；

**•** 在 Perplexity 的旅行搜索与预订场景中，Stripe 会为 AI agent 生成一次性虚拟卡，代表用户完成支付。这种虚拟卡机制类似于 Doordash 司机代为购买咖啡的模式，它受消费额度与时间窗口限制，无法访问用户的真实信用卡信息，从而保障安全与可控。

2. 欺诈检测机制

ACP 在支付流程中加入风险评分体系，帮助商家在面对自动化购买请求时可以做出正确判断。这个机制主要用于区分“善意机器人”和“恶意机器人”。过去，商家往往会屏蔽所有机器人流量，但现在来自 ChatGPT 等平台的机器人购买请求往往是真实的商业机会，这对传统的防欺诈机制提出了新的挑战。

尤其是当 agent 被用于购买稀缺资源（比如演唱会门票、活动票务）时，传统的防欺诈机制可能会被颠覆。一位票务平台的 CEO 表示，之前在销售约 3000 张 Bad Bunny 演唱会门票时，涌入了 40 万人尝试购买，其中绝大多数是机器人。这些机器人通常由黄牛操作，他们确实完成了付款交易，不会引发退单纠纷，但黄牛并不是平台希望服务的真正客户。

由此可见，“欺诈”不仅限于争议性扣款或未付款等问题，还包括扭曲市场公平、恶意囤货和资源滥用的行为。Emily 强调，企业需要在结账前尽早识别这些非理想交易者，因为在票务系统中，一旦门票被加入购物车，库存会被锁定 10 到 15 分钟，即使后续交易被拦截，也会浪费优质客户的购买机会。

而 AI 可以极大改进传统机制。传统系统往往依赖固定规则来做出“阻止”或“不阻止”的行动，但现代模型可以基于基础模型（foundation models）生成可解释的文本理由，说明系统为何怀疑某笔交易有风险，未来的防欺诈流程可能将是先由 AI 模型做初步判断，然后由人工或更高层次的 agent 进行复核，从而形成动态的决策体系。

同时，当系统拒绝了真实、善意的用户时，必须提供清晰的解释和申诉途径。如果人们被一个无法自我解释的机器人拒绝购买资格，挫败感会极强。Emily 指出人类也会犯错，甚至错误率可能高于 LLM，因此需要有完善的“二级人工客服”机制。目前，现实中极少数的不良行为者往往占据了大量交易量，迫使平台不得不收紧规则，这反而让普通用户承受了不必要的代价，例如被限制免费试用、预付积分额度受限，或不得不支付更高的价格。

**02.**

**Stripe 和 AI 公司共同探索商业模式**

Stripe 将自身定位为 AI 公司的支架，大部分在做商业化的 Forbes AI 50 都在使用 Stripe。这些公司（比如[Cursor](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510163&idx=1&sn=f3a636901cd1b55dadf71e2884f04982&scene=21#wechat_redirect)、[Lovable](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247511710&idx=1&sn=64bef999305f0e7d388b671a5bc3bd8f&scene=21#wechat_redirect)）普遍以极其精简的团队构建出可规模化运营的企业，因此更倾向于全面依赖 Stripe 来一站式获得完整的金融 infra，从而可以避免额外的人力投入。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/005.png)

此外，这些 AI 公司的国际化速度也远超以往的 SaaS 企业。Emily 表示，收入最高的前 100 家 AI 公司在成立第一年平均就覆盖了 55 个国家和地区，第二年则扩展到 100 个以上的市场，全球化速度几乎是三年前 SaaS 浪潮的两倍。为了满足这种高速扩张的需求，这些公司几乎都采用了 Stripe 的 Optimized Checkout 套件（开箱即用、支持 100 种支付方式），并使用 Radar 等反欺诈套件，来确保跨国交易的安全与合规。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/006.png)

值得一提的是，Stripe 的独特之处在于 Stripe 会主动投入资源去改进整个支付市场的运作效率，比如让支付更顺畅、让商家更容易完成交易，但它并不会直接为这些改进向用户收费，因为只要 Stripe 平台上的企业实现增长，Stripe 自身也会随之受益。Emily 表示，在过去一年中，使用 Stripe 的企业的平均增长速度是 S&P 500 企业的七倍。尽管这一结果可能受到选择效应的影响，但仍充分说明了 Stripe 生态模式的有效性与可持续性。

**Stripe 支持按 Token 和按结果付费**

当前，AI 行业存在多种商业模式，如固定费用订阅、按使用量付费以及积分消耗模式（credit burndown model）。这些模式不仅影响 AI 公司的收入结构和欺诈风险，也直接决定这些公司的单位经济效益。

对于 AI 套壳公司（wrappers）而言，这种影响尤为突出。因为它们的成本与底层 LLM 的推理价格紧密相关，而模型的成本和性能又在不断波动，导致传统固定费用的订阅模式难以维持。为了保持稳定的盈利空间，这些公司被迫快速迭代商业模式，从按使用量付费、按积分消耗付费，逐步探索按结果付费等更灵活的模式。

为应对这种波动，Stripe 推出了 “Token 计费”（Token Billing）这个创新功能。通过一个 API，AI 公司可以实时追踪自身服务所消耗的底层 LLM 推理成本，并基于这些数据动态定价。当模型成本上升时，企业能及时调整价格以避免亏损；而当成本下降时，也可将节省的部分让利给用户，从而在竞争中保持价格优势。这种与成本联动的实时定价机制，成为 AI 公司维持健康商业模式的重要基础。

此外，Stripe 还支持另一种前沿商业模式：按结果付费（Outcome-based Billing）。例如，客户服务公司 Intercom 就是根据 AI 所成功解决的案例数量向客户收费，而不是按使用时长或 API 调用次数计费。这种模式大大降低了企业客户的采用门槛，因为企业只需为真正产生正向业务成果的 AI 服务付费，从而可以确保投资回报既明确又可验证。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/007.png)

Stripe 表示，几乎所有领先的 AI 公司都在使用 Stripe 的计费套件。无论是 Token 计费还是按结果付费，这些功能都超越了传统支付处理的范畴，成为帮助 AI 企业在不确定的技术与市场环境中实现商业落地的关键基础设施。借助这些工具，AI 公司自身可以专注产品创新，而 将复杂的商业化与财务管理交由统一平台处理。

**稳定币支付和 Link 支付带来网络效应**

Emily 在访谈中还表示，AI 公司正在迅速采用稳定币（stablecoin）支付。虽然这一趋势仍处于早期阶段，但已展现出显著的应用价值，例如，Vercel 已允许用户使用稳定币结算。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/008.png)

目前这种做法在两类 AI 公司中尤为常见：

1. 从第一天起就面向全球市场、有跨国交易需求的公司；

2. 单笔交易金额较高、对支付成本极为敏感的公司。

YC 初创公司 Shadertoy 就是一个典型案例。目前 Shadertoy 的交易中已有 20% 来自稳定币。Shadertoy 之所以采用这一方式，就是因为自身业务遍及全球，而传统支付方式成本过高：美国常用的低成本结算方式 ACH（自动清算所）并不适合国际交易，但如果通过国际信用卡支付，大额交易需承担约 4.5% 的手续费，会严重压缩公司的利润空间。

Shadertoy 是一个面向计算机图形专业人士、学者和爱好者的在线社区和平台，他们通过 GLSL 代码分享、学习和试验渲染技术和程序化艺术。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/009.png)

Shadertoy 开放稳定币支付后，总收入提升了 10%。其中，一半的稳定币交易是增量收入，也就是说这些客户如果没有稳定币支付选项就不会购买，另一半来自原有支付方式的转移。同时，稳定币的交易成本仅为 1.55%，给企业多保留了点利润。

稳定币的使用还带来了明显的网络效应（network effect）。AI 产品的购买者往往也是其他 AI 产品的提供者，当他们拥有稳定币钱包后，便能在不同服务商之间直接完成支付，从而形成自我强化的交易循环。

这种网络效应同样体现在 Link 上，Link 是 Stripe 推出的一个一键结账（one-click checkout）和支付信息保存服务，主要面向消费者使用。目前 Link 用户已突破 2 亿，Lovable 有 58% 的交易量来自 Link。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/010.png)

Emily 指出，在研究这些网络结构时，传统的赫芬达尔指数主要用于衡量市场或交易的集中度，而并非严格意义上的网络密度。但同时，Emily 表示过高的集中度与 Stripe 追求的多样化目标也是相悖的。Stripe 希望能在多个行业和市场中保持广泛分布，实现真正的全球覆盖。Stripe 的目标不仅限于服务 AI 产业，而是通过这些技术基础设施来广泛提升整个互联网的生产力，推动全球互联网 GDP 的长期增长。

赫芬达尔指数（Herfindahl-Hirschman Index，简称 HHI）是用于衡量市场集中度的指标，计算方法是所有企业市场份额平方之和，数值越高表示市场越集中、竞争越弱。

**“可认领沙盒”降低商业化门槛**

随着 Replit、Vercel 等 AI 开发平台上初创企业的迅速崛起，Stripe 希望用户能在这些平台的原生环境中直接实现货币化，而不必跳出流程去单独创建或验证账户。为此，Stripe 推出了可认领沙盒（Claimable Sandboxes） 功能，允许用户可以在还没有 Stripe 账户的情况下也能在沙盒中完成产品创建、定价、测试扣款等。当他们准备上线时，只需一键登录或注册，即可将认领沙盒并转化为真实业务。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/011.png)

这种机制大幅降低了创业门槛，推动了“低代码创业”的浪潮。如今，Stripe 已成为 Vercel 平台上集成度最高的前三个工具之一，越来越多的用户正通过这种方式创建新企业，其中相当一部分是非技术背景的创始人。更重要的是，当用户从 Vercel 跳转至 Stripe 时，系统已经自动识别了他们的业务意图和偏好，用户可以直接进入后续阶段，沙盒环境也会自动激活，从而实现无缝的商业化体验。

**03.**

**Stripe 是如何使用 AI 的？**

**AI 提高了欺诈检测的准确性和速度**

Stripe 使用机器学习已有十多年，早期通过 Radar 系统识别和阻止欺诈，确保每天大量用户的注册与交易是安全、可靠且无欺诈风险的。

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/012.png)

Stripe 最早在 GPT-3.5 出现时开始深入使用 AI 和 LLM。当时，Stripe 意识到，想要让 AI 真正发挥价值，关键在于要让所有人都能安全、便捷地使用高质量的模型，并能真正构建出可用于生产的产品。

从 2023 年初起，Stripe 将 AI 基础设施和应用从传统机器学习体系中独立出来，开始构建自身特定领域基础模型（domain-specific foundation model）。这一转变让 Stripe 从依赖单一任务模型，升级为基于更丰富的支付嵌入（payment embeddings）体系，能够支持多样化的下游应用。

目前 Stripe 的基础模型被应用于每一笔交易中，模型在“盗刷测试”（card testing）中的表现尤其突出。攻击者通常在大规模交易流中隐藏大量小额测试支付，传统模型难以识别。而 Stripe 的模型通过将每笔交易转化为信息密集的嵌入向量，在多维空间中实时分析分布，精准识别异常聚集的交易，从而实现高效阻断欺诈。这种方法将大型用户的盗刷检测率从约 59%提升至 97%，并且整个决策过程的延迟控制在 100 毫秒以内。

具体来说，Stripe 是将支付数据视为一种“语言”，从而理解交易的“序列”信息，就像一个词的意义取决于上下文，一笔支付的风险也取决于它与其他相关交易的关联。模型会捕捉并分析各种可能相关的序列，例如“某个特定商户从某个 IP 发起的连续支付”或“某个特定信用卡在某个时间段内的所有活动”，在更深层次上理解交易行为的本质，发现隐藏的异常模式。

这种方法不仅显著提升了欺诈检测的准确性，还极大地提升了 Stripe 响应新型风险的速度。当 AI 公司客户提出需要识别那些虽未导致欺诈性争议但仍属可疑的交易（例如来自机器人而非真实用户的流量）时，Stripe 能在数天内快速响应。通过分析基础模型生成的嵌入向量，团队可以迅速识别出代表不同可疑行为的交易集群，并为它们打上人类可读的标签，然后将这些可疑交易流提供给客户，由客户自行决定是否阻止。

**•** 什么是“善意欺诈”（friendly fraud）？

AI 公司的商业模式正面临一种极具破坏性的新型欺诈：“善意欺诈”（friendly fraud），这种欺诈并非源于信用卡被盗，而是由合法用户滥用服务条款导致，如免费试用滥用、退款滥用或积累大量费用后拒绝支付。Emily 认为，47%的公司领导人会认为目前最大的挑战是“善意欺诈”（friendly fraud）。

过去，SaaS 行业服务的边际成本（marginal cost）接近于零，免费试用滥用等问题不会严重影响 SaaS 产品的单位经济效益。但在推理成本昂贵的 AI 时代，每一次推理都伴随着高昂的边际成本，因此善意欺诈会对 AI 企业构成生存威胁。一些小型 AI 企业创始人甚至为防止善意欺诈而彻底关闭免费试用或大幅限制积分，但这反过来又扼杀了自身的收入。

值得注意的是，这类欺诈并非 AI 公司独有。广告平台也面临类似问题：广告主先投放广告后付费，如果客户最终不支付，平台不仅损失了收入，还错失了本可以出售给付费客户的广告位。

更令人担忧的是，现在市面上还出现了“免费试用卡”（free trial cards），这是一种有效期只有 24 小时的虚拟卡，被滥用者专门用于注册各类服务的免费试用。

Stripe 正在拓展 Radar 的功能来应对这些欺诈，包括在源头捕获大部分免费试用的滥用，此外，针对大额订阅计划中常见的退款滥用，即用户在消耗完所有服务（如大量模型调用额度）后发起退款，Stripe 也能通过追踪使用记录进行有效识别和干预。

**AI 提升了 Stripe 内部工作效率**

GPT-3.5 发布后，AI 也在 Stripe 内部掀起了一股应用热潮。最初的内部用例是自下而上的：Stripe 员工创建了一个类似 ChatGPT 的界面，可以与多种模型互动。这个早期版本不是生产级的 LLM，而是带有预设功能的平台，允许员工保存和共享 prompt 模板，例如“找出潜在客户并生成联系邮件”或“用 Stripe 的语气重写营销内容”等。Emily 表示，几乎是在一夜之间就出现了上百个预设模板。在这之后，Stripe 内部又推出了面向工程师的 LLM，让工程师可以访问生产级的 LLM。

值得注意的是，由于每天有成千上万的商家加入 Stripe，Stripe 需要了解这些商家的业务类型、信用水平和欺诈风险，因此在内部，AI 的许多早期用例都集中在“理解商家”这个场景中。如今，LLM 工具已在 Stripe 内部广泛使用，在约 1 万名员工中，每天约有 8500 人在使用 AI 工具。

**•**本地支付方式（Local Payment Methods，LPM）团队的实践

由于 Stripe 客户普遍在国际市场有销售行为，因此支持多样的本地支付方式对于降低商家成本非常重要。虽然 Stripe 的 Optimized Checkout Suite 已内置 100 多种支付方式，但客户仍常提出新增集成的请求。过去，集成一种新的支付方式通常需要几位工程师耗时两个月，现在在 LLM 的帮助下，LPM 团队仅用两周就可以完成一种新的支付方式的集成，而且团队还计划将周期进一步缩短至一到两天。

**•** AI Coding 的实践

在工程生产力方面，Stripe 65-70% 的工程师在日常工作中使用 AI coding 助手。尽管使用率很高，但要衡量 AI coding 对生产力的实际提升却是非常困难的，因为“代码行数”并不是理想指标。此外，许多 coding 模型的成本也较高。

从投资视角来看，Emily 认为应以 2-3 年的周期来看待 ROI，而不是过度关注短期收益。工程师是高价值人才，给予工程师理想的工具能提升他们的创造力与积极性。而且模型还会不断变得更好、更快、也更便宜，例如，GPT-4o 可能在早期成本较高，但后续发布的更轻量的模型（如 o3-mini）则能以更低成本替代人工，每年为企业节省数百万美元。

**•**数据查询领域的实践

在数据查询方面，Stripe 内部开发了一个名为 Hubert 的自然语言工具，Hubert 能根据自然语言生成 SQL 查询并用自然语言解释查询逻辑，让非技术人员也能理解和验证，由于 Stripe 的数据结构良好且文档完善，Text-to-SQL 的体验非常可靠。目前约有 900 名员工每周使用 Hubert，但目前 Stripe 仍将这个工具的使用限制在技术人员范围内，这是考虑到这个工具尚处早期阶段，可能产生错误结果，而技术人员更能验证并反馈。

考虑到 Hubert 在数据发现（data discovery）方面表现最弱，常常难以找到最相关的表和字段。因此，Stripe 正在弃用低质量表，并由人力维护高质量表，因为目前尚不确定是否能依赖 LLM 完成高质量文档记录，因此这一任务仍由领域专家负责。

此外，为了支持内部这些 AI 应用，Stripe 正在开发一个内部系统，相当于一个内部 MCP 服务器，能集中管理并访问所有内部工具，这个工具不仅接入了 Slack、Google Drive 和 Git 等常用工具，还能访问数据目录，可以查看和查询全部数据。

除了上述实践外，Stripe 还正在向语义事件基础设施（semantic events infrastructure）转型，Emily 认为实时、高质量、文档完善的数据价值将显著提升，因为在未来，无论是用户还是 agent，都不再满足于静态仪表板，而会需要实时洞察。

其中，最重要的两个数据类型是支付数据和基于使用量的计费数据，后者对 AI 商业模式的实时性要求尤其高。因此，Stripe 正将语义事件和规范化数据集以近实时方式提供给仪表板和数据管道，以便客户将 Stripe 数据与其他系统（如 BigQuery）集成。同时，为解决不同产品间数据源割裂的问题，Stripe 还计划在未来六个月内重构支付和计费流程。

**Stripe 对 AI 写作的反思**

近年来，随着 LLM 的普及，一些组织中长期存在的“表演性写作”现象开始被重新审视。过去，在没有 AI 的时候，员工即使掌握了清晰的 bullet point，也常常被要求撰写冗长的 memo，这既是为了表示重视，也是出于组织文化的惯性。但如今，AI 的出现似乎正在打破这种模式，人们可以直接提交 bullet point，而无需再进行繁琐的文字包装。

但这种变化也引发了更深层的担忧。写作，尤其是非 AI 生成的写作，本质上是一种思考的过程。它迫使领域专家深入分析、组织推理，并从第一性原理出发进行逻辑构建。这一过程虽然耗时，却能带来真正的理解。而 LLM 的特性恰恰相反：它允许人们仅仅输入 bullet point，却不必真正完成推理。这种便捷表面上提高了效率，但也可能让人们失去严谨思考的机会。

同时，阅读习惯的改变也在影响写作行为。随着越来越多人倾向于阅读摘要，人们开始质疑撰写长文档的必要性，甚至更愿意直接写短文。

但无论写作形式发生什么变化，在 Emily 看来，在使用 LLM 辅助写作的过程中，有两个明确且不可妥协的原则：

1. 凡是使用 LLM 参与内容创作，必须明确标注；

2. 创作者需警惕“LLM 敷衍”（LLM slop），即输出看似合理、实则缺乏深度的文本。

从更宏观的社会视角看，最重要的是不要停止思考。LLM 的存在并未削弱人类思考的重要性，反而使思考更加关键。在 AI 能够自动生成内容的世界里，真正稀缺的能力是深入推理、批判质疑以及指挥机器完成目标的能力，而非机械地执行任务。过度依赖 LLM 的一代人可能逐渐低估“深度”的价值，而这恰恰是最危险的事情，因为在 AI 时代，深度才是最核心的竞争力。

最后，关于使用 AI 的原则，关键在于责任归属。用户对自己生成的文档或代码负有全部责任，不能将错误或偏差归咎于 LLM。AI 应被视为思考、实验和快速迭代的工具，而非替代品。正如一些公司（如 Vercel 的 V0 UI 版本）所展示的，清晰的演示与原型往往比冗长的文档更具沟通效率，因此使用 LLM 生成内容本身没有问题，但在最终提交、发布或推送之前，创作者必须重新加入自己的判断与思考，确保产出的内容真正可靠、符合意图。

**04.**

**经济学家视⻆：AI 对经济有哪些宏观影响？**

**AI 是否存在泡沫？**

关于“AI 是否存在泡沫”，核心问题在于：这些 AI 公司是否真正创造了可持续的价值，是否拥有真实的收入流入？

Emily 通过分析 Stripe 平台上收入最高的 100 家 AI 公司，并将这些公司与五年前收入最高的 100 家 SaaS 公司进行对比后发现：

1. 从增长速度来看，AI 公司的扩张远超以往的 SaaS 企业。它们达到 100 万、1000 万或 3000 万美元 ARR 的速度，比传统 SaaS 公司快两到三倍；

2. 从全球化程度来看，AI 公司在创立的第一年和第二年，国际化进展也显著领先于以往的 SaaS 公司，AI 公司平均向两个以上的国家销售产品，收入中相当大一部分来自海外市场。例如，一家法国初创公司有多达 95% 的收入来自法国以外；

3. 从留存率与竞争态势来看，AI 公司的客户留存率略低于 SaaS 公司，这符合它们仍处于早期阶段的特征，但更重要的是，AI 市场的客户行为模式与 SaaS 行业不同：AI 用户流失后往往会转向另一家竞争公司，几个月后又可能回流。这种高频切换说明市场竞争非常激烈，同时也表明客户对“需要解决的这个问题”有很高粘性，也就是说，用户可能会更替具体产品，但需求本身始终存在，并且愿意持续付费；

4. 从垂直化发展速度来看，AI 的演进路径与 SaaS 类似：从横向通用平台（如模型或基础设施提供商）逐步转向垂直行业。不同之处在于，AI 的垂直化速度快得多。如今已经出现大量行业专用的 AI 公司，例如医疗健康领域的 Nabla、法律领域的 Harvey。这种趋势得益于 AI 模型的可复用性与低构建成本，使得创业者能够在大型模型之上快速推出专业化解决方案，同时全球性利基市场的边界也被显著放大。

总体而言，Emily 认为，虽然无法确切判断当下 AI 是否处于泡沫阶段，但这些 AI 公司具备几个共同特征：高速增长、客户群体多样、客户需求强并且愿意持续付费。这些迹象表明，AI 公司正在成为真正具备持续价值和健康收入结构的高质量企业。

需要注意的是，从成本结构来看，AI 公司的一个突出特征是人员开销极低。收入最高的 AI 公司在每位员工创造的收入上，远高于多数以效率著称的上市公司。但这一指标往往忽略了另一项关键成本，即推理成本（inference cost）。因此，Emily 认为，不能用当下的成本结构来评估这些公司的价值，而应基于模型成本将持续下降的合理预期来建模。随着推理成本在未来会显著降低，这些公司有望展现出更强的盈利能力和更具吸引力的经济模型。

而且 AI 成本结构中既有良性也有不那么良性的部分。良性的一面在于，AI 替代了原本需要人工完成的劳动，从而直接提升了效率；不那么良性的一面则在于，一些公司可能在以低于成本的价格（例如以 50 美分卖 1 美元的服务）换取高速增长，这种情况类似于早期的 Uber 或 DoorDash 借助风投资金补贴用户的阶段。

值得庆幸的是，Stripe 平台上的许多 AI 公司，尤其是面向垂直领域的 AI 套壳公司（wrappers），正在追求健康的单位经济效益。他们希望确保每一个客户能够带来实际利润，而非依赖补贴驱动增长。这种趋势也解释了他们对 Token Billing 的强烈需求。

**对人均 GDP 和企业品牌的影响**

关于 AI 对宏观经济的影响，有一种热门看法认为，如果 AI 确实是一个主要的经济驱动力，那应该会很快在人均 GDP 这个指标中体现出来。但 Emily 认为，GDP 有许多其他驱动因素，且不能衡量一切，AI 影响的显现只是时间问题，她更看好 AI 会在以下场景发挥积极影响：

1. 提高市场效率： AI 和 agent 应该使市场更有效率，从而让人们可以更高效地消费；

2. 加速业务创建： agent 能让业务创建更有效率，加速了新兴初创公司的增长。许多以前不会起步的企业，现在正借助 AI 开发工具快速启动。

尽管存在成本问题，但 Emily 认为未来会有足够便宜的模型。而且 AI 公司在定价模式上正变得精明，传统 SaaS 基于 seats 的定价可能不再适用，基于结果或基于使用量的定价模式将更有发展空间。此外，在美国以外的市场，比如巴西，AI 被采用的程度也超出了 Emily 预期。

在时间节奏上，Emily 指出，人们不应期待 AI 的作用能在一年之内就体现在员工效率上。当前大多数企业希望到 2027-2028 年能通过 AI 提升员工产出效率。如果能将更高效的生产与更高效的消费相结合，即企业内部的生产效率与 agent 驱动的消费效率同步提升，那么全球 GDP 的增长将呈现出显著的复合效应。

这种转变还将催生新的组织形态，即“小团队+大产出”（small teams， big output），这些团队可能只有几名员工，却能创造数百万美元的收入，从而颠覆初创公司的传统结构，使企业有机会在第一轮融资时就实现盈利。

除了经济增长的讨论之外，另一个流行观点认为，在技术高度发达的世界中，品牌的重要性正在下降。然而，Emily 强调，AI 公司创造的许多价值恰恰来自品牌。一些在激烈竞争中脱颖而出的 AI 套壳公司（wrappers）的获胜关键并非技术本身，而是差异化的用户体验、吸引人的品牌形象和紧密的社区关系，例如 Lovable。这说明，即便在 AI 驱动的时代，技术卓越的创始人仍必须高度关注用户体验、产品美感和设计的巧思。

这种对品质与体验的执着，也体现在 Stripe 的企业文化中。Stripe 一直以技术卓越和行业领先的设计并重而著称。设计主管 Katie Dill 坚持对质量“零妥协”的原则：无论是仅有 2000 个用户可见的横幅，还是字体大小等微小细节，任何质量问题都必须被视为需要修复的 SLA（服务级别协议）级别错误。这种对细节的极致追求，构成了 Stripe 宏观创新的基础，也为公司确立了明确的标准：只要不符合质量要求，就必须被修复。

排版：夏悦涵

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/013.png)

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/014.png)

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/015.png)

延伸阅读

[![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247519112&idx=1&sn=562af823af24b984bc3c0242c389caa8&scene=21#wechat_redirect)

Coatue 最新报告：复盘 400 年、 30+ 次泡沫，我们离 AI 泡沫还很远

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/017.png)

[![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/018.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247519023&idx=1&sn=54a12b29668ca5b99582d8d4b931125f&scene=21#wechat_redirect)

领投 Ilya 新公司，13 年净 IRR 33%，Greenoaks 的科技投资哲学

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/019.png)

[![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/020.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518893&idx=1&sn=d97353a4eaff11bf3a12a3712ca328db&scene=21#wechat_redirect)

RL 是新的 Fine-Tuning

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/021.png)

[![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/022.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518860&idx=1&sn=033bb7b4db2d36c742d68acaf4218dd0&scene=21#wechat_redirect)

SemiAnalysis 创始人解析万亿美元 AI 竞争：算力是 AI 世界的货币，Nvidia 是“中央银行”

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/023.png)

[![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/024.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518822&idx=1&sn=d6b378e1e41e739fe132926b3cd4565f&scene=21#wechat_redirect)

告别 260 亿美元低效投入，HappyRobot 为物流业配置 “AI 调度员”

![](../images/2025-11-06-lian-shou-openai-fa-bu-acp-stripe-shi-ru-he-si-kao-agent-zhi/025.png)
