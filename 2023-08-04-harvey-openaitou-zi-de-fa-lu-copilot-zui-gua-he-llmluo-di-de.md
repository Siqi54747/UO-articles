---
title: Harvey：OpenAI投资的法律Copilot，最适合LLM落地的垂直行业
publish_date: '2023-08-04'
publish_timestamp: 1691151260
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/gSTjy730BpEfaODsch80dw
msgid: 1000000213
appmsgid: 2247503539
itemidx: 1
digest: 法律 LLM 公司三要素：模型能力、专业数据、客户工作流
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxE0X0rqZc20tVgpEnoOl1kEJkZwSbjuePJANwMYwEYdrGFrwnteejLDb7OkQ4jypAXSp9zVnPKYQ/0?wx_fmt=jpeg
image_count: 35
archived_at: '2026-04-20T01:24:31+08:00'
---

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/001.gif)

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/002.png)

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/003.png)

作者：haina

编辑：penny、Siqi

排版：Scout

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/004.png)

“如何将 LLM 的智能带入专业服务场景”是市场对本轮 AI-native 应用的猜想之一。作为典型的依赖于行业 know-how 、甚至 billed with hours 的行业，法律一直是 AI 创业公司们试图颠覆的领域，在 LLM 浪潮中也不例外。

法律行业天然和 LLM 能力适配：作为一个典型的 text-in/text-out 的场景，法律行业的数据以文本为主，并且多为绝对事实和真实案件，很适合大模型学习。此外，法律工作的强知识性和逻辑性也让大模型能够在更多法律工作流环节中提供价值。在 LLM 之前，Legal Tech 企业的核心商业价值在于电子签名、合同管理这两个环节，**LLM 之后，法律领域极有可能会出现 Copilot 一样量级的效率工具。**

我们关注到 Harvey 首先因为它是 OpenAI Fund的首批投资项目之一，OpenAI 在法律领域的押注一定程度上代表了他们对 GPT-4 有机会再造法律领域的信心，Sam Altman 在一次访谈中也提到对 GPT-4 在法律场景应用的期待。其次，Harvey 的创始团队兼具模型训练经验和法律行业实践，这样的组合可以说是新兴技术改造专业服务领域的创业团队的理想画像。

目前 Harvey 的产品尚未开始公开销售，其披露的标杆客户包括 Allen & Overy 及普华永道，根据其新一轮投资方红杉的公开信息，目前有 1.5 万家律师事务所正在排队使用 Harvey。

不过，因为数据隐私及 LLM 的“幻觉”问题，Harvey 目前尚未真正在实际用例中进入到直面客户的法律服务中，更多被运营于合同起草、法律研究等一般性环节中。**律师事务所及企业对生成性人工智能的使用仍采取谨慎态度。**

考虑到法律服务的特殊性，LLM 在法律行业的渗透会是一个伴随 LLM 能力提升、“幻觉”及“数据隐私”问题解决的缓慢而渐进的过程。同时，大模型训练能力、行业专业数据库、深入大客户工作流，是成就法律 LLM 公司的三要素，能够同时满足的公司将占据竞争优势。

基于这一前提，法律行业巨头与 LLM 法律创业公司的绑定格局已经初步显现，LLM 创业公司是为了获得专业数据和客户资源，大型机构则是为了适应技术发展保持领先地位：Harvey 和 Allen & Overy、普华永道等大型事务所合作，汤森路透收购发布了 CoCounsel 的 Caestext，LexisNexis 发布 Lexis+AI，Robin AI 则与其他两家四大审计公司达成合作。

**以下为本文目录，****建议结合要点进行针对性阅读。**

**👇**

01 Harvey 背后的市场机会

02 法律 LLM  Landscaping

03 Harvey：LLM 如何再造法律服务

04 Harvey 的面临的挑战

05 结论

06 附录

**01.**

**Harvey**

**背后的市场机会**

**Legal Tech Landscape**

根据服务对象划分，Legal Tech 的种类可以分为 **ToL 服务律师事务所、ToB 服务企业法务部门及 ToC 服务消费者。但值得注意的是，无论是 ToL 还是 ToB，企业才是最终付费方。即便产品的客户是律师事务所，由于律师事务所是为企业服务的，律师事务所会把 Legal Tech 工具转交给客户报销。**

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/005.png)

具体到工作场景，传统 Legal Tech 多是广义上的案件管理平台或点解决方案，执行的只是文件资源管理等 ERP 功能。新一代 Legal Tech 引入 NLP 等新技术，可以拆分为法律研究、eDiscovery、合同管理、文件管理、文件分析自动化及面向 C 端消费者的诉讼融资、法律教育、技术驱动的法律服务等。**根据 Legal Tech 的融资分布和头部上市公司所在的领域，可以看出在大模型出现前，Legal Tech 企业的核心商业价值在于电子签名、合同管理这两个环节。**

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/006.png)

*Tracxn 2018 年报告：法律科技初创企业融资分布*

其中，**电子签名**的市场已经被头号玩家 DocuSign 所垄断，占据超七成市场份额。**合同及文件管理领域**，则出现了 CS Disco、Ironclad、Evisort 等独角兽，且服务对象均为企业法务。

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/007.png)

💡

DocuSign 成立于 2003 年，**成功原因是选择以 API 的方式打开市场，将签名功能嵌入各大成熟的软件应用中。**2005 年，与专注房地产行业的电子签名中介商 ZipLogix 成为合作伙伴，开始占领房屋出租赁、出售市场；2010 年，Apple 整合了 DocuSign 的电子签名服务，用于苹果商店等线上交易的签名认证；2012 年，与 PayPal、Salesforce、Google 达成合作。DocuSign 以电子签为入口，搭建了平台化的产品矩阵，包括合同生命周期管理、合同审查、远程公证等产品。

不过，如果和其他企业主要职能领域相比，在 Legal Tech 领域，除了电子签头号玩家 DocuSign 外，尚没有诞生其他数十亿美元收入量级的企业级软件公司。

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/008.png)

**其中的原因可能包括：**

1. 法律行业虽然工作流定义明确且价值高，但对准确性及数据质量要求也很高，不同法律领域知识细分，很难做出行业的通用工具。

2. 受传统规则和商业模式约束更大，采用新技术和工具的速度很慢。

**所以 Legal Tech 领域的公司多专注于法律领域的部分人群（如企业法务、律师）或工作的某些环节（如只专注合同管理、文件检索），没有出现行业通用工具，用户总体量小；Word 和 Email 仍是法律团队的主要工作软件。**

**LLM 带来了市场新动能**

使用 AI 来为法律行业降本增效的探索一直在持续，主要原因是培养、雇佣律师的成本都非常高。**LLM 出现前的法律 AI （以 NLP 为主）主要运用于合同管理、诉讼预测、法律研究等领域。**比较出圈的工具如以 IBM Watson 设计的在线研究工具为基础的第一个机器人律师 ROSS Intelligence，可以在一分钟内翻阅超过一百万页的法律文件。**但这些工具以信息检索为主，很难对信息进行深度的处理与分析。**

💡

十多年前律师曾因 AI 被宣传为濒临灭绝的职业。2011 年，《纽约时报》一篇文章称："昂贵的律师大军，被更便宜的 AI 软件所取代"。但后续发展证明了 AI 并非替代工具，而是提高了律师的工作效率，如搜索法律文件以获得有用信息。**这带来了更多的业务需求，法律行业就业增长速度超过了美国整体劳动力。**

**LLM 的出现极大提高了 AI 的智能水平，更重要的是，法律行业适配大模型的能力。这可以从数据、工作逻辑两个维度来看：**

• **数据维度：**

**法律场景是一个典型的 text-in/text-out 的场景**，数据以文本为主，多为绝对事实和真实案件，没有模棱两可的主观判断和情感色彩，很适合大模型学习；

• **工作逻辑维度**：

无论是美国判例法还是中国成文法，法律工作内容都有非常强的知识性、逻辑性，所以大模型适合解决法律文书审核、案件检索、法律咨询等工作。不过不同法律体系结合大模型的方式和场景有一些区别，例如在中国，利用大模型做法律咨询一般需要先援引法条。

**这对于法律 AI 软件能力有两方面的提升：**

**1. 深化法律 AI 在原有的合同管理、诉讼预测、法律研究等领域的功能。**以法律研究为例，NLP 法律 AI 时期，以搜索关键词和初步分析为主，比如对应某句话出自哪条法律；但是 LLM 可以启用对话式的搜索方式，并且可以对研究内容进行总结提炼，回答细节问题。

**2. 从“提取”到 “生成”**，生成能力可以应用于起草法律合同、为法官提供判决建议等。

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/009.png)

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/010.png)

左图，2022 年 12 月，研究员测试 ChatGPT（GPT 3.5） 使其成功的通过了法律考试。右图，GPT4 击败了 90% 参加律师资格考试的人类（Casetext 赞助）。

**最直接的影响体现在提升效率：**

**1. 工作内容方面：**

 LLM 协助律师查找法条及案例，起草、审核合同，使律师专注制定核心方案策略。如人工审核法律合同错误率高、消耗时间多、会存在主观偏见；LLM 可以帮助律师减少重复工作，通过输入数据保证知识的实时更新，减少主观偏见。

**2. 人员方面：**

减少了对初级律师的需求。缓解较小的律师事务所和独立执业者人手短缺问题，更有效地与规模更大的律师事务所竞争；法律援助律师和公设辩护人也能够更好开展工作。

**OpenAI 的 ChatGPT “横空出世”为法律从业者带来了一定的心理转变。但目前律师事务所对生成性人工智能仍保持谨慎态度，主要担忧在于准确性及隐私问题。**2023 年 3 月底汤森路透的调查发现，虽然 51% 的法律从业者认为 ChatGPT 等 Gen-AI 应该应用于法律，但仅有 3% 已经在工作中使用，2% 正计划使用，34% 处于考虑阶段，其余 60% 表示没有使用计划。15% 表示公司禁止在工作中使用 ChatGPT 等工具。

\*受访者包括分布在美国、英国和加拿大的 443 名律师事务所专业人士。

**“计时收费” 商业模式被冲击**

**企业是法律服务的最终付费方，企业预算直接决定律所营收。**近年来，许多大公司试图改变律师收费模式，通过按项目收费，而非“计时收费”来减少法律成本，费用审核也越发严格。法律基层员工工资不断上涨加上客户持续降低法律预算，**律所依靠支付给律师的工资<企业支付给律师事务所的报酬所产生的规模效应慢慢不再成立，客户和市场倒逼律师事务所采用技术提高效率。**

💡

英国法律学者 Richard Susskind 认为，律师事务所通过 "拥有年轻的律师大军”而获利，因为他们向这些律师支付的工资低于他们向客户收取的费用。

**LLM 对于按时计费的商业模式也会产生进一步的瓦解作用。**

**• 从客户角度考虑，**当客户意识到 AI 的能力，有可能不再认可传统的付费模式和需要工作时长；也可能会自己购买软件，减少对外部法律服务的依赖。

**• 从律师角度考虑，**AI 的高效会使得律师的计费时间减少，促使律师事务所改变收费模式。

**不过颠覆传统的“计时收费”模式还有一些阻碍：**

• 法律知识的高度专业化加定制化服务，客户很难客观判断服务质量，定价以律师声誉及成功案例为导向，以律师为中心的模式使效率工具的推广受到阻碍。

• 大型律师事务所建立在合伙人分享利润的所有权结构上。说服合伙人将这些钱中的一部分投资于新技术很困难，因为大部分合伙人接近职业生涯终点，采纳新技术的动力不强。

• 在美国，大多数商业交易都要通过律师完成。计时收费而非按交易是否完成或额度大小收费，可以减少律师为了自身经济利益去违法犯罪的风险。

**变化是不可逆的，领先变革者最先吃到时代红利。**如律师事务所 Axiom 摒弃了传统的计时收费，采用年度或按项目收费，声称只有大型律所费用的 25-50%。财富 100 强公司有超过一半是 Axiom 的客户，包括阿里巴巴，2019 年公司收入达到 3 亿多美元。

💡

Axiom 由美国著名的华尔街律所达维律师事务所（Davis Polk＆Wardwell）的前律师 Mark Harris 在 2000 年创立，试图重新书写律所的商业模式。到 2012 年，拥有 900 名律师，却没有合伙人。律师多为大所的前合伙人或资深律师，及大型公司的法务总监，平均拥有十年以上工作经验。

Axiom 提留一定比例的费用，其余收入均归律师个人，这一分配方式受到了大量律师的欢迎。对企业客户而言，按需求购买临时性律师服务，避免了固定人工成本等，也明显降低了法律开支。

**02.**

**法律**

**LLM  Landscaping**

法律 LLM 应用领域，目前的产品**目标客户以律师事务所为主**，主打效率的提升；也有 Robin AI 自建法律团队，采取"SaaS+"的方式面向企业客户提供服务。

**通常而言，律师的工作环节主要包括以下方面：客户诉求的沟通与拆分、法律研究（法条检索和判例研究）、客户方案设计、合同、诉讼文书或其他法律文件的处理，以及其他涉及到法律适用问题的工作。**部分 LLM 创业公司想成为律师的通用性法律助理，协助律师的所有日常工作环节；部分专注合同及法律文件的处理这一细分环节。

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/011.jpg)

*\*目前公司法务部门的法律 LLM 用例很少，原因可能在于处于安全考虑，企业还不能接受将自己的法务数据放入大语言模型。*

目前美国约 135 万名律师，中国约 57 万名律师，法国约 5 万多律师，德国约 16 万律师，全球共约 **2000 万名律师**。按照 CoCounsel Basic Research Level 的定价为 110 美元/月，**ToL 的市场规模能达到约 260 亿美元。**

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/012.png)

*点击查看大图*

因为**大模型训练能力、行业专业数据库、深入大客户工作流这三点**是成就法律 LLM 公司的关键，所以从这三个方面来看，以上公司的差异如下：

**• 模型层：**

法律 LLM 创业公司主要直接接入 API 或 finetune 大模型，不同公司选择了不同的供应商，Harvey、CoCounsel、Spellbook 接了 GPT4，其中 Harvey 和 CoCounsel 2022 年下半年就获得了 GPT4 的优先使用权，Robin AI 则选择了与 anthropic 的 claude 合作；公司多采取多个模型组合去完成不同细分任务。

**• 数据层：**

不同公司能获得的优质数据不同，这对于 LLM 的表现会产生较大影响。CoCounsel 因具有 Casetext 多年的数据积累，并被汤森路透收购，可以使用其世界级法律内容库，在数据维度具有较大优势；Lexis AI 背靠 LexisNexis 也有类似的优势。而 Harvey、Robin AI 等新兴创业公司选择与头部律师事务所、四大审计公司绑定的方式获得优质训练数据。

**• 团队层：**

公司核心团队均有出身于头部律师事务所的律师，但除了 Harvey 之外，绝大部分公司缺少大模型背景的创始人。

**• 客户资源层：**

法律 LLM 很重要的商业逻辑是向已有客户进行 upsale，客户资源积累十分重要。所以相比较之下，CoCounsel、Lexis AI 在客户端的先发优势更大，Harvey、Robin AI 等新兴创业公司则选择与头部审计公司、事务所绑定的方式，后续尝试进一步服务它们的企业客户。

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/013.png)

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/014.png)

*CoCounsel demo*

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/015.png)

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/016.png)

*Robin AI demo -*

*方便合同填写，并且可以 Ask Robin*

除了 To B、To L 的产品外，目前也出现了 Donotpay 这种 ToC 场景的法律 LLM 实践，**LLM 有机会降低公众运用法律的门槛，使人们更方便的用法律维权。比如成熟 AI 法律 Agent 直接服务 C 端用户，**咨询婚姻、离职或者租房、租办公室、创业等日常问题。Donotpay 在消费者维权领域做了初步尝试，其 AI Agent 曾和通信运营商的客服机器人直接对话，通过列举服务问题并威胁采取法律行动，最终使客服机器人给出了互联网账单每月扣除 10 美元的方案。**但是因为没有专业律师的核审环节，这对准确性提出了更高的要求，相比 B 端需要更长的发展周期。**

**03.**

**Harvey：LLM 如何再造法律服务**

**Harvey 是 OpenAI Fund 的第一批投资标的之一，其产品定位是成为律师的通用性助理，目前已经完成了红杉领投的 2100 万美金 A 轮融资，最新估值为 1.5 亿美元。Harvey 的发展还十分早期，但可以作为 “LLM 会如何颠覆法律服务”的一个研究切入点进行长期关注。**

**Harvey 的首个产品是一个在 GPT4 底座模型上加入大量法律专业数据 finetune 的 AI Chatbot，其产品形态类似 ChatGPT**，它的主要能力包括：

• 法律写作：撰写长篇、格式化的法律文件，帮助起草合同，撰写客户备忘录，作为工作起点。

• 掌握专业法律知识，可以回答复杂的法律问题，如 “第四巡回法庭中雇员和独立承包商之间有什么区别？”、“租赁合同中的这个条款是否违反了加州法律？请改写它并使其合法”等。

• 进行合同及文件的理解与处理；

• 定制公司特有的模型：使用客户特有工作产品和模板训练，以嵌入工作流，类似新员工加入律师事务所时的入职培训等。

Harvey 的第一款产品目前还在内测阶段，而根据其外部招聘负责人 Brian Burns 在其 Twitter 账号 AI Pub 上的发言，Harvey 还在秘密开发第二款产品，“比第一个产品更雄心勃勃，研发强度极高”。

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/017.png)

*AI Pub twitter*

目前 **Harvey GTM 的主要方式是 To L**，即以大型律师事务所作为目标客户，为律师事务所及其客户打造个性化定制的 LLM 工具，切入法律行业高价值、高壁垒的工作流。公开披露的标杆客户包括 Allen & Overy 及普华永道，根据 Hill 的报告，Quinn Emmanuel、O'Melveny 和其他公司已经在与 Harvey 进行演示。红杉在官方博客上表示，**目前有 1.5 万家律师事务所正在排队使用 Harvey 的 AI 产品。**

Harvey 和 Allen & Overy、普华永道等大型事务所密切合作，一方面可以借助这些事务所的大客户资源基础实现 GTM；另一方面则是获得优质数据集，基于事务所的实际使用实践来共同打磨产品，使产品更为贴合目标客户的需求。

除了获得 OpenAI 投资支持外，Harvey 另外一个值得关注的点在于它的团队。在这一批法律+LLM 创业公司中，Harvey 的创始团队唯一同时拥有 LLM 技术和行业 knowhow 背景的组合：Gabriel Pereyra 做为 CEO 及创始人曾是 DeepMind、Google Brain 和 Meta AI 的研究科学家，并参与过大模型的训练，而另外一位创始人 Winston Weinberg 则是 O'Melveny & Myers 律师事务所的证券和反垄断诉讼律师。

此外，Harvey 的其他团队成员均为人工智能研究实验室的工程师和来自头部律师事务所的律师。这样的组合使得团队**既拥有丰富的法律实践经验，同时又深入了解大模型的能力、知道如何训练模型。**

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/018.png)

此外，作为 OpenAI 最早投资的大模型创业公司之一，Harvey 也在相当早期就得到了 GPT-4 的使用权，虽然从模型能力上，Harvey 和其竞对都只是接了大模型 API 进行 finetune，但 Harvey 或许会因为对于大模型能力有更早、更深的了解以及团队天然具备的符合法律实践的产品视角而具备竞争优势。

**04.**

**Harvey 面临的挑战**

**1. 数据安全与幻觉带来的用户渗透阻碍**

LLM 在企业级应用中遭遇的数据安全与隐私的问题同样存在于法律领域。例如，即使是最早与 Harvey 合作的 Allen&Overy ，在 Harvey 的应用上仍处于起草、研究等一般性工作层面，并没有在 Harvey 内输入保密数据，更没有将其深入其客户服务。

💡

**Harvey 与 Allen&Overy 的合作**

2023 年 2 月，Harvey 签约第一个企业客户 Allen & Overy，**主要使用 harvey 进行起草并购文件或给客户的备忘录等任务。**Harvey 表示，Allen & Overy 的 3500 名律师团队的 25% 每天都会使用 Harvey，80% 每月至少使用一次。截至 6 月份，A&O 在 Harvey 中的查询次数接近 20 万次。

**但是经历了 3 个季度的尝试，Harvey 在实际用例中仍处于起步阶段。**在 Legaltech 6 月的采访中，A&O 全球技术联合主管 Daren Orzechowski 表示，内部的三个用例为**起草，研究，审查**。对于起草和研究，Harvey 解决了 "从哪里开始"的问题，帮助迈出第一步；而审查用例还在解决方案的探索阶段。**信任、安全和保密问题仍是担忧的重点**，Daren 认为 Harvey 的可靠性还没有达到要求，A&O 规定律师只能询问一般性问题，不可以输入、输出保密信息。**A&O 的客户对 LLM 如何提供服务感到好奇，但总体上还没有到达想把敏感信息放进 harvey，或外包给第三方解决方案的阶段。**

此外，LLM 一直被诟病的幻觉问题同样也会发生在 **Harvey** 。为了减轻影响，Harvey 使用大量专业数据进行微调，还做了大量数据隔离和企业的安全与合规。免责声明表示使用应在法律专业人士的监督下进行，对生成的任何信息进行核查。目前 Harvey 在通用法律上表现良好，但是在细分法律领域仍表现较差，更容易出现“幻觉”。

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/019.png)

**2. 来自老牌法律服务巨头的“打压”：**

**法律作为典型的专业服务领域，要在该领域进行 LLM****实践的核心或许在于更多的专业数据积累和法律工作经验**，所以，对于 Harvey 以及这一批法律 LLM 创业公司而言，来自老牌法律巨头以及上一波 AI 软件公司带来的竞争不容小觑。目前，老牌法律巨头和上一波 AI 软件公司都在积极收购或推出自己的 LLM Chatbot，它们的竞争优势有以下几点：

**• 老牌法律巨头资金雄厚，可以通过收购和投资的方式，与最具竞争力的法律 LLM 公司合作：**

这对于老牌法律巨头和法律 LLM 公司来说是双赢。如汤森路透以 6.5 亿美元的现金收购了 Casetext，将 Casetext 的 AI 法律实践经验与汤森路透的世界级法律内容库和行业影响力相结合，将使其 LLM 产品 CoCounsel 更具有竞争力。

此外，汤森路透还领投了合同管理平台 Rally Legal 推出的产品 Spellbook，并计划每年在人工智能领域投资超过 1 亿美元，在产品套件中开发自己的生成性人工智能工具，与微软 365 Copilot 合作为法律专业人士提供新的插件。而普华永道同 Harvey 合作的同时也在打造自己的 LLM 工具，所以普华永道是否会持续需要 Harvey 也需要打一个问号。

💡

**Harvey 与普华永道的合作**

2023 年 3 月，普华永道成为 Harvey 的第二个企业客户，签订了为期 12 个月的合同，旗下全球 4000 名律师会全部使用 Harvey。普华永道将与 Harvey 合作训练自己专有的人工智能模型，创造定制产品，包括为普华的客户定制产品服务，简化内部法律流程等。

同 A&O 类似，普华客户表示有兴趣了解生成性人工智能的潜力，但目前并没有公布任何具体用例，**核心担忧点在于数据安全问题。**

**• 法律领域的实践经验更多，在训练产品过程中能更精准定位市场和客户需求，具有法律数据积累，更利于训练大模型：**

以 Casetext 为例，2018 年推出了专为法律从业者定制的人工智能案例分析助理 CARA （Case Analysis Research Assistant），通过从文档中提取文本和引文来进行辩诉状的数据挖掘，截至 2020 年获得了 5000 多家律师事务所客户。**2020 年 1 月推出了，Casetext 又基于 Transformer 的大语言模型的搜索工具 Parallel Search，作为 Casetext 平台上起草工具的一部分，并密切关注 OpenAI 的研究进展。**

2022 年下半年，同 Harvey 一样，Casetext 也收到了 OpenAI 试用 GPT-4 的邀请。Casetext 认为这一版模型真正开始有能力应用于法律实践，**于是便迅速开发并将产品广泛的推向市场，不像 Harvey、Robin AI 等创业公司，2023 年 3 月发布的 CoCounsel 无需排队等待，可以直接使用。**

💡

**开发 CoCounsel 的成本很高**，Casetext 建立了 AI 工程师、诉讼和交易律师团队，花费了近 4000 个小时，根据 30000 多个法律问题对 CoCounsel 的输出进行了 prompt engineering。部署之前，所有 CoCounsel 应用程序都进行了 beta 测试，测试人员为来自全球的顶尖律师事务所、内部法律部门和法律援助组织的 400 多名律师。**团队会记录 CoCounsel 用户的每一条评论建议，根据客户需求来决定产品的更新。**

**数据维度，CoCounsel 还将 GPT-4 与公司自有法律数据库相结合**，分别扮演 “大脑（GPT-4）”和 “存储器（自有数据库）”，还与公司自研的 Parallel Search 和 AllSearc 结合，指导 GPT-4 从内存中检索正确的数据，回答用户的法律问题。

**• 具有客户群和声誉基础，有利于快速获取客户：**

Casetext 的客户包括个人和小型事务所、美国法律 100 强公司和企业内部法律部门。**因为已经有客户积累，通过 upsale，Casetext 向已有的客户销售 CoCounsel 并进行口碑裂变。**CoCounsel 推出之前，公司拥有 10,000 名付费客户。在 CoCounsel 推出的前 45 天，Casetext 仅自助服务产品就增加了 1000 名客户，并有很多财富 100 强企业加入，到年中收入几乎比 2023 年初翻了一番。CoCounsel 目前每天约处理 20 亿字，客户包括 DLA Piper、Eversheds Sutherland、Orrick， Herrington & Sutcliffe 和美国劳工和就业公司 Fisher Phillips。

**3. 律师事务所及大型公司自建**

数据隐私问题是大型公司的法务部门迟迟不愿采用 LLM 的主要原因之一，也有一部分企业或律所可能会选择基于开源小模型定制化的解决方案。目前法律 LLM 服务的客户主要为律师事务所，是否选择自建本质上是一个成本、效果、安全的权衡问题。除了前面提到的普华永道， Holland & Knight 律师事务所正在创建一个能帮助律师审查和修改信贷协议的 AI 工具。Ballard Spahr、Cozen O'Connor 律师事务所也在定制自己的 LLM。

**4. 通用性 LLM 能力增强**

“AGI 打败一切”的论点始终存在，模型能力的增强会淹没掉很多应用实践，但这一点或许在法律等专业领域不同存在，因为法律领域数据隐私十分重要、和对专业性要求极高，所以需要法律机构的专业数据进行打磨，更重要的是，这些数据很难公开获得。

与之对应的，**国内幂律联合智谱 AI 发布了基于中文千亿大模型的法律垂直大模型——PowerLawGLM**，不仅仅对模型进行了微调，而是使用了 Continue training，在基座模型 ChatGLM 130B 上使用更多的专业数据和迭代次数做了增量训练，加入了约 5-10%的增量语聊。这相比仅仅对基座模型进行微调能更大规模的利用法律数据，将进一步减少模型的“幻觉”问题，提高在法律领域的专业推理能力和准确性。

**05.**

**结论**

法律行业采用 LLM 的速度仍很缓慢，是伴随着 LLM 能力的提升和”幻觉“"数据隐私”问题解决的缓慢渗透过程。正如上文所提到的，**大模型训练能力、行业专业数据库、深入大客户工作流**，是成就法律 LLM 公司的三要素。**而同时拥有大模型专业能力和最丰富的法律专业数据及客户群的公司将占据竞争优势。与普华永道达成密切合作关系的 Harvey 及汤森路透 Thomson Reuters 收购的 Casetext 都值得密切关注。**

法律 LLM 及 Harvey 能否成长起来有以下待解决的问题：

**1. 数据隐私问题**

客户同意将隐私数据放入 LLM 是法律 AI 深度发挥作用的前提。目前的问题在于客户担心放入 LLM 的数据可能成为模型训练数据的一部分，导致数据泄露。这可能违反对客户的保密义务和个人的数据隐私权，如在欧洲可能会违反欧盟《一般数据保护条例》（GDPR）的原则。

Harvey 正在努力满足客户的合规需求，对用户数据进行匿名处理，并在预定时间后删除数据，用户也可以根据要求随时删除数据。但正如上文提到的，这些措施似乎并没有说服客户，极少有客户愿意将隐私数据放入 Harvey 等 LLM。

💡

**CoCounsel 客户数据隐私保护解决方案：**

1. CoCounsel 通过私人专用服务器和零保留的 API 访问 OpenAI 的 GPT4 模型。所有数据在传输过程中都被加密。这意味着 OpenAI 存储任何客户数据的时间不能超过处理请求所需的时间，并且不能查看任何这些数据或使用它们来训练 CoCounsel 的底层 LLM。用户始终保留对数据的控制权，并可以在任何时候将其从平台上完全删除。

2. 采用复杂、多方面的安全计划：确保 CoCounsel 符合 NIST 800-53-mid 和 NIST 网络安全框架（业内最受尊敬的两个安全框架）。CoCounsel 安全控制符合 ISO 27001 和 SOC 2 标准（国际公认的信息安全管理的最佳实践）。

**2. 幻觉问题**

Gabriel 表示人工智能有许多方式来防止和检测幻觉。Harvey 针对海量法律数据集的法律用例进行了微调，与现有系统相比，大大减少了幻觉。即便如此，Harvey 还是会出错，所以 Allen & Overy 有围绕 Harvey 的风险管理计划。用户必须验证 Harvey 中出来的一切。

💡

**"幻觉” 案例：**Levidow & Oberman 律师事务所的 Steven Schwartz 向美国纽约南区地方法院提交了一份由 ChatGPT 生成的备忘录，该备忘录包含对**六个不存在的案例的引用**。他的审核方式是询问 ChatGPT 这些案例是否是真实的，而 ChatGPT 保证 "提供的案例是真实的，可以在有信誉的法律数据库中找到"，并提供了虚假的 URL。

**目前的幻觉解决方案主要有以下两种：**

• **人类反馈强化学习”（RLHF）：**

OpenAI 首席科学家 Ilya Sutskever 提出，让模型对错误的输出结果进行调整。最新的 RLHF 框架为 FINE-GRAINED RLHF（细粒度的人类反馈强化学习）。通过多种不同类型的“打分器”（reward model），对语言模型输出的每句话进行评估，能很好地降低语言模型生成内容的错误率、毒性，并提升它回答问题的全面性和解析能力。但目前这种方法还是类似于通过建立“不许做什么”准则来限制胡说八道行为，并不是从生成本身解决幻觉问题。

**• 向量嵌入（vector embeddings）：**

通过为大语言模型创建一个向量数据库，把来源权威，可信的非结构化数据转换成向量，并储存到数据库中，就能帮助大语言模型具有“长期记忆”，并且减少它产生“幻觉”的可能性，这可能是更靠谱的办法。

💡

**CoCounsel 就采用了向量嵌入的“幻觉”解决方案：**将 GPT4 与公司专有法律数据库相结合，该数据库是全面、准确、最新的法律语料库，如州和联邦案例法、法规、条例。工程师 "指示"该平台根据数据库中包含的实际段落进行回答，或者根本不回答，这意味着 CoCounsel 的所有输出都来自于法律信息汇编，不给 CoCounsel 任何产生幻觉的机会。同时，推出 CoCounsel 以后团队每天都进行测试，通过输入和检查数以千计的查询，推出了后台警报程序，筛选和标记潜在的不准确之处，审查并防止它们出现在终端用户面前。

但目前仍没有从根本上解决幻觉的方式，大语言模型的使用离不开人工的核审。

**3. 数据造成的偏见及负面用例**

**大模型的价值取向受到训练的数据集的影响，使用人工智能可能会反映甚至放大司法系统数据中固有的偏见。**大多数合同从未在法庭上出现过，所以它们的条款未经测试，使用这些合同训练的人工智能生成系统有可能同时反应错误和正确的工作。如 Equivant 公司开发了替代性制裁的罪犯管理分析（COMPAS），用来评估被告的累犯风险，以决定拘留、判刑或提前释放。根据 ProPublica 的研究，这种评估工具似乎对黑人囚犯有偏见，将他们标记为比白人囚犯更有可能重新犯罪。

**AI 也有可能被用来操纵或欺骗他人。**例如生成虚假或误导性的法律文件。这需要针对 AI 的能力制定合理的监管规则。

**同时，法律 LLM 还有一些值得讨论的问题：**

**• 行业最终广泛的解决方案为 OpenAI GPT 系列等大模型，还是开源小模型？**

Harvey 采用 OpenAI GPT4 作为底座模型，但目前市场上也存在微调开源模型的解决方案。**GPT4 等大模型的优势**在于模型能力显著更强，目前开源小模型仍难以超越。不过有社区观点认为，模型不需要绝对领先的能力，在特定任务上能力足够即可。

**开源小模型优势**在于训练基座模型的数据量较小，在微调过程中可以较容易地通过增加法律数据的比例来提升在法律场景上的表现；同时也可以有效保护企业隐私，避免信息泄露的风险。

**开源模型的能力配上专业化数据集，在法律场景是否够用？**如果够用，大型客户可能会普遍选择内部部署开源模型，Harvey 可能就会从 SaaS 产品公司转变成模型训练提供商。此时模型部署公司（如 cohere）也可能成为 Harvey 的潜在竞争对手。亦或者该领域会像云平台一样演变，大企业最终也会接受大模型的 SaaS 服务。

**• 律师的培养体系将如何演进？**

**如果律师事务所减少对初级律师的需求，如何培养高级律师呢？**大型律师事务所培训年轻律师的主要方式是从基础的案头研究做起，比如翻阅数百万页的文件，找出可能存在问题的合同；对相关案例进行基础法律研究，为资深律师准备 memo 等，**这正是法律 LLM 擅长做的事情。**如果初级律师不再需要做这些工作，他们如何成长为资深律师？不过， AI 也可能会促使律师事务所重新思考培养初级律师的方式。

**06.**

**附录**

**1. 融资**

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/020.png)

**2. NLP 阶段的法律 AI**

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/021.png)

**Reference**

https://www.mdpi.com/2071-1050/11/4/1015#https://www.harvey.ai/blog

https://www.legaldive.com/news/law-firms-generative-AI-ChatGPT-artificial-intelligence-thomson-reuters-institute/648075/

https://fortune.com/2023/03/07/openai-chatgpt-llms-legal-software-robot-lawyers/

https://www.wired.co.uk/article/generative-ai-is-coming-for-the-lawyers

https://clp.law.harvard.edu/knowledge-hub/magazine/issues/generative-ai-in-the-legal-profession/the-implications-of-chatgpt-for-legal-services-and-society/

https://businesslawtoday.org/2022/02/how-ai-is-reshaping-legal-profession/

https://legal.thomsonreuters.com/en/insights/articles/ai-and-its-impact-on-legal-technology

https://www.nytimes.com/2023/04/10/technology/ai-is-coming-for-lawyers-again.html

https://www.forbes.com/sites/robtoews/2019/12/19/ai-will-transform-the-field-of-law/?sh=225c72d17f01

https://medium.com/leislat-io/artificial-intelligence-robots-replacing-lawyers-592e09ba15bf

https://iacajournal.org/articles/10.36745/ijca.343

https://hbr.org/2018/02/how-ai-is-changing-contracts

https://www.nytimes.com/2023/04/10/technology/ai-is-coming-for-lawyers-again.html

https://www.pwc.com/gx/en/news-room/press-releases/2023/pwc-announces-strategic-alliance-with-harvey-positioning-pwcs-legal-business-solutions-at-the-forefront-of-legal-generative-ai.html

https://fortune.com/2023/03/01/will-artificial-intelligence-replace-lawyers-ai-harvey-aron-solomon/

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/022.png)

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/023.png)

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/024.png)

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/025.png)

延伸阅读

[![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/026.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503488&idx=1&sn=24bf3cef8b6d859e0b3d4607dc3235b3&chksm=ce9b711ef9ecf808c248dbde533b37b47ced78cdabc4d25b31e96d7fbbab265029d00af377bf&scene=21#wechat_redirect)

拾象硅谷见闻系列：生产力 SaaS 如何应对 AI 的颠覆？

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/027.png)

[![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/028.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503441&idx=1&sn=19397a87b3993ccd6f85fcfcc872d13f&chksm=ce9b71cff9ecf8d919696795beea88ba25056c52262bd5b43e278fa34ec6927fbb118dfff3f8&scene=21#wechat_redirect)

Covariant：OpenAI Mafia创业，为机器人开发AI大脑

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/029.png)

[![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/030.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503355&idx=1&sn=587f9d2354699b5531e797c9c5f3b157&chksm=ce9b7265f9ecfb73a213f324904851a4bde4223cf9728b28ccbe289ea7969c9eebe596da4787&scene=21#wechat_redirect)

拾象实践：为了理解AI-Native，我们做了几款AI应用

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/031.png)

[![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/032.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503155&idx=1&sn=ce93d9e4476ca641d2c5f1283d4ef563&chksm=ce9b72adf9ecfbbbc90a551840965531cb8174620b4bbc31a6d03489c70bf3e611a3cca64bf6&scene=21#wechat_redirect)

Perplexity AI，比Google Bard和Bing Chat更靠谱的问答引擎

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/033.png)

[![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/034.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247503042&idx=1&sn=64c30e9be599064b90f8b57891ab1f9d&chksm=ce9b735cf9ecfa4a2c3fb60d4de31d02b52ce15406eb2feab41854d3749ae305abdd4cf4cee7&scene=21#wechat_redirect)

OpenAI基金首批投资赛道，Kick是下一代ERP雏形？

![](../images/2023-08-04-harvey-openaitou-zi-de-fa-lu-copilot-zui-gua-he-llmluo-di-de/035.png)
