---
title: Endor Labs：比Snyk更进一步的开源安全卫士，Prisma Cloud操盘手创立
publish_date: '2023-11-02'
publish_timestamp: 1698926400
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/xab2t6AKYF0n9z10HkChOg
msgid: 1000000231
appmsgid: 2247505317
itemidx: 1
digest: Endor Labs 为应用安全提出了一套新的叙事和愿景。
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgziaCKh0ZP1TkRXpibblPz6hK0Cs1p2U42WIK4MQSobLoCkicGe1VBjWsYtIRlDEhg6JUIOP4eN3hdAA/0?wx_fmt=jpeg
image_count: 30
archived_at: '2026-04-20T01:47:37+08:00'
---

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/001.gif)

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/002.png)

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/003.png)

作者：程天一

排版：Scout

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/004.png)

Endor Labs 处于应用安全、Shift-Left、软件供应链安全（SSCS）和开源安全的大潮之下，其两位创始人在 Palo Alto Networks 工作期间感受到当前应用安全工具难以平衡开发生产力与合规性，因此希望构建一个更强调可触达性和依赖关系的平台来保护当前使用了大量开源代码的软件开发过程，同时让组织无需为此支付“生产力税”。

这家公司最大的亮点之一在于其创始团队。在 Nikesh Arora 于 2018 年接任 Palo Alto Networks 的 CEO 之后，他激进地通过超过 10 笔收购搭建起了公司的云安全 Portfolio。这些被收购公司的创始人大多在 Palo Alto Networks 停留了相当长的时间，并且担任 Prisma Cloud、Cortex 等业务的顶梁柱。Endor Labs 的两位核心创始人就走过了这一路径。**其 CEO Varun Badhwar 在 18 年将自己创立的 CSPM 公司 RedLock 卖给 Palo Alto Networks 之后担任其 SVP 和 Prisma Cloud 的 GM，将这一业务一手带到 3 亿美元 ARR，在 2021 年离职创立 Endor Labs。**

Endor Labs 围绕可触达性的架构及叙事获得了市场的充分认可，在今年的 RSA Innovation Sandbox 和 Black Hat Startup Spotlight 均成为决赛选手，拿下了 Navan、Zoom、Five9、Atlassian 等优质科技客户并且在美国前十大银行中的 4 家内进行试点。2023 年 8 月，Endor Labs 宣布逆势完成了 7000 万美元的融资，由 LSVP 领投。在跟 AI 的结合上，Endor Labs 推出了 DroidGPT，将聊天式的自然语言交互与开源包的风险信息结合帮助开发人员和应用安全工程师大幅提效。

**在团队质量、产品技术以及 GTM 势能上，Endor Labs 都是明星级的表现，并且为应用安全提出了一套新的叙事和愿景。从投资视角来看，围绕着这家公司最大的问题在于它所处的市场，狭义的 SSCS 本身是个不到百亿美元的细分市场，并且已经相当拥挤。**因此本文试图讨论清楚 Endor Labs 的核心价值主张以及对它的投资回报可能性。

Endor Labs 的业务跟 Snyk 有很多相似之处，不了解这一市场的读者可以先阅读我们之前[**关于 Snyk**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247489343&idx=1&sn=a9d3ed29d23d5b108532603ded8c2a20&chksm=ce98a8a1f9ef21b79fea024177497db305111490ad50f5ca5d5121f9b801cc24a8e3f8a795e1&scene=21#wechat_redirect)的文章。

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 开源安全的新叙事

02 Endor Labs 的产品

03 开源安全的市场机遇与 TAM

04 竞争：最大对手是 Snyk

05 团队：前 Prisma Cloud 主力

06 未来

**01.**

**开源安全的新叙事**

Varun Badhwar 这样描述当前开发者所面对的“生产力税”问题：

（企业）给程序员的 KPI 永远是他们写了多少代码、推出了多少功能。在 KPI 之外，他们付了许多不必要的税，为了（在安全误报面前）证明自己的“无辜”，以及将一堆的安全工具部署在他们的开发管道当中。Snyk 的扫描往往会告诉你现在有成百上千个漏洞，开发者们需要花 8 个小时来排查。目前应用安全最大的“生产力税”是处理开源代码的风险，其次是在处理它们的过程中不得不面对的噪音。

Endor Labs 将传统 SCA（Software Composition Analysis，软件组成分析）围绕“漏洞”的开源安全叙事转变为围绕“可触达性”和“依赖关系”。这一叙事的完整逻辑很清晰：

大量的组织在今天已经不是在做“软件开发”，而是“软件组装” —— 没有程序员希望重复造轮子，因此他们会引入大量可复用的开源代码。根据 GitHub 的统计，平均单个组织内 90% 的代码量实际上都来自于开源包。按照 Varun 的说法，目前典型的企业拥有 4 万个以上的直接依赖项，平均每个还会带来 77 个间接依赖项，这引入了极大的复杂性。

更糟糕的是，没有人实际上为这些复杂性负责。虽然大型企业在第三方采购上有大量的合规流程，但是开发者实际上每一天都在使用陌生人做的开源项目的代码。没有企业专门设立围绕着排查和维护这些第三方依赖项的岗位。因此一旦发生 Log4j 这样严重的开源安全漏洞，大型组织往往要花费数千个小时排查问题。

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/005.png)

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/006.png)

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/007.png)

面对开源依赖项的这种无人维护的复杂性，传统 SCA 的叙事是围绕漏洞的，比如 Snyk Open Source 的壁垒之一是“史上最完备的商用代码漏洞数据库”。但 Endor Labs 认为漏洞只是众多风险的一个角度。

靠漏洞数据库，企业无法规避掉名字混淆攻击和 core-js 这样的开源风险 —— 前者意味着攻击者通过看起来相似但实际上非同一语种的字母诱骗开发者使用其伪造的库；后者是最流行的开源包之一，但依赖其发起者维护，而这位发起者威胁社区如果不对其进行捐助就将停止维护。

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/008.png)

单纯使用漏洞的视角不仅无法发现某些风险，与此同时它往往还有太多的误报（false positive）。组织内的开源依赖项是多层的，每一层内往往仅有部分 function 在应用内实际发挥作用。比如下图展示了应用的实际依赖关系 —— 虽然有许多直接依赖项，但应用实际只使用了 function 2，而 function 对于其间接依赖项也仅使用了 function 6。

传统的 SCA 扫描无法提供这些可见性和洞察，可能扫描结果会显示 function 5 有问题，而这实际上压根无法触达应用，也没有修复以及关注的必要。在使用 Endor Labs 之前，这是大多数组织内安全和开发团队面临的困境，他们缺少针对可触达性和依赖项的可见性和上下文，在“fix never”的东西上花费了太多时间，以至于耽误了需要“fix now”的风险或者严重阻碍开发流程的进展。

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/009.png)

基于这些大背景，Endor Labs 将静态分析的方法引入了开源安全中，将价值主张转移到可触达性和依赖关系，并且不再单纯以漏洞为中心来评估风险，而是引入开源包的流行度、改动历史、质量、安全性来做充分评估，从而在开发者引入开源依赖项的事前就可以为他们提供潜在风险的可见性。

举个直观的例子，Endor Labs 评估一个开源包的信息包括：项目背后有多少维护者？他们有多活跃？提交历史如何？项目背后的邮箱地址是否还有效？当前版本和分支的代码有没有经过 review、有没有做单元测试？在有问题被提交后，维护者进行修复和升级的速度有多快？提交的代码是否有编写习惯的明显改变？

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/010.png)

从客户访谈来看，Endor Labs 的这一套叙事的确切中了当前企业组织内的痛点，那些使用了 Snyk 的组织仍然觉得它的 SCA 给出的警报太多，使用比 Snyk 更陈旧的 SCA 工具的公司则更加苦不堪言。以美国一家商务差旅领域的独角兽为例，它的安全团队决策者非常认可 Endor 的价值主张：

传统的 SCA 只是将开发者使用的第三方库跟已经的漏洞数据库做对比，然后将已知漏洞标记出来。有时候一个有历史遗留问题的库可能会被标记出上万条风险，压根无法处理，而且还损害开发跟安全团队之间的关系。

上下文和可见性真的非常重要，我需要知道这些漏洞对我们的应用而言真的是严重或者高危的吗？我们调用 function 是否受到影响？我们的调用是否是面向外部的、是否经过了认证？我们目前在使用另一家 SCA，但会把预算完全转移到 Endor Labs。Endor Labs 的技术是将静态分析的逻辑应用到了 SCA，可以提供深度的、有上下文的 SCA。

**02.**

**Endor Labs 的产品**

Endor Labs 的产品思路和上述叙事以及广大安全从业者和投资人对下一代安全产品的期许相同：让安全产品及工具帮助客户提升生产力，而并非仅仅达到合规目的。Varun 自己对打造产品的原则总结是：“尽早发现风险，找到那些真正关键的依赖项，最优先保护它们，给客户足以升级和修复它们的洞察”。

Endor 自己将当前的产品划分为 3 类：

**端到端的开源安全治理**

使用过 Snyk 的开发者会将它的体验描述为“无打扰”的。这些开发者无须改变自己的工作习惯，只需要在有风险被扫描出来的情况下去查看是否需要修复它们即可。而 Endor Labs 自脱离匿名状态以来，推出的第一个产品是“依赖项生命周期管理平台”，希望让开发者在挑选开源包的过程中就开始考虑风险因素，通过 Endor Labs 产品中给出的安全、质量和流行度等指标来决定是否选择一个包。这是评估的最佳时点，因为开发者还没有开始编码和引入依赖项，但是这也需要开发者主动地改变自己的行为模式。

上述这一具体的产品使用体验上的分野代表着 Endor Labs 对于“端到端” 的定义。经过过去十几个月的发展，它在开源安全的事前、事中、事后都有完整的功能帮助开发者和安全团队提效：

• 对于开源生态中每个包的各个版本，Endor Labs 都基于其安全性、质量、流行度、活跃情况给予一个安全评分，帮助开发者和安全团队事先评估和选择开源依赖项；

• 对于已经“组装”好的代码，Endor Labs 提供基于可触达性的 SCA，使用静态分析的方法，无需运行时代理就可以确定开源依赖项对于应用的实际影响，能够将误报率降低 80%；

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/011.png)

• 让客户在 CI 管道内能够设置定制化的规则以限制开源依赖项的引入和使用；

• 美国政府在 2022 年开始要求软件供应商通过提供 SBOM（Software Bill of Materials，软件材料清单，记录了软件构建过程中使用的所有组件、库和依赖项）为其产品自证安全，Endor Labs 提供了 SBOM Hub 产品来帮助客户创建、存储和分析其 SBOM，并且提供 VEX（Vulnerability Exploitability eXchange，漏洞可利用性交流）。

**Endor Labs 的这套开源安全治理产品是否有足够高的进入门槛？**

是的，非常高，Endor Labs 团队汇聚了全球范围内最强的一批 SCA 以及可触达性领域的 PhD 和科学家来构建这套方案。

具象来看，这套产品有以下门槛：

• 最大的难度在于开源世界中有太多的包和不同的版本，Endor Labs 需要做实时的跟踪和可触达性的分析。在 Endor Labs 之前，其他供应商的分析大多停留在 Metadata 层面，而且能覆盖的包数量也很有限，JFrog 自己推出的官方认证受信任的 Artifact 数量也只覆盖了数百个包。如上文介绍过的，Endor Labs 在分析一个包时所使用的信息远超过 Metadata 本身；

• 除了包的覆盖之外，还需要覆盖多种语言，如下图所示，Endor Labs 目前已经支持了各种主流语言。Snyk Open Source 推出过类似 Endor Labs 的依赖项分析，但是在相当长一段时间内仅支持 1-2 种语言。甚至连 Endor Labs 自己目前也还不支持一些主流的动态语言，比如 JavaScript 目前并没有原生支持，也侧面证明了这个领域本身在研究层面也是非常前沿的；

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/012.png)

• 使用静态分析而非运行时代理本身也是创新性的做法。安装代理需要耗费大量的时间和资源，因此无代理本身是一个巨大的趋势。具体到开源安全的场景上，Endor Labs 需要对上述语言都做到事前/静态编译才能实现对运行时代理的取代，需要很深的 Know-How 和前沿研究。目前我们观察到的 Endor Labs 分析还聚焦在 Control Flow，而不是 Data Flow，同样表明这个领域的前沿性。

**为什么 Snyk 或者其他传统 SCA 不能加大投入追赶 Endor Labs？**

有多个层面的原因，最重要的是 Endor Labs 团队有明确的愿景 —— 这家公司目前给人的感觉跟早期的 Datadog 非常像。当其他的可观测性玩家们还主要致力于满足客户的合规诉求时，Datadog 非常富有前瞻性地向下深挖了一步，跟 k8s 和 node.js 进行了深度的结合，从而成为了可观测性赛道中的领先者。这一点可以解释为什么大多数传统的 SCA 供应商没有布局进入 Endor Labs 的产品。

具体到 Endor Labs 和 Snyk 的竞争上，已经是 Snyk 的客户认为 Snyk Open Source 和 SCA 的误报率在下降，但是也有客户认为 Snyk 需要配备更大体量的团队使用，因为需要有专人为 Snyk 的警报进行分类和寻找上下文，因此他们转向 Endor Labs。

从我们的调研来看，有多个层面的原因让 Snyk 暂时还不会将经营的核心转向与 Endor Labs 的竞争上：

• 虽然 Snyk Open Source 是 Snyk 的第一个产品，但是它目前最核心的产品可能已经变成 Snyk Code，而 Endor Labs 短期还不会对它造成威胁，甚至在某些层面落后于 Snyk，比如 Snyk 对于 Data Flow 的分析及风险扫描有更深的积累；

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/013.png)

*Snyk Code 的技术架构*

• 在收入层面，Snyk 已经拥有 2-3 亿美元的 ARR，并且没有显著的降速，Endor Labs 还未变成同一体量的对手；

• Snyk 本身目前成为了一家缺少创始人控制的公司，可能在下一代架构和愿景的投入上面更加保守，它目前的重点是延伸至云安全。它的几位联合创始人甚至是一些新兴的开源安全公司的天使投资人，比如其前 CTO Adi Sharabani 投资了以色列的开源安全公司 Oligo。

此外 Endor Labs 所进行的研究很前沿而且高门槛，但是 TAM 短期内可能有限（在下一章进行分析），因此 Endor 的 CEO 向 Techcrunch 表示的“Snyk 是最大的竞争对手之一，但 Endor 并没有直接竞争对手”在目前来看是准确的表达。

**Endor Labs 争夺的是客户的哪部分预算？**

SCA，通常是更传统的 SCA 或者 Snyk Open Source。取代后者的情况下，客户往往在同时使用 Snyk 的 3-4 个模块的产品。存在相当多的情况是成长期的客户仍然同时使用 Snyk 和 Endor Labs，他们希望有多重的风险提示来确保万无一失。

Endor Labs 自身的定价和 Snyk 的思路类似但略有不同，按照提供的模块以及扫描的 Git 仓库数量定价。一个 1000 名员工的新经济公司一般能贡献 10 万美元左右的 ACV。

**CI/CD 治理**

这一产品主要为客户提供代码管道的可见性以及对 Secrets 等权限的控制，目前还不是 Endor Labs 的亮点，客户普遍反馈 Snyk 在跟代码库和不同环境的自动化集成上面做得更好。

从 Endor Labs 的客户视角来看，它在跟 GitHub 和 Jira 的集成上做得不错，特别是跟 GitHub Advanced Security 的集成：

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/014.png)

**DroidGPT**

DroidGPT 结合了 Endor Labs 背后的风险及代码库数据与 ChatGPT 的理解与推理能力，通过提供一个对话式的界面帮助客户快速地研究开源包。

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/015.png)

整体而言，这一产品在 GenAI 本身的技术层面没有太多领先的地方，但是证明了 Endor Labs 团队在 GenAI 结合、转 Chat Interface 和进行市场营销等方面的敏感度。我们在客户访谈中观察到大量的客户已经将 Endor Labs 定义为“在 AI 上领先的供应商”，一些大型金融客户愿意将它纳入 POC 列表的原因往往是“它的 SBOM 功能领先并且还有 GenAI 的功能”。

**03****.**

**开源安全的市场机遇与 TAM**

**开源安全处在多个安全趋势下**

Endor Labs 处在一个被大肆炒作的市场，和多个主题相关：

**• AppSec：**

即应用安全。这一市场在过去 5 年逐渐兴起，和云安全是唯二过去 3 年 CAGR 突破 20% 的安全细分市场。它通常被视作一个 70-80 亿美元 TAM 的市场，被 Web 应用防火墙、应用安全测试（Endor Labs 所在的赛道）和漏洞管理三个子方向各自占据约 1/3 的 TAM。

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/016.png)

*Source - Gartner & Cybersecurity Market Perspective*

**• DevSecOps：**

在 DevOps 崛起后，行业开始鼓励安全专家也开始深度介入和参与开发及运营团队的工作流之中，这代表了终端用户行为和心智的改变趋势。Endor Labs 在整个产品的实际使用工作流上和 Snyk 有许多不同之处，目的就是为了推动安全与开发团队拥有更和谐的关系。不过这种做法并不是完美的，很可能会为其 GTM 带来一定挑战，因为 DevSecOps 转型存在很多阻力，许多工程师和安全人员并不享受彼此的协作。本文下一章会详细地讨论这一点。

**• Shift-Left Security：**

这是 DevSecOps 实践的组成部分，即在开发早期就发现漏洞并修复它们。经历了过去 5 年的发展，目前的 Shift-Left 市场非常分散，采用这种实践的团队往往面对十几种产品给出的数不清的安全警报，因此 Endor Labs 这种提供上下文和可触达性分析以减轻客户压力的产品代表了最近的创新趋势。

**• SSCS：**

即软件供应链安全，在源代码的管理、编译、部署、打包及最终分发安装的过程中确保安全。20 年底的 SolarWinds 漏洞事件让 SSCS 成为一个所有 CISO 都在讨论的概念，21 年底的 Log4j 漏洞又进一步加深了这一趋势。

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/017.png)

*Source - Anatomy of a supply chain software attack by Snyk*

Dell Technology Ventures 的 Tyler Jewell（也是一位 Endor Labs 投资者）在他的 Newsletter Tyler's Musings 对 SSCS 整个市场的各个环节做了详尽的测算 —— 整个 SSCS 市场目前拥有超 20 亿美元 ARR，60% 以上由未上市公司贡献，Endor Labs 目前所处的 External Supply Chain 赛道拥有接近 4.5 亿美元的 ARR。

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/018.png)

从上面的分析中可以看出，在不进行大幅度平台拓展的情况下，Endor Labs 目前的产品处在 25 亿美元左右的 TAM 内。

如果它最终进行了成功的平台拓展，计算它 TAM 的方法将和 Snyk 类似：

• 只考虑 AppSec 的最终渗透，它可以服务全球的 2800 万开发者，按照 600 美元每年每坐席的定价，对应 168 亿美元的 TAM；

• 如果成功切入了云安全，它将和 Snyk 一样成为 Palo Alto Prisma Cloud、Wiz 等玩家的竞争对手，角逐独立安全供应商可能拿到的 250-375 亿美元 TAM。

**短期以科技及新经济客户群为主**

在我们看待安全行业的框架中，公司可以被简单粗暴地划分为两类：

• 在红海市场中竞争，它们提供的产品和服务需要时间才能被认可并逐渐替换掉原有的供应商。典型的市场是端点安全和网络安全（Network Security），像 Netskope 这样的公司获取客户并替换其原来的供应商很难，但是 TAM 大且确定性强，一旦被客户认可就能维持住 NDR、Net New ARR 和增速；

• 在新兴市场中竞争，它们可以通过创意性的方式快速地获取大量客户（比如 Snyk 通过它的 PLG 方式），但是静态的 TAM 小，依赖这些供应商自己对愿景和下一代架构的定义来推动整个市场的增长，并且鉴于引入新工具可以很迅速，客户替换它们也可以很迅速。

在安全行业内，前者最典型的例子是 Netskope 和 SentinelOne，分别处于各自都长到了数十亿美元体量。它们需要担心的问题不是扩大自己所处的市场，而是证明自己可以替代客户已有的供应商并提供更好的 ROI。

**Endor Labs 所处的市场是后者，它的目标客户需要满足两个最基本的条件：上云以及在软件开发过程中愿意并敢于使用开源。**

目前满足这两者的企业主要是科技行业以及创新创业的新经济客群。企业采纳开源都是发生在其基础设施云化之后的。根据客户访谈来看，像 JP Morgan 这样云旅程还在进行中的客户，Endor Labs 这样的产品很难提供跟跨环境的多个库的集成。因此即使对它进行了 POC，这些传统客户对于实际使用它仍然有顾虑。

这意味着传统的制造、零售、金融服务、医疗等行业客户对于 Endor Labs 来说将是长尾的，它的 SOM 客户群量级可以参考 Snyk 和 GitLab，前者截止 2023 年 4 月拥有超 2500 家付费客户，后者截止 2023 年第二季度拥有接近 8000 个年付费 5000 美元以上的客户和 810 个年付费 10 万美元以上的客户。Endor Labs 目前的代表性客户 Logo 包括 Snowflake、Rubrik、Mile IQ、Five9、Skyflow、Cowbell、Navan、Netskope、Zoom、Uber 和 Attlassian 等。

**Shift-Left 公司的平台延伸难度很大**

如果希望将单个客户榨取的价值最大化，Endor Labs 需要有更强的平台延伸。Snyk 事实上已经走了这条路，除了维护代码安全、开源安全之外，它还做了容器扫描、SAST、IaC 以及 Wiz 所处的 CSPM 等延伸。

从客户反馈的角度看，Shift-Left 环节还远未成熟，企业普遍倾向于购买多个独立最佳的供应商，而不是一家供应商捆绑销售的其他产品。不同于网络安全或者端点安全只能选一家供应商的逻辑，目前科技公司在推动 DevSecOps 的过程中非常能接受“overlay”，即购买多个产品然后将它们叠加在一起使用，因此其中的单个产品很难获得超越其他竞品的中枢性位置。

**ARR 测算**

综合上面的判断，Endor Labs 所处的赛道对创始人非常友好，但是可能会让投资人难以判断终局：我能看到它通往 1 亿美元 ARR 的清晰路径，但是由于上述问题，很难想象它目前的产品如何通向 10 亿或者 100 亿美元的 ARR。

1 亿美元 ARR 可以这样拆解：

• 从云上的工作负载保护的 ROI 角度看，目前云上的容器和虚拟机数量为 1.5 亿（本地的机器资源为 3.4 亿），Qualys 拥有超过 1 亿个代理，Endor Labs 只需要为每个工作负载新增或替换 1 美元的保护成本就能做到 1-2 亿美元 ARR；

• 从 ACV 和客户数量的角度看，按照平均 ACV 为 10 万美元来计算，Endor Labs 需要 1000 个客户来达到 1 亿美元 ARR，有充足的空间可实现；

• 从单个开发者所需要付出的成本来看，按照比 Snyk 略低的 500 美元每年的定价来计算，Endor Labs 需要 20-30 万开发者，即渗透全球开发者的 1% 左右，也不是一个困难的目标。

如果按照 5 亿美元的估值进入并预期一个 3x 的回报，在 10x EV/ARR 的情况下，Endor Labs 需要做到 1.5 亿美元的 ARR，达到接近目前 Snyk 一半的体量。它需要做到的是：

• 维持住自己目前在开源安全中 Best-of-Breed 第一梯队的位置；

• 一定程度上突破科技客户群体，在 GTM 上达到今天 Snyk 的水平，能够卖给一部分较先进的传统行业客户。鉴于其 CEO 在 Prsima Cloud 在 3 年内将 77% 的财富 100 企业转化为了客户，他有经验做到这一点。

**04.**

**竞争：**

**最大对手是 Snyk**

Endor Labs 有以下竞争对手，按照竞争的直接和预期激烈程度由低到高排序：

**• 传统 SCA（被取代）**

这部分对手目前所服务的市场很容易被 Endor Labs 夺取，但是 GTM 搭配一定程度的市场教育内容，目前看 Endor 走在正确的路径上。

**• GitHub 及 GitLab 等代码托管平台（竞合关系，短期无直接竞争）**

目前它们将 SCA 这部分的安全功能作为高级版方案的免费捆绑部分提供给客户，客户往往会选择再购买一个更全面的 SCA 或者开源安全产品搭配使用，格局和用户习惯比较稳定。

GitHub 虽然购买了 Dependabot，但是过去几年其最核心的业务目标仍然是用户的活跃、每个库的活跃，而非提供原生的安全性。与前文分析 Snyk 与 Endor Labs 的竞争局势类似，GitHub 大幅度投入 Endor Labs 这样的前沿开源安全研究是个吃力不讨好的事情，需要兼顾平台本身的进展，又得平衡跟生态内安全合作伙伴的关系，短期内不太可能在这方面跟 Endor Labs 直接竞争。

**• JFrog 及 Sonatype 等 DevOps 平台（竞合关系，短期无直接竞争）**

它们和 GitHub/GitLab 的情况类似。JFrog 虽然做了 XRay，但是整体的客户体验上跟传统的 SCA 更接近，客户往往需要再搭配一个全面的 SCA 或开源安全产品使用。

**• 独立的新兴创业公司，如 Oligo 和 Chainguard 等（竞争，短期可能共存）**

这些创业公司本身和 Endor Labs 所要保护的企业资产类似，但是切入角度不同，比如 Oligo 更强调数据科学和数据挖掘驱动的开源安全，但通过运行时代理来提供解决方案，而 Chainguard 整体更古典，强调对容器和 k8s 的深入理解。鉴于目前的开源安全客户群还在完善其购买的产品列表，这些产品很可能跟 Endor Labs 及 Snyk 是共存状态，客户购买多种产品以获得多重的保护。

其中 Oligo 是以色列公司，同样由 LSVP 投资，并且获得 Snyk 前 CTO 在内的许多美国及以色列安全行业领袖的天使投资。而 Chainguard 是红杉和 Spark Capital 等头部基金支持的公司，刚刚完成一轮 6100 万美元的融资，获得了前 Wiz CMO Ryan Carlson 的加盟。

**• Snyk（竞争，短期可能共存）**

Snyk 目前仍然是应用安全和开源安全的代名词，我们在上文已经分析过了二者的竞争局势和可能走向。

**05.**

**团队：**

**前 Prisma Cloud 主力**

团队仍然是 Endor Labs 最大的亮点之一：

**• CEO Varun Badhwar：**

他在 2018 年 8 月将自己创立的 RedLock 以 1.73 亿美元出售给 Palo Alto Networks，正式开启了 Palo Alto Networks 在云安全领域的布局。在 Prisma Cloud 的 3 年里，他将业务增长到 3 亿美元 ARR，获得了 2700 名客户，包含了财富 100 中的 77%。这一增长速度是企业级 SaaS 中最快的之一。

**• CTO Dimitri Stiliadis：**

他在 2019 年 11 月将自己作为 CTO 创立的微隔离公司 Aporeto 以 1.5 亿美元出售给 Palo Alto Networks，随后担任 Prisma Cloud 的 CTO。

Varun 过去的经历像是安全行业的“吕布”，非常骁勇善战，在发现新兴趋势、建立领先的产品、通过 GTM 扩大销售以及最终退出上都有很好的经验。

他在 Salesforce 1500 人时加入，是安全团队的第五号员工。随后他在 2006 年观察到了 SaaS 兴起的趋势，作为联合创始人创立了 CASB 领域的 CipherCloud，该公司随后被 Lookout 并购。在 2015 年观察到全面云转型的趋势后，他创立了 RedLock 进军 CSPM，并最终出售给 Palo Alto Networks。在 Palo Alto Networks，他经历了 Solarwind  事件并亲身体会了当时董事会和管理层的慌乱，因此创业开始尝试解决 SSCS 和开源安全的难题。

**06.**

**未来**

本文上述分析的大体结论是：Endor Labs 拥有非常好的团队和产品，我们也有理由相信它未来的 GTM 势能，唯一的问题在于 SSCS 和开源市场本身较为细分，并且非常分散。基于这一结论，我们目前可以大致推演下 Endor Labs 最终的结局：

**• Bull Case：打透开源安全，拥有应用安全方面的全面布局，并且在云安全领域找到差异化的优势。**

这一点依赖于 Endor Labs 的管理团队迅速巩固和扩大当前在开源安全的技术架构和产品上的领先优势。鉴于他们在 Prisma Cloud 打造全面解决方案的经验，他们可以选择并购或者快速找到优质人才自建的方式进入 IaC、容器以及 SAST 等应用安全的其他领域。同时，Varun 过去在 CSPM、CASB 方面的经验可能帮助他找到当前已经格局稳定的云安全行业中的一些遗留空隙从而提供差异化的产品，比如可能的方向是 API 安全。

这些延伸非常难有机地发生，完全依赖于管理团队充分利用他们之前的经验和人脉。但是如果能做到这些延伸，Endor Labs 就从一个 4 亿美元市场的领域拓展到了数百亿美元 TAM 的广阔市场，完全可以成为一个做到数十亿美元 ARR 的独立安全巨头。

**• Base Case：在开源安全单点做到极致，整体接近或超过当前 Snyk 的状态。**

Snyk 打了一个很好的模板，如果 Endor Labs 在开源安全上能做到 Snyk Code 这种统治级的状态，它完全可以复制 Snyk 的策略，哪怕在延伸领域的产品不是完美的，也仍然可以获得一定的 ARR 补充，并且通过 GTM 销售到科技行业以外的客户群，达到 2-3 亿美元的 ARR，并且有做到 5 亿美元级别的可能性，不论是独立发展还是卖给微软、Google 等巨头都有一定的可能性。甚至不能排除它和 Snyk 做互相的 M&A 的可能性。

**• Bear case：架构和产品成为 commodity，应用安全合并潮提前到来。**

尽管不太可能，但是 Endor Labs 领先的技术架构背后的 Know-How 和积累有可能随着人才流动逐渐扩散到其他公司，这会极大程度地削弱 Endor Labs 的价值主张以及独立存在的价值。它最大的可能是被 Palo Alto Networks 或者 Snyk 这样的安全玩家以一个较低的价格收购。

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/019.png)

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/020.png)

延伸阅读

[![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/021.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505241&idx=1&sn=a4494cb520106b02aa183fa663f88bbf&chksm=ce9b6ac7f9ece3d1c691379df492f533234e68d5883e00a56cdedffe0d94c6becca64b5851e1&scene=21#wechat_redirect)

Hex：数据行业会出现“Figma” 的机会吗 ?

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/022.png)

[![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/023.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505204&idx=1&sn=eaf9d179c6a41cd0dac7b88e201573e8&chksm=ce9b6aaaf9ece3bcae1bb525bc53a23e2781dd048022cc5a3e4411e499540f1adc17f9af11ad&scene=21#wechat_redirect)

Inceptive：指令药物时代的 AGI 编辑器

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/024.png)

[![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/025.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505125&idx=1&sn=706c0b4f57dbbfe90fdd7309a42942dd&chksm=ce9b6b7bf9ece26d4a36dc4b65d772f5c8b46007a462d27b504b3ad818b5653d7ec7ad466e53&scene=21#wechat_redirect)

Character AI：如何把LLM变成人类想象力引擎？

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/026.png)

[![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/027.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505021&idx=1&sn=d38be45e65b35b228539e22b3dfceca6&chksm=ce9b6be3f9ece2f562f54e18d6a74edf17c99a4ee91287f53d4bc453f6fcb1d9df293b704550&scene=21#wechat_redirect)

Nile：前Cisco掌门人创立，用AIOps重构千亿企业网络

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/028.png)

[![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/029.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504973&idx=1&sn=603596db2a31e1e53d71ac05d775cb7c&chksm=ce9b6bd3f9ece2c577720045239314840757fa578587f4a5adbf21e18a9dadd6bf1af3913b61&scene=21#wechat_redirect)

AI Agent的千亿美金问题：如何重构10亿知识工作职业，掀起软件生产革命？

![](../images/2023-11-02-endor-labs-bi-snykgeng-jin-yi-bu-de-kai-yuan-an-quan-wei-shi/030.png)
