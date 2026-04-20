---
title: LLM 进化分岔口：多模态、成本、代码推理
publish_date: '2024-09-05'
publish_timestamp: 1725540263
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/3Om_Ssen7F1kvCKKzm0NsQ
msgid: 1000000284
appmsgid: 2247509611
itemidx: 1
digest: OpenAI 和 Anthropic 的主线分别是什么？
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzPoJrtOobvRcbBUOss7FrHtTZT5FYlvj8sRN0QkGHjc5ftca40vibgd0YrGZg8nhMXb9icCjz58XWQ/0?wx_fmt=jpeg
image_count: 38
archived_at: '2026-04-20T02:37:26+08:00'
---

[![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/001.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508588&idx=1&sn=6f48ab2576f486b9365d9435c4d8c2e6&chksm=ce9b1df2f9ec94e437ee22ca0dc5d050b8a53b3e6df4c4442baf7ae293b54f4afc48414ccb64&scene=21#wechat_redirect)

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/002.png)

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/003.png)

作者：Cage，hanbo

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/004.png)

头部模型的新一代模型的是市场观测、理解 LLM 走向的风向标。即将发布的 OpenAI GPT-Next 和 Anthropic Claude 3.5 Opus 无疑是 AGI 下半场最关键的事件。

本篇研究是拾象团队对 OpenAI 和 Anthropic 在 2024 年至今重要技术动作、产品投入、团队变化的总结和分析，我们希望从这些关键细节来理解头部模型公司的核心主线，更深入地把握 LLM 的进化方向。

**在这个过程中，我们很明显能感受到，虽然 OpenAI 和 Anthropic 的新一代模型都选择了**[**self-play RL 技术路线**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509516&idx=1&sn=40db663d98ed3de0fd4441a5a2da893f&chksm=ce9b1992f9ec908465e80fc42286538f65730ea921018317050e0871adc93dd941599dc4765d&scene=21#wechat_redirect)**，但两家公司其实在 LLM 接下来要怎么进化的问题上出现了分叉：**

• 对于 OpenAI 来说，模型成本下降和多模态能力的提升是最重要的主线，4o-mini 的发布就比最早的 GPT-4 成本下降了 150 倍，并且 OpenAI 也在积极地尝试新的产品方向；

**•**Anthropic 的关注点显然放在了推理能力上，尤其是在代码生成能力上下功夫。在模型产品线上，也能感受到 Anthropic 明确的取舍，多模态不是它们的未来重心，尤其视频生成是一定不会在产品中加入的。

OpenAI 和 Anthropic 之间的差异既和创始人风格、团队技术审美、商业 roadmap 等因素相关，也是 LLM 领域各派声音的集中呈现。本系列会保持半年一次的更新频率，希望为市场理解 LLM 带来方向性启发。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/005.png)

**💡**目录 **💡**

            01 模型更新              

            02 产品进展   

            03 人才更新 

            04 Research 更新

**01.**

**模型更新**

**OpenAI**

**主线 1：成本下降**

LLM 大模型的成本下降趋势是非常明确的，在 GPT-3.5 和 GPT-4 的模型定价上都体现得尤其明显。4o 的模型设计初衷除了大家熟知的多模态之外，就是为了推理成本优化而设计的。在这基础上，甚至 4o-mini 可以再下降 33 倍的成本，这个成本下降幅度是非常惊人的。**我们相信未来随着时间推进和工程 infra 的优化，4o 模型可能还有 10 倍的成本下降空间，很多当前模型能力下的 use case 都能迎来 ROI 打正的时刻。**

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/006.jpg)

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/007.png)

同时值得一提的是，OpenAI 推出了新的 batch API 方案：API 不实时返回结果，而是在未来 24 小时内返回结果，这能使 API 价格打对折。**这适用于对时间不敏感的大批量任务，可以大量节省成本。**这个方法能降成本是因为目前的实时推理中 long context 和短的会放在一个 batch 中处理浪费很多资源，而降低实时性能够将相 context length 放在一起计算来降低成本。

OpenAI 还没有推出 Anthropic 使用的 prompt caching，不确定是否已经用类似方式进行降本了：**Claude 在 long context 下可以通过把部分常用 prompt 存在缓存中来节省 90% 成本，降低 85% latency。这个方法在 RL 技术路线下会非常有用，因为模型 self-play 探索时会有大量重复 context。**

另外 4o 对多语言数据的 tokenizer 效率提升，也能带来更低的成本。多语种在压缩过程中的 token 消耗量都显著降低，例如一句话原本需要 34 个中文 token，现在 24 个就能够实现。

**主线 2：多模态交互能力提升**

模型能力角度上，OpenAI 在今年上半年最大的进展在多模态能力上：

**理解侧**

1）GPT-4o 模型的发布实现了端到端的多模态能力，在语音对话和多模态能力上有明显提升的同时，降低了成本且没有降低推理能力。其语音功能至今仍未大面积推出， advanced mode 还在缓慢 roll out 中。

**speech-to-text:** 显著领先于 Whisper。端到端模型在语音上显示出了一定的 emergent capability，比如何时能打断并介入与用户的对话。等大规模铺开后在语音陪伴等场景的 PMF 可能迎来新一波的机会。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/008.png)

**视觉理解：** 显著高于其他模型，但**没有出现多模态 unify 带来的智能涌现。**视频数据的信噪比太低，在当前架构下和文本数据放在一起，并没有带来显著的多模态智能，这是多模态理解领域上需要解决的问题。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/009.jpg)

**生成侧：**

a. 在 vision 方面发布了 Sora 视频生成模型，**Sora 发布后视频生成领域的 SOTA 暂时收敛到了 DiT 架构。**由于 Sora 目前还在 demo 阶段，我们预期下半年会发布给公众使用。

b. 4o 模型作为一个端到端生成模型，也**在探索用端到端 autoregressive 的方式生成图片。**

**Anthropic**

**主线 1：模型推理能力增强**

2024 年上半年，Anthropic 在 Claude 模型系列上取得了显著进展。3 月 4 日，公司推出了 Claude 3 系列，包括 Opus、Sonnet 和 Haiku 三个版本，每个版本都针对不同的应用场景和需求进行了优化。President Daniela Amodei 在最近的一次公开分享中提到，他们设计时的想法是 ：

• Opus 为复杂推理、研究场景设计。Opus 是第一个超越 GPT-4 的模型，但定价偏高性价比差。

• Sonnet 是为企业常用需求如 RAG 设计的，可能是因此第一个做了 3.5 版本。

• Haiku 是为实时性强的客服等对话场景设计**（由此推测，他们也可能在 voice 领域推出端到端模型）。**

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/010.png)

6 月 21 日 Anthropic 又发布了 Claude 3.5 Sonnet，进一步提升了模型的性能和能力。Anthropic 还预告将在 2024 年晚些时候推出 Claude 3.5 系列，包括 Haiku 和 Opus 版本。**Opus 版本是最值得期待的，看其是否能够大幅超越 GPT-4 的推理水平。**

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/011.png)

在性能方面，Claude 模型取得了很大进步。Claude 3.5 Sonnet 在很多领域的表现**超越了 GPT-4，特别是在研究生级推理和编程能力方面。直到 9 月，其他所有模型的更新都无法在 Coding 和复杂推理能力上超越 Sonnet 3.5。其 coding 能力提升也带来了一系列 AI coding 产品的实现**：Cursor 作为 IDE 的开发体验一下子流畅了很多，甚至 Websim 这样在上半年看起来是 toy project 的产品在现在也有了不错的效果。背后原因都是 Claude Sonnet 3.5 能生成上百行的可靠代码，而之前的 SOTA 模型只能生成 20 行左右。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/012.jpg)

模型的其他维度能力也在各个 use case 得到了全面扩展。Claude 3.5 Sonnet 的推理速度是 Claude 3 Opus 的两倍，可以处理 200K token 的上下文窗口，相当于约 500 页文档的内容。多模态能力也得到显著增强，特别是在视觉理解方面，包括图表解读和从不完美图像中准确转录文本的能力。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/013.png)

**主线 2：模型拟人能力增强**

Anthropic 首次在 Claude 3 系列中引入了"性格训练"（Character Training），这项能力是在 post training 加入的。这项创新旨在赋予模型良好的性格特征，通过生成数据和自我排序来内化这些特征。这不仅提高了模型的吸引力和互动性，用户反馈也表明与模型的对话变得更加有趣。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/014.png)

**训练方式：**首先要求 Claude 生成各种与特定性格特征相关的人类消息——例如，关于价值观的问题或关于 Claude 自身的问题。然后向 Claude 展示这些性格特征，并让它针对每条消息产生符合其性格的不同回应。之后，Claude 会根据每个回应与其性格的契合程度对这些回答进行排序。通过对这些回答的排序训练一个偏好模型，我们可以教导 Claude 内化其性格特征，而无需人类的交互或反馈。

尽管这个训练流程**仅使用 Claude 自身生成的合成数据，**但构建和调整这些特征仍然是一个相对手动的过程，需要人类研究人员密切检查每个特征如何改变模型的行为。

这个方向结合他们的 interpretability 的研究，**可以看到他们在模型的可控性上下了很多功夫。**

**用户评价**

我们也收集了一系列用户对 4o 模型和 Claude 3.5 的用户使用评价：

**GPT-4o 优势：**

• 速度快，响应迅速：在 iOS 应用中使用 GPT-4o 时，几乎感觉不到延迟，能够实现类似实时对话的体验。

• 多模态能力强：GPT-4o 有更完备的语音对话和图片识别能力，且语音识别准确度、对话智能度很高，还有创作图片的能力。

• 在一般对话和简单任务中表现良好。

• ROI 高：用户普遍表示，对于需要频繁使用 AI 但预算有限的情况，GPT-4o 提供了很好的性价比。

**GPT-4o 劣势：**

• 在复杂推理、数学和编程任务中表现不佳 ：例如有用户提到在使用 GPT-4o 编写 C++的类型定义时，4o 不能特别好的理解复杂需求。

• 输出冗长，常忽视简洁指令：即使用户明确要求简短回答，GPT-4o 仍倾向于提供详细解释，有时甚至重写整个段落/代码块而非只给出必要修改。

• 在专业问题下不如早期的 GPT-4 版本：一些用户提到在处理特定领域的专业问题时，GPT-4o 的表现不如早期的 GPT-4 模型，可能和其模型进行量化降成本有关。

**Claude 3.5 Sonnet 优势：**

• 在复杂推理、长文本处理和编程方面表现优异：多位用户提到 Claude 在处理 C#和 C++等编程语言的复杂任务时表现出色，能够准确理解和执行复杂指令。

• 更好地遵循复杂指令：用户发现 Claude 能够准确执行多步骤任务，如在学术研究中按特定格式生成报告并同时进行数据分析。

• 创意写作和人性化交流能力强 用户表示 Claude 能够更好地捕捉和模仿特定的写作风格，产生的内容往往更贴近人类作者的水平。

• 在 C#、C++等特定编程语言中表现出色：一位用户提到，在使用 Claude 重写 C#方法时，生成的代码通常可以直接使用。

**Claude 3.5 Sonnet 劣势：**

• 模型外部能力局限：Claude 无法生成图像，没有实时网络搜索功能，也没有语音交互的能力。

• 某些用户反映最近性能有所下降：有用户提到 Claude 在某些特定领域的回答质量不如以前准确，可能是由于成本优化导致的。

**02.**

**产品进展**

**OpenAI**

**用户数据上涨：多模态带动交互创新，4o 让产品再度扩圈。**

**1）ChatGPT 用量随 4o 的发布大幅增长：**

a. OpenAI 的访问量自 2023 年 5 月达到峰值后，因为暑假开始下降，后续变进入波动，直到今年 5 月 GPT-4o  发布后再次飙升，在 2024 年 6 月的访问量达到 2.9 亿次，比 2024 年 5 月增长了 15.6%，而 2024 年 5 月则比历史最高值增长了 40%（2023 年 5 月），GPT-4o 对用户量的拉动是极为明显的。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/015.png)

b. **去年访问量在夏季下降，今年没有出现这种趋势，**主要得益于 GPT-4o 推出，OpenAI 能够持续保留和吸引新用户。（一定程度上也得益于 GPT-4o 多模态能力使得 ChatGPT 进一步向生活场景拓展，而非仅仅是一个效率工作产品）。但节日趋势在其他产品上还是明显存在的：C.AI 流量上升，Perplexity 流量下降。

c. 截止到今年 6 月的 **Web MAU 约为 2.3 亿，移动端 DAU 约为 320 万。**

**2）****放在搜索引擎语境下，**ChatGPT 的用量持续超越 Bing 和 Perplexity，与 Google 仍有量级上的差距，但开始逐渐蚕食传统搜索引擎的心智。

尽管 Google 整体搜索份额还比较稳定在 91%+，但其桌面端被拿份额的趋势比较明显，美国和全球数据都是这个趋势。ISI 发布了一份报告介绍他们对 1000 多名消费者的调查结果。他们注意到，**从6月到8月，Google 作为首选搜索引擎的份额从80%下降到74%，而ChatGPT的份额从1%增加到8%。**

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/016.png)

• 6 月份 ChatGPT / Perplexity 流量略降，Claude 有个跳涨，和 Sonnet 3.5 模型能力显著提升有关。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/017.png)

**3）对 AI 产品流量和商业模式的思考**

a. 在 AI 时代流量最大的产品不一定产生最大的价值，完成任务的难度更重要。这个观点的前提是广告模式不是 AI 时代最后的 business model。

b. 大模型公司的商业模式不比移动互联网简单，更像传统零售的库存模式：资源都分配给训练用户用不上产品，那就是库存积压；资源给推理太多模型能力跟不上，是库存短缺。

c. 目前看到的大模型公司商业模式，要明显比互联网广告和软件订阅的商业模式差很多。后两者最重要的特征是 ① 提供服务的边际成本几乎是零，或是持续显著下降。② 黏性/用户留存极强。意味着企业只要投入建立平台/软件产品及获客，后续收入的利润率极高，且持续性很强。大模型无论是 API 还是订阅制，定价端很难提价，而随着模型能力增强，用户query/任务会更加复杂，服务用户需求的成本还可能是上升的。

**从生产力助手到 Agent 探索：**

**feature 更新和收购并行**

根据 chatgpt 今年 1 月-7 月的产品升级，可以发现如下几个趋势，他们是明显在从生产力助手往 agent 方向在探索：

• **新的交互模式已经有了雏形，在日常生活中的应用场景大大扩宽：**通过对多模态能力的不断强化，目前能够对图片进行解读、翻译和推荐、实时语音交流、屏幕读取功能。

•**工作效率产品逐渐完善：**针对数据分析需求，ChatGPT 新增了与云存储服务如 Google Drive 和 Microsoft OneDrive 的直接集成，以及实时表格交互和可定制的图表功能。

•**在逐步搭建生态系统，尽可能多的平台整合：**与苹果等大平台的整合，推出桌面版，提升了在不同操作系统和应用中的可用性和用户接触点。

•**memory 功能加入：**目前还只是把文字内容总结成简单的一个标签放进 system prompt。下一步结合 Rockset 的收购可能为外部互联网和每个用户的聊天记录建立 index，做到更强的个性化。

同时也值得分析一下他们是收购三家公司的价值，和他们实现 agent 的愿景高度相关：

**1）Rockset（2024 年 6 月收购）：**

Rockset 是一家专注于实时分析数据库的公司，以其先进的数据索引和查询能力而闻名，成立于 2016 年。OpenAI 收购 Rockset 的战略动机主要是为了增强其检索基础设施。这将使 OpenAI 能够提供更强大和高效的数据处理能力，特别是在**实时搜索和 RAG 上。**此次收购预计将显著提升 OpenAI 在数据 retrieval、分析和检索方面的能力，使其 AI 解决方案更加强大，能更好地响应实时数据需求。这也增强了 OpenAI 在与其他 AI 模型提供商和全栈生成 AI 平台竞争时的技术实力。

此外，**未来的 agent 中最关键的工程设计在于 memory 的设计，**前面这套在 RAG 和 search 的方案也可以用在未来 agent 的记忆机制上。

**2）Multi（原 Remotion，2024 年 6 月收购）：**

Multi 是一家开发实时协作工具的初创公司，允许用户共享屏幕并在编码等任务上协同工作。OpenAI 收购 Multi 的战略目的是利用其技术来增强远程协作能力和 AI 驱动的内容摘要功能。这与 OpenAI 通过 AI 改善团队协作和生产力的更广泛目标相一致。**这次收购的一个重要意义可能是实现未来人与 AI agent 在屏幕前的共同协作。**

**3）Global Illumination（2023 年 8 月收购）：**

Global Illumination 是一家专注于创意工具、基础设施和数字体验的公司，由来自 Instagram、Facebook、YouTube、Google、Pixar 和 Riot Games 的前关键设计师创立。收购 Global Illumination 的目的是增强 OpenAI 的核心产品，包括 ChatGPT。此外我们也猜想，他们之前的产品也可能适合成为 virtual agent 的进行强化学习的交互环境。

**Anthropic**

**交互：Artifact 时软件生成 task engine 的早期形态**

Artifacts 是我们使用 Claude 产品时会出现的动态 workspace，能把我们需要完成的任务转换成代码，并用代码的方式来实现基础的任务。我们可以认为它是 OpenAI Code Interpreter 基础上对 UI/UX 的创新。

Claude 团队给 Artifact 的未来定位是企业团队将能够安全地将他们的知识、文档和正在进行的工作集中在一个 Artifact 这个 workspace 中进行交互，而 Claude 则根据需求作为 copilot 对这个workspace 进行交互。所以可以认为 Artifact 是 Anthropic 团队对下一代 AI-native 协作平台和工作流的想象。

在实际使用场景中，现在还是开发者使用 artifact 制作初步代码比较多：

• 示例一：一行 prompt 制作日历 app，artifact 直接呈现出 code 和 UI，不需要自己动手写基础代码

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/018.png)

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/019.png)

• 示例二：上传一本书后，边读边通过 artifact 总结每一页的内容

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/020.png)

**Agent 探索：**

**还在 tool use 阶段，未来 roadmap 可期**

Tool use 能力的提升标志着 Anthropic 在 agent 技术上比较稳健的一次进步。2024 年 5 月，Anthropic 为 Claude 3 系列模型增加了与外部工具和 API 交互的能力，这一进展大大拓展了模型的实用性。这项功能使得 Claude 能够执行更为复杂和实际的任务，不再局限于纯粹的文本生成。用户只需用自然语言描述他们的需求，Claude 就能智能地选择合适的工具并执行相应的操作。这种自然语言接口大大降低了使用门槛，使得即使非技术背景的用户也能轻松地利用 AI 的强大能力。

Anthropic 展示的 agent 应用场景涵盖了多个领域，充分体现了其技术的广泛适用性和潜力。首先，在数据处理方面，Claude 能够从非结构化文本中提取结构化数据，这对于自动化数据录入和分析具有重要意义。其次，Claude 可以将自然语言请求转换为结构化 API 调用，这大大简化了系统间的交互过程。在信息检索方面，Claude 能够通过搜索数据库或使用 Web API 来回答问题，提供即时且准确的信息。对于日常任务自动化，Claude 可以通过软件 API 执行简单任务，提高工作效率。

其中最特别的一个例子是 **Claude 能够协调多个快速子 agent 来完成细粒度任务，这是复杂任务的分解和并行处理的未来方向。**这种阶梯式的模型分工方法可能涉及多个专门化的 agent 协同工作，每个 agent 负责特定的任务或领域。这种架构不仅能提高整体系统的效率和灵活性，还能更好地处理复杂的多步骤任务。通过让不同的子代理各司其职，系统可以更有效地利用资源，并且能够根据任务的需求动态调整工作流程。

Anthropic 在官网公布了他们的未来方向，其中他们对 agent 的长期规划是宏大而全面的：

**• 知识融合（结合多个领域的交叉知识）**

**• 超越现有训练数据、本科生水平的知识推理**

**• 自主执行端到端科研项目**

**• 提出新假设和设计的能力**

**• 隐性知识（只能通过在实验室中的学徒制获得的那种知识）**

**• 需要做出连续决策才能实现的 long horizon task**

**• 自动化数据分析**

这些能力的实现都会和我们期待的 agent 有着方向上的汇合。仔细看会发现 Anthropic 对 AI 的期待很多都落在软件和科学发现上。

**03.**

**人才更新**

**OpenAI**

OpenAI 依旧保持快速增长状态，已经从纯粹的 AI Lab 演进至更加工程、产品、收入导向的公司。公司目前有 400 名以上的 Researcher，超过 1200 位非研究类员工，包含工程、销售、产品、后台支持等，对比 2023 的 770 人增加近乎一倍。

从招聘侧重点看，近三个月，有 460 人新加入 OpenAI，其中 Member of Technical Staff 依旧占主要，共有 130 人，偏工程类员工占整体 MTS new hire 的 80%。Go-to-market 是招聘数量第二多的团队，新招聘 46 人。产品新招聘 24 人，其中包括新加入的 CPO Kevin Weil。

**离开的关键人才**

• Ilya 于 2024 年 5 月与 SuperAlignment Co-lead Jan Leike 接连离职。Ilya 在离职后创办了 SSI，致力于构建安全超级智能 。而 GPT-4 的核心人物 Jakub 接任了 Chief Scientist 的角色。Ilya 对于 OpenAI 是指明方向的灵魂人物。但也有观点是 Ilya 的远见对于 OpenAI 初期带来很大帮助，但在 OpenAI 已经明确远期方向后，Illya离开的影响并不大。

• 同样为 OpenAI 早期灵魂人物的 Greg 会休假至年底后再回归公司。

• Andrej Karpathy 在加入 OpenAI 一年后于 2024 年 2 月离开 OpenAI，离职后创办 Eureka Labs 的 AI 课程教育公司，自己担任讲师帮助学生更好理解 AI 与 LLM 训练。

• John Schulman 离开 OpenAI 加入 Anthropic。晋升为 alignment lead 前，John 曾是 reinforcement learning team lead，是 RLHF 的开创者，确定了 OpenAI RL 的路线。John 是 OpenAI 创始团队之一，师从 Pieter Abbeel。离开 OpenAI 后，John 加入 Anthropic。

• Jan Leike 跟随 Ilya 一同离职后**加入 Anthropic，**继续负责 Alignment 方向工作。John Schulman 和 Jan Leike 的加入意味着 OpenAI 的研究路线图对于 Anthropic 团队几乎是一张明牌。

• Peter Deng 作为 Product VP 离开 OpenAI，Kevin Weil 作为 OpenAI 新加入的 CPO 继续领导 OpenAI 的产品工作。Kevin 在加入 OpenAI 前为 Meta Diem、Instagram 的 VP of product，在 Instagram 任职期间帮助 Instagram 在与 Snap 竞争阶段获得优势。**从 Peter 的离职也能感受到 OpenAI 对新产品开发落地的激进程度。**

• Aleksander Madry 于一年前从 MIT 教职暂时离开，加入 OpenAI 创办 Preparedness 团队，目标是通过理论研究帮助 OpenAI 提前控制可能发生的重大风险。Aleksander 于 2024 年 7 月离开，接任者为 Joaquin Quiñonero Candela，加入 OpenAI 半年时间，先前在 Meta 带领 Responsible AI 团队近九年。

• Jeffrey Wu 是 GPT- 2 的核心贡献者，参与了 GPT 的可解释性、可拓展监督方向的工作。也作为核心参与了 InstructGPT 这一 RLHF 的重要项目。Jeffrey 于 OpenAI 任职 6 年，于 2024 年 7 月离职，加入 Anthropic。

• Yuri Burda 是 OpenAI reasoning team 的创始成员之一，负责 OpenAI 的数学方向研究，并于早期项目：Dota、Codex 中有核心贡献。离开 OpenAI 后 Yuri 加入 Anthropic。

**值得关注的新团队和岗位**

我们也观察到 OpenAI 出现了一些新的小组：

**1）Solution Architect**

在 Success Team 下新增了 Solutions Architect 团队，隶属于 Success Team 下。目前整体团队大约 20 人，均为一年内加入 OpenAI，对 Enterprise 提供整体部署解决方案。Solutions Architect 团队源于 OpenAI 的策略调整：OpenAI 为了防御 Azure 捆绑销售策略下的折扣定价，承诺可以为大客户根据需求定制软件。

**2）集群硬件**

OpenAI 从 0 到 1 搭建了新的硬件团队。从团队配置看，更像是计划搭建数据中心集群所需要的人才。目前硬件团队还是一个不到 10 人的小团队，由 Richard Ho 带领。Richard 先前于 Google 任职近十年，是 Google TPU 的 Senior Engineer Director。先前有报告提及 OpenAI 至少要等到 2025 年才可以自己开发芯片，并且目前在与博通商讨合作设计的形式，Richard 做为 Google TPU 的负责人，在 OpenAI 的定位会是 lead 起 co-design 任务的角色。

Richard 团队内，Reza Khiabani 先前于 Tesla Dojo、Google TPU 负责数据中心液冷方向工作。Xin Li 先前于 Google 负责数据中心电源工作。

**3）投资了 Opal 团队**

此外，消费硬件层面，OpenAI 于 2024 年 8 月投资了 Opal，有可能在之后一起合作 AI 硬件。Opal 的产品为高清摄像头，并且十分重视设计。

Opal 于 2020 年成立，是一个 15 人的小团队。创始团队为 Uber 背景。CEO Veeraj Chugh 在创办 Opal 前于 Uber 任职 3 年，先后负责 Uber Freight、Uber New Mobility 的产品运营工作。Co-founder Stefan Sohlstrom 是设计背景出身，2014 年作为第 5 号员工加入 Plaid，担任 Plaid 的 Head of Design。2017 年开始于 Uber Freight 从设计职责转换成产品经理，成为 Uber Freight Shipper Platform 的产品 Head。

**4）Model Behavior scientist**

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/021.png)

对于 Model Behavior 研究人员的招募可能揭示 OpenAI 希望增强模型的可控性并且希望能够发展新的交互方式，同时提升模型的创造能力。

**5）mid-training scientist**

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/022.png)

Mid-training 已经被正式定义为一个新的训练阶段。其主要环节可能包括一些比较接近模型基本能力的 alignment，与 human feedback 离得相对远、更靠前。

**Anthropic**

2024 年以来，公司人数从 300 人增加至 500 人左右。2024 起，公司招聘共 180 名新的 Member of Technical Staf，使 Anthropic 整体 Member of Technical 数量达到约 260 人，其中 90 名 Researcher，210 名 Engineer。Anthropic 的第二大招聘重心为产品团队，2024 年前，Anthropic 的产品团队共 10 人，而今年已经是接近 30 名，包含产品经理、Product Partnerships / Marketing 相关员工的团队。

Anthropic 和 OpenAI 相比更看重 Alignment、可解释性、AI 社会影响三个方向研究，也是 Anthropic 官网上 Research 部分的三个主要构成部分。

可解释性团队由 Shan Carter 带领，现已经是 20 余人的团队。Shan 先前于 OpenAI、Google Research 工作，主要负责可解释性方向研究，曾与 Co-founder Chris Olah 于 Google 时参与 Google 重要可解释性研究：*The building blocks of interpretability*。

可解释性团队在 Claude3 发布后发了一篇新论文：*Scaling Monosemanticity:  Extracting Interpretable Features from Claude 3 Sonnet*，突破了模型的透明度并且建立了新解决黑盒问题的机制。

除了前面提到的几位从 OpenAI 离职的几位早期重要 researchers 之外，还有这样几位重要 OpenAI / DeepMind 出身的重要科学家加入：

• Pavel Izmailov 自 2023 年 6 月加入 OpenAI，工作一年后离开加入 Anthropic。于 OpenAI 期间 Pavel 是 superalignment 的成员，加入 Anthropic 也有大概率与 Jan 继续合作 alignment 方向工作。

• Steven Bills 于 2022 年 3 月加入 OpenAI，是 superalignment 团队的成员，参与了 OpenAI 发布 GPT 后的可解释性研究：Language models can explain neurons in language models。

• David Choi：David 于 2017 年至 2023 年 12 月于 Deepmind 担任 Staff Research Engineer。先前是 Deepmind 的 AlphaCode Co-lead，是 Deepmind 在 2022 年时的核心代码生成模型。David 在 agent 方向的研究可以追溯至 2019 年与 xAI 的 Igor 共为一作的 AlphaStar 论文。

• Jascha Sohl-Dickstein：Diffusion model 核心一作，曾是 Google 的首席科学家。于 2024 年 1 月加入 Anthropic，此外，Jascha 曾发布了 Score-based SDE，构建了生成 Diffusion 模型理论的框架。

Anthropic 产品团队最大的更新是新 CPO 的加入。Mike Krieger 原先是 Instagram 的 Co-founder & CTO，经历了在 Instagram 被收购后从只有 6 位全栈工程师成长到包含 300 位工程师的 full function 工程团队的过程。Mike 于 2021 年时与 Instagram CEO Kevin 开始做 AI 新闻推送创业 ARTIFACT，于 2024 年 5 月停止项目，加入 Anthropic。Mike 本身的经历和 Anthropic 经历了只有 80+人的小团队，但创造出了 SOTA 模型，之后迅速扩张的过程非常相符。加入 Anthropic 后 Mike 带领 Claude APP，以及企业服务的产品工程、管理、设计工作。

Anthropic 的产品团队自 2024 年也快速扩张，目前 30 位产品成员大多数来自于 Stripe、Google、AWS 三家诞生了出色的 enterprise 产品的公司。

**Artifacts**

Artifacts 是 Mike 加入 Anthropic 后负责的新产品，外部对 Artifacts 的评价是“又懂模型、又懂产品的人做出的产品”，对比 OpenAI “互联网风格”的产品会更 AI-native。而 Artifacts 的名字和 Logo，都与 Mike 先前创业项目 ARTIFACT 高度相似。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/023.jpg)

Mike 的 Artifact 项目

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/024.jpg)

Artifacts 与 Claude 的 Logo

与 Mike 一同加入的还有先前共创 Artifact 的工程师 Justin Bisignano。Justin 2020 年加入 Instagram 团队任安卓工程师，所写的代码支持了 20 亿用户。2022 年 7 月加入 Artifact 任职至 2024 年 4 月后加入 Anthropic，负责 Claude 的产品工程方向工作。

**04.**

**研究更新**

****OpenAI****

***Prover-Verifier Games improve legibility of language model outputs***

**新的训练方法：**OpenAI 开发了一种称为"Prover-Verifier Games"的新训练方法，旨在平衡模型的性能和可读性。

**解决关键问题：**这种方法解决了之前模型在性能和可读性之间存在的权衡问题。过去，注重可读性可能导致幻觉（hallucination），而过度注重正确性则可能降低可读性。

**训练机制：**

• 使用一个强大的模型（prover）和一个较弱的模型（verifier）。

• verifier 经过训练，预测 prover 生成解决方案的正确性。

• prover 被指示扮演"helpful"或"sneaky"角色，分别生成正确或错误的高分解决方案。

• 通过多轮训练，verifier 不断学习识别错误解决方案，迫使 prover 探索新策略。

**意义：**

• 通过 multi-agent 分工的方式实现，在减少人类直接干预的情况下，实现对超智能 AI 系统的对齐。

***CriticGPT, Finding GPT-4’s mistakes with GPT-4***

• 基于 GPT-4 开发的模型，旨在发现 ChatGPT 代码输出中的错误。

• 实验表明，使用 CriticGPT 辅助的人在代码审查中，60%的情况下表现优于没有辅助的人。

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/025.png)

**研究意义：**

• OpenAI 正在努力将类似 CriticGPT 的模型集成到他们的 RLHF（Reinforcement Learning from Human Feedback）标注流程中。

• 这将为他们的训练人员提供明确的 AI 辅助。

**局限性和未来发展方向：**

• 目前 CriticGPT 主要针对较短的 ChatGPT 答案进行训练。

• 未来需要开发能够帮助训练人员理解长期和复杂任务的方法，以便监督未来的 AI 代理。

• 模型仍存在幻觉问题，有时训练人员会因这些幻觉而做出错误标注。

• 当前研究主要关注可在一处指出的错误，未来需要解决分散在多个部分的错误。

• CriticGPT 的辅助能力有限：对于极其复杂的任务或响应，即使是有模型辅助的专家也可能无法正确评估。

**长期目标：**

• 开发能够处理长文本的能力。

• 最终目标是使用这种技术来监督 AI agent 的训练。

**Anthropic**

***Scaling Monosemanticity, Extracting Interpretable Features from Claude 3 Sonnet***

• 使用机器学习中“dictionary learning”的方式，并借助训练大模型的 scaling law techniques，将这个技术沿用到大模型上，从中 isolate 出大模型激活神经元的 pattern，解读模型激活神经元的方式。文章中提到探索了几种能力：

**◎** 针对不同 entities（景点如 golden gate，抽象概念如程序 bugs，gender bias），神经元被激活，并且是 multilingual 和 multim - modal 的。

 ◎ 可以根据激活神经元方式的不同，计算特征之间的“distance”，做近邻计算。

 ◎ 可以人为改变特征被激活的方式，会直接影响模型生成的答案。也能从中发现一些模型可能被潜在激活的不好的方向，为之后监控这些潜在威胁        提供了工具。

• Anthropic 真正做到了 interpretability 的 scale-up：使用 sparse autoencoder 来做到解读神经网络中的 feature。之前主要使用数学统计模型无法 scale-up，sparse autoencoder 的稀疏性可以很好的捕捉到一些关键点，其他不关键信息在 vector 中都不会激活。

•**对比 OpenAI 的可解释性工作：**

◎ OpenAI 的研究较为浅层，主要捕捉 LLM 的行为模式；Anthropic 的研究更深入，挖掘到了不同单词和实体在神经元激活上的规律。

◎ Anthropic 的研究通过干预可以直接改变模型的输出结果，而 OpenAI 的研究主要停留在观察层面。

**这几篇研究可以看出一些对 RL 方向研究的端倪，也可以发现 Anthropic 团队对可解释性的追求是更强的，很可能他们未来会给予可解释性设计更多的模型可控性feature。我们也期待这些研究能带来下一波 AI-native use case 的解锁。**

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/026.png)

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/027.png)

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/028.png)

排版：Doro

延伸阅读

[![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/029.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509557&idx=1&sn=71125c44b6d3d81ea104a71c4d5ef29b&chksm=ce9b19abf9ec90bd495f1a90abdf37394827c935a61d1495c863e5e2cfe723acf9082da021bb&scene=21#wechat_redirect)

Unstructured.io：让企业非结构化数据 LLM-Ready

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/030.png)

[![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/031.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509516&idx=1&sn=40db663d98ed3de0fd4441a5a2da893f&chksm=ce9b1992f9ec908465e80fc42286538f65730ea921018317050e0871adc93dd941599dc4765d&scene=21#wechat_redirect)

LLM的范式转移：RL带来新的 Scaling Law

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/032.png)

[![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/033.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509467&idx=1&sn=83a96582ed9df341818301100de2a070&chksm=ce9b1a45f9ec9353596b692cdca804d0d44113c90c5f7023824e5ae0f55d259276ca5f93a46f&scene=21#wechat_redirect)

寻找 AI 大周期下的 beta 和 alpha ｜AGIX 投什么

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/034.png)

[![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/035.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509417&idx=1&sn=538e456cba3361ea7321c2b9e1d08a7a&chksm=ce9b1a37f9ec93213b13058778e593f99830a6f6ff762361a80f26c55b392a9d0acbdc510732&scene=21#wechat_redirect)

RL 是 LLM 的新范式

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/036.png)

[![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/037.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509327&idx=1&sn=d704398f92260ee8aca930c92dd8cadb&chksm=ce9b1ad1f9ec93c71ffa31e404877b9873661ddb963736896cca17ebc73c768fde570b668844&scene=21#wechat_redirect)

Twelve Labs: 多模态重塑视频内容检索

![](../images/2024-09-05-llm-jin-hua-fen-cha-kou-duo-mo-tai-cheng-ben-dai-ma-tui-li/038.png)
