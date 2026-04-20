---
title: Netskope：零信任头号领导者，能否颠覆Zscaler？
publish_date: '2023-08-17'
publish_timestamp: 1692273600
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/ObBASaet6SVIvlRVXY2z0Q
msgid: 1000000216
appmsgid: 2247504081
itemidx: 1
digest: 一级市场最重要的安全独角兽之一。
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxX7YoAhnEZdozWcAsno6GQW5o1Sa6XIeD5lMAX0kZdwjVEJQaKSp9LibLwkr05USuBcmeQwqhw2Gw/0?wx_fmt=jpeg
image_count: 31
archived_at: '2026-04-20T01:28:15+08:00'
---

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/001.gif)

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/002.png)

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/003.jpg)

作者：程天一

排版：Scout

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/004.png)

随着 SaaS 的普及、企业数据的爆发增长以及全球招聘与混合办公的兴起，传统网络安全（Network Security）依赖防火墙、堡垒机、VPN 组成的“堡垒与护城河”防护已经很难奏效，不光容易被攻破，性能也很难满足要求。

试图解决这一问题的厂商通常会被纳入 SASE 的范畴内。这个单词代表着过去 10 年我们见证的安全和网络的一系列演进：

SWG 从硬件盒子走向 Zscaler 引领的云交付模式；BeyondCorp 概念被提出，ZTNA 则很快进入每一个 CIO 和 CISO 的视野；CASB 帮助企业更安心地使用在云上的 M365、Salesforce、Box 等 SaaS；SWG、ZTNA、CASB 与云上防火墙的融合与统一交付成为大势所趋；SD-WAN 与这些安全产品的分分合合，SASE 最终被 Gartner 拆分为提供网络能力的 SD-WAN 与提供安全能力的 SSE……

最优秀的一批安全厂商都在 SSE 领域厮杀 —— Broadcom、Fortinet、Palo Alto Networks、Zscaler、Cloudflare 在内的老牌玩家希望捍卫优势或现金流，Netskope、Cato Network、Perimeter 81、Tailscale 等新兴公司则各自有独特的价值主张和对下一代架构的愿景。

**在群雄逐鹿这个 35% CAGR、150 亿美元市场的过程中，Netskope 先后完成了在 CASB 和 SSE 两个红海战场的逆袭，在 2023 年成为了 Gartner SSE 魔力象限的头号领导者，成为了一级市场最重要的安全独角兽之一。**

讲清楚 Netskope 背后的技术架构和完整的 IT 趋势需要更大的篇幅，因此本文主要从投资者视角出发，将内部 Memo 脱敏化简发布，更简明和通俗地讲述 Netskope 身上独特的竞争优势，希望帮助广大安全投资者和爱好者对 Netskope 增加更多了解，也欢迎专业的安全从业者添加我在文末的微信进行更多交流。

\* 鉴于许多读者可能没有网络安全的行业基础，在此对本文中的安全概念进行一个简单科普：

**• SASE：**安全访问服务边缘，SSE + SD-WAN。

**• SSE：**安全服务边缘，SWG + CASB + ZTNA + FWaaS。

**• SWG：**Web 安全网关，用来检查和控制互联网流量，组织网络威胁和数据泄露。

**• CASB：**云访问安全代理，帮助企业员工安全地使用 SaaS，防止出现影子 IT 和数据泄露。

**• ZTNA：**零信任网络访问，可以替换传统的企业 VPN，在授权每个用户和设备访问内部资源之前对其进行严格的验证。

**• FWaaS：**防火墙即服务，即云交付的防火墙，企业无需再自行维护硬件盒子。

**• SD-WAN：**顶软件定义广域网，供应商帮助企业在 MPLS、互联网、LTE 等网络线路中进行优化选择。

**• PoP：**入网点，处于企业网络边缘的接入点。

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 Thesis

02 什么是 Netskope

03 走向真正的 SASE

04 商业化进展

05 结论

**01.**

**Thesis**

Netskope 是一级市场最重要的成长期网络安全资产之一，也是安全投资者们非常期待在不久后 IPO 的明星公司。在持续追踪研究后，我们基于以下原因对 Netskope 的未来前景非常看好：

**1. SASE（SSE + SD-WAN）赛道仍然处于黄金增长期，Gartner 预计其市场将以 35% 以上的 CAGR 在 2025 年增至 150 亿美元。**

疫情显著提升了客户对完整 SSE 套件的需求，各家供应商产品也走向成熟，在争夺客户的过程中展现出产品、架构愿景、网络性能和 Go-To-Market 上的明显梯度分层。Netskope 目前成为 SSE 市场的领导者；

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/005.png)

**2. 整合分散的安全供应商是各大 CISO 的明确任务。**

目前平均每个大型企业需要购买 76 个安全工具，并且以接近 20% 的速度增长，因此之前 SSE 下 SWG、CASB、ZTNA、FWaaS 单独向最佳供应商购买的情况正在转变，CISO 逐渐更倾向于向同一家供应商采购。CASB 在 23 年初成为了 CISO 最高优先考虑的产品（20 年以前为 SWG，目前逐同质化；疫情期间为 ZTNA），而 Netskope 的 CASB 和 DLP 能力处于绝对领先位置；

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/006.png)

*（横轴越靠前代表进入 POC 的概率越大，纵轴越靠上代表 POC 中胜出的概率越大）*

**3. Netskope 以 CASB 起家，但是目前已经布局非常完善，团队能力也很优秀，没有明显短板。**

创始人 Sanjay 此前是通信巨头瞻博网络的 VP 及安全事业部 GM，对安全和网络的理解都很深，在 19 年及时招募了 AWS 负责 Network Infra 的 SVP，一年时间构建起了 100Tbps  网络带宽的全球 PoP 基础设施。Netskope 之前在 Marketing 上没有 Zscaler 强势的弱点也被 Gartner 魔力象限的突破补足，年初以来各类销售线索激增；

**4. Netskope 通过 SD-WAN 布局显著扩大了 TAM，和 Zscaler 走向战略分化。**

Netskope 在 2022 年收购了由 Velo Cloud 早期团队创立的 SD-WAN 厂商 Infiot，将无边界 SD-WAN 服务添加到了产品组合中，而 Zscaler 暂时还没有明确的 SD-WAN 进展，市场上也已经没有接近 Infiot 质量的标的可供收购；

**5. AI 及 LLM 的一系列进展是 Netskope 拓展业务很好的催化剂。**

我们之前在[**云之后，大模型是网络安全的新机会吗？**](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247501647&idx=1&sn=e555f31970ad9bd4a03e66cf4b7a9391&chksm=ce9b78d1f9ecf1c7fc466ad5edf096e47baec211a0877fa9b7bb62d57bec3f1e4106a800b236&scene=21#wechat_redirect)一文中详细讲过 LLM 时代 CISO 对于使用 ChatGPT 这类产品的数据防泄漏需求。此外，如果 LLM 的延迟以及成本问题能够迎来突破，Netskope 强势的 DLP 引擎可以将传统机器学习和语义搜索的技术快速叠加上 LLM 完成升级；目前 Netskope 已经迅速推出了 Skope AI 来抓住这些催化剂机会。

此外，在经济下行周期投资网络安全有一系列好处，包括客户分配的 IT Spending 稳定、毛利率以及对云计算成本的 Add-On 价值高、高部署和迁移成本让客户 Retention 极强等。

**02.**

**什么是 Netskope**

Netskope 有一个非常有趣的成长轨迹。

它首先是一家随着云趋势成长的公司，在 2012 年之后的数年时间里都是专注于 CASB，帮助 CIO 和 CISO 们克服使用云和 SaaS 的安全顾虑。

它还是**一家一直在红海战场中逆袭的公司**。尽管有 Greylock、Sequoia Capital、ICONIQ、Accel、Lightspeed 等优秀基金的一路支持，Netskope 在早期一度被 Skyhigh、CloudLock 等玩家压了一头，但这些竞争者没有 CEO Sanjay Beri 的长期愿景，在 2016 年后陆续卖身给 Cisco、Macfee 等老牌厂商并且逐渐丧失创新。

Sanjay 是连续成功创业者，在 Netskope 之前将上一家创立的公司卖给了瞻博网络，并且留在那里操盘数亿美元级别的业务线，离职再度创业的愿景是打造一家 100 年的公司，因此在 CASB 的收购潮中坚持独立，并且在过去 5 年不仅站稳了 CASB 方向的独立第一名位置，还大幅拓展了产品线和 TAM，成为了现在的 SASE Leader。

**核心安全产品与网络基础设施**

**Netskope 产品背后的 IT 架构演变与客户遭遇的挑战**

为了让没有太多安全领域经验的读者也可以更好地理解这部分，我在下面使用了 Netskope 的 Chief Evangelist Bob Gilbet 在 2021 年采用的叙事。尽管 Netskope 产品组合在过去 2 年已经有了更多发展，但是他讲述的 IT 趋势和客户挑战仍然存在：

在过去 10 年，每个人都能直观感受到的变化是云上应用（SaaS）数量的提升，数据量级的提升，以及全球招聘与混合办公趋势的兴起。

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/007.png)

在这种情况下，防火墙、堡垒机、VPN 等传统网络安全工具组成的“城墙与护城河”防护已经很难奏效，非常容易被攻破，并且处理流量的性能很难满足混合办公时代的企业员工诉求。

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/008.png)

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/009.png)

企业进行补救的方法是在每个单点购买对应的产品，导致了安全供应商的分割，总预算的上升，同时每个安全工具只是被用来处理单点问题，缺乏上下文和全局防护。

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/010.png)

**对这种混乱情况的终极解法是使用一个统一的平台，同时提供 SWG、CASB、Private Access（ZTNA）、FWaaS（防火墙即服务）这些完整的 SSE 套件，帮助企业一站式地解决对 SaaS、Web 和内网应用资源的访问、规则设置、DLP 监测等。**这样做的好处是企业无需安装实体设备、多次进行复杂部署、使用分散的控制台等。在这些产品之上，边缘的 PoP 基础设施网络则可以帮助客户最高性能地使用这些服务。

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/011.png)

这种统一的 SASE 平台目前来看是网络安全领域皇冠上的明珠之一，对供应商要求很高，因此 Netskope、Zscaler、Palo Alto Networks、Cloudflare 等最优秀的安全和网络公司都在角逐成为赢家。

**Netskope 的 SSE 产品**

SSE 包含 3 个核心产品：

**• SWG：**

帮助公司员工和 Web 流量之间安全交互，比如老板希望普通员工在上班期间无法访问 YouTube，而社交媒体运营员工可以浏览 YouTube 但无法上传视频，就可以通过 SWG 进行 URL 过滤以及限制 HTML 中的 POST 来实现。

**• CASB：**

帮助公司员工和 SaaS 安全交互。比如通过 CASB 设置某些员工可以创建一项 Salesforce 活动而别人只能浏览，或是让营销 团队可以在 Linkedin 上发帖而研发团队只能编辑不能发新帖。SaaS 没有固定的编写方式，可以是 HTML、JavaScript、JSON，需要 CASB 供应商做许多解析逻辑。

**• ZTNA：**

帮助公司员工和企业部署在自己数据中心或云上的内网应用高性能和安全地交互。比如通过使用 ZTNA 来限制已提交离职员工在周五晚上访问内网的某个存有敏感表的应用。

从现有的产品矩阵来看，Netskope 的布局已经相当完善，不光涵盖了 SSE 的 3 个核心组成部分，在 RBI（远程浏览器隔离，被视作下一代 SWG 的核心）和 CSPM（即 Wiz 的核心业务）等延伸领域也已经有资产布局：

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/012.png)

我们之前在云安全的文章中将 Netskope 作为 CASB 的代表者展示，而 CASB 目前仍然是 Netskope 的安身立命之本，不管是宽度还是深度都有绝对优势：

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/013.png)

**• 宽度：**

Netskope CASB 支持的总应用数超 5 万，最接近的 Palo Alto Networks 的 CASB 只有 2.5 万，预计年底到 3 万，Zscaler 的 CASB 则在 2021 年才起步，还差距狠大。

**• 深度：**

Netskope 对于 Out-Of-Band C  ASB的集成、SaaS 的攻击威胁上都理解非常深，在最核心的 SaaS 上，比如 Dropbox、Salesforce、M365 等，Netskope 提供的可见度和权限控制颗粒度都是最强大的。

\*Out-of-Band CASB 通过连接到各个 SaaS 的 API 来检查文件以实现安全，而 In-Line CASB 则通过安装代理讲 SaaS 的所有流量转给代理来实现 CASB 能力。Out-Of-Band 需要极深的 Know-How，而 In-Line CASB 则兴起于疫情期间。

**在狭义的 SWG 和 ZTNA 产品上，这两类产品的供应商本身已经相当同质化，很难做出差异点，更多是全球 PoP 基础设施的基本功比拼。**在被视作 SWG 的下一个核心战场的 RBI 上，Netskope 在 21 年收购了 Randem 获得了服务器端渲染用将视频信号传输到本地的基础技术，和 Zscaler、Palo Alto Networks 的架构没有太大差异，但略落后于收购了 S2 Systems 并获得了本地渲染能力的 Cloudflare。

**NewEdge 全球网络**

构建一个全球分布式的 PoP 边缘基础设施本应是一件极其困难的事情，Cloudflare、Zscaler、Fastly 等公司花费了数年还是十几年的时间实现这一点。

Netskope 从 19 年开始补足自己的全球 PoP，挖到了 AWS 的 Global Network 和 Amazon carrier 负责人 Joe DePalo 操刀。**得益于已经发展成熟的数据中心托管服务商，Joe 基本上只花了一年的时间就在 Netskope 建立起构建了 50 个全球 PoP 网点和 100Tbps 的网络容量。**目前跟 Zscaler 等竞争对手相比已经不落下风。

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/014.png)

**Netskope 也是少数在中国有 PoP 的公司，分别在北京、上海、深圳有 1 个 PoP** —— 核心原因是 Netskope 对于用户体验的重视，只要发现某个区域的网络请求达到一定量级就会去开 PoP。由于一直这样比较激进地开 PoP，Netskope 的 PoP 网络利用率可能平均只有 20%+，比行业均值要低很多，它靠通过比竞争对手更高的定价来维持这种奢华的网络性能。

目前 Netskope 正在探索的 Container Service 可以帮助客户在其 PoP 里部署应用，起到类似边缘云计算的效果。这最终可以帮助 Netskope 提升 PoP 的利用率并且向客户追加销售。

**市场机会**

单纯看 Netskope 的天花板比较简单，起码有能做到 Zscaler 的 15 亿美元 ARR 的空间，现在离这个里程碑还有数倍的空间。

**从更大的 TAM 视角看：**

• 最宽泛的 TAM 是全球 10 亿知识工作者 \* 150 美元/年的定价，对应 1500 亿美元的市场；

• Gartner、G2、Netskope CFO 的口径是整个 SASE 在未来 2-3 年达到 150 亿美元，30% 左右的复合增速。

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/015.png)

从比较保守的客户角度估计，**Netskope 和它的主要竞争者基本都不做 SMB：**

**• 从地域视角看：**

- 最核心的是美国，它的 SMB/SME 没太大 SSE 的需求，所以 1.5 亿工作群体里有 30% 的 Mid-Market 和 Enterprise 雇员，按照 150 美元/年对应 70 亿美元左右的年收入池子；

- EMEA 的大型企业基数较少，但是 SMB/SME 从过去来看购买意愿反而比较强，对应也有 50 亿美元的年收入池子；

- APEC 和 Latam 基本可以忽略，日本属于有一定潜力的市场，但是会比较偏向 Cisco、Fortinet 这种老牌厂商，暂时在 Netskope 射程之外。

**• 从行业看：**

主要的 SSE 需求是金融服务、能源、零售、科技以及医疗公司和机构。

**客户**

**Netskope 从 Mid-Market 切入市场，在追求性能、对定价没那么在意的客户群中享有很高的声誉，发展了几年时间就已经完全 Enterprise Ready，在大型企业市场拥有一席之地，很早就获得了财富 500 强的客户。**

目前 Netskope 拥有超过 2000 家客户，包含 25 家财富 100 强客户 —— 全球 4 家最大商业银行中的 2 家，全球 7 家最大医疗保健提供商中的 5 家，全球 3 大电信公司中的 2 家。当红炸子鸡 NVIDIA 也是 Netskope 的客户。

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/016.png)

由于 Netskope 过去以 CASB 见长，Zscaler 过去以 SWG 见长，许多客户过去需要同时采购它们的产品才能真的满足需求，但是随着 SASE 统一平台的趋势被 CISO 接受，Netskope 和 Zscaler 互相 Land & Expand 的情况更加明显。

根据 Netskope 前 Field CTO 和 Zscaler VP 的观察，Zscaler 的客户在采用它的 CASB 方面会迟疑一些，而 Netskope 的客户在 CASB 之上购买 SWG 或者 FWaaS 则更顺畅，正好可以替换掉 Blue Coat 的硬件，但 Netskope 本身的客户基数仍小于 Zscaler —— 后者在全球拥有超 5600 个客户。

**竞争**

Netskope 最大的对标和竞争对手仍然是 Zscaler，SSE 的业务布局几乎一模一样，但是在经营的势头上已经有分化的趋势：Zscaler 是 07 年的公司，系统都不是基于 Linux 的，也不是最新一代底层架构，更像是大型跨国企业落后技术堆栈的胶水，帮助客户把内部破碎的、陈旧的系统联合在一起，非常适合在疫情期间渗透，但是性能和安全性都在实际使用中较 Netskope 已经没有领先。

包括 Zscaler 在内，Netskope 的核心、正面竞争对手主要包括以下两类：

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/017.png)

值得注意的是微软在 2023 年 7 月宣布其 Entra 业务线推出了 SSE 产品，提供 SWG 和 ZTNA，但是缺少 CASB。鉴于微软的竞争策略一向是价格和客户服务，这可能对 Zscaler 带来更大冲击，而 Netskope 和 Palo Alto Network 的客户群反应还有待观察。

**03.**

**走向真正的 SASE**

一旦谈及到零信任或者 SASE，往往会牵扯到 SD-WAN。但是在过去 3-5 年时间里，从业务叙事和竞争的角度看，两者的关系发生了几个大的变化：

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/018.png)

**1. 网络和安全销售分离；**

SASE 一开始由 Gartner 在 19 年提出，试图将网络（Network）和安全捆绑在一起，大量公司冲向 SASE 概念并且试图真的贯彻这种捆绑销售，但是很快发现销售结果并不理想，因为 SD-WAN 需要对企业主干网进行重塑，考虑到整个转换项目的成本和周期，大多数时候 SD-WAN 并不比 MPLS 便宜，所以企业拥抱的动力并不强。同时一部分 CISO 也并不是负责网络的决策者，反而是安全的部分更好卖，因此 Gartner 在 2021 年开始放弃了 SASE 这个术语，单独定义了 SSE。

**2. 网络和安全能力的再整合；**

尽管在销售上分离，SD-WAN 本身在 19 年前后已经变成了成熟市场，VMWare、Cisco、Fortinet、Versa、Palo Alto 等 6-7 家头部公司通过收购整合瓜分大部分市场份额，并逐渐深入安全领域，比如 VMWare 在 20 年推出了 SSE 产品，成为最年轻的 SASE 解决方案。

SSE 厂商也在做针对性防守。Zscaler 没做太多 SD-WAN 的布局，但是 Netskope 在 22 年很聪明地收购了 Infiot，这是 Velo Cloud 的早期团队。目前它提供无边界 SD-WAN 服务，还在 SSE 的捆绑中提供提供类似企业私有的、用于计算而非存储的 CDN 服务。

**3. 叙事从降低成本变成“安全必备”；**

从 IT Spending 角度看，使用其他厂商或 Netskope 的 SSE 并不能帮助企业省钱。对大型企业客户来说，反而比传统的安全硬件盒子+ VPN 的组合贵 20% 左右。所以目前各大 SSE 厂商的销售卖点不再是降成本，而是“更好的员工/用户体验”以及“云时代、混合办公新常态下的安全性”。

**4. Netskope 和 Zscaler 的战略逐渐分化。**

基于以上几点，Netskope 和 Zscaler 目前处于战略分化的路口 —— Netskope 把负责网络建设的 Global VP Joe 晋升为了 Chief Platform Officer，负责全球数据中心（最强性能的 PoP 和解决 First-Mile 的 SD-WAN/Infinot）和内部中台（Unified Engine）的建设，下面团队的核心都来自 AWS 的全球网络建设团队，积累和经验不比 Cloudflare 差，而 Zscaler 暂时没有把 SD-WAN 以及更多的网络属性产品作为下一阶段重点。

**04.**

**商业化进展**

鉴于最新的财务数据较为敏感，下面可以对 Netskope CFO 在投行活动中分享过的 22 年上半年数字跟 Zscaler 的情况做个对比：

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/019.png)

Zscaler 在 IPO 时拥有 50% 的增速，至今没有失速。

**这种情况背后的原因是网络安全（Network Security）的特殊性 —— 这不是那种 PMF 未验证的新兴市场或者客户的预算未达到稳定的蓝海市场，而是一个红海市场，客户往往已经拥有相似功能的产品，新的供应商需要说服客户更换、放弃已有产品的投资、花成本切换到新的解决方案，只有拥有极强产品力的供应商才能做到这一点。**

而一旦达成了这一目标，网络安全领域的创新公司就有机会享受一个较长的增长期，持续占据客户的 IT Spending，增速从 50% 级别缩减到 30% 需要数年的时间。

**05.**

**结论**

Netskope 展现出了极强的长期愿景、韧性和执行力。在 CASB 领域实现逆袭之后，Netskope 又在 SASE 领域复刻了同一剧本，在红海级别的网络安全领域实现了这一战果。创始人 Sanjay 不光懂产品和技术，还从 Day One 就非常重视文化建设和为招募人才制定标准。总体而言，每一个安全投资者、从业者和爱好者都非常值得关注 Netskope 并且期待它走向二级市场的那一天。

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/020.png)

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/021.png)

延伸阅读

[![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/022.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247504039&idx=1&sn=1db11c088051ceb00681781bcc9d3b73&chksm=ce9b6f39f9ece62f8836bb1fd5b66e8d5ee616ea614ac7e6b1e5d860897bbdc24aed27156f32&scene=21#wechat_redirect)

Typeface：Adobe前CTO创立的AI营销内容生成平台，1年估值10亿美金

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/023.png)

[![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/024.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503594&idx=1&sn=7962f283bd87e27fc00aa6dd62c8c9ab&chksm=ce9b7174f9ecf862e4040b3a7babac14851f36916bba0fb360d8c4b8dc5f2d34835a62f57751&scene=21#wechat_redirect)

H100 供需分析：芯片战争将持续多久？

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/025.png)

[![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/026.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503539&idx=1&sn=b3c54e6cadd70072269ac1a7478988d4&chksm=ce9b712df9ecf83bd5a5b465311ed483a4a4a554e9b1f5dece94621dee4451b748f3e9d0e8a3&scene=21#wechat_redirect)

Harvey：OpenAI投资的法律Copilot，最适合LLM落地的垂直行业

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/027.png)

[![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/028.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503488&idx=1&sn=24bf3cef8b6d859e0b3d4607dc3235b3&chksm=ce9b711ef9ecf808c248dbde533b37b47ced78cdabc4d25b31e96d7fbbab265029d00af377bf&scene=21#wechat_redirect)

拾象硅谷见闻系列：生产力 SaaS 如何应对 AI 的颠覆？

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/029.png)

[![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/030.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503441&idx=1&sn=19397a87b3993ccd6f85fcfcc872d13f&chksm=ce9b71cff9ecf8d919696795beea88ba25056c52262bd5b43e278fa34ec6927fbb118dfff3f8&scene=21#wechat_redirect)

Covariant：OpenAI Mafia创业，为机器人开发AI大脑

![](../images/2023-08-17-netskope-ling-xin-ren-tou-hao-ling-dao-zhe-neng-fou-dian-fu/031.png)
