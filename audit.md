# audit.md — 终审核验汇总(2026-09-28)

> 三个核验工人(audit-arxiv / audit-official / audit-media)回原始页面逐条判定,判定值:confirmed / wrong / not-on-page / nuance / confirmed-absent。完整判定表见 evidence/audit-*.md。

## 结果

| 簇 | 核对数 | confirmed | wrong | nuance | 需改稿 |
|---|---|---|---|---|---|
| arXiv 论文 | 14 组 | 12 | 1(GEPA) | 1(Voyager) | 2 |
| 官方页(实验室/PDF) | 30(含 2 否定主张) | 28 + 2 confirmed-absent | 0 | 0 | 0 |
| 媒体/社区 | 30 | 27 | 0 | 3 | 1 |

## 已执行的改稿(3 处,report.md r3)

1. **GEPA 数字口径**(audit-arxiv #9):v2(ICLR 2026 Oral)摘要是 "6% on average"(六任务),10% 仅 v1(四任务)→ 稿中改为"超 GRPO(v1 四任务口径 10%,v2 六任务口径 6%)"。
2. **自纠错退化数字轮次**(audit-arxiv #4):GPT-3.5 CommonSenseQA 75.8→38.1 是 round 1(round 2 为 41.8)→ 补"仅第一轮"。
3. **Anthropic 报告首发日期依据**(audit-media #7a):6-05 Tom's Hardware 主报道未写标题与 6-04;首发日期依据改为 VentureBeat publishedTime 2026-06-04 + Tom's Hardware 6-09 续篇逐字句 → 稿中 §4 补交叉来源注。

## 记入细节页的 nuance(不改正文)

- Voyager "15.3×" 应表述为"解锁科技树关键里程碑最多快 15.3 倍(up to 15.3x faster)"(正文未引此数,细节页引用时注意)。
- Anthropic 3 万 agent 的限定语:"in our most-used internal platform...These measurements cover this platform only"。
- 59%/35% 归因:59%=模型对人类,35%=人类对人类。
- 26% 图表基线(2026-02 <1%)仅见于图,文本无句。
- METR TH1.1:Opus 4.5=320 分钟为 TH1.1 点估计;页内另有 270/289 分钟基建对比表勿混用。
- HN 15%/9% 弹性数字出自 zuzuen_1 评论转引论文,基于自报调查数据。
- CACM Kale 引句前半是否定句("not separable on a benchmark"),勿截半。
- Dwarkesh "crazy RSI" 为双重否定句式,引用需带全。
- OpenAI Critical 阈值 "superhuman research scientist agent"(官方 PDF 无连字符,r2 笔记曾写 research-scientist)。

## 否定主张核验

- 《When AI builds itself》页面无 "we don't consider ourselves to have..." 字样 → **confirmed-absent**(全文检索 0 命中)。
- 该页面无 "26%"(有 51%/64%/76%/20%)→ **confirmed-absent**(26% 出自另一份 9-17 报告)。

## 终审结论

62 组判定,60 confirmed(含 2 confirmed-absent),wrong 仅 1(已在稿中修正),全部需改稿项已落实。报告 r3 为终稿。
