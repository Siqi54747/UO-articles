---
title: Deep Research 类产品深度测评：下一个大模型产品跃迁点到来了吗？
publish_date: '2025-04-21'
publish_timestamp: 1745241193
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/Ho3gGGRuAZpt9_zg2vrFwg
msgid: 1000000345
appmsgid: 2247512752
itemidx: 1
digest: 本文聚焦 Tool Use、Instruction Following、Memory 以及报告输出能力进行评估。
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgycxwhl1qRicoPP0wmLqe762sKZp8z3FT2MlibUdXa2dmM9v5pBlFnONop5s1VuDwE1LaYm0a7kl74w/0?wx_fmt=jpeg
image_count: 87
archived_at: '2026-04-20T03:28:21+08:00'
---

[![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/001.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&scene=21#wechat_redirect)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/002.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/003.jpg)

作者：Krystal

编辑：penny

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/004.png)

从 2024 年末问世的 Google Deep Research，到 2024 年 2 月以来密集发布的 OpenAI Deep Research、Perplexity、xAI Deep Search、Manus，Deep Research 成为各家 Agent 产品角逐的白热化赛道。

Deep Research 产品可被理解为**一个以大模型能力为基础、集合了检索与报告生成的端到端系统，对信息进行迭代搜索和分析，并生成详细报告作为输出。**

参考 Han Lee 的 2x2 分析框架，目前 Deep Research 类产品在**输出深度、训练程度**两大维度呈现分异。**输出深度**即产品在先前研究成果的基础上进行了多少次迭代循环以收集更多信息，可进一步被理解为 Agentic 能力的必要基础。**低训练程度**指代经过人工干预和调整的系统，比如使用人工调整的 prompt，高训练程度则是指利用机器学习对系统进行训练。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/005.png)

**和传统 LLM Search 产品相比，Deep Research 是迈向 Agent 产品雏形的一次跃迁，可能也将成为具有阶段代表性的经典产品形态。**

Deep Research 产品通过系列推理模型嵌入，已生长出了 Agent 产品必要的推理能力。

更为关键的是，是 Deep Research 采用多次搜索和异步返回模式，在持续搜索过程中迭代和优化回复，从而输出更符合用户需求的内容，信息推理深度显著提升。这一自主计划、反思、行动的落地，是 Agent 路线图中必须迈过的一级阶梯。

💡 目录 💡

     

     01  测评对象

     02  测评任务

     03  测评结果

     04  总结：走向下一级 Agent 阶梯

**01.**

**测评对象**

为描画当前 Deep Research 产品版图，厘清主要产品的能力层次，本文选取 Google Deep Research （下称 Google）、OpenAI Deep Research （下称 OpenAI）、Perplexity （下称 PPLX）、xAI Deep Search （下称 xAI）、Manus 五个产品进行测评，主要维度比较如表 1 所示。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/006.png)

表 1 测评产品比较（信息截至 2025 年 4 月）

从这一比较不难发现，除 Google、xAI 以外，迄今其他三家产品均支持图片等多模态输出。

考虑到目前公开性能表现有限，包括 Hugging Face、JINA 等团队自行的开源复现项目，并不在此次测评对象之中。

**02.**

**测评任务**

本文锚定**“Agent 能力+产品核心能力”**任务框架设计，聚焦 Tool Use、Instruction Following、Memory 三大维度的 Agent 能力，以及**报告输出能力**这一 Deep Research 的核心性能，对五大 Deep Research 产品进行评估。

需要指出的是，**Memory 没有进入到最终的任务域。**主要原因在于，经多任务测试，Deep Research 的自动联网检索构建了一个“后门机制”，即使向其投喂长文，它也可以通过联网检索获得精炼信息，从而绕过用户给定的长文 context。因此，目前难以通过长文 prompt 有效评估其 memory 空间。

本文最终的**“2+1”任务设计选取遵循“代表性案例”思路**，完成各任务的主要能力可被视为 Tool Use、Instruction Following 等“代理变量”，二者并非严格对应关系。在不同能力维度统摄下，分别设计了任务场景如下。

**Tool Use**

**在线检索能力：小众内容定位**

小众内容检索反映出模型处理在线信息“长尾效应”的综合能力，亦是 ODR 团队访谈中提到的优势任务，如 Josh Tobin 所言：“当你有一个需要详细描述的问题，而且获得最佳答案需要大量阅读互联网内容时，Deep Research 真的特别擅长。如果你提出一个比较宽泛的问题，它会帮你理清楚具体想要什么。但它最出色的表现是在**查找特定****信息**时。”

**Task 1 冷门电影检索**

本文参考 IMDb 观影全球评论数，选取了一部冷门电影（N<500），截取了电影中非关键帧场景，对其进行简要描述，逆向检索电影名称，从而评估 Deep Research 产品是否能依据有限信息，通过外部网页检索，准确定位到长尾内容。

**Task 2 最新书籍检索**

考虑到测试内容可能在模型训练集中出现，为提升测评信度，本文设计了最新出版书籍的检索任务，选取了于 2025 年 4 月刚出版的经济学书籍《Startup Capitalism New Approaches to Innovation Strategies in East Asia》，并使用书中使用的理论框架和案例提供线索，再次检测产品的检索能力。

**数据分析能力：基于财报的因子计算**

数据分析能力体现了产品对数据进行基础处理以及复杂分析的性能，评估其数值分析的准确性、推理逻辑可靠性的综合表现。

本任务关注 Tesla 财报信息的因子计算，选取基于财报以及 Earnings call 的结构化数值数据分析，提供 EPS 增速跳跃因子这一指标的计算公式，评估产品调用代码进行数值计算的自主性和有效性。

**编程能力：智慧城市设计**

产品设计规划需要进行目标分析、流程分解、方案比较，并通过 coding 加以实现，贴合效率、美观等现实目标进行创新，能够评估模型在给定目标下进行自主探索的潜力。

本任务围绕智慧城市大脑的前端产品场景，要求模型通过数据计算、指标构建、模块设计，最终形成一个能够展示的网页解决方案，从而评估模型贯穿美观设计、指标运算、代码落地的全流程能力。

**Instruction Following**

**文献分析能力：多话题科研综述**

科研文献综述需要模型围绕特定科学问题进行文献整合与现状梳理，难点一在于专业领域文献的检索源可得性确认，难点二在于分析特定领域研究的纵深性，完成对已有文献的整合分析。

本文基于文献综述这一任务场景，进行分段任务设计，其中每段的综述主题、数据信源、分析逻辑、字数要求、引用格式均有所不同，通过不同维度的差异化要求，考察产品对于“碎片化”需求的 instruction following 程度。

**路线设计能力：旅游方案规划**

消费方案推荐要求模型对消费属性以及用户评论进行全方面检索与梳理，并在个体偏好、预算等多重约束条件下，生成最优规划，主要体现在旅行规划和购物推荐两大任务，ODR 团队 Isa Fulford 在访谈中推荐：“我认为**购物和旅行****推荐**是最主要的应用场景。我个人已经使用这个模型好几个月了。”

本文设计了一个上海-韩国旅游规划的场景，考察产品兼顾时间要求、消费预算限制、目的地偏好，最终提供具有一个用户需求贴合性、可行性方案的 instruction following 能力。

**报告输出能力：研报分析**

市场研报分析考察模型自主确定关键分析维度、确认数据来源，结合宏观趋势、中观行业、微观企业与用户的多角度整合分析表现，并在报告输出环节保证数据与图表的结构化输出。

本文围绕关注的 AI 招聘初创公司 Mercor，要求产品从市场格局、产品技术、商业模式、竞品公司、团队特征进行调研分析，并强调可通过图表形式可视化。

**03.**

**测评结果**

**Tool use 能力**

**在线检索：OpenAI“一骑绝尘”**

**Task 1**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/007.png)

根据一幕线索顺藤摸瓜出一部冷门电影，**这一任务只有 OpenAI 成功检索出电影名《布宜诺斯艾利斯 100 公里 （Buenos Aires 100 km）》，其他产品均在“狐疑”中给出了错误答案。**

需要指出的是，五家产品均收到了两次机会——在收到第一轮 prompt 时，均未给出正确回复，而在提示“这部电影好像是在阿根廷拍摄”后，OpenAI 结合这一线索成功定位到电影的主要信息。

本文选取测评镜头并非电影关键情节，并且描述极尽简单，OpenAI 能够在极其有限信息的情况下，展开多源网页搜索，验证了其主打的“小众内容检索能力”确实一骑绝尘。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/008.png)

图 OpenAI 的正确电影输出

Manus、Google、xAI 三家产品则在回复语气中透露出一丝迟疑和不确定性，在表示需要更多信息继续推理的同时，给出了 3-5 个错误回复。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/009.png)

图 Manus 的电影猜测结果

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/010.png)

图 Google 的电影猜测结果

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/011.png)

图 xAI 的电影猜测结果

而 PPLX 则在输出中坦诚表示，基于给定线索，无法给出任何潜在答案，未生成其他冗余信息。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/012.png)

图 PPLX 的无结论输出

**Task 2**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/013.png)

与 Task 1 结果无异，OpenAI 在给出三本潜在书籍结果的同时，**仍是唯一成功检索到正确书籍的产品，**Google 和 xAI 则提供了一些更为古早、延伸性的书籍和论文，Manus 则未输出实质性书籍检索结果。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/014.png)

图 OpenAI 的正确书籍输出

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/015.png)

图 Google 的书籍猜测结果

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/016.png)

图 xAI 的电影猜测结果

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/017.png)

图 Manus 的书籍猜测结果

**数据分析：“全军覆没”**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/018.png)

在初始 prompt 中，产品被要求自行挖掘财报和 earings call 相关信息，并根据给定公式进行计算。然而，PPLX 并未正确爬取各季度的 EPS 数据、以及同比每股收益增长率 （%），可能存在信源偏差问题。

因此，在第二次 prompt 中直接给定了 Tesla 在 2023 年 Q1 到 2024 年 Q4 的 EPS growth 的数据，要求产品进行计算。

这一计算过程并不算复杂，用普通最小二乘法（OLS）即可完成拟合，**然而，五家产品均败下阵来，无一成功计算出正确数值，且“各有各有的问题”。**

**“中道崩殂”：**

**xAI、Google 未完成计算任务**

**•** xAI 大篇幅展示了对于计算公式的理解，长篇大论看似严谨，然而【预测 2024 Q1（基于 2023 Q2-Q4 和 2024 Q1）】的表述，**实则未能正确理解公式。**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/019.png)

图 xAI 展示的计算过程

**•**xAI 在给出了计算样例后，仅完成了 1/4 的计算量，输出了第一个数据点 2024Q1 的计算值，其对于公式的错误理解导致基准有误，作为唯一输出的 -4.19 同样与正确答案差之千里。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/020.png)

图 xAI 未完成的因子计算

**•****Google 对计算口径的理解具有明显偏差**，将所需数据点错误推至 2025 年 Q1，基于这一错误逻辑，其同样未完成极端，甚至未输出任何测算结果。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/021.png)

图 Google 给出的计算示例

**“南辕北辙”：**

**PPLX 计算对象错位**

**•** PPLX 早在输出中重复了 prompt 中提到的计算方式，在计算公式渲染效果上更胜一筹，**但从结果来看，其同样未能正确理解计算逻辑，**混淆了 2024 年 Q1-Q4 的计算对象，反而输出了 2023 年 Q3-2024 年 Q2 的计算值。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/022.png)

图 PPLX 展示的计算过程

**•** 相较于 LLM Search 计算的结果，PPLX 将计算数值结果与市场分析文本高度杂糅，使得其答案异常隐匿。其输出的 4 个结果点中，2024 年 Q1、Q2 符合计算需求，但同样并非正确答案。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/023.png)

图 PPLX 的错误计算数据点

**“失之毫厘”：**

**OpenAI、Manus 计算结果略有偏差**

**从计算对象准确性、计算完备度而言，OpenAI 和 Manus 在这一数据分析任务中表现出最高的能力成熟度。**二者均正确了定位了 2024 年 Q1-Q4 的分析目标，且在数值计算的大方向上把握正确，但在数值计算的微观代码实现层面有所偏差。

**•**OpenAI 基于表格直接给出了 2023 年 Q2-2024 年 Q4 的计算结果，尽管输出并非完全准确，但其 2024 年 Q1-Q4 在数据整体分布趋势上与正确数据相似。**由于并未给出数值计算的完整运行代码，难以排查其计算偏差发生点。**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/024.png)

图 OpenAI 的计算结果

**•**Manus 在明确给出了计算结果的基础上，主动输出折线图、条形图对结果进行可视化，相较于 OpenAI 的表格更具易读性。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/025.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/026.png)

图 Manus 输出结果与可视化图表

但 Manus 在回归运算过程中未能正确处理数理逻辑，使用了带有截距的 np.polyfit 进行计算，导致结果出现偏离。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/027.png)

图 Manus 的代码运算偏差

**编程：Manus 领衔，三大梯队分化明显**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/028.png)

针对这一结合设计 + coding 的任务，五家产品的输出呈现出显著分层。

**第一梯队：Manus“多快好省”**

**•**Manus 是唯一提供了完整项目文件，顺利运行网页，且在功能和美观性上均达到合格线的产品。值得注意的是，其不仅完全兑现了“环境洁净指数”等指标可视化展示、舆情分析等各项要求，还增加了【最新城市动态】一栏动态板块，产品意识超前。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/029.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/030.png)

图 Manus 输出的网页设计结果

**第二梯队：OpenAI“可以 run”但“不美观”**

**•**OpenAI 给出了 HTML、CSS 和 JavaScript 三个文件，保存到本地后形成了一目了然的原始网页，能够发现环境洁净指数等组件，仪表盘和折线图并列一行，勉强实现了数据展示功能。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/031.png)

图 OpenAI 输出的网页设计结果

**第三梯队：Google、xAI、PPLX“run 不了”**

**•**Google 并未给出可执行的前端网页完整方案，而是从“拟真”视角在每个部分象征性提供了一个代码模板。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/032.png)

图 Google 输出的网页设计代码

**•**xAI 以简洁形式分块给出了示例，但内容极度简洁，代码块无法构成可运行网页。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/033.png)

图 xAI 输出的网页设计代码

**•**PPLX 给出了分区运行文件模版，但缺乏相应图表和资源，本地保存后同样无法正常运行网页。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/034.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/035.png)

图 PPLX 输出的网页设计代码

**Instruction Following 能力**

**文献分析：“选择性执行”居多**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/036.png)

从三段任务输出总结来看，五家产品均**无法完全****遵循指令进行文献分析**，按照所要求的内容逻辑、引用规范、组织结构、字数体例的执行力不一，**在这一任务上体现的指令执行力均有瑕疵。**

**“选择性执行”组：**

**OpenAI、xAI、PPLX**

**• OpenAI 在末段中的现有文献总结和表格输出相较于其他四家产品，在结论梳理和字数上均更符合规范**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/037.png)

图 OpenAI 的末段文献综述输出

**•** OpenAI 的首段即无视了字数和主题要求，花了近一半篇幅点出透明和信任的概念，但随后偏移到了论述二者的关系，字数超过 500 字，未完全满足要求。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/038.png)

图 OpenAI 的首段输出

**•**xAI 是五家产品中唯一严格执行字数要求的“字数警察”，主动在各部分标注了总字数。且首段内容严格围绕概念论述，并无走题情况。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/039.png)

图 xAI 的首段文献综述输出

然而，可能正是受制于字数的严格执行，其按照要求进行内容分析的表现差强人意，在研究现状总结和未来研判的表现明显劣于前者。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/040.png)

图 xAI 的末段文献综述输出

**•****PPLX 是唯一完全遵循了第二段要求的产品，**在第二段输出中明确论述了各个研究的理论基础、假设逻辑，并且在此部分内容“简美”，未超过字数上限。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/041.png)

图 PPLX 的第二段文献综述输出

但 PPLX 的首段输出同样并未依照指令进行概念的论述，而是将重点偏离至二者的关系，**在指令内容之外“夹带题外话”似乎是贯穿五家产品的通病。**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/042.png)

图 PPLX 的首段文献综述输出

**“对牛弹琴”组：**

**Google、Manus**

Google 在指令遵循方面属于**内容逻辑与字数体例叛逆选手，**在首段并未按照 prompt 要求在 500 字内论述透明、信任的概念，而是洋洋洒洒地从概念谈到二者关系。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/043.png)

图 Google 的首段文献综述输出

在第二段内容中，Google 并未按照要求分析整理 2021 年以来的高被引文献，并论述其各自理论基础，而是采用一种绕口令地方式重复文章内容。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/044.png)

图 Google 的第二段文献综述输出

Manus 首段的内容逻辑并未严格围绕透明、信任概念，而是天马行空地谈到二者关系的调节因素，实际输出字数完全超过 500 字要求。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/045.png)

图 Manus 的首段文献综述输出

Manus 输出的第二段内容与第三段指令有所混淆，本应出现在末段的未来方向研判和参考文献同样出现在了第二段。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/046.png)

图 Manus 的第二段文献综述输出

**路线设计：xAI 掉队明显**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/047.png)

由于旅游路线设计作为一个典型的多目标规划问题，需要满足时间、距离、预算等多重可行性，难以从主观角度进行全面评估，故本文设计了一个六维评估体系，包括**旅游目的地丰富度、目的地交通时间、交通方式合理度、预算利用率、购物体验丰富度、咖啡馆体验丰富度**六项指标，由 Deepseek R1 对五家产品给出的旅游方案分别进行打分（每项满分为 5 分）。

**瑕疵明显：**

**xAI 走马观花**

xAI 提供的方案并未观照 prompt 中的咖啡馆体验需求，未设计主题咖啡馆路线，缺乏专业级咖啡体验（烘焙工坊/杯测活动，同时建议前往南怡岛游览与咖啡和购物主题相关度较低，有走马观花之感。

针对此方案，R1 给出的各指标得分如下：

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/048.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/049.png)

图 xAI 的旅游方案策划

**美中不足：**

**PPLX 目的地较同质化**

该方案在购物/咖啡的核心需求上实现度超预期，但近覆盖首尔核心区域（明洞、江南、弘大），并未涉及传统市场等购物体验。

针对此方案，R1 给出的各指标得分如下：

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/050.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/051.png)

图 PPLX 的旅游方案策划

**接近满分：**

**Google、Manus、OpenAI**

**•**Google：交通可行性不足

Google 方案的 1 分同样扣在前往釜山的交通时间，跨城交通成本吞噬 37%有效游览时长。

第一天：抵达首尔 & 明洞美妆购物

第二天：景福宫与弘大

第三天：江南时尚与 K-Pop 体验

第四天：釜山一日游

第五天：特色咖啡馆与艺术街区

第六天：首尔全景

第七天：离境前的最后购物

针对此方案，R1 给出的各指标得分如下：

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/052.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/053.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/054.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/055.png)

图 Google 输出的旅游方案

**•**Manus：交通可行性不足

唯一用 html 手册格式输出旅游方案的产品，整体来讲，首尔动线完成“美妆-轻奢-潮牌”的完备消费策划，但在交通动线设计上仍有资源错配不足。

针对此方案，R1 给出的各指标得分如下：

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/056.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/057.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/058.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/059.png)

图 Manus 输出的旅游规划手册

**•**OpenAI

OpenAI 相较于其他产品方案，真正考虑到了购物需求，但仍在釜山跨城交通上略有损耗。

针对此方案，R1 给出的各指标得分如下：

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/060.png)

第 1 天：上海 ✈ 首尔 – 抵达首尔 & 明洞购物美食

第 2 天：首尔 – 古都文化探索 & 韩屋咖啡体验

第 3 天：首尔 – 潮流时尚购物 & 年轻活力夜生活

第 4 天：首尔 🚄 釜山 – 高铁前往釜山 & 甘川文化村、南浦洞市场游

第 5 天：釜山 – 海滨风光 & 咖啡休闲体验

第 6 天：釜山 – 休闲自由行（可选行程：温泉放松或购物扫货）

第 7 天：釜山 ✈ 上海 – 返回温馨之家

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/061.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/062.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/063.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/064.png)

图 Google 输出的旅游方案

**报告输出能力**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/065.png)

基于商业研报场景，从**信息准确性、分析完整性、观点创新性、媒介多元性、论证充分性**五个维度对五家产品的报告输出能力评估，基于报告整体的可用性，各产品能力排序为：

**OpenAI > Manus > PPLX = xAI >> Google**

**•****OpenAI：90 分，兼顾深度与广度**

**OpenAI 的分析视角和行文风格是五家产品中最具有专业性、拟真性，也是唯一精确锚定三大竞品公司并展开比较分析的产品。**

从可用性而言，在 OpenAI 输出报告基础上稍加语言修缮、添加图表后即可作为一份咨询建议阅读。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/066.png)

图 OpenAI 对 Mercor 的竞品分析

**•****Manus：85 分，全视角、强图表意识的实习分析师**

Manus 的优势在于**分析维度的高效全面分解**，能够在市场趋势、外部竞争的信息中提炼出明确观点；并且相较于其他产品，在对应章节**自主绘图意识极强**（尽管渲染不完全稳定）。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/067.png)

图 Manus 对 Mercor 的竞品分析与矩阵图

在五家产品中，**仅有 Manus 明确提到 Mercor 存在估值泡沫风险，**但在信息准确性、论证充分性方面存在不足。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/068.png)

图 Manus 对 Mercor 的潜在风险分析

**• PPLX、xAI：70 分，基本达标**

PPLX 与 xAI 输出报告的尴尬之处在于**，整体质量都在及格线以上，但作为投资简报 bullet point 观点清晰度不足，而作为 ground truth 进一步拓展分析，创新性又有所欠缺。**

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/069.png)

图 xAI 对 Mercor 的竞品分析

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/070.png)

图 PPLX 对 Mercor 的竞品分析

二者在分析上专业性上“平分秋色”。xAI 受限于输出媒介，无法像 PPLX 一般输出分析图表。在竞品公司锁定上，xAI 相较于 PPLX 更为精准，而对于潜在风险分析，PPLX 的输出则有“套公式”之嫌。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/071.png)

图 PPLX 对 Mercor 的潜在风险分析

**•****Google：60 分，以总篇幅“见长”**

**Google 输出的报告停留于整合基本事实信息，分析观点并不明确，且在商业分析方法论上存在偏差。**对于 Mercor 的竞品公司，其仅仅与传统招聘平台进行比对，在识别同赛道产品公司有明显缺失。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/072.png)

图 Google 对 Mercor 的竞品分析

同时，与其前序任务表现一致，Google 在商业命题报告的论证深度有限，而是在模型幻觉之下输出一部“加长版”的扩写作文，信息密度极为有限。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/073.png)

图 Google 对 Mercor 的潜在风险分析

**04.**

**总结：**

**走向下一级 Agent 阶梯**

回到本文开始的问题，相较于前代 LLM Search，陆续问世的 Deep Research 产品正在打破外部工具调度、需求执行的平均线。

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/074.png)

Gemini 不拘于任务场景，以报告篇幅取胜，换言之，其模型幻觉仍有待干预。

OpenAI 在报告输出、分析、设计任务中综合表现最强，长尾内容检索能力确如其官方所称“行业标杆”，但在数据分析、编程维度的 tool use 潜力仍未完全实现。

PPLX 在各任务中将将达到合格线，但在具体产品能力上“难有姓名”。

xAI 的相对优势在于保留了短平快的检索底色，坚持“不说废话”，尤其在涉及字数要求的任务中表现出稳定的 instruction following 能力，但多目标规划设计能力较为薄弱。

Manus 作为衔接了 Deep research 和其他 Agent 功能的产品形态，其 tool use 能力有显著优势，但 instruction following 仍有行动空白。

但从测评结果来看，**Deep Research 作为 Agent 产品的初代形态，无论是 Agent 的内生能力、亦或是长文本报告输出能力，消除可见的短板障碍，触达天花板仍需要市场的耐心。**

在这一浪潮褪去后，Agent 产品的下一级阶梯，或许将更快降临。

**Reference**

1.

https://leehanchung.github.io/blogs/2025/02/26/deep-research/

**2、****ODR 团队访谈**：****

https://www.youtube.com/watch?v=bNEvJYzoa8A

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/075.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/076.png)

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/077.png)

排版：Doro

延伸阅读

[![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/078.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512371&idx=1&sn=18a739c12c028fd9748d12f9eab50551&scene=21#wechat_redirect)

B2B 场景下的 AI 客服，Pylon 能否成为下一个 Zendesk?

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/079.png)

[![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/080.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512336&idx=1&sn=f149c8f599f037377f0e75a0111a9c7d&scene=21#wechat_redirect)

The Second Half：一位 OpenAI 科学家的 AI 下半场启示录

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/081.png)

[![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/082.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512305&idx=1&sn=307f2ebde8ee40d2d13e621230d6fcfe&scene=21#wechat_redirect)

AI Agent 摩尔定律：每 7 个月能力翻倍，带来软件智能大爆炸

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/083.png)

[![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/084.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512241&idx=1&sn=a2a3fe33f7b0038afd75f4d948d42c5f&scene=21#wechat_redirect)

为什么 AI Agent 需要自己的浏览器？

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/085.png)

[![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/086.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512202&idx=1&sn=6cd431892eba5b3a19bcc5faa7172146&scene=21#wechat_redirect)

Exa：给 AI Agent 的 “Bing API”

![](../images/2025-04-21-deep-research-lei-chan-pin-shen-du-ce-ping-xia-yi-ge-da-mo/087.png)
