---
title: Luma AI会是3D领域的Midjourney吗？
publish_date: '2023-08-29'
publish_timestamp: 1693314227
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/xB1goASIKneVlsTIrTYFsA
msgid: 1000000219
appmsgid: 2247504262
itemidx: 1
digest: 我们距离3D的Midjourney时刻还有多远?
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxDSg4IcuOaGoibkYN7t0SD3HervOLictBhIWWhiaSGcZWCf1Nlib1oEpXnXCr8e9T3IVDiceGjWcskeFA/0?wx_fmt=jpeg
image_count: 43
archived_at: '2026-04-20T01:31:41+08:00'
---

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/001.gif)

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/002.png)

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/003.jpg)

作者：Kefei

排版：Scout

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/004.png)

**随着语言、图像等领域的 foundation model 被广泛应用，头部公司和应用逐渐跑出来，我们开始期待其他模态或其他领域的 foundation model 的出现。**3D 是我们非常关注的一个领域，相比图文和视频，传统 3D 建模流程复杂，多为人工手动操作，周期长，成本高。如果 3D 生成技术成熟，现有的管线中的大部分环节将被替代，极具创新性和破坏性，想象空间巨大。另一方面，3D 有成熟的应用场景，如游戏、影视制作等，每一个场景的市场规模都很可观。

**如果我们相信每个模态都会有 foundation model 的机会，那么 Luma 可能是目前 3D 领域最有竞争力的创业公司。**

**Luma AI 于2021 年 9 月成立**，创始人为前 Apple AR/CV 工程师 Amit Jain、Alberto Taiuti 和 Berkeley BAIR 毕业生 Alex Yu。Alberto 现已离开公司。**Luma 的核心技术是 NeRF，通过 Luma，用户可以使用手机拍摄少量照片来生成和渲染出 3D 内容。公司成立至今已推出多个产品和功能，包括图片转 3D、视频转 3D、文本转 3D 等。**

**Luma 在一个相对正确的技术方向上，有非常高质量的团队，同时还有社区和数据优势。**2023 年 3 月，Luma 完成由 Amplify Partners 领投，Nvidia(NVentures) 和 General Catalyst 等跟投的 2,000 万美元的 A 轮融资。老股东包括 Matrix Partners、South Park Commons 等。

3D 领域的 foundation model 无疑是一个非常宏大的叙事，但 3D 生成目前仍存在许多瓶颈，包括生成质量不稳定、生成速度慢、可生成的场景多样性较差等等。如果进一步落地到具体商业场景还涉及到设计风格、可编辑的灵活度、如何与现有管线结合或是完全重塑现有管线等一系列问题。

因此整体来看，行业目前仍处于 research 阶段，距离能够真正在产业界大规模应用还需要一段时间。**我们期待 3D 尽快迎来 “Midjourney 时刻”。**

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 什么是 Luma

02 技术研究：NeRF、3D 建模、3D 生成

03 团队

04 场景及市场规模

05 行业其他玩家及技术进展

06 结论与投资判断

**01.**

**什么是 Luma**

**Luma AI 是一家 3D 内容解决方案公司，核心技术是 NeRF。通过 Luma，用户可以使用手机拍摄少量照片来生成和渲染出 3D 内容。**Luma 由前 Apple AR/CV 工程师 Amit Jain、Alberto Taiuti 和 Berkeley BAIR 毕业生 Alex Yu 在 2021 年 9 月联合创立，Alberto 现已离开公司。

**Luma 产品的主要功能有：拍摄捕获 3D 图像和视频、图片转 3D、视频转 3D、文本转 3D 等，用户可以通过 iPhone、网页以及 API 等载体或方式实现用 NeRF 技术构建 3D 模型的功能。**

2023 年 3 月，Luma 完成由 Amplify Partners 领投，Nvidia(NVentures) 和 General Catalyst 等跟投的 2,000 万美元 A 轮融资。老股东还包括 Matrix Partners、South Park Commons 等。**Amplify 此前也对 RunwayML 进行了投资，或将为两家公司来带一些协同效应。**

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/005.png)

**产品发布时间线**

• **2022 年 10 月 22 日，Luma AI 开放网页版 Luma**，在测试版社区中，用户可以根据网页中给出的拍摄指导上传符合规范的视频素材，生成 3D 视频。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/006.png)

*Source：Twitter*

• **2022 年 12 月 14 日，Luma AI 发布 Imagine 3D，即推出文本转 3D 模型的功能**，用户输入文字描述，即可生成对应的 3D 模型，模型的质量与输入的文本有很大关系。当前，该功能尚未全量开放，还处于测试阶段。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/007.png)

*Source：Twitter*

• **2023 年 1 月 7 日，Luma AI 在 IOS 上推出了 NeRF Reshoot**，Luma AI 是市场上第一个 NeRF + App 解决方案的提供者。当前，Luma 只推出了 iOS 版本，Android 版本尚在测试环节。这意味着用户仅需通过一部 iPhone 即可使用 NeRF 技术进行 3D 建模。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/008.png)

*Source：Twitter*

• **2023 年 1 月 19 日，用户可以将 Luma 的交互式 NeRF、全景图、视频渲染嵌入到用户自己的网站、博客等中，能够自定义共享页面的 UI。**

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/009.png)

*Source：Twitter*

• **2023 年 1 月 25 日，Luma AI 宣布 Luma NeRF 捕获的下一版本**，视频的清晰度和分辨率更高。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/010.png)

*Source：Twitter*

• **2023 年 2 月 24 日，Luma AI 实现了网页版全体积 NeRF 渲染器**，大大提高 3D 生成的逼真程度，宣传语中通过“实时可见，所见即所得”（All in realtime! What you see is what you get for photorealistic 3D is finally here!）对这一进步进行描述。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/011.png)

*Source：Twitter*

• **2023 年 3 月 21 日，Luma AR 发布，用户可以在实景照片中标记想要的 AR 视频路线，并自动生成视频**，Luma AI 成为首款 NeRF AR 记录器，同时用户还可以对视频进行编辑和修改，例如修改图片或视频比例、调整帧率等。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/012.png)

*Source：Twitter*

• **2023 年 3 月 27 日，推出视频转 3D API**，这使开发人员可以通过 API 将 Luma 的 3D NeRF 模型集成到其他应用程序和产品中。就使用情况而言，其输出能够直接嵌入交互式的 3D 场景中、在传统 3D 管道中构建交互的 coarse textured models 以及预渲染的 360° 图像和视频。**目前转换一个视频费用为 1 美元，转换时间在 30 分钟左右。**

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/013.png)

*Source：Luma官网*

• **2023 年 4 月，推出 Luma Unreal Engine Alpha**，是 Unreal Engine 5 的全新插件，为 engine 带来全体积的 Luma NeRF，可用于游戏、虚拟制作、传统图形内容和 VR 等。

*欢迎关注**海外独角兽**视频号*

*获取最前沿的科技行业资讯*

• **2023 年 5 月，发布 Unreal Engine plug-in V2**。支持 Unreal Engine 5.2；支持 macOS 和 Linux。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/014.png)

*Source：Twitter*

• **2023 年 7 月，发布 Unreal Engine plug-in v0.3**。Luma 在该版本中引入质量控制，提取 NeRF 的特定区域，微调渲染质量以匹配特定用例。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/015.png)

*Source：Twitter*

• **2023 年 8 月，发布 Flythroughs**。Flythroughs 是一个视频生成 APP，可以模拟生成无人机一镜视频。

*Source：YouTube*

**02.**

**技术研究：NeRF、3D 建模、3D 生成**

**NeRF 简介**

**Luma 核心技术是 NeRF，NeRF 全称 Neural Radiance Fields，是一种基于深度学习的系统，可以根据少量的 2D 图像对 3D 场景的几何形状和外观进行建模，是 3D 领域的一个重大突破。**

**2020 年，Google 研究员 Jonathan T. Barron** 与 Berkeley、San Diego 的研究员 Ben Mildenhall、Pratul P. Srinivasan、Matthew Tancik 等人共同发布了 paper——**NeRF：Representing Scenes as Neural Radiance Fields for View Synthesis，首次提出 NeRF 的概念。**

“通过使用一组稀疏的输入视图优化底层连续体积场景函数，从而获得用于合成复杂场景的视图的最优结果。NeRF 算法使用全连接（非卷积）深度网络表示场景，其输入是单个连续的 5D 坐标（空间位置 (x, y, z) 和观察方向 (θ, φ)），其输出是该空间位置的体积密度和视点相关的发射辐射率。通过沿相机光线查询 5D 坐标来合成视图，并使用经典的体积渲染技术将输出颜色和密度投影到图像中。”

We present a method that achieves state-of-the-art results for synthesizing novel views of complex scenes by optimizing an underlying continuous volumetric scene function using a sparse set of input views. Our algorithm represents a scene using a fully-connected (non-convolutional) deep network, whose input is a single continuous 5D coordinate (spatial location (x,y,z)(θ,ϕ)) and whose output is the volume density and view-dependent emitted radiance at that spatial location. We synthesize views by querying 5D coordinates along camera rays and use classic volume rendering techniques to project the output colors and densities into an image.

**不过，在当时，以 NeRF 的方式完成 3D 重建的过程仍然很缓慢，且需要一定的专业知识。**

**2022 年，Nvidia 发布 Instant NeRF，即将逆向渲染（在几秒钟内将一组静止图像转换为 3D 数字场景）与 NeRF 相结合，生成和渲染速度提高了 1,000 倍以上。**Instant NeRF 可以在几秒钟内训练几十张 2D 图片以及它们相机角度的数据，学习高分辨率 3D 场景，并在几毫秒内渲染该场景的图像。

Nvidia 图形研究 VP David Luebke 表示：“如果像多边形网格这样的传统 3D 表示类似于矢量图，那么 NeRF 就像位图图像，它们密集地捕捉光线从物体或场景中辐射的方式。因此，Instant NeRF 对 3D 的重要性就像数码相机和 JPEG 压缩对 2D 摄影的重要性一样——极大地提高了 3D 捕捉和共享的速度、便利性和范围。”

**传统 3D 建模方法**

为了更好地了解 NeRF，我们可以退一步了解传统的、目前被广泛应用的 3D 建模方法，进而知道 NeRF 究竟在哪些方面具有创新性。

以下是常见的 3D 建模方法：

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/016.png)

**• NeRF 与摄影测量**

从上表可以看到，摄影测量和 NeRF 一样都是用于捕捉真实场景建立 3D 模型的技术，但他们的基本原理和方法不同。摄影测量涉及识别图像中的共同特征，例如点或边缘，然后使用三角测量技术确定这些特征的 3D 位置。**而 NeRF 不涉及识别图像中的共同特征，而是通过深度学习从一组 2D 图像推断出场景的连续 3D 表示。**

**摄影测量是一项成熟的技术，多年来一直用于创建真实世界对象和场景的精确 3D 模型。它使用起来相对简单并且可以产生高质量的结果，尤其是当应用于具有明确特征和纹理的对象或场景时。**它还可用于从历史或考古数据（如旧照片或扫描图像）创建 3D 模型。摄影测量最常见的使用场景是在建筑、工程、文化遗产等各个领域创建真实世界对象和场景的 3D 模型。

而 NeRF 是一项较新的技术，在以高精度和细节捕获复杂的 3D 场景方面显示出巨大的潜力。它可以处理具有复杂几何形状和照明条件的场景，如反射和透明物体、小细节、模糊物体等等，并且可以生成仅靠摄影测量难以实现的逼真效果图。**NeRF 更灵活和准确，对用于重建的图片的数量和分辨率要求也更低。不过，NeRF 需要大量的训练数据和计算资源，并且使用起来可能是计算密集型的。**

因此，NeRF 不太可能完全取代摄影测量，两种技术各有优缺点，适合不同类型的应用。

**NeRF 与 3D 生成**

**目前 3D 生成的主流技术路径大致可以分为：(1) text-to-2D，再通过 NeRF 或 Diffusion 模型完成 2D-to-3D，或直接通过 2D 素材完成 3D 建模；以及（2）直接 text-to-3D，该路径直接使用 3D 数据进行训练。**

**其中，路径（1）更为常见，因为相比于 3D 数据，2D 数据更多、更丰富，可生成的 3D 内容也更丰富多样**。OpenAI 的 Point-E、Google 的 Dreamfusion、Nvidia 的 Magic3D 等模型均是此路径，该路径的许多模型都利用到 NeRF 技术。但 2D 转 3D 生成速度较慢，生成质量也相对较低，即使单个场景的数据量足够大，目前也很难看到质量有显著提升，或许还需要算法层面的创新。

**路径（2）直接使用 3D 数据集进行训练**，从训练到微调到推理都基于 3D 数据，OpenAI 的 Shap-E、Nvidia 的 Get3D 等模型是基于此路径。**Text-to-3D 的优势在于生成速度较快，理论上生成的内容质量也较高，但受限于 3D 数据的数量、质量和多样性，此路径下可以生成的 3D 场景有限，收集数据的难度更大，成本也更高。**

至于哪条路径更好？行业最后是否会收敛到其中一条路径？又或是有新的路径？这些问题目前在学术界仍有争议，暂时无法给出明确的结论。

**03.**

**团队**

**• 创始人**

2020年，Apple 在 iPad Pro 和 iPhone 12 Pro 上加入 LiDAR 激光雷达镜头，赋予了移动设备采集物体 3D 空间数据的能力。一年后，**苹果 AR/VR 的原员工 Amit Jain 和 Alberto Taiuti （Alberto 现已离开 Luma）共同创立 Luma AI。另一位联合创始人 Alex Yu 于同年加入，担任 CTO。**苹果系和伯克利系的创始人构成，使得 Luma 团队在产品和技术层面有着先进的理解，这也是为什么 Luma 能够率先抢占市场的最主要原因。

**Amit Jain 是 Luma 的 Cofounder 和 CEO。**Amit 毕业于 Missouri Valley College 的 Mathematics and Computer Science，2011 年至 2015 年曾创立 Cultured Pixel 并担任 Lead Developer，也曾担任 Product Hunt 等公司的工程师，2017 年加入 Apple 担任 AR/VR 部门的工程师，在 3D 计算机视觉、相机、机器学习、系统工程和深度技术产品方面有着丰富的经验。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/017.png)

*Source：Linkedin*

**Alex Yu 是 Luma 的 Cofounder 和 CTO**，Alex 于 2021 年毕业于 UCB 的 Computer Science and Applied Mathematics，毕业后即选择参与联合创立 Luma。在校期间他与 BAIR 教授 Angjoo Kanazawa 一起进行 NeRF 相关的 3D 计算机视觉研究。Alex 也曾在 Adobe 和 Google 实习。在 BAIR 和 Adobe，Alex 一直致力于通过 Plenoxels (CVPR 2022)、PlenOctrees (ICCV 2021) 和 PixelNeRF (CVPR 2021) 推进神经渲染和实时图形领域的研究。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/018.png)

*Source：Linkedin*

**• Team**

除了创始人之外，官网还展示了部分 Luma 团队成员，信息整理如下表：

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/019.png)

**04.**

**场景及市场规模**

**Luma 当前应用场景主要为生活记录、游戏制作、动画和影视制作、商品展示和销售。除此之外，NeRF 和 3D 生成技术还可应用于地图和导航、机器人等领域。**

**Luma 应用场景及市场规模**

**1. 生活记录**

Luma 在手机端上的应用赋予了普通人利用手机拍摄便可创建 3D 场景的能力，有人把 Luma 和 NeRF 比作“现代摄影的进化”，在 Luma 官网和 Discord 社区中，我们可以看到已经有非常多的用户利用它进行日常生活的记录和分享。

这部分 C 端业务是 Luma 的最大特色，但目前没有非常清晰的商业模式，Luma 未来可能更大概率还是通过 toB 在游戏、影视、电商等场景商业化。但 C 端平台依然很重要，若能做好，用户量和用户生成的 3D 资产爆发，将为 Luma 训练 3D foundation model 带来很大优势。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/020.png)

*Source：Luma 官网*

**2. 游戏**

游戏一直以来都是一个规模巨大的市场，利用 NeRF 和 3D 生成技术，游戏创作者可以将拍摄或文本生成的游戏资产导入游戏引擎中。游戏开发通常包括策划、程序、美术、音效、测试等环节，美术又包含了角色原画、场景原画、角色 3D 建模、场景建模、灯光、动画、绑定、特效等。其中，美术占总开发成本的大约 60%，而 3D 又占美术总成本的大约 40%。根据 Research and Markets 数据，2022 年，全球游戏开发市场规模为 990 亿美元，2030 年预计达到 2,480 亿美元，则 3D 生成可进入的市场规模大约为 595 (2,480 x 60% x 40%) 亿美元。

不过，目前的技术成熟度远远无法满足商业化的要求，无论是生成质量、速度、风格等等都仍未能满足游戏开发的标准。并且从技术角度看，网格是大部分 3D 世界的运行基础，但 NeRF 难以兼容网格，不过 Nvidia 等公司正在努力解决这一问题。但假设网格问题得以解决，生成的 3D 网格素材依然不能直接在游戏中大规模使用，目前的 NeRF-网格最适合的场景是创建超高保真模型素材，但这实际上需要大量的人工后期处理，需要一定的行业知识和大量的额外工作。

**3. 影视、动画制作**

NeRF 和 3D 生成可以简化各类影视项目的制作流程，减少后期制作过程及所需要的人力，建模、纹理、优化、照明等都将变得更高效。3D 在影视、动画中的应用通常包括 3D 建模、MG 动画（Motion Graphic）、3D 渲染、视觉效果等。其中，3D 建模、MG 动画、视觉效果未来都有可能通过 3D 生成完成。

根据 Grand View Research 数据，2022 年全球 3D 影视、动画市场规模为 204 亿美元，预计到 2030 年市场规模增长至 510.3 亿元美元。3D 建模、MG 动画、3D 渲染、视觉效果的市场规模占比分别为 31%、35%、20%、14%。

3D 生成可替代的环节包括 3D 建模、MG 动画、视觉效果，假设 3D 生成技术成熟，能够完全取代现有管线，2030 年 3D 生成在影视和动画制作中的市场规模将达到大约 408.2 (510.3 x 80%) 亿美元。而如果只看 NeRF，NeRF 更有可能在视觉效果这一环节发挥作用，这部分市场规模在 2030 年预计可达到 71.4 (510.3 x 14%) 亿美元。

以下是第一个采用 NeRF 进行制作的大型电视广告，是由 Luma 与 McDonald 和内容创作者 Karen X. Cheng 共同创作。

*Source：YouTube*

**4. 电商销售**

相较于线下购物，电商的最大劣势之一在于客户无法对商品进行全方位观察。因此，3D 图像是一种很好的商品展示方式，但由于请 3D 艺术家参与并对扫描的对象进行调整的成本十分高昂，因此，过去一般被应用于高科技设备、房地产等高价值的商品。

NeRF 技术的使用大大降低了 3D 生成的成本，根据 Luma AI 的官网说法，创建 3D 模型需要 60-1,500 美元和 2-10 周的时间，而使用 Luma 可实现 “1 场景 1 美元” 的超低 3D 展示成本，使普通商品使用 3D 展示成为可能。未来我们在线购物时，可以通过旋转照片，从各个角度查看产品，并且还可以进行各个角度的缩放。

Luma 还在 2023 年 1 月推出了 Share & Embeds 功能，电商商家可将其生成的 3D 图像直接嵌入到产品页面中。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/021.png)

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/022.png)

*Source：Luma Twitter*

根据 Market Watch 数据，2029 年 3D 电商市场规模可超过百万美元。

以上规模测算均是基于 3D 生成技术已经成熟到可以完全替代现有的 pipeline 的基础之上。

**NeRF 其他应用场景**

**1. 地图、导航、室内空间展示**

地图、导航、室内空间展示是一个对虚拟和现实交互要求和需求很高的场景，用 NeRF 来创建非常合适且可行。Luma 官网有一些相关的展示，但我们可以从 Google 的项目中获得更直观和震撼的感受。

2023 年初，Google 推出沉浸式地图，通过 AI 将数十亿张街景和航拍图像融合在一起，创建多维的世界视图。但假设我们想前往一家餐厅，我们通常会遇到以下问题：这家餐厅空间大小如何？有户外或靠窗的座位吗？哪个座位是我最希望预定的？虽然照片和视频可以部分解决此类问题，但依然很难创造身临其境的感觉。

因此，Google 在沉浸式地图中加入了各个餐厅、咖啡馆以及其他场所的室内视图，为用户提供了虚拟近距离观察的能力，而背后的核心技术就是 NeRF。

*Source：Google Research*

**2. 机器人研究**

AI+机器人的一条研究路径是，将真实场景建模，然后在模拟器里训练，这样理论上不需要依赖大量的真实数据采集，并且从模拟环境转换回真实环境的效果也会更好，尤其是像 navigation 这类对物理运动细节要求较低的环节。而 NeRF 可以大大降低场景建模的成本，是低成本场景建模的一大突破。因此我们会看到许多机器人科学家对 NeRF 感到非常兴奋。

**05.**

**行业其他玩家及技术进展**

**NeRF**

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/023.png)

**3D生成**

**• Google**

Google 在 2022 年 9 月公开了 DreamFusion 模型，DreamFusion 使用 2D 扩散实现文本到 3D 的生成，结合了预训练的 2D 扩散模型 imagen 与 NeRF 的能力。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/024.png)

*Source：Google Research*

**• Nvidia**

Nvidia 2022 年 9 月发布 GET3D，GET3D 只需要一块 GPU 每秒能生成大约 20 个模型。2022 年 12 月发布 Magic3D，Nvidia 声称 Maigc3D 可以在 40 分钟内创建高质量的 3D 网格模型，比 DreamFusion 快 2 倍。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/025.png)

*GET3D*

*Source：Nvidia*

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/026.png)

*Magic3D*

*Source：Nvidia*

**• OpenAI**

OpenAI 2022 年 12 月发布 Point-E，Point-E 的特点是生成速度快，生成一个 3D 模型只需要几秒到几分钟时间。2023 年 5 月发布 Shap-E，采用 INR（隐式神经表示），支持 NeRF 和 DMTet（纹理网格） 两种方法，可以更好地捕捉细粒度的形状和纹理，突破了传统扩散模型的局限性。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/027.png)

*Point-E*

*Source：OpenAI*

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/028.png)

*Shap-E*

*Source：OpenAI*

**• Meshy AI**

Meshy 是一个 3D 生成平台，目前可实现 text-to-3D、image-to-3D、AI 3D Texturing 等功能，目标是利用 GenAI 实现整个 3D 制作流程的自动化。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/029.png)

*Text-to-3D*

*Source：Meshy*

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/030.png)

*Image-to-3D*

*Source：Meshy*

*AI 3D Texturing*

*Source：Meshy*

**• Ilumine AI**

ilumine 推出的 InstaVerse 是一款 text-to-3D 资产生成器和可视化工具。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/031.png)

*Source：Ilumine AI*

此外，有消息称 Midjourney 也在尝试进入 3D 生成领域，创始人 David Holz 也曾公开表示过开发 3D 生成模型的意愿。

**06.**

**结论与投资判断**

**为什么看好**

**1. 值得 bet 的技术方向，值得 bet 的技术团队**

我们询问了 AI、图形学、CV 领域专家的意见，大家普遍认为 NeRF 是 CV/3D/图形学领域非常值得关注的技术方向。2020 年 NeRF 出现的时候学术界都非常兴奋，NeRF 实现了全流程可微，可以在深度学习框架上方便地实现场景表征的训练优化，**是 3D 领域一个具有开创性意义的、非常巨大的突破。**此外，近几年许多 3D paper 和 3D 生成技术都包含了 NeRF 技术或围绕 NeRF 进行研究，NeRF 技术也因此在短时间内不断有突破和进展。因此，从技术路线看，NeRF 是一个值得关注、值得 bet 的方向。

**而 Luma 团队在技术方面绝对称得上是 NeRF 或 3D 领域最头部的玩家之一**，CTO Alex Yu 在学术界口碑非常好，Matt Tancik 参与了最初 NeRF 论文的研究，Quei-An Chen 做过许多非常流行的开源 NeRF 和 3D 项目，团队里的其他科学家也在学术界和产业界有着丰富的 3D 研究经验，团队技术底子深厚，技术有新进展也能很快 catch up，长期保持在行业领先地位。**鉴于 NeRF 和 3D 生成仍处在 research 阶段，团队技术实力强在现阶段非常重要，可以被看作是公司的核心竞争力。**

**2. 社区和数据优势**

与大多数 3D 生成玩家不同，Luma 除了面向 toB，还有一个 toC 的平台，靠 toC 平台起家。用户通过 Luma，使用手机拍摄照片或视频来生成和渲染 3D 内容，这些都是后续训练 3D foundation model 的宝贵的数据。**截至 2023 年 8 月，Luma 在 Discord 的社区成员数量达到 1.7 万名**，这个数字在 3D 领域算是一个 popular 的社区，但和大家熟知的图文社区相比，用户体量依然非常小。

尽管通过手机收集 2D 素材进而生成 3D 内容已经在设备、操作方法、成本上大大降低了 3D 生成的门槛，但目前生成一个 3D 内容需要的时间仍较长，生成质量也不稳定，在当前技术水平下 C 端应用爆发的可能性仍较低。但假设技术持续有进展，门槛持续降低，3D 内容生成质量持续提升，C 端用户和 3D 资产数量有可能迎来一个大爆发。届时 Luma 将处在一个非常好的位置，数据优势也将显现。**数据是目前训练 3D foundation model 的一大卡点，如果能够通过 C 端自发收集 3D 数据，将是一种非常好的低成本收集大量 3D 数据的方式，也会成为公司的一大优势。**

**Concern**

**1. 技术成熟的 Timing**

技术研究和技术进展部分我们有讨论到 NeRF 和 3D 生成目前的技术发展情况。**3D 生成目前仍存在生成质量不稳定、生成速度慢、可生成的场景多样性较差等瓶颈，如果进一步落地到具体商业场景还涉及到设计风格、可编辑的灵活度、如何与现有管线结合或是完全重塑现有管线等一系列问题。事实上，仅是生成质量这一个维度，目前就难以满足商用的需求。**

并且，我们在上文也提到，3D 生成目前有两条相对主流的技术路线：(1) text-to-2D，再通过 NeRF 或 Diffusion 模型完成 2D-to-3D；以及（2）直接 text-to-3D。目前即使是学术界也很难判断哪条路径更有机会。路径（1）在质量和生成速度上能否达到我们想要的效果？路径（2）又是否通过收集足够多的 3D 数据就能实现？有没有可能还需要更底层的架构和算法层面的创新？这些目前都没有答案。而对于投资者来说，我们需要清楚今天投进去的钱更多是用于研发投入，而非是资本效率更高的产品投入或 S&M 投入。研发投入意味着周期长，timing 和回报无法预测。

**2. 商业化**

3D 研发需要大量的资金投入，对于创业公司而言，仅依靠投资机构支持不是长久之计，长期看企业还是需要有自我造血能力。能否自我造血一方面涉及供给端技术的成熟以及需求端的采用程度，另一方面也看团队的产品和商业化实力。

CEO Amit Jain 有创业经历，并在 Apple AR/VR 部门参与过产品研发，在工程和产品方面有丰富的经验。不过从 Luma 团队配置可以看出，Luma 核心成员多为技术背景，产品和商业化人员相对较少。据调研，Luma 团队目前对于商业化还没有特别清晰的路径和思考，而更多聚焦在技术上。**因此，我们现阶段对 Luma 的乐观预期是成为 3D 领域的 Midjourney，而不是 3D 领域的 Adobe。当然，成为 Midjourney 也已经足够好。**

**投资判断**

如果从 venture 或 early stage 角度看，我们认为 Luma 值得投资。如果是追求稳定回报的 growth stage，Luma downside 太大，可能不是一个特别合适的投资标的。

**• 为什么值得投？**

**1. 随着语言、图像、代码等领域的 foundation model 被广泛应用，头部公司或应用已逐渐跑出来，我们也开始期待视频、音频、3D、甚至是机器人领域的 foundation model 的出现。如果我们相信每个模态或领域都会有 foundation model 的机会，那么 Luma 是 3D 领域最有竞争力的创业公司之一**，其他的具有竞争力的玩家多为 Google、Nvidia 等大型科技公司。

**2. 3D 生成是一项具有极强创新性和破坏性的技术。**传统 3D 建模流程繁琐，多为人工手动操作，周期长，成本高。如果 3D 生成技术成熟，现有的管线中的大部分环节将被替代，效率大幅提升的同时，成本大幅下降，想象空间巨大，upside 无限。

**• 关于 Downside**

**我们认为 Luma 目前的 downside 较大**。我们投资技术型创业公司，往往希望 downside 至少是被收购，判断一家技术型创业公司被收购的概率，通常会从以下几个维度考虑：(1) 团队技术实力，以及技术方面是否能一直保持领先；（2）技术实力强劲的大厂 catch up 的难度；（3）其他潜在收购方如平台型、产品型公司的业务协同程度与收购意愿。

Luma 团队技术实力很强，人才质量很高，但目前整个行业还处于早期，和 Luma 竞争的多为技术实力强劲的大公司，人才质量也非常高，核心玩家中暂时没有谁遥遥领先或有差异化优势，不过我们看到 Nvidia 也参与了 Luma 的 A 轮融资。其他潜在收购方如游戏制作公司是否有收购意愿，我们的调研发现这些公司虽然对 NeRF、3D 生成等前沿技术感兴趣，但不太愿意在技术上做过多的投入，而是希望等待技术成熟时直接使用成熟产品。因此，对于 Luma 的 downside，目前很难做出一个清晰的判断，需要持续观察。

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/032.png)

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/033.png)

延伸阅读

[![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/034.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504173&idx=1&sn=ea5f1900311aa117848c492b224efeb9&chksm=ce9b6eb3f9ece7a5fa2715ff5bcfb2b8872b481c809063144e086e7f789eebba3adfe94ea51e&scene=21#wechat_redirect)

Alkira：SD-WAN 先驱再创业，多云网络对 GenAI 关键吗？

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/035.png)

[![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/036.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504129&idx=1&sn=71c27329771d12a401fb28b7bbaa1d8e&chksm=ce9b6e9ff9ece78955e0ce922e3ec34d6b9d170b78608870a2a2e148e358d7a916633c7084d3&scene=21#wechat_redirect)

Anthropic创始人访谈：Scaling与强化学习，可解释性与AGI安全

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/037.png)

[![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/038.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504081&idx=1&sn=62ced4d90fde49343da1c0f88df33e37&chksm=ce9b6f4ff9ece659ab32a97e0baa7103dfc1222ff04041e2bbebd6c6182699a6d91d3f599fb0&scene=21#wechat_redirect)

Netskope：零信任头号领导者，能否颠覆Zscaler？

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/039.png)

[![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/040.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504039&idx=1&sn=1db11c088051ceb00681781bcc9d3b73&chksm=ce9b6f39f9ece62f8836bb1fd5b66e8d5ee616ea614ac7e6b1e5d860897bbdc24aed27156f32&scene=21#wechat_redirect)

Typeface：Adobe前CTO创立的AI营销内容生成平台，1年估值10亿美金

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/041.png)

[![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/042.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503594&idx=1&sn=7962f283bd87e27fc00aa6dd62c8c9ab&chksm=ce9b7174f9ecf862e4040b3a7babac14851f36916bba0fb360d8c4b8dc5f2d34835a62f57751&scene=21#wechat_redirect)

H100 供需分析：芯片战争将持续多久？

![](../images/2023-08-29-luma-aihui-shi-3dling-yu-de-midjourneyma/043.png)
