---
title: OpenEvidence，医疗领域诞生了第一个广告模式 Chatbot
publish_date: '2025-05-08'
publish_timestamp: 1746705664
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/0kcjBkt10dOY0bR7Vret8Q
msgid: 1000000351
appmsgid: 2247513040
itemidx: 1
digest: Vertical DeepResearch 在医疗领域率先落地
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzvy9wvBut8o6MYYSUOncQgD5733iciaF5MNAQyOLqlS4Zhuepic26lvNgmuVicHfibNo9ODIgzhaWq1rg/0?wx_fmt=jpeg
image_count: 28
archived_at: '2026-04-20T03:34:09+08:00'
---

[![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=3570724992708624387#wechat_redirect)

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/002.png)

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/003.png)

作者：Bryan

编辑：Cage

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/004.png)

在[上一篇研究图谱](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247513001&idx=1&sn=c1e83808616ac17d64c09b9cd5912bcb&scene=21#wechat_redirect)中，我们指出医疗领域很可能是 Vertical Agent 最先落地的领域，其中最有代表性的公司之一是 OpenEvidence，一款专为医生设计的 AI 专业诊断 Copilot。面对医学知识的爆炸式增长和临床信息的严重过载，OpenEvidence 致力于用类似垂直领域 Deep Research 的产品形态，帮助医生提高诊断效率与决策质量。

创始人 Daniel Nadler 是 AI 领域的连续创业者，他在采访中提到，OpenEvidence 在美国医生群体中迅速普及，目前已有超过 10 万名医生每月使用他们的产品。2025 年 2 月，OpenEvidence 完成了由 Sequoia Capital 独家投资的 A 轮融资，融资规模 7500 万美元，投后估值突破 10 亿美元。

有别于传统医疗软件依赖医院系统的复杂采购流程，OpenEvidence 采用直接面向用户的增长策略：直接向医生个人提供服务，省去了冗长的审批与集采环节。凭借精准契合日常临床需求的功能设计，以及医生间的口碑传播，产品实现了病毒式增长。其商业模式则通过与制药企业、医疗器械厂商合作，嵌入精准广告投放，将 AI Agent 顺利切入传统医药代表和学术会议的广告预算分配中，开启了全新的变现路径。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/005.png)

💡 目录 💡

   01 背景

   02 产品和技术

   03 商业化与竞争

   04 团队与融资

   05 结语

**01.**

**背景**

在当今医疗领域，医生们正面临前所未有的挑战。医学知识的爆炸式增长让临床诊断和信息处理变得异常复杂：医学知识每 5 年会有一次更新，文献以每两分钟一篇的速度增加，PubMed 已索引了 3600 万篇摘要，每年新增 100 万篇；Google Scholar 包含约 4 亿篇文章、引文和专利。在这样的背景下，医生在诊疗过程中需要处理大量临床信息，但传统搜索工具难以快速找到深藏在文献中的特定信息，导致信息过载问题愈发严重。

与此同时，医疗资源分配的不均衡进一步加剧了问题。世界卫生组织（WHO）的报告显示，低收入国家医生接触前沿医学证据的频率仅为高收入国家的 1/9 ，形成了显著的“认知剪刀差”。即便在美国本土，乡镇医院购买临床决策系统（如 UpToDate）的渗透率也不及教学医院的 1/7。

此外，随着老龄化社会的到来，多病共存的复杂病例愈发频繁。数据显示，65 岁以上患者平均服用 5 种以上药物，其药物交互作用的可能性超过 3 亿种组合，而传统诊疗指南在此类场景的覆盖率不足 7%。在如此复杂的诊疗环境下，医生仅凭经验作出决策的难度显著增加。

具有 world knowledge + long context 优势的 LLM 能否改善这一困局？实验显示通用 AI 大模型在医疗领域的应用仍存在明显局限性。纽约科恩儿童医疗中心的研究人员将 100 份儿科病例报告输入 ChatGPT，结果显示其错误率比经验丰富的医生高出 83%；而在 Medscape 的 150 个病例测试中，ChatGPT 的诊断准确性曲线下面积（ AUC ）仅为 66%。这些数据表明，AI 在处理复杂疾病时的诊断能力仍存在较大不足。这种局限性直接影响了临床医生对通用 AI 的信任度。当 AI 的建议与医生的临床推理不一致时，医生往往倾向于相信自己的判断忽略 AI 的建议，导致 AI 在实际诊疗中的潜力未能被充分挖掘。

面对医学知识爆炸、资源分配不均以及通用 AI 局限性等多重挑战，医疗行业需要找到新的解决方案，以提升诊疗效率和准确性，同时弥合医疗资源分配的鸿沟。OpenEvidence 是这个方向的代表性公司。

**02.**

**产品和技术**

OpenEvidence 是一款专注于辅助医疗诊断的 Chatbot 产品，旨在为医生和医学生提供高效、精准的临床支持。其交互界面设计独具特色，**每句回答均标注交叉引用编号，并在文末附上参考文献清单，确保信息的可溯源性和验证性。**

它提供“护理指南”与“临床证据”双模式回答，分别侧重实践建议与理论数据支持。每个问题答案后还列出可能的 Follow-up 问题，方便用户进行多轮深入交互。

此外，OpenEvidence 提供全面的临床诊断与治疗支持。症状分析模块可快速解析模糊症状，提供潜在病因分析并推荐相关检查路径。治疗决策支持功能基于最新研究，推荐治疗方案并对比药物疗效及耐药性数据，特别适用于罕见病与复杂交叉病例。系统还内置实时指南访问功能，支持快速调取临床指南与标准，如 CHA2DS2-VASc 评分等。

行政与工作流程辅助功能同样实用。系统可自动生成预先授权信、患者出院指导等医疗文书，并自动附上引用文献。此外，集成的 50+ 临床计算器覆盖疾病评分、药物剂量计算等高频场景，简化复杂计算流程。

医学知识跟踪学习功能（TL；DR）则通过每日精选新发表论文，生成可视化图表与专科分类总结，帮助用户快速掌握学科前沿动态。这种结构化的知识更新机制，为医生和医学生提供了持续学习的便捷途径。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/006.png)

OpenEvidence 对话界面

OpenEvidence 产品主要面向以下用户群体：

• **医生（核心用户）：**包括全科医生、专科医生及偏远地区医疗资源不足的社区医生，用于查询罕见病例、优化诊疗方案、提效工作流程等。

• **护士、医师助理、药剂师等：**用于查询护理指南、药物信息等。

• **医学生：**用于学习最新临床指南、备考医学考试（如美国医师执照考试 USMLE），获取结构化知识支持。

• **医学研究人员：**用于追踪学科动态、关注最新论文摘要与可视化数据，缩短文献综述时间。

以医生为例，一个使用 OpenEvidence 产品的典型用例如下：

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/007.png)

根据其产品设计思路可以看出，OpenEvidence 核心价值主张在于帮助医生快速获取最新、最相关的医学证据，并提供直截了当的临床诊断建议。系统通过整合跨学科医学信息，支持复杂临床决策，尤其在罕见和边缘病例处理中表现出色。更重要的是，OpenEvidence 旨在实现医学信息的民主化，让所有医生，而不仅仅是大型医疗机构的从业者，能够平等获取高质量医学资源。

在技术表现上，OpenEvidence 展现出显著的可靠性。作为首个在美国医学执照考试（USMLE）中得分超过 90% 的 AI 系统，其在 USMLE 三项考试中的表现均优于 ChatGPT，整体错误率比 ChatGPT 低 77%。这种低错误率的表现大幅降低了通用 AI 大模型的幻觉问题，显著提高了医生对 AI 助手的信任度。通过这些特性，OpenEvidence 正在重新定义医疗 AI 的实用性和可信度标准。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/008.jpg)

USMLE 是美国医学生获得临床执业资格的唯一准入测试，  
考试内容分为三个步骤，分别侧重于考察基础医学、  
临床医学和技能应用的情况。

那么 OpenEvidence 是如何从技术上实现其价值主张的呢？自 2022 年创立之初，OpenEvidence 便选择了与众不同的技术路径。当时，行业普遍将注意力放在开发更大参数规模的通用 LLM，而 OpenEvidence 团队却专注于开发小型专业化模型。这一选择虽然一定程度上牺牲了模型的泛化能力，却显著提升了其在专业医学医疗领域的精准性和可靠性。

2023 年，OpenEvidence 团队的研究论文《Do we still need clinical language models》进一步验证了这一决策的正确性。论文指出，在医疗领域，小型专业化模型的表现优于大型通用模型，并因此荣获当年机器学习与医疗保健领域会议的最佳论文奖。

创始人 Daniel Nadler 曾引述美国科幻作家 Ted Chiang 的比喻 “大语言模型就是对世界的 JPEG 压缩”，意指其在追求广泛适用性时牺牲了细节精度。而 OpenEvidence 则专注于医学领域的高质量压缩，确保在这一关键领域的信息准确性和可靠性。这种专注使得 OpenEvidence 能够在医疗 AI 领域提供更为精准和可信的信息支持。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/009.png)

**03.**

**商业化与竞争**

**Chatbot 领域第一个  
广告主导的 business model**

OpenEvidence 颠覆了传统医疗软件的销售模式，采用了**类似于“消费互联网”**的创新 GTM （Go-To-Market）策略，通过**直接面向医生和医学研究者提供免费产品，并利用这些专业消费者的口碑传播快速打开市场。**

这一 GTM 策略的本质是一种依靠产品质量和用户体验驱动增长（PLG）的模式，避开了传统医疗 SaaS 依赖医院系统采购的复杂流程（包括多次会议、AI 委员会审核、预算审批等，通常一整套审批决策的周期长达为 2-5 年，且审批结果存在不确定性），从而极大降低了医生的使用门槛，促使产品在医生群体中快速传播。

创始人 Daniel Nadler 也指出，免费策略让 OpenEvidence 绕过了漫长的企业采购流程。例如，美国退伍军人事务部（VA）作为全国最大的医疗系统之一，采购新技术通常需要三年时间。而 OpenEvidence 通过免费开放给 VA 医生，已收到大量认可和赞誉来自 VA 医生的反馈：许多医生称 OpenEvidence 的产品其在关键时刻帮助他们做出治疗决定，大大改善了退伍军人的护理质量。

事实证明，OpenEvidence 选择的这一 GTM 策略卓有成效：OpenEvidence 在**短短一年内实现了从零用户到覆盖美国 10%-25% 执业医生**的爆炸式增长，每月约有 10 万名医生使用该产品，MAU 达到 30-40 万，这验证了创始人 Nadler “做一个足够优秀的产品，它就会自己传播”的理念。与此同时，OpenEvidence 还获得了《新英格兰医学杂志》（NEJM）的认可，进一步增强了医生等专业用户对于 OpenEvidence 的信任程度。

值得一提的是，OpenEvidence 自 2023 年**与《新英格兰医学杂志》（NEJM）建立了独家战略合作关系。**NEJM 编辑部高层主动联系 OpenEvidence 寻求合作，希望其常用工具包含 NEJM 内容，同时拒绝了其他 AI 大模型公司的数据合作邀请。合作框架重视 NEJM 品牌纯粹性和学术价值。这是由于，以 OpenEvidence 为中心可以形成上下游互惠链条：NEJM 等内容提供方获得曝光，OpenEvidence 平台通过更强大的模型服务获得流量，医生用户获得高质量信息。具体来说，OpenEvidence 为 NEJM 带来数千万访问量，而 NEJM 为 OpenEvidence 提供使用 NEJM 全文进行训练的独家权限，几乎实时更新知识库，持续提升 AI 大模型知识水平。

此外，OpenEvidence 于 2023 年 3 月成为梅奥诊所平台加速器成员，进入为期 20 周的孵化计划，借助梅奥的临床资源和技术支持加速创新。梅奥诊所向 OpenEvidence 开放临床指南和部分去标识化临床数据集，用于 AI 模型的验证与优化，并提供临床专家指导，确保建议符合循证医学规范。

OpenEvidence 还进一步完善 2B 拓展用户渠道。2023 年 8 月，OpenEvidence 与媒体集团 Ziff Davis 达成协议，其技术将集成到 Ziff Davis 旗下健康相关网站，包括面向健康专业人士的 MedPage Today 和面向普通读者的 Everyday Health，进一步扩大用户覆盖面。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/010.png)

在变现方式上，OpenEvidence 以**精准广告**为核心。通过面向制药企业、医疗器械厂商等医疗相关行业的广告投放，实现商业化闭环。由于医生群体的高价值属性，其日常诊疗决策与药品、医疗器械高度相关，吸引了相关厂商的广告投入。

广告内容与临床决策场景紧密结合，例如在医生查看免疫疗法论文时，自动推荐相关药企的 PD-1 抑制剂广告，并标注引用次数；或在医生输入糖尿病合并肾病病例后，推荐 SGLT2 抑制剂并附上真实世界研究数据。我们认为，这种基于专业用户池的精准广告模式可能比通用大模型的广告商业化速度更快。

**竞争对手：传统医学数据库**

从竞争格局上来看，OpenEvidence 真正的竞争对手其实是 **UpToDate 临床医学数据库**。UpToDate 是全球最大的临床社群，现已涵盖 25 个专科的 10,000 多篇临床专题，所有的专题都由来自全球的著名临床医生遵循循证医学的原则以教科书/教学指南的形式撰写，并经过严格的同行评议，附上最新的参考文献，以保证内容质量。截至目前，UpToDate 已经拥有 200 万医护人员使用，企业版收费 $50-100/用户/月，总计年收入 ～5,760 万美元。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/011.png)

相较于 UpToDate，OpenEvidence 的优势是**AI 驱动的交互能力**，它不是静态的文本页面，这意味着用户可以在针对性的提问后获得答案，省去了繁琐的查询过程。

例如，当医生问出 “贫困患者如何替代利福昔明治疗小肠细菌过度生长” 的问题时，OpenEvidence 的深度垂直模型能跳过百万字的主题摘要，直接从 metadata 中抓取二甲双胍联合疗法的亚期临床数据，输出精确到第四段落第三行的解决方案。而使用 UpToDate 的医生，则需要查看相关主题摘要，点击链接阅读，才能在文章中找到他们寻求的具体答案。

**04.**

**团队与融资**

**团队**

OpenEvidence 的创始人 Daniel Nadler 拥有哈佛大学经济学博士学位，其学术背景涵盖经济学与人工智能交叉领域，这使他能够深入理解人工智能的复杂技术问题，并将其应用于实际商业场景。

他是个跨领域的成功连续创业者的创业经历同样令人瞩目。2013 年，他与 Peter Kruskall 共同创立了 Kensho Technologies，这是一款专注于服务华尔街的 AI 量化交易工具。Kensho 提出了“ Warren 算法”，通过分析数百万个市场数据点寻找相关性和套利机会。2018 年，Kensho 以 5.5 亿美元的价格被标准普尔收购，成为当时 AI 领域最贵的一笔交易，标志着 Nadler 在 AI 领域的首次重大成功。

2021 年，Nadler 创立了 Xyla，专注于开发高准确性的 LLM。Xyla 团队包括十几名博士及在读博士员工，并配备了一台位于内华达州沙漠的超级计算机。同时，新冠大流行使得 Nadler 意识到医生在获取最新医学知识方面的挑战。因此，他在 Xyla 中孵化了 OpenEvidence，专注于通过 LLM 提升临床决策准确性。为解决高昂的运算成本问题，Nadler 和团队采用了“检索增强生成”（Retrieval Augmented Generation，RAG）技术，将用户数据与预训练大模型结合，提供更有针对性、更可靠的输出，同时避免 AI 回答中的“幻觉”问题。

除了创业者的身份，Nadler 还展现了多方面的才华。2016 年，他的首部诗集《Lacunae: 100 首想象中的古代爱情诗》出版，并被美国全国公共广播电台评为年度最佳书籍。此后，他又涉足电影圈，担任了《布鲁克林秘案》和《帕尔默》的制片人。这些经历展现了他在科技与艺术领域的多元成就。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/012.png)

Daniel Nadler

Nadler 领导组建的团队秉承学术精英化风格，成员多来自哈佛、MIT 顶尖实验室，偏向学术研究落地。他信奉“顶尖人才只想和顶尖人才共事”，在采访中称：“在 Kensho 的经验让我意识到，如果你让高智商、学习速度极快的人去攻克一个难题，他们的进展会远超一支普通规模大 100 倍的团队。”

CTO Zachary Ziegler 是哈佛大学计算机科学专业的博士候选人，师从 NLP 领域的顶级学者 Alexander Rush，拥有扎实的学术背景和专业的机器学习知识。他曾在 IMAX AI 担任人工智能负责人，2021 年与 Nadler 一同创立 Xyla，并作为 CTO 主导了 OpenEvidence 的开发，专注解决医学领域 AI 幻觉问题。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/013.png)

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/014.png)

**融资**

2025 年 2 月，OpenEvidence 完成 Sequoia Capital 独家投资 7500 万美金的 A 轮融资，投后估值超过 10 亿美元。红杉合伙人 Pat Grady 领导了这一轮投资，他认为 OpenEvidence 的采用与消费者互联网产品的传播方式相似：“没有多少医疗工具能像消费者应用程序那样传播，但这是其中之一”。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/015.png)

**05.**

**结语**

OpenEvidence 的核心价值主张，本质上是利用 AI 破解了医疗领域 “信息爆炸” 与 “索引低效” 的矛盾。更具有指导意义的是它的商业模式：它像消费互联网平台一样直接 “黏” 住医生 —— 靠超高准确率、超低幻觉的临床 AI 工具解决刚需，靠口碑传播实现裂变，再把专业用户池转化为药企、器械商所青睐的高度场景化的精准广告场。

由此，OpenEvidence 既踩中了医生对临床 AI 工具的迫切需求，又切入了传统医疗健康企业从前分配给传统医药代表和学术会议的广告预算——想想看，糖尿病医生查看并发症用药时可以弹出新药数据，肿瘤医生制定方案时可以看到最新器械研究……比这些 “医生决策时精准推送治疗方案相关产品” 更高 ROI 的广告场景可能并不多见。

这种 “垂直领域精准变现” 的打法，为专注于 AI 应用的创业企业思考如何在内卷中杀出重围提供了一条新的思路。随着医疗、法律、金融等更多领域的 Vertical Agent 落地，或许我们会看到一个比通用 AI Chatbot 内嵌广告更高效的商业模式正在成型 —— 而 OpenEvidence，显然已经抢到了专业医疗赛道的先手棋。

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/016.png)

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/017.png)

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/018.png)

排版：杨乐乐

延伸阅读

[![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/019.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247513001&idx=1&sn=c1e83808616ac17d64c09b9cd5912bcb&scene=21#wechat_redirect)

医疗 Agent 最全图谱：AI 如何填补万亿美金“效率黑洞”

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/020.png)

[![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/021.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512957&idx=1&sn=da563a8b6596ef1464c9993219cac3af&scene=21#wechat_redirect)

o3 深度解读：OpenAI 终于发力 tool use，agent 产品危险了吗？

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/022.png)

[![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/023.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512861&idx=1&sn=9aef295be30dc91fbeafa391c31885cf&scene=21#wechat_redirect)

OpenAI：computer use 处于 GPT-2 阶段，模型公司的使命是让 agent 产品化

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/024.png)

[![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/025.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512817&idx=1&sn=9458f5df92bbdba210b9abafc77afde6&scene=21#wechat_redirect)

代码即界面：生成式 UI 带来设计范式重构

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/026.png)

[![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/027.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247512752&idx=1&sn=48839c24a35e6e5094e8022a599989ac&scene=21#wechat_redirect)

Deep Research 类产品深度测评：下一个大模型产品跃迁点到来了吗？

![](../images/2025-05-08-openevidence-yi-liao-ling-yu-dan-sheng-liao-di-yi-ge-yan-gao/028.png)
