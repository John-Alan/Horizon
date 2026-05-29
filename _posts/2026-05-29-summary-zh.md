---
layout: default
title: "Horizon Summary: 2026-05-29 (ZH)"
date: 2026-05-29
lang: zh
---

> 从 22 条内容中筛选出 15 条重要资讯。

---

1. [仅用 Postgres 即可实现持久化工作流](#item-1) ⭐️ 8.0/10
2. [GitHub 因零日 Windows 漏洞封禁安全研究员](#item-2) ⭐️ 8.0/10
3. [Anthropic 在 H 轮融资中实现 470 亿美元年化收入](#item-3) ⭐️ 8.0/10
4. [MONET：1.049 亿高质量图文数据集发布](#item-4) ⭐️ 8.0/10
5. [Wall-OSS-0.5：开源 4B VLA 模型，零样本机器人表现强劲](#item-5) ⭐️ 8.0/10
6. [更强 AI 模型在部署中可能老化更快](#item-6) ⭐️ 8.0/10
7. [Anthropic 发布 Claude Opus 4.8，带来小幅改进](#item-7) ⭐️ 7.0/10
8. [宿舍键盘项目成长为百万美元生意](#item-8) ⭐️ 7.0/10
9. [蓝色起源新格伦火箭静态点火测试中爆炸](#item-9) ⭐️ 7.0/10
10. [游戏模拟 AI 代理权限疲劳](#item-10) ⭐️ 7.0/10
11. [初创公司因在 Airbnb 秘密测试机器人被起诉](#item-11) ⭐️ 7.0/10
12. [互动文章批判 AI 自动化与财富不平等](#item-12) ⭐️ 7.0/10
13. [第二届 LLM 社会模拟研讨会将在 COLM 2026 举办](#item-13) ⭐️ 7.0/10
14. [uv 0.11.17 发布，新增诊断和 workspace 支持](#item-14) ⭐️ 6.0/10
15. [《创：战纪》中的 Shell 历史场景细节剖析](#item-15) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [仅用 Postgres 即可实现持久化工作流](https://www.dbos.dev/blog/postgres-is-all-you-need-for-durable-execution) ⭐️ 8.0/10

DBOS 的一篇博文认为，仅靠 Postgres 就能为构建持久化工作流提供坚实基础，挑战了对 Temporal 或 Restate 等专用工作流引擎的需求。 这种方法可以通过减少对外部工作流系统的依赖来简化架构，可能降低开发者在构建可靠分布式应用时的成本和运维复杂性。 文章引用了 Armin Ronacher 的'absurd'项目，该项目直接在 Postgres 上实现了持久化工作流，并将 DBOS 与 Temporal、Restate 和 Cloudflare Workflows 等其他解决方案进行了比较。

hackernews · KraftyOne · 5月28日 18:41 · [社区讨论](https://news.ycombinator.com/item?id=48313530)

**背景**: 持久化工作流（或持久化执行）允许长时间运行的函数在崩溃或重启后不丢失状态。传统上使用 Temporal 等专用工作流引擎，但有人认为，通过合理设计，像 Postgres 这样的关系型数据库也能处理相同任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.hatchet.run/v1/durable-workflows-overview">Durable Workflows - Hatchet Documentation</a></li>
<li><a href="https://lucumr.pocoo.org/2025/11/3/absurd-workflows/">Absurd Workflows : Durable Execution With Just Postgres</a></li>
<li><a href="https://github.com/meirwah/awesome-workflow-engines">meirwah/awesome-workflow-engines - GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区评论重点比较了 Temporal、Restate 和 Cloudflare Workflows，用户分享了实际经验。一些人注意到使用 Postgres 的简便性，而另一些人则提醒注意潜在的扩展限制。

**标签**: `#Postgres`, `#durable workflows`, `#database`, `#software engineering`, `#distributed systems`

---

<a id="item-2"></a>
## [GitHub 因零日 Windows 漏洞封禁安全研究员](https://www.tomshardware.com/tech-industry/cyber-security/microsofts-github-bans-security-researcher-who-posted-zero-day-windows-exploits-because-company-ruined-their-life-expert-claims-action-is-vindictive-and-promises-further-retaliation) ⭐️ 8.0/10

GitHub 封禁了一名发布 Windows 零日漏洞的安全研究员，理由是其违反了可接受使用政策。该研究员声称微软毁了他的生活，并承诺将进一步报复。 这一事件凸显了漏洞赏金计划与平台政策之间的紧张关系，可能阻碍研究人员报告漏洞。它还引发了关于科技巨头如何处理安全披露和研究员报复的质疑。 该研究员发布了 Windows 零日漏洞利用代码，GitHub 在封禁账户前删除了这些内容。微软和 GitLab 也封禁了该研究员，表明跨平台采取了协调行动。

hackernews · possibilistic · 5月28日 21:45 · [社区讨论](https://news.ycombinator.com/item?id=48315968)

**背景**: 零日漏洞是指软件厂商未知的漏洞，攻击者可在补丁发布前利用它。漏洞赏金计划奖励负责任披露此类缺陷的研究人员，但公开发布漏洞利用代码可能违反平台规则并助长恶意使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zero-day_exploit">Zero-day exploit</a></li>
<li><a href="https://en.wikipedia.org/wiki/Bug_bounty_program">Bug bounty program</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：一些人认为微软处理不当并会后悔，另一些人则认为该研究员行为失常。有人猜测研究员的动机以及是否违反了平台规则。

**标签**: `#security`, `#zero-day`, `#GitHub`, `#Microsoft`, `#bug bounty`

---

<a id="item-3"></a>
## [Anthropic 在 H 轮融资中实现 470 亿美元年化收入](https://simonwillison.net/2026/May/29/anthropic/#atom-everything) ⭐️ 8.0/10

Anthropic 宣布完成 650 亿美元的 H 轮融资，并披露其年化收入已突破 470 亿美元，较 2025 年底的 90 亿美元和 2026 年 4 月的 300 亿美元大幅增长。 这种爆炸性的收入增长——短短几个月内从 90 亿美元增至 470 亿美元——标志着企业 AI 采用率空前高涨，重塑了市场格局，使 Anthropic 成为 AI 行业的主导力量。 年化收入是基于最近一个月收入乘以 12 的年化预测。470 亿美元的数字是在 H 轮融资公告中披露的，该公司此前在 2026 年 2 月和 4 月分别报告了 140 亿美元和 300 亿美元。

rss · Simon Willison · 5月29日 01:23

**背景**: 年化收入是一种财务指标，通过将当前短期收入外推来估算年度业绩，常被快速增长的公司用于展示发展势头。Anthropic 一直在融资公告中分享这一指标，向投资者提供透明度。该公司的快速增长反映了对企业 AI 解决方案（尤其是其 Claude 模型）的激增需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://corporatefinanceinstitute.com/resources/accounting/revenue-run-rate/">Revenue Run Rate - Definition, Calculation, Examples</a></li>
<li><a href="https://www.investopedia.com/terms/r/runrate.asp">Run Rate Explained: Benefits, Risks, and Business Insights</a></li>
<li><a href="https://finance.yahoo.com/sectors/technology/articles/anthropic-raises-65b-series-h-184801308.html">Anthropic raises $65B in Series H funding at $965B valuation</a></li>

</ul>
</details>

**社区讨论**: 一些怀疑论者质疑自我报告的年化收入数字的可靠性，但作者认为，考虑到 650 亿美元的融资，撒谎将构成证券欺诈。Ed Zitron 此前对 300 亿美元的数字表示极度怀疑，他是否会更新观点仍有待观察。

**标签**: `#Anthropic`, `#AI industry`, `#revenue`, `#funding`, `#enterprise AI`

---

<a id="item-4"></a>
## [MONET：1.049 亿高质量图文数据集发布](https://www.reddit.com/r/MachineLearning/comments/1tq2vxa/a_new_dataset_with_more_that_100m_hiquality/) ⭐️ 8.0/10

MONET 数据集以 Apache 2.0 许可证在 Hugging Face 上发布，包含 1.049 亿个高质量图文对，附带标题和元数据，并提供了论文、UMAP 可视化、检索工具和训练代码库。 这一大规模高质量数据集为训练和评估提供了免费资源，可显著推动文本到图像生成和多模态研究，有望减少对专有数据集的依赖。 该数据集从 29 亿张图像中精选至 1.049 亿个高质量样本，并附带配套工具：用于可视化的 UMAP、用于文本或图像搜索的检索工具，以及基于 MONET 训练文本到图像模型的代码库。

reddit · r/MachineLearning · /u/dh7net · 5月28日 12:59

**背景**: 大规模图文数据集对于训练现代文本到图像模型（如 Stable Diffusion 和 DALL-E）至关重要。然而，许多现有数据集存在噪声多、质量低或许可证限制等问题。MONET 旨在通过提供干净、开源的替代方案来解决这些问题。

**标签**: `#dataset`, `#text-to-image`, `#multimodal`, `#open-source`, `#machine learning`

---

<a id="item-5"></a>
## [Wall-OSS-0.5：开源 4B VLA 模型，零样本机器人表现强劲](https://www.reddit.com/r/MachineLearning/comments/1tq8v8m/walloss05_4b_vla_with_open_training_code_and/) ⭐️ 8.0/10

X Square Robot 发布了 Wall-OSS-0.5，这是一个基于 3B VLM 骨干网络和混合 Transformer 架构的 4B 视觉-语言-动作（VLA）模型，并提供了开源训练代码和零样本真实机器人评估结果。 该发布通过提供一个在零样本和微调设置中均优于 pi0.5 的强 VLA 基线，推动了开源机器人学的发展，开源训练代码使更广泛的社区能够复现和创新。 该模型使用视觉对齐的 RVQ 分词器处理离散动作令牌，并使用流匹配处理连续动作，梯度桥接显示动作令牌交叉熵主导骨干网络更新。它还采用了分布式 Muon 优化器 DMuon，声称能显著降低开销。

reddit · r/MachineLearning · /u/Tall-Peak2618 · 5月28日 16:37

**背景**: 视觉-语言-动作（VLA）模型整合视觉、语言和动作模态用于机器人控制。混合 Transformer（MoT）是一种稀疏架构，将计算分配给多个专家，降低预训练成本。流匹配是一种生成方法，通过速度场将噪声映射到动作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Vision-language-action_model">Vision-language-action model - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2411.04996">[2411.04996] Mixture - of - Transformers : A Sparse and Scalable...</a></li>
<li><a href="https://www.emergentmind.com/topics/flow-matching-transformer-action-head">Flow - Matching Transformer Action Head</a></li>

</ul>
</details>

**社区讨论**: 社区对梯度桥接消融实验和 DMuon 优化器的声称提出了技术性质疑，希望其他 VLA 从业者验证。用户还询问视觉对齐的 RVQ 分词是否在本论文之外明显优于 FAST 风格的分词，并呼吁在真实硬件上进行第三方复现。

**标签**: `#VLA`, `#robotics`, `#open-source`, `#machine learning`, `#real-robot evaluation`

---

<a id="item-6"></a>
## [更强 AI 模型在部署中可能老化更快](https://www.reddit.com/r/MachineLearning/comments/1tqaoio/your_agents_are_aging_too_agent_lifespan/) ⭐️ 8.0/10

一项名为 AgingBench 的新基准测试发现，在 Claude Code CLI 代理中将更强模型（Opus 4.7）替换为较弱模型（Sonnet 4.6）后，长期部署中的 PyTest 通过率下降了 15%，挑战了更强模型在长期部署中表现更好的假设。 这一发现意义重大，因为它表明仅凭模型能力并不能保证长期可靠性；记忆状态演变和维护策略起着更大的作用。这影响到所有部署长期 AI 代理的人，表明简单地换用新模型可能会降低性能。 该基准测试衡量了不同场景下的代理半衰期，仅记忆策略就导致了 4.5 倍的半衰期差异，大于任何模型替换的影响。论文提出了代理寿命工程（ALE）这一新领域，用于测量、诊断和修复长期运行代理系统的退化。

reddit · r/MachineLearning · /u/CategoryNormal149 · 5月28日 17:41

**背景**: 长期 AI 代理越来越多地被部署为持久化系统，但它们仍像刚初始化的模型一样被评估。单日基准测试忽略了代理的记忆状态在多次会话中因压缩、干扰、修订和维护冲击而演变的方式。代理寿命工程（ALE）通过关注纵向可靠性来填补这一空白。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://agingbench.github.io/">AgingBench: AI Agents Age Too</a></li>
<li><a href="https://arxiv.org/abs/2605.26302">[2605.26302] Your Agents Are Aging Too: Agent Lifespan Engineering for Deployed Systems</a></li>
<li><a href="https://arxiv.org/html/2605.26302">Your Agents Are Aging Too: Agent Lifespan Engineering for Deployed Systems</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的讨论内容充实，用户们就反直觉的结果展开辩论并分享类似经验。一些人质疑退化是由于模型架构还是记忆策略，另一些人则强调 ALE 对生产系统的实际重要性。

**标签**: `#AI agents`, `#deployment`, `#benchmark`, `#model aging`, `#software engineering`

---

<a id="item-7"></a>
## [Anthropic 发布 Claude Opus 4.8，带来小幅改进](https://www.anthropic.com/news/claude-opus-4-8) ⭐️ 7.0/10

Anthropic 发布了其旗舰模型 Claude Opus 4.8 的小幅更新，改进了编码性能，并允许在网页界面中禁用自适应思考功能。 此次发布表明 Anthropic 致力于迭代改进，回应了社区对 Opus 4.7 的反馈，并为从业者提供了一个更可控、更强大的模型，用于复杂编码任务。 Opus 4.8 被描述为相比前代有“适度但切实的改进”，早期编码评估显示它能以更少的错误实现复杂功能。用户现在可以禁用自适应思考功能，该功能此前有时会导致输出质量不佳。

hackernews · craigmart · 5月28日 16:49 · [社区讨论](https://news.ycombinator.com/item?id=48311647)

**背景**: 自适应思考是大语言模型中的一种机制，用于动态决定何时进行扩展推理或思维链处理。在之前的 Claude 版本中，该功能无法关闭，有时会导致输出质量不一致。现在可以禁用它，让用户对模型行为有更多控制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/TianhaoTonyWu/Awesome-Adaptive-Thinking-Papers">GitHub - TianhaoTonyWu/Awesome- Adaptive - Thinking -Papers</a></li>
<li><a href="https://newsletter.tensorteach.ai/p/reinforcement-trained-reasoners-teacher-hints-and-adaptive-thinking-three-paths-to-smarter-llms-3c81">Reinforcement Trained Reasoners, Teacher Hints, and Adaptive ...</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体积极，用户指出 Opus 4.8 回应了 Opus 4.7 引发的反弹。一些用户报告在编码基准测试中取得显著改进，例如构建简单的即时战略游戏，而另一些用户则对能够禁用自适应思考表示赞赏。少数评论者认为这些改进是渐进式的，而非突破性的。

**标签**: `#AI`, `#LLM`, `#Anthropic`, `#Claude`, `#model release`

---

<a id="item-8"></a>
## [宿舍键盘项目成长为百万美元生意](https://nick.winans.io/blog/nice-nano/) ⭐️ 7.0/10

一位开发者将在宿舍启动的分体式键盘控制器项目，到 2025 年发展成为收入超过一百万美元的产品。 这个故事表明，小众硬件 DIY 项目可以发展为可持续的业务，激励机械键盘社区的其他创客和创业者。 该产品 Nice!Nano 是一款支持无线连接和 QMK 固件的分体式键盘控制器，面向人体工学键盘爱好者。

hackernews · mattrighetti · 5月28日 20:25 · [社区讨论](https://news.ycombinator.com/item?id=48314951)

**背景**: 分体式键盘将键盘分为两半以提供人体工学优势，每半需要控制器进行管理。QMK 是广泛用于自定义键盘的开源固件，团购是机械键盘社区常见的预售模式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.qmk.fm/features/split_keyboard">Split Keyboard | QMK Firmware</a></li>
<li><a href="https://www.reddit.com/r/MechanicalKeyboards/comments/axjh17/working_on_my_split_keyboard_controller/">r/MechanicalKeyboards on Reddit: Working on my split keyboard controller</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了对这一成功的钦佩，许多人表示自己是早期客户。几位评论者请求更多关于营销策略和项目如何扩展的细节，还有一位分享了一个类似项目因专利问题失败的警示故事。

**标签**: `#hardware`, `#entrepreneurship`, `#keyboard`, `#DIY`, `#success-story`

---

<a id="item-9"></a>
## [蓝色起源新格伦火箭静态点火测试中爆炸](https://twitter.com/nasaspaceflight/status/2060164928472854821) ⭐️ 7.0/10

蓝色起源的新格伦火箭在卡纳维拉尔角进行全时长静态点火测试时爆炸，导致发射台和基础设施严重损坏。无人受伤。 此次事故可能导致蓝色起源的发射运营推迟一年以上，影响其商业和政府合同。同时也引发了对大型甲烷燃料火箭安全性的质疑。 火箭当时加注了约 1000 吨甲烷，爆炸能量堪比小型核武器。发射基础设施遭受大面积损坏，需要长时间修复。

hackernews · enraged_camel · 5月29日 01:16 · [社区讨论](https://news.ycombinator.com/item?id=48317774)

**背景**: 静态点火测试是常规发射前程序，火箭发动机在箭体固定于发射台时点火，以验证发动机性能和系统。新格伦是蓝色起源的重型轨道火箭，设计为部分可重复使用，能够将有效载荷送入轨道。甲烷是常见的火箭燃料，但由于其低温特性和高能量密度，存在独特风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cbsnews.com/news/blue-origin-new-glenn-rocket-explodes-launchpad-florida/">Blue Origin New Glenn rocket explodes on launch pad in Florida - CBS News</a></li>
<li><a href="https://en.wikipedia.org/wiki/New_Glenn">New Glenn - Wikipedia</a></li>
<li><a href="https://www.blueorigin.com/new-glenn">New Glenn | Blue Origin</a></li>

</ul>
</details>

**社区讨论**: 评论者对基础设施的严重损坏表示担忧，并估计需要一年以上的修复时间。有人指出爆炸能量相当于小型原子弹，也有人将其与中国近期一次静态点火中火箭升空的事故相比较。

**标签**: `#space`, `#rocket`, `#Blue Origin`, `#accident`, `#infrastructure`

---

<a id="item-10"></a>
## [游戏模拟 AI 代理权限疲劳](https://llmgame.scalex.dev/) ⭐️ 7.0/10

一款名为“Continue? Y/N”的 60 秒游戏已在 llmgame.scalex.dev 上线，模拟反复批准或拒绝 AI 代理权限请求的过程，以突出权限疲劳问题。 该游戏引发了对一个日益严重的现实问题的关注：由于疲劳，用户批准了约 93%的 AI 代理提示，从而带来安全风险。它引发了关于 AI 工具中生产力与安全性平衡的讨论。 游戏呈现一系列权限请求（如读取~/.zshrc、运行 lsof），玩家需快速决定批准或拒绝。评论指出，拒绝所有请求可获得完美安全分数，但可能忽略细微风险。

hackernews · Wirbelwind · 5月28日 13:02 · [社区讨论](https://news.ycombinator.com/item?id=48308376)

**背景**: AI 代理通常需要权限来执行命令或访问文件，导致频繁的批准提示。这可能导致“批准疲劳”，用户不加思考地批准请求，从而削弱安全性。该游戏以浓缩形式模拟了这一困境。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reddit.com/r/ClaudeAI/comments/1tq3eb5/continue_yn_a_60second_game_about_ai_agent/">Continue? Y/N: A 60-second game about AI agent permission fatigue</a></li>
<li><a href="https://medium.com/@naman12345/the-coming-approval-exhaustion-of-agentic-ai-5338d993349f">The Coming Approval Exhaustion of Agentic AI | by Naman Bhansali</a></li>
<li><a href="https://unit42.paloaltonetworks.com/navigating-security-tradeoffs-ai-agents/">Navigating Security Tradeoffs of AI Agents</a></li>

</ul>
</details>

**社区讨论**: 评论褒贬不一：一些人称赞游戏的创意和相关性，而另一些人则批评其安全假设（例如，将秘密存储在~/.zshrc 中是不良实践）。一些人指出，拒绝所有请求是一种可行策略，但缺乏细微差别，并且通过 lsof 杀死进程可能很危险。

**标签**: `#AI`, `#security`, `#game`, `#permission fatigue`, `#developer tools`

---

<a id="item-11"></a>
## [初创公司因在 Airbnb 秘密测试机器人被起诉](https://sfstandard.com/2026/05/28/sf-startup-secretly-testing-robots-airbnbs-trashing-lawsuit-claims/) ⭐️ 7.0/10

由前特斯拉和 Cruise 员工创立的旧金山初创公司 The Bot Company 被起诉，指控其以虚假借口租用 Airbnb 来测试家用机器人，并造成财产损坏。 此案引发了关于初创公司如何测试新兴技术的严重伦理和法律问题，尤其是在未经知情同意的情况下进入私人住宅，可能为机器人测试的问责制树立先例。 诉讼称，冰箱搁架破裂，碎盘子留在垃圾处理器中，木质床头柜抽屉有缺口。该初创公司估值 20 亿美元，已获得数亿美元风险投资。

hackernews · drewda · 5月28日 23:42 · [社区讨论](https://news.ycombinator.com/item?id=48317093)

**背景**: The Bot Company 正在开发用于家务的机器人，这需要大量的真实环境测试。然而，未经明确许可在私人住宅进行测试引发了隐私和财产权问题。该公司创始人具有自动驾驶汽车背景，该领域在测试期间也曾面临公众审查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://plato.stanford.edu/entries/ethics-ai/">Ethics of Artificial Intelligence and Robotics (Stanford Encyclopedia of Philosophy)</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了愤怒，有人指出该初创公司正在‘将愿景的成本转嫁给社会其他人’。还有人呼吁对以虚假借口预订的员工提起指控。一些人注意到机器人在被训练做家务时却损坏财产的讽刺意味。

**标签**: `#robotics`, `#startup`, `#ethics`, `#AI`, `#privacy`

---

<a id="item-12"></a>
## [互动文章批判 AI 自动化与财富不平等](https://permanent-upper-crow.jasonwu.ink/) ⭐️ 7.0/10

一篇名为《永久的上层乌鸦》的互动文章，通过游戏式隐喻批判 AI 驱动的自动化和炫耀性消费，认为这种动态会催生一个永久的上层阶级。 这篇创意作品引发了科技界对 AI 和自动化伦理问题的共鸣，促使人们反思社会不平等和“内卷”心态。 文章包含 106 位 CEO/公司，到 107 时循环，由 whiteblossom 一时兴起创作。作者也是一家旨在自动化体力工作的 AI 初创公司的联合创始人，增添了讽刺意味。

hackernews · whiteblossom · 5月28日 15:23 · [社区讨论](https://news.ycombinator.com/item?id=48310280)

**背景**: 文章通过一个游戏让玩家通过炫耀性消费积累财富，说明追求地位商品如何使人陷入工作与消费的循环。它批判了 AI 自动化必然导致永久底层阶级的观点，并与“被提”等宗教概念相类比。

**社区讨论**: 评论者注意到作者作为 AI 初创公司联合创始人的讽刺性，并讨论了经济是否为零和博弈。一些人认为，退出炫耀性消费才是唯一的获胜之道。

**标签**: `#AI`, `#societal impact`, `#automation`, `#inequality`, `#interactive fiction`

---

<a id="item-13"></a>
## [第二届 LLM 社会模拟研讨会将在 COLM 2026 举办](https://www.reddit.com/r/MachineLearning/comments/1tqhdoe/social_simulation_with_llms_fidelity_in/) ⭐️ 7.0/10

第二届 LLM 社会模拟研讨会（Social Sim'26）已公布，投稿截止日期为 2026 年 6 月 23 日，主题聚焦应用中的保真度，从演示转向严格评估和真实世界验证。 该研讨会解决了基于 LLM 的社会模拟中的一个关键缺口——确保模拟社会对治理和政策分析等真实应用具有保真度和实用性。 研讨会征集关于模拟评估、真实数据验证、智能体与角色建模、文化演化及伦理影响等主题的投稿，截止日期为 2026 年 6 月 23 日（AoE）。

reddit · r/MachineLearning · /u/RSTZZZ · 5月28日 21:38

**背景**: 基于 LLM 的社会模拟利用大语言模型创建在数字社会中互动的智能体，从而研究社会动态、信息传播和集体行为。然而，确保这些模拟忠实于真实世界现象仍是一个挑战，本次研讨会旨在解决这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://colmweb.org/">COLM 2025</a></li>
<li><a href="https://arxiv.org/html/2605.00197">The Silicon Society Cookbook: Design Space of LLM - based Social ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#social simulation`, `#workshop`, `#fidelity`, `#AI evaluation`

---

<a id="item-14"></a>
## [uv 0.11.17 发布，新增诊断和 workspace 支持](https://github.com/astral-sh/uv/releases/tag/0.11.17) ⭐️ 6.0/10

uv 0.11.17 为 `uv add` 添加了标准库模块的诊断功能，在帮助输出中公开了 `uv workspace` 子命令，并为 uv-build 增加了 PEP 794 支持。 这些改进通过提供更清晰的错误信息和更好的 workspace 管理，增强了开发者体验，使 uv 在 Python 项目工作流中更加健壮。 该版本还包括直接 URL 的离线锁新鲜度检查、`--no-editable-package` 标志，以及多项错误修复，例如改进了大型 `tool.uv.conflicts` 条目的性能。

github · github-actions[bot] · 5月28日 20:41

**背景**: uv 是一个用 Rust 构建的快速 Python 包管理器和工具链，旨在作为 pip 和 pip-tools 的直接替代品。Workspace 允许在单个项目中管理多个相关的 Python 包，而 uv-build 是一个构建后端，支持用于命名空间包的 PEP 794。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.astral.sh/uv/concepts/projects/workspaces/">Using workspaces | uv</a></li>
<li><a href="https://docs.astral.sh/uv/concepts/build-backend/">Build backend | uv</a></li>

</ul>
</details>

**标签**: `#python`, `#package-manager`, `#uv`, `#release`

---

<a id="item-15"></a>
## [《创：战纪》中的 Shell 历史场景细节剖析](https://www.chiark.greenend.org.uk/~sgtatham/quasiblog/tron-legacy/) ⭐️ 6.0/10

一篇对 2010 年电影《创：战纪》中 Shell 历史场景的详细技术分析揭示了多处不准确之处和隐藏彩蛋，例如虚假命令和不切实际的进程管理。 该分析突显了流行文化中常对技术进行错误呈现，但也展示了电影制作人在创造可信界面上的努力，引发了技术爱好者对媒体中真实性的讨论。 场景中出现了如'kill -9 1'（会导致系统崩溃）和'login -n root'（语法错误）等命令。彩蛋包括对'hanoi-unix'和'backdoor'登录的引用。

hackernews · speckx · 5月28日 19:15 · [社区讨论](https://news.ycombinator.com/item?id=48314002)

**背景**: 类 Unix 系统中的 Shell 历史命令记录终端中键入的命令。《创：战纪》中有一个角色滚动查看 Shell 历史的场景，作者对其技术准确性进行了分析。该片是 1982 年电影《电子世界争霸战》的续集，故事发生在计算机世界内部。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=48314002">Nitpicking the shell history scene in ' Tron : Legacy ' | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tron">Tron - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，在电影语境中杀死进程可能代表阻止像 Clu 这样的角色，并指出 Dillinger 使用 Emacs 而 Flynn 使用 vi，反映了特效艺术家的偏好。Daft Punk 的原声带也被赞为杰作。

**标签**: `#pop culture`, `#shell history`, `#Tron`, `#Easter eggs`, `#technical analysis`

---