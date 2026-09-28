# w2-shallow-loop
question: AI 领域 RSI 浅层(不改权重,只改上下文/记忆/技能库):(a) Self-Refine/Reflexion 循环结构与失败模式(含自纠错无效说);(b) OPRO/DSPy/GEPA prompt 自优化;(c) Voyager 技能库/MemGPT 分层记忆/Generative Agents reflection;(d) 该层解决什么、不解决什么。
checked: https://arxiv.org/abs/2303.17651, https://ar5iv.labs.arxiv.org/html/2303.17651, https://ar5iv.labs.arxiv.org/html/2303.11366 (arxiv.org/abs 页两次超时,改用 ar5iv), https://arxiv.org/abs/2309.03409, https://ar5iv.labs.arxiv.org/html/2309.03409, https://arxiv.org/html/2305.16291v2 (abs 页超时,改用 HTML 全文), https://ar5iv.labs.arxiv.org/html/2310.08560, https://ar5iv.labs.arxiv.org/html/2310.01798 (经 WebSearch 定位,编号 2310.01798 而非任务书未写明的猜测), https://ar5iv.labs.arxiv.org/html/2507.19457 (经 WebSearch 定位), https://arxiv.org/html/2304.03442v2, https://dspy.ai (根页是跳转壳,实际内容取自 dspy.ai 首页渲染内容), https://ar5iv.labs.arxiv.org/html/2406.01297 (追加:自纠错批判综述), WebSearch ×2 ("Large Language Models Cannot Self-Correct Reasoning Yet"; "GEPA reflective prompt evolution")

## claims
- [C1] Self-Refine 的循环就是同一个 LLM 充当生成器、反馈器、修正器三角色,交替"反馈→修正"直到停止条件 | src: https://ar5iv.labs.arxiv.org/html/2303.17651 | quote: "instead uses a single LLM as the generator, refiner and the feedback provider." | type: primary
- [C2] Self-Refine 覆盖 7 个任务、平均约 20% 绝对提升,且完全不需要训练或强化学习 | src: https://arxiv.org/abs/2303.17651 | quote: "Self-Refine does not require any supervised training data, additional training, or reinforcement learning" (7 任务与 ~20% 见 https://ar5iv.labs.arxiv.org/html/2303.17651: "improving by ∼20% absolute on average in task performance.") | type: primary
- [C3] Self-Refine 的失败主要来自反馈定位错(33%)与修法不当(61%),且提升随迭代边际递减 | src: https://ar5iv.labs.arxiv.org/html/2303.17651 | quote: "33% of unsuccessful cases were due to feedback inaccurately pinpointing the error's location, while 61% were a result of feedback suggesting an inappropriate fix." 另 "the marginal improvement naturally decreases with more iterations." | type: primary
- [C4] Self-Refine 的可用性受底座模型能力下限约束 | src: https://ar5iv.labs.arxiv.org/html/2303.17651 | quote: "the base models need to have sufficient few-shot modeling or instruction-following abilities" (弱模型直接失灵:"Vicuna-13B was not able to consistently generate the feedback in the required format.") | type: primary
- [C5] Reflexion 是"语言反馈强化":不更新权重,靠把反思文本存进情景记忆缓冲改善后续决策 | src: https://ar5iv.labs.arxiv.org/html/2303.11366 | quote: "We propose Reflexion, a novel framework to reinforce language agents not by updating weights, but instead through linguistic feedback." 另 "maintain their own reflective text in an episodic memory buffer to induce better decision-making." | type: primary
- [C6] Reflexion 由 Actor、Evaluator、Self-Reflection 三个模型组成,反思模型生成口头强化线索供 Actor 使用 | src: https://ar5iv.labs.arxiv.org/html/2303.11366 | quote: "generates verbal reinforcement cues to assist the Actor" | type: primary
- [C7] Reflexion 在 HumanEval 达 91% pass@1,超过当时 GPT-4 的 80% | src: https://ar5iv.labs.arxiv.org/html/2303.11366 | quote: "Reflexion achieves a 91% pass@1 accuracy on the HumanEval coding benchmark, surpassing the previous state-of-the-art GPT-4 that achieves 80%." | type: primary
- [C8] Reflexion 在 ALFWorld 完成 130/134 任务,HotPotQA 摘要口径 +20%(正文另有 +22% 表述) | src: https://ar5iv.labs.arxiv.org/html/2303.11366 | quote: "completing 130 out of 134 tasks using the simple heuristic" 另 "on reasoning questions in HotPotQA by 20%." | type: primary
- [C9] Reflexion 已知局限:依赖 LLM 自评能力、会陷入局部最优、无法完成需要大量探索的任务(WebShop) | src: https://ar5iv.labs.arxiv.org/html/2303.11366 | quote: "Reflexion is unable to solve tasks that require a significant amount of diversity and exploration." 另 "may still succumb to non-optimal local minima solutions." | type: primary
- [C10] 反方核心证据:不加外部反馈的"内在自纠错"普遍让性能下降,有时越改越差 | src: https://ar5iv.labs.arxiv.org/html/2310.01798 | quote: "our research indicates that LLMs struggle to self-correct their responses without external feedback, and at times, their performance even degrades after self-correction." | type: primary
- [C11] 自纠错退化的具体数字:GPT-4 GSM8K 95.5→91.5→89.0(两轮),GPT-3.5 CommonSenseQA 75.8→38.1(第一轮即崩),全模型全基准下降 | src: https://ar5iv.labs.arxiv.org/html/2310.01798 | quote: "we observe that, after self-correction, the accuracies of all models drop across all benchmarks." | type: primary
- [C12] 根因是模型无法正确判断自己推理的对错;但外部反馈(oracle 标签、代码执行结果等)到位时自纠错确实有效 | src: https://ar5iv.labs.arxiv.org/html/2310.01798 | quote: "The fundamental issue is that LLMs cannot properly judge the correctness of their reasoning." 另 "when valid external feedback is available, it is beneficial to leverage it properly to enhance model performance." | type: primary
- [C13] 2024 批判性综述的结论:没有任何先前工作证明了"被提示的 LLM 自我反馈"式自纠错普遍成功;有效场景集中在可靠外部反馈或大规模微调 | src: https://ar5iv.labs.arxiv.org/html/2406.01297 | quote: "no prior work demonstrates successful self-correction with feedback from prompted LLMs" 另 "self-correction works well in tasks that can use reliable external feedback" | type: secondary
- [C14] OPRO 把优化本身交给 LLM:每步从"含历史候选解及其得分"的 meta-prompt 中生成新解,优化轨迹完全活在上下文里 | src: https://ar5iv.labs.arxiv.org/html/2309.03409 | quote: "the LLM generates new solutions from the prompt that contains previously generated solutions with their values" | type: primary
- [C15] OPRO 优化出的 prompt 超过人工设计:GSM8K 最高 +8%,Big-Bench Hard 最高 +50% | src: https://arxiv.org/abs/2309.03409 | quote: "outperform human-designed prompts by up to 8% on GSM8K, and by up to 50% on Big-Bench Hard tasks" | type: primary
- [C16] DSPy 是编译式的:写声明式程序,对着 metric 编译,框架自动调 prompt/示例直到质量收敛(也可顺带微调权重) | src: https://dspy.ai | quote: "Compile your program against a metric, involving bootstrapping useful examples, finetuning model weights" 另 "It tunes your prompts automatically until quality converges" 与 "DSPy has been used to optimize prompts or finetune LLM weights" | type: official
- [C17] DSPy 官方优化器梯队:BootstrapFewShot 级(简单)、MIPROv2(中型任务主力)、GEPA(最复杂高风险任务) | src: https://dspy.ai | quote: "MIPROv2 — for mid-size tasks (the bulk of use cases)" 另 "GEPA — teach agents to learn from their mistakes, for the most complex and high stakes tasks" | type: official
- [C18] GEPA 机制:采样系统级轨迹(推理、工具调用、工具输出)用自然语言反思,诊断问题→提出并测试 prompt 更新→从 Pareto 前沿组合互补教训 | src: https://ar5iv.labs.arxiv.org/html/2507.19457 | quote: "GEPA samples system-level trajectories (e.g., reasoning, tool calls, and tool outputs) and reflects on them in natural language" | type: primary
- [C19] GEPA 效果:四任务上平均超 GRPO 10%(最高 20%)且 rollouts 少至 1/35,并超 MIPROv2 10%+ | src: https://ar5iv.labs.arxiv.org/html/2507.19457 | quote: "Across four tasks, GEPA outperforms GRPO by 10% on average and by up to 20%, while using up to 35x fewer rollouts." 另 "GEPA also outperforms the leading prompt optimizer, MIPROv2, by over 10% across two LLMs" | type: primary
- [C20] GEPA 的论点:语言的可解释性本身就是比稀疏标量奖励更丰富的学习媒介 | src: https://ar5iv.labs.arxiv.org/html/2507.19457 | quote: "We argue that the interpretable nature of language can often provide a much richer learning medium for LLMs, compared with policy gradients derived from sparse, scalar rewards." | type: primary
- [C21] Voyager 三机制:自动课程 + 可执行代码技能库 + 迭代提示机制 | src: https://arxiv.org/html/2305.16291v2 | quote: "Voyager consists of three key components: 1) an automatic curriculum that maximizes exploration, 2) an ever-growing skill library of executable code for storing and retrieving complex behaviors, and 3) a new iterative prompting mechanism" | type: primary
- [C22] 技能库沉淀方式:程序按"描述的嵌入向量"索引、相似情境检索 top-5 复用,简单程序组合成复杂技能产生复利并缓解灾难遗忘 | src: https://arxiv.org/html/2305.16291v2 | quote: "Each program is indexed by the embedding of its description, which can be retrieved in similar situations in the future." 另 "Complex skills can be synthesized by composing simpler programs, which compounds Voyager's capabilities rapidly over time" | type: primary
- [C23] Voyager 效果:独有物品 3.3 倍、移动距离 2.3 倍、科技树里程碑最快 15.3 倍,160 次提示迭代内发现 63 个独有物品 | src: https://arxiv.org/html/2305.16291v2 | quote: "It obtains 3.3× more unique items, travels 2.3× longer distances, and unlocks key tech tree milestones up to 15.3× faster than prior SOTA." | type: primary
- [C24] MemGPT 用操作系统式分层记忆管理突破固定上下文:main context(在上下文内)与 external context(上下文外),记忆读写检索完全自定向 | src: https://ar5iv.labs.arxiv.org/html/2310.08560 | quote: "virtual context management, a technique drawing inspiration from hierarchical memory systems in traditional operating systems" 另 "Memory edits and retrieval are entirely self-directed: MemGPT autonomously updates and searches through its own memory" | type: primary
- [C25] MemGPT 多会话聊天基准:GPT-4 基线 32.1% → 加 MemGPT 92.5%(ROUGE-L 0.296→0.814) | src: https://ar5iv.labs.arxiv.org/html/2310.08560 | quote: "++ MemGPT 92.5% 0.814" (同表 GPT-4 baseline "32.1% accuracy, 0.296 ROUGE-L") | type: primary
- [C26] Generative Agents 的 reflection:最近事件重要性分数之和超过阈值(150)即触发,把记忆合成更高层推断、长成反思树;消融显示去掉 reflection 可信度 μ 从 29.89 降到 26.88(全消融 21.21) | src: https://arxiv.org/html/2304.03442v2 | quote: "we generate reflections when the sum of the importance scores for the latest events perceived by the agents exceeds a threshold (150" 另 "the full generative agent architecture produced the most believable behavior (μ=29.89; σ=0.72)" 与 "the ablated architecture with no access to reflection was the next best (μ=26.88; σ=0.69)" | type: primary
- [C27] 该层的自改进定位:Voyager 与黑盒 GPT-4 交互即可持续长能力,明确绕开参数微调——但也受 API 成本与底座幻觉约束 | src: https://arxiv.org/html/2305.16291v2 | quote: "Voyager interacts with GPT-4 via blackbox queries, which bypasses the need for model parameter fine-tuning." 另 "The GPT-4 API incurs significant costs. It is 15× more expensive than GPT-3.5." 与 "The automatic curriculum occasionally proposes unachievable tasks" | type: primary

## conflicts
- 自纠错有效 vs 无效:Self-Refine(7 任务 ~+20%)与 Reflexion(HumanEval 91% 超 GPT-4)主张自评自改有效;Huang et al. 2310.01798(ICLR)证明纯内在自纠错全线退化(GPT-3.5 CommonSenseQA 75.8→38.1),Kamoi et al. 综述更进一步称 "no prior work demonstrates successful self-correction with feedback from prompted LLMs"。调和:成功案例的反馈都不是"纯自己看看"——Self-Refine 用任务专属 actionable 反馈 prompt,Reflexion 的 Evaluator 多来自单元测试/环境信号(外部反馈),与 Huang 的 oracle/自调试可改进结论一致。
- Reflexion HotPotQA 数字口径不一:摘要 "+20%",正文实验节出现 "+22%" 表述,引用时需注明出处节。
- GEPA 数字随版本变动:v1 摘要 "10% on average / up to 20% / 35x fewer rollouts"(四任务),WebSearch 检索摘要提到后续版本有六任务 ~6% 平均口径;引用需锁定 arXiv 版本号。
- DSPy 与浅层定义的交叠:官方页明言编译可含 "finetuning model weights",即 DSPy/GEPA 默认产物是 prompt(浅层),但框架能力跨层;"DSPy=浅层"的归类只在"默认用法"意义上成立。

## gaps
- MemGPT 文档分析任务的精确准确率只在图 5 中,文本未给出数字,未取证。
- OPRO 的著名产物 "Take a deep breath..." prompt 的确切措辞未从页面取证(在正文表格中)。
- GEPA 四任务清单未逐项取证(仅确认 "Across four tasks")。
- Self-Refine 各任务分项数字(如 code optimization 单项)未逐项取证。
- Generative Agents reflection 的计算成本/延迟未取证。
- dspy.ai 官方页无统一 benchmark 数字表;DSPy 侧效果数字只能引 GEPA 论文。

## leads
- ExpeL (arXiv 2308.10144):经验洞见(insights)沉淀进记忆供复用,浅层技能沉淀的代表作。
- Agent Workflow Memory / AWM (arXiv 2409.07429):把成功轨迹蒸馏成 workflow 记忆,网页代理复用。
- Dynamic Cheatsheet (arXiv 2504.07952):官方叫法 "test-time learning",自适应记忆在测试期积累能力、不改权重。
- ACE: Agentic Context Engineering (arXiv 2510.04618):官方叫法 "evolving playbook",上下文当增量自改进介质,含 context collapse 防护。
- Promptbreeder (arXiv 2309.16797):官方自称 self-referential self-improvement,prompt 与 mutation prompt 共同进化。
- TextGrad (arXiv 2406.07496):把文本反馈当"梯度"做 prompt 优化,OPRO/DSPy 之后一脉。
- LATS (arXiv 2310.04406):Reflexion+MCTS 结合的语言代理树搜索。
- Critic (arXiv 2305.11738):tool-interactive critiquing,"外部反馈使自纠错有效"一脉的工具化实现。
- Self-Correction Bench (2025, alphaxiv 线索):自纠错能力的系统基准,争议的后续量化。
- Letta(https://letta.com):MemGPT 团队公司化产品;有 sleep-time agents 做离线记忆整理,是"记忆层自改进"的产品化线索。
- DSPy GEPA 官方教程页:https://dspy.ai/tutorials/gepa_ai_program
- CoALA (arXiv 2309.02427):Cognitive Architectures for Language Agents,给记忆/反思/技能分层定位的分类学,适合 atlas 框架。
- Voyager 官方术语:"automatic curriculum / skill library / iterative prompting",后续社区复现多用 "skill library" 一词;长期记忆版 Voyager(嵌入式记忆)线索在论文后续工作中。
