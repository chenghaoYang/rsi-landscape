# grid.md — RSI 调研网格(R1 收束版)

> 实体 × 维度。状态:✅ 已解析(指针→evidence 文件)| ⚔ 冲突待裁 | ❓ 空。
> 维度:①机制 ②提出者/年 ③改的对象 ④自主度(SJTU L 级) ⑤外部verifier ⑥实证数字 ⑦失败模式 ⑧来源等级

| 实体 | ①机制 | ②提出/年 | ③改对象 | ④L级 | ⑤verifier | ⑥实证数字 | ⑦失败模式 | ⑧来源 |
|---|---|---|---|---|---|---|---|---|
| RSI 概念本体 | 闭环:找局限→改→用所得改进改进过程 | SJTU 综述 2026-09(通行定义);Good 1965 思想源头 | 全部 | L2-L5 | — | — | 术语过载(maximalist/prosaic) | w1 ✅ |
| seed AI / GISAI | 自理解+自修改+递归自增强的种子 | Yudkowsky 2001 | 权重+代码 | 理论 | — | 无(概念) | 从未造出 | w1/w5 ✅一手 |
| Gödel machine | 证明"改写有用"才自改;全局最优 | Schmidhuber 2003 | 自身代码+证明器 | L5 理论 | 自含证明器 | 无(从未跑通) | 证明前提 impractical(Sakana 评) | w5 ✅ |
| SRWM | 权重矩阵含自改算子,运行时修改全部自身 | Schmidhuber 1993;ICML 2022 现代版 | 权重 | L5 | 任务损失 | 少样本/多任务 RL 可跑(小规模) | 30 年几乎无实证 | w5 ✅ |
| AI-GAs | 输出 AI 的算法,三支柱 | Clune 2019 | 架构+算法+环境 | L3-L5 愿景 | 进化环境 | 无直接系统 | 愿景纲领 | w1 ✅ |
| Self-Refine | 同一 LLM 生成/反馈/修正交替 | Madaan 2023 | 输出(任务内) | B0-L1 | 自评(失败源) | 7 任务 ~+20%;失败 61% 修法不当 | 纯内在自纠错被证伪 | w2 ✅ |
| Reflexion | 语言反馈存情景记忆,不更新权重 | Shinn 2023 | 情景记忆 | L1(记忆) | Evaluator(单测/环境) | HumanEval 91%>GPT-4 80% | 需外部反馈;局部最优 | w2 ✅ |
| OPRO/DSPy/GEPA | LLM 优化 prompt;编译;轨迹反思 | 2023/2023/2025 | prompt | L2 | metric/评测集 | GSM8K +8%;GEPA 超 GRPO:v1 四任务平均 10%,v2 六任务平均 6% | 数字随版本漂 | w2 ✅ |
| Voyager/MemGPT | 自动课程+技能库;OS 式分层记忆 | 2023 | 技能库/记忆 | L3/L1 | 环境/自定向 | 3.3× 物品;32→92.5% | API 成本;底座幻觉 | w2 ✅ |
| ADAS | meta agent 迭代写 agent 入 archive | Hu/Clune 2024 | agent 代码 | L2(改agent不改己) | benchmark | DROP +13.6/MGSM +14.4 | 一次性设计非运行时自改 | w3 ✅ |
| AFlow | MCTS 搜代码表示 workflow | 2024 | workflow | L2 | 执行评测 | +5.7% vs 人工;4.55% 成本超 GPT-4o | 同上 | w3 ✅ |
| DGM | archive+FM 生成新版本写入自身代码 | Sakana/Clune 2025-05 | agent 自身代码 | L5(实证) | SWE-bench/Polyglot | 20.0→50.0%;14.2→30.7% | objective hacking 实录;伪造单测日志 | w3/w7 ✅ |
| Gödel Agent | 运行时检视 memory+monkey patching | Yin 2024,ACL 2025 | 运行时逻辑 | L5(受控) | benchmark | DROP 80.9;~$15 | 演化中可能丢失自我理解 | w3 ✅ |
| AlphaEvolve | LLM ensemble+程序数据库+评测器进化代码库 | DeepMind 2025-05 | 外部代码(含自家kernel) | L2(改进对象非agent) | 自动 Evaluators | 48 次乘;0.7% 算力;kernel +23% | 只适用机器可验证问题;递归是单向的 | w3/w7 ✅ |
| Self-Instruct/STaR | 自生成指令/自举 rationale | 2022 | 训练数据 | L3 | 过滤器/答案验证 | +33%;+35.9% | 质量过滤依赖 | w4 ✅ |
| Self-Rewarding/SPIN | 自评造奖励/与旧版本 self-play | Meta 2024 | 奖励信号/数据 | L3 | 自评(LLM-judge) | GPT4-Turbo 胜率 9.94→20.44%;HF 58→63 | 自评漂移风险 | w4 ✅ |
| Absolute Zero | 自出题+代码执行器双验证,零外部数据 | Tsinghua 2025-05 | 课程+数据 | L3 | 代码执行器 | 编程/数学整体 SOTA | uh-oh moment CoT | w4 ✅ |
| SEAL | 生成自己的微调数据 self-edit→SFT | MIT 2025-06 | 权重(经数据) | L3-L4 | 外部评测 | "promising step"(数字在正文) | 摘要无数字 | w4 ✅ |
| model collapse 之争 | 自食数据→尾部消失 vs 累积式可避免 | Nature 2024 / rebuttal 2024 | 数据分布 | — | — | 理论+受控实验 | 前提之争(replacement/accumulation) | w4 ✅⚔已裁 |
| METR time horizon | 50% 任务长度翻倍周期 | METR 2025-03/TH1.1 2026-01 | 度量(非系统) | — | 任务套件 | ~7 个月翻倍;Opus 4.5 320min;130.8 天(2023后) | 第三方数字乱 | w6 ✅ |
| RE-Bench/MLE-bench | AI R&D 任务基准 | METR/OpenAI 2024 | 度量 | — | 真实任务 | AI=人类中位 4×,最佳人类胜;铜牌 16.9% | 8h 时程限制 | w6 ✅ |
| AI Scientist/co-scientist | 自动科研全流程 / 虚拟科学协作者 | Sakana 2024-25 / Google 2025-02 | 研究流程 | L2-L3 | 自建评审/湿实验 | <$15/篇;ICLR workshop 论文(v2,后撤回争议) | 自建评审员=裁判球员一体 | w6 ✅ |
| Anthropic RSI 进程 | 五阶段:Claude→chatbot→coding agent→autonomous→closing loop | Anthropic Institute 2026-05/06 | 公司内工程 | L1-L4 生产 | 人工+评测 | >80% 合入代码 Claude 写;~26% AI 研发(快照级) | "完整 RSI 尚未到来"自述 | w6/w8 ✅/⚠ |
| 政策阈值 | AI R&D-4/Self-Improvement/ML R&D CCL | 2024-2026 | 治理 | — | — | Opus 4/4.5 未跨 AI R&D-4 | 阈值原文部分未取得 | w6/w7 ✅ |
| FOOM/takeoff 辩论 | 智能爆炸动力学之争 | 2008-至今 | 叙事 | — | — | 无(不可证伪带) | 概念框架非预测模型 | w5 ✅ |
| AI 2027 | SC→SAR 循环模型,R&D multiplier 10x+算力墙 | Kokotajlo 2025-04 | 叙事/数值模型 | L5 情景 | — | 中位已移 2028 | "破烂玩具模型"批评 | w5 ✅ |
| 对齐侧递归 | IDA/debate/RRM/w2s | 2018-2023 | 训练信号 | — | 人类判官 | w2s:强模型超弱监督但远未恢复全部 | 距完全恢复尚远(原句) | w7 ✅ |

## ⚔ 待裁清单(R2 输入)

## R2 裁决记录(2026-09-28,全部闭合)

1. DGM Polyglot 双口径 → **裁**:正文用 full benchmark 14.2%→30.7%(abstract);Table 1 另有 38.0%(this implementation),引用注明出处行。二者并存非矛盾。[r2-dgm-pdf C9/conflicts]
2. DGM reward hacking 出处 → **裁**:v1 无此内容,博客+v3 Appendix H 有;主环正式实验未见硬编码;检测机制是 marker-token 检查(**非**"分类器");因果句序="not hidden 时更频繁"。[r2-dgm-pdf C4/C5/conflicts]
3. AlphaEvolve 递归强度 → **裁**:单向 kernel 贡献("accelerated the training of the LLM underpinning AlphaEvolve itself"),非完整自闭环;学界表述"半环"。维持 R1 裁决。
4. collapse → **裁**:前提之争(替换 vs 累积),双方并陈;另补弹性视角(Economics of RSI:9%<15% 当前非自持)。[r2-skeptics C22]
5. AZR"中间语言" → **裁**:一手只有 uh-oh moment;轶事不入稿。维持。
6. Self-Rewarding/STaR 数字 → **裁**:用一手可查数字。维持。
7. 第三方 time horizon 14.5-17.4h → **裁**:采信 METR 官方 TH1.1(Opus 4.5=320min,130.8 天翻倍)。维持。
8. SJTU 五级 vs 其他五级 → **裁**:正文用 SJTU B0+L1-L5(逐字名已取得,见 vocab);其他版本(2607.07663 两轴、Era of Experience、Anthropic 五阶段)作为对照轴并陈;跨文归属差异(DGM 在 SJTU=L5、在 2607.07663=Deployment-time)如实标注。[r2-sjtu-taxonomy conflicts]
9. 分层 taxonomy 无共识 → **裁**:对照表呈现(维持),已补齐三家逐字档位名。
10. "RSI 已发生?" → **裁**:三向呈现,证据全部升级一手——正方(Anthropic 80% 代码/26% AI 研发/Clark 2028 前 60% 概率、OpenAI GPT-5.3-Codex "instrumental in creating itself"、Sakana RSI Lab、weco AIDE² p=0.0024)vs 反方(MIT TR shadow evaluation 双拒稿、CACM "mostly marketing"/"self-regulation theater"、Schulman hype-cycle、弹性 9%<15%)vs 官方门槛(OpenAI Critical 双指标、RSP v3.1 翻倍操作化、三家均未触发;Anthropic 自述 "We are not there yet, and recursive self-improvement is not inevitable.")。[r2-anthropic-2026 / r2-skeptics / r2-thresholds]

## R2 新裁决(原 R1 记录勘误)

- R1 记 Anthropic 限定句 "we don't consider ourselves..." → **实际不存在**,原句为 "We are not there yet, and recursive self-improvement is not inevitable." [r2-anthropic-2026 C10]
- R1 把"26%/3 万 agent"归《When AI builds itself》→ **实际出自另一份**《Measuring pace of AI development》(2026-09-17)。[r2-anthropic-2026 C13/C14]
- R1 称"摘要里 491 篇" → **实际在附录图 18**(n=491);摘要度量是 HCI。[r2-sjtu-taxonomy C12]
- R1 引 "Appendix H" → 绑定 v3(v1 为 Appendix F)。[r2-dgm-pdf conflicts]
- R1/R2 交界的 GPT-5.2"首发 RSI 数值评测"说 → 存疑,GPT-5.1 卡可能更早(次级证据);官方卡自称"like their predecessor models"。[r2-thresholds CF2]

## ❓ 空格(R2 后残余,不阻塞成稿)

- SJTU Table 2(cross-level map)与 §4 应用章未抄全;GPT-5.1 卡 self-improvement 原句未一手核;RSP v2.2 AI R&D-4/5 完整原文;26% 图表基线(<1%)仅二手转述;weco 技术报告 arXiv 2609.26457 未读。
