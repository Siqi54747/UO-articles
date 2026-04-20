---
title: 'Stripe x Cursor，硅谷两代“金童”对谈: 未来5年IDE里将不再是代码'
publish_date: '2025-09-18'
publish_timestamp: 1758197135
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/uXtbtbSZEtV64_M68DDDKg
msgid: 1000000423
appmsgid: 2247518145
itemidx: 1
digest: AI 改变的不是 IDE 而是“编程语言”
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzico8ykY6CicDz1ZWrINQctrAy4ly3yzAymUAA7ia8YDk99yLHVx0bdhQUicEALib6Lv8BNHCweLZZW4Q/0?wx_fmt=jpeg
image_count: 15
archived_at: '2026-04-20T04:25:05+08:00'
---

[![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1)

![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/002.png)

编译：Yangqi

![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/003.png)

本文是 Cursor CEO Michael Truell 和 Stripe CEO Patrick Collison 的深度对谈。Patrick 和 Michael 都被硅谷视为“天才少年”：两位创始人都在大学辍学开始商业探索，Stripe 和 Cursor 又恰好都是他们在 22 岁时创立，并且都快速成为 cloud 和 AI 时代的重要公司。

作为成功创业者，Michael 和 Patrick 至今保持着一线技术视角。在本篇对谈中，他们也讨论了 Stripe 的技术实践、编程的未来。

**•**Patrick 很早就在技术前沿做探索：用 Lisp 语言写 AI chatbot，用 Smalltalk 搭建了第一家公司……

**•**LLM 对 IDE 的改变应该是一个真正的开发环境，不仅仅是一个文本编辑器，真正的 AI  IDE 中将不存在“编程语言”，更多是开发者描述需求；

**• 创业公司的早期技术选型往往很随意，但同时又会带来深远影响，Stripe 的技术核心是 **Ruby（今天仍是 Stripe 的主要语言） 和 MongoDB ，为了让 MongoDB 符合金融级别的响应和可靠性，Stripe 工程师团队在 infra 上投入了大量精力；****

**• AI 的一个重要价值是持续重构与美化，降低大规模代码库的修改成本，**代码库的“重量”是衡量 AI 是否有用的标注之一；****

**•**Patrick 在日常生活中更多把 AI 用于偏事实与经验性问题，以及代码写作上；

**•**在访谈中还首次公开了 Stripe 正在进行的 V2 版本 API 重写计划，**Stripe 的 v2 API 用统一的数据模型减少特例，强调“能统一的尽量统一”。**

![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/004.png)

**01.**

**Patrick 的早期技术实践**

**Michael Truell：****我听说你的第一家创业公司是用 Smalltalk 语言编写的？**

**Patrick Collison****：**因为在我看来它就是最好的编程语言。我以前写过 Lisp 和它的变体，也做过 Lisp 的 Web 框架。我们第一次创业是用 Ruby on Rails 起步的，但和 Lisp 的体验一比，我觉得那个开发过程挺让人挫败。细节就不展开了。当时我坚信续延式（continuation-based）Web 框架才是做 Web 应用的正路，但可惜 Ruby 生态并没有这种框架。

Lisp：Lisp（LISt Processor）是一系列编程语言的家族，1958 年由约翰·麦卡锡提出，是仍在使用的最早的高级语言之一。它的核心特点是“用表（list）来表示一切”，代码本身就是数据，因此非常适合做元编程与构建领域专用语言。

Ruby: Ruby 是 1995 年由松本行弘（Matz）在日本创造的动态、解释型、纯面向对象语言，核心理念是“开发者幸福感”和可读性。最具代表性的生态是 Ruby on Rails Web 框架，它曾大幅提升 Web 应用的迭代速度并带动活跃社区。

Small talk: Smalltalk 是 1970 年代 Xerox PARC 由 Alan Kay 等人创造的纯面向对象语言兼“活”开发环境，一切皆对象，靠消息传递交互。强调实时和交互式开发：在程序运行时即可修改对象与代码并继续执行。

我到处寻找方案，发现有个不错的框架是用 Smalltalk 写的，就先上手试了试。结果很快发现，Smalltalk 不只是语言，它还是个特别有意思的开发环境，保留了我在 Lisp 里最欣赏的东西：完全交互式环境（interactive environment）和像样的调试器（debugger）。你可以在处理某个 Web 请求（web request）的过程中，甚至在很深的堆栈跟踪（stack trace）里直接改代码。比如请求里报错，你改好后在更高一层栈帧（stack frame）处恢复执行，整次请求就能跑完。

这个过程就不用走之前那套烦人的流程：先加日志（log statements）、靠二分法（binary search）排查、再部署修复，可能一小时才搞定。而在 Smalltalk 里，只需检查栈帧，找到值不对的变量，改完跳回去点继续（proceed），流程就能顺利跑通。

在寻找这个基于延续式的网络框架的过程中，我意识到 Smalltalk 在开发环境方面，通常比 Ruby，或者说比其他所有主流编程语言都强大得多。

所以我们决定将它用在了公司产品搭建上。事后看来，我其实不知道这是不是一个糟糕的决定。我认为大家会觉得它很糟糕的原因是，会使用这样冷门编程语言的人很少, 因此你会很难招聘到合适的人，也很难扩展，诸如此类。但事实并非如此，人才招聘并不难，或者说没有人知道它，但很容易教会他们。所以我不认为这是一个不使用非主流语言的理由。

我第一次创业最后没做成，我更倾向归因于点子本身不够强，而不是编程语言和技术栈选择。我们在 Stripe 也用了 Ruby，这也说明 Smalltalk 带来的边际收益没我当时想得那么大。

**Michael Truell：****你最早的项目之一是用 Lisp 写的一个  AI bot，它的形态很像一个 MSN 客户端, 而且你当时还想让它通过图灵测试？**

**Patrick Collison：**是的。这个项目当年一度很流行，它本质上是个非常简单的贝叶斯  next-word predictor，谈不上多复杂。

但比较特别的是：它的训练数据来自它自己在 MSN 上的对话，而不是通用文本语料库（text corpora）。效果还可以，更好的版本会向前多看几个词。严格来说，它从未在“对方有防备、刻意分辨”的场景下通过图灵测试，但在一些“毫无戒心”的场景，人们确实会和它聊上相当久。

这件事也把我带进了 Lisp 的世界。Peter Norvig 的 Paradigms of AI Programming 对我启发很大，书里几乎没讲神经网络（neural networks）。我读过 Marvin Minsky 的 Society of Mind 等，但并没有认真做过神经网络实验。

但我在遗传算法上做了很多尝试，在当时的 PC 上，这比训练神经网更加可行。我甚至写了一个遗传优化器（genetic optimizer）去搜索“最优键盘布局”，结果基本指向 Dvorak 键盘布局，我和我弟弟 John Collison 都在用 Dvorak，所以几乎没人能用我们的电脑。

总体上我在遗传算法里钻得很深，但几乎没碰神经网络，这大概也是我没有做出 ChatGPT 的原因。

**Michael Truell：****你在之前一段访谈里提到过喜欢 Smalltalk、Lisp 这些语言的特性，并预测接下来主流的 C 语言会越来越多地借鉴过去这些“老编程语言”的思想，这件事今天在 JavaScript 和 Python 生态里已成事实。你觉得在那些“冷门”编程语言中，还有哪些被低估、值得主流借鉴的点子？**

**Patrick Collison：**有的。很有意思的是，许多想法竟是通过 Web Inspector 这种“曲线通道”进入 JavaScript 生态的，那其实成了多数人最常接触到的丰富的运行时（runtime）之一。就标准而言，我确信 ECMAScript 没有一等栈帧（first-class stack frames）（也许某些非常规扩展能做），而“一等栈帧”能解锁很多能力，这里不展开。

更普适的观点是：把开发环境而不是纯文本编辑器当成核心。这在Lisp machines、Mathematica、Smalltalk 中都曾经存在。我们今天把运行时、文本编辑和代码运行的环境割裂开有可能是错的，因为这三者完全可以共存。

直到今天，我仍大量使用 Mathematica，不是为了做多么深奥的符号数学，而是因为它带来更高效的开发体验。当然，随着 LLM（大型语言模型） 的出现，这点可能在变化，因为 Mathematica 还不支持 Cursor 那种提示式开发（prompted development）。我希望大家能更进一步：比如鼠标悬停到一行代码时，直接看到该函数或者代码的运行时特征（runtime characteristics）与性能分析（profiling information）；悬停到变量时，叠加显示日志（logging）、错误信息（error information），以及它在生产环境（production）的常见取值。这种深度集成（integrations）才是我期待的方向。

**02.**

**5 年后的 Cursor 长什么样？**

**Michael Truell：****你日常是如何用 AI 的？**

**Patrick Collison：**我用 LLM 的方式比较常规：主要拿它们来解答我感兴趣的事实性和经验性问题。至于深度研究式问题，因为现在模型的工具调用与自主网络检索能力更强了，其实很多时候不需要专门做深度研究。

写作方面我其实一直不太满意 AI 的结果，无论是代写还是润色、 点评我的文章，AI 的产出常常显得很平庸。不过我想强调我不喜欢 AI 写作并不是我写得多好，而是我的个人风格和今天 LLM 得默认风格确实不太合拍，在写作时我更想保留自己的声音。

比如我读书时会开启 Grok 的语音模式，一边阅读一边随口发问，它在后台静默聆听并即时作答，很有帮助。写代码我也经常用 LLM ，通常基于 Cursor 来使用。

 **Michael Truell：****很多模型的写作风格确实出奇地重复。我也试过通过提示来避免这种千篇一律，让它多引用具体人物与细节，但效果并不稳定，这点挺让人失望的。**

**Patrick Collison：**有人说基础模型（base models）在写作上更好，而基于 RLHF 微调后的模型会导致一种规范化（normification），把输出拉向某个特定风格。就我个人而言，暂时还没把它们用出特别理想的写作效果。大家常说 Claude、O3 比早期 OpenAI 模型在写作上更强也许是真的。

 **Michael Truell：****Curosr 会做一个真正一体化的 IDE 吗？**

**Patrick Collison：**我们在试着把 AI 更多地放到后台去“想”，把想法当代码跑、看输出再反应，同时跟前台工作无缝协同。

我们特别强调 in-flow（不中断流程）、速度和控制感：让程序员始终掌控、看懂 AI 产出的每一处细节，并保持超快的迭代循环（iteration loops）。

程序员最怕等，某些场景下，可以让 AI 先想一阵，再把结果带回来，那时的 API 更像和同事协作：它先给你一个 70% 完成度，你拖到前台快改，随后再丢回后台继续跑。

要让这种“后台思考”有价值，AI 得能实际运行代码并对结果做出反应；否则就只是盯着自己写的东西发呆。

**Patrick Collison：****再过 5 年，我在 Cursor 里主要看到的还是代码，还是别的东西？**

**Michael Truell****：** 我觉得更可能是别的东西。

简单说，软件有两块：一块是逻辑组件（logic component），工程师花很多时间定义“它到底怎么工作”；另一块是视觉组件（visual component），尤其对有 GUI（图形界面） 的终端应用（end user applications）。

我猜未来我们跟 AI 的互动，不再把它当“可委派的人类助手”或“站在肩膀上提示下一步”，而更像编译器（compiler），或者解释器技术（interpreter technology）的进化。这可能会推动编程语言本身改变：更不拘泥形式、更高抽象层级，强调说清你要什么，而不是细写怎么做。

我认为未来的编程会更不拘形式、有更高的抽象层级，更多表达“你要什么”，更少描述“怎么做”。

它未必会变成 Google Docs 那样的文档形态；有些“编程资产”仍应保留，比如对逻辑的命名（naming of logic）并在多处复用。另一个关键维度是软件的视觉呈现（visuals of software）：我相信软件开发、编程会走向一个让 UI-based 直接操作发挥更大作用的世界。当然，这些还带有一定的前瞻与试验色彩。

总体来说，真正让我在意的是：过去 20 年，我们在编程范式上的探索并不多。

我们现在讨论的很多想法可以追溯到 70–80 年代。虽然开发者数量比以往多得多，但实验的广度并未同步扩大。JavaScript 生态做出过不少酷的尝试，在语言层面也出现了 Rust、Go 等创新；但在开发环境层面，不知是因为难度或复杂度，实际实验仍少于预期。

一方面，AI 对于我们就像突然多了一整套全新的“颜料”可以创作。另一方面，编程语言里有很强的锁定效应：

**1.**一是大脑层面的“肌肉记忆”，语言本身就是程序员精确定义计算机行为的复杂用户界面，学会一门后很少愿意频繁改；

**2.**二是企业资产层面，当大量业务逻辑已经用某种语言写好，你就必须长期维护它。

我还觉得，随着 AI 编程越来越强，会暴露出一个现实问题：在专业应用（professional applications）里，几百人维护上百万行代码时，代码库的重量（weight of the codebase）会让人喘不过气。新项目一开始都很顺手，但规模一上来就变成这里一改、那里就崩，最后容易滚成一个巨大的泥球（big ball of mud）。把这份重量降下来，让改动更轻松，我认为正是 AI 能把编程变得更好的重要方向。

**Patrick Collison：**我今天在 Twitter上看到一句话。大意是：用提示让模型写代码是一回事，而让 AI 去做代码库的优化与重构又是另一条很有潜力的路。比如可以想象：白天我们产出了一些还不够优雅、抽象不到位的实现，夜里有个系统在背后自动清理、提炼抽象、重组依赖。

我上过的唯一一门计算机科学课是 Gerald Jay Sussman 的 Large-Scale Symbolic Systems（大型符号系统）：核心在于构建易于修改的代码库、环境与抽象（abstractions）。课堂上没有从零开始的作业，所有作业都是在改造现有系统。我很认同这点，关键是让修改变得简单，哪怕是很深的修改。当然，现实里受制于交付压力，你常常明知“该用更漂亮的做法”，却没时间重构。如果有个 AI 能在我们身后把欠账补齐、把架构清理干净，那就太理想了。

**Michael Truell：****你会对 Cursor 提哪些建议？不论是作为你个人还是站在公司角度？**

**Patrick Collison：**Stripe 内部已经有数百名、很快到上千名的高黏性大家普遍反员工在使用 Cursor，大家都提到了生产力显著提升。仅从我个人视角看，我会在意以下三点：

**1.**运行时特性与一体化（runtime characteristics & integrations）：把运行时画像、性能剖析（profiling）、日志、错误（logging、error）等信息和代码体验深度融合。当我悬停或浏览某段代码时，能直接看到它在真实环境中的时延、吞吐、错误率、常见变量取值等。这类端到端集成对工程效率非常有价值；

**2.**重构与美化（refactoring & beautification）：让 AI 像夜间清道夫一样，自动把日间产出的零散代码收束成更优的抽象与结构，降低未来改动成本，持续提升架构质量（architecture quality）。

**3.**工艺与美学（craft & beauty）：我们非常在乎软件的工艺与美感：不仅是像素层面的顺手，更是深层的稳定、可托付的“设好就能放心忘记”。一个现实担忧是 AI 可能催生更多平庸粗糙（slop）的产物，而不是更多最好的软件。我不确定 Cursor 能怎样直接解决这点，但如果能推动行业产出更多一流作品而不仅是更多作品，那会是非常重要的贡献。

**Michael Truell：****什么时候我们才能对人类生物学（human biology）进行编程？**

**Patrick Collison：**我对个人对  Arc 在做的工作非常兴奋，我参与了它的创建。我们在做两件事：一是用 DNA 等多模态数据训练生物学基础模型（foundation models for biology）；二是研发一个虚拟细胞（virtual cell）。

投入这块之后我才真正意识到：人类从未治愈过“复杂疾病（complex disease）”。粗分的话，疾病大致有三类：

**•**传染病（infectious diseases）：如流感、感冒、新冠、结核等；

**•**单基因病（monogenic diseases）：由单一基因突变（genetic mutation）致病，如亨廷顿病（Huntington’s）；

**•**复杂疾病（complex diseases）：在我们基本攻克多数关键传染病（至少在西方世界）之后，剩下的大头——如大多数心血管疾病（cardiovascular disease）、癌症（cancers）、自身免疫疾病（autoimmune disease）、神经退行性疾病（neurodegenerative disease）等。

其中有些我们有有效治疗（比如他汀治疗心血管风险），但谈不上“治愈”，我们既未完全掌握其因果通路（causal pathways），也做不到像接种疫苗那样从机制上解决。

我们的假设是：之所以卡住，部分原因在于过去缺乏与问题规模匹配的实验与认知技术（experimental 、 epistemic technology）。一方面，基因的多效性（pleiotropy）让单个基因影响到身体多个系统、细胞内多条机制，呈现巨大的组合复杂性（combinatoric complexity）；另一方面，环境因素既广阔又难以量化（quantify）。这两者叠加，使得我们很难真正搞清这些疾病的病因学（etiology）与动力学（dynamics）。

但过去约十年里（很多关键进展集中在这段时间），生物学迎来三类“读-想-写”的新工具：

**•**读（Read）：高通量测序技术（sequencing technology）、单细胞测序（single-cell sequencing），以及对 RNA 的单细胞层面读出，读取能力大幅提升；

**•**想（Think）：神经网络与深度学习（neural networks & deep learning）的跃迁，尤其是 Transformer 带来的表征与推断能力进步；

**•**写（Write）：功能基因组学（functional genomics）、CRISPR，以及碱基编辑（base editing）等定点扰动（perturbations）手段迅速成熟（Arc 也在推进相关方向）。

把这三类能力耦合起来，我们就在单细胞（single-cell）层面具备了“读—想—写”的闭环，这开始让人感到像是一种新的“图灵环（Turing loop）”，而且具有自身的完整性。接下来能在多大程度上攻克复杂疾病、这种系统化范式是否真的胜任，还有待验证，但我们充满希望，也非常兴奋。

**03.**

**Stripe 的技术理念和 Infra**

**Michael Truell：****许多开发者在自己的职业生涯中会开始转做 engineering manager 、总监，甚至自己创业，日常工作从写代码变成了协调人与人的协作。在你看来，编程里的哪些理念能迁移到组织层面的编程？**

**Patrick Collison：**我们需要重视 API 和数据模型（data models）。如果让我把 Stripe 重做一遍，细枝末节会改无数，大方向也有调整，但我最确定会投入更多时间在 API 与数据模型上。

原因之一是康威定律：这两样不仅会塑造组织结构，还深刻影响组织的运作方式。如果你没有深刻内化这点，你对组织动态的掌控就会比你期望的要少。

Conway’s Law: 1968 年 Melvin Conway 提出：“设计系统的组织，其产出的设计会复制该组织的通信结构（communication structures）。” 也就是：你公司里人是怎么分组、怎么沟通的，最终做出来的系统就会长成那个样子。

我经常思考的一件事是， iOS 软件生态系统在很长一段时间内，而且很可能直到今天，都比 Android 应用生态系统更有活力、更重要、更成功。这两个生态系统之间有很多不同的地方，我相信今天使用的 Android 设备量比 iOS 多得多。但 App 开发者往往更倾向于喜欢基于 iOS 开发 App、并选择在 iOS 上首发，甚至有时候 iOS 版本比 Android 版本更好。所以，我认为这是一个正确的 API 设计、正确的抽象设计最终产生了相当大的商业影响的案例。

也许这件事也不值得深究，因为技术的一切都变化得如此迅速、我们做的任何假设都会在两年内过时。但在实践中，这并不是真的，正确的 API 设计和正确的抽象到正确数据模型确实可以持久。在 iOS 的第一个版本中，人们使用的许多类都以 ns 为前缀，这当然代表 Next Step。所以这是一个 API 设计持续了二十年甚至更长时间的案例。

NS 是苹果早期操作系统 NeXTSTEP 的缩写，用作 Objective-C/Cocoa 框架的类名前缀，相当于一种历史沿袭的“命名空间”。你在 iOS/macOS 里看到的 NSString、NSArray、NSDate 等都源自当年的 Foundation/AppKit 设计，用前缀来避免命名冲突。到了 Swift，面向 Swift 的类型通常不再带 NS（如 String、Array），但 NS\* 类仍广泛存在并与之互操作，体现了这些 API 设计的持久性。

在 Stripe 的案例中，Stripe 现在已经有 15 年历史了，我们 15 年前设计的很多东西至今仍在被使用，这在某种程度上是好事也是坏事，因为它们经久不衰，但我们也仍然在承受它们的缺点。

**Michael Truell：****我曾和硅谷一家很成功的工程负责人聊过，他们的代码库用的是 Scala 语言，这个选择其实是团队创业早期创始成员们随手做的技术决策，但后来却影响了团队数百名工程师，对应到 Stripe，你们是否也有类似的例子？哪些早期决策在今天仍旧产生着重要影响？**

**Patrick Collison：**对于 Stripe 来说，类似于“定海神针”一样的技术选择可能是：一开始我们就选了 MongoDB和 Ruby，它们至今还是 Stripe 的重要 infra。

为了让 MongoDB 达到我们需要的可靠性，我们在 infra 上投入了很多，如今它确实做到了。拿数据说明：Stripe 去年关键 API 可用性（critical API availability）为 99.99986%，全年不可用总时长约 44 秒，虽然很多公司不会公布这么细节的数字，我们相信这是行业最佳。

Ruby 也是一样。公司偶尔会改主语言，但最初那一下往往会把你的技术路线长期锁死。

**Michael Truell：****我听说 Stripe 当年内部还争论过是否要迁到 Java，甚至有一堆文档？**

**Patrick Collison：**对，我们部分迁移了。把不少关键服务（用 Java 重写。因为有些服务（比如吞吐量（throughput）要求很高的）确实更适合 Java。当然，Ruby 也能被“榨”得很快：把热点路径（hot paths）用 C 重写之类的。但你会频繁和内存分配器（allocator）搏斗，Ruby 在字符串等细节上也不够高效。所以我们现在两种语言并用。

**Michael Truell：****你们当时有没有评估过 MongoDB 以外的选项, 有没有走 RFC 流程，或者更正式的决策流程？**

**Patrick Collison：**说实话，选择 MongoDB 就是我和 John 坐在沙发上商量的结果。开源社区口碑一定程度上也对我们产生了影响。

我在上一家公司写过一个基于对象的数据存储（object-based data store），对 SQL 一直有点不适，主要是应用域（application domain）与 SQL 可表达范式之间存在明显的“翻译、阻抗不匹配”（translational、impedance mismatch）。用 SQL 往往得把业务概念压扁到一组相对有限的原始形式（primitive forms）里；比如在 Stripe 的语境里，“钱”这个概念，和某些 SQL 数据库里的表示法并不完全对齐。

所以我对 SQL 有点“天然排斥”，并不是说这一定正确。而在 Stripe，我们希望技术栈更主流一点：没有再用 Smalltalk，也没走到 Java，而是选了相对主流的 Ruby；同理，也没再自研数据库，而是用了更主流的 MongoDB，它依然提供了我们想要的灵活性。

**04.**

**“重写” Stripe**

**Michael Truell：****假如今天有机会重新做一遍 Stripe，比如有个“ Stripe V2”，你会做哪些不一样的决定？**

**Patrick Collison：**我们其实还没有在公开场合谈论过这个话题。在 2022 年，围绕数据模型（data model）和抽象（abstraction）的讨论中，我们意识到 Stripe 内部有些核心抽象（core abstractions）从长期看并不理想，必须修正。于是我们设计了一批 v2 API (第二代API)。幸运的是，早在 2010 年我们就为这种演进留了余地：多数对外 REST URI 一开始就以 /v1 前缀命名。到 2022 年，我们决定提升命名空间（namespace），据此设计了新 API，并且它们今年已经开始上线。

v1：第一代接口。是 Stripe 早期对外提供的 REST API（路径通常以 /v1/ 开头）。覆盖面广、存量集成最多，强调稳定兼容，很多老项目一直在用它。

v2：第二代接口。基于 Stripe 对底层数据模型与核心抽象的重构而推出的新一代 API（路径通常以 /v2/ 开头）。目标是统一概念、减少特例、提升一致性与可组合性，并承载更多新能力。

简单来说 Stripe V2 会带来一些根本性改进：过去我们把终端客户（end customers）、子账户（sub-accounts）、不同支付类型的收款人（recipients）等分别建模；现在我们把这些统一到同一种实体表示（entity representation）之下。

这些改变让我们的客户可以不必反复录入信息，甚至能在不同国家、地区复用同一账户，对效率提升帮助很大。

整个升级过程相当复杂，因为独立设计一个 API 并不难；难的是让它们与 Stripe 既有系统全面互操作（interoperable），为此还要构建转译层（translation layers），并且与客户一起制定可行的升级路径（upgrade path），毕竟我们只能控制自己的代码库，无法掌控客户的代码库。

某种程度上，这很像芯片架构的指令集迁移（instruction set migration）：指令集本身不复杂，真正棘手的是各种共存问题（coexistence questions）。

无论如何，能在今年把它们落地发布实属不易，我们对此非常兴奋。至于你问的经验和启示，如果要给一个朴素但实用的答案，那就是：能统一的就尽量统一（unify everything you can plausibly unify）。

**Michael Truell：****你是如何测试 v2 的设计理念的？**

**Patrick Collison：**先插一句教训，再回答这个问题。第一，必须有一位首席 API 设计师对全局单点负责。可以有工作组，但仍需要一个人作为整体架构与一致性的最终把关者，这点必要。

第二，我的老生常谈：凡是可能存在一对多、多对多（n-by-m）关系的场景，都要原生支持。你也许当下只看到一对一、一对多，但实际业务里各种排列组合（permutation）终会出现；若没预留，就会被反噬。

回到“怎么验证 v2 是否正确”，设计者长期亲历旧版的不足，带着强烈痛点起步；同时我们尽早向客户演示早期版本。即便有清楚的想法，也可能预测错误（predict wrongly）、外推过度（extrapolate wrongly）或过度设计（overengineer），所以客户验证（customer validation）、反馈（customer feedback）循环非常关键。

我们不只画 API，还亲手写“新世界”的实际集成，把各类业务模型（business models）与流程（flows）用这些 API 落地，感受易用性、冗余度。就像 Java 解决了 C、C++ 的内存管理（memory management）问题，却引入冗长与开销（overhead）；我们用真实代码来防止自己无意间过度工程化。

总体上我很乐观，但实话说目前完成度约 60%–70%，还没到 100%，还很早。

排版：傅一诺

![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/005.png)

延伸阅读

[![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/006.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518120&idx=1&sn=6f4e7c983c66e5a5c2b84be206ab223e&scene=21#wechat_redirect)

超越 Prompt 和 RAG，「上下文工程」成了 Agent 核心胜负手

![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/007.png)

[![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/008.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518031&idx=1&sn=bb6cada95f0ffbb951f6bdcc21663afa&scene=21#wechat_redirect)

一半美国医生都在用的AI产品，OpenEvidence 是医疗界的 Bloomberg

![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/009.png)

[![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/010.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517863&idx=1&sn=ebf449b114d7325f15247ad28ddddd61&scene=21#wechat_redirect)

Vibe Working：AI Coding 泛化的终局想象 ｜AGIX PM Notes

![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/011.png)

[![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/012.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517781&idx=1&sn=22cb82ed020d508c26cb0be9187300ee&scene=21#wechat_redirect)

Cloudflare 的 AI 新叙事：线上内容“做市商”，Agent 互联网流量基建

![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/013.png)

[![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/014.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247517743&idx=1&sn=124cd41acb1263ba70c332934acbd675&scene=21#wechat_redirect)

对谈 Macaron 创始人陈锴杰：RL + Memory 让 Agent 成为用户专属的“哆啦 A 梦”｜Best Minds

![](../images/2025-09-18-stripe-x-cursor-huo-gu-liang-dai-jin-tong-dui-tan-wei-lai-bu/015.png)
