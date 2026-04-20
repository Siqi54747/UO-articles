---
title: 深度讨论 Online Learning ：99 条思考读懂 LLM 下一个核心范式｜Best Ideas
publish_date: '2025-09-30'
publish_timestamp: 1759233780
mp_name: 海外独角兽
url: https://mp.weixin.qq.com/s/K4eROyUU97QZY4uTacMtRw
msgid: 1000000433
appmsgid: 2247518581
itemidx: 1
digest: pre-training 和 RL scaling 后的下一个新范式
cover: https://mmbiz.qpic.cn/sz_mmbiz_jpg/3tHNibnJ2jgzat6o2FEN5hjlVTCiaoliaudCun150BbqPicm52UtKvj31UicZhJZibQEHCKnRs3Z1TruRwCyo2rCU3Jg/0?wx_fmt=jpeg
image_count: 14
archived_at: '2026-04-20T04:32:16+08:00'
---

[![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/001.png)](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=Mzg2OTY0MDk0NQ==&action=getalbum&album_id=4157672299245862924&token=1418147436&lang=zh_CN#wechat_redirect)

**讨论主题：**Online Learning

**参与嘉宾：**拾象 Best Ideas 社群

![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/002.png)

在 OpenAI o1 将 LLM 带入 [RL 范式](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247509694&idx=1&sn=f0723aa72f1d9e4ffff5f828f8a49389&scene=21#wechat_redirect)一年后，我们再次迎来 AI labs 的密集发布周期：OpenAl 在推出 [Pulse](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518470&idx=1&sn=21efdd5f223ca848235c6d9ce65472b9&scene=21#wechat_redirect) 后紧接着在今天凌晨推出 ChatGPT 即时支付功能和协议，Anthropic 也同步推出最强编程模型 Claude Sonnet 4.5，能连续专注任务执行超过 30 小时。

这些迭代背后的共同特性是：推动模型在复杂、长程任务上的表现不断精进，甚至直接、实时地参与人类社会经济活动。要彻底实现这一目标、真正走入 AGI，更高效的模型进步路径、新的技术范式一定是当下的关键问题，online learning 极有可能是这个问题的答案。

两周前，海外独角兽组织了一场 「Best ideas」闭门讨论，和一线 AI researchers 围绕 online learning 展开思考。虽然今天 AI 社区对于 online learning 是什么、以及怎么做还存在非共识，但 online learning 代表了一种新的交互和推理范式，在实现极致个性化的同时能够动态迭代整个 AI 系统智能，是值得投入、探索的方向。

本篇文章是我们对讨论会精华的总结与开源，也期待激发大家对于 online learning、下一个 LLM 技术范式的讨论。欢迎在评论区留下观点与思考！

**01.**

**Online learning 是通往 L4+ 智能的关键路径**

**如果模型只在现有人类知识内循环，就无法迈向 ASI**

**1.**Online learning 长期的预期是让模型在很长程的任务上出现新的 scaling law。模型表现出现极大程度的提升，是 AGI 的关键因素。

**2.** Online learning 和模型自主探索（exploration）的能力十分相关。从 AGI 到 ASI 的本质是模型要突破人类知识上限，而 exploration 过程中模型如果要获得超越人类知识的小突破，就意味着需要具备自我探索（self-exploration）和自我奖励（self-rewarding）的能力。

**3.**如果模型只在现有人类知识内循环，就无法迈向 ASI。真正突破点在于 explore 和 exploit 的平衡，以及模型能否实现自主生成新知识。

**4.**Online Learning 是通往对于更高层次的智能（如 L4 级别智能或 AGI）的关键途径。例如，在撰写研究论文的过程中，研究者需要不断学习和调整；在证明一个复杂定理时，需要将问题拆解为多个引理，并通过探索逐步推进。这些过程都充分体现了系统级 Online Learning 的必要性。

**5.** 在此基础上，更强形式的 Online Learning 可能是这样一种模式：人们可以给模型一天时间，不指定任何任务，让它自主生成任务、规划学习路径，并在结束时接受测试。

**Cursor 的实践到底是不是 online learning？**

**6.** Cursor 最近自己在博客中分享的代码补全模型训练过程可能就是 online learning 的一个现实实践：根据 Cursor 的技术 blog，团队每隔两个小时就会对模型进行一次迭代更新，迭代过程直接使用了真实用户的反馈（在 cursor 中这里具体指用户对补全结果的选择）作为环境，而不是像传统那样专门训练一个 reward model 代替（模拟）人类真实反馈。

![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/003.png)

**7.**Cursor 实践的启发在于：人和 AI、模型交互中的数据能不能用来提升智能？什么数据是有用的？

**•**短程交互（如代码补全）：反馈直接、清晰、海量，适合替代 reward model。

**•**长程任务（如应用开发、PPT 生成）：反馈稀疏、周期长、噪声大，难以高质量积累，不适合作为 Online Learning 信号。

**8.**虽然 Cursor 的例子很有启发，但它可能不是真正的 online learning。

**9.**Cursor 收集了 ～2h 的数据，在训练实践中理论上这些数据不会作为一个 batch，而是会拆分从好几个步骤去实现，这个过程更像是 off-policy。

当数据由当前模型采样产生，并能立即与环境交互并更新，则属于 on-policy；如果数据来自历史记录，或者反馈经过延迟、整理后才进入训练环节，更接近于传统的 off-policy。

**10.** 所以 Cursor 的做法可能不是真正的 online learning，而是更接近 Lifelong Learning 或“自动数据收集+定期训练”。在这种模式下，任务目标（e.g 代码补齐 或 next token prediction）的分布是稳定的，并不涉及长期演化

**11.** 真正的 Online Learning 系统应能够随着数据的不断收集持续提升性能，而不是在短期内很快收敛。

**02.**

**概念定义与非共识**

**两个关键概念：Online Learning & Meta Learning**

**12.**今天关于 online learning 是什么还没有具体的概念，但可以确定的是在当下讨论中 online learning 并非一个单一概念，需要拆开两类分别讨论：

**•**Lifelong Learning：特点是目标与手段都相对明确：需要通过 online RL 来做，其中的关键是怎么做 reward 和数据收集。比如 Cursor 通过用户反馈优化补齐模型，做法明确，数据也很丰富。

**•** Meta Online Learning：与 Lifelong Learning 相比，目标明确但手段不清晰，需要新的算法与架构进行探索。它的核心目标是优化 test-time scaling 曲线的斜率，让模型在短期内快速适应新任务（fast adaptation）。

**13.**Online Learning 目前来看有两条技术路径，这两条路径并不完全重合：

1）直接路径：直接通过 RL 和环境交互来实现 Lifelong Learning；

2）先做好 Meta Learning，然后能更好实现 Lifelong Learning。

从实现路径上，做好 meta learning 之后再做 lifelong learning 会更轻松。

**14.**第二条路径表明，Meta Learning 很可能是 Lifelong Learning 的前置条件，可以嵌入到 Lifelong Learning 之中。Meta Learning 为 Lifelong Learning 提供了更高上限。具体来说，Meta Learning 能让模型快速适应新任务并积累知识，在这一过程中，模型还可以利用自身的适应能力不断收集更有价值的数据，这些数据再被迭代更新，从而推动 Lifelong Learning 的实现，通过这种结合，模型可以逐步实现 ASI。

**15.** 也有观点认为，Online Learning 更像是从 Meta Learning 发展起来的概念。Meta Learning 强调  fast adaptation 的能力，看重在真实的在线场景下进行持续学习与适应。LLM 时代 Meta Learning 更进一步演变成了 in-context learning  或者说 in-context RL，今天我们说的 context engineering 也是 in-context learning 的一部分，本质上是通过调整 context 来优化模型表现。

**16.**Online learning 可以看作是面向一个 agent system、在 online 情况下实现快速学习、不断适应新的环境，这个学习过程既包括了模型部分，也有非模型部分（e.g memory 就是非模型部分）。

**17.**可能到未来 meta learning 是一条很好的路，但它能够让模型在新任务中更快地适应与改进。但今天很多系统依然主要集中在实时数据驱动的渐进改进，而非全面实现自适应的高阶学习能力。

**Online Learning 不是 Online RL**

**18.**很多讨论中会出现把 online RL 和 Online Learning 两个概念被混用的情况，类似于“Agent”时代在商业化过程中被过度含糊化，这种模糊性可能反而会妨碍领域的发展。Online learning 的定义今天比较多关注 online 的部分：

1）在 test-time 要求模型（AI 系统）有 learning 或 training 的能力；

2）实现方法并不一定通过 training 来做。

所以这里会有两个问题需要思考、解决：

1）online learning 和 in-context learning 之间的关系是什么样的？

2）learning 和 training 是不是同时必须？

**19.**Online Learning 更多强调模型随着时间一直不断、不停止地跟随系统自身的运行在学习，在 LLM 和 Agent 系统中，凡是能让系统在交互中改变未来行为的机制（如 memory 更新、test-time adaptation），都可以被广义地称为 Online Learning。

**20.**Online RL 的范畴很大，比如 GRPO、传统 RL 等都是 online 的，只不过训完之后不会实时 update 模型。

**21.**Online RL 的关注点在于模型更新，即可以在 online 的情况下提升模型水平，但模型能力提升本身是否 online 并不重要，因为利用收集的历史数据同样可以提升模型能力。

**22.**Online learning 最终的目标是让模型本身有很强的 in-context learning 能力，即 learning 的更新过程由模型自己完成，这件事短期可以通过 online RL 系统在短期内来提升，但上限达不到 ASI。

**23.** Online RL 的上限在于它达不到 in-context learning 的能力，因为系统的更新是 RL 系统更新带来的，但 RL 更新的频率不可能太高。这件事本质上是因为今天 Model 的数据利用效率问题，虽然数据吞吐量已经很大，但效率和效果还没提升，只要数据分布发生变化带来的模型表现差异就会很大。

**24.**Online RL 系统要依赖某种形式从环境中提取 reward 信号，很大程度上依赖于人工设计。

**Online learning 代表了一种新的交互和推理形式**

**25.**Online Learning 是面向整个 agent 系统，因此 online learning 的最终目标并不仅限于优化模型参数，而是动态优化整个 agent 系统。这包括模型与非模型组件（如 memory）的协同更新，使系统能够快速适应新环境，并且通过不断的交互持续提升表现。

**26.**Online learning 代表了一种新的交互和推理形式：

**•**Chat 时代通过 reward model 提升和人类用户的对话体验；

**•**Long reasoning 时代可以基于 RL 让模型（AI 系统）思考更加深入，做专家级任务；

**•**Agent 时代我们需要 agent 在生产或训练环境通过自主探索（exploration）的能力来自主收集 reward 信号、完成某些任务，这种新的交互形式可能就是 online learning 的体现。

**27.**如果未来模型能够在没有预设任务的环境（task-free setting）下学得比现有基于任务驱动的 RL 效果更好，才算是实现了真正强大的 Online Learning。在这种情况下，环境依然存在，但任务或查询（task/query）不再由人类设定，而是由模型自己探索。这种能力的实现可能需要借助 Meta Learning 的路径。

**28.**但因为 online learning 的目标到今天还没有达成共识，现实中更为可行的目标是让系统能够依靠实时收集到的数据不断变好，而不一定要求其立即具备完整的 meta learning 能力。

**29.**还可以从 online learning 的两个实现阶段来理解它和 meta learning 的关系，这两个阶段其实也是 online learning 的两个不同目标：

**•**通过一个系统赋予模型学习能力，但模型本身并没有学习能力：典型例子是 AlphaGo，整个 rule-based 系统具备 test-time scaling，但模型没有，本身并不具备独立学习的能力，online RL 并不解决 in-context learning 能力

**•**让模型有内生的 learning 能力：这个目标更高阶。例如 Reasoning model 时代是模型具有 learning 能力而系统就不需要有了。

**30.** Meta learning 的思路是把模型的 in-context learning 能力提高，并把 in-context learning 作为一个工具去系统性地处理系统的 learning 问题。Online RL 并不预期能提高 in-context learning 的能力

**31.**Online Learning 与其说是当前模型必须达成的目标，不如说是未来模型必备的能力。

**32.**Coding 等高反馈、任务明确的领域，可能率先展现 online learning 的雏形。因为 coding 的反馈更加明确、信息密度也更高、数据获取成本低、环境高度可控，而且 Coding 也是梯度最大、效果最直接的场景；而在推荐系统中，噪声较多，且单一样本所包含的信息量有限。

**33.**数据分布差异越大，Online Learning 价值越突出：

**•**如果想要提升的模型能力是一个通用能力（e.g Coding，数学），即模型收集的数据分布没有随着时间发生很大的变化，交互的环境相对比较稳定，这种稳定环境下的优化通过渐进式学习就可以实现；

**•** 如果是需要模型实现对动态环境适应、更 personalized 学习，例如探索每个个体的偏好（涉及人类偏好、实时新闻或个性化需求的任务中），这种时候模型面对的数据分布差异很大，因为模型要和每个个体交互，而每个个体给出的反馈数据差异极大，这种场景/需求下 online learning 更能够效益最大化。

**03.**

**怎么才能做好 Online Learning？**

**5 类 AI 系统对比**

**34.**Online Learning 实践中遇到的第一个问题是反馈信号过于稀疏与单一，可以通过对比其他领域，把 AI 系统反馈信号过于单一这个问题看得更清楚。在 LLM 与 Agent 的场景中，因为目标本身比较模糊，而现有的数据反馈又过于简单。这类信号很难支撑模型能力的实质性提升。

![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/004.png)

**35.**Coding 可能是相对容易的一个环境：完全虚拟、reward 数据相对好拿。

**36.**但今天像 Claude Code 这些工具还存在对用户个性化习惯的理解不足、记忆机制缺乏，导致用户必须反复提示，如果能够解决记忆问题，性能的提升将会立竿见影。

**37.**个性化是低点的目标，最终的目标仍旧是模型能力。今天做 online learning 如果不应该只考虑“点赞、点踩”这些偏好数据，心态上可以把用户看成“环境”，agent（系统）和用户交互就是在学习信号，就和 coding 中建议是否获得采纳类似，所以模型个性化和模型能力变强是同一个问题。

**38.** Chatbot 时代，用户的点赞和输入本身提供了丰富的 in-context 奖励，但这些信号并没有显著提升模型的整体能力。而到了 Long reasoning 时代，RL 使得模型的深度推理能力得到了激发，从而出现了阶段性的能力跃迁。这表明，问题的本质不在于交互形式是否丰富，而在于能否找到适配模型能力的新训练或推理范式。

**39.** 反馈信号过于单一引发了一系列待解决的问题：是否需要收集更复杂、更多样化的反馈数据，才能让 Online Learning 真正发挥作用？用户交互数据的形态和质量究竟如何设计，才能真正用于提升模型智能？这种基于真实交互信号的迭代方式，未来是否可能成为主流路径？

**40.** 现阶段数据质量和环境是绑定在一起的：首先有一个环境，有了环境之后就需要构建任务、reward，任务质量的高低就是数据质量的一部分，同时又需要环境做得足够好来确保不会被 hacking。

**核心瓶颈 ：Reward 信号的获取**

**41.**今天要做好 online learning 有两大核心瓶颈：

**•**Online Learning 对 Reward 高度依赖，但 online 环境中怎么获取 reward？

**•**模型 in-context learning 能力不足。

**42.**在一些简单场景中，Reward 相对明确且高密度，因此更适合用 online learning：

**•**简单场景越容易实现 online learning：在 Cursor 的代码补全中，用户对补全结果的接受或拒绝能直接转化为清晰、快速的反馈信号，在客服场景中，用户的满意或不满意也能直接反映系统表现；

**•** chatbot 中用户给反馈的在推荐系统中，点击或不点击同样能够作为有效的反馈；

**43.**在更复杂的场景中，Reward 信号的获取变得更加困难。

**•**在通用 Chatbot 中，用户通常缺乏强烈的反馈意愿，而即使给出反馈，往往也比较模糊或稀疏；

**•**在多步 Agent 任务中，因为缺乏用户 context ，很难完整复现用户交互、要做一次 online trial 常常行不通，因此很难像单步任务一样获得清晰的 Reward。

所以 Online learning 在相当大程度上会以 RL 的方式来实现，但和 online RL 和 Online Learning 存在一定的 gap， 主要表现在 reward 和 environment 上。

**44.** Reward  Model 的问题在于存在 reward 定义与最终目标之间的差距，这种不一致容易导致学习过程偏离预期方向，从而影响效果。

**45.**从过去推荐系统模型的实践来看系统的反馈速度是实现有效 Online Learning 的关键。离线模型的话很容易取得效果提升，但我们希望模型能够持续在线学习，因此模型收集数据的频率和更新参数的频率可能是需要提升的，但今天模型参数都很大，如何做到快速更新、收集到的数据是否足够让模型向前一个 step 都属于没有研究清楚的问题。

**46.**除了上述两个因素之外，RL 环境的变化程度也会极大地影响 Online Learning 的有效性与稳定性，如果环境高度动态，模型就难以捕捉到稳定的学习信号。

**47.**在 reward 上，Online Learning 非常依赖从环境或用户交互中提取的 reward，但现实中许多任务缺乏清晰的 reward 信号，往往需要人工设计，这限制了模型的适用性与通用性。

**48.**围绕 Reward 的设计，目前的做法通常依赖于封闭环境（如 coding），因为这类环境的 reward 定义明确且容易获取。但未来的发展方向应是让模型具备自我生成 reward 的能力，从而减少对外部显式 reward 的依赖，而这可能正是实现真正高水平智能的关键路径。

**49.** 也有观点认为，虽然 Online Learning 具体实现形式尚不清晰，但研究方向已经较为明确，也就是通过交互、探索（exploration）和奖励的自我收集（reward self-collection），让模型能够不断改进自身能力。

**2 种机制选择： in-context learning 还是 in-weights learning？**

**50.**Online Learning 的目标场景可以分成两类：

1）任务分布随时间演化的场景，例如金融（市场信号会随便，但这类场景在实际应用中相对有限）；

2）大规模个性化：即每个用户的需求不同，agent 需要持续适应个体化偏好，

**51.**从实用主义角度出发，weights 级别的个性化学习（即每个用户的需求不同，agent 需要持续适应个体化偏好）其实并不实际，因为：

1）Weights 级别的个性化学习成本很高，相当于要为每个用户单独运行一次模型，但每个用户都有一个自己的模型从部署上很不现实；

2）Weights 这种黑盒级别的个性化会在可解释性角度没有 in context learning 好，会在商业落地上遇到挑战。

**52.**从 learning 手段来看 online learning 的话，online learning 可以和 in-context learning 对应，更进一步就是 in-weights learning，它和 slow weight 是两类重要但不同的学习机制：

**•**Fast weight： 代表短期的快速变化，例如 KV cache 或线性 attention state 等机制。需要注意的是，Fast weight 并不一定是纯 forward，在一些新结构中，fast weight 的更新也包含了 backward；

**•** Slow weight：通常对应传统的参数更新方式，例如通过梯度下降来调整模型参数。这类更新频率较低，更偏向长期的稳定改进。

**53.** Fast weight 与 slow weight 并不冲突。前者能够支持模型在短时间内快速适应新的输入或环境，而后者则为模型提供持久的记忆和稳定性。因此，Online Learning 可以结合 Fast weight 与 slow weight，并不必局限于某一种机制。

**54.** 传统的 in-weights learning 是通过更新模型参数来实现学习，而 in-context Learning 则依赖于上下文信息（fast weight）来实现快速适应，并不一定需要参数的更新。

**55.**换一个角度来看，也可以将 Learning 分成两种方式：

**•**参数化学习（Parametric Learning）：通常就是指狭义的 training，即通过更新模型参数将知识编码到参数里，比如 RL 中的参数更新。

**•**非参数化学习（Non-parametric Learning）：不依赖显式的参数更新，而是在推理过程中，通过改变梯度流、内部状态或输出分布来适应任务。典型代表就是 in-context learning。

**56.**Richard S. Sutton 说的“Learning from experience” 讲的也是 online learning：当模型在某个任务上第一次出错时，如果能立即在第二次执行时纠正错误，这就是 online learning 能力的直接体现，但这件事今天模型还做不到第一遍做错之后能够从中获得教训、立刻改正，缺乏类似人类的快速复盘与即时改进能力。

**57.**在不更新模型参数的情况下要会实现 online learning 有个前提是 in-context learning（或 fast-weights）需要保证系统前序和环境交互产生的实时数据能够影响后续模型的输出。但不确定今天的模型架构或数据处理机制是否可以做到这一点？以现在的架构 fast weight 做不到永久性的，存在一个时间上限，但这个上限可以很长。

**58.**从技术实践上需要解决 2 个问题：

**•**架构：需要设计一种能够持续收集新数据并影响输出的体系。这可能包括维护 memory、context 或参数更新等手段，简单来说是确保策略（policy）能够随着新数据不断更新和优化。

**•**数据筛选：今天的模型普遍缺乏辨别哪些数据的能力，但人类学习效率高的原因之一就在于能够自动筛选并聚焦关键数据，这一点可能对于模型实现 online learning 很关键。

**59.**现阶段的 in-context learning 中 context 的内容完全由外部输入决定，模型只能被动利用已有信息来完成任务。而在下一阶段（e.g in-context agent learning），可能会出现agent 自己决定 context、自己做 context engineering 的能力。这种演进会让 learning 的形态发生根本性的变化。

**60.**Online Learning 的关键其实不在于是否更新权重，而在于如何将 reward 注入模型，如果模型能够理解 reward 的含义，例如区分正负反馈在此基础上调整策略（policy），那么它并不一定需要依赖参数更新即可完成适应；但如果模型无法直接理解 reward，那么就必须通过参数更新（如 RL）将这些信息写入模型内部。

**61.**是否做 in-weights learning 可能并不重要，更重要的是引入环境、获取 reward，以及模型怎么用好 reward。假如模型有 in-context RL 能力，能够理解 reward 代表的意思，就不需要 weights 更新。但如果模型不懂，就需要把 reward 更新到模型中。

**62.**选择怎么更新 reward 随着架构层面演技改变的：以现在的技术更新 reward 的方式仍旧是 RL 的方式，假如未来有一天架构能够支持在 fast weight 层直接注入 reward，就可以绕过传统的参数更新。

**63.**对于非架构研究者而言，可以重点关注两个方向：

**•** 如何更好地抽取 reward 信号，从而能从复杂环境和长任务链条中提炼有效反馈；

**•** 如何设计能够体现持续改进需求的长任务。

**64.**在理解 Online Learning 时，需要区分 Learning 与 Training 的概念：training 在狭义上是指通过反向传播（如 SGD 等方法）来改变模型权重；Learning 并不一定依赖参数更新，例如 in-context learning。

**65.**从硬件角度来看，Training 意味着存在反向传递的计算，而 in-context learning 是 哦依赖前向推理过程，虽然没有涉及权重更新，但同样能够实现部分 Online Learning 的功能。目前对于 in-context learning 的极限究竟在哪里，还没有明确答案。

**Memory 是重要组成部分**

**66.** 从实用主义角度出发，优化 memory 是比全参数角度更好的路径。

**67.**如果把 Agent 系统当成一个学习目标，那么 online learning 的实现并不一定是模型更新，也可以是更新 memory 或者其他外部组件来实现能力提升。

**68.**Memory 是 Online Learning 的重要组成部分。即使模型参数保持不变，随着记忆的不断积累，模型的策略（policy）也会发生变化。这种能力与人类的记忆系统相似，能够帮助模型识别和存取重要信息。

**69.**今天 memory 系统大多还是外部的固定组件，但未来希望模型能够拥有自主的 context engineering 和记忆管理能力。类似于人类有自己的一套记忆系统，自己决定哪些重要、不重要，甚至自己回忆，理想状态下 AI（agent）系统也需要这样的能力。

**70.**可以通过 Memory 更新来推动 online learning 的发展，这与自动化的 context engineering 不同，这个方法强调通过 memory 来为每个用户存储独立的 memory slot（外部参数），并在每次交互后直接改写 memory，而不是单纯累积 context 再由系统进行筛选。

**71.**但 memory 的路径做 online learning 会遇到模型学习效率的问题。如果系统只是依赖 memory 而不更新模型参数，虽然形式上也可以说是 online learning，但有一个技术问题需要解决：如何保证模型在与环境多次交互时前后计算的连贯性。

**•**理想状态下，模型在回答完一个问题后，会根据结果对 memory 进行更新，再依赖更新后的 memory 去回答下一个问题。这样一来，不同交互之间的计算就能够建立起联系，整个系统的学习效率也会显著提高。

**•**反面情况是：如果模型在回答多个问题时，没有对 memory 进行及时更新，那么每一次计算实际上彼此之间没有任何关系，本质上就等于只是把已经收集到的问题和答案重新堆叠，然后再统一计算一次。

**72.**但 online learning 不应该被狭义地理解为模型参数的更新。类比人类大脑，我们并不会随时重构神经网络，而是依靠记忆、存储以及对外部信息的利用来提升认知与能力。因此，Online Learning 更合理的定义是：整个 agent 系统的动态优化，而不仅仅局限在模型本身。比如，参加一场讨论会可能会改变一个人的策略或认知方式，但并不会直接修改那个人的神经网络结构。系统层面的 Online Learning 正是通过外部知识的存储与利用来实现能力提升。

**04.**

**架构与算力问题**

**来自推荐系统的启发**

**73.**Online Learning 的价值并不在于追逐最新的数据分布，而在于真正理解用户的长期行为，也就是实现个性化。在推荐系统的实践中，Online Learning 不仅仅是为了适应动态变化的分布，更重要的是捕捉并建模用户的个性化偏好，比如通过引入端到端的架构，尤其是更接近 decode 的结构来提升模型的容量，从而更好地对用户的长期特征进行建模。

**74.**好的 online learning 是 reward environment 给的奖励只和模型决策有关，这一点很重要。

**75.** 推荐系统模型很早就进入到 online learning，并且更新频率在 1 分钟以内，但过去之所以做得不好是因为没有做到端到端， in-model 的结果没有立即拿到 reward。

**76.** 目前推荐系统已经能够实现分钟级的更新，而现有的大模型往往需要以小时甚至天为单位进行迭代，这也印证了前文提到的 Online Learning 的一个必要条件：端到端的反馈必须足够短。也就是说，模型产生结果后需要能够迅速获得与该决策直接相关的 reward，如果 reward 需要经过复杂的处理后才能传递给模型，它的价值就会被大大稀释。

**77.**推荐系统实操中，相比 offline 系统，online 系统的表现差异并没有拉大的趋势，最终效果往往仍然趋于一个恒定的 gap。

**78.**为什么推荐场景还没有构建出完善的 online learning ？

**•**一定程度上和推荐系统的学术研究投入不够相关，工业界以业务 KPI 为核心，相关的基础研究相对较少；

**•**最本质原因是推荐系统在过去都还不是一个端到端的结构。从结构上看，过去的推荐系统大多采用多模块拼接的方式，e.g 召回、粗排、精排等。非端到端的系统 learning 很低效，因为无法确定某个模块的迭代是否会对整个系统表现带来升级。

**•**随着硬件性能提升和模型结构的发展，行业在最近几年才开始有机会做端到端的生成式推荐系统，在这种架构下，online learning 和数据筛选等问题才有可能真正发挥作用。

举例：在非端到端推荐系统里，可以拿到的用户行为反馈在于最后“行为曝光”环节，但这个数据只能用于最后一个模块（通常为精排）。这个模块处理的数据也不是端到端的，它处理的问题是：输入 M 个候选集里，最终曝光了 N 个内容。因此模型训练只能围绕 N 个曝光内容得到的用户反馈进行迭代，且这个反馈只能用于提升最后一个模块的能力，但当系统的性能迭代到一定程度后，如果希望进一步提升用户体验或提高线上点击率，仅靠优化最终排序往往是不够的。在这种情况下，就要考虑前序模块的能力提升，例如提供 M 个候选集的模块质量，但它的优化是没有办法通过 N 个曝光的数据反馈来提升的。

**79.**用户的最终反馈只能直接影响最后的精排模块，而前端模块（如召回）难以直接优化，因为它们的 action 与最终 reward 之间缺乏端到端的关联，这导致系统容易快速收敛到局部最优，难以持续探索和改进。

**80.** 推荐系统和 coding 不一样：Coding 给出的结果用户是否接受很明确，即用户反馈足够清晰，而推荐系统交互时间短：用户做决策、信息量、一条样本可提供的有效信息很少。

**81.** 即便推荐的优势在于数据量足够大，但在实践情况中，可以学习的有效数据并不多。目前在推荐领域的端到端实践还比较失望，和 offline 相比还没出现预期中的“模型越来越好”的情况。

**Agent 系统需要端到端吗？**

**82.**Cursor 今天拿出来的结果其实不是特别震撼，因为如果真的实现 online learning 的效果，Cursor 应该给出一个随着收集的 data 越来越高，模型能力持续提升的趋势，而不是快速收敛，后者通过 off-line learning 就可以做到的。

**83.** 端到端系统有机会实现更高天花板的迭代，LLM 的成功受益于端到端的架构，受益于 scaling law，一旦系统被拆解成很多个模块，那么系统定义、模块迭代

**84.** 从实操角度，Agent 系统在中短期有一定概率会模块化：

**•**商业角度上，在今天技术还没研究基础的情况下，为了满足用户任务需求，有可能在短期内通过拆解成多个模块，但要实现 online learning ，可能会存在 1）把实现关键结果的模块做到端到端，2）一些模块不更新，以“固定策略”的形式呈现。

**•**本质上会回归 RL 的归因问题（credit assignment）。类似于 Language Chain of Thought（LCOT）中，我们无法确定某一段话或某个 token 应该被赋予怎样的价值。在多模块的 agent 系统中，也很难判断 memory 或其他中间模块对最终结果的贡献度。因此，在实际应用中，系统通常只能依赖最终的 outcome reward 来决定是否对模块做了正确的更新。

**Online Learning 的算力挑战**

**85.**假设我们把模型个性化问题定义为 context 问题，则存在两种范式：

**•**模型直接利用更长的 context，例如，有时模型在对话中会尝试纠正用户，那么我们可以把这些历史纠正的记录都放入 context 中。通过分析更长的 context，模型能够更好地理解语境，从而从中获得更多信息，用于学习和改进。

**•** 由于现有模型并不擅长直接处理 context 数据，因此需要在训练过程中，将 context 中的关键信息注入到模型的参数（weights）中，通过 learning 来改变分布。

**86.**相对于前者而言，后者的可实施性更强，因为在算力上更高效。因为如果只依赖模型自己处理更长的 context 来实现模型能力提升，就意味着在此前的所有交互中（无论是用户与系统、还是模型与环境之间的交互），计算都是相互独立的，彼此之间没有共享或复用，也没有得到更好的效果。

在长 context 路径上，由于大量计算仅仅用于简单的信息累积，而没有真正转化为学习，这在算力层面可能会造成明显的资源浪费。假设总 context 长度为 100 万个 token，而每次交互需要处理 1 万个 token，那么系统必须重复进行 100 次推理，累计处理 100 万个 token。但这些推理计算彼此之间是独立的，并不会对下一次推理产生增益。结果就是，大量计算仅仅被用于简单的累积，而没有转化为真正的学习。

**87.** 从这个角度来想， in-weight learning 具有更明显的优势。通过 in-weight learning 或 memory 更新，让每一次交互的计算结果都能被留存，从而对后续模型表现产生影响。

**88.**但今天 GPU 也许并不是主要问题，需要先把流程跑通再考虑 scaling 的问题，更多的挑战在于数据与环境，如果没有合适的数据和环境支撑，过早做 scaling 是非常危险的。

**05.**

**Online learning 下的评估范式变化**

**89.**可以优先选择一些冷启动场景进行检验，比如在新功能上线后，可以观察能否通过少量的用户交互快速提升整体满意度是最直接的检验方式。

**90.**还可以找一个“新游戏”（AI 没见过的新游戏），让 AI 系统不断地玩，希望社区有人做这件事：

**•**比如 DeepMind Atari 街机、下围棋等都是类似的思路；在这种设定下，模型一开始的表现可能很弱，但经过几十到上百局的交互，能力会逐步提升。

**•** 在这个过程中，关键的观测指标不是最终分数，而是性能提升的斜率，这个数字能直观反映模型在短期内的学习速度。

**91.**这个过程和迁移学习不同，不是从已有任务迁移到新任务，而是检验模型在全新环境中的即时学习过程。

**92.** 进一步来看，上述框架可以类比为一种 Meta Learning 测试方式。具体做法是：给模型一个从未见过的新任务，允许模型在一定时间内进行 online adaptation，然后再对模型的表现进行评估。例如，在游戏场景中，可以让模型适应一种全新的棋类环境，并观察它在数小时内的进步幅度；

**93.** 评价 meta online learning 的标准是 text-time scaling 曲线的斜率：主要观察模型 CoT 或者 inference compute 过程中，随着时间增加，生成 token 的质量和智能水平是否显著提升。

**94.**机器人领域也可以沿用这个思路，也急需拥有的能力：可以测试模型进入陌生房间后，是否能在短时间内学会在环境中移动并完成任务。这里的核心指标是模型在适应前后性能的差距（gap），它能够量化模型真正的 online learning 能力。

**95.**在传统模型学习中，通常使用固定的训练集（training-set）和固定的测试集（testing-set），目标是衡量模型在静态任务上的性能。在 online learning 场景下，testing 本身就包含了 training 的过程。

**96.**在 meta learning 的视角下，online learning 的测试流程可以是这样一个流程：

**•** AI 系统和 100 个用户做交互。其中，如果用户 A 与系统进行了很多轮互动，这个过程本身就可以被视作 Online Learning 的过程。

**•**互动结束后可以再测试系统对用户 A 的理解程度，形成 reward。

这个流程和目标本身就和 meta learning 的逻辑高度一致，也就是系统需要通过少量交互快速适应用户的需求和偏好。但这一点今天还没形成共识。

**97.** 测试流程必须包含交互与适应环节，才能真实反映系统的学习能力。

**98.** 虽然 RL 环境仍然是底层的重要框架，但最终依旧需要设计合理的 final reward 来衡量整体表现。

**99.**Memory 与 agent 的使用方式也必须被重新纳入测试与优化的环节。

排版：夏悦涵

延伸阅读

[![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/005.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518502&idx=1&sn=2930195ac8478084ca8d8770c08a4dd1&scene=21#wechat_redirect)

经验时代的 Scaling Law｜AGIX PM Notes

![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/006.png)

[![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/007.png)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518470&idx=1&sn=21efdd5f223ca848235c6d9ce65472b9&scene=21#wechat_redirect)

深度讨论 Pulse：OpenAI 超越 Google之路的开始 ｜Best Ideas

![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/008.png)

[![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/009.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518426&idx=1&sn=523497b9f61a5b0c3fc4614ec5cd842f&scene=21#wechat_redirect)

AI X 用户研究：能并行千场访谈的“超级研究员”，正重塑产品决策的未来

![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/010.png)

[![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/011.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518339&idx=1&sn=98990578287f19823437707618ddff0e&scene=21#wechat_redirect)

Notion、Stripe 都在用的 Agent 监控，Braintrust 会是 AI-native 的 Datadog 吗？

![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/012.png)

[![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/013.jpg)](https://mp.weixin.qq.com/s?__biz=Mzg2OTY0MDk0NQ==&mid=2247518280&idx=1&sn=4269bb7783a39377b1a856bc0d88f6bb&scene=21#wechat_redirect)

RL Infra 行业全景：环境和 RLaaS 如何加速 RL 的 GPT-3 时刻

![](../images/2025-09-30-shen-du-tao-lun-online-learning-99-tiao-si-kao-du-dong-llm/014.png)
