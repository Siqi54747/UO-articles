---
title: Nile：前Cisco掌门人创立，用AIOps重构千亿企业网络
publish_date: '2023-10-17'
publish_timestamp: 1697544000
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/cCch9UQYsrcWSx2K49AXgA
msgid: 1000000227
appmsgid: 2247505021
itemidx: 1
digest: Nile 希望打造网络界的 AWS，提供完全统一的硬件和服务
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxmz5S8KdX3wvymeE0VibjHtwia4Pws9q8oCicDc9QFojnibPXJUNk3gJWicU0Ouzkj3XtD78qhnrNhKdg/0?wx_fmt=jpeg
image_count: 37
archived_at: '2026-04-20T01:41:36+08:00'
---

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/001.gif)

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/002.png)

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/003.png)

作者、编辑：程天一

排版：Scout

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/004.png)

企业网络的设备（AP、交换机、防火墙、堡垒机等硬件盒子）是一个 1000 亿美元的市场，在此之上还有 3x 的生命周期总运维成本。在云、AI/ML、Pay-as-you-go 等技术和模式充分渗透了计算及存储并带来 AWS 等巨头之后，它们颠覆网络行业的势头才刚刚开始。

**Nile 由担任了 Cisco 20 年 CEO & President 的 John Chambers 及他实质上的二把手、Cisco 的前 EVP & Chief Development Officer Pankaj Patel 创立，致力于于打造企业网络的 Networking-as-a-Service 解决方案。**Nile 希望打造网络界的 AWS，提供完全统一的硬件和服务，在 AIOps 的驱动下接近完全取代客户的运营人力，并且将付费模式转变为订阅制，从而大幅降低企业部署和维护网络的复杂度和成本。

Pankaj 在 2018 年就创立了 Nile，但公司一直处于 Stealth Mode，直到 2022 年中他判断 Cisco 等巨头已经无法抄袭并击败 Nile 所构建的基础设施及解决方案后才脱离隐身状态。**在此之后的一个季度，Nile 拥有了 200 万美元 ARR，2023 年管理层的 ARR 目标是 2000-3000 万美元，目前知名客户包含 Carta、Sprinklr、斯坦福（CS 大楼）等。**

公司目前的估值大约在 15-20 亿美元，8 月公布了 1.75 亿美元的融资由 March Capital 和 Sanabil Investments 领投。**Nile 这一轮的股东主要都是网络安全专家和 MENA 的战略伙伴 —— John Chambers 是全球最懂渠道及合作伙伴销售的管理者之一，他希望让 Nile 打造 Cisco 曾经拥有的合作伙伴网络。**

由于其行业元老级的团队以及远大且清晰的愿景，可以判断 Nile 是网络领域最重要的项目之一，并且是潜在的 Cisco disruptor，值得长期关注。本文详细介绍了 Nile 背后的市场机会以及它给出的具体解决方案，欢迎网络行业从业者添加文末作者微信交流。

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 Why we should care

02 市场机会

03 Nile 的解决方案

04 案例：斯坦福 CS 大楼

05 团队

06 竞争

07 未来：John Chambers 的 GTM 故事

**01.**

**Why we should care**

Nile 完全不是一家 GenAI 公司，它是一家 AI 公司，但技术主要由 ML 而非深度学习驱动。但是其团队背景和它愿景的完美契合仍然值得我们在这个时间点将一部分注意力分给它：

**1. John Chambers 的深度参与。**

John Chambers 是美国科技行业最成功的 CEO 之一，他在 1995 年开始担任 Cisco 的 CEO，到 2015 年卸任，将公司收入从 95 年的 22 亿提升至 492 亿美元，在过程中发明并发扬光大了“Build, Acquire, Strategically Partner”的模型，收购了上百家创业公司，并且将它们在 Cisco 全球伟大的渠道网络中销售出去。他在 2018 年开始成为投资人，创立了 JC2 Ventures，投资了 Spinklr、Rubrik 等明星公司，但只有 Nile 一家 Portfolio 是他选择成为 Co-Founder 并且深度参与公司运营的项目；

**2. Networking-as-a-Service 是个明确的、大的趋势。**

过去 20 年，云和 as-a-Service 模式完全改变了计算和存储，但是网络（具象来看，就是企业员工、学校师生、政府雇员连的 WiFi 网络以及它背后的相关硬件盒子及服务）仍然落后，将 AIOps、云、内置的安全性等元素引入这个领域是明确的机会。同时，这个生意的 TAM 巨大，每个机构的成员都需要上网，企业愿意为员工付出的 ARPU 在 $150-200 级别，学校能够付出的 ARPU 在 $50-100 级别；

**3. Nile 目前的解决方案进展符合它的愿景。**

从已有的进展看，Nile 很踏实和 solid，没有大佬创业不落地或者见光死（Quibi）的问题。在 Day 0（现场勘探、拓扑制造、运输和安装硬件设备）方面，Nile 做出来了 Apple 级别的简洁的硬件产品和 UX。在 Day 1 & n（日常使用和运维网络）方面，Nile 的 NaaS 架构、AIOps、安全性设计的确也很超前，能够提供非常高级别的可用性、容量和覆盖范围 SLA，AI 在满足这种等级的 SLA 中也发挥了决定性的作用。

**02.**

**市场机会**

**Network 非常复杂**

John 和 Pankaj 是 Cisco 的实际运营者，因此他们很明确地意识到了当前行业存在的问题：他们在 Cisco 是 QoQ 的经营，每个季度做财务规划，然后要交付，每个季度都为网络行业增加 incremental 的复杂度。所以他们选择 Nile 这个空白画布来推动 Network-as-a-Service 的下一代产品。

下图阐述了网络层本身的复杂性，在每一层都有多种历史原因遗留的标准/协议，比如 OS 和 Config 层有 Cisco、Aruba、Ubiquiti 针对不同设备、不同历史时期、不同部门的多套标准共存。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/005.png)

在此之外，企业在实际部署及运维网络的每个环节都有挑战：

• 网络规划本身就很困难；

• 后续采购硬件盒子也可能出岔子：比如 COVID 期间等货要多个月但是老设备已经用不成了，或是购买了 Aruba 的交换机和 Extreme 的 WiFi AP，而这是两家公司各自的非王牌产品；

• 安装和运维更是多个维度的困难：比如设置和维护 DHCP、定期更新软件补丁、替换和升级老旧设备、网络分段、为访客网络构建安全性等。

因此大多数组织自行维护围绕网络的 IT 软硬件非常困难，必须依赖外部的 MSP（Managed Service Provider）或者高价雇佣网络方面的专家。在为每 $1 硬件付出的 $3 服务成本的同时往往在网络覆盖、宕机、速度等方面还有挑战。

这里讨论的硬件和我们日常家里用的 WiFi 路由器、光猫的复杂度不是同一量级的，可以参考下面这个视频中的企业级路由器。

**Nile 的市场路线图与 SOM**

Nile 的愿景是提供一套软硬件的 NaaS 解决方案，客户将无需再担心一切。因此它最终的 TAM 是当前交换机、路由器、AP 等设备及服务厂商的收入池子，包括 Cisco、HPE 旗下的 Aruba、Ubiquiti、Juniper Networks 等玩家。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/006.jpg)

在公开采访和闭门的分析师对话中，Nile 的管理者表示其长期目标是 Cisco 占据的软硬件收入池，但是其中短期将聚焦在 Campus WiFi 市场，主打 K-12 及高等教育校园网络以及 Mid-Market 的科技公司办公室/园区网络。下面是对这些细分市场的网络部分的 SOM 测算：

**1. 教育市场**

**1）美国 K-12 学校**

**• Top-Down 视角：**美国大约有 10 万所 K-12 机构，平均每所拥有 500 名以上的师生，这类机构能够为单个师生支付的年度 ARPU 在 $50-100 级别，保守估计单所学校平均可以贡献 3.5 万美元 ARR，整个美国可服务市场规模在 35 亿美元。

**• Bottom-Up 视角：**Chromebook for Education 有 4000 万台量级的设备，必须联网才能正常进行教学活动，按照单设备对应 $50-100 ARPU，市场规模和 Top-Down 视角相同。

**2）美国大学**

美国有超过 5000 所大学，平均拥有超 6000 名在校生，按照 $100 ARPU，平均单所大学可以贡献 60 万美元 ARR，可服务市场为 30 亿美元。

**3）**考虑到 Nile 进入加拿大和 MENA 的决心已经很明显，按照全球其他市场总和和美国的规模相关，**其对应的总可服务市场规模在 150 亿美元左右，如果能做到 40% 的渗透率（管理层的目标，Cisco 在细分品类通常能达到的市场份额），对应 60 亿美元 ARR；能做到 10%，则对应 15 亿美元 ARR 和 2.1 万客户数。**

**2. 科技公司市场**

可服务市场可参考 Zscaler 的客户群体（Mid-Market 及 Enterprise 级别的泛科技公司及 MNC），Zscaler 目前在全球拥有 7700 名客户，按照平均 2000 名员工，Nile 可以获得 $150-200 的 ARPU，平均单个客户能贡献 30 万美元 ARR，**可服务市场为 24 亿美元，做到 40% 渗透率的可能性不低，对应 ~10 亿美元 ARR。**

**Why Now**

Nile 创立的时间点是 2018 年，随后经历了疫情和疫情的退散，目前这个 timing 对它的生意有两个帮助：

• “Return to Office”是比较明确的主题，各种机构和公司有动力焕新办公设备，对园区 WiFi 网络的重视程度开始回升（20-22 年企业管理层的关注重点更集中在 Netskope 所在的 SASE/ZTNA，即让员工在家里能够更方便地连接内网）；

• 过去几年美国的学校校园网络一直事故不断，包括宕机的问题、速度慢的问题以及经常发生网络攻击的问题，Nile 做替换性销售的 win rate 可以比较高。

**03.**

**Nile 的解决方案**

从大面上理解 Nile 的独特之处包括：

• 提供初始的实体勘察（通过 Nile 的合作伙伴）、网络拓扑设计、基础设施布线（从建筑内的光纤怎么走到 AP 的点位及数量如何安排）、设备的安装、修补、网络日常维护以及生命周期内的所有事物；只要客户仍在订阅，Nile 将在设备老化时升级设备并确保从 OS 到软件层都及时更新；

• 提供 3 项有保证的 SLA，包括可用性、容量和覆盖范围；如果有一项 SLA 没有达到，客户可以在下一个账单中获得退款，实时的 AI softbot 将帮助确保 Nile 满足了这些 SLA；

• Nile 通过云端提供 DHCPaaS、零信任访问、网络分段等功能，并且提供一个云上的 Portal 帮助客户的网管或者 WiFi 用户自行配置网络、了解网络实时情况、self-serve 排查问题等；

• Nile 的服务完全是 as-a-Service 模式，完全基于 OpEx（定期付费）而不是 CapEx（一次性支付设备及服务订单）。

**Day 0：简洁和现代化**

**Apple 风格的硬件**

Nile 为客户提供其自行设计和代工生产的盒子，提供无线 AP 和交换机，这些硬件在台湾的 OEM 组装生产。团队遵循了 Apple 的许多产品原则：

• 外形优美简洁，指示灯含义明确，绿色就是正常工作，红色就是掉线，而不像许多 AP 那样有一连串的灯；

• 不提供说明书，不会拼写的高中生都可以安装，只需要扫描 QR 码并且在手机 App 中激活即可；

• 各个盒子都使用相同的 Broadcom 和 Qualcomm 芯片组，并且在芯片及软件中内置了“秘密诀窍”。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/007.png)

**完全 Frictionless 的 Day-0 体验**

客户可以在完全现代化的云端软件上完成跟 Nile 的互动从而安装和部署设备：

1. 首先将教学楼/办公楼地址上传给 Nile，Nile 负责部署的团队就会进行分析和各种资源的盘点；

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/008.png)

2. 客户上传 floor plan 的图纸文件之后，Nile 会继续做勘察和网络拓扑的设计，然后安装服务商会上门安装各种走线和 AP 等盒子，在安装完成后网络用量热点图；

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/009.png)

3. 客户在安装当天可以在线批准各类需要权限的任务，然后需要上门的服务就会自动完成，客户也可以通过手机 App 完全自助式地安装和激活盒子。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/010.png)

**大幅度简化底层的 Config**

Nile 完全承担了网络底层的规划和构建，所以帮助客户大大简化了 Configuration，比如 AP、交换机等盒子之间怎么连接、用什么协议去做通讯、版本如何控制和升级等。在此之上，客户可以在 Portal 里对于具体需要定制的 Configuration 再自行进行调节，比如 DHCP 的控制等。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/011.png)

**Day 1：稳定高性能和安全**

**24/7 网络监控及补救**

在安装和部署完成后，Nile 通过其 Portal 为客户提供 24/7 的实时网络监控。Sprinklr 的这个案例比较具象地显示出 Nile 可提供的价值：

（21 年 10 月 Facebook 陷入史上最严重 7 小时宕机）在员工发现登录不上 Facebook 后，和往常一样，第一个被怀疑的是网络。Sprinklr 内部存在（对Nile 提供的网络的）担忧和压力。然而，尽管看起来不太可能，但 Nile 的 Portal 立即指出 Facebook 是问题所在。作为一家社交媒体营销公司，Facebook 对 Sprinklr 至关重要。几个小时后，Facebook 宣布宕机。

Sprinklr 的全球 IT 总监Foy 表示：“如果 Facebook 瘫痪时我们没有 Nile 的 Portal，我可能会整天不停地循环寻找问题所在。但有了 Nile，我在 Facebook 宣布出问题的几个小时前就知道了原因所在。”

Nile 的客户在日常的网络运维中会充斥着这类问题，比如连不上 Zoom，在缺少 Nile 的情况下需要 IT 员工或 MSP 逐层排查员工电脑网卡、员工网络连接设置、WiFi 网络、ISP 电信公司、Zoom 各个环节是否出现了问题，非常费时费力。

对于网络管理员，Nile 提供一整套系统支持他们实时监控网络情况，并且可以进行 OSI Layer 1 到 7 级别的测试诊断，如果 OSI 模型这几层都没有问题，还可以通过部署的传感器获取更多信息并通过 traceroute 遥控进行更多的测试：

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/012.png)

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/013.png)

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/014.png)

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/015.png)

对于 WiFi 网络的使用者，Nile 也提供界面供他们查看当前的网络情况，并且在出现问题时自行诊断 —— 普通员工也可以发现 Facebook 宕机并第一时间截图跟 IT 部门沟通：

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/016.png)

**底层内置的安全性**

Nile 提供一系列企业级网络必须的安全性，比如：

• SSO 连接（无需更换 SSID）；

• 端到端 MACsec 加密；

• DHCPaaS，Nile 侧的员工也会深度参与原始 RFC，并负责处理所有复杂问题，客户不用再让 IT 人员监视服务器是否分配了重复的 IP 地址；

• 有线和无线的 802.1X 身份验证；

• 零信任访问及网络的隔离等。

其中最后一点有非常大的潜力，并且和我们过去讨论的“零信任”含义略有不同：

• **Nile 提供的零信任及隔离：**在 WiFi 网络层面为不同的设备和用户群组做隔离，没有必要业务联系或权限的用户在分层的内网里；

• **Zscaler/Netskope 提供的零信任（ZTNA）：**指的是用户访问企业内部应用的用例，本质是确保员工访问每个内部应用时有且只有一条 VPN，是 per App VPN for users；

• **Illumio 提供的微隔离：**主要是服务器直接的通讯用例，是 per App VPN for servers。

其工程师对于这部分的架构实现有更详细的解释：

我们自己不提供直接的 NAC 解决方案。由于 Nile 本质上是一个具有加密快速流量传输的零信任网络，因此我们是用户身份验证的中间人，我们将身份验证转发到 RADIUS 或 NAC 解决方案，就像任何传统 NAD 所做的那样。这些同类最佳的安全解决方案向 Nile 发出是/否的访问信号，以及告诉 Nile 如何对待该用户（隔离、生产等）的标准（例如通过 VSA）。根据随身份验证一起返回的属性，我们将用户置于 Nile 客户配置的正确 IP 段中。我们不会检查 NAC 的状态或自行采取行动（尽管我们可以完全阻止某人加入）。

Nile 的客户可以在 Portal 内很方便地构建和管理这样的网络分段：

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/017.png)

**AI：确保满足 SLA**

AI 是实现 Nile 的 NaaS 愿景最基本的支柱，具象来看就是用 AI softbots 替代人类网管和 MSP 的服务人员，这样 Nile 才能以很低的边际成本服务客户并且将原来 75% 的运维成本消减。

Nile 给客户最重要的承诺就是其 SLA，比如保证客户公司员工连接到 Teams 的延迟不高于 90ms、抖动不超过 25ms，并且需要确保网络覆盖全部工位并在 100% 的时间内不宕机。

它实现这一承诺的方法就是基于 ML 实现 AI 的自动化运维：通过规划传感器以及实时通过探针做网络测试，一旦出现网络波动就通过规则和 ML 的手段进行自动化修复。如果无法自动修复和补救，AI 才会判断问题上升到人类参与级别，由 Nile 总部的工程师进行调查并且在极短时间内解决问题。通常 AI 自动解决的问题在秒和分钟级，人类参与的问题解决时长在小时级，因此对于 AI 自动化的确定性和延时要求非常高，这也是 Nile 在这个阶段没有引入深度学习的原因。

**定价：OpEx 替换 CapEx**

在 Nile 出现之前，一个 500 人以上的大楼、办公室或者园区构建其 WiFi 网络的常见做法是购买几十上百个硬件盒子，雇佣 MSP 进行方案设计、部署然后做运维。挑战在于：

• 一次性的 CapEx 支出非常高，IT 团队需要努力争取 CFO 的首肯；

• 很难做到每个工位和办公区域都有高速网络覆盖；

• 后续运维过程中宕机、遭受网络攻击的风险很高，宕机后 24 小时内修复的难度也很大；

• ……

Nile 为客户规划的 5 年 TVL 是希望帮助客户节省 2-3 倍的开支，将 CapEx 转化为 OpEx 以减轻客户的现金流压力，并且消除宕机及入侵带来的损失。

目前 Nile 刚刚脱离隐身阶段，其 Pricing 的逻辑是完全订阅制，但是还在不断调整的过程中，大体的逻辑是根据 per seat + per area 定价。但是在目前的客户身上，Nile 试验了比较多种的定价方式，一些是按照月/年的 per seat 固定费率，另一些则根据 per seat + 具体流量的 usage 情况计费。客户可以选择合同期限，包括每月订阅以及多年订阅，Nile 提供的费率也不相同。

**04.**

**案例：斯坦福 CS 大楼**

斯坦福的 CS 系拥有自己的大楼，拥有 900 台机器组成的高性能计算机集群，为超过 700 名师生服务。这些 IT 基础设施由其总监 Andrej Krevl 及手下的 6 名员工管理和提供支持。在引入 Nile 之前，WiFi 是让他们最头疼的问题。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/018.png)

Andrej Krevl 面临的问题包括：

• 旧的 WiFi 设备情况很糟糕，经常掉线并且很多区域无法连接，讲师往往得找到不依赖 WiFi 的方法上课和开展研究工作，Zoom 通话中也经常卡顿和掉线；

• IT 团队不胜其烦，需要花费大量时间在大楼里奔波以解决网络问题，并且需要经常和用户坐在一起排除故障，过程中 IT 工单不断堆积；

• 用户的新设备在注册使用校园网时需要进行繁琐的步骤，甚至需要下载 App；

• 更新网络设备需要高额的一次性资本支出，并且还需要搭配一名全职员工来管理流程和提供持续的支持。

在使用 Nile 后，他的这些问题都被解决掉：

• Nile 提供的服务包含了始终在线的 SLA，可以让师生不再为连接和性能发愁；

• myNile 可以让 WiFi 用户自行调试连接问题，帮助 IT 团队显著节省了时间和简化故障排除过程，而且 Nile 部署的传感器和 24/7 的网络可见性让 T 团队可以快速确定问题根源。IT 团队为 WiFi 分配的人手从一名员工全职变为他的 4% 的时间；

• 零信任的连接帮助校园网用户平衡了安全和体验，门户内进行 ID 和硬件地址注册即可使用；

• Nile 提供自动软件升级和安全补丁，显著降低了 CS 部门的网络总体支出，并且让员工可以专注于网络支持以外的事情。

**05.**

**团队**

客观来讲，Nile 的团队属于网络行业的老炮，跟硅谷的年轻一代小天才不是一个风格。团队倾向于雇佣那些在安全和网络行业有 20 年经验的人，并且 300 多人的团队中有大量的研发实际上放在了印度。

团队比较自豪的一个数据是：尽管它保持隐身了 4 年，整体离职率只有低个位数。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/019.png)

**06.**

**竞争**

Nile 在它的目标市场（教育以及 Mid-Market 科技公司）没有其他的创业公司作为直接竞争对手，最接近竞争对手的实际上是它的潜在渠道合作伙伴 MSP。一些比较有创新意识的 MSP 在过去几年逐渐开始尝试分期租赁网络设备，提供了类似订阅制的商业模式，但是缺少 Nile 这样下一代架构的软硬件产品。从终局来看，Nile 和 MSP 很可能是共赢而非竞争的关系。

Cisco 仍然致力于高端、大型用户因此短时间内不会和 Nile 证明碰撞。HPE Aruba Greenlake NaaS 是 Nile 最直接的竞争对手，它提供了一种类似 MSP 那样的订阅制模型来售卖设备，因此同样没有 Nile 级别的干净架构和技术，目前也还没有形成 GTM 的势能，还需要观察 Nile 开始大规模对外销售时二者的竞争结局。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/020.jpg)

在科技公司的 SMB 及新经济创业公司领域，红杉投资的 Meter 的构想抽象来看跟 Nile 比较相近，但是二者针对的核心客群有所不同。在手上现金的体量上，Meter 跟 Nile 有一定的客观差距 —— 它 15 年成立，22 年的 B 轮融资拿了 3800 万美元。不过 Meter 整体更受硅谷的新一代圈子推崇，Sam Altman 也是股东，还被 Tishman Speyer 战略投资以进入其新建筑中。Meter 的产品非常简洁和标准化，但是拓展到教育客户和非新经济型科技公司的能力有待考察。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/021.png)

**07.**

**未来：John Chambers 的 GTM 故事**

目前 Nile 的客户能看出 John Chambers 介绍了不少 Portfolio 和相关资源，他们都相当于首批测试客户。在它们之外，Nile 的目标是完全通过渠道和合作伙伴进行销售，它在脱离隐身模式时就签了 57 个合作伙伴，比如 World Wide Technology（全球最大的技术集成商之一），已经跟这些合作伙伴完成了培训等待铺开。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/022.png)

Cisco 通常被视作全球通过渠道和合作伙伴销售最成功的公司（软件领域类似的玩家是微软），在全球 100 多个国家和地方跟各个行业和政府都有对应的渠道伙伴。它收购的创业公司往往能够在 12-18 个月的时间内 ARR 从数亿美元跃迁到几十亿美元，核心就在于这个强劲的渠道网络。从国内视角来看，最接近的类比是华为和它的经销商们。

网络安全领域的公司除了 Zscaler 之外没有以渠道见长的，Crowdstrike 招募了 SentinelOne 的前 CMO 来增强渠道，Palo Alto Networks 近几年也是积极投资于这一点，今年打出的 show-case 是一家 MSP 在跟 Palo Alto Networks 签约的第一个月就获得了一个 1000 万美元级别的客户，也侧面说明了这些公司过去对于渠道潜力挖掘的不足。

John Chambers 是对构建渠道合作伙伴的 Know-How 和人脉资源最深的人。从最基础的细节就可以看出：

Nile 招募渠道伙伴的页面非常强调“高两位数分润”、“正向现金流”、“co-sell”等关键词，证明对经销商的心理理解很深，主打“共赢”和“一起赚钱”。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/023.png)

这些元素在 Crowdstrike 和 Palo Alto Networks 的相关页面中就没有出现在最醒目的位置，甚至很难找到：

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/024.png)

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/025.png)

总体而言，目前 Nile 在 GTM 层面所讲的渠道故事非常合理且有希望，但是可能仍然需要 1-2 年的时间来验证是否有效。但如果 Cisco 的渠道机器有望被复制出来，Nile 有机会完成一个非常陡峭的 ARR 增长曲线。

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/026.png)

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/027.png)

延伸阅读

[![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/028.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504973&idx=1&sn=603596db2a31e1e53d71ac05d775cb7c&chksm=ce9b6bd3f9ece2c577720045239314840757fa578587f4a5adbf21e18a9dadd6bf1af3913b61&scene=21#wechat_redirect)

AI Agent的千亿美金问题：如何重构10亿知识工作职业，掀起软件生产革命？

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/029.png)

[![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/030.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504914&idx=1&sn=5c932e52d662b44d47853f1b35a38ba7&chksm=ce9b6b8cf9ece29ac8f6ab548ee87ae6ae9be9f5948fb5c60fe2de92e3203ec6854279d339a2&scene=21#wechat_redirect)

Sambanova：前瞻的芯片能匠，软硬结合抢滩企业LLM Serving

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/031.png)

[![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/032.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504850&idx=1&sn=586f2fe41859f2685054d921c093ff95&chksm=ce9b6c4cf9ece55a33436461c257f753d526730024dec33abd93adc1de86e31f03a7e2cd37c5&scene=21#wechat_redirect)

Synthesia: AI Avatar的PMF样本，像PPT一样做视频

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/033.png)

[![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/034.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504793&idx=1&sn=ddcd5c58f353281d07f30f15daca9080&chksm=ce9b6c07f9ece51127cb6db1d2ae0395ba236a7f263e8138722e927facf88f834688f663927f&scene=21#wechat_redirect)

GenAI云计算百亿角斗场，算力之外的错位博弈

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/035.png)

[![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/036.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504471&idx=1&sn=108970a82e8ffba8b648fe3eea9eb523&chksm=ce9b6dc9f9ece4dfe52bdf89524c3b1adfef27277e996b7d012b0a95247b493a2d48bdef82b6&scene=21#wechat_redirect)

11Labs：声音模态能否突围OpenAI？

![](../images/2023-10-17-nile-qian-ciscozhang-men-ren-chuang-li-yong-aiopszhong-gou/037.png)
