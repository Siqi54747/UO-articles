---
title: “10x Cursor”开发体验， Claude Code 如何带来 AI Coding 的 L4 时刻？｜Best Ideas
publish_date: '2025-07-06'
publish_timestamp: 1751808405
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/GB4t6GKOd4oU0Fsb-NfyEA
msgid: 1000000384
appmsgid: 2247514519
itemidx: 1
digest: Agent 的内核能力比前端形式更重要
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgz8bbHjMnIDsTHm16tNNBMh5tYpKT6gEmdIfIWJ0Ey5pnDcAR60Reehujuv5FNcZQsPWYhBGibL0Zw/0?wx_fmt=jpeg
image_count: 41
archived_at: '2026-04-20T03:56:34+08:00'
---

[![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/002.png)

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/003.png)

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/004.png)

今年以来 Coding 领域的最大变量是 AI labs 们的加入，模型大厂纷纷发力，和创业公司共同竞争这一关键场景：两周前，all-in coding 的 Anthropic 更新了 Artifacts 功能，用户可以在聊天界面里直接生成、预览和编辑代码，实现类 vibe coding 的体验；同一天，Google 也推出了自己的命令行工具 Gemini CLI，开发者可以使用自然语言直接调用 Gemini 2.5 Pro 来实现编码、调试和内容生成等操作。

毫无疑问，模型厂商最大的优势是对模型能力理解和成本。Claude Code 从今年 2 月上线以来，迅速在开发者群体中积累了口碑，我们观察到不少深度开发中表示自己已经从 cursor 迁移到了 Claude code。产品角度，它所提供的 agentic 异步性几乎已经让 AI coding 的 L4 时刻得以实现。

为什么开发者“放弃”Cursor 纷纷迁移到 Claude Code？ Claude Code 的 10x 开发体验是如何实现的？它的增长会给 cursor、lovable 等其他现象级 coding 产品带来哪些影响？它所主打的 CLI 会是 coding 产品的最好形态吗？

…

为了更好地理解 Coding 领域正在发生的变化、梳理关键问题，我们邀请到了黄航、Tony、周弋涵三位开发者组织了一场「Best Ideas」讨论会，他们结合自身的开发体验分享了对 Claude Code、cursor、lovable 等 coding 产品的观察，并和海外独角兽社群成员一起讨论了对 coding agent 赛道的观点与洞察。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/005.png)

💡 目录 💡

   01 开发者视角下的 Claude Code

   02 Claude Code 是第一个 L4 Coding Agent

   03 Anthropic 可能会成为 Coding 领域的 AWS

   04 Agent 的内核理念比前端形态更重要

   05 Coding 的终级的赢家会是谁？

**01.**

**开发者视角下的**

**Claude Code**

**Part 1: 为什么 Claude Code 会成为 Anthropic 的 Killer App**

**分享人：**

**•**黄航：InsForge 创始人，创业前在 Amazon 担任 Senior PM

**•**Tony：InsForge 联合创始人，创业前在 Databricks 工作

**1. 为什么开发者迁移到了 Claude Code**

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/006.png)

**1）****成本低：Claude Code 极大降低了用户使用最先进的 model 的成本，非常适合每天都写代码的高频开发者。**

目前 Opus 是交付能力最好的模型，但在 Cursor 的产品设计中，默认提供的是 Sonnet 模型，用户如果要使用 Opus 模型就需要按使用量单独计费。

和 Sonnet 比，Opus 非常昂贵，消耗的 token 量为 Sonnet 的 5 倍，费用大约为每小时 20–40 美元。对于高频开发者来说，在 Cursor 目前的产品设计下，如果要持续使用 Opus 模型，月支出往往会达到 4000-5000 美元。

作为对比，Claude Code 可以直接选择 Opus 模型，几乎可以无限使用 token，月固定费用为 200 美元，成本可以降低至之前的 1/20，显著低于 Cursor。

即便不使用 Opus 模型，只采用 Sonnet 模型，在 Cursor 按使用计费的情况下，开发者每月需要花费约 400–500 美元。同等开发量和 token 使用量在 Claude Code 上通常只需每月 100–200 美元，成本至少可以降低 1/2，且在交付效率和响应质量方面，Claude Code 也明显优于 Cursor。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/007.png)

Cursor 官网定价

**2）效率高：端到端建立项目的成功率和效率都极高**

Cursor 没有自主拆解任务的能力，所以需要开发者在使用 Cursor 的时候就要有对于如何构建这个 project 的具体想法。

相比之下，Claude Code 具有 planning 能力，用户只需要在 prompt 中给出大致需求后，Claude Code 就可以自主地将任务拆分为子任务，逐步完成且实时反馈。

而且 Claude Code 在读已有的很大的 codebase 的时候，还会自主创建一个 context 文件并学习 context，能够在开发过程中生成 test command，进行自主地调试，出了问题会自己 debug 等。

比如，就有开发者提到，提高 vibe coding 成功率的关键就是要有测试依据。除了单元测试（时间成本与维护成本都较高）之外，基于 language server 及时编译（比如 tsc）的检查更有价值，Cursor、Windsurf 在今年都陆续支持了这个功能。此外，Claude Code 的出色能力，不仅受益于大模型本身智商的提高，工程也很关键，Windsurf、Cursor 早期经常出现编译错误，但 Claude Code 几乎就没这个问题。

**3）****异步 async 开发和高代理（L4）：Claude Code 对于超长文本有记忆管理能力，是真正的 agentic 模式，大幅减少了需要人介入的部分。**

由于 Cursor 有 context window 限制，在长 context 的场景下会遗忘最开始的 prompt 和需求，因此需要开发者辅助定义 workflow 和进行 debug。而 Claude Code 有 memory context 的功能，可以在即将遗忘 context 的情况下自主地回顾、压缩先前的 prompt，形成 memory。

**2. 虽然 CLI 很火，但 GUI 才是未来**

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/008.png)

今天我们看到的 Claude Code 的产品形态其实是内部工具直接开发给外界用户的产品，并不是 Anthropic 为了专攻 coding 领域而专门规划、打造出来的产品。

Anthropic 的 CPO 就专门讲过这件事，Anthropic 团队内部已经有 90% 的代码都由 Claude Code 生成了，后来，公司觉得这个工具有潜力对外试水，于是在几乎没有进行任何产品优化的情况下，就发布了。

在编程领域，开发者更关注工具的最终效果，因为 Claude Code 所使用的底层模型 Opus 能力非常强大，所以即使没有进行产品化设计、即便 CLI 很难用，大家也愿意使用。因此 Claude Code 爆火更多证明了 Opus 模型能力很强，并不能验证 CLI 这个形态是 coding agent 的终局。

最近 CLI 之所以讨论度很高，还因为 Google 在看到 Claude Code 的成功和市场需求后，为了快速入局并抢占市场份额，选择直接推出免费且量大的 Gemini CLI，迅速吸引了价格敏感、对产品忠诚度不高的 coding agent 开发者，进一步推高了 CLI 的声量和热度。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/009.png)

但如果站在用户体验角度看 CLI，其实 CLI 的局限相当明显：

1）AI 是直接生成代码的，一旦出现幻觉或错误，用户不能修改与撤销，只能依赖 Git 等外部工具进行版本回滚，操作非常繁琐；

2） 在安装插件、配置内存或指定任务等高级操作上，用户需要手动编写和修改配置文件，对普通用户而言，使用门槛很高；

3）处理图片等多媒体文件非常不便，用户无法像在 GUI 中那样通过拖拽来实现图片上传、实时展示等功能，多模态交互体验很差。

因此，coding 工具只有通过 GUI 来优化体验，才能被更广泛的用户群体所接受。Claude Code 也已经开始推出 UI 界面和 VSCode 扩展。

此外，未来的产品形态将会是 GUI，但不一定是 IDE。

因为 IDE 是过去数十年软件开发模式下的产物，它本身也存在一定的学习曲线和历史包袱。AI-native 开发工具可能会带来全新且更高效的交互模式。

**3. Cursor or Claude Code?**

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/010.png)

如果综合 coding 领域所有 use case，结合用户使用偏好和工具交付效果来看，Cursor 还是优于 Claude 的。

这是因为 Cursor 对用户体验做了很多优化，而且 Cursor 在处理简单任务时的速度非常快。

此外，Cursor 的市场认可度和渗透率也是最高的，满足了大企业对 SLA（服务稳定性）、数据隐私和安全性的严格要求，比如 Tony 就提到 Databricks 目前就与 Cursor 谈合作，内部数千名员工都可以使用 Cursor。此外，黄航还提到 Amazon 也正在与 Cursor 进行合作谈判。

但 Cursor 和 Claude Code 并不是简单的取代关系，目前来看，二者会在不同的应用场景中展现出各自的优势：

**•**对于修改按钮样式这类需要快速提供 context 的简单场景，Cursor 的运行速度更快；

**•**对于需要理解数万个文件构成的大型代码库，或需要完成端到端的复杂任务的时候，Claude Code 会更加合适。

比如在企业日常开发环境中，Cursor 这类 Agent+IDE 的模式因为可以融合现有的工作流，更加用户友好，企业忠诚度也会更高，而在自动化场景中，Claude Code 这样的 CLI 工具更具优势。

**4. 现在的 Coding Agent 还缺什么？**

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/011.png)

1）**语音输入**

通过键盘输入冗长、结构化的文字指令，对普通人来说费时且困难。人类更擅长说话来描述复杂需求，而这恰好是 LLM 最擅长的。未来 coding agent 或许可以将语音作为主要的交互方式，用户只需要通过说话下达命令，AI 就可以理解并执行。

现在已经有开发者在 coding 时会使用转录工具，将语音直接转为指令，这很大程度上提升了开发的效率。

也有开发者认为，目前的语音输入技术能满足转录需求，但长期来看，考虑到 coding 任务的复杂性，效率较高的交互方式或许并不是单纯依靠语音输入，而是可以实现定向修改，类似在使用 PS 工具的时候，选中某一区域让 AI 针对性修改。

2）**GUI 编排异步编程**

GUI 编排异步编程也是一个值得发展的方向，比如，用户可以在一个画布上同时让多个 Claude Code 分别执行不同任务，并可以对任务进行终止或回退，在这种工作流下，用户扮演的是项目管理者的角色，这将大幅提升开发效率和灵活性。

**5. Demo 互动：搭建一个互动提问网页**

在分享过程中，黄航也演示了如何用 AI coding 工具搭建一个实时互动的 Q&A 网站，并对 Lovable 和 Claude Code 的效果进行了对比。

需要指出的是，Windows 系统下的用户需要先安装并切换到 Linux 命令行环境才能进行 Claude Code 操作，没有做原生集成这一点也是影响 Claude Code 市场渗透率的因素之一。

网站设计的 prompt 如下：

```
帮我开发一个观众 QA 产品：观众可以登录然后 Post 自己的问题每个 Post 的问题可以被点赞，问的 list 按照赞数从高到低排列，每个用户对每个问题只能点赞一次，也可以取消点赞合适的剧新机制，让现众能看到重新排列的 list赞数排列和交替位置的特效要比较 cool，除了数字以外，模向能有 bar 来展现赞数的多少效果
```

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/012.png)

Lovable VS Claude Code

从效果来看，Lovable 和 Claude Code 生成的网页在前端上没有显著差别，但是在后端上，Lovable 使用 Supabase 进行后端数据库的连接，但在上传问题时，Lovable 会显示报错，也就是说 Lovable 并没有成功连接数据库。而 Claude Code 通过 MCP 连接到黄航自己的产品 InsForge，交付的网页可以成功使用。

注：InsForge 是一个专门为 AI 打造的后端系统，能让 coding agent 自己连接和配置后端。在本次演示中，Claude Code 通过 InsForge 的 MCP 成功配置了用户登录和鉴权功能（authentication），并实现了数据库中的用户信息存储、 QA 点赞数记录以及排行榜的实时更新等功能。

Claude Code 配合上 InsForge 可以实现从 prompt 到应用的端到端流程，整个过程都在 Claude Code 界面中进行，并且始终通过 agent 完成。

左右滑动查看完整图片

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/013.png)

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/014.png)

Lovable VS Claude Code

**Part 2:  Claude Code 交互方式**

**分享人：**

**•**周弋涵：AI 创业者，探索用游戏化方式评估人类使用 AI 的能力

*注：这一 Part 的 deck 均由 Claude Code 生成*

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/015.png)

**1. Claude 的 CLI 交互体现了Anthropic 对自己模型 Coding 能力的信心**

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/016.png)

Claude Code 目前使用的交互方式，其实是 Anthropic 对自身模型能力更有信仰的体现。

Claude Code 的设计会让用户在修改代码的时候非常不方便，迫使用户减少手动改代码的次数，这有可能是 Anthropic 并不鼓励用户手动修改代码的体现，相比之下，使用 Cursor 等 GUI 的工具时，用户会不自觉地进行大量手动修改，频繁地接受或拒绝 AI 的建议。

**2. AI-native IDE 或许是伪命题**

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/017.png)

未来 GUI 很可能会继续存在，但未必是以 IDE 的形态。

GUI 本质上是在限制用户，通过编辑区、文件区、预览区等固定的区域，引导人类的操作，GUI 虽然牺牲了操作自由度，但也降低了人类在操作上的心理负担。

IDE 本质是对 shell line 的 wrapper，经过多年发展，IDE 在交互界面上积累了大量为了方便工程师手动编程而做的功能，比如语法高亮、一键运行、代码快速预览等，它更像是服务于工程师的“手套和铲子”，但 AI 其实并不需要这些“手套和铲子”。相比之下，CLI 可以更方便地被脚本调用，融入到自动化的 pipeline 里，AI 可以轻松地将多个独立的 CLI 工具串联起来，形成自己的工作流。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/018.png)

比如，Claude Code 只有 chat 这一种交互模式，在 IDE 界面可以做的所有事情现在都可以通过 chat 去做。这种自由对普通用户来说可能是一个负担，但对于需要高度定制化的人来说，是一个比较舒服的方式。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/019.png)

而且 AI 操作 CLI 比操作 GUI 容易，如果是 GUI，也就意味着工作流中需要拖拽，那开发方式就又变回人工手动了。因此比较好的产品开发方式是，先开发一个 CLI 让 AI 用起来，然后做一个方便与人类交互的界面，比如语音交互，从而实现优先优化 AI 对工具的使用，避免过渡优化人类对工具的使用。

在这一点上，有开发者指出，Cursor 基于 GUI，可以把对代码的修改分散到多个 tab 里，从而保持对话历史简洁，而 Claude Code 基于 CLI，修改记录只能嵌入对话历史里，在最初使用 Claude Code 的时候，由于用户对 Claude Code 不信任，会非常仔细地审查 AI 生成的代码，但随着对 Claude Code 信任度的提升，用户会更倾向于同时打开多个命令行，来并行操作多个项目。

**3. Claude Code 的产品形态是模型开发者工作习惯的映射**

Claude Code 之所以选择 CLI，与大模型开发者自身的工作习惯密切相关。Claude Code 原来是 Anthropic 内部使用的工具，相比用户体验，内部工具一般会更在意可定制化程度、可编程性和可组合性，也就是说希望这个工具在内部 pipeline 中是可以自动化的。

相比之下，Cursor 是 GUI，其实是没有办法自动化运行或可编程地运行。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/020.png)

此外，每个工程师都有自己的习惯，这和入行时间、工种等因素相关。比如，前端开发工程师大概率是使用 IDE 的，但模型训练工程师的工作天然就是异步、多线程的，他们习惯于同时开启多个命令行窗口，提交训练任务后便去处理其他事情，大部分时间都在等待而非实时交互，这样的开发者工作习惯造就了 Claude Code 的 CLI 产品形态。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/021.png)

**4. Demo：用 Claude Code 制作 ppt**

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/022.png)

将文档里的文字转成 ppt 的 prompt 如下：

```
use reveal js to create a slide using content from prm-163 in main branch
```

左右滑动查看完整图片

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/023.png)

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/024.png)

在第一版生成的结果中，文字都集中在了 ppt 上方。

左右滑动查看完整图片

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/025.png)

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/026.png)

为了进一步优化 ppt 排版，再次输入了如下 prompt：

```
use playwright to screen shot each page of @shixiang_main/index.html，如果内容都挤在上边，请你重新改一下排版，然后重新截图确认一下
```

第二次运行后，Claude Code 通过自行截图并进行图像理解，修正了之前的问题。

左右滑动查看完图片

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/027.png)

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/028.png)

**02.**

**Claude Code 是**

**第一个 L4 Coding Agent**

**1. 如何定义 Coding 领域的“L4 能力”？里程碑事件会是什么？**

Claude Code 在很大程度上已经达到了 L4 级别。

虽然 coding agent 需要的运行时间越来越长了，但开发者需要手动介入（如 Debug、审查、修改代码）的时间和精力大幅减少。**开发者的角色从先前的程序员变为了定期对流程进行监测和管理的指挥**出现问题的背后原因往往是用户自己提出的 prompt 不够清晰。

而且 L4 级别的 agent 不需要用户手动提供所有相关的 context，目前 Claude Code 就可以实现自主阅读整个代码库，在多个文件中自动寻找和理解完成任务所需的信息，然后进行正确的跨文件操作，这是它与像 Cursor 这样的上一代工具的区别。

有开发者提到，在 Claude Code 发布之前，即便 Windsurf 的工程质量和用户体验远低于 Cursor，但 Windsurf 却是他唯一一个即使明知有这些问题，仍然长期重度使用并持续付费的产品，就是因为 Windsurf 的 context awareness 能力极强，由此带来的开发体验要更好。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/029.png)

2024 年 11 月 21 日在 Windsurf 官网的截图

此外， Claude Code 不仅能执行计划，还能在执行中发现自身规划的漏洞并进行自我修正。比如 Claude Code 会发现自己出现了幻觉，应该先读取文件才能写入文件时，它会主动调整自己的行为顺序。这种反思能力是 L4 的重要体现，让用户可以更放心地将任务交付给它。

**2. Claude Code 的能力边界在哪里？背后体现了 coding model 和 coding agent 哪些底层能力的不足？**

相较于 Cursor 等产品，Claude Code 在能力边界上的拓展在于有拆解任务的 multi-agent 思维和 workflow 管理能力，能将一个复杂的 coding 任务，自动拆解成几十个更小的、专门的子任务，分派给不同的子 agent 去执行，最后再将结果整合。

也有开发者认为 Claude 和 Cursor 的核心差异并不在于是否是 multi-agent，而在于 context 理解能力有差异，进而导致 planning 水平有差异，最后导致交付结果存在差异。也有开发者认为 Claude 和 Cursor 的区别在于能否 parallel executation，但 parallel 理论上不能提升效果，只能提升效率。

总的来说，目前 AI coding 产品的不足在于对冷门或私有知识的掌握能力比较差。

因为 AI 模型的能力来源于 online 训练，本质上还是 pre-training 的状态，因此，它在主流、公开的技术（如 Web 开发）上表现出色，但对冷门的编程语言（如 Jsonnet，Scala）或公司内部的私有代码库的效果就很差。

而要突破这个边界，需要让 agent 具备调用外部知识库的能力。像给游戏机插上记忆卡，为 agent 提供一个即插即用的知识库（如某个特定库的文档、某个行业的专业知识），让它能瞬间获得特定领域的专业能力，从而极大地扩展其应用的能力边界。

**3. Coding agent 能力达到 L4 后，下一个机会会在哪里？**

当 AI 写代码的能力足够强时，下一个机会将会从代码生成，转移到代码的运维部署和交互优化。

**•****自动化代码后端的运维与部署**

DevOps 这类工作目前仍是人力密集、繁琐且易错的重灾区。AI 写代码的效率越高，后端运维的压力就越大。这需要深度的行业知识，是纯粹的 coding 能力无法解决的。痛点在于怎么让模型使用工具来自主完成这种任务，让它们能自动化处理像 AWS 这类主流云平台的云服务配置、持续集成/部署（CI/CD）。

因为配置云服务是一个极为复杂的任务。如果一个游戏公司要搭建测试集群，需要专门的工程师花费数天时间进行复杂的配置、连接、权限设置和调试。这个过程不仅耗时，而且高度依赖个人经验，一旦该工程师请假，工作就会停滞。而通过 agent，可以将这些复杂的的任务，简化为一句话指令，agent 就能自动完成所有后续工作。

因此，能跨所有主流云平台（AWS、GCP、Azure）实现上述功能的 agent 将会很有市场。因为人为配置的系统，即使能用，也往往不是最高效的。人类的精力很难对庞杂的系统进行持续的、精细化的监控和优化。比如有创业团队在内部配置了 AWS，过了很久才发现每月多花了 10 万美元，只是因为没有关闭一个不需要的功能。

**•****人机交互层面的优化**

不同的人用 AI 的效果是有差异的，未来 1-2 年，会用 AI agent 将不再是优势，但不会用 AI agent 将成为劣势，就像招聘的时候，如果候选人不会用电脑，那大概率是不会得到录用的。

有一位开发者曾为了测试 Cursor 和 Windsurf 的能力边界，去开发了一个飞机大战游戏，结果发现 AI coding 工具在数值设计等复杂场景效果不佳，还是需要人类专家的 know how，因此如何能准确描述自己的需求预期会极大影响 AI coding 工具的使用效果。

因此有一个机会就是帮助非专业用户去发现自己的需求并将用户的需求结构化，比如有开发者之前想开发一个访谈式 AI，通过对话和实时构建原型产品来帮助用户澄清和定义需求。

**4. Coding Agent 会不会像 Siri 一样成为未来操作系统的附属功能？**

从构想来看，AI agent 或许不会成为操作系统的附属，相反，未来的 OS 可能会成为 AI agent 的附属，甚至可以说 LLM 本身就是新的 OS。

Coding agent 本质上是一个能通过写代码完成任何任务的通用问题解决器。只要用户向 agent 输入一个任务，agent 就会自行决定是调用现有功能，还是通过即时 coding 来完成任务。比如欧美的 AI-native 初高中生已经把 ChatGPT 作为解决一切问题的主要入口，无论是搜索还是情感陪伴。对他们而言，ChatGPT 在功能上已经扮演了 OS 的角色。

但对未来的长期预测是非常困难的，因为 AI 领域发展非常快，任何超过一两年的推演都存在巨大的不确定性，讨论的过程中应该更尊重短期事实，而对长期预测保持谨慎。

**5. 从用户体验角度，开发者最希望 Claude Code 支持的功能是什么？**

未来的方向应该是 multi-agent 并行开发。重点是将开发者从繁重的执行工作中解放出来，开发者只需要将执行任务分派给 AI，自己则可以专注于更高层次的产品设计、架构规划和项目管理。

这事的难点在于 multi-agent 之间的通信与内存共享，需要确保 agent 在协作时能够同步状态。现在可以通过一些手动操作来模拟简易的并行开发，但这并非原生支持，缺乏真正的内存共享。

在人应该如何与 AI 进行日常交互的这个问题上：

**•**支持 GUI 的开发者认为，在拖拽式添加文件、配置 API、查看变更等日常操作上，GUI 比输入繁琐的命令行指令要直观和高效得多，比如添加 MCP 时只需要将网络上的代码直接复制到 GUI 中，因此在大众软件开发上，纯 CLI 会是一个缺点。目前比较理想的状态是在 IDE 中集成并使用 Claude Code 的强大能力，形成一个 GUI 外壳 + CLI 内核的混合模式。

**•**支持 CLI 的开发者认为，真正的效率提升，不应该是让人更快地完成某个步骤，比如手动粘贴 MCP 配置，而应该是让 AI 自主完成配置的全过程。用户无需学习如何配置，只需向 AI 下达做什么的指令，不用关心实现细节，这才是 CLI 的价值所在。给 Claude Code 套一个 GUI 的壳是不难的，但让 GUI 把全部底层功能用 CLI 或者 MCP 开放出来，是比较难的。

**03.**

**Anthropic 可能会是 Vibe Coding 的 AWS**

**1. 如何看待 Lovable 等 vibe coding 产品长期价值？**

 

Lovable 的技术护城河其实已经消失了，原因在于：

 

**•** Lovable 依赖大量硬编码的工具和流程来构建应用，这使得 Lovable 在面对复杂场景，或者调用像 Supabase 这样的外部工具时非常脆弱，很容易出现连接失败的 bug。相比之下，Claude Code 能通过 MCP 动态地调用后端服务。

 

**•** Lovable 作为 vibe coding 产品最大的亮点是能快速生成漂亮的 UI。但今天用户完全可以通过给 Claude Code 输入一个特定的 prompt，例如要求 Claude Code 把 UI 生成的更好看一点，也就是说 Lovable 最大的亮点已经可以通过优化 prompt 被 100% 复现，并且随着模型能力提升还能比 Lovable 做得更强大。

 

**•** 虽然 Lovable 作为一个 web，可以不需要任何的下载配置，但长期来看，任何人都可以把 Claude Code 部署到 web 上去实现。

 

目前有一种趋势是，产品经理、设计师等非专业开发人员会倾向于使用 Lovable 这类简单直观的工具，而专业开发者则会使用 Cursor 或 Claude Code。

 

考虑到给专业开发者和完全不会代码的人做产品，在产品优化的方向上可能不同，因此 Lovable 这类产品未来更明智的商业路径应该是基于 Claude Code 这类强大的底层 agent 进行封装，做好底层模型不会优化的环节，比如做项目的分发与消费，成为专注于作品分享的创作者平台；帮助用户在 coding 前理清思路，做构思和 prompt 生成的助手等。

 

此外，Claude 的 Artifacts 功能也会对 Lovable 和 Bolt 这类产品产生很大的冲击，未来 3-5 年，用户最关心的是 AI 工具能不能交付一个高质量、可迭代的产品，产品越复杂，意味着对底层 coding agent 的能力要求就越高，而 Claude 凭借强大的底层模型，就会有竞争优势。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/030.png)

Anthropic 在上周更新了 Artifacts 功能，用户可以在聊天界面里直接生成、预览、编辑和运行代码，相当于把“AI 原型开发工具”整合到了对话里。

**2. 在 ToC 场景中，AI coding 产品需求卡点在哪？**

第一个卡点在于需要对产品做大量的体验优化。大众用户需要傻瓜式的体验，所以要将所有复杂技术都封装起来。

Claude Code 还有很多人没有用的原因就在于安装和使用方法不太完善。这一点 Anthropic 未必会自己花精力做，**它有可能会选择扮演新时代 AWS 的角色，只提供核心模型能力并收取订阅费用**，让其他公司在它们的模型基础上封装简单易用的 ToC 产品。

第二个卡点在于部署环境。

AI coding 在技术上已具备渗透 ToC 市场的能力，但 ToC 的核心需求多是临时、具体的需求，需要即时生成一次性的软件。比如用户如果想下载某个 Youtube 上的视频并总结内容，AI 会即时生成一个脚本，调用 yt-dlp 和 whisper 等工具完成任务，这个脚本是一次性的。AI 生成代码后，普通用户可能没有能力在本地配置环境来运行它。

因此或许需要提供一个 Sandbox 或云，让 AI 生成的一次性软件可以更方便地运行。在这个模式下，**代码本身变得廉价，而清晰的需求和测试用例变得更有价值。**

真正的 ToC 产品爆发点可能在于，每个人都可以为自己创造一次性或高度个性化的应用。个人自用型 APP 可以绕过分发和商业化问题，比如开发个人邮件系统，在用户开车时帮助总结邮件内容，通过语音交互安排日程或回复消息。

**04.**

**Coding Agent 的内核理念比前端形态更重要**

**1. 如何从 Gemini CLI 的不足中反向理解 Claude Code 的优势？**

**•****人才聚集效应**

在 Claude 3.5 模型展现出极强的 Coding 能力后，Anthropic 就将几乎所有资源都倾注于 coding，而并没有像其他大厂在图像、视频等多个领域分散精力，而 coding 作为目前 AI 最明确的落地场景，也吸引了顶尖的 AI coding 人才向 Anthropic 聚集，形成马太效应，进一步加强了 Claude 的壁垒。

**•****清晰的产品审美**

此外，Claude Code 的 CLI 设计背后有清晰的产品审美，但 Gemini CLI 没有，Gemini CLI 的不足主要源于 Google 急于推出这个产品。它既缺少了 Compact mode，也缺少 Headless mode，在 context window 和 command line 的可交互性上都有欠缺，产品逻辑不清晰。

**•****头部 AI lab 内部 AI coding 最佳实践的积累**

Claude Code 在公开发布前，已经作为内部工具得到了 Anthropic 团队的长期使用和优化，体验和效能都非常成熟，而 Gemini CLI 的 GitHub 首次提交在 4 月底，缺乏产品的打磨，只是为了市场竞争，利用了大厂的免费策略进行推广。

即使在开源的 GitHub Copilot CLI 中更换底层模型并补齐相应的功能，也是难以真正复刻 Claude Code 的体验。因为 Claude Code 的 agent 流程和各项功能都是专门针对自家模型深度优化的，GitHub 若替换底层模型，这既不符合 Claude 的利益，也会导致兼容性和性能折损，像用 5 号电池的转接头去适配 7 号电池的设备，虽然可以勉强运行，但无法达到最佳效率和性能。

**2. Cursor 未来是否可以进化到以任务为交互的方式？并且增加 GUI 进行产品迭代从而增强开发者粘性？**

目前 Cursor 可以通过 background agent 来实现这个功能，但用户已经可以通过开启多个 Claude Code 的终端来达到类似的多任务并行处理效果。Cursor 在这方面并没有很强的壁垒。

而且在 coding 领域，**Claude Code 与 Cursor 其实并不能完全用设计行业的 Canva 和 Figma 对比，底层 coding 的通用性会导致开发者在不同 coding 工具间的迁移成本极低，市场会更偏向去整合，并不会存在 niche 市场。**

**3. 如何看待 Claude Code（类 iOS 的封闭生态）和 Gemini CLI（类 Android 的相对开放生态）的区别和未来？**

**Agent 的内核能力比前端形式更重要。**

有开发者提到自己最初是因为看重 GUI 的便利性而没有使用 Claude Code，但重度使用这些 coding 产品后发现，Claude Code 的核心优势其实在于 agent 的能力本身就已经远超 Cursor 这样的竞品了，这比前端是 CLI 还是 GUI 更为重要。

但 GUI 和 CLI 并非互斥，可以在 CLI 上加一层 GUI（如在 IDE 中使用）来达到最佳效率，**但归根结底，用户最终会选择效果最好的工具，而不在乎其形式。**

Anthropic 做产品一直是闭源状态，有自己的审美，有点 IOS 的感觉，Google 的特点总是起了个大早，赶了个晚集，但凭借雄厚的资金，总能慢慢追上，就像当年 GCP 追 AWS。

但需要承认的是 Google 的长期优势在于拥有云服务和自家顶尖模型的完整生态，成本控制能力极强，无需向外部模型厂商付费，Google 模型能力的体现在，**Gemini 2.5 Pro 在某些任务上的幻觉率可能是最低的。**

**4. Claude Code 生成的代码的幻觉率有多高？**

Claude Code 的幻觉率极低，因为 agentic flow 具有工程上的自主纠错能力，通过详细的 To-do list 和自我修正机制，在工程层面解决了底层模型的传统幻觉问题，能把跑偏的模型拽回来。相比之下，Cursor 会经常出问题，在复杂项目下，出现问题的概率大概是 30-50%，需要人及时查看检查。

此外，Claude Code 的幻觉可能更多表现在：

1）生成冗余代码或文件，也就是说虽然代码能跑，但不整洁高效，用户需要主动去提醒它定期扫描并 Refactor 代码库；

2）修改范围超出预期，比如在修改功能 A 时，意外地改动了功能 B 的相关代码。

有一个减少幻觉率的 Claude Code 使用技巧是，开发者可以在处理下一个不相关任务前，及时清空当前的历史记录，因为模型的性能在长对话中会断崖式下跌，因此，需要解构相互不影响的独立任务。

在任务复杂度上，Claude Code 已经能处理远超 CRUD（创建 create、读取 read、更新 update、删除 delete）的复杂任务。比如整合两个不同的大型开源项目时，代码量会高达几十万行，用户要求 Claude Code 理解两个项目后，通过替换核心组件将它们结合，Claude Code 能够成功完成了主体连接，整体表现能达到 75-80 分。

而对于纯算法问题，比如在特定约束下优化矩阵算法，只要能提供足够好的测试用例和明确的优化指标，Claude Code 也能够很好地学习和胜任。

**05.**

**AI Coding 的**

**终级赢家会是谁？**

**Coding 这个领域的赢家一定会是 LLM 的模型提供商，其次是云服务厂商。**因为他们在产业链上的位置更具话语权，同时云厂商拥有巨大的成本优势，比如 Amazon 内部正在开发的类似 Cursor 的产品，定价（20 美元/3600 次请求）远低于 Cursor（20 美元/500 次请求）。

因此，真正具备长期竞争力的，将是那些能够深度整合先进大模型和云计算基础设施的玩家，比如 Google（GCP+Gemini）、AWS 与 Anthropic。微软和 OpenAI 虽然曾紧密合作，但近期各自的重点也在分化，OpenAI 正将更多精力投入到泛娱乐和泛应用领域。

在中国市场，国内最顶尖的科技公司为了追求最佳的交付效果和全球竞争力，可以使用顶尖的海外模型进行开发，但对于大多数人，比如中小型企业，阿里云和通义千问会是一个值得关注的组合，海外产品因为地缘政治问题难以进入，而阿里云可以结合口碑不错的通义千问模型，切入这个市场。

此外，字节拥有海量的视频和语音数据，这使字节在多模态 AI 的研发上限很高，可能在特定领域超越阿里，比如在手势模型方面，阿里只有约 11 种，而火山的手势模型有高达 37 种，这种差距在复杂度和飞轮效应方面可能会越来越大。

不过，也有人认为，字节的优势在于产品工程能力，底层语言模型的能力一直未能领先。优秀的多模态产品更像是堆工程的结果，而非基础模型的突破。

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/031.png)

排版：夏悦涵

延伸阅读

[![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/032.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514422&idx=1&sn=be5cceb8d96e2b9a300ca353d4c97d1c&scene=21#wechat_redirect)

Jack Clark: 美国 AI 政策的隐形推手，时代的良心还是囚徒？

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/033.png)

[![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/034.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514384&idx=1&sn=4150d9e5bc851d09a23f519b825521f3&scene=21#wechat_redirect)

Cluely：最具争议的 00 后 AI 创业者，用一款 “作弊神器”2 个月实现 600 万美金 ARR

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/035.png)

[![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/036.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514353&idx=1&sn=a2dfe3b5f7c67c2e3ea1b4eb03b26fb0&scene=21#wechat_redirect)

OpenAI 研究员 Noam Brown：Mid-training 是新的 pre-training

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/037.png)

[![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/038.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514318&idx=1&sn=fabf9ae395300b08039d5c4545b5643b&scene=21#wechat_redirect)

从 Co-pilot 到 Agentic AI，Sierra 如何改变客服的游戏规则

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/039.png)

[![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/040.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247514277&idx=1&sn=e66a0f2624855871a754adf86393d1f2&scene=21#wechat_redirect)

FutureHouse 联合创始人：AI Scientist 不是“全自动化科研”

![](../images/2025-07-06-10x-cursor-kai-fa-ti-yan-claude-code-ru-he-dai-lai-ai-coding/041.png)
