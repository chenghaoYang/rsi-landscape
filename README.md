# RSI Landscape 2026 · 递归自我改进(Recursive Self-Improvement)全景调研

> English: A fully-sourced landscape study of **Recursive Self-Improvement (RSI)** in AI agents — how it is layered, what each layer concretely does, and what is empirically real versus still conceptual. Snapshot of **2026-09-28**. 正文中文；证据笔记包含原句、摘要转述与检索线索，须按条目类型阅读。

## 这是什么

2026 年,RSI 从科幻词汇变成了有 35 人综述、有公司专门部门(Sakana RSI Lab)、有官方评测类目(OpenAI "AI Self-Improvement")、有政策触发器(Anthropic RSP / GDM FSF)的工作领域。本调研用多智能体深度调研流程完成,特点:

- **16 份证据笔记 / 309 条 claims**——保留来源、引文与检索记录；不将摘要或线索当作逐字引文,见 [evidence/](evidence/);
- **终审回源核验**——3 个独立核验通道的判定表共 92 行:85 confirmed、2 confirmed-absent、2 confirmed(nuance)、2 nuance、1 wrong。按判定行统计,不混用文献组数;已确认勘误同步到成稿,见 [audit.md](audit.md);
- **分层成稿**——[report.md](report.md) 为完整成稿，字段对照册与专题页供按需查证。

## 三个核心问题(速览)

1. **RSI 分几层?** 没有唯一分层,最系统的是 SJTU 综述的六级 **B0→L5**:任务内改进 → 改进执行 → 改进策略 → 经验获取 → 环境适应 → **递归继承(改"改进机制本身")**;另有"修改对象轴"与"有界 vs 开放 × 闭环三档"两种主流分法,三家逐字对照见 [atlas.md](atlas.md) §1。
2. **每层对 AI agent 的具体做法?** 每层都有已跑通的系统与数字:浅层改上下文/记忆/prompt(Reflexion、GEPA、Voyager),中层改工作流与代码(**DGM 自改自身代码 SWE-bench 20%→50%**,ADAS、AFlow、AlphaEvolve),深层改数据与权重(STaR、Self-Rewarding、Absolute Zero 零数据自博弈、SEAL),元级理论为主(Gödel machine 从未跑通)+ 雏形(weco AIDE²)。
3. **哪些有实证、哪些是概念?** 分界线在 2026 年有了官方数值定义——OpenAI Preparedness 把"真 RSI"列为 **Critical 阈值**(超人研究科学家 agent,或 1/5 墙钟时间持续数月产出代际模型跃迁),三家实验室均未触发;但 **prosaic RSI 已发生**:Claude 写了 Anthropic **>80% 的合入代码**、"leads" **26%** 的自家 AI 研发(约 3 万 agent 并行)。反方最硬证据:shadow evaluation 实验——Opus 4.8 六天攻两篇未发表 NeurIPS 研究问题,双遭原作者拒稿。快的是编码,不是(还)研究本身。

## 阅读路线

| 想要 | 去哪 |
|---|---|
| 15 分钟看懂 | [report.md](report.md) §0–§2 |
| 查某个系统 / 数字 / 阈值原文 | [atlas.md](atlas.md)(字段对照册) |
| 深读三个专题 | [details/](details/) — [SJTU 六级逐字判据](details/sjtu-ladder.md) · [DGM objective-hacking 案例复盘](details/dgm-hacking-case.md) · [2026 产业引语底册](details/frontier-2026.md) |
| 核对任何一句话 | [evidence/](evidence/)(309 条 claims 与来源记录)+ [audit.md](audit.md)(核验判定表) |
| 全景网格(27 实体 × 8 维) | [grid.md](grid.md) · 术语表 [vocab.md](vocab.md) |

## 方法与可信度

- 方法、证据纪律与残余缺口见 [METHODOLOGY.md](METHODOLOGY.md)；数字口径陷阱见 report §5。
- 时效声明:2026-09-28 快照,这个领域以周为单位变化。

## License

[CC BY 4.0](LICENSE)。引用请注明本仓库;商业内容(论文/报告原文)版权归原作者,本仓库仅作逐字短引与出处指引。
