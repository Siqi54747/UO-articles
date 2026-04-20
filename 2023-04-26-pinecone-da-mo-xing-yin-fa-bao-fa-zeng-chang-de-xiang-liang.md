---
title: Pinecone：大模型引发爆发增长的向量数据库，AI Agent的海马体
publish_date: '2023-04-26'
publish_timestamp: 1682510400
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/Brmzkw9oH_miPwwlODYeSw
msgid: 1000000193
appmsgid: 2247501819
itemidx: 1
digest: 向量数据库在未来的Infra中将占一席之地。
cover: https://mmbiz.qpic.cn/mmbiz_jpg/3tHNibnJ2jgzVZKu2CZkPCpjYIx4icStUD2vtdt2lofJ5dicNE43smImgX3iaydbM2ibt1MWHxqjBpX0KD9XQjyoJcg/0?wx_fmt=jpeg
image_count: 30
archived_at: '2026-04-20T01:03:03+08:00'
---

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/001.gif)

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/002.png)

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/003.jpg)

作者：Cage

编辑：penny

排版：Ziyu

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/004.png)

每天当我们睁开双眼，记录光线强度的信号传到视觉皮层，那里的神经元激活后形成对眼前事物的神经表征，这就是人脑真正理解和学习的对象。AI 模型的学习原理也并无二致，**它实际识别和理解的不是一个个具体的文字符号，而是神经网络对各类数据的向量化表示**，表示的结果便是向量 embedding 。

移动互联网时代，JSON 文档作为支撑大规模灵活数据存储的通用格式，推动了 MongoDB 的流行；而在 AI 重塑软件的时代，**向量作为大模型理解世界的数据形式，也可能促成新的重要基建：**向量数据库。

13 世纪，红衣主教雨果·圣谢尔创建了第一部拉丁圣经词汇表，列出了重要关键词及其出现的位置。之后 800 年，数据库都基于类似的精确匹配逻辑，输出一一对应的“正确答案”；而**向量数据库做的是模糊匹配，输出的是概率上的最近似答案，**这个逻辑更接近机器学习中的无监督聚类，和传统数据库擅长的二进制命题截然不同。因此传统数据库的技术方案无法迁移至向量场景。

**如果说 LLM 是容易失忆的大脑，向量数据库就是海马体**，记忆的缺失让每一次和 LLM 的交互像是一次次不断重头再来的闭卷考。而向量数据库的存在让这一过程能变成开卷考：一方面，**LLM 能浏览专用数据与知识，解决 Hallucination 的问题使回答更精准**；另一方面，**LLM 能回忆自己过往的经验与历史，更了解用户的需求，通过反思实现更好的个性化**。

像 AutoGPT 这样需要记忆系统的多轮项目正在涌现，向量数据库的用量也陡然增长。其中增长最快的是本文所研究的对象 Pinecone，**他们用开箱即用的产品体验占据了 AI 应用开发者的心智，最近其 Python 库巅峰时期日下载数接近 50000 次，**甚至免费版方案都因需求量暴增一度停摆。

我们认为未来的 AI native 应用有几个重要元素：**LLM + 交互 + 记忆（专有数据 + 个性化） + 多模态**，后两者都与向量数据库高度相关。随着多模态大模型的出现，向量 embedding 会像之前的 JSON 数据一样覆盖多个使用场景，需求量也将大幅增长。

因此，我们认为向量数据库会在 Infra 领域占有重要位置，甚至 LLM + Vector DB 的组合会对传统数据库产生冲击，因为这一组合对数据资产的理解和利用效率会显著高于结构化的数据表达。

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 大模型是大脑，向量数据库是海马体

02 向量是 AI 理解世界的通用数据形式

03 OP Stack 中的P，Pinecone 的发展之路

04 探讨与展望：智能体的结构、LLM 和 DB 的关系是尚不明晰的关键问题

**01.**

**大模型是大脑**

**向量数据库是海马体**

1953年，Henry Molaison 因为饱受癫痫症带来的痛苦，接受了一种实验性的手术。这次手术让他成为神经科学家们最耳熟能详的病人。

手术切除了他部分内侧颞叶，包括海马体，这些区域在当时被认为与癫痫发作有关。术后，身边的医护人员发现 Henry 的记忆就像沙滩上的字，时间的海水一冲就会消失，无法形成新的记忆；同时，他对以前发生的事情、语言中每个词语的意义、理解和发音记得一清二楚。也就是说，海马体的缺失使他的记忆永远停留在了手术那一天。

对于人类这种智能体，记忆似乎是与生俱来的能力；而如果把 ChatGPT 类的大语言模型比作大脑，其天然就缺失了形成记忆能力的海马体。在大模型中，世界知识和语义理解被压缩为了静态的参数，模型不会随着交互记住我们的聊天记录和喜好，也不会调用额外的知识信息来辅助自己的判断。

但当大家提到对 AI native 应用的预期时，有几个关键词是高频的需求：B 端需要专用数据、C 端需要个性化与自动化。而这些需求都要记忆来实现，因此给大模型记忆功能的尝试越来越多：

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/005.png)

*( 表格自上而下是检索记忆的频率提高 )*

**单次检索：片状的记忆**

最早出现的记忆方案是 Retrieval Augmentation，通过外部储存来增强模型记忆。当模型需要记忆大量的聊天记录甚至一整个行业知识库时，将其储存在向量数据库中，后续按需去获取最相关的信息。每次用户输入 prompt 时，从外部记忆中找到最相关的内容和 prompt 一起输入给模型，得到的生成内容会更有针对性且减少了 hallucination 的问题。

这一能力在我们之前[**对 Langchain 的介绍**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501117&idx=1&sn=e860ac5e259a969f62b05d080bf42d14&chksm=ce9b7aa3f9ecf3b503656e9a09b55210fdba0844b54bd6a5714f5fc8c57b8c3570acbe2d342f&scene=21#wechat_redirect)中，已经有过相关的介绍。后续 OpenAI 官方 Retrieval plugin 也支持了这一能力。

例如在下图的 demo 中，当用户想要从联合国的数据库中获取最近联合国的信息时，ChatGPT 会从联合国过往文档中检索到和问题最相关的信息，并将其信息组织起来。在 Greg 最新的 Ted Talk 中，这一功能已经支持搜索用户的历史聊天记录。

这一能力的实现中，Pinecone 是 OpenAI 的下游，由于大模型的训练和推理不依赖这一能力，因此 Pinecone 等 vector DB 提供这向量存储和语义搜索的服务，暂时不会受到 OpenAI 的冲击。

单次的记忆增强很好的发挥了 ChatGPT 的信息整合能力，通过领域知识避免了 Hallucination。但这种方式没有充分挖掘其高阶的逻辑链（Chain of Thought）能力，因此最近的学术论文 ReAct、Reflexion，和开源项目 AutoGPT、BabyAGI 就在这个能力和记忆的结合下功夫。

**连续检索并更新：絮状的记忆**

以 AutoGPT 为例，其对 prompt 的使用是之前论文与项目的集大成者，这一点的实现与记忆系统密切相关。在 prompt 的一开始就跟 GPT-4 声明了“好记性不如烂笔头”：你输入 prompt 的空间限制只有 4000 token，因此发生重要的事情一定要记录到向量数据库中。记录之后，AutoGPT 定期会记忆进行复盘，即通过对历史行为的反思形成经验，来决定接下来的执行计划。这个记忆系统使黑盒的大模型把自己行为和推理的中间步骤说出来，一定程度实现模型记录经验的可解释性。

而 25 Agents 小镇在此基础上，加入了多 Agent 之间的交互，也就是说每个 Agent 的记忆系统是包含彼此的信息交织。其一作 Park 在采访中提到，最开始设计小镇时有很多环环相扣的设计，而实现过程中删繁就简保留下来最核心的内容，就是每个 Agent 的记忆系统和围绕其的使用与优化。**这一套记忆系统同时实现了感知的记录、记忆重要性的召回和定期的更新 Agent 人设。**通过简单的人设规则和记忆能力，AI 小镇展现出了一些人类社区的特质。沿着这条路走下去，群体智慧一定会涌现出更多令人吃惊的效果，如果 AI 们能被设计做一些对抗，甚至可能有 Game of Thrones 的效果。

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/006.png)

类似思路在开发者社区引发了很多思考和实验，AutoGPT 也成为了史上项目初期增长速度最快的项目之一。仅一个月的时间，其 star 数就超越了 Stable Diffusion ；最近其 star 数已经超越了 10万大关，接近  Stable Diffusion 的两倍。

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/007.png)

而在 AutoGPT 的早期发布中，主要就使用了 OpenAI api 来提供基础语言能力，Pinecone 来提供记忆能力。后续由于 Pinecone 免费服务需求量暴增有所限制，其他向量数据库才作为候备选项加入。在这一波 LLM 的热潮中，根据 Google Trend 的关键词搜索，Pinecone 在开发者中的心智优势进一步扩大了优势。

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/008.jpg)

**02.**

**向量是 AI 理解世界的通用数据形式**

第一部分讨论了向量数据库当前最主要的使用场景和火热原因——为大模型提供记忆。但其实向量 embedding 这一数据结构，和向量搜索的需求都是随着 ML/AI 模型逐渐发展到今天的，接下来就介绍下这一领域的演进。

**向量是多模态数据的压缩**

当我们见到一个熟悉的人的时候，大脑是这样思考的：首先，眼睛中的视杆细胞和视锥细胞记录下光的强度。这些信号传递到位于你大脑后方的视觉皮层，在皮层中数以百万计的神经元以不同的强度被激活。激活信号传输到你的颞叶，你的大脑解释为：我看到了某某。

也就是说，当我的大脑试图理解和解释看到的信息时，大脑解读的是视觉皮层输出的神经表示，而非进入眼睛的原始图像。

深度学习模型也是如此。

尽管大模型呈现出的形式是端到端、文本输入输出的，但实际模型接触和学习的数据并不是文本本身，而是向量化的文本，因为文本本身直接作为数据维度太高、学习起来太低效（稀疏）了。所谓向量化的文本，就是模型对自然语言的压缩和总结。早年的 NLP 教材有一个很经典的例子：如果我们把每一个单词看作向量，king 减 queen 之差与 man 与 woman 之差是相等的，都代表着性别的差异。

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/009.png)

以 Pinecone 的使用为例，我们常用会设置 dimension 为 1536，也就是说向量 embedding 是一个由 1536个浮点数组成的列表。当我们从向量库中查询这一列表的时候，就可以像下图中一样，看到其中的浮点数数值，和对应的原始文字内容。

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/010.png)

做一个类比，评价一个人有非常多的维度，我们见人的时候会根据自己的经验总结出一些关键维度的信息，这些关键信息就是人脑加工的 embedding。基于这些维度，我们评价的时候会围绕这些维度说出文本。但如果面试后要对一些候选人做筛选，我们不会拿文本评价，而是用内心的各个维度去比较、排序，然后找到最合适的那个人。这个比较并给出答案的过程，就是向量搜索。

**向量搜索是一种模糊的匹配，**

**需求在 LLM 前已经出现**

向量搜索就是在海量存储的向量中找到最符合要求的 k 个目标。当我想从海外独角兽的文本库中找出与“硅谷最新动态”最相关的 5 段文本时，首先会使用 OpenAI Embedding api 将海外独角兽的所有文章加工成向量，存入向量数据库中；然后把“硅谷最新动态”的向量与数据库中所有向量进行语义相似度的对比；比对后，对相似度排名返回 top 5 的文本，很可能来自去年团队去硅谷的所见所闻。

理解了这个过程，我们会发现向量搜索和传统数据库的查找最大区别在于：传统数据库是精确的索引，查找到的内容是有正确答案的。也就是说，数据库中的数据只有两类，一类是符合查询要求、返回给用户的数据，另一类就是不符合要求。而**向量搜索则是模糊的匹配，找到的是相对最符合需求的数据，并没有精确的标准答案。**

将这个过程和互联网业务联系起来，会发现向量搜索和之前我们研究过的 Feature Store 一样，是一个已经存在的需求。互联网中的搜索、推荐业务，安保系统的人脸识别、对比，都有很多使用场景。在这些场景下，系统需要根据多个维度进行数据关联计算，因为实际业务场景中数据量非常大，很容易形成类似“笛卡尔积”这种变态的结果，即使减少维度数量，进行循环遍历，来获取某几个向量的相似度计算，在海量数据的场景下也是不现实的。

💡

**笛卡尔积：****序偶**可以简单理解为带顺序的集合，而笛卡尔积就是 X 和 Y 两个集合内，包含的所有有序对组成的集合（序偶集合），又称为“直积”，在数学上记为 f={<x, y>｜x∈X, y∈Y}。

因此之前向量搜索算法就已经出现，Facebook 开源的 FAISS 是其中的翘楚，只是在大模型出现之前，这个需求只在大厂中存在，主要通过自研产品满足。

**向量数据库是 LLM 下游的新数据库产品**

向量数据库是一种高效存储和搜索向量的数据库产品，传统数据库无法很好的满足这一需求。传统数据库只能部分满足向量数据的存储，而且在搜索上技术有明显差异。

在存储上，向量数据规模超过传统的关系型数据库，传统的关系型数据库管理 1 亿条数据已经不算小的量级。而在向量数据库需求中，一张表千亿数据是底线，并且原始的向量通常比较大，例如 512 个 float = 2k，千亿数据需要保存的向量就需要 200T 的存储空间。因此对向量数据的存储需求量是很大的，如果不做数据库只做向量搜索算法，很大一部分需求还需要用户自己研发。

而查询方式的差异更大。前面提到，传统的数据库查询通常是点查和范围查，都是一种精确查找，即查询得到的结果只有符合条件和不符合条件。而向量数据库的向量查询往往是近似查找，即查找与查询条件相近的结果，即查询得到的结果是与输入条件最相似的。**近似的查找对算力要求更高。**

在大模型场景下，向量搜索的需求真正开始爆发式增长：如果有大量信息或语料需要给 LLM 作为参考，把大量文本一股脑的作为 Prompt 显然很不经济，而且过多不相干信息还可能误导模型输出。因此大部分创业者的方式是，提前把语料库向量化，再查询跟问题 embedding 相似的语料，最终一同送入 GPT 模型。这是一种典型的创业项目整合 OpenAI api 的路径，是现阶段比较灵活且经济的方式。向量搜索在这里扮演了择优选择 prompt 的角色。而 AutoGPT 更是把需求量推到了更高的水平。根据近期主流向量数据库 Python 包的下载量，几款头部产品都在近两个月有需求量的暴涨：

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/011.png)

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/012.png)

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/013.png)

*Pinecone、Weaviate、Chroma 下载量统计*

**向量数据库需求量的爆发****会出现在多模态领域**

尽管 AutoGPT 的项目创新带动了 Pinecone 用户数的大热，但这个使用场景对 Pinecone 等数据库的使用是略有浪费的。当前 AutoGPT 的思维链长度很难超过四位数的情形下，对最近邻进行穷举搜索（也就是 256 维向量与 10000 x 256 矩阵之间的点积）用时仅需不到一秒钟。

与 GPT 3.5/4 动辄 10 秒钟的调用速度比起来，对向量搜索这 1 秒的一步，优化到上限也只有加速 10%。也难怪 Andrej Karpathy 会在 Twitter 上表示自己存储和检索向量，使用的是 Python Numpy 库中的 array 函数，并吐槽人们会过度追求新鲜的事物。

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/014.png)

但从另一个角度说，当前的使用形式存在那么明显的过度使用问题，却能成为那么多独立开发者调用的首选（AutoGPT 使用了 Pinecone，基本没有使用 Langchain），恰恰说明对记忆模块的计算和存储需求的刚性：开发者们更乐意把时间花在 prompt engineering 上，而不是自己操心向量搜索、存储相关的能力。

进一步从动态的视角来看，当多模态大模型技术成熟之后，上文中提到的过度使用问题都不再存在。模型推理速度会加快，向量数据的复杂度提升，检索速度会变慢，届时向量搜索的性能是产品可用性至关重要的因素。而且向量数据库在多模态领域会有更显著的检索能力，毕竟人类和传统数据库对多媒体数据的检索能力是很弱的。多媒体数据也能大幅增加其存储量和迁移成本，使其成为更加刚性的需求。

MongoDB 的重要性一部分来自于 JSON 的灵活性，其覆盖多个场景，使用单个数据库完成了多种数据库的任务。而向量 embedding 也有这一潜质，文本、图片、音频、视频等多媒体数据，未来都可以用通用大模型压缩成向量化的数据。

因此如果我们认为 **AI 应用 = LLM + 交互 + 记忆 + 多模态**，那么在后二者的实现中向量数据库都将扮演非常重要的角色。

**03****.**

**OP Stack 的 P，**

**Pinecone 的发展之路**

在 AI 应用的开发者中，OP Stack 的心智已经慢慢传开：OpenAI + Pinecone。Pinecone 作为目前向量数据库的领先者，大模型记忆的第一选择，接下来就来介绍下这家公司的发展之路。

**团队**

**AWS 重要 Leader 带队**

CEO Edo Liberty，出生在以色列，在特拉维夫大学完成本科之后，来到耶鲁大学完成了 CS Phd 的学习。3 年博士后生涯让他厌倦了学术生活，和朋友创业成为 CTO。在公司卖掉之后，来到了 Yahoo 成为 ML Scientist 。在雅虎工作了 7 年后，他来到亚马逊 AWS 带领 Sagemaker 的工作，之后成为了亚马逊 AI Lab 的 Reasearch Head。

和其他专注 CV/ NLP / Robotics 的科学家不同，Edo 更在乎的是计算机数据系统与 AI 的结合，并且有着敏锐的产品嗅觉。在亚马逊期间，他观察到了 embedding 这一业务需求的增长，便离开 Amazon 出来创业。创业之初公司叫做 Hypercube.ai，当时做的是基于深度学习的多媒体搜索解决方案，尽管不是做向量搜索，但基于 embedding 的 retrieval 确实是核心技术之一。在 21 年初正式 pivot 成为 Pinecone 这家公司。

团队总人数在 50 人+，大部分的团队在工程方向，小部分负责产品与销售。工程团队的背景实力很强，不少来自 Google/Databricks/Splunk 类似背景的工程师，其中 21 年底从 Splunk 加入的工程 VP Ram Sriharsha，他是整个团队的工程核心，在向量存储、产品 Scaling 相关的架构创新上做了很多工作。而产品与销售团队主要来自于创业公司，少有大公司背景。

**产品发展**

**清晰的产品优化节奏**

2021 年 1 月，Pinecone 正式宣布公开测试版产品。在宣布中，CEO Edo Liberty 提到，他在亚马逊领导 Sagemaker 的期间意识到，很多公司运用 ML 的难点不在于训练或部署模型，而在于实时处理海量的向量数据：

• 向量需要被存储和索引；

• 索引需要随着数据的变化实时更新，其实时性对分布式计算的要求很高；

• 这个产品需要很好的运维和监控。

2021 年 9 月，Pinecone 2.0 发布，其中提供了元数据筛选的能力，使向量数据能被打上标签，使搜索兼具精准和模糊搜索的能力。例如，当我们想要搜索“金融”领域的数据时，数据库就可以高效的从 Industry = Finance 的向量数据中进行语义检索。同时 Pinecone 2.0 正式将产品定价与硬件使用量绑定，并将产品分为免费、标准和个性化三类价格梯度。

2021 年 12 月前 Snowflake CEO Bob Muglia 和前 Couchbase CEO Bob Wiederhold 宣布成为 Pinecone 的投资人和顾问。后者在 22年底成为了 Pinecone 的总裁和 COO，他此前是连续创业者，做过 Couchbase、Transitive 和 Tality 的 CEO。

从 2021 年下半年起，Pinecone 的工程团队意识到原本基于 C++ 和 Python 的架构不够高效，开始用 Rust 开始整体推倒重写。对于一款没有开发者社区支持的产品来说，这样的决定是很有魄力也很危险的，CEO Edo 一度也反对这样的想法。到 22 年 3 月，重写工作基本完成，完成后 Edo 事后总结这样的转变对公司后面的工程维护有着很大的优化。

22 年下半年开始，产品的更新速度显著加快：为向量索引提供快照记录的 Collections 功能上线、兼具语义搜索和关键词搜索优点的混合搜索能力加入，并且 Pinecone 在 GCP 和 AWS Marketplace 都上架了产品。

可以看到，**Pinecone 从产品发布第一天就以闭源 Saas 的思路在运营整个产品，对整个产品的优化方向有着很清晰的规划，技术革新有着很强的魄力。**其他精品如 Milvus、Weaviate 的产品思路都有与 Pinecone 亦步亦趋的迹象。清晰的优化路径才能带来今天的优势：当 LLM 爆发点到来的时候 Pinecone 成为开发者最拥护的产品。

**定价模型与商业化进展**

****收入尚有限，********但出色的产品体验使其****成为中小型创新团队的首选****

Pinecone 当前的定价是同时基于数据存储量和计算资源使用时长一起决定的，其中存储量每个月每 GB 定价在 0.025 美元，而计算使用量则是每小时 0.1 - 1 美元不等，根据算力等级有所差异。

向量数据库的商业化模式是 MLOps 中最接近 DataOps 的，有大量基于模型处理的数据留存，且迁移成本比其他 MLOps 工具来得显著要高；当然由于当前客户大多在早期使用阶段，还没有达到数据库那样特别高的迁移门槛。根据 Pinecone 的重要客户 Gong 的计算，如果他们持续使用这一服务，未来每年的成本将达到数十万美元。

而对数据进行向量化的成本在每1000 tokens 0.0004 美元，比最便宜的 GPT 3.5-turbo api 要便宜一个数量级。因此即使是向量数据库比较贵，考虑到其语义搜索能够以精准的搜索内容达到不错的效果，加上向量数据的可复用性，其价值也是非常高的。

**2022 年 Pinecone 商业化的主要难点在****于：**新型公司使用向量搜索的功能大多是实验性的，不够核心，因此客户对向量数据库的付费意愿会相对弱；而向量搜索占据核心功能的顶级大厂，自己有着自研和部署向量数据库的能力。例如 Atlassian 在调研发现 Pinecone 最为好用之后，仍然没有付费，很可能是实现这一功能并不那么重要。因此，2022 年的 Pinecone 的 ARR 只有百万美元的水平。我们通过用户调研深挖了这一现象背后的因素。

在对用户的调研中，我发现对 Pinecone 优点的称赞主要来自于以下两点：

**1. 产品实现好，使用门槛低：**

使用 Pinecone 完全不需要 infra 工程师的介入，就可以很快的完成开发投入生产。虽然是一个数据库产品，但其使用难度和把一个 Python Library 用起来一样低。这个优势帮助他们在早期和 Milvus、Weaviate 等产品的竞争中赢得了很多用户，其他两个竞品在推出云托管服务之前，都需要比较大的力气来让其稳定运行；

**2. Scaling 性能好，支持强实时性、高并发量：**

很多用户在使用中前期使用过 FAISS 算法和 Elastic 的类似功能，当数据量一旦增加后有明显不稳定的情况。尤其在一些网络安全的场景下，要求文本一旦被向量化，立马可以比对其异常情况，并且要有 500 以上的 QPS，在 2022 年上半年 Pinecone 是能最好满足这一要求的解决方案。

看到这里会发现，向量搜索的效果本身并不是决胜的关键，因为模糊的匹配没有 100% 正确的标准答案，**快速稳定地返回答案比精准来得更重要。**换言之，从 Elastic 的关键词搜索切换至 Pinecone 的语义搜索的提升很重要，但语义搜索精度的优化边际收益就没那么高了。

这里有一个前提：搜索的结果不会直接影响产品的收入，例如 Tik Tok 的视频召回准确率会直接影响产品的留存和收入，那么客户就会更倾向于 self-host 算法进行调优，而不是交给第三方去实现。这就引出了用户选择 Pinecone 的顾虑：

**1. 如果向量搜索是他们产品收入的核****心，**那么他们可能会使用开源方案自研并部署，这样可以对核心功能有更多的定制和调优的空间；

**2. 如果客户的数据是高度机密受监管****的，**不愿意放到公有云上部署，他们可能会选择开源模型 + 数据库自己部署。

根据这些调研，Pinecone 在 2023 年新增的用户肖像就很明确了：精简的 LLM 时代开发团队 LLM， Prompt 的调试比记忆检索更接近他们产品的核心，想要一个开箱即用的向量数据库服务。在未来这样的团队很可能不会成长为一个有很多工程师的大公司，也不会选择自研和 host 向量数据库的相关服务。

这类团队很可能大规模，且 LLM 和向量数据库是其最主要的成本项。因此，我认为在 LLM 时代的新型开发需求带有巨大的市场空间，尽管以前的需求没有给 Pinecone 挣到大规模的收入，但为其做好了产品打磨和需求理解的基础，而在未来有了很强的竞争力。说到这里，就让我们来看看 Pinecone 现在和潜在的竞争对手有哪些。

**竞争**

****竞争对手云集，****传统数据库和公有云厂商是更大的对手****

**1. OpenAI 是否会做向量数据库：不做****Retrieval Plugin 中需要外接 Pinecone 等数据库**

Retrival 召回插件被 Greg 称为 Plugin 中最特殊的一个。在最近的 TED Talk 中，Greg 的展示中也对 Retrieval 的进阶功能进行了展示，可以记忆用户的聊天历史，并基于个性化历史进行对话。有了 Retrieval Plugin，ChatGPT 离个人能力近了一步。

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/015.jpg)

在 Plugin 的项目代码中，官方推荐了使用 Pinecone 等作为插件搜索和存储向量数据用的数据库。考虑到大模型的训练和推理本身并不需要向量数据库，是基本解耦的，这一领域大概率不会直接受 OpenAI 的产品影响。

**2. 创业团队**

**• Weaviate**

来自荷兰的 SeMI 团队打造的开源数据库 Weaviate 也获得过 OpenAI 官方的推荐，推荐语中其实就清晰地解释了 Weaviate 和 Pinecone 的差异：Pinecone 的服务是完全交给他们和 AWS/GCP 托管的，包括数据存储和资源管理；而 Weaviate 则把这项任务交给用户 self-host，自己提供支持性的运营和服务。

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/016.png)

对于不想自己花精力和成本 host 服务的客户来说，Pinecone 的服务更加一体化和开箱即用；对于不愿意将数据完全交出去、希望有自主控制权的用户来说，Weaviate 的方式更加灵活，但也需要相对大的时间成本。

Weaviate 希望通过好的运营和产品体验获胜，认为 MongoDB 是赢在流畅的产品体验。2022 年付费量不大，ARR 在 5 万美元左右。最近他们也已经推出了自己的云服务。

**• Chroma**

Chroma 是由在旧金山的连续创业者 Jeff Huber 和  Anton Troynikov 创立的。他们俩分别来自 3D 视觉和机器人领域，对 AI 领域的需求很熟悉。他们的产品比 Pinecone 和 Weaviate 更加轻量级，目前还是一个开源项目的形态，正在开发自己的托管产品中。当前整个产品还在比较早期的阶段开放使用，暂时没有商业化收入，Pinecone 的免费服务受到限制之后，很多用户迁移到了 Chroma 进行开发，很好的积累了早期用户。

**• Zilliz**

Zilliz 是一支来自中国的团队，他们打造的 Milvus 是最早发布的向量数据库。在 Milvus 1.0 阶段，产品形态比较接近 Weaviate，是一个封装了近邻搜索算法的向量搜索产品；而到了 Milvus 2.0 阶段，产品形态就更接近 Pinecone，提供了 Zilliz Cloud 这一完全托管的服务，同样是在 AWS 和 GCP 上提供。产品定价上，在存储端价格与 Pinecone 基本一致，计算端的小时单价是 Pinecone P2 Pod 的两倍、V1 Pod 的三倍。

**• Vespa，Yahoo 开源产品**

Vespa 是来自 Yahoo 的开源产品，有些类似 OLAP 届的 Clickhouse：很多企业基于这一产品 self-host 向量数据库，但少有用户为产品付费。

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/017.png)

**3. 传统数据库：Elastic Search / Redis / Snowflake**

从一个角度来说， 这类公司有着很大量级的 ARR、很多客户在使用他们的服务。对于 vector search 的需求，他们对速度和规模的支持都比较弱。由于这当前不是个大市场的需求，可能还没有进入他们主要重视的阶段。而当这一市场成长到足够大以后，未来模型对输入的 token 数可能会达到无限长，那时候 Elastic 关键词搜索和 vector DB 语义搜索的性能差异可能会被缩小：搜索召回的精度没那么重要，模型都能大规模的输入并理解。

但从另一个角度说，如果他们选择进入这一市场并将性能优化好，考虑到很多客户的数据都在他们的数据库上，一体化的解决方案对开发者的吸引力是很强的，不用新签合同，只需要提高对正在使用产品的预算也是流程上更友好的。主要的问题是他们相对传统的工程架构，是否能适应这一新的需求。目前 Redis 已经在积极的进入这个市场了。

在这三者中，尽管 Snowflake 和 Redis 比起 ES 离这一领域更远，但是我们认为同样也是 Pinecone 值得畏惧的对手，因为这两家公司使用的技术架构更新、计算速度更快，不像 Elastic Search 天生在语义搜索的能力有一定的 scaling 缺陷。

**4. 公有云厂商：AWS/GCP/Azure**

和 10 年代的竞争一样，公有云厂商永远是现代数据库的竞争对手：尽管 MongoDB 在开发者领域有着很好的生态，AWS 的 DynamoDB 在收入上并不显著逊色。

GCP 在 Vertex AI 上有自己的向量数据库 Matching Engine。作为同时拥有很强搜索和 AI 能力的谷歌，有这样的能力并不让人吃惊，如果他们把 Bard 的 embedding 能力和向量数据库做好整合，是一个很大的竞争对手。毕竟 Pinecone 本身只负责加工和存储来自别的 api 的能力。

同理，Azure 和 AWS 尽管目前没有向量数据库产品，也有相应的能力建设，在各自的云平台上搭建一套 LLM + 向量数据库的整合能力是他们潜在的目标之一。尤其是 OpenAI api 是 Azure 主要的服务之一，他们目前没有也没有和 Pinecone 产生合作，微软很有可能推出向量搜索的能力，直接将 GPT3.5 Embedding 存在 Azure 上提供搜索服务。

**04****.**

**探讨与展望：智能体的结构、LLM 和 DB 的关系是尚不明晰的关键问题**

刚刚列举了 Pinecone 众多的竞争对手，想必能感知到整个向量数据库市场现在还在早期阶段，未来的变化值得我们一起持续关注。除了市场本身的格局之外，有两个问题值得深入讨论与思考，也会对向量数据库的位置产生重要影响。

Pinecone 在官网把自己定义为 Long-term Memory for AI，我认为这是有待商榷的。回到开篇对人类智能的讨论，我们提到大模型是记忆缺失的大脑，而向量数据库是补足这一能力的海马体。其实调用 Pinecone 的过程，比较像人类死记硬背使用短期记忆的方式。因为当我们进入某一领域时，会首先根据一些知识与过来人的经验依葫芦画瓢，然后随着自己的试错和经验积累慢慢形成自己的直觉、风格和行为习惯，直到那时我们才成为这一领域的专家。而 Pinecone，只实现了依葫芦画瓢的那一步。

换言之，从人类智能的角度看，**Pinecone 是短期记忆，LLM 是长期记忆**，但目前他们之间的交互还是单向的，缺少了短期记忆累积沉淀，形成长期记忆的过程。但直接去调整大模型的参数是不太可行的。因此这一过程可能需要一些新的组件来弥补，例如一个基于 Lora 进行微调的小模型，来帮助大模型做一些领域专业知识的记忆；也或者是由多个 LLM 交互形成群体记忆，来达到更新长期记忆的效果。

无论是哪一种方式，都有可能对向量数据库产生依赖或替代的关系，甚至有可能 Pinecone 会根据客户需求提供这样的能力。因此未来的架构变化对向量数据库的重要性至关重要。

同时，还有一种观点认为，**当 LLM 能够读入无限 token 时，向量数据库的必要性就不大了**。理论上这是完全可行的，但这忽略了经济成本和工程复用性的问题。当每一次执行都要将相关语料库不经检索地作为 prompt 输入时，其中大部分的内容信息增益和 ROI 是很低的，可能带来很多不必要的商业成本和资源浪费。尤其是当大模型允许多模态输入之后，这一问题会更加显著。而且模型使用向量化的记忆，再将输出向量化存入记忆中是很好的记忆回路，能够一定程度上 LLM 对过往经验知识的总结和复用。

随着 LLM 能力越来越强，还会有很多这样的讨论。其背后隐藏的主线逻辑是：**当 AI 能有这么强的信息提取和组织能力之后，传统数据库的很多能力是受到冲击的。**

向量搜索的普及过程中，很多之前用 SQL 和结构化数据比较难解锁的产品功能自然得到了实现，长期用户的使用范式肯定慢慢会从传统数据库转移到 LLM + Vector DB。那么**数据仓库未来会如何面对这一冲击，届时的 Vector DB 又比今天的形态复杂多少呢？**这是值得我们一起持续思考和关注的重要问题。

**Reference**

**1. 丁香医生，遗忘症科普：**https://mp.weixin.qq.com/s/oGSjxydwi5f-I\_tsJ2ZC1A

**2. Jina，AutoGPT 对向量数据库的过度使用：**https://mp.weixin.qq.com/s/9KS4rWLBCXFo7R9LRB0fhw

**3. The rise of vector data:** https://www.pinecone.io/learn/rise-vector-data/

**4. Inside the pinecone:** https://www.pinecone.io/learn/inside-the-pinecone/

**5. Edo Liberty 在 CMU Andy 课上的分享：**https://www.youtube.com/watch?v=8LXotdzX\_84

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/018.png)

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/019.png)

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/020.png)

延伸阅读

[![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/021.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501117&idx=1&sn=e860ac5e259a969f62b05d080bf42d14&chksm=ce9b7aa3f9ecf3b503656e9a09b55210fdba0844b54bd6a5714f5fc8c57b8c3570acbe2d342f&scene=21#wechat_redirect)

LangChain：Model as a Service粘合剂，被ChatGPT插件干掉了吗？

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/022.png)

[![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/023.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501768&idx=1&sn=333ee99a036fcefce15edc127a236f63&chksm=ce9b7856f9ecf14081c419fb9980c76624ed531a188b9b55c339b93019deafbe63b96f6d4fef&scene=21#wechat_redirect)

22年逆风后，Stripe能靠AI扳回一局吗？

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/024.png)

[![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/025.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501716&idx=1&sn=5422dbcec1099d7a0cc9df87d18941c6&chksm=ce9b780af9ecf11c6ee9a7743d0ee7a50eba3e36baa28fba92891d5b94db93dec391d0b70c27&scene=21#wechat_redirect)

拾象AI投资图谱：挖掘AIGC军火产业链，颠覆巨头的机会和风险

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/026.png)

[![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/027.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501604&idx=1&sn=52bc78af407aacc49549f0bb050cffce&chksm=ce9b78baf9ecf1ac66bd00c5030b72ffe6628e241dcc2f3088d323bf94f62681691a66cbd95d&scene=21#wechat_redirect)

Replit：“人人可编程”的探索者，代码生成时代的Figma

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/028.png)

[![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/029.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501517&idx=1&sn=623a0cc2c384de58da437b5ed5ef2d2c&chksm=ce9b7953f9ecf0458a113dbc3ef2c3d6b2482894d9e747775252a5b17dde107b7d7636306499&scene=21#wechat_redirect)

Discord和它的中国“学徒”们

![](../images/2023-04-26-pinecone-da-mo-xing-yin-fa-bao-fa-zeng-chang-de-xiang-liang/030.png)
