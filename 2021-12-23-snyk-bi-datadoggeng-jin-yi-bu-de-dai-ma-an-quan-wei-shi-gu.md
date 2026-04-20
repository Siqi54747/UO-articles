---
title: Snyk：比Datadog更进一步的代码安全卫士，估值85亿美金
publish_date: '2021-12-23'
publish_timestamp: 1640262565
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/2J8hg5QSe1GiaM_seWmSWQ
msgid: 1000000052
appmsgid: 2247489343
itemidx: 1
digest: 云原生意味着开发者需要管理自己的云基础设施，并武装上正确的安全工具。
cover: https://mmbiz.qlogo.cn/mmbiz_jpg/3tHNibnJ2jgxQ8T6YsBoZEmd12bYdFIbI5licxpLVOKb7Z2Q25KL1al1oVs7nnwgwrhibR6hpmsmlS4ONJbL2Vbog/0?wx_fmt=jpeg
image_count: 39
archived_at: '2026-04-19T23:14:33+08:00'
---

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/001.gif)

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/002.png)

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/003.png)

**作者：东方明**

**编辑：penny , 穆奕**

**排版：雨欣**

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/004.png)

Snyk 是 Dev-first Security （开发者优先的安全应用）的开创者和布道者，创造了第一个真正面向开发者的应用安全工具，**凭借史上最完备的商用代码漏洞数据库，和快于其他代码分析技术 10～50 倍的扫描速度，**真正赋能了开发者对安全问题的实时监测和自我反馈。

**在 Snyk 出现之前，代码安全问题由安全团队负****责，编写代码和维护代码、安全测试、事故解决的链条是严重割裂的。而随着现代开发需求的数量、速度、复杂程度的陡升，科技企业意识到不能再后验地进行“安全审计”，而要把安全问题的主导权交给开发者，**打赢大代码时代的科技战。

Snyk 以对代码漏洞的理解深度著称，其独特的“安全智能”工具帮助开发者们持续监测可能发生的漏洞，并不断自动化安全性能升级。Snyk 帮助开发者们**在开发生命周期中一以贯之地查找、修复和监测代码的脆弱性，让开发者更好地应对纷繁复杂的微服务、API，以及日益增长的复杂性。**

Snyk 在开发者圈饱受好评，也收获了许多重要客户，包括 Google, Salesforce, Revolut, MongoDB 等，目前已经被两百多万开发者使用，拥有1200多家科技公司客户。

公司于今年 9 月初获得了 Tiger, BlackRock, Temasek 以及 Accel 的 F 轮，不到一个月内，Salesforce 和 Atlassian 又追加了 7500 万美金，**F 轮总融资金额超过 6 亿美金，公司估值达到了 85 亿美金。**

从开源安全起家，慢慢拓展到云原生应用安全的方方面面， Snyk 对容器化、基础设施即代码等新趋势的布局相当迅速。同时 Snyk 还在稳固大本营的路上，今年连续收购了 FossID, CloudSkiff 两家开创性的开源安全公司。我们既期待 Snyk 在所擅长领域的纵深，又对其不断拓宽云原生应用安全的边界充满想象。

**以下为本文目录，**

**建议结合要点进行针对性阅读。**

**👇**

01. 背景：开发复杂性陡升和开发者崛起

- 网络安全“新元年”下的大变迁
- 开发者及其生产工具的崛起

02. 创始心路：以开发者优先为北极星

03. 产品发展：向云原生应用安全出发

- 强大的漏洞库和 Peace-of-mind 的自动修复
- 收购 DeepCode：AI-driven 更快更精确的 SAST 方案
- 容器化和基础设施代码化大趋势

04. 客户与竞争格局

05. 未来的三个命题

**01.**

**背景：开发复杂性陡升和开发者崛起**

Snyk 是 2015 年诞生的，5 年内，Snyk 在开发者安全领域掀起了一场 Shift Left Movement，shift left 意思是把测试时间提前，**在这里意味着开发阶段就引入安全检查工作，确保代码库从一开始就以安全为目标进行设计，而不是流程结束时再检查安全问题。**

也就是说，Snyk 认为，代码安全问题的主导权应该向链条上游移动，并无缝整合进开发者的工作流当中，而这必然需要一定程度的自动化。那么 Snyk 能引领这场运动的大背景是什么？

**网络安全“新元年”下的大变迁**

2020 年是网络安全投资创纪录的一年，全球的投资额超过 78 亿美元，2021 年的投资记录甚至更高。近两年网络安全领域的独角兽将近 20 家，也是创记录的成绩。

2020 年 4 月，联邦调查局网络部门报告称，由于黑客利用远程工作的漏洞，每天的网络安全投诉增加了四倍。网络漏洞的成本相当高昂，无论是从解决问题的成本方面，还是从信任缺失后失去客户的潜在成本方面。因此，科技公司对于网络安全工具的支付意愿因此也是很强的。

根据 Gartner 的报告，到 2024 年，信息安全和风险管理市场的终端用户支出预计将达到 2077 亿美元。微软今年 9 月宣布，将在未来五年内将其网络安全上的投资翻四倍，达到 200 亿美元。

**为什么市场这么火？**

Northzone 的 VC 投资人 Wendy Xiao Schadeck 在‘The Future Belongs to Devs’一文中很好地概括了当下软件开发格局的几大重要变迁，其中很重要的两点是：

- **为了解耦代码构建过程，降低开发门槛，单体应用程序被分解为了成百个微服务。这能够增加敏捷性、降成本、提高效率，但也大大增加了 DevOps 的复杂性，以及新软件和数据馈送出入口数量。进而增加安全风险。** Kong 在去年的一次调研显示，84% 的大中型组织已经采用了微服务，且平均每个组织部署了 180 多个微服务。而安全性问题是使用微服务过程中的最大挑战。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/005.png)

- 随着 API 的激增（一定程度上也是由于微服务和 GraphQL 的流行），有越来越多的构建单元供开发人员构建。在 API 集成的几大挑战中，安全问题也在前列。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/006.png)

在这样的背景下，Snyk 所做的，就是帮助开发者们**在开发生命周期中一以贯之地查找、修复和监测代码的脆弱性，让开发者们更好应对纷繁复杂的微服务、API，以及日益增长的复杂性。**

什么是脆弱性？就是在软件和硬件组件中发现的计算逻辑（例如代码）中的弱点，一旦被利用，会对机密性、完整性或可用性产生负面影响。在这种情况下，漏洞的缓解通常涉及编码更改，但也可能包括规范更改甚至规范弃用（例如，完全删除受影响的协议或功能）。

比如，JavaScript 的漏洞会使项目容易受到 Cross Site Scripting、Cross Site Request Forgery 等不同形式的攻击。**由于开源 JavaScript 项目近年来呈指数级增长，并且它们直接或间接地依赖于一些广为使用的函式库（如 lodash），导致 npm（全世界最大的 software registry）的漏洞单单在 2018 年一年就增长了 47%。**

近日，被全球广泛应用的组件 Apache Log4j 被曝出一个已存在在野利用的高危漏洞，攻击者仅需一段代码就可远程控制受害者服务器。这一漏洞堪比“永恒之蓝” ，已发现近万次攻击。

**用一句话概括，现代软件开发的复杂性带来脆弱性，脆弱性中 Snyk 应运而生。**

**开发者及其生产工具的崛起**

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/007.png)

曾经，科技巨头会给开发者们提供自研的生产工具，将其作为一种公共物品补贴给他们，甚至开发给其他中小科技公司免费使用，比如微软的 Visual Studio Code。因此，开发者社群流通着很多免费工具，但产品体验都很一般，更没有向外界采购更优产品的自主权。风投之所以不愿投资开发者体验 (DX) 领域，就是因为后发的这些开发者工具提供商很难跟巨头的免费产品正面肉搏。

**但开发者的地位今非昔比了，目前开发者群体的数量达到 2700万人，比澳大利亚的人口还多，增长速度快于巴西的人口，并有望超过加拿大的人口。**他们支撑着现代最重要的科技变迁，区块链技术、云原生、甚至低代码、无代码和创作者经济，开发者们的作用是支柱性的。

**于是，围绕开发者为中心诞生了一批最有价值的科技公司**：包括 Atlassian、MongoDB、Splunk、Datadog、Elastic、HashiCorp、和 Twilio 等上市公司，以及 Stripe、Auth0、Snyk 和 Unity 等独角兽公司，**都通过直接为开发人员构建（build with developers in mind）大获成功。**

效率工具越来越多的同时，开发团队构建新功能、触达消费者并不断进行适应性调整的能力和速度，也在经受考验。

**一方面，随着企业基础设施转向云，流程转向 DevOps，代码的部署速度以及系统性能指标都成为开发者的职责。**Datadog 就是通过帮助开发团队直接监控整个堆栈的性能而成为独角兽的，上市后已达到 560 亿美金市值。Snyk 则是帮助开发人员在软件开发生命周期（SDLC）中构建开源代码安全性，让其客户从根本上解决问题，而不是依赖单独的流程来查找和修复它们。

未来还会有更多业务指标可以直接集成到开发工作流程中，例如身份验证和隐私（Magic.Link、Evervault、Metomic）和云优化（Northflank、Env0、Cloudskiff）。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/008.png)

**另一方面，随着技术进一步从成本中心转向利润中心，开发者们作为天然的 power users，可以无限优化生产力。**David Ulevich 曾在一次 a16z 的演讲中高度概括了开发人员的典型工作方式，这些工作方式在带来生产力的同时也随之带来了一些安全隐患：

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/009.png)

这里我们可以就其中“Don't Repeat yourself”举一个很好理解的例子：

为了不重复耗力，开发者们往往去 git repository 和类似的代码库上找一些现成的包（微软 CEO 在一次 Node 峰会上说过，常常会发现一个包裹中只有2%的代码是开发者自己写的，其他都是第三方代码）。

**就像建设大楼不需要从钢筋水泥开始铸起，而是可以采购已有的材料，这种上下游的依赖关系在软件行业被称为“dependencies / 依赖项”。**依赖项可以是企业维护的，也可以是个人维护的（比如 gRPC 是谷歌维护的，JavaScript 上很多都是个人开发者在维护）。**之所以花这么多精力维护，是因为78% 的代码脆弱性问题就来源于这一个个依赖项。这也是为什么开源安全问题被放在开发者安全的首要位置上。**

现有对于这些依赖项的不确定性采取的缓解方案是什么样的呢？就是开发者们必须谨慎科学地记录日志以便日后锁定出错点，部署后一旦出现安全问题，得靠安全团队找到出错点再扔回给开发者修改，这里的跨团队沟通和反复是非常耗时的。更不用说，目前的安全工具都是为了安全团队而非开发团队而设计的，对开发者极其不友好。

Snyk 从建立伊始，就致力于将开源代码诊断和修复完全自动化，减少团队间反复的沟通摩擦，为开发者提供快捷、完备、Peace-of-mind 的安全解决方案。

**02.**

**创始心路：**

**以开发者优先为北极星**

Snyk 创始人 Guy Podjarny 曾是 Blaze.io 的联合创始人，2012 年将其出售给了Akamai（一家内容传递网络和云服务提供商，世界上最大的分散式计算平台之一，承担了全球 15%~30% 的网络流量）。

收购后，他成为 Akamai 网络体验业务的 CTO，直到 2015 年建立了 Snyk。联创 Peter 有 20 多年安全领域的从业经验，和创始人 Guy 是从 Watchfire （一家网络应用漏洞评估和合规方案提供商，后来被 IBM 收购）就认识的 16 年老友。

BoldStart Ventures 的创始人 Ed Sim 在投资了 Guy 的第一个创业项目并成功退出后，也是 buy in 了代码安全的市场，从最开始就是 Snyk 的忠实投资人。**回看当初 A 轮投资 memo 的剪影，对比如今 Snyk 的估值，已经超越了其中任何一个市场规模的预期。**

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/010.png)

**Snyk 几乎是创造了“开发者优先安全工具”（dev-first security）这个市场**，最初也受到了很多质疑。唱衰者们提出了开发者对安全问题的漠不关心、开发团队和安全团队之间的激励和信任问题等等。

但是，'It takes time to build a movement'，和任何消费者需求一样，想建立起消费心智必须进行市场教育，早期Snyk也是花了大量的精力将开发者友好的安全工具的必要性根植进潜在用户的大脑里。

现如今的大代码时代，随着部署代码的数量、速度和复杂性的陡升，科技企业们都认识到把代码安全的探察点移到整个周期前端，将自主权交给开发者的重要性，并自觉加入了这场 Shift Left Movement. 正如 Guy 在这里说的：

**“整个云原生运动意味着，开发者需要管理他们自己的云基础设施，并且需要被武装上正确的安全工具。两百多万使用 Snyk 的开发者们，日益增长的 DevSecOps 运动，以及越来越多的嵌入开发平台的安全功能模块，都是这一论断的最好证明。”**

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/011.png)

Snyk 这家公司把“开发者优先”刻在了自己的 DNA 里，始终将开发者的体验摆在第一位，创始人将其称作是“Product North Star”。**SNYK 这一缩写，其实想表达的是“So Now You Know a lot more about your applications”，是创始人的美好期许。**

在最初制定产品方案的时候，董事会上有过究竟是追求广还是追求精的争论。Snyk 的竞争者 Sourceclear 选择了前者，在产品推出之初就支持 8 种计算机语言的整合，但在每种语言的语法范式上都认识粗浅，也没有真正整合进开发者们的工作流当中，导致反响平平、出现了很多 fire sales（2018 年 Sourceclear 被 CA Technologies 收购，具体数额虽未披露但内部人士表示收购价格并不高）。

**相反，Snyk 在最初只支持一种语言JavaScript，但是做得很深入，不仅帮开发者找出漏洞，还提出建设性的修补意见，从而赢得了开发者的喜爱。**

Snyk 在公司早期没有一味地追求“支持多种语言”来讨好客户，但却在一个方面不断沉潜，在开发者社区中获得了很高的评价。这种“82 原则“为 Snyk 打下了很好的产品基础。Snyk 很在乎开发者社群的建设，他们有自己的Snyk社区私域，买下了 DevSec Conference 进行知识传播，还会做一些开发者调研进行聆听来启发功能拓展的方向等等。这种基于群众的产品营销策略是现在 SaaS 界奉行的产品驱动增长（PLG）的灵魂所在。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/012.png)

**在 2020 年的五周年回顾上，当创始人 Guy 提起 Snyk 做对的五件事时，其中一个就是“Don't go enterprise too early”：当社群建构起来，越来越多的企业自然会主动寻求合作，到时再根据企业的需求提供本地化服务，或者支持多种语言（目前 Snyk 已做到 11 种语言的整合），也为时不晚。**

Snyk 较早时期某个企业客户，ARR 在两年间从 4 万美元扩张到了7位数。联创兼 CEO Peter Mckay 也在一次采访中透露，目前 Snyk 60-70%的客户是 inbound 的，复购率达到了 95%。

有趣的是，公司的两位创始人 Peter 和 Guy 分别来自美国和以色列，是去年网络安全领域的头两大热点区域。他们 的相识是在 2007年，Guy 在一家以色列开网页应用防火墙和网页安全扫描之先河的公司 Sanctum 做软件工程师，被 Peter 时任 CEO 的 Watchfire 收购之后，担任起了首席架构师。

后来在 2010 年几乎同时，Guy 创立了 Blaze.io，而 Peter 创立起了 Desktone（后来被 VMware 收购），两人各自沿着网络安全领域建树，经历了 Web 1.0、2.0 时代，又在 3.0 时代聚首塑造这个时代需要的安全工具，可谓是将使命一以贯之了。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/013.png)

**03****.**

**产品发展：**

**向云原生应用安全出发**

好的创始人并不是从最开始就怀着百亿美元的野望建立一家公司的，他们总是从某一个他们认为亟待解决的问题切入，并带来独特的技术洞察力，以 10-100 倍的精神不断迭代那个解决方案。**Snyk 的差异点就在于：真正的开发者友好，修复漏洞的语境化和自动化，以及代码安全的深度。**

**Snyk 从最擅长的开源安全切入**：开源安全背后的软件组成分析（SCA）可以帮助开发者们快速跟踪和分析“开源引入项”，包括所有相关组件、它们的支持库以及直接和间接依赖项；还可以检测软件许可证、弃用的依赖项以及漏洞和潜在威胁，检测完成后会生成项目软件资产的完整物料清单 (BOM)。

**过去几年中开源代码使用率的大幅提升使得 SCA 成为应用程序安全测试 (AST) 的关键支柱。**应用程序安全测试是一个更广泛的概念，除了 SCA 以外主要包括了静态 AST (SAST) , 动态 AST (DAST) 和交互式 AST (IAST) 三大技术。

**Snyk 通过收购 DeepCode 进入了 AST 领域，并将范围从代码文件中开源部分的安全，拓展到了整个云原生 AST 领域**：企业的数据中心甚至基础设施移到云端后，其复杂程度也是爆炸式增长的，尤其是“API 化”之后，开发者手上的安全大任变得更加多层次。

于是 Snyk 开始增加产品的延展性，从源代码管理（如 git repo），IDE 插件，到持续集成和持续开发管道（CI/CD pipelines），从容器化 registry 的 Docker Hub 和 Kubernetes， 到更“未来”的软件生成物 registry，以及 Terraform 下的基础设施即代码（Infra as a Code），甚至无服务器（serverless）。

**Snyk 目前有 Snyk Open Source, Snyk Container, Snyk Code 和 Snyk Infrastructure as Code 四大功能模块**，分别是为企业开源代码、容器化项目、应用软件和基础设施代码的安全问题提供的安全工具。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/014.png)

**强大的漏洞库和 Peace-of-mind 的自动修复**

第一个功能模块是 Snyk Open Source，用于测试开源安全。

开源安全的重要性是不言而喻的。96% 的应用程序含有开源代码，而随着开发者们拉取越来越多的开源依赖，其脆弱性在过去的两年间上升了两倍，而且往往盘根错节极为复杂。就像病毒软件会扫描设备并找出威胁一样，Snyk 的产品会扫描源代码并进行漏洞报警，之后将漏洞的严重性进行详细的描述和分类并提供一键修复方案。

其工作原理很简单：首先，Snyk 通过完整的 dependencies tree（依赖项的系谱） 把脆弱点和许可问题的源头路径给语境化和具象化，从而为开发者们带来更深的洞察；

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/015.png)

接着，Snyk 会自动触发最利于漏洞修补的 Pull Request，进行一定规模内的安全性能升级，或者通过专有的精确性补丁（Precision Patches）的形式减少变动；

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/016.png)

最后，Snyk 还会持续监测可能发生的脆弱点，不断自动化安全性能升级的流程。**这有赖于 Snyk Intel，一个自研的代码漏洞数据库，这个数据库的覆盖范围比第二大公开商用数据库大将近4倍，靠的就是 Snyk 的研究团队进行人工搜寻、分析和准确性测量后收录进数据库；Snyk 还会和客户进行数据库上的合作，秉持着人人为我、我为人人的原则，把这个数据库做得越来越周全，达到竞争者难以企及的代码安全深度。**

目前，国家漏洞数据库（National Vulnerability Database, NVD）中92%的 Javascript 漏洞会首先添加到 Snyk 的数据库，所以 Snyk 数据库的漏洞识别整体比第二大公开商用数据库快 25天。**这就是 Snyk 强大的护城河和壁垒。**

最初，Snyk 针对开源项目的服务是完全免费的， 包括针对开源漏洞的无限次测试和修复。现在的 free plan 限制了测试运行的数量，参与收费计划才对 Open Source 和 Container 两个模块开放无限次安全测试，像传统 SaaS 一样采取基于开发者数量的不同收费层级。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/017.png)

**收购 DeepCode：**

**AI-driven 更快更精确的 SAST 方案**

Snyk 通过收购 DeepCode 进入了应用程序安全测试(AST)领域，更准确说是静态 AST 这个子方向。将 Snyk 的超全数据可和 DeepCode 的 AI 技术结合，就诞生了 Snyk Code 这个新功能模块。

DeepCode 是苏黎世联邦理工学院的研究成果(后来分拆出来)，一直专注于应用 AI 来帮助开发者在编写代码时实时提高应用程序的质量和安全性。

这家公司有两大突破性创新点：一是非常复杂的、可解释的机器学习语义代码分析技术，其扫描代码的速度比其他同类技术快 10-50 倍，保障了开发过程中安全工作的实时性（这种实时性对开发者意义非凡，帮助他们在编写代码的过程中即时地受到教育和反馈），而且通过从大量代码中快速学习的机器学习能力，显著减少了误报（包括 false positives 和 false negatives）。

二是通过自定义的下一代 Datalog 解算器，带来了最好的开发者体验。这一技术开创性地实现了实时高精度语义代码分析，并且支持 IDE 和 git 级别的代码扫描，让开发人员得以将安全扫描实时无缝整合到他们的开发过程中，而无需添加中断步骤。

Snyk Code 仍然是秉持重开发者体验的原则，将 Snyk Code 工具直接适配于各个开发者最喜欢的工具和流程。使用 Visual Studio Code 的 Snyk Code IDE 扩展工具或者 IntelliJ、WebStorm、PyCharm 的插件，就可以在编写代码时实时查看代码中的潜在安全漏洞。

**Snyk Code 还解决了传统 SAST 解决方案的最突出问题，同时做到了准确和快速。**它借助语义分析来提升准确性（意味着更少的 false positives，为开发者们节省了宝贵的时间），同时以指数方式增长其知识库；它使用专有的逻辑编程引擎来实现高于竞对的扫描速度；与此同时，Snyk Code 又能提供清晰的解释，使开发者能够轻松理解和解决手头的问题。

**容器化和基础设施代码化大趋势**

Garnter 在今年刚出的一份应用安全测试（AST）行业报告中提到，在过去的三年里，科技企业越来越多地要求额外的服务和工具来完善他们的 AST 覆盖范围并囊括了一些新的开发方法和工件，其中包括 Snyk 一直推崇的云原生支持、API 测试、Infra as Code (IaC) 测试，和容器化安全。

这里就展开讲讲 Snyk Container 和 Snyk Infrastructure as Code 这两大功能模块。

**首先，什么是容器？**

正如航运业使用物理层面的集装箱来隔离不同的货物一样，现在的软件开发越来越多地使用一种“容器化”或者说“集装箱化”的方法。一个标准的“容器”会将应用程序的代码、相关的配置文件和库以及应用程序运行所需的依赖项捆绑在一起，这样开发者和 IT 专员就能跨环境无缝地部署应用程序。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/018.png)

我们可以将容器和传统的虚拟机进行比较：虚拟机包括应用程序、所需的库或二进制文件以及完整的主机操作系统，而对于 Docker 容器，它载有应用程序及其所有依赖项，但它们与其他容器共享操作系统内核，在主机操作系统的用户空间中作为独立进程分别运行。

正因如此，**容器需要的资源比虚拟机少得多，所以它们易于部署且启动速度更快，能在同一硬件单元上运行更多服务，从而降低成本。**

容器和 Kubernetes (常用的容器编排系统) 的广泛采用意味着应用程序可以跨不同的基础设施而移植，目前大约 90% 的公司采用容器化运行以保持灵活性、节省基础设施成本并提高开发人员效率。Snyk Container 的功能便是帮助识别和修复应用程序中所使用的容器镜像中固有的问题。

**那什么是 Infra as Code 呢？**

**如果把软件行业比作建筑行业。Infra as code 其实就是建筑行业原材料的标准化，只不过在软件行业是通过代码来描述他的特点。**

对于水泥而言，有一些参数来表明他可以用于建设何种建筑，在软件行业是通过配置文件和代码来对软件行业的基础设施进行标准化，这里做得比较好的是前不久刚刚 IPO 的 HashiCorp 的 Terraform。

对于建筑行业有监理单位，各种测试机构来保证建筑的安全性，那么谁来保证标准化后的基础设施代码（IaC）的安全性呢？

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/019.png)

以前由 IT 维护的基础设施层，已成为开发人员在云原生应用程序中管理的 API，开发人员越来越多地站在安全的前线，但却没有相应的工具，而 Snyk Infrastructure as Code 的理念就是将基础设施代码纳入应用程序安全的范畴内进行保护，因为它本质上已然成为了应用程序的一部分。

Snyk 是如何扫描并识别云基础设施配置中的安全问题的呢？

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/020.png)

以 CLI （命令行界面）为例（Snyk 同时支持 CLI 和 GUI，但很多 IaC 文件只能通过 CLI 调用，故此），CLI 把 IaC文件内容发送到 Snyk 的后台服务，Snyk 从不断更新的IaC政策数据商店中获取最新政策，并把 IaC 文件与之进行嵌入式对比，发现其中的错误配置，最后，再把结果返还给 CLI 供开发者使用。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/021.png)

其实掌管应用和底层 infra 的存储库都会随时间而改变，但是手动审阅的过程中很可能会忽视云安全的一些新知识和新语境；所以 Snyk 把扫描 IaC 错误配置的过程给自动化，而持续开发和持续集成管道也可以帮助更新和纳入这些变化。

**04.**

**客户与竞争格局**

如今 Snyk 已经有 1200 个企业客户，包括 Google, Intuit, MongoDB, New Relic, Revolut , Salesforce 等重要科技公司。今年9月创始人 Guy 曾分享道，Snyk 的全体用户在过去 12 个月内总共运行了超过 3 亿次测试，并在过去 90 天内修复了超过 3000 万个漏洞。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/022.png)

同时作为 Snyk 的投资人和客户，Atlassian 和 Snyk 合作完成了旗下 Bitbucket, Jira Software, Jira Service Management 的集成。过去，Atlassian 的容器扫描覆盖率非常小，但和 Snyk 合作后实现了 100% 的覆盖率，而且在短短几个月内 Atlassian 的高危开放容器漏洞分别减少了 65%。截至今天，Atlassian 已经使用 Snyk 运行了 550 万次依赖项扫描，并扫描了 370 万个容器。

Snyk 绝大部分客户的使用人数、使用量和相应价格计划等数据都未公开，且 Snyk 至今未披露平均合同额。但根据企业客户数和去年 4 千万美元的收入，可以看出其单个合同价值大概是每年 3 万美元。

Snyk 从基于 SCA（软件组成分析）的开源代码安全起家，推出 Snyk Code 向 SAST（静态应用程序安全测试）延展。其最核心优势就在于真正直接面向开发者的解决方案，但在 AST（应用程序安全测试）领域的知名度不高，毕竟才刚刚借由收购 DeepCode 进入该领域。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/023.png)

**在 SCA 领域，Github 是一个天然的竞争者，**而且就像 Snyk 的客户之一 Segment （Twillo的子公司）所说的那样，因为内部很多代码本身就在 github 上，所以用他们的安全工具非常方便。目前的缺陷是和其他存储库的整合度以及所支持语言的广度不大。

**Snyk 还面临云工作负载保护平台 (CWPP)的玩家竞争**，比如 Lacework（Sutter Hill 孵化的基于Snowflake 的安全公司，最新估值 83 亿美金），Rapid7 的 InsightVM 等。

**在 AST 领域，Snyk 还缺乏自己的 IAST、模糊测试和 DAST 功能模块**，而是与刚刚才提到的 Rapid7 合作提供这些功能。在其他竞争者中，WhiteHat 以 AST 工具系谱的完整性著称，并且在逐渐拓展 SCA 工具；同样是以开发者为中心的 Contrast Security 最大的差异化优势就是被动 IAST 工具，也就是不靠主动扫描而达成的安全检测，其挑战者地位有待证明；Invicti 打的是 DAST 的 niche，Onapsis 则对于一些业务关键的企业软件格外好用；还有像 Veracode（2018 年已被一家美国 PE 以 9.5 亿美金收购）,CheckMarx（去年以 12 亿美金的价格被收购），以及 Synopsys(SNPS)这样的领先玩家。

另外，Snyk 的某个客户访谈中提到，市面上有很多面向传统企业的传统安全公司，他们的优势语言可能是传统的 NET, Java, 或者 Python，且他们的客户有充足的预算可以反复沟通进行适应性调整；相比下来，Snyk 的优势就在于其方案的易用性，不用担心后续的转移成本。这也是为什么一些云服务商的安全工具比如 Amazon Inspector, 微软的 Azure Security，反倒可采购性不及 Snyk 这样的新兴玩家。

当然，那些采用瀑布式开发等传统开发方法的企业，以及主要购买产品供安全团队而非开发团队使用的企业，并不会欣赏 Snyk 的产品，但是这就是 Snyk 所画的边界：Snyk 对未来的预判就是应用层和基建层之间、开发和运行阶段间的边界会越来越模糊，Snyk 就是为支持开发者优先安全的公司而生的。

**05.**

**未来的三个命题**

展望未来，Snyk 有三个方向性的命题。

**第一，是地理上的扩张。**

目前 Snyk 的影响力主要集中在美国和部分欧洲地区。创始人 Guy 公开表明 Snyk 将与新的投资伙伴淡马锡和 Geodesic 合作，将足迹扩展到亚太地区。他还援引了 Ernst and Young 去年的研究发现：在未来两年内，亚太地区 87% 的公司将逐渐实现数字化转型，而“忽略 DevSecOps 会带来给这些刚刚转型的公司带来严重的危机”。

**Snyk 认为这是将 DevSecOps 带到亚太地区的最好时机**，尤其是预计未来十年亚太地区开发者数量的增长将最为强劲。需要注意的是，在新的地缘下开发者生态以及工作模式等方面的不同，是否意味着 Snyk 可能需要在新的场域重新再发起一次 Shift-Left Security 运动？这次市场教育的回报周期需要多长？

**第二，是收费模式的再思考。**

目前 Snyk 的大多数客户还是在 freemium 模式之下，付费用户占 20% 左右。创始人其实有认识到而且多次提及一个重要问题：由于 Snyk 是直接面向开发者的，而购买安全服务的往往是企业内的安全团队，使用者和采购者的不同一导致完全靠产品驱动的销售逻辑并不成立，付费意愿也并不能很好地传导。

在相对比较小的科技公司中，我们看到越来越多的开发团队也有安全工具的采购权。但在大的企业客户组织架构中，笔者采访了一些开发者后得出的结论是，Snyk 产品的可见性不高甚至内部 documentation 都很少提及，**一个合理的猜想是， Snyk 在大公司中的使用场景可能还是在某些小团队，大规模使用的还是自研的安全工具。**

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/024.png)

未来 Snyk 可能需要增强产品团队和销售团队之间的互通，不仅像现在这样做到将销售漏斗的头部扩大，还要减少过程中的流失，通过产品性能和大面积采用进行更好的产品合格线索（PQLs）的转化；Snyk 还有机会探索现在 PLG 公司常用的按用量计费的模式，或者对于检测出的漏洞、以及漏洞相关的智能洞察（Vulnerability Intelligence）进行额外收费。

**最后，是技术拓展以及合作伙伴潜在威胁的审****视。**

Snyk 一路不断在做自动化修补漏洞性能、扩展工具的提升，也一路收割了很多的合作伙伴，比如 RedHat, Docker, Datadog 等，并且战略上 Snyk 也明确表明计划加深与 Atlassian, AWS, Trend Micro 等公司的合作。

但我们也看到，Datadog 和 Palo Alto Network 分别收购了 Spreen 和 Bridgecrew从而也直接入局了 DevSecOps，这个领域随着更多的收购只会更加竞争激烈并且拥挤。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/025.png)

因此，在合作过程中，Snyk 可能需要进行一些战略的防守和布局，从而增强产品的独立性，不至于因为任何伙伴关系的不稳定而损害产品的完整性。

与此同时，Snyk 也要赶在 AST 领域的竞争对手攻入自己所擅长的 SCA 大本营之前，不断向 AST 领域突破，提供更多更纵深的产品支持，锁住更多开发者和企业客户。

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/026.jpg)

**Reference**

https://medium.com/boldstart-ventures/snyk-from-first-check-to-leader-in-dev-friendly-open-source-security-27394201d61d

当时BoldStart投Snyk的memo，可以开放给读者

https://www.youtube.com/watch?v=SriRYKTqBbU

https://www.youtube.com/watch?v=tFmpjBtx1l4

https://mattturck.com/snyk/

https://www.youtube.com/watch?v=sA5q8\_OEiHM

https://www.youtube.com/watch?v=7Z\_BdXXL1Dk

https://go.snyk.io/rs/677-THP-415/images/CNAS\_OReilly.pdf

https://snyk.io/blog/accelerating-developer-first-vision-with-deepcode/

https://snyk.io/blog/snyk-code-now-available-free-sast/

https://whatshot.substack.com/p/whats-in-enterprise-itvc-254

https://whatshot.substack.com/p/whats-in-enterprise-itvc-228

https://whatshot.substack.com/p/whats-in-enterprise-itvc-202

https://faun.pub/snyk-a-security-platform-introduction-2380c28dbe93

https://medium.com/@leonfeng/how-to-protect-your-javascript-projects-from-vulnerabilities-using-snyk-cbfe613cb428

https://medium.com/@allangrds/snyk-io-b35fd761bf38

https://docs.microsoft.com/en-us/dotnet/architecture/microservices/container-docker-introduction/docker-defined

https://www.forbes.com/sites/johnkoetsier/2020/10/15/more-than-a-billion-phones-wide-open-to-backdoor-remote-code-execution-in-adtech-companys-code/?sh=637b3cdb4ef4

https://snyk.io/case-studies/revolut/

https://snyk.io/case-studies/pearson/

https://snyk.io/blog/our-journey-to-today/

https://snyk.io/blog/the-inevitability-of-developer-security/?utm\_campaign=Blog&utm\_medium=Social&utm\_source=Twitter-Organic&utm\_content=the-inevitability-of-developer-security

https://www.cnbc.com/2021/09/08/microsofts-20-billion-and-cybersecuritys-big-spending-problem.html

https://about.crunchbase.com/cybersecurity-research-report-2021/

https://www.gartner.com/doc/reprints?id=1-26OO2IJ1&ct=210630&st=sb

https://medium.com/northzone/the-future-belongs-to-devs-4df5c3a0d929

https://www.computing.co.uk/sponsored/4032679/interview-snyk-best-implementation-devsecops-finalist

https://www.computing.co.uk/sponsored/4032735/interview-simon-maple-snyk

**关于「海外独角兽」**

「海外独角兽」是一个优质内容公共平台，每周两次，我们在这里深度分享科技大航海时代的顶级创新公司。偶尔也会分享让商业世界变得更好的新理念、新技术、新思考。

「海外独角兽」背后的支持团队包括**科技媒体从业者，顶级机构投资人，游戏、crypto、生物科技领域的创业者**。我们相信信息筛选的价值，也相信无论投资还是创业，都需要对未来趋势有清醒的认识和把握。

如果你想参与优质内容的推荐或翻译，欢迎加入我们的内容共创群；如果你是投资人或LP，对全球领先公司感兴趣，也欢迎找我们碰撞思想。主理人微信：

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/027.jpg)

延伸阅读

[![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/028.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485500&idx=1&sn=a81b7c5c3d2c277015b82bd08650e4fe&chksm=ce98b7a2f9ef3eb49a1fbcd4e18f3b36ddba140f32afd996b17e5cc0ab2abb17d662fc358cb2&scene=21#wechat_redirect)

HashiCorp：企业上云的桥梁，云计算领域的 Shopify

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/029.png)

[![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/030.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247486373&idx=1&sn=e85632ccbbed9c58c9591f423ab997c8&chksm=ce98b43bf9ef3d2d58e8eff801055457131fb92a79a528de4cef9828a246250fb4c4f7b78dba&scene=21#wechat_redirect)

Zapier：“API 的 API”，无代码的超级聚合器

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/031.png)

[![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/032.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247488600&idx=1&sn=c909b3fbad3b129452f40c3975fe4b4f&chksm=ce98abc6f9ef22d0989fe304822b0da1cda08ff31e6507775ddb2c48e194c1767dc6bdc92901&scene=21#wechat_redirect)

Fivetran：云计算时代的数据管道，估值56亿美金的行业创新者

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/033.png)

[![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/034.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247483926&idx=1&sn=00e1fdffd348773595df034971844ced&chksm=ce98bd88f9ef349ed2d04102a3e79c2e98ecba0a8f19c6ab5eabe0e5356bacda0c9e4259fbc8&scene=21#wechat_redirect)

Stripe：从7行代码到千亿美金的互联网基础设施

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/035.png)

[![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/036.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485588&idx=1&sn=4ac9cf6394e4e111b81c49ec5aa389bd&chksm=ce98b70af9ef3e1cff4e22bed48867a2850d8423c509d95ee0253240eb7ca2704358bd8519aa&scene=21#wechat_redirect)

[Airtable不是Excel，是企业服务界的Roblox](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485588&idx=1&sn=4ac9cf6394e4e111b81c49ec5aa389bd&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485588&idx=1&sn=4ac9cf6394e4e111b81c49ec5aa389bd&scene=21#wechat_redirect")

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/037.png)

[![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/038.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247487791&idx=1&sn=86b06aace5914a6aee26b9d2e1400d7d&chksm=ce98aeb1f9ef27a7e8be3b008ed2fd96471c47a53cc213cd1ffb42e24b4186c7c6ee9dae4f54&scene=21#wechat_redirect)

分拆 Office 数十年后，40亿美金的 ClickUp 重新整合生产力工具

![](../images/2021-12-23-snyk-bi-datadoggeng-jin-yi-bu-de-dai-ma-an-quan-wei-shi-gu/039.png)
