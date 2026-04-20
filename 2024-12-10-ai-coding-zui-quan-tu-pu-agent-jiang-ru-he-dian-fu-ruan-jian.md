---
title: AI Coding 最全图谱：Agent 将如何颠覆软件
publish_date: '2024-12-10'
publish_timestamp: 1733833968
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/6pOGxolaJ5JE1fvzrReNfg
msgid: 1000000307
appmsgid: 2247510746
itemidx: 1
digest: AI Coding 将会开启多大的市场？
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxaI3vG3QuG5skltiaZF4jfaYtPte0uVbVjomQ7zlvvnhmyTLmjYNRmM02z6ZxVcPMRaUdw3SzyWcA/0?wx_fmt=jpeg
image_count: 24
archived_at: '2026-04-20T02:57:33+08:00'
---

[![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/001.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect)

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/002.png)

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/003.png)

作者：Cage

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/004.png)

Coding 领域的投资在两个核心变化的趋势下，底层推理引擎的持续进步和市场空间的变化，因此格外值得我们关注。LLM 作为推理引擎，coding 是最好的应用场景：代码的逻辑比自然语言更清晰，执行的结果能由 AI 自动化验证。因此我们看到从 Sonnet 3.5 到 o1 pro，每一次模型能力的提升都会反映在 coding 能力的提升上，这一领域的应用进步就尤其显著。

能力的持续进步让我们期待软件生产过程中有专业开发者之外的更多用户参与进来。本次研究对 AI coding 领域的方向和公司进行全览，研究框架中除了面向 professional（专业，包括企业和独立）开发者的产品，还有 citizen（小白，泛知识工作者）开发者方向的公司，他们的产品重心有所差异。

面向 professional developer，我们期待的是 coding 能比其他垂直方向更快地从 copilot 进化到 agent，并且两者共存。现阶段 [Cursor](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510163&idx=1&sn=f3a636901cd1b55dadf71e2884f04982&scene=21#wechat_redirect)、Windsurf 等产品体验非常优秀的 copilot 对独立开发者的工作体验和生产力已经带来了巨大提升。而企业中有庞大的 codebase、复杂的 engineering context，以及严格的安全合规要求，这些短期之内很难快速解决。因此 agent 会在 testing、review、migration 等具体 use case 上落地，同时通用的 copilot IDE 仍能发挥价值成为 coding agent 的工作环境。

对于 citizen developer，我们期待软件生产方式有颠覆性的变革，出现新一代产品形态 task engine。AI coding 能使更多知识工作者的长尾需求被实现，生成出 disposable app：随用随抛的下一代软件，每一个 app 不需要满足大量 DAU，而是针对不同用户有自己个性化的体验，其中的内容甚至可以实时生成。UI/UX 交互层面的创新是必要的，交互门槛更低的产品能允许更多用户表达个性化需求，形成 coding agent 层面的新一代 OS。类比 PC 历史，现在的产品还在命令行时代，我们期待 AI coding 方向的“GUI 时刻“。

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/005.png)

**💡**目录 **💡**

01  Investment Thesis

02  State of AI coding landscape

03  Open Discussion

**01.**

**Investment Thesis**

Coding 领域的投资主要面临着两个大变化，底层推理引擎的持续进步和市场空间的变化：

**1）Coding 能力是 LLM + RL 范式下能力进化最快的方向，会是从 copilot 渐进到 agent 的第一个领域。**

RL 范式下，自动化验证的环境、明确的reward model 是推理能力提升的重要前提。coding 就是最适合符合这个要求的场景，很可能是 LLM 从 copilot 走向 agent 的第一个场景。o1 pro 的发布再次验证了这一 thesis。

**2）Task engine 会把市场从 5000 万开发者拓展到 5 亿知识工作者，从 professional citizen developers。**

专业开发者只有 5000万，世界上有 99%的人不会写代码。但其实有很多人有个性化的任务需求，适合由软件来进行规范化。之前软件行业的试错成本太高，而 AI 生成式的 task engine 能带来这样的很多软件。

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/006.jpg)

想像下一代的互联网，用户在浏览器网址框输入的不再是网址，而是自然语言 prompt，需要的内容就会实时生成渲染出来；下一代的操作系统每次打开，都会根据用户近期行为和时间环境得到最适合的内容。这里可能孕育着 AI 时代 Google 的机会，成为赛博世界的新入口。

以上是我们看好 AI coding 领域投资机会的根本原因，接下来介绍对 AI coding landscape 中兴起几类产品的分类坐标系：

**•**Y 轴定义标准：产品多大程度地需要 human in the loop，上方产品更能端到端完成任务，下方更专注于 empower developer；

**•**X 轴定义标准：产品的目标用户的开发能力有多强。左侧产品偏向于服务专业开发者，右侧偏向于服务没有编程基础的用户。

**3）Copilot for pro & Agent for citizen 是现在模型能力与产品需求相匹配的领域。**

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/007.jpg)

**•****左下象限，Copilot for pro dev：**

最近口碑优秀的产品 Cursor、Codeium Windsurf 等基本都在这个象限。他们能在 early adopter 开发者圈子获得了优秀的口碑，对用户需求的深入理解和 Claude Sonnet 3.5 出色的意图理解能力在这里缺一不可。

他们要保持的增长的关键问题是，优秀的产品体验能得到 indie developer 的欣赏，但这对于 enterprise GTM 只是必要条件，而不是充分条件。从产品到企业信任，还有 privacy/compliance 等很多复杂需求。同时最近觉醒开始加速迭代的 Github Copilot 对他们的市场空间也会压缩。

**•****右上象限，Agent for citizen dev：**

给普通人的 coding agent 产品形态还没有固定：几个 coding 领域的前端deployment 和 web IDE 独角兽推出了自己的产品，Vercel V0， bolt.new 能智能地生成前端 web app，Replit agent 可以跟用户多轮交互生成基础的软件；而早期的创业公司则有更创新的产品形态，websim 在模拟实时生成的 chrome，wordware 用类似 notion 的交互使用户在其产品中创作软件。

但这个象限的机会可能才刚刚开始，因为目前的产品还拘泥于之前的思路。可以类比施乐实验室创新 GUI 之前的命令行时代，对大众用户的使用门槛很高，停留在 early adopter 圈子。

**•****左上象限，Agent for pro dev：**

要实现这一愿景，现在的模型能力还要继续提升。欧美有>5家融资规模上亿美金的公司在这个领域攻坚，因为 code token 的消耗量级很大，要解决的工程问题也很多。其中最关键的问题是企业 codebase context 的问题：

一方面，如何从巨大的 codebase 中做精准的 retrieval 是个难题，在科技大厂中也常常有老工程师离职之后之前的代码项目难以理解的问题，AI 理论上能有更长的 context window 但目前理解并搜索的精确度还不够；另一方面，enterprise codebase 中包括了大量公司内部的业务逻辑，需要专有数据微调、甚至 on-prem deployment。MS Stanley/Coca Cola 这样的大型企业 developer 数量是不比 Google、Meta 少的，而他们对 compliance 和 privacy 的要求高于技术本身。

**• 右下上限，copilot for citizen dev：**

这一个领域已经有比较成熟的解决方案，因此后文的公司 mapping 中不会出现这一象限。之前几代 low-code/RPA 有不少成功的产品，也有 UIPath 等上市公司和 Retool 等独角兽公司。但他们都停留在 copilot 阶段，其抽象方式只能辅助一部分用户固定的工作流。

反而 excel 成为了最好的 no-code 产品，帮助大部分知识工作者实现了很多科学计算和统计任务。这是一个有趣的历史启示，这一代 AI Coding 产品面对的 "Excel" 是 ChatGPT 这个 5 亿 MAU 的产品，如何绕过他们的 user base 和最强模型是创业团队们要思考和保持迭代的问题。

**02.**

**State of AI coding landscape**

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/008.jpg)

根据以上 thesis，我们对整个 AI 编程图景下的创业公司进行了 mapping：

**• Copilot for pro：**根据开发工作流可以分为 Coding、Testing、Code review 和 Code search。其中核心价值还是集中在入口级的 coding 部分。

**• Agent for pro：**这个领域有两类公司，Coding agent 和 coding model 公司。他们之间最大的差异是是否从头开发模型。前者是基于顶尖 LLM 之上去建立工作流和 agent，而 coding model 类公司则自己从头开始训练 coding-specific 模型。其中并不看好后一类，因为在 LLM 公司的主航道上。

**• Agent for citizen：**这个领域的公司目前还没有明显的收敛，我们可以分为三类。第一类是 task engine，为用户完成任务实现 Prototype 的 Task engine 类公司；第二类是前端网页生成；第三类是 low-code 类使用“乐高”式组件搭建应用的产品。最终大家的目标可能都是 task engine，只是现在大家选择了不同的路线 bet on。

**Copilot for pro**

•**Coding 代表公司：Anysphere(Cursor), Codeium, Augment**

**Product**

专注在编程体验的产品可以分为两类：IDE 和 VSCode extension。两者有各自的优势：自己做 IDE 能有完整的产品自由度和用户数据积累，做 VSCode Extension 则更加敏捷、用户迁移成本比较低。

Cursor 团队在这里的选择很聪明，通过 fork VSCode 获得了两个选择各自的优势。Codeium 也在通过 Windsurf 也都在往 IDE 的方向切入，因为 IDE 还是更好的入口级产品，能自己积累数据、有更多 feature 修改的空间，这对于产品构建自己的壁垒至关重要。

Cursor 在用户体验上花了很多精力，做到“快”和 next action prediction。这样用户的开发过程就是不断按 Tab，进入很快得到反馈的正循环中（快=fun，进入心流）。上个月他们收购 Supermaven，就是把产品体验中的“快”做到极致；这意味着短期内的重点还在人与 AI 的同步协作，o1 这样的异步交互暂时还不在产品主线上。

而 Codeium 团队从 VSCode extension 开始到 IDE，体现出了和 cursor 团队思路的区别。Cursor 更强调编程体验和对用户下一步意图的识别，Codeium 的新产品 Windsurf 更强调高自动化。他们的 Chat 功能比 Cursor 做得更加完善，很多用户不用 hands-on code 也能完成基础的开发。

同时，他们的产品还体现出了更强的对企业级需求更强的理解，支持 on-prem 专有模型和各种compliance协议。这里就要提到他们在 GTM 策略上的巨大差异。

**Market**

根据 Sacra 最新报告 Cursor 产品 ARR 已经达到 $65M，也就是大约30万付费用户。由于 Cursor 的产品没有对企业级codebase的重视，他们的核心用户还是硅谷 indie hacker。那他们未来的关键 bet 是 indie hacker 是否能在所有开发者比例中变高：如果 AI 产品的开发范式下独立开发者数量达到500万，也就等于今天所有开发者的 10%，cursor 的市场空间才能达到十亿美金。

而企业侧 BD 和开发者市场的增长方式不一样，Codeium 在企业 GTM 签订单上的能力很强。因为企业数据 compliance 需求不是最顺畅的产品体验，而是在安全、合规等企业在意的方向有。在 Latent Space 的一篇专访中 Anshul 提出了 enterprise infra native 的概念，强调了要做财富500强用户，需要突破硅谷开发者圈子的mindset：

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/009.png)

• **安全：**需要支持多种部署选项，比如 self-host 或混合部署；容器化部署（Docker、Kubernetes）是关键，需确保客户环境的数据隔离。

• **合规：**企业对 LLM 使用的训练数据有高度敏感性，需证明未使用受版权保护或未经许可的数据；数据清理和数据来源追踪，确保合规性。

•**个性化：**数据质量直接决定个性化效果，需要对数据的时效性和相关性进行评估。，帮助企业通过 fine-tuning/RAG 写出更高质量的代码。数据预处理和基于角色的访问控制（RBAC）是关键，避免因信息整合导致数据泄露。

•**ROI 分析：**生成式 AI 的 ROI 难以量化，通过提供分团队的使用数据，帮助客户优化使用效果、证明价值。

**• 规模：**企业环境复杂且规模庞大（如数万代码库、数万开发者），需解决大规模索引和延迟管理的问题。系统设计需在高用户量、高数据量的情况下保持高效稳定。

企业侧的机会可能是更明确的低垂果实，只是他们面对的竞争是 Github Copilot 极强的分发渠道。面对竞争时，用 research 去解决 Github 可能做不好的地方是至关重要的。

**Research**

这些 coding 公司不能只看成应用层产品公司，而是 research 和产品一体的公司。Cursor 官网称自己为 applied resarch lab，Codeium 官网博客中写了大量对微调/RAG 技术方案的思考，Augment 也在 Retrieval、RL 等方向上做了大量探索。

Augment 和 Codeium 更在乎的是企业级技术方案，尤其是 Github Copilot 目前解决不好的问题。例如 Augment 在解决的事在数万个企业codebase 中怎么精准地做好 retrieval 和交互理解。和企业文档 RAG 遇到的难题类似，codebase retrieval 需要重新训练专用的 embedding model，对话、补全、跨文件生成需要的embedding 都不一样。Codeium 还思考很多在企业 on-prem/VPC 上部署专用 coding 模型的问题，来达到安全性和智能程度的平衡。

而对于 Cursor，强 reasoning 能力下的异步协同是研究的核心方向，对应到内部项目 shadow workspace。shadow workspace 是 Cursor 为后台 coding agent 设计的开发空间，这个空间需要能看到 agent 修改引发的 lint 提示信息，并且和 IDE 背后的LSP协议进行充分交互，但不去修改用户原本的文件。AI 和用户会一起根据 shadow workspace 下的 Lint 反馈来决定是否进行下一步的迭代。这个过程和 o1 inference time compute 类似。

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/010.png)

Shadow Workspace 早期架构图

**• Testing 代表公司：QA Wolf, Momentic, Gru AI**

Coding testing 是所有开发者必经的工作流，来保证代码的准确性。其中有两个常见常见：其一是 unit test，在错综复杂的系统中，代码被更新之后需要 unit test 来验证其可用性，减少其引发意外崩溃的概率；其二是前端或应用开发中，需要对 UI 每一个功能进行交互测试。

测试任务和 codegen 的适配度也很高，因为：其写的过程是高重复性高，且有规律可循的；而且这是人类工程师不太愿意工作的任务，大部分团队的 unit test 的覆盖率比较低，能侧面说明这一点。

同时 Cursor 团队在访谈中提到过 debug 对 LLM 底座颇有难度，LLM 的训练方式不是去发现错误，要让 LLM 理解一个看起来不大错误的后续重大影响是比较难的。因此这里能有独立创业公司的机会。

这个领域的代表公司中：QA Wolf 是 LLM 出现之前就有的公司，以 Rule-based 的方法就能实现很多 test case；Momentic 是最近 YC 和 AI Grant 中涌现的项目，更偏向人和 AI 协作对视觉产品 UI 进行测试；Gru AI 则是为 Unit Test 场景设计专用的 agent 来端到端企业中的测试需求。

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/011.png)

Momentic feature from homepage

• **Code Review & Refactor 代表公司：CodeRabbit**

Code Review & Refactor 是开发者工作中比较重要的质量保障工作，无论是企业还是独立开发者都需要花时间 review 组织内外部的 PR request。根据 Techcrunch，50% 的 enterprise developer 每周要花5个小时进行 code review相关工作。

这里的代表公司 CodeRabbit 不到一年的时间内就实现了 $100M+ ARR，是GitHub 和 GitLab 上安装次数最多的 AI app，已经review PR 300万条以上，说明 LLM-native 产品在这个领域已经能提供不错的服务。

同时还有更大型的 CI/CD 任务可以被归类为 code refactoring，对代码项目进行优化和重构，来解决组织中之前遗留的技术债，甚至可能对技术架构需要进行重构和迁移，那就是 Code Migration。这样的需求也是非常繁重、人类工程师不太愿意完成的。因此，这成了我们接下来介绍的 Coding agent 公司最早得到 PMF 的场景。

**Agent for pro**

• **Coding agent 代表公司：Cognition (Devin), Factory**

Coding agent 公司的平均融资规模是最大的，因为这些公司的目标是实现 end-to-end 替代人类开发者，实现这个过程的工程量大、消耗 code tokens 数量大。这个领域的现状可能有两个要解决的问题：

1) 技术上模型底层推理能力不够。在企业大 codebase 中去完整的处理问题需要很强的推理能力，去理解用户和codebase 两端的 context，然后将任务拆解为多个解决步骤。这样的 long-context + long-horizon reasoning 能力才能真正解决企业侧复杂的工程问题。

2) 产品上，UI/UX 层需要与人类协作方式的创新。既然模型的能力还没达到完全可用，如何去 involve human in the loop 到协作中就是一个比较难的问题：模型遇到难的问题时是选择 inference-time compute 做搜索还是交给用户去介入给更多的指导和context？如果这个问题解决得不好，呈现出的效果可能是，AI 自己工作了 12 个小时之后发现束手无策，交给用户也很难在AI 的基础上进行修正。

由于以上问题，我们推测现在实际能有 PMF 的场景会是 code migration，code refactoring 和 PR commit 等任务。这些任务对于开发者来说往往是 toil 也就是不愿意做的事情，开发者专注在这些任务上以后可以把精力集中在别的更有创造力的领域。因此目前 coding agent 现阶段做得更多是从 1 到 100 的事情，还没有到从 0到 1 的任务上。我们看好 coding agent 在未来 2 年内会逐渐承担更多的责任，不过那需要底层模型的能力和上层 agent 框架的共同进步。

定价问题也很值得思考：传统 dev tool 的定价一般是按使用者数量 seat-based 付费，对于coding agent 而言 consumption-based 付费可能是更合理的定价，优秀的、完成大量任务的 coding agent 价格可能值得和 junior developer 在同一个数量级。

**• Coding Model 代表公司：Poolside、Magic**

Coding 领域对模型能力的要求是不完全一致的，比如 code tokenizer 对代码中的变量、符号、函数名都要做专门的切分，以及主流 LLM 的训练是以文本生成为主要目标函数，代码能力看起来是其智能的副产品。因此 Coding model 领域开始出现一些独立公司：

• Magic 强调特别长的 context window，能把企业中复杂的 codebase 完整读进来解决问题，尽量避免 retrieval；

• Poolside 强调 RL from machine feedback，能把 Git history 中复杂的工程链条完整解决。

不过这一领域的公司在 OpenAI、Anthropic 的主航道上，考虑到 Coding 能力是模型推理能力最好的proxy，这两家公司的模型一定会在 LLM + RL 的范式下在 coding 能力上持续进步。

**Autopilot for citizen**

**• Task engine 代表产品：Replit、Websim、Wordware**

Task engine 对应的是 search engine，用户得到的不再是基于搜索关键词的网页，而是基于用户需求生成的软件。我们定义为 task engine 是希望弱化软件和 code 这些词带来的高门槛意味，coding 能力带来的 killer app 应该是大众用户都有意愿和能力去使用的。

Anthropic Artifact 和 OpenAI Canvas 在一定层面上也是希望能实现这个目标，但其产品形态并不是很易用，加上用户对主产品的预期还是 chatbot。因此现在的 task engine 还在命令行时代，需要一个 GUI 级别的产品创新来让更多用户能理解使用。

目前这类产品的形态其实还有很大分歧：

• **Replit agent:** cloud IDE for coding agent。产品使用 chat 多轮对话交互，每一次执行 action 都是渐进式的，遇到问题会向用户提问来补足context、厘清需求，对话过程类似开发者和产品经理对需求的过程。这种产品设计思路用 alignment 解决了模型多步执行时的可靠性问题，但也要求用户对自己的需求想得比较清楚。

• **Wordware:** Notion for LLM app。产品完成度高，使用体验比较像创作内容，通过 Twitter 嘲讽 bot 找到了很好的viral 增长第一枪。用 Twitter 作为增长起点的方式让人想起了去年的 Perplexity。成为增长最快的 ProductHunt 产品之后，流量开始快速下降，高度依赖头部流量产品是 Wordware 现在的挑战。

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/012.png)

**• Websim:** 用类似 Google Chrome 的简陋 UI，打造了一个用户能同时创作和消费 web app 的产品。这个产品的想象空间很大，用户可以在上面基于用户的 template 继续生成和修改，有点像 Canva 的模板化思路。而且用户在 Websim 上打造的网站每一个超链接可以继续点击并深入生成新的网站。不过他们的产品设计细节还欠打磨，有点类似 C.ai 有一个很好的框架但在产品上不够极致。

•**前端生成代表公司：Vercel (V0)、Stackblitz (Bolt.new)**

这一领域的公司之前就在前端框架和部署领域有比较深的积累。例如 Vercel 是 Next.js 框架的发明者，主要业务是前端网站的部署，ARR 也已经达到 1 亿美金以上，我们之前有过详细的研究。他们的 Vercel V0 产品一直在进步，无论是审美风格还是对话修改上的体验都比刚发布时优秀很多。另一个很火的产品是 bolt.new，也能通过一句话把产品需求变成不错的 web app 产品。其进步速度更快，同样的prompt 每一两周都能看到其生成质量的进步。

这类产品的效果已经接近可用了，不过实际持续使用的时候会遇到一些问题。web app 生成出来的 demo 十分优秀，但由于其技术栈比较杂，生成的产品真正开始有规模之后很难维护和管理。因此前端生成的未来 use case 很可能是 desposable application，这个网页的生成就是为了服务某个临时、长尾的需求，并不用为更大的群体、更长的时间去维护。

前端是开发中相对好上手的领域，因此之前每一代 Low-code/No-code 都会讲前端民主化的故事，诞生了 Wordpress、Wix、Spacesquare 甚至 Shopify 这样的公司。整个市场很大，但需求比较零碎，市场头部集中度不高。AI 前端生成现在看起来很有前景，但他们是否能抓住大量增量需求，甚至代替过去的存量需求呢？这直接决定了其市场规模的上限。

**03.**

**Open Discussion**

**1）Coding 能力的民主化？不，是软件工程的民主化。**

技术会带来一个领域的民主化，这是很多领域都发生过的故事，例如 Canva 成为了设计师民主化的一站式模版和设计平台。而开发领域是否会有这样的民主化故事呢？

我们认为 Coding 能力不会发生民主化，但软件工程会。这意味着软件的制造成本会随着 AI coding 带来大幅下降，但用户不一定需要理解 code 编程是如何操作并执行的，只需要明白 high level 的运行逻辑即刻。也就是说，用户们不需要是开发者，但需要是自己需求的产品经理

**2）UI/UX：同步与异步，GUI 时刻的到来。**

未来的开发体验可能由同步和异步组成：同步的部分，开发者一边写代码，AI 一边在后台同步做 code testing/review/optimization；异步的部分，o1范式下的 inference-time compute 能把 coding 任务拆解为多个子任务，推理出最合适的解决方案并自己验证。

而未来更广义的 AI coding 也是如此，很多软件都是实时根据 context 来实时生成，而真正复杂的任务则不需要交互，AI 能异步的完成并通过邮件等方式向用户同步。

现在的产品交互使用门槛还偏高，类似 GUI 到来前的命令行时刻。等待新交互到来时，AI 应用的空间会被打开，coding 领域可能是最先验证和感知到的。

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/013.png)

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/014.png)

排版：Doro

延伸阅读

[![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/015.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510708&idx=1&sn=b0845873a87e9a344ee23c221d922214&scene=21#wechat_redirect)

Sora V2 即将发布，AI Creativity 赛道有哪些机会？

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/016.png)

[![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/017.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510599&idx=1&sn=ee43e19424257d4fde48b01f5b0b1453&scene=21#wechat_redirect)

AI-native 应用长什么样？

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/018.png)

[![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/019.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510461&idx=1&sn=c194bbd73a249334e592c6b03e1f9672&scene=21#wechat_redirect)

Anthropic 创始人最看好的领域，AI for Science 深度解读

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/020.png)

[![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/021.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510411&idx=1&sn=b73b9ab225cd33abbe434a2934ef3ad3&scene=21#wechat_redirect)

AI 影响最大的行业？LLM 如何让教育产品化

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/022.png)

[![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/023.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510331&idx=1&sn=eb059cae85eb79d8b433973d9eff3ba6&scene=21#wechat_redirect)

Anthropic 联创：机制可解释性的秘密

![](../images/2024-12-10-ai-coding-zui-quan-tu-pu-agent-jiang-ru-he-dian-fu-ruan-jian/024.png)
