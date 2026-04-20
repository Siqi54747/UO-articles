---
title: Mistral AI：欧洲最强模型团队，打造开源轻量LLM
publish_date: '2023-11-23'
publish_timestamp: 1700741133
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/v747iGx_XpZhGlbhySlCjw
msgid: 1000000234
appmsgid: 2247505540
itemidx: 1
digest: 期待Mistral AI的下一代新模型成为game changer的潜力。
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxV1wUXFeDKUmr0UPfJ24QicyUib8gRzaxhja5x0136RiaAeIjZW1xMibjOzZMaRqgiaclv975I9gTnDVw/0?wx_fmt=jpeg
image_count: 28
archived_at: '2026-04-20T01:51:47+08:00'
---

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/001.gif)

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/002.png)

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/003.png)

作者：Cage

编辑：penny

排版：Scout

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/004.png)

Mistral AI 是欧洲最强的 LLM 大模型公司，团队由来自 Google、Meta 和 Hugging Face 的新生代法国科学家们组成。法国是欧洲 AI 人才最集中的地方，Falcon 模型和 Hugging Face 社区都来自法国团队。他们**在多模态、检索增强生成（RAG）等大模型突破方向有着丰富经验**，有理由期待 Mistral AI 的下一代新模型成为 game changer 的潜力。

企业端使用 LLM 时考虑的不仅是最前沿的模型能力，也包括**数据安全隐私、成本控制**等多种考虑。向企业开放的开源模型更符合**定制化、私有化使用**的需求，而 OpenAI 等闭源模型公司并不能满足这样的需求。未来的 LLM 市场很可能是开源模型满足基本的智能需求，闭源模型满足高阶的智能需求。随着模型的升级，开源模型能满足的需求逐渐变多。

欧洲市场是 Mistral AI 的机会和挑战，**欧洲企业对新技术 adoption 保守、数据监管严格**，且付费能力强，是适合欧洲科学家们使用开源模型获取信任的市场。对于这样一个科学家为主的公司，走向市场的能力会成为他们的短板。

但**开源模型的商业化还没有得到充分验证**，公有云厂商也完全有能力 serve 开源模型、进入欧洲市场，尤其 Mistral AI 希望打造的是一个轻量级的 LLM，企业使用时并不会有很高的使用门槛。Mistral AI 当下最大的挑战并不只是训练出优秀的模型，还有找到**关键的企业合作伙伴**。

**以下为本文目录，****建议结合要点进行针对性阅读。**

****👇****

01 Overall Thesis

02 Mistral 7B，最强开源小模型

03 团队与融资历史

04 关键问题

05 需要开放、安全模型的欧洲市场

**01.**

**Overall Thesis**

**1. 打造优秀的 LLM 科学家团队**

Mistral AI 团队打造了目前市场上最强的小模型，用 7B 模型越级达到了大部分模型 20B 左右的水平。且实际使用时进一步微调的表现也比其他模型更容易学到领域专用知识，得到很多开源和企业使用者的认可。根据 Percy Liang 团队最新 update 的 HELM 模型测评报告，**Mistral 7B 的表现甚至超越了 Cohere 52B 的模型：**

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/005.png)

Mistral 创始团队大部分来自 Google、Meta、Hugging Face，之前领导过 Llama 1&2、Flamingo（Google DeepMind 论文，GPT-4V 外最重要的多模态模型）、Chinchilla（Google DeepMind 论文，建立了模型数据与参数量的标准）、RETRO（Google DeepMind 论文，第一个结合 Retrieval 和 LLM 的大模型）、BLOOM（Llama 1 出现前的最重要开源模型）等重要模型。由于他们有着多模态大模型、检索增强生成（RAG）大模型的丰富经验，有理由期待 Mistral AI 的下一代新模型成为 game changer 的潜力。

**2. 开源模型能更灵活地满足企业需求，尤其是欧洲市场**

企业端使用 LLM 时考虑的不仅是最前沿的模型能力，还会希望数据安全隐私、控制成本等多种考虑。因此向企业开放的开源模型在很多场景下是更符合企业定制化使用的需求，而 OpenAI 等闭源模型公司并不能完全满足这样的需求。未来的 LLM 市场很可能是开源模型满足基本的智能需求，闭源模型满足高阶的智能需求，两者互补。

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/006.jpg)

*Source：Retool State of AI Report*

同时欧洲企业对新技术 adoption 保守、数据监管严格，且付费能力强，是适合 Mistral AI 使用开源模型获取信任的市场。且 Mistral 的种子轮投资方有很多欧洲大企业，能成为长期合作伙伴。

**3. 务实、贴近企业需求的战略路线**

Mistral 团队有能力打造 OpenAI、Anthropic 水平的前沿闭源 LLM，但他们选择开放模型交给企业端部署、定制化使用，是符合企业需求的差异化路线。其未来战略 roadmap 有着对企业端需求的深入理解，例如其中提到内容热插拔（context hot-pluggable）的 LLM，就是为企业在不同使用场景进行数据权限控制的定制化，这一需求在大部分在意数据隐私和安全的公司都将非常重要。

**02.**

**Mistral 7B，最强开源小模型**

Mistral 7B 是 Mistral AI 团队在 9 月底发布的开源模型，尽管在 Llama 2 之后发布，但 Mistral 7B 成为了所有 7-13B 小模型中最有竞争力的模型，在开源社区中话题讨论度比较高。这个模型表现出几个重要特点：

**1. 跨级挑战成功的小模型**

在大部分 benchmark 上，Mistral 7B 的能力都比 Llama 2 13B 更优秀。例如在语言能力上，MMLU（多语言能力）这个在欧洲市场很重要的能力 Mistral 有着显著优势；在推理能力上，Mistral 也只是小幅弱于 Code-Llama 7B 这个专门在代码场景训练的模型。

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/007.png)

**2. Low cost, low latency**

Mistral 7B 专门为低推理成本和延迟做了优化。整个模型架构中最差异化的亮点为：

• grouped-query attention，能加快推理速度；

• sliding window attention，能够增大 input context，并降低推理成本。

Hugging Face CSO 在推特中以 Summarize.tech 为例，提到他们在实际应用中，使用 Mistral-7B 替代了 GPT-3.5 节省了一大半的推理成本。这代表了 Mistral 的底座模型能够帮助企业平衡模型能力和成本控制之间的 tradeoff，是开源模型中最有竞争力的选择之一。

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/008.png)

**4. Easy for fine-tuning**

尽管 Mistral 9 月底才发布，但是开源社区已经很快推出了很多基于 Mistral 7B 的微调模型，开发者普遍的反馈是 Mistral 7B 很适合根据使用场景进行进一步 fine-tune。

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/009.png)

*You.com 创始人对 Mistral 基座模型能力的认可*

其中比较有代表性的反馈来自 MetaMath 团队，他们原本是开发了自己针对数学场景的开源模型 MetaMath 7B/13B，但最近将 Mistral 发布模型之后将其 base model 切换为了 Mistral 并将自己的数学数据集加入进行微调，得到的效果更优，可见 Mistral 7B 的泛化能力是相当优秀的：

***GSM8k Pass@1* MATH Pass@1**

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/010.png)

此外，还有三个非常优秀的 mistral AI 微调的模型，都在各类微调模型的 leaderboard 中排名很靠前：

• Multimodal: BakLLaVa-1

• Model fine-tuned on direct preferences: Zephyr-7B-alpha

• Model fine-tuned on generated data: OpenOrca

总的来说，Mistral 7B 已经非常优秀，让人期待他们的下一代模型，可能是 Mistral-13B/70B，能成为开源世界的 game changer。能做到这样优秀的模型，离不开他们优秀的科学家团队。

**03.**

**团队与融资历史**

Mistral AI 是科学家为主组成的团队：团队年轻、研究能力强，技术栈互补且全面，在 LLM Pretrain、Alignment、RL 和 Infra 等环节都有擅长的科学家。其中7人来自Facebook（4位是 Llama 的参与者），3人来自Hugging Face，2人来Deepmind。

大部分都参与过知名 LLM 模型：Llama 1&2、Flamingo（Google DeepMind 论文，GPT-4V 外最重要的多模态模型）、Chinchilla（Google DeepMind 论文，建立了模型数据与参数量的标准）、RETRO（Google DeepMind 论文，第一个结合 Retrieval 和 LLM 的大模型）、BLOOM（Llama 1 出现前的最重要开源模型）等。

有趣的是，Mistral 7B的论文作者中囊括了公司所有成员，商业方向以及助理方向员工亦在作者名单中。其中有6位为偏科学探索方向的 scientist，6位是偏工程实现方向的 engineer，2 位负责 BD 和 GTM。

Mistral AI 的管理层一共四人。其中CEO Arthur Mensch来自Deepmind，参与了Deepmind的多个经典的模型：Flamingo、Chinchilla、Gopher。CTO 和 Chief Scientist分别是Llama & Llama2的核心工程、研究角色（由于离职，并未在Llama2论文中体现）。Chief Business Officer Florian 则由创始顾问，Alan的CEO推荐加入。

**CEO：Arthur Mensch**

Arthur 加入 Mistral AI 前曾于2020年11月至2023年7月于Deepmind任职三年。Arthur参与了Deepmind的多个经典的模型：Flamingo、Chinchilla、Gopher、RETRO，是其中Flamingo和Chinchilla的核心贡献者。因此，Arthur的研究能力非常优秀。

Arthur的研究领域聚焦于多模态、RAG、LLM，参与的项目都是Deepmind最知名的几大项目。此外并没有很多的职业经历，其履历相比 CEO 更符合科学家的定位。

**CTO：Timothée Lacroix**

Timothée在读期间即在Facebook实习，从毕业后加入Facebook至离开创办Mistral AI共在Facebook工作八年。Timothée的工程能力很强，是Llama和Llama2的核心技术贡献者。他其他的研究方向聚焦于Inference、Embedding Model。Timothée对Inference cost的管理能力研究很深入，近期有一篇访谈聚焦于Inference cost：https://www.youtube.com/watch?v=mYRqvB1\_gRk 。

**Chief Scientist：Guillaume Lample**

Guillaume与Timothée一样来自llama的核心贡献团队，二位路径亦非常一致，自实习开始就在Facebook。2016年至2023年近7年时间内，Guillaume在Facebook发表多篇重要的学术论文，他的研究方向聚焦于Transformer Architechture、Pretrain、Reasoning。

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/011.jpg)

*Chief Scientist 对 Meta 将他移除 Llama 论文名单表示不满*

**Chief Business Officer: Florian Bressand**

在加入Mistral AI之前，Florian于2005年加入麦肯锡，服务于零售和旅游行业的客户，任职12年。借助客户积累，他于2017年4月加入Mirakl，担任COO。Mirakl是市场上唯一一家可以让B2B和B2C机构规模化建立和发展企业电商平台的SaaS独角兽公司。Mirakl的客户包括许多零售巨头，如Best Buy、Office Depot、Hudson's Bay、Kroger、Express、Urban Outfitters、家乐福、迪卡侬等。同时Mirakl也开拓B2B业务，获得了空客、丰田、惠普等公司的订单。Florian在Mirakl主要负责三个团队：销售、客户成功和战略，见证了Mirakl从B轮到E轮的成长，成为法国的SaaS独角兽。2023年4月，Florian离开Mirakl，经过Board meber Jean的介绍加入Mistral AI。

Florian 之前在 Saas 公司的成功经验会对 Mistral 的 GTM 有很多帮助：

• Mirakl 的业务增速非常迅速，2022年已经保持了3年的40%以上增长。2023年的续订收入达到1.35亿美元。

• 在 Mirakl 的客户结构中，B2C企业依然占大多数，占整体业务的84%。

• Mirakl 不做小B生意，以中型企业和大型企业客户为主。

此外，在 Mistral 董事会和顾问席位上也有几位成功的创业者和公众人物。Alan 是法国最成功的保险公司之一，其 CEO Jean-Charles Samuelian 和 CTO Charles Gorintin 都是 Mistral 的创始顾问，同样还有 Cédric O，前法国数字事务国务秘书。他们的帮助都能为这个科学家为主导的公司进行保驾护航

**融资历史**

Lightspeed Venture 的种子轮阵容十分庞大，由欧洲 LightSpeed 领头，法国的 Redpoint、Index Ventures、Xavier Niel、JCDecaux Holding、Rodolphe Saadé和Motier Ventures，德国的 La Famiglia和 Headline，意大利的 Exor Ventures，比利时的 Sofina，以及英国的 First Minute Capital 和 LocalGlobe 也都参与其中。法国投资银行 Bpifrance 和谷歌前首席执行官Eric Schmidt也是股东。接近该公司的消息人士证实，种子轮融资金额为 1.05亿欧元的融资，Mistral AI 的估值达到 2.4 亿欧元，股东占比接近 50%。

其中 JCDecaux Holding 这样的企业战略投资者也是欧洲的内容提供商，他们有可能为获取高质量的数据集打开大门，让 Mistral 的模型可以进行训练和微调。

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/012.png)

总的来说，Mistral 的投资人背景是非常 impressive，其中有一些潜在的合作伙伴和社会资源，会为他们长期的商业化路径打下不错的基础。

**04.**

**关键问题**

**1. 商业化路径：开源模型的付费客户是谁？**

目前 Mistral AI 还没有开始商业化，我们认为未来 Mistral 最佳的 GTM 策略还是服务高价值用户，尤其是欧洲那些开放性、数据安全性和模型能力并重的大企业。其具体的商业化形式可能有三：

**• 卖开源模型的定制化版本**

在企业实际使用的时候，可能有各种数据 IP 上的顾虑和定制化的需求，Mistral 能够将其修改并卖给企业。

**• 标准商业化 api**

这一商业化路径与闭源厂商的产品形态接近，开源模型 API/平台目前确实还没有过成功的商业实践，目前这块业务收入最高的应该还是 MosaicML。

**• 模型 inference 平台**

为企业提供模型 serving、RAG、定制化服务等能力的平台。这一形式接近目前的 model inference infra，但 Mistral 对模型训练的细节，能做更彻底的优化。

这里最大的挑战还是开源模型的商业化：开源模型展现出了满足基本业务需求的能力，是应用层公司为自己、Infra 公司为客户降低成本的重要手段。Mistral 和 Llama 2 都开始有了一定的 adoption，但是还未出现围绕着开源模型好的商业模式， Stability、Mistral 并不能从每一次商业使用中获得收入。未来优秀的小模型可能会继续作为应用公司、工具公司，乃至公有云的生态合作伙伴，但不一定会有高价值的付费。

**2. 服务价值差异点：轻量级模型部署难度小，服务价值不明晰**

Mistral 有一个战略是开发轻量级模型，可以在边缘端为每个人提供 AI 助手。小模型的部署难度是远低于标准大模型的，可能是未来每个硬件必备的一部分，因此很难产生高客单价高价值的商业模式。Stability AI 就有遇到类似的困难，文生图模型的inference难度不大企业可以自行部署，同时还有很多专业 inference 公司以更低廉的价格提供类似的服务，使他们的营收难以快速 scale。

同时 OpenAI、Anthropic 等公司都有希望能够打造出优秀的小模型，只是他们目前的战略重心还在追求 AGI 上。比如 GPT 3.5 Turbo 其实就是基于之前的 GPT 3.5 和训练 GPT 4 的经验，重新进行训练和 scale down 得到的模型，其效果出色且成本很低。

**3. 竞争格局：LLM 领军者和公有云厂商，欧洲市场是否能支撑起独角兽公司**

后面将分析到欧洲市场可能有独立的 LLM 机会，但这一判断是存在变数的。欧美之间的文化相似度是最高的，彼此之间比较容易对齐。因此在美国能够发挥价值的大模型迁移到美国也不会有太大的阻碍，并不像其他地区可能还需要价值观的重新 alignment。

同时，各大云厂商在欧洲市场的渗透率已经很高了，很多前面提到的财富500强公司已经 adopt 了公有云。而且 Google Deepmind London 的人才有很大比例来自欧洲，欧洲市场的独立性是有可能被 tech giant 侵蚀的。最近微软也已经宣布了 serve Mistral 模型。

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/013.png)

在开源模型层面上， Mistral 最大的竞争对手和变量是 Meta，在 LLM 领域 Meta 近期变得团结且很卷，不容易击败。Meta 的开源和 OpenAI 纷争中人员的流动是最有可能推动技术扩散的。

另一个视角是看欧洲独角兽收入中美国市场的占比：欧洲软件行业的优秀案例是 SAP、 Adyen 和 Hugging Face。欧洲在这些公司的收入百分比中都不是高占比。SAP 收入的 42% 来自美国，43% 来自 EMEA（欧洲、中东和非洲），其中 34% 来自德国；Adyen 收入的 50% 来自 EMEA；Hugging Face 主要收入来自美国。

**05.**

**需要开放、安全模型的欧洲市场**

Mistral AI欧洲市场与美国乃至全球市场比起来，是有着特殊的机遇和挑战的。

**优势分析**

**1. 企业付费能力强**

欧洲拥有大量的财富500强公司，这意味着企业有足够的财力投资于先进的技术解决方案。特别是在法国、德国、英国、瑞士和荷兰等国家，这些企业多集中在传统行业如汽车、石油和天然气、制药、电信、银行和保险等。

财富500强公司中有近四分之一来自欧洲，如果按国家拆分的话主要来自：

• France - 31

• Germany - 27

• United Kingdom - 22

• Switzerland - 14

• Netherlands - 10

**2. 技术工程能力相对较弱**

相较于美国等地的科技公司，欧洲的企业在技术工程方面相对较弱。这为LLM公司提供了进入市场并提供技术支持和服务的机会。

根据行业进行拆分，欧洲公司主要为传统公司，技术工程能力弱：

• Automobiles - Volkswagen, BMW, Mercedes-Benz, Stellantis

• Oil & Gas - Royal Dutch Shell, TotalEnergies, BP

• Pharmaceuticals - Roche, Novartis, GlaxoSmithKline

• Telecommunications - Deutsche Telekom, Orange, Vodafone

• Banks - HSBC, BNP Paribas, Credit Suisse

• Insurance - Allianz, AXA, Zurich Insurance

**劣势分析**

**1. 严格的监管环境**

欧洲对新技术的使用和数据监管非常严格，特别是在个人数据保护方面。GDPR的实施意味着任何在欧洲运营的公司都必须遵循严格的数据处理规则，包括数据访问、修改、删除的权利，以及在数据泄露发生时的快速报告要求。

💡

GDPR是欧盟于2018年5月实施的一项关键数据保护法规，旨在统一欧洲的个人数据保护法律，并增强欧盟公民对其个人数据的控制权。GDPR的主要特点包括：

1. 适用范围广泛：GDPR不仅适用于欧盟境内的组织，也适用于处理欧盟居民个人数据的境外组织。

2. 严格的处罚措施：违反GDPR的组织可能面临高达全球年营业额4%或2000万欧元的罚款。

3. 增强个人权利：个人有权访问、修改、删除其数据，并可以随时撤回同意。

4. 企业责任加强：企业需要设置数据保护官，并在数据泄露发生后72小时内报告。

5. 数据传输：规定了个人数据跨境传输的规则，确保数据在离开欧盟时仍受到保护。

6. 同意和透明度：要求企业在收集和处理个人数据时获得明确同意，并向用户提供透明度。

**2. 企业对技术开放度的要求高**

由于监管环境的严格性，企业对采用的技术解决方案的开放度和透明度有更高的要求。这可能会减慢技术的采用速度，尤其是对于依赖大量数据和复杂算法的LLM产品。

💡

欧盟AI法案是首个全面的人工智能法律框架，目前仍在立法过程中。其主要特点包括：

1. 风险基础的分类：将AI系统分为三个风险等级：不可接受风险、高风险和有限风险。不可接受风险的AI系统将被禁止，如生成“信任度”分数的系统。高风险AI系统（如用于招聘和福利决策的系统）须遵守严格的合规要求。

2. 基础模型和生成AI的额外要求：对于基础模型和生成AI，提供商需要在市场上推出模型之前，通过适当的设计和测试来识别和减少健康、安全和基本权利的风险。还必须在欧盟数据库中注册这些AI系统。

3. 透明度要求：特别针对与人交互的AI系统（如聊天机器人），要求提供明确的透明度，让用户知道他们正在与AI系统而非真人互动。

4. 监管沙盒和标准定义：提出了监管沙盒用于AI实验和发展，以及行业主导的合规标准制定过程。

5. 欧盟以外的影响：虽然AIA的影响可能主要局限于欧盟，但其对全球AI开发和监管环境的塑造作用不可小觑。

根据 EU AI Act 的条例去进行分析，目前市场上的模型安全都尚未满足这一要求，其中唯一基本满足的是 Hugging Face 的 BLOOM 模型，也正是 Mistral AI 团队中两位成员之前领导的项目。对 EU AI Act 的遵守，会是 Mistral 比较大的机遇和挑战。

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/014.png)

**机遇点**

Mistral AI 的策略是模型checkpoint的完全开放和Apache 2.0协议，以及针对企业端的定制化服务。这种策略非常适合欧洲市场，能够提供更符合当地法规和企业需求的产品。根据上半年 Mistral 泄露的战略memo，他们对最近一年有如下规划：

1. 他们将首先专注在训练最好的 LLM 上：打造可以击败 ChatGPT 3.5 、Bard 和 Claude 2 的模型，充分向合作伙伴验证自己的技术能力。其中一部分模型是开源的建立标准，另一部分是商业化供企业端进行使用的。

2. 下一步做 embedding model 和多模态模型来实现技术的差异化，发挥团队的优势技术能力。

3. 最后实现两个目前没有解决的需求，这两个会与合作伙伴一起进行推进：

• 训练能运行在 16GB 笔记本电脑的小模型，成为一个有用的人工智能助理；

• 训练可hot-pluggable extra-context 的模型，也就是将 RAG 和 LLM 结合在一起。

这一路线非常务实，也非常适合欧洲市场。因为总的来看，虽然欧洲市场在监管严格性、企业对技术开放度要求高等方面存在挑战，但其强大的企业付费能力和技术服务需求，为独立的LLM大模型公司提供了显著的机会。特别是像Mistral AI这样能够提供开放、透明且定制化的服务的公司，可能会在欧洲市场获得成功。重要的是需要在遵守当地法规的同时，灵活调整产品和服务以适应市场需求。

值得关注的是，欧洲这两年的创新创业生态有着一定的进步，今年的独角兽数量已经超越了中国市场：

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/015.jpg)

综上我们期待 Mistral AI 能找到文中关键问题的解法，成为欧洲市场的 OpenAI，推动 LLM技术的开放和落地。

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/016.png)

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/017.png)

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/018.png)

延伸阅读

[![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/019.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505500&idx=1&sn=a4e443893c4f1a977fa240c65f12ffb2&chksm=ce9b69c2f9ece0d4b75914e979fdbc8e0ee32b9e1f935ed0db2ce27661cb919ac99f4762c4ee&scene=21#wechat_redirect)

2023独角兽市值分析：Gen AI的崛起与地域分布

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/020.png)

[![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/021.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505355&idx=1&sn=e8b1d121d20b3f275db936d81db1a009&chksm=ce9b6a55f9ece343098cca201e0fd7584b30858925ead37f0facd280f940e6dcf316dfcde703&scene=21#wechat_redirect)

Figure：为人类部署数十亿台人形机器人

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/022.png)

[![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/023.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505317&idx=1&sn=abbaa85b85b680f5da92163621bdfb7d&chksm=ce9b6a3bf9ece32d5e2d8dd4bb0a28c15ec413975d312f29400edbd58ea244215591a6037a89&scene=21#wechat_redirect)

Endor Labs：比Snyk更进一步的开源安全卫士，Prisma Cloud操盘手创立

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/024.png)

[![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/025.jpg)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505241&idx=1&sn=a4494cb520106b02aa183fa663f88bbf&chksm=ce9b6ac7f9ece3d1c691379df492f533234e68d5883e00a56cdedffe0d94c6becca64b5851e1&scene=21#wechat_redirect)

Hex：数据行业会出现“Figma” 的机会吗 ?

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/026.png)

[![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/027.png)](http://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247505204&idx=1&sn=eaf9d179c6a41cd0dac7b88e201573e8&chksm=ce9b6aaaf9ece3bcae1bb525bc53a23e2781dd048022cc5a3e4411e499540f1adc17f9af11ad&scene=21#wechat_redirect)

Inceptive：指令药物时代的 AGI 编辑器

![](../images/2023-11-23-mistral-ai-ou-zhou-zui-qiang-mo-xing-tuan-dui-da-zao-kai-llm/028.png)
