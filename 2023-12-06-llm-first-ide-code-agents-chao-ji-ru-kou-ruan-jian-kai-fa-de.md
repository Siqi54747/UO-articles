---
title: LLM-first IDE：Code Agents 超级入口，软件开发的“Excel 时刻”
publish_date: '2023-12-06'
publish_timestamp: 1701864618
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/G9lxBql1HNmRocd-0kv4vA
msgid: 1000000238
appmsgid: 2247505717
itemidx: 1
digest: 差异化功能的实践是 Code Agents 的试验田
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxqfUtDErrZYeniaHdlgelfchiaTjQs3qzm92KSu3SS9zicaOOfTqPuLwMDZHcECF9hE27wv2at2W1QA/0?wx_fmt=jpeg
image_count: 49
archived_at: '2026-04-20T01:55:20+08:00'
---

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/001.gif)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/002.png)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/003.jpg)

作者：NCL

编辑：Siqi

排版：Scout

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/004.png)

在《[AI Agent 的千亿美金问题](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504973&idx=1&sn=603596db2a31e1e53d71ac05d775cb7c&chksm=ce9b6bd3f9ece2c577720045239314840757fa578587f4a5adbf21e18a9dadd6bf1af3913b61&scene=21#wechat_redirect)》一文中，我们提出，目前 Agent 实践中，Code Agent 最有可能快速落地，作为开发流程中覆盖最广的工具，IDE（Integrated Development Environment）不仅是开发者的超级入口，也有机会完整地收集到测试、环境配置和 Debug 等环节的复杂推理过程的重要数据信息，因此，**是最有机会、最早能够出现 Coding Agent 的场景。**

**Excel 的出现让数据库使用变得“民主化”，通过更加友好的界面、内置图表公式等工具，让非技术用户也能轻松进行数据的存储、管理和分析。我们相信，在 LLM 的推动下，软件行业也会迎来“Excel 时刻”：**LLM 融入 IDE 后，入门级开发者甚至非技术背景用户也能够更好更快地实现程序编写，用户在代码编写中调用各种 LLM-based 服务、Code Agents 就像在 Excel 里用使用公式一样简单。

因为流量和产品先发优势，IDE 目前几乎是被 Visual Studio 和 Github Copolit 联盟所垄断，Tabnine 、Codeium、Cursor 以及 CodeWhisperer 等 LLM-first IDE 团队则试图基于 LLM 提供更具差异化的用户体验挑战突破 Visual Studio 和 GitHub Copilot “统治”，这些差异化功能的实践是 Code Agents 的试验田。

因为模型能力层面上的拉平，挑战者们中短期内想要突破 VScode 和 GitHub Copolit 市场占领的难度极高， LLM-first IDE 赛道当下最核心的价值在于 LLM Agents 的实践，我们相信，在赛道的充分竞争中，Code Agnets 生态一定会不断丰富，值得保持长期关注。

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 为什么关注这个赛道

02 现状：微软帝国的裂痕

03 挑战者：LLM  新浪潮下的暗流

04 结论

**01.**

**为什么关注这个赛道**

我们在《[AI Agent 的千亿美金问题](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504973&idx=1&sn=603596db2a31e1e53d71ac05d775cb7c&chksm=ce9b6bd3f9ece2c577720045239314840757fa578587f4a5adbf21e18a9dadd6bf1af3913b61&scene=21#wechat_redirect)》一文中做出判断，目前 Agent 实践中，Coding Agent 最值得期待，不仅最有可能快速落地，且有很大潜力成为人类所有 Agent 交互中的“翻译官”。作为开发流程中覆盖最广的工具，IDE（Integrated Development Environment）不仅是开发者的超级入口，也有机会完整地收集到测试、环境配置和 Debug 等环节的复杂推理过程的重要数据信息，因此，我们认为 IDE 是最有机会、最早能够出现 Coding Agent 的场景。与此同时，我们也观察到，一批 LLM-first IDE 公司试图基于 LLM 提供更具差异化的用户体验，去挑战过去被 Visual Studio 和 GitHub Copilot “统治”的 IDE 。

**趋势一：IDE 是开发者的超级入口，LLM 为 IDE 的商业化带来新机遇**

**IDE 是开发者的超级入口。**大多数 DevOps 的使用都需要先在 IDE 中编写、Debug 后，再提交到各类 DevOps 里进行各种自动化和集成，包括测试、部署和监控等流程。以测试为例，传统测试中需要人力撰写多种测试代码和环境，这通常在 IDE 中完成；其中重复性高的部分已被 AtomicJar 等 DevOps 公司抽象化，还能自动为客户提供测试图表和报告。

**DevOps 的市场初具规模，而作为超级入口的 IDE 却商业化堪忧。**根据 Global Market Insights 和 Markets and Markets 的研究数据， 2022 年，全球 DevOps 总收入规模在 80-100 亿美元左右，并正以每年 20-30% 的增速增长，而作为超级入口的 IDE 却商业化堪忧，**主要原因是市占率占比最大的 Visual Studio 坚持开源和免费路线，VS 的免费策略让大部分竞对只能被动跟随、难以开展商业化，整个赛道中几乎只有 Jetbrains 能获得较可观的收入，**通过 Pycharm 和 IntelliJ 两款明星产品，Jetbrain 吃下了 IDE 市场 18% 份额, 2022 年营收规模为 4.9 亿美元左右。可以看出作为超级入口的 IDE 占整个 DevOps 的份额并不大，面临商业化能力疲软的局面。（**拾象注：**份额估算部分参考了 Top IDE Index ，该网站在 Google 的搜索频率基础上来推理出各家份额，也有观点认为 VS 系列产品的市占率在 70%，但该数据引用可靠度偏低，暂不采用。)

💡

Jetbarins 创立于 2000 年，旗下拥有一系列 IDE 工具，其中最出名的 IntelliJ 和 PyCharm 分别为 Java 和 Python 开发设计的 IDE 产品，Jetbarins 的商业化主要来自 IDE 工具及商店抽成。

**而 LLM 的到来也许会为 IDE 这一超级流量入口带来新的商业化途径、改善 IDE 商业化现状。**文本场景入口的 Notion 通过 Notion AI 仅用短短几个月的时间便成功实现了数百万美元的 ARR ；Google Workspace 最初依赖廉价的云盘空间作为商业化方式，而如今则有望通过 Bard 的增值服务提高这数亿用户产品的收益潜力；此外，微软通过将 GitHub Copilot 引入 VSCode 这一庞大的开发者渠道，在产品正式上线的 18 个月内，就实现了 1 亿美元 ARR。

**趋势二：IDE 是探索 LLM 复杂推理能力的最好场景，LLM 能力边界逐步从代码补全渗透到代码重构、测试、Debug 和分析等高价值环节。**

**GitHub Copiliot X 引入 GPT-4 后，由于能为模型提供更完整的代码、环境和反馈信息，不少用户认为，类 Copilot 在代码重构、测试、Debug 和分析等高价值环节有很大的潜力。**Github Copilot 在 2021 年 10 月初次推出的时，其能力是基于 120 亿参数量的 OpenAI Codex 模型，擅长以较低延迟推理出质量不错的代码，尤其适合代码自动补齐功能，到今年 3 月，Github 推出的 Copilot X 则引入了 1.8 万亿参数的 GPT-4，在 GPT-4 的支持下，用户将代码、环境和反馈信息结合指令输入后，模型能在开发过程中的各个子环节都有亮眼的表现，Copilot X 从初代的代码自动补齐渗透到更多开发环节中。

**早期 Copilot 采用的 Codex 只能覆盖属于只能覆盖 Code 和 Create 部分需求，而这类需求只占到预算份额的 3.8%，而随着 GPT-4 等更强力模型的发布，其能力能逐步渗透到整个内容工具 18%。**DevOps 可以简单拆分成流程工具和内容工具，流程工具主要用于自动化和优化软件开发和部署的过程，内容工具主要用于生成文档、任务、报告或图片等内容。Redpoint 的合伙人 Sai Senthilkumar 调研了 60 位来自有 500 位员工以上的中大型公司的  DevOps 负责人，对各个类型 DevOps 的预算份额进行总结（如下表）。**随着 GPT-4 等后继新模型的能力增强，配合上 LLM 应用的演化，我们预计传统内容工具背后的算法将逐步被 GPT 模型这样的通用模型替代、覆盖改板块 18% 的预算份额。**

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/005.png)

*Source: Redpoint Partner Sai Senthilkumar*

**趋势三：软件开发将迎来“Excel 时刻”，而 IDE 则是巨变的关键入口**

**当 LLM 能力迅速迭代不断降低开发门槛，我们一定会迎来开发者数量的迅速增长。**知名的开发者社区 Stackoverflow 在 ChatGPT 推出后，首当其冲地受到冲击、流量明显下滑，除了 ChatGPT 之外，LLM-first IDE 也正替代 Stackoverflow、甚至提供比 Stackoverflow 更好的开发体验，更是成为 LLM 正逐渐成为新手开发者学习和纠错的首选工具。真正的学习通常需要犯下大量的错误并从中吸取经验，而 LLM 以其卓越的能力，帮助新手深入理解编程概念，提供实时的建议和指导，助力他们战胜编程学习过程中的挑战和困惑。此外，Github 也发现代码新手更容易接受 Copilot 的建议（如下图），他们将显著受益于 LLM 的普及。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/006.png)

Excel 是数据库使用的“民主化”。和需要专业编程知识和复杂查询语言的数据库相比，Excel 首先提供了一个用户友好的界面，使得非技术用户也能轻松进行数据的存储、管理和分析，其次，在处理小规模数据时，Excel 的内置图表、公式等数据分析工具极大地简化了数据处理过程。虽然数据库在处理大规模、复杂数据时更具优势，如更高的处理效率和数据安全性，但 Excel 在财务分析、小型项目管理等场景中仍显示出其独特的适用性。

我们认为，**在 LLM 的推动下，软件行业也会迎来类似于“Excel 时刻”的转变**。毫无疑问， IDE 充当的正是一个用户友好的“界面”，在 LLM 的辅助下，各行业的非技术人群能为自己的工作编写小程序，调用 LLM 功能、Code Agents 就像如今人们在 Excel 里用使用公式一样简单。

**趋势四：轻量程序的开发流程再革新，对需求描述和测试的 AI Agents 市场将涌现，而 IDE 有望成为 Agents 的分发平台**

传统的开发流程是编码完成后再进行测试，这一流程意味着开发人员直到项目晚期才会发现漏洞，也因此漏洞带来的影响范围、解决漏洞的成本相应提升，近年流行的 TDD(Test-Driven Development) 则在项目早期就花大量精力设计测试，确保每个功能从一开始就经过严格测试，从而保证复杂的长期项目更稳定。

但在相对轻量的编程程序中，**开发者们通常偏好直接编码，在这一过程中，LLM 则可以用于辅助生成需求描述和测试，以确保再使用的上手简易性和稳定性。**比如，大部分人在使用 Excel 公式功能时，都通常不会为公式编写详尽的说明，这造成了再次使用时的摩擦；更不会写详尽的测试案例，导致报表有时会因为数据类型等问题报错。

‍

**编程的高复杂度会带来巨大的再使用摩擦和稳定性考量，涌入的编程新手意味着对 LLM **Agents 的海量需求******，IDE 则能成为 Agents 的分发平台。**由于轻量软件所涉及的编程语言和代码库远复杂于 Excel 公式语法，这意味着巨大的再使用摩擦和稳定性难题，毕竟同样的代码在切换电脑时报错是极为常见的问题。这就需要 LLM Agents 的协助，帮助他们将根据代码生成需求描述和测试（如下左图），甚至是自动帮用户优化/Debug 代码（如下中图）。若不少 Agents 能充分证明自身的独特性，如擅长 Python Numpy 库或 JS VUE， 这时将会出现 LLM Agents 平台，而 IDE 作为开发者的超级入口则能顺势成为 Agents 的分发平台。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/007.png)

**02.**

**现状：微软帝国的裂痕**

GitHub Copilot 是现阶段 IDE 场景下的绝对头部。根据 The Information 今年 10 月的报道，GitHub Copilot  目前拥有 100 万付费用户、达到了 1 亿美元 ARR，GitHub Copilot Business 版本在今年 3 月时只有 5000 个企业使用，但到 6 月底这一数字就飙升到了 20000 个。GitHub CEO Thomas Dohmke 也极其乐观地表示，GitHub Copilot 在未来将会覆盖 1500 万开发者用户，从而为世界带来 1.5 万亿的 GDP 增量。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/008.png)

Thomas Dohmke 的底气来自于 GitHub Copilot 在用户侧的出色表现：**目前 Copilot 用户已有 46% 的代码由模型生成，能让这些用户节省 55% 的开发时间；Copilot 建议代码接受率在 30%以上 ，并在用户上手半年后能提高到 36% 左右。**Thomas 预计，在未来， Copilot 将撰写 80% 的代码，而程序员能将主要精力和思考花在系统设计和剩下的 20% 关键代码上。

下图为 GitHub 对 2000 位用户所做的客户体验洞察，可以看到，GitHub Copilot 不仅在效率提升上表现优越，也显著改善了用户的开发体验的满意度。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/009.png)

*Research Source: Quantifying GitHub Copilot’s impact on developer productivity and happiness*

**GitHub Copilot 强势增长的背后是“微软联盟”带来的综合优势：**IDE 里近 40% 市占率 的 Visual Studio 系列产品、拥有最强 LLM 模型的 OpenAI ，以及还有多年代码生成产品积累的 GitHub Copilot 三者同属于微软体系。VS 作为强势渠道为 GitHub Copolit 带来绝对的流量优势，OpenAI 则是 Coding 服务表现的基础保障，GitHub Copilot 不仅受益于前两者，其多年来在产品和用户上的积累也会推动自身的增长飞轮。

**GitHub Copilot 的产品壁垒首先建立在它和 Visual Studio 的深度整合上，VS 在其前端 UX 上给 GitHub Copilot 预留了多个专属功能，在 VS 的庞大流量滋养下 GitHub Copilot 成长迅速。**

**早期， GitHub Copilot 的成功离不开前端交互方式的创新。**早期 Copilot 的产品负责人 Alex Graveley 在当时创新地提出了代码自动补齐的交互，即“根据前文内容，不断地跳出代码建议，如果用户认同则在摁下 Tab 后就能填入建议”。这样的多行代码补全是当时 VS 无法做到的，在微软出面牵线下， VS 团队为 GitHub 开发了 InlineCompletionProvider 这一 API，从而让用户在 VS 中就可以使用代码补齐，而这个 API 为 Github 带来的效益也相当亮眼，GitHub 前 CEO Nat Friedman 在 2 月份的 Jasper Conference 上透露，**这样全新的 UI 在内测时表现亮眼，产品的终生留存率超过了 65%。**

**为了巩固 Github Copilot 的壁垒，VS 还违背开源和 Extension 友好的初衷，持续为 GitHub Copilot 优先推出多个专属 UX API。**尽管在开源精神下， VSCode 在后期将专门为 Github Copolit 开发的 InlineCompletionProvider API 公开， VSCode Extension 市场里有几个不错的 Copilot 挑战者，如 Tabnine 和 Codeium，都调用了这个 API 来达到实现类 Copilot 的代码补全效果，但为了巩固 GitHub Copilot 的地位，微软和 Visual Studio 的资源倾斜相当明显：除了 Visual Studio 官网主推 Github Copilot（如下图），VS 团队还继续为 Copilot X 专属开发了 UX API，比如 in-editor Chat 和 ChatView 等，并且这些 API 短期内都不会开放给其他产品/开发者。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/010.png)

In-Editor Chat 能让用户方便地选取一段代码后，让 GPT 提供更针对性的帮助，如下一图。Chat View 则让用户直接在 IDE 里直接向 GPT-4 询问代码问题，它可以自动读取相关的代码文件，而不用复制并切去 ChatGPT，如下二图。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/011.png)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/012.png)

尽管 GitHub Copilot 利用 VSCode 的专属 UX API 和渠道优势几乎垄断了代码生成市场，但我们认为，GitHub Copilot 自身的产品壁垒可能并不深，也存在一些问题，而这些都留给了挑战者们增长窗口期：

**1. Github Copilot X 的核心能力来自  LLM 的技术壁垒， Github Copolit 并不能独占模型能力。**

Github 最新推出的 Copolit X 底层是 GPT-4，尽管背靠微软让 Github Copilot 能够获得 OpenAI 最新模型的内测资格，但这一优先权并非独家，类似 Codium、Cursor 等优秀的初创公司也能在新一代模型正式发布前期参与内测。这意味着，在测试、Debug 等高价值环节，Github Copilot X 并不能提供性能上的明显优势。

Github Copilot 的代码补齐（Code Completion ）是基于OpenAI CodeX 模型实现的，在今年 6 月更新后，最新一代模型能够在更长的上下文里更智能地选取相关的上文进行推理，从而将用户代码接受率从 30% 提升到了 36% 左右，此外，模型的延迟也下降了 13%。

但我们认为，CodeX 这样的小模型也并不能让 GitHub Copilot 建立自己的壁垒：首先， GitHub 一直都没能像 OpenAI  GPT-4 那样拿出碾压全场的测评比分，反而多个竞争对手（Tabnine 和 Codeium）都拿出了各个场景的测评，证明自身产品能力和 Copilot 的差距不大；此外，随着 Llama，Mistral 和 Falcon 等开源中小模型已能在各种测评集里挑战 GPT-3.5 的性能，我们认为 OpenAI CodeX 已经很难帮助 Github 在代码补全这样的小模型上建立明显的护城河。

此外，因为 Github 严重依赖 OpenAI 的模型研发能力，导致 Code Completion 的模型没有及时更新训练集，并对于上下文窗口的利用能力不高。首先，Github 团队目前并没有展现出自己训练小模型的能力，仍需要微软牵头让 OpenAI 团队匀精力到这个模型上，导致 Copilot 的模型更新频率不高，模型目前甚至不知道 Langchain 这样爆火的项目，导致生成效果不佳；此外，目前 Github Copolit 团队还没有用向量数据库来协助模型找到最相关的代码块，这样能充分利用有限的上下文窗口（Code Completion 模型通常在 2000 tokens），以达到更好的生成效果。

**2. 数据安全和合规性上存在纰漏：**

尽管 Github 明确表明会保证零数据留存，并在传输过程中进行加密，但是这些安全承诺并没有经过第三方机构的认证，根据 Github 的 FAQ 内容， Github Copilot 预计要到 2024 年 5 月才能完成 SOC 2 这样行业通用的安全认证。

**Github 在训练模型时并没有清除未经许可或特殊许可的代码，包括 GPL，LGPL 和 AGPL 的代码。最直接的例子是 Copilot 会直接生成 ffmpeg 的代码片段，而这显然是有合规风险的。**在 Twitter 上，也有不少用户抱怨 Copilot 的灰色行为，比如 Tim Davis 就怒斥 Copilot 使用了他版权保护的 CSparse 库，也有用户深扒了 Github Copilot 的用户协议，发现**用户将需要自己确保生成代码的法律合规性。**

数据安全和合规上的短板会让用户有极大概率选择放弃 Copolit，在 2024 年 5 月 GitHub Copilot 完成安全认证之前，新一代 LLM-first IDE 团队则可以积极利用该时间窗口期拓展用户，尤其是看重数据安全与隐私的企业侧客户。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/013.png)

**3. 企业级功能并不完善：**

除了数据安全上的短板，GitHub Copolit 也尚未提供分析面板、模型个性化套件和权限管理等企业级用户常用的功能上。

例如，企业通常都需要通过分析面板来评判工具是否有实现预期的能力，而 Github 仅给最大的几个客户提供使用情况分析，而不会提供像下图一样的实时分析面板。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/014.png)

*Codeium 产品面板*

和 LLM 类似，出于性能、成本和合规等考虑，企业客户对 Code Completion 的 Fine-tune 需求也很旺盛。**具体来说，大多数企业通常希望能利用好自己的专属数据**，比如，Google 内部会有大量优质内部工具或优化 TPU 性能的代码，显然 Fine-tune 后模型能力会有质变；专属数据也允许模型能用更少的参数就能获得类似的性能，这将带来更低的推理成本、延迟；在严格的监管环境下，处理敏感数据的企业可能需要对其模型进行微调，以确保其尊重隐私要求，遵守内容准则。

**既然模型是数据的一种压缩形式，在理想情况下，模型的权限管理要求应接近数据的要求，所以权限管理和私有化部署是一个常见需求。**比如，一种方式是通过管理不同部门的人能接触不同版本的模型，并记录下每个用户使用 Log；而有更极端数据安全要求的公司，也会寻求私有化部署模型的方案。但目前 Github Copilot 并没有推出这些功能。

总之，尽管 VSCode 和 Github 在微软的统筹下，已初步垄断了 LLM 在开发者超级入口 IDE 的应用，但是目前也有许多初创公司注意到了微软帝国的裂痕，打算在这个充满想象力的市场里能占据一席之地。

**03.**

**挑战者：LLM  新浪潮下的暗流**

**尽管 Github Copilot 目前拿走了市场的主要声量，但仍旧有不少挑战者初露头角，值得我们关注。**Stackoverflow 在 2023 年 6 月份发布了其年度开发者报告，其中最流行（下图1）和最受好评（下图2的红点）的 AI 工具毫无疑问都是 GitHub Copilot，但与此同时，我们也看到很多新名字上榜、并且成绩不俗：Tabnine 已经拥有较为可观的用户基数，Codeium 则已经在较小的用户群体（下图2的蓝点）里取得了极高的评价（下图 2 的红点），CodeWhisperer 依靠AWS 的背书和渠道，也有不错的用户基数和评价。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/015.png)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/016.png)

我们可以把 VS 和 Github Copolit “微软联盟”的挑战者们划分为两大类：“模型+Extension”和“模型+IDE”。前者更适合在中短期内通过类似 GitHub Copilot 的形式，通过 VSCode Extention 和现有渠道结合来捕获客户心智，而后者则尝试通过交互和 UI 上的创新，在中长期里探索下一代开发体验。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/017.png)

从差异化角度，我们则可以从底层能力（模型）和产品（交互、辅助工具和 Coding Agents ）来看，其中：

**1）模型能力：**

各家几乎拉平，但在模型服务上，Codeium 和 Tabnine 做得要比 Github Copilot 好；

**2）产品：**

• 用户交互（UI/UX） ：Github Copilot 凭借 VSCode 所提供的专属 UI API 在触达用户上有一定优势，但目前 LLM 的功能发掘仍在早期，留给初创公司进行创新的空间还很大；

• 辅助工具上主要是 Prompt Engineering 和 RAG 系统的搭建，但目前还没有一家公司有明显优势；

• Coding Agents：Agents 是我们认为长期可以拉开仍处于行业早期，Cursor 和 CodiumAI 目前有一些不错的小尝试，但没有一家公司有明显优势。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/018.png)

**需要强调的是，Github Copolit 背靠 Visual VSCode 躺在流量富矿之上，新玩家们目前主要通过 PLG 的方式实现增长，短期内要超越 GitHub Copilot 还需要 GTM 角度的非凡策略和卓越表现。**

**模型**

在后端模型侧，行业的主要选手都倾向于选用两套模型：

• 一个中小模型（10-40B 参数）进行代码补齐任务；

• 另一个针对复杂任务的模型则主要借助 GPT-4 或 Claude-2 等大模型来实现。

由于大模型的头部领先优势较为明显，并且生态开放程度高，所以主要选手都调用 GPT 或 Claude 等头部模型的 API，但在中小模型环节，正如我们在前文中分析的，OpenAI 为 Github Copilot 开发的 Codex （以及后续更新）优势并不明显，并有多个开源模型证明自己模型已追上 GPT-3.5 能力，**所以现阶段初创团队通常选择自研、或基于开源模型进行继续训练。**

**虽然从模型调用上各家无法真正拉开差距，或建立独特壁垒，但在模型服务环节，则有机会真正拉开差距。**

我们整理了多家开源和自研代码的中小模型的代码生成测试成绩，其中 Code Llama 34B 的多个变种在代码任务上能超过 GPT-3.5，甚至在一些理想条件下能接近 GPT-4，而 Github 先前采用的 CodeX 则早已没有什么性能优势。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/019.png)

*测评参考：https://paperswithcode.com/sota/code-generation-on-humaneval)*

此外，**由于 OpenAI 为了最小化训练和推理成本，可能将代码生成任务交给 GPT-3.5，所以 Github Copilot 的竞对除自研外也可以调用 GPT-3.5 API。**OpenAI 在 2023 年 3 月份宣布了将推荐先前 Codex API 的用户逐步转向 GPT 3.5-Turbo（根据上表来看 GPT3.5-Turbo 的性能的确有显著的提升），因为代码数据能提高模型的推理能力，而文本数据能提高模型理解用户意图的能力。此外，由于推理服务器通常能通过同时服务数十个请求来摊低推理成本，所以整合文字和代码的推理请求后，**GPT-3.5 Turbo API 等成本大概率能做到比大多开源模型更低，以带来性价比优势。**

就像前文中说的，**Github 代码补全模型服务环节的主要问题在于数据安全和合规性上存在纰漏，并且仍无法提供各种企业级需求，而挑战者们正积极抓住这个机会：**

• Tabnine 和 Codeium 都已完成 SOC2 数据安全认证，并在训练数据中尽力去除了未经许可/特殊版权保护的代码库。

• Tabnine 和 Codeium 都允许用户将模型部署在自有服务器，满足用户对数据安全的需求。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/020.png)

• Tabnine 和 Codeium 都允许用户自有的代码库对模型进行 Fine-tune，不过 Codium 所提供的模型管理面板功能更全面，而 Tabnine 则只能联系团队定制。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/021.png)

由于以上需求大多为企业级场景，因此我们认为在几乎同样的模型能力下，**主打 Enterprise 的代码补全公司有局部市场机会，而在 to C 场景下，市场将继续由 Github Copilot 领跑。**这是因为 Github Copilot 凭借 VSCode 渠道优势和 Github 的品牌效应就能俘获大多数用户的心智，**而 toC 市场的挑战者必须要在 UX 上有明显创新才能拥有自己的一席之地。**

**产品**

[Perplexity](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503155&idx=1&sn=ce93d9e4476ca641d2c5f1283d4ef563&chksm=ce9b72adf9ecfbbbc90a551840965531cb8174620b4bbc31a6d03489c70bf3e611a3cca64bf6&scene=21#wechat_redirect) 以其出色的 Prompt Engineering 和 LLM Agents 设计，在搜索这个被 Google、Bing 等大厂占领的场景突围，所以我们认为，在 Coding 领域，初创公司也有机会能通过 Prompt Engineering 和 LLM Agents 挖掘出更多 GPT-4 的潜力从而给到用户更好的使用体验、形成新一代产品心智。

Anshul Ramachandran 在其 *How to Make AI UX Your Moat* 文章中提到，LLM 产品的 UX 护城河能在三个方向逐步建立，分别是：

• Presence：将 LLM 尽可能的嵌到现有的 UI 和 工作流中；

• Praticality：当 LLM 已经嵌入工作流后，在相同任务或问题解决上，即便明明大家都用的是 GPT-4 API，用户仍旧能明显能感觉到一家的生成内容比其他家更优质（例如格式/内容实时性/易用性等）；

• Power：指的是用 LLM 做竞争对手或传统技术下没有的功能，直接在功能丰富度上与对手竞争。

**Presence**

Presence 指的是先将 LLM 尽可能地嵌到现有的 UI 和 工作流中，这里主要涉及到的是 UI 创新。

IDE 入口中，**VSCode 的前端界面基本成为了行业的通用标准**，Cursor、Google Project IDX、AWS Cloud9 和 Codestory 都采取了类似的界面。这种前端界面通常由 Activity Bar、Primary Sidebar、Editor、Secondary Sidebar 以及 Status Bar 等几个组件构成（如下一图）。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/022.png)

Github Copilot 主要是在 Editor 部分加入了 Code Completion 和 In-Editor Chat，并在 Primary Sidebar 加入了 Copilot Chat 。值得指出的是，VSCode 目前仅允许 Github Copilot 在 Editor 界面弹出 In-Editor Chat 窗口，而其他产品则只能在 Primary Sidebar 显示 Chat 界面。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/023.png)

为能和 Github 竞争，这些挑战者们在 UI 上进行了多处创新：

**• Copy to Chat：**

将 Chat 融入 IDE 首要的好处是能快速向 Chat 导入代码段。比如 Cursor 就在 Editor、Terminal 里允许用户快速导入代码段到 Chat 中，并小心处理回车和前置空格。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/024.png)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/025.png)

**• Context Provider @：**

为了绕过 VSCode 的 Restricted API，Cursor 选择基于 VSCode 开源代码自研一个 IDE，团队首当其冲做的功能就是复刻了 In-editor Chat，并基于此创新地引入了 @ 符号，类似 Notion、飞书等文档协作工作中已经普遍使用的 关联文档功能。在 @ 的功能下，开发者能够更准确地表述需求，例如，如果开发者想让生成的代码使用另一个文件里的特定代码段，就可以使用 @ 来选取相关文件（如下左图）。CodeStory 也有类似的功能，如下右图。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/026.png)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/027.png)

**• Quick Command：**

 Codeium 在 Editor 界面中加入了快捷键（如下左图），将一些常用功能用固定的 Prompt 方式交给模型，这不仅能降低用户 Prompt Engineering 的门槛，团队也能在模型训练过程中强化这些 Quick Command 的性能。Codestory 则参考了 Notion 中的 Slash（/） Command，将常用的指令能通过 / 调用（如下右图）。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/028.png)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/029.png)

**Practicality**

Praticality 指的是，在 LLM 已经嵌入工作流后，在相同的任务或问题的处理上，即便大家都调用的是 GPT-4 API，在底层模型能力拉齐的基础上，用户仍能明显能感觉到其中某个产品的生成内容比其他家更优质，这里的优质可以具象化为生成格式、内容实时性、易用性等细节，本质上则是不同团队在 Prompt Engineering 和 RAG 的优化上的能力体现，Praticality 也是不同产品团队对用户洞察能力的体现。

**1）Prompt Engineering：**

一个优质 Prompt 通常包含以下三个组件：

**• Command：**

用户的指令和任务，可以提示并辅助用户填入更明确的需求。比如更追求计算高效还是内存高效，函数名是否要确保符合命名规则等，是否要尽量用调用上下文的其他函数等。

**• Constraints:**

收集用户偏好设置后，在每次任务中自动导入。这类似于 ChatGPT 的 Custom Instructions，用户能输入自己的编程背景，更偏好 GPT 在哪些生疏的语言里配上更详细的注释，同样的功能更偏好用什么语言和包完成。

**• Context:**

从代码库和企业知识库中，提取出和问题最相关内容；再结合系统环境和运行情况（如报错信息和 Log），在有限的 Context Window 中放入更高质量的信息。我们将在后文的 RAG 部分展开介绍。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/030.jpg)

*类似这样的 Prompt 模版还有 RTF、Tree of Thought 等，暂时不做展开介绍。*

具体来说，尽管在 Codeium 的 UI 上仅有一个“Refactor” 词作为 Prompt，但是在后台真正输出给 GPT-4 的可能是下面这样的：

You are a software developer. You will be given a function as context, and are responsible for rewriting it according to a given set of instructions and constraints, and returning the rewritten function to the user. Make sure that the rewritten function is easily understandable by other software developers and add comments describing how the code works: <constraints><funciton code><context>

其中的 “Constraints”，可以学习 GPTs 设置过程中的引导对话，并从中提炼出用户的使用习惯和编程经验。比如问答之后，LLM 总结出了如下一段话。

<constraints>: I prefer compute efficient and robust code, so please vertorize the computation whenever possible. I am using 14700K+RTX4090+128G DDR6. The function naming should follow Google Style Guides. I am familiar with Numpy and Pytorch, so please use them whenever possible. I am currently using MinGW-W64 GCC-7.3.0 for cpp.

此时，UI 上还应该提示一些常见的代码偏好，进一步丰满 Constraints，让模型的生成效果更贴合用户需求，比如下面几条

A. add console log statement to make debugging easier

B. add print statement to make debugging easier

C. add comments and docstring to the code

D. add codes to reallocate memory

E. ...

**总之，仅一个 Refactor Code 的按键设计背后都需要复杂的系统工程，要先引导用户去丰满他们的指令，再导入用户的偏好和限制要求，协助用户稳定快捷地获取高质量的输出。**还有极为重要的部分是 RAG，自动找到相关的各种背景知识，在有限的输入窗口中放入更高质量的代码。

**2) RAG**

（该部分内容主要基于拾象团队 Cage 的内部研究)

尽管 GPT-4 在近期已成功将上下文窗口扩展到 128000 tokens，但是出于成本和延迟的考虑，并且典型的 Code Autocomplete 模型的窗口仍限制在 10000 Tokens 不到，所以行业实践中，通常会通过 RAG 技术来作为 LLM 的辅助。

💡

RAG 技术指的是用各种搜索算法帮助模型从数据库中找到和用户请求较为相关的内容，用来提升模型生成内容的质量和个性化程度。

**语义搜索数据库的建立和维护通常有以下几个步骤（如下图），其中， TextSplitter 和 Embedding Model 的技术护城河重要性高于 Vector DB。**

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/031.png)

TextSplitter 通常被用来将长短不一的文档切割成合理的信息长度，以放入 Embedding Model 做索引。一个优秀的 TextSplitter 需要避免将较相关的上下文切到两端文本中，以避免重要信息丢失。

Embedding Model 则负责将文本段转化成向量，一个优秀的 Embedding Model 通常在分类、召回等任务中有不俗的表现。

（读者可以参考 Hugging Face 对各个开源 Embedding Model 的全面测评 https://huggingface.co/spaces/mteb/leaderboard ）

由于 Textsplitter 的切割效果对 Embedding Model 的效果测评有明显影响，而各家公司也能对开源 Embedding Model 进行 Fine-tune，所以**我们认为会有团队能在代码和文字混用的场景下围绕 Embedding Model 和 Textsplitter 建立起护城河。**

**此外，很多团队正在探索从单 Embedding Model 转向多 Embedding Model 做 Index，认为这将显著改善召回结果的性能和个性化程度。**根据  Hugging Face 的 Embedding Model 测评，目前还没有一个 Embedding Model 能够在所有任务中都能成为表现最好的，所以有很多团队提出用多个 Embedding Model 进行 Index。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/032.png)

在搭建 RAG 的召回流程上，行业目前的通用做法是用一个 Embedding Model 将 Query 和数据进行相似性比对，找出相似度最高的几个 Retrieved Contexts （粗排），这时再用 Reranker 模型对这些 Contexts 进行排序（精排），最后整合到 Prompt 中作为重要信息（如图1）。最近行业里正在将传统**搜索/推荐算法和技巧结合到语义搜索中：用户的 Query 先到各个 Vector DB 多路找出相关 Context 后再用 Reranker 模型进行排序（如图2）。**

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/033.png)

**现阶段，市面上的 IDE 代码助手在这方面的探索并不充分：**

• Github Copilot 在自己的技术博客中表示，他们目前只通过最简单的 Vector DB 找到相关 Context ；

• Codeium 是在所有团队中唯一在 RAG 上进行探索的，但 Codeium 的方式也只是多加一步 Reranker。

**虽然目前行业里通常认为语义搜索算法配合上关键词搜索的效果最好，并且即将成为主流选择，但我们认为 RAG 的技术路径还将继续发散，这套方法还有很大的优化空间，将显著增强相关性，减少延迟，并优化提示，我们相信，如果会团队能在 RAG 环节积累 Textsplitter、Embedding Model 和召回流程上的技术优化，就有机会在 IDE 代码助手上复刻 PerplexityAI 对搜索巨头的效果碾压。**

**Power**

**Practicality 的目标是在现有功能实现上给予更好的体验，而 Power 则是指如何基于 LLM 来实现竞争对手或传统技术下没有的功能，是从功能丰富度上与对手竞争，也正是这些功能开发实践会带来丰富的 Code Agents 生态，这是我们在今天关注 LLM 和 IDE 融合的最主要原因。沙盒环境的运用和 Agents 的搭建可能会成为这一环节的竞争关键。**

**OpenAI 推出的 Code Interpreter 解锁了 LLM 在沙盒环境自主运行代码的能力，Python 代码包生态的繁荣将为 LLM 提供近乎全能的工具箱。**Code Interpreter 的推出进一步让用户感受到 LLM 的惊人潜力，既能用数学代码库大幅提升了模型的复杂运算能力和可靠性，又能凭借 Python 丰富的代码库读写几乎所有常用的文件格式，还能给出精美的数据分析和可视化图表，这让宾大的副教授 Ethan Mollick 都感叹，Code Interpreter 在很多复杂数据分析中出错的概率甚至比人类还低。

但因为 Code Interpreter 的沙盒环境由 OpenAI 负责托管在云端，出于安全和成本的考量，它不仅无法访问互联网、API 和数据库，且沙盒环境的设置自由度和运行时间受限，云端托管也让用户上传的各类文件还会有泄密的风险。而 Open Interpreter 则允许 LLM 使用本地电脑或服务器上的沙盒环境，从而转嫁了成本和安全风险。

💡

**Open Interpreter ：**

 实现 OpenAI Code Interpreter 效果的开源代码，今年 9 月上线，Open Interpreter 可以让 LLMs 在本地运行代码（比如 Python、JavaScript、Shell 等）。安装后，在终端上运行即可通过类似 ChatGPT 的界面与 Open Interpreter 聊天。

在 IDE 环境中，LLM 通过 Open Interpreter 自我测试代码，不仅提高了准确性和自动化程度，还通过利用 Python 的丰富生态系统，满足了更广泛的需求，并降低了针对不熟悉的代码库的学习成本。同时，LLM能够获得系统级的上下文信息，大大减少了用户在管理代码环境方面的精力和学习成本。

**Open Interpreter 所消耗的 Token 数需求比文案多两到三个数量级，促使代码场景的客单价可能远超文案，从而弥补代码人群大幅少于文案人群的质疑。**Open Interpreter 通常会在多步思考里导入大量的上下文、系统和报错信息，还要用大量的空格和符号维护详细的代码结构，所以 Open Interpreter 的成熟将为 GPT 带来天量的生成需求。比如 Reddit 上的 jaimito 是一位前端工程师，**他仅仅用了 1 小时就为 GPT-4 API 支付了 10 美元**，而这在文案场景下通常够用 1 个月。

在《AI Agent 的千亿美金问题中》，我们提到，LLM Agent 和 LLM- Based 应用的显著差异点主要体现在：

• 合作机制（ Orchestration）：存在多模型、多 agent 分工与交互的机制设计，能实现复杂的工作流。

**•**环境交互 （Grounding）：Agent 能理解自己的不足，并适时从外部寻找合适的工具解决问题。

个性化记忆 （Memory）：能记忆用户偏好和工作习惯，使用越久越了解用户。

• 主动决策 （Decision）：Agent 有能力在虚拟环境中探索、试错、迭代。

**不难发现，当 LLM 熟练掌握沙盒环境的运用能力，配合上 GPTs 带来的模型个性化普及，结合前文提到的 RAG 技术的成熟后，我们认为惊艳的 AI Agents 将逐步涌现。**

**CodiumAI 为代码测试开发了 Integrity Agent，致力于挖掘出潜在的代码漏洞。**Integrity Agent 会先找出文件中现有的测试，再利用 LLM 给用户建议数个多个潜在问题点，再生成用户感兴趣的测试并导入现有测试代码的边上。Integrity Agent 使用了 TestGPT（为测试场景 Fine-tune 版本的 GPT-4），生成的描述会更符合常见测试需求的规整，而生成的代码则允许根据用户样例更贴合用户习惯。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/034.png)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/035.png)

**Cursor 在 Twitter 上火爆的原因之一是其 Auto-Debug 功能，致力于一键修复用户运行代码后的报错。**例如下图就展示了一个 Auto-Debug 功能：Cursor 从报错信息中得知你可能打错了文件名/文件路径，会主动用文件夹浏览工具扫描代码库，它要么会告诉你这个文件夹里没有此文件，或是建议另一个类似的文件名（可能是大小写错误）。

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/036.jpg)

由于我们仍处于 Agent 早期，尽管 CodiumAI 和 Cursor 的例子仅在 Orchestration 和 Grounding 上取得进展，我们已能初步窥探 LLM Agent 潜在的功能爆发。在这些功能配合上 UI 和小工具的辅助后，用户将能明显体验到和Github Copilot 的产品区分，并摆脱 LLM Wrapper 的质疑。

**04.**

**结论**

单纯从 IDE 工具角度来看，因为底层模型能力基本拉平，而用户体验上的努力是一个长期的过程，整个 IDE 领域可能在相当长时间仍是 VScode 和 Github Copolit 的主场，对于 LLM-first IDE 们而言，除了在用户体验和功能上做增量外，找到差异化的 GTM 策略也至关重要，例如我们在前文提到的抓住企业级需求，此外，考虑到 LLM 还带来新开出了发者的涌入，参考生产力软件中常用的教育策略，LLM-first IDE 也可以通过绑定新手开发者、培养新一代用户的 IDE 入口也是一种方式，例如 Replit 就曾尝试过和 CodeAcademy 等开发者学习网站合作。

虽然在 IDE 挑战者主题下，VScode 被颠覆挑战的可能性较低，但 LLM-first IDE 整个赛道对于行业来最大的价值在于 LLM Agents，我们相信 Code Agnets 生态会在整个竞争过程中不断丰富，因此，值得对赛道保持长期关注。

**Reference**

https://pypl.github.io/IDE.html

https://github.blog/2022-09-07-research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/

https://codeium.com/blog/code-assistant-comparison-copilot-tabnine-ghostwriter-codeium

https://github.blog/2023-06-27-the-economic-impact-of-the-ai-powered-developer-lifecycle-and-lessons-from-github-copilot/

https://www.freethink.com/robots-ai/github-copilot

https://cloudinfrastructure.substack.com/p/cloud-infrastructure-part-ii-devops?s=w

https://code.visualstudio.com/blogs/2023/03/30/vscode-copilot

https://www.reddit.com/r/OpenAI/comments/16hu7nr/open\_interpreter\_vs\_cursor\_ai\_anyone\_compared/

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/037.png)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/038.png)

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/039.png)

延伸阅读

[![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/040.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505656&idx=1&sn=63974aa43c18cea3857e3184569649d3&chksm=ce9b6966f9ece070aa01c039ab855cbb4cc8c4bc4d153187494be3b76dc903eb32e9101872ae&scene=21#wechat_redirect)

Filming Less：AI时代的视频剪辑产品淘汰赛

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/041.png)

[![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/042.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505606&idx=1&sn=babbb6632abe2776b6284bc8660e1620&chksm=ce9b6958f9ece04e3ea09b9acef703569a999aced2332c060cdce6721138bd75a0602eb10281&scene=21#wechat_redirect)

专访Pika Labs创始人：探索视频生成的GPT时刻

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/043.png)

[![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/044.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505540&idx=1&sn=fc36a6d08a7266df8ce520c8cf1bf50b&chksm=ce9b691af9ece00c555981d452202b7997d938b2d87d398c286856d0fd3f9e51b06ca3d3e60d&scene=21#wechat_redirect)

Mistral AI：欧洲最强模型团队，打造开源轻量LLM

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/045.png)

[![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/046.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505500&idx=1&sn=a4e443893c4f1a977fa240c65f12ffb2&chksm=ce9b69c2f9ece0d4b75914e979fdbc8e0ee32b9e1f935ed0db2ce27661cb919ac99f4762c4ee&scene=21#wechat_redirect)

2023独角兽市值分析：Gen AI的崛起与地域分布

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/047.png)

[![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/048.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505355&idx=1&sn=e8b1d121d20b3f275db936d81db1a009&chksm=ce9b6a55f9ece343098cca201e0fd7584b30858925ead37f0facd280f940e6dcf316dfcde703&scene=21#wechat_redirect)

Figure：为人类部署数十亿台人形机器人

![](../images/2023-12-06-llm-first-ide-code-agents-chao-ji-ru-kou-ruan-jian-kai-fa-de/049.png)
