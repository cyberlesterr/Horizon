---
layout: default
title: "Horizon Summary: 2026-08-14 (ZH)"
date: 2026-08-14
lang: zh
---

> 从 64 条内容中筛选出 9 条重要资讯。

---

1. [DRAM 加扰漏洞：通过地址别名解锁 CPU 隐藏内存](#item-1) ⭐️ 9.0/10
2. [DeepSeek 发布 V4-Pro-0813：1.7T 参数模型基准大幅跃升](#item-2) ⭐️ 9.0/10
3. [OpenAI 与 Cerebras 推出 GPT-5.6 Sol Ultrafast，速度提升近 7 倍](#item-3) ⭐️ 8.0/10
4. [理解成为 AI 辅助编程时代的新瓶颈](#item-4) ⭐️ 8.0/10
5. [SQLite 作者 Richard Hipp 2024 年演讲详解 SQLite 内部原理](#item-5) ⭐️ 8.0/10
6. [SvelteKit 3 进入候选发布阶段](#item-6) ⭐️ 8.0/10
7. [采用 CHERI 实现内存安全与细粒度隔离](#item-7) ⭐️ 8.0/10
8. [ZOOMSDAY：Zoom 标注功能零点击漏洞可致远程代码执行](#item-8) ⭐️ 8.0/10
9. [DeepSeek V4 Pro API 上线、腾讯 HY4 计划、iPhone 18 涨价传闻](#item-9) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [DRAM 加扰漏洞：通过地址别名解锁 CPU 隐藏内存](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

研究员 Christopher Domas 发布了“Spaghettifying DRAM”技术，它可映射 AMD 处理器上的 DRAM 地址加扰，并借助 z3 求解出的变换，到达通常对 ring-0 隔离的保护内存区域。该概念验证项目以“skitter-creek-bath-salts”为名托管在 GitHub，能通过加扰视图中的别名访问 PSP 私有内存、SMRAM 和 C6 空闲状态等区域。 这一发现意义重大，因为它揭示了一个硬件层面的攻击面：ring-0 代码可以绕过平台针对一致内存视图精心构造的围栏和安全检查。它可能影响主机安全与底层利用研究，因为 Xbox、PlayStation 这类系统通常依赖这些保护来应对一旦发生的 ring-0 沦陷。 根据 README，该漏洞利用目前适用于 AMD16h（AMD Jaguar），而 Zen 3 的内存控制器寄存器基地址不同，但该技术思路可能扩展到其他处理器家族。已求解的变换相当于一块“罗塞塔石碑”，能把任意目标一致地址转换成加扰后的“面条化”内存视图中的别名。

hackernews · Lobste.rs · 8月13日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49286341)

**背景**: DRAM 加扰是一种硬件特性，通过对地址和数据线进行置换来均匀分散内存芯片上的功耗与电负载，从而使物理寻址变得不那么直观。如果攻击者能解出这种置换，就可以构造别名地址，绕过 SMRAM、PSP 私有内存等 CPU 级保护。“Spaghettification”一词借自天体物理学，指强引力把物体拉伸成细长形状，这里用来形容被加扰、被“拉伸”过的内存视图。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/xoreaxeaxeax/skitter-creek-bath-salts">GitHub - xoreaxeaxeax/skitter-creek-bath-salts: Unlocking _everything_ on the CPU with DRAM scrambling · GitHub</a></li>
<li><a href="https://news.ycombinator.com/item?id=49286341">Spaghettifying DRAM | Hacker News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Spaghettification">Spaghettification - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论区反响热烈，不少网友称赞 Christopher Domas 的过往演讲并认为这项研究“很棒”，也有人感叹如今 DRAM 的复杂度已经远超早期时代。还有人追问该攻击是否影响除 AMD Jaguar 之外的新款 CPU——README 中只列出了 AMD16h，仅提到 Zen 3 的情况——并推测 Xbox 和 PlayStation 的安全团队可能会对此感到紧张。

**标签**: `#security`, `#DRAM`, `#hardware`, `#exploitation`, `#reverse engineering`

---

<a id="item-2"></a>
## [DeepSeek 发布 V4-Pro-0813：1.7T 参数模型基准大幅跃升](https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro-0813) ⭐️ 9.0/10

2026 年 8 月 13 日，DeepSeek 悄然发布了 V4-Pro 正式版，版本号为 DeepSeek-V4-Pro-0813，这是一个 1.7T 参数的混合专家（MoE）模型。该模型在 Hugging Face 上被短暂下架后很快重新上传，社区猜测与 config.json 配置问题有关。 这是 DeepSeek 自 4 月预览版以来最重要的开源发布，基准测试成绩提升巨大——例如 DeepSWE 从 12.8 跃升至 62.7，超越了 GLM-5.2 和 Opus-4.8。在 Kimi K3 等前沿模型的激烈竞争下，这重新确立了 DeepSeek 在开源大模型领域的领先地位。 该模型采用大规模混合专家（MoE）架构，上下文窗口为 1,048,576 tokens，最大输出 384,000 tokens，OpenRouter 上输入/输出价格分别为每百万 tokens 0.435/0.87 美元。API 模型名称仍为 `deepseek-v4-pro`；社区成员发现 config.json 最初显示 43 个隐藏层，而实际分片有 61 层，推测短暂下架与配置修复有关。

reddit · r/LocalLLaMA · mossy_troll_84 · 8月13日 12:37 · [社区讨论](https://www.reddit.com/r/LocalLLaMA/comments/1vn9it4/deepseekaideepseekv4pro0813_hugging_face/)

**背景**: DeepSeek-V4 是中国 AI 公司 DeepSeek 推出的大语言模型系列。2026 年 4 月 24 日发布的预览版包含 1.6T 参数（激活 49B）的 V4-Pro 和 284B 参数（激活 13B）的 V4-Flash；V4-Flash 正式版于 2026 年 7 月 31 日上线。V4 系列集成混合注意力机制，支持百万 token 上下文，直接对标 Kimi、GLM 和 Anthropic 的 Opus 系列。从预览版到正式版间隔 111 天，期间 Kimi K3 高调发布抢走开源社区头条，也推高了外界对此次发布的期待。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-pro-0813">DeepSeek V4 Pro 0813 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.reddit.com/r/LocalLLaMA/comments/1vmhaue/deepseekv4pro0813_is_up/">DeepSeek-V4-Pro-0813 is UP! : r/LocalLLaMA</a></li>
<li><a href="https://arxiv.org/abs/2606.19348">[2606.19348] DeepSeek-V4: Towards Highly Efficient Million ...</a></li>

</ul>
</details>

**社区讨论**: 社区情绪非常正面——有评论称"永远不要低估这头鲸鱼 🐋"，认为 1.7T 模型取得如此 DeepSWE 提升（对比 Kimi 的 2.8T）"离谱"。多位用户在下架期间遇到 404，一位成功下载的用户怀疑 config.json 与实际分片不一致（43 层 vs 61 层），并预计官方可能会有修复。

**标签**: `#DeepSeek`, `#LLM`, `#Benchmarks`, `#Hugging Face`, `#AI`

---

<a id="item-3"></a>
## [OpenAI 与 Cerebras 推出 GPT-5.6 Sol Ultrafast，速度提升近 7 倍](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

OpenAI 与 Cerebras 宣布推出 GPT-5.6 Sol Ultrafast，这是以极高速度运行的前沿模型版本。在测试中，它用 11 小时 11 分钟回答完 2500 道 HLE 题目，速度约为竞品前沿模型的 7 倍，且准确率相当。 这是 OpenAI 与 Cerebras 合作的首个重磅公开成果，可能让前沿 AI 在时效敏感场景中更实用。如果广泛开放，可能改变开发者在成本、延迟和模型质量之间的权衡。 该评测包含 2500 道 Humanity's Last Exam（HLE）题目，据报道 Claude Fable 5 完成同样题目耗时 78 小时 27 分钟。官方尚未公布定价和开放范围，也未明确说明 Ultrafast 与标准 GPT-5.6 Sol 性能完全一致。

hackernews · pr337h4m · 8月13日 18:10 · [社区讨论](https://news.ycombinator.com/item?id=49289844)

**背景**: Cerebras 设计专用的超大 AI 芯片，包括晶圆级引擎（Wafer-Scale Engine），目标是比传统 GPU 更快地训练和运行模型。该公司还提供 AI 云 API，支持训练与推理，从而实现大模型的低延迟部署。Ultrafast 似乎是运行在 Cerebras 硬件上的 GPT-5.6 Sol 的一个模式，这也是该组合最早的公开展示之一。像 GPT-5.6 Sol 这样的前沿模型通常规模巨大、算力要求高，因此专用硬件能显著缩短响应时间。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://www.cerebras.ai/chip">Product - Chip - Cerebras</a></li>
<li><a href="https://www.cerebras.ai/press-release/cerebras-announces-third-generation-wafer-scale-engine">Cerebras Systems Unveils World’s Fastest AI Chip with ...</a></li>

</ul>
</details>

**社区讨论**: 评论者对快速的前沿推理感到兴奋，有用户表示如果该功能正式开放，愿意支付目前 Claude 费用两倍的价格。也有评论较为谨慎，指出 OpenAI 与 Cerebras 没有明确宣称与标准 GPT-5.6 Sol 精度完全相同，且缺少定价信息令人关注。还有人强调，速度通过支持更多迭代来提升“思考质量”。

**标签**: `#AI`, `#LLM`, `#OpenAI`, `#Cerebras`, `#performance`

---

<a id="item-4"></a>
## [理解成为 AI 辅助编程时代的新瓶颈](https://www.geoffreylitt.com/2026/07/02/understanding-is-the-new-bottleneck) ⭐️ 8.0/10

这篇文章指出，随着大语言模型（LLM）越来越多地自动化代码生成，软件团队的主要约束从编写代码转变为理解他们需要审查和维护的代码。文章呼吁采用新的实践和工具来支持人类对 AI 生成代码的理解。 这种转变影响着每一个使用 AI 辅助工具的开发者以及管理他们的工程领导者。如果理解成为瓶颈，代码生成带来的生产力提升将受限于人类对陌生代码建立心智模型的速度。 这篇随笔是对此前关于‘新瓶颈’写作的延续，更多涉及工程文化主题而非具体基准测试。社区评论指出，LLM 生成的 PR 描述往往描述机械性改动但缺乏动机，并且用 LLM 来生成理解会削弱人工验证 AI 输出的意义。

hackernews · sebg · 8月13日 18:47 · [社区讨论](https://news.ycombinator.com/item?id=49290299)

**背景**: 大语言模型（LLM）如今能够根据自然语言提示编写代码，但软件工程流程仍然依赖人类的判断。开发者必须审查代码的正确性、可维护性以及与现有架构的一致性，这需要真正的理解。随着代码生成变得日常化，快速阅读和推理代码的能力成为许多团队的限制因素。

**社区讨论**: 评论既有认同也有质疑。alecbz 报告 LLM 生成的 PR 描述普遍不受欢迎，因为它们只关注机制而非动机，并警告 AI 生成的理解无法替代对 LLM 本身的验证需求。madrox 认为这个瓶颈是早就存在的领导力挑战，iainctduncan 则要求更具体地定义‘新瓶颈’，euthymiclabs 引用 Mitchell Hashimoto 的‘我读代码’来强调个人责任。

**标签**: `#AI`, `#software engineering`, `#LLM`, `#code comprehension`, `#engineering culture`

---

<a id="item-5"></a>
## [SQLite 作者 Richard Hipp 2024 年演讲详解 SQLite 内部原理](https://www.youtube.com/watch?v=ZSKLA81tBis) ⭐️ 8.0/10

在 2024 年的一次演讲中（幻灯片日期为 2024 年 6 月 24 日），SQLite 的创造者 Richard Hipp 详细介绍了 SQLite 的架构与设计。该演讲深入讲解了 SQLite 的内部工作方式，包括其核心组件和设计取舍。 这场演讲意义重大，因为它是 SQLite 原作者亲自进行的罕见深度技术讲解，为使用 SQLite 或构建数据库系统的开发者提供了独特的洞见。它有助于揭开 SQLite 内部机制的神秘面纱，促进社区对嵌入式数据库工程的更深理解。 演讲详细介绍了 SQLite 的核心组件，例如 VDBE（虚拟数据库引擎）字节码解释器、管理页面缓存与事务的 pager（页面管理模块），以及 B-tree 索引结构。幻灯片可在 sqlite.org/talks/howitworks-20240624.pdf 公开获取。

rss · Lobste.rs · 8月13日 11:56

**背景**: SQLite 是一个自包含的嵌入式关系数据库管理系统，无需独立服务器进程即可运行。当执行 SQL 语句时，SQLite 会解析、分析并编译成一种字节码程序，然后由 VDBE（虚拟数据库引擎）执行。数据库文件按页面（page）组织，页面缓存由 pager 模块管理，负责事务与回滚；B-tree 则用于高效存储和索引数据。这场演讲深入讲解这些内部机制，让更广泛的受众能够理解其设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sqlite.org/vdbe.html">The Virtual Database Engine of SQLite</a></li>
<li><a href="https://dev.to/lovestaco/the-pager-where-sqlite-transactions-touch-disk-reality-44cg">The Pager: Where SQLite Transactions Touch Disk Reality - DEV Community</a></li>
<li><a href="https://fly.io/blog/sqlite-internals-btree/">SQLite Internals: Pages & B - trees · The Fly Blog</a></li>

</ul>
</details>

**标签**: `#sqlite`, `#database`, `#systems`, `#talk`, `#architecture`

---

<a id="item-6"></a>
## [SvelteKit 3 进入候选发布阶段](https://svelte.dev/blog/sveltekit-3-release-candidate) ⭐️ 8.0/10

Svelte 团队在官方博客上宣布了 SvelteKit 3 的候选发布（Release Candidate）。这标志着该框架第三个主要版本的首个候选版正式登场。 SvelteKit 3 的 RC 是 Svelte 生态系统的重大里程碑，因为 SvelteKit 是使用 Svelte 构建生产级应用的官方应用框架。对更广泛的 JavaScript 社区而言，它也代表了 Next.js 之外的有力选择。 该博客文章附带了 Lobsters 上的讨论链接，显示社区正在积极参与。作为候选发布版，该版本旨在供开发者测试和反馈，随后发布正式稳定版。

rss · Lobste.rs · 8月13日 19:08

**背景**: Svelte 是一个组件框架，它将组件编译为高效的 JavaScript，而不是在浏览器中运行虚拟 DOM。SvelteKit 是构建在 Svelte 之上的应用框架，类似于 React 生态中的 Next.js，提供路由、服务端渲染、数据获取等生产级特性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://svelte.dev/docs/kit/introduction">Introduction • SvelteKit Docs</a></li>
<li><a href="https://svelte.dev/tutorial/kit/introducing-sveltekit">Introduction / What is SvelteKit? • Svelte Tutorial</a></li>
<li><a href="https://en.wikipedia.org/wiki/Svelte">Svelte - Wikipedia</a></li>

</ul>
</details>

**标签**: `#sveltekit`, `#svelte`, `#release`, `#javascript`, `#webdev`

---

<a id="item-7"></a>
## [采用 CHERI 实现内存安全与细粒度隔离](https://www.infoq.com/presentations/cheri-memory-safety-compartmentalization/) ⭐️ 8.0/10

这场 InfoQ 演讲讨论了如何实际采用 CHERI（硬件增强 RISC 指令能力）为软件系统实现内存安全与细粒度隔离，重点关注该技术的真实落地考量。 CHERI 是一项重要的研究技术，可从根本上消除整类内存安全漏洞，有望重塑系统安全。这场聚焦采用实践的演讲，对评估 Arm Morello 等新一代硬件的系统与安全工程师极具参考价值。 CHERI 在传统指令集上扩展出硬件强制的 capability，用携带权限和地址范围限制的有界引用取代原始指针。该技术已在 MIPS、RISC-V 和 ARMv8-A（通过 Morello 原型）上实现，并配有适配的 Clang/LLVM、FreeBSD 和 FreeRTOS 软件栈。

rss · Lobste.rs · 8月13日 14:30

**背景**: CHERI 是剑桥大学与 SRI International 的联合研究项目，重新审视硬件/软件接口的基本设计选择，以提供细粒度内存保护。它在指令集中加入 capability，将内存引用限制在特定地址范围和允许操作内，有助于防止缓冲区溢出、释放后使用等内存安全问题。Arm 在 UKRI 资助的 Digital Security by Design（DSbD）项目下开发的 Morello 芯片，是在 AArch64 上评估 CHERI 特性以用于生产的主要原型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Capability_Hardware_Enhanced_RISC_Instructions">Capability Hardware Enhanced RISC Instructions - Wikipedia</a></li>
<li><a href="https://www.cl.cam.ac.uk/research/security/ctsrd/cheri/">Department of Computer Science and Technology: Capability ...</a></li>
<li><a href="https://ctsrd-cheri.github.io/cheri-faq/">CHERI Frequently Asked Questions - CHERI FAQ</a></li>

</ul>
</details>

**标签**: `#CHERI`, `#memory safety`, `#compartmentalization`, `#security`, `#systems`

---

<a id="item-8"></a>
## [ZOOMSDAY：Zoom 标注功能零点击漏洞可致远程代码执行](https://a.security/blog/asecurity-zoomsday) ⭐️ 8.0/10

a.security 发布的一篇博客披露了"Zoomsday"漏洞集，即 Zoom 标注功能中的零点击漏洞，可在参会者客户端上实现远程代码执行。Zoom 已修复这些漏洞，对应编号为 CVE-2026-53413、CVE-2026-53414 和 CVE-2026-53415。 Zoom 是最广泛使用的视频会议平台之一，而这些零点击漏洞影响所有支持平台，攻击者可能无需用户交互即可控制参会者设备。漏洞的严重性和影响范围使其对企业和个人用户都极为重要，同时也凸显了专有协作协议中固有的风险。 这些漏洞位于 Zoom 处理会议中共享标注数据的代码中，作为会议参与者的攻击者无需受害者进行任何操作即可触发代码执行。研究人员将此漏洞集命名为"Zoomsday"，该漏洞同样影响共享屏幕的演示者，因为恶意标注数据通过共享屏幕传递。

rss · Lobste.rs · 8月13日 15:27

**背景**: 零点击漏洞是一种无需用户交互（例如点击链接或打开文件）即可入侵目标设备的网络安全漏洞。Zoom 的标注功能允许参与者在共享屏幕上绘制或输入内容，而 Zoomsday 漏洞即利用了这一功能所使用的专有协议。零点击漏洞对攻击者极具价值，因为它们可被用于隐蔽的大规模入侵。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://securityaffairs.com/197042/hacking/zoom-patches-zoomsday-zero-click-flaw-enabling-remote-code-execution.html">Zoom Patches “Zoomsday” Zero-Click Flaw Enabling Remote Code Execution</a></li>
<li><a href="https://www.malwarebytes.com/blog/bugs/2026/08/zoomsday-flaws-could-let-one-zoom-participant-attack-another">"Zoomsday" flaws could let one Zoom participant attack another | Malwarebytes</a></li>
<li><a href="https://thehackernews.com/2026/08/zoom-annotation-flaws-could-let-meeting.html">Zoom Annotation Flaws Could Let a Meeting Participant Hijack Another Attendee's Client</a></li>

</ul>
</details>

**标签**: `#security`, `#Zoom`, `#vulnerabilities`, `#zero-click`, `#research`

---

<a id="item-9"></a>
## [DeepSeek V4 Pro API 上线、腾讯 HY4 计划、iPhone 18 涨价传闻](http://www.geekpark.net/news/368747) ⭐️ 7.0/10

8 月 13 日，DeepSeek 正式版 V4 Pro 发布并更新至 API，调用模型名保持不变。新版本增强了 Agent 能力，支持 OpenAI 的 Responses API 和 Codex 接入，定价为缓存命中每百万输入 token 0.025 元、缓存未命中每百万输入 3 元、每百万输出 6 元。 这一事件意义重大，因为 DeepSeek V4 Pro 以远低于西方顶级模型的成本提供了接近 Anthropic Fable 5 的性能，可能重塑 AI API 市场格局。同时，它支持 Responses API 和 Codex，使已经使用 OpenAI 工具的开发者可以轻松迁移。 该模型采用 MoE 架构，总参数量 1.6T，激活参数 49B，支持 100 万 token 上下文窗口。官方渠道放出的评测对比表显示，DeepSeek-V4-Pro-0813 在多项测试中接近 Fable 5 水平，相比此前预览版能力大幅提升。

rss · 极客公园 · 8月13日 00:14

**背景**: DeepSeek 是中国一家以发布高性价比、开放权重语言模型著称的 AI 实验室。DeepSeek V4 Pro 是大型 MoE 模型，总参数 1.6T（激活 49B），支持 100 万 token 上下文，面向高级推理、编程和长时间运行的 Agent 任务。Responses API 是 OpenAI 用于构建类 Agent 应用的统一接口，Fable 5 是 Anthropic 发布的最高能力广泛可用模型。本条新闻是极客公园的每日科技资讯汇总，还涵盖腾讯计划发布 HY4 大模型、iPhone 18 涨价传闻等消息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-pro">DeepSeek V4 Pro - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro">deepseek-ai/DeepSeek-V4-Pro · Hugging Face</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI模型`, `#API`, `#腾讯`, `#科技新闻`

---