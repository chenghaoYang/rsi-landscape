# audit-official
checked: 2026-09-28 实际重开
- https://www.anthropic.com/institute/recursive-self-improvement
- https://www.anthropic.com/institute/measuring-pace-of-ai-development
- https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf
- https://deploymentsafety.openai.com/gpt-5-2/gpt-5-2-system-card.pdf (实为 HTML,已按 HTML 抓取)
- https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/strengthening-our-frontier-safety-framework/frontier-safety-framework_3-1.pdf
- https://www-cdn.anthropic.com/files/4zrzovbb/website/bf04581e4f329735fd90634f6a1962c13c0bd351.pdf (RSP, 页脚标 "April 2, 2026 (RSP v3.1)")
- https://metr.org/blog/2026-1-29-time-horizon-1-1/
- https://sakana.ai/rsi-lab
- https://people.idsia.ch/~juergen/goedelmachine.html
- https://ai-2027.com/

## verdicts

| # | 主张(短语) | 判定 | 证据/正确原句 |
|---|---|---|---|
| 1a | "As of May 2026, more than 80% of the code we merge into Anthropic's codebase was authored by Claude." | confirmed | 原句逐字一致,后接脚注 3;前文 "Before Claude Code launched in research preview in February 2025, this number was in the low single digits." |
| 1b | 五阶段标题 | confirmed | "2021–2023 Building the first Claude / 2023–2025 Chatbots / 2025–2026 Coding agents / Today Autonomous agents / 20XX? Closing the loop" |
| 1c | "8x as much code per quarter" | confirmed | "today, Anthropic engineers on average ship 8x as much code per quarter as they did from 2021-2025" |
| 1d | "76% in May 2026, up 50 percentage points in six months" | confirmed | "On the most open-ended tasks, Claude's success rate reached 76% in May 2026, up 50 percentage points in six months." |
| 1e | "~52x"(Mythos Preview, April 2026) | confirmed | "In May 2025, Claude Opus 4 averaged a ~3x speedup over the starting code. By April 2026, Claude Mythos Preview was achieving ~52x."(另有 "both across models (~3x to ~52x over the past year)") |
| 1f | "We are not there yet, and recursive self-improvement is not inevitable." | confirmed | 逐字一致,紧接 "But it could come sooner than most institutions are prepared for." |
| 1g | 三情景第三句 | confirmed | 页面明写 "We can imagine at least three future scenarios:";第三情景首句逐字为 "AI systems themselves become capable of full recursive self-improvement, and begin building their successors." |
| 1h | 【否定】无 "we don't consider ourselves to have" | confirmed-absent | 全文 "consider ourselves" 命中 0 次,"don't consider" 命中 0 次 |
| 1i | 【否定】无 "26%" | confirmed-absent | 全文 "26%" 计数 0(有 51%/64%/76%/20%,无 26%) |
| 2a | "Claude 'leads' 26% of Anthropic's AI R&D work" | confirmed | "As of August 2026, Claude is not operating fully autonomously for any measured subset of AI R&D work. Claude \"leads\" 26% of Anthropic's AI R&D work. The share of work at or above \"AI collaborates\" is above 90%." |
| 2b | "approximately 30,000 agents doing research and engineering work" | confirmed | "As of August 2026, there were approximately 30,000 agents doing research and engineering work at Anthropic at any one time in our most-used internal platform. These measurements cover this platform only."(引用需保留限定语) |
| 2c | AL4 定义句 | confirmed | "In AL4, AI \"leads\": it can complete most of the task end-to-end from a high-level prompt, while the human supervises."(AL3: "can do large chunks of work under close human direction") |
| 2d | judge 一致率 59% 与 35% | confirmed | "model-versus-human exact agreement was 59%, human-versus-human exact agreement was 35%), and model and human ratings were within one level of each other 97% of the time." 注意归因:59%=模型对人类,35%=人类对人类 |
| 3a | Preparedness 定义 "AI Self-improvement: The ability of an AI system to accelerate AI research..." | confirmed | 全句:"AI Self-improvement: The ability of an AI system to accelerate AI research, including to increase the system's own capability."(Tracked Category) |
| 3b | High "…mid-career research engineer assistant" | confirmed | "[High] The model's impact is equivalent to giving every OpenAI researcher a highly performant mid-career research engineer assistant, relative to those researchers' 2024 baseline." |
| 3c | Critical "recursively self improving (i.e., fully automated AI R&D)…1/5th the wall-clock time" | confirmed | "[Critical] The model is capable of recursively self improving (i.e., fully automated AI R&D), defined as either (leading indicator) a superhuman research scientist agent OR (lagging indicator) causing a generational model improvement (e.g., from OpenAI o1 to OpenAI o3) in 1/5th the wall-clock time of equivalent progress in 2024 (e.g., sped up to just 4 weeks) sustainably for several months." |
| 4 | GPT-5.2 self-improvement 未达 High | confirmed | 两处:"evaluations of final checkpoints indicate that, like their predecessor models, GPT-5.2 models do not have a plausible chance of reaching a High threshold." 及 §5.1.3 "gpt-5.2-thinking performed at a similar capability level to gpt-5.1-codex-max and did not meet our High thresholds. The High capability threshold is defined to be equivalent to a performant mid-career research engineer and performance in the evaluations below indicate we can rule this out for gpt-5.2-thinking." |
| 5a | FSF 3.1 "ML R&D acceleration level 1" | confirmed | "ML R&D acceleration level 1: Has been used to accelerate AI development, resulting in AI progress substantially accelerating from historical rates." |
| 5b | FSF 3.1 "ML R&D automation level 1" | confirmed | "ML R&D automation level 1: Can fully automate the work of any team of researchers at Google focused on improving AI capabilities, with approximately comparable all-inclusive costs."(注意含 "focused on improving AI capabilities") |
| 6a | RSP "Automated R&D in key domains" 阈值句 | confirmed | "Automated R&D in key domains. AI systems that can fully automate, or otherwise dramatically accelerate, the work of large, top-tier teams of human researchers in domains where fast progress could cause threats to international security and/or rapid disruptions to the global balance of power—for example, energy, robotics, weapons development and AI itself." |
| 6b | 操作化:全额替代/5 倍成本内;翻倍+可归因 | confirmed | "(1) our models would be able to fully substitute for our entire set of Research Scientists and Research Engineers, at competitive costs (i.e., within a factor of 5); or (2) … (a) we observe or expect double the rate of progress … and (b) it is plausible that this doubling is substantially attributable to the automation of research and/or engineering (as opposed to other factors, such as increased headcount, compute, or general productivity)" |
| 6c | 脚注 4 | confirmed | "\"Double the rate of progress\" means \"as much progress in one year as one would see in two years at baseline.\""(后接 3x×3x→81x effective scaleup 示例) |
| 7a | Opus 4.5 = 320 分钟 | confirmed | 表 "Changes to Model Horizon Estimates":"Claude Opus 4.5 289 [110,1268] → 320 [170,729] (+11%)"(TH1→TH1.1,单位为 50% time horizon 分钟)。注意:另一张基建对比表为 "289 mins"(Vivaria)/"270 mins"(Inspect),勿混用 |
| 7b | 翻倍周期 130.8 天(2023 后) | confirmed | 表:"P50 doubling time, >=2023: TH1 165.3 days [129,211] / TH1.1 130.8 days [107,161]";正文亦写 "The post-2023 doubling-time is 131 days under TH1.1" |
| 8a | Sakana "redesigning the AI development process itself with AI" | confirmed | "the formal establishment of the Sakana AI RSI Lab, a dedicated research group within Sakana AI, tasked with redesigning the AI development process itself with AI."(另:Schmidhuber 任 Chief Scientific Advisor,2026 年 9 月加入) |
| 8b | "the most sample-efficient one" | confirmed | "we are building not the most compute-hungry self-improvement engine, but the most sample-efficient one." |
| 9a | Goedel "provably optimal self-improvements" | confirmed | "Goedel machines are self-referential universal problem solvers making provably optimal self-improvements." |
| 9b | "globally optimal - no local maxima" | confirmed | "We show that such a self-rewrite is globally optimal - no local maxima! - since the code first had to prove that it is not useful to continue the proof search for alternative self-rewrites." |
| 10a | "AI R&D progress multiplier is now 10x" | confirmed | "The AI R&D progress multiplier is now 10x, meaning that OpenBrain is making about a year of algorithmic progress every month."(故事内 Superhuman coder 阶段;同页还有 "their AIs give a 10x research progress multiplier compared to America's 25x" 指中国) |
| 10b | "200,000 Agent-3 copies" | confirmed | "OpenBrain runs 200,000 Agent-3 copies in parallel, creating a workforce equivalent to 50,000 copies of the best human coder sped up by 30x." |

## 总结
- confirmed:28 条正面主张全部逐字/近逐字命中;2 条否定主张均 confirmed-absent。
- 需改稿:0 条。无 wrong / not-on-page。
- 引用时建议保留的限定语(非必改):2b 的 "at any one time in our most-used internal platform / platform only";2d 的 59% 与 35% 归因方向;3b 的 "The model's impact is…relative to those researchers' 2024 baseline" 尾巴;5b 的 "focused on improving AI capabilities";7a 注明 320 为 TH1.1 点估计(分钟),页内另有一张 270-mins 基建对比表勿混用;10a 注明是叙事时间线内某时点的数值。
