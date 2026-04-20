---
title: Decagon：用 AI Agent 解放客服团队，能否成为下一个独角兽？
publish_date: '2025-01-23'
publish_timestamp: 1737633977
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/iMPbIFWow_hBzWKCR_aFYg
msgid: 1000000319
appmsgid: 2247511140
itemidx: 1
digest: Decagon 让 AI Agent 从 “黑盒” 变 “白盒”
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzAscUjA6f8qxkv6MMzcHwErI0OAYXrL1dNceehlFqoGqAsJia4jz99kZtJFRykHmDxsnFhYH7icVkg/0?wx_fmt=jpeg
image_count: 21
archived_at: '2026-04-20T03:04:46+08:00'
---

[![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/001.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect)

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/002.png)

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/003.jpg)

编译：yaxin，haina

海外独角兽原创编译 转载请注明

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/004.png)

我们对 Decagon 这家公司保持了持续关注。Decagon 专注于 AI for Customer Support 领域，致力于用 AI Agent 彻底改变客户服务体验。他们打造的不是简单的聊天机器人，而是能不断进化的 AI Agent 引擎，能够真正理解客户的需求并高效地解决问题。

Decagon 由 Jesse Zhang 和 Ashwin Sreenivas 创立于 2023 年，致力于为企业解决复杂的客户支持问题。他们发现，传统的客服自动化工具往往只能处理简单问题，无法真正赢得客户的信任。因此，Decagon 希望打造一款能够与企业现有客户支持工作流深度集成的 AI Agent，并提供易于管理和配置这些 Agent 的工具，打破 AI 技术的“黑箱”。他们的客户包括 Motion、Vanta、Bilt、Webflow、Substack 和 Rippling 等中小型科技公司。公司在 2024 年 10 月完成了由 Bain Capital Ventures 领投的 B 轮融资，融资金额达到 6500 万美元。

本次编译整理了 No Priors 对 Decagon 创始人兼 CEO Jesse Zhang 的访谈。Jesse 在访谈中与主持人 Elad 深入探讨了 AI 如何重塑客户服务：AI Agent 如何帮助企业提升效率、降低成本，到语音交互面临的技术挑战（如延迟问题），再到多模态 AI 和更自然交互方式的未来趋势，以及数学竞赛背景对 AI 创业的影响。通过这次访谈，我们可以更立体的理解 AI 客服的现状和挑战，以及是 Decagon 如何利用 AI Agent 引擎，为 Rippling、Notion、Duolingo 等企业提供更智能的客户支持解决方案的。

**01.**

**Decagon：****用 AI Agent 重塑客户服务**

**Dec****agon 的创立：**

**不能过度思考，而应****该迅速行动**

Jesse Zhang 从小就展现出对数学的浓厚兴趣，他在 Boulder 长大，从小参加数学竞赛，后来在哈佛大学学习计算机科学。毕业后，他创立了第一家公司 Lowkey ，该公司最终被 Niantic 收购。**从这次经历中，Jesse 认识到不能过度思考，而应该迅速行动。**他与 Ashwin 共同创立了 Decagon，专注于 AI Agent 领域，并迅速开始了商业探索。

Decagon 的对于创业方向的选择并非一蹴而就。起初，创始团队也在思考 AI Agent 的最佳应用场景。他们意识到，并非所有领域都适合快速部署 AI Agent。通过市场调研和客户访谈，Decagon 发现了目前 AI Agent 的能力并不适配两个场景：

**1） 需要高初始精度的场景：**在某些领域，比如安全，容错空间几乎不存在。这些场景需要 Agent 从一开始就表现出极高的准确性。以安全信息管理系统（SIMs）为例，虽然有大量日志数据，非常适合 AI 模型处理，但其工作目标是捕捉每一个小的异常事件。可是，现在的AI模型有时候会出错，因此客户很难完全信任 AI Agent。在这些场景，AI Agent用得很慢。

**2）难以量化 ROI 的场景：**有一些领域，表面上看似非常适合 AI Agent，但难以明确量化 ROI。比如，很多“文本转 SQL ”的公司做的演示看起来不错，但仍需要人工监督和调整。AI Agent 更像是一个 co-pilot，而非独立的解决方案。对于大多数企业来说，需要人工干预的 AI Agent 难以证明其 ROI，公司很难为这样的 AI Agent 签订大额合同。

通过不断探索，Decagon 团队逐渐明确了成功的 AI Agent 用例需要具备两个关键特质：

**1）可逐步推广性：****成功的 AI Agent 应用不应追求一步到位，而应支持逐步推广和迭代优化。即使 AI Agent 在初期只能完成部分任务，也应该能够立即为客户创造实际价值。**例如，Coding Agent 可以先承担部分编码任务，显著减轻人类开发者的负担。

**2）有明确的 ROI：****能够清晰量化 ROI 是关键。**在客户服务领域，存在着大量可跟踪的明确指标，例如对话解决率、客户满意度等。这些指标使得 AI Agent 的价值能够得到有效的衡量和证明。

在此过程中，Decagon与Rippling、Notion、Eventbrite、Vanta和Substack等多家潜在客户进行了深入交流，逐渐确定了主要用例——**客服领域。**在初期，Decagon并没有刻意强调宏大的愿景，而是专注于如何打造让客户真正喜爱和满意的产品。

**Decagon 的差异化优势：**

**透明与可观测**

Decagon 的核心优势在于其 **AI Agent 的高透明度和应用效果的可观测性。**

对于大型企业来说，确保 AI Agent 不是一个“黑箱”至关重要。Decagon 的平台能够清晰地展示 AI Agent 的每一个决策过程，包括使用了哪些数据、如何生成答案等。这种高度的透明性显著提升了客户的信任度。

此外，在客服领域，自动化软件的效果通常是可量化的，客户会用一些明确的指标来评估 Agent 的表现，比如 **AI Agent 与人工相比的效果、节省的成本，以及客户体验的质量提升**等等。这种可量化的特性使得客户可以先在小范围内试用 Decagon 的 AI Agent ，然后再逐步扩大应用规模。

尽管客户服务领域的竞争异常激烈，客户通常会同时试用多家不同的 AI Agent 产品进行比较，并基于具体的数据（例如指标的优劣、代理的效果等）进行最终评估。**目前，Decagon 凭借其高透明度和效果的可观测性，在客户的评估中表现出色。**例如，多邻国在 2024 年 8 月对 Decagon 进行了一个月的测试后就决定正式采用其 AI Agent，并迅速实现了 80% 的对话解决率。

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/005.png)

Decagon 与 Built Rewards 进行了一项大型案例研究。Built Rewards 拥有庞大的用户群体，用户可以通过其平台赚取积分或进行支付。由于用户基数增长迅速，客服需求呈指数级增长。在使用 Decagon 之前，Built Rewards 的客服团队面临巨大的工作量。**采用 Decagon 后的一个月内，AI Agent 接管了大部分自动化工作。不到一年时间，Built Rewards 节省了约 65 个人工客服的成本。**

**Decagon的技术架构：**

**协调层与定制化模型**

Decagon 将自己定位为一家软件公司，尽管频繁调用 GPT-4、Claude 等 AI 基础模型，但这些模型只是工具。**Decagon 的独特价值在于基础模型之上的内容，包括协调层（orchestration layer）和围绕核心 AI Agent 开发的其他功能。**协调层决定了 AI Agent 如何混合使用不同的 AI 模型，并围绕客户的业务逻辑进行工作。此外，Decagon 还开发了透明度工具和分析功能，帮助客户了解 Agent 使用的数据和执行的步骤，并自动分析海量客服对话。

对于不同的 AI Agent，协调层可能差别很大，客服 Agent 与 Coding Agent 的协调逻辑就非常不同。但归根结底，各种协调层都是在 LLM 之上构建的一种结构化系统。**Decagon 非常注重协调层，因为它决定了 AI Agent 将如何混合使用不同的 AI 模型。**Decagon 设置了评价机制来衡量每个模型在特定客服任务中的表现，以此决定如何将这些模型整合起来，使其能够围绕客户的业务逻辑进行工作。

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/006.png)

Modern AI Stack

**除了协调层，Decagon 还围绕 AI Agent 构建了一些其他的客服软件功能。**例如，Decagon 开发了一个透明度工具，能让客户了解 Agent 所使用的数据和执行的步骤，这也保证了 AI Agent 不再只是一个只会回答问题的“黑箱”。此外，当面对海量的客服对话时，手动查看所有内容是难以实现的。因此，Decagon 还设计了一个分析功能，可以让 AI Agent 能够自动分析对话，并生成需要关注的客服问题类别和趋势报告。

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/007.png)

Decagon AI Agent Engine

**创始人 Jesse 的"数学基因"与社区文化**

**如今，AI 领域有许多公司是由具有数学竞赛背景的人创立的，比如 Braintrust、Pika AI 和 Cognition 的创始团队。**主要原因有二：首先，过去几年内，大量聪明且才华横溢的人涌入创业市场，**创业对他们来说比传统学术或量化交易更具吸引力；**其次，**数学竞赛历史悠久，形成了一个能让聪明孩子相互认识并建立联系的社区文化。**Jesse 在高中时期就参加过多项数学竞赛和学术项目，包括美国数学奥林匹克项目（MOP）、Intel STS 决赛 SPARC 以及美国计算机奥林匹克竞赛（USACO）。

**在创业过程中，这些背景相似的人们会彼此支持。Jesse 个人也投资了许多 AI 初创公司的创始人，而他们中的许多人也是 Decagon 的天使投资人。**这种支持大多是非正式的，更像是朋友间的互相帮助。此外，创建企业需要考虑招聘、销售、产品构建和薪酬结构等诸多问题，因此他人经验作为参考非常有帮助。

**这种数学竞赛背景也影响了 Decagon 的人才画像。**Decagon 的团队中也有许多人有数学竞赛或编程竞赛的背景。Decagon 会不定期举办数学竞赛或类似活动，并将这些活动当作吸引人才的重要途径。

**02.**

**AI Agent 怎么走向真正的智能化？**

Klarna（一家瑞典先付后买公司）的 CEO Sebastian Siemiatkowski 在 X 平台上分享了他们使用AI Agent的显著成效：短短四周内，AI Agent 处理了 230 万次客户对话，客户满意度与人工客服不相上下。更重要的是，AI Agent将重复性问题减少了 25%，平均问题解决时间从 11 分钟大幅缩短至 2 分钟。此外，AI Agent 还能提供 24/7 全天候服务，覆盖 23 个市场和 35 种语言，极大地提升了运营效率。通过部署 AI Agent，Clara 得以将 700 名全职客服人员重新分配到其他更具价值的工作岗位。

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/008.png)

Clara 的出色案例为整个客服行业使用 AI Agent 带来了很大的推动力。对于 Decagon 的客户来说，他们通常最关注以下两点：

**1）工作量的减少：**AI Agent 能够完成多少对话和任务，从而为客户节省了多少时间和资源。

**2）客户满意度的提升：**主要通过客户满意度得分（CSAT）和净推荐值（NPS）来衡量。当然，也会有一些客户非常重视 AI Agent 回答的准确性，尤其是受监管行业内的客户。

**Voice Agent 的延迟问题**

语音支持是客户服务中至关重要的一环。人们对 AI 模型的主流讨论依旧围绕 text，text-to-speech、理解语音和通过音频进行响应的能力似乎被低估了。像 11 Labs、OpenAI、Google 等公司开始提供这类服务和 API。Decagon 同样推出了语音支持功能，现有客户也在试用他们的 Voice Agent。**Jesse 认为，对客户而言，沟通渠道的选择因人而异：有些人喜欢语音通话，有些人则更喜欢聊天、邮件或短信。因此，覆盖所有渠道至关重要。**

Decagon 最初选择从文本 Agent 入手，因为文本渠道相对简单，也更容易进行效果评估。**然而，现在行业正进入一个新的阶段，有一些大公司对 Voice Agent 非常感兴趣，他们认为“既然 Text Agent 效果很好，那么生成语音并用于电话支持应该也能达到同样的效果”。**今年许多模型公司在语音技术方面取得了巨大进展，尤其是语音的真实感上。Decagon 正与 11 Labs、OpenAI 和Google 等公司紧密合作，探索如何大规模构建这些语音系统。

**延迟也是非常关键的一个指标，**特别是在电话交谈时，用户会期待非常流畅的对话体验，不能有明显的延迟。目前，语音模型在处理流程中——从捕获用户语音、将其转换为文本、输入语言模型处理，再到生成语音输出——不可避免地会产生一定的延迟，导致用户感到停顿或等待。许多公司正在努力解决这个问题，例如通过流式处理（streaming）技术来缩短延迟。

**Decagon 正在尝试使用 voice-to-voice 模型。**OpenAI在这方面进行了大量研究。这类模型的延迟表现通常较好，但在某些情况下，例如需要获取外部数据或进行多次模型调用时，模型“思考”的时间会更长。此外，voice-to-voice模型可能并不适用于所有场景。

**除了 voice-to-voice 模型外，也可以先将语音转录为文本（speech-to-text），在文本层面完成所有计算后，再生成语音（text-to-speech），**但这种方法通常会引入额外的延迟。许多公司已经找到了一些方法来缓解延迟问题，例如在后台提前生成部分内容。在 Decagon 的应用中，客户可以通过添加语音提示（例如“请稍等，正在查询您的数据”）来减少延迟对用户体验的负面影响。

**AI Agent 的发展预测**

Jesse 认为未来**人类与 AI Agent 的协作模式将发生巨大变化。**可能会有更多人从事**监督和编辑 AI Agent** 的工作。与人工客服相比，AI Agent 的特性完全不同。例如，AI Agent 可以无限扩展，可以通过 hard coding 来实现特定任务。因此，如何有效地管理 AI Agent 将是一个重要的研究方向。Decagon 也一直非常关注如何让客户的人工客服团队更好地监控和调整 AI Agent，希望为他们提供更多的可见性和控制权。

**Jesse 认为，目前 AI 行业仍旧处于真正“Agent 化”发展的早期阶段，包括将复杂任务按序列化（sequence）并结合某些形式的 reasoning 能力。**虽然已经有一些先进模型（例如“o1”或 Sonnet）在尝试解决这一问题，但主要集中在**量化推理智能，**如在 coding 和 math 领域表现更好，而**客服领域最看重的是 Agent 的指令遵循能力（instruction following）。客服工作中有很多明确的操作指令（例如 SOP 或工作流），AI Agent 需要做到严格且准确地执行这些指令。**

**值得期待的 AI 技术**

未来 1-2 年，Jesse 非常期待的 AI 技术主要有**多模态、用户 Context Window 以及未来 Computer Use。**模型的多模态能力（尤其是语音）发展可以进一步完善 Decagon 的产品 Roadmap，而 AI Agent 的 context window 的进一步扩展和更自然的交互方式则可以优化用户的使用体验，甚至更进一步，AI Agent 可以帮助客户直接完成任务。此外，基础模型能力的改进同样值得关注，比如 Anthropic 的 Computer Use，虽然目前还没准备好进入生产环境，但随着技术的提升，将带来许多令人期待的应用可能性。

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/009.png)

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/010.png)

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/011.png)

排版：Doro

延伸阅读

[![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/012.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247511096&idx=1&sn=dee1163cad5af574582fa538532a9a0a&scene=21#wechat_redirect)

拾象 2025 AI Best Ideas：20大关键预测

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/013.png)

[![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/014.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247511038&idx=1&sn=68b0d25b603317d23ed18b07e887338a&scene=21#wechat_redirect)

Agent 最全 Playbook：场景、记忆和交互创新

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/015.png)

[![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510990&idx=1&sn=2e5ad4a0b80c9900095929eff692cdaf&scene=21#wechat_redirect)

LLM 竞赛 2025: 超越 Google 之路

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/017.png)

[![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/018.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510949&idx=1&sn=015de5d623ae801d0f25a8e992bdd92f&scene=21#wechat_redirect)

Metronome：OpenAI、Anthropic背后的计费平台，会是AI时代的Stripe吗？

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/019.png)

[![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/020.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510898&idx=1&sn=3b4e8babc8aa2b71b5c5681534e8ff89&scene=21#wechat_redirect)

估值13亿美金，Clay 用 AI Agent 帮企业找客户

![](../images/2025-01-23-decagon-yong-ai-agent-jie-fang-ke-fu-tuan-dui-neng-fou-cheng/021.png)
