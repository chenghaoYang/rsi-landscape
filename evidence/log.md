# log.md — RSI(Recursive Self-Improvement)调研日志

## 2026-09-28 R0(主题重定向)

- 用户纠正:RSI = Recursive Self-Improvement(递归自我改进,AI agent 语境),非金融 Relative Strength Index。旧工作区(金融 RSI 完整调研至 R2)整体归档到 `deep-search/rsi-trading/`,本目录从头开始。
- 写 `brief.md`:三疑点 = ①RSI 从简单到复杂分几层、每层是什么;②每层对 AI agent 的具体做法/机制;③哪些已实现有实证、哪些还是概念/畅想。
- 反向词表(R0 不搜索)→ `vocab.md`:34 个对象词、7 个问题词、6 条对立轴,全 ⚠ 待核。
- taxonomy 预判(待 R1 检验):至少三种分层法并存——按修改对象(prompt→记忆→工作流→权重→硬件)、按闭环自主度、按"理论 vs 已实现"。疑点 1 的答案大概率是"几种主流分法对照"而非唯一答案。

## R1 计划(8 工人,Explore 类型,问题串见各 Agent 派发 prompt)

| 工人 | 覆盖区 |
|---|---|
| w1-rsi-origins | 定义、谱系(Good/seed AI/Gödel machine/AIGA)、多种分层框架、术语之争 |
| w2-shallow-loop | 浅层:Self-Refine/Reflexion、prompt 自优化(OPRO/DSPy/GEPA)、记忆与技能库(Voyager/MemGPT) |
| w3-scaffold-evolution | 中层:ADAS/AFlow/DGM/Gödel Agent/AlphaEvolve——agent 自改工作流与代码 |
| w4-training-loop | 深层:Self-Instruct/STaR/Self-Rewarding/SPIN/Absolute Zero、model collapse、RLVR |
| w5-theory-takeoff | 理论:Gödel machine 细节、SRWM 现状、FOOM/takeoff 辩论、AI 2027、算力约束 |
| w6-frontier-2026 | 前沿:METR time horizon/RE-Bench、MLE-bench、AI Scientist/co-scientist、产业自循环声称、政策阈值 |
| w7-safety-evals | 安全:DGM 造假、evaluation awareness、scheming、自我复制、对齐侧递归、治理触发 |
| w8-scout | 侦察:2025-2026 社区分层说法、争议点、官方叫法回报 |

- 工人落盘:优先 Bash heredoc 写 `notes/<name>.md`;被只读沙箱拒绝则全文随返回消息带回,lead 代存。
- 已知坑(上轮踩过):general-purpose 子代理模型被钉死在已下线模型 → 一律用 Explore。

## 2026-09-28 R1 派发与收束

- 派发 8 工人(Explore):首轮 w1/w4/w8 三个撞限流(1302),按"失败重派一次"规则重派成功;8/8 回收。
- 沙箱全部只读(heredoc 被系统禁),8 份笔记均由 lead 代存。
- notes_lint:207 claims(official 46 / secondary 161),修 12 条(5 条 quote 引号未放开头、7 条 src 裸域名)后 0 missing;25 conflicts / 46 gaps / 87 leads。
- 收束:.vocab.md 更新(52 词,新增 STOP/Dream-RSI/meta-evolution/bounded-open-ended/RSI substrate/maximalist-prosaic/uh-oh moment 等);grid.md 27 实体×8 维(93% 解析);report.md r1 版 9153 字符(预算 20000),加 [1]-[16] 编号引用,roundstat 干净。
- 10 处 ⚔ 中 8 处已就地裁决(写进 grid ⚔ 清单),2 处结构性(分层 taxonomy 对照呈现;RSI 是否已发生三向呈现)。
- R2 定向缺口(5 简报):①SJTU 综述后半全文(L4/L5 逐字判据+代表系统,HTML 截断于 §3.3.4)+ 2607.07663 两轴档位名;②Anthropic《When AI builds itself》全文+五阶段+TIME/产业声称取证;③反方阵营完整引语(MIT TR/CACM/Schulman)+weco AIDE² 可信度;④三实验室阈值原文(OpenAI PF v2 self-improvement High/Critical、Anthropic RSP v3.x、GDM FSF v3.1 ML R&D CCL);⑤DGM PDF Appendix H/I+ablation 基线。

## 2026-09-28 R2 派发与收束

- 5 工人全部返回(skeptics 自行写盘成功——curl 绕 403/r.jina.ai 绕 Cloudflare;其余 4 份 lead 代存)。
- 关键突破:SJTU PDF 用 curl+pdftotext 流式全文解析(绕过所有 HTML 镜像在 §3.3.4 截断),拿到六级逐字名/判据/三问/八方向/structural vs effective L5;OpenAI PF v2 与 GDM FSF 3.1、Anthropic RSP v3.1 阈值原文逐字到手。
- 裁决 10 项 ⚔ 全闭合+5 项 R1 勘误(Anthropic 限定句原句更正;26%/3 万 agent 另出自 9-17 报告;491 在附录图 18;Appendix H 绑定 v3;GPT-5.2"首发数值评测"存疑)。详见 grid R2 裁决记录。
- lint:R2 102 claims,修 53 处(代存"src: 同上"展开为 URL、quote 引号前置)后 0 missing。
- report.md r2 版 13078 字符:引用编号系统改为 [1]-[21] 并在文末给出编号↔笔记文件映射;§0 改以 OpenAI Critical 阈值作为"真 RSI"分界;§4 增产业现状(Anthropic 两报告/Sakana/OpenAI/政策卡点);§5 增反方最硬证据(shadow evaluation);§6 未决表全面更新。roundstat 干净(93% 解析)。
- 终审核验清单见 audit 派发(3 簇:arXiv / 官方页 / 媒体社区,含 2 个"不存在"型否定主张)。

## 2026-09-28 终审与分层成稿

- 3 个核验工人(audit-arxiv / audit-official / audit-media)回原页逐条判定:62 组判定,60 confirmed(含 2 个 confirmed-absent:《When AI builds itself》无 "we don't consider ourselves"、无 "26%"),wrong 仅 1,not-on-page 0。
- 按判定改稿 3 处:GEPA 数字口径(v2 六任务 6% vs v1 四任务 10%)、自纠错退化数字标"仅第一轮"、Anthropic 报告首发日期补交叉来源(VentureBeat 时间戳 + Tom's Hardware 6-09 续篇)。nuance 记 audit.md 不改正文。
- 分层成稿:report.md 终稿 13243 字符(≤20000,快照 r3-final);atlas.md 13331 字符(≤40000:分层框架逐字对照/代表系统字段全表/产业政策字段册/安全字段册/谱系时间线);details/ 3 页(sjtu-ladder 3102、dgm-hacking-case 3401、frontier-2026 压缩后 ≤4000)。roundstat 全绿。
- harness.md 补 ZCode 实战坑(general-purpose 被钉死已下线模型→用 Explore;只读沙箱双预案;代存"src: 同上"要展开;1302 限流重派)。
- 交付:deep-search/rsi/{report.md, atlas.md, details/, grid.md, vocab.md, audit.md, log.md, notes/×16, snapshots/×3}。旧主题(金融 RSI)完整归档于 deep-search/rsi-trading/。

