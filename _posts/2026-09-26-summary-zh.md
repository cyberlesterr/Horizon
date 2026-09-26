---
layout: default
title: "Horizon Summary: 2026-09-26 (ZH)"
date: 2026-09-26
lang: zh
---

> 从 43 条内容中筛选出 6 条重要资讯。

---

1. [Go 团队提出实验性的平台无关 SIMD 方案](#item-1) ⭐️ 8.0/10
2. [美国上诉法院维持五角大楼对 Anthropic 的供应链风险认定](#item-2) ⭐️ 8.0/10
3. [陶哲轩：社会将需要多得多的数学家](#item-3) ⭐️ 8.0/10
4. [Ollaya：为开源 Jev 式决策模型提供 Ollama 风格本地推理](#item-4) ⭐️ 7.0/10
5. [John Gruber 警告 Meta Muse 强大却暗藏风险](#item-5) ⭐️ 7.0/10
6. [文件通知攻击：跨操作系统通知 API 的侧信道信息泄漏](#item-6) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Go 团队提出实验性的平台无关 SIMD 方案](https://go.dev/blog/simd-experiment) ⭐️ 8.0/10

Go 团队在官方博客上发布了一项关于平台无关 SIMD 的实验性提案，让开发者只需编写一次向量运算代码，就能由编译器映射到不同 CPU 架构的向量指令上。该消息在 Hacker News 上引发热烈讨论（344 分、132 条评论），人们将其与 C++ 的 std::simd、WebAssembly SIMD 以及 Mojo 进行了对比。 Go 广泛应用于后端服务、网络与数据处理，但目前要写出高性能的向量化代码仍必须手写汇编或使用不可移植的 intrinsic；一个标准库级别的 SIMD 包将能为图像处理、编解码、密码学等场景的热点循环带来显著收益，同时保持代码的可移植性。这同时也是一个语言设计层面的信号：目前很少有语言在标准库中内置 SIMD 支持，而 Go 选择的“非固定宽度向量”模型可能影响未来可移植 SIMD API 的设计方向。 这是一个实验性项目，而非已正式发布的语言特性，因此 API 与性能表现仍可能变化。在一项由社区成员提供的基准测试中（在浏览器内通过 WASM 对图片做纯本地换色处理），可移植 SIMD 比不可移植的 archsimd 慢约 11%，但两者都比非 SIMD 版本快约 5 倍。值得注意的是，有评论指出该设计在近期众多可移植 SIMD 方案中，首次更自然地支持了 Arm SVE 和 RISC-V RVV 这类非固定宽度向量指令集。

hackernews · yurivish · 9月25日 11:47 · [社区讨论](https://news.ycombinator.com/item?id=49843269)

**背景**: SIMD（单指令多数据）是指用一条 CPU 指令同时处理多个数据元素，编译器和库正是借助它来加速对数组的循环运算。传统上它要么以绑定特定指令集的固定宽度 intrinsic 形式出现（x86 的 SSE/AVX、Arm 的 NEON），要么依赖编译器自动向量化；但 Arm SVE 和 RISC-V RVV 等较新的架构采用长度仅在运行时才确定的可伸缩向量，使固定宽度的代码难以适配。其他生态也在朝类似方向发展：C++ 正在引入 std::simd，WebAssembly 提供 128 位固定宽度 SIMD，Mojo 则提供由编译期参数 N 决定长度的向量；而 Go 的方案描述的是一种宽度不在编译期固定的向量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_(programming_language)">Mojo (programming language)</a></li>
<li><a href="https://www.stonybrook.edu/commcms/ookami/support/_docs/3+-+Intro+to+SVE.pdf">Arm SVE Fundamentals</a></li>
<li><a href="https://docs.riscv.org/reference/isa/extensions/vector/_attachments/riscv-v-spec.pdf">[PDF] RISC-V "V" Vector Extension - riscv.org</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的整体情绪是正面且相当技术性的。有评论者分享了 WASM 换色基准测试，显示可移植 SIMD 比不可移植 SIMD 慢约 11%，但比标量代码快约 5 倍；也有人称赞该设计是首个让 SVE、RISC-V RVV 这类非固定宽度指令集更容易支持的可移植 SIMD 方案。此外，评论者还对比了三种架构思路——WebAssembly 固定 4 个 float32、Mojo 以编译期参数 N 决定 float32 数量、Go 则不固定向量宽度——并指出 C++ 的 std::simd 以及标准库对 SIMD 支持的增多反映了整个行业的趋势。

**标签**: `#Go`, `#SIMD`, `#performance`, `#compilers`, `#programming-languages`

---

<a id="item-2"></a>
## [美国上诉法院维持五角大楼对 Anthropic 的供应链风险认定](https://www.cnbc.com/2026/09/25/pentagon-anthropic-ai-risk-appeals-court.html) ⭐️ 8.0/10

2026 年 9 月 25 日，美国联邦上诉法院维持了五角大楼将人工智能公司 Anthropic 认定为“供应链风险”的决定，驳回了阻止该禁令的请求。此前，五角大楼已于 2026 年 3 月初正式通知 Anthropic，其被列入供应链风险名单。 据报道，这是这项原本用于防范外国对手的认定首次被用来对付一家美国本土公司，从而为美国政府限制 AI 采购树立了先例。这可能重塑 AI 实验室与军方就使用护栏进行谈判的方式，并加剧外界对国家安全生产采购规则被政治化利用的担忧。 尽管“供应链风险”这一标签已存在多年，但在五角大楼对 Anthropic 采取行动之前，从未被用于任何一家美国公司。上诉法院只是拒绝阻止该认定，而非就实体问题作出最终裁决，这意味着围绕 Anthropic 拒绝向国防部提供无限制模型访问权的争议很可能还将继续。

hackernews · cramer4next · 9月25日 15:29 · [社区讨论](https://news.ycombinator.com/item?id=49845977)

**背景**: “供应链风险”认定是一种法律层面的采购工具，允许美国政府将某家供应商排除在军事和联邦供应链之外，历史上主要针对与外国对手有关联的实体。Anthropic 是一家领先的 AI 实验室，会在其模型的使用方式中嵌入技术性和政策性的护栏（guardrails），据称它希望对自主武器或目标选择等军事用途施加限制。而越来越依赖商业 AI 供应商完成各类任务的五角大楼拒绝了这些条件，转而将 Anthropic 彻底排除出供应链。因此，这场争议处于 AI 安全政策、国防采购法律与国家安全权力的交汇点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://abcnews.com/Business/anthropic-appeals-court-declines-block-pentagon-blacklisting/story?id=136755690">Federal appeals court upholds Pentagon designation of Anthropic as supply chain risk - ABC News</a></li>
<li><a href="https://qz.com/pentagon-supply-chain-risk-designation-history-anthropic-052726">Pentagon supply chain risk designation history explained</a></li>
<li><a href="https://www.cnbc.com/2026/09/25/pentagon-anthropic-ai-risk-appeals-court.html">U.S. appeals court upholds Pentagon designation of Anthropic as supply chain risk</a></li>

</ul>
</details>

**社区讨论**: 评论者意见严重分化：一些人认为这是教科书式的供应链决策——既然 Anthropic 对军事用途附加了条件，五角大楼只需选择没有此类附加条款的供应商即可。另一些人则对一项本用于对抗外国对手的认定被用来对付本国私营企业感到不安，并警告这种权力可能被两党中的任何一方滥用来打击政治立场不合的公司，例如 Palantir。一个反复出现的主题是“选择性执法”：有用户将 Anthropic 设置护栏的做法与 OpenAI 被指控的若干事件作对比，质疑为何唯独 Anthropic 遭到针对。

**标签**: `#AI policy`, `#national security`, `#Anthropic`, `#government regulation`, `#supply chain risk`

---

<a id="item-3"></a>
## [陶哲轩：社会将需要多得多的数学家](https://terrytao.wordpress.com/2026/09/24/were-gonna-need-a-lot-more-mathematicians/) ⭐️ 8.0/10

陶哲轩（Terence Tao）于 2026 年 9 月 24 日发表了一篇题为《We're gonna need a lot more mathematicians》的博客文章，主张社会所需要的数学家数量将远超目前的规模。该条目本身只提供了一个指向 Lobsters 评论区的链接，并未转载文章的完整论证内容。 陶哲轩是菲尔兹奖得主，也是人工智能与数学交叉领域最具影响力的公共发声者之一，因此他的论述直接反驳了「AI 将让人类数学家变得多余」这一流行叙事。随着 AI 工具在科研中普及，他的观点可能影响高校、资助机构和用人单位对数学人才需求的判断。 文章标题化用了电影《大白鲨》中那句著名台词「you're gonna need a bigger boat」，暗示的是量级上的跃升而非细微调整。由于该条目只链接到评论区，陶哲轩在文中给出的具体论证、数据或建议无法从此条目中获得，需要阅读原文。

rss · Lobste.rs · 9月25日 18:27

**背景**: 陶哲轩是澳大利亚裔美国数学家、加州大学洛杉矶分校教授，因在偏微分方程、组合数学、调和分析和加性数论等领域的贡献于 2006 年获得菲尔兹奖。人工智能正越来越多地通过自动定理证明器和交互式证明助手等工具进入数学研究，这些工具通过人机协作帮助形式化并验证证明。与此同时，研究者也提出了 AI 应用于数学的多项担忧，包括结果不可靠、引用缺失、依赖封闭的商业系统、夸大宣称以及科学独立性的丧失。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Terence_Tao">Terence Tao - Wikipedia</a></li>
<li><a href="https://www.tue.nl/en/news-and-events/news-overview/03-06-2026-ai-threatens-math-researchers-warn">AI threatens math , researchers warn</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_assistant">Proof assistant - Wikipedia</a></li>

</ul>
</details>

**标签**: `#mathematics`, `#AI`, `#research`, `#commentary`, `#academia`

---

<a id="item-4"></a>
## [Ollaya：为开源 Jev 式决策模型提供 Ollama 风格本地推理](https://ollaya.dev/) ⭐️ 7.0/10

Ollaya（ollaya.dev）作为一个 Ollama 风格的工具发布，让开发者可以在本地运行开源的 Jev 式决策模型，而无需依赖托管 API。该项目在 Hacker News 上获得 299 分和 88 条评论，用户围绕其实用价值展开讨论，并将其 Laya 模型与 Jev 进行比较。 通过让决策模型以熟悉的 Ollama 式工作流在本地运行，Ollaya 可能降低在应用中添加结构化分类和评分功能的门槛，且无需付费 API 调用。这也引发了更广泛的讨论：开源工具能以多快的速度复制 AI 初创公司的创新，进而可能削弱 TypeSafe 等公司的护城河。 Ollaya 提供模型库（例如 ollaya.dev/library/laya），并模仿 Ollama 的本地执行方式，但评论者指出其示例聚焦于文本分类（如预测 refund_requested），而非更丰富的决策任务。用户还反映，相较于 Jev，Laya 在复杂查询上置信度更低、错误决策更多；而 Jev 的托管 API 已开放，定价为每 100 万输入 token 0.042 美元，输出免费。

hackernews · Ardakilic · 9月25日 18:33 · [社区讨论](https://news.ycombinator.com/item?id=49848269)

**背景**: Ollama 是一个广泛使用的开源运行时，简化了在本地运行大语言模型的过程——它封装 llama.cpp、内置模型仓库，并提供兼容 OpenAI 的 API，使本地推理像使用 Docker 一样简单。TypeSafe AI 的 Jev 是一个“系统一”模型，返回选择、分数或 yes/no 概率，而非对话文本，面向结构化、可重复的决策任务。Jev 式决策模型正在被公开共享，其训练标签来自人工、精确规则或 LLM 教师模型。Ollaya 将 Ollama 的本地优先理念应用到这类新兴的决策模型上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jevmodel.org/">Jev AI Model (TypeSafe) — Typed System One Decisions</a></li>
<li><a href="https://read.theaimerge.com/p/the-complete-guide-to-ollama-local">The Complete Guide to Ollama: Local LLM Inference Made Simple</a></li>
<li><a href="https://huggingface.co/collections/davanstrien/jev-style-decision-models-open-data">Jev-style decision models: open data - a davanstrien Collection</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论整体对其实用性持怀疑态度：一位用户表示安装并运行了 Ollaya 的示例，但看不到它有什么用处，并认为退款分类的示例显得刻意。其他人质疑 Jev/Laya 与基于 instruct 的重排序器有何区别，还有人反映 Laya 的表现明显不如 Jev。更广泛的讨论涉及 AI 初创公司的护城河，指出开源项目最快可在两周内复制创新，这引发了对创新者如何获取价值的疑问。

**标签**: `#AI/ML`, `#open-source`, `#decision-models`, `#Ollama`, `#local-inference`

---

<a id="item-5"></a>
## [John Gruber 警告 Meta Muse 强大却暗藏风险](https://simonwillison.net/2026/Sep/25/john-gruber/) ⭐️ 7.0/10

在 Daring Fireball 的一篇文章中（由 Simon Willison 引用），John Gruber 指出 Meta Muse 在技术上具有突破性——每位用户都会在 Meta 云端拥有自己的一台持久化 Linux 虚拟机——并且在安装与使用上极其简便，但大多数消费者恐怕并不清楚它有多强大、因而有多危险，尤其是当它运行在你的 Mac 上时。他用买电锯作比喻：人们都知道电锯能切断手指，却未必意识到这个智能体（agentic）AI 系统具有同等量级的风险。 Muse 被称为首个面向普通消费者的智能体 AI 系统，这意味着 AI 的风险性质从“给出错误答案”转变为“以用户身份执行错误操作”，且这些操作涉及真实的凭据、文件和网络访问权限。由于 Meta 能把它推送给规模庞大、大多不具备技术背景的用户群体，智能体安全性的讨论便从研究实验室转移到了普通消费者的日常计算环境中。 Muse 由 Muse Spark 驱动，Meta 称其为迄今面向真实世界智能体任务能力最强的模型，并在 Meta Connect 2026 大会上发布，宣传中还包括大量的免费 token 额度。关键的架构细节是每名用户在 Meta 云端拥有一台持久化的 Linux 虚拟机，这意味着该智能体拥有可长期保存的状态和文件系统，而不仅限于一次聊天会话。

rss · Simon Willison · 9月25日 17:22

**背景**: Meta Muse 是 Meta 在 Meta Connect 2026 大会上发布的新一代个人 AI 智能体平台：它不只是回答问题，而是被设计来真正执行发邮件、订机票、填写表单等任务。“智能体 AI”（agentic AI）通常指能够设定目标、调用工具、在步骤之间保留上下文，并在较少人工监督下完成多步任务的系统，这正是它需要像虚拟机这样持久化执行环境的原因。John Gruber 是长期专注苹果生态的博客 Daring Fireball 的作者，而 Simon Willison 是知名开发者与大语言模型评论者，经常引用并传播关于 AI 的重要观点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/">Introducing Muse : The World’s First Personal AI Agent Built for Everyone</a></li>
<li><a href="https://www.computerweekly.com/news/366651213/Meta-Connect-26-Muse-paves-the-way-to-global-domination">Meta Connect 26: Muse paves the way to global... | Computer Weekly</a></li>
<li><a href="https://www.anandriyer.com/glossary/agentic-ai">Agentic AI — definition — Anand Iyer</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#AI safety`, `#Meta Muse`, `#consumer AI`, `#virtual machines`

---

<a id="item-6"></a>
## [文件通知攻击：跨操作系统通知 API 的侧信道信息泄漏](https://inoti.fyi/) ⭐️ 7.0/10

一篇安全研究论文提出了首个通用的“文件通知模板攻击”，证明 Linux（inotify）、macOS（FSEvents）、Windows 与 Android 的文件通知子系统可被滥用为侧信道，用于窥探系统与用户活动。研究者采用系统化、半自动化的方法来发现泄漏点，并展示攻击者能够绕过安全机制，访问甚至篡改受保护的文件系统数据。 这些通知 API 无处不在，通常被视为无害的低权限可观测性工具，因此该发现几乎波及所有主流消费级与服务器平台，任何注册了文件监视的应用都可能变成非预期的信息泄漏源。这很可能促使操作系统厂商开展缓解工作，并改变开发者在沙箱或安全敏感场景中使用通知 API 的方式。 该研究被称为首个覆盖 Linux、Windows 与 macOS（Android 亦在范围内）的通用文件通知模板攻击，其基础是一套半自动化方法论，能够系统性地挖掘可利用的泄漏，而非依赖单一手工构造的案例。核心问题在于通知事件（例如哪个文件发生了变化、何时变化、由谁触发）携带的元数据会暴露受保护的文件系统活动，从而使攻击者推断出或间接操作用其权限本无法直接读取的数据。

rss · Lobste.rs · 9月25日 02:50

**背景**: 文件通知系统让程序可以订阅文件系统变化，而不必反复轮询：Linux 的 inotify（自内核 2.6.13 起提供）会告知应用被监视的文件或目录何时被修改，macOS 的 FSEvents API 及其 fseventsd 守护进程提供类似的按磁盘或按主机的事件流，Windows 与 Android 也有各自的对应机制。由于这些 API 只报告活动的元数据而非文件内容，它们通常被视为安全、低权限的功能——正因如此，把它们变成侧信道意义重大，因为它可以在不直接读取任何受保护数据的情况下跨权限或沙箱边界泄漏信息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://snee.la/pdf/pubs/file-notification-attacks.pdf">[PDF] file-notification-attacks.pdf</a></li>
<li><a href="https://hannesweissteiner.com/publications/inotify/">File Notification Attacks: Templating and Exploiting Side-Channel ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Inotify">inotify - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/FSEvents">FSEvents - Wikipedia</a></li>

</ul>
</details>

**标签**: `#security`, `#side-channel`, `#operating-systems`, `#privacy`, `#inotify`

---