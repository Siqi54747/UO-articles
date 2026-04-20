---
title: Alkira：SD-WAN 先驱再创业，多云网络对 GenAI 关键吗？
publish_date: '2023-08-25'
publish_timestamp: 1692964800
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/nfm0mvkJS_A9gre3SKr7jQ
msgid: 1000000218
appmsgid: 2247504173
itemidx: 1
digest: Alkira 处于网络即服务与多云网络的交汇点上
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzicemUO22w5g3sia4pTngplkOiaBYich275fOiaicwvibaBwrTeGMSwoHxwDQkKibN8dQ69HiaozT1R6iaEzcQ/0?wx_fmt=jpeg
image_count: 34
archived_at: '2026-04-20T01:30:06+08:00'
---

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/001.gif)

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/002.png)

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/003.jpg)

作者、编辑：程天一

排版：Mengxi，Scout

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/004.png)

Cisco 是红杉资本在硅谷的重要成名作之一，在过去几十年里为全球的网络提供了基础设施，让互联网的蓬勃发展成为可能。但是网络行业本身没有继续成为 VC 回报的最大来源，甚至成为一个被视作极少有创新发生的地方。

Alkira 的两个创始人 Amir Khan 和 Atif Khan 连续投身了两波网络领域的罕见创新，在 2011 年创立了 SD-WAN 的先驱 Viptela，迅速成为市场领导者，在 2017 年被 Cisco 以  6.1 亿美元收购，随后在 2018 年又投身 Networking-as-a-Service 与多云网络的交汇处，创立了 Alkira，以完全 NaaS 化的方式交付多云网络。

**吸引我们在这个时间点关注 Alkira 的核心原因有两个：**

• 随着 Alkira 和 Nile 等前 Cisco 系高管的创业公司逐渐向外界披露其架构愿景并且拿到客户，**我们看到了这个固化的领域出现新涟漪的可能性。**

• 随着 GenAI 的公司们崛起，**云与云、云与数据中心、数据中心与数据中心的网络互连以及安全保障也可能迎来变化，可能会被 Alkira 这一类更具创新能力的供应商抓住机会。**

Alkira 在 2018 年成立，拿了 3000 万美元的融资后花了 2 年时间打造全球的云交换点基础设施，2020 年才面向市场推出产品，目前已经拿到了 S&P Global、Koch、华纳音乐集团等在全球拥有几十个数据中心的大型企业客户，不管是产品力还是 Go-To-Market 的能力都非常亮眼。本文详细介绍了 Alkira 的团队背景、行业格局以及产品组合，欢迎对网络领域有钻研的从业者添加作者文末微信进行更深入的探讨。

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 市场机遇：NaaS 和多云兴起

02 大型企业的挑战：以华纳音乐集团为例

03 Alkira 如何解决 Multiple-Cloud Networking

04 竞争格局：Cisco 系创业公司内战

05 团队：SD-WAN 开创者再创业

06 未来：LLM 时代的 Networking 需求

**01.**

**市场机遇：**

**NaaS 和多云兴起**

Networking 是“互联网投资”的起点，Don Valentine 时代红杉资本最重要的项目就是 Cisco，**但是 40 年过去后，这一领域已经成为一个接近完全固化的领域：**

Cisco、Juniper、Aruba、华为等几十年历史的公司提供着硬件盒子，将有可能颠覆它们的潜在浪潮在早期就通过 M&A 吞并掉；每个国家的头部运营商也几乎没有变化，NTT、中国联动、Organge、AT&T、Verizon 们提供着通信运营服务。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/005.png)

SD-WAN 曾经被视作一个转机，可以让软硬件解耦，从而使网络也可以像计算和存储一样敏捷。它发生的背景是大型企业们在过去拥有自己的通信基础设施，通过昂贵但 SLA（服务等级协议，定义了服务类型、质量及赔付标准等）很好的 MPLS 专线来连接总部和跨地区的分支机构。随着互联网出现，更便宜同时还很高速的连接来临。Viptela 作为 SD-WAN 的先驱在 2011 年创立，试图帮助企业简化其网络运营，让语音通话等对延迟要求较高的服务继续走 MPLS，但是将另一些流量导向互联网，并提供相应的安全性。

但是这一浪潮没有像大家预期那样颠覆通信巨头们，Viptela 最终以 6.1 亿美元在 2017 年卖身给 Cisco，让 Cisco 成为了 SD-WAN 的领导者。SD-WAN 的 300 亿美元 TAM 和 80 亿美元的可服务机会一直存在，但是由于我们在 Netskope 文章中分享过的替换成本及周期等原因，一直渗透缓慢。**因此这个领域也已经走向集中，仍然由老牌厂商占据主要市场份额，独立的领头供应商只剩下 Versa Networks 一家。**

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/006.png)

在将 Viptela 卖给 Cisco 之后，这家公司的创始人 Amir Khan 在 2018 年创立了自己的下一家公司 Akira，站在了 Multi-Cloud 和 Networking-as-a-Service 两大主题的重合点上。

Networking-as-a-Service 是一个在 2010 年左右被提出的概念，最终是一个围绕 Cisco 的叙事 —— 鉴于 AWS、Azure 等公有云在当时都还远未成熟，投资者们试图押注 Cisco 可以做成一朵云，直接帮助客户把他们本应购置的 Cisco 硬件都管理起来，从而免除自行部署和运维的麻烦，但是 Cisco 的管理层一直没有执行和实现这一愿景。

**尽管 Cisco 没有成为想象中的云赢家，NaaS 这一概念（即像云计算和存储那样帮助客户管理其网络基础设施）仍然被巨头和创新者们拥抱。**在发展了十几年后，NaaS 目前的主要玩家格局已经比较清晰，大致有几大流派：

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/007.png)

其中最后两个领域是我们观察到创新发生的地方，**我们列出的 4 家公司都仍处于一级市场和创业阶段，并且创始人大都是 Cisco 的高管。**

**本文首先聚焦在多云和混合云为 NaaS 带来的机会上：**

如果一家公司将一个应用只部署在 AWS，另一个只部署在 GCP，那么它处于多云（Multi-Cloud）状态。另一种情况是它将同一个应用同时部署在 AWS 和 GCP，某些情况下甚至还会在本地数据中心，则它处于混合云（Hybrid Cloud）状态。目前来看，多云和混合云的架构已经成为了大型企业上云的主流。

一旦企业希望多个云以及云和数据中心之间实现互连，这种做法为网络层引入了巨大的复杂度，因为每个云内部的通信网关、负载均衡器等组件都不同，企业还需要 DIY 大量围绕流量路由、BGP、NAT、防火墙的规则。如果涉及到数据中心和云的连接，还需要去购置网络设备安装在数字中心，并且在 Colocation 的机房进行连接层的部署。这一过程往往需要 3-6 个月进行规划和 POC，3-6 个月进行实际安装和部署落地。

Akira 和 Aviatrix 这样的公司观察到了云的起势，并且发现了网络层的问题并没有像计算和存储那样被解决，**现有的解决方案缺乏端到端的基础设施控制能力、网络隔离和分段能力、快速扩展基础设施、容灾及恢复能力，因此打造了一套可复用的 Cloud-Networking-as-a-Service 基础设施，以完全 SaaS 化的方式交付，让客户能在几分钟内构建和部署安全的全球云网络。**

根据 MarketsAndMarkets 的报告，这一市场目前在 27 亿美元体量，有机会在 5 年内成为一个 76 亿美元的市场，主要玩家可以参考本文中的竞争格局部分。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/008.png)

**02.**

**大型企业的挑战：**

**以华纳音乐集团为例**

如果你是一家完全处于云上的创业公司，可能完全无法想象大型企业在多云和混合云上遭受的挑战 —— 以 Alkira 的客户 S&P Global 为例，它在全球拥有超过 4 万名员工，管理着 50 个数据中心，并且同时使用 3 朵云，每年为 Alkira 贡献百万美元级别订单，并且缩减了大量的成本。

**大型企业陷入这种复杂度的原因有很多种：**

• 为了避免 vendor lock-in 和建立容错能力而使用多朵云；

• 处于数据安全等因素仍然不能将核心敏感业务从本地数据中心迁移到云上；

• 过去构建了自己的数据中心，因此虽然进行了云迁移，但是仍然有工作负载运行在本地；

• 频繁的 M&A 在全球各地引入了不同的云和遗留的数据中心；

• 仍希望将前后端分离，通过将后端的一部分调用保留在本地以降低云账单；

• ……

华纳音乐集团是 Alkira 的早期重要客户，可以更直观地体现出这种复杂度：

由于华纳悠久的历史，它在几十个地区的办公室用着完全不同的电信运营商，分配了不一致的网络管理策略和人员，每个网络环路计入预算和最终计费的方式也不一样。与此同时，它的业务又一直在增长，需要新开办公室以及进行 M&A，这一套云和本地混合的网络几乎无法被管理。IT 团队在这种混乱中观察到了云和大数据的潜力，因此希望做出改变。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/009.png)

**除了技术层面的分散和割裂，对网络的管理也散落在各个团队手里，IT 设备管理团队、网络团队、安全团队、云团队各自负责一摊事**，给网络的集中管理和可见性也带来挑战。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/010.png)

**华纳音乐集团的诉求是一个统一的网络环境、大型企业级别的云网络质量以及配套集中的管理与治理。**它 POC 了多家多云通信厂商，最终选择 Alkira，核心原因在于其端到端的连接、集成的安全能力以及提供对网络的可见性。它不需要自己购买任何硬件盒子，只需要在 Alkira 的 UI 中无代码拖拽并且设置 Intent-Based-Policy 就能完成设置。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/011.png)

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/012.png)

**这一套操作最终实现的是敏捷性、网络性能、成本、安全性的全面提升。**

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/013.png)

**03.**

**如何解决****Multiple**

**-Cloud Networking**

**技术架构**

Alkira 在 2018 年创立，从 KPCB 和 Sequoia Capital 等早期支持者手上拿了 3000 万美元，但是向市场推出第一个产品的时间是 2020 年，**核心原因就是其整套技术设想需要十几个月的时间来实现。**

在没有 Alkira 这类解决方案以前，企业也可以通过 AWS Direct Connect/Private Link、Azure ExpressRoute、GCP Dedicated Interconnect 等方式 DIY 实现多云网络以及云与本地数据中心的连接。

尽管下图的架构看起来很简洁，但是企业在多个云上都有不同区域的上千个个 VPC，复杂度是华纳音乐的架构示意图种的密密麻麻的线条。**因此不论是在 Colocation 还是云上自行管理这些连接以及相关的防火墙、负载均衡器等服务，都需要非常复杂的配置，并且由于需要流量以固定的方式编排或是来回传输，很容易出错或是达到性能瓶颈。**

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/014.png)

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/015.png)

**因此 Alkira 在底层构建的基础设施是一个 Cloud Services Exchange，提供 Cloud Exchange Points，发挥一个中间层的交通枢纽作用，为各个云环境之间建立快速且可靠的连接，并且实现数据的传输和跨云的互操作性。**客户不再需要自行购买各种硬件盒子并且配置复杂的交换器，因为 Alkira 已经在背后实现了这一切，并且以 NaaS 的形式交付。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/016.png)

**用例**

有了 Cloud Services Exchange 的基础设施之后，Alkira 可以发挥用处的一些常见用例包括：

**在多个云上拓展网络和安全性**

通常在业务的初期，公司很难感受到对多云网络的需求急迫性，因为它们通常仅在单个地区使用一朵云。但随着业务扩张，它们很可能会遭遇突然有一波新增用户流量，但是没有做好扩容准备，服务直接被冲垮。另一种情况是运营这个网络的人可能突然离职了，整个公司失去了对自己云网络的知识。**因此在早期就引入 Alkira 这样的中间网络和安全层也是有必要的。**

对于大型企业客户，它们几乎不可能停留在单个地区的一朵云上，不管是自然增长还是 M&A 都会将它们导向多个地区的多个云上。使用 Alkira 来连接这些云、进行网络的隔离和分段以及架设防火墙可以大大减少 DIY 和运维的成本。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/017.png)

**M&A、合作伙伴、IoT 设备所需的外联网**

这是 Alkira 的 CTO Atif Khan 经常提到的一类用例，S&P Global 这样的客户在全球范围内有上千个合作伙伴，都需要能够接入 S&P 的网络以进行指数业务的协作。在没有 Alkira 的时代，它需要几个月的时间才能将一个合作伙伴引入网络。现在它可以用几小时取代过去几个月的工作量。

当试图将二者的网络连接到一起，直接打开网络的大门会导致各种病毒、勒索邮件以及 IP 和端口号级别的攻击进入。因此往往需要等待 IT 团队花费时间检查一切。**但是通过 Alkira 来将网络分段为两个隔离的段 M&A Segment 和 Corporate Segment 就可以在保证安全性的同时将两者敏捷地连接起来。在两个段之间，也可以使用 Alkira 直接设置云端防火墙。**

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/018.png)

**WAN/Backbone-as-a-Service**

尽管 Alkira 的创始团队有 SD-WAN 的经验，但是 **Alkira 本身并不提供 WAN 能力，而是基于云厂商的高性能、高带宽、低延迟、低丢包率、全球的骨干网能力来帮助客户将分支机构、数据中心、远程用户互相连接起来**。客户想要替换 MPLS 但是没决心上 SD-WAN 的话，Alkira 的这个骨干网服务也是可用的 WAN。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/019.png)

**替换 Colocation**

尽管 Colocation 还可以提供托管的计算和存储等能力，但是的确有一部分的大型企业使用它们来将数据中心和云的网络连接在一起，通过私有的光纤将彼此互联。**但是如果企业有上云的更大决心，Alkira 的基础设施可以完全取代掉这些缝缝补补的私有连接。**

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/020.png)

**走向市场**

得益于创始团队在 Viptela 的经验，Alkira 的 Go-To-Market 实践非常亮眼，主要依赖了两个抓手：

**1. 猛攻大客户**

尽管 2018 年才成立、20 年才推出产品，Alkira 已经顺利拿到了 S&P Global、华纳音乐集团、Koch、Tekion、Chart 等大型客户。作为对比，2014 年就成立了的 Aviatrix 在很长一段时间内只有 Netflix 这一个大型客户。

**2. 积极和合作伙伴构建集成**

Alkira 和企业的云、安全以及 DevOps 堆栈中最重要环节的核心公司进行了深入的技术集成和战略合作，支持 AWS、Azure、GCP、Oracle 等云，与 Cisco、Infoblox 等网络厂商合作，积极白标 Palo Alto Networks、Fortinet、Check Point 等防火墙，还跟 ServiceNow、Terraform 等 IT 及 DevOps 重要工具进行了深度集成。

**同时，Alkira 还拥有真正云原生的商业模式，根据网络消耗量来定价，不用的时候不收费。**通常一家 S&P Global 级别的客户每年需要在 Alkira 上支出超过百万美元，一家 Mid-Market 级别的公司每年需要在 Alkira 上支出 30-50 万美元。

**04.**

**竞争格局：**

**Cisco 系创业公司内战**

Alkira 主要有以下几类竞争对手：

**1. 老牌网络设备厂商或通信运营商提供的多云网络服务：**

Cisco Secure Agile Exchange 和 AT&T Netbound for Cloud 算是这一类服务的代表。这类解决方案虽然也能提供云到云、云和本地数据中心直接的连接，但是缺少 Network-as-a-Service 的属性，客户仍然需要自行处理许多路由逻辑，并没有从根本上简化网络运营；

**2. 云厂商提供 Transit：**

包括 AWS Direct Connect/Private Link、Azure ExpressRoute、GCP Dedicated Interconnect 等，它们都提供了能力帮助企业将私有数据中心连接到云的能力，但是同样缺乏 Network-as-a-Service 的属性，并且几乎只为自家云工作，没有提供先进的云到云连接。如果客户处在多云环境，他们需要面对每个云的 Transit 在配置项上有诸多不同的情况。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/021.png)

**3. 多云网络领域的创新创业公司们：**

**Aviatrix：**一家 20 亿美元估值的多云网络公司，由 CRV 和 General Catalyst 主力支持，2014 年成立时的价值主张是“云上的路由”，由 Cisco 的工程经理 Sherry Wei 创立，拥有接近亿美元级别的 ARR。在 21 年上半年以前，Alkira 能够进入的 POC 中往往也会有 Aviatrix 存在，Aviatrix 的胜率更高，因为其产品和客户支持更加完善，但这正随着 Alkira 的产品成熟而发生改变。

在产品细节上，Alkira 和 Aviatrix 互有优劣，比如一些客户指出：

• **Aviatrix 提供 IP 重叠的解决** —— 每个区域的 AWS 环境本来已经分配了一个 IP 范围，但是可能由于某些原因数据中心和云之间有重合的 IP 范围，当尝试连接这两个网络，就会报错说无法在不同网络中拥有相同 IP。Aviatrix 可以尝试创建一个掩码或者二级 IP 来完成链接并给出警告和解决方案，而 Alkira 没有 IP 重叠的这个功能；

• **Alkira 和 Aviatrix 的核心差异在于 Alkira 帮助简化了配置和管理所有功能的过程**，Aviatrix 仍然需要培训员工进行管理然后亲自追踪不同的云和数据中心的动态，需要了解每个公有云上的特定术语以及它们提供的互连服务的特点，而 Alkira 在此之上可以提供托管服务，客户可以自行选择便利度和灵活性；

• **Aviatrix 唯一的问题是不提供防火墙能力，而 Alkira 提供防火墙能力**，客户无需自己购买，而是获得白标的 Palo Alto Networks 的云端防火墙，并且同样也是 pay as you go 模式计费。

• ……

**F5：**93 亿美元的上市公司，以售卖 F5 硬件设备作为网站或应用的负载均衡器出发，收购了大名鼎鼎的 Nginx 以提供 HTTP 软负载均衡。F5 的优势在于旗下解决方案完善，不光售卖多云网络的必要产品，还提供 Bot 防护、负载均衡器、防火墙等产品，但是更希望捆绑交易，因此定价昂贵。

**Prosimo：**由 Viptela 的创始团队成员和 VP of Product 创立，同样致力于多云网络，但声势上明显弱于 Aviatrix 和 Alkira。

**05.**

**团队：**

**SD-WAN 开创者再创业**

Alkira 由 Amir Khan 和 Atif Khan 兄弟俩创立。Khan 兄弟算是巴基斯坦裔在美国成功创业的典范。**但是他们身上更大的传奇在于其创立的上一家公司 Viptela。**

Viptela 在 2011 年开始做，12 年中拿到融资，当时世界上还没有 SD-WAN 这个概念。在随后的 1 年里，很快出现了 4-5 家 VC 支持的 Viptela 竞争者。到了 2015 年前后，由于云和 SaaS 被广泛地接受，SD-WAN 开始被各大 CIO 关注，Viptela 仍然保持着市场中领导者的地位。

Viptela 这段经历充分显示出 Khan 兄弟的一些闪光点：

**• 富有愿景：**成为了 SD-WAN 的先驱，而不是滞后于这一概念的追逐者；

**• 拥有创业者精神：**尽管已经在 Cisco 和 Juniper Networks 做到了 Senior Director 级别，Khan 兄弟出来创业时仍然非常接地气地构建自己的 MVP，第一个 WAN 的实现是去 Cellular 商店中买了一个 WIMAX modem 路由器并且在此之上尝试组网；

**• 极强的大客户销售能力：**尽管直面 Cisco 等老牌竞争对手，Viptela 拿到了大量的大型企业客户，第二个客户 PNC Bank 甚至在 POC 中直面击败了 Cisco，最终在这一个客户的 2750 个支行里部署了 5500 个网络设备；

**• 对股东和员工负责：**为了在好的时机给大家好的回报，最终在 2017 年以 6.1 亿美元的价格将 Viptela 出售给 Cisco。

类似的特质在 Alkira 这段创业经历上再次表现出来。Alkira 在 18 年的首轮融资由 Sequoia Capital、KPCB 支持，**其中 KPCB 的董事席位是其掌门人 Mammon Hamid，他也是我们看好的 Netskope 最重要的早期投资者之一。**

在 2020 年的 5400 亿美元 B 轮融资中，Alkira 将其客户变成了领投方 —— Koch Disruptive Technologies 领投了这轮融资，背后的原因是 Koch 这家 1150 亿美元年收入、在全球 70 多个国家和地区经营并且拥有 13 万名员工的大型企业使用了 Alkira 重建云骨干网并拓展到多云，在过程中亲眼目睹了 Alkira 如何帮助大型企业简化其网络向云过渡的旅程。

**06.**

**未来：****LLM 时代的**

**Networking 需求**

吸引我们关注 Alkira 的近期催化剂是 GenAI 的兴起 —— 主流的 GenAI 公司普遍展现出复杂的混合云架构，不光使用公有云，还在搭建自己本地的数据中心，从 Stability AI 到 Mistrael AI 都在试图对数据中心拥有更大的掌控力和灵活度。

有点体量的模型与应用一体的公司普遍已经拥有自己的数个数据中心，需要根据机器空闲和用户距离等策略来进行网络的调度。如果不使用 Alkira 这样的基础设施，就需要自己花费几周时间来 DIY，正处在单地区单云的复杂度阶段，一旦继续拓展地区和增加云的复杂度，网络相关的运维难度又会上升。

**在长期，鉴于 LLM 明显的延迟问题，我们相信成功的 AI 公司应该在全球各个大区都有 3-4 个数据中心，避免让网络的性能再增加额外的延迟。如果这一未来到来，将不同洲之间的数据中心与数据中心、数据中心与云的网络互相连起来也非常有难度，可能有 Alkira 这类供应商的机会。**

同时，从客户视角来看，仍然有相当大比例的客户在跨云和私有基础设施使用 GenAI，这也隐含着多云网络的大趋势。

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/022.png)

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/023.png)

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/024.png)

延伸阅读

[![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/025.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504129&idx=1&sn=71c27329771d12a401fb28b7bbaa1d8e&chksm=ce9b6e9ff9ece78955e0ce922e3ec34d6b9d170b78608870a2a2e148e358d7a916633c7084d3&scene=21#wechat_redirect)

Anthropic创始人访谈：Scaling与强化学习，可解释性与AGI安全

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/026.png)

[![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/027.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504081&idx=1&sn=62ced4d90fde49343da1c0f88df33e37&chksm=ce9b6f4ff9ece659ab32a97e0baa7103dfc1222ff04041e2bbebd6c6182699a6d91d3f599fb0&scene=21#wechat_redirect)

Netskope：零信任头号领导者，能否颠覆Zscaler？

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/028.png)

[![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/029.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504039&idx=1&sn=1db11c088051ceb00681781bcc9d3b73&chksm=ce9b6f39f9ece62f8836bb1fd5b66e8d5ee616ea614ac7e6b1e5d860897bbdc24aed27156f32&scene=21#wechat_redirect)

Typeface：Adobe前CTO创立的AI营销内容生成平台，1年估值10亿美金

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/030.png)

[![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/031.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503594&idx=1&sn=7962f283bd87e27fc00aa6dd62c8c9ab&chksm=ce9b7174f9ecf862e4040b3a7babac14851f36916bba0fb360d8c4b8dc5f2d34835a62f57751&scene=21#wechat_redirect)

H100 供需分析：芯片战争将持续多久？

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/032.png)

[![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/033.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503539&idx=1&sn=b3c54e6cadd70072269ac1a7478988d4&chksm=ce9b712df9ecf83bd5a5b465311ed483a4a4a554e9b1f5dece94621dee4451b748f3e9d0e8a3&scene=21#wechat_redirect)

Harvey：OpenAI投资的法律Copilot，最适合LLM落地的垂直行业

![](../images/2023-08-25-alkira-sd-wan-xian-qu-zai-chuang-ye-duo-yun-wang-luo-dui-ma/034.png)
