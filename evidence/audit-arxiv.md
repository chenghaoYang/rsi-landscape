# audit-arxiv
checked:
- https://arxiv.org/html/2609.11873v3 (+ https://arxiv.org/abs/2609.11873)
- https://arxiv.org/html/2505.22954v3 (+ https://arxiv.org/pdf/2505.22954)
- https://arxiv.org/pdf/2506.13131
- https://arxiv.org/pdf/2310.01798
- https://arxiv.org/pdf/2503.14499
- https://arxiv.org/pdf/2404.01413
- https://arxiv.org/pdf/2505.03335 (+ https://arxiv.org/abs/2505.03335)
- https://arxiv.org/pdf/2410.04444
- https://arxiv.org/pdf/2507.19457 (+ https://arxiv.org/abs/2507.19457, + https://arxiv.org/abs/2507.19457v1)
- https://arxiv.org/pdf/2303.11366
- https://arxiv.org/pdf/2401.10020
- https://arxiv.org/abs/2305.16291
- https://arxiv.org/pdf/2202.05780 (+ https://arxiv.org/abs/2202.05780)
- https://arxiv.org/pdf/2403.05812

## verdicts
| # | 主张(短语) | 判定 | 证据/正确原句 |
|---|---|---|---|
| 1 | 2609.11873 六级名逐字 B0/L1-L5 | confirmed | 3.1-3.6 节标题逐字一致:"3.1 B0: In-Task AI Improvement / 3.2 L1: Autonomy over Improvement Execution / 3.3 L2: Autonomy over Improvement Strategies / 3.4 L3: Autonomy over Future Learning Experience / 3.5 L4: Autonomy in Deployment and Environmental Adaptation / 3.6 L5: From Environmental Adaptation to Meta-Improvement" |
| 1 | 三问原句 | confirmed | "Where does the loop close? determines whether an apparent improvement actually returns to the system. What is updated and inherited? determines the persistent carrier of improvement. Which decisions remain external? determines..."(三句均在 v3 正文) |
| 1 | B0 判据 output change without persistent system change | confirmed | "the defining criterion of B0 is output change without persistent system change" |
| 1 | L5 判据 persistently revises a mechanism... | confirmed | "(L5) Recursive Inheritance Autonomy. The system persistently revises a mechanism that governs subsequent improvement, such as an improver, verifier, or successor-generation procedure." |
| 1 | 491 篇在附录 Figure 18 | confirmed | "Figure 18: RSI Landscape: Autonomy Levels and Improvement Targets. Distribution of 491 surveyed papers."(HTML 中 Figure 18 位于附录节内) |
| 1 | structural vs effective L5 句 | confirmed | "These conditions distinguish structural L5, which demonstrates that an AI-directed change persists and controls a later improvement round, from effective L5, which demonstrates that the revised mechanism produces or selects better successors under comparable budgets and independent assessment." |
| 1 | AIDE2 效率优势不统计显著 | confirmed | "the AIDE 2 experiment reviewed in this survey did not establish a statistically significant efficiency advantage when an evolved harness was installed as the outer improver (Weco Team [2026])";另处 "Its stronger test of whether the evolved agent improves the outer search faster found no statistically significant efficiency advantage."(注意论文写法是 "AIDE 2",带空格) |
| 2 | 2505.22954 abstract 20.0→50.0 / 14.2→30.7 | confirmed | abstract:"increasing performance on SWE-bench from 20.0% to 50.0%, and on Polyglot from 14.2% to 30.7%" |
| 2 | Table 1 数字 DGM 50.0/38.0、w/o Open-ended 23.0/14.0、w/o Self-improve 39.0/28.0、Greedy 39.7/30.0 | confirmed | PDF:"Method DGM / DGM w/o Open-ended exploration / DGM w/o Self-improve / DGM Greedy — SWE-bench 50.0% 23.0% 39.0% 39.7%;Polyglot 38.0% 14.0% 28.0% 30.0%",正文 "As shown in Table 1, DGM Greedy achieves 39.7% and 30.0% on SWE-bench and Polyglot" |
| 2 | proving that most changes are net beneficial is impossible in practice | confirmed | 逐字在(引 Schmidhuber 2007 段) |
| 2 | node 114 removed the logging of special tokens...bypassing hallucination detection | confirmed | "the agent removed the logging of special tokens that indicate tool usage (despite instructions not to change the special tokens), effectively bypassing our hallucination detection function" |
| 2 | occurs more frequently when these functions are not hidden | confirmed | "objective hacking (i.e., optimizing for the measurable objective instead of truly solving the underlying problem) occurs more frequently when these functions are not hidden" |
| 3 | 4×4 复矩阵 48 次标量乘 | confirmed | "AlphaEvolve developed a search algorithm that found a procedure to multiply two 4 × 4 complex-valued matrices using 48 scalar multiplications; offering the first improvement, after 56 years, over Strassen's algorithm" |
| 3 | Borg 回收 0.7% 算力 | confirmed | "this heuristic function continuously recovers on average 0.7% of Google's fleet-wide compute resources, which would otherwise be stranded" |
| 3 | Gemini kernel 平均 23%、训练时间 -1% | confirmed | "a heuristic that yields an average 23% kernel speedup across all kernels over the existing expert-designed heuristic, and a corresponding 1% reduction in Gemini's overall training time" |
| 3 | accelerated the training of the LLM underpinning AlphaEvolve itself | confirmed | 逐字在摘要 |
| 4 | GPT-4 GSM8K 95.5→91.5→89.0 | confirmed | 表:"GPT-4 Standard Prompting / Self-Correct (round 1) / Self-Correct (round 2),# calls 1/3/5:95.5 / 91.5 / 89.0" |
| 4 | GPT-3.5 CommonSenseQA 75.8→38.1 | confirmed | 表:"GPT-3.5 ... CommonSenseQA 75.8 (标准) → 38.1 (round 1)"(注意 round 2 是 41.8,引 38.1 对应 round 1/3 calls) |
| 5 | doubling approximately every seven months since 2019 | confirmed | "frontier AI time horizon has doubled approximately every seven months since 2019, though the trend may have accelerated since 2024";Figure 1 caption "doubling approximately every 7 months for the last 6 years" |
| 6 | accumulating...avoids model collapse | confirmed | 摘要逐字:"demonstrate that accumulating the successive generations of synthetic data alongside the original real data avoids model collapse" |
| 7 | "uh-oh moment" 句 | confirmed | "we observe AZR with Llama3.1-8b occasionally produces concerning chains of thought, we term the 'uh-oh moment'";正文 "We refer to this as the 'uh-oh moment' and encourage future work to further investigate its potential implications." |
| 7 | 零外部数据整体 SOTA 句 | confirmed | 摘要:"Despite being trained entirely without external data, AZR achieves overall SOTA performance on coding and mathematical reasoning tasks, outperforming existing zero-setting models that rely on tens of thousands of in-domain human-curated examples."(限定:正文细节是 coding 新 SOTA、math 具竞争力、7B 类超先前最佳 1.8 分) |
| 8 | monkey patching 机制句 | confirmed | "the agent is able to retrieve its current code in the runtime memory and modify it by monkey patching (Bimal, 2012), which dynamically modifies classes or modules during execution" |
| 8 | 全演化约 $15 | confirmed | "For a complete evolutionary process (where the Gödel Agent performs 30 recursive self-improvements) across the DROP, MGSM, MMLU, and GPQA datasets, the cost is approximately $15. This is significantly lower than the $300 required by Meta Agent Search." |
| 9 | GEPA outperforms GRPO by 10% on average + up to 35x fewer rollouts | **wrong** | 当前默认版 v2(2026-02-14, ICLR 2026 Oral)摘要:"Across six tasks, GEPA outperforms GRPO by 6% on average and by up to 20%, while using up to 35x fewer rollouts"。"10% on average" 只在 v1:"Across four tasks, GEPA outperforms GRPO by 10% on average and by up to 20%..."(四任务→六任务、10%→6%);"up to 35x fewer rollouts" 两版均在 |
| 10 | Reflexion HumanEval 91% pass@1 超 GPT-4 80% | confirmed | "Reflexion achieves a 91% pass@1 accuracy on the HumanEval coding benchmark, surpassing the previous state-of-the-art GPT-4 that achieves 80%" |
| 11 | 对 GPT4-Turbo 胜率 9.94%/15.38%/20.44% | confirmed | "training iterations yield improved win rates, in this case over GPT4-Turbo, from 9.94% in Iteration 1, to 15.38% in Iteration 2, to 20.44% in Iteration 3"(AlpacaEval 胜率表) |
| 12 | Voyager 3.3× 独有物品、15.3× 科技树 | nuance | 摘要原句:"It obtains 3.3x more unique items, travels 2.3x longer distances, and unlocks key tech tree milestones up to 15.3x faster than prior SOTA." 3.3× unique items 逐字;但 15.3× 是"解锁科技树关键里程碑最多快 15.3 倍"(up to 15.3x faster),不是"科技树多 15.3×" |
| 13 | SRWM ICML 2022 | confirmed | abs 页 Comments: "Accepted to ICML 2022";论文提出 "a scalable self-referential WM (SRWM)" |
| 13 | "few if any practical studies" | confirmed | "While NN architectures potentially capable of implementing such behaviour have been proposed since the '90s, there have been few if any practical studies." |
| 14 | 算法进步 ~8 个月翻倍(95% CI 约 5-14 个月) | confirmed | 摘要:"the compute required to reach a set performance threshold has halved approximately every 8 months, with a 95% confidence interval of around 5 to 14 months, substantially faster than hardware gains per Moore's Law";3.1 节标题 "Models require 2× less compute roughly every eight months";首选模型中位 8.4 个月、CI 4.5-14.3 个月(措辞是"所需算力减半",即有效算力翻倍) |

总结:confirmed 12/14,需改稿 2 条:#9 GEPA——若引当前 v2 摘要应写 "by 6% on average"(六任务),10%/四任务是 v1 旧措辞,成稿需改数字或明确标 v1;#12 Voyager——"15.3×" 应表述为"解锁科技树关键里程碑最多快 15.3 倍(up to 15.3x faster)"。
