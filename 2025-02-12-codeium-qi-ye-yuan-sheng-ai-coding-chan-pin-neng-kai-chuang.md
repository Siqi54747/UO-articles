---
title: Codeium：企业原生 AI Coding 产品，能开创 Agentic IDE 新范式吗？
publish_date: '2025-02-12'
publish_timestamp: 1739362987
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/POhx1GUGRXgmPVaKFAhNVg
msgid: 1000000324
appmsgid: 2247511347
itemidx: 1
digest: Github Copilot 和 Cursor 的最强竞争者
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgyEVIIHx8nicEVJuoBaB7oV3jgaemyfHvd9icJmkDDKPmW82ojqnjGW0j2mlo6a4Cxdp7vtYHhXrtJw/0?wx_fmt=jpeg
image_count: 31
archived_at: '2026-04-20T03:08:24+08:00'
---

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/001.png)

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/002.png)

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/003.png)

作者：Theodore、Cage

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/004.png)

美国企业开发市场的潜力巨大，目标用户群体相比独立开发者和科技大厂，技术能力更弱，更需要 AI 工具来提高开发效率，同时也比 citizen developer 市场的需求更加明确。Codeium 从 2022 年中就专注于满足非科技企业的复杂需求，确保其产品不仅适用于小型团队和SMB，也能适应大型企业复杂的环境和代码库。因此，Codeium 在安全性、合规性、个性化微调和部署服务上投入大量资源，力求在这些方面超越 GitHub Copilot 和 Cursor 等竞品，给企业客户更强的信任感。

去年 8 月，Codeium 完成了由 General Catalyst、Kleiner Perkins 等参与的 1.5 亿美元融资，估值来到 12.5 亿美元，是这些老牌基金在 AI Coding 领域下的重注。之后在 11 月 Codeium 正式发布了 Agentic IDE **Windsurf**，与 Cursor/Devin 进行差异化竞争。

Windsurf 找到了 Agentic IDE 平衡的产品体验，将开发者置于 “copilot” 的位置，把适合自动化的多步任务交给 Cascade 系统接管。根据用户反馈，Cursor 产品体验很棒，但开发者仍主导了开发过程；而 Devin 在处理复杂问题时成功率不高、人类难以介入帮助 agent。这一设计不仅更能促进产品经理等强动机、弱开发能力的 prosumer 用户增长，还可能让 Codeium 得以打开企业客户的预算空间 —— 企业不仅在购买开发工具，还可以有效替代一部分开发人员的薪资支出。当然，考虑到 GitHub Copilot 有很强的分发渠道，近期也推出了 agent mode，Codeium 需要保持在半年以上的产品和身位优势。

‍

**‍💡**目录 **💡**

01 产品分析

02 融资情况

03 创始团队：Dream bigger

04 商业化与客户采用

05 结论与猜想‍

‍

**01.**

**产品分析**

**Codeium**

Codeium 最早的产品形态为 **IDE 插****件**，能支持 40 多种 IDE（包括 VSCode、JetBrains 等）和 70 多种编程语言。他们的产品迭代速度很快，每个月都会发布新功能、UI/UX、性能、稳定性等方面进行的优化更新，已经逐渐覆盖了我们在 [AI Coding 图谱](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510746&idx=1&sn=c12a07bb6dfb69d1180d029bbd7c55be&scene=21#wechat_redirect)中涉及到的每一个工作流环节，包括代码补全、测试、审查、搜索等，并开发了自有的代码专用模型。插件主要由补全和对话两部分功能组成：

1. 补全：**Supercomplete** 是 Codeium 最新的补全能力，发布于 2024 年 10 月，**付费用户**可在 VS Code 中无限使用。通过实时分析用户意图，直接将光标导航到下一步的代码位置，并执行补全、纠错、编辑、删除等操作，**类似 Cursor 中通过连续点击 "tab" 键去预测并执行下一步。**其技术难点主要是如何降低延迟、微调专用小模型、压缩 context window 和 prompt 等。

根据 Gartner 在 2024 年 7 月的最新报告，Codeium 在代码生成、测试、现代化、解释等方面的得分已经全面超过了 Github Copilot。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/005.png)

2. **Chat 是经典的 Chat UI，**并列于 IDE 的右边栏；**Command (Ctrl + I) 是 in-line 编辑，**在 IDE 原有界面内，和 Cursor 的 **Ctrl + K** 快捷键特意做了差异化。两者都可通过自然语言指令生成、重构、debug、解释代码，询问相关问题，还可用于单元测试、文档生成等；对于 Chat 对话的上下文，可以自定义固定、引用**多个存储库**，或通过“@对象”进行引用。

Codeium 有多种聊天模型供用户选择，包括自有模型、开源代码模型以及第三方 API 。Command 使用的是专用于编辑任务的自有模型，效果比 GPT-4 更好，并且速度比 PT-4o 快 4 倍。自有模型版本的 Command 发布后，Edit 几周内使用量就增长了 250% 以上，并在超越 Generate 用例后保持了大幅领先；代码接受率也提高了 38%。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/006.jpg)

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/007.jpg)

除了插件之外，Codeium 还有两个相对独立的 feature：

1）**Forge** 是专用于代码审阅和 PR 工作流的 **Chrome** 插件，目前还在 beta 阶段，仅对企业团队开放，在 GitHub 云上可用。在 Forge 中，可以选中代码区域并进行解释，或就此向 Chat 提问；Forge 能自动生成针对评论的修改建议，以节省开发者和审阅者的沟通时间。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/008.png)

2）**Live** 是网页版app，于2023年11月上线，主要用于通用的疑难问题问答。能针对各种主要 IDE 和代码库的最新版本展开对话，并根据提供的上下文搜索开源代码片段和文档。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/009.png)

Codeium 强调自身产品的最大亮点在于强大的 **context awareness**，在所有任务中都会考虑临近文件，乃至整个存储库，并可以自定义固定上下文。其中最能显著展现上下文能力的用例是**企业级代码库的语义搜索。**

在 2024 年 8 月，公司推出了用于所有产品的推理引擎 **Cortex**（在 Windsurf 发布后改名为 **Riptide**），**基于自****己训练的代码专用 LLM，Riptide 能准确回答** **“****代码片段与输入查询的相关性有多大****”** **这个问题，**并在数百 GPU 上并行调用 LLM，针对不同的代码片段进行数千次推理，表现优于市面的 embedding model 和 RAG 系统，recall rate 是其他系统 3 倍；由于使用分布式计算，Riptide 的延迟极低，能在1秒内处理上亿代码，实现实时人机交互；只需6秒就能把单个代码更新应用到代码库中所有文件。

在隐私方面，Codeium 符合零数据保留政策和 SOC II 标准；且与 Copilot 不同的是，从不使用未经许可的代码（如 GPL）训练模型。对于付费用户承诺零数据保留，免费用户也可以选择设置不储存数据。用户拥有生成代码的所有权。

**Windsurf**

Codeium 不满足基于 VSCode 等传统 IDE 在 **UI/UX** 和信息收集上的局限性，开发了自己的 **IDE 产品 Windsurf**。产品不仅集成了 Codeium 插件的所有功能，支持 Codeium 的所有部署方式，更旨在**融合 Copilot 和 Agent 两种理念中找到一个平衡点**，以实现轻量化的丝滑工作流。团队表示构建 Windsurf 的初衷是他们相信，**AI Coding Assistant 的最终目标不只是提升开发者的生产力，而是实现创新，让用户做到以前无法实现的事情。**

团队在 Windsurf 中重新构想了 **AI Coding** 产品所必需和可以剔除的功能，实现了以下革新：

1）产品基于 **Flows 引擎，结合了 Copilot 和 Agent，能够深度理解代码库并实时感知程序员的操作，**从 UI、延迟等方面配合，实现真正的无缝、持续协作。下图中上方的灰色轴是人类开发者的任务，下方的绿色轴是 AI 介入的工作。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/010.png)

2）**协作代理系统 Cascade** (ctrl L) 从 8 月开始推出，以 Riptide 引擎为基础，11月被集成于 Windsurf。这个系统把传统 Chat UI 进化为了 **agent 系统，能进行主动的工具调用和迭代能力，**从而模仿开发者从检索、规划到执行的工作流程。这一设计扩展了上下文窗口，解决比单个 LLM 范围更大的问题。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/011.png)

Cascade 有 2 种协作模式：一种是 write，可以编辑代码，**自然语言交互门槛很低，对非编程人员十分友好，**可以用类似 Bolt 的方式一句话开始一个项目；一种是 read，可以与 AI 问答，In-line command 的 UI 设计减少了手动操作，不需要反复提供 prompts，就能自动迭代修正直到生成正确代码。Cascade 还能从团队的编辑行为中不断学习，积累团队特定的 **Trajectory understanding，**从而更好识别用户意图。

团队尽可能改善一切能提升开发者体验的细节，例如“从上次中断处继续”的记忆功能；多文件的代码审核中，能够在文件内部、之间跳转，快速接受/拒绝的 UI 界面等，都基于用户反馈进行了打磨。今年 1 月，Windsurf 发布了第二次更新，开始支持互联网实时信息搜索，可以获取开源项目的最新更新；如果使用公司 VPN，还可以将公司内网加入上下文。此外，Cascade 不仅能自动捕捉用户的使用习惯，还支持用户对其总结的记忆和默认规则进行自定义管理，加强了产品的个性化功能。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/012.png)

Cascade 自动生成的用户使用习惯记忆，可以进行自定义

在最新一次更新中，Windsurf 开始集成 DeepSeek R1、DeepSeek V3 和 OpenAI o3-mini 模型，是第一个集成 R1 的 coding agent。DeepSeek 模型完全托管在西方服务器上，向所有付费个人用户开放；o3-mini 向所有付费个人和组织用户开放。

公司博客写到，Windsurf 已经带来了可见的变化。**让 Coding 工作范围得以扩展到非开发人员：**产品经理、分析师、架构师、设计师等都能使用 Cascade 来理解或编写代码；Cascade 能解决更多的单元测试、迁移等**维护工作，让开发者更专注业务。小型初创公司也能使用 Windsurf 来构建自己的低代码工具，而不需要向外部 SaaS 采购。**

我们总结了来自 Reddit, X, 即刻等社群的用户反馈，将 Windsurf 与 **Copilot 和 Agent 两类产品中的 best player Cursor 和 Devin 进行了对比。**整体而言，**Windsurf 产品表现更 Agentic，上下文能力**及自动化表现好于 Cursor，且价格便宜，已能够替代**小型个人项目**对Cursor的需求。相比之下，Cursor 作为 Copilot 产品的代表，仍有最好的 **Autocompletion** 功能，能通过连续按 “Tab” 流畅快速地生成代码；同时产品成熟度胜于Cursor，稳定性、准确度、协作功能都更强，比 Windsurf **更适合中大型的团队项目。**

在另一端，**最为 agentic 的 Devin** 形态是 **Slack** **交互**，更能减少手动输入，适合用来处理工作中不想自己处理的繁琐任务；但对于细节的把握不如前两者。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/013.png)

**Enterprise solution**

Codeium 产品创始团队成员 Anshul Ramachandran 在 Latent Space 上分享了公司在企业端的方法论。团队**从构建产品的第一天开始，就想好要针对传统行业里的大企业。这是因为相比在红海争夺个人用户，企业才是软件的主要买单方，**赢得一个大企业客户的收益相当于成千上万的个人用户。而具备开发 DNA 的大型科技公司会更倾向于通过开源 LLM 和各种框架自建GenAI能力，而非向外采购。他们往往也**拥有庞大的 B2C 基础和分销渠道，**与之竞争难度大，机会少。

相反，**非科技型大企业非常愿意为提升效率、创造更多价值的工具买单。**同时，GenAI 的黑匣子使生成的代码更难追溯，也为这类企业带来更多复杂的安全、合规限制。相比巨头，初创公司可以更加快速、灵活地开发本地部署、审计控制等方案来满足这些复杂需求，从而脱颖而出。

Anshul 认为，一支仅面向消费级市场的开发团队，是无法通过后期补救来切入企业市场的。但 Codeium **在设计产品、组建团队时****都将大企业的需求置于核心：**要有先进的推理系统，才能处理企业内复杂庞大的代码库；打造具备深度技术专长的团队（如 GPU 优化、安全合规等），才能**实现 Enterprise Infrastructure Native。**文章中总结了团队正确关注到的 **6 个关键方面：**

• **安全****：**

Codeium 作为 SaaS 的云部署方案符合零数据保留政策和 SOC 2 标准，并提供**自托管/VPC、Hybrid**（即企业自托管数据，Codeium托管计算推理）的部署选项，**这是区别于 Copilot 和 Cursor 的最大优势** —— Cursor 仅提供承诺不存储数据的云方案，但不支持本地方案。Copilot 也不支持自托管，只在组织方案中默认不使用客户数据训练。**这点也得到了多名 Codeium 客户的认可，**尤其是在结合内部库自定义的场景中，客户对自托管方案更加放心。

在构建过程中，Codeium 进行了一系列技术准备，包括容器化部署（Docker、Kubernetes）；自建与客户扫描系统兼容的镜像扫描系统；确保能在 hyperscaler 和本地硬件部署上正常运行，合理调整 GPU 硬件来优化成本等。Codeium 也早早通过了多项耗时的隐私安全认证。

• **合规**：

**Codeium 主动展示了使用数据的合规性，**建立了训练数据的净化措施，并遵守 OpenAI 等第三方服务条款，**承诺永远不用未经许可的代码（如GPL）、ChatGPT 的生成结果和客户数据训练模型。**同时为企业提供归因过滤、归因和审计日志功能。

•**个性化**：

**基于企业客户的私有代码库进行推理，**在模型内评估数据的时效性和相关性，给出更高质量的个性化回答。Codeium 的本地部署方案能让个性化的实现更加安全，也是**相对于行动缓慢的巨头的最大优势**。虽然 Github 在 2024 年 2 月也在企业方案中推出了定制化功能，并在同年 6 月通过了 SOC 2 认证，但客户对其 SaaS 方案的隐私安全仍有顾虑。

• **ROI 分析**：

**Codeium 能受益于企业相信 AI coding 能提高生产力的普遍信念，**但产品的 ROI 难以量化。为此，Codeium 开发了**数据分析仪表盘**，能够对照分团队的使用数据，跟踪 Codeium 对其软件开发的直接影响，可视化客户效率的提高程度，并收集最佳实践。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/014.png)

• **延迟**：

Codeium 开发了基于 speculative decoding 的方法，生成尽可能少的 token；同时，公司**有 ML Infra 方面的基础和基因，对基础设施架构进行了性能优化，**可将 GPU 利用率提高至 97%，降低自托管客户的 TCO，并**在包括检索、推理、推断、检查的每个环节控制延迟。**

• **规模**：

**Codeium 从一开始**就考虑到企业环境复杂且规模庞大（如数以万计的代码库和开发人员），需解决大规模索引和延迟管理的问题。系统设计需在高用户量、高数据量的情况下保持高效稳定。对于新开发成员面对陌生环境的 onboard 过程，也能将所需时间缩短到 1/4。

****定价****

Codeium 发布后 2 年左右的时间内都对个人用户免费。从 2024 年 9 月开始，推出了 $10/月的 Pro Plan，相对免费用户提供更多次数的高级模型（Claude 3.5 Sonnet  GPT-4o）使用量、更快的完成速度及更丰富的上下文功能；12月开始，顺应 Windsurf 的发布，Pro Plan 涨价至 $15/月，并增加了 $60/月的 Pro Ultimate Plan。

目前方案中，免费用户可以使用基础模型 Cascade Base，第一次下载 Windsurf 会赠送 50 个 User Prompt（用于调用高级模型）和 200 个 Flow Action 积分（用于执行特定自动化任务，如代码审查、文档生成等）。

2024 年 12 月起，对于 50 人以内的团队，Teams Plan 从 $24/人/月涨价至 $35/人/月，相比个人版增加了组织分析、席位管理、远程/多存储库索引和代码审查 **(Forge)** 的功能，还包括每人 300 个 User Prompt 积分和 1,200 个 Flow Action 积分；多余的积分可以在用户间共享。Teams Ultimate Plan 定价 $90/人/月，包括无限个 User Prompt 积分和 2,500 个 Flow Action 积分。企业 SaaS 方案定价，需要客户与 Codeium 销售联系确认。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/015.png)

值得注意的是，在 Codeium 依靠涨价增收的同时，本就拥有强大销售渠道能力的 Github Copilot 却开始了价格战：Github Copilot 在 2024 年 12 月发布了免费版本，在 VS Code 中对所有用户开放，可在 GitHub.com 上使用。用户每月可获得 2000 次代码完成（相当于每个工作日约 80 次）及 50 次聊天请求，访问 GPT-4o 和 Claude 3.5 Sonnet 模型。个人 Pro 用户定价为 **$10/月**，可以无限次使用高级模型。而 Codeium 仅在 Windsurf 目前的推广期内开放了 Claude 3.5 的无限使用权限，在插件形态没有个人用户的无限使用方案。

对于组织用户，Github Copilot 增加了安全和数据保护等方面的一系列功能。分为 Business ($19/人/月) 和 Enterprise  ($39/人/月) 两种方案，后者**允许企业根据内部代码库定制 Copilot Chat**，更深入地了解客户知识，提供更有针对性的建议，为客户提供经过微调的自定义私有代码模型，并能够连接到 Github Enterprsie Cloud。仅从用量角度比较，Github Copilot 的定价目前全面低于 Codeium。

**02.**

**融资情况**

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/016.png)

Codeium 创立于2021年6月，当时名为 Exafunction，方向是机器学习 Infra，AI 工作负载的 GPU 优化和虚拟化。2022 年 4 月，公司获得 Greenoaks 领投，Founders Fund 参投的 2500 万美元 A 轮融资。虽然当时 ARR 已经达到几百万美金，但团队意识到原有领域难以做出差异化优势，AI coding 这一最结构化的赛道才是最适合 AI 技术落地、从 Day 1 就能证明前沿技术 PMF 的机会，因此决定重塑品牌，转型开发自己的 AI coding 产品。2022 年 10月，Codeium 发布了 beta 版本，依赖公司的 infra 基础向用户免费提供，并迎来用户数量的快速增长。

在 Codeium 推出的一年时间里，虽然缺少商业营收数据支撑，但凯鹏华盈 (Kleiner Perkins) 从 CIO 网络中的信息中明确了解到，企业对 coding 工具的真实需求恰恰与 Codeium 强调安全、上下文感知和 IDE 可扩展性的价值主张相吻合。这使 KP 于 2024 年 1 月 领投了 Codeium 的 B 轮融资，共计 6500 万美元，General Catalyst 和老股东 Greenoaks 参投，估值 5 亿美元。KP 投后扶持 Codeium 完成了市场拓展、组建销售团队等关键工作，为近一年来企业收入的快速增长打好了基础。

仅仅 7 个月后，2024 年 8 月，Codeium 宣布完成由 General Catalyst 领投，凯鹏华盈 (Kleiner Perkins) 和 Greenoaks 参投的 **1.5亿美元****C 轮融资**，估值达到 **12.5 亿美元**，在半年左右时间里增长了 250%。

**03.**

**创始团队：**

**Dream bigger**

Codeium 团队具有 “卷王” 的基因，被凯鹏华盈投资人 Leigh Marie Braswell 评价为 “见过最有活力的团队之一”，能够非常快地把握机遇，并从早期开始多维度规划并解决问题。在 GTM 团队扩张前，Codeium 的招募原则是精简和效率至上的，坚持只招必要的、足够自驱和优秀的人，以尽可能小的规模运行。在 A 轮融资时，创始团队仅有 8 人左右；在 2024 年中才达到百人规模。

公司由 **CEO** Varun Mohan 和 Douglas Chen 联合创立。二人在中学数学奥赛中结识，并一同进入 **MIT 计算机系**；Chen 在 MIT 以满绩毕业，并曾在 Facebook 担任机器学习工程师，专注于 Oculus VR 等项目的开发。技术团队里，有 40% 左右的工程师同样来自 MIT，很多人都是创始人在学校里曾经一起竞争的对手。这些理工人才不仅背景相似，更有着共同的热忱追求 —— 为软件开发带来彻底的革新。为此，工程师会在产品发布前自发加班到凌晨 4 点，创始人也同样宵衣旰食。这种**不满足于现状的进取心**让 Codeium 能在 A 轮融资后毅然决定转型，专注于更有前景的赛道，也使投资人对团队的长期表现充满信心。

CEO Mohan 是一个非常有野心的创业者，相信“求其上者得其中”，习惯于设定高目标；做事风格雷厉风行，追求效率和速度，在竞争中有着强烈的好胜心。在创立 Codeium 前，他曾在Linkedin、Quora、Cloudian 等软硬件公司实习，积累了数据基础设施和 ML 系统的软件工程经验；唯一一段全职工作经历是 2018-2021 在自动驾驶公司 NURO 担任自治基础设施技术主管，领导一个20人左右的团队。

Mohan 不满足于自动驾驶领域缓慢的商业化进展，认为在硬科技行业创业，需要在解决技术不确定性的同时产生收入甚至盈利。CEO 的坚定信念和执行力激励了团队克服了市场推广初期的挫折，并在产品和团队走向成熟后，在商业化表现上突飞猛进，在一年半里就超越了 SaaS startup GTM 的 **T2D3** (“Triple, Triple, Double, Double, Double”) 标准。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/017.png)

Mohan 对软件开发领域有着长期主义的远见，希望自己创立的公司能带来真正有意义的改变，同时能"用让人信服的方式将未来带到现在"。Codeium 的最终目标是让开发者的工作效率提高到原来的 20 倍。对于软件开发的未来，Mohan 并不认为效率提高会使企业中的开发人员减少，“人不会因为食物的价格跌到1/10就吃10倍的东西，但技术的采用是无上限的”。相反，由于 R&D 的 ROI 提高，企业会以更快的速度拓展开发的范围和深度。Mohan 相信 AI coding 的迭代有望带来 AGI 的真正普及。

**04.**

**商业化与客户采用**

2023 年，Codeium 收入仅 100 万美元；但近两轮融资以来，公司的商业化进程大幅加快。B 轮融资完成后，在 SaaS 领域具有丰富经验的销售主管 Graham Moreno 加入 Codeium 担任全球销售副总裁；而 C 轮融资后，公司集中招募了一批 GTM 人员，负责全美各个范围乃至全球范围的企业销售。

不到两年的时间内，活跃个人用户增长到了 70 万以上，并已被包括**许多财富 500 强在内的数千家企业**所采用，包括 JP Morgan Chase, Dell, Vector, Anduril 等。尤其是在 2024 年前 9 个月内，ARR 增长至 8 位数，YTD 涨幅超过 500% 。根据 Stack Overflow 的调查，**2024年6月，Codeium 的使用份额同比增长了近 600%，**成为使用率最高的 startup AI 助手。与此同时，GitHub Copilot 虽然凭借先发优势保持领先地位，但在专业开发人员中受欢迎的程度实际有所下降。

我们整理了部分 Codeium 企业客户的反馈。客户普遍认为，Codeium 和 Github Copilot 的**基础功能**和**代码生成质量**差别不大，区别主要在于 Codeium 可以本地部署，更能满足基于公司内部库的**定制化需求，且安全性更高；**而 Copilot 在 24 年 6 月才通过 SOC 2 认证，多名客户表示隐私安全性不足是采购 Copilot 时较大的 concern。然而在实际使用中，**两者互相替换、或被同时采购的情况**均有出现。预算充足的客户可能会同时购买两种产品，用于不同人群和任务；预算不足的客户可能基于实际情况，保留性价比更高的产品。

公司评估、试点 AI dev tools 时，一般都有自上而下的框架进行指导，但具体部门和团队也有一定自主权，并且在采购决策上彼此相对独立。各个公司考察 AI 产品的节奏不同，有些会同时比较 Copilot 和 Codeium，有些则会在在采用一种产品后发现痛点，而开始考虑新产品。**验证周期通常在3个月左右。**试点中最重要的考核维度包括：1）生成结果与prompt之间的匹配度、2）上下文能力/定制化需求、3）安全和隐私保护、4）对 IDE 和语言的支持范围。**ROI**的测算比较困难，很难直接量化生产力提高的幅度，但可以确定的是，能够改善开发人员工作体验。Codeium 的代码搜索功能是做出了差异化的亮点，但对销售的实际影响有限。

多个客户同时也有考察或购买 Tabnine，并认可了它在 ML、安全和隐私等特定任务方面的表现。以 Meta 为代表的大厂还开始考察了 Factory 等多代理系统，但目前技术实验属性较强，实际用例比较孤立，落地程度较低；Magic、Poolside 等专用 coding 模型也受到了关注，未来着眼点主要在于扩展上下文窗口大小，并能同时降低计算量和成本。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/018.png)

**05.**

**结论与猜想**

在 AI coding 领域的创业公司中，Codeium 拥有最鲜明地针对企业需求的价值主张，在企业安全、合规和个性化等关键维度上建立了差异化优势，并在短短两年内构建起相对完整的产品矩阵，覆盖了广泛的 IDE 插件和 IDE 产品，Windsurf 也在 Copilot 和 Agent 之间找到了独特定位，开创了新颖的开发范式。**从企业市场角度****，**Codeium 有望保持对 Cursor 等同领域创业公司的领先地位，作为估值快速翻倍的独角兽有着确定性的亮点，甚至能够重塑企业对开发工具的认知。

在与巨头的竞争方面，不容否认，Codeium 的差异点正在被一定程度地效仿、追赶，如 Github Copilot 在 2024 年推出企业定制化功能，并推动云方案通过 SOC 2 认证，但这恰恰验证了 Codeium 早期布局的前瞻性。诚然，Github Copilot 本身的产品性能并不落后，且凭借微软的强大背书和销售能力，已经在企业市场建立起深厚的用户基础，但 Codeium 在企业定制化等方面仍属于先驱者，且团队始终对市场竞争动态保持高度警觉，在频繁的产品更新和迅猛的商业化进程中，展现出了卓越的技术实力和战略眼光。Codeium 惊人的迭代速度仍在突破开发工具市场的想象空间，这是行动迟缓的巨头难以匹敌的优势。

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/019.png)

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/020.png)

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/021.png)

排版：Doro

延伸阅读

[![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/022.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247511288&idx=1&sn=b3090c9105c230991f922eea0f4d901b&scene=21#wechat_redirect)

对 DeepSeek 和智能下半场的几条判断

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/023.png)

[![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/024.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247511248&idx=1&sn=cd5f82195c0a7f4801f8cc7667017dba&scene=21#wechat_redirect)

扛住 DeepSeek 黑天鹅，AGIX 如何实现 3 倍纳指回报

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/025.png)

[![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/026.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247511172&idx=1&sn=cc83f26bf31183099252c13779614a45&scene=21#wechat_redirect)

86 条 DeepSeek 的关键思考 ｜Best Ideas 开源

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/027.png)

[![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/028.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247511140&idx=1&sn=54324979e1d404918f84114cd3e081ad&scene=21#wechat_redirect)

Decagon：用 AI Agent 解放客服团队，能否成为下一个独角兽

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/029.png)

[![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/030.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247511096&idx=1&sn=dee1163cad5af574582fa538532a9a0a&scene=21#wechat_redirect)

拾象 2025 AI Best Ideas：20大关键预测

![](../images/2025-02-12-codeium-qi-ye-yuan-sheng-ai-coding-chan-pin-neng-kai-chuang/031.png)
