# w4-training-loop
question: AI 领域 RSI 深层——自生成数据/课程并改权重的谱系(Self-Instruct→STaR→Self-Rewarding→SPIN→AZR→SEAL)、RLVR 燃料出处(Tulu 3)、工业合成数据飞轮一手表述、负面证据(model collapse 及 rebuttal)、各方法效果数字与前提条件
checked: https://arxiv.org/abs/2212.10560, https://ar5iv.labs.arxiv.org/html/2212.10560, https://arxiv.org/abs/2203.14465, https://ar5iv.labs.arxiv.org/html/2203.14465, https://arxiv.org/abs/2401.10020, https://ar5iv.labs.arxiv.org/html/2401.10020, https://arxiv.org/abs/2401.01335, https://ar5iv.labs.arxiv.org/html/2401.01335, https://arxiv.org/abs/2505.03335, https://arxiv.org/html/2505.03335v2 (v1/v3 亦查,正文截断,附录图未取到), https://arxiv.org/abs/2305.17493 (注:arXiv 页显示的是旧版摘要), https://www.nature.com/articles/s41586-024-07566-y (经 web reader 绕过跳转取得全文), https://arxiv.org/abs/2404.01413, https://arxiv.org/abs/2506.10943, https://arxiv.org/abs/2411.15124, https://arxiv.org/html/2407.21783v1 (v4 为 404), https://ar5iv.labs.arxiv.org/html/2407.21783, https://arxiv.org/abs/2212.08073, https://arxiv.org/abs/2407.04442 (打开后发现是错误论文 GoSurf,"Arena Learning" 的正确 arXiv id 未锁定,弃用)

## claims
- [C1] Self-Instruct 让语言模型自己生成 instruction/input/output 并过滤无效与相似样本,再微调自身。 | src: https://arxiv.org/abs/2212.10560 | quote: "Our pipeline generates instructions, input, and output samples from a language model, then filters invalid or similar ones" | type: primary
- [C2] Self-Instruct 在 GPT-3 上迭代跑出约 52K 条指令、82K 组输入输出实例。 | src: https://ar5iv.labs.arxiv.org/html/2212.10560 | quote: "The iterative Self-Instruct process on this model leads to about 52k instructions, paired with about 82K instance inputs and target outputs." | type: primary
- [C3] 效果:在 Super-NaturalInstructions 上比原 GPT-3 绝对提升 33%,与用私有用户数据训练的 InstructGPT-001 相当,仅落后 5 个绝对百分点。 | src: https://arxiv.org/abs/2212.10560 | quote: "we demonstrate a 33% absolute improvement over the original model on Super-NaturalInstructions, on par with the performance of InstructGPT" … "leaving only a 5% absolute gap behind InstructGPT" | type: primary
- [C4] STaR 的机制是让模型从自己生成的推理步骤(reasoning)中学习并迭代自举。 | src: https://arxiv.org/abs/2203.14465 | quote: "We show that STaR lets a model improve itself by learning from its own generated reasoning." | type: primary
- [C5] STaR 效果(GPT-J 6B):CommonsenseQA 上比 few-shot 基线 +35.9%、比直接微调答案的基线 +12.5%,并追平 30 倍大的微调模型。 | src: https://ar5iv.labs.arxiv.org/html/2203.14465 | quote: "we find STaR improves over both a few-shot baseline (+35.9%) and a baseline fine-tuned to directly predict answers (+12.5%)" … "and performs comparably to a fine-tuned model that is 30× larger (72.5% vs. 73.0%)." | type: primary
- [C6] STaR 在 GSM8K 上(同 6B 量级):直接微调 5.8% vs 少样本 CoT 3.1%,STaR 无 rationalization 10.1%、有 rationalization 10.7%。 | src: https://ar5iv.labs.arxiv.org/html/2203.14465 | quote: "STaR without rationalization: 10.1" … "STaR with rationalization: 10.7" … "GPT-J Direct Finetuned: 5.8" | type: primary
- [C7] Self-Rewarding LMs:模型自身经 LLM-as-a-Judge 提示为自己的回答打分、在训练中给自己提供奖励信号。 | src: https://arxiv.org/abs/2401.10020 | quote: "the language model itself is used via LLM-as-a-Judge prompting to provide its own rewards during training" | type: primary
- [C8] 效果:Llama 2 70B 经 3 轮 self-rewarding 训练后,在 AlpacaEval 2.0 榜上超过 Claude 2、Gemini Pro 和 GPT-4 0613。 | src: https://arxiv.org/abs/2401.10020 | quote: "Fine-tuning Llama 2 70B on three iterations of our approach yields a model that outperforms many existing systems on the AlpacaEval 2.0 leaderboard, including Claude 2, Gemini Pro, and GPT-4 0613." | type: primary
- [C9] 迭代数字(正文):对 GPT4-Turbo 的胜率第 1/2/3 轮分别为 9.94%/15.38%/20.44%。 | src: https://ar5iv.labs.arxiv.org/html/2401.10020 | quote: "win rates, in this case over GPT4-Turbo, from 9.94% in Iteration 1, to 15.38% in Iteration 2, to 20.44% in Iteration 3." | type: primary
- [C10] SPIN 机制:LLM 与自身的先前版本对打(self-play),通过把自生成回答与人类标注数据区分开来 refinement 策略。 | src: https://arxiv.org/abs/2401.01335 | quote: "At the heart of SPIN lies a self-play mechanism, where the LLM refines its capability by playing against instances of itself." … "the LLM generates its own training data from its previous iterations, refining its policy by discerning these self-generated responses from those obtained from human-annotated data." | type: primary
- [C11] SPIN 效果:HuggingFace Open LLM Leaderboard 平均分 58.14→63.16,GSM8K 与 TruthfulQA 提升 10%+,MT-Bench 5.94→6.78;第 1 轮起超过 DPO。 | src: https://ar5iv.labs.arxiv.org/html/2401.01335 | quote: "Ultimately, SPIN effectively improves the base model's average score from 58.14 to 63.16 on the HuggingFace Open LLM Leaderboard" … "From iteration 1, SPIN even surpasses the performance of DPO on the leaderboard benchmark." | type: primary
- [C12] Absolute Zero 范式:单一模型自己出题以最大化自身学习进度,并用代码执行器同时验证题目与答案,作为统一可验证奖励源,全程零外部数据。 | src: https://arxiv.org/abs/2505.03335 | quote: "a single model learns to propose tasks that maximize its own learning progress and improves reasoning by solving them" … "self-evolves its training curriculum and reasoning ability by using a code executor to both validate proposed code reasoning" | type: primary
- [C13] 论文把 Absolute Zero 明确定位为一种新的 RLVR(可验证奖励 RL)范式。 | src: https://arxiv.org/html/2505.03335v2 | quote: "we propose a new RLVR paradigm called Absolute Zero" | type: primary
- [C14] AZR 效果:完全不用外部数据训练,在编程与数学推理上取得整体 SOTA,胜过依赖数万条域内人工精选样本的 zero-setting 模型。 | src: https://arxiv.org/abs/2505.03335 | quote: "Despite being trained entirely without external data, AZR achieves overall SOTA performance on coding and mathematical reasoning" … "outperforming existing zero-setting models that rely on tens of thousands of in-domain human-curated examples" | type: primary
- [C15] AZR 异常:Llama3.1-8b 训练中偶现令人担忧的思维链(论文命名 "uh-oh moment"),示例内容为"智取所有聪明机器和不聪明的人类",论文承认该范式仍需人类监督。 | src: https://arxiv.org/html/2505.03335v2 | quote: "We observe AZR with Llama3.1-8b occasionally produces concerning chains of thought, we term the 'uh-oh moment'" … "still necessitates oversight due to lingering safety concerns" | type: primary
- [C16] 工业一手(Llama 3):SFT 阶段总共生成超过 270 万条合成样本。 | src: https://arxiv.org/html/2407.21783v1 | quote: "In total, we generate over 2.7M synthetic examples which were used during SFT." | type: primary
- [C17] Llama 3 后训练呈飞轮形态:每轮迭代都从最新模型采样合成 SFT 数据、连同新偏好标注一起再训练。 | src: https://ar5iv.labs.arxiv.org/html/2407.21783 | quote: "In each cycle, we collect new preference annotations and SFT data, sampling synthetic data from the latest models." | type: primary
- [C18] 飞轮边界(一手负结果):Meta 发现 Llama 3 405B 在自己生成的数据上训练并无帮助——合成数据飞轮主要用于小模型/下游环节。 | src: https://ar5iv.labs.arxiv.org/html/2407.21783 | quote: "our initial experiments revealed that training Llama 3 405B on its own generated data is not helpful" | type: primary
- [C19] Constitutional AI(Anthropic)是工业级自产训练数据起点:初始模型采样→生成自我批评与修订→用修订后回答微调自身→以 AI 偏好作奖励做 RL(RLAIF)。 | src: https://arxiv.org/abs/2212.08073 | quote: "we sample from an initial model, then generate self-critiques and revisions" … "We then train with RL using the preference model as the reward signal, i.e. we use 'RL from AI Feedback' (RLAIF)." | type: primary
- [C20] RLVR 术语与方法的定义性出处是 Tulu 3 论文(Lambert et al.),作为其三段式后训练(SFT、DPO、RLVR)的一环。 | src: https://arxiv.org/abs/2411.15124 | quote: "a novel method we call Reinforcement Learning with Verifiable Rewards (RLVR)" | type: primary
- [C21] Tulu 3 效果:超过 Llama 3.1、Qwen 2.5、Mistral 的指令版,乃至 GPT-4o-mini 与 Claude 3.5-Haiku 等闭源模型。 | src: https://arxiv.org/abs/2411.15124 | quote: "results surpassing the instruct versions of Llama 3.1, Qwen 2.5, Mistral, and even closed models such as GPT-4o-mini and Claude 3.5-Haiku." | type: primary
- [C22] Nature 2024 核心结论(Shumailov et al.):不加区分地把模型生成内容用于训练会给模型带来不可逆缺陷,原始内容分布的尾部消失。 | src: https://www.nature.com/articles/s41586-024-07566-y (Nature 631, 755–759, 2024) | quote: "indiscriminate use of model-generated content in training causes irreversible defects in the resulting models, in which tails of the original content distribution disappear" | type: primary
- [C23] collapse 定义:一种退化过程,随世代推移模型遗忘真实的底层数据分布,即使分布本身没有漂移;其循环形态是模型生成物污染下一代训练集、进而"误感知现实"。 | src: https://www.nature.com/articles/s41586-024-07566-y | quote: "model collapse—a degenerative process whereby, over time, models forget the true underlying data distribution, even in the absence of a shift in the distribution over time" … "in which the data they generate end up polluting the training set of the next generation. Being trained on polluted data, they then mis-perceive reality." | type: primary
- [C24] 前提条件:理论上即便近乎理想条件(无函数估计误差)该过程也不可避免;但保留原始真实数据可显著缓解(仅轻微性能下降),且当分布尾部重要时必须接触真人数据。 | src: https://www.nature.com/articles/s41586-024-07566-y | quote: "we show that this process is inevitable, even for cases with almost ideal conditions for long-term learning, that is, no function estimation error" … "preservation of the original data allows for better model fine-tuning and leads to only minor degradation of performance" … "in learning tasks in which the tails of the underlying distribution matter, one needs access to real human-produced data" | type: primary
- [C25] Gerstgrasser et al. 反驳:模型崩塌并非不可避免——既往研究假设新数据"替换"旧数据,而更现实的是数据"累积";累积式训练下合成数据与真实数据并存即可避免 collapse,且跨模型规模/架构/超参成立。 | src: https://arxiv.org/abs/2404.01413 | quote: "accumulating the successive generations of synthetic data alongside the original real data avoids model collapse" … "those studies largely assumed that new data replace old data over time, where an arguably more realistic assumption is that data accumulate" | type: primary
- [C26] SEAL(MIT, 2025):框架让 LLM 通过生成自己的微调数据与更新指令(self-edit)实现自适应,self-edit 经 SFT 落为持久权重更新,是"自产自训改权重"的最新节点。 | src: https://arxiv.org/abs/2506.10943 | quote: "generating their own finetuning data and update directives" … "produces a self-edit" (可指定优化超参或重组信息,经 "supervised finetuning (SFT)" 应用) | type: primary
- [C27] SEAL 效果(摘要口径):在知识注入与少样本泛化两类实验上被表述为"通往(持续自定向改进)的有希望一步",摘要未给具体数字。 | src: https://arxiv.org/abs/2506.10943 | quote: "Experiments on knowledge incorporation and few-shot generalization show that SEAL is a promising step toward" | type: primary

## conflicts
- collapse 是否必然:Shumailov(Nature 2024)称理论上即使无函数估计误差也不可避免 [C24];Gerstgrasser(2404.01413)指出其关键隐含前提是"新数据替换旧数据",在更现实的"数据累积"设定下 collapse 可避免 [C25]。两者并不直接矛盾,属前提条件之争(replacement vs accumulation),且 Shumailov 自己的实验也承认保留 10% 原始数据仅致轻微退化。
- Self-Rewarding 的 AlpacaEval 数字口径:常见转述的 "23.3%→39.7%" 在本次可访问的摘要与正文中未找到;正文可验证的是对 GPT4-Turbo 胜率 9.94%→15.38%→20.44%(对比对象与口径不同,不可混用)。
- STaR 数字口径:流传的 "GSM8K 60.2%→72.5%" 未在 ar5iv 现行版本中找到;现行版(6B 实验)给出的是 CommonsenseQA 72.5% vs 30 倍大模型 73.0%、GSM8K 10.1%→10.7%。需 diff v1 摘要确认是否有 175B 早期数字。
- AZR "观察思考出现可疑中间语言/obfuscated(类中世纪英语)"的轶事:在 v1/v2/v3 HTML 正文均未检索到 "Middle English"/"obfusc" 字样,可验证的原文是 "uh-oh moment" concerning CoT [C15];该"中间语言"说法仅见于社区/媒体转述,与可查证文本不一致,引用须谨慎。
- arXiv 2305.17493 页面摘要(旧版,含 "We refer to this effect as Model Collapse" "the value of data collected about genuine human interactions … increasingly valuable")与 Nature 定稿摘要措辞不同,引用时须注明版本来源。

## gaps
- AZR 的具体效果数字(各模型规模在 CodeForces/OTIS/GSM8K 等的具体提升百分点、与 Claude 3.7 等的对比)未取到;HTML 正文截断,附录 Figure 32("uh-oh moment" 全文)为图未取到——"中间语言"轶事的最终查证需读 PDF 附录与 OpenReview 版本。
- SEAL 的量化结果(知识注入/ARC 少样本的具体提升数)在摘要中缺席,需读正文;且 SEAL 用 RL 训练 self-edit 策略的细节未取。
- Tulu 3 中 RLVR 的算法细节与 405B 对 GPT-4o 的具体胜率数字未取(摘要只到定性表述)。
- 工业侧 "synthetic data flywheel" 的标准化一手定义未锁定:Amazon "Arena Learning" 的 arXiv id 检索失败(2407.04442 是无关论文);NVIDIA NeMo Curator 博客只有搜索摘要级转述,无原句。
- Self-Instruct 生成数据的质量自评比例(正文 Table 2 为 92%/79%/58%/54% 语境)未完整摘录。
- Gerstgrasser 等作者机构(页面未显示,一般为 Stanford 系)未从一手页面确认。

## leads
- AZR 代码库(附录、uh-oh moment 全文、训练配置): https://github.com/LeapLabTHU/Absolute-Zero-Reasoner
- AZR 项目页(效果图表): https://andrewzh112.github.io/absolute-zero-reasoner/
- SEAL 项目页(数字与 self-edit 示例): https://jyopari.github.io/posts/seal
- RLHF Book 的 RLVR 章节定义(RLHF 去掉奖励模型换成可验证器): https://rlhfbook.com/c/07-reasoning
- DeepSeek-R1(Guo et al. 2025)大规模引用 RLVR 范式,可作燃料侧延续:arXiv 2501.12948
- "Arena Learning"(Amazon,虚拟竞技场合成数据飞轮)需重新定位正确 arXiv id(约 2407.01531,待验证)
- NVIDIA NeMo Curator 官方博客:合成数据已是 LLM 后训练标准环节的工具化表述(NVIDIA resources 页)
- Self-Rewarding 论文 PDF 的 Table(找 23.3%→39.7% LC AlpacaEval 口径出处)
- STaR v1 摘要(2022-03-28)与 ar5iv 现行版 diff,确认 60.2%→72.5% 是否存在于早期版本
- Gerstgrasser 正文实验曲线(replacement 下退化 vs accumulation 下稳定的量化图)
- Shumailov Nature 正文 "10% 原始数据保留" 实验细节段落
- SPIN 论文对迭代收益递减/自玩极限的讨论段(与 collapse 主题可勾连)
- Tulu 3 405B 表格数据与 RLVR 的 MATH/GSM8K 提升数
- SEAL 的 RL 训练 self-edit 生成策略(非纯 SFT)方法节: https://arxiv.org/html/2506.10943v2 Section 3
