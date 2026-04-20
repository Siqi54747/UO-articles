---
title: Vercel：用生成式UI重塑前端开发
publish_date: '2024-04-02'
publish_timestamp: 1712060000
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/7UBlsoP8mjfcwtZaAFVSow
msgid: 1000000257
appmsgid: 2247507124
itemidx: 1
digest: AI-native app 最好的前端开发平台
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgyFvicicHIUh56x0clheek9cWWjRgeDXg3tneibicPuTHm76ZMdJD887YPXdRhjnBD0xzlSNXUrwHyOmA/0?wx_fmt=jpeg
image_count: 32
archived_at: '2026-04-20T02:10:57+08:00'
---

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/001.gif)

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/002.png)

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/003.png)

作者：Cage、Scarlett

排版：Scout

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/004.png)

**AI 正在重塑软件的生产方式，而前端开发是最先可能受影响的领域：**前端开发逻辑适合**模板化**，且开发者多、头部开发语言集中。前端的视觉属性适合用户快速表达偏好，形成**数据飞轮**。随着前端代码能够被实时生成，生成式 UI 能带来人机交互方式的创新，比 Chatbot 更智能的 LUI+GUI 产品交互将涌现。

Vercel V0 是目前**最好的 UI 生成模型，且可控性远强于其他模态的生成模型**，因为软件的可编码性让用户可以对任意一个web组件用prompt进行改写。同时他们的 AI SDK 也让前端开发者更无缝地将 LLM 能力融入产品中，打造出一个能实时生成 UI 的产品。对比其他代码模型还停留在 code autocompletion 和 demo 的状态，Vercel 团队对前端开发的深入理解和数据积累让他们能成为领军者。

Vercel 从前端开源框架 Next.js 起家，打造了**开发者口碑最佳的 frontend cloud**，让用户可以快速在其平台上完成 web development 并进行部署。他们保持着 ARR 100%+ YoY 的高速增长，并且 AI-native application 的首选平台：Jasper、Scale、Anthropic 等公司的 AI 产品均使用 Next.js + Vercel 打造。由于其创始人 Guillermo Rauch 对 AI 前沿技术十分敏锐，我们相信 Vercel 能抓住 web application 文艺复兴的机会，成为**新时代 AI 产品开发者的第一选择。**

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 前端开发与 Next.js 的发展

02 Generative UI: Gen AI x Web development

03 Frontend Cloud：最好的 AI-native 产品部署平台

04 市场与商业化

05 创始人：从开源开发者到 CEO

**01.**

**前端开发与 Next.js 的发展**

**为什么关注前端市场**

**AGI 很可能在开发领域率先实现**，因为代码比自然语言更清晰明确、是经过形式逻辑优化的语言，而且开发场景的 feedback loop 是可以由机器自己验证并迭代的，因为代码环境本身能够验证报错。

长期最值得关注的是能够把 coding + CI/CD 工作流完整自动化的 coding agent，比如最近由 Cognition Labs 发布的 Devin demo 就是一个优秀的例子。但 Devin 作为 SOTA，在没有人类干预的情况下能解决的 Github issue 比例也只有 ~13%，距离实际部署到生产环境还有一段 gap。

就像自动驾驶在 L3 的状态时，有机会的是自动驾驶卡车这样的垂直领域。而前端开发 web development 就是现阶段 coding 最值得期待的领域，这个领域有以下几个重要趋势：

**1. Web 市场大，开发者渗透率高：**

全球范围内有10 亿+网站，web hosting 是一个千亿美金级的市场。根据 2023 年数据市场集中度低，美国市场占了 42%，其中老牌域名托管 GoDaddy 占了 9.3%，后面两位分别是 GCP（7.03%）和 AWS（4.48%）。

除了专业前端开发者，很多独立或全站开发者都承担一定的前端工作来实现产品交互。根据 StackOverflow 2023 的统计，Javascript 和 HTML/CSS 的开发者占比 SQL 类数据库语言需求更普遍。后端语言中最火的语言的分布更为离散，使用门槛更高。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/005.png)

StackOverflow 2023 编程语言统计

**2. 实现门槛低，适合模板化：**

前端工程师的准入门槛比较低，而且其对视觉交互、 SEO 都有直接影响，会和用户留存这样的业务数据紧密挂钩。同时，与视觉元素的强相关使人类可以更快速给出 human feedback，就像 MidJourney 收集用户反馈比 ChatGPT 要容易很多。因此和设计场景的 Canva 类似，web 开发有很多可以复用的代码框架和网站搭建的模板可用。

相比之下后端开发的难度更大：简单的后端开发与运维系统已经有云厂商产品化和 commoditize 了，而复杂高阶的后端开发则涉及每家公司的核心业务逻辑， 自建是更普遍的选择。

**3. Gen AI 时代会带来 web application 的文艺复兴：**

互联网有着更深的知识密度，更开放的分享调用生态，web 的地位在欧美市场尤其高。这也是为什么如今 AI 浏览器、AI 搜索重新成为一个创业的热点，web 生态为 [AI agent](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504973&idx=1&sn=603596db2a31e1e53d71ac05d775cb7c&chksm=ce9b6bd3f9ece2c577720045239314840757fa578587f4a5adbf21e18a9dadd6bf1af3913b61&scene=21#wechat_redirect) 提供了学习知识并进行 grounding 的环境。

当前 ChatGPT 这样 Chatbot 形式还比较基础，未来的 AI agent 会需要响应快的动态 UI 来给用户实时展现 agent 行为的关键过程，未来前端技术栈和 AI 前沿产品形态将一起持续演进。

**Next.js：前端技术栈发展的后起之秀**

前端开发的历史始于 1990 年代早期，当时的网页主要由 HTML 构成。这些网页是静态的，用户交互性极低，HTML 为网页提供了骨架。

但只有一个骨架是不够的，CSS 和 JavaScript 的引入使得网页变得更加动态和富有交互性：

• CSS 允许开发者将网页表现层（如字体、颜色、布局等）与网页内容层（HTML 语言负责）分离。

• JavaScript 则比 HTML 和 CSS 出现得更晚一些，它为网页添加了交互性，使其能够响应用户操作。

同时，随着 web 应用的复杂度增加，开始有了前端和后端的清晰分工：前端开发则专注于用户界面和用户体验，负责将后端返回的数据以视觉友好的方式展示给用户；后端开发主要关注服务器、数据库和应用程序逻辑，负责处理来自前端的请求，并返回所需的数据。这样的分工下前端开发者可以更专注地投入到用户界面和交互体验的优化中，不必同时担心服务器的性能和负载。

随着 JavaScript 成为 web 开发中最关键的编程语言，web application 的复杂度还在提高，仅使用原生 JavaScript 来管理大型项目的用户界面会变得非常困难。这就是为什么需要像 React、Vue 这样的库（library）。它们就像是搭积木的模具，有了这些模具，开发者可以更快速、更标准化地搭建出高性能的应用程序。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/006.png)

Javascript 已经成为 98% web application 使用的语言

其中 React 是由 Facebook 团队开发的开源 JavaScript library，用于构建用户界面，特别是单页应用程序。它的出现极大地改变了前端开发的方式，使得开发复杂的动态网页应用变得更加简单和高效。它很好地提高了 Javascript 代码的可维护性和重用性，成为 Javascript 语言使用最多的框架。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/007.png)

React 成为最火的 Javascript 库

而 React 也不能满足所有现在网页开发需求，在其之上有进一步优化的框架。其中 Next.js 是最近几年增长最快的框架。它的开发者就是 Vercel CEO Guillermo Rauch，一个传奇的开源开发者。Next.js 在 React 框架中的下载量远超其他框架，并且仍在稳步增长：

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/008.png)

图中的 Gatsby 和 Remix 均为 Next 的直接竞争对手。Gatsby 是 Vercel 竞对 Netlify 收购的框架，从数据看这次收购并不成功

Next.js 的流行背后是其技术选型更适合现代 web 开发需求：

1. 支持服务端渲染(SSR)和静态站点生成(SSG)，实现更快的内容加载和更好的 SEO；

2. 内置功能丰富，如自动代码拆分、强大的路由功能和图像优化，简化了复杂应用的开发；

3. 优先考虑开发者体验，提供直观高效的开发流程，如 TypeScript 支持和代码热重载；‍

总结一下，JavaScript、React 和 Next.js 之间的关系可以概括为：JavaScript 是构建 Web 应用的基础；React 在此基础上提供了一种高效的方式来构建用户界面；而 Next.js 则在 React 的基础上增加了服务器渲染、路由处理等功能，使得构建现代 Web 应用变得更加高效和强大。

**02.**

**Generative UI: Gen AI x Web development**

自 ChatGPT 问世开始，大家对下一代人机交互的形式有很多想象，尤其是 Language UI 和 Graphic UI 结合成为了焦点话题。实现交互创新的前置条件是什么呢？

在之前的 Agent 综述文章中，我们提到过随着 coding AI 的发展，软件开发将进入一个新的自适应生产阶段（adaptive software）。就像 3D 打印技术一样，软件将根据用户的具体需求自动生成相应的UI组件。

而打造 Next.js 的 Vercel 团队打造了 V0：第一个能生成 production-ready 水平前端代码的生成模型。

**Vercel V0**

Vercel V0 是一个代码生成模型，能让用户生成网页 demo 和代码，代码能直接够部署成为一个基础版网页，也在其产品 demo 上进行进一步修改。每次生成之后，v0 类似 MidJourney 会给 3 个版本 AI 生成的 UI，可以选择一个进行深入编辑，甚至粘贴到自己原本的项目中进一步开发。

例如我可以先要求 V0 生成一个 Saas dashboard 布局作为底稿（V0 名字的来源，version 0），再在其基础上进行交互。demo 中的每一个组件都是可以单独点击并进行修改的，例如，下图中可以让 V0 将 logo 改成蓝色，模型就会直接进行对应组件。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/009.png)

V0 的使用体验充分展现了前端代码模型的**可编码性**，这带来了网页生成远大于图片生成的**可控性**。其中的每一个组件都对应着具体的几行代码，如果我们要求对某个组件进行修改的话，这几行代码就可以重新生成，并用其他代码作为上下文，保证新生成代码有着很高的可用性，能直接融入原本的代码。

这些能力已经对所有开发者开放，且已经被不少新团队用于自己的产品开发中：Ingo 使用 v0 构建了他们的简历生成器产品的第一个版本。Braintrust ，一个新的 AI 平台，使用 v0 构建了其定价页面。以下 gallery 中都是用户使用 prompt 对应生成的网页和前端组件：

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/010.png)

对比现在的大多 coding model 不是在做 Github Copilot 那样的代码自动补全，就是仍在不可用的 demo 阶段。Vercel V0 在可用性上比其他模型强很多，其团队对前端代码的深刻理解是其中的重要原因：

• V0 模型的训练数据有三部分：团队自己积累写的 code、开源前端代码和 AI 合成数据。每次生成之后，v0 类似 MidJourney 会给3个版本 AI 生成的 UI，可以形成优秀的 RLHF 反馈闭环。

• Vercel 作为用户做网页开发的 go-to 选项，有足够多的用户web开发数据积累，有高质量模板和代码库。而且团队自己本身是设计 Next.js framework出身，有 know-how 定义什么是从语言设计出发的高质量代码。

v0 的野心是下一代用户界面的起点。Vercel 团队蓝图中的下一步有：**支持自定义设计、多模态识别将图像转化为代码**，以及更强的代码安全和访问控制。这些路线图很清晰，会有效地提升开发者体验。

**AI SDK**

AI SDK 是 Vercel 为前端开发者设计的 Model Router。它提供了一个抽象层，让开发者可以用自己熟悉的前端语言来处理数据，而不需要关心各类 LLM api 实现细节。

他们 SDK 第一批合作者接入了 Perplexity、11 Labs、Pinecone、Together 等公司。如果开发者要在 next.js 框架中使用 Perplexity API ，只需要一小段代码就可以融入前端中，输入一些基础的参数就可以产生出高质量的 streaming response 交互。这样的开发方式对于前端程序员而言更 intuitive：

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/011.png)

而 AI SDK 3.0 是其最近的一版更新，接入了 Vercel V0 使用户可以轻松地做出带有 Generative UI 的产品。 Vercel 在这里给出了一个股票咨询助手的案例，我们以这个 demo 为例：那么当我们要求它给出苹果最近的股价并进行购买时，它就能直接给出对应的 UI，给我们展示苹果股价，并生成实时购买功能。这是一种优雅的方式实现 Language UI + Graphic UI 的结合。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/012.png)

目前这个产品还在 demo 阶段，而且 demo 本身展现的能力过于高频，因为股票交易是一个非常常见可复用的操作。但随着这一能力后续可用之后，可以满足很多用户使用 app 时的长尾需求，能够在一个应用中生成出新定义的小程序来满足一些 ad-hoc 需求。

这一技术有两个关键要点：

• API 设计时要以发挥 LLM 强大的 function calling 能力为出发点，让用户尽可能感受到 LLM 的全面性和智能度。

• 发挥 React Server Components 对每个模块组件进行渲染的能力，使用户进行颗粒度更细、性能更优的交互。

为达到这些目标 AI SDK 中引入了两个独立的状态：AI State 和 UI State：

AI State 是一个 JSON 格式的文字，包含了大型语言模型（LLM）需要读取的所有上下文。对于聊天应用来说，AI State 通常存储用户和助手之间的文本会话历史。还可以用来存储每条消息的创建时间等其他 metadata。AI State 可以在服务器和客户端上被访问和修改。

UI State 是应用程序用来展示 UI 的状态，它完全在客户端（类似于 React的 useState）。它可以保留 LLM 返回的数据和 UI 元素。这个状态可以是任何内容，但不能在服务器上访问。

从技术文档来看，AI SDK 的设计有效兼顾了应用开发者的性能需求和用户的数据安全需求。期待这一能力为开发者使用之后涌现出更多的 use case，来验证这一开发者接口的 PMF。

**03.**

**Frontend Cloud：最好的 AI-native 产品部署平台**

上一部分介绍了 Vercel 团队最新在 Gen AI 前沿的实践，那么他们在 Next.js 之后，Generative UI 之前所做的产品究竟是什么呢？

Vercel 把自己的主产品定义为 frontend cloud，是一个易用、且 scalable 的 web application 部署平台。其高性能建立在几个重要的技术趋势之上：JAMstack、边缘计算和 serverless 设计。尤其 Serverless 设计允许开发者在无需管理底层服务器的情况下运行和构建 Web 应用，帮助用户能够省去很多冗杂的 Infra 部署工作。

Vercel 产品根据前端工作流可以拆解为 4 个关键部分：(1) develop，(2) preview，(3) ship，(4) analytics。

**• Develop:** Vercel 为开发者提供了一个快速将 web application 实现的 workflow。让开发者可以从 Github 等源头导入前端项目模板，并集成 MongoDB 等外部数据源。在代码开发完成后，Vercel 还提供了从缓存到 serverless functions 的端到端测试。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/013.png)

**• Preview:** 这一部分产品可以类比为前端开发的 Figma。设计、开发和运维团队可以摆脱复杂的测试管线，在每次部署之前协作测试他们对网站的更改。Vercel 会自动生成一个可分享的实时预览站点，允许在网页 demo 在上线前进行测试，团队间互相 comment 给反馈。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/014.png)

**• Ship:** Vercel 基于对 Next.js 的原生支持， serverless 和 edge computing 的能力为开发者提供快捷的部署、稳定的性能，和对 SEO 的支持。同时他们允许在全球范围内部署网站，并在300毫秒内进行修改更新。这项功能直接和开发者/付费的 value prop 相关，后续会在 business model 处介绍。

**• Analytics:** 2022年10月，Vercel 宣布 收购了 Splitbee，这是一个分析和运营工具，可以了解用户的网站体验。该产品和团队被纳入 Vercel 现有的分析产品。由于 Vercel 负责管理网站，因此他们旗下的分析平台不需要第三方脚本或 cookie 跟踪。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/015.png)

以上这些产品让 Vercel 成为市场上开发者体验最好的 web 部署平台。不过前面提到过，web 市场集中度不高，所以 Vercel 在存量客户中并没有因为优秀的开发者体验，而成为大幅领先的第一名，而是小幅领先 Netlify、云厂商等公司。

因此抓住增量机会就至关重要。在 ChatGPT 发布一个月之后，Vercel 就开始成为 AI-native 应用开发的布道者，通过博客和模板的形式引导大家最快地使用  Vercel 来快速迭代开发 AI 应用。

而在今年初，Vercel 产品定位进一步清晰：最好的 AI 产品部署平台。由于他们出色的产品开发体验，已经有很多公司使用 Next.js + Vercel 开发了自己的主力 AI 应用：

• Scale AI 强调通过使用  Vercel 和 Next.js 让他们在团队中只有三个设计师的情况下很快地迭代和部署了自己的 Generative data engine；

• Anthropic 工程师用 Vercel + Next.js 开发了 Claude AI 的 web 产品，团队中有人是第一次开发 Next.js 代码，表示其易上手且开发体验很棒；

• Runway 称赞 Vercel 让团队加快整个产品开发周期。比如团队成员称迁移到 Vercel 后，DNS 构建从 Netlify + GitHub Pages 的 5-8 分钟缩短到 Vercel 的 40 秒；

• Jasper 用 Next.js 框架 + Vercel 部署，尤其强调网页中的 content management (posts, tweets, short stories 等)体验很好。

此外，Replicate、发布 Devin 的 Cognition 等一众 AI-native 公司都使用 Vercel 开发部署了自己的主力产品。我们有理由相信随着模型升级、应用爆发，Vercel 能成为 web development 中重要的受益者。

**04.**

**市场与商业化**

**Business Model**

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/016.png)

Vercel 主产品采用 freemium 的商业模式，他们有三个主要的定价梯度:

**1. Hobby:**这个方案用于吸引客户来试用平台，其 offering 对搭建比较少小流量网站的个人开发者也够用，有一定的公共品属性；‍

**2. Pro:**prosumer 用户每月20美元的订阅服务，这是他们对中小开发者的核心付费产品，按 seat 收费；‍

**3. Enterprise:**这是为大型企业提供的定制解决方案和定价，具体价格不公开，但他们为企业提供更多网络安全功能和更快的速度。根据客户访谈，企业客户平均一年的费用在十万美金级别，最大的可以到百万美金量级。

V0 向用户全量开放后成为了单独定价的模型产品，其定价和主产品基本一致：

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/017.png)

70% 的 Vercel 用户是 Next.js 用户。当更多开发者使用 Next.js 时，Vercel 的增长也会加速。从 2020 年 4 月到 2023 年 5 月，由 Next.js 驱动的网站数量已经从 3.5 万个增长到 400 万个，包括 Walmart, Apple, Nike, Netflix, TikTok, Uber, Lyft, Starbucks 等公司的网站。

优秀的 traction 让 Vercel 的商业化收入一直在高速增长的状态：2020 年成立的第一年，ARR 为 1mil USD；21 年达到 5 mil USD，22 年达到 25mil USD。在这一年他们以 100 倍 ARR，也就是 $2.5b 的估值进行了一轮融资。而在 2023 年，他们还是以 100%+ YoY 的高速增长，创始人在一次 23 年 6 月的访谈中公开提到他们的 ARR 已经达到 $ 50+ mil。

**用户画像与市场竞争**

在整个 web 市场中，33% 的流量集中在最顶尖公司产品上：Google、Meta、Amazon 等，33% 的流量集中在第 10 名-第 10000 名的腰部 web 产品，最后 33% 则是独立开发者开发的网站。

其中前十名的公司有自己非常成熟的 tech stack，完全自研；最后这部分用户很多对开发的了解甚少，可能会选择 Shopify、Squarespace 这样的网页模板产品。而 Vercel 目前客户的基本盘主要来自腰部的 web developer。

Vercel 主要的客户目前可以分为几类：

• 业余爱好者：免费用户，托管单一网站，未来可能会将其带到公司使用。

• 小型初创公司及中型公司（认为这是 customer base 的一大部分；这些公司可能拥有有限的开发团队，或只有市场营销部门）。

• 电商团队这样需要 SEO 带来转化，付费意愿强的客户在 Vercel 付费客户中占比比较大。

创业公司中 Netlify 是 Vercel 最直接的竞争对手，这是一家 2014 年成立的公司。2021年，Vercel 通过 D 轮融资筹集了 1.5 亿美元，估值达到 25 亿美元；同时，Netlify 通过 D 轮融资筹集了 1.05 亿美元，估值达到 20 亿美元，a16z 是他们的主要投资人之一，据了解，公司最新的 ARR 已经超过了 30 mil USD。

Netlify 提供的也是一个 Jamstack 开发平台，包括 Web 应用程序和动态网站的构建、部署和无服务器后端服务。但他们的产品没有 Vercel 那么 Next.js 友好，同时对 Gatsby 的收购也并不成功（伴随着 Gatsby 的 traction 逐渐下滑）。他们团队对 Gen AI 这一波 catch up 的速度就要慢不少。

而大公司中，云厂商都有 Web Development 产品。AWS Amplify 是云厂商中口碑最好的，不过用户的反映普遍是定价比较有优势，但开发者体验仍不如 Vercel。此外大家使用 ChatGPT、Perplexity 等产品时经常遇到的 Cloudflare，也从其云安全产品延伸出了 Cloudflare 这个网页开发工具，和云厂商类似的是用户选择的原因是与原本选用方案的耦合度比较深，不需要上手新平台。

**05.**

**Guillermo Rauch：从开源开发者到 CEO**

介绍到这里，Vercel 团队展现出了几个重要的特点：

• 开发 Next.js 时对前端技术的前瞻性，引领最前沿趋势；

• 对 Gen AI 前沿趋势敏锐且活跃，用新产品线抓住增量用户；

• 产品中对开发者体验的极致优化，带来优秀的用户反馈；

• 从开源到商业化的高速增长。

这背后离不开 Vercel CEO Guillermo Rauch 对产品 PMF 的持续追求、优秀的技术品味和极强的执行力。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/018.png)

Guillermo Rauch 在阿根廷布宜诺斯艾利斯比较落后的郊区出生长大。父亲对计算机的兴趣让 Guillermo 在 7 岁获得了自己的第一台电脑，从小种下了对编程、对开源热爱的种子。第一个任务便是父亲让他将 Windows 的系统替换成 Linux，之后便一发不可收拾地在开源社区自学编程和英语，十一二岁在开源社区成为 celebrity。后来有陌生人在网上对 Guillermo 说你可以用这方面的 expertise 建立事业，Facebook 也抛出橄榄枝想要招聘他，让他意识到自己的 passion 和事业成就是完全能够自洽的，更是从高中辍学到美国工作、创业。

这种特殊的成长经历让他天然更在意商业化和业务规模。相比很多技术小天才类型的 founder 喜欢做开源“玩具”，Guillermo 是希望让产品有更高的商业认可度的。

他创办的第一家公司 CloudUp 是一个云端文件存储与分享平台，CloudUp 其实就已经有了一部分 Vercel 的雏形，这款产品在当时的 killing feature 是拖放文件夹即可迅速创建超链接，便于在线分享文件和协作，若文件为 HTML 格式，还能获得高性能的静态网站托管。这满足了 WordPress 在实时协作的需求，于是Guillermo 将 CloudUp 卖给 WordPress 实现了第一次成功退出、并加入了 WordPress，Guillermo 在 WordPress 的两年间学到很多关于如何平衡开源项目和大规模商业运作的经验。

Guillermo 来到湾区的时间让他恰好成为 AWS 的第一批用户，他由此认识到了云服务价值，于此同时也认为其易用性很糟糕。加上 React 越来越流行，但同样难以快速上手，且开发者需要自己管理和维护服务器，他作为一个经验丰富的开发者在开发网站时也深受困扰。在市场需求端，Guillermo 也由此想到那些正在经历数字化转型的传统零售在从线下实体转型中如果要和 Amazon、 “.com” 的竞争必然面临更大的挑战。Next.js 和 ZEIT 由此应运而生，在 2020 年 A 轮融资时，公司更名为 Vercel 。

Vercel 和 Next.js 成功的背后是设计原则和工程实践的精细打磨。在正式创立 Vercel 之前，Guillermo 列出了 Web 应用开发的七项原则，底层的 philosophy 是必须 at big scale, at global scale，并且这七项原则的背后是 Guillermo 反向工程 Google、Amazon 等全球最大的网站的结果，这就为 Next.js  设定了一个很高的标准。而在发布 Next.js 之后，最重要的权衡就是如何兼具开发者体验与企业级应用的性能和可靠性。作为 dev tool，Next.js 必须提供出色的开发者体验；而作为支撑企业级应用的基础设施，它又必须兼顾业务上的高 ROI 和终端用户体验。这在当时被许多人认为是不可调和的 tradeoff。而 Guillermo 坚持在这个 spectrum 中两头都要抓，为其产品后来获得企业和开发者认同奠定基础。

在从 Next.js 开源框架专做商业化产品之后，Vercel 的高速增长获得了投资人的追捧，两年间融资 3 亿美金左右：

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/019.png)

这一波 Gen AI 的趋势中，Guillermo 又对 Software 2.0 做了许多预言。他认为，随着 AI 技术从 paper-first 渐渐变为 product-first，软件开发也将从 backend-first 转为 frontend-first。我们非常认同这个判断，且期待看到这波机会中 Vercel 在这个千亿美金的市场中将领先的开发者 mindshare 转化为持续的产品和商业化增长。

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/020.png)

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/021.jpg)

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/022.jpg)

延伸阅读

[![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/023.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507057&idx=1&sn=fe134fc24736727fb9d2ba921d2e98ef&chksm=ce9b63eff9eceaf9e080f4e98a592f1f92d0a40b259c40224e6fa8757f36a7019f5828435eb5&scene=21#wechat_redirect)

红杉美国：GenAI是一场10倍速的生产力革命

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/024.png)

[![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/025.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247506900&idx=1&sn=543867a300f4c5372de921168ae5985e&chksm=ce9b644af9eced5c112af69fd2269eadb8d3e6011dcfc87f8e0feb1de79e559e2361e5c0d45d&scene=21#wechat_redirect)

AI重塑法律行业：为80%的工作带来10x提升

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/026.png)

[![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/027.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247506441&idx=1&sn=e1139bea284a7a9ef3187315924d133f&chksm=ce9b6597f9ecec81bc1a02868fbadeb8fc47c65f0feffcf3d4cb2f56e7f5325bf8a9b883a9a4&scene=21#wechat_redirect)

Sora的算力数学题

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/028.png)

[![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/029.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247506393&idx=1&sn=ef1862fcb85381e96a8a61aed367082b&chksm=ce9b6647f9ecef51b33084d26051ed97ae405c2b421278a8bf3d8c0a080e308c9b7e84a118f0&scene=21#wechat_redirect)

Notion CEO：为什么RAG会彻底改变知识型工作？

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/030.png)

[![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/031.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247506357&idx=1&sn=c3689ef7f01b3419e25cc7f9ca933bc0&chksm=ce9b662bf9ecef3d755e82e65904d9b2c862a0b6c4c0ce24cf16728b72b85bb7ab7703c6db7f&scene=21#wechat_redirect)

我们距离AGI还有多远？

![](../images/2024-04-02-vercel-yong-sheng-cheng-shi-uizhong-su-qian-duan-kai-fa/032.png)
