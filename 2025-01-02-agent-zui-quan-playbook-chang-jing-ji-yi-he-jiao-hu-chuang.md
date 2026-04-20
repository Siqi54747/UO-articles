---
title: Agent 最全 Playbook：场景、记忆和交互创新
publish_date: '2025-01-02'
publish_timestamp: 1735820999
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/1LAsbI0kPdp4xyXtMnelxA
msgid: 1000000316
appmsgid: 2247511038
itemidx: 1
digest: 2025 年 AI Agent 应用即将涌现，步入人机协作的新范式
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgy9NZib6ETP8tcibxXolqLIFMKLp2c9G3g6jA7eJfLPQiaK7mhVu3ficD1DPFU6feScqaKF2rOHibWs8mw/0?wx_fmt=jpeg
image_count: 37
archived_at: '2026-04-20T03:03:06+08:00'
---

[![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/001.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect)

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/002.png)

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/003.png)

编译：Jiayu, Cage

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/004.png)

AI Agent 是我们紧密追踪的范式变化，Langchain 的一系列文章对理解 Agent 的发展趋势很有帮助。在本篇编译中，第一部分是 Langchain 团队发布的 State of AI Agent 报告。他们采访了 1,300 多位从业者，包含开发者、产品经理、公司高管，揭示了 Agent 在今年的现状和落地瓶颈：**九成公司都对 AI Agent 有计划和需求，但 Agent 能力的局限让用户只能在少数流程和场景中落地。比起成本和 latency，大家更在乎 Agent 能力的提升，和对其行为的可观测和可控性。**

第二部分我们编译了 LangChain 官网的 In the Loop 系列文章中对 AI Agent 关键要素的分析：**规划能力、UI/UX 交互创新和记忆机制**。文中分析了 5 种 LLM-native 产品的交互方式，类比了 3 种人类的复杂记忆机制，对理解 AI Agent，对理解这些关键要素有所启发。在这一部分我们还加入了一些有代表性的 Agent 公司 case study，如 Reflection AI 创始人的访谈，来展望接下来 2025 年 AI Agent 的关键突破口。

在这个分析框架下，我们期待 2025 年 AI Agent 应用开始涌现，步入人机协作的新范式。对于 AI Agent 的规划能力，以 o3 为首的模型正在展现出很强的反思和推理能力，模型公司的进展正在从 reasoner 逼近到 Agent 阶段。随着推理能力持续提升，Agent 的“最后一公里”会是产品交互和记忆机制，这更可能是创业公司突破的机会。关于交互，我们一直期待 AI 时代的“GUI时刻“；关于记忆，我们相信 Context 会成为 Agent 落地的关键词，个人层面的 context 个性化、企业层面的 context 统一都会让 Agent 的产品体验得到大幅提升。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/005.png)

**💡**目录 **💡**

01 State of AI Agent

02 AI Agent 中的核心要素

**01.**

**State of AI Agent**

**Agent 使用趋势：**

**每个公司都在计划部署 Agent**

Agent 领域的竞争正在变激烈。在过去一年中，许多 Agent 框架变得普及：例如使用 ReAct 结合 LLM 进行推理和行动、使用 multi-agent 框架进行编排，或者是使用类似 LangGraph 这样更可控的框架。

关于 Agent 的讨论并不全是 Twitter 上的炒作。大约 51%的受访者目前正在生产中使用 Agent。根据 Langchain 按公司规模的数据，100-2000 员工的中型公司在 Agent 投入生产方面最为积极，比例达到63%。

此外，78%的受访者有在近期内将采用将 Agent 投入生产的计划。很明显，大家对 AI Agent 有很强烈的兴趣，但实际要做好一个 production-ready 的 Agent 对许多人来说仍然是一个难题。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/006.png)

尽管技术行业通常被认为是早期的 Agent 使用者，但所有行业对 Agent 的兴趣都在与日俱增。在非技术公司工作的受访者中，有90%已经或计划将Agent投入生产（与技术公司的比例几乎相同，为89%）。

**Agent 的常用 use case**

Agent 最常用的 use case 包括进行研究和总结（58%），其次是通过定制化的 Agent 简化工作流程 （53.5%）。

这些反映了人们希望有产品来处理那些过于消耗时间的任务。用户可以依赖 AI Agent 从大量信息中提取关键信息和见解，而不是自己从海量的数据中筛选，再进行资料回顾或研究分析。同样，AI Agent 可以通过协助日常任务来提升个人生产力，使用户能够专注于重要事项。

不仅个人需要这种效率的提升，公司和团队也同样需要。客服（45.8%）是 Agent的另一个主要应用领域，Agent 帮助公司处理咨询、故障排除，并加快跨团队的客户响应时间；排在第四、第五位的是更底层的 code 和 data 应用。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/007.png)

**监控：Agent 应用需要可观测和可控性**

随着 Agent 实现功能变得更加强大，就需要管理和监控 Agent 的方法。追踪和可观测性工具位列必备清单之首，帮助开发人员了解 Agent 的行为和性能。很多公司还使用 guardrail（防护控制）以防止 Agent 偏离轨道。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/008.png)

在测试 LLM 应用程序时，离线评估（39.8%）比在线评估（32.5%）被更常被使用，这反映了实时监控 LLM 的困难。在 LangChain 提供的开放式回答中，许多公司还让人类专家手动检查或评估响应，作为额外的预防层。

尽管人们对 Agent 的热情很高，但在 Agent 权限上普遍还是比较保守。很少有受访者允许他们的 Agent自由地读取、写入和删除。相反，大多数团队只允许读取权限的工具权限，或需要人类批准 Agent 才可以做更有风险的行动，如写入或删除。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/009.png)

不同规模的公司在 Agent 控制方面也有不同的优先级。不出所料，大型企业（2000名以上员工）更加谨慎，严重依赖 “read-only” 权限以避免不必要的风险。他们也倾向于将 guardrail 防护与离线评估相结合，不希望客户看到任何问题。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/010.png)

与此同时，小型公司和初创公司（少于100名员工）更专注于追踪以了解其 Agent 应用程序中发生了什么（而不是其他控制）。根据 LangChain 的调查数据，较小的公司倾向于专注于通过查看数据来理解结果；而大型企业则在全面范围内设置了更多的控制措施。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/011.png)

**将 Agent 投入生产的障碍和挑战**

保证 LLM 的高质量 performance 很难，回答需要有高准确性，还要符合正确的风格。这是 Agent 开发使用者们最关心的问题——比成本、安全等其他因素的重要性高出两倍多。

LLM Agent 是概率式的内容输出，意味着较强的不可预测性。这引入了更多的错误可能性，使得团队难以确保其 Agent 始终如一地提供准确、符合上下文的回应。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/012.png)

对于小型公司尤其如此，性能质量远远超过了其他考虑因素，有 45.8 %的人将其作为主要关注点，而成本（第二大关注点）仅为22.4%。这一差距强调了可靠、高质量的性能对于组织将 Agent 从开发转移到生产的重要性。

安全问题对于需要严格合规，并敏感处理客户数据的大型公司也普遍存在。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/013.png)

挑战不止于质量。从 LangChain 提供的开放式回答中，许多人对公司是否要持续投入开发和测试 Agent 仍保持怀疑。大家提到两个突出的阻碍：开发 Agent 需要的知识很多，且需要一直跟进技术前沿；开发部署 Agent 需要的时间成本很大，是否能可靠运行的收益又不太确定。

**其他新兴主题**

在开放性问题中，大家对 AI Agent 展示出的这些能力有很多称赞：

• 管理多步骤任务：AI Agent 能够进行更深入的推理和上下文管理，使它们能够处理更复杂的任务；

• 自动化重复性任务：AI Agent 继续被视为处理自动化任务的关键，这可以为用户解放时间，让他们去解决更有创造性的问题；

• 任务规划和协作：更好的任务规划确保正确的 Agent 在正确的时间处理正确的问题，特别是在 Multi-agent 系统中；

• 类似人类的推理：与传统LLM不同，AI Agent可以追溯其决策，包括根据新信息回顾并修改过去的决策。

此外大家还有两个最期待的进展：

• 对开源 AI Agent 的期待：人们对开源 AI Agent 的兴趣明显，许多人提到集体智慧可以加速 Agent 的创新；

• 对更强大的模型的期待：许多人正在期待由更大、更强大的模型驱动的 AI Agent 的下一次飞跃—在那时，Agent 能够以更高的效率和自主性处理更复杂的任务。

问答中很多人也提到了 Agent 开发时最大的挑战：如何理解 Agent 的行为。一些工程师提到他们在向公司 stakeholder 解释 AI Agent 的能力和行为时会遇到困难。部分时候可视化插件可以帮助解释 Agent 的行为，但在更多情况下 LLM 仍然是一个黑箱。额外的可解释性负担留给了工程团队。

**02.**

**AI Agent 中的核心要素**

**什么是 Agentic 系统**

在 State of AI Agent 报告发布之前，Langchain 团队已经在 Agent 领域写了自己的 Langraph 框架，并通过 In the Loop 博客讨论了很多 AI Agent 中的关键组件，接下来就是我们对其中关键内容的编译。

首先每个人对 AI Agent 的定义都略有不同，LangChain 创始人 Harrison Chase 给出的定义如下：

💡

AI Agent 是一个用 LLM 来做程序的控制流决策的系统。

*An AI agent is a system that uses an LLM to decide the control flow of an application.*

对其实现方式，文章中引入了 Cognitive architecture（认知架构） 的概念，认知架构是指 Agent 如何进行思考、系统如何去编排代码/ prompt LLM：

• Cognitive：Agent 使用 LLM 来语义推理该如何编排代码/ Prompt LLM;

• Architecture: 这些 Agent 系统仍然涉及大量类似于传统系统架构的工程。

下面这张图展示了不同层次 Cognitive architecture 的例子：

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/014.png)

• 标准化的软件代码（code） ：一切都是 Hard Code ，输出或输入的相关参数都直接固定在源代码中，这不构成一个认知架构，因为没有 cognitive 的部分；

• LLM Call ，除了一些数据预处理外，单个 LLM 的调用构成了应用程序的大部分，简单的 Chatbot 属于这一类；

• Chain：一系列 LLM 调用，Chain 尝试将问题的解决分成若干步，调用不同的 LLM 解决问题。复杂的 RAG 属于这一种：调用第一个 LLM 用来搜索、查询，调用第二个 LLM 用于生成答案；

• Router：在前面的三种系统中，用户可以提前知道程序会采取的所有步骤，但在 Router 中，LLM 自行决定调用哪些 LLM ，采取怎样的步骤，这增加了更多的随机性和不可预测性；

• State Machine ，将 LLM 与 Router 结合使用，这将更加不可预测，因为这样结合放入循环中，系统可以（理论上）做无限次的 LLM 调用；

• Agentic 的系统：大家也会称为“ Autonomous Agent ”，使用 State Machine 时，对于可以采取哪些操作以及在执行该操作后执行哪些流程仍然存在限制；但当使用 Autonomous Agent 时，这些限制将被删除。LLM 来决定采取哪些步骤、怎样去编排不同的 LLM ，这可以通过使用不同的 Prompt 、工具或代码来完成。

简单来说，一个系统越是“ Agentic ”，LLM 就越大程度地决定系统的行为方式。

**Agent 的关键要素**

**规划**

Agent 可靠性是一个很大的痛点。常常会有公司使用 LLM 构建了 Agent，却提到 Agent 无法很好地规划和推理。这里的规划和推理是什么意思呢？

Agent的计划和推理指的是 LLM 思考要采取什么行动的能力。这涉及短期和长期 reasoning ，LLM 评估所有可用信息，然后决定：我需要采取哪些一系列步骤，哪些是我现在应该采取的第一个步骤？

很多时候开发者使用 Function calling（函数调用）来让 LLM 选择要执行的操作。Function calling 是 OpenAI 于 2023 年 6 月首次添加到 LLM api 的能力，通过 Function calling ，用户可以为不同的函数提供 JSON 结构，并让 LLM 匹配其中一个（或多个）结构。

要成功完成一项复杂的任务，系统需要按顺序采取一系列行动。这种长期规划和推理对于 LLM 非常复杂：首先 LLM 必须考虑一个长期的行动规划，再回到要采取的短期行动中；其次，随着 Agent 执行越来越多的操作，操作的结果将反馈给 LLM ，导致上下文窗口增长，这可能会导致 LLM “分心”并表现不佳。

改进规划的最容易解决的办法是确保 LLM 拥有适当推理/计划所需的所有信息。尽管这听起来很简单，但通常传递给 LLM 的信息根本不足以让 LLM 做出合理的决定，添加检索步骤或阐明 Prompt 可能是一种简单的改进。

之后，可以考虑更改应用程序的认知架构。这里有两类认知架构来改进推理，通用认知架构和特定领域的认知架构：

**1. 通用认知架构**

通用认知架构可以应用于任何任务。这里有两篇论文提出了两种通用的架构，一个是 “plan and solve” 架构，在 Plan-and-Solve Prompting: Improving Zero-Shot Chain-of-Thought Reasoning by Large Language Models 一文中提出，在该架构中，Agent 首先提出一个计划，然后执行该计划中的每个步骤。另一种通用架构是 Reflexion 架构，这一架构在 Reflexion: Language Agents with Verbal Reinforcement Learning 中提出，在该架构中，Agent 执行任务后有一个明确的 “反射” 步骤，以反映它是否正确执行了该任务。这里不赘述，详细可看上两篇论文。

尽管这些想法显示出改进，但它们通常过于笼统，无法被 Agent 在生产中实际使用。（译者注：这篇文章发布时还没有 o1 系列模型）

**2. 特定领域的认知架构**

相反，我们看到 Agent 是使用特定领域的认知架构构建的。这通常表现在特定领域的分类/规划步骤、特定领域的验证步骤中。规划和反思的一些思想可以在这里应用，但它们通常以特定领域的方式应用。

AlphaCodium 的一篇论文中举了一个特定的例子：通过使用他们所谓的 “流工程”（另一种谈论认知架构的方式）实现了最先进的性能。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/015.png)

可以看到 Agent 的流程对于他们试图解决的问题非常具体。他们告诉 Agent 分步骤做什么：提出测试，然后提出解决方案，然后迭代更多测试等。这种认知架构是高度专注特定领域的，不能泛化到其他领域。

**Case Study:**

**Reflection AI 创始人  Laskin****对 Agent 未来的愿景**

在红杉资本对 Reflection AI 创始人 Misha Laskin 的访谈中，Misha 提到他正在开始实现他的愿景：即通过将 RL 的 Search Capability 与 LLM 相结合，在他的新公司 Reflection AI 中构建最佳的 Agent 模型。他和联合创始人 Ioannis Antonoglou（AlphaGo、AlphaZero 、Gemini RLHF 负责人）正在训练为 Agentic Workflows 设计的模型，访谈中的主要观点如下：

• **深度是 AI Agent 中缺失的部分。** 虽然当前的语言模型在广度方面表现出色，但它们缺乏可靠完成任务所需的深度。Laskin 认为，解决“深度问题”对于创建真正有能力的 AI Agent 至关重要，这里的能力是指：Agent 可以通过多个步骤规划和执行复杂的任务；

• **将 Learn 和 Search 相结合是实现超人性能的关键。** 借鉴 AlphaGo 的成功，Laskin 强调 AI 中最深刻的理念是 Learn（依靠 LLM）和 Search（找到最优路径）的结合。这种方法对于创建在复杂任务中可以胜过人类的 Agent 至关重要；

• **Post-training 和 Reward modeling 带来了重大挑战。** 与具有明确奖励的游戏不同，现实世界的任务通常缺乏真实奖励。开发可靠的 reward model，是创建可靠的 AI Agent 的关键挑战

• **Universal Agents 可能比我们想象的更接近。** Laskin 估计，我们可能只用三年时间就可以实现“digital AGI”，即同时具有广度和深度的 AI 系统。这一加速的时间表凸显了在能力发展的同时解决安全性和可靠性问题的紧迫性

• **通往 Universal Agents 的道路需要一种的方法。** Reflection AI 专注于扩展 Agent 功能，从一些特定的环境开始，如浏览器、coding 和计算机操作系统。他们的目标是开发 Universal Agents ，使其不局限于特定任务。

**UI/UX 交互**

在未来几年，人机交互会成为 research 的一个关键领域：Agent 系统与过去的传统计算机系统不同，因为延迟、不可靠性和自然语言界面带来了新的挑战。因此，与这些 Agent 应用程序交互的新 UI/UX 范式将出现。Agent 系统仍处于早期阶段，但已经出现多种新兴的 UX 范式。下面分别进行讨论：

**1. 对话式交互 (Chat UI)**

聊天一般分为两种：流式聊天（streaming chat）、非流式聊天（non-streaming Chat）。

流式聊天是目前最常见的 UX。它是一个 Chatbot，以聊天格式将其思想和行为流回——ChatGPT 是最受欢迎的例子。这种交互模式看起来很简单，但也有不错的效果，因为：其一，可以使用自然语言与 LLM 进行对话，这意味着客户和 LLM 没有任何障碍；其二，LLM 可能需要一段时间才能工作，流式处理使用户能够准确了解后台发生的事情；其三，LLM 常常会出错，Chat 提供了一个很好的界面来自然地纠正和指导它，大家已经非常习惯于在聊天中进行后续对话和迭代讨论事情。

但流式聊天也有其缺点。首先，流式聊天是一种相对较新的用户体验，因此我们现有的聊天平台（iMessage、Facebook Messenger、Slack 等）没有这种方式；其次，对于运行时间较长的任务来说，这有点尴尬—用户只是要坐在那里看着 Agent 工作吗；第三，流式聊天通常需要由人类触发，这意味着还需要大量 human in the loop。

非流式聊天的最大区别在于响应是分批返回的， LLM 在后台工作，用户并不急于让 LLM 立刻回答，这意味着它可能更容易集成到现有的工作流程中。人们已经习惯了给人类发短信——为什么他们不能适应用 AI 发短信呢？非流式聊天将使得与更复杂的 Agent 系统交互变得更加容易—这些系统通常需要一段时间，如果期望即时响应，这可能会令人沮丧。非流式聊天通常会消除这种期望，从而更轻松地执行更复杂的事情。

这两种聊天方式有以下优缺点：

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/016.png)

**2. 后台环境 (Ambient UX)**

用户会考虑向 AI 发送消息，这是上面谈到的 Chat，但如果 Agent 只是在后台工作，那我们该如何与 Agent 交互呢？

为了让 Agent 系统真正发挥其潜力，就需要有这种允许 AI 在后台工作的转变。当任务在后台处理时，用户通常更能容忍更长的完成时间（因为他们放宽了对低延迟的期望）。这使 Agent 可以腾出时间做更多的工作，通常比在聊天 UX 中更仔细、勤奋做更多推理。

此外，在后台运行 Agent 能扩展我们人类用户的能力。聊天界面通常限制我们一次只能执行一项任务。但是，如果 Agent 在后台环境运行，则可能会有许多 Agent 同时处理多个任务。

让 Agent 在后台运行，是需要用户信任的，该如何建立这种信任？一个简单的想法是：向用户准确展示 Agent 在做什么。显示它正在执行的所有步骤，并让用户观察正在发生的事情。虽然这些步骤可能不会立即可见（就像在流式传输响应时一样），但它应该可供用户点击并观察。下一步是不仅让用户看到发生了什么，还让他们纠正 Agent 。如果他们发现 Agent 在第 4 步（共 10 步）中做出了错误的选择，客户可以选择返回第 4 步并以某种方式更正 Agent 。

这种方法将用户**从 “In-the-loop” 转变为 “On-the-loop”。**“On-the-loop”要求能够向用户显示 Agent 执行的所有中间步骤，允许用户中途暂停工作流，提供反馈，然后让 Agent 继续。

AI 软件工程师 Devin 是实现类似 UX 的一个应用程序。Devin 运行时间较长，但客户可以看到所采取的所有步骤，倒回特定时间点的开发状态，并从那里发布更正。尽管 Agent 可能在后台运行，但这并不意味着它需要完全自主地执行任务。有时 Agent 不知道该做什么或如何回答，这时，它需要引起人类的注意并寻求帮助。

一个具体的例子是 Harrison 正在构建的电子邮件助理 Agent 。虽然电子邮件助理可以回复基本电子邮件，但它通常需要 Harrison 输入某些不想自动化的任务，包括：审查复杂的 LangChain 错误报告、决定是否要参加会议等。在这种情况下，电子邮件助理需要一种方法来向 Harrison 传达它需要信息来响应。请注意，它不是要求其直接回答；相反，它会征求 Harrison 对某些任务的意见，然后它可以使用这些任务来制作和发送一封漂亮的电子邮件或安排日历邀请。

目前，Harrison 在 Slack 中设置了这个助手。它向 Harrison 发送一个问题，Harrison 在 Dashboard 中回答它，与其工作流程原生集成。这种类型的 UX类似于客户支持 Dashboard 的 UX。此界面将显示助手需要人工帮助的所有区域、请求的优先级以及任何其他数据。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/017.png)

**3. 电子表格 (Spreadsheet UX)**

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/018.png)

电子表格 UX 是一种支持批量处理工作的超级直观且用户友好的方式。每个表格、甚至每一列都成为自己的 Agent，去研究特定的东西。这种批量处理允许用户扩展与多个 Agent 交互。

这种 UX 还有其他好处。电子表格格式是大多数用户都熟悉的 UX，因此它非常适合现有的工作流程。这种类型的 UX 非常适合数据扩充，这是一种常见的 LLM 用例，其中每列可以表示要扩充的不同属性。

Exa AI、Clay AI、Manaflow 等公司的产品都在使用这种 UX，下以 Manaflow举例展示这种电子表格 UX 如何处理工作流程。

**Case Study:**

**Manaflow 如何使用****电子表格进行 Agent 交互**

Manaflow 的灵感来源于创始人 Lawrence 曾任职的公司 Minion AI，Minion AI 构建的产品是 Web Agent 。Web Agent 可以控制本地的 Geogle Chrome，允许其与应用程序交互，例如订机票、发送电子邮件、安排洗车等。基于Minion AI 的灵感，Manaflow 选择让 Agent 去操作电子表格类的工具，这是因为 Agent 不擅长处理人类的 UI 界面，Agent 真正擅长的是 Coding。因此 Manaflow 让 Agent 去调用 UI 界面的的 Python 脚本，数据库接口，链接API，然后直接对数据库进行操作：包括阅读时间、预定、发邮件等等。

其工作流如下：Manaflow 的主要界面是一个电子表格（Manasheet），其中每列代表工作流程中的一个步骤，每行对应于执行任务的 AI Agent。每个电子表格的 workflow 都可以使用自然语言进行编程（允许非技术用户用自然语言描述任务和步骤）。每个电子表格都有一个内部依赖关系图，用于确定每列的执行顺序。这些顺序会分配给每一行的 Agent 并行执行任务，处理数据转换、API 调用、内容检索和发送消息等流程：

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/019.png)

生成 Manasheet 可以的方法为：输入类似上面红色框里的自然语言，如上图中想向客户可以发送定价的邮件，就可以通过 Chat 输入 Prompt，来生成 Manasheet。通过 Manasheet 可以看到有客户的姓名，客户的邮箱，客户所属的行业，是否已经发送邮件等信息；点击 Execute Manasheet 即可执行任务。

**4. 生成式 UI (Generative UI)**

“生成式 UI”有两种不同的实现方式。

一种方式是由模型自行生成需要的的原始组件。这类似于 Websim 等产品。在后台，Agent 主要编写原始 HTML，使其能够完全控制显示的内容。但是这种方法允许生成的 web app 质量有很高的不确定性，因此最终结果可能看起来波动较大。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/020.png)

另一种更受约束的方法为：预定义一些 UI 组件，这通常是通过工具调用来完成的。例如，如果 LLM 调用天气 API，则它会触发天气地图 UI 组件的渲染。由于渲染的组件不是真正生成的（但是有更多选择），因此生成的 UI 将更加精致，尽管它可以生成的内容不完全灵活。

**Case Study：**

**Personal AI 产品 dot**

举例来说，在 2024 年曾被称为最好的 Personal AI 产品的 Dot，就是一个很好的生成式 UI 产品。

Dot 是 New Computer 公司的产品：其目标是成为用户的长期伴侣，而并不是更好的任务管理工具，据联合创始人Jason Yuan讲，Dot 的感觉是，当你不知道该去哪里、该做什么或该说什么时，你就会求助于 Dot。这里举两个例子介绍产品是做什么的：

• 创始人 Jason Yuan 常常在深夜让 Dot 推荐酒吧，说自己想要一醉方休，断断续续几个月，某天下班之后，Yuan 再次问了相似的问题，Dot 竟然开始劝解 Jason，不能再这样下去了；

• Fast Company 记者 Mark Wilson，也和 Dot 相处了几个月的时间。有一次，他向 Dot 分享了书法课上他手写的一个「O」，Dot 竟然调出了几周前他手写「O」的照片，夸他的书法水平提高了。

• 随着使用Dot的时间越来越多，Dot 更加理解了用户喜欢打卡咖啡馆，主动推送给主人附近的好咖啡馆，附上了为何这个咖啡馆好，最后还贴心的询问是否要导航.

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/021.png)

可以看到在这个咖啡馆推荐的例子中，Dot 通过预定义 UI 组件，来达到 LLM-native 的交互效果。

**5. 协作式 UX（Collaborative UX）**

当 Agent 和人类一起工作时会发生什么？想想 Google Docs，客户可以在其中与团队成员协作编写或编辑文档，但倘如协作者之一是 Agent 呢？

**Geoffrey Litt** 和 **Ink & Switch** 合作的 **Patchwork项目**是人类- Agent 合作的一个很好的例子。（译者注：这可能是最近 OpenAI Canvas 产品更新的灵感来源）。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/022.png)

协作式 UX 与前面讨论的 Ambient UX 相比如何？LangChain创始工程师 Nuno 强调了两者之间的主要区别，在于是否有并发性：

• 在**协作式 UX** 中，客户和LLM 经常同时工作，以彼此的工作为输入；

• 在**环境 UX** 中，LLM 在后台持续工作，而用户则完全专注于其他事情。

**记忆**

记忆对于好的 Agent 体验至关重要。想象一下如果你有一个同事从来不记得你告诉他们什么，强迫你不断重复这些信息，这个协作体验会非常差。人们通常期望 LLM 系统天生就有记忆，这可能是因为 LLM 感觉已经很像人类了。但是，LLM 本身并不能记住任何事物。

Agent 的记忆是基于产品本身需要的，而且不同的 UX 提供了不同的方法来收集信息和更新反馈。我们能从 Agent 产品的记忆机制中看到不同的高级记忆类型——它们在模仿人类的记忆类型。

论文 CoALA: Cognitive Architectures for Language Agents 将人类的记忆类型映射到了 Agent 记忆上，分类方式如下图的所示：

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/023.png)

**1. 程序记忆（Procedural Memory）：**有关如何执行任务的长期记忆，类似于大脑的核心指令集

• 人类的程序记忆：记住如何骑自行车。

• Agent 的程序记忆：CoALA 论文将程序记忆描述为 LLM 权重和 Agent 代码的组合，它们从根本上决定了 Agent 的工作方式。

在实践中，Langchain 团队还没有看到任何 Agent 系统会自动更新其 LLM 或重写其代码，但是确实存在一些 Agent 更新其 system prompt 的例子。

**2. 语义记忆(Semantic Memory):** 长期知识储备

• 人类的语义记忆：它由信息片段组成，例如在学校学到的事实、概念以及它们之间的关系。

• Agent 的语义记忆：CoALA 论文将语义记忆描述为事实存储库。

在实践中上，常常是通过使用 LLM 从 Agent 的对话或交互中提取信息来实现的。此信息的确切存储方式通常是特定于应用程序的。然后这些信息在将来的对话中检索并插入到 System Prompt 中 以影响 Agent 的响应。

**3. 情景记忆（Episodic Memory）：**回忆特定的过去事件

• 人类的情景记忆：当一个人回忆起过去经历的特定事件（或“情节”）时。

• Agent 中的情景记忆：CoALA 论文将情景记忆定义为存储 Agent 过去动作的序列。

这主要用于让 Agent 按预期执行动作。在实践中，情景记忆的更新通过 Few-Shots Prompt 的方法实现。如果相关更新的 Few-Shots Prompt 足够多，那么接下来的更新就通过 Dynamic Few-Shots Prompt 来完成。

如果一开始就有指导 Agent 正确完成操作的办法，后面面对同样的问题就可以直接使用这种办法；相反，如果不存在正确的操作方式，或者如果 Agent 不断做新的事情，那么语义记忆就会更重要，反而在前面的例子中，语义记忆不会有太大帮助。

除了考虑要在 Agent 中更新的记忆类型外，开发人员还要考虑如何更新 Agent 的记忆：

更新 Agent 记忆的第一种方法是 **“in the hot path”**。在这种情况下， Agent 系统会在响应之前记住事实（通常通过工具调用）， ChatGPT 采取这种方法更新其记忆；

更新 Agent 记忆的另一种方法是 **“in the background”** 。在这种情况下，后台进程会在会话之后运行以更新记忆。

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/024.png)

比较这两种方法，“in the hot path” 方法的缺点是在传递任何响应之前会有一些延迟，它还需要将 memory logic 与 agent logic 相结合。

但是， “in the background ”可以避免这些问题 - 不会增加延迟，并且 memory logic 保持独立。但是“in the background ”也有其自身的缺点：记忆不会立即更新，并且需要额外的 logic 来确定何时启动后台进程。

更新记忆的另一种方法涉及用户反馈，这与情景记忆特别相关。例如，如果用户对某次交互标评分较高（Postive Feedback），Agent 可以保存该反馈以备将来调用。

基于以上编译内容，我们期待规划、交互、记忆三个组件的同时进步，会让我们在 2025 年看到更多可用的 AI Agent，进入人机协同工作的新时代。

**Reference**

https://www.langchain.com/stateofaiagents

https://blog.langchain.dev/tag/in-the-loop/

https://www.sequoiacap.com/podcast/training-data-misha-laskin/

https://www.youtube.com/watch?v=pBBe1pk8hf4

https://www.qodo.ai/products/alpha-codium/?ref=blog.langchain.dev

https://news.ycombinator.com/item?id=41259754

https://arxiv.org/pdf/2309.02427

https://github.com/mem0ai/mem0

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/025.png)

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/026.png)

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/027.png)

排版：杨乐乐

延伸阅读

[![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/028.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510990&idx=1&sn=2e5ad4a0b80c9900095929eff692cdaf&scene=21#wechat_redirect)

LLM 竞赛 2025: 超越 Google 之路

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/029.png)

[![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/030.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510949&idx=1&sn=015de5d623ae801d0f25a8e992bdd92f&scene=21#wechat_redirect)

Metronome：OpenAI、Anthropic背后的计费平台，会是AI时代的Stripe吗？

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/031.png)

[![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/032.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510898&idx=1&sn=3b4e8babc8aa2b71b5c5681534e8ff89&scene=21#wechat_redirect)

估值13亿美金，Clay 用 AI Agent 帮企业找客户

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/033.png)

[![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/034.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510837&idx=1&sn=0519e620d90fc536a0140aee9b1fce70&scene=21#wechat_redirect)

Bolt.new：AI Coding 领域的 Figma，2 个月实现近千万美元 ARR

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/035.png)

[![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/036.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510791&idx=1&sn=23c60bf34dac2f4906d897fc6b7863e1&scene=21#wechat_redirect)

Abridge：AI Scribe 成为 AI 医疗应用的最佳实践

![](../images/2025-01-02-agent-zui-quan-playbook-chang-jing-ji-yi-he-jiao-hu-chuang/037.png)
