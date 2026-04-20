---
title: 对谈 Pokee CEO 朱哲清：RL-native 的 Agent 系统应该长什么样？｜Best Minds
publish_date: '2025-08-01'
publish_timestamp: 1754049600
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/kw2HbUqryB4E8V-1j9w7Ag
msgid: 1000000395
appmsgid: 2247515450
itemidx: 1
digest: RL 系统如何让 Agent 会学、会记、会探索
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgxDfg4PPC68DAPNy9icKO5ibu3K7GkDcbwrichsKJ1ib2oN0EbtB9rtqmu53nWOqe3BeOibh0IxDtp6Aow/0?wx_fmt=jpeg
image_count: 21
archived_at: '2026-04-20T04:05:22+08:00'
---

[![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4022587657917186053&subscene=126&scenenote=https%3A%2F%2Fmp.weixin.qq.com%2Fs%3F__biz%3DMzg2OTY0MDk0NQ%3D%3D%26mid%3D2247514246%26idx%3D1%26sn%3Dde104fc02cb120d9180f47b22fa4a1ef%26chksm%3Dcf71d6a76892668cf18f007c4c9974e8d4c946ed18281f0143b7aedede4e175cc1910467c9ba%26scene%3D126%26sessionid%3D1750994837%26subscene%3D227%26clicktime%3D1750994839%26enterid%3D1750994839%26key%3Ddaf9bdc5abc4e8d03659350f1d5aeabe879f96bc6ba36414330ae668002f202b47d03b5db81c8b59665b83c1f8583ed968cbf8713d565f7013dadcb18b5804616bb5ce7883c006475ceef002b63ded413b8449bda249ab3abfe984c0cd65c1607e949c660fbedd2861c0575826fd540c6b63d48daf52d266776cd0faaf14674e%26ascene%3D78%26uin%3DMzQ2MTE3Mjg4MA%253D%253D%26devicetype%3DiMac%2BMacBookAir10%252C1%2BOSX%2BOSX%2B15.5%2Bbuild(24F74)%26version%3D13080a10%26nettype%3DWIFI%26lang%3Dzh_CN%26countrycode%3DCN%26fontScale%3D100%26exportkey%3Dn_ChQIAhIQMhoe%252BBPXgCBc6nwySTgX3RKGAgIE97dBBAEAAAAAAGgMKk7HoFYAAAAOpnltbLcz9gKNyK89dVj06DcmtrpDZoWdSCBGOPJA66XNCp0UFc4sLz7qtEx1hnlkVeDHNk5hV7vMNOzdOtOosagsHj5muxBVZo0sOecdPmNP3T7iq4eEBJ9X8vvAnUEDd%252BU8wlAOvWgruJkbS52o0iBCOyQ45RJfP3drPexeLSBfHBUSZHBVBCPfKhi6sGZTy3mF3BXImYm5%252B1TmA7S5HqP6Ok6uUJgKw1Hz195uSKSgWSfUqH9bE6kS8YXBTwekZedpRNiRexmlTSTerks4nboMfPDUUb%252ForaE%252FLMO9NUkzH83hgOjqBw2Q82p8WuY%253D%26acctmode%3D0%26pass_ticket%3DvgeInrhLtYDDMndp7X7xyCAaYKDLCCE2DQ0Rvt2WjIeLFFGTYjZOw1iLHrrMxp7c%26wx_header%3D0%26fasttmpl_type%3D0%26fasttmpl_fullversion%3D7794116-zh_CN-zip%26fasttmpl_flag%3D1&nolastread=1&uin=&key=&devicetype=iMac+MacBookAir10%2C1+OSX+OSX+15.5+build(24F74)&version=13080a10&lang=zh_CN&nettype=WIFI&ascene=78&fontScale=100)

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/002.png)

嘉宾：朱哲清（Bill Zhu） 

访谈：haina

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/003.png)

AI Agent 正在走向它的 “foundation model 时刻”。

如果说 ChatGPT 的崛起验证了语言理解模型的通用性，那么 Agent 的下一个关键跃迁，则是将语言能力转化为具备规划、执行和自我优化能力的通用智能体。这一跃迁的核心，不在于更大的模型，而在于是否具备多步决策、目标导向、持续学习和高效探索的能力。

Pokee 正在尝试给出一种答案：它不是在用 LLM 套壳实现 tool calling，而是从底层架构就以 RL 为核心，围绕 goal evaluation、self-training 和 memory retrieval 等能力做了系统性设计。其训练方式不再依赖大规模预训练，而是以“少样本高目标密度”的方式自我成长，显著降低了推理成本，提升了泛化能力。在已上线的 beta 产品中，用户高频调用上万次，体现了其 agentic workflow 的真实落地能力。

我们与 Pokee 创始人 Bill 进行了深入访谈，围绕“如何构建一个真正的 RL-native Agent”展开探讨：

**•**为什么 Pre-training 并不能带来真正的 reasoning，RL 是多步规划能力的唯一路径；

**•** Pokee 如何用 self-play + self-evaluation 构建通用 agent，降低 hallucination 并提升执行可控性；

**•** Memory 如何成为终身学习系统的基石，以及目前所有系统在 memory 构建上都存在的巨大空白；

**•**Exploration 如何帮助 Agent 在开放世界中理解目标、掌握工具使用、提升泛化能力；

**•** 为什么通用 Agent 的护城河不是“技术壁垒”，而是“被用户使用的轨迹”本身；

**•**为什么他们不押注 C 端变现，而在服务 Google 等企业客户的同时，以更低成本、更强策略能力构建未来的 Agent 基础设施

我们认为，Pokee 所代表的并非“agent 工具链”的一次增强，而是代表一种范式的转向：从 pre-trained LLM 套壳走向以目标为核心的 RL system，从静态的提示词走向具备长期记忆与主动规划的智能体，从面向 token 的预测引擎走向面向任务的决策机器。这场转向才刚开始，但未来已来。

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/004.png)

**01.**

**多步 Agent****训练范式正在改变**

**海外独角兽：****你觉得现在 AI agent 时代来了吗？**  
  
**Bill：**我认为已经来了。有几个很明显 AI agent 几乎已经 ready 的方向：

**•****首先是 coding agents。**现在的 coding 场景已不限于修改代码，Codeium、Cursor、GitHub Copilot 都可以启动 agent 模式，执行 multi-step reasoning 和 multi-step execution。**至少在 coding 领域，我认为它已经完全具备了一个真正 agent 应有的能力，能够产生 side effect、接收用户或真实世界反馈，并据此进行后续决策。从这一角度看，coding agent 已基本具备大规模应用的条件。**

**•****其他领域相对落后，尤其是 workflow automation。**目前除 Pokee 外，使用较多的仍是 Zapier 等传统工具。我们产品上线后，收到大量用户反馈，表示原本使用 Zapier 搭建自动化体验不好，几乎所有内容都需要手动搭建，改用 Pokee 节省大量的活。另一个常见反馈是关于拖拽式工作流。包括 Langchain、LangGraph 在内，也可以视作拖拽式，只不过是通过代码定义拖拽的流程，而不是通过 UI 来完成。从这个角度来看，在工作流方面，Pokee 要比那些工具要好用。

**•****Creative 工作流也在逐步展开，例如长视频制作、图像编辑等**。昨日美图发布了一个面向修图的 agent，我认为是一个初步尝试。Lovart 等产品在 design 方向也可看作起步阶段。但在打通完整流程方面仍存在障碍。例如生成内容如何进入 Figma，目前通常只能输出固定图像，难以进一步编辑迭代。又如视频制作完成后，理想状态是导入 AE 并保留图层以便调整，但现阶段生成的视频内容无法实现后续分层编辑。

**这也是我觉得 agentic experience 还没有真正到头的一个原因。像 Pokee，让用户觉得可用，正是因为事情做完之后还可以再调整。**比如你写文章、写 docs，或者生成内容后要发布到社交媒体，这些流程里都有可以调整的步骤。但在 design 领域，很多时候一步做完就结束了，没办法往回改。这可能就是目前 creative 或 design 类 agent 的一个瓶颈。

**但我觉得，到 2025 年底到 2026 年中，会成为一个 agent 特别爆发的时间段。**因为现在几乎所有公司都在努力把 multi-step reasoning 和 multi-step execution 做得更好，这是一个非常关键的时间点。

**海外独角兽：****回顾你过去的 research 和在 meta 的经历，是哪些核心洞察让你决定以 RL 为核心做 Pokee？**  
  
**Bill：**首先需要更正的一点是，RL vs。 transformer 或者 RL vs。 LLM 这个对比我觉得是不太精确的。因为目前大多数 LLM 本身已经在用 RL 来做 reasoning，所以这两者并不能简单地一分为二来看。

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/005.png)

RL 过程示意

**Agent：**训练的程序，目的是完成指定的工作

**Environment：**代理执行动作的世界

**Action：**代理采取的行动，导致环境发生变化

**Reward：**对某个行为的评价，类似于反馈

**State：**代理观察到的环境信息状态，用于决策

**Reinforcement Learning（RL）：**代理通过在交互式环境中不断试错，从自身行为和经验中获取反馈（奖励）进行学习。目标是在环境中找到一种最优策略，使得累计奖励最大化

**Policy：**将状态映射为动作的函数。可使用神经网络（参数为 θ）进行近似表示，在传统 RL 理论中也称为函数逼近

**那为什么我们 Pokee 会以 RL 作为整个核心算法的基石？我们认为在 agentic experience 里面 Pre-training 的能力或者 Pre-training 的重要性是非常低的。**它可能带来的唯一的作用就是理解，比如理解用户意图、一些常识、对工具的理解。但真正的 reasoning 过程，Pre-training 几乎帮不上忙。比如全工作流自动化，就不存在现成的现实数据集。要么手动标注，要么想办法从现实场景中提取数据来指导工作流的构建，但这样一来数据量会非常小，而且人工标注要耗费大量时间。

举个例子，不同工具对应的具体操作完全不同。如果要把 Google Docs 的所有功能拆解开，可能会有 100 多个可调用的 request 或 API。不可能让一个人对着文档，纯手动编排几百个 API 调用来完成某个任务 —— 这不是人类可以做的的事。在这种情况下，想通过 Pre-training 得到一个预热的模型基础上实现 reasoning 能力，几乎是不可能的。**必须要从头开始，靠 RL 的 self-play、self-evaluation 和 self-training 来实现能力的持续迭代。**  
  
从我过往在 Meta 的经历看，当时在推荐系统中大量落地 RL 和 RLHF 技术，甚至 Meta 广告系统里的整套 pacing 逻辑，就是我们团队做的，也有论文发表。这些应用场景中， RL 落地时会明显发现 offline training data 能带来的效果其实非常有限，必须经过多轮迭代。比如，先用 online data 训练出一个具备推理能力的 planning agent，再将其部署到生产系统中生成新的输出，基于这些输出继续训练，得到一个新的 agent，如此循环迭代，才能逐步实现理想的效果。**给我们的启发是，完全依赖 offline RL 是只能拿到非常小的增益。**

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/006.gif)

RL 与 Offline RL 示意图

RLHF 其实从某种意义上想像成一个 Offline RL 步骤，因为 reward model 的能力限制了 RL 算法完全 off-policy 的能力。当然，它所带来的 reasoning 能力已经是超过了超越传统监督学习的 Pre-training，但提升幅度仍然非常有限。**所以 experience / exploration 的 online 运行是无法避开的重要步骤。**

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/007.png)

On-Policy vs Off-policy

**基于此，我们认为要让真正的 RL agent 成功上线，可以用多步 tool use，必须做 online RL，同时要有能力去做 self-training ，作为一种能力上的迭代。**过去我们在 Meta 部署 RL 在多个生产系统中，带来的收益很多时候也只是 0。几百分点。对于整个生态来说可能就无足轻重。但我们希望能做出对整个世界、对全人类产生实质性影响的成果。  
  
**海外独角兽：****你觉得一个真正的 agent 需要具备哪些能力？比如 Pokee 跟 Manus、Genspark 这些比起来，会有哪些新的能力或者增强的能力？**

**Bill：**首先，不能只是做套壳。因为现在的模型能力强在能实现合理 function calling。只要选对 function，在单步执行中调用中就能得到正确的结果。但正常的工作流或者正常的多步 Agent 任务，它一定是多步的。

**在多步的情况下，如果完全依靠一个未经过特殊训练的 Agent 来完成长链条的 reasoning，它往往是走一步看一步，缺乏清晰的目标导向。**因为训练过程并未基于用户希望达成的目标进行条件建模。像“是否达成了目标”“如何通过多步的 function calling 来完成目标” 这类问题，从未出现在 LLM 的训练过程中。

**•**第一，要解决这个问题，就必须采用特定的训练方式：明确用户给定的目标，并在此基础上判断目标是否完成，给 LLM reward，再去确认这种目标。目标导向的规划是目前在 agentic experience 里面超越 function calling 的一个非常关键的点，但目前在训练中还未得到足够重视。

**•** 第二可能是 self improvement 的难点，因为 evaluation 的能力本身存在瓶颈：一旦模型取得的输出的调用序列超出了它训练时见过的范围，就没有能力做好 evaluate，也就没有办法自我优化。

**•**第三个重要问题是 memory，虽然我们还未深入研究，但这是我们重点推进的方向。能否理解用户的历史行为，对 Agent 是否能完成任务至关重要。比如，曾有位投资人用 Pokee 进行 LinkedIn 营销活动，他说“帮我写一篇 LinkedIn 帖子”。这里的“写”到底是起草还是发布？本质上是一个对齐问题。而目前唯一的解决方式，是通过历史上下文或记忆来判断：用户历史交互上面“写” 之后是直接发出去了，还是没发，哪种情况对用户来说才算完成了目标。**这需要的不是对单一任务的记忆，更需要跨多个工作流的记忆来支持 Agent 个性化理解用户习惯。**这是个难题，可能是一个很重要随机阅读完成，目前我们也还没找到最终解。

**海外独角兽：****我们也了解到最近无论是 Google Gemini 还是 OpenAI，核心重点都在做 memory 以及 long context。**

**Bill：**对，这个很重要，只是没有什么特别好的解决方案。

**02.**

**从 0 开始****RL 端到端训练是新路径**

**海外独角兽：****市面上主流架构（如 ReAct、AutoGPT、function calling agent）你怎么看？**

**Bill：**我认为 ReAct、AutoGPT 和 function calling agent 其实都属于 agentic experience 的一部分。比如 ReAct，是在缺乏 reasoning 或 planning 的情况下，通过某种形式的 chain thought 来完成特定的行动；而 function calling 则是在给定函数库的前提下，能够调用正确的 function。**但它们缺失的部分在于，整个过程并非目标导向的，而等于是一个依赖上下文摸索最优行动序列的过程。**

其一，我不希望把上下文学习等同于训练过程。也就是说，不希望仅依赖上下文学习，而是要在训练阶段就把推理和规划能力植入 agent。第二，未来最大的突破可能不会出现在纯 LLM 架构，不是以逐 token 生成的架构来完成 agentic experience。ToB 领域其实已经在走这个方向了。

**海外独角兽：****如何看待 RL 跟 Transformer 架构之间的关系，以及对未来的预期是什么？**

**Bill：**Transformer 与任何神经网络架构以及 RL 之间其实都不冲突。可以把 RL 和任何神经网络架构想成一个相对垂直的关系，神经网络架构性能越好，RL 的能力就会越强。**因为 RL 本质上可以看作一种基于目标的优化器，而神经网络架构的设计与优化方式本身并没有太大关联。**

从现代深度学习理论来看，现有的优化器确实可以应用于任何神经网络架构上。所以在我们看来，RL 和 Transformer 之间完全不存在冲突或不兼容的问题。未来，我们总体认为 Transformer 架构、自回归生成架构和 RL 之间，需要找到一种动态平衡的关系。比如，当前针对任何问题的架构设计中，决策步骤往往等同于 token 的生成，而 state 此前所有的上下文，也就是在当前 token 出现前的全部文本序列。

但 RL 有个众所周知的问题：当 action space 变得极大、历史信息过长，且问题本身趋于复杂时，它就解决不了。比如，如果 LLM 完全跳过 Pre-training 阶段，只靠一个 Reward function 从零开始训练模型，即使函数设计得再好，模型也几乎不可能达到当前 LLM 的能力水平。原因在于探索空间过大，模型在找到有效策略前就可能迷失或崩溃。**这是现在有 Pre-training 到 Post-training 到 Reinforcement fine tuning 多步训练的核心原因。通过巨长无比的 Pre-training 去预热策略模型，在一定程度上解决 exploration 问题，再用 RL 进行优化是有效的。**

但这套体系也存在核心问题：模型的 plasticity（可塑性）有限。训练时间一旦过长、模型结构达到饱和，就会出现 catastrophic forgetting（灾难性遗忘），也就是模型无法再学习新知识，甚至丢失旧知识。这就像一块海绵吸满了水，再强行注水只会把原来的水挤出去。这也意味着，模型的训练能力不可能无限提升。如果数据集持续增长，Pre-training 阶段纳入无限量的原始数据，模型规模也得不断扩大才能适配，以记住任何事情。**但人类知识的增长是指数级的，GPU 支撑能力的算力和模型扩展能力却是线性的。最终，这种线性与指数之间的不匹配会形成无法逾越的瓶颈。**

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/008.png)

catastrophic forgetting 示意

我觉得未来可能会出现一种趋势：既然从零开始训练的瓶颈在于动作空间与 horizon 过大，就反过来简化问题本身，重构产品目标以压缩两者。只需少量数据或规则即可构建 Benchmark 或环境，通过 RL 从零开始训练 agent，实现端到端学习来完成目标，而不再依赖数十亿级别的数据点。**从零开始用 RL 训练，是另一种路径。这时候只需有 goal evaluation，而 goal evaluation 的数据量可以是固定的，或者说环境本身的配置是固定的。**即便现实世界中出现了很多不同的场景，你也只需要告诉 RL 工程师：“这是你的目标，我不会给你任何数据，你从零开始想办法解决。” 这种情况下，训练所需的数据量不会指数级增长，因为模型不需要记住训练内容，只要能解决问题。

**所以在 agent 领域，我认为后期在 all in Transformer 这条路上，可能需要通过去掉 Pre-training 来找到一个平衡点。**这个平衡点目前还没人找到，而我们现在正尝试迈出第一步。

**海外独角兽：****你觉得找到这个的过程会很长吗？**

**Bill：**不会特别长。因为所有的所需要的技术其实雏形都有，是需要去找一个非常好的设计，使得这个 agentic system 不再跟 LLM 完全重合。

**海外独角兽：****大家现在都在探索这个领域，而像硅谷这样的环境，人才都是流动的，有一天一个公司探索出来，就会很快被部署应用。**

**Bill：****我觉得现在还有很多问题没解决，不一定是更复杂的，反而有不少 low-hanging fruit。**我通常会这样看待时间线：比如当下，在编码能力、coding agent 能力，以及图像生成、视频生成这些单一模态领域，还有那些仅需单步操作的能力上，提升空间其实很明显。未来 3 到 6 个月，甚至一年内，就能看到显著进步。

**至于 Pokee，虽然我们的第一版模型加产品已经推出，但要真正实现我们理想中的状态，可能需要一到两年的时间。**所以我们算不上是那种追求短期成果的研究方向竞争者，更偏向中期赛道的选手。而在这条赛道上，竞争者要少得多。因为现在所有人都挤在最前端的 “6 个月内必须出成果” 的层级里，卷得非常厉害；而我们所处的第二层级，大家可能没想得那么远，更多是 “先熬过这个月再说”，毕竟很多公司都在烧钱。你最近应该也看到新闻了，比如 Cursor 等有些公司已经烧不动了，开始调整所有人的定价方案，改成按具体 use case 收费了。

**海外独角兽：****Cursor 亏损其实非常严重。**  
  
**Bill：**不是一点点严重，这种问题就跟 Manus 一样。Manus 之后也会遇到同样的困境。虽说融了几千万美金，但它现在的 credit cost 已经很高了。1000 credit cost 也就够用户用两三次。即便在这种高消耗模式下，公司还是巨额亏损，因为每次运行成本要 2 到 3 美金，现在可能稍微降了点，大概 1.5 到 2 美金，但依然不低。而且这还只是单个任务的成本。

反观 Pokee，比如用户一次性抛出二三十个任务，我们并没有采用 credit system，但实际成本算下来也就零点几美金，实际花费最多 0.1 到 0.2 美金，属于很低的水平。但其他公司的实际成本，据我了解，一开始就有高的 total cost。所以从这个角度看，大多数硅谷公司眼下的首要任务是活下来：先在未来 6 个月的竞争中站稳营收脚跟，才有余力去思考更长期的研究，去把产品真正做好。

**海外独角兽：****那看来 Pokee 的 cost 真的很低，不太会担心出现 “烧钱烧不动” 的情况。**

**Bill：**我们也要烧一点钱在用户身上，比如现在给所有免费用户都提供 10 美金的额度供他们使用，大家用得都挺踊跃。从上周发布 Beta 版到现在，workflow 的数量已经有大几千个，运行过的 task 更是达到了几万甚至几十万个，算是一个被高频使用的工具了。

**海外独角兽：****那表现还挺好的，因为目前宣发也没有很用力。**  
  
**Bill：**我们现在想先找到一批真正的用户，而不是急于大力宣传。毕竟我们是从 Meta 出来的，很清楚产品怎样能打火，什么样打不火。一旦用力宣发，肯定能带来流量，但关键是得接得住这些流量。如果花了很多钱把流量做起来，产品却跟不上，最终必然会落得 negative reputation。而一旦有了差评，再想砸钱宣传扭转口碑，那就很难。

**03.**

**开放世界****Agent 需强探索能力**

**海外独角兽：****目前第一版本 pokee 是怎么设定 ai agent 的思维边界和行动空间呢？**

**Bill：****第一件事情是如何把开放式任务变成一个可以学习的任务，而核心点就在于 exploration。**首先，数据质量非常重要。比如我们现在有 evaluation model 来帮助我们评估 Agent 的表现，这个 evaluation model 本身的质量就非常关键。如果它不够好，那你有没有 exploration 其实都没意义，因为你的 reward 是错的，整个训练信号就是无用了。**所以泛化能力的核心点，第一是高质量的数据，也可以说是高质量的 reward，第二是 exploration。**

举个例子，在 classic RL 的设定中，如果我们训练一个 Agent 去完成一个简单的 target game，或在 multi-step 环境中达成一个既定目标，会发现 agent 只能学会一种“拿分技巧”。但你要它去做别的事情，它完全不会，只要 reward 稍微改一改，可能就完全做不了。**而 exploration 带来的最大好处是，它能主动去识别和解决不同 state 上的不确定性。当到达某个 state 后，对未来状态序列的信息越来越清楚，就能做出更好的推理。**

举个更直观的例子，来说明为什么 exploration 很重要：假设有一个简单的环境，只有四个点：A、B、C、D。Agent 从 A 出发，目标是到达 C 点，因为 C 是唯一一个可能带来正向 reward 的点，其他点都没有奖励。A 到 C 是单向可达，同时 A 也能到 B，B 可以到 D，D 可以再到 C。整个路径是 A → C 或 A → B → D → C，所有路径都是单向的。

**•** 在这种情况下，如果你用一个传统的 RL agent，它很可能在最开始尝试几步后就发现 A → C 能拿到 reward，就会直接收敛在这条路径上。因为 reward 是正的，step 数又最少，这是一条非常 “高性价比” 的路线。

**•** 问题是，Agent 在这种训练方式下，根本不会探索 A → B → D → C 这条路径。假设这个路径上的每一步都有轻微的负 reward，比如 step cost 是 -0.01，那它就更不会走。它甚至意识不到这个路径存在。

**•** 现在我们把设定稍微改一下：C 点的 reward 是 +1，而 D 点的 reward 是 +2，而且 D 不能从 C 到达，只能通过 B 到 D，再到达。那最优路径其实是 A → B → D → C。但由于 Agent 早早就学会了走 A → C，它就会完全忽略掉 B 和 D，从而无法获得更高的总 reward。

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/009.png)

A → B → D→ C 奖励机制

**这就是 exploration 的重要性。它不仅帮助我们理解 reward 的不确定性，更是解决整个 trajectory（路径序列）和世界结构中各种不确定性的关键。**通过 exploration，Agent 可以以某种方式量化并逐步解析这些不确定性，从而在面对未来的新任务或问题时，能够产生更好、更快速的解决方案啊。**以上问题可能相对比较容易，e-greedy 就可能能解决，但是如果这条 A → C → D → E → F 的路径更深，那 e-greedy 就不太可能完成了。因此，一个能在开放世界中学习的 Agent，必须具备强大的 exploration 能力。**

Exploration 也是我和我的导师，在我读博期间以及后续在 Meta 做实验时长期关注的方向之一。实际中大型模型的落地、主流研究趋势，exploration 一直是一个相对不受重视的方向。但最近几个月，越来越多的人开始重视它。大家逐渐意识到，如果没有 exploration，没有办法对这个世界有更好的认知，泛化性也会变差。这个例子是非常短期，但是也说明了，如果你只有单一 reward， 用 reward 来优化，可能就会损失很多的对世界的了解信息。

**海外独角兽：****多步决策能力是 RL agent 适配真实世界的关键。你们是如何设计、评估、debug agent 的 planning 能力的？是否有专门的 multi-step benchmark？你怎么看现有 planning benchmark 的局限？**

**Bill：**Benchmark 这件事，我们内部其实有自己的一套体系：首先是单步动作决策和 function calling 的准确度；其次，针对多步的 planning 能力，我们有专门的 evaluation model ；再者，还有真实世界的 benchmark —— 也就是执行后输出的结果与预期目标的吻合度。内部是有非常严格的训练流程，会持续监控每次模型训练或新 engine system 搭建后，这三个指标是否出现下降。

**04.**

**终身学习****是比个性化更大的命题**

**海外独角兽：****关于通用型 Agent 的理解，memory 与 tool use 是两个核心能力点。你认为 memory 为什么重要？在哪些方向上可能更值得深入研究**？

**Bill：****第一个关于 memory 的问题里，是一个 personalization 的问题。**通过用户与 Agent 之间过往的交互，Agent 可以逐步理解用户的行为习惯、偏好目标，进而推断出用户真正想要的结果。用户可能不再需要逐字逐句地表达需求，比如他说“这几个文件你帮我弄一下”，Agent 应该能够结合历史对话或任务记录，理解“弄一下”具体意味着什么，从而做出恰当处理。

**第二个问题首先我们提到的 “Lightning goal space”，背后是非常复杂的问题。**因为 goal representation 本身无法仅靠语言来定义。一个目标是否真正达成，取决于具体的输出结果，得到这个具体的输出结果才能判断是否与想要的东西一致。目标本身也需要做 reasoning，拿到的是一个抽象、模糊的目标表达，而不是一个确定的目标状态。

这时，系统就需要基于这个模糊的目标表达，以及与用户过往的所有交互记录，去推理出什么样的执行结果才算是与该目标匹配，达到一个 policy reward。这就比正常的 RL 中的流程麻烦得多。**无论是在代码执行还是在游戏环境中，state 执行完后得到的结果就是对应的 policy reward。而真实工作流环境中，并不存在清晰定义的 end state。**

**另一个是 memory 的检索问题。比较麻烦的点在于整个 memory 上下文不是线性的。**比如，过往创建了 50 个文件，但这 50 个文件并不是一个线性叠加的过程。可能是 A 和 B 文件合并生成了 C，随后 C 和 B 又产生了 D。这些文件不会是一个线性叠加，而是 graph 格式。那么怎么去找到和要完成的目标所相关的 minimal cluster？需要从某一个节点出发，找出所有相关文件，以非线性方式组合成有效上下文，再交给模型进行推理，最终得到合理输出。这个过程是目前没有任何一个系统已经解决，所有的系统都采用简单的 indexer + concatenate 的方式再去做推理。 graph structure 以及找 minimal cluster 的过程目前均不存在，这个是一个非常值得研究的一个方向。

**海外独角兽：****你提到 agent 会根据一个用户的上下文去理解他到底要想干什么， 那 agent 是不是能够根据 memory，自主地去学习在这个情景下用什么样的工具，以及怎么去识别用户的意图？**

**Bill：**这其实也呼应了之前的问题，Agent 对工具的使用偏好，应该是能够通过过往的上下文自动学习的。它不仅要理解用户在当前场景下的意图，还要记住用户“习惯用什么、不喜欢用什么”。举个例子：如果某家公司默认只使用 Microsoft Office 而不是 Google Slides，而用户只是简单地说了一句 “Can you create a slides deck for me”，一开始 Agent 可能会尝试用 Google Slides，但被告知“我不能用 Google Slides”。此时 Agent 应该切换到 Microsoft Office，并在任务完成后，记住未来对这个人或这家公司，创建 slides 时应默认使用 Microsoft Office。

**海外独角兽：****是的，这其实非常重要，如果一个 Agent 能减少用户表达的负担，持续理解并适应用户偏好，就会让用户很难 switch。感觉这就是我们所说的“终身学习型工具智能体”，能不断积累与更新理解，最终成为真正意义上的个人助理。**

**Bill：****对，我觉得是这样。终身学习系统和 continuous learning 很有关系，要解决的问题远比 personalized 更大。原因在于用户行为可能是非常 nonstationary 的**。举个例子，一个用户原来在一家公司只用 Microsoft Office，后来跳槽去了只能使用 Google Slides 的公司。他会告诉 Agent：“我现在只能用 Google Slides”，而这与之前得到的信息是“只能用 Microsoft office 不能用 Google slides”相冲突。在训练数据里面前后的偏好是同一回事，没有一个先后顺序说后面的更重要，前面的不重要。

**这是终身学习系统一个非常大的问题，系统都是“只进不出”的，即新信息可以不断添加，但几乎没有机制可以主动“遗忘”旧信息。**它像一个吸水的海绵，却无法挤出旧水。我们只能不停在把模型变得更大、再大。但是信息的爆炸速度是超过模型可以接收的速度。不是说 news 或者 knowledge 的信息，而是从 personal level 的这种 knowledge 信息。这远远超过了模型容量的扩展速度。把每一个人身上的所有的 personalize 的信息的叠加，六七十亿人口，然后每人每天产生的信息全部都叠加在一个模型里面，但是肯定吃不下，所以这件事情就变得很难办。

**海外独角兽：****明白，那感觉这个路线如果想要去个性化地理解每个人肯定是更 make sense 的。**

**Bill：**对，那可能有几个方向。首先，可能是每个人拥有一个自己的小模型，也不分享给任何人。但这就打破了 OpenAI 想走的方向，如果说这是最终方向的话，那 OpenAI 等于现在自己把自己走进一个死胡同里面。因为它的模型越做越大，但从某种意义上来说，我们要思考说小模型怎么能拥有世界信息？类型就有那么多，我觉得目前没有特别好的可逆解决方案。**着重要说的一件事，是模型是如何在吸收新信息时与已有知识进行调和，并怎样遗忘旧信息，以解决这个 continue learning 问题，这是一个长期来说最先要解决的问题，然后再去先思考如何设计小模型。**

**05.**

**通用 Agent 的护城河是用户使用**

**海外独角兽：****关于商业化路径的调整，你们早期尝试过电商场景的 AI agent，后来又转向了通用框架。这个转向的过程经历了什么？为什么做出这样的选择？**

**Bill：**我们从一开始的目标就是做通用的 agent 架构。电商是一个 proof concept 的环境。 因为 Shopify 平台的 API 比较成熟，接入无需审批，很简单就能直接把我们的技术直接扔进去，把所有的 API 接进来，从而看架构能不能自主执行。电商场景验证可行以后，我们立刻就开始做通用 case。

**海外独角兽：****现在做真正的通用场景，未来即使大厂进入市场，我们的护城河是什么？是能够和用户的数据及个人工作流紧密绑定，还是能力集成更多工具，集成更深更广？**  
**Bill：**我觉得都有。首先一个简单的论点是，如果你是 Microsoft，想做通用工作流，为什么 Google Slides 会让你接入呢？双方都拿不到对方的整体访问权限。比如 Meta 想做社交网络的工作流自动化，怎么拿到 YouTube 的访问权限？YouTube 不会给。

**大厂之间有很大 barrier。**

我相信 Google 和 Microsoft 作为偏企业方向的团队会想做工作流，但做不了，因为除了他们自己内部工具，外部工具都不会对他们开放，要么是竞争关系。**我们处于一个类似 Switzerland 的状态，不绑定任何一方，只专注工作流，也不会占用对方流量，只用开放的 API。API 的开放也本身是希望获得更多程序访问权限。**比如 YouTube 希望更多视频在平台上，Facebook 希望更多内容在 Facebook 页，Instagram 希望创作者更多创作，他们乐见其成，我们不与他们冲突。但 Meta 不希望被 YouTube 流量绑架，所以不会开放给 YouTube，但会开放给我们，这形成了一种独特的商业化状态。

**第二是用户行为的集成。**用户工作流通常在企业内部，企业对本地部署和合规要求高。我们合作的投资方和合作方多为企业用户，我们做的是小模型，可以做到本地部署，满足所有安全合规要求，因此更容易推动合作和合规。最后，当这些都做得很好，用户数据和历史会带来最大的价值和用户习惯。

无论是企业侧的 API 访问，还是消费者侧的行为，这都会形成用户粘性，自然而然形成护城河。

**海外独角兽：****所以还是得推出产品，让用户尽可能多使用，用户自然形成护城河。你之前的访谈中提到想给其他 agent 提供 planning 和 decision 层能力，我当时觉得这个模式像 decision as a service。现在怎么看，是继续做这个，还是直接做面向 ToC 端的产品？**  
  
**Bill：**我们还是会给其他 agent 提供服务。比如和谷歌的合作，我们给他们面向用户的产品提供背后的 agent 服务，不是 decision service，而是端到端的 tool calling，包含 planning、tool calling 和 outcome，整套流程完成，作为 API 服务提供。不是告诉你做什么 decision，而是从头到尾完成并交付结果。  
  
**海外独角兽：****这块业务和现在做的面向 C 端产品，哪个未来是主要产品？哪个收入更高？**  
**Bill：**还不好说，但我们的架构支持两者同时进行。就像云服务，后端 API 服务带来大部分收入，但其实两个产品是一个产品，区别只是前端 UI。

**海外独角兽：****我们了解到 Claude 和 OpenAI 的 API 服务是很赚钱的业务。一开始不看好 API 业务模型，但后来发现它利润高，底下的 C 端产品还在烧钱，而 API 是赚钱的。**  
  
**Bill：****对，我认为企业服务是 AI agent 甚至 AI 本身最终唯一赚钱路径。**单靠消费者粘性赚钱不现实，必须靠别的，就像 Google 搜索一样，都是亏钱，最后靠第三方推广或广告带来收入，或者根本没有变现。  
  
**海外独角兽：****有一个有趣的点，我在访谈中看到 pokee 性能在成本和速度上达到市面产品的十倍以上。为什么 Google、Meta 这种大厂做不到？**  
  
**Bill：**方向不一样。如果你专注做 LLM，就会被卡住。我们能做到的，他们也能做到；他们能做到的，我们未必能。比如写代码、写更好的文章，他们可能是我们的十倍、二十倍。这与切入点有关，不是我们能力更强，而是切入点完全不同。

**06.**

**Agent 的未来、落地场景与创业机会**

**海外独角兽：****之前提到 agent 很可能成为浏览器的替代，未来大家不再和浏览器交互，只和 agent 交互。这是否意味着互联网的基础交互结构会改变，无论是 UI 还是电脑的形态？**  
  
**Bill：**我同意。这是我们创建 pokee 的第一个基本原则。现在很多浏览器无法避免，因为信息储存基于以浏览器为核心的 HTML 架构。**但长期来看，当 agentic experience 成为交互核心，前端可能会被废弃，变成一个任何 agent 都能访问的标准化数据库。如果形成这样的标准化数据库，就不需要传统前端，所有呈现都是动态渲染。**

未来交互结构会是用户配对自己的个人 agent，或在公司配备中央 agent，用户向 agent 提问并得到结果，agent 以个性化方式呈现结果，背后 agent 与其他公司数据库或 agent 交互，这个过程不暴露给用户，其无需知道数据转发。

**海外独角兽：****感觉与 AI 的交互会越来越简化，更加直观，才能让大部分用户使用 agent。**  
  
**Bill：**唯一的顾虑是，很多 human in the loop 在这种方式下难以实现。比如 agent 只沿着三四个方向寻找，用户觉得不满意，但 agent 受限于训练或设计，只锁定这几个方向。用户若想深入探索一两个其他方向，agent 却不会去找。用户对世界的认知被 agent 限制，无法看到更多信息。**这与现有搜索引擎类似，只是搜索引擎表面上用户似乎掌控了，但在 agent 领域用户实际上失去控制权。这是个需要思考的问题。**  
  
**海外独角兽：****如果能根据个人的好奇心和探索能力，决定是否向其展示更多过程会更好。有些人喜欢强控制感，可以看到整个过程；有些人喜欢简单操作，不想看到细节。能做到这点会很不错。**  
  
**Bill：**对，但这个很麻烦，这个整个 user experience 是个 UI 问题，不是 engineer 问题。  
  
**海外独角兽：****最近大家常讨论 agent OS ，我们认为它包含核心组件如 RL 、LLM，还有 memory 和 tool use。你觉得还缺哪些部分？**

**Bill：**基本上就是这些，没有更多了。非要补充的话，就是 resource allocation 系统。比如在本地端，作为一个操作系统，尤其是在手机端，底层的内存管理很重要，包括 RAM 和存储的部署。如果任务调度过度，可能会很快耗尽内存。如何实现可扩展性，不只是能执行任务，还要能在本地设备上有效扩展，这是需要考虑的问题。  
  
**海外独角兽：****你觉得未来两三年最看好的 agent 落地场景是什么？现在有不少热门公司，无论是大量的 sale agent、customer support agent，还有目前营收最高的 coding agent。还有一开始提到的电商，用好了也挺不错。你觉得还有哪些场景？**  
  
**Bill：**我觉得主要是 sales、RPA、coding engineer ，可能也包括 marketing。我们做的东西也可以看作是 RPA 相关，RPA 范围很大，几乎所有东西都能归为 RPA。还有可能是 crearive 类的应用。

电商我起初觉得有希望，但现在不太确定。新的范式对传统模式的提效很低。之前很多电商用户找过我，聊完后觉得这个方向有问题。agent 能带来什么？卖得更多吗？不会。推荐系统已经做得很成熟了。客服方面，虽然可以做得更好，但用户很讨厌机器人，AI 客服已被整体生态破坏了信任，导致从售前到售后大家都不愿用 AI。  
  
**海外独角兽：****那你觉得个人类服务，比如订票、订酒店、规划旅游行程怎么样？**  
  
**Bill：**agent 可以，但这些产业利润本来就小。用户对旅行流程掌控要求高。用户不会直接说“帮我订机票”就完成，大多数情况下他们会先说要订，然后自己还会去看有没有更便宜、更性价比高或者时间更合适的。他们不会完全交给 agent 处理，订完还是会自己再去看一眼。  
  
**海外独角兽：****有道理，还是做那些用户不太关心结果，只要“有结果”的场景更合适。**  
**Bill：**对，我举个例子。为什么很多人在做 slides 或文档？因为大家真的很在意 slides 的质量，能判断好坏，但是并不在乎这个 slides 能做到多极致。现在我用 pokee 做到这个程度，非特别重要的演讲，我都会让它帮忙做大量准备。比如我做一个开场的 10 分钟演讲，前 30 分钟我让 pokee 生成 12 页 slides，帮我写提纲，然后即兴讲完，节省了大量时间。以前可能要提前一天准备信息、检索、搜索、总结，现在只需 30 分钟。  
  
**海外独角兽：****明白，倒数第二个问题，你现在最期待的技术突破是什么？刚才提到 memory 很重要，终身学习系统也重要，你对哪个方向最感兴趣？**  
  
**Bill：**我觉得还是 RL 的泛化能力。目前已经有很大进展，但基于 LLM 的 action decision making 和 token decision making 架构。如果跳出这个架构，能否做到同样优秀，这是我们正在研究的一个重要问题。  
  
**海外独角兽：****最后一个问题，除了 pokee，你觉得还有哪些值得创业的 AI 方向？**  
Bill：值得创业的方向很多。比如创意类，当前视频生成如何做长视频，agentic 的长视频。基础设施方面，目前多聚焦于 inference 和模型运算，是否能有类似 memory 方向的 AI 推理？比如把用户所有过往文件信息都扔给某个信息引擎，它帮你做序列化和索引，查询时像调用 API 一样。另外， payment 也是个好方向。在 agent workflow 中出现支付时如何做安全支付，是个重要课题。还有编码方面，后端如何自动对接不同数据库和服务，比如当前只能对接 Supabase，但后端需求更多，如何自动化接入并部署到云或高级平台，也是大问题。这些方向都有很大发展潜力，任意一个都可以做成独角兽。

排版：夏悦涵

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/010.png)

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/011.png)

延伸阅读

[![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/012.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247515372&idx=1&sn=bd32817adb35b8d0e050b831c755a23e&scene=21#wechat_redirect)

Figma：年度最火 IPO，设计与代码生成一体化的最佳选手

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/013.png)

[![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/014.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247515322&idx=1&sn=6900771e945ad2e971613abe80e818d1&scene=21#wechat_redirect)

bootstrap 到十亿美元 ARR：Surge AI 这匹黑马如何颠覆 Scale 霸权 ？

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/015.png)

[![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/016.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247515255&idx=1&sn=8c5e8c28e73a75082816a092ba242474&scene=21#wechat_redirect)

Elad Gil 复盘 AI 投资：GPT Ladder，AI Agent，AI 领域将迎来大规模整合并购

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/017.png)

[![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/018.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247515170&idx=1&sn=af951e288f33d2475a4fcebbdd1a4619&scene=21#wechat_redirect)

AlphaEvolve：陶哲轩背书的知识发现 Agent，AI 正进入自我进化范式

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/019.png)

[![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/020.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247515068&idx=1&sn=b8577dfde5fab5080ec6ef365c3da76f&scene=21#wechat_redirect)

估值 16 亿美元的 AI 护士：Hippocratic AI 是全球护士短缺的解药吗？

![](../images/2025-08-01-dui-tan-pokee-ceo-zhu-zhe-qing-rl-native-de-agent-xi-tong/021.png)
