---
layout: default
title: "Horizon Summary: 2026-08-02 (ZH)"
date: 2026-08-02
lang: zh
---

> 从 59 条内容中筛选出 12 条重要资讯。

---

1. [Lean 内核健全性漏洞 #14576 的事后分析](#item-1) ⭐️ 9.0/10
2. [NetBSD 11.0 发布：引入快速 microVM 内核与改进的 NPF 防火墙](#item-2) ⭐️ 8.0/10
3. [DeepSeek 发布 V4-Flash 正式版 API 公测，Agent 能力大幅提升](#item-3) ⭐️ 8.0/10
4. [苹果屏幕共享爆出预认证远程代码执行漏洞](#item-4) ⭐️ 8.0/10
5. [欧盟人工智能法案于 2026 年 8 月 2 日生效](#item-5) ⭐️ 8.0/10
6. [《64 位汇编艺术》新版引发社区热议](#item-6) ⭐️ 7.0/10
7. [谷歌如何帮助摧毁了 RSS 的普及](#item-7) ⭐️ 7.0/10
8. [OpenAI Astra 声称攻克十道未解数学难题](#item-8) ⭐️ 7.0/10
9. [部分美国企业改用中国大模型降本](#item-9) ⭐️ 7.0/10
10. [消息称 OpenAI 或因投资者担忧与竞争压力推迟 IPO 至明年](#item-10) ⭐️ 7.0/10
11. [Chrome 启动邮箱验证协议的 Origin Trial 测试](#item-11) ⭐️ 7.0/10
12. [Arch Linux 维护者宣布辞职](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Lean 内核健全性漏洞 #14576 的事后分析](https://leodemoura.github.io/blog/2026-8-1-postmortem-for-kernel-soundness-bug-14576/) ⭐️ 9.0/10

Leonardo de Moura 发布了 Lean 内核健全性漏洞 #14576 的事后分析，该漏洞涉及内核接受错误的结构投影。该漏洞允许对抗性元程序添加声明，使普通 Lean 代码能利用这些声明证明 False，而 #print axioms 却不报告任何公理。 Lean 可信内核中的健全性漏洞非常严重，因为它可能破坏 Lean 所验证的每个证明都有效这一基础保证。形式验证和数学社区依赖 Lean 获得经过验证的结果，因此内核中的任何缺陷都需要及时、透明的分析。 该问题源于内核处理结构投影的方式，报告称其影响“checked-kernel 健全性”。对抗性元程序可利用该漏洞证明 False，而 #print axioms 却不显示任何公理，这意味着这种不一致性可能在常规检查中被忽略。

rss · Lobste.rs · 8月1日 21:51

**背景**: Lean 是一种基于归纳构造演算的证明助手和函数式编程语言，其核心是一个负责验证证明的小型可信内核。健全性意味着内核只接受真正有效的证明；如果内核接受了 False 的证明，根据爆炸原理，整个逻辑系统就会变得不一致。该项目是开源的，并由 Lean Focused Research Organization 提供支持。形式验证和交互式定理证明都依赖于对这个内核的信任。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/leanprover/lean4/issues/14576">Kernel accepts wrong-structure projections, allowing ... - GitHub</a></li>
<li><a href="https://news.ycombinator.com/item?id=49137060">Postmortem for Kernel Soundness Bug #14576 | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 在 Hacker News 上，评论者指出，即使像 Rust 这样更简单的类型检查器也会偶尔出现健全性问题，并强调应把经过验证的结果视为极其强大但并非绝对的保证。整体语气较为平和：社区欢迎这篇事后分析，认为这是对该问题的严肃、透明处理。还有人提到更广泛的背景，即多个 Lean 健全性漏洞曾被私下报告。

**标签**: `#Lean`, `#kernel soundness`, `#formal verification`, `#theorem proving`, `#bug postmortem`

---

<a id="item-2"></a>
## [NetBSD 11.0 发布：引入快速 microVM 内核与改进的 NPF 防火墙](https://blog.netbsd.org/tnf/entry/netbsd_11_0_released) ⭐️ 8.0/10

NetBSD 11.0 已正式发布。亮点包括面向 x86 的全新 MICROVM 内核，可在约 10 毫秒内启动；同时改进了 NPF 防火墙，新增二层过滤及用户/组过滤功能。 这一主版本发布巩固了 NetBSD 作为可移植、轻量级 BSD 操作系统的地位。约 10 毫秒启动的 microVM 内核可能使 NetBSD 在微服务和边缘/云工作负载中更具吸引力，而 NPF 的改进则增强了其作为防火墙平台的实用性。 NetBSD 11.0 为 x86 引入了新的 MICROVM 内核配置，专为在 QEMU 的 microvm 机器类型下快速启动而设计。NPF（NetBSD 的数据包过滤器）在原有第 3/4 层能力基础上，新增了二层过滤及基于用户/组的规则支持。

hackernews · Lobste.rs · 8月1日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49136736)

**背景**: NetBSD 是一款历史悠久的开源类 Unix 操作系统，以跨多种硬件平台的可移植性著称。NPF 是 NetBSD 采用 BSD 许可的有状态数据包过滤器，与 iptables、ipfw 和 PF 类似，支持 IPv4/IPv6，并可执行 NAT。MICROVM 内核是一种最小化内核配置，配合 QEMU 的 microvm 机器类型，可在约 10 毫秒内启动客户机，适合需要快速启动的微虚拟机场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NPF_(firewall)">NPF (firewall) - Wikipedia</a></li>
<li><a href="https://man.netbsd.org/npf.7">npf (7) - NetBSD Manual Pages</a></li>
<li><a href="https://www.phoronix.com/news/smolBSD">smolBSD Builds On The NetBSD-MicroVM Kernel For Booting To Service VMs In Milliseconds - Phoronix</a></li>

</ul>
</details>

**社区讨论**: 评论者对 NPF 二层及用户/组过滤的改进和快速的 MICROVM 内核表示欢迎，认为这些功能"可能会打开一些局面"。还有人提出了更广泛的问题，例如 BSD 家族与 Linux 相比的现状和采用情况，以及 NetBSD 上的 Wine 是否仍能可靠运行仅支持 Windows 的软件。

**标签**: `#NetBSD`, `#BSD`, `#Operating Systems`, `#Release`

---

<a id="item-3"></a>
## [DeepSeek 发布 V4-Flash 正式版 API 公测，Agent 能力大幅提升](http://www.geekpark.net/news/368270) ⭐️ 8.0/10

7 月 31 日，DeepSeek 宣布 DeepSeek-V4-Flash 正式版 API 上线公测。该模型的 Agent 能力大幅增强，基准测试成绩远超 V4-Pro-Preview，且模型结构与参数量与预览版一致，仅重新进行了后训练。 此次发布为开发者提供了正式支持的 API，并在 agent 与编程基准测试上大幅提升，表明模型在真实自主任务上的能力出现明显跃升。这也加剧了 AI agent 模型领域的竞争，因为工具调用、终端操作与代码仓库自动化正变得越来越重要。 其基准测试成绩包括 Terminal Bench 2.1 为 82.7、NL2Repo 为 54.2、Cybergym 为 76.7、DeepSWE 为 54.4、Toolathlon verified 为 70.3、Agent Last Exam 为 25.2、Automation Bench（Public）为 25.1、DSBench-FullStack 为 68.7、DSBench-Hard 为 59.6。DeepSeek-V4-Flash-0731 原生支持 Responses API 格式，并针对性适配了 Codex。

rss · 极客公园 · 8月1日 00:42

**背景**: DeepSeek 是一家通过 API 提供大语言模型的中国 AI 实验室。文中提到的基准测试用于衡量 agent 能力：Terminal-Bench 在真实终端任务中测试智能体，NL2Repo 测试模型根据自然语言需求生成长时程、完整可运行代码仓库的能力，DSBench 则评估数据科学智能体在真实分析与建模任务上的表现。V4-Flash 是 DeepSeek V4 模型系列中的 Flash 变体，V4-Pro-Preview 则是此前更强的预览版。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/harbor-framework/terminal-bench">GitHub - harbor-framework/terminal-bench: A benchmark for LLMs on complicated tasks in the terminal · GitHub</a></li>
<li><a href="https://github.com/multimodal-art-projection/NL2RepoBench">GitHub - multimodal-art-projection/NL2RepoBench</a></li>

</ul>
</details>

**社区讨论**: 评论区整体以玩笑和“硬件钱包焦虑”为主：有用户调侃自己的钱包需要“送上祝福和祈祷”，还有人说正在看 r/LocalLLaMA 来研究本周工资要花到哪里。还有人表示刚冲动下单了 128GB DDR4，并努力忍住再买两张 RTX 3090 的冲动。也有用户猜测这个模型是否能在本地运行。

**标签**: `#DeepSeek`, `#AI`, `#API`, `#LLM`, `#Benchmarks`

---

<a id="item-4"></a>
## [苹果屏幕共享爆出预认证远程代码执行漏洞](https://warez.sl0p.foo/apple-screensharing-rce/) ⭐️ 8.0/10

一份安全公告报告了 Apple Screen Sharing（屏幕共享）存在预认证远程代码执行（RCE）漏洞。该公告本身未提供技术细节，仅附有 Lobsters 讨论帖链接。 Apple Screen Sharing 的预认证 RCE 属于严重问题，因为未认证的远程攻击者可能在受影响的 Mac 上执行任意代码。若此漏洞得到证实，可能影响大量开启了屏幕共享的用户，因此需要立即关注并安装补丁。 该公告内容非常简略，未提及受影响的 macOS 版本、CVE 编号、补丁或概念验证（PoC）。读者需要点击所附的 Lobsters 讨论帖，以获取社区讨论和可能的更多细节。

rss · Lobste.rs · 8月1日 19:39

**背景**: Apple Screen Sharing 是 macOS 内置功能，允许用户通过网络查看和控制另一台 Mac 的屏幕，可在系统设置中开启或关闭。预认证远程代码执行意味着攻击者无需先提供有效登录凭据，就能在目标系统上运行恶意代码，因此这类漏洞尤为危险。屏幕共享服务通常暴露在局域网甚至互联网上，因此该组件若存在预认证 RCE，影响范围会很大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.apple.com/guide/mac-help/turn-screen-sharing-on-or-off-mh11848/mac">Turn Mac screen sharing on or off - Apple Support</a></li>
<li><a href="https://www.securityscientist.net/blog/12-questions-and-answers-about-pre-authentication-rce/">12 Questions and Answers About pre-authentication rce</a></li>

</ul>
</details>

**标签**: `#security`, `#RCE`, `#Apple`, `#vulnerability`

---

<a id="item-5"></a>
## [欧盟人工智能法案于 2026 年 8 月 2 日生效](https://www.reddit.com/r/LocalLLaMA/comments/1vcqpn4/eu_ai_act_takes_effect_tomorrow_august_2_2026/) ⭐️ 8.0/10

欧盟人工智能法案于 2026 年 8 月 2 日正式生效，要求对看似真实的 AI 生成内容进行强制标注。相关规定适用于 AI 生成或篡改的图像、音频、视频和文本。 这是 AI 监管的一个重要里程碑，欧盟成为首个对 AI 输出实施全面透明度规则的司法管辖区。任何面向欧盟用户的服务提供者都必须合规，否则将面临处罚，这为其他监管机构树立了全球标杆。 透明度义务仅适用于看起来真实的内容，并豁免个人作品、“明显具有艺术性”的作品、讽刺作品和虚构作品。AI 法案采用基于风险的分层框架，覆盖所有 AI 系统，而最低风险应用（如 AI 游戏或垃圾邮件过滤器）则不受监管。

reddit · r/LocalLLaMA · xoxaxo · 8月1日 15:44

**背景**: 欧盟《人工智能法案》是 2024 年通过的一项综合性法规，旨在对欧盟境内的人工智能进行监管。该法案将 AI 系统按风险分为不可接受、高风险、有限风险和最低风险四类，并规定了相应的义务。与《通用数据保护条例》（GDPR）类似，该法案可适用于欧盟境外但只要在欧盟境内有用户的提供商。开源通用模型享有减轻的要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EU_AI_Act">EU AI Act</a></li>
<li><a href="https://pandectes.io/blog/labeling-ai-generated-content-what-the-new-rules-require/">Labeling AI Generated Content: What the New Rules Require for Compliance</a></li>
<li><a href="https://www.consilium.europa.eu/en/policies/artificial-intelligence-act/">Artificial intelligence act - Consilium</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的讨论总体持欢迎态度，用户支持标注规则，并指出个人用户无需担心合规问题。一位评论者举例说明该法律的作用：附近一家餐馆用 AI 生成的食物图片误导顾客；另一位评论者则分享了关于艺术创作豁免的新闻报道链接。

**标签**: `#EU AI Act`, `#AI regulation`, `#AI policy`, `#generative AI`, `#content labeling`

---

<a id="item-6"></a>
## [《64 位汇编艺术》新版引发社区热议](https://nostarch.com/art-64-bit-assembly-v2) ⭐️ 7.0/10

No Starch Press 发布了由 Randall Hyde 撰写的《64 位汇编艺术》（The Art of 64-bit Assembly），这是一本约 800 页的汇编编程书籍，发布消息在 Hacker News 上引发了社区讨论。讨论集中在 MASM 与 GAS 等工具的技术取舍，以及 AI 生成内容在技术书籍中的角色。 这本书更新了学习底层编程的经典资源，而底层编程对系统编程、操作系统开发和逆向工程仍然至关重要。社区讨论也凸显了技术社区在工具选择及 AI 生成文本日益普及方面存在的持续分歧。 书中的示例使用 MASM（Microsoft 宏汇编器），公告引发了与 GAS（GNU 汇编器）的比较，有评论者指出 GAS 缺少 while 循环和字符串处理等功能。据报道，书中第一页包含 AI 生成的宣传文字，引起了一些用户的不满。

hackernews · 0x54MUR41 · 8月1日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49134599)

**背景**: 汇编语言是最底层的人类可读编程语言，直接表示特定 CPU 架构的机器指令。Randall Hyde 之前的《汇编语言艺术》（The Art of Assembly Language）几十年来一直是标准教材，这本新书面向现代桌面和服务器处理器使用的 x86-64 架构。MASM 是 Windows 生态的汇编器，而 GAS 是 GNU 汇编器，常用于 Linux 和开源项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nostarch.com/art-64-bit-assembly-volume-1">The Art of 64-Bit Assembly, Volume 1 | No Starch Press</a></li>
<li><a href="https://www.amazon.com/Art-64-Bit-Assembly-Language/dp/1718501080">The Art of 64-Bit Assembly, Volume 1: x86-64 Machine Organization and Programming: Hyde, Randall: 9781718501089: Amazon.com: Books</a></li>
<li><a href="https://kolegite.com/EE_library/books_and_lectures/Програмиране/The+Art+of+64-Bit+Assembly,+Volume+1+x86-64+Machine+Organization+and+Programming+(Randall+Hyde)+(z-lib.org).pdf">The Art of 64-Bit Assembly Language</a></li>

</ul>
</details>

**社区讨论**: 社区观点不一：有评论者称赞这本书的持久价值以及学习汇编语言的重要性，也有人对讨论聚焦于工具和 AI 生成内容等元话题而非书籍本身感到失望。一些用户将 MASM 与 GAS 进行对比，或表示希望有一本面向 Linux 的替代书籍；还有评论者指出作者几十年来一直在更新这本书。

**标签**: `#assembly`, `#programming`, `#low-level`, `#book`, `#systems`

---

<a id="item-7"></a>
## [谷歌如何帮助摧毁了 RSS 的普及](https://openrss.org/blog/how-google-helped-destroy-adoption-of-rss-feeds) ⭐️ 7.0/10

这篇文章分析了谷歌在 RSS 普及率下降中所扮演的角色，尤其聚焦于 2013 年关闭 Google Reader 的决定，认为这加速了内容向封闭生态系统的集中。该文于 2023 年发表在 openrss.org 上，是对开放网络历史的一次回顾。 RSS 是一种使用户能够自主获取内容的开放网络标准。谷歌的决定，加上其他平台的整合，塑造了今天由广告驱动、高度中心化的互联网格局。对开放标准和开放网络倡议的支持者来说，理解这段历史具有重要意义。 文章讨论了谷歌关闭 Google Reader 的理由——使用人数下降——但当时许多人认为这只是为了推广其苦苦挣扎的 Google+社交网络的借口。文章还提到 RSS 的衰落并不仅仅由谷歌造成，并引用了 Mozilla 在 Firefox 64 中移除 RSS Live Bookmarks 和反馈订阅功能的例子。

hackernews · pudgywalsh · 8月1日 18:07 · [社区讨论](https://news.ycombinator.com/item?id=49136821)

**背景**: RSS（真正简单的联合供稿）是一种网页订阅格式，用户可以通过聚合器或新闻阅读器订阅并阅读网站更新。Google Reader 于 2005 年上线，曾是广受欢迎的 RSS 阅读器之一，但于 2013 年被谷歌关闭。在技术领域，“围墙花园”是一种封闭平台，如微信或 X，使用户被限制在其自身生态系统中，这与 RSS 开放、基于标准的方式形成鲜明对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/RSS">RSS - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Walled_garden">Walled garden - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论区普遍认为 Google Reader 的关闭是互联网走向中心化的转折点。也有人提出反驳，指出 RSS 至今仍是开放网络倡议的核心组成部分，并且支持 RSS 几乎没有成本；还有人称 Mozilla 等浏览器厂商也移除了内置 RSS 功能，表明这是更广泛的行业变化，而非完全由谷歌导致。

**标签**: `#RSS`, `#Google`, `#Open Web`, `#Web History`, `#Technology`

---

<a id="item-8"></a>
## [OpenAI Astra 声称攻克十道未解数学难题](https://simonwillison.net/2026/Aug/1/ten-advances-in-mathematics/#atom-everything) ⭐️ 7.0/10

OpenAI 宣布其下一代主要模型的内部版本 Astra 解决了十道至少十年未有进展的数学问题，按 GPT-5.6 Sol 代币价格计算，每个问题的花费不到 2,000 美元。该公司还发布了 Lean 4 形式化证明和相关论文。 这是一次高价值的展示，表明 AI 能够攻克长期存在的数学研究难题，并预示着向陶哲轩所称的“大数学”——大规模人机协作——的转变。这可能会改变数学家的研究方式，由 AI 承担大量技术性工作，而人类专注于创造性部分。 OpenAI 尚未透露有多少问题尝试后未获解决，Simon Willison 也表示希望能看到所用提示词。公司发布了 openai/ten-proofs 仓库，包含 Lean 4 形式化证明、一篇论文，以及一份由大语言模型生成的、重构证明过程细节的 PDF 文件。

rss · Simon Willison · 8月1日 20:34

**背景**: 这条新闻来自 Simon Willison 的博客，该博客持续关注 AI 发展动态。近期已有多项 AI 研究成就出现；数日前，Anthropic 使用其 Claude Mythos 模型发现了密码学弱点。OpenAI 的 Astra 是专为长时程、多智能体任务设计的新模型系列，本次数学成果正是由该模型的一个内部版本完成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://the-decoder.com/openai-announces-its-next-major-model-astra-by-dropping-ten-previously-unsolved-math-solutions/">OpenAI announces its "next major model" Astra by dropping ten previously unsolved math solutions</a></li>
<li><a href="https://thenextweb.com/news/openai-astra-model-ten-math-proofs-non-sofic-groups">OpenAI says its next model, Astra, has solved ten open problems in mathematics</a></li>

</ul>
</details>

**标签**: `#AI`, `#mathematics`, `#OpenAI`, `#research`, `#LLM`

---

<a id="item-9"></a>
## [部分美国企业改用中国大模型降本](https://36kr.com/newsflashes/3920583026929281?f=rss) ⭐️ 7.0/10

据美联社报道，Coinbase 和 Airbnb 等美国公司正改用 Kimi、Qwen 等中国大模型以降低成本。与此同时，月之暗面发布的新一代开源模型 Kimi K3 拥有 2.7 万亿参数，震动了资本市场。 这标志着全球 AI 竞争格局出现显著变化，意味着中国开源模型正成为西方企业具成本竞争力的替代选择。这可能加速西方企业采用美国之外的开源权重模型，并促使美国 AI 厂商调整定价策略。 据 Fortune 和 Kimi API 平台介绍，Kimi K3 是当前最大的开源权重 LLM，拥有 2.7 万亿参数和 100 万 token 上下文窗口。Airbnb 使用的阿里巴巴 Qwen 模型则在 Apache 2.0 等许可下开源。

rss · 36氪 · 8月1日 07:30

**背景**: 大语言模型是在海量文本数据上训练的人工智能系统，开放权重模型允许开发者下载并自定义。中国的 DeepSeek 和月之暗面发布了性能可媲美美国系统且成本更低的开源权重模型，引发了与 ChatGPT 时代颠覆性相当的讨论。华尔街日报等媒体报道称，Kimi K3 的发布引发的市场恐慌与 DeepSeek 在 2025 年发布时类似。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_(AI)">Kimi (AI) - Wikipedia</a></li>
<li><a href="https://fortune.com/2026/07/16/moonshots-kimi-k3-pushes-chinese-ai-into-fable-level-territory/">Moonshot’s Kimi K3 pushes Chinese AI into Fable-level territory | Fortune</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>

</ul>
</details>

**标签**: `#AI`, `#large language models`, `#cost optimization`, `#open source`, `#industry trends`

---

<a id="item-10"></a>
## [消息称 OpenAI 或因投资者担忧与竞争压力推迟 IPO 至明年](https://36kr.com/newsflashes/3920415886061193?f=rss) ⭐️ 7.0/10

据报道，OpenAI 可能将 IPO 推迟到明年；与此同时，Anthropic 正在加快秋季 IPO 计划，并已开始与潜在投资者会面。部分 OpenAI 大投资者私下对该公司相对于增长的现金消耗速度表示担忧，还有人通过投资 Anthropic 来对冲押注。 这反映出 AI 行业投资者情绪的变化，以及头部 AI 初创企业之间竞争的加剧。推迟 IPO 可能影响 OpenAI 的融资能力，并影响两家公司上市的时间与估值。 据知情人士透露，Anthropic 的营收增长和估值近期已超过 OpenAI。OpenAI 最初希望抢在 Anthropic 之前上市，但现在可能会等到明年。

rss · 36氪 · 8月1日 04:45

**背景**: OpenAI 是 ChatGPT 的开发商，Anthropic 是以 Claude 模型闻名的竞争对手。两家公司都依赖大规模资本投入和高营收增长，而 IPO 是融资和回报投资者的关键里程碑。这则报道突显出在现金消耗率较高的背景下，快速成长的 AI 公司如何争夺投资者的信心。

**标签**: `#OpenAI`, `#Anthropic`, `#IPO`, `#AI Competition`, `#Startup Funding`

---

<a id="item-11"></a>
## [Chrome 启动邮箱验证协议的 Origin Trial 测试](https://developer.chrome.com/blog/email-verification-protocol-origin-trial) ⭐️ 7.0/10

Chrome 已面向 Email Verification Protocol（EVP）启动 Origin Trial，从 Chrome 150 开始提供。该试用允许网站以密码学方式证明用户的邮箱所有权，而无需用户点击验证链接或输入验证码。 EVP 有望取代传统的邮箱验证流程，在账号注册与恢复过程中减少操作摩擦并保护用户隐私。这对构建身份与账号管理系统的 Web 开发者意义重大，因为它简化了一个常见但繁琐的步骤。 该 Origin Trial 从 Chrome 150 起可用，Microsoft Edge 也通过自己的 Origin Trial 提供 EVP 支持。EVP 以密码学所有权证明替代手动验证，帮助用户创建、访问和恢复账号；开发者需要为自己的域名启用该试用才能使用此协议。

rss · Lobste.rs · 8月1日 12:34

**背景**: 目前，网站通常通过向用户邮箱发送一次性验证码或链接来验证邮箱所有权，这既暴露了邮箱地址，也需要额外操作。Email Verification Protocol 旨在让浏览器在自动填充时直接证明邮箱所有权，从而减少钓鱼风险并提升隐私。借助密码学证明，EVP 可以完全避免发送验证邮件，也与 Web 向无密码和隐私友好身份验证迈进的大趋势一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.chrome.com/blog/email-verification-protocol-origin-trial">Test the Email Verification Protocol with an origin trial</a></li>
<li><a href="https://developer.microsoft.com/en-us/microsoft-edge/origin-trials/trials/683027d2-a798-460f-9b35-03a95002d9af">Microsoft Edge Origin Trials</a></li>
<li><a href="https://issues.chromium.org/issues/452052812">Email Verification Protocol: Origin Trial [452052812] - Chromium</a></li>

</ul>
</details>

**标签**: `#web-platform`, `#privacy`, `#email`, `#chrome`, `#origin-trial`

---

<a id="item-12"></a>
## [Arch Linux 维护者宣布辞职](https://linderud.dev/blog/resigning-from-arch-linux/) ⭐️ 7.0/10

一位开发者在博客上发布了题为《Resigning from Arch Linux》的文章，宣布退出该项目。这篇声明内容十分简短，并附有一个 Lobsters 讨论帖链接供社区评论。 维护者辞职可能预示着大型 Linux 发行版中存在的倦怠或治理问题，并引发更广泛开源社区的关注。Lobsters 上的讨论表明，这一离开引发了用户和贡献者的共鸣，凸显了人们对项目可持续性的担忧。 这篇博文不包含任何技术细节，现有内容中也未提供作者身份和辞职原因。唯一补充信息是一个 Lobsters 讨论帖链接，表明该声明引发了社区的积极讨论。

rss · Lobste.rs · 8月1日 22:47

**背景**: Arch Linux 是一个广泛使用的独立 Linux 发行版，以其滚动发布模式和 DIY 理念著称。贡献者和维护者都是志愿者，负责管理软件包、安全更新和项目基础设施，因此他们的离开会影响项目的连续性。开源项目中的辞职声明常常引发关于维护者倦怠和可持续性的讨论。

**标签**: `#Arch Linux`, `#open source`, `#maintainership`, `#community`

---