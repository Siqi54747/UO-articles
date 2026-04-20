---
title: 为 OpenAI 秘密提供模型测试， OpenRouter 给 LLMs 做了套“网关系统”
publish_date: '2025-09-23'
publish_timestamp: 1758613800
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/upu73ygn2Sc89vZBOvm8Ow
msgid: 1000000425
appmsgid: 2247518212
itemidx: 1
digest: 不只是模型用量风向标
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgwhJtU6ziaEYoLwtambxpXsMq4mXdqfE4gmDmUeTuEVKLDXPAGSagdqMKiaftIl2URQe7h9gh4XoBnQ/0?wx_fmt=jpeg
image_count: 25
archived_at: '2026-04-20T04:26:43+08:00'
---

[![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/002.png)

编译：Xeriano

编辑：Haozhen

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/003.png)

在 [2025 Q2 的大模型季报](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517203&idx=1&sn=1444daf92341aadaeee873f0a7479c53&scene=21#wechat_redirect)中，我们判断硅谷的各个模型公司已经开始分化到各个领域：Google Gemini 和 OpenAI 在做通用的模型；Anthropic 分化到了 Coding、Agentic；Mira 的 Thinking Machines Lab 分化到了多模态和下一代交互。

随着应用场景的不断细分，用户请求也需要被路由到最合适的基础模型上，模型路由逐渐演变为大模型市场重要的 infra。OpenRouter 就是这一领域的佼佼者。

OpenRouter 成立于 2023 年初，为用户提供一个统一的 API Key，来调用各类模型，OpenAI 甚至在模型正式发布前，会先用其他名字在 OpenRouter 上秘密上线，用来收集开发者使用反馈。今年，OpenRouter 的周请求量从年初的 4050 亿 tokens，增长到 9 月的 4.9 万亿，增长超过 12 倍。

值得一提的是，OpenRouter 关于模型用量的报告在业内和社交媒体上都引发了广泛讨论，一度“出圈”，成为开发者和投资人群体的必读内容。

为了更好了解 OpenRouter，我们整理了创始人 Alex Atallah 的近期观点。Alex 认为大模型不是一个赢家通吃的，开发者会希望根据请求对模型进行路由，并且对使用体验拥有完全的控制权，OpenRouter 正是切中了这一诉求。未来，Alex 希望 OpenRouter 能成为 agent 的最佳推理层，为所有模型添加记忆、网页搜索这些有状态的 agent 能力，让开发者永远不被模型供应商锁定。

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/004.png)

**01.**

**OpenRouter 是什么？**

OpenRouter 创立于 2023 年初，给用户提供一个统一的 API Key，用于调用自身接入的所有模型，既包括了市面上的主流基础模型，也包括部分开源模型，一些开源模型还有多个不同的供应商。如果用户选择使用自有的 Key ，也可以同时享受 OpenRouter 的统一接口与其他服务。

在使用过程中，OpenRouter 会根据用户的 prompt，自动或依据用户指定的条件（如价格、时延、吞吐量或综合指标），将请求路由至最合适的模型和供应商。同时，OpenRouter 会展示不同供应商的价格、地理位置、吞吐量和时延等信息。

今年，OpenRouter 平台的 token 用量经历了高速的增长。6 月，公司完成了 $40M 的融资，投后估值 5 亿美金，投资者包括 a16z 和 Menlo Ventures。截至 8 月，平台的 token 用量已经从今年年初的 405B 增长到 3210B，增长了约 8 倍。

**OpenRouter 解决了 API 调用的三大痛点**

1. 缺少统一的市场与接口：目前市面上 API 众多且格式不统一，采购和管理成本非常高。OpenRouter 提供了统一模型调用接口，可以简化采购、账单和用量管理。

2. API 不稳定：即使是 OpenAI 也无法始终保证 API 的绝对稳定。而 OpenRouter 由于同时接入了大量模型，如果是开源模型，还有多个供应商，因此如果一个模型供应商的服务器暂时宕机了，OpenRouter 可以为用户自动的选择其他类似的供应商，这种方式增加了 API 的稳定性。

3. 成本与性能难以平衡：不同模型价格差异非常大，OpenRouter 可将简单任务分配给低成本模型，复杂任务交给高性能模型，实现成本与性能平衡。

**模型用量排行榜**

一直以来，OpenRouter 发布的报告都广受开发者和投资人的关注，往往是行业热议的话题。

作为模型路由平台，OpenRouter 掌握了用户在各家模型上的使用数据，比如不同场景、应用和模型的调用占比，并将这些数据开源出来，这既帮助用户直观了解了各模型的受欢迎程度，也提升了 OpenRouter 的知名度。

滑动以查看全部内容

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/005.png)

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/006.png)

OpenRouter 的模型用量排行榜

马斯克就曾多次引用 OpenRouter 的数据宣传 Grok Code：

1. 2025 年 8 月，他在推特上庆祝自家模型 Grok Code 登顶 OpenRouter 排行榜，超过 Claude Sonnet；

2. 9 月，他又发文称 Grok Code 调用量突破 1 万亿次，帖子当日的浏览量就超过了 500 万。

这些事件也为 OpenRouter 带来了巨大的曝光。

滑动以查看全部内容

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/007.png)

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/008.png)

Musk 发布的推特

以下是创始人 Alex Atallah 近期的一场访谈，经海外独角兽编辑整理。

**02.**

**大模型不是一个赢家通吃的市场**

**Ejaaz:****你之前是 OpenSea 的联合创始人兼 CTO，现在是 OpenRouter 的创始人，能否和我们分享一下你之前在 OpenSea 的经历，以及为什么会创立 OpenRouter？**

**Alex:**我在 2017 年底，与 Devin Finzer 共同创立了 OpenSea。OpenSea 是第一个 NFT 市场。它和 OpenRouter 相似，同样存在一个零散的生态系统，比如分散存放的 NFT 元数据。作为加密领域中最早的“不可替代”案例，NFT 是一种独立的数字物品，可以在不同用户之间自由转让和交易。但世界上大多数事物都是不可替代的，比如一把椅子，它是独一无二的；而货币则是可替代的。

OpenSea 是一家美国的 NFT（非同质化代币）在线交易平台，由 Devin Finzer 和 Alex Atallah 在 2017 年创立。它支持在多种区块链上进行 NFT 的购买、出售和铸造，涵盖的数字资产类型包括艺术品、音乐、游戏道具和域名等。

在 2018 年，没有人从“不可替代商品”的角度去思考加密货币。当时的问题在于没有统一的标准来表示和交易这些不可替代的物品，OpenSea 正是把这些分散、异构的资源整合到一个平台上。我们制定了元数据标准，并投入了大量工作，确保用户在浏览和交易每个藏品时，都能获得良好的体验。

这和今天 AI 的运作方式有很多相似之处：同样存在一个由不同模型和提供商组成的高度异构生态系统，各自提供不同的功能。OpenRouter 也投入了大量精力，把这些分散的资源进行整合与组织。我在 OpenSea 一直工作到 2022 年，当时我想做一些新事情，我在 8 月离开了公司，几个月后 ChatGPT 就发布了。

那时我最大的问题是：这会是一个赢家通吃的市场吗？因为当时 OpenAI 遥遥领先于其他所有人，尽管我们有 Cohere Command 和其他几个开源模型，但 OpenAI 是唯一真正可用的。

我当时用 GPT-3 的 API 做了一些小项目，接着 Llama 在 1 月发布了，它的大小大约是 GPT-3 的十分之一，在一些基准测试中表现不错，但当时还不能很好地聊天。几个月后，斯坦福大学的一个团队将 Llama 蒸馏成一个叫做 Alpaca 的新模型，他们先用 ChatGPT 蒸馏了一套合成数据，然后在 Llama 上微调。这是据我所知第一个成功的大规模蒸馏项目，而且 Alpaca 是一个真正可用的模型。

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/009.png)

Alpaca 7B 基于 LLaMA 7B 并用 ChatGPT 蒸馏的数据进行微调，仅花费不到 $500

当时我在想，如果只花六百美元就能训练出像 Alpaca 这样的模型，那就没必要投入上千万美元去做一个模型了。这样一来，未来可能会涌现成千上万个模型，这些模型就像一种新的原语，它们理应在互联网上占据一席之地。可问题是，当时并没有一个平台能让人们方便地发现新模型，也看不到是谁在用它们、又是出于什么目的。OpenRouter 正是在这样的背景下诞生的。

在计算机科学中，原语（primitive）指的是构成更复杂操作或数据结构的最基本、最简单的单位。它们是编程语言提供的基础构建块，本身不能被分解成更小的部分。

**Josh:****当你在探索新的科技前沿时，你认为什么是最重要的？**

**Alex:**我觉得找到发烧友社区并尝试融入其中是非常关键的。每当有新事物出现，而且它具备形成生态系统的潜力时，都会孕育出这样的社区。互联网让这一切变得顺理成章，你只需要加入进去就好。

Discord 是一个非常好且被严重低估的平台，因为里面的社区相对私密，你不会觉得有人在为了 SEO 而刻意推广。在 Discord 里没有 SEO，只有人们围绕自己热爱的事物交流，而且话题往往非常小众。比如，当你在 Discord 上加入一个围绕某项刚刚出现、还不太成熟的新技术的小组时，你会看到大家一起探索如何使用它、如何改进它。我认为这才是最有价值的地方。

我认为要保持一种愿意变得古怪的心态。因为如果你只从表面去看，这些社区往往显得很傻，比如“哦，这只是个游戏”或者“这是个奇怪的收藏游戏，我对这种东西没兴趣，所以我要退出”。但关键是，你不能只停留在这种表面判断，而是要带着创造力去思考。比如，那些在区块链上交易的“猫”，不该只被看作是人们单纯买卖虚拟宠物，而是要想它们解锁了过去无法实现的什么可能性？有些人天生擅长这样做，他们会加入社区，在实时交流中不断碰撞想法，你能清楚地看到大家一起头脑风暴、不断探索新的可能。

另一个很典型的例子是 Midjourney 的 Discord，它后来成为了 Discord 上最大的社区。Midjourney 最初看起来有点奇怪、傻气，甚至似乎没什么用，但你能看到发烧友们都在里面实时头脑风暴，探索如何让它变得更美好、更有价值。结果，然后它就爆炸式地增长了。在我看来，这是 Discord 上最令人惊叹的小众社区：从一开始看似无用，到后来变得无比疯狂又令人振奋。

但我早在 2021 年看到一个叫做 Big Sleep 的模型，可以生成类似 DeviantArt 风格的图片。那些图片都是动态图像，没有太多实际用途，但常常能带来一些非常酷的效果，虽然它们并不是你会拿来当桌面壁纸的东西。但如果你深入 DeviantArt 社区，就能学会欣赏这种美感。那时候我就认为这里面有很大潜力。又过了一两年，Midjourney 才真正流行起来。

**Ejaaz:****你是在随机的论坛里找到这些信息的，还是跟着你的直觉去寻找的？**

**Alex:**有一个 Twitter 账号专门发布 AI 研究论文，并展示这些论文背后可能的应用。我大概在 2021 年发现了它。虽然和加密货币完全无关，但我觉得 Big Sleep 是我第一次看到能用 AI 生成、并有潜力成为 NFT 的东西。于是我开始尝试，看能否引导它创作出一个有意义的 NFT 系列，结果发现这件事极其困难。

**Ejaaz:****为什么即使 GPT 已经出现，你仍然坚信未来会有成千上万，还是几十万个 AI 模型？在当时这并不是一个共识。**

**Alex:** Alpaca 的出现让我相信未来会有很多很多模型，而不是只有少数几个。Alpaca 是在 Llama 发布之后出现的，因为 Llama 是一个文本补全模型，所以人们很难很好地与它聊天。但是在一些基准测试中，它击败了 GPT-3，而且它的尺寸大约是 GPT-3 的十分之一，所以这是一个很了不起的成就。

Alpaca 的团队用 ChatGPT 生成了大量合成数据，再利用这些数据对 Llama 进行微调。这一步实际上带来了两个效果：一方面，微调赋予了模型对话的风格，让模型能够更自然地“聊天”；另一方面，也在一定程度上传递了知识，让模型更聪明。因此 Alpaca 在交互体验上弥补了当时最大的缺口，同时在后续的基准测试中也展现出更强的性能。

如果能够在不泄露全部输入数据的前提下做到这个效果，那么就能通过 API 来出售数据，而不是一次性将数据公开、从此失去价值，永远无法再次变现。由此，围绕数据诞生了一种全新的商业模式。这种模式不仅能让数据持续变现，还能推动开放智能的发展，更高效地构建和测试新架构，并快速完成微调，也就是说，你可以在巨人的肩膀上进行构建而不需要每次都从零开始。

许多最重要的开发者体验创新其实就是让开发者能够从更高的起点开始，而不必每次都从零起步。Llama 就为社区提供了这样一个巨大“馈赠”，但它并不是唯一在做开源模型的公司：几个月后，Mistral 发布了自己的 7B Instruct 模型，这是一个非常出色的模型；几个月后，他们又推出了第一个开源专家混合模型。这个模型感觉就像实现了真正的智能，但完全开源。这些进展为其他开发者提供了更高的起点，让全世界的众包创意能够在坚实的基础上发展，不断迭代和创新。

当我看到整个趋势逐渐清晰时，我意识到这个领域将面临一个“库存过剩”的问题。这让我联想到 NFT 收藏品的情况，尽管两者完全不同，市场机制和买家目标也各不相同，但本质上都是面对大量库存。我早期的很多实验，比如开发了一个名为 window.ai 的 Chrome 扩展，目的只是为了了解这个生态系统如何运作，它与其他领域有何不同，以及人们，尤其是开发者，真正需要什么。

window.ai 是一个 Chrome 扩展，让网站应用可以随意切换使用任意的大模型。

**03.**

**OpenRouter 是如何运行的？**

**Josh:****OpenRouter 是如何运行的？为什么有这么多人喜欢使用 OpenRouter？**

**Alex:**OpenRouter 是一个大语言模型的聚合器和市场。你可以把它想象成 Stripe 与 Cloudflare 的结合体。OpenRouter 就像一个统一的控制面板，让你在一个地方编排、发现和优化所有智能需求。你可以访问超过 470 个模型，但只需通过 OpenRouter 管理账单。

虽然这些不同的模型都能完成任务，但实现方式各不相同，而且如 Andre Karpathy 所说，模型经常会出现“智能褐化”（intelligence brownouts），即使是 Anthropic、Gemini 或 OpenAI 这样的顶级模型也可能宕机。

智能褐化（intelligence brownouts）这个概念由前特斯拉 AI 总监 Andrej Karpathy 2025 年 6 月在 YC AI Startup School 上的演讲上提出，指的是当 GPT、Claude 等模型服务中断时，整个互联网都变“笨”了。

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/010.png)

我们知道开发者有多样化的需求：首席技术官需要高可靠性，首席财务官希望成本可预测，首席信息安全官则需要复杂的策略控制。基于这些需求，我们构建了一个统一视图，让模型运行更可靠、成本更低、选择更多，并能帮助你决定从哪里获取智能服务。

**Josh:****你们如何决定将请求路由到哪个提供商，从而让用户的请求可以得到最佳的结果？**

**Alex:**我们并没有专注于为用户提供一个模型路由器，而是致力于帮助用户选择合适的模型。为此，我们在用户账户界面和排名页面上都创建了大量分析数据，让用户能够浏览和发现哪些模型在特定工作负载下被高级用户证明了是最有效的。

我们认为，今天的开发者仍然希望自己选择模型，因为在不同模型家族之间频繁切换可能会带来高度不可预测的行为。但一旦用开发者确定了模型，我们会尽力让开发者无需再费心考虑模型提供商。

对于同一个模型，通常有几十个提供商可选：既有大型云厂商如 AWS、Google Vertex 和 Azure，也有成长中的初创公司如 Together、Fireworks 和 DeepInfra，还有许多提供独特功能和高性能的供应商，每家都有各自的差异化优势。

我们所做的，就是把所有供应商集中到一个地方。

**•**如果你需要某个特定功能，我们会帮你找到支持该功能的供应商。

**•**如果你追求高性能，我们会优先将请求路由到性能最佳的供应商。

**•**如果你对成本敏感，我们会优先选择当前成本最低的供应商。

本质上，我们创建了各种路由通道，同时让你对整个用户体验保持完全控制。这正是我们在整个生态系统中发现缺失的东西：一种真正让开发者掌控模型访问方式的解决方案。

通过智能负载均衡，我们将请求发送到正常运行且最适合处理的供应商，这使得模型运行时间通常可以比直接连接供应商平均提升 5% 到 10%。我们非常注重效率和性能：整个过程仅增加约 20 到 25 毫秒的延迟，因为所有服务都部署在离你的服务器很近的边缘节点。

总体来说，我们把不同提供商的优势叠加起来，帮助你借鉴已有成果，充分利用大数据的力量，让开发者在访问自己选择的模型时，获得更可靠、更高效的体验。

**Josh:****你们是如何对 LLM 进行基准测试的？这些基准测试在用户路由中起到了怎样的作用？**

**Alex:**总体来说，我们的立场是：希望成为模型领域的“资本主义基准”（Capitalist Benchmark）。部分原因是我认为大数定律和高级用户的活跃参与对整个生态系统都有巨大价值。

这里的“资本主义基准”指的是模型领域中最能体现市场效率和用户价值、并且真实反映实际使用情况的标杆标准。

举个例子，如果你在欧洲使用 Claude 4，某个提供商的吞吐量可能会突然大幅下降。你通常只能在其他用户先遇到问题时才会发现。而我们会绕过在欧洲表现较慢的提供商，将请求路由到速度更快、符合你数据策略的其他提供商，从而提升性能。这就是在供应商层面上，数据如何带来帮助。

在模型选择层面的作用体现在我们的排名页面上。每当上线一个新模型，我们的高级用户会立即进行深入测试。他们会探索模型在哪些核心用例上表现出色，找出有趣的工作负载。然后，其他用户就可以从这些数据中受益。这就是为什么我们会在排名页面上免费开放和分享这些数据，让每个人都能从高级用户的发现中获益。

**Ejaaz:****我看到所有这些排名中都有一个一致的计量单位叫 token。OpenRouter 为什么选择 token 来衡量这些模型的表现或者用户的使用情况？**

**Alex:**我认为价格也是一个很好的衡量标准，但我们选择用 token 的主要原因是因为模型价格下降太快。OpenRouter 从 2023 年初就开始运行，我不希望一个模型仅仅因为价格下降得太快，就在排名上受到惩罚。这里有一个悖论叫杰文斯悖论（Jevons Paradox）：当价格下降 10 倍时，用户对某个基础设施组件的使用量可能会增加超过 10 倍，但他们实际上并没有获得真正的 10 倍增长。

杰文斯悖论（Jevons Paradox）由英国经济学家威廉·斯坦利·杰文斯（William Stanley Jevons）在 1865 年提出，指的是，当一种资源的使用效率因为技术进步而提高时，人们反而会更大量地使用这种资源，导致整体消耗不减反增。

相比之下，使用 token 作为衡量单位有几个优势：

1. 它不会因为模型价格下降而改变排名，也不会受杰文斯悖论的滞后影响。

2. token 还能体现时间维度：如果一个模型为大量用户生成了很多 token，并且持续了一段时间，这意味着这些 token 实际上被用户使用和阅读了。

3. 即使模型的 prompt 成本非常低，如果模型被用于处理大量文档，那这个模型仍然是有价值的。这种高使用量的情况是我们希望在排名中体现的用例。

因此，我们决定使用 token 作为衡量标准。未来我们可能会加入价格指标，用来观察哪些用例确实需要以成本来衡量。但我认为 token 的优势在于它不会受到杰文斯悖论带来的滞后影响。实际上，当时没有其他可行的指标，也没有任何公司在做类似的整体分析。直到几个月前，Google 才开始公开 Gemini 模型处理的总 token 数量。

**04.**

**OpenRouter 是如何与 OpenAI 合作的？**

**Ejaaz:****OpenAI 在正式发布他们的模型前，为什么会用 OpenRouter 进行低调测试？**

**Alex:**OpenAI 有时会提前向自己的部分客户开放新模型的早期访问权限来做测试。我们当时提出 OpenAI 可以和我们一起尝试一种“隐形发布”的方式，也就是用另一个名字上线模型，让用户可以在毫无先入偏见的情况下去使用。

OpenAI 决定尝试这种方式，于是我们和他们一起发布了 GPT-4.1，当时我们称它为 Quasar Alpha。这是一个拥有百万上下文长度的模型，也是 OpenAI 的第一个超长上下文模型，它也针对编程进行了优化。

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/011.png)

OpenRouter 上 Quasar Alpha 的发布界面

我们有一个专门运行开源基准测试的社区，其中许多人获得了我们的资助，用 OpenRouter 的额度来帮助他们测试。他们会对所有模型运行各种创意测试：

**•**有的会测试模型生成小说的能力；

**•**有的会测试它是否能在 Minecraft 中创建 3D 对象（MCBench）；

**•**还有一些针对不同编程语言的专项测试，比如 Ruby，因为事实证明很多模型在 Ruby 上的表现并不好。

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/012.png)

MCBench：比较哪一个 AI 生成的 Minecraft 建筑更符合题意

因此，我们积累了一整套非常小众但有价值的基准测试。这些测试人员都可以免费在 Quasar Alpha 上运行实验，并发现了非常惊人的结果。OpenAI 也能实时获得这些反馈。随后，OpenAI 基于用户反馈做了一个新版本的模版，以 Optimus Alpha 的名字发布，这样 OpenAI 可以对比两个版本的用户反馈。大约两周后，GPT-4.1 就正式向所有用户开放。

此后，我们又和另一家模型提供商尝试了类似的方式。这种方法的价值在于：你可以依靠社区的力量，获得许多意想不到的基准测试，并从中得到真实、客观、不带偏见的反馈。

**05.**

**开源模型承担着“优化最后一公里”的角色**

**Josh:****你如何看待开源模型和闭源模型，OpenRouter 如何为用户提供这两类模型的服务？**

**Alex:** 这两类模型都有供应方面的问题，但性质非常不同。

闭源模型的供应商很少，通常只有一到两家。比如 Grok 只有官方和 Azure，Anthropic 则有官方供应、Google Vertex 和 AWS Bedrock。我们还会在不同地区进行部署，比如我们在欧盟有部署，用来服务那些只想让数据留在欧盟的客户。同时，我们也会为闭源模型做定制化部署，确保用户获得良好的吞吐量和高请求速率。

在 OpenRouter 上，闭源模型占据主导地位，占用了大约 70%–80% 的 token。针对它们，我们的负载均衡更侧重于缓存和功能优化，确保用户能命中干净的缓存，并且只有在缓存过期时才切换到新的供应商。

开源模型的供应更分散，不同提供商的请求速率限制通常不够稳定，而大型公司往往需要一段时间，才能将一个新的开源模型打磨完善并提供稳定服务。所以我们为开源模型所做的负载均衡工作通常更有价值。

与闭源不同，大多数开源模型几乎没有缓存机制，所以用户切换模型供应商是非常常见的。与此同时，我们还会追踪开源供应商之间的质量差异。有些供应商会用较低的量化（quantilization）水平来部署模型，量化就像是一种压缩模型的方式，通常不会影响输出质量，但我们仍然发现部分供应商的结果会出现异常。因此，我们会在内部运行测试来检测这些问题，并计划投入更多精力，可以自动将质量不佳的提供商移出路由通道，避免影响用户体验。

量化（quantilization）指把模型中原本用高精度浮点数（如 32 位浮点数，FP32）表示的参数转换为低精度的数字表示，比如 8 位整数（INT8）。

**Josh:****闭源模型占据了大约 80% 的份额，这是一个非常大的比例。你觉得以后会发生改变吗？**

**Alex:**在短期内，开源模型可能会继续成为 OpenRouter 上增长最快的类别。虽然很多用户最初是为了使用某个闭源模型而来的，但在优化过程中，他们可能希望降低成本，或者尝试一个在特定应用场景上表现更好的模型，于是从闭源转向开源。换句话说，开源模型往往承担着“优化最后一公里”的角色。

当然，这只是一个总体趋势，反向情况也可能发生。但正因为开源模型经常承担这种优化角色，它们的增长幅度更容易被放大：一个原本几乎没人用的模型，一旦被部分用户（比如离开 Claude 4、寻找新编程用例的人）采用，就能表现出远高于闭源模型的增长率。而闭源模型由于用户基数本来就很大，增速显得没那么突出。

至于是否可能出现逆转，这是一个值得单独讨论的话题。

我认为，当前开源模型面临的最大问题是激励机制不足。相比之下，模型实验室和模型提供商拥有明确的激励：他们知道如何推动公司成长，以及如何吸引高质量的 AI 人才。而如果直接把模型权重免费公开，这些激励就会被削弱。

未来，我们或许能看到去中心化供应商在这方面发挥作用。比如，有一种既能够吸引优秀人才投入开源模型研发，同时又能确保至少保持权重开放的激励机制，这可能就是解决问题的关键。我个人也在努力与去中心化供应商保持紧密联系，从他们那里学习经验。在供应商层面，也就是运行推理的环节，确实已经涌现出一些很有潜力的激励模式。但在模型本身的开发环节，目前还没有看到足够的进展。

因此，如果未来出现某种逆转趋势，那它一定会显现在我们的视野里。但在此之前，我个人对此仍然持怀疑态度。

**06.**

**OpenRouter 的目标是成为 Agent 最佳推理层**

**Ejaaz:****OpenRouter 掌握用户 prompt 的所有数据，OpenRouter 打算如何处理这些数据？理论上，如果愿意，可以为每个用户创建最具个性化的模型？**

**Alex:**这是我们正在思考的问题。默认情况下，用户的 prompt 和输出内容都是完全不记录的，如果要记录，用户必须在设置里手动开启记录功能。而结果是，很多人确实选择了开启。因此，我认为我们可能已经拥有迄今为止规模最大的多模型 prompt 数据集。但目前我们几乎没有加以利用，只是对其中一小部分进行了分类，这就是你在排名页面上看到的内容。

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/013.png)

OpenRouter 模型用量排行榜（单位 / T Token）

在个人账户层面，我们主要能做三件事情：

1.**开箱即用的记忆功能**

今天，用户已经可以通过结合 OpenRouter 和“记忆即服务”（Memory as a Service）来实现这一点。比如 Memzero、SuperMemory 等公司都在做这类服务。我们可以与其中一家合作，或者自己提供类似功能，并借助 OpenRouter 的分发渠道推广。这样，模型就能真正“记住”你，在生成时自动补充合适的上下文。

2. **更智能的模型选择**

现在有很多模型，需要用户做出明确的迁移决策，我们能够从数据中清楚看到这些迁移趋势。目前，我们只是有一个渠道与客户保持畅通，来提醒用户：“你正在大量使用的模型已经被弃用，这个新模型在同类工作负载上表现更好，迁移到这个模型还能获得更优惠的价格。”但未来，这些建议可以变得更智能、更自动化，更自然地融入产品中。

3. **更深入的响应分析**

这是潜力最大的一块，就是智能分析模型和供应商的行为，并把结果展示给用户。比如：

**•**哪类 prompt 会流向哪个模型？

**•**模型给出的回复是怎样的？

**•**模型是否拒绝回答，拒绝率是多少？

**•**模型是否成功调用工具，还是忽略了所有工具？

**•**模型是否正确利用了上下文？

**•**在 prompt 发送给模型之前，是否发生了截断？

这些看似边缘的情况，往往会让开发者的应用“变笨”。而通过检测和分析这些情况，我们可以把最有价值、最直观的数据反馈给用户。

**Ejaaz:****OpenRouter 是否可以把 agent 作为内置功能提供？让用户能够使用更直观、具备丰富上下文的智能 agent。还是说，这已经超出了 OpenRouter 的定位范围？**

**Alex:**我们的策略是成为 agent 的最佳推理层。

我们认为开发者需要的是对 agent 运作方式的控制。对他们来说，OpenRouter 是一个统一的视图，可以直接运行推理，但同时又能清晰地看到并掌控 agent 的行为，agent 在循环中不断进行推理，并决定前进方向。因此，我们的重点是提供优秀的文档和高质量的原语，让开发者能够轻松上手。

很多开发者都在构建 agent，他们真正想要的是可靠的原语，这样就能不断迭代新版本和新想法，而不用重复实现工具调用。这也是一个难题，因为几乎每天都会有新的模型或供应商出现，开发者既需要它们，也会真正使用它们。因此，我们要专注于标准化这些工具并确保它们的稳定性，让 agent 开发者不必再为此分心。

**Josh:****随着我们越来越接近 AGI 甚至超越它，OpenRouter 的终局是什么？假设这些系统变得更智能后，它们能够自己做出决定并选择自己的工具集，那么 OpenRouter 会扮演什么角色？**

**Alex:**目前，OpenRouter 是一个自带工具的平台。我们还没有类似工具市场的 MCP，而我认为，大多数最常用的工具最终会由开发者自行配置，agent 会像被授予访问权限一样去使用这些工具。

我认为，OpenRouter 的终极目标是避免供应商锁定。不同于一些平台通过添加状态管理、服务器端工具调用、有状态网页搜索、记忆功能等粘性功能来让用户依赖它们，OpenRouter 希望开发者感到自由、有选择权，并且可以使用最优秀的智能模型，即使他们之前从未尝试过，但切换到更智能的模型永远不晚，这也是我们追求的“永远在线”的理念。

因此，我认为我们的未来方向是：要么与其他公司合作，要么在必要时自己构建工具，让开发者始终不会感到被束缚。这就是我的看法。

排版：夏悦涵

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/014.png)

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/015.png)

延伸阅读

[![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518173&idx=1&sn=4e2a05aa5ededbc950079253803c57eb&scene=21#wechat_redirect)

Agentic Enterprise：生成式软件重新定义企业形态｜AGIX PM Notes

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/017.png)

[![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/018.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518145&idx=1&sn=c4603e0ee1c1a45a0bcd4c1eafd4e016&scene=21#wechat_redirect)

Stripe x Cursor，硅谷两代“金童”对谈: 未来5年IDE里将不再是代码

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/019.png)

[![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/020.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518120&idx=1&sn=6f4e7c983c66e5a5c2b84be206ab223e&scene=21#wechat_redirect)

超越 Prompt 和 RAG，「上下文工程」成了 Agent 核心胜负手

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/021.png)

[![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/022.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518031&idx=1&sn=bb6cada95f0ffbb951f6bdcc21663afa&scene=21#wechat_redirect)

一半美国医生都在用的AI产品，OpenEvidence 是医疗界的 Bloomberg

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/023.png)

[![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/024.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517863&idx=1&sn=ebf449b114d7325f15247ad28ddddd61&scene=21#wechat_redirect)

Vibe Working：AI Coding 泛化的终局想象 ｜AGIX PM Notes

![](../images/2025-09-23-wei-openai-mi-mi-ti-gong-mo-xing-ce-shi-openrouter-gei-llms/025.png)
