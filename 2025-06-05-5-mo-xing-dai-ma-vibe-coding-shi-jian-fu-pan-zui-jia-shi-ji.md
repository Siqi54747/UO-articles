---
title: 5 万行代码 Vibe Coding 实践复盘：最佳实践、关键技术，Bitter Lesson
publish_date: '2025-06-05'
publish_timestamp: 1749124800
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/6BgZ1HSyv4Kj6-dtYDsyjw
msgid: 1000000365
appmsgid: 2247513779
itemidx: 1
digest: Coding Agent 结合 MCP 是一种值得探索的新的自动化方式
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzM9j6wyOQXDk7V9awbCtg8UTHbibB2f7HSSVFRbKEeTMhOg8fSfyDqX3w5wjR5KicsCBtG7siblgkqw/0?wx_fmt=jpeg
image_count: 31
archived_at: '2026-04-20T03:42:54+08:00'
---

[![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/001.gif)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=3570724992708624387#wechat_redirect)

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/002.png)

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/003.png)

作者：天哥

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/004.png)

本文来自一位大厂工程师的投稿，作为一位 22 年经验的资深工程师，他在最近几个月他深度体验了 Cline AI，[Cursor](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247510163&idx=1&sn=f3a636901cd1b55dadf71e2884f04982&scene=21#wechat_redirect)，GitHub Copilot 等产品，投入 3 个月的假期和周末时间，完全依赖 AI 编写了约 5 万行代码、成功完成了 3 个不同功能的产品。

这篇文章不只是关于 Coding Agent 的使用体验，也包括对相关关键技术，例如语言搜索、[MCP](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247511799&idx=1&sn=c063b0da3fcbfd309d1d6294f58bbc72&scene=21#wechat_redirect) 的探索和理解。Coding Agent 结合 MCP 是一种值得探索的新的自动化方式。

除了这 3 个月的 Vibe Coding 体验，从 2023 年起，作者和团队就开始尝试开发一款代码测试 Agent，并且在这个过程中探索人类经验和 AI 自由度之间的平衡，最终的结果很有趣：人类植入了过多的经验，反而限制了 AI 的发挥，锁死了产品上限。 对于 Agent 开发者来说，The Bitter Lesson 中的经验同样重要。

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/005.png)

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/006.png)

💡 目录 💡

   01 我的 Vibe Coding 之旅

   02 Coding Agent 的关键技术

   03 Coding Agent 对比

   04 Agent 开发中的 The Bitter Lesson

   05 结语

**01.**

**我的 Vibe Coding 之旅**

2025 年，Vibe Coding 开始大火，Vibe Coding 是指用户使用 Coding Agent 来编程，几乎 100%代码都是 AI 生成。通常用户会使用 Windsurf，Cursor，Cline，Devin 等产品。

**实践**

为了验证“Vibe Coding”的真假，尤其是深入了解 coding agent 的真实效能，我投入了 3 个月的假期和周末时间，期间完全依赖 AI 编写了约 5 万行代码，成功完成了 3 个不同功能的产品。

我个人的技术背景主要集中在 C/C++/汇编领域，对于前端开发常用的 JavaScript （JS） 和 TypeScript （TS） 没有经验。这种背景看似不利，但在 AI 编程时却恰好变成了优势：由于我缺乏相关经验，我不得不完全依赖 AI 进行开发。这段经历让我不仅理解了如何（how）有效利用 Coding Agent，也初步领悟了其背后的原理（why）

以下是我使用 AI 完成的产品（demo，just for fun）：

**产品 1: 增强型 Cline（基于 Cline3.5 版本开发）**

**•****产品功能：**增加了 index、multi-agent、context summary 和写爬虫的工具功能

**•****代码量：**2 万行 TS 代码

**•****Coding Agent：**从 GitHub Copilot 迁移到 Cursor

**•****开发费用：**$100 USD

**•****耗时：** 春节假期 + 4 个周末

**产品 2 : twitter 订阅系统**

**•****产品链接：**https://xtracker.fun/（需复制到浏览器体验）

**•****产品功能：**用户可以订阅任意 X 账号的消息，并形成一份日报

**•****代码量：**2 万行 JS 代码

**•****Coding Agent:**  Cursor

**•****开发费用：**$200 USD

**•****耗时：** 6 个周末

**产品 3 : 增强型 browser-use**

**•****产品链接：**https://codingbaby.fun/（需复制到浏览器体验）

**•****产品功能**：让 AI 操作你自己的浏览器完成简单工作，AI 借助视觉来工作，能绕过一切人机验证，权限

**•****代码量：**1 万行 JS 代码

**•****Coding Agent:**Cursor

**•****开发费用：**$200 USD

**•****耗时：** 五一假期 + 2 个周末

**开发体会**

这段经历带来了几点深刻体会：

**•****当前顶尖 Coding Agent 的强大威力：**以 Cursor 配合 Claude 3.7 Max 模型为例，对于 2 万行代码级别的项目，从 0 开始，100% 由 AI 生成代码是完全可以实现的。这证明了 AI vibe coding 并非空谈，而是已经具备了相当的实用价值。AI 的研发效能大致每天能完成 5000 行经过验证的代码，远大于人类手工编程的能力，需要指出的是，这里的 5000 行是指在 AI 一天可以生成 1 万行代码中，我会采纳其中的大约 5000 行代码。

**•****AI 能让人人成为全栈工程师：**即便是在我完全陌生的技术领域（如 JS/TS 开发），借助 coding agent 也能快速上手并完成项目。这对公司内部的人才培养和技能栈拓展具有重要的指导意义。相信在不久的将来，人人都可以是全栈工程师。

**•****人类角色的转变：**虽然代码可以由 AI 生成，但人类的角色依然关键。人类逐渐从代码开发者转向架构师，架构师需要定义需求、审查 AI 的结果，并且在合适的时机让 AI 进行代码重构。

**•****“提示工程”的重要性：**任务的成功与否，很大程度上取决于架构师能否向 AI 清晰地描述问题，并提供充分的上下文信息。例如，在为 Cline 设计 multi-agent 能力时，我构造了一个 2000 多字的 prompt （具体内容见下方），Cursor Claude 3.7 Max 准确理解了需求，经过大约 20 轮迭代，实现了这个复杂功能。这凸显了“提示工程”的重要性。

**给 Cline 的 Prompt 如下：**

请你仔细阅读这些文件，理解 Cline 作为一个 coding agent 的整体架构。

现有的架构存在严重的缺陷：

system prompt 里面一次性加入了所有的 tool，所有的 rule，AI 无论在干什么任务都会接收全部的 prompt，我预计至少 80%的轮次中是浪费 token 的。我们需要有新架构把 tools 抽象出来。针对任务来动态插拔 tools 。

请你帮我实现新架构，实现 multi agent 架构设计。

请注意：一定不要修改任何现有的文件。你应该始终通过新增文件来实现新架构，如果涉及旧文件的改动，请你给出建议，我来手动修改。为了确保向后兼容，对于旧文件的改动越小越好，控制在 1-2 行新代码插入是最佳的。

新架构的详细描述：

有一个 memory.txt 贯穿全局，是一个 sop 内的 task 共享的全局 memory。理论上每一个 task 的输出都要在 memory 中有记录。

最顶层是 domain sop 的抽象：domain sop（后续简称 SOP）是针对一类型任务的最佳实践的抽象，sop 数据结构中主要包含了 tasks 的集合。具体：crawler 爬虫任务使用的是一种 crawler sop，里面预定义了几个 task： analyze html dom，coding，test。

中间是 task 的抽象：task 是最核心的类，主要包含：tools（描述了做一个 task 需要的工具组合），prompt（描述了当前 task 的独特的 system prompt， 每个任务的 prompt 不同，并且与 system.ts 文件内容可以完全不一样），input（描述当前任务的输入）， output（当前任务的输出）

最底层是 tools 的抽象：请你把 system.ts 中的所有 tool 抽象成数据结构，可以动态插拔，任意组合。每一个 task 动态选择 tools，这样会极大减少 ai 处理多任务时候的 token 消耗。

user story:

以下是关于 crawler sop 的用户使用场景，请你仔细体会：

Cline 启动后，user（我）输入任务：请你写一个爬虫程序，把 musk 的推文爬下来，做成日报，每天早上 9 点发给我邮箱 xyz。

Cline 调用 crawler sop，从中读取 tasks，针对每一个 task 组装 tools，准备好 prompt，类似如下：

task1:  analyze html dom

tools: write\_to\_file, browser\_action, domAnalyzer

input: url, memory.txt

output: 把 html dom 写入 memory.txt

prompt：你是一个分析网页 dom 的 ai，你将为一个爬虫工程师提供写爬虫必须的信息，比如网页可视化内容，关键词信息，html dom 的详细信息，你拥有以下工具。你的输出要写入 memory.txt 文件。

task2: coding

tools: write\_to\_file, replace, read\_file, execute\_command

input: user task, memory.txt

output: 代码，状态写入 memory.txt

prompt：你是一个 ai coding 助手，你将根据用户任务编写爬虫程序，你的重要信息来自于 memory.txt 中的 html dom 信息，请你必须遵守 dom 信息来写爬虫。

Cline 开始一次执行每一个 domain sop 中的 task。这里的 task 其实对应的是 Cline 现有架构中的 user task。新架构相当于在更高维度抽象出来了 task 结构。在现有架构下，Cline ai 处理一个用户的端到端任务，而在新架构下，每一个 ai 只处理属于它的那部分 task，多个 ai 组合起来完成用户任务，这就是 multi agent 架构！

Cline 执行完成 task1 之后，让 ai 执行 task\_completion 工具，然后新架构自动选中下一个 task2 开始执行，直到最后一个 task 执行完成为止。

请你在实现新架构的时候：

不要修改 Cline.ts，这个文件太大了，你改不动。如果要修改，请你给我建议，我来手动修改。

新增一个 domainsop 文件夹，把新架构文件放到里面去。不要修改任何现有的文件！尽可能通过新增文件实现新功能。

注意模块化，每一个文件尽可能小，单一原则。

尽可能向后兼容，新架构与旧架构用一个开关可以自由切换

利用好 Cline 现有的处理 user task 的大逻辑，不要绕开它去与 ai 交互。Cline 旧架构的 user task 逻辑，要映射成为新架构中 domain sop 下的一个 task。

请你一步一步来，不要尝试一次性输出所有代码。

第一步任务：先把现有的 Cline 的 tools 抽象出来，变成可以动态插拔注册。等你完成 tools 抽象，再实现 sop 和 task 的抽象。

滑动查看全部内容

**AI Coding 最佳实践**

要充分发挥 coding agent 的潜力，并使其真正成为提升工作效率的得力伙伴，掌握正确的使用方法和培养积极的心态至关重要。

**•****实践出真知：**这是学习和掌握任何新工具不变的真理。只有亲身实践，才能深刻理解 coding agent 的特性、优点和局限性。建议从实际工作中的小任务开始尝试，逐步挑战更复杂的场景。

**•****理论联系实践：**读一读 Cline 的源代码，单步调试一下核心的流程，打印一次 api 调用中 AI 的 input 和 output message 分别是什么，会非常有助于你理解 coding agent 的原理，从而更好地指导你的实践。其中，**system.ts** 和**src/core/task/index.ts**2 个文件是必读的

**•****选用最强模型：**在条件允许的情况下，尽量选择当前能力最强的 AI 模型。例如，在 Cursor 中，优先使用 Claude 3.7 Max 或 Gemini 2.5 Pro Max 等顶级模型，它们通常能提供更准确、更智能的辅助；

**•****提供充分的上下文：**与 coding agent 交流，本质上与人沟通类似。当遇到 AI 执行任务失败或结果不理想时，首先应反思是否提供给 AI 的上下文信息不够充分或存在歧义。清晰、完整、准确的上下文是获得高质量输出的关键；

**•****拥抱“Agent 模式”：**如下文所述，务必开启并坚持使用 Agent Mode。这能让你体验到 coding agent 工具的核心功能，并在实践中积累宝贵的经验。

**•****培养积极的协作心态：**关键在于思考“如何才能让 AI 更好地为我所用？”，而不是试图证明“AI 在某些方面不行”。要找出 AI 的不足之处很容易，每个人都能举出很多例子，但这种做法对于提升认知和解决问题并无益处。更有效的方法是分析 AI 失败的原因，并尝试配合 AI 一起解决问题。

**02.**

**Coding Agent**

**的关键技术**

Coding Agent 的代表有 Cursor，Cline，GitHub Copilot，Windsurf（刚被 OpenAI 收购）等。注意：有些 coding agent 产品默认并没有开启 Agent 模式，请根据使用方式来区分你是否真的在使用这些产品的 agent 能力。

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/007.png)

**强烈建议大家在实践中开启并坚持使用 Agent 模式。**虽然初期可能需要一定的适应和学习，但这种投入对于掌握未来编程范式而言是值得的。其中，Cline 本身就是 Agent 模式，不用选择模式，直接用就可以，GitHub Copilot 和 Cursor 则需要专门设置。

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/008.png)

GitHub Copilot 打开 Agent 模式：vscode- settings，在搜索栏里输入 agent，在出现的选项中，把 Agent:Enabled 打勾

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/009.png)

Cursor 打开 Agent 模式：很简单，在输入窗口下拉中直接选择模式

**我个人判断：Coding Agnet 关键技术是：Model， Context 和 Tools。**

为什么我认为这三点最重要？**可以将 Coding Agent 类比为一个公司，而其背后的 AI 模型则是一位员工。**

一个公司要让员工发挥最大价值，通常需要：招聘最强的员工，在布置任务时提供“充分且必要，外加反馈闭环”的上下文信息，并为其配备一套强大的工具链。

以上是“公司如何发挥人类员工最大价值”的答案，Coding Agent 的关键技术也遵循同样的逻辑：

**•****AI 的“大脑”：模型（Model）**

越聪明越好，目前最强的编程模型是 Cursor 官方调教的模型：Claude 3.7 Max（作者注：本篇文章写于 2025 年 5 月初），以及 Gemini 2.5 Pro Max，两者都在 Cursor 收费版中可以使用。

**•****AI 的“工作记忆”：上下文（Context）**

对于 AI 来说，Context 相当于是 AI 看到的信息全集，context 由很多部分组成：

1. System prompt：告诉 AI，你是什么角色，你有什么工具（write to file， read file， shell，browser use）可以使用，Cline 的 system prompt 有 1000 多行，节选如下：

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/010.png)

2. User prompt：用户输入的任务，用户临时给的反馈，等。

3. Feedback loop：每一次 tool 使用的 result，用户的反馈等，Cline 的 user prompt 节选如下，assistant 代表 AI 说的话和做的事情，user 代表用户给 AI 的反馈：

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/011.png)

**•****AI 的“工具链”：工具（Tools）**

常规的 tool 比如 write to file， read file， execute shell 等，是各大产品的标配。但有一些 tool 是各自的特色，也是各种 Coding Agent 之间能力的本质区别，比如：

**1.**Cursor 自带了互联网搜索工具：**web\_search**，当你想要 Coding Agent 处理一个非常新的技术（比如 MCP），AI 模型有可能没有 pre-train 这个知识，于是他会胡乱回答。这时候你可以让他搜索互联网确认最新的技术文档和最新的开源代码，他会迅速掌握这个新知识，接下来就可以写出正确的代码了。

**2.**Cursor 拥有语义搜索工具：**codebase\_search**，**这是 Cursor 能够驾驭 10w 行代码以上大型工程的核心能力之一。**

**3.**MCP：各家都支持，但是有优劣，Cline 支持最好，Cursor 其次，GitHub Copilot 有待优化。

**4.** Cline 自带 browser use 工具：browser action 工具让 Cline 可以访问互联网，基于浏览器进行工作，底层基于 puppeteer。

理解这三个核心组成部分（强大的模型、充分的上下文以及高效的工具）是掌握和有效利用 coding agent 的关键。

接下来我会展开讲一下 Coding Agent 的几个关键的 tool：语义搜索 和 MCP

**语义搜索工具：codebase\_search**

AI 要掌握一份中大型代码，搜索是一个很重要的能力。在编程领域，代码搜索大致分两种技术：关键词搜索和语义搜索。

关键词搜索就是大家今天每天都在用的搜索方式，我们可以在 Vscode 或者 Cursor，点击搜索按钮，输入关键字进行搜索。但假设我们要在上万行的 Cline 代码中查找“Cline 的浏览器配置是什么？”，如果直接输入这个查询语句，vscode 无法返回任何结果：

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/012.png)

与关键词搜索不同，语义搜索侧重于理解用户查询背后的上下文含义和意图，而不仅仅是匹配关键词 。

它力求像人一样理解查询的深层含义，从而提供更相关的结果。例如，当用户搜索“什么 AI 可以做视频通话？”，搜索引擎返回的结果并非基于“视频通话”的字面完全匹配，而是理解了用户的真实需求。

搜索引擎用的就是语义搜索技术，如果我们用 Google 搜索：“什么 AI 可以做视频通话？”，结果如下：

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/013.png)

**Cursor 的语义搜索工具**

Cursor 总共给 AI 配置了 5 个 search 工具：

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/014.png)

其中本地文件搜索的主要是 2 个：

**•**语义搜索工具 codebase\_search（Cline 没有这个工具）

**•**传统的文本搜索工具 grep\_search（Cline 拥有类似的工具）

**Cursor 的语义搜索有什么用？**

做一个简单的测试，用 Cursor 打开 Cline 的源代码，index 完毕后，提出一个纯语义的模糊指令“我想请你搜索一下：Cline 的浏览器参数是如何指定的？”

Cursor 直接调用了 codebase\_search 工具，输入的参数是纯语义级别的模糊自然语言“How are Cline browser parameters specified or configured？”，Cursor 返回了相关的语义级别的代码片段给 AI 看，然后 AI 总结出了答案，如下：

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/015.png)

Cursor 的 AI 往往会结合 list + codebase\_search + grep\_search 多种工具查找他需要的代码片段，这种能力使得 AI 能够更高效地理解复杂的代码结构。

**Cursor 的 index 设置**

Cursor 的索引功能默认是开启的。对于特别庞大的工程，例如超过 10 万行级别的代码库，可以尝试按子模块进行索引，这可能会获得更好的效果。

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/016.png)

**Cursor 语义搜索的实现原理**

所谓的语义搜索，本质类似于百度的搜索，或者说是一种 RAG 技术，我们可以把 Cursor 的 codebase\_search 能力类比成：**Cursor 在云端为每一个人的每一个工程建立了一个专属的百度搜索**，语义搜索背后的技术，在行业中一般称为：index，index 一旦完成之后，Cursor 背后的那个 AI 就可以使用语义来搜索你的工程中所有源代码，类似于你可以用语义搜索百度信息。

**语义搜索的核心技术**

**1.** ast 语义切分：把整个工程按照代码结构进行分块

**2.**向量嵌入：对代码块进行压缩后存入向量数据库

**3.**向量搜索：AI 输入语义，得到语义最接近的几个代码片段

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/017.png)

codebase\_search 工具描述，也就是 AI 视角看到的语义搜索工具长什么样

**Cline 的缺陷： 缺少语义搜索**

个人体验：Cline 处理的代码量超过 1w 行通常会有点吃力，超过 5 万行之后就更困难了。

其中一个原因是：缺失了关键的 codebase\_search 工具，无法进行语义级别的搜索。但好消息是：Cline 是开源的，我们可以做一个语义搜索给它用。

**如何在 Cline 上复现 Cursor 的语义搜索？**

为 Cline 做一个 demo 级别的本地 index 系统，代码量在 2000 行以上，我用 Cursor 3.7 max 来编程实现 100%代码，大概用了 30 个来回搞定。其中的关键技术如下：

**1.**用 OpenAI 的 text-embedding-ada-002 模型生成文本嵌入

**2.**使用 ChromaDB 做本地 embedding 数据库

**3.**搜索的时候，用余弦距离计算相似度

要在公司级别做成一个稳定的线上 index 系统，需要投入更大人力和时间，实现的功能包括但不限于：

**1.**基于 ast 的代码分块

**2.** 云端 embedding

**3.** 云端 cache，共享

**4.**基于哈希树的 diff 查询

**5.**各种工程优化

**MCP 工具**

**为什么需要 MCP？**

MCP 是现在非常火的技术，Cursor，Cline 以及 GitHub Copilot 都已经支持 MCP。

但因为这个协议很新，大部分 AI 对这个技术的理解非常浅，因此让 Coding Agent 写出高质量的 MCP 需要一定的技巧。

思考这样一个问题：如何让 Cline 这个 Coding Agent 可以使用你们公司的某一个现成的工具链？

**如果没有 MCP， Cline 的开发是这样的：**

**1.**针对 AI 的使用习惯封装工具链 的 api

**2.** 在 system.ts 里面加一段关于工具链接口的描述

**3.** 在 Cline.ts（3.5 版本，最新版本改到 index.ts 里面了）里面增加工具链 api 的 handler

**4.** 在 3-5 个前后端文件中添加：参数描述，ui 展示信息，工具描述，等

这种开发模式存在 2 个问题：

**1.**效率问题：整个流程有些琐碎， 需要改动 3-5 个 Cline 的源代码文件

**2.**通用性问题：这个工具链的 MCP 工具只能给 Cline 用，Cursor 不能用，GitHub Copilot 也不能用

**如果有 MCP，开发就变得非常简单：**

**1.** 封装工具 的 api，成为一个 MCP 工具；

**2.**编辑 Cline\_MCP\_settings.json，添加一段工具链 MCP 的描述；

有了 MCP 后，对应的优点是：

**1.**整个流程很简洁，除了封装 api 之外，只需要改动一个 json

**2.**这个工具链 MCP 工具能同时在 Cursor， Cline，GitHub Copilot 上使用，就像 usb 设备一样通用

如果你想让 Coding Agent 使用公司已有的工具链，那么 MCP 提供了一种高效且标准化的途径。

**Coding Agent 结合 MCP 是一种值得探索的新的自动化方式。**

**MCP 的原理**

大家有兴趣可以看一下 Cline 源代码，有助于理解 MCP 的 host，client，server 的概念，代码位置在：src/services/mcp/mcphub.ts，在 Cline 的 AI 的视角，MCP 本质上也是一种 tool，在 Cline 中，MCP 具体的名称叫：use\_mcp\_tool。

use\_MCP\_tool 与 read\_file 这个 tool 没有本质区别，AI 从 system prompt 中得到 tool 的描述，AI 输出针对这个 tool 的调用，如下：

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/018.png)

**用 Coding Agent 开发 MCP 的要点**

理论上，你可以用 coding agent 来开发任意的 MCP 工具，但 MCP 是一个非常新的生态，各大 coding agent 对于 MCP 的支持能力参差不齐，**截止到****25/05/03****， 我感觉 Cline 对于 MCP 的支持是最佳的，Cursor 其次，而 GitHub Copilot 处于苦苦追赶的阶段。**

大致对比如下，但也许这些结论在 1 个月后就会过时（作者注：Cursor 截止到 25 年 3 月还不支持 AI 看到 MCP 返回图片，但是 25 年 4 月迅速支持了 claude 3.7 看到 MCP 返回的图片）

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/019.png)

**如何增强 Cursor 开发 MCP 的能力？**

虽然 Cursor 对于 MCP 的支持不如 Cline，但是由于 Cursor 拥有更强大的模型 claude 3.7 max，以及强大的互联网搜索能力，因此我尝试让 Cursor 提升开发 MCP 的能力，最终让 Cursor 与 Cline 一样优秀，方法如下：

**1.** 把 Cline 的 system prompt 中 MCP 相关的内容给 Cursor 的 3.7 max 参考一下。

**2.** 让 Cursor 的 AI 先做这个任务：“请你搜索互联网，了解 Anthropic MCP（model context protocol）的实现原理，查找 Cursor MCP 的源代码，总结到 。**cursor/MCP.md**文档里面，要求：1。 描述 MCP 是什么？2. 描述 MCP 的协议是什么？3. 描述 anthropic 官方的 MCP 参考代码是什么？4. 描述在 Cursor 这个 ide 中实现 MCP 的官方参考代码是什么？”

**3.** 然后重新启动一个新任务（刷新 context windows，防止爆炸）：“请你参考 。**cursor/MCP.md** 文档，进行新 MCP tool 的开发， 目标：…… 要求：……”

**MCP 与传统的工具链开发对比**

**•****传统模式：**工具链团队要负责工具开发，同时也要为用户开发使用工具的业务逻辑，比如让 编译系统 与 仿真系统 打通，等。缺点是当用户需求众多的时候要排队开发，无法做到随时响应需求

**•****MCP 模式下：**工具链团队把现有工具封装成 MCP，用户用自然语言描述任务 SOP，由 coding agent 背后的 AI 来自动串联各种 MCP，比如：“帮我解决这个 bug，然后编译，然后做一个仿真测试” 这样的需求可以让 AI 用 1 个或者多个 MCP 来完成。优点是：在端到端 SOP 并不是特别确定的时候，用户自己就能完成全流程任务，没必要排队等工具链团队开发代码

**MCP 工具开发实战**

Manus 背后有技术是：browser use，也就是让 AI 操作浏览器完成任务。但当我下载 browser use 开源代码实验的时候，发现它很难攻破 Cloudflare 的人机验证，也无法在公司内网下使用，我换成 playwright MCP 工具，发现这些问题仍然没有解决。

受到智谱轻言的 AutoGLM 产品的启发，我发现可以做一个增强版本的 browser use MCP，完全绕过人机验证和内网检查。原理是：直接使用

用户的浏览器来完成任务，ai 发出的浏览器指令通过 chrome 插件来执行，这种方式很难被反爬虫发现。

它的效果如下：左边是 playwright MCP，右边是我开发的 codingbaby browser MCP，playwright 在访问一个需要权限的网页的时候被人机验证拦截了，而 codingbaby 这个 MCP 完全复用用户的浏览器，没有触发人机验证，于是就可以全自动完成浏览器任务：

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/020.gif)

如果有兴趣的话可以体验一下 browser use MCP，也可以看一下 AI 写的 MCP 代码长啥样：https://github.com/buyitsydney/CodingBaby-Browser-MCP

**03.**

**Coding Agent 对比**

我从个人的体验（与网上的任何评测无关），对三个产品进行了综合对比：

滑动查看全部内容

滑动查看全部内容

|  |  |  |  |
| --- | --- | --- | --- |
| **对比项** | **Cursor** | **GitHub Copilot** | **Cline（3.5 版本）** |
| model | 稍强 有独特的 claude 3.7 max 和 gemini 2.5 pro max 但是否能持续领先不好说，通用 llm 的发展速度也许会磨平这项优势 | 跟随行业 LLM | 跟随行业 LLM |
| context 管理 | 中 有 summary，但偶尔也会失忆 | 差 虽然有 summary，但是表现很差，需要微软后续迭代优化 | 稍差 预计这将会是 Cline 的重要补强方向 |
| MCP | 中 Claude 3.7 可以识别 MCP 工具返回的图片，但是   gemini 2.5 pro 不能识别 | 差 有兼容性问题 所有模型都无法识别 MCP 工具返回的图片 | 强 只要模型支持图片，就能识别 MCP 工具返回的图片 |
| 语义搜索/index | 支持 | 支持 | 无 预计这将会是 Cline 的补强方向 |
| 互联网搜索 | 支持 | 支持 | 无 可以通过 MCP 扩展 |
| 可扩展能力 | 普通：Clinerule，MCP 等 | 同 Cursor | 强：可以任意修改源代码 可以自行增加语义搜索 index 可以优化 context 管理 可以增加 multi agent 功能 |
| UI 设计 | 普通 | 普通 | 强 Cline 的 UI 设计我一直很喜欢： 1. 早期版本就有费用，token，  cache，context window 等数字的显示 2. 最新版本 3.15.1 版本更是把   task timeline 显示在了 ui 上，对于用户理解 Cline 在干什么很有帮助 |
| 能驾驭的代码规模 | 10w 行+ 量级 凭借语义搜索和   context summary 功能，  能理解更多代码 | 1-5w 行 微软暂时是落后的， 但是这个领域是微软必争之地， 也许后续会反超 | 1-5w 行 缺失重要的能力： 1. 缺少语义搜索：用传统方式搜索大型代码库效率低，容易引爆 context window 2. context 管理缺少 summary：一旦超过 context window 阈值，立刻丢失前半段记忆 这几项能力都可以开发实现，  Cline 潜力非常大 |

滑动查看全部内容

**详细解读：**

**•****Cursor - “现阶段的王者”**

当使用 Cursor 并选择 Claude 3.7 Max 模型时，用户可以体验到当前最顶尖的 coding agent 能力。对于 10 万行代码级别的项目，完全从零开始，100% 由 Cursor 生成代码是可行的。

用好 Cursor 的关键在于：多实践、选用最强模型、以及在提问时提供充分的上下文信息。与 AI 交流的本质和与人沟通类似，当 AI 执行任务失败时，应该反思是否是提供给 AI 的上下文不够充分。

在充分的上下文支持下，Cursor 和 Claude 3.7 Max 往往能在 10-30 轮以内对话正确完成一个相当复杂的任务。

**•****Cline - “潜力巨大，公司应考虑深度定制”**

Cline 的最大优势在于其开源特性，允许进行深度定制和二次开发。此外，它对 MCP 的支持是三者中最佳的，是第一个支持 MCP 的产品，并且截至目前（2025/05/08）是唯一能让 Gemini 2.5 模型看到 MCP 返回截图的工具。 然而，Cline 存在明显的优化方向：

**1.****缺乏语义搜索：**如前所述，这使其难以驾驭中大型工程。

**2.****上下文管理：**Cline 的对话历史会无限累积，达到阈值后采取简单的“砍半”策略，极易导致 AI“失忆”，这也是 Cline 运行成本较高的主要原因之一。 针对上下文管理问题，大致的解决思路包括：实现一个历史摘要（historySummarizer）功能，当历史记录超过一定阈值后，用 AI 进行总结，有损压缩成一段历史摘要；对于特别消耗历史记录空间的工具（如 Cline 调用一次 curl 可能返回大量文本），要及时精简工具结果。

以上两大问题（增加语义搜索、优化上下文管理）不难解决，理论上 Cline 完全有能力处理 10 万行甚至更大规模的代码工程，潜力巨大。

**•****GitHub Copilot**

在对 Cline 进行二次开发的体验中，GitHub Copilot 的表现相较于 Cursor + Claude 3.7 Max 稍逊一筹。其上下文管理能力较差，MCP 支持也有待优化。

尽管目前在某些方面暂时落后，但 coding agent 领域是微软的必争之地，凭借其强大的研发实力和生态整合能力，未来完全有可能实现反超。

总体看，Coding Agent 就像程序员的十八般兵器，有人喜欢短剑，有人喜欢长枪，没有绝对的“最佳”兵器，只有最适合自己的兵器。但在这个 pre-AGI 时代，赤手空拳一定是不行的。

**04.**

**Agent 开发中的**

**The Bitter Lesson**

强化学习之父 Sutton 在 2019 年写的一篇短文  The Bitter Lesson 来概括，被称为是“AI 领域的圣经”，从 2023 年 2 月份接触 ChatGPT，到 2025 年 5 月，这 2 年来我使用 AI 的最深刻的感受也可以被 The Bitter Lesson 总结。

2023 年，我和团队尝试在一款 quality agent 产品的早期版本中更多利用好 AI 的能力来写单元测试、发现 bug，但是由于 GPT-4 能力较弱，AI 还搞不定这些需求。

2024 年，我们开始更多植入人类经验，让 AI （GPT-4o）只做简单的事情，产品效果不错，单元测试覆盖率能够做到 70%左右，一度觉得找到了 AI 时代做 Agent 的正确方法。

但这样的架构设计带来了一个严重的问题：虽然外界 AI 能力不断提升，但产品的测试覆盖率却无法同步提升，用 Claude 3.7 和用 GPT-4o 的覆盖率数字几乎相同，显然不合常理，因为 Claude 3.7 的编程能力是远超 GPT-4o 的。

这个反常现象很直接地展示了 bitter lesson：人类植入了过多的经验，反而限制了 AI 的发挥，锁死了产品上限。

2025 年，团队开始重构这个产品，让 AI 能力占主导地位，尽量减少人类的经验。最新的数字证明：测试覆盖率可以做到 99%以上。

因此，对于做 Agent 的同学来说，Sutton 的这篇文章也值得经常读一读，提醒自己是不是正在犯同样的错误。

这里我把 The Bitter Lesson 的节选翻译如下：

这个“苦涩教训”基于以下历史观察：

1）AI 研究人员经常尝试将知识直接构建到智能体中；

2）这种做法在短期内确实有所帮助，并给研究者带来个人满足感；

3）但从长远看，这种方法会遇到瓶颈，甚至阻碍进一步发展；

4）真正的突破性进展最终来自于一种对立的方法——通过搜索和学习来扩展计算能力。这种最终的成功常常伴随着一丝苦涩，且往往未被完全接受，因为它战胜的是一种备受青睐的、以人为中心的方法。

我们应该汲取的一个重要启示是通用方法的强大力量——那些能够随着计算资源增加而不断扩展的方法，即使在可用计算资源已经非常庞大的情况下仍然如此。

能够以这种方式无限扩展的两种方法是 search 和 learning。

第二个要点是，心智的实际内容极其复杂，这种复杂性是不可避免的。我们应当停止尝试寻找简单方法来理解心智内容，比如简单地思考空间、物体、多智能体系统或对称性。

这些都只是任意复杂的外部世界的一部分。我们不应该将这些内容直接内置到系统中，因为它们的复杂性是无穷无尽的；相反，我们应该只内置那些能够发现并捕捉这种任意复杂性的元方法。这些方法的关键在于它们能够找到良好的近似解，但寻找这些近似解的过程应该由我们的方法完成，而非我们自己。我们需要的是能够像我们一样进行发现的人工智能系统，而不是简单包含我们已发现知识的系统。将我们的发现内置到系统中只会使理解发现过程本身变得更加困难。

**05.**

**结语**

世界发展太快，我以上说的所有内容，仅 2025 年 5 月 10 日这个时间点成立，也许半年后，绝大多数的内容都将是错误的。

**Reference**

1、Cursor CTO 的访谈：[https://mp.weixin.qq.com/s/IiJ24HfKCdXQ-6rm9T4iqw](https://mp.weixin.qq.com/s?__biz=MzkzNjkzNDMzMA==&mid=2247483706&idx=1&sn=5bb3c8920d5dbe935b513950f0a7e4c3&scene=21#wechat_redirect)

2、Cursor index 官方介绍：https://www.Cursor.com/security#codebase-indexing

3、Cursor index 的实现介绍：https://www.xmsumi.com/detAIl/281

4、Cline 源代码：

https://github.com/Cline/Cline

5、Browser use MCP: 

https://MCP.so/server/codingbaby-browser-MCP/buyitsydney

6、Browser use chrome extension: https://chromewebstore.google.com/detAIl/codingbaby-extension/pjadpjgapfnmaaabkjbeldmjdmcfgcco?hl=zh-CN&utm\_source=ext\_sidebar

7、The bitter lesson: https://www.cs.utexas.edu/~eunsol/courses/data/bitter\_lesson.pdf

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/021.png)

排版：夏悦涵

延伸阅读

[![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/022.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247513700&idx=1&sn=bfddb74bdb74b57b8ed593c880796d5b&scene=21#wechat_redirect)

为什么 AI Agent 需要新的商业模式？

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/023.png)

[![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/024.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247513646&idx=1&sn=3642b9ba23ed41a058a2bf2afa314fbf&scene=21#wechat_redirect)

AI-Native 的 Infra 演化路线：L0 到 L5

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/025.png)

[![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/026.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247513619&idx=1&sn=68a8461c86713b0535736d41d71079aa&scene=21#wechat_redirect)

AI x 保险图谱：第一家 AI-Native 的保险独角兽会长什么样？

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/027.png)

[![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/028.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247513580&idx=1&sn=fdec5d42c8e23ae753aac4ccdfa6c798&scene=21#wechat_redirect)

Claude 4 核心成员：Agent RL，RLVR 新范式，Inference 算力瓶颈

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/029.png)

[![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/030.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247513518&idx=1&sn=d7c5b28351e46e12c00aaae61649d408&scene=21#wechat_redirect)

多邻国的「AI-first」到底是什么？｜AGIX投什么

![](../images/2025-06-05-5-mo-xing-dai-ma-vibe-coding-shi-jian-fu-pan-zui-jia-shi-ji/031.png)
