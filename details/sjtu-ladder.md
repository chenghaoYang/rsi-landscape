# SJTU 六级阶梯深读(《The Last AI Built by Humans》)

> arXiv 2609.11873(v1 2026-09-10,v3 2026-09-22),Yi Duan 等 35 人,基于 491 篇文献(附录图 18)。终审:audit-arxiv 逐字 confirmed。这是疑点1"分几层"的锚点框架。

## 刻度化三问(每级都回答)

1. "Where does the loop close?"——决定表面的改进是否真的回到系统本身。
2. "What is updated and inherited?"——决定改进的持久载体。
3. "Which decisions remain external?"——决定改进过程的多少权威已从人转移到 AI。

## 六级阶梯

**B0 In-Task AI Improvement**(任务内改进)。判据:"output change without persistent system change"——只改输出、不留持久状态,"We therefore treat B0 as a non-RSI reference level"。代表:Self-Refine、Reflexion、Tree of Thoughts(单次使用即 B0;Reflexion 的记忆缓冲若跨任务复用则上探 L1)。

**L1 Autonomy over Improvement Execution**(改进执行自主)。判据:"AI system executes a human-defined improvement procedure whose accepted results are retained and reused in later tasks or improvement rounds."——人定改什么/怎么改/何为成功,AI 只跑流程,但**被接受的结果保留复用**(这一条使它越过 B0)。代表:FineWeb-Edu、Data-Juicer、NeMo Curator 等数据过滤/合成流水线。

**L2 Autonomy over Improvement Strategies**(改进策略自主)。判据:"the AI system uses evaluation feedback to choose which improvement intervention to attempt next, rather than merely executing a prescribed update."——AI 看评测反馈决定下一个干预,但目标、任务边界、验收标准仍由人定。代表:GEPA、Promptbreeder、ADAS、AFlow、AgentSquare、AutoKernel。这是当前工业界最活跃的一层。

**L3 Autonomy over Future Learning Experience**(学习信号/经验获取自主)。判据:"The system also determines the experience needed for its next improvement round."——系统还自己决定下一轮用什么经验(自出题、自造课程、自采数据)。代表:Voyager(自动课程)、Absolute Zero(自出题+自验证)、SIMA 2、R-Zero。

**L4 Autonomy in Deployment and Environmental Adaptation**(环境适应自主)。判据:"The improvement loop uses deployment interaction to revise persistent system state under external acceptance and governance rules."——从部署交互中持续修订持久状态(记忆/技能/权重),但接受与治理规则来自外部。代表:ReasoningBank、ACE、Dynamic Cheatsheet。已知失败:activation/execution 双失败与 Library Drift。

**L5 From Environmental Adaptation to Meta-Improvement**(简写 recursive inheritance,递归继承)。判据:"The system persistently revises a mechanism that governs subsequent improvement, such as an improver, verifier, or successor-generation procedure."——修订"支配后续改进的机制"。代表:STOP、Gödel Agent、Darwin Gödel Machine、RQGM、AIDE2。综述结论:"Finding: L5 makes the improvement procedure inheritable."

## 最重要的警告:structural ≠ effective L5

综述 §6 逐字:"structural L5 … demonstrates that an AI-directed change persists and controls a later improvement round";"effective L5 … demonstrates that the revised mechanism produces or selects better successors under comparable budgets and independent assessment." 现有 L5 系统几乎都只证明了前者:AIDE2 进化 harness 装进外环后"did not establish a statistically significant efficiency advantage"。**即:结构递归已被多次实现,有效递归尚无统计显著的一手证据**——这是"真 RSI 尚未达成"的最佳学术引句。

## 评估与其他要点

- 度量:HCI(Headroom-Closed Index),分量 H_mbh=100×(s̄−F_b,0)/(100−F_b,0),F_b,0=基准入榜年份 90 分位分;实证 393 条模型-基准观测(2023–2026-09,十个能力域)。
- 三大挑战(§1.3):安全继承(Gödel Agent 试验低于基线)、自主性归属(区分 AI 决策与固定搜索流程)、可靠验证(random-seed cherry-picking、test-label extraction 实录)。
- 八个研究方向(§6):跨组件诊断与协同改进;学习者条件化经验获取;持久状态管理与可靠复用;受治理适应;改进机制的可信演化;长程继承评估;资源感知改进与人机协作;跨轮继承的可复现基础设施。
- 使用注意:层级名在摘要(五段 autonomy 叙述)与 §3(B0/L1-L5 编号)两套并存;L5 有双名(标题名 vs 简写名);跨 taxonomy 归属不同(DGM 在 2607.07663 里归"部署期自演化"而非 L5)——引用时注明出处位置。
