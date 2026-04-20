---
title: 云之后，大模型是网络安全的新机会吗？
publish_date: '2023-04-13'
publish_timestamp: 1681387734
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/nmeDrQX5dTRUT23-2sGI-g
msgid: 1000000190
appmsgid: 2247501647
itemidx: 1
digest: Generative AI和Cyber Security是当下持续火热的赛道。
cover: https://mmbiz.qpic.cn/mmbiz_jpg/3tHNibnJ2jgzUcbA4GXJWzIkhrctz6FWjEIKnvIpVKa0z2g3NdcfmUyJMeGzRpCibdAwagYrlZUficjQ7ibhcicbM6w/0?wx_fmt=jpeg
image_count: 29
archived_at: '2026-04-20T00:59:40+08:00'
---

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/001.gif)

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/002.png)

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/003.png)

作者、编辑：程天一

排版：Mengxi

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/004.png)

宏观环境继续冰冷的情况下，一级市场只有 2 个赛道继续火热，一个是 Generative AI，另一个就是 Cyber Security。[**云安全公司 Wiz**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247500575&idx=1&sn=5c113c85a79cc8bc58d15fb2d4ace921&chksm=ce9b7c81f9ecf597d9041598d4637b4fbfcfa1e90f7e32e6d59c8c0d1bc00417e91b5a3d478f&scene=21#wechat_redirect) 在我们的研究发表后不久又完成了一轮百亿美元估值的融资。

“AI 安全”是二者的交叉点，但是当下讨论起来非常痛苦，LLM 的安全（Safety）、模型及使用它的安全（Security）和 LLM 发展对于“传统”网络安全的影响往往被混为一谈。因此我们在本文先提出了一个更清晰地区分这三者的框架。

此外，对网络安全（和 LLM）缺乏了解的人可能会担心 LLM 会直接干掉原来的安全公司，但是 Microsoft Secure Copilot 背后的安全能力来源仍然是既有的安全产品，而 OpenAI 最近因 Redis bug 导致的宕机表明世界上最懂 LLM 的公司仍然需要完整的网络安全堆栈来保护自己。

在正文的主体部分，我更多地聚焦于了 LLM 为“传统”网络安全公司带来的短期机遇。

举一个很直观的机遇。大多数读者可能都刷到过这条新闻：三星半导体部门工程师将公司绝密数据喂给了 ChatGPT，虽然并不会被 ChatGPT 直接学走，但是数据不可避免地泄露到了 OpenAI 的服务器上。**这绝对不是孤例，每家公司都在面临巨大的数据泄露风险，一部分大型企业选择了先使用 Netskope 和 Palo Alto Networks 等 SSE/CASB 供应商的产品将就着。**Office 365 转云带动了 CASB 的兴起，ChatGPT 和 LLM 的出现为 CASB 厂商提供了短期红利，但是它们需要快速创新以适配客户对 LLM 的精细需求，不然新时代的 Netskope 可能出现，或者 OpenAI 自己也可以入局将敏感数据泄露问题解决掉。

其他的机遇包括 API 安全、邮件安全、应用安全在 LLM 时代的变化，和 LLM 对自动化的智能 SecOps 的助力。

在这些趋势下，我非常看好 Netskope 和 Palo Alto Networks，你可以在正文找到原因。

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 更清晰地讨论“AI 安全”

02 大部分企业安全堆栈不会消失

03 深入剖析 LLM 剧变下的五大安全机遇

04 小结

**01.**

**更清晰地讨论“AI 安全”**

讨论安全在最近几个月的 LLM 狂潮下格外令人抓狂 —— Safety 和 Security 在中文里都叫安全，LLM 本身的安全和它对于传统网络安全的影响两者之间的边界也非常模糊，这为 AI 安全的讨论带来了背景上相当的不一致性。

我们在这篇文章中试图提出一个更清晰和非常简单的框架，从而帮助我们日常更好地讨论“AI 安全”：

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/005.jpg)

在这个框架里，我们划分出了 3 个概念：

**• AI Safety**

这是一个古老的名词，更聚焦于 AI 系统的内部，具体内容包括模型与人类意图的对齐、可解释性和鲁棒性等。在大模型和逼近 AGI 的时代，这个安全概念和 Alignment、RLHF 等具体的概念耦合地更深，强调让 AI 为人所用，尽可能地消除 AI 对人类造成伤害的可能性。在上周发布的 *Our approach to AI safety* 中，OpenAI 再次强调了它引领的这个定义 —— 在 GPT-4 完成训练后，OpenAI 花费了 6 个月的时间让模型更安全、**更（与人类意图）对齐**。

我认为在 AI Safety 的议题和生态上占据主导权的将是开发模型的公司们，比如 OpenAI、Anthropic 和 DeepMind 等领导者，而我们之前关注的 Scale AI 和 Surge AI 等标注公司有机会从人类反馈的标注需求中获益。除了商业公司外，AI Safety 也会是从计算机科学到社会政策等广泛的学术界关注的重要问题。

**• Security for AI**

AI Safety 关注 AI 系统的内部，而 Security for AI 更关注如何保护这些系统免受外部威胁和攻击，并且符合现实世界的合规框架。相较于更广泛的网络安全，Security for AI 则更聚焦于对 AI/ML 模型的保护，而更少关注外围的防火墙和网关等防护层。

许多我们熟悉的 AI for Security 公司在 LLM 时代前已经存在，比如进行模型监控的 Arize、Fiddler、Credo 等，它们传统上帮助公司确保其机器学习模型满足数据安全要求、保护用户隐私并且结果无偏见，并提供一定的可解释性。类似的工具在 LLM 时代还有 Calypso AI 等。同时，LLM 带来了新的攻击手段和防护需求，比如下图是最通俗易懂的“Prompt 注入攻击”。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/006.png)

*Riley Goodside 在 Twitter 上演示的恶意输入攻击示例*

**• AI/LLM 对于现有的网络安全堆栈的影响**

从经典网络安全堆栈的视角看，端点、网络和身份安全的需求一直存在，但是其背后的技术一直在演进 —— 1990 年代开始出现的 McAfee 们基于硬编码的签名数据库来杀毒，2010 年代路线出现的 CrowdStrike 们则开始使用云和有监督的浅层机器学习。在端点安全之外更富有创新性的安全领域里，我们已经看到无监督学习的兴起和人类反馈的引入。因此网络安全一直是跟 AI 的发展一起演进的。

在 LLM 横空出世后，我认为它对于现有的网络安全堆栈的影响主要是三方面：

**1. 与 LLM 的交互带来了新的安全需求，**比如企业内部希望控制员工使用 ChatGPT 时泄露敏感信息，此外由于 GPT-4 和 PaLM 等领先的模型都以 API 的形式对外交付能力，对 API 作为新兴的 Attack Surface 的保护需求也将增加；

**2. 攻击者并不攻击模型，而是利用 LLM 进行其他攻击。**LLM 天然适合各类 Social Engineering，可以用来批量生产钓鱼邮件，还能伪造证书、凭据、身份等。生成恶意代码也是一个重要的攻击手段。这在现在网络安全供应商的防护范围内，但是它们仍需要一定程度的创新；

**3. LLM 可能会为安全的某些环节带来颠覆式的改变。**天然的两个场景分别是代码生成阶段以及 SecOps 环节。我们将在本文的 03 中详述。

**02.**

**大部分企业安全堆栈不会消失**

大家有理由对 LLM 在安全领域发挥的作用感到兴奋。我非常喜欢的安全工程师 Frank Wang 为各类安全公司提出过一个高度概括性的总结：

💡

绝大多数的安全用例本质上可以归纳成两点：

1. Access Management；

2. Visibility。

每家安全公司本质上都在收集系统或设备中收集各类数据，其中一些特定的数据可以通过提供额外的上下文，来显著提高检测可疑和恶意活动的能力。这些数据是平台级安全公司的核心，并且使它们能更容易地构建垂直的应用作为产品交付给客户。

在 [**The Age of AI：拾象大模型及 OpenAI 投资思考**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501241&idx=1&sn=aa2046e1cb75cb21b703805f294b6d5c&chksm=ce9b7a27f9ecf331863dc73ddc883373d18db3eaba2c847b0b147edd359f2b899942c62b4115&scene=21#wechat_redirect)中，我们分享过可被采集的数据结构和数据规模都将迎来变化，此外由于计算机的理解能力上升，拼接上下文的想象空间也将被打开，而传统的垂直安全应用的交互形式也非常可能会发生变化。这都为 LLM 发挥作用提供了想象空间，一种具象的形态可能是 Palo Alto Networks 的 Cortex XIASM 产品，我将在 03 中多聊聊。

在这些想象空间之外，一个事实是 —— 大部分安全堆栈在大模型时代不会消失。这里的逻辑非常简单，安全能力的很多关键部分与语言模型关系不大，同时一旦采取行动的出错后果会比较严重，因此中短期内 LLM 在其天然契合的场景发挥 Copilot 的副驾驶作用会是比较理想的形态。

**印证这一点的产品是 Microsoft Security Copilot，上个月在 Microsoft Secure 大会上新鲜出炉。**

要知道，微软是安全和 LLM 交叉点上最具有竞争力的公司，它的安全收入在上个季度突破 200 亿美元，并且安全是集团战略的重要支柱。22 年的 Microsoft Ignite 大会的 Keynote 演讲也给了安全很大比重，几乎有一半时间在讨论安全产品。同时微软还重新梳理了安全产品线，全部以 Microsoft 打头，打破过去安全能力和产品分散在 Windows、Office、Azure 各个部门的情况。

而 Security Copilot 这一封答卷完全没有摧毁其已有的安全产品的价值，只是让 Copilot 作为可以使用自然语言交互的对象来帮助客户更好地进行 SecOps（比如可疑行动的调查），背后的安全能力仍然有 Defender 和 Sentinel 等产品提供。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/007.png)

类似的例子还有 OpenAI。**这是全世界最懂 LLM 的公司，但是毫不令人意外，它仍然需要传统的企业安全堆栈来保护自己，比如使用 Cloudflare、Auth0 来管理流量和用户身份。**我相信任何人都很难想象 LLM 如何替换 Cloudflare 的全球路由网络。ChatGPT 上个月还经历了宕机，核心原因是 Redis 库里的新 Bug，更好地处理这种问题仍然需要 Datadog 和 Sumo Logic 这样的 APM 和可观测性供应商。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/008.png)

**03****.**

**深入剖析 LLM 剧变下的五大安全机遇**

下面我会详细聊聊 LLM 为现有的网络安全堆栈带来的机遇，请注意这里列举的五大机遇并不是为了穷举当前的变化，而是旨在列举出最前沿的一些景观让读者对这些变化有些体感。

**LLM 时代的数据防泄漏**

💡

安全环节：SSE；

机遇类型：渗透率提升、产品增购；

机遇的可能捕获者：

• SSE 玩家：Netskope、Palo Alto Networks、Zscaler、微软、Cloudflare 等；

• 大模型玩家：OpenAI 等；

• 新兴创业公司。

ChatGPT 中的数据防泄漏（DLP）是企业客户目前绝对的头号安全需求。

根据 CYBERHAVEN 在 3 月 21 日发布的调查，8.2% 的员工在工作场合使用过 ChatGPT，6.5% 的员工曾经将公司数据粘贴进去过，3.1% 的员工曾经将公司敏感数据喂给过 ChatGPT，敏感数据占员工粘贴总数据的 11%。Traceable 的 VP Jisheng 在近期的一个分享中也表示，其服务的银行大客户都有迫切的 ChatGPT DLP 需求。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/009.png)

类似的剧本在 Office 365 转云时代曾经上演过，这引发了 CASB 的兴起，目前微软的 CASB 部门贡献超 20 亿美元的收入，接近微软在云安全方面一半的营收，独立的供应商如 Netskope 也已经拥有超过 2.7 亿美元的 ARR。这些 CASB 的 Out-of-Band 产品通过 API 监控用户在 SaaS 内的活动，其 inline 产品则先将用户流量转发至供应商的 PoP 检查后再发送给 SaaS，这种 inline 的处理方法对于目前 LLM 的 DLP 具有相当大的可迁移性，因此我认为顶级的 CASB 玩家有机会从中受益。

对于不熟悉 DLP 领域的读者来说，最传统和初级的 DLP 解决方案通常只用来保护 PII 数据，比如 SSN 或者信用卡号，它们相当地“可识别”，只要阻止员工对外粘贴任何对应位数的数字即可。但是用户丢给 ChatGPT 的是五花八门的文字，并且是否敏感强烈取决于客户公司的业务背景，因此这些初级的 DLP 对于 ChatGPT 来说几乎是完全失效的。

在这个背景下，对 ChatGPT 最简单的 DLP 应对是封建其 URL，这完全封死了员工的灵活性。像 Netskope 这样的厂商可以提供更精细化的管控。比如对用户发出警告，只有在他们再次确认后才将问题提交给 ChatGPT：

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/010.png)

客户还可以使用 Netskope 创建更高级的规则，比如拦截特定的字符串或关键词：

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/011.png)

Netskope 目前为 ChatGPT 提供的 DLP 能力已经属于 60 分左右可用的水平，所以我们了解到目前客户对 Netskope 和 Palo Alto Networks 在 LLM DLP 方面的咨询激增。但是随着越来越多基于 LLM 的 Web 应用出现，单一为 ChatGPT 这个应用构建的能力可能很快会失效，因此有更多的用户在呼吁 SSE 厂商将 AI 应用作为一类单独的类别管控。类似的需求会非常多，因此接下来一段时间将是观察各大 SSE/CASB 厂商产品能力的重要时期，能更快地为 LLM DLP 构建出 80-90 分水平产品的公司有机会抢走更多的订单和扩大增购。

需要留意的是 OpenAI 本身有机会成为这个领域的搅局者，鉴于各个国家和地区的政府（比如动作最大的意大利）和公司（从 Amazon 到 JP Morgan）都因为敏感数据问题而限制对 ChatGPT 的使用，OpenAI 可能需要通过自行构建或是与合作伙伴共建的形式为自己的应用构建更原生的 DLP 策略。

**自动化 SecOps 加速**

💡

安全环节：SecOps；

机遇类型：新产品形态、已有创新产品渗透率提升；

机遇的可能捕获者：微软、Palo Alto Networks 等。

这是一个可能会令 SOC 内一些分析师下岗的机遇，但的确 SecOps 的效率提升和整个 SOC 的成本缩减是大型企业在当前经济形势下非常重要的经营目标。这让 Palo Alto Networks 在去年底开始给大客户做 Beta 测试的 Cortex XSIAM 产品获得了极好的市场反馈，过去几个月时间已经超过了 1 亿美元 ARR，并且每个订单价值都在 100 万美元以上。

Palo Alto 的 CEO Nikesh Arora 对这个产品的来龙去脉讲得非常清楚，读者可以看他的原话：

安全方面，大多数企业传统上的 AI 是 garbage in, garbage out。企业大多数时候拥有 30-40 家安全供应商，从不同的供应商那里收集数据然后尝试将其交叉关联，这类似让 40 个说不通语言的人交流。你需要一个单一的事实来源。**因此 Palo Alto Networks 内部先做了实验，之前我们从 200 家供应商那里收到 6.7 万条警报，现在我们用自己的一个端点替换了这一切。我们对数据进行交叉关联，并通过使用 AI 将平均响应时间从 27 天缩短到不到 1 分钟。这就是我们 4 个月前投入市场的产品，名为 XSIAM。**

我认为这个概念将成为未来 5 年安全领域的颠覆性事件——让 AI 交叉关联数据，使其保持一致，在客户公司运行标准化的数据湖，并能够阻止威胁的发生。当勒索软件攻击发生，从入侵者攻击公司的时间点到他们提取 PB 级数据的整个时间为 14 小时，但今天大多数公司的平均响应时间为几天。所以对我来说，这是一件大事。这是需要发生的事情。希望我们成为市场上能够实现这一目标的参与者之一。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/012.png)

*XSIAM 产品界面*

*（绿色的数字和饼图代表被自动化的事件）*

Cortex XSIAM 在 ChatGPT 的 hype 之前并没有和 OpenAI 的直接集成，但是很显然它是一个非常易于叠加 LLM 的场景。

一个非常理想的 SecOps 自动化产品可能将是 Cortex XSIAM 和 Microsoft Secure Copilot 的结合，有强劲的安全能力、自动化处理能力和简单易用的自然语言交互界面。Palo Alto Networks 能够推出这一产品的重点在于它完整的安全堆栈 Portfolio，并且同时占住了防火墙和端点，通常拥有客户超 85% 以上的安全数据。拥有类似完整产品线的对手似乎只有微软。

**API 仍是新兴 Attack Surface**

💡

安全环节：API 安全；

机遇类型：渗透率提升；

机遇的可能捕获者：Cequence、Traceable、Noname Security、Salt Security 等。

除了云安全之外，API 安全是过去 3 年 VC 在安全领域押注的重点，最核心的 thesis 只有一项 —— 寻找下一个大的 Attack Surface，它曾经是端点，随着端点增多演变出了网络和身份，而随着 API 成为软件之间交流的核心纽带，它越来越有机会成为下一个诞生重要公司的 Attack Surface。

这是个非常新和快速崛起的领域，根据 US Bancorp 开放银行部门负责安全的 VP 回忆，18 年左右的 API 安全供应商还几乎是一片空白，OWSAP API top 10 到 2019 年才被单独提出。而根据 Future Market Insights 的调查，API 安全市场在 22 年价值大约 10 亿美元，预计在未来 10 年能够维持 25% 左右的复合增长率。

**LLM 当前的情况再次验证了这个 thesis，并为 API 安全增添了一些 upside，因为从 OpenAI 到 Anthropic、Cohere 乃至 Google 的 PaLM，最强大的 LLM 都以 API 的方式交付能力。**

OpenAI 的 Mira 在 Greylock 的活动采访中已经将这种方式视作一个安全上的默认最佳实践，用于持续和可控地对外部署 LLM，比如 GPT-3 就是先通过 API 部署到一小群用户，然后逐步扩大访问范围，在过程中进行黑灰产和滥用的治理。

具象来看，LLM 和 API 安全的结合有两方面：

1. 对于 OpenAI、Anthropic 和 Google 这些模型和 API 的拥有者来说，它们非常需要 API 安全公司提供的 Bot 防御能力。尝试使用它们 API 的可不光是正常用户，还有大量恶意编写的机器人和被盗的账户会对它们进行大规模的自动攻击，而 Cequence 等在这个方向领先的 API 安全供应商可以通过 AI/ML 的能力找到偏离基线的恶意行为从而帮助客户对 Bot 形成一定的治理和防御；

2. 对于这些 LLM 的 API 使用者来说，Traceable、Noname 和 Salt 等典型的 API 安全供应商可以让企业管理者对内部的 API 使用情况保持可见性（想象下你是一个小型独角兽的 CEO，然后你希望盘点下多少员工正在使用 OpenAI 的 API key，治理这种 shadow IT 通常非常麻烦），并尽可能避免经过身份验证的、无法防范的 API 使用威胁。

**恶意使用为邮件安全带来水花**

💡

安全环节：邮件安全

机遇类型：新技术代际产品

机遇的可能捕获者：

• 下一代邮件安全网关玩家：Cloudflare（Area 1）、Abnormal Security 等；

• SSE 玩家：Netskope、Palo Alto Networks 等；

• 新兴创业公司。

邮件安全是一个 20 多年来缺少创新的领域，Proofpoint 几乎统治着市场。

这种情况在疫情之后有些变化，因为在疫情期间钓鱼邮件数量显著上升，Proofpoint 的陈旧科技被打的千疮百孔，那些没用上 Proofpoint 和下一代防火墙的公司则迫切地寻找邮件安全供应商。这导致了 Area 1 和 Abnormal Security 这些下一代邮件安全领域的公司崛起，它们非常易于部署，并且有更好的爬虫技术、AI 能力，在疫情期间捕捉了大量用户需求。

由于 ChatGPT 和用于文本生成的 LLM 能力过于强大，我们可以预见钓鱼邮件和各种形式的 Social Engineering 继续发生，这将持续助推疫情以来在邮件安全领域发生的创新。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/013.png)

*Abnormal Security 演示*

*让 ChatGPT 创建一封勾引收件人点击链接的邮件*

尽管这个方向有一定的门槛，但是其下一代邮件安全的解决方案本质仍然是用 API 连接到 Gmail、Outlook 等邮箱上，然后分析异常行为和数据，这和 Out-of-Band CASB 的解决方案非常相似，理论上 Netskope 和 Palo Alto Networks 都可以随时扩大它们在这个领域的影响力。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/014.png)

**应用程序安全可能变天**

💡

安全环节：应用安全；

机遇类型：新产品形态；

机遇的可能捕获者：GitHub、SourceGraph、Snyk、GitLab 等。

GitLab 本来也在 DevSecOps 的大道上走得正好，Snyk 也在这个蓝海中快速崛起，但是突然间 GitHub Copilot 成了搅局者 —— 如果“代码生成”和程序员写代码的过程继续耦合，拥有 Copilot 和 OpenAI 下一代 Codex 深度绑定的 GitHub 将成为程序员和代码的中枢性平台，可以高打低把安全给兼容掉。

StrongDM 的安全 SVP 代表着一类典型客户：

StrongDM 目前使用 Snyk 扫描代码漏洞。GitHub 一直无法分析 IaC 或者其他第三方依赖，一旦 GitHub 提高它在安全方面的布局，将非常有动力从 Snyk 切换到 GItHub。

对 GitHub 进军的信心来源于多个方面：

1. 这个世界上大部分的源码存放在 GitHub，这让它能了解和接触到最丰富的漏洞；

2. 微软内部其实完整具备 Snyk 交付的这种安全能力；

3. Copilot 是很好的信号，先用 AI 写代码，下一步就可以使用 AI 读取代码并扫描漏洞，并且可以让漏洞扫描不再是基于规则的，而是 LLM 驱动的。

公司目前每个月给每个工程师支付 150 美元的 Snyk 费用，而 GitHub 每个工程师每年也只有 250 美元。从成本和减少供应商的角度，有非常强的迁移动力。

波太金在他这篇《[**AI 如何颠覆软件：你能为 AI 打工吗？**](http://mp.weixin.qq.com/s?__biz=MzI2MTM2MTgxNQ==&mid=2247485067&idx=1&sn=8bf37ff8a7a7aeac7da10c4c87131fef&chksm=ea5adf73dd2d56655d5ae8e7783783b0162c56a1ef99b5b74ee6efdd512d0f18c709f13e2db5&scene=21#wechat_redirect)》中讲了对 GitHub 最 Bullish 的判断：

代码库产品在**过去主要承担的是分类与存储的功能，代码及安全能力，以及与 CI/CD 其他产品的集成，在未来这些很可能都不是最重要的。**

**在 AI 的影响下：**

• 代码库将很快变成**“写代码的工具”**，而 GitHub Copilot 作为在 AI 浪潮至今，最让人兴奋的应用级产品，将继续保持对行业内其他代码库公司的领先优势；

• 成为“写代码工具”的**代码库将成为整个 Dev 流程的核心中的核心**，在未来渠道项目管理工具的核心地位，AI 未来将有**开发流程的“派单权”**。

现实点看，GitHub 切入安全环节已经有一定的可能性了。微软的架构师 Jorge 展示了 Azure OpenAI Service 和 davinci-003 模型进行代码漏洞扫描的能力：

davinci-003 能够发现 SQL 注入。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/015.png)

davinci-003 能够识别出 CSRF。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/016.png)

davinci-003 能发现身份验证和会话管理失效。

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/017.png)

不过，在我们见到 Codex 2.0 之前，GitHub 对 GitLab 和 Synk 这些玩家目前还不是绝对碾压级的优势。通过 OpenAI 和 LangChain，客户可以自行在 GitLab 的 CI pipeline 中创建自动化的代码检测和修复能力，做到接近 Copilot 的体验，而 Snyk 也有一定的 AI 布局，在 20 年收购了 DeepCode，在上个月还参投了使用 AI 来自动化代码测试的 CodiumAI。随着 Copilot 的能力边界继续扩张，Snyk 和 GitLab 如何演进其产品是个非常值得观察的课题。

**04.**

**小结**

站在全球成长期投资者的角度，我们花费许多时间思考的问题是：现在已经进入成长期的公司是否会被更 LLM Native 且更灵活的早期公司颠覆？

这个问题的答案最终收敛到一个关键判断和五个关键维度上。一个核心关键判断在于 —— OpenAI 一家独大的局面是否会持续维持，如果 LLM 今天这样的格局维持下去，OpenAI 将有很强的动力进入许多自然的垂直场景，比如使用 ChatGPT 时的 DLP、Codex 和 GPT 能够提供的代码安全扫描能力等。安全公司对于 OpenAI 的市占率没有干预的可能，所以更重要的是下面五个关键维度：

**1. 在客户预算和安全堆栈中，重要程度越高越安全。**在应用程序安全的 StrongDM 的案例中，我们可以看出 GitHub 和 Snyk 对于客户的重要程度显然不同。拥有更稳固地位的安全公司通常是 SSE、EDR 和 CSPM 公司，LLM Native 的应用很难找到足够的价值主张来入侵这些领域；

**2. 产品线越丰富越安全。**微软和 Palo Alto Networks 属于此类，丰富的产品线意味着深厚的客户关系，不光不容易被颠覆，还更有可能在 SecOps 和 SOC 自动化的趋势中受益；

**3. 没有技术债务并且能够快速创新的公司越安全。**Netskope 是这个维度的最好案例，它在 CASB 和 SSE 的竞争中突围主要就得益于持续的创新力以及尽可能少的技术债务，这对于 LLM 时代同样重要；

**4. 拥有“硬积累”的安全公司比只有“软积累”的安全公司更安全。**这一点非常“顺常识”，Cloudflare、Netskope 这样的公司在全球建设了足够多的 PoP 才能提供足够低延时和高性能发服务，仅仅 LLM Native 并不能改变这种物理基础设施建设层面的差距；

**5. 拥有更丰富的无监督学习使用经验的公司更安全。**一部分缺少 DD 和安全领域 Know-How 的投资者可能会判断 CrowdStrike 等同样有 AI 标签公司是 LLM 浪潮的受益者，但事实是它们往往使用了有监督的、浅层的深度学习，和现在的无监督的、深度学习不是同一个方向。考察一家安全公司使用机器学习和使用无监督学习的具体年份应该成为 DD 时的重要问题。

**Reference**

https://www.youtube.com/watch?v=wqXsCMc5lzQ

https://www.cyberhaven.com/blog/4-2-of-workers-have-pasted-company-data-into-chatgpt/

https://community.netskope.com/t5/Next-Gen-Secure-Web-Gateway-SWG/Netskope-Next-Gen-Secure-Web-Gateway-Controls-for-ChatGPT/td-p/3646

https://www.cequence.ai/products/api-spartan/

https://abnormalsecurity.com/blog/double-edged-sword-of-chatgpt

https://www.crowdstrike.com/cybersecurity-101/machine-learning-cybersecurity/

https://nocamels.com/2023/03/generative-ai-startup-helps-developers-test-code-logic/

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/018.png)

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/019.png)

延伸阅读

[![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/020.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501604&idx=1&sn=52bc78af407aacc49549f0bb050cffce&chksm=ce9b78baf9ecf1ac66bd00c5030b72ffe6628e241dcc2f3088d323bf94f62681691a66cbd95d&scene=21#wechat_redirect)

Replit：“人人可编程”的探索者，代码生成时代的Figma

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/021.png)

[![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/022.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501351&idx=1&sn=31597b03b587b5eaf0132f2392f581e6&chksm=ce9b79b9f9ecf0af030f54142f5639296643713edc719d3839756f2ae3d5ee514502f1378461&scene=21#wechat_redirect)

Inworld：AI NPC能否将《失控玩家》的游戏体验带入现实？

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/023.png)

[![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/024.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501299&idx=1&sn=99e93b17273cb535610ff6213b79802e&chksm=ce9b7a6df9ecf37b41d90c4a0d1be2622f3bae3d74635ca5616f83ccb894d71bb90ef886ddd4&scene=21#wechat_redirect)

Scale AI：大模型还需要数据标注吗？

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/025.png)

[![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/026.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501241&idx=1&sn=aa2046e1cb75cb21b703805f294b6d5c&chksm=ce9b7a27f9ecf331863dc73ddc883373d18db3eaba2c847b0b147edd359f2b899942c62b4115&scene=21#wechat_redirect)

The Age of AI：拾象大模型及OpenAI投资思考

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/027.png)

[![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/028.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501117&idx=1&sn=e860ac5e259a969f62b05d080bf42d14&chksm=ce9b7aa3f9ecf3b503656e9a09b55210fdba0844b54bd6a5714f5fc8c57b8c3570acbe2d342f&scene=21#wechat_redirect)

LangChain：Model as a Service粘合剂，被ChatGPT插件干掉了吗？

![](../images/2023-04-13-yun-zhi-hou-da-mo-xing-shi-wang-luo-an-quan-de-xin-ji-hui-ma/029.png)
