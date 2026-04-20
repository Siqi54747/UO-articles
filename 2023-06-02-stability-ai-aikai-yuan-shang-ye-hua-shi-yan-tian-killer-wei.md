---
title: Stability AI：AI开源商业化试验田，Killer Model能成长为Killer App吗？
publish_date: '2023-06-02'
publish_timestamp: 1685708761
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/5go54jHKplEPZIzY3ymgvQ
msgid: 1000000202
appmsgid: 2247502483
itemidx: 1
digest: Stability AI抛掷的硬币两面是成功的开源生态与波折的商业化探索。
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgytWYIIpHGY0aMiaeiajulrGomHn4uFQ8W8PYrBupKA5HO7EGFicKUW9IVP6QhicQaraN5SASnGP1cp0Q/0?wx_fmt=jpeg
image_count: 46
archived_at: '2026-04-20T01:11:26+08:00'
---

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/001.gif)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/002.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/003.png)

作者：Cage、haina

编辑：penny

排版：Mengxi

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/004.png)

Stability AI 早期通过计算资源和研究经费，与众多 AI 开源科学家团队建立了深度合作。Stable Diffusion 就在他们的支持和推广下成为了文生图领域的开源模型标准，营造了优秀的下游技术和应用生态—— LoRA、ControlNet 等可控生成技术得以普及，苹果 M 系列芯片提供了支持，基于 Diffusion Model 的创业公司开始涌现。

而语言模型 LLM 领域都在等待着这样一个 “Stable Diffusion 时刻”的出现——成为标准、统一可商用的开源模型，因此 Stability AI  成为了我们关注和研究的重要公司。

**与开源生态的成功相比，当前 Stability AI 的商业化探索似乎并不顺利。**Stable Diffusion 的模型特性不需要很大的参数量，因此部署和使用的难度都比较轻量，加上活跃的开源社区使客户使用的时候门槛不高，较难设计商业化付费点。而开源的模式使其无法实现闭环的数据飞轮并优化模型，Stable Diffusion 目前的数据量和 Midjourney 不在一个量级，DreamBooth 直接使用的效果渐渐被 MidJourney 拉开了一定差距；不过图片领域，数据数量或许没有这么重要，够用即可，差距的原因是是否将重点放于风格化处理。

随着 StableLM 的发布正式宣告其进军 LLM 领域，Emad 称，Stability 的商业模式重心除了开源厂商常见的 B 端客户，**还会为发展中国家的 G 端提供服务。**其创始人 Emad 多次提到 Open model + Private Data 的方式会比 OpenAI 类 Close model + Public Data 更容易获得客户的信任，尤其在印度、中东、非洲等国家都有本地语言模型的需求，能极大的改变当地的教育和社会分工。

大模型时代的 AI 模型研发，需要很强的团队组织力和科学前瞻性，而**创始人 Emad Mostaque** 喊单、投资和 PR 为主的领导方式可能与此有所背离。Stability AI 的管理风格去中心化且自治，**自由度可以让卓越的科学家拥有更大的发挥空间，但也会因为缺乏规划导致团队的凝聚力下降和较大的财务压力。**

综上，**团队内科学家与外部开源团队的合作机制，管理团队对未来研究重心和商业模式的规划，都将是 Stability AI 目前需要解决的问题。**当然，OpenAI 用了 7 年时间才证明自己所下注模式的成功，我们也应对 Stability AI 开拓 AI 开源的商业模式保有耐心。

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 为什么要关注 Stability AI？

02 团队及创业愿景

03 技术模型 & 产品图谱

04 商业化与竞争

05 开源社区及关系

06 收购与合作

07 成功要素与风险

08 结论

**01.**

**为什么要关注**

**Stability AI？**

**以 Stable Diffusion 搭建了最好的开源生态**

随着 LLM 领域的开源模型开始涌现，Llama、Alpaca、Vicuna 都有不错的表现，甚至谷歌内部开始讨论：**We Have No Moat, And Neither Does OpenAI。**有一个问题经常出现：**谁能成为大语言模型领域的 Stable Diffusion？**这个问题意味着，Stable Diffusion 成为了文生图领域开源模型的统一标准，而 LLM 领域还没有这样的标准。

Stable Diffusion 之所以能成为标准，有这样几个重要特点：使用门槛低、模型调优灵活度高、生成效果好，加上 Stability AI 出色的运营能力，**Stable Diffusion 成为了第一个拥有极强生态的开源模型。**

Stable Diffusion 的生态包括付费应用 DreamStudio、全球开发者开源模型分享社区 civitai、Stable Diffusion 模型图片合集网站 Lexica、以及在 Replicate / Huggingface / Google Colab 上都有 Stable Diffusion 上手即用的模型。因为 Stable Diffusion 可以在任意硬件设备上运行，手机硬件端也有应用程序 Make AI Art、DRAI，以及将 Stable Diffusion 下载到 Apple 本地运行的 Drawthings、DiffusionBee。

**Github Star 和 Hugging Face 的下载量也能很好的反应 Stable Diffusion 的开源生态搭建。**在 Github 中，Stable Diffusion web UI 获得了 69.9k star，而 Hugging Face 中 RunwayML / Stable-Diffusion-V1-5 更是获得了 1.81M 的下载量。目前官宣和 Stability AI 围绕 Stable Diffusion 密切合作的企业包括 AWS、Krikey AI，Clipdrop 则被 Stability AI 收购，具体细节会在后文详细展开。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/005.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/006.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/007.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/008.png)

*Github 上的 Stable Diffusion 相关模型*

*（向右滑动查看更多）*

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/009.png)

*Hugging Face 上的 Stable Diffusion 相关模型*

**战略性新产品 Stable Diffusion XL** 暂未开源，早期社区成员表示似乎与原模型的模型设计、使用效果并没有很大差别；但近日社区涌现了更多积极的反馈，并且期待能够早日下载、finetune 该模型；团队表示该模型最终会开源，并提供 API。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/010.png)

*社区用户评价*

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/011.png)

*团队回复*

**开源模型中的营销专家**

**Stability AI 的营销能力有目共睹。**创始人 Emad Mostaque 没有 AI 技术背景，也没有科技创业经验，但 Stability AI 却获得了极高的关注度，并快速发展。Stability AI 在 A 轮筹款时没有宣布任何专有的人工模型，ToC 的产品也仅有访问其核心产品 API 的 DreamStudio。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/012.png)

*泄露的 A 轮融资 deck*

Stable Diffusion 由开源社区、Stability AI 及 Runway 研究员合作完成，Stability AI 并不独立拥有该模型的知识产权，但在 Emad 的强大宣发下被打上了 Stability AI 所拥有的印象；而其开源语言模型 StableLM 似乎又是一个营销胜于实际工作的例子：与其他开源模型相比结果很平庸，使用 ShareAlike 许可证，需要在相同的许可下共享修改后的模型权重，在实际使用中并不比 LLaMa 更方便。但是其每一次产品宣发都很强势，在社区和媒体引起轰动。

Stability AI 与开源社区的关系也很有趣，最初只是提供算力支持。但凭借着开源社区、“Stable Diffusion”背后的公司完成了 1 亿美元的融资后，Stability AI 再通过为开源社区提供更多的算力，收编开源研究团队等方式，进一步密切与开源社区的关系，撬动更大的杠杆。

**开源商业模式探索的试验田**

**目前 Stability AI 的核心商业化逻辑是“模型即服务”，将基础模型开源，凭借专业的团队为企业提供定制化服务咨询服务。**该领域竞争十分激烈，除了大型科技公司（OpenAI、Anthropic），Hugging Face，以及欧洲公司 Aleph Alpha 和 Silo AI 也在提供类似的服务。

根据近期访谈中传达的使命和目标，Stability 与其他 to B 的模型公司差异在于，Emad 表示其客户很多会来自发展中国家的政府，例如印度政府、非洲、中东、日本等都是他们积极布局的领域。Open model + Private Data 的方式会比 OpenAI 类 Close model + Public Data 更容易获得当地的信任，尤其在印度、中东、非洲等国家都有本地语言模型的需求，能极大的改变当地的教育和社会分工。例如印度大量的外包开发行业，可能会被当地的开源大模型所颠覆。

**Stability AI 对于开源模型如何进行商业化的探索对未来 AI 的发展意义重大。**尽管未来预训练模型很可能 commoditize 趋同，但是模型的 alignment 都将随着民族、文化、行业有显著的差异，开源模型的高自由度很可能在这一趋势中扮演重要角色。

**02.**

**团队及创业愿景**

**CEO 及核心成员**

Emad 是印度人，在约旦出生、童年在孟加拉长大，7 岁时跟随父亲来到英国，直到 22 年 10 月才第一次来硅谷。和他居所一样多变的，是他的职业生涯。在成立 Stability 之前，他做过程序员、VC 分析师、电影评论家、对冲基金经理。20 多岁的时候，他的儿子被诊断为自闭症患者，这让他离开对冲基金开始追求更有意义的事。

他开始对慈善事业及帮助他人充满热情，2019 年，为降低贫困人群的智能手机、互联网使用成本创立了 Symmitree；2020 因为对 AI 的痴迷及**开源 AI 社区缺乏组织，创建了 Stability AI。**

目前，Linkedin 上显示公司有 110 位员工。很多员工加入 Stability AI 的路径都是先在社区做贡献，之后以全职的身份加入。Emad 采用 “分布式” 的公司管理方法，员工分散在世界各地，给予极大的自由。对这样的工作模式，观点是比较两极分化的，根据 The Information 文章，有内部人士认为管理模式 “很混乱”，这**增加了成本，减缓了产品开发；**但也有研究员表示，该模式使得 AI 科学家们能够自由地选择自己感兴趣的主题进行研究。

其他核心成员及研究员如下：

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/013.png)

**公司愿景**

**2020 年 Emad Mostaque 建立了 Stability AI，**开展联合国支持的新冠项目 CAIAC (以集体和增强智能应对新冠肺炎)，这是他第一次真正接触到大模型，但该项目后续遇到了官僚主义等问题。为了继续促进 AI 模型开源，Emad 自掏腰包购买芯片，为 Eleuther 和 LAION 等社区**提供算力支持**。

**一个月后，团队意识到扩大开源模型的触达规模，发展商业化服务才是促进模型的普惠的关键，也是 Stability AI 合理的商业路径；**Stable Diffusion 是第一个足够好、足够快、足够便宜，任何人都可以运行的模型，所以 Stability AI **将 Stable Diffusion 作为突破口，为客户提供扩展和定制服务。**Stability AI 成功围绕 Stable Diffusion 搭建了文生图生态和商业版图，在 EleutherAI 研究基础上发布了 StableLM，同 Harmonai 合作开发音频生成模型，在 Stable Diffusion 的基础上进行视频、动画生成研究，进军其他 AI 模型领域。

**Stability 不把 AGI 作为最终目标，将“AI for the people by the people”作为标语，在产品、模型开发上追求低门槛和通用性。**Emad 认为“有人需要开放并分享引擎盖下发生的事情，确保完全合规，它们不能是黑箱，政府也不会在黑箱上运行。”开源模型与私有数据的结合将远远大于闭源通用模型的价值，因为闭源会受到更多监管、数据隐私等因素的影响。**Stability AI 的使命是为激活人类的潜力建立基础，而 Stability 的模型是乐高。**

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/014.png)

**Emad 认为人工智能的影响可能比工业革命还要大。**人工智能可能会导致一大批人被 AI 取代，人类需要控制 AI 的发展方向，创造出更好的工作，“生产力的提高最终会趋于平衡”，人类可以专注“使我们成为人类”的事情。**但 Emad 也认为这一轮人工智能的泡沫比以往的泡沫都大。**类似 .com 的泡沫，资本和机会的数量是完全错位的，很多商业性为零的项目都将得到超额资助。**长期来看这将不利于 AI 的发展：引发军备竞赛，每个人都试图建立自己的模型，导致大量的经济浪费。**而 AI 模型是国家的基础设施，比 5G 更重要，真正需要做的是国家内部的模型标准化，给模型提供更好的数据：不应该是更多的网络脚本数据，而是国家数据集。

**Emad 始终对 AI 未来的发展保持谨慎态度：**“如果未来出现比人类更有能力的 AI Agent，不受人类控制，在互联网上自由行动，最坏的情况就是它们扩散并控制了人类。”一如 Sam 在国会听证会上反复强调的，Emad 也认为政府需要制定监督政策，防止巨头利用模型控制人类。他**参与了马斯克等人暂停 GPT5 的呼吁。**一方面是出于风险的考虑，希望 AI 的研究开发应更加专注于准确、安全、可解释和透明，另一方面也有阳谋的因素，想获得追赶上 OpenAI 的时间。

**他表示 Stability AI 的下一步就是与跨国合作伙伴、多国政府合作，建立框架，让好的数据为模型服务，推动模型的本地化。**他认为在三到五年内，世界上只会有五到六家基础模型公司，将是 Nvidia、Google、Microsoft、OpenAI 以及 Apple。Stability AI 不准备、也没有必要去做基础模型的提供商。

**03.**

**技术模型 & 产品图谱**

**Gen AI 生成模型**

**Stable Diffusion**

Stable Diffusion 模型技术来源是发表在 CVPR 2022 的论文 *High-Resolution Image Synthesis with Latent Diffusion Models*，5 位作者分别来自慕尼黑大学、海德堡大学、Stability AI 和 Runway。其中 Robin Rombach 来自 Stability AI，Patrick Esser 来自 Runway ML。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/015.png)

在此论文的基础上，Stable Diffusion 被训练出来，研究团队用了 4000 个 A100 Ezra-1 AI 超大集群，并使用了非营利组织 LAION 提供的数据集（LAION-5B 的一个大子集），**Stability AI 是算力提供者。**在 GitHub 项目的描述中，Stability AI 和 Runway 的贡献是平等的，Stability AI 并不是 Stable Diffusion 的所有者。且 Stable Diffusion 生成的作品版权遵循 CC0 协议，不归属于任何个人和公司，但可以用于商业用途。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/016.png)

**在 Stable Diffusion 的基础上，Stability AI 开发出了付费版产品 DreamStudio 及供开发者使用的 API，以及暂未开源的 Stable Diffusion。**

**基于 Stable Diffusion 走红的可控生成技术：ControlNet 和 Lora**

原生的 Stable Diffusion 模型中有几个影响可用性的缺陷，都随着开源社区的合力贡献得到了优化：

**1. LoRA，更可控、灵活的微调方法**

初始版本中的绘画主题并不可控，也就是说不能保证连续多张绘画的主人公是同一个人物、同一种风格。而 LoRA 的存在完美的解决了这个问题。在微软研究院的相关论文中，这一方法最早的提出是为了语言模型的可控微调，而在 Stable Diffusion 的社区中因为出色的效果和高效的微调出圈。例如以下是 Civit AI 上比较有名的深底色摄像风格，生成出的图片风格高度一致：

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/017.png)

这个方法就像上图左侧的汉堡，如果想要使汉堡的有蛋黄酱的味道，在不改变其他用料的情况下向汉堡中加入一层蛋黄酱即可。LoRA 的微调方式就是保证了原本模型网络不变的情况下，通过一个 LoRA 小模型将需要的人物或风格加入模型外接，高效的实现想要得到的效果。

**2. ControlNet，对图片结构的深入控制**

如果说 LoRA 是一个把已有方法放到文生图领域焕发光采的方法，ControlNet 是一个完全基于 Stable Diffusion 开发出的重要方法。这个方法允许设计师可以根据设想中的构图，对图片进行高自由度的学习和生成。例如在下图中，ControlNet 可以先识别出图片的边缘，再用其作为骨架，注入 prompt 实现新的生成效果。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/018.png)

这个方法通过将模型网络分解为可训练和锁定两部分，可训练的部分可以随着学习进行更新，而 locked 部分则作为前置条件被保留在每一次生成中，作为前置条件。例如当我们想创作一个连环漫画时，其中的主要核心人物和线稿图的风格就能通过这一方式，在图像中一贯地保留下来。

**DeepFloyd IF**

DeepFloyd AI Research 是 Stability AI 旗下的独立研发团队，团队成员为 Stability AI 的雇员。Stability AI 为其发放工资和提供研究资助基金。该团队近期发布了的全新开源模型 DeepFloyd IF，解决了文生图的两大难题：准确绘制文字、准确理解空间关系。DeepFloyd IF 第一次使得目前已经获得了 5.1k 星。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/019.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/020.png)

*工作原理*

**准确绘制文字对文生图的商业化应用有很大价值：**在此之前，文生图模型无法准确生成文字，但运用 DeepFloyd IF 可以将想要的文字放置在画面的任何地方，进一步打通了海报、插图、服装等渲染图的工作流。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/021.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/022.png)

*DeepFloyd IF demo*

**Stable Animation**

Stability AI 发布的 Stable Animation SDK 是基于文生图模型的动画领域尝试，使得用户可以实现 prompt、prompt + 图像、prompt + 视频三种方式生成动画，该模型目前仅能通过 SDK 和付费 API 使用。

但用户表示，Stable Animation 的生成的动画效果欠佳，仍不能达到 Runway 的标准，且门槛更高，SDK 及 API 必须通过 Python 脚本调用。

**StableStudio**

StableStudio 是付费应用 DreamStudio 的开源版本，此举进一步表现了其开源的决心，但在产品维度并没有显著的创新。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/023.png)

而其在公告中提到的即将推出的聊天界面，与几天前发布的 StableViccua 所提到的界面一致。

**LLM 底座模型**

**StableLM**

Stability AI 4 月 20 日发布了可商用开源语言大模型 StableLM，目前包括 3B 和 7B 参数版本，接下来将推出 15B、65B 参数的版本。在 CC BY-SA-4.0 许可条款的约束下，开发者可以自由查看、使用、调整基础模型，用于商业或研究目的。

StableLM 基础模型建立在 EleutherAI 开源早期语言模型 GPT-J、GPT-NeoX 和 Pythia 套件的经验之上，基于 The Pile 构建了 1.5 万亿 token 的新数据集进行训练。团队称这个数据集使 StableLM 在会话和编码任务方面具有惊人的高性能。未来还将发布经过指令微调的模型，使用的数据集包括 Alpaca、GPT4All、Dolly、ShareGPT 及 HH，仅供研究使用。

**但 StableLM 看起来又是一个营销胜于实际工作的例子。**根据用户测评，与其他开源模型相比结果相当平庸，与 GPT 也相差甚远，其输出的真值几乎不存在：

• stablelm-base-alpha-3b 平均准确率为 25.6%；

• flan-t5-xl(3B) 平均准确率为 49.3%；

• flan-t5-small(80M) 平均准确率为 29.4%。

该模型明显缺乏对某些敏感内容的保护；而且在实际使用中，Stability 发布的模型中并不比 LLaMa 更开源：StableLM 的许可证实际上是 ShareAlike 许可证，需要在相同的许可下共享修改后的模型权重。模型还遇到了过度拟合的问题，可能是由于他们数据集中存在重复数据。

用户表示“很多这样的开源项目似乎只是试图追随和（糟糕地）重现 OpenAI 的突破，而不是试图超越它们。”

**StableVicuna**

Stability AI 近日又发布了 StableVicuna, 是旗下开源团队 CarperAI 的研究成果。CarperAI 专注人类偏好学习研究，从 EleutherAI 孵化并独立出来。团队声称 StableVicuna 是第一个开源的基于人类反馈的增强学习（RLHF）LLM Chatbot。AI Chat 模型的成功得益于两种训练范式：指令微调和通过人类反馈的强化学习（RLHF）。但因为 RLHF 的复杂性，在大多数模型中指令微调是在没有 RLHF 训练的情况下应用的。**StableVicuna 是 Vicuna v0 13b（指令微调的 LLaMA 13b 模型）的进一步指令微调和 RLHF 训练的版本。**

Stability AI 在公告中也发布了未来的产品界面：

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/024.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/025.png)

**04.**

**商业化与竞争**

类似于 MongoDB 和 Red Hat 的模式，根据 Emad 的 Twitter 表示，“Stable models 是基于公开数据的每一种模型的基准开源版本。**Stability AI 会通过合作伙伴（如 AWS) 为客户的私有数据提供部门/商业许可的模型；也为大型公司、政府建立定制化模型。”**

**Emad 表示 Stability AI 有一个很快会产生巨大利润的商业模式，和美国以外的其他国家政府合作。**但是他没有给出更多的细节，但他表示 Stability AI 不需要在硅谷，因为他将把技术带到整个世界：所有的国家广播公司、世界各地的家庭办公室。

具体的收入和成本拆分如下：

**收入**

**1. 服务大公司，提供定制模型和咨询服务**

类似 Huggingface/Adobe，Stability AI 的核心业务是为大公司建立专门的团队，形成合作伙伴关系，出售模型（扩展和定制 Stable Diffusion 或其他大型生成模型，每个模型的报价约几千万美元），并为企业提供咨询服务，帮助大型公司和政府对 AI 模型的采用。

团队早期表示尤其聚焦于创意产业，为内容生产公司定制专属模型，**这也与团队技术背景以及 Stable Diffusion 的适用场景紧密联系。**Emad 在最近的采访中表示，正在为世界上**最大的资产管理公司**建立它们的专有模型。他表示，“**最大的人工智能公司将是为大型企业提供大模型服务的公司。”**

**2. 付费应用**

**孵化社区生态中的技术与应用，推出商业化版本，如以 Stable Diffusion 为基础的 DreamStudio，**上线第一个月，收入就达到数百万美金，用户数量达到 180 万。

**3. API**

**通过提供开源模型的 API 收费，并提供增值服务。**团队自己的具体尝试包括 Photoshop 插件，使用户可以在 Photoshop 中使用 Stable Diffusion 生成和编辑图像；以及 Blender Plugin，可以生成纹理，从渲染图中生成 AI 视频等等。

4 月 13 日，Stability AI 发布 **Stabile Diffusion XL（SDXL），通过 API 提供服务，为企业客户构建，**擅长照片写实主义。团队表示 XL 版本使用了 23 亿个参数，远远超过 SD V2.1 的 9 亿个参数，所以生成的图像和构图细节处理更好。不过也有用户表示 XL 与原模型的模型设计、使用效果并没有明显差别。

**成本**

**1. 一方面，Stability AI 作为开源生态的基础设施，为开源社区提供算力及资金支持是一笔极大的开支。**

据说目前 Stability AI 拥有在 AWS 运行的、由 4000 多个 Nvidia A100 GPU 组成的集群，用于训练包括 Stable Diffusion 的 AI 系统，导致其运营和云服务方面的支出超过了 5000 万美元。

**2. 另一方面，Stability AI 在全世界招募顶尖团队，并且给予其极高的自由，这使得养团队的成本也不容小觑。**

**竞争**

**1. Hugging Face：开源模型的流量入口**

首先，Stability AI 和 Hugging Face 设想的商业化路径都是把开源模型定制化部署到企业，但开源模型目前均依赖 Hugging Face 做 demo，是获取开源模型的必经之处，Stability AI 绕不开的场景。由于开源模型的特性，Hugging Face 也可以为企业提供基于 Stable Diffusion 的定制化服务。

而且 Hugging Face 上有更多符合各类企业定制化需求的模型，其丰富度也是 Stability 暂时无法企及的。因此在很长的一段时间里，Stability AI 都将与 Hugging Face 处于竞合的关系，由于其对 Private Model Private Data 市场的相同切入点，Hugging Face 也有着很完善的 Diffuser 库和 app 产品，将成为 Stability 开源 AI 基建的主要竞争对手。

**2. MidJourney：Gen AI 领域数据飞轮最强的产品**

图像依然是 Stability AI 的主战场，因为开源模型最适合的场景还是类似 Stable Diffusion 等图像生成的中小模型，大模型开源的意义并不大。Midjourney 作为目前最成功的闭源模型-产品-社区一体化公司对 Stable Diffusion 形成了强烈的竞争关系。

普遍的观点是，Midjourney 的进化之快得益于其出色的产品设计和闭源属性带来的的数据飞轮。相比之下 Stable Diffusion 中大量的数据反馈由于其开源属性无法形成优化模型的反馈回路，SD 更多的体现在开源生态中的创新，如 Lora/ControlNet，但 Midjourney 同步受益于这些技术创新。[**具体内容可见我们之前关于 Midjourney 的研究。**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247500477&idx=1&sn=55e3d87d20c407a2b18b840288518988&chksm=ce9b7d23f9ecf435a4d8a34c65cca05393a8c37516b8b241b8605b2b6b7ee13d07a35cad22a6&scene=21#wechat_redirect)

但近期研究表明，LLM 领域使用精挑细选的数据做 fine-tune，比 blindly 的选更有用，在图片领域数据量级的重要程度也没这么高，够用即可。Stable Diffusion 2.1 之前的版本，只做了最基础的美学工作，没做风格化，XL 之后才开始加入风格；更注重通用性，MJ 做了较强的风格化处理，使得 to C 用户体感更好，但是我们注意到，SD 开源社区的 Finetune、Alignment 模型风格化后也能达到较好的效果，所以不排除 Stability AI 也有能力做到，只是重心不同。

**05.**

**开源社区及关系**

**开源社区**

目前，Stability AI 官网上包括 Harmon.ai、CarperAI、OpenBioML、MedARC、DeepFloyd 等开源社区及产品 Clipdrop，**删除了 EleutherAI 和 LAION 这两个核心社区，但 Stability AI 与这两个社区仍有较为密切的合作关系。**

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/026.png)

开源社区简介及合作模式如下：

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/027.png)

**关系与组织的边界**

团队表示 Stability AI 是社区里面成长出来的公司，是开发者社区的一员，并驱动、赋能整个开发者社区更好的成长，但不是管理开发者社区，更不是从属关系。Stability AI 支持这些社区，比如说 Laion, Clip ViT-H 使用了 Stability AI 提供的算力进行训练，训练完成后开源，成为 Stable Diffusion 2.0 的基础编码器，**Stability AI 再将 Stable Diffusion 进行商业化，所以是共生的关系。**

**开源与闭源**

**其实不同机构之间的 AI 研究并没有完全闭源，只有开源程度的区别：**Stability AI 所理解的开源是完全暴露权重、底层架构、在用户可以在自己的消费级 GPU 上面去运行。但 Meta、Google、OpenAI 也并不是完全的闭源，也通过发论文，开源部分小模型的方式来促进 AI 研究的发展，这些论文的方法部分会被社区吸收使用，推动 AI 行业的进步。不过近期，OpenAI、Google 等大公司呈现出更加闭源的趋势。

**• 推进 AI 行业发展的维度来看：**不同于大语言模型，小模型尤其是文生图领域，整体发展似乎是基于开源模型的发展速度向前推进，现有的模型都不会和开源社区的内容有太大的差距，这也是开源的魅力。

**• 安全的维度来看：**或许发布开源模型可能被用于不光彩的事情，如钓鱼邮件或恶意攻击，但 Stability AI认为，将模型开源，可以提高透明度和培养信任。研究人员可以对模型进行开放的、细颗粒度的访问，充分的验证模型性能，研究可解释性技术，识别潜在风险，并帮助开发保障措施，这是封闭模型无法做到的。

**• 公司发展维度来看：**开源和闭源的选择也取决于团队的特质，当创始人对未来发展有非常明确认知的时候，闭源是更高效的，比如 OpenAI；但是 Emad 没有技术背景，对未来没有明晰的认知，所以开源是 Stability AI 合理的战略选择。

**06.**

**收购与合作**

**收购 Clipdrop**

2023 年 3 月，Stability AI 官宣收购 Init ML 的 Clipdrop。Clipdrop 是成像应用套件，可以进行背景去除、光线调整、图像扩展等编辑。累计用户超过 1500 万，适用于 iOS、Android、macOS、Windows 等平台，曾六次获得 Product Hunt 的 “每日最佳产品” 奖。Clipdrop 目前作为 Stability AI 的全资子公司独立运营。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/028.png)

**目前 Clipdrop 集成了 Stable Diffusion XL（基于模型做产品包装），并且发布了新产品 Stable Diffusion Reimagine，**允许用户无限制地生成一张图片的多种变化。原理是用图像编码器取代了原有的文本编码器，不是根据文本输入来生成图像，而是从图像中生成图像。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/029.jpg)

*集成 Stable Diffusion XL*

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/030.jpg)

*Stable Diffusion Reimagine*

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/031.png)

*可以生成不同视角、不同风格元素*

**与 Krikey AI 合作**

2023 年 2 月，Stability AI 与 Krikey AI 合作推出了 Text-to-Animation 的 AI 工具，使用户能够在几分钟内通过输入文本短语生成动画，并把动画作为视频文件或 fbx 文件输出到**社交媒体账户、3D 游戏引擎或电影编辑软件，**还允许用户定制三维头像并生成 AI 动画。该生成 AI 动画工具结合了人工智能、计算机视觉和 ML 模型。

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/032.png)

*近期 Youtube 视频效果*

Krikey AI 的开发者工具还包括定制 3D 头像工具、AR 移动应用工具包等，使创作者能够生成动画，带入任何平台进行 3D 内容创作。Krikey AI 已与 Snapchat、T-Mobile、Google Maps, The Ellen DeGeneres Wildlife Foundation, Sony Pictures Entertainment 和 the National Audubon Society 合作，为品牌合作伙伴建立了定制的 AR 游戏，达到 500 多万用户。

Krikey AI CTO Ketaki Shriram 认为**“这是关于如何创建 3D 内容的革命的开始。”**生成性 AI 动画在电影、游戏、Metaverse 化身、社交媒体和云计算等行业中都有丰富的应用场景，AI 动画可能是下一个创造者经济的基础。但是虽然目前 Krikey AI 的 Twitter 保持了持续更新，但几乎没有用户关注，Product hunt 等平台上也找不到产品 Review，产品效果与市面上常见的 Text-to-Code 产品并没有明显优势。

**与 Amazon 合作**

Stability AI 与 Amazon 的合作包括 AWS、SageMaker 及 Bedrock 等几个方面。

**• 在算力层面：**

Stability AI 选择 AWS 作为首选云供应商，使用其云服务来建立和扩展其图像、语言、音频、视频和 3D 内容生成的 AI 模型。使用 Amazon SageMaker（端到端机器学习服务），Stability AI 在拥有数千个 GPU 或 AWS Trainium 芯片的计算集群上建立、训练 AI 模型，将训练时间和成本降低 58%。

Stability AI 与 AWS 的合作使世界各地的学生、研究人员、初创公司和企业都可以使用其开源工具和模型。**据称，Stability AI 获得了来自亚马逊的超过 4000 个英伟达 A100，**以 50% 的 margin 与 AWS 合作，为计算密集型模型提供服务。在此之前，Stability AI 计算资源来自创始人自己购买的 32 个 GPU。

**• 在模型层面：**

Stability AI 宣布与 Amazon 的 Bedrock AI 平台结成战略商业联盟，使 Stability AI 的模型在该平台上可用。Bedrock 为 Stability AI 的客户提供了灵活、可扩展的平台，并可以使用大量的工具。

除此之外，Stability AI 还与拥有 1.2 万部的电影资料库的印度的投资机构 Eros Investments（爱神投资）成立了合资企业；与 Peter Gabriel 合作推出名为 #DiffuseTogether 的系列 AI 动画挑战赛# 等等。

**07.**

**成功要素与风险**

**成功要素**

**1. 为开源模型的商业模式能否跑通**

目前我们无从得知 Stability AI 的定制化商业模型及付费版本产品及 API 的盈利情况如何，但传言称内部创收缓慢。开源商业模式始终饱受争议，根本原因是**开源 AI 模型的商业化不闭环，Stability AI 发展的最大难题还是开源 AI 模型和商业化如何同时达成。**目前还未看到合理的解决方案。

**2. Stability AI 的获客能力**

获客能力主要的影响因素来自于**团队人脉及 BD 能力**，以及**公众对团队技术实力的认可**。相比之下，目前 Hugging Face 获得了更多的认可，但 Stability AI 正在持续的收编团队，加上创始人的影响力，仍具有发展的潜力。

**3. 核心团队对于盈利的态度、行动，以及人员管理能否加强**

目前 **Stability AI 因 Emad 的管理风格创收缓慢，资金告急。**Emad 给 AI 研究员极度的独立性，将服务器权限直接交给他们，不进行任何监督，这导致了大量的成本风险，一些员工对 Emad 的领导风格失去信心。**传闻 Stability AI 可能正在寻找另一位真正专注于赚钱的高管。**目前，Stability AI 已经烧掉了去年底筹集的 1 亿美元中的大部分资金，并在寻求估值 40 亿美元的新一轮融资。若不及时加强内部的监督和完成新的一轮融资，Stability AI 会始终面临着资金问题和盈利困难，未来的领导风格及人员管理对 Stability AI 的发展至关重要。

**风险**

**1. 没有属于自己的闭源产品和数据飞轮，壁垒相对较浅**

不同于大语言模型领域的 OpenAI 和文生图领域的 Midjourney，Stability AI 没有独属于自己的闭源模型。Stable Diffusion 也是同 Runway 及社区共同开发的。其提供的 API 和定制化模型在技术上并不存在壁垒，用户没有必须选择它的服务的理由，虽然 Stability AI 也有自己运营的社区和开源合作伙伴，但开源使用的数据反馈也无法全部用于对模型的优化上。

**2. 没有深度绑定的合作伙伴，承担模型训练成本**

不同于 OpenAI 与微软的深度合作，Stability AI 与 AWS 的合作相对较浅，虽然也有 Revenue Share 机制，在不盈利的情况下难以负担较高的模型训练成本，也就无法堆积算力训练模型，和 OpenAI 抗衡。其新推出的 StableLM 的效果欠佳就在侧面反应了这一点。

**3. 面临的监管问题：如 AI 绘画涉嫌侵权被起诉**

文生图模型是否侵权一直是行业内热议的话题。三位艺术家指控他们在未经授权的情况下使用他们的艺术作品，使他们各自的人工智能图像生成器能够创造出相当于侵权衍生作品的 "新 "图像；目前 Stability AI 已经发布了驳回要求。不过这不会成为 Stability AI 发展的重要阻碍，AI 的发展是不可阻挡的趋势。

**08.**

**结论**

**发展预期**

Stability AI 以算力支持开源社区起步，并通过融资拉到了一些有名的研究者，以开源模型为基础搭建自己的生态。但是无论是人才的密度还是长期的愿景，距离 OpenAI 和 Deepmind 还有很远的距离。

Stability AI 未来的发展有以下几种可能的前景：

1. 成为 AI 领域的 MongoDB 和 Red Hat，以开源模型为基础，为大型企业、政府提供定制化模型及咨询服务，实现了较好的商业化效果；并持续在 AI 模型的开源、公平、安全领域做出贡献；

💡

开源软件（如 Red Hat）的商业模式：

**• Service & Support：**让尽可能广泛的用户使用开源软件，社区用户“为爱发电”，待软件进入生产环节，便会出现愿意付费的企业级客户。（类似 redhat 的 Linux1992）；

**• Open Core：**把核心的内容开源，对于部分内容，尤其是企业有关的 feature，变成需要收费的闭源内容。

2. 在开源领域的竞争中不及 Hugging Face 和 Replicate，无法实现有效盈利，最终成为了与社区共生的开源非盈利组织。

**不过目前 Stability AI 面临的混乱和困境是情有可原的，仅仅以现状去评判它的未来是草率且不负责任的。**一方面开源 AI 模式下的商业化探索本身就是一件全新的事情，开源模式原本常见于小成本的软件；另一方面 AI 领域的研究是长期且艰难的过程，OpenAI 在成立最初也没有获得行业的认可，在 7 年后才获得了如今的成就。Stability AI 仅仅成立了两年多的时间，就已经获得了极大的关注度和社区贡献，CEO 的影响力也有目共睹。如果其能度过目前成长的阵痛，找到合适的路径，未来的发展仍是可期的。

**Reference**

https://mp.weixin.qq.com/s/nmDgSq50iAB9iEhucmbXQg

https://www.thefashionlaw.com/stability-ai-looks-to-get-copyright-suit-over-ai-generator-tossed-out/

https://www.semafor.com/article/04/07/2023/stability-ai-is-on-shaky-ground-as-it-burns-through-cash

https://www.goldmansachs.com/insights/pages/stability-ai-ceo-says-ai-will-prove-more-disruptive-than-the-pandemic.html

https://www.webpronews.com/stability-ai-is-on-amazon-bedrock/

https://www.bbc.com/news/uk-politics-65582386

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/033.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/034.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/035.png)

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/036.png)

延伸阅读

[![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/037.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502215&idx=1&sn=faae751dafabaa9dc4167fda33a7d30a&chksm=ce9b7619f9ecff0f6031851e09690e2c060fa9b0019ff1b85bfb4a59d4378e8402d3067f29eb&scene=21#wechat_redirect)

Inflection创始人：从DeepMind到Pi，AI智能体如何迎来寒武纪大爆发

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/038.png)

[![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/039.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502183&idx=1&sn=6c02066bceb1b1df73c94cbdf5126ed4&chksm=ce9b76f9f9ecffef376df6b8795abe2af4a28efbc647293e288ab7c2fccb1672aea5c3f0e353&scene=21#wechat_redirect)

Ayar Labs：挑战计算中心“最后一米”，LLM浪潮下的硅光探路者

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/040.png)

[![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/041.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502123&idx=1&sn=a7f55af90ad231b359f4724744d24a97&chksm=ce9b76b5f9ecffa321602156f722fd1578ee253333f728cdaf7c720d41f9af44c101860e4bcc&scene=21#wechat_redirect)

C-Eval: 构造中文大模型的知识评估基准

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/042.png)

[![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/043.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502089&idx=1&sn=6a676c7b77853ad9aee2a1a1ccc8aa74&chksm=ce9b7697f9ecff81bc3fb5bcb443d7bdb3feb9b2cd4c263e3bbbe442aa05a4bbbdf0ccfa8a5d&scene=21#wechat_redirect)

对谈OpenAI：如何为全球70亿人部署“超级大脑”？

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/044.png)

[![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/045.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247502024&idx=1&sn=4b23b7979ddb713e6f049d4dbb0cf61e&chksm=ce9b7756f9ecfe40e95e76fa87da8cae2d4caa09a3778189ddd1e06cb478f107265353ddb66d&scene=21#wechat_redirect)

Character.AI：AI Agents 平台下的大模型“民主化”梦想

![](../images/2023-06-02-stability-ai-aikai-yuan-shang-ye-hua-shi-yan-tian-killer-wei/046.png)
