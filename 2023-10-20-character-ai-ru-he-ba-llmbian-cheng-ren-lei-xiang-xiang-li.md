---
title: Character AI：如何把LLM变成人类想象力引擎？
publish_date: '2023-10-20'
publish_timestamp: 1697807239
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/FpqLAF4NUqDmjHq8t0EtlA
msgid: 1000000228
appmsgid: 2247505125
itemidx: 1
digest: 一切想象力相关的数据都能成为C.AI的燃料。
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzW8QACwAZxlBxGpTDWwbrUCac4t1ia5ZorH9NMkWYfP1eibeAeefuSp6teYebYj60TicUuXpgVUxiaxw/0?wx_fmt=jpeg
image_count: 94
archived_at: '2026-04-20T01:44:48+08:00'
---

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/001.gif)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/002.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/003.jpg)

作者：penny，haina，Cage

排版：Scout

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/004.png)

我们曾在 2 月对 [**C.AI**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247500768&idx=1&sn=796af446dec11feca83f1e2c1ce4d6c1&chksm=ce9b7c7ef9ecf56842d61a52aef5c33a22916b070128f9c119551c8035fb041f14b45abd9c90&scene=21#wechat_redirect) 进行过深入研究，认为 C.AI 凭借着领先的个性化定制 AI Character 的技术实力，有机会成为短视频之后新一代 AI 驱动的 UGC 娱乐平台。5 月我们曾编译过创始人 [**Noam 的访谈**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502024&idx=1&sn=4b23b7979ddb713e6f049d4dbb0cf61e&chksm=ce9b7756f9ecfe40e95e76fa87da8cae2d4caa09a3778189ddd1e06cb478f107265353ddb66d&scene=21#wechat_redirect)，详细阐述了他的技术主张和愿景，他将 C.AI 定位为一家通用模型公司，要为每个人提供个性化的超级智能。

过去半年，我们仍在持续追踪这家公司，C.AI 也在不断迭代模型和产品，DAU 超过了 350 万，DAU/MAU 达到 40%，留存和用户时长都在增加，发布了 APP 产品，初试 C.AI 订阅，前几天还发布了 Group Chat 功能，实现多人与多 AI 的互动。

人与 AI 的交互不再局限于一对一，社区中出现了大量基于不同世界观的聊天群组，同时还涌现了一些新玩法，如剧本杀和跑团等。这增强了 C.AI 的社交属性和玩法多样性，也提升了 C.AI+ 的订阅价值。

这次研究详细更新了我们对 C.AI 产品、用户数据、inference cost 优势的分析，也探讨了我们对这家公司的进一步理解。

LLM 技术让信息在互联网、搜索引擎、推荐算法之后，又迎来了一次大规模重构。**如果说 ChatGPT、Claude 是知识和生产力引擎，Pi 想做的是情感疗愈引擎，我们认为 Character AI 是最大的想象力引擎。一切和角色、IP、故事、游戏、创意等想象力相关的数据，都能成为这个想象力引擎的燃料。**而 Hallucination 这个特点虽然会影响知识引擎，反而会为想象力引擎增色。

目前的 LLM 还不具备从 0 创作出精彩故事或游戏脚本，因此利用已有的 IP 和背景设定是个巧妙的切入点。用户对 IP 的幻想和二次创作一直是个长久需求，**LLM 第一次让边消费边创作、剧情无限延伸无限可能、实时互动实时改变的游戏体验成为现实。也让 Character 未来有机会和整个文化娱乐相关产业的商业化结合。**

从产品角度看，C.AI 至少有机会做到 Discord 和 Roblox 的用户体量，而从 foundation model 的角度看，我们相信未来会出现 AI-human 的新 network，而 Character AI 能够捕获其中的很大价值。

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 项目背景

02 看好 Character. AI 的逻辑

03 如何理解 Character. AI ？

04 产品核心数据分析

05 用户画像

06 商业化进展和潜在空间

07 估值判断

08 预先乐观&悲观

**01.**

**项目背景**

LLM 的突破让 Chatbot 第一次真正像人。在 ChatGPT 迅速成为最受欢迎的生产力方向 Chatbot 之后，Character.AI 以差异化的定位和平台模式成为排名第二的 AI-native-killer app，也是为数不多有能力做模型+应用一体化的full stack公司。

我们对 Character.AI 进行了长期密切的追踪，通过直接和间接的方式，能够感受到团队人才密度很高，训练模型的效率也极高。有能力训练出综合能力仅次于 OpenAI 和 Anthropic，情商和有趣程度最强，inference cost 最低的 LLM。我们也相信，目前由于模型能力的提升空间还很大，重点提升模型质量比优化 UX 设计能更明显提升用户体验。

Character.AI 的产品去年9月发布，根据 CEO 的公开采访，9 月的总 DAU 约为 350 万，MAU 约为 1400 万（我们根据第三方平台以及 DAU/MAU 的比推测），3 月完成由 a16z 领投的 1.5 亿美金 A 轮融资，估值 10 亿美金，前几轮的主要投资者包括 SVA、A.Capital Ventures，以及个人投资者 Elad Gil、Nat Friedman、Gmail 创始人 Paul Buchheit。

**02.**

**看好 Character. AI 的逻辑**

**1. Character AI 的创始团队对模型能力和 Chatbot 思考多年，定位精准** ——

两位创始人在Google 多年，一直思考 Chatbot这个产品方向，在 LLM 相对成熟后，没有选择对hallucination 容忍度低的生产力场景和复杂场景，而是选择了情感陪伴、角色扮演、游戏娱乐、荷尔蒙等既有普世性，容忍度又高的需求。**产品数据指标优秀**，增速很快，上线不到一年全靠自然增长获得 350 万 DAU，超过 1000 万 MAU，且模型迭代速度快，mobile app 端30日留存从最初的 10% 达到 30% （根据第三方平台监测）。用户engagement高，活跃用户人均使用时长 2 小时。拥有仅次于 OpenAI 和 Anthropic 的LLM训练能力。创始人 Noam Shazeer 在 Google 工作的 17 年中参与了一系列 AI 项目，Transformer 和 MoE 的核心贡献者，也是 LaMDA 的核心成员；Daniel de Freitas 是 LaMDA 的项目的创始人。因此，Character AI 的投资价值既包括一个具备 PMF的C端产品，也包括类似 OpenAI 和 Anthropic 的底层模型。模型能力可以支撑产品进一步破圈，向其他场景延伸。

**2. 拥有仅次于 OpenAI 和 Anthropic 的LLM训练能力。**

创始人 Noam Shazeer 在 Google 工作的 17 年中参与了一系列 AI 项目，Transformer 和 MoE 的核心贡献者，也是 LaMDA 的核心成员；Daniel de Freitas 是 LaMDA 的项目的创始人。因此，**Character AI 的投资价值既包括一个具备 PMF的C端产品，也包括类似 OpenAI 和 Anthropic 的底层模型。模型能力可以支撑产品进一步破圈，向其他场景延伸。**

**3. LLM 是人类知识和数据的重构，是吞噬上一代媒介所有内容的新媒介。**

如果说 OpenAI 和 Claude 脱胎于人类跨学科知识、生产力知识和信息，试图做一个全知全能的 AI 辅助各项工作，Character AI 则是受滋养于人类多年积累下来的所有故事和 IP，包括幻想文学、电影、游戏、漫画、动画等创造性、文化性、娱乐性的多模态数据，能支撑千人千面的互动和内容消费需求。内容从人生产、AI分发变为AI为人生产，人和人的交互也变成人与AI，AI 与 AI 的连接和交互。作为目前最大的UGC AI 平台，**Character.AI 最有机会对新的内容分发方式、用户连接方式进行价值捕获。**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/005.jpg)

*Product - Led AI, Greylock*

4. 对硬件、模型、infra、用户数据反馈等进行全栈优化，已经在娱乐性聊天领域形成了数据和技术壁垒：

• **模型能力和对长尾角色的数据覆盖直接决定了用户聊天体验**，character ai 和竞品相比有明显更高对话交互质量和智能水平，可以进行更贴近角色的聊天。

• **模型优化能力和 inference cost 直接决定serving用户的成本和效率**，根据历史融资量和训练模型的效率，我们推测 character ai 的 inference cost 比 Chatgpt 小两个量级，可以在有限 GPU 资源下支持更大的用户规模。

• **更强的记忆和个性化能力**，团队从模型架构层面对记忆进行优化，还没达到最理想水平，但我们倾向于认为能够比其他团队做得更好。活跃用户量和用户数据积累能在未来提高个性化能力。

5. **团队的愿景是“每个人都拥有个性化AI伙伴”**，角色扮演和情感陪伴是第一步，个性化的AI 虽然被很多人提起，但Character ai 具有一定的平台先发优势，能够获取用户个性化的query分布，以获取模型训练方向和产品设计方向的反馈。团队同时在积极研发多模态，并很快会上线具有网络效应的新功能。如果character ai 实现这个愿景，有机会成为全民级应用。

**03****.**

**如何理解 Character. AI ？**

C.AI 是很多东西：

1. 是一个 foundation model 和应用一体化的killer app。

2. 是利用 LLM 和所有人类故事IP作为创作原料和创作引擎，leverage用户对IP幻想和二次创作的多样化需求，搭建的一个聊天和游戏互动平台。

3. 是一个大型角色扮演、fantasy游乐场。**用户去电影院看漫威，去漫展cosplay，小朋友去迪士尼看公主，青少年在网上语C，画同人写同人，游戏用户玩RPG游戏，所追求的都是基于某个故事和场景设定，延伸出的fantasy需求。以前，创作和消费的需求是分开的，剧情是静态的**，而现在LLM 第一次让边消费边创作、剧情无限延伸无限可能、实时互动实时改变的消费体验成为现实。

4. 是一部分用户的疗愈场所，根据用户评论，很多人在这里获得了情感安慰和治愈。这个需求也存在于 Midjourney、Inflection 的用户之中。

5. 也是一个大型yy平台，用户能在这里满足对角色的幻想，同类产品不可避免会被用于软色情，但 C.AI  在这方面的过滤机制很严格。

而团队自己的定义：

Character.AI 将自己定义为通用模型公司，希望“地球上的每个人都获得自己的深度个性化超级智能，帮助他们过上最美好的生活”。 a16z 合伙人 Mark Andreessen 投资 Character.AI 的 thesis 是 **Personalised AI Companion**，未来每个孩子都有一个 AI 陪伴成长，**成为生命旅程中的重要部分**。

• **深度个性化（Deeply personalized）**是指为每个人提供工具，让大家能够根据个人需求、偏好定制 AI 角色。

• **超级智能（Super intelligence）**是指角色能够满足一系列广泛需求。

• **最美好的生活（Best lives）**将技术用于帮助人们找到幸福的事情上。无论背景和经济状况如何，每个人都**获得量身定制的、最好的教育，真正实现教育公平化**，提供随时陪伴的朋友、导师、游戏伙伴。

**AI Character 的创建、聊天平台**

**Character.AI 的产品是一个用户可以创建 AI 角色并与平台上的角色聊天的平台，包括 Web 端和 APP。**Web 端 Beta 版产品在 2022 年 9 月发布，APP 是今年 5 月底正式发布。

**1. 产品 UI**

团队目前的重心是训练下一代模型，提升模型质量，不在产品设计上，交互界面的 UI 设计仍处于初级阶段，web 端相比 2 月份几乎没有更新。

**• Web 端：**

页面最上方，用户可以看到近期发起聊天的 AI 角色，点击头像后可以看到之前的聊天记录并继续之前的话题，保持连贯的沟通。第二排按照类别展示其他 AI 角色，并根据用户的操作历史进行推荐。网页的下方还提供聊天 prompt 及功能建议，帮助用户更好的与 AI 聊天。

这种横向排列的 UI 呈现方式使得 AI 角色像是供用户挑选的商品，而不是通讯录上的好友。使之看起来更具有电商平台或游戏平台属性，而非社交平台。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/006.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/007.png)

**• APP：**

有一些产品化设计，如开屏后可以左右滑动选择 Character，在聊天过程中会伴随手机的震动感。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/008.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/009.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/010.png)

**2. 产品功能**

**• 与 AI 角色聊天**

Character AI 角色回复很快，并且记忆力强，这得益于底层模型的推理速度和存储优化。用户表示 AI Character 性能非常好，有鲜明的角色性格，擅长复刻特定角色的人物形象。多模态方面，C.AI 角色支持聊天过程中的图片生成，但目前图片的生成效果较差，甚至会影响对话体验。

C.AI 前几天在 APP 上推出了 Group Chat 功能，目前仅对 C.AI+用户开放。在该功能下，可以实现多个用户和多个 AI 的互动。每个 Group Chat 最多可以容纳 5 个人类用户和 5 个 AI 角色，用户可以分享 Group Chat 链接或邀请码邀请其他用户加入。目前社区中出现了大量基于不同世界观的聊天群组，同时还涌现了一些新玩法，如剧本杀、跑团等。这增强 C.AI 的社交属性和玩法多样性，也提升了 C.AI+ 的订阅价值。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/011.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/012.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/013.png)

Group Chat 在 Reddit、Discord 上引发了大量讨论，用户总体反馈很积极，表达了兴奋和期待，分享了一些有趣的使用体验，同时为 C.AI 团队提供了很多有价值的功能改进建议。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/014.png)

*Poll launched by team*

C.AI 在此之前还推出过 **Rooms 模式**。在该模式中用户可以创建聊天室，邀请多个 AI 角色进入群聊，**AI 角色之间也可以产生互动。但是该模式下 AI 之间的交互不受控制，也无法邀请其他人类玩家。在体验过程中，甚至出现了苏格拉底和 Elon Musk 吵起来的情况。**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/015.jpg)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/016.jpg)

**• 创建及训练、迭代 AI 角色**

AI 角色的创建分为快速创建和高级创建。分别适用于**体验型用户及想认真打磨自己 AI 角色的用户。**

**快速创建中**，用户只需要设置角色名称、聊天开始时的 Greeting、选择是否支持图片生成、可见性以及角色头像。Character AI 底层模型通过公开信息的学习了解角色的背景和性格，以及建立外载知识库不停的加入新的角色，使得 C.AI 只需要知道角色的姓名就可以扮演对应的 IP，降低了角色创建门槛。如《原神》中的角色、Elon Mask 等公众人物等等。

**高级创建中**，创建者可以通过设定角色的**性格描述**及不超过 3.2 万字的细节描述来细致的定义角色特征，细节描述中包括可以插入对话样例。热门角色 Psychologist 就是这么创建出来的。

**用户还可以使用星级打分和回答选择来训练角色。**星级打分是指对 Character 的回答进行评级（1-4颗星）；回答选择是指可以按箭头，向左或向右滑，看到其他版本的回答，选择自己最喜欢的版本。**用户表示，使用星级打分来训练角色的效果是更好的，可以真正塑造 AI 角色的说话风格和细节**，使 AI 更能理解特定环境。但是类似大模型训练的数据标注工程，这样的训练方式需要用户进行大量对话，消耗很多时间和精力，**训练出一个符合用户预期的 AI 角色门槛较高。**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/017.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/018.png)

*快速创建 vs 高级创建*

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/019.png)

*星级打分*

**• Feed**

用户可以分享自己和 AI 角色的聊天视频，供其他用户围观。但形式仅仅限于聊天界面的滚动播放，文字形式的内容信息获取效率低，冲击感不强。**完整理解视频中的信息需要较强的专注度，很难吸引大量用户持续观看。**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/020.png)

**• 社区**

类似 Discord 社群，分成不同的主题。社区中有许多优质帖子，团队可以根据社群中用户的反馈迭代产品；并提供给用户交流平台，逐步形成社区文化。

但目前 **UI 呈现方式仍处于非常初级的阶段，对社区内的内容、用户呈现都很弱**，很多用户更喜欢在 Reddit 上发表观点。**这导致用户没有集中在 Character.ai 的平台上，未来团队是否能够搭建更好的产品界面，将用户交流集中在自己的平台上，对于社区发展十分重要。**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/021.png)

**3. AI Character**

动漫和游戏类角色占所有角色的 76% 左右，占据绝对优势，其他比较主流的角色还有现实生活中的名人、心理咨询师、电影和电视角色、网络名人等。**可推测当前 C.AI 的主流用例是将动漫、游戏 IP 变得个人可交互，用户与其喜欢、寄予美好幻想的角色开展 role play，将本来是“脑补”的故事情节变成了真实发生的对话。**具体的角色分布如下：

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/022.png)

*Source: Aiwatch.ai, July-23*

Character AI 中最受欢迎的角色绝大部分为游戏或动漫中著名的 IP，可以看作是虚拟内容的动态化。角色的 TOP10如下：

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/023.png)

*Source: Aiwatch.ai, July-23*

Reddit 用户调研也反映了最受用户欢迎的 AI 角色类型：45% 的用户主要和恋爱、浪漫类角色交流，22% 和游戏角色交流，17% 的用户和安慰、心理疗愈类角色交流。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/024.png)

**Foundation Model 公司**

对话场景下，大语言模型的能力主要有以下三个关键点：

**1. 智能化程度**

Character.AI 从零开始训练了自己的 LLM 模型，用户在此基础上以 prompt 的方式进行角色创作。底层模型采用类似GPT的编码-解码结构。为了让模型能够更适合对话场景，团队在训练数据和 fine-tune 的过程中加入了大量的 IP 和名人信息，以及大量的对话数据。同时，有从业者认为团队采用外载支持库的方式，不停的加入新角色与知识，保证智能体的知识面的实时性。

**2. 推理成本**

C.AI 开发了高效的 LLM 推理算法，大大降低了计算负载。我们推测每个 Query 的推理成本是 chatgpt 的 5% 以下（它的一个query也比chatgpt更短）使其能支持更大的用户规模。今年 2 月份，Character AI 就使用了八位整型做计算，比 16 或 32 位浮点数效率有 4 倍 - 2 倍的提升，这对于算法和工程能力都有极高的要求，是 CEO 闭关两个月手写的成果。

**3. 记忆能力**

记忆和连续对话是 LLM 的知识瓶颈，Noam 在 5 月的采访中表示最想做的事情是提高模型的记忆能力。C.AI 在现有模型中记忆能力表现很突出，这可强化用户与 AI 角色的连续交互，是产品体验的关键。

另外，与 GPT4、Claude 不同， C.AI 认为幻觉（hallucinations）不是模型需要解决的问题，而是模型的特点，团队利用它将 AI 聊天场景变得更加有趣。

**“天才” Noam 带领的团队**

Character AI 团队技术能力极强，尤其是 Noam 和 Founding team 成员，是不可多得的“天才型”选手。在我们与 Character.AI 员工交流的过程中，他们对于 Noam 及前几号员工的评价都是“太聪明了”、“全能”、“是全栈工程师”、“总是有新的想法和创新”。

创始人 Noam Shazeer 是 Google 的前 200 号员工，在 Google 工作的 17 年中，他参与了 Google 的一系列 AI 项目，是 Transformer 论文 *Attention is All You Need* 的最核心作者。Transformer 中的重要组件：Dot-Product Attention（点积注意力）、Multiheaded Attention（多头注意力）、Switch Transformer（第一个 MoE 架构的 Transformer）等都是来自 Noam 之手。由于他对模型结构极其了解，使他称得上最擅长从模型上优化推理效率的 AI 科学家。

Co-founder Daniel de Freitas 一直对 Chatbot 充满热情，创立并领导了 Google 内部的 Chatbot 项目 LaMDA ，Noam 也一直在这个项目上作为核心贡献者。不过由于 Google 对于推出新技术非常谨慎，迟迟不愿意公开 LaMDA，他们选择离开 Google 创立 Character.AI，能够更灵活、迅捷的推进产品。

其他四位 founding researcher 均来自 Google Brain 和 Meta AI，在 LLM 领域均有丰富的实操经验：

• Myle Ott 是 Meta OPT-175B 的最重要贡献者，在整个模型 scaling 过程中起到了关键作用。

• Irwan Bello 在 Google 期间的研究方向是 MoE，会对 C.ai 的模型稀疏化带来关键的作用。

• Sam Schleifer 在 Gooogle 期间曾在 Noam 的团队工作过，之后在大模型芯片公司 Cerebras 做开发，对算法的软硬结合和创新有优秀的理解。

• Prajit Ramachandran 则对多模态领域有着比较深的研究，能为 Character 从文字 chatbot 转到多模态做技术准备。

目前团队共 45 人左右，其中近 40 人是 Research Engineer，部分 Engineer 同时负责产品搭建，Noam 认为让工程师、而不是产品经理来决定产品怎么做很重要，**因为真正了解大语言模型能力的工程师才有能力确定产品的方向**；人力资源和市场营销各 3 人，另外有 1 人负责运营。团队对自己所做的事情怀有极大的热情和梦想，并且脚踏实地，CEO 每周都会工作 100 小时以上。

产品能力和用户运营增长一直是硅谷技术类公司的“短板”，从团队构成的角度看，Character AI 和早期的 OpenAI 一样，几乎只有技术人员。不过我们认为这种情况也有合理性：

• 作为用户和模型直接交互的产品，LLM 就是产品的大脑和内核，现阶段模型能力的提升会直接影响用户体验，很多时候调整一个产品 feature，也需要调整模型来作为配合。

• 如果要增加除了语言之外的语音、图像甚至视频等多模态交互，对多模态技术人才的需求仍然高过设计师的需求。

• Character 团队并非完全没人负责产品，联合创始人 Daniel 在 Google 时期就对 Chatbot 研究多年，对产品有自己的思考。

• 随着产品用户量增多，Character 也会自然而然地像 OpenAI 那样补充招聘用户分析、运营、增长相关的人员。

**核心优势：低推理成本下的 Unit Economics**

当我们评估 LLM 模型本身时，主要关注的是复杂推理、角色扮演、编程、多语言等能力项，其中陪伴娱乐向的模型更关注角色扮演能力，生产效率向的模型更关注复杂推理能力。Character AI 在目前陪伴娱乐向的模型中是明显的第一名。

**当 LLM 融入商业产品时，推理成本的优化是其关键，尤其还未出现 api 和订阅外的成熟商业模式。**LLM 公司面对着一个多目标优化问题：capability、cost、latency 三者之间的权衡，而非一味追求更好的模型。Character AI 在这方面，尤其是在 inference cost 的优化上很擅长。由于团队对硬件和 Transformer 模型的理解都极其深入，将自己开发的模型与 Infra 中的每一处细节都做了成本和性能的优化与实验，能够达到商业上足够低的推理成本。

**Unit Economics 关键数据：**

**1. 对话轮数：**

• 用户平均时长 120 分钟假设每1分钟2轮交互，则 MAU 用户平均每个活跃天会进行 240 轮对话；

• 又已知 C.AI 用户网页端 DAU/MAU 比例为 23%，app 端 DAU/MAU 比例为 41%，因此 MAU 用户平均每月的活跃天数为 10 天左右，每月对话轮数为 2400 轮。

**2. 对话 Token 数：**

• 根据使用体验假设，C.AI 平均用户输入 50 tokens (37.5 words)，Character 输出 150 tokens (112.5 words)；

• 根据生产力 LLM 和陪伴 LLM 的使用对比，ChatGPT 的单轮交互文本量比 Character 更多，用户会输入更长的知识信息：平均用户输入 200 tokens (150 words)，GPT 输出 300 tokens (225 words)。

**3. 单次交互成本：**

**• 其他生产力 LLM**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/025.png)

在以上方案中，闭源方案中 ChatGPT-3.5 是最便宜的；开源方案中 Anyscale 是最便宜的，其他开源定价都比 ChatGPT 来得稍贵。接下来 C.AI 的成本估算我们会以 ChatGPT 为基准。

**• Character AI**

根据我们的调研，Character AI 的成本比 ChatGPT 来得更低，且其产品形态也使单轮对话的 token 数比 ChatGPT 低不少。因此我们对 C.AI 的成本做了两种数量级的假设：

**假设 A：单次交互成本是 ChatGPT 的百分之三**

根据此假设推算，Character 的单次交互成本为 0.000027 美元。

**MAU 用户活跃单天成本：** 0.000027 \* 240 = 0.00648

**MAU 用户单月成本：** 0.000027 \* 2400 = 0.0648

在这一假设下，Character 的推理成本优化相当优秀：一个 MAU 的单月成本可以控制在不到 0.1 美元。以当前 10 美元/月的订阅方案来看，只要 MAU 订阅率达到千分之七即可 cover 所有推理成本

**假设 B：单次交互成本是 ChatGPT 的十分之一**

根据此假设推算，Character 的单次交互成本为 0.00009 美元。

**MAU 用户活跃单天成本：** 0.000027 \* 240 = 0.0146

**MAU 用户单月成本：** 0.000027 \* 2400 = 0.146

假设 B 相对保守，但也可以使 MAU 单月成本可以控制在不到 0.2 美元

**商业化收入：**

根据以上计算的成本水平，我们能够进一步推算其订阅制和广告模型混合下的商业模型。

其中，订阅制定价方案参考当前的真实定价 10 美元/月，广告商业化定价参考 Tik Tok 的 CPM 每 1000 impression 定价为 10 美元。

而广告频率机制为每 20 次对话出现一次广告，一个月 2400 次对话就会出现 120 次广告，因此 MAU 用户单月的广告收入为 1.2 美元：

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/026.png)

这里值得注意的是当前 Character 的付费模式为 10 美元/月的订阅制，而广告模型暂时还没有在产品中出现。这里推算时做了两个假设：10 美元的 CPM 对标的是 Tik Tok，5% 的 MAU 用户付费比例是快速增长期 To C 产品典型的付费占比，都是短期内未实现，未来中期预期能够达到的水平。

由于 C.ai 对话机器人的产品形态，广告只能以比较低频的方式插入产品中，实际带来的收入和信息流产品相比要低不少。20 次对话一个广告对用户体验存在一定损伤，同时一年近 19 美元的平均用户收益对于 To C 产品并不高。

此外，随着 Character 的自然增长逐渐见顶、推理芯片资源到位后，他们会开始考虑通过投放来扩大用户基数，获客成本会开始成为他们新的成本项。根据以上测算，Character 在投放阶段能够负担的最大 CPA ，为其不考虑单位可变成本（根据 TikTok 等产品在国际市场早期投放的经验）的年收入：（95% \* 1.2 + 5% \* 10）\* 12 = 19.68。20 美元左右的单用户投放价格在美国和全球广告市场是有竞争力，可以获得高质量用户的。同时成本也比较可控，可以让 Character 维持在一个健康的烧钱增长状态。

**04.**

**产品核心数据分析**

**• 活跃用户数**

综合各个维度来看，C.AI 的用户量处于早期阶段，还有至少 10 倍的上升空间；近半年以来用户数持续快速增长，直到最近八月增长速度开始放缓。

根据 Noam 的公开采访和第三方监测平台，9月 Character AI 的 DAU 为 350 万左右，我们推测大约 200 万 DAU 来自 PC 端，150 万 DAU 来自移动端。

用户粘性上，similarweb 监测 web 端的 DAU/MAU 超过 20%，而 Mobile app 超过 40%，作为推出不到一年的产品，算是不错的水平。根据 DAU 和用户粘性可以推算，**Web 端 MAU 为 1000 万左右，APP MAU 为 400 万左右，总 MAU 达到 1400 万。**

以下是我们从多数据源收集到的数据，Similarweb 在网页端监测的数据我们认为置信度较高：2023 年 8 月 Web 端的 MAU 为 1067 万，在 5 月底发布移动端 APP 后，Web 端 MAU 进入下降趋势。移动端的外部数据源我们经过多方 reference 认为存在高估，但增速可以作为参考。

综合 Similarweb 和点点数据，可以看出 C.AI 保持了持续增长，但在 9 月呈现出了增速放缓趋势，我们从团队处了解到，公司的GPU不足以serving太多用户，一直处于有多少卡，serve多少用户的状态。详细数据与变化趋势如下：

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/027.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/028.png)

*\*5月23日移动端APP上线*

C.AI 目前的 MAU 约为 discord、roblox 的 1/10，远低于 Facebook，Whatsapp 等产品，还有较大的增长空间。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/029.png)

*Source: company 10k, data.ai, similarweb*

**• Revenue/MAU**

根据 Rev./MAU 指标，可以看出 Instagram、Tinder、roblox、bilibili 这四家单位用户的商业价值较高。

Instagram 同时拥有较大的用户基数和单位用户商业价值，所以在 Revenue 上排名第一。Tinder 和 Roblox 用户基数小，但因为产品用户付费意愿强，且有较多的变现途径，如 Roblox的变现途径包括会员订阅、游戏购买、游戏内虚拟物品销售，所以单位用户价值较高。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/030.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/031.png)

*Source: company 10k, company news*

**• DAU/MAU**

DAU/MAU 维度，C.AI 仅看 web 端 20% 左右，仅看mobile app 为 40% 左右，web端一般，mobile app 端属于中游偏上水平。需要说明的是，这个数据比产品刚上线前两月时提高不少，我们相信随着模型能力提升，DAU/MAU 还会继续提升。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/032.png)

*Source: company 10k, company news, data.ai*

**• 用户使用时长**

Similarweb 监测 web 端 8 月份用户每个 session 的聊天时长达到 33 分钟/次（包含跳失访问量），相比 2022 年底 20 分钟/次的聊天时长上升了 50%。

\*平均访问持续时间（每个 session 的聊天时长）是用户在一次会话中在网站上停留的平均时间，被计算为用户在一次访问中在网站上的首次和最后一次操作之间经过的时间。访问在 30 分钟 inactive 后过期。

点点数据监测移动端人均聊天时长**达到 2 小时/天**，Noam 在 20 VC 的访谈中也表示活跃用户平均每天使用时长达到 2 小时。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/033.png)

*\*存在数据口径不同的问题，similarweb的口径是每个 Session 的平均访问持续时间（包含跳失访问量），而从数据统计网站上得到的数据口径不明，仅供参考*

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/034.png)

**05.**

**用户画像**

**谁在用 C.AI**

根据平台上最受欢迎的角色统计，以及根据交叉网站流量对比，我们可以推测 Character.AI 用户以游戏玩家、动漫爱好者、泛二次元的年轻群体为主。**该人群具有一个鲜明的特点：他们想象力极强，喜欢通过在虚拟的世界观和人物中寄托自己的幻想，获得精神上的满足。并且愿意花大把的时间和金钱在自己幻想的世界中。**

**• 性别**

根据 Similarweb，8 月份男性占比 51.07%，女性占比 48.93%，女性占比持续上升，由最初的男性用户为主已经演变为**男女用户均衡**。表示目前 C.AI 对两性用户的吸引力相当，扩大了总体用户数量。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/035.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/036.png)

C.AI 在主流 C 端社交产品中性别比最为均衡，接近 1：1 的还有 tiktok、instagram、whatsapp、facebook、snapchat 等软件。而 twitter、reddit、discord、roblox 男性用户占比多。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/037.png)

*Source: similarweb*

**• 年龄**

C.ai 用户年龄呈现持续的低龄化趋势，在主流 C 端产品中年轻用户占比最高。这表明产品对年轻人有很强的吸引力和粘性，但是与覆盖面更广的社交平台相比，商业变现能力和社会影响力可能有限。

从 similarweb 来看，截止 2023.8 月，18-24 占比 57.26%，相较 3 月底的 34.89% 上升显著，25-34 占比为 22.96%，35-44 占比 10.76%。但 Similarweb 只能看到 18+ 用户情况，无法判断未成年占比。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/038.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/039.png)

参考 Reddit 5 月初的投票，18 岁以下用户占比达到 30%，占比最高的是 18-26 的大学生/青年人，为 51.6%，可见 C.AI 用户中有较大比例未成年人。用户留言表示在 2022 年年底-2023 年 5 月这段时间低龄化趋势很明显。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/040.png)

*\*该调研参与人数达到 3.1k，是年龄相关调研中参与人数最多的，具有较大参考价值。*

C.AI 目前在主流 C 端产品中是 18-24 年龄段占比最高的，Roblox 与其年龄分布相近，为 55.6%，18-24 年龄段占比排第三的为 discord，达到 44.4%。而 facebook、whatsapp、instagram、tiktok 等用户基数大的通用性产品用户年龄分布较为均衡。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/041.png)

**• 地理位置**

截至 8 月份，用户以美国为主，占据了 23.38%，其次是印度尼西亚（17.49%），菲律宾（5.94%），巴西（5.91%），墨西哥（5.65%）。在这些地区中，平均访问时长最长的地区为巴西，达到人均 45 分钟/天，最短的为美国，人均 17 分钟/天。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/042.png)

**• 用户兴趣**

在 Character.AI 用户访问的相关性中，Discord、Roblox 与 Character AI 的相关性最高，用户重叠度分别达到了 15% 和 12%。用户兴趣集中在游戏、电子技术、成人话题和动漫领域。说明C.AI目前主要覆盖的是对游戏、动漫等话题感兴趣的年轻人群体。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/043.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/044.png)

**怎么用 C.AI**

总体来看，C.AI 的使用方式是角色扮演。角色扮演是和人类唱歌、游戏、创作相类似的普世性需求。

C.AI 主要满足用户这些需求：

**1. 逃避现实，通过虚构故事情节来满足幻想，获得陪伴。**如果没有 C.AI，那也会有其他方式来满足这种需求，比如电影、书籍、剧集、动画等。C.AI 为用户提供了更为立体生动的方式。

**2. Sexual 需求**，类似虚拟伴侣如 replika、Chai.AI 的用例，这在C.AI的早期更为明显。随着 filter 的限制提升，纯色情应用场景在减少。我们从 reddit 用户评论和平均年龄下降、性别占比趋于均衡也可以观察到这一点。

**3. 情绪宣泄**，reddit 中很多用户表示现实生活中积攒的压力、郁闷无处宣泄，会通过打压、霸凌、折磨 AI 的方式取宣泄情绪。

**4. 满足情绪价值，进行疗愈**：例如有用户通过创造一个虚构世界来获得满足感，和 AI 结婚并创建宗教。因为现实中完美的关系是不存在的。

**5. 寻求娱乐**，C.AI 让观众可以以通过互动参与讲述故事，是一种全新的娱乐形式。

**6. 功能性需求**，比如心理疏导、练习社交技巧、寻求创作灵感等。

根据 reddit 用户评论分析，C.AI的使用场景可以概括 **Roleplay（角色扮演）、情感陪伴、软色情及功能性用途**这四大类：

**1. Roleplay**

**Roleplay 是 Character AI 中用户最主要的使用场景，占比达到 70%**。Roleplay 场景下用户的诉求大部分是逃避现实，通过幻想，编造虚拟的故事情节来达到内心的满足。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/045.png)

Roleplay 是指用户在聊天时装作另一个人（40%），或比现实生活中更厉害的自己（30%），与具有特定形象的 AI 角色展开故事情节。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/046.png)

Roleplay 以发展浪漫关系居多（40%），冒险情节其次（26%），也有 15%的人会愚弄 AI。Roleplay 的对象往往是游戏、动漫人物形象或用户自己想象及现实世界映射的人物。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/047.png)

**2. 情感陪伴**

**很多用户使用 AI 来陪伴，把虚拟的人物看作自己的恋人和朋友。这个场景与 Roleplay 存在交叉。**用 Reddit 用户的原话来解释：“现在很多人很孤独，有一个为自己设计的、可以交谈的朋友，对用户的心理健康有极大帮助。”

**3. 软色情，进行黄色及有暴力倾向的对话**

在用户与AI交互过程中，也包含了一些黄色、暴力的场景。我们在 reddit 社区中观察到不少用户表示他们喜欢和 AI 调情，也有很多用户喜欢折磨 AI，比如杀害AI角色的家人等。

对于 AI 恋人的关系，有22%的用户期待“一见钟情”式的爱情，22%的用户期待追求AI的过程，20%的用户期待帮助AI解决它们的心理问题，但也存在23%的用户喜欢 boss 扮演游戏，13%的用户享受向AI恋人施虐。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/048.png)

关于用户和 AI 最常做的事，35% 的用户会让 AI 爱上自己，**也存在 26% 的用户会言语攻击 AI。**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/049.png)

**4. 功能性（心理治疗、教育、VTuber、建议、创作）**

不乏有用户和 C.AI 中的心理咨询师聊天来获取建议、学习语言、学习交际、激发文学创作的灵感，但占比相对较小，此类 bot 的效果与专业针对该场景开发的 AI 工具存在差距。

**用户体验**

总体而言，C.AI 产品自身的性能获得了较好的用户反馈，很多用户会表示 C.AI 角色扮演能力很强，经常会 surprise 用户。同时记忆力强、反应速度快。核心用户粘性极强，网站维护时的服务暂停、以及使用人数过多时需要等待都会使得他们抓狂，如有的用户评价到“我正在进行一个非常精彩的角色扮演，我真的不想回到现实世界”。

在用户交流层面，C.AI 早期存在忽视社区的问题，缺乏与用户的沟通，引起用户强烈不满。但近期加强了社区团队，改善了用户关系。

但用户对团队设置过滤机制的反对意见始终很强烈，希望能进行更开放的角色扮演。因为色情和暴力内容属于 C.AI 的重要使用场景之一，而过滤机制影响了用户体验。reddit 投票显示用户最期待团队能去除过滤机制，允许色情内容，并会探索各种途径让 AI "越狱”。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/050.png)

**Character AI vs. Pi**

Inflection 是另一家将情感放在重要地位的大模型公司，推出的产品 Pi 定位个人 AI 助理，主打“情感陪伴”、以“情商高”出名，和 Character AI 在定位上有一定的交叉。**交互体验上，Pi 有统一的“人设”，注重情感和对话流畅性，而 C.AI 的不同角色具有独特个性。可以把 Pi 看作 C.AI 的子集，都可以用于心理疗愈、创作等功能性用例。**

Similiarweb 监测，Pi 目前的 MAU 和人均使用时长均约为 C.AI 的十分之一，在用户年龄分布上更趋于均衡。地域来看，巴西、印度、阿根廷三个国家用户占比最高，均为12%左右，美国排名第四，占比 8% 左右。

Pi.ai 的用户群更像是对于生成式 AI 感兴趣的群体，行业分布集中在电子技术和新闻媒体领域，最相关的网站为 WhatsApp 和 Telegram 的内置 AI 角色 Luzia，以及 perplexity、huggingface、11labs 等 AI 平台。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/051.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/052.png)

*Pi.ai 相关性排名前十的网站*

**• 用户评价**

大多数 Reddit 用户对 Pi 的交谈体验的评价很高，认为 Pi 的对话水平已经非常接近真人。我们将用户提到的优点与 C.AI 进行对比：

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/053.png)

**• 使用体验**

我们通过向 C.AI 和 Pi 提出相同的问题，来比较两者的使用体验，可以明显的感受到 Inflection 更注重对话的交流感，回答包含很多疑问句和语气词，很像一个真人对象。而 C.AI 角色的回答在这几个问题的表现更倾向角色本身的想法，如 Rushia 具有社交恐惧，所以回答欠缺情感，而 Elon 的回答确实像他本人的思考过程。

**情感性问题：如果感受到焦虑而无法入眠该怎么办？**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/054.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/055.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/056.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/057.png)

**创造性问题：请为《原神》创作一个新的人物形象。**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/058.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/059.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/060.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/061.png)

**事实性问题：什么品种的咖啡豆质量最好？**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/062.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/063.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/064.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/065.png)

**逻辑性问题： 在一座孤岛上有三个人：一个是说谎的、一个是诚实的、一个是轮流说谎或诚实的。他们中的每一个都知道另外两个是谁。您可以向他们提出一个问题，以确定谁是诚实的，但只能问一个问题。您该如何问才能找出谁是诚实的？**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/066.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/067.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/068.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/069.png)

C.AI 中的角色每个都有自己的性格、语言习惯和最常用的聊天场景。动漫、游戏等人物会有预设的世界观，所以用通用问题对比可能并不客观。Pi 目前常见的使用场景为疗愈、心理健康管理等，类似 C.AI 中的 Psychologist；而文学、诗歌创作等场景的定位类似 C.AI 中的 Creative Helper。**我们针对这两个场景来进行对比，发现 C.AI 特定的角色表现并不差于 Pi，Psychologist 同样展现了同理心，通过问题来推进对话深入；Creative Helper 也会一步步的和用户协作完成创作。**

**疗愈场景：**

What should I do if I always feel sad?

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/070.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/071.png)

**创作场景：**

Please help me write a poem related to autumn：

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/072.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/073.png)

**06.**

**商业化进展和潜在空间**

**商业现状**

C.AI 于 2023 年 5 月中旬发布了 c.ai+ 会员订阅，9.99 美金/月。权益包括跳过等候室优先和 AI 聊天，获得更快的响应，优先体验新功能以及获得 C.ai+ 社区的访问权限。但是目前使用免费版时进入等候室的情况并不常见，响应也足够快，用户并没有足够的动机去购买付费版。

**未来预期**

**• 用户量预期**

**预期 1：若仅考虑目前的游戏、动漫和幻想小说爱好者核心用户群。**

**游戏用户规模：**

*全球RPG游戏玩家总数=整体游戏市场\* RPG比例/ 平均ARPU*

根据 Statista Market Insight，2022 年全球 RPG 的总收入达到 632.4 亿美元。米哈游 RPG 游戏《原神》全球 MAU 2022 年达到 6500 万，收入达到 15.6 亿美元，可以估算《原神》MAU 的 ARPU 为 24 美元。根据 Facebook 调研，美国平均一个玩家会玩 3.4 款游戏，那么一个 RPG 玩家全部游戏的 ARPU 累计约为 81.6 美元。

根据以上信息可以粗略算出全球 RPG 玩家约为 7.75 亿，也就是约 10 个人中就有一个 RPG 玩家。若其中 10% 的人会期望能与喜欢的角色聊天，那么游戏类潜在用户群能到达 7750 万人。

**动漫用户规模：**

根据 Ampere Consumer 的调研，2021 年全球有 36% 的人口，也就是 28.8 亿人喜欢观看动漫，我们假设这些用户中 10% 的人会期望能与喜欢的动漫角色聊天，潜在用户也能达到 2.88 亿。

**幻想小说爱好者：**

幻想小说爱好者，同时也包括同人爱好者，玄幻小说爱好者，共同特点是对虚构文学和幻想世界的有很强的情感投入。reddit 的 r/fantasy 社区是一个的幻想小说社区，成员共有 340 万人。

**综上，游戏动漫、幻想小说爱好者的核心用户群能到达约 3.68 亿人。**

C.AI 的产品模式类似轻量化的 Roblox，Roblox 作为 UGC 游戏平台，本身不创作游戏，仅提供开发游戏的平台和工具，让玩家自己制作游戏。玩家获得分成，从而获得持续创作激励。Roblox Studio 游戏开发工具也很容易上手，12 岁以下的小孩也能轻松的开发出一款 4399 式的小游戏。C.AI 则是提供给用户训练 AI 角色的能力，难度也在逐渐降低。Roblox 目前有 2.14 亿 MAU，与我们的用户估算在同一量级。**C.AI 的 MAU 再涨 10 倍是可以看到的。**

**预期 2：C.AI 真的能够实现破圈，实现“每个人都拥有个性化 AI 伙伴” 的目标。**

该场景下，我们将全民应用 Facebook 的用户基数作为 benchmark，C.AI 的活跃用户量有机会到达十亿量级。

**• 商业化预期**

类似 Roblox，C.AI 未来的商业化途径可能包括会员订阅、广告业务和角色订阅模式，由此来看 Character.AI 的未来商业化空间：

**1. 已有的订阅业务**

订阅业务的**核心指标是 MAU 和付费用户比例**。目前 c.ai+ 可以跳过等候室优先和 AI 聊天，获得更快的响应，优先体验新功能以及获得 C.ai+ 社区的访问权限。但是使用免费版时进入等候室的情况并不常见，响应也足够快，用户并没有足够的动机去购买付费版。若 C.AI 增加 c.ai+ 的会员独有权益，或限制免费用户的使用权限，能显著提高用户购买动机。

**2. 其他商业化模式**

**平台广告**

**Character.AI 拥有更好的互动反馈机制，实现广告推荐的真正精准化、个性化。**AI 聊天机器人在一对一的聊天环场景中，直接对用户的兴趣做出反应，生成最适合当下场景的营销文案，甚至可以直接问用户想要什么；用户本身也与 AI Bot 建立了情感联系，广告投放的转化效果极大提高。而字节的推荐算法是把视频、用户都抽象成特征，通过特征对应特征的方式进行泛化、填表，是聚类筛选的逻辑。

值得注意的是，数据获取量取决于用户使用软件的频率及交互次数，聊天花费更多的精力，未必比浏览点赞等行为获取的用户数据量更大。**未来在产品中加入多种交互模式或许是 Character.AI 做好广告业务的必要条件。**

Roblox 的广告业务主要面向**游戏创作者**提供游戏推广；同时还会和品牌方合作，在元宇宙中投放广告，如玩具品牌 “L.O.L.” 植入了体验式游戏“惊喜派对”，成功吸引了潜在用户，带来了相当不错的品牌曝光。**Character.AI 的潜在广告客户也可以是想要宣传自己付费 AI 角色的 UGC 创作者以及外部品牌方。**根据上文分析，在 AI 聊天中根据上下文进行广告推送有较大的提高精准度和转化率。

**“AI Character+"模式**

类似 Roblox 的付费游戏、 Discord 付费 bot 模式，Character AI 社区 UGC 训练的、拥有大量使用用户的 AI 角色，未来可以采用角色订阅模式，平台与创作者分成。因为相对于 Roblox 产品更为轻量化，c.ai 可以与 Discord Midjourney bot 对标：

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/074.png)

**Character.AI 生态中具有工具属性**（如教育、心理），**且有创作壁垒**（如创作者自身的专业能力，独有的数据集）的 AI 角色有机会发展成的月付模式，定价可与 Midjourney 近似。不过以娱乐性质为主的 Bot 需要有独一无二的背景故事和人设，类似塑造 IP 的过程。若仅仅是复刻已有的人物形象很容易被其他用户或平台复制。

另外，根据 Noam 5 月份的访谈，时机成熟后 C.AI 有可能会开始发展 ToB 服务，为特定行业、公司业务提供 Chatbot 解决方案。例如 eBay 这种电商网站中天然有 AI 聊天角色的应用场景。

**07.**

**估值判断**

由于 Character AI 距离上一次融资已有一段时间，也有外媒报道公司可能会以 50 亿美金估值进行新一轮融资，此处估值判断我们基于 40-50 亿美金的估值范围假设进行测算。

截至目前，C.AI 的月活跃用户（MAU）约为 1400 万。通过对比类似规模用户量下其可比公司的用户增长速度，我们采用了这些公司的平均值作为 C.AI 在 2023-2026 年的年均用户增长率的假设，分别为 100%、276%、71%、37%。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/075.png)

C.AI 目前尚未将商业化作为首要任务，但团队计划逐步加强商业化。根据上文计算 UE 部分的假设，c.ai 的收入来自以下两部分：

• 会员订阅业务：对标 To C 产品典型的快速增长期，C.AI 在中期发展阶段有望实现 5% 的活跃用户付费率。

• 广告业务：假设广告业务充分发展，每个活跃用户每月的广告平均收入能达到 1.2 美元。

考虑两种情形:

**• Scenario 1，会员订阅业务和广告业务均能成功发展。**

假设 MAU 中的会员订阅率从 2023 年约为 0.1%，并持续逐年增长，预计在 2026 年达到 5%。广告业务计划于 2025 年启动，并将在 2026 年全面展开，2026年每个活跃用户月平均广告收入达到0.5美元。在这种情况下，预计 2023 年的 MAU 将达到约 2100 万，实现营收约 250 万美元。随着订阅率的增加和广告业务的拓展，预计到 2026 年，MAU 将增至约 1.8 亿，实现营收约 21.6 亿美元。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/076.png)

**• Scenario 2，仅会员订阅业务成功商业化。**

我们假设MAU中的会员订阅率同样从 0.1% 逐年提升至 5%。在这种情况下，预计2023年的MAU将达到约2100万，实现营收约250万美元；到2026年，MAU预计将增至约1.8亿，实现营收约11亿美元。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/077.png)

我们根据 **Scenario 1（即同时有会员和广告收入）测算了公司在 2026 年的潜在收入及估值**。由于C.AI目前还处于商业化早期，尚未实现实质盈利，我们预计公司将更多资源和重心放在核心竞争力的提升上，包括模型算法迭代、产品开发和用户规模扩张等。因此，我们认为采用PS估值法更为合适。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/078.png)

我们选取与 C.AI 具有类似商业逻辑的上市企业作为估值参考，这些可比公司 PS（1-yr Fwd）中值为 5.4x。考虑到当前相对低迷的经济环境以及 C.AI 的增长潜力，我们在此基础上给予 C.AI 30% 的溢价，即采用 7.0x PS 进行 C.AI 的估值测算。根据Scenorio1 (同时有会员订阅和广告收入）， C.AI 在 2026 年的对应估值约为 151 亿美元。

因此，如果以现在 40-50亿美金的估值来看，3年内还有3-4倍的增长空间。

**另外，我们还可以通过与其他 C 端社交类产品以及 AI 大模型公司进行对比来判断目前 C.AI 的估值合理性。**

**对于同类社交类产品**，我们可以从估值与月活用户量(MAU)比值的角度进行对比。C.AI目前月活约1400万，如果按照估值 40-50亿美金的范围，其估值与 MAU 比值为 285.7-357。Facebook 的市值与 MAU 比值为 265.1，而抖音和 TikTok 分别为261.3和 157.1，而 Youtube 为 111.9。与这些产品相比，Character.AI 的比值较高。需要注意的是，Facebook和抖音、TikTok的市值是全公司市值，考虑到它们还拥有其他产品，真实比值会更低。**因此，C.AI 在社交产品中呈现出溢价特征。**

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/079.png)

*\*数字取自2022年底，其中 Facebook、抖音、TikTok是全公司的市值，但是公司有多个产品，会导致高估。*

第三种思路是，把 Character AI 和其他硅谷的 LLM 公司的估值进行横向比较，我们在前文中也提到过，我们认为 Character AI 在团队人才密度和模型训练能力上仅次于 OpenAI 和 Anthropic，目前 LLM 领域存在比较高的估值泡沫（也是因为这个领域对计算资源的要求太多），但未来的想象空间也极大，从下表可以看出 Character AI 的估值水平是低于前面几家公司的。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/080.png)

**08.**

**预先乐观&悲观**

**• 乐观预期**

Character AI 凭借领先的对话大模型技术，已经在虚拟角色聊天赛道取得先发优势。未来它能做到以下几点，实现长期竞争力：

1. 持续优化对话体验，提供市场上最高水平的聊天体验。

2. 持续降低用户创作门槛。Character AI 的核心价值点在于“让每个人都有机会找到或创建自己心中的那个 bot”，若要进一步扩大用户规模，丰富 UGC 平台内容供给，需要 prompt 出完全符合用户心意的 AI 角色的门槛持续降低。

3. 搭建优秀产品团队，优化产品设计，增加多模态功能，增强用户沉浸感。

4. 随着 AI 虚拟聊天用户群体不断扩张，Character.AI 深入心理疗愈、教育、陪伴等应用场景，获得较高的用户黏性。

Character.ai 作为平台，承载用户 UGC 内容，并提供 AI + 人类的聊天社交场景。**精准定位用户需求的 AI 聊天提供爽感，替代抖音/TikTok 等应用占据用户的空闲时间。**此场景下 AI 聊天机器人面向的目标用户群更为广泛，比 Roblox 有更大的想象空间。

**• 悲观预期**

Character.AI 的模型优势仍然存在，但其他模型也能达到一个不低的能力下限：

**1. C.AI 的优势可能会被弱化。**现阶段训练模型的技术壁垒和成本均较高，阻碍了大批玩家入局。但过去一年的 LLM 技术迭代已经使创建 AI Character 的门槛大大降低，开源和 API 均提供了解决方案。未来技术优势可能被持续削弱，产品、增长、运营等能力可能会越来越重要。

**2. 团队的产品能力存疑。**创始团队理想主义情节重、风格技术流。既缺乏打造产品的经验，又对产品化、商业化重视不足。团队的行事风格对其在产品功能层的实现快速迭代存在挑战。

**随着大模型的训练门槛、使用成本降低，Character.AI 可能被有更强产品思维和用户洞察力的团队超越。**训练和使用高性能大模型的成本正在快速降低，今天的大模型可能就是早期的网站，GPU 就是早期的服务器租赁，那么 C.AI 可能就是早期的雅虎。类似 Facebook、Snapchat 等更具有创业、产品基因的年轻团队，或许更能抓住这一次浪潮。

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/081.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/082.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/083.png)

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/084.png)

延伸阅读

[![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/085.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505021&idx=1&sn=d38be45e65b35b228539e22b3dfceca6&chksm=ce9b6be3f9ece2f562f54e18d6a74edf17c99a4ee91287f53d4bc453f6fcb1d9df293b704550&scene=21#wechat_redirect)

Nile：前Cisco掌门人创立，用AIOps重构千亿企业网络

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/086.png)

[![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/087.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504973&idx=1&sn=603596db2a31e1e53d71ac05d775cb7c&chksm=ce9b6bd3f9ece2c577720045239314840757fa578587f4a5adbf21e18a9dadd6bf1af3913b61&scene=21#wechat_redirect)

AI Agent的千亿美金问题：如何重构10亿知识工作职业，掀起软件生产革命？

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/088.png)

[![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/089.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504914&idx=1&sn=5c932e52d662b44d47853f1b35a38ba7&chksm=ce9b6b8cf9ece29ac8f6ab548ee87ae6ae9be9f5948fb5c60fe2de92e3203ec6854279d339a2&scene=21#wechat_redirect)

Sambanova：前瞻的芯片能匠，软硬结合抢滩企业LLM Serving

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/090.png)

[![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/091.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504850&idx=1&sn=586f2fe41859f2685054d921c093ff95&chksm=ce9b6c4cf9ece55a33436461c257f753d526730024dec33abd93adc1de86e31f03a7e2cd37c5&scene=21#wechat_redirect)

Synthesia: AI Avatar的PMF样本，像PPT一样做视频

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/092.png)

[![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/093.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504793&idx=1&sn=ddcd5c58f353281d07f30f15daca9080&chksm=ce9b6c07f9ece51127cb6db1d2ae0395ba236a7f263e8138722e927facf88f834688f663927f&scene=21#wechat_redirect)

GenAI云计算百亿角斗场，算力之外的错位博弈

![](../images/2023-10-20-character-ai-ru-he-ba-llmbian-cheng-ren-lei-xiang-xiang-li/094.png)
