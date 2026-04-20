---
title: LangChain：Model as a Service粘合剂，被ChatGPT插件干掉了吗？
publish_date: '2023-03-24'
publish_timestamp: 1679659148
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/3coFhAdzr40tozn8f9Dc-w
msgid: 1000000182
appmsgid: 2247501117
itemidx: 1
digest: 第一个被广泛接受的LLM应用开发框架。
cover: https://mmbiz.qpic.cn/mmbiz_jpg/3tHNibnJ2jgzEFnrWRYpXyJVVR80ic8l2umtrBjmr2Hk3OxjC79xgSYicibPBgXiadt2b7MzgnTZsBGdhDD2FzNZqcw/0?wx_fmt=jpeg
image_count: 40
archived_at: '2026-04-20T00:50:57+08:00'
---

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/001.gif)

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/002.png)

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/003.png)

作者、编辑：程天一

排版：Lydia、Zoey

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/004.png)

LangChain 很火，有关它的前途命运也有很多争议，但一个相对肯定的结论是：**LangChain 已经成为了 AI 应用开发的新手村。**22 年 11 月初，Hacker News 上“如何入门 AI”的帖子回复中，LangChain 第一次被列进入门套装：

看 Fast.ai 和 Andrej Karpathy 的 YouTube 频道。在本地试试跑 Stable Diffusion。用 YOLO 标记你的图片。用 LangChain，在 Hugging Face 学学如何使用 Transformer 的库。然后去 Kaggle 吧。

LangChain 由前 Robust Intelligence 的机器学习工程师 Chase Harrison 在 22 年 10 月底推出，是一个封装了大量 LLM 应用开发逻辑和工具集成的开源 Python 库，有成为第一个被广泛认可的 LLM 应用开发框架的势头。**随着 Harrison 为 LangChain 添加了很多实用的抽象，以及 23 年 1 月众多 AI Hackathon 决赛项目使用 LangChain，它的 Github Star 迅速破万，成为 LLM 应用开发者选择中间件时想到的第一个名字。**

从开发者视角看，LangChain 是个挺友好且优美的库：

**•**它非常**模块化**，还通过 Chain、Agent、Memory 对 LLM 的抽象帮助开发者提高了构建较复杂逻辑应用的效率；而且每个模块有很好的可组合性，有点像“为 LLM 提供了本 SOP”，能实现 LLM 与其他工具的组合、Chain 与 Chain 的嵌套等逻辑；

**•**它**一站式集成了所有工具**，从各种非结构化数据的预处理、不同的 LLM、中间的向量和图数据库和最后的模型部署，贡献者都帮 LangChain 跟各种工具完成了迅速、全面的集成。

**作为成长期投资者看 LangChain，它本身还太早期，远没到成长逻辑。**除此之外，我对它在商业层面未来发展的核心担忧在于：

**•**我们不能直接套用旧时代的中间件视角，**随着 ChatGPT Plug-In 出现和 OpenAI 的更多边界延伸，LangChain 的价值可能被取代，**很快像机器学习历史上的其他明星库一样隐入尘埃；

**•**LangChain 本身的壁垒也比较薄，是**“其他开源库身上的开源库”**，没有太多技术壁垒，只是替大家省下来了码的时间。如果要收费使用，很多开发者可能会选择自己把 LangChain 这套东西码出来；

**•**目前使用 LangChain 库的**以个人开发者和极客的 side project 为主**，还不是正经的企业级 LLM 集成工具，而稍微有点体量的公司都会选择 fork LangChain 的源码或者干脆自己再码套框架。

**从投资人的角度看，LangChain 的创始人 Harrison Chase 想做的不止是 LangChain 这个开源库而已，我们比较期待他服务 AI 应用开发者的下一步动作。**此外，我在本文使用了尽可能通俗易懂的方式呈现和分析 LangChain 的能力，所以没有技术背景的读者也可以放心阅读本文，也欢迎 LangChain 开发者**填写反馈征集问卷**。

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 构建 AI 应用远不只是调用模型 API

02 案例：为一本 300 页的书构建问答机器人

03 产品：拼接好 LLM 的大脑和四肢

04 挑战：对 Prompt Ops 的质疑

05 竞争：以和为贵、各展神通的时代

06 未来：Harrison 超越 LangChain

**01.**

**构建 AI 应用远不只是**

**调用模型 API**

一旦在 LLM 领域花了足够多的时间，在兴奋之余你会意识到当前模型本身的两点局限：

**1. 它只有“脑子”没有“手臂”，无法在外部世界行动，**不论是搜索网页、调用 API 还是查找数据库，这些能力都无法被 OpenAI 的 API 提供；

**2. 甚至它的“脑子”也不完美，**OpenAI 的训练数据截止至 2021 年，并且没有任何企业和个人的私有数据，这让模型只能根据自己的“记忆”回答问题，并且经常给出与事实相悖的答案。一个解决方法是在 Prompt 中将知识告诉模型，但是这往往受限于 token 数量，在 GPT-4 之前一般是 4000 个字的限制。

从抽象层面看，我们使用 LLM 时在期待两种能力（这是个没那么科学严谨的分类）：

1. 一种是使用它的生成能力，这是 GPT-3 和 ChatGPT 刚刚出现时最初被体验的能力 —— 让 ChatGPT 写首诗，你可以接受它的上述不完美；

2. 进入到围绕模型构建“真正有用”的应用时，我们更多在使用它通过思想和记忆进行推理的能力。而简单直接地通过 API 调用模型无法将推理所需的一些事实和知识给到它，即这时候模型总是缺少“Context”（广义的上下文）。

这就需要为模型注入 Context 并进行一定的 Prompt Engineering。**正确的 Prompt 可以激发出 LLM 的能力，这在 GPT-3.5 以前的时代更为重要。**将 Context 注入 LLM 实际上在 Prompt Engineering 的上游，把知识告诉 LLM，Prompt 只是中间桥梁。前 Stitch Fix 的 ML 总监 John McDonnell 画的这幅图很好地展示出了二者的关系：

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/005.png)

“脑子”的问题目前已经有了成熟的解决方案来绕开 token 数量的限制。通常的方法借鉴了 Map Reduce 的思想，涉及到给文档切片、使用 Embedding 引擎、向量数据库和语义搜索（我们在 02 中详细介绍了这个过程）。

关于“手臂”的探索也早就有很多，OpenAI 的 WebGPT 给模型注入了使用网页信息的能力，Adept 训练的 ACT-1 则能自己去网站和使用 Excel、Salesforce 等软件，PaLM 的 SayCan 和 PaLM-E 尝试让 LLM 和机器人结合，Meta 的 Toolformer 探索让 LLM 自行调用 API，普林斯顿的 Shunyu Yao 做出的 ReAct 工作通过结合思维链 prompting 和这种“手臂”的理念让 LLM 能够搜索和使用维基百科的信息……

有了这些工作，在开源模型或者 API 之上，开发者们终于可以做有相对复杂步骤和业务逻辑的 AI 应用。**而 LangChain 是一个开源的 Python 库（后续又推出了 Typescript 版本），封装好了大量的相关逻辑和代码实现，开发者们可以直接调用，大大加速了构建一个应用的速度。**

如果没有 LangChain，这些探索可能首先将被局限在 Adept、Cohere 等有充足产研资源的公司身上，或仅仅停留在论文层面。然后随着时间推移，开发者需要闷头码个几周来复现这些逻辑。但是有了 LangChain，做一个基于公司内部文档的问答机器人通常只需要两天，而直接 fork 别人基于 LangChain 的代码构建个人的 Notion 问答机器人则只需要几个小时。

**02.**

**案例：****为一本 300 页的书构建问答机器人**

我自己知道的第一个使用 Map Reduce 思想的应用是 Pete Hunt 的 summarize.tech，一个基于 GPT-3 的 YouTube 视频总结器。Pete 在去年 9 月兴冲冲地在 Twitter 上表示自己找到了让 GPT-3 调用成本下降 80% 的方法 —— **不是一股脑将 YouTube 视频的文稿做总结，而是先将它分成很多的文本块（chunk），对每个块分别总结，最后给用户交付的是“摘要的摘要”，过程中消耗的 token 数能节省很多。**

事实上，**这不光能让成本降低，还可以解决单个 Prompt 中 token 数量限制的问题。**随着 12 月 OpenAI 新的 Embedding 引擎推出和 ChatGPT 让更多 AI 应用开发者入场，这种做法目前已经成为解决 Context 问题的绝对主流做法。

下面我们以一个 300 页的书的问答机器人为例，给读者展示下 LangChain 如何封装这个过程（这个例子来自 YouTube 博主 Data Independent 的 LangChain 101 系列视频，如果你想迅速上手 LangChain，强烈推荐观看）：

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/006.png)

1. 哪怕是 GPT 的 32k token 限制，300 页的书也绝对超过了，因此我们需要引入上文这种 Map Reduce 的做法；

2. LangChain 提供了许多 PDF loader 来帮助上传 PDF，然后也提供许多类型的 splitter 让你可以将长文本切成数百个文本块，并尽量避免这么切可能导致的语义缺失；

3. 有了文本块之后，你可以调用 OpenAI 的 Embedding 引擎将它们分别变成 Embeddings，即一些大的向量；

4. 你可以在本地存储这些向量或者使用 Pinecone 这样的云向量数据库存储它们；

5. 调用 LangChain 的 QA Chain 就可以进行问答了，这背后发生的是 —— 输入的问题也被 Embedding 引擎变成向量，然后使用 Pincone 的向量搜索引擎找到语义最接近的一些 Embedding，将它们再拼接在一起作为答案返回。

**LangChain 在过程中提供了完整的集成，从 OpenAI 的 LLM 本身、Embedding 引擎到 Pinecone 数据库，并且将整体的交互逻辑进行了封装。**如果你想用别人基于 LangChain 的代码 fork 这个 PDF 问答机器人，基本只需要换一下 OpenAI API key、Pincone API key 和用的这份 PDF。

**03****.**

**产品：拼接好 LLM 的大脑和四肢**

LangChain 身上有许多标签：**开源的 Python 和 Typescript 库、第一个被广泛采用的 LLM 开发框架、Model as a Service 设想的中间件、AI 应用层的基础设施......**感兴趣上手使用 LangChain 的读者可以参考下图观远数据的这个讲解视频，或是去 LangChain 的文档中心和 Github 逛逛。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/007.png)

*Source：《微软 365 Copilot 是如何实现的？*

*揭秘 LLM 如何生成指令》- Bilibili*

我在这一部分将不再罗列 LangChain 本身的一系列功能，而是详细讲讲我认为 LangChain 最重要的 3 个身份 —— **让 LLM 拥有上下文和行动能力的第一选择、所有 LLM Ops 工具的粘合剂/螺栓、一个快速崛起的开源社区。**

**让 LLM 拥有上下文和行动能力**

目前基于 LangChain 开发的第一用例是建立使用私有数据的问答机器人，而大多数开发者想到要导入私有数据，第一选择就是基于 LangChain 来做。**可以说 LangChain 是目前将上下文信息注入 LLM 的重要基础设施。**Harrison 在去年 11 月为 LangChain 总结的 4 大价值主张支柱也都围绕这一点，体现出了很优美的模块化和可组合性特点：

**LLM 和 Prompts**

如果是一个简单的应用，比如写诗机器人，或者有 token 数量限制的总结器，开发者完全可以只依赖 Prompt。此外，这也是更复杂的 Chain 和 Agent 的基础。LangChain 在这一层让切换底层使用的 LLM、管理 Prompt、优化 Prompt 变得非常容易。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/008.png)

此处最基础的能力是 Prompt Template。一个 Prompt 通常由 Instructions、Context、Input Data（比如输入的问题）和 Output Indicator（通常是对输出数据格式的约定）。使用 LangChain 的 Prompt Template 很好地定义各个部分，同时将 Input Data 留作动态输入项。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/009.png)

围绕 Prompt，LangChain 还有很多非常有意思的小功能，比如 0.0.9 版本上的两个能力：Dyanamic Prompts 可以检查 Prompt 的长度，然后调整 few-shots 给出的示例数量，另一个  Example Generation 可以检查 Prompt 里 token 数量还有剩余的话就再多生成些示例。

**Chain**

当一个应用稍微复杂点，单纯依赖 Prompting 已经不够了，这时候需要将 LLM 与其他信息源或者 LLM 给连接起来，比如调用搜索 API 或者是外部的数据库等。LangChain 在这一层提供了与大量常用工具的集成（比如上文的 Pincone）、常见的端到端的 Chain。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/010.png)

**今天 LangChain 封装的各种 Chain 已经非常强劲，一开始 300 页 PDF 的案例中用到的是它的 QA Chain，**我再举一些足够简单、易于理解的 Chain 作为例子：

它的第一个 Chain 可以让完全没有技术背景的读者也对 Chain 有个概念 —— 这个 Chain 叫做 Self Ask with Search，实现了 OpenAI API 和 SerpApi（Google 搜索 API）的联动，让 LLM 一步步问出了美国网球公开赛冠军的故乡。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/011.png)

还有一个很直观的 Chain 是 API chain，可以让 LLM 查询 API 并以自然语言回答问题，比如下面这个示例中 LLM 使用了 Open-Mateo（一个开源的天气查询 API）来获取旧金山当天的降雨量：

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/012.png)

**Agent**

Agent 封装的逻辑和赋予 LLM 的“使命”比 Chain 要更复杂。在 Chain 里，数据的来源和流动方式相对固定。而在Agent 里，LLM 可以自己决定采用什么样的行动、使用哪些工具，这些工具可以是搜索引擎、各类数据库、任意的输入或输出的字符串，甚至是另一个 LLM、Chain 和 Agent。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/013.png)

Harrison 将 Agent 的概念引入 LangChain 是受到前文提到的 ReAct 和 AI21 Labs 的 MRKL（Modular Resaoning, Knowledge, and Language 模块化推理、知识和语言）系统的启发。作为 Agent 的 LLM 深度体现了思维链的能力，充当了交通指挥员或者路由者的角色。

重新回归 OpenAI 的 Anrej Karpathy 在 Twitter 上经常说 LLM 会成为编排资源的认知引擎，LangChain 的 Agent 走得其实就是这个方向。所以 Agent 究竟能干什么呢？下面是我最喜欢的一个例子。

众所周知，ChatGPT 能听懂你的几乎所有问题，但是老胡编乱造。另外有一个叫 Wolfram Alpha 的科学搜索引擎，拥有天文地理的各类知识和事实，只要能听懂你提问就绝不会出错，可惜之前只能用官方给的语法搜索，非常难用。所以它的创始人 Wolfram 老师一直在鼓吹 ChatGPT 与 Wolfram Alpha 结合的威力。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/014.png)

23 年 1 月 11 日，LangChain 贡献者 Nicolas 完成了 ChatGPT 和 Wolfram Alpha 的集成。Agent 可以像下图一样运行，自行决定是否需要工具和 Wolfram Alpha，在回答“从芝加哥到东京的距离”时选择了调用它，在回答“Wolfram 是否比 GPT-3 好”时选择不调用它，自行回答。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/015.png)

**Memory**

LangChain 在上述的 3 层都做得很好，但是在 Memory 上一直相对薄弱，Harrison 自己不懂，一直由非全职的贡献者 Sam Whitmore 贡献相关代码，他也承认 LangChain 在这块儿有些技术债。

对于不了解 Memory 是什么的读者，你在 ChatGPT 每个聊天 session 都会出现在入口的左侧，OpenAI 会贴心地为你生成小标题，在每个 session 的问答里 ChatGPT 都能记住这个对话的上文（不过也是因为每次请求都会把之前的问答 token 都传给 OpenAI），但是新的对话 session 中的 ChatGPT 一定不记得之前 session 中的信息。LangChain 中的 Chain 在前几个月一直也都是这种无状态的，但是通常开发 App 时开发者希望 LLM 能记住之前的交互。

**在前 ChatGPT 时代，LangChain 不久还是实现了 Memory 的概念，在不同的 Query 间传递上下文，实现的方法跟开始的总结 300 页 PDF 类似：**

**•**总体而言的方法是记录之前的对话内容，将其放到 Prompt 的 Context 里；

**•**记录有很多的 tricks，比如直接传递上下文，或者对之前的对话内容进行总结，然后将总结放 Prompt 里。

微博博主宝玉 xp 画过一个系统交互图，如果不使用被封装好的库，自己手写的话实际上这套逻辑也很复杂。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/016.png)

在 Scale AI 今年的 Hackthon 决赛上，Sam 又为 LangChain 做了 Entity Memory 的能力，可以为 LLM 和用户聊天时 Entity 提供长期记忆上下文的能力：

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/017.png)

在 ChatGPT 发布后，LangChain 又优化了 Memory 模块，允许返回 List[ChatMessage]，将逻辑单元拆分为了更小的组件，更符合模块化的思想。

**一站式粘合所有工具**

模块化和可组合性是 LangChain 的关键理念，但它还有一个理念和我们介绍过的 Universal API 公司很像。

其实站在投资者的视角看，LangChain 的壁垒比较薄。有人问过 Harrison：为什么开发者要用 LangChain 而不是直接使用 OpenAI 或者 Hugging Face 上的模型？**LangChain 作为一个开源库仍然主要依赖于其他的开源库，它的长期目标是什么？**Harrison 的回答是：

Hugging Face、OpenAI、Cohere 可以提供底座模型和 API，但是在产品中集成和使用它们仍然需要大量的工作，长期目标是帮助人们更容易地构建 LLM 支持的应用。

从这个视角看，LangChain 更像“胶水”和“螺栓”。它的价值在于：

1. 全过程一站式的集成，从非结构化数据的预处理到不同模型结果的评估，开发者所需要的工具和库 LangChain 基本都有现成的集成。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/018.png)

2. LangChain 作为 Universal Layer 在 LLM 身上包了一层，让用户可以更自由地在多个 LLM、Embedding 引擎等之间切换，以避免单点风险和降低成本。

这里的逻辑和 Universal API 很像 —— 每个 LLM 提供者的 API 数据结构不同，但是 LangChain 包了一层后做了遍 Data Normalization。**从想象力的角度看，LangChain 有一定的编排价值，如果 Model as a Service 和多模型是未来，那么 LangChain 的价值会比想象中厚一些。**

举两个例子：

去年 OpenAI 的 API 还很贵的时候，一些数据加载器将文本块变成向量的方式是调用 OpenAI 的 Davinci Embedding，Harrison 觉得 LangChain 可以做到先用 Hugging Face 或者 Cohere 上便宜的模型做一道，然后再传给 Davinci Embedding，这样可以降低不少成本。

还有今年以来，ChatGPT 有时候会崩，这也引发了应用开发者们的担忧。Will Brenton 觉得出于这种理由用 LangChain 就很值得，可以用几行代码实现在多个 LLM 之间切换的逻辑，一个 LLM 如果服务挂掉了就自动试下一个。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/019.png)

*使用 LangChain 对比多个模型的输出*

**快速崛起的开源社区**

LangChain 是目前 LLM 领域最热门的开源项目之一，从下面可以看出今年以来的曲线和绝对 Star 数跟最热门的开源模型 LLama 相比也不遑多让，发布不到 5 个月已经拥有了超过 1 万个 Github Star。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/020.png)

人多力量大，我们在上文介绍的集成大多数也都是社区贡献的，目前 LangChain 的全职团队只有 2-3 个人：

**•**发起人是 Harrison Chase，他 17 年从哈佛大学毕业，分别在 Kensho（一家金融自动化公司，做金融分析决策与 NLP 的结合）和 Robust Intelligence（AI 模型部署的安全公司）做机器学习工程师，在 2022 年 9 月 的 Homebrew AI Club 聚会上听到 Sam Whitmore 构建 AI 应用的过程和痛点后，他开始做 LangChain；

**•**第一位全职加入 Harrison 的 LangChain 创业之旅的人似乎是 Ankush Gola，他从普林斯顿毕业后分别在 Facebook、Robust Intelligence 和 Unfold 做软件开发，可以弥补 Harrison 在软件工程方面经验的缺失。Harrison 搞不定 LangChain 的异步支持问题，Ankush 加入后迅速弥补了这一点，让 LangChain 能够使用 asyncio 库。

**开源是扩大影响力和话语权的最好手段，LangChain 在 ChatGPT API 和 GPT-4 问世的当天都迅速发布了集成，**基于 LangChain 构建的应用想转用 GPT-4 只需要换下 API key 和模型名字就行了，显然 LangChain 是 OpenAI 的重点合作对象之一。

除了 OpenAI 的这些更新，Zapier 推出的 Natural Language Actions API 也是跟 LangChain 进行了深度合作，Zapier NLA 对其 2 万多个工具的操作实现了“自然语音 → API call → LLM-friendly 输出”，也是基于 LangChain 做的。然后在推出当天，LangChain 也官宣了跟 Zapier NLA 的集成，用户可以先在 Zapier 支持的 App 上设置好一个 NLA API endpoint，然后就可以在 LangChain 中调用和组合使用 Zapier。

从这两个案例看，**LangChain 是大模型能力“B2B2C”的一个重要中间站。**

此外，除了给 LangChain 项目直接做贡献，还有不少人已经在围绕 LangChain 做生态项目，下面是我最喜欢的 2 个：

LangChain 本身是一个没有 UI 的库，但社区成员 Rodrigo Nader 为它构建了一个开源的 UI，叫做 **LangFlow**，让用户可以通过拖拽就能做出来应用原型。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/021.png)

大多数用户会使用 Streamlit 或者 Replit 来部署它们的应用，但是已经有社区成员开始为 LangChain 应用打造更炫酷的部署方式，比如 **Kookaburra**，可以让 LangChain 应用非常方便地被部署为短信机器人。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/022.png)

**04.**

**挑战：对 Prompt Ops 的质疑**

从投资者视角，我对 LangChain 的担忧有两点：

1. 它是一个**很难被商业化的开源项目，**因为它是一个**“依赖其他开源库的开源库”，**我所访谈的 LangChain 开发者也都认为自己不会为它付费，如果要构建一个基于 LLM 应用的公司，他们会选择自己 fork LangChain 再写一套框架，还能顺手把成本和延时问题做更多优化；

2. 和第一点相辅相成的是，**目前使用 LangChain 的主流人群是 Hacker 和独立开发者们，而不是 B 轮以后的 Mid-Market 或者大型企业公司。**当然，这是目前 AI 应用生态的现状，独立开发者在数量上占据主导。而且当前的 LangChain 实现一些复杂逻辑需要多个 Chain 的嵌套，并且多次 call LLM API，对于大规模调用的产品可能也确实成本不经济也有不稳定的情况。但是正因为此，LangChain 更难进行商业化，特别是在从数据准备到模型部署的全环节已经非常卷的情况下。

从演进的视角看，我对于 LangChain 这个库本身能不能具备服务中大型公司倒比较有信心 —— 两个月前人们还不认为 LangChain 是一个在生产环境中可靠的东西，一个月前 LangChain 才刚刚支持自托管模型，让企业 LLM 用户可以在 LangChain 中调用共享远程 API，但是它在客户自己的云账户或者本地硬件中运行。给 LangChain 时间，贡献者们会让它高度可用。

市场上普遍对 LangChain 有担心，但是我认为短期影响不大的两点是：

**1. LLM 本身的变化会让 LangChain 库中的许多部分过时。这一点我认为恰恰是开源项目的优势，贡献者可以迅速帮助它过渡到新版本；**

比如 ChatGPT API 发布后，它有了新的交互，这也意味着需要新的抽象，原来的很多 Prompt 不管用了，适用于 GPT-3 的 Prompt Templates 在 ChatGPT 下效果不好，所以 LangChain 又新增了 PromptSelectors 功能。此外 ChatGPT 在遵循特定的输出数据格式上表现得不好，有很多“无法解析 LLM 输出”的报错，LangChain 很快上了一个 chat-zero-shot-react-description Agent 来严格约束输出的数据格式，还大受好评。使用 LangChain 可能帮助很多公司避免过多的 Prompt Engineering 开发资源浪费。

2. 随着模型支持的 token 数量变多，LangChain 的核心用例 —— 用分块、Embedding、语义搜索、再拼回来 —— 可能会直接消失。这在短期内不是个问题，因为哪怕 GPT-4 的 3.2 万 token 也仍然不是很够用。同时，这种 Map Reduce 的方式还能省钱。

在理性的质疑中，我比较认可的是 Notion AI 的 Linus 的观点，他在 Twitter 上表示当前所有类似 LangChain 的 Prompt Ops 工具都是为 side-project 级别的用户服务的，很难正经接受它们，主要有 3 点原因：

1. 这些工具都假设一个服务是对 LLM 的调用，然后在此之上把业务逻辑耦合进去。而不是反过来，在已有业务逻辑里插入对 LLM 的调用，这让现有的 SaaS 等公司很难使用这些工具；

2. 对于模型的输出大家目前都没有可量化的方式来评估，Humanloop 已经有最好的模型评估 UI 了，但是也是为了人类反馈对齐而不是为了应用开发者的性能优化和迭代；

3. 这些工具都希望成为生产环境下工作负载的关键中间点，但是有延时和安全性上的很有问题，还不如给用户交付模型配置和最终 prompt 然后让用户自己调用模型。

一些朋友在 Linus 的观点下指出： **LangChain 不是一个 Prompt Ops 工具，它是一个 LLM 增强工具，**通过粘合一系列的模块（这些模块本身可能是 Prompt 增强工具）增加了 LLM 可以融入的业务逻辑复杂度。Linus 也认同这一点。总体而言，我认为这些批评为 LangChain 指明了方向，它也的确在 3 月拥有了更多和模型评估以及性能可观测性相关的集成。

**05.**

**竞争：以和为贵、各展神通的时代**

抛开直接面向消费者的应用不看，LangChain 的核心竞争对手是三类：

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/023.jpg)

**• GPT-Index** 本身是基于 LangChain 构建的，它的用例更集中于 Memory 和将数据导入 LLM，用例非常明晰，而 LangChain 的功能更抽象和庞大，用户需要在其中挑选符合自己用例的进行组合；

**• Microsoft Semantic Kernel** 的整体目标和 LangChain 非常接近，Planner 类似我们上文提到的 Agent，但是它针对的受众不是独立应用开发者，而是那些需要在兼顾原有开发工作的同时将 LLM 能力嵌入自家应用的工程师们，因此采用了一个轻量级 SDK 的形式交付，它是 LangChain非常强劲的潜在竞争对手，但是 Microsoft 和 OpenAI 的亲密关系可能让它在未来无法像 LangChain 一样灵活支持各类 LLM；

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/024.png)

**• Dust 和 Scale AI Spellbook** 代表着 LLM 应用开发的无代码和低代码思路，拥有非常好的 UI/UX，但是大多数开发者认为自己并不是需要低代码的工具，而是需要更多的功能和可实验性。

**我们访谈的所有 LangChain 用户都只使用 LangChain，对于 GPT-Index 和 Dust 只探索到去它们的 Github 和官网逛逛的程度。**有 Twitter 博主专门横向测评了这三个工具，结论是：

如果你想构建复杂逻辑并且自己托管后端的应用，那就使用 LangChain。Dust 和 Everyprompt 是通过 UI 来定义 Prompt 和创建 LLM 工作图，LangChain 作为一个 Python 库提供了更多的灵活性、可控度但更笨重。它的 game changer 是围绕 Agent 的能力，一个可以跟外部工具（python interpreter、搜索引擎）交互从而回答问题的 LLM，这是其他工具所不具备的。

不看大厂的话，**创业三杰 LangChain、GPT-Index、Dust 互相有很多羁绊，绝对不是火并竞争的关系：**Dust 比 LangChain 出现得更早，由前 OpenAI 的Stanislas 创建，它的理念和对可组合性的重视对 Harrison 做 LangChain 有很大的启发。而 GPT-Index 的创始人 Jerry Liu 是 Harrison 在 Robust Intelligence 时的同事，因此两个人经常交流产品想法，GPT-Index 和 LangChain 互相有非常多的集成。

甚至 GPT-Index 本身也是基于 LangChain 构建的，能享受 LangChain 基建升级的许多好处。比如 LangChain 在 1 月底提供了 tracing 的能力，让用户能更好观测和 debug 自己的 Chain 和 Agent，GPT-Index 作为基于 LangChain 的包也自动获得了这个功能。下图是一个 GPT-Index query 的 tracing 视图：

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/025.png)

**06.**

**未来：Harrison 超越 LangChain**

**LangChain 是一个开源项目，Harrison Chase 想构建的似乎不止于 LangChain。**上个月，The Information 报道 Benchmark 以数千万美元估值投资了 LangChain 数百万美元。Harrison 有可能在继续扩大 LangChain 影响力的同时做出更产品化的开发者工具。

从早期投资押注人的角度，Harrison 是一个很好的创业者和项目经理，尽管还没有直接交流过，但我比较喜欢他的几个特质：

**敏锐地把握到了 LangChain 的机会**

在 22 年下半年，市场逐渐开始意识到 LLM 的下一步是“Action”，也就是在外部世界能够采取行动。标志性的事件之一是 Cohere 在 9 月推出了基于 LLM 的 Discord 搜索机器人。

Harrison 这时候已经花了不少时间思考下一步所需要的工具，并且留意到了 Dust 的尝试，随后就开始构建 LangChain 这个 Python 包，并且在 10 月就立马推出。在此期间，碰到有人做应用，Harrison 经常会问问对方“什么工具会帮你提效”、“还缺什么工具”。

回过头看，**LangChain 能继续火下去的前提是，目前 AI 应用已经从模型技术能力的 pk 到了产品能力的 pk，Harrison 自己的总结是“能有好的产品创意的人 > 能创建更好模型的人”，而 LangChain 就希望解锁这些人的创意和效率。**

**对 LLM 的进展、能力、痛点**

**有自己独到的理解**

从后视镜看，LangChain 的 Chain 和 Agent 逻辑似乎是个无脑的选择。但是 Harrison 当时选择构建这一点是基于对 Action 驱动和对 LLM 能力的判断，受到了 ReAct 这篇论文不少影响。

他对于 token 数量限制的理解也很敏锐，将 Map Reduce 的实现提到了 LangChain 比较高的优先级，后面随着 1 月份各种 AI Hackthon（Hugging Face、Scale AI 等）的举办，对快速使用这个逻辑的需求激增，并且相关参赛队伍都会提到自己使用了 LangChain，让 LangChain 迅速变成了 AI 应用开发者们的第一选择。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/026.png)

*LangChain 开发者旧金山 Meetup 的盛况*

**非常紧贴用户需求并且展现出**

**很强的执行力**

LangChain 上线各类新模型和新集成的速度非常快，Harrison 自己干活快，而且迅速让 LangChain 的社区非常有凝聚力 —— **AI 和 LLM 本身是有趣且实用的，Harrison 推动做了 LangChain Hub，旨在为用户提供一个易于分享和发现 Prompt Sequence、Chain 和 Agent，又加深了这一点。**同时，Harrison 很善于跟社区成员交流获得更多的反馈，在 LangChain Discord 社区频繁互动，并且建立了一个专用的 Slack 频道帮助大家将 LangChain 用于生产环境。

有一个小的细节是：在 1 月中旬，有用户反馈 LangChain 的 verbose（根据内容来自的模型或组件来使用突出色号显示）挺有用但可以更详细，比如每个查询到底用了多少 token，这样在应用可能被大规模使用时可以更好地追踪成本。这是个很细节的功能，但是 Harrison 表达了重视并且在一周之后添加了对 token 的计算和显示，并且通过 GPT-Index 统计 token 的具体使用情况。类似的例子我还观察到了不少，只要是 Harrison 答应用户的需求，一定不久就会发布。

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/027.png)

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/028.png)

**Reference**

Blog@LangChainTwitter@Harrison Chasehttps://www.youtube.com/watch?v=h0DHDp1FbmQhttps://www.youtube.com/watch?v=X51N9C-OhlEhttps://www.youtube.com/watch?v=Zn-L6t1BliAhttps://www.youtube.com/watch?v=lhby7Ql7hbk&t=8s

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/029.png)

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/030.png)

延伸阅读

[![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/031.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501059&idx=1&sn=3a13676863ccaafa125089891c74cb8d&chksm=ce9b7a9df9ecf38bd31ce245c5b7327580986738b221c10c640815d4b069c82595bc5b785861&scene=21#wechat_redirect)

Runway：AI Native Tools工厂，视频生成领域的字节跳动

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/032.png)

[![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/033.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247500861&idx=1&sn=f7605b32cef79109105d32267fd9ed16&chksm=ce9b7ba3f9ecf2b55735c7ce23e955fe1405395ac069adfb3269cffdf277a7775875a5cfab07&scene=21#wechat_redirect)

Jasper：早期GPT生态最大赢家，是否会被边缘化？

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/034.png)

[![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/035.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247500815&idx=1&sn=013c1b284623e5fd8e86acc0eec69761&chksm=ce9b7b91f9ecf287b235ec2f9d40629a3dcfe806cc69af9c505905e6cb3f4d40cc77ef9a40bc&scene=21#wechat_redirect)

Anthropic：出走OpenAI，Google站队，AGI是天使还是魔鬼？

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/036.png)

[![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/037.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247500768&idx=1&sn=796af446dec11feca83f1e2c1ce4d6c1&chksm=ce9b7c7ef9ecf56842d61a52aef5c33a22916b070128f9c119551c8035fb041f14b45abd9c90&scene=21#wechat_redirect)

Character.AI：个性化的ChatGPT，AI大模型时代的UGC平台

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/038.png)

[![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/039.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247500685&idx=1&sn=14447f063bcd73f763405758da160206&chksm=ce9b7c13f9ecf50561af25a0d5e4c427da445b2425e7b05e57e642f466eace7544285fd2e87f&scene=21#wechat_redirect)

OpenAI创始人的AGI预言：AI Safety、Scaling laws与GPT-20

![](../images/2023-03-24-langchain-model-as-a-servicenian-he-ji-bei-chatgptcha-jian/040.png)
