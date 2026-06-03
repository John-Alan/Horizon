---
layout: default
title: "Horizon Summary: 2026-06-03 (ZH)"
date: 2026-06-03
lang: zh
---

> 从 22 条内容中筛选出 12 条重要资讯。

---

1. [反向传播在一轮训练中破坏 V1 脑对齐](#item-1) ⭐️ 9.0/10
2. [通过 VSCode 漏洞一键窃取 GitHub 令牌](#item-2) ⭐️ 8.0/10
3. [斯坦福研究显示 AI 表现优于法学教授](#item-3) ⭐️ 8.0/10
4. [微软发布 MAI-Thinking-1 和 MAI-Code-1-Flash 大语言模型](#item-4) ⭐️ 8.0/10
5. [MiniMax 推出 MSA：百万上下文，速度提升 4 倍](#item-5) ⭐️ 8.0/10
6. [PapersWithCode 复兴版新增 CVPR 2026 会议浏览功能](#item-6) ⭐️ 7.0/10
7. [在 Linux 上将 Nvidia GPU 显存用作交换空间](#item-7) ⭐️ 6.0/10
8. [CT 扫描揭示比亚迪汽车零部件质量](#item-8) ⭐️ 6.0/10
9. [用户因 AI 建议离开 Gmail，称赞 Fastmail](#item-9) ⭐️ 6.0/10
10. [使用 Clojure 一个月：结构化编辑与 REPL](#item-10) ⭐️ 6.0/10
11. [西雅图监控设施步行导览](#item-11) ⭐️ 6.0/10
12. [Datasette Agent MicroPython Alpha 发布](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [反向传播在一轮训练中破坏 V1 脑对齐](https://www.reddit.com/r/MachineLearning/comments/1tupu9z/backpropagation_destroys_v1_brain_alignment_in/) ⭐️ 9.0/10

一项新研究表明，反向传播（BP）在一个训练周期内破坏了 90%的 V1 脑对齐，而预测编码（PC）和 STDP 则保留了它，BP 的 RSA 相关性从 0.102 降至 0.011（p=0.031）。 这揭示了全局误差信号与早期视觉表征之间的根本权衡，挑战了监督训练改善脑对齐的假设，并表明生物合理的学习规则可能更适合建模早期视觉。 该研究在 40 个训练周期内追踪了 BP、反馈对齐（FA）、PC 和 STDP 在 8 个检查点的 RSA 对齐，每种规则使用 5 个种子；PC 和 STDP 稳定后仅下降 25-31%，而 FA 下降了 49%。

reddit · r/MachineLearning · /u/ConfusionSpiritual19 · 6月2日 12:43

**背景**: 表征相似性分析（RSA）衡量人工神经网络与 V1 等脑区之间神经表征的组织相似程度。反向传播使用全局误差信号更新权重，而预测编码和 STDP 依赖更符合生物合理性的局部学习规则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/nilsleut/learning-rules-rsa">nilsleut/learning-rules-rsa - GitHub</a></li>
<li><a href="https://arxiv.org/html/2605.30556v1">Supervised Training Rapidly Degrades Early Visual Cortex ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Spike-timing-dependent_plasticity">Spike-timing-dependent plasticity - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Reddit 讨论强调了种子间惊人的一致性（Cohen's d > 5）以及高层表征与早期视觉对齐之间的权衡。评论者还指出了 5 个种子的局限性（p ≈ 0.031），以及在 32×32 CIFAR-10 上训练、在 224×224 THINGS 上评估所带来的分辨率/领域偏移混淆。

**标签**: `#neuroscience`, `#backpropagation`, `#predictive coding`, `#brain alignment`, `#learning rules`

---

<a id="item-2"></a>
## [通过 VSCode 漏洞一键窃取 GitHub 令牌](https://blog.ammaraskar.com/github-token-stealing/) ⭐️ 8.0/10

安全研究员 Ammar Askar 披露了 VSCode 嵌入式网页编辑器（github.dev）中的一个漏洞，攻击者只需一次点击即可窃取 GitHub OAuth 令牌。该漏洞利用了编辑器加载任意扩展的能力，这些扩展可以访问已认证用户的令牌。 该漏洞突显了广泛使用的开发工具中的关键安全缺陷，可能使数百万开发者的 GitHub 账户面临被入侵的风险。披露还批评了微软安全响应中心（MSRC）对报告处理不当，引发了对 VSCode 及类似基于 Electron 的应用安全状况的担忧。 攻击通过诱使用户点击链接，在 github.dev 中打开恶意仓库，然后加载精心制作的扩展来窃取 OAuth 令牌。令牌存储在浏览器的 localStorage 中，可通过扩展的网络请求被窃取。

hackernews · ammar2 · 6月2日 15:29 · [社区讨论](https://news.ycombinator.com/item?id=48371562)

**背景**: VSCode 的网页版 github.dev 允许用户通过导航到任何 GitHub 仓库直接在浏览器中编辑代码。它通过 GitHub OAuth 进行用户认证，并将令牌存储在浏览器的 localStorage 中。VSCode 中的扩展可以访问 webview 并执行任意 JavaScript，从而读取令牌。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.ammaraskar.com/github-token-stealing/">1-Click GitHub Token Stealing via a VSCode Bug – Ammar's Blog</a></li>
<li><a href="https://code.visualstudio.com/api/extension-guides/webview">Webview API | Visual Studio Code Extension API</a></li>
<li><a href="https://github.com/coder/code-server/discussions/6623">Why I can't paste text of clipboard in the terminal of vscode embedded ...</a></li>

</ul>
</details>

**社区讨论**: 社区对微软的安全响应表示失望，用户指出 MSRC 经常静默修复漏洞而不承认研究人员。一些评论者赞扬研究人员在回应不佳的情况下仍提高了安全意识，而另一些人则猜测研究人员可能会被微软列入黑名单。

**标签**: `#security`, `#vscode`, `#github`, `#vulnerability`, `#bug bounty`

---

<a id="item-3"></a>
## [斯坦福研究显示 AI 表现优于法学教授](https://law.stanford.edu/press/ai-outperforms-law-professors-in-stanford-law-study/) ⭐️ 8.0/10

斯坦福法学院的一项研究发现，AI 模型（尤其是谷歌的 NotebookLM）在法律分析任务中表现优于法学教授，NotebookLM 的得分高于 Gemini 2.5 Pro 和人类教授。 这项研究挑战了关于 AI 在专业领域能力的假设，并表明 AI 可以作为法律教育中具有成本效益的辅导工具，可能降低法律培训的门槛。 该研究比较了 16 位法学教授与 AI 模型，但社区评论者指出教授间差异大且可能存在统计功效问题。NotebookLM 使用了额外法律资源，而 Gemini 2.5 Pro 未使用外部资源。

hackernews · berlianta · 6月2日 23:43 · [社区讨论](https://news.ycombinator.com/item?id=48377761)

**背景**: NotebookLM 是谷歌的一款研究工具，利用检索增强生成（RAG）帮助用户与文档交互。该研究聚焦于将 LLM 用作法律学生的辅导工具，而非替代律师。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NotebookLM">NotebookLM</a></li>
<li><a href="https://arxiv.org/abs/2510.07243">[2510.07243] LeMAJ (Legal LLM-as-a-Judge): Bridging Legal ... LeMAJ (Legal LLM-as-a-Judge): Bridging Legal Reasoning and ... Large Language Models in Legal Systems: A Survey - Nature Evaluating LLMs for Legal Workflows - emergentmind.com Efficient Large language model evaluation for legal tasks LegalAgentBench: Evaluating LLM Agents in Legal Domain A rapid evidence review of evaluation techniques for large ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论对该研究的方法论表示怀疑，指出教授间差异大且可能存在偏见。一些人注意到研究重点是辅导而非替代律师，而另一些人质疑 AI 在没有领域专业知识的情况下能否有效教学。

**标签**: `#AI`, `#legal tech`, `#LLM evaluation`, `#education`, `#research`

---

<a id="item-4"></a>
## [微软发布 MAI-Thinking-1 和 MAI-Code-1-Flash 大语言模型](https://simonwillison.net/2026/Jun/2/microsofts-new-models/#atom-everything) ⭐️ 8.0/10

微软宣布了两款新的大语言模型：MAI-Thinking-1，一个拥有 1 万亿参数、35 亿活跃参数的推理模型；以及 MAI-Code-1-Flash，一个拥有 1370 亿参数、50 亿活跃参数的代码模型，专为 GitHub Copilot 打造。 这些模型展示了微软利用混合专家架构推动高效、专业化大语言模型的努力，有望在保持竞争力的同时降低推理成本。代码模型集成到 GitHub Copilot 可能影响数百万开发者。 MAI-Thinking-1 仅对选定的早期合作伙伴开放，而 MAI-Code-1-Flash 正在向 VS Code 中的 GitHub Copilot 个人用户推出。两个模型均使用专有网络爬取和 Common Crawl 数据训练，并非最初猜测的仅使用许可数据。

rss · Simon Willison · 6月2日 22:21

**背景**: 混合专家架构是一种每次输入仅激活部分参数（专家）的架构，能够在较低计算成本下实现更大的总参数量。微软的模型使用 MoE 在保持高总参数的同时降低活跃参数，类似于 Qwen3.6-35B-A3B 等其他近期模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://microsoft.ai/news/introducing-mai-thinking-1/">Introducing MAI-Thinking-1 | Microsoft AI</a></li>
<li><a href="https://microsoft.ai/news/introducingmai-code-1-flash/">Introducing MAI - Code - 1 - Flash | Microsoft AI</a></li>

</ul>
</details>

**社区讨论**: 社区评论对模型性能表示怀疑，指出 MAI-Code-1-Flash 的 SWE-bench 得分（51%）仅略高于 Qwen3.6-35B-A3B（49.5%）。一些用户批评微软对 GitHub Copilot 的定价变更，并质疑小型代码模型在严肃编程任务中的实用性。

**标签**: `#AI`, `#LLM`, `#Microsoft`, `#reasoning`, `#code generation`

---

<a id="item-5"></a>
## [MiniMax 推出 MSA：百万上下文，速度提升 4 倍](https://www.reddit.com/r/MachineLearning/comments/1tvameq/minimax_dropped_a_new_attention_architecture_n/) ⭐️ 8.0/10

MiniMax 发布了一种名为 MiniMax Sparse Attention (MSA) 的新型稀疏注意力架构，该架构实现了原生 100 万 token 的上下文窗口，执行速度比 Flash-Sparse-Attention 快 4 倍，并将每个 token 的计算量降至前代模型的 1/20。 这一突破使长上下文大语言模型更加实用和经济，支持持续智能体执行和多模态推理等应用，同时是首个将前沿编码、百万上下文和原生多模态结合的开源权重模型。 MSA 采用“KV outer gather Q”方法，将 KV 块作为外层循环，确保连续内存访问且每个块仅读取一次，从而在完整百万上下文下实现 9 倍预填充加速和 15 倍解码加速。

reddit · r/MachineLearning · /u/superintelligence03 · 6月3日 01:26

**背景**: 标准注意力机制的计算复杂度随序列长度呈二次增长，使得长上下文计算成本高昂。稀疏注意力通过仅关注部分 token 来降低复杂度，但往往牺牲召回率。MSA 在操作符层面重构内存访问模式，改进了 Flash-Sparse-Attention 等先前稀疏方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.minimax.io/blog/minimax-m3">MiniMax M3: Frontier Coding, 1M Context, Native Multimodality — All...</a></li>
<li><a href="https://www.marktechpost.com/2026/06/01/minimax-releases-minimax-m3-with-msa-architecture-supporting-1m-token-context-native-multimodality-and-agentic-coding/">MiniMax Releases MiniMax M3 with MSA Architecture... - MarkTechPost</a></li>
<li><a href="https://www.reddit.com/r/LocalLLM/comments/1ttlmfy/thoughts_on_minimax_m3s_msa_minimax_sparse/">Thoughts on MiniMax M3's MSA (MiniMax Sparse Attention)? - Reddit</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的讨论内容充实，用户称赞其技术创新和性能提升。一些评论者质疑在极端长度下的实际召回质量，并将 MSA 与 MoBA 等其他稀疏方法进行比较，而另一些则强调开源权重发布是一项重要贡献。

**标签**: `#attention`, `#LLM`, `#context window`, `#efficiency`, `#open-weight`

---

<a id="item-6"></a>
## [PapersWithCode 复兴版新增 CVPR 2026 会议浏览功能](https://www.reddit.com/r/MachineLearning/comments/1tukrf4/browse_cvpr_2026_papers_on_paperswithcode_p/) ⭐️ 7.0/10

Hugging Face 的 Niels 宣布了 paperswithcode.co 的复兴，并新增了会议支持功能，用户可按任务、口头报告/亮点论文状态以及 GitHub 和 Hugging Face 资源链接浏览 CVPR 2026 论文。 此次复兴恢复了深受喜爱的 AI 研究前沿跟踪平台，会议浏览功能使研究人员更容易发现和访问 CVPR 论文及其相关代码和资源。 该平台索引了所有 CVPR 2026 论文及其 arXiv ID，按任务分类，并标记了 GitHub 链接、项目页面、Hugging Face 资源和评测结果。用户还可以按口头报告和亮点论文进行筛选。

reddit · r/MachineLearning · /u/NielsRogge · 6月2日 08:32

**背景**: PapersWithCode 曾是一个广受欢迎的网站，维护着各领域 AI 前沿技术的排行榜，但后来关闭了。Hugging Face 的 Niels Rogge 在 paperswithcode.co 上发起了社区驱动的复兴版，现在新增了会议支持功能，帮助研究人员跟踪 CVPR、NeurIPS 和 ICML 等主要 AI 会议的论文。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/nielsr/paperswithcode-launch">Relaunching PapersWithCode with new features - Hugging Face</a></li>
<li><a href="https://github.com/ooonesevennn/CVPR_2026_Oral_Papers">ooonesevennn/CVPR_2026_Oral_Papers - GitHub</a></li>
<li><a href="https://resources.paperdigest.org/2026/04/cvpr-2026-papers-highlights/">Paper Digest: CVPR 2026 Papers & Highlights – Resources ...</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的讨论是积极的，用户对复兴版和新的会议浏览功能表示赞赏。一些人表示希望看到支持更多会议和更多筛选选项。

**标签**: `#computer vision`, `#conference`, `#paperswithcode`, `#CVPR`, `#AI research`

---

<a id="item-7"></a>
## [在 Linux 上将 Nvidia GPU 显存用作交换空间](https://github.com/c0dejedi/nbd-vram) ⭐️ 6.0/10

一位开发者发布了 NBD-VRAM，这是一个开源工具，通过 NBD（网络块设备）接口，允许在 Linux 上将 Nvidia GPU 显存用作交换空间。 该工具为内存焊死且无法升级的笔记本电脑提供了一种扩展系统内存的新方法，但性能受限于 PCIe 带宽和延迟。 在 RTX 3070 笔记本 GPU 上，顺序吞吐量约为 1.3 GB/s，比典型的 NVMe SSD（约 2-3 GB/s）慢。该工具使用 NBD 将显存暴露为块设备用于交换。

hackernews · tanelpoder · 6月2日 22:55 · [社区讨论](https://news.ycombinator.com/item?id=48377404)

**背景**: 交换空间是当 RAM 满时用作虚拟内存的存储区域。NBD-VRAM 使用 GPU 显存作为交换，速度比 SSD 快，但由于 PCIe 开销比系统 RAM 慢。该工具是一个概念验证，不建议用于生产环境。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=48377404">Use your Nvidia GPU's VRAM as swap space on Linux - Hacker News</a></li>
<li><a href="https://www.phoronix.com/news/NVIDIA-NBD-VRAM">NBD-VRAM Provides Swap Space On Your NVIDIA GeForce GPUs</a></li>
<li><a href="https://www.reddit.com/r/linux/comments/1ttrwju/nbdvram_use_your_nvidia_gpus_vram_as_swap_space/">nbd-vram: Use your NVIDIA GPU's VRAM as swap space on Linux.</a></li>

</ul>
</details>

**社区讨论**: Hacker News 和 Reddit 上的评论强调了该工具的 niche 用例和性能限制。一些用户指出 Windows 和 AMD GPU 上存在类似项目，而另一些用户则质疑其在 PCIe 瓶颈下的实用性。

**标签**: `#Linux`, `#GPU`, `#swap`, `#performance`, `#Nvidia`

---

<a id="item-8"></a>
## [CT 扫描揭示比亚迪汽车零部件质量](https://www.lumafield.com/scan-of-the-month/byd) ⭐️ 6.0/10

Lumafield 发布了比亚迪汽车零部件的高分辨率 CT 扫描图像，包括钥匙、控制臂和动力总成部件，前所未有地展示了其内部结构和制造质量。 这通过提供比亚迪制造质量的客观视觉证据，挑战了外界对中国汽车制造业的负面看法，而媒体经常批评其质量问题。 扫描显示机械备用钥匙是拔出式而非铰链式，这一点在评论中得到了比亚迪车主的澄清。比亚迪约 75%的零部件自产，与特斯拉相当，并且高度垂直整合。

hackernews · viasfo · 6月2日 20:30 · [社区讨论](https://news.ycombinator.com/item?id=48375824)

**背景**: 工业 CT 扫描用于汽车制造中的质量控制、缺陷分析和设计验证。比亚迪是全球销量最大的电动汽车制造商，但在国际市场上曾面临质量投诉，因此这次独立检测值得关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://insideevs.com/news/712148/byd-quality-problems-hit-international-markets/">BYD’s Quality Problems Hit International Markets: Report</a></li>
<li><a href="https://4nsi.com/case-study-category/automotive/">Industrial CT Scanning for Automotive Parts | X-ray Inspection</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍称赞比亚迪的制造质量，一位高级技师指出其重型部件打破了“中国车质量差”的说法。一位比亚迪车主纠正了钥匙机制的细节，其他人则强调了比亚迪的垂直整合和组织创新。

**标签**: `#BYD`, `#CT scan`, `#automotive`, `#manufacturing`, `#EV`

---

<a id="item-9"></a>
## [用户因 AI 建议离开 Gmail，称赞 Fastmail](https://moddedbear.com/gmail-thinks-im-stupid-so-i-left) ⭐️ 6.0/10

一位用户公开宣布因对 Gmail 的 AI 驱动邮件建议感到不满而离开，转而使用 Fastmail，并称赞其速度和隐私功能。 这凸显了用户对电子邮件服务中 AI 功能日益增长的反感，以及对 Fastmail 等注重隐私的替代方案的需求增加。 Fastmail 提供与 Gmail 类似的功能，包括应用密码、掩码邮件和 iOS 集成，但日历缺少地址自动补全。用户指出 Gmail 的 AI 建议常常显得侵入且不必要。

hackernews · speckx · 6月2日 19:27 · [社区讨论](https://news.ycombinator.com/item?id=48375016)

**背景**: Gmail 集成了智能回复和帮我写等 AI 功能，这些功能会分析邮件内容以生成建议。谷歌表示，这一处理遵循现有的隐私保护措施，不会将邮件用于 AI 训练。Fastmail 是一款付费电子邮件服务，强调速度和隐私，提供掩码邮件以保护用户身份。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Fastmail">Fastmail - Wikipedia</a></li>
<li><a href="https://www.fastmail.com/features/">Better features - Fastmail</a></li>
<li><a href="https://mailmeteor.com/blog/how-to-use-ai-in-gmail">How to Use AI in Gmail (Gemini, Help Me Write, Smart Reply & More)</a></li>

</ul>
</details>

**社区讨论**: 评论者大多支持这一举动，一些人分享了自己因隐私原因离开 Gmail 的经历。一位用户称赞 Fastmail 的速度，另一位批评 AI 写邮件对母语者来说不必要。少数人指出谷歌地图仍然难以替代。

**标签**: `#email`, `#privacy`, `#AI`, `#Google`, `#Fastmail`

---

<a id="item-10"></a>
## [使用 Clojure 一个月：结构化编辑与 REPL](https://www.acdw.net/clojure/) ⭐️ 6.0/10

一位开发者分享了学习 Clojure 一个月后的初步体验和挑战，强调了结构化编辑和 REPL 驱动开发的重要性。 这篇反思凸显了 Clojure 独特的学习曲线，它要求学习者投入特定工具和工作流程，有助于新手了解预期。 作者指出，结构化编辑（如 slurp 和 barf 操作）以及在开发中使用 REPL 是 Clojure 中提高生产力的关键技能，与其他语言不同。

hackernews · speckx · 6月2日 19:56 · [社区讨论](https://news.ycombinator.com/item?id=48375393)

**背景**: Clojure 是一种运行在 JVM 上的现代 Lisp 方言，强调函数式编程。结构化编辑通常通过 Paredit 实现，帮助保持括号平衡并结构化地导航代码。REPL 驱动开发允许通过将代码片段发送到正在运行的运行时进行交互式编码，从而实现快速反馈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://clojure.org/guides/structural_editing">Clojure - Structural Editing</a></li>
<li><a href="https://danlebrero.com/2018/11/26/repl-driven-development-immediate-feedback-for-you-backend/">REPL driven development: immediate feedback for you backend code</a></li>

</ul>
</details>

**社区讨论**: 社区评论强调，学习结构化编辑和 REPL 使用对于 Clojure 的生产力至关重要。一位评论者指出，Clojure 的价值不仅限于 JVM，还扩展到 ClojureScript 和 ClojureDart 等多个平台。

**标签**: `#Clojure`, `#functional programming`, `#learning`, `#REPL`, `#Lisp`

---

<a id="item-11"></a>
## [西雅图监控设施步行导览](https://coveillance.org/a-walking-tour-of-surveillance-infrastructure-in-seattle/) ⭐️ 6.0/10

一次详细的步行导览记录了西雅图部署的各种监控技术，包括摄像头、传感器和数据收集系统，突出了它们的普遍性和设计。 这次导览引发了关于隐私和公民自由的辩论，展示了城市监控基础设施如何变得常态化，并引发了关于安全与自由之间权衡的质疑。 导览涵盖了具有不同“观看方式”的摄像头，这些方式强制执行社会规范；社区评论显示出不同的反应：一些人认为监控对控制犯罪是必要的，而另一些人则批评自由的丧失以及描述技术时使用的晦涩语言。

hackernews · eustoria · 6月2日 13:24 · [社区讨论](https://news.ycombinator.com/item?id=48369980)

**背景**: 城市监控基础设施包括闭路电视摄像头、自动车牌识别系统和枪声检测系统等技术。城市通常部署这些技术以增强公共安全，但引发了关于隐私、数据滥用和社会控制的担忧。西雅图因其科技产业和进步主义活动而成为此类辩论的焦点。

**社区讨论**: 评论者表达了不同观点：一些人支持将监控作为犯罪控制的工具，因为起诉缺乏证据；另一些人则批评自由的丧失以及使用学术术语使公众疏远。少数人强调了安全与自由之间的紧张关系，一位评论者愿意用部分自由换取安全。

**标签**: `#surveillance`, `#privacy`, `#urban technology`, `#Seattle`

---

<a id="item-12"></a>
## [Datasette Agent MicroPython Alpha 发布](https://simonwillison.net/2026/Jun/2/datasette-agent-micropython/#atom-everything) ⭐️ 6.0/10

Simon Willison 发布了 datasette-agent-micropython 0.1a0，这是一个 alpha 插件，利用 WebAssembly 沙箱安全执行 LLM 生成的 Python 代码。 这解决了 AI 代理中的一个关键安全挑战：安全运行 LLM 生成的代码。如果成功，它可以在不牺牲安全性的情况下，实现 Datasette 中更强大、更自主的数据探索。 该插件使用编译为 WebAssembly 的 MicroPython 来沙箱化代码执行，GPT-5.5 至今未能突破沙箱。它仍处于实验阶段，仅为 alpha 版本。

rss · Simon Willison · 6月2日 19:28

**背景**: Datasette Agent 是 Datasette 的 AI 助手，帮助用户探索和查询数据。WebAssembly 为不受信任的代码提供强大的隔离和沙箱功能，使其成为安全执行 AI 生成代码的有前途的方法。MicroPython 是 Python 3 的精简实现，专为微控制器和嵌入式系统设计，但也可以在 WebAssembly 环境中运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://agent.datasette.io/">Datasette Agent : an AI assistant for Datasette to help explore and...</a></li>
<li><a href="https://thenewstack.io/webassembly-sandboxing-ai-agents/">WebAssembly could solve AI agents' most dangerous security ...</a></li>

</ul>
</details>

**标签**: `#datasette`, `#sandboxing`, `#webassembly`, `#python`, `#llm`

---