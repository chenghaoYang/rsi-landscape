# w6-frontier-2026
question: AI 领域 RSI(递归自我改进)的前沿能力、产业声称与政策阈值:(a) METR time horizon 论文与 RE-Bench;(b) MLE-bench 与 SWE-bench Verified SOTA;(c) 自动科研 agent(AI Scientist v1/v2、Google AI co-scientist)及其争议;(d) 产业自循环声称(区分官方一手 vs 媒体报道级);(e) 政策阈值(Anthropic RSP、OpenAI Preparedness、DeepMind FSF)。
checked: https://arxiv.org/abs/2503.04961(打开实为一篇量子物理论文——任务给的 ID 有误,METR 论文正确 ID 为 2503.14499), https://arxiv.org/abs/2503.14499, https://metr.org/blog/, https://metr.org/research/, https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/, https://metr.org/blog/2026-1-29-time-horizon-1-1/, https://metr.org/blog/2024-11-22-evaluating-r-d-capabilities-of-llms/, https://arxiv.org/abs/2410.07095, https://arxiv.org/abs/2408.06292, https://arxiv.org/abs/2504.08066, https://arxiv.org/abs/2502.18864, https://research.google/blog/accelerating-scientific-breakthroughs-with-an-ai-co-scientist/, https://www-cdn.anthropic.com/872c653b2d0501d6ab44cf87f43e1dc4853e4d37.pdf(RSP v2.2 PDF), https://www.anthropic.com/responsible-scaling-policy, https://www.anthropic.com/institute/recursive-self-improvement, https://deploymentsafety.openai.com/o3/tacit-knowledge-and-troubleshooting(o3/o4-mini system card), https://blog.samaltman.com/reflections, https://deepmind.google/discover/blog/introducing-the-frontier-safety-framework/ || 打不开的: https://www.anthropic.com/news/anthropic-responsible-scaling-policy(404,旧地址,已被 /responsible-scaling-policy 取代), https://cdn.openai.com/preparedness-framework-v2.pdf(404), https://openai.com/index/preparedness-framework-v2/(403), https://metr.org/research/re-bench-evaluating-rd-of-ai-systems/(404,新链接为 /blog/2024-11-22-evaluating-r-d-capabilities-of-llms/), theinformation.com(付费墙)

## claims
- [C1] METR time horizon 论文核心结论:前沿 AI 能以 50% 成功率完成的任务长度自 2019 年起约每 7 个月翻倍 | src: https://arxiv.org/abs/2503.14499 | quote: "frontier AI time horizon has been doubling approximately every seven months since 2019" | type: official
- [C2] 论文自带外推表述(即 2027-2030 方向的官方口径):约 5 年内 AI 可自动化当前人类耗时一个月的软件任务 | src: https://arxiv.org/abs/2503.14499 | quote: "extrapolation of this trend predicts that within 5 years, AI systems will be capable of automating many software tasks that currently take humans a month" | type: official
- [C3] 2026-01-29 发布 TH1.1:任务套件扩充、基础设施更换,新数据点覆盖 2025-2026 旗舰模型 | src: https://metr.org/blog/2026-1-29-time-horizon-1-1/ | quote: "We're releasing a new version of our time horizon estimates (TH1.1), using more tasks and a new eval infrastructure." | type: official
- [C4] TH1.1 数字:Claude Opus 4.5 的 50% 时间视野为 320 分钟(≈5.3 小时),GPT-5.1-codex-max 173 分钟;整体翻倍周期 196.5 天(≈7 个月),2023 年后加速至 130.8 天(比 TH1 估计快约 20%)| src: https://metr.org/blog/2026-1-29-time-horizon-1-1/ | quote: "Our estimates of time horizons for many models have been updated. The new estimates generally fall within our existing confidence intervals" | type: official
- [C5] METR 2026-08-14 资助公告把"追踪递归自我改进"列为机构工作方向——RSI 已成为 METR 官方研究议程用语 | src: https://metr.org/blog/ | quote: "...studying autonomous capabilities, tracking recursive self-improvement..." | type: official
- [C6] RE-Bench 定义:8 个开放式 ML 研发任务、AI 与人类专家同预算 8 小时,另有 71 次 8 小时人类专家尝试作基线 | src: https://metr.org/blog/2024-11-22-evaluating-r-d-capabilities-of-llms/ | quote: "RE-Bench: 8 challenging ML R&D tasks, 8-hour budget for both AI agents and human experts" | type: official
- [C7] RE-Bench 对比结论:固定 8 小时预算下最强 AI agent(o1-preview+AIDE)得分约为人类参赛者中位数 4 倍、接近最佳人类,但最佳人类仍胜出;更长时程下人类优势扩大 | src: https://metr.org/blog/2024-11-22-evaluating-r-d-capabilities-of-llms/ | quote: "At the fixed 8-hour budget, the top AI agent (o1-preview + AIDE) scores approximately 4x higher than the median human competitor (and approaches the best human), though the best humans still edge out AI agents." | type: official
- [C8] MLE-bench(OpenAI)定义:用 Kaggle 机器学习工程比赛测自动化 | src: https://arxiv.org/abs/2410.07095 | quote: "75 ML engineering-related competitions from Kaggle" | type: official
- [C9] MLE-bench 最好成绩(论文时点):o1-preview + AIDE 达到或超过铜牌水平的比例 16.9% | src: https://arxiv.org/abs/2410.07095 | quote: "the best-performing setup--OpenAI's o1-preview with AIDE scaffolding--achieves at least the level of a Kaggle bronze medal in 16.9% of competitions." | type: official
- [C10] SWE-bench Verified 当前 SOTA 大致水平(2026 年中,二手、未经官方榜核实):约 88-94% | src: https://blink.new (Blink Blog, 2026-06-07) | quote: "As of May 2026, Claude Mythos leads SWE-bench Verified at 93.9%, followed by Claude Opus 4.8 at 88.6% and Claude Opus 4.7 at 87.6%." | type: secondary
- [C11] AI Scientist v1(Sakana 等)端到端自动化(选题→实验→写作→自动评审),成本低于 15 美元/篇 | src: https://arxiv.org/abs/2408.06292 | quote: "less than $15 per paper" / "the first comprehensive framework for fully automatic scientific discovery" | type: official
- [C12] AI Scientist v1 争议要害:"超过顶会接收线"的判断来自作者自建的自动评审员,非人类同行评审 | src: https://arxiv.org/abs/2408.06292 | quote: "can produce papers that exceed the acceptance threshold at a top machine learning conference as judged by our automated reviewer" | type: official
- [C13] AI Scientist v2(2025-04)称产出首个通过同行评审的全 AI 生成 workshop 论文(ICLR 2025 workshop);去除了人工代码模板依赖 | src: https://arxiv.org/abs/2504.08066 | quote: "the first entirely AI generated peer-review-accepted workshop paper" | type: official
- [C14] Google AI co-scientist(2025-02-19 博客)定位为"虚拟科学协作者"而非自主科学家:基于 Gemini 2.0 的多智能体系统辅助人类科学家生成假设与提案 | src: https://research.google/blog/accelerating-scientific-breakthroughs-with-an-ai-co-scientist/ | quote: "a multi-agent AI system built with Gemini 2.0 as a virtual scientific collaborator" | type: official
- [C15] co-scientist 的人类在环边界:假设须经合作实验室湿实验验证;AML 药物重定位与肝纤维化靶点为两个验证案例 | src: https://research.google/blog/accelerating-scientific-breakthroughs-with-an-ai-co-scientist/ | quote: "inhibit tumor viability at clinically relevant concentrations" | type: official
- [C16] Anthropic RSP v2.2(2025-05-14 生效)原文:AI R&D-4 阈值定义(ASL-4 触发器)="能完全自动化 Anthropic 入门级、仅远程研究员的工作" | src: https://www-cdn.anthropic.com/872c653b2d0501d6ab44cf87f43e1dc4853e4d37.pdf | quote: "AI R&D-4: The ability to fully automate the work of an entry-level, remote-only Researcher at Anthropic." | type: official
- [C17] RSP 现行版本为 v3.4(2026-07-08 生效,页面 2026-08-14 更新);跨过 AI R&D-4 须提交 affirmative safety case | src: https://www.anthropic.com/responsible-scaling-policy | quote: "once models cross the AI R&D-4 capability threshold, we develop an affirmative case identifying the most immediate and relevant misalignment risks from models pursuing misaligned goals" | type: official
- [C18] Anthropic 对 Claude Opus 4 / Opus 4.5 做过 AI R&D-4 评估,未跨线 | src: https://www.anthropic.com/transparency(经检索确认;Opus 4.5 System Card 引 18 项评估套件) | quote: "none of the 18..." (评估套件结果,检索摘要级,原句待核) | type: secondary
- [C19] OpenAI Preparedness Framework v2(2025-04-15)追踪三大类别,其中之一即 AI Self-Improvement | src: https://deploymentsafety.openai.com/o3/tacit-knowledge-and-troubleshooting(o3/o4-mini system card) | quote: "The Framework currently has three Tracked Categories: Biological and Chemical, Cybersecurity, and AI Self-Improvement." | type: official
- [C20] o3/o4-mini 在 self-improvement 类"软件工程与 AI 研究任务上有改进表现"但开放式真实世界评估表现差,未达 High | src: https://deploymentsafety.openai.com/o3/tacit-knowledge-and-troubleshooting | quote: "determined that OpenAI o3 and o4-mini do not reach the High threshold in any of our three Tracked Categories" / "demonstrate improved performance on software engineering and AI research tasks relevant to AI self-improvement risks" | type: official
- [C21] DeepMind Frontier Safety Framework v1(2024-05-17):初始 Critical Capability Levels 覆盖四域,含 machine learning R&D(即 self-improvement/AI R&D 加速对应类别) | src: https://deepmind.google/discover/blog/introducing-the-frontier-safety-framework/ | quote: "Our initial set of Critical Capability Levels is based on investigation of four domains: autonomy, biosecurity, cybersecurity, and machine learning R&D" | type: official
- [C22] FSF 对 ML R&D 能力的关切表述:可能助长其他关键能力模型扩散或能力"快速且不可控的升级" | src: https://deepmind.google/discover/blog/introducing-the-frontier-safety-framework/ | quote: "enable the spread of models with other critical capabilities, or enable rapid and unmanageable escalation" | type: official
- [C23] Sam Altman(官方博客 Reflections,2025-01-06):已知如何造 AGI,且目标已转向 superintelligence,因其能大规模加速科学发现 | src: https://blog.samaltman.com/reflections | quote: "We are now confident we know how to build AGI as we have traditionally understood it." / superintelligent tools "could massively accelerate scientific discovery" | type: official
- [C24] Dario Amodei(CFR 活动,2025-03-10,媒体报道级):AI 将在 3-6 个月内写 90% 的代码,其后逼近 100% | src: https://www.benzinga.com (2025-03-27,转述 CFR 现场发言) | quote: "Anthropic CEO Says AI Could Write '90% Of Code' In '3 To 6 Months'" | type: secondary
- [C25] Anthropic Institute 报告《When AI builds itself》(2026 年中,Marina Favaro 与 Jack Clark 署名,页面含 2026-09-18 更新):官方一手承认已进入 RSI 进程——Claude 写下 >80% 合入代码、领导层估计 90%+;外推到"自主设计开发自身后继者" | src: https://www.anthropic.com/institute/recursive-self-improvement | quote: "As of May 2026, more than 80% of the code we merge into Anthropic's codebase was authored by Claude." / "Taken far enough, and given enough compute, that trend points to an AI system capable of fully autonomously designing and developing its own successor." / "In 2027, AI systems could be capable of tasks that take a person weeks." | type: official

## conflicts
1. 任务给定的 METR 论文 arXiv ID 2503.04961 有误——该 ID 实为一篇量子物理论文("Role of Matter Interactions in Superradiant Phenomena");METR time horizon 论文正确 ID 为 2503.14499,且 v4(2026-07-10)已更名为 "Measuring AI Ability to Complete Long Software Tasks"。
2. 第三方追踪站(apiardata.com、canagentswork.com 等)称 2026-02 前沿 50% 视野已达 ~14.5-17.4 小时,与 METR 官方 TH1.1 数据(Opus 4.5 = 320 分钟 ≈ 5.3 小时)明显不一致;第三方可能混入外推值或不同任务口径,应采信 METR 官方页。
3. RE-Bench 任务数:METR 官方博客为 8 个任务;openreward.ai 写 "7 challenging, open-ended ML research engineering environments"。采官方 8,差异待核(可能为删减版环境数)。
4. "entry-level, remote-only" 短语在 RSP v2.2 中属于 AI R&D-4(ASL-4 触发器);部分二手资料把它记成 "ASL-4/AI R&D-2" 混称。v3.x 拆分阈值后另有 "dramatically accelerate effective AI research" 的更高档位,检索摘要可见但未取原文。
5. 《When AI builds itself》发布日期:Tom's Hardware 称 6 月 4 日、Cloud Security Alliance 引为 May 2026;页面含 "Update 9/18/2026"。取"2026 年 5-6 月发布、9/18 更新"为宜。
6. SWE-bench Verified SOTA(93.9% "Claude Mythos")仅见于非官方博客,未在 swebench.com 官方榜核实,置信度低。
7. 有评论称 Preparedness v2 移除了 persuasion 追踪类别(airuntimesecurity 等),未获一手原文确认。

## gaps
- 【最大缺口】The Information 2025-11 关于 OpenAI 内部 "superhuman coder" 的报道:付费墙且各路转载均未给出可引用的原文段落;目前仅有报道级间接证据(The Information 2025-12-01 报 Altman "code red";TIME 2025-01 报道 OpenAI 董事会/超级智能规划;80,000 Hours 播客讨论 superhuman coder 框架)。未能完成"一手引语+发言人+日期"的取证。
- OpenAI Preparedness Framework v2 的 self-improvement High/Critical 阈值定义原文未取得(官方 PDF 链接失效、openai.com 403);仅有二手确认三类别结构与"发布时无模型达 Critical"。
- DeepMind FSF v2.0(2025-02)/v3.0(2025-09)的 ML R&D CCL 原文(如 "Machine Learning R&D uplift level 1: Can or has been used to accelerate AI development...")仅见于 ETO agora 存档的检索摘要,未直接打开核验。
- Dario Amodei CFR 2025-03-10 发言的官方 transcript 未直接抓取(经 Benzinga 2025-03-27 等二手确认)。
- METR 对 GPT-5 的单独评估帖(2025-08)与 Expenditure Horizon 页未打开。
- AI Scientist v2 论文随后从 ICLR workshop 撤回及评审造假争议的原始档案(邮件/公示)未取到。
- Anthropic Opus 4.5 未跨 AI R&D-4 的结论只在检索摘要级(Transparency hub),未取原句。

## leads
- https://time.com/article/2026/08/07/ai-recursive-self-improvement-anthropic-openai — TIME《Inside the Race to Make AI Build Itself》(2026-08-07),d 类产业声称的集中报道源
- https://www.tomshardware.com (2026-06-09) — "Anthropic's warning over AI self-improvement has a hidden [angle]",对 C25 报告的独立技术评论
- https://metr.org/blog/ — 2026-02-24 "Review of the 'Risks from automated R&D' section in the Anthropic Risk Report (February 2026)";2026-03-20 "Impact of modeling assumptions on time horizon results"(含 Opus 4.6 8-20 小时敏感性讨论)
- https://metr.org/blog/2025-08-20-forecasting-impacts-of-ai-acceleration — METR×FRI《Forecasting the Impacts of AI R&D Acceleration》试点研究(2025-08-20)
- https://metr.org/research/ — "GPT-5 evaluation" 页与 "Expenditure Horizon"(2026)可作 time horizon 补充数据点
- https://www-cdn.anthropic.com/files/4zrzovbb/website/bf04581e4f329735fd90634f6a1962c13c0bd351.pdf — RSP v3.1 PDF(v3.x 阈值拆分后的原文,补 C16/C17 差异)
- https://www.anthropic.com/transparency — Opus 4 / Opus 4.5 对 AI R&D-4 的评估结果原句
- https://agora.eto.tech/instrument/2040 — FSF v2.0 全文存档(ML R&D CCL 原文)
- VentureBeat — "Anthropic says 80% of its new production code is now authored by Claude"(C25 的媒体交叉源)
- https://blog.samaltman.com/the-gentle-singularity(2025-06)— Altman 关于 AI 做 AI 研究的进一步官方表述
- https://ai2027-tracker.com/changelog — "superhuman-coder threshold ... independently corroborated (Microsoft)";AI 2027 场景与现实的对照线
- https://80000hours.org 播客 "What the hell happened with AGI timelines in 2025?" — superhuman coder 概念谱系(AI 2027 起源)批判
- https://futureoflife.org — AI Safety Index: Winter 2025(实验室"竞速 AGI/超级智能"的第三方批评)
- https://smarterx.ai/smarterxblog/anthropic-ipo-recursive-self-improvement — Anthropic IPO 文件中的 RSI 表述线索(值得核实一手 S-1)
- https://www.deeplearning.ai (2026-05-22) — "AI Agents May Not Be Getting Better at Full Range of Tasks",对能力叙事的反方观点

**给 lead 的备注**:(1) 沙箱只读,笔记未落盘,上文即完整代存稿;(2) 任务输入中的 arXiv ID 2503.04961 系笔误,后续轮次请统一使用 2503.14499;(3) 若下一轮要做 d 类取证,优先攻 The Information 原文与 Anthropic IPO 文件这两个缺口。
