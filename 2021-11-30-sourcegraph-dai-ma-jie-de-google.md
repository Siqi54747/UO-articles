---
title: Sourcegraph：代码界的Google
publish_date: '2021-11-30'
publish_timestamp: 1638275440
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/AlA1J1uziWBGlvJUP2X3cA
msgid: 1000000044
appmsgid: 2247488558
itemidx: 1
digest: Sourcegraph把代码搜索带给所有人，而不仅是Google、Meta里1%的开发者。
cover: https://mmbiz.qlogo.cn/mmbiz_jpg/3tHNibnJ2jgziblIgyibR9V7Q21kz6ZiaiaI8SBYWoeOrG37JZCkk4GssOiboufFicCy0YSz7uItNRo1vcSQI4Oho2COQ/0?wx_fmt=jpeg
image_count: 32
archived_at: '2026-04-19T23:06:32+08:00'
---

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/001.gif)

积极推动中国企业家参与科技大航海

打造全球领先的资产配置服务

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/002.jpg)

**作者：Jessie**

**编辑：penny**

**排版：Jessie**

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/003.png)

**Sourcegraph 被称为“代码界的 Google”，它的出现旨在解决****开发者****面对海量代码时的困扰****——代码搜索。**

日益增长的源代码数量和种类使代码管理变得棘手，开发者承受着混乱、低效且工作量巨大的编程体验。

Google 和 Meta 率先开发了代码搜索，在内部构件了强大的专有工具，而 Sourcegraph 将这项技术带给每个人。**Sourcegraph****不仅使通用代码搜索民主化，还通过将新的工作流附加到搜索中，进一步推动品类定义。**

通过代码搜索，Sourcegraph 把软件开发和 IT 运营的各个环节联系起来，让团队能更便捷地写代码，更快地发现和修复 bug，更流畅地进行协作。

Sourcegraph 由两位极富才华的工程师于2013年创建，今年7月，以 26 亿美元估值获得了 1.25 亿美元 D 轮融资，由a16z 领投，历史股东包括红杉资本、Craft Ventures 等。

**去年，Sourcegraph 的营收和客户量增长了 4 倍，有 80 万开发者在使用这个产品，索引的代码超过 540 亿行**，付费客户包括 Amazon、Paypal、Uber、Unity、Plaid、GE 和 Atlassian 等知名企业。

**GitLab的CEO Sid Sijbrandij 曾评价 Sourcegraph****，** **“拥有这个****世界上****最好的查找定义、查找引用和智能代码导航能力。”**

**以下为本文目录，建议结合下方要点进行针对性阅读。**

**👇**

01. 背景：代码的困境

- 开发者的革命
- 大代码问题
- 什么是通用代码搜索？

02. 两个“代码迷”的相遇

03. 产品：为什么要选择 Sourcegraph?

04. 客户应用

05. 盈利模式及行业启发

06. 远望：代码搜索民主化的未来

**01.**

**背景：代码的困境**

**开发者的革命**

1983 年，一批开发者受邀到加州蒙特利（Monterey）参加苹果开发者大会。

开发者们见证了刚诞生的 Lisa 电脑，以及一年后轰动全美、引起巨大争议的广告 “1984”。

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/004.png)

苹果1984年的广告

广告中，一群面如死灰，动作整齐的人正在聆听屏幕上一个硕大头像的演讲：“我们思想上的统一，比世界上任何军队都强大……” 与此同时，一个穿背心和运动短裤，戴随身听的年轻女孩抡着锤子拼命奔跑，最后把大锤砸向了巨幕。

这一意象来自奥威尔的小说《1984》。广告里的硕大头像讽刺的是 IBM 的垄断和专制，IBM 靠着 PC 和 DOS 掌控着绝大部分市场，**而**苹******果这一年推出个人消费型计算机 Macintosh，第一次将定义互联网发展的权力交到了开发者个体手中。**

“1984”广告的创意导演 Lee Clow 回忆说：“‘1984’表达了苹果的理念和目标：**让大众而非大公司掌握操纵技术，让计算机变得普通人可及，而不是控制人的生活**”。

2018年，微软以75亿美元收购了全球最大的开发者社区 GitHub。公布收购消息后，微软 CEO Nadella 第一时间转发 Twitter，并写道：“Microsoft + GitHub = Empowering Developers（微软 + GitHub = 赋能开发者）。”可见，**微软试图更好地与几千万开发者接触。**

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/005.png)

但是，开发者们并不买账。**这一举动引发了一向推崇“开放、开源、反垄断”的开发者们的强烈不满，造成 Github 的用户大规模向 Gitlab 迁徙，这也是促成 Gitlab 快速崛起、成为 Github最强大的竞争对手的重要原因之一**。

这两个例子都反映出巨头对开发者的重视，以及开发者地位的增加。

**开发者成为 “新英雄”，是因为科技日益成为 “新宗教”。**

一方面，互联网红利消失，市场重新进入新一代技术开荒期，新商业机会的技术门槛徒增：云计算、大数据、AI、区块链…… 无一不需要大量开发者来贡献力量。

另一方面，全球疫情使互联网基础设施变成维持世界良好运转最重要的底盘之一，这一切都依赖开发者群体的贡献。**开发者不再是拓荒时期的牛仔、嬉皮士和独行侠。连结、协作、以及有如粮食般的海量数据是开发者重塑世界时不可或缺的工具。**

**个人、组织和整个社会都面临一个共同议题：如何适应正在成形并崛起的 “开发者文化” 和开发者共同体？**

**大代码问题**

大代码就是开发者面临的一个很大挑战。

过去二十年互联网的飞速发展带来了大代码问题：分散的团队开发各种不同语言的应用软件、成百上千的微服务和第三方代码库、随时担心代码出问题的焦虑感……

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/006.png)

Dimensional Research 发布的《2020软件专业报告》显示，**我们已经进入了大代码（Big Code）时代。所谓“大代码”，主要体现在四个维度，可以用四个“V”来概括 —— Volume（数量）、Variety（多样性）、Velocity（速度）、Value（价值），也即代码数量和复杂性上的急剧增长，包括开发环境、平台和工具的多样性，交付速度变快，预期的商业价值提高。**

调查显示，94%的人都认为自己受到了大代码的冲击。

- **Volume（数量）：**51%的人认为他们拥有超过10年前100倍的代码量；
- **Variety（多样性）：**超过60%的人认为，在开发的不同维度，架构、支持设备、开源使用、平台数量等方面，都有巨大增长；
- **Velocity（速度）：**92%的人发布代码速度的压力比过去十年增加了很多；
- **Value（价值）：**90%的人认为他们交付的软件变得越来越至关重要。

**代码复杂性的急剧上升给开发团队带来了广泛的挑战。**被提到的首要挑战是新员工要花很多时间和精力来提高工作效率（62%），其次是由于不了解依赖关系而导致的代码中断（57%），管理代码更困难（50%），团队协作和重复工作缺乏可见结果（46%），代码审查缓慢（43%），开发者难以找到特定的代码（40%），很难理解新的代码库（38%）等等。

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/007.png)

大代码问题给开发团队带来了哪些挑战？

Google 最早意识到开发者们的需求，**在公司内****投入数亿美金进行代码管理的基础设施建设，让内部开发者更轻松地浏览代码库、使用更强大的搜索语言查找函数和变量、轻松定位想要的代码位置等等。这种工具被称为“代码搜索”。**

但 Google 的代码搜索工具并不对外开放，更多公司并没有 Google 的雄厚财力去支撑这种基础设施建设。

**同时，代码搜索是一个高频需求。**早在2015年，Google 研究人员发布的论文就显示：开发者平均每天至少做5次搜索，12次查询。考虑到后来微服务的爆发，这个需求在近两年以及未来只会更加强烈。

**所以，****通用代码搜索是必要的。**

**什么是通用代码搜索？**

如果有个第三方公司，可以做一个**通用型的代码搜索工具，为所有有需求的企业提供代码搜索服务**，这个问题就能得到解决——这就是Sourcegraph在做的事情。

和 Google 内部的代码搜索工具不同，Sourcegraph 要为所有公司提供通用的代码搜索服务，

传统的开发者工具，如编辑器和 IDE （Integrated Development Environment，集成开发环境），都是为在单个代码库中工作的个人开发者建立，而不是为大规模处理大型代码库的团队建立的，因此在搜索方面受到严重限制。

GitHub 正在努力改善其代码搜索能力，但其为单一代码主机建立，不能成为一个通用的、跨存储库的解决方案。

*注：IDE（Integrated Development Environment 集成开发环境），一种用于构建应用程序的软件，可将常用的开发人员工具合并到单个 GUI（ Graphical User Interface 图形用户界面）中。*

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/008.png)

**通用代码搜索则不同。**无论是什么样的系统、存储库或语言，它都以一种统一的、高度可扩展的方式来探索、浏览和分析一个组织的所有代码存储。

**对于使用通用代码搜索的开发者而言**，可以在不同的代码库中搜索和调用已经存在的代码，而不必重新编写和调试代码，找出适合某项任务的库或服务，并分享代码链接和团队成员们协作。

**对于 API 所有者而言，**也可以看到并监控谁在使用他们的代码以及如何使用，在所有存储库中升级 API 用户的调用站点，并废止旧的 API。

*注：API（Application Programming Interface，应用程序接口），是一些预先定义的接口（如函数、HTTP接口），或指软件系统不同组成部分衔接的约定。*

**对于 DevOps 和安全团队而言**，通用代码搜索可以准确定位错误或漏洞的来源，发现造成意外事件的代码变更，评估在生产中特定代码行的性能，并在所有存储库中打补丁和升级。

*注：DevOps是一套结合了软件开发（Development）和 IT运营（Operations）的流程，它旨在缩短系统开发生命周期并提供具有高软件质量的持续交付。*

为了有效，搜索必须在以下几个维度具有普适性：

- 所有存储库（repositories）；
- 所有编程语言 (programming languages)；
- 所有代码变更 (code changes)，包括代码的分支（branches）、分叉（forks)；
- 所有的文件格式 (file formats)；
- 所有其他生成代码元数据的开发者工具，如用于记录（logging）、跟踪（tracing）和分析（profiling）的工具。

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/009.png)

通用代码搜索满足所有要求，用户只需通过浏览器、shell 或直接在 GitHub、GitLab、Bitbucket Server、Phabricator、Perforce 和 Subversion 等流行工具中进行搜索，就会立刻得到搜索结果，非常便捷。

不过，构建通用代码搜索也是非常困难的，**它需要支持所有主要语言、所有代码主机，例如 GitHub、GitLab、Bitbucket 以及它们的所有最新版本；数百万个存储库需要与开发堆栈中的许多工具集成。这是极其大量、极有挑战的工作。**

那么，Sourcegraph 团队是如何走上这条艰难的创业之路呢？

**02.**

**两个“代码迷”的相遇**

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/010.png)

左：Quinn Slack    右：Beyang Liu

2011年，Sourcegraph 的创始人 **Quinn Slack 敏锐地意识到了“大代码”的问题，他在那时就断言：“代码搜索将成为每个开发人员都会使用的新事物之一。”** 2013年，Quinn Slack 和 Beyang Liu一起创立了Sourcegraph。

CEO Quinn Slack 从十岁就开始自学编程，尤其热衷泡在各种论坛中，为一些大的开源项目打补丁。从斯坦福大学获得计算机学士学位后，他曾在 Palantir Technologies 创建了一个技术平台，帮助美国前五名银行中的两家从次贷危机中复苏；后来，他又联合创立了 一家技术公司 Blend Labs，拥有约 500 名员工，致力于改善住房贷款。**可见，他一直是喜欢用技术解决实际问题的人。**

*注：Palantir Technologies，美国一家专注于大数据分析的上市软件公司。Sourcegraph 的联合创始人 Beyang Liu 也曾就职于此。*

Sourcegraph 的 CTO Beyang Liu 同样毕业于斯坦福大学计算机专业。和 Quinn Slack 一样，Beyang 从小就痴迷于编程技术，非常热衷于探索各种有趣先进的编程语言。

后来，他在 Google 实习时发现内部都在使用一种代码搜索工具，于是产生了开发第三方代码搜索工具，以供更多企业使用的想法。**这与当时 Quinn Slack 的判断和想法不谋而合。**

可以说，**正因为两人都是****痴迷代码、热衷解决代码问题工程师，才能长久坚持做一家解决“代码困境”的企业。**

Sourcegraph D 轮融资的领投机构 a16z 如此评价这两位创始人：

"Quinn 和 Beyang 才华横溢，以使命为导向，思想开放，而且坚持不懈。**他们拥有我们希望的最好的创始人拥有的那种勇气。**最好的开发工具不是一天建成的——Quinn 和 Beyang 自 2013 年以来一直在努力，**因为他们坚信可以构建开发人员所需的工具，也坚信代码搜索会像 Google 搜索那样普及和通用。"**

**03.**

**产品：****为什么要选择 Sourcegraph?**

**产品功能优势**

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/011.png)

**保证工作流畅**

导致编程效率低下的原因之一是无数次的切换。比如一个开发者正在修复一处报错，突然需要跳到代码库的另一个部分查找某个库函数，**开发者不得不在 IDE 中打开这些文件，这样做会破坏当前的工作状态，之后再重建。**这种“中断”具有很大的破坏性，因为它们使开发者脱离了“工作流”状态，造成生产力低下。

而 Sourcegraph 基于浏览器的代码搜索和探索界面让开发者在搜索代码时，其他部分保持编辑状态。**这种对工作状态的保留使得页面切换的成本大大降低。**

**不再“大海捞针”**

开发者常见的一个任务是在代码中寻找一个特定的字符串，比如出现报错的时候。

但找到那些特定的微小标记，非常麻烦。IDE 有搜索功能，但有问题的代码可能存在于 IDE 所打开的内容之外。**代码主机只对其托管的代码进行搜索，而不能访问本地文件系统以外的代码，以至于这种搜索往往是缓慢或低质量的，代码搜索必须是通用的才有效。**

有了 Sourcegraph，开发者就可以**横跨整个代码库。**Sourcegraph 的搜索引擎针对源代码进行了优化，所以它的速度非常快，它的设计初衷也是为了扩展到大型代码库。**有些组织有数十万个存储库，而 Sourcegraph 将它们全部向每个（组织内的）开发者开放。**

强大的搜索语法让用户可以通过文件、语言、资源库和无数其他属性过滤结果。Sourcegraph 还了解代码语义，允许直接搜索符号。

**通过实例学习**

"我如何使用这个？"这是开发人员每天要问几十次的问题。

**Sourcegraph 的全局查找参考功能让开发者可以在整个代码库中查找使用范例，**即使理想的使用范例存在于另一个资源库中。这对那些老旧的、不熟悉的、或文档不全的代码库特别有帮助。

**快速审查代码**

有一个关于代码审查的常见调侃：如果你提交一个10 行的修改集，你会得到10条评论，但如果你提交一个1000行的修改集，你不会得到任何评论 —— 而是自动批准。

**高质量的代码审查往往是极其缓慢的，因为传统工具缺乏许多必要功能来帮助审查者快速了解代码的变化。**Sourcegraph 为开发者现有的代码审查工作流程增加了类似 IDE 的代码导航和工具提示。

Sourcegraph 的悬停工具提示让审查员迅速浏览函数定义和文档，而不必将变更集拉到本地 IDE 中。在不离开代码审查界面的情况下，Sourcegraph让你跳转到一个新的定义，以更全面地了解被引用的代码是如何工作的。

**简化大规模的重构**

随着代码库的增长，大规模的重构成为提高代码质量和实现新功能的一个不可避免的瓶颈。例如，一个共享库的 API 可能需要更新以支持一个新的功能，但这样做可能需要更新几十个甚至几百个下游的依赖项。只要更新一个共享的依赖关系，代码中必须改变的数量就可能达到上千个，而且分布在不同团队的不同组件中。

Sourcegraph 不仅帮助开发人员了解重构的影响（通过让他们搜索和发现所有使用特定库函数的地方），它还提供了一个执行重构、管理更改集和代码审查运动的装置。

*注：库函数（Library function），是指把一些常用的函数编完放到一个文件里，供不同的人进行调用。*

**鼓励整个组织知识共享**

软件团队通过协作来分享代码知识。但由于以下原因，团队一起讨论代码往往很难：

- 不能分享你在IDE中打开的文件的超链接
- 传统的浏览器代码查看工具没有好的代码导航

Sourcegraph 提供了解决这两个问题最好的工具：精准的代码导航。这便于分享链接，接收者可以立即探索和理解链接到的代码，而不需要在本地 IDE 中拉出代码。

**代码链接共享对于远程工程团队来说更加重要。**Sourcegraph 链接每天通过聊天、问题追踪器、官方文档共享数百次。这些都成为知识分享的重要渠道。

**它是开源的**

Sourcegraph 是开源软件。问题跟踪器是公开的，团队对错误报告和功能请求的反应非常迅速。这让**所有人都可以了解它是如何工作的，所有人都可以帮助改进它。**

**产品战略优势**

**集成性**

开发者可以在 Datadog 平台进行云监控，可以使用 Codecov 之类的工具检查代码库的测试覆盖率，然后用LaunchDarkly 停用导致故障的新实验功能。**但问题是，所有这些工具都是分开存在的。**

Sourcegraph 的 CEO Quinn Slack 说：

"这些服务都有助于处理大代码——**困难的是将它们串联成一个开发人员可以快速执行的工作流程，**一家公司的所有开发者工具都应该结合在一起，以便有效地解决大代码问题。"

因此，Sourcegraph 提供了各种扩展，允许公司将所有这些工具集成到一个平台中。

**安全性**

**从云托管转为本地自托管**

2017 年 12 月，Sourcegraph 从传统的云托管软件即服务 (SaaS) 产品转变为内部部署的自托管产品。

尽管企业的工程师们对通用代码搜索工具有明显的需求，但 Sourcegraph 在切入市场时只服务少量中大型客户。原因是：**企业工程师们并不想将自己的私有代码库推送给外部软件提供商。由于频繁收到这一反馈，Sourcegraph 决定逆 SaaS 趋势，将产品转变为本地自托管解决方案。**

自从 Sourcegraph 2.3 作为内部部署、自托管产品发布以来，Sourcegraph 在企业使用中迎来了更高的采用率。

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/012.png)

**从 SaaS 切换到本地部署对于 Sourcegraph 被 Lyft、Uber、Plaid、Convoy 等顶级公司中采用至关重要。**虽然 SaaS 可能在很多场景下是一种良好的解决方案，但**提供本地部署更是那些具有安全意识的公司采用 Sourcegraph 的决定性因素。**

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/013.png)

**建设安全云**

2020年12月，Sourcegraph 获得红杉资本领投的5000万美元 C 轮融资后， Quinn Slack 表示：“将投入2000 万美元用于建设大型企业的安全且可扩展的 Sourcegraph 云。”

当时，Sourcegraph 已经拥有了一众知名大客户，但 **Sourcegraph 的本地自托管对于企业的计算基础设施建设的要求非常高，成本相当高昂。**

为了争取更多的中小企业用户，对于那些不到100人的组织，Sourcegraph 团队**推出了 Sourcegraph Cloud 作为 Sourcegraph Server 的替代方案，**使他们可以在 Sourcegraph Cloud 上托管私有代码。同时**加强对安全性的建设，不仅确保产品的安全性（这对于内部部署也很重要），也保障了 Sourcegraph Cloud 基础架构的安全性。**

**04.**

**客户应用**

**客户画像**

Sourcegraph 受到诸多知名大企业的青睐，诸如 Amazon、PayPal、Uber等，这些优质的巨头客户给 Sourcegraph 带来了巨大的品牌资产，奠定了其通用代码搜索领域的领先地位。

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/014.png)

我们在营销情报数据平台 HG Insights 上查看了Sourcegraph 客户中35家的基本信息，其中大型企业为主，员工规模在10,000人以上的企业占到25.7%，1000人以上的企业占到48.6%；营收在10亿美金以上的企业占到46%；集中在科技、金融领域。

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/015.png)

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/016.png)

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/017.png)

Sourcegraph 的客户集中在科技、金融领域

这不难理解。**大企业的代码量更大，科技行业尤其如此，代码搜索功能能极大地改善开发团队的工作体验；而且大企业有更好的付费意愿和付费能力。**大公司拥有大预算，这将转化为最大的 ACV （Annual Contract Value，年度合同价值），将为面向B端的销售工作带来更高的投资回报率。而且一旦签约，这些客户几乎不会流失，一旦满足大公司的深层产品需求，就会形成护城河。

**这也是 Sourcegraph 团队尤其注重面向大企业销售的原因，这极大地帮助他们在行业内形成了一定的品牌效应和行业地位。**

虽然大客户在 Sourcegraph 的客户群体中占据着绝对亮眼的比重，但小企业对 Sourcegraph 的采用也很重要。如前文所说，Sourcegraph 建设的 Sourcegraph Cloud  ，试图为中小企业带来便利。

**实例：****SoFi 使用 Sourcegraph 管理数百个微服务**

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/018.png)

SoFi (Social Finance Inc.) 帮助超过 90 名会员实现财务独立，通过借贷、储蓄、支出、投资和保护资金的产品满足客户需求。

SoFi 运行着数百个微服务，它们的快速增长使得维护已发布 API 的完整列表非常困难。Sourcegraph 的一个常见用例是查找哪个微服务被另一个引用。**这种能力可以防止因某部分代码更改而中断生产，并避免代码重复。**

SoFi 工程经理 Ursula Robertson 这样评价：

**“Sourcegraph 是我在 SoFi 日常工作中必不可少的一部分。使用 Sourcegraph，我们的工程师可以了解到其他服务进行更改所带来的所有影响。”**

**05.**

**盈利模式及行业启发**

**收费模式**

Sourcegraph 的收费模式相当简单，10 人以下免费使用，企业版则需要定制价格，不限用户数，并且有专门的客户工程师服务协议和私人 Slack 频道。

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/019.png)

**自下而上使用**

Sourcegraph 是一个给 C 端使用，但 B 端乐意买单的产品。

在 B 轮融资时，Craft Ventures 的创始人 David Sacks 着重讨论了这个问题，**市场的需求是由开发者自下而上驱动（Bottom-up），也就是 PLG（Product-Led-Growth，SaaS公司依靠产品、优秀的用户体验来推动增长）。Sacks 说他们最喜欢的 SaaS 业务是员工将产品作为终端用户带入公司的业务。**

这种免费增值使用有助于 SaaS 供应商快速证明产品价值，缩短漫企业销售周期。所谓**免费增值，就是指提供免费的基础版本，并通过付费去解决功能更加全面、强大的高级版本，非常适合于那些鼓励用户生成内容、网络效应强大或自下而上采用的病毒式产品。**

David Sacks 称为“两全其美”的销售活动，因为**它兼顾了企业预算与销售周期。**

自下而上的模式不仅对供应商有利，对客户也更有利。**免费增值使用降低了购买风险，消除了软件最终成为摆设的可能性。**

**业务增长**

David Sacks 在 Sourcegraph 2020年B轮融资时，分享了一些几个关于 Sourcegraph 的增长数据：

- ARR（Annual Recurring Revenue，年度经常性收入）的年增长已经达到了 4 倍左右；
- 企业客户流失率为 0；
- NRR（Net Revenue Retention，净收入保留率）超过了 200%；
- 获得了大批知名大客户的认可，包括Uber、Lyft、Yelp、Convoy 和 SoFi。

*注：NRR —— Net Revenue Retention，净收入保留率，在一定时间内（通常是每月或每年）从现有客户保留的经常性收入的百分比。*

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/020.png)

Yelp上 Sourcegraph 的每日活跃用户

在今年7月最新一轮融资中以26亿美金的估值获得了1.25亿美金的D轮融资，由 Andreessen Horowitz （a16z）领投，Insight Partners、Geodesic Capital 和其他现有投资者参投。

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/021.png)

企业估值

**行业启发**

**对于寻找创业切入点的创始人，一个有用的办法是找到一家卓越的科技公司为自己打造的内部工具，将其变成通用产品。**

Google 和 Facebook 率先开发了代码搜索并构建了强大但专有的工具，而 Sourcegraph 将这项技术带给每个人，帮助开发团队驾驭所有企业都采用的复杂工具、语言和平台。

**Sourcegraph 不仅使通用代码搜索民主化，它还通过将新的工作流程附加到搜索中来进一步推动品类定义，**例如管理代码更改活动的能力。例如，工程副总裁可以使用 Sourcegraph 修复所有代码中的关键安全问题，并确保它永远不会退化。

搜索为进一步创新提供了广阔的空间。Google 已经证明，如果你可以为某人生活的一部分建立搜索，就可以在他们的生活中发挥越来越重要的作用。强大的搜索功能会简化工作流程，并成为其他一切的起点。

**06.**

**远望：****代码搜索民主的未来**

Sourcegraph 有着宏大而浪漫的愿景。

**正如见过光明的人无法想象再次回到黑暗，Sourcegraph 坚信自己是取火的普罗米修斯，将代码搜索从科技的奥林匹斯山下取回，让每个人都能使用它，而不仅仅是那些在 Google 或者其他科技巨头工作的 0.1%的开发者们。**

就像所有人都可以通过 Netscape Navigator 和 Google Web Search 等工具访问互联网，所有人都可以通过 Windows 和 Macintosh 访问桌面计算，Sourcegraph 的愿景是让使所有人都可以使用代码，**实现真正的“代码平权”。**

然而当下，Sourcegraph 也存在一些挑战需要去克服。

虽然当前 Sourcegraph 的用户量很好，**但每天使用频率并没有很高**；而且，**软件开发主管很难了解到团队对代码搜索工具的具体使用情况**，缺乏他们想要的数据和信息从而支持他们更多的决策，形成具有高价值的反馈循环。

不过关于这些问题，Sourcegraph 团队已经想出了明确的解决方案，相信在得到如此高额的 D 轮融资以及明星风投的资源加持之后，团队可以更加从容地解决这些障碍。

**Reference**

https://discovery.hgdata.com/product/sourcegraph

https://au.sports.yahoo.com/sourcegraph-secures-50-million-series-130000457.html

https://thenewstack.io/universal-code-search-a-new-search-tech-for-the-era-of-big-code/

https://venturebeat.com/2020/12/03/sourcegraph-raises-50-million-to-tackle-big-code-problems-with-universal-search/

https://handbook.sourcegraph.com/company/strategy?\_ga=2.42935653.1904866798.1635479405-418481644.1635479404#purpose

https://sacks.substack.com/p/why-we-invested-in-sourcegraph-5ace28317e3d

https://forgeglobal.com/sourcegraph\_stock/

Why Sourcegraph switched from cloud SaaS to on-premises, self-hosted software

https://www.infoworld.com/article/3514213/sourcegraph-universal-code-search-and-intelligence.html

https://www.ifanr.com/1048152

**关于「海外独角兽」**

「海外独角兽」是一个优质内容公共平台，每周两次，我们在这里深度分享科技大航海时代的顶级创新公司。偶尔也会分享让商业世界变得更好的新理念、新技术、新思考。

「海外独角兽」背后的支持团队包括**科技媒体从业者，顶级机构投资人，游戏、crypto、生物科技领域的创业者**。我们相信信息筛选的价值，也相信无论投资还是创业，都需要对未来趋势有清醒的认识和把握。

如果你想参与优质内容的推荐或翻译，欢迎加入我们的内容共创群；如果你是投资人或LP，对全球领先公司感兴趣，也欢迎找我们碰撞思想。主理人微信：

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/022.jpg)

延伸阅读

[![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/023.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485500&idx=1&sn=a81b7c5c3d2c277015b82bd08650e4fe&chksm=ce98b7a2f9ef3eb49a1fbcd4e18f3b36ddba140f32afd996b17e5cc0ab2abb17d662fc358cb2&scene=21#wechat_redirect "http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247485500&idx=1&sn=a81b7c5c3d2c277015b82bd08650e4fe&chksm=ce98b7a2f9ef3eb49a1fbcd4e18f3b36ddba140f32afd996b17e5cc0ab2abb17d662fc358cb2&scene=21#wechat_redirect")

HashiCorp：企业上云的桥梁，云计算领域的 Shopify

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/024.png)

[![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/025.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247487791&idx=1&sn=86b06aace5914a6aee26b9d2e1400d7d&chksm=ce98aeb1f9ef27a7e8be3b008ed2fd96471c47a53cc213cd1ffb42e24b4186c7c6ee9dae4f54&scene=21#wechat_redirect "http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247487791&idx=1&sn=86b06aace5914a6aee26b9d2e1400d7d&chksm=ce98aeb1f9ef27a7e8be3b008ed2fd96471c47a53cc213cd1ffb42e24b4186c7c6ee9dae4f54&scene=21#wechat_redirect")

分拆 Office 数十年后，40亿美金的 ClickUp 重新整合生产力工具

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/026.png)

[![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/027.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247486373&idx=1&sn=e85632ccbbed9c58c9591f423ab997c8&chksm=ce98b43bf9ef3d2d58e8eff801055457131fb92a79a528de4cef9828a246250fb4c4f7b78dba&scene=21#wechat_redirect "http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247486373&idx=1&sn=e85632ccbbed9c58c9591f423ab997c8&chksm=ce98b43bf9ef3d2d58e8eff801055457131fb92a79a528de4cef9828a246250fb4c4f7b78dba&scene=21#wechat_redirect")

Zapier：“API 的 API”，无代码的超级聚合器

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/028.png)

[![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/029.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247486004&idx=1&sn=afd920032d7bf7239d75bb11ee3d80ae&chksm=ce98b5aaf9ef3cbc4a19ea0af49a688159fb67f7711a7cd91880170d19b8de54806c70c1dbda&scene=21#wechat_redirect "http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247486004&idx=1&sn=afd920032d7bf7239d75bb11ee3d80ae&chksm=ce98b5aaf9ef3cbc4a19ea0af49a688159fb67f7711a7cd91880170d19b8de54806c70c1dbda&scene=21#wechat_redirect")

[Zoom、Figma都采用的PLG策略，代表了SaaS的未来趋势](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247486004&idx=1&sn=afd920032d7bf7239d75bb11ee3d80ae&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247486004&idx=1&sn=afd920032d7bf7239d75bb11ee3d80ae&scene=21#wechat_redirect")

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/030.png)

[![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/031.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247483926&idx=1&sn=00e1fdffd348773595df034971844ced&chksm=ce98bd88f9ef349ed2d04102a3e79c2e98ecba0a8f19c6ab5eabe0e5356bacda0c9e4259fbc8&scene=21#wechat_redirect "http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247483926&idx=1&sn=00e1fdffd348773595df034971844ced&chksm=ce98bd88f9ef349ed2d04102a3e79c2e98ecba0a8f19c6ab5eabe0e5356bacda0c9e4259fbc8&scene=21#wechat_redirect")

Stripe：从7行代码到千亿美金的互联网基础设施

![](../images/2021-11-30-sourcegraph-dai-ma-jie-de-google/032.png)
