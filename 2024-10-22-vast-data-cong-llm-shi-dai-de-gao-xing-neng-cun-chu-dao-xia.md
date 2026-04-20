---
title: VAST Data：从 LLM 时代的高性能存储到下一代数据平台
publish_date: '2024-10-22'
publish_timestamp: 1729598400
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/-KuU0_ydFEQkDDZOv_-YrQ
msgid: 1000000296
appmsgid: 2247510027
itemidx: 1
digest: GPU 时代也需要数据存储的全面升级
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzWX0O2SSicHqkvUGmW8s2RKO3KuODeQXddDWDoJPPsxHdbcFTdUicj8F0iaAG24VdzXQVOsdUJOWddg/0?wx_fmt=jpeg
image_count: 29
archived_at: '2026-04-20T02:44:49+08:00'
---

[![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/001.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247507749&idx=1&sn=1403008340bbe16dff1b9fc2d5ae6eae&chksm=ce9b60bbf9ece9ad6b7028fd2aa90e43dba20a6a92f9202cdd88b806dd9a18f3e0e17ce7e8e1&scene=21#wechat_redirect)

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/002.png)

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/003.png)

作者：Cage

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/004.png)

在传统的数据基建中，很少有大量非结构化数据需要高速存取，LLM 训练对这个能力提出了新的挑战。VAST Data 打造了专为 AI 深度学习优化的解决方案，尤其擅长处理 10 PB 量级的多模态数据。其独特的 DASE（Disaggregated Shared Everything）架构，让企业能够以近乎线性的效果扩展存储。

VAST 的优势不仅体现在技术架构上，它还通过软硬一体化的存储方案，为客户提供更完整的使用体验，成为了 Data Infra 领域最快达到 1亿 ARR 美金的公司之一。从Coreweave、Lambda Labs 这样的 GPU 云，到科研机构、金融量化机构，以及 Zoom、Agoda 这样的企业客户，VAST 的解决方案已经渗透到了多个高数据密度的行业。

未来 VAST 的目标并不仅仅是存储市场的“高性能”尖端部分，而是通过其灵活的架构和软件策略，进军通用存储与 AI 数据平台领域。这种愿景让它不仅是一家高性能存储公司，更是在多模态 AI 时代数据平台的先驱者。

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/005.png)

**💡**目录 **💡**

    01 Investment Thesis

    02 AI 时代的数据新需求

    03 核心技术与产品

    04 商业模式与商业化情况

    05 市场竞争与团队

**01.**

**Investment Thesis**

**1.****VAST Data 站在 AI 和 GPU 计算的大趋势上，能力极其适合高性能的数据存取**

Snowflake 客户的平均数据规模为 40 TB 左右，而 VAST Data 客户的数据规模可以达到 10 PBs。VAST 目前的客户集中在 GPU 数据中心和科学计算研究中心，原因就是他们最适合在 10+ PB 的数据量级下提供高速、易用且易扩展的产品。由于架构设计满足 AI 需求，VAST 与 NVIDIA 建立了独特的 GTM 合作伙伴关系。

**2.** **VAST Data 独特的 DASE 架构使其有极强的 scale-up 能力**

VAST 的解耦、共享一切（DA Share-Everything）架构是 Snowflake 存算分离级别的架构创新，颠覆了公有云的不共享（Share-Nothing）架构，平衡了规模、速度和成本。客户可以增加计算来解决 I/O 网络瓶颈问题，而不用大幅提升储存投资。接近 linearly scale 的规模化能力是 VAST 最大的差异化优势。

**3.****VAST Data 有机会颠覆存储市场：从高性能存储扩展到通用存储**

传统存储市场可以被分为金字塔形，高性能存储只负责金字塔尖的部分。VAST namespace 的网络效应未来有机会打破金字塔，LLM 能让大量数据活起来，高性能存储能占据更大的市场。

**4.****VAST Data 不只是存储公司，而是 next-gen AI 数据平台**

VAST 的vision 是构建一个全面的深度学习和非结构化数据平台，而不是传统存储解决方案。他们的盈利模式已经是一家软件供应商，独立于硬件库存。这种灵活性使 VAST 能够根据新技术调整其软件。下一步 VAST 正在向 AI 时代的数据仓库公司转型，提供可以互联各种平台的通用存储和分析方案。

**Key Risk**

**估值风险：**估值 $ 9.1 B，基于 on-prem 存储市场的空间，估值比较难 justify。

**增长放缓的风险：**AI 模型训练需求放缓，推理中可能不刚需高性能存储。

**关键问题：prompt caching 这样的方案是否能驱动 All-flash 的存储方案？**

**云巨头的竞争：**AWS、GCP 和 Azure 等可能开发自己的存储平台，减少对 VAST on-prem 方案的需求。VAST 只能在当前的 on-prem 350 亿美元的市场中扩大占比到 10% 来 justify 估值。

**扩展能力的不确定性：**database、 data engine 和存储是完全不同的市场策略，VAST 是否能够扩展到新市场还不好判断。历史上的参考案例只有 Oracle。

**02.**

**AI 时代的数据新需求**

AI 时代的数据管线和 BI 时代发生了非常大的改变：

• BI 数据管线最终产出是数据分析，为企业和产品决策服务；AI 数据管线的最终产出是模型，直接决定了产品能力且会进一步生成数据

• BI 数据管线中有大量的数据聚合，数据量都大规模缩减；AI 管线没有那么明显的聚合效果，且每一步数据量都比 BI 大3个数量级以上

具体可以参考下面的图和表格（来自VAST Youtube session 视频）：

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/006.png)

BI data pipeline

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/007.png)

AI data pipeline

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/008.png)

由于这样的 pipeline 差异，对下一代的数据平台就有了新的需求。Vast Data 就是在这样的需求中打造了自己的产品：

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/009.png)

**03.**

**核心技术与产品**

VAST 有一本非常详尽的技术白皮书，读完发现他们有几个核心差异化优势：

• 高性能高 scalability：Vast 在全闪存架构下能 scale 到 100 PB 量级下保持很高的性能，目标的规模上限是 EB 级别（1 PB = 1024 TB，1 EB = 1024 PB）。

• Transactional + analytical 不冲突：DASE 架构让读写能完全并行，也不再有传统的交易/分析数据库互斥。

• 全局一致性：在每一个位置都可以高效访问到全部数据

而这些优点都可以归功于 DASE 这个关键的架构设计。

**DASE: 核心架构**

VAST 在设计中最关键的选择是 **Disaggregated Shared Everything (DASE)** 这样的架构，和主流公有云和分布式系统的 SN (Shared-nothing) 架构是完全不同的。这个架构创新是非常重要且有技术壁垒的，其重要性可以类比 Snowflake 对云数据仓库存算分离的创新。

2005 年 NS 系统的早期重要论文 Google file system 发布，分布式系统这个领域开始蓬勃发展。当时的分布式系统是数千个节点在管理着几百 TB 数据，**今天一个节点就能存储这样的数据量。**

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/010.png)

上图为 share nothing 架构，每一个node 有CPU、存储和内存；而下图为 share everything 架构，将计算单元和存储单元分离了。

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/011.png)

同时，**node 之间的互联传输速度比当时快了几个数量级：**VAST 需要 100 Gbps Ethernet or Infiniband interconnect。以上两个背景让 DASE 在最近才成为可能。

在 DASE 架构下，数据对系统中的每一个节点都是 accessible 的，这种 share-everything 的方式让节点之间不再需要频繁沟通来寻找和拼凑数据。实际参与的节点有两种：

• CNode 是专门负责逻辑操作的计算节点，比如找到从哪里读取关键数据。他们是跑在 x86 和 ARM CPU 上的容器。所有 CNodes 能通过 NVMe Fabric 的互联层直接读取到数据，所以他们不会彼此沟通

• DNode 是实际和硬件存储交互的数据节点。他们不执行逻辑操作，可以在类似与 DPU 这样的专用硬件上跑

• CNode 直接访问所有数据、元数据和系统状态。系统状态存储在 NVMe SSD 上，形成高可用的 NVMe JBOFs（a Bunch of Flash），这些存储设备通过 NVMe fabric 互联

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/012.png)

这样的设计让存储端和计算端可以解耦，根据客户实际的使用需求进行 scale-up，而且让硬件提升的性价比更高：如果需要更多存储，就增加更多DNode；如果遇到计算瓶颈需要更多 I/O，那就增加更多 CNode；每一次增加 node 都可以在之后持续的发挥性能。

在这种架构中，所有计算都由无状态容器中的计算节点（CNode）执行。这使得集群计算资源可以独立于存储容量进行扩展。

DASE 架构支持高达 100PB 的扩展能力，并且在一年的时间里只有几秒钟可能会出现宕机。通过使用无状态存储服务器和软件驱动的智能，DASE 实现了极高的系统弹性。

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/013.png)

**核心产品线**

**DataStore：Vast DATA 平台的存储基础，是他们在2019年发布的核心产品，后续的产品也都在 DataStore 基础上实现。**可以存储大量 raw 非结构化数据（high capacity），以接近实时流式的方式存储（high bandwidth）。

**DataBase：** 结构化数据库，与传统的 DBMS 不同，它结合了事务处理（例如基于行的 OLTP 数据库）、基于列的分析查询（例如基于闪存的数据仓库）。这个数据库的价值在于对 DataStore 中非结构化数据进行语义分析。

VAST database 其实应该视为 data warehouse solution。其 SQL 功能不直接插入新数据或创建新表，而是利用已有的外部数据，定义自己的查询来整合和调整数据（重点在于数据的存储、查询和分析，而不是数据的实时修改和更新）

**DataEngine：** 最新发布的产品，提供函数执行环境，使函数和事件通知/触发器可以在每一个容器中自动执行，这样可以将原始的非结构化数据转化为信息。

**DataSpace：** 将这些产品扩展到整个数据中心，构建一个统一的计算结构和存储命名空间。DataSpace 的最终目的是在全球范围内扩展访问权限，实现联邦 AI 训练和 AI 推理。**这会是 VastData 产品在大公司内部产生网络效应的来源。**

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/014.png)

**04.**

**商业模式与商业化情况**

**商业模式：Gemini**

巧合的是 VAST 的商业方案和 Google 的 Gemini 撞了名字。

在软件上，客户购买的是 Gemini 订阅，获得 Vast 软件的使用许可，并包括对软件和运行其上的 Gemini 支持硬件的支持和维护。Vast 提供全面的支持服务，包括硬件和软件的支持。例如，当 SSD 或风扇在 Vast 集群中出现故障时，系统会发送警报给 Vast 支持团队，支持工程师会联系客户安排更换。

而对于硬件，Vast 的客户通过 Vast 安排的制造合作伙伴获取经过 Gemini 支持的硬件。这些合作伙伴包括 Viking Enterprise Solutions、Intel、Kioxia 和 Nvidia 等。这些制造合作伙伴根据与 Vast 协商的成本价格向 Vast 的经销商提供硬件，这些成本价格考虑了 Vast 所有客户的综合购买量。

这种组合方式使 Vast 的客户能够避免企业存储供应商在像 SSD 这样的商品组件上的巨大加价，同时保持系统的稳定性和安全性，因为整个系统由一个供应商（Vast）负责支持。

**商业化数据**

VAST Data 在 2023 年末宣布自己的 ARR 超过了 1亿美金，成为 Data Infra 领域最快超过 1亿 ARR 的独角兽。

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/015.png)

**客户 use case 与反馈**

VAST 客户主要有几类画像：GPU 云服务、有高性能计算需求的五百强企业、对冲基金和研究机构。而他们的 use case 主要集中在 HPC（高性能计算）和 AI 领域：

• 生命科学：基因组测序、电子显微镜、图像处理中的 AI

• 研究：药物发现、制药开发和研究中的图像处理

• 金融服务：新交易算法、金融建模

• 汽车行业：自动驾驶、数据处理模型训练

• 媒体与娱乐：大文件处理、渲染大型文件、8k 视频后期制作

具体 use case 可以根据文件类型分为两类：

• 大型数据，本身对 scalability 要求高，瓶颈在网络带宽

• 小文本大批量处理，对软件做数据并行化的能力要求高，客户 Lambda 表示这是传统硬件厂商做不好的领域

在用户实际使用的反馈中，大部分对 VAST 的评价是比较正面的：

• **乐意为高使用量和客单价买单：**好评反映在客户的付费意愿上，好评反映在客户的付费意愿上，核心客户的平均使用量在 10PB上下，客单价能达到七位数，而且这些用户在过去几年内的付费都在持续的成倍增长。

• **优秀的性能和兼容性：**VAST 在 PB 级别上保障了运营效率并防止系统崩溃。系统提供多种数据访问方式，包括 NFS、对象存储和直接数据加载到 GPU 中，适合 AI 应用。其兼容性确保了文件传输速度快，能够无缝集成到现有工作流程中。

• **高性能和可扩展性：**VAST 未来的主要优势在于可扩展性和跨不同系统/硬件的兼容性。VAST 的 DASE 架构使客户只需逐步添加新的硬件和软件容量，而不是替换现有的整套设施，减少了数据存储的更新周期。

• **软硬件一站式的客户支持：**VAST 的客户服务响应速度很快，而且以软件为主硬件外包提供的方式也受到好评。对比竞品新公司 Weka 只有软件需要客户自己采购硬件，和老公司 Pure Storage 在软件上性能较差，VAST 以结合的方式做到了更有的体验。

• **与英伟达的合作：**对 DGX Superpod 的支持是很多 AI GPU 云厂商选用 VAST 的原因，体现了他们在这个领域的专业性。

当然用户也提出了一些使用中的顾虑：

**云部署：**VAST 的主要设计更多地与 on-prem 本地部署契合，在云连接延迟上做得比较差。尽管与 HPE Cloud 有合作，但缺乏真正的混合解决方案。这在主要云平台上的部署灵活性不足，使其在与 AWS 或 GCP 平台更好集成的竞争对手面前处于不利地位。

**成本：**与高性能存储的同行比起来，VAST 有少许溢价，但客户都愿意为其优秀的使用体验买单。但对比廉价的基础存储，VAST 的价格还是很高，因此在 on-prem 存储中的市场份额还相对有限。

**共存与竞争挑战：**VAST 目前还没有表现出竞争中的排他性，往往还是和其他系统共存的，比如与现有的存储系统 IBM Spectrum Scale 和 DDN Storage 并存，而不是取而代之。此外，NetApp 和 EMC 等竞争对手正在通过 QLC 驱动器等技术适应，并可能超过 VAST。像 WEKA 这样的公司瞄准更告诉要求的高性能使用场景，有时甚至超越 VAST。但好消息是 VAST 渐渐能在预算上占据 75%+。

**客户的预算分配逻辑**是这样的：

• 在厂商之间，常见选择2-3家，VAST、DDN、Weka 是提到最多的三个名字。如果只保留一家，VAST 基本是大家的 top choice

  

• 在整个数据中心，存储占据 5-10% ，GPU 占大头 65-70%, 网络互联 20%, CPU、内存、能源加起来 5%

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/016.jpg)

**05.**

**市场竞争与团队**

**竞争对手分析**

市场上直接的竞争对手有两类：

• 新公司：Weka 为首的创业新公司

• Existing company：DDN、Pure Storage、NetApp

在实际使用中客户往往会从几个角度来评价产品，我们也根据这个框架来分析各个精品之间的差异：

产品核心维度：

• 速度：评价标准是 IOPS，一秒钟之内能够传输多少个文件

• scalability：能不能规模化到 10 PB 以上保持高性能

• 服务：multi-tanency 支持，软硬件方案的结合程度

其他维度：

• 外部合作：是否与 NV DGX 有紧密合作

• 部署位置

• 团队 leadership

• GTM 策略

在速度上，VAST Data 的性能虽不及 WEKA，但它的通用存储能力已经足够满足大多数场景的需求。相较之下，WEKA 在处理 10 PB 以下的数据时表现最为出色，到了大量级上性能开始逊于 VAST。相比这些公司，Pure Storage 和 NetApp 等传统厂商在性能上落后了约 15%-20%，倒是 DDN 和 Weka 速度接近。

在可扩展性上，VAST Data 展现出强大的扩展能力，其架构设计使其能够在接近 100 PB 的规模上保持近乎线性的扩展。得益于 VAST 独特的 DASE（Disaggregated Shared Everything）架构，它不仅降低了扩展的运营成本，也大幅减少了技术复杂性。与之相比，WEKA 需要至少 6 至 8 个节点才能开始部署，并且随着节点的增加，网络架构的需求也会大幅增加。DDN 在过去的表现虽然足够快，但由于架构限制，现如今已经难以满足高吞吐量和低延迟的现代需求。

在客户服务上，VAST Data 提供全天候的客户服务，并且其解决方案涵盖硬件和软件，客户只需面对 VAST 一家公司即可处理所有问题，整体体验更佳。此外，VAST 的多租户支持也很强，这对需要多个用户共享存储的场景至关重要。相比之下，WEKA 的多租户支持稍差，并且仅提供软件，客户需要自行购买硬件，这降低了整体使用体验。

在部署方面，VAST Data 主要面向 on-prem 部署，这也符合其在 AI 和高性能数据存储领域的优势，而 WEKA 则更支持云计算。

在团队 leadership 上，VAST Data 的管理团队由存储行业的资深人士带领，广受行业好评。相比之下，WEKA 的团队则因为难以明确目标、频繁调整战略而受到一定批评。过去两年内，WEKA 经历了四次重大转型，包括从专注于 OEM 硬件销售转向软件定义存储，再到仅提供云端解决方案，这样的频繁转向让其战略显得有些随意。

在市场推广策略（GTM）上，VAST Data 的销售周期通常为 9 至 12 个月，他们的销售来源主要分为三类：三分之一来自全新项目，通常是由 AI 需求推动；三分之一来自现有客户的扩展；另三分之一则是完全替换现有的存储系统。

WEKA 的销售周期比 VAST 更长，通常需要 18 至 24 个月。WEKA 的战略重心放在向云计算公司转型，它的销售渠道主要依赖于 OEM，WEKA 的软件被部署在各种硬件上，如 Lenovo、HP、Dell 和 Hitachi，并通过这些 OEM 进入 on-prem 市场。

**团队情况**

VAST 的经营情况和 vision 离不开优秀的团队。VAST 由 Renen Hallak 于 2016 年创立，现在团队已经达到 700+人。该公司拥有一支经验丰富的领导团队，包括首席执行官 Renen Hallak、首席营销官 Marianne Budnik 和首席收入官 Rick Scurfield  等。其中 Renen 是公司的灵魂人物，也是存储行业的老兵。

• Co-Founder & CEO: Renen Hallak

Vast DATA CEO Renen Hallak 是一位非常特别的企业家。在创建 VAST 之前，他创建了 XtremIO （世界领先的全闪存阵列），并将公司以 4.3 亿美元出售给戴尔 EMC。作为戴尔 EMC 的一部分，Renen 继续将 XtremIO 扩展到数十亿美元的收入。他的领导才能得到广泛认可，连续三年被高盛评为" 100 位最有趣的企业家"之一。

• Co-Founder: Jeff Denworth

Jeff 负责公司的产品和商业战略。Jeff 为 VAST 带来了二十多年的先进计算和**大规模可扩展大数据及云存储技术经验。**在加入 VAST 之前，Jeff 曾在 DDN、CTERA Networks 和 Cluster File Systems 担任管理职务。

• Co-Founder & Chief R&D Officer: Shachar Fienblit

Shachar 是 VAST 的联合创始人兼首席研发官，负责监管**全球工程**。他的团队负责提供 VAST 创新技术的核心软件。Shachar 曾在 Kaminario 和 IBM 担任领导职务，拥有丰富的知识和专业技能。

• Co-Founder & VP, Technology, Alon Horev

Alon 是 VAST 的联合创始人兼技术副总裁。Alon 领导过多个工程项目，并在与战略客户的合作中取得了成功。在加入 VAST 之前，Alon 曾在**思科和 IBM 等公司成功设计和实施创新数据库和存储平台。**Alon 对技术充满好奇和热情，是自学成才类型的技术人才。

**长期 upside 分析**

Vast 要挑战的不只是高性能存储领域的对手，他们的 vision 是希望能做到对存储市场的颠覆：

1. 打破存储市场的金字塔：

  • 存储市场可以被分为金字塔形：金字塔尖是和公司使命、收入有关的关键数据，由高性能存储保管着；金字塔底是存档数据，之后不再会有太多读取和写入需求

  • VAST namespace 的网络效应未来有机会打破金字塔，如果 LLM 能让大量数据活起来，高性能存储能占据更大的市场

2. 减少数据存储领域的 restore cycle：

  • 存储行业的 restore cycle 指的是企业定期更新其存储设备和基础设施的周期，通常每三到五年进行一次。这个周期与企业购买的支持服务合同期限相对应，合同到期后，企业通常面临着两个选择：延长现有设备的支持服务或者通过购买新设备来全面更新其数据中心。

  • VAST DASE 架构使客户只需逐步添加新的硬件和软件容量，而不是替换现有的整套设施。

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/017.png)

甚至存储也不是 VAST 局限的目标市场，VAST 要做到的是往计算和数据库方向延伸自己的业务：

1. 长期高性能不会是主要的优势。scale-up 的易用性，在不同系统/硬件上的兼容度会是取胜的关键，这是 VAST 最擅长的地方。

2. 数据库与非结构化数据的分析会成为 VAST 长期重要的差异化支持，甚至能与 Snowflake、Databricks 竞争市场。但现阶段还不成熟，Lambda labs 作为 VAST 的客户还是需要使用 Snow/dbx 的产品

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/018.png)

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/019.png)

排版：Fia

延伸阅读

[![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/020.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509981&idx=1&sn=2560050c51ab5373bd7d6e0b0766794b&chksm=ce9b1843f9ec9155cb6956b236716dd45e8eda76d5b924bd62152909d5368174efce6756e0bf&scene=21#wechat_redirect)

NotebookLM 是 Google 的 ChatGPT 时刻吗？

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/021.png)

[![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/022.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509858&idx=1&sn=de9e36616828fa11fc93649864521b33&chksm=ce9b18fcf9ec91ea6b75634d9eb3b2412eebe800e2b3ca01c22f7969a6ff353fd0ee113589ab&scene=21#wechat_redirect)

拾象英雄帖：寻找 AGI 同行者

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/023.png)

[![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/024.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509817&idx=1&sn=3cd92ea1fada076f1247e456bc47a578&chksm=ce9b18a7f9ec91b15438462b32d7fe7fb4dc82d22859faf28565c5c1a2267095f363db589f66&scene=21#wechat_redirect)

Chelsea Finn: RL 是如何在 Robot Learning 领域创造价值的？

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/025.png)

[![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/026.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509786&idx=1&sn=adfc2d4cfa86f4a8449fe694a78c5388&chksm=ce9b1884f9ec9192ca7a2ff46a3949c5c9a085b36521b10476db10d9d6c1853efd06fc852601&scene=21#wechat_redirect)

Andrej Karpathy: Tesla 能实现自动驾驶领域的 AGI | AGIX 投什么

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/027.png)

[![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/028.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509696&idx=1&sn=6409bd98f7045584687d59360f417562&chksm=ce9b195ef9ec90483a5ce4bef2a5d74d5a3884184e53b49d3c30e2558f81515235758427d9d0&scene=21#wechat_redirect)

LLM 新范式：OpenAI o1, self-play RL 和 AGI 下半场

![](../images/2024-10-22-vast-data-cong-llm-shi-dai-de-gao-xing-neng-cun-chu-dao-xia/029.png)
