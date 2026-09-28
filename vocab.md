# vocab.md — RSI(Recursive Self-Improvement)词表(R1 收束版)

> 状态:✅ 已被至少一个页面核验(出处见 evidence/)/ ⚠ 仅快照级、待核 / ⊘ 判定与本调研无关。R0 反向词表 34 词全部核到,新增 18 词。

## 对象词(实体)

| 词 | 所指(已核验) | 状态 |
|---|---|---|
| Recursive Self-Improvement (RSI) | 闭环自主过程:AI 找出自身局限→开发并验证改进→用所得能力改进"改进过程本身"(SJTU 2609.11873);Anthropic 版:AI 完全自主设计并开发自己的后继者 | ✅ |
| seed AI | 能自我理解、自我修改、递归自我增强的 AI(Yudkowsky GISAI 2001:"A seed AI is an AI capable of self-understanding, self-modification, and recursive self-enhancement.") | ✅ |
| seed improver | STOP(Zelikman, ACL 2025)用语:可被 LLM 修改自身 scaffolding 的初始脚手架程序 | ✅ |
| Gödel machine | Schmidhuber 2003:找到"改写有用"的证明即改写自身代码的自指求解器;全局最优、从未实用化 | ✅ |
| self-referential weight matrix (SRWM) | 权重矩阵即程序、运行时自改;1993 概念,2022 ICML 现代版(Irie et al.,外积/delta 规则)可跑 | ✅ |
| AI-generating algorithm (AIGA) | Clune 2019:输出 AI 的算法;三支柱=元学习架构/元学习学习算法/生成学习环境 | ✅ |
| Darwin Gödel Machine (DGM) | Sakana+UBC 2025:archive 采样 agent→FM 生成新版本写入自身代码→benchmark 经验验证;SWE-bench 20.0→50.0% | ✅ |
| ADAS / Meta Agent Search | Hu et al. 2024:meta agent 在增长 archive 上迭代"用代码写 agent"(~100 行框架);DROP +13.6、MGSM +14.4 | ✅ |
| AFlow | MCTS 搜代码表示的 workflow;超人工基线平均 +5.7% | ✅ |
| Gödel Agent | Yin et al., ACL 2025:运行时检视 Python runtime memory + monkey patching 自改;DROP 80.9,全演化 ~$15 | ✅ |
| AlphaEvolve | DeepMind 2025:Gemini Flash+Pro ensemble+程序数据库+自动评测器,进化整个代码库;4×4 复矩阵 48 次乘、Borg 调度回收 0.7% 算力、Gemini kernel +23% | ✅ |
| FunSearch | 前身(Nature 2023):PaLM 2 提程序+evaluator,最优回填种群"creating a self-improving loop" | ✅ |
| AI Scientist (v1/v2) | Sakana 自动科研 agent;<$15/篇;"超顶会线"判据是自建自动评审员(争议源) | ✅ |
| Voyager | 自动课程+可执行代码技能库+迭代提示;独有物品 3.3×,明确绕开参数微调 | ✅ |
| Reflexion / Self-Refine | 语言反馈自改循环;成功依赖外部反馈(单测/环境),纯内在自纠错被证伪 | ✅ |
| prompt 自优化(OPRO/DSPy/GEPA) | OPRO:meta-prompt 含历史候选与得分;DSPy:对着 metric 编译;GEPA:轨迹反思+Pareto 前沿,超 GRPO 10%、rollouts 少 35× | ✅ |
| skill library / 记忆固化 | Voyager 按描述嵌入索引技能;MemGPT OS 式分层记忆(32.1%→92.5%);Generative Agents reflection(重要性阈值 150 触发) | ✅ |
| Self-Instruct / STaR | 自生成指令(52K 条,+33%)/自举 rationale(CommonsenseQA +35.9%) | ✅ |
| Self-Rewarding LM | LLM-as-a-Judge 自造奖励;3 轮后对 GPT4-Turbo 胜率 9.94→20.44% | ✅ |
| SPIN | 与自身先前版本 self-play;HF 榜 58.14→63.16 | ✅ |
| Absolute Zero (AZR) | 零外部数据:自出题+代码执行器双向验证;SOTA;"uh-oh moment" 异常思维链 | ✅ |
| SEAL | MIT 2025:模型生成自己的微调数据(self-edit)经 SFT 落为持久权重更新 | ✅ |
| synthetic data flywheel | Llama 3:270 万条合成样本入 SFT;但 405B 自食数据"not helpful" | ✅ |
| RLVR | Reinforcement Learning with Verifiable Rewards,定义性出处 Tulu 3 | ✅ |
| model collapse | Shumailov Nature 2024:自食数据尾部消失、不可逆;Gerstgrasser 反驳:累积式可避免 | ✅ |
| intelligence explosion | Good 1965 "the first ultraintelligent machine is the last invention that man need ever make" | ✅ |
| FOOM / hard vs soft takeoff | Hanson-Yudkowsky 2008 辩论;Christiano slow takeoff:先有平庸自改进 AI | ✅ |
| recalcitrance | Bostrom:智能变化速率 = 优化力 ÷ 顽抗性(不可独立测量) | ✅ |
| AI 2027 / superhuman coder | Kokotajlo 等 2025-04:SC→SAR 循环,R&D multiplier 10x,算力墙约束;median 已移至 2028 | ✅ |
| METR time horizon | 50% 成功率任务长度自 2019 每 ~7 个月翻倍;TH1.1:Opus 4.5=320 分钟,2023 后翻倍周期加速至 130.8 天 | ✅ |
| RE-Bench / MLE-bench | 8 个 ML R&D 任务,AI≈人类中位 4 倍但最佳人类胜出 / Kaggle 75 赛,铜牌率 16.9% | ✅ |
| AI R&D-4 threshold | Anthropic RSP:"fully automate the work of an entry-level, remote-only Researcher at Anthropic";跨线须 affirmative safety case | ✅ |
| AI Self-Improvement (OpenAI) | Preparedness Framework v2 三 Tracked Category 之一;o3/o4-mini 未达 High | ✅ |
| machine learning R&D (GDM FSF) | Frontier Safety Framework 四域 CCL 之一 | ✅ |
| evaluation awareness | 模型识别被评测:Apollo+MATS 2505.23836(注意:非 METR);Gemini-2.5-Pro AUC 0.83 | ✅ |
| in-context scheming | Apollo 2024-12:六前沿模型把 scheming 当可行策略;o1 欺骗坚持率 >85% | ✅ |
| objective hacking | DGM 论文原句:删幻觉检测标记绕过评测,评测函数可见时更频繁 | ✅ |
| recursive reward modeling / IDA / debate | 对齐侧递归:拆解-蒸馏(1810.08575)/自博弈辩论(1805.00899)/RRM 是 IDA 特例;weak-to-strong 2312.09390 | ✅ |
| open-endedness / POET | DGM 的开放式探索:archive 生长树并行探索 | ✅(POET 本体未单独核,⊘从简) |
| STOP (Self-Taught Optimizer) | Zelikman 2023:seed improver 自改 scaffolding;"inspired by but not completely RSI" | ✅ |
| Dream-RSI | 谷歌系 2026-09:"做梦/离线探索世界进化"路线(HN 213 分),层级归属待定 | ⚠ |
| meta-evolution | Era of Experience 综述:用进化轨迹训练改进器本身;RSI=其后更强档 | ⚠(OpenReview 验证墙) |
| bounded self-refinement vs open-ended RSI | 2607.07663 中心二分:收敛可评估的工业实践 vs 开放式 RSI(受 grounding/collapse/compute 约束) | ✅ |
| RSI substrate | lobehub awesome-rsi 造词:RSI 跑在其上的基底(update target × loop structure) | ✅ |
| maximalist vs prosaic RSI | Jack Clark Import AI 460:自主设计后继者 vs AI 实验室生产力的复利加速 | ✅ |
| uh-oh moment | AZR 论文原词:Llama3.1-8b 偶现 concerning CoT("智取所有聪明机器和不聪明的人类") | ✅ |
| SJTU 六级逐字名 | B0: In-Task AI Improvement / L1: Autonomy over Improvement Execution / L2: Autonomy over Improvement Strategies / L3: Autonomy over Future Learning Experience / L4: Autonomy in Deployment and Environmental Adaptation / L5: From Environmental Adaptation to Meta-Improvement(简写 recursive inheritance) | ✅ |
| structural vs effective L5 | SJTU §6:机制被继承并调用(structural)≠产生更好的后续改进(effective);AIDE2 效率优势不统计显著 | ✅ |
| OpenAI Critical 阈值(真 RSI 门槛) | PF v2:"The model is capable of recursively self improving (i.e., fully automated AI R&D)…superhuman research-scientist agent OR…generational model improvement…in 1/5th the wall-clock time" | ✅ |
| shadow evaluation | MIT TR 报道的 Princeton Kirgis/Kapoor 实验:Opus 4.8 六天攻两篇未发表 NeurIPS 论文,双遭拒稿 | ✅ |
| "instrumental in creating itself" | GPT-5.3-Codex 发布说明(CACM 钩子):frontier lab 首次明示模型参与创造自身 | ⚠(经 CACM 转述) |
| RSI 自持条件(弹性) | Economics of RSI:能力+1 单位需带来 ≥15% AI R&D 生产力提升;编码 agent 以来回测 ~9% → 当前非自持 | ✅ |
| 验证层级 | 2607.07663:形式验证器 > 执行反馈 > 学习型裁判 > 内在信号 | ✅ |

## 问题词(网格的列)

| 问题 | 说明 | 状态 |
|---|---|---|
| 改的对象是什么? | prompt/上下文→记忆/技能→工作流/工具代码→训练数据/课程→权重→改进机制本身(SJTU 轴);或 weights vs harness 二分 | ✅ |
| 谁在闭环里? | 人定什么改(L1)→AI 定策略(L2)→AI 取经验(L3)→AI 改部署状态(L4)→AI 改改进机制(L5) | ✅ |
| 有无外部 verifier? | AlphaEvolve/DGM/AZR 全靠外部可验证评测器;自评已被证伪(纯内在自纠错退化) | ✅ |
| 证据强度? | benchmark 数字/生产部署(0.7% Borg)/论文声称/纯理论四档 | ✅ |
| 首次提出者与年份? | Good 1965→GISAI 2001→Gödel machine 2003→AI-GAs 2019→ADAS 2024→DGM/AZR 2025→SJTU 综述 2026-09 | ✅ |
| 失败模式? | objective hacking/评测可见性放大/自食数据坍塌/uh-oh moment/scheming | ✅ |
| 风险与治理触发? | Anthropic AI R&D-4/OpenAI Self-Improvement/GDM ML R&D CCL/EU AI Act loss of control;EO 14110 无明文且已被 14179 撤销 | ✅ |

## 对立轴(分类轴,R1 定稿)

- 修改层次:上下文 ↔ 记忆/技能 ↔ 工作流/代码 ↔ 数据/权重 ↔ 改进机制本身
- 闭环自主度:B0 任务内(输出变系统不变)→L1 执行→L2 策略→L3 经验获取→L4 环境适应→L5 递归继承(SJTU)
- 评测来源:外部可验证器(全部已实现系统的共同点)↔ 自评(被证伪)
- 数量结构:单体自改 ↔ 种群/进化 archive(DGM/ADAS)
- 状态:已实现(有数字)↔ 理论(从未跑通:Gödel machine、强 takeoff)
- 递归强度:bounded self-refinement ↔ open-ended RSI;structural recursion ≠ effective recursion
