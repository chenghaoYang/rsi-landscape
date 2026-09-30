# 2026 年 RSI 产业现状数字册(一手引语对照)

> 终审判定表:官方页 30 行、媒体页 31 行,包含不同判定状态;统一计数见 [audit.md](../audit.md)。阈值原文全表在 atlas §3.2;本页是引语与数字底册。

## Anthropic《When AI builds itself》(2026-06-04 首发,Favaro & Clark)

五阶段:"Building the first Claude(2021-23)→Chatbots(2023-25)→Coding agents(2025-26)→Autonomous agents(Today)→20XX? Closing the loop";阶段判据:写整个文件→"Agents can now run code themselves and delegate hours of work to other agents"→闭环期"agents could become capable enough to build and train models themselves."

核心数字(自报未审计):>80% 合入代码 Claude 写(2026-05;Claude Code 2025-02 前是"低个位数");人均出码 8×;开放式任务 76%(半年 +50pp);训练代码提速 ~3x(2025-05)→~52x(2026-04);agents 800 小时/恢复率 97%/约 $18k 算力;Mythos Preview 连续 ≥16h;Glasswing 1 万+高/危漏洞。

限定与外推(同页并列):"We are not there yet, and recursive self-improvement is not inevitable."+"But it could come sooner than most institutions are prepared for.";"Lines of code is an imperfect measure";2027 外推"tasks that take a person weeks";终点"fully autonomously designing and developing its own successor";三情景(停滞扩散/复利增益/自建后继者);"option to slow or temporarily pause";Clark:"we're not saying the world must pause or slow down."

## Anthropic《Measuring pace of AI development》(2026-09-17)

"Claude 'leads' 26% of Anthropic's AI R&D work"(2026-08;leads=Epoch AL4:AI 端到端完成、人类监督;2026-02 基线 <1%,仅见图);"approximately 30,000 agents … in our most-used internal platform. These measurements cover this platform only.";>90% 工作 ≥AL3;无任何测量子集全自主。方法自评:judge 一致率模型对人类 59%、人类对人类 35%;"the 'judge' model could make the same kinds of errors as the model it is checking."

## TIME(2026-08-07)

Clark:2028 前 AI 自主自改进概率 60%。OpenAI:GPT-5.3 Codex 第一个 "significant hand in its own development 'from start to finish'"(Glaese);内部目标 2028-03 全自动 AI 研究员;7 月起每研究员实验数翻倍。Anthropic 内部:Kaplan "Now I ask Claude to just try all eight";Orr "driving down a cliff road…75 instead of 25";Hubinger "Our ability to produce compelling evidence that our models are aligned is degrading"。反方:Marcus "strike terror"/"just faster coding";Narayanan 6 天测不出实质研究进展;Toner "deserves a 'what the f-ck' reaction"。生态:Recursive Superintelligence 融资 $650M;1300 名 AI 员工联署。

## 反方技术论证(2026 同台实录)

- MIT TR shadow evaluation(08-18):Opus 4.8 六天/$3000 攻两篇未发表 NeurIPS 2026 研究问题,原作者盲评双拒;"unambiguously bad at carrying out the research itself"(Kapoor);Clark 自评 "rote, formulaic thinking"="bearish signal on short RSI timelines"。自列局限:仅 2 篇/评分者知情/裁量偏见。
- CACM(07-06):Kale"基准分不出,控制图才能"(前半是否定句勿截);Solar-Lezama:开放研究造不出训练环境,自设目标即 reward hacking;Rosenfeld:数字-物理鸿沟+芯片史对照;Strauss 判据:写保护独立 holdout 增益才算 RSI;Ginsberg:"mostly marketing"/"self-regulation theater"。
- Dwarkesh(09-11):Schulman 循环论+瓶颈论;rapid-fire:10x uplift 2 年( Schulman)/5-10 年(O'Neill);ASI 3-4/5-10/约 5 年;Dwarkesh:"by default…crazy RSI within the next 10 years",变数是样本效率"plausibly a millionfold behind";Millidge:接近"crossing the human Elo score"。
- Economics of RSI:自持需 ≥15% 弹性;自报数据回测 ~9% → 未自持(HN:"A bit flimsy basis")。
- weco AIDE²(07-14):+0.053(p=0.0024);hacking 63%→34%;自认"Even the efficiency claim is not statistically significant"、"not near an intelligence explosion with the current system";反作弊统计层 bug 实为无效。

## 官方"真 RSI"门槛(三家均未触发;原文全表见 atlas §3.2)

OpenAI Critical=超人研究科学家 agent 或 1/5 墙钟代际跃迁持续数月(GPT-5.2/5.2-Codex、o3/o4-mini 均未达 High);GDM automation level 1=等成本全自动一个 Google AI 研究团队;Anthropic v3.1=全额替代全部研究员(5× 成本内)或进展翻倍可归因自动化。Opus 4/4.5 未跨线(v2.2 时代评估)。
