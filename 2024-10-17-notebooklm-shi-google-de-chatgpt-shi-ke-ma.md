---
title: NotebookLM 是 Google 的 ChatGPT 时刻吗？
publish_date: '2024-10-17'
publish_timestamp: 1729166400
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/EUhHcekY4vMN0HH2_7_eqA
msgid: 1000000294
appmsgid: 2247509981
itemidx: 1
digest: 如何打造一款 AI-native 产品
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgyXFmfO6GMbrku5NOTZA8XX56fuhmicyqxicBs1aqDOumcLpgmic3OdF6xvLibgtBwmPfnN8QeYYmgz3g/0?wx_fmt=jpeg
image_count: 18
archived_at: '2026-04-20T02:43:46+08:00'
---

[![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/001.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&chksm=ce9b60bbf9ece9ad6b7028fd2aa90e43dba20a6a92f9202cdd88b806dd9a18f3e0e17ce7e8e1&scene=21#wechat_redirect)

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/002.png)

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/003.jpg)

编译：牛佳晨

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/004.png)

并不擅长 to C 产品的 Google 推出的 NotebookLM 在近期刷了屏，Andrej Karpathy 称 NotebookLM 让他想起了 “ChatGPT 时刻”，Sam Altman 也公开表示，“NotebookLM 很酷”。

NotebookLM 的前身是 Project Tailwind，最初是 Google 推出的一款实验性的 AI 工具。它允许用户上传多种格式的文件，随后用户可以用对话的方式和这些文档进行交互，而近期推出音频总结更是能将 AI 对文档总结生成播客，让用户用“听内容”的方式获取信息，最终引起了产品的病毒式传播。从一个“20% 项目”快速增长到拥有 6 万 Discord 社群成员的现象级产品。‍‍‍‍‍

本篇内容是红杉美国的 Pat Grady 和 Sonya Huang对 NotebookLM 的核心开发团队成员的访谈。其中，Raiza Martin 是 NotebookLM 的产品负责人，而 Jason Spielman 是技术负责人。

团队成员除了讨论 NotebookLM 的诞生背景、关键技术原理外，也分享了他们观察到的 NotebookLM 的 一系列 use case。关于如何打造一款 AI- native 产品，NotebookLM 团队也有着有趣的理解：

1）上下文是 LLM 交互的一个重要特点，只有基于上下文才能创造粘性极高的用户体验；

2）今天 AI 应用的开发处于“拟物化”的阶段，和 iOS 早期一样，这是因为还有大量用户才刚开始接触到 AI，开发者需要通过用户熟悉交互或者场景来让他们习惯和 AI 互动；‍

3）Claude Artifacts 的动态 UI 也许是 AI 交互的未来形态之一。

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/005.png)

**💡**目录 **💡**

    01 NotebookLM 是 Google 的   

         ChatGPT 时刻吗

    02 NotebookLM 的用例 

    03 如何设计出好的 AI-native 产品

    04 NotebookLM 的未来

**01.**

**NotebookLM****是**

**Google 的 ChatGPT 时刻吗？**

**Sonya Huang:****虽然 NotebookLM 只是一个实验性的尝试，但它很快就形成了病毒式传播。所以大家都把 NotebookLM 看作是 Google 的 ChatGPT 时刻，你们怎么看这个观点？**

**Raiza Martin:**对我来说，把 NotebookLM 比成 ChatGPT 时刻可能太大了，但我也看到很多人通过项目感受到原来 AI 是这样的、也体会到了 AI 的能力，从这个层面上，NotebookLM 和 ChatGPT 带来的影响可能是类似的。

**Jason Spielman:**我在第一次听 Audio Overview 的时候，随着第二个主持人声音的出现、音频总结变成了一个播客的时候真的是一种令人震惊的体验。但我认为，更本质上，Gemini 1.5 Pro 很好地处理这些复杂文本，并以相当简洁的方式呈现出来，这一点也很重要。所以对我来说，语言模型和声音的结合确实是一个很重要的时刻。

**Sonya Huang:****你们自己会怎么定义 NotebookLM？**

**Raiza Martin:****Notebook 是一个 AI 驱动的研究和写作工具，今天很多人可能会把它用来将某个内容生成语音总结或者 Podcast。**

**Sonya Huang:** **作为一个 Killer App，Notebook 是怎么诞生的？是偶然还是刻意设计的结果？**

**Raiza Martin:** 我们一直在研究多模态的生成和输出，我认为声音是下一个重要方向，在这个基础上我们选择了对话的形式。Notebook 发布之前我们并不知道它会成为一个所谓的 Killer app，我们只是觉得它的体验会让人感到很新奇，但从结果来看人们和这个产品的交互体验比我们想象中更惊人。

去年我们一直在做 AI Test Kitchen 这个项目，Notebook 最初可能只是一个完成度只有 20% 的项目。当时我们团队中有一位工程师在开发一个叫做“talk to small corpus”，我一开始并不理解这个项目，但后来我和他交流时，他解释说，这个项目的核心思想是利用 LLM 和自己的数据对话，从而从中提取有用信息。当时我就觉得这个想法很有趣。

💡

**AI Test Kitchen** 是 Google 在 2022 年推出的一个实验性平台，最初在 Google 的 I/O 开发者大会上亮相，目的是共同负责任地学习、改进和创新 AI。AI Test Kitchen 提供了多种交互式实验，让用户能够体验到最新的 AI 技术，例如使用 LaMDA 对话模型，用 MusicFX 生成音乐，或者通过 ImageFX 将文字转化为图像等等，平台也允许用户提交反馈。

也由此我会继续想这项技术具体能有哪些应用场景。作为一名成人学习者，我突然意识到，如果我能利用 LLM 与教科书进行对话，那将会是一件很有意义的事情。我能想象到这项技术不仅可能改变我的生活，还可能改变许多人的生活。

从那时起，我们就开始着手考虑如何打造这项技术的第一个版本，并将其介绍给大众。去年 5 月，我们推出了 Project Tailwind，这个项目就是这个想法的具体实现。用户可以上传一个 PDF 文件作为信息源，然后与之进行对话交流。

**Jason Spielman:** 我认为 NotebookLM 最独特的地方在于它是基于源文档的（source-grounded）。在开始做这个项目时，我都没意识到我们日常创造的每样东西，往往都是基于某些已有的资料或文档。所以目前来说，我会把它称为一个基于源文档的工具。但实际上，它正在发展成为一个用于创作和其他多种用途的源文档工具。

**Sonya Huang:****Notebook 的播客和音频总结的体验确实很神奇，背后的技术原理是什么？比如，为什么它听起来如此逼真的？生成的对话是怎么做到能吸引听众的？**

**Raiza Martin:**首先，这绝对是团队协作的成果。其次，能实现这些体验的核心还是得益于 Google 强大的模型能力。最关键的是 Gemini 1.5 模型，它能够处理用户输入到 NotebookLM 的所有数据，并在此基础上生成全新的内容。NotebookLM 的音频功能也是基于 Google 的语音模型实现的。这些不同模型的结合最终造就了 Notebook 的独特体验。当然，除了模型本身的能力外，我们团队在如何有效利用这些模型方面也下了不少功夫。

在 Gemini 1.5 和音频模型之间还有一个很关键的组件是一个叫做 Content Studio 的工具。**Content Studio 在用户提供的内容源到最终生成的播客的过程中扮演了内容编辑的角色。基于 Content Studio ，Notebook 在生成内容的过程中拥有了某种程度上的“创作空间”。**

**Sonya Huang:** **你们是否考虑在未来把 Studio 这个功能开放给用户？比如让用户可以自己调整内容，让内容更有趣一些，或者更正式一些？**

**Raiza Martin:** 现在使用 Notebook 的用户很多，对于我们来说下一步就是让用户有更多可控性，让他们可以自己来调整生产的内容。其实一开始我听到这些需求我会直觉性地反应说：“好，那就把这些调节选项加上吧”。但我现在在尝试更加谨慎地思考这个问题。大家喜欢上这个功能是因为它让人感到惊喜。那么，我们怎样才能在保持这种惊喜和魔力的同时，还能给用户一些可控性？

**Jason Spielman:** 我认为 NoteLM 音频总结功能爆发式增长的部分原因就在于它是一个简单的一键式体验。我之前在电话里向我奶奶解释如何使用这个功能，结果发现根本不需要解释。我只要告诉她“把资料导入进去”，她就回答“我看到了，然后点这个按钮就能生成是吧”？我觉得正是这种创建的简易性真正催化了 Notebook 的爆发式增长。所以，在考虑增加一些可控性的选项时，我们会很谨慎地去做这件事，保持这种产品简单易用的特性。

**Pat Grady:**  **今天几乎所有 AI 产品都还在围绕对话框来展开，你们是怎么想到让用户“听内容”这件事的？为什么人们会想要通过听播客的形式来了解某些信息？**

**Raiza Martin:** 这件事来自 Jason 之前提到的一点，那就是：我们要怎么以一种人们易于理解也易于接受的方式来呈现新的事物，让他们愿意去尝试？当我们想到可以让用户上传素材，然后生成新的语音内容时，我们就在想，到底能生成哪些语音内容呢？Google 的这个语音模型非常强大，既可以生成独白，也可以生成对话，还可以让用户来选择生成什么格式的内容。**但真正能引起人们共鸣的点在于，播客是一种对话形式，它能做的不只是把文本转成语音，让我们去听朗读的文本。我认为，一旦我们看到这种形式实际的应用，就会知道这就是我们要去做的事情。**

**02.**

**NotebookLM 的用例**

**Sonya Huang:****你们提到人们最初是冲着播客功能来的，然后因为其他功能留下来。能分享一下音频之外的好的 use case 吗？**

**Raiza Martin:** 我在前面提到过 NotebookLM 在教育场景的 use case，我看到很多学生和教育工作者在使用 NotebookLM，我觉得这件事对我个人来说很有意义。但令人惊讶的是，我发现有很多人在工作中也会使用 NotebookLM。

一个很好的例子是我们在 Google 内部试用 NotebookLM 时看到的一个 use case。Google 广告团队中有很多广告销售人员和广告专家，这些广告销售人员的销售培训和文档往往有几百页那么长，并且这些内容还会经常变化。要熟悉这些内容到能够销售的程度是很困难的。所以销售团队内部通常的做法是，或者说在有 NotebookLM 之前的做法是，互相询问。一个典型场景是，他们会提出类似这样的问题：“Joe，这个产品到底是怎么运作的？我该怎么向客户推荐？”等 Joe 回复后，他们再把回复复制粘贴到邮件里，稍作修改就发出去了。

但实际上，像 Joe 这样阅读了所有文档、掌握了大量知识的人，他们会通过 NotebookLM 创建一个文档，然后分享给其他销售人员，这样就有上百人自动开始使用这个 Notebook，也因此他们不用再去咨询 Joe 了。我觉得这件事很有趣，因为这是一个非常简单的应用场景，但在此基础上还可以开发出更多用途。

**Jason Spielman:** 我最近和一个做销售的朋友聊天，他也提到自己做了一个 Notebook，在和客户交流中遇到某些问题不清楚答案的时候，就会和这个 Notebook 对话，然后得到对应的答案。我认为这种知识分发的方式对于大规模的销售团队或数据中心来说非常有帮助。

另一个我觉得很有意思的 use case 是，很多在 VC 行业工作的人在日常工作中要看很多公司信息和对应的文件，我有位 VC 朋友说，他现在会把收到的文档或 deck 放进 Notebook 里面，从而更加快速地处理这些信息，工作效率差不多提高了 10 倍。

**03.**

**如何设计出好的 AI-native 产品？**

**Sonya Huang:** **你们在产品设计上做了哪些取舍来让 Notebook 好用且便捷？**

**Jason Spielman:** 我想先说明的是，我们到现在还是在持续不断地做这些产品层面的决策，我觉得我们现在的重点在于快速推出产品，然后通过和用户密切互动来理解什么是最好的、他们想要什么。今天模型能力迭代得很快，很难说基于模型能力再来决定做具体什么事情。

但具体来讲的话我认为我们有一个决策是做对了，就是让左侧的 Source 栏很突出。我认为我们是一个基于源文档的项目，我们需要明确表示你是在与你上传的源文档对话。所以我认为左侧的 Source 栏是这个产品的一个关键部分。另外一点就是正如我之前提到的，一键生成音频总结对于产品传播来说也很有效，我们在产品设计上整体倾向于这种简单的体验。

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/006.png)

**Raiza Martin:** 我想补充一点我们在产品层面上的考虑，特别是在产品优先级上，我们一直在思考的问题是如何让一个新事物变得很直观。要做到这一点非常困难，特别是像“首先用户必须上传一个源文档”这种细节，用户通常会对这一步产生抵触，他们可能第一反应会问“为什么？”，因为在使用 ChatGPT 或 Gemini 的时候第一步并不需要上传任何文档，直接就能用。所以我认为在“上手即用”这个方向上，我们还有很多工作要做。

**Sonya Huang:** **你认为在让人们适应这种新的 AI 原生体验时，还面临哪些最大的挑战？**

**Jason Spielman:** 我觉得今天 AI 产品设计所处的阶段可以总结为“拟物化（skeuomorphic）时代”。拟物化是指用虚拟对象来映射现实世界。在早期 iOS 中可以看到这个特点，比如 Apple 的 Note 应用顶部有皮革边框，记事本页面是黄色的，这是为了帮助用户更容易从物理世界过渡到虚拟世界。我觉得今天我们在 AI 产品上的实践也处于类似阶段，我们首先要构建一些 UI 来满足用户当下的需求。但我也想强调的是，在不断给用户创造新奇体验的同时，也要意识到，对许多用户来说，这是他们第一次与 AI 互动。

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/007.png)

**Sonya Huang:** **我认为 Midjourney 做得非常好的一点是，它很好地解决了用户不擅长提 prompt 的问题。在你看来有没有哪些 AI 应用在解决这些 UI 挑战也做得很好的？**

**Raiza Martin:** 我最近用了 Pika，我很喜欢 Pika 的效果预览功能，通过这个功能用户可以很清楚地看到上传图片后会发生什么、得到什么。在看到这些效果预览的时候我就觉得这些尝试很有趣，所以我上传了一张饮料的图片，然后选择了一个蛋糕效果，想把饮料变成蛋糕。等待饮料变成蛋糕的过程让我兴奋不已，我甚至当时就在想是不是可以付费了。所以我觉得这种效果预览不仅可以激发用户使用产品的意愿，甚至还可以驱动付费。

**Jason Spielman:** 我觉得 Claude Artifacts 做得很不错。我认为他们在代码生成方面做得非常出色。我觉得我们今天所处的阶段是怎么平衡 AI 和人类之间的关系，我们想要创建一个 AI 产品绝对不想要取代一群人的工作，而是想提供更好的支持。我之所以认为 Claude Artifacts 是一个完美的例子，就是因为我们在和 AI 交流的同时，它就已经在开始按照我们的交流去构建一些东西了。

**Sonya Huang:** **在你看来，NotebookLM 的产品思路和 Claude 相比是有哪些异同？**

**Jason Spielman:** 首先，我们和 Claude 最根本的不同是我们还是围绕一个特定文档来展开交互的工具（source-grounded tool）。

**Raiza Martin:** 围绕这一点来说的话，**LLM 交互中围绕上下文展开是一个很重要的特点，我觉得也正是因为上下文的存在才能创造粘性极高的用户体验。**Anthropic、OpenAI 以及 Google 等所有参与 LLM 研究的人肯定都知道这一点，但**我认为关键在于在什么时候引入这个特点，以及基于什么样的交互界面？**

这也是我对于 NotebookLM 感到兴奋的原因。因为我们从一开始就突出了上下文交互这一点。当用户意识到 source-grounded 的重要性时，就会发现 NotebookLM 会是他们在寻找的工具。所以我们当下也会更专注于这一点，在其它 LLM 工具还在专注其它 use case 时，我们会在这个方向上先走得更远。

**Sonya Huang:** **你之前提到 Chat 是 AI 产品设计中的一种拟物化交互界面，NotebookLM 现阶段在尝试更前沿的方式，这种形态可能会是什么样子？**

**Jason Spielman:** 我个人对动态 UI 很感兴趣，Claude Artifacts 就是一个动态 UI 例子。但总体上我觉得我们目前还处于一个探索阶段，但考虑到用户是不是也能很好理解 AI 产品的意图，我们能做的事情是比较有限的。所以现在我们要平衡这种 AI 带来的无限可能和面前的有限需求。

**Raiza Martin:** 我会更多地考虑倾向于新的模式。我自己做了很多原型设计，也实验了很多自己的行为。我最喜欢的一个尝试是我可以边走边和我的 LLM 交谈，或者说和一整个 AI 生态系统进行交互。

我个人最近最喜欢的例子之一是，我开始通过这种方式来“写”日记。不是我自己来写，而是通过来回对话，让 LLM 为我创建一个日志，然后基于这个日志来形成一个可视化的内容，呈现的信息大致是，这周我不开心的天数比开心的天数多，哪些是让我开心的事情，哪些是让我不开心的事情。我认为在交互中会产生更多丰富的内容。

我们现在尝试的这种基于一个特定源文档的 AI 有一些非常实用的 use case，主要集中在工作和学习场景。但个人用例也非常吸引人，所以我在思考如何把我的这些个人产品实践的经验带回到 NotebookLM 中，也许是在 Mobile App 里。

**04.**

**NotebookLM 的未来**

**Sonya Huang:** **关于 NotebookLM 的增长有哪些可以分享的？**

**Raiza Martin:** 我可以简单分享一些情况。在推出音频总结功能之前，NotebookLM 的增长一直比较平稳，但自从推出这项功能后，产品的增长速度就迅速加快了。所以音频总结成了吸引用户尝试我们产品的一个非常好的切入点。**另外值得一提的是，虽然用户最初是被音频总结吸引来的，但他们往往会因为其他功能而继续使用我们的产品。这个现象很有意思，它让我们看到用户到底想从 Notebook 这样的工具中获得什么。**

**Pat Grady:****你们往前推进这个项目的思路很像一家创业公司，团队足够精简、和用户交互足够多、产品快速迭代。这和大家印象中 Google 做事情的方式不太一样。加入 Google 对你们做 NotebookLM 有什么帮助吗？**

**Raiza Martin:** Google 做得比较好、也比较特别的两点是，首先，在模型完善之前，我们就能接触到它们，提前了解计划推出的功能，这能帮我们从不同的角度去思考该如何开发产品，从而可以更好地去规划该怎么完善产品的整个开发流程。其次，我们团队里的人都非常聪明，很有才华，也很善于合作，而且都很希望能打造出好的产品。

所以，作为产品的开发者，能够同时集齐这两大要素，就很幸运了，之后只需要去执行交付就可以了。只要继续做下去，就一定能做出有意思的产品。

我觉得，我们做的一件打破常规的事是，我们最在意的是先把产品做出来。因为我之前在 Google 工作过，我经常会想这样做会不会产生这样那样的影响什么的，要考虑的事情太多了，但其实一旦我们的目标是推出产品，就必须不惜一切代价去实现它。

**Jason Spielman:** 现在很多人会误以为 Google 做事情很慢。但是我在 Google 工作的 7 年里，我其实发现事情推进得非常快。有些团队的规模很大，他们每天影响的用户能有几个亿，所以会在决策上更加审慎。我们团队现在其实是处在一个最好的位置，既拥有大公司拥有的规模和数据优势，但也足够精简，我们团队大概有 10 人左右，所以我们的速度也会很快。

**Sonya Huang:** **你们对 NotebookLM 下一步的规划是什么？**

**Raiza Martin：** 说实话，就是继续往下开发 NotebookLM。我们希望用户体验能更好，能让他们真的把 NotebookLM 用起来，让人们愿意留下来继续用它。

**Pat Grady:** **你们觉得现阶段 NotebookLM 还有哪些是没做到的？**

**Raiza Martin:** 如果我能回到过去，在发布之前多设计一些功能，我想要在产品层面实现更好的内容分享。我在刷 X 的时候会常常看到有一部分人为了呈现 NotebookLM 使用了一些视频或可视化工具，而不是最原生的 NotebookLM 的界面，我就觉得自己错过了这部分用户，因为他们去用了别的平台。所以，对我来说，**NotebookLM 缺的是音频总结的分享和协作功能。**

**Jason Spielman:** 我比较期待能增加写作功能。比如很多人都会做 Q&A 调查，然后基于 Q&A 收集到的答案来完成新的内容创作，所以我很期待能让 NotebookLM 参与到用户创造内容的整个过程里。

**Sonya Huang:** **NotebookLM 生成的内容质量确实高，对我来说，甚至已经可以取代人类做的播客了。但为什么你们会认为现在 NotebookLM 做得还不够好，还不能取代人类做的播客？**

**Raiza Martin:** 在我们的观察中，用户想要做成播客的内容，和很多人类做的播客内容其实并不重合。比如说，我非常喜欢 Lenny’s Podcast，但我不会想要把他的播客做成一篇文章，再重新生成新的播客去听，而是会直接听他的播客，听他对某个话题的看法是什么。

有些用户会用 NotebookLM 给他们的简历或者 LinkedIn 的个人资料页来制作音频总结，还有些初创公司的创始人会把他们公司登陆页的内容放到  NotebookLM 里，来看看他们的信息表达得是不是足够清楚。这些做法都很有意思，因为之前从来没有人会给自己的简历做播客。

**Jason Spielman:** **NotebookLM 的音频交互其实和播客是不同的媒体形态。虽然 NotebookLM 生成的音频听起来是播客，但 Raiza 举的这些例子也很好地说明了，人们会把它用在各种各样的场景中。**我觉得可以去想问什么今天社交媒体上有很多 reaction 视频。人们现在来听这期播客不仅仅是因为我们，也是因为他们想听到你们作为投资人对这个领域的看法，所以当我们在讨论播客的时候，不同立场、背景的人之间的讨论互动也是要考虑到的。

**Raiza Martin:** 关于这一点我想分享一个很有意思的点。虽然很多用户都在分享他们生成的音频总结，但这个东西其实是很私人的。就像我做了个人简历的播客，但其实我并不是为了让其他人来听我的简历。还有人在 TikTok 上上传了她从 2004 年开始写的日记，像这种事情如果做成播客一起听，肯定很有意思，但是对她来说，有意思的是她自己写的日记可以被转成音频的过程，她可能也不会专门去听同类型的播客。

我最喜欢的一个 use case 是，最近有人说，周末的时候他们的大学群里突然因为某件事大家聊了很多内容，不过他们并没有选择在当时去读这些消息，而是把它们全部复制粘贴到一个文档中，放到周一早上开车上班的时候听，我觉得这真的很棒，个性化生成就是这样的。

**Sonya Huang:** **今天的 NotebookLM  除了有 Podcast 这个 Killer feature 之外，还提供了一个面向很多场景应用的 horizontal 的交互的界面，你认为接下来还会做什么？是继续强化播客这个功能吗？比如有没有可能可以生成一段 YouTube 视频？**

**Raiza Martin:** 输出视频的话需要看成本什么时候能降下来。

对于我们来说，首先，我们现在想要实现的是，让用户能够导入各种类型的内容，然后用 AI 创造出新内容。播客当然是我们想要继续探索的一种输出形式，因为我们已经看到人们都很重视播客。

其次，我们也想往其他方面发展，做一些更实用的东西，因为每个人的偏好都不一样，甚至就在两三天前，还有人问我，“能输出播客确实很好，但你能让输出的代码质量更高一点吗”？这个方向也很好，但对我们来说都只是 roadmap，我们确实要想想怎么去探索输出的形式。

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/008.png)

排版：Fia

延伸阅读

[![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/009.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509858&idx=1&sn=de9e36616828fa11fc93649864521b33&chksm=ce9b18fcf9ec91ea6b75634d9eb3b2412eebe800e2b3ca01c22f7969a6ff353fd0ee113589ab&scene=21#wechat_redirect)

拾象英雄帖：寻找 AGI 同行者

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/010.png)

[![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/011.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509817&idx=1&sn=3cd92ea1fada076f1247e456bc47a578&chksm=ce9b18a7f9ec91b15438462b32d7fe7fb4dc82d22859faf28565c5c1a2267095f363db589f66&scene=21#wechat_redirect)

Chelsea Finn: RL 是如何在 Robot Learning 领域创造价值的？

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/012.png)

[![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/013.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509786&idx=1&sn=adfc2d4cfa86f4a8449fe694a78c5388&chksm=ce9b1884f9ec9192ca7a2ff46a3949c5c9a085b36521b10476db10d9d6c1853efd06fc852601&scene=21#wechat_redirect)

Andrej Karpathy: Tesla 能实现自动驾驶领域的 AGI | AGIX 投什么

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/014.png)

[![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/015.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509696&idx=1&sn=6409bd98f7045584687d59360f417562&chksm=ce9b195ef9ec90483a5ce4bef2a5d74d5a3884184e53b49d3c30e2558f81515235758427d9d0&scene=21#wechat_redirect)

LLM 新范式：OpenAI o1, self-play RL 和 AGI 下半场

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/016.png)

[![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/017.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509647&idx=1&sn=186ab424d16c06cfa4616e3267c426ca&chksm=ce9b1911f9ec9007f4199514c813cae33a5f2d5e6b33ed8e4b04b7da6bfe051a3204db5e97b2&scene=21#wechat_redirect)

草莓模型即将发布，如何参与新一轮 AI 上涨周期 | AGIX 投什么

![](../images/2024-10-17-notebooklm-shi-google-de-chatgpt-shi-ke-ma/018.png)
