---
title: Voice Agent：AI 时代的交互界面，下一代 SaaS 入口
publish_date: '2024-07-26'
publish_timestamp: 1721998658
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/-a2MrHLCG1zXnMr8xbtXJA
msgid: 1000000275
appmsgid: 2247508881
itemidx: 1
digest: Voice is the API to the world, AI will take this to the next level.
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgy9ldRWEc228JnukuCAhmAGDjRtFeItzgtYZMP16hOBnm6icZKCEO46BVkJb4GkRap3Z4wA3fLPRpg/0?wx_fmt=jpeg
image_count: 32
archived_at: '2026-04-20T02:26:27+08:00'
---

[![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/001.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect")

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/002.png)

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/003.jpg)

作者：Cage, haina

编辑：Siqi

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/004.png)

Voice agent 是与人类进行对话沟通的 AI，是下一代人机交互界面。‍‍

和文本相比，声音交互的优势主要体现在：

• 语音交互以其与人类自然沟通方式的高度一致性，提供了一种更为直观和低能耗的交互体验，而打字文本交互的使用门槛更高；

• 语音交互非常适合于简短、即时的信息交流；

• Text copilot 往往需要人机协作，最后一公里由人类完成，voice agent 一旦落地将彻底替代人类，独立完成交流任务。‍

以上差异使 voice agent 能产生不同于其他模态的价值，所以我们选择 voice agent 作为独立市场进行研究。

GPT-4o 是第一个实现端到端 voice-in, voice-out 的大模型，**低延迟、高智能**使下一代交互成为可能。传统语音中 ASR + NLP（即使被替换为 LLM） + TTS 的延迟是用户难以接受的，且很难沿着 scaling law 产生足够智能的对话体验。GPT-4o 的出现让新的交互形态成为可能，带来了更多应用场景的想象。

本篇研究中，我们根据不同场景对于实时性、准确性、创造性的不同要求搭建了分析 voice agent 能力禀赋框架，识别出了值得高度关注的创业及投资机会：**短期内，我们较看好开发者工具和面向垂直领域的 voice agent workflow，长期则更期待消费者端“Killer app”的出现。**

**01.**

**Voice Agent 全景图**

为了快速框定出端到端模型出现后什么领域会有剧烈变化、什么领域不会，我们搭建了以下框架来分析声音领域的不同场景需求。‍

**象限分类标准：**1）纵轴是该场景是否对实时性敏感，上方的需要实时在线的回答，下方的可以离线完成声音制作。2）横轴是区分该场景准确度还是创造力更重要，左侧的要求 voice agent 能精准的解决问题或念出文稿，右侧的需要 voice agent 更有创造力和表现力，能给出随机应变的回答。

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/005.png)

• **第一象限（右上）：**是端到端模型带来最大积极影响的。需要实时回答，但对 AI 交流内容的容错率和自由度比较高，典型的场景有：陪伴、心理疗愈。

• **第二象限（左上）：**同时要求实时回答和高准确度，目前是落地难度最大的场景，需要像真人一样可靠。这需要通过对 latency 和 RAG workflow 的极致优化，常见场景有：call center、销售、客服、教育。

• **第三象限（左下）：**可以离线完成，但要求 voice agent 能按台本发挥，因此是 TTS 技术最好的使用场景。常见场景：有声书、短视频配音、模板化外呼电话。

•**第四象限（右下）：****这是一个想象空间比较大的领域，对创意要求高，但同时可以离线生成。**目前比较常见的用例是：音乐生成、npc 语音生成。

根据以上分析框架，我们认为有以下几个值得高度关注的创业和投资机会。类比开发软件时，前端和后端必然是分离的。声音领域前端的机会在于 TTS，后端的机会在于 enterprise workflow，同时也存在端到端的应用机会：

**1）疗愈/陪伴类 voice agent（第一象限）：**端到端模型解锁下一代交互形态，在教育、陪伴等领域出现 killer app。

**2）Enterprise workflow（第二象限）：**企业使用时最大的痛点在于如何解决 corner case（边缘场景） 的准确性，planning & RAG workflow 在这里就非常重要。同时，加入了 RAG 之后如何优化 latency 提升用户体验也很关键

**3）TTS（第三象限）：**LLM 是大脑，但开发者仍需要 interface 的可控性。11 Labs 这样公司的价值持续存在。

前面我们提到 4o 这样的端到端模型取代的是 ASR + LLM + TTS 的链路，那这几个创业方向在整个工作流中处在什么位置？

我们根据目标客户将其分为开发者（To Developer）,企业用户（ To Enterprise）, 消费级（To Customer） 三个不同类型进行梳理，这三个领域的成熟度和壁垒、价值各不相同。以下为结论，我们会在第二部分进行详细分析说明。‍‍‍‍‍‍‍‍‍‍‍

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/006.png)

**To Developer:**

**•****定义：**指的是面向开发者的 API 或开发平台，包含 tts 那样的单点模型、也包括把各 API 连接起来的平台公司。

**•****价值：**高短期价值，所有需要搭建 voice agent 的团队都需要快速搭建的工具来缩短开发周期；长期价值不明确，业务真正依赖 voice agent 的公司最终一定会选择自建。

**•****壁垒：**中，其中部分公司有一定的技术壁垒，部分公司只是其他技术产品的连接器。可能被e2e大模型颠覆。

**• 重要方向：**TTS，emotion engine，RTC，Full stack platform

**•****值得关注的公司：**

**[11labs：](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504471&idx=1&sn=108970a82e8ffba8b648fe3eea9eb523&chksm=ce9b6dc9f9ece4dfe52bdf89524c3b1adfef27277e996b7d012b0a95247b493a2d48bdef82b6&scene=21#wechat_redirect)**作为海外独角兽持续追踪的公司，我们认为 11 labs 是目前最好的 TTS 公司，它凭借完胜竞品的声音克隆体验和声音质量获得了市场的关注和认可，业务收入增长迅速；

**Hume AI：**唯一相对成熟的 emotion engine，比 4o 更早实现了有高质量语义情感的对话；

**LiveKit：**GPT-4o RTC 方案提供者；

**Bland AI：**Full stack 平台中自有模型方案最成熟的公司；

**Retell AI：**Full stack 平台中用户体验较好的公司。

**To Enterprise：**

**• 定义：**面向企业用户的 voice agent，既包括为销售、医疗等垂直领域设计的 AI phone agent，也包括企业端的无代码平台。两者边界比较模糊。

**• 价值：**长短期价值均一般，能够替代临时工提供的人力服务，其精确性尚未达到标准；长期因为市场比较 fragmented，最多也只能在某一个垂直行业中占据比较大的份额。

**• 壁垒：**中等，壁垒主要来自于 GTM 和业务 SOP 积累，其他主要依赖模型能力提升。

**• 重要方向：**Sales and Customers agent, Training and Recruiting

**• 值得关注的公司：**

**Sierra：**Sequoia、Benchmark 投资, 团队实力强，资源丰富；

**Sema4.ai：**Benchmark 和 Mayfield Fund 领投, 团队实力较强；

**[Kore.ai：](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508115&idx=1&sn=3a897e184295128abbe124f8db6524b4&chksm=ce9b1f0df9ec961b90749b66452bb56cc9ac6fbf328b9149a377698299fa27e985a83e0dfab5&scene=21#wechat_redirect)**虽然是相对传统的 AI 客服公司，但 Kore.ai 的业务综合表现在整个领域中仍相对靠前；

**Cognigy：**创立于 2016 年、位于欧洲，值得关注的是它在过去几年中实现了三位数的增长；

**Hyperbound：**AI 销售角色扮演平台，使用 voice agent 技术模拟真实的买家对话，帮助销售团队提高电话销售技巧。

**To Customer:**

**•** **定义：**面向消费者的语音交互应用，例如 AI 陪伴、疗愈师、语言老师，甚至 AI 交互硬件。

**•** **价值：**短期内较低，目前商业化价值尚不明确，还在探索下一代交互的过程中。但长期价值高，可能出现下一个 AI-native killer app。

**•** **壁垒：**中~高，让用户交流更流畅的产品形态和用户数据是其主要壁垒。如果出现更明确的数据飞轮，将有强规模效应。

**•** **重要方向：**心理疗愈，教育和陪伴。

**•** **值得关注的公司：**

**Sonia：**除了看好 voice agent 在心理疗愈领域的应用外，Sonia 的团队背景也较为亮眼；

**Clare&Me：**看好 voice agent 在心理疗愈领域的应用，欧洲市场广阔。

**02.**

**具体环节分析**

**To Developer:**

**机会来自搭建 voice agent 的核心要素**

AI voice agent 的搭建链路很长，把这些工具组合起来让 voice agent work 并不容易。这个领域创业公司的核心价值就是使开发者更快地开发出一个高质量的 voice agent，而其中最重要的变量是端到端模型。

**1. 端到端多模态模型**

GPT-4o 作为多模态端到端模型有着很惊艳的效果：低延迟、真实情感表达、很强的语义理解能力。未来可以同时用于 entertainment & productivity 场景，作为每个人的朋友和工作助理，想象空间巨大。同时，对 voice agent 的落地还有几个关键问题：

**关键问题1：****voice agent 是否真的能在企业用例上落地？**

端到端模型降低 latency 的同时也降低了可控性，这是企业端落地的重要阻碍：enterprise 使用时需要精确的内容输出，此时就需要 decompose 和 RAG 的加入。这对端到端模型并不友好，因为其延迟优势会被 RAG 弱化，这时可控性、精确度和低延迟成了不可能三角。

在强领域知识的场景，可能需要端到端、易于微调的开源模型（可能是 Llama 3 8b 的语音版），才能让 voice agent 真正落地。这时 Workflow 搭建很重要，用于解决 corner case 的精确性。

**关键问题2：****GPT-4o 以什么形式、什么时间开放 API ？**

对于 to developer 的公司其 API 的开放时间和形式可能是最大的变数。目前端到端 model 推理成本相比传统方法明显更贵，这让 API 甚至今年内可能都不会开放。如果 OpenAI 将语音输入输出的接口也开放了，Full stack 的平台价值会降低，voice agent 的技术栈会变成 LLM (+emotion engine/ TTS) + streaming service。

如果 API 能开放多模态输出的 API，语音+文字双重输出可以解决问题 1 中的 RAG 问题。先输出一部分文字开始对话的前半部分，在说话的过程中完成一次 RAG，这样可以基本避免 latency 问题。

**关键问题3：****端到端模型如何改变 voice agent 工作流？**

GPT-4o 的出现把工作流中的很多步骤给简化了。在端到端模型出现前，要搭建一个好的 voice agent 链条很长：

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/007.png)

• **VAD 识别发言时机：**

voice agent 需要判断何时用户说完了内容、合适插入对话，以确保足够互动自然。这一领域的算法称为 VAD，voice automatic detection，在 LLM 出现前就有相关技术。

从官方 demo 中，我们能感受到 GPT-4o 的涌现能力对之前的技术降维打击，尚不清楚 4o 中这一模块是外置模块（可能是类似 speculative encoding 那样的 oracle model ）还是 LLM 自身的能力。

• **ASR 音频转文字：**

这一领域的技术供给一直比较稳定，但端到端 LLM 会对这一类模型的能力产生降维打击：以更快的实时性做到高质量的语义理解。

**这个领域的**代表公司包括******：**Assembly AI，OpenAI（Whisper 是开源SOTA）

•**LLM 生成回答：**

即使用 LLM 理解用户意图，生成自然的回答文本。这个过程中需要对回答推理步骤进行 planning 拆解问题，再用 RAG 从专有数据库中检索回答中的相关概念。要实现这一点就要求 LLM 要了解对解决问题需要执行的操作，比如下单退货指令，并用 function call 能力分发至对应任务上等。

• **TTS 文本转声音：**

TTS 将文本转换为自然的语音输出。这里可以加入更有感情和表现力的声音，也可以加入固定的音色。

TTS 公司的业务主要替代传统配音市场（有声书、翻译等），离线的个人创作者内容生产。而 voice agent 则对实时性要求非常高，因此当前 TTS 和 voice agent 相关度还比较低。两者对 voice 评估的目标不同，11labs 客户要求的是高质量的声音，而 voice agent 用户要求的是高质量的语义回答和 low latency。需求的不同让 11labs 相对难被冲击到，interface 层不会直接被 LLM 大脑冲击到。

关于 GPT-4o 的影响，使用 4o 不一定必须用其自带的 TTS。TTS 位于大模型内，对开发者不太友好。客户可能需要更多样化的声音模式，如定制化或卡通化风格。未来最值得关注的是 4o API 是否同时支持Voice 和 Text 双头输出。

**代表公司：**11labs，Wellsaid，play.ht

• **让对话更加生动的情感引擎（**Emotion engine）**：**

Voice agent 在客服、陪伴等场景中都非常需要理解人类的情感表达，并尽可能模拟出人类表达时的情感，支持这样能力的技术便被称为 emotion engine。

代表公司 Hume AI 是目前唯一效果不错的 emotion engine。Hume AI 的 API 接口背后是一个“共情大模型”（eLLM）驱动，它能够完成情感理解、共情回应、通过个性化建议和干预帮助用户管理情感。Hume AI 不是端到端模型，可以结合其他 LLM一起使用

但 emotional engine 方向最大的风险在于被涌现能力颠覆。GPT-4o 向我们证明了学习足够多对话数据的端到端多模态模型自己能涌现出对人类情感的模仿能力，Hume 的能力很可能被降维打击。

**代表公司：**Hume AI

• **用RTC 降低 streaming latency：**

这类技术接口的价值是降低 LLM 交互的速度，让其交互对用户更丝滑无感。Voice agent 需要选用合适的 streaming service 来降低 voice agent 对话的延迟，例如 OpenAI 选择 livekit 来降低 latency，Bland 选择 Twillo 来接入各类语音电话。

LLM 需要实时接收用户的音频。由于人和 AI 都无法加速产生内容，为了减少 100-200 毫秒的延迟，RTC是必须的解决方案。对于用户的沟通文本，decoder-only transformer 无法提前读入内容，但 RTC 可以保证其在读入内容和输入内容时的 latency 被降到足够低，且不同人物之间可以有并行处理和加速。

考虑到 RTC 是一个已经发展了十年的技术，其能力已经相对 commoditize了。对于 OpenAI 这样的团队，未来更有可能的是选择招聘团队自建更完备的系统。这类玩家更可能的客户是受到 OpenAI 名声影响到的 voice agent applications。

**代表公司：**LiveKit

**总的来说，在整个 vocie agent 的 workflow 中，每一个模块，都出现了一些重要公司：**

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/008.png)

Source: a16z

**2. Full stack 平台**

除了围绕 voice agent 的技术链条提供服务外，还有一类公司是将以上各个环节打通的 Full stack 平台。值得一提的是，这是在 GPT-4o 前就出现的产品形态，帮开发者快速把 ASR + LLM + TTS 的链路打通。可以细分为以下两类，核心区别在于**是否自己训练模型：**

**•****End2end infra：**自己训练模型，端到端完成所有任务的公司，从转录、推理、文本到语音，到构建决策图和可配置的函数调用和 API 请求。

**这个板块的代表公司 Bland AI** 是一家专注于托管客户微调模型栈并提供低延迟通话解决方案的公司，为开发者和企业定制化语音代理以适应特定用例。其核心产品是一个多功能的 AI Phone API，能够自动化和管理各类电话呼叫，包括出站和入站呼叫、对话能力、合规工具、可扩展性以及与现有系统的无缝集成。Bland AI致力于构建 AI 呼叫中心，通过将语音转换为文本并快速生成回应，同时在 LLM 中构建防护措施以降低风险。该公司采用订阅模式，提供从每分钟 0.07 美元起的定价，已获得Acacia Venture Capital Partners、Team Ignite Ventures和Y Combinator的投资。

• **Middleware router：**中间件层，不自己训练模型而是将不同组件串联起来。帮助企业提高了灵活性，能以最快的方式选择自己合适的模型并将其开发为 voice agent。

在11labs 客服访谈中，我们看到有不少客户选用 11labs 作为tts，和其他 API 一起使用，往往就采用了中间件或自建基站，而不是上文的 Full stack 平台一体化基建。

例如， Verizon Communications 利用 11labs 为在野外工作的工程师建立 AI agent，使得工程师可以通过手机应用程序与聊天机器人交流，通过语音来接收信息。

**作为中间件的代表公司，Retell AI** 提供用于构建对话式语音 AI 代理的中间件解决方案。API 主要功能包括语音稳定性控制、实时自动语音识别（ASR）转录、自定义语音以及即将推出的情感分析和环境噪声添加等，团队由前字节跳动/TikTok 产品经理，Google 软件工程师，Meta 项目经理和技术主管组成。包括 Y Combinator 在内的投资者已经为 Retell 投资了总计453 万美元的资金。

**To B: 新一代 Saas 入口**

**语音是进入核心客户行为（如预订、续约、报价等）的自然入口。**如果下一代SaaS解决方案能够充分利用voice agent技术，那么在2B领域，它们将拥有较大的增长潜力和市场优势。

大部分语音对话不需要很高的智能程度，相反，它们更依赖于对上下文的理解、随时 on call 以及对客户需求的快速响应。有了可靠的 voice agent，企业就不再需要人工接线员来工具式地打电话，可以节省大量时间和成本。由于 To B voice agent 就是与客户沟通的电子员工，需要了解很多相关领域的背景知识，因此这一个领域是垂直公司的机会。

**以下是一些关键因素，解释了为什么垂直领域存在市场机会：**

• **呼叫类型、语气和内容结构：**不同行业的客户互动具有特定的模式和风格。语音代理需要根据行业特点调整其沟通方式。比如语调、内容结构；‍

•**数据集成和工作流：**每个垂直领域都有其独特的数据管理和工作流程；‍

•**GTM 策略（GTM）和 killer feature：**需要具备能够解决特定行业痛点的能力。

• **边缘场景难度：**将电话交给AI的质量标准非常高。这些公司最关键的任务就是去解决垂直领域里的边缘场景，例如通用模型可能会误解的独特词汇。

• **法规和许可：**一些语音代理公司面临特殊的限制和认证需求。例如，医疗保健领域需要遵守 HIPAA 合规性，销售领域也出现了针对 AI 冷呼叫的国家级别的法规。

**为什么 To B 场景下的垂直解决方案相对难被端到端模型颠覆？**

在垂直场景中真正解决问题，需要做严谨的 RAG 和任务规划，因此并不适合端到端模型一次生成。通常的过程是先通过文本内容 retrieve 相关信息，再次生成文字和进行 TTS。这时端到端模型的 latency 优势就不再了，关键难点在于领域数据和 workflow 的推理。

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/009.png)

**1. 企业工作流**

企业工作流领域的公司不局限于特定行业、特定场景，而是跨行业提供服务，但目前主要应用场景仍为 sales/support。他们以 low code 平台或 SaaS 的形式提供服务。

我们根据销售工作流，可以将 AI 客服分为几类:

1）**营销类外呼：**售前场景因为对于模型的理解和智能能力要求较低，是目前比较好的落地场景。Voice agent可以带来更自然的对话体验，同时能够结合分析历史通话数据，实现营销转化的提高。如果遇到太难的问题，LLM 也可以检测后发给普通的客服。

2）**销售中：**目前LLM还比较少的被应用到直面leads，因为受能力限制，失败了损失过大。但被充分应用于客服培训中，一方面节省了因为电销频繁离职导致的过多培训时间成本；另一方面可以做到知识库实时对齐，成为电销的语音 copilot。

3）**投诉/售后服务、客户回访：**AI 可以帮助客服收集客户投诉，解决简单的售后服务问题。同时可以进行大规模的客户回访，也开始被企业广泛的采用。

**代表公司：**传统公司以 Parloa、Kore AI 为代表；新兴公司则包括 Sierra，Sema4.ai

Sierra 专注于为企业打造 AI Phone Agent，提供基于 autonomous agents 理念的软件，结合多个模型生成响应。由 Salesforce 前高管 Bret Taylor 和 Google 前VR负责人Clay Bavor创立，已获得Sequoia和Benchmark 等投资方 1.1 亿美元融资。公司采用基于结果的定价策略，客户仅在问题解决时付费。WeightWatchers 利用 Sierra AI 提高了客户服务效率和质量，实现了高客户满意度和问题解决率。

**2. Training and Recruiting**

Training and Recruiting 是值得关注的另一大模块。

GPT-4o 可能预示着新一代解决方案的到来。引入 voice agent 技术有助于企业降低成本并提高效率。值得注意的是，该领域的专业性非常强，因为不同行业的培训内容和面试测试有不同的需求。企业培训市场覆盖了技术培训、软技能开发、质量培训、合规培训等多个细分领域，服务于零售、医疗保健、金融服务、IT 等多个垂直行业。

根据 Global Industry Research 研究，Corporate Training Market 市场规模在2024年估计为 1331 亿美元，并预计在预测期内以 9.47% 的复合年增长率增长。而 Polaris 调研 Recruitment Process Outsourcing (RPO) 市场在2023年的市场规模为 87.5 亿美元，预计到 2032 年将达到 333.4 亿美元。在这一市场中，头部培训公司包括 Skillsoft、LinkedIn Learning（微软）、Pluralsight、Cornerstone OnDemand、Udemy for Business等。同时，头部RPO公司有Cielo、Randstad Sourceright、Korn Ferry、Alexander Mann Solutions (AMS)。尽管市场存在一些头部企业，但并没有形成垄断，为创新公司提供了机会。招聘方向的创业公司如 HeyMilo、Interviewer.AI；在培训方向的Hyperbound和moctalk 等公司值得关注。

**如 Hyperbound** 是一个利用 AI 和 voice agent 的 AI 销售角色扮演平台，通过模拟真实买家对话来提升销售团队的电话销售技巧。该平台通过 AI 买家模拟、角色扮演练习，快速提升销售代表的熟练程度，加速新员工入职，提高转化率，并减少练习过程中对潜在客户的负面影响。Hyperbound 还提供分析和反馈工具，帮助管理者评估和提升销售团队表现。团队由销售教练、AI 工程师以及前 Salesforce Einstein 工程师组成。

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/010.png)

**To C: AI 时代的交互界面**

To C 产品的主要逻辑是，将昂贵或难以获得的人类服务，且是基于对话且可以在线完成的，替换为 AI，主要场景包括心理疗愈、辅导、陪伴等。

早期的 AI 陪伴等应用主要基于文字，如 [character.ai](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505125&idx=1&sn=706c0b4f57dbbfe90fdd7309a42942dd&chksm=ce9b6b7bf9ece26d4a36dc4b65d772f5c8b46007a462d27b504b3ad818b5653d7ec7ad466e53&scene=21#wechat_redirect)，但文字形态的用户门槛高一直限制着用户规模。声音比文字增加的维度：音色、情绪，让用户与 chatbot 交互的使用成本大幅降低。

**1. Consumer Apps**

对于 comsumer apps，未来可预见的确定性变化，**其一是成本会大幅度降低，甚至降低 99%，从而带来用户规模的扩大。**对于现阶段的 AI 教育、陪伴、心理疗愈这些产品，如 Duolingo Max、[Speak](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505802&idx=1&sn=6e2942bb9c845f85be8109bbb0719c1d&chksm=ce9b6814f9ece1028aeb4698c238edb6a1057784d87c4d1d38994167de9b883be99d74474046&scene=21#wechat_redirect)、praktika 等普遍由于 LLM 及 TTS 调用成本过高，限制了大规模的采用。如果调用成本大幅度降低，将使得企业能够以更低的价格提供服务。

其二是由于 GPT-4o 新架构的采用、webrtc 优化， latency 将继续降低，带来更自然的交互，那么对于 c 端实时、拟人程度要求高的场景，也有较大的效果提升。

**具体有 4 个应用场景：**

**面向成人的教育应用：**成人教育目前主要以语言学习应用为主，而语言学习也正是目前最适合通过语音交互进行的领域，因此我们认为 vocie agent 的发展可以让这个领域直接受益。

****面向儿童的教育应用：****除了语言学习外，在更高质量的声音辅助下，儿童学习伴侣的具象化和游戏化是创新的方向。

**陪伴：**Character.ai 和 ChatGPT Dan 的爆火已经佐证了陪伴市场的潜力，但目前大多数应用仍停留在简单的 AI 朋友或虚拟伴侣阶段，未来的创新可能包括具象化、游戏化，以及将AI伴侣集成到硬件中，实现随时随地的陪伴。

**心理疗愈：**心理疗愈是陪伴场景的升级，其核心在于情绪疏导和心理健康支持，但因为是医疗场景，所以关键挑战在于合规性和避免幻觉问题。

**与 Gen-AI 结合的具体案例：**

**1）Praktika.AI**

**• 产品：**Praktika 使用 GPT-4+Unity Avatars+11labs，创建 voice agent 形式的 AI tutor，提供不同地域口音的 Avatar，模拟真实对话，帮助用户克服语言障碍，提升沟通技巧；

**•****差异：**针对有实际英语沟通需求的用户，如职业需求、出国留学等。与竞争对手相比，Praktika 更注重真实对话的模仿，Avatar 是其特点。

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/011.png)

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/012.png)

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/013.png)

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/014.png)

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/015.png)

**2）Ello：**

面向儿童的阅读伴侣应用程序，为幼儿园到三年级的孩子设计，提供与孩子阅读水平和兴趣相匹配的电子书籍和纸质书籍，帮助孩子培养阅读习惯。Adaptive Learn™ 是 Ello 的 AI 引擎，能够像一对一的教师一样理解、适应并响应每个孩子的需求。

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/016.png)

**3）Sonia：**

开发了 AI 驱动的认知行为治疗师（CBT），提供语音和文本会话的心理健康治疗服务。为用户提供了成本效益高、可访问性强、随时可用的心理健康治疗解决方案，改善心理健康服务的可及性。

Sonia 通过手机应用来提供完整的会话治疗服务，用户可以选择语音或文本与 AI 治疗师进行交流，这一服务收费为200 美元/年，和传统的每次 200 美元的治疗费用，成本极低。

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/017.png)

**2. Hardware**

To C 的另一个机会是基于 voice agent 的消费级硬件，实时收集记录用户信息，实时交互反馈，成为更为具象的 personal assistant。但目前出现的出现的 humane、rabbit 的可用性、使用价值仍较差。

尽管尚未出现被广泛认可的“下一代硬件”，但该领域正积极尝试开发新产品。主要有两种尝试方向：首先是创造全新的、以语音交互为核心的硬件设备，如 Humane 和 rabbit ，这些产品旨在提供更加自然和直观的用户体验，但目前可用性、使用价值仍较差。市场上也出现了小型陪伴玩具，它们通过搭载 voice 交互能力，提供互动性和娱乐性，例如 curio和 moxie 这样的产品，不仅能够吸引儿童的注意力，还能在一定程度上辅助教育和情感陪伴。

**与 Gen-AI结合的具体案例：**

因为大家对 Humane 和 rabbit 已经比较熟悉了，下面主要介绍两款以 voice 为核心的游戏和陪伴类机器人：

**1）Curio：**

Curio Interactive Inc. 推出了 Grok、Grem和Gabbo 等 AI 玩具系列，这些玩具配备 WiFi、蓝牙、扬声器和麦克风，支持与儿童进行语音或文本互动，通过游戏和对话提升孩子的听力和交流技能，同时减少他们对屏幕的依赖。

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/018.png)

**2）Moxie**

Moxie 是由 Embodied 公司开发的一款具有情感智能的 AI 机器人，专为 5 至 10 岁儿童设计，帮助他们克服社交焦虑和孤独感。它能够理解语音和面部表情，维持眼神接触，并以肢体动作响应互动。Moxie 还能记住过去的对话，运用特定疗法如认知行为疗法，并适应不同学习阶段。

此外，Moxie 集成了先进的对话 AI 技术，能够为多达四名儿童提供个性化互动，且在不使用客户数据的前提下，根据用户反馈持续更新，从而提升智能和同情心。

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/019.png)

请点击文章末尾处阅读原文查看参考文献。

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/020.png)

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/021.png)

排版：Doro

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/022.jpg)

延伸阅读

[![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/023.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508795&idx=1&sn=3f4ace2030df25ec6e7e8ff4b4765245&chksm=ce9b1ca5f9ec95b355b76e5ddfca3be6712c28442b289c00810490e82dab5f851f623593ec80&scene=21#wechat_redirect)

为什么英伟达能达到 5万亿 ｜ AGIX 投什么

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/024.png)

[![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/025.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508733&idx=1&sn=ac86eb2fa3a8eef7c3d7e704bdf507a8&chksm=ce9b1d63f9ec9475d597e848f6dacef13174b87c31f1e23b785fad0d68fd04ee8ff677d8d74b&scene=21#wechat_redirect)

专访 Luma AI 首席科学家：我们更相信多模态的Scaling Law

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/026.png)

[![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/027.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508588&idx=1&sn=6f48ab2576f486b9365d9435c4d8c2e6&chksm=ce9b1df2f9ec94e437ee22ca0dc5d050b8a53b3e6df4c4442baf7ae293b54f4afc48414ccb64&scene=21#wechat_redirect)

AGIX ETF 上线：构建 AI-native 的投资工具

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/028.png)

[![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/029.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508533&idx=1&sn=97b7b0e0440164f45bda9a03d17ae806&chksm=ce9b1dabf9ec94bd32ba6ed939dca5b18c2c49632c6344ec6b117c54e743674e07b91a26bef8&scene=21#wechat_redirect)

10 万卡集群：通往 AGI 的新门票

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/030.png)

[![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/031.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247508357&idx=1&sn=e00726dddc2ea74111fecb8faee23c86&chksm=ce9b1e1bf9ec970d937685132547a0f18157ae704ff581e97c05bf36136602f37ff44d84fb87&scene=21#wechat_redirect)

通用机器人是 AI 时代的新 "iPhone" 吗？

![](../images/2024-07-26-voice-agent-ai-shi-dai-de-jiao-hu-jie-mian-xia-yi-dai-saas/032.png)
