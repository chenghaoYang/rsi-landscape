# 方法论(Methodology)

本调研由多智能体深度调研流程完成:一个主控(lead)加多个并行子代理工人,工人默认继承会话模型(GLM-5.3)。流程分六步,全程留痕。

## 1. R0:反向词表(不搜索)

从任务 brief 反向生成本领域词表:52 个对象词、7 个问题轴、6 条分类对立轴(见 [vocab.md](vocab.md)),同时建立 27 实体 × 8 维度的网格骨架([grid.md](grid.md))。作用:让后续并行工人的问题串互不重叠、缺口可定位。

## 2. R1:八路并行扩展

8 个工人各负责一个区,互不重叠:

| 工人 | 覆盖区 | claims |
|---|---|---|
| w1-rsi-origins | 定义、谱系(Good 1965→Gödel machine→AI-GAs)、分层框架、术语之争 | 32 |
| w2-shallow-loop | 浅层:Self-Refine/Reflexion、prompt 自优化、记忆与技能库 | 27 |
| w3-scaffold-evolution | 中层:ADAS/AFlow/DGM/Gödel Agent/AlphaEvolve/FunSearch | 25 |
| w4-training-loop | 深层:Self-Instruct→STaR→Self-Rewarding→SPIN→Absolute Zero→SEAL、collapse | 27 |
| w5-theory-takeoff | 理论:Gödel machine/SRWM/FOOM/AI 2027/算力约束 | 25 |
| w6-frontier-2026 | 前沿:METR/RE-Bench/MLE-bench/AI Scientist/产业声称/政策阈值 | 25 |
| w7-safety-evals | 安全:objective hacking/评测觉察/scheming/自复制/对齐侧递归 | 29 |
| w8-scout | 侦察:社区分层说法、代表系统频率、争议双方、新术语 | 17 |

小计 207 条。工人纪律:每条 claim 必须带来源 URL + 页面英文原句(逐字)+ 来源类型;conflicts/gaps/leads 必填。

## 3. 收束

格式 lint(脚本校验 src/quote 完整性)→ 词表更新 → 27×8 网格填格 → 10 项结构性冲突显式裁决(裁决记录在 [grid.md](grid.md))→ 报告 r1 版。

## 4. R2:五路定向补深

针对 R1 的缺口与冲突派定向简报:

| 工人 | 任务 | claims |
|---|---|---|
| r2-sjtu-taxonomy | SJTU 综述全文逐字(curl+pdftotext 绕过 HTML 截断):六级名/判据/三问/代表系统/structural vs effective L5;另补两篇 2026-09 分层综述 | 23 |
| r2-anthropic-2026 | Anthropic《When AI builds itself》与《Measuring pace of AI development》全文+TIME/Tom's Hardware 交叉+数字溯源 | 25 |
| r2-skeptics | 反方完整引语:MIT TR shadow evaluation/CACM 七人/Dwarkesh rapid-fire/weco AIDE² 限定/Economics of RSI | 22 |
| r2-thresholds | 三家阈值 PDF 原文逐字:OpenAI PF v2 High/Critical、GDM FSF 3.1 ML R&D CCL、Anthropic RSP v3.1 操作化 | 18 |
| r2-dgm-pdf | DGM 论文 v3 附录 H 逐字(objective hacking 案例)+ ablation Table 1 + Gödel machine 对比段 | 14 |

小计 102 条,累计 309 条。R2 闭合全部 10 项冲突,并修正 5 处 R1 勘误(如 Anthropic 限定句原句、"26%" 的真实出处、491 篇的位置)。

## 5. 终审:回源核验

3 个独立核验通道(arXiv 论文簇 / 官方页簇 / 媒体社区簇)重新打开原始页面逐条判定,判定值 confirmed / wrong / not-on-page / nuance / confirmed-absent:

- arXiv 簇:14 组,12 confirmed,1 wrong(GEPA v2 摘要是 "6% on average",10% 仅 v1——已改稿),1 nuance(Voyager 15.3× 应为 "up to 15.3x faster");
- 官方页簇:30 组(含 2 个否定主张),28 confirmed + 2 confirmed-absent(《When AI builds itself》页面无 "we don't consider ourselves" 字样、无 "26%"),0 需改稿;
- 媒体簇:30 组,27 confirmed,1 nuance 需改稿(Anthropic 报告首发日期的逐字依据应挂 Tom's Hardware 6-09 续篇/VentureBeat 时间戳——已改)。

判定表:[evidence/audit-arxiv.md](evidence/audit-arxiv.md) · [evidence/audit-official.md](evidence/audit-official.md) · [evidence/audit-media.md](evidence/audit-media.md);汇总与改稿记录:[audit.md](audit.md)。

## 6. 分层成稿

report.md(叙事,≤2 万字符,一屏看懂→词表→分层→矩阵→逐层做法→坑→置信度)→ atlas.md(字段对照,不做省略)→ details/(三个专题页,每页 ≤4 千字符)。三层去重:字段级只在 atlas、叙事只在 details、report 概括加指针。

## 残余缺口(透明起见,不阻塞结论)

- SJTU 综述 Table 2(cross-level map)与 §4 应用章未逐字抄全;
- GPT-5.1 system card 的 self-improvement 评测原句未一手核验(仅次级报道),故 "GPT-5.2 首次发布该类数值评测" 存疑;
- Anthropic RSP v2.2 编号阈值族(AI R&D-4/5)完整原文未取(仅有 changelog 佐证);
- 26% 的 2026-02 基线(<1%)仅见图表,文本无句;
- weco 技术报告(arXiv 2609.26457)未读。

## 复现说明

工具链要求:任意外层能(a)并行 spawn 子代理并回传结构化笔记,(b)工人可 WebFetch/WebSearch。流程规范(词表驱动、分轮并行、收束纪律、终审回源)与配套脚本(notes_lint / roundstat)在作者的 parallel-search-skill 项目中。单人工(不开子代理)也可执行同一流程,只是 R1/R2 变成顺序多轮。
