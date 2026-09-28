# audit-media
checked(实际重开):
- https://time.com/article/2026/08/07/ai-recursive-self-improvement-anthropic-openai (标题 "Inside the Race to Make AI Build Itself",Harry Booth,2026-08-07)
- https://www.technologyreview.com/2026/08/18/1142188/ai-recursive-self-improvement/ (标题 "AI's recursive self-improvement might not come so quickly after all",Michelle Kim,2026-08-18)
- https://cacm.acm.org/news/is-recursive-self-improvement-really-here/ (Logan Kugler,posted Jul 6 2026)
- https://www.dwarkesh.com/p/john-beren-charlie (2026-09-11,Schulman/Millidge/O'Neill)
- https://weco.ai/blog/first-evidence-of-recursive-self-improvement (实际标题 "AIDE²: The First Evidence of Recursive Self-Improvement",2026-07-14)
- https://news.ycombinator.com/item?id=48901224 ("The Economics of Recursive Self-Improvement [pdf]" → elasticity.institute/rsi-paper.pdf)
- https://www.tomshardware.com/tech-industry/artificial-intelligence/anthropic-says-claude-now-writes-more-than-80-percent-of-its-merged-code (6-05 主报道) + https://www.tomshardware.com/tech-industry/artificial-intelligence/anthropic-warns-ai-self-improvement-could-end-in-lost-human-control (6-09 续篇)
- https://venturebeat.com/technology/anthropic-says-80-of-its-new-production-code-is-now-authored-by-claude-how-your-enterprise-can-keep-up

## verdicts

| # | 主张(短语) | 判定 | 证据/正确原句 |
|---|---|---|---|
| 1a | Clark 2028 前 60% | confirmed | "Though he puts the chances of AI improving itself autonomously by 2028 at 60%, he's content with brinkmanship for now."(Jack Clark) |
| 1b | Glaese "from start to finish" | confirmed | GPT-5.3 Codex "was the first to have a significant hand in its own development 'from start to finish,' Amelia Glaese, OpenAI's vice president of research, told TIME"(原句含 "significant hand in";引语本身逐字) |
| 1c | Marcus "strike terror" | confirmed | "'Anthropic is trying to strike terror into everyone's hearts,' wrote AI skeptic Gary Marcus, adding 'all they have really shown is just faster coding.'"(出自其 Substack 帖,TIME 转引) |
| 1d | Kaplan "try all eight" | confirmed | "'Before, I'd have eight ideas and I'd try one of them,' Kaplan told TIME in February. 'Now I ask Claude to just try all eight.'"(eight=他的研究想法) |
| 1e | Orr 悬崖路 75/25 | confirmed | "'I just feel like our margin for error is getting smaller over time. Because we're driving down a cliff road. A mistake will kill you. And now we're driving at 75 instead of 25.'"(Dave Orr,无 "mph" 单位) |
| 1f | Hubinger aligned 证据退化 | confirmed | "'Our ability to produce compelling evidence that our models are aligned is degrading,' Hubinger said."(Evan Hubinger) |
| 1g | Clark 不要求暂停 | confirmed | "'The world needs options, but we're not saying the world must pause or slow down. That's not what the evidence says,' he told TIME in July." |
| 2a | NeurIPS 双拒 6天/$3000/Opus 4.8 | confirmed | "The agents were given six days, $3,000 in Anthropic API credits, a GPU budget…";Claude Opus 4.8 跑 OpenClaw 攻两篇未发表 NeurIPS 2026 论文;"Those authors rejected both papers." |
| 2b | Kapoor "unambiguously bad" | confirmed | "'On the other hand, the agents were unambiguously bad at carrying out the research itself,' says Kapoor." |
| 2c | Clark "rote, formulaic thinking" | confirmed | "…they seem to have a certain property of rote, formulaic thinking that might prevent them [from] being good researchers" |
| 2d | Clark "bearish signal…" | confirmed | He called AI systems' lack of creativity a "bearish signal on short recursive self-improvement timelines." |
| 3a | Codex 发布说明 "instrumental in creating itself" | confirmed | 2026-02-05 发布说明:early versions of the model were "instrumental in creating itself," helping to debug training runs…(注意主体是 "early versions") |
| 3b | Kale "separable on a control diagram" | confirmed | "Genuine recursive self-improvement and sophisticated internal automation are not separable on a benchmark… They are separable on a control diagram."(否定在前,引用时勿截半句) |
| 3c | Ginsberg "mostly marketing" | confirmed(nuance) | 原句:"The capability frontier expansion claim is mostly marketing from frontier labs,"(限定在 capability-frontier-expansion 主张上) |
| 3d | Ginsberg "self-regulation theater" | confirmed | "'Anything less,' he said, 'is self-regulation theater.'" |
| 3e | Strauss 写保护 holdout | confirmed | RSI "should count only when model-led changes produce gains that hold up on independent, write-protected holdout evaluations the model cannot see or edit."(Jacob Strauss, ChaseLabs CTO) |
| 4a | Schulman 循环句 | confirmed | "There's this cycle that keeps repeating where a new model comes out and people are blown away and they're like, 'This is it. This is AGI.' But then they use it a bit, and it starts to feel dumb after a month or so. That cycle just might keep going." |
| 4b | "you still get bottlenecked" | confirmed | "Right now, you don't get explosive growth in capabilities because you still get bottlenecked enough when you're trying to do research and engineering." |
| 4c | 10x uplift 2 年(Schulman) | confirmed | rapid-fire 段,问 10x 研究生产力提升还要多久,Schulman:"I would say two years."(O'Neill 同题答 "Somewhere between 5-10 years?"——注意这是 10x 题,非 ASI 题) |
| 4d | ASI 3-4 年(Schulman)/5-10 年(O'Neill) | confirmed | 终题 "dominates top human experts…basically just ASI?":Schulman "I would say 3-4 years.";O'Neill "I'd say 5 to 10."(Millidge:"I kind of agree on the 5-year range") |
| 4e | Dwarkesh "crazy RSI within 10 years" | confirmed | "by default, I don't see how you don't get some kind of crazy recursive self-improvement within the next 10 years."(双重否定句式,引用需带全) |
| 4f | "millionfold behind" | confirmed | "They're plausibly a millionfold behind humans in terms of how much data a human sees from birth to adulthood versus how much a model sees from cold start to finishing training." |
| 4g | Millidge "human Elo score" | confirmed | "Because we're already pretty close, in my opinion, to where we'll start crossing the human Elo score." |
| 5a | MLE-Bench Lite +0.053 (p=0.0024) | confirmed | "MLE-Bench Lite: mean of 3 seeds; deltas are paired by task vs AIDE0: +0.053 (p = 0.0024) for AIDE47"(另有 +0.042, p=0.0041 for AIDE85) |
| 5b | KernelBench 63%→34% | confirmed | "cutting its reward hacking rate from 63% to 34% on the held-out GPU kernel engineering benchmark"(正文:AIDE0 63% → AIDE85 34%) |
| 5c | "Even the efficiency claim…" | confirmed | "Even the efficiency claim is not statistically significant." |
| 5d | "not near an intelligence explosion" | confirmed | 原句句首带 "So":"So we believe we are not near an intelligence explosion with the current system." |
| 6a | HN 15% 阈值 + ~9% 句 | confirmed(nuance) | 在 zuzuen_1 评论(引用论文)内:"We find that the condition is met if a one-unit increase in AI model capabilities results in at least 15% higher AI R&D productivity";~9% 为 "a rough back-of-the-envelope calculation based on reported AI engineer uplift",估计回报 "has been around 9% since the launch of coding agents" → "we are not experiencing a self-sustaining acceleration"。非提交文本原句,且基于自报调查数据 |
| 6b | "flimsy basis" 评论 | confirmed | zuzuen_1:"A bit flimsy basis but an interesting paper nonetheless."(原句前有 "A bit") |
| 7a | Tom's Hardware 6-05 新闻确认首发 6-04 | nuance | 6-05 文章存在(Luke James,5 June 2026):"Anthropic warns Claude AI is building itself faster than expected, calls for option to halt frontier development — 'recursive self improvement' increases risk humans lose control of AI",引 "More than 80% of the code merged into its production codebase as of last month was authored by Claude"。但该页未点名报告标题《When AI Builds Itself》、未写 6-04;"On June 4, Anthropic published a report" 逐字出现在 Tom's Hardware 6-09 续篇(lost-human-control 那篇) |
| 7b | VentureBeat 标题 | confirmed | 标题逐字:"Anthropic says 80% of its new production code is now authored by Claude — how your enterprise can keep up"(og:title 尾作 "catch up";publishedTime 2026-06-04T16:25-04:00,正文称 report shared "today",可佐证 6-04 首发) |

## 总结
- confirmed 27 条(含 3 条带小 nuance:3c 限定语、6a 出处在评论区、4e 双重否定句式),wrong 0,not-on-page 0。
- 需改稿 1 条:7a 交叉引用——6-05 Tom's Hardware 文章本身未写《When AI builds itself》标题与 6-04 首发;"首发 6-04" 的逐字依据应改挂 Tom's Hardware 6-09 续篇("On June 4, Anthropic published a report,")或 VentureBeat 2026-06-04 发布时间戳。
- 建议性微调(非必改):Dwarkesh "crazy RSI" 引用保留双重否定原句;HN 15%/9% 建议注明出自 zuzuen_1 评论转引论文且为自报数据估算;CACM Kale 引句勿截掉前半否定句。
