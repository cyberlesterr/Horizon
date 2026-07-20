---
layout: default
title: "Horizon Summary: 2026-07-20 (ZH)"
date: 2026-07-20
lang: zh
---

> 从 63 条内容中筛选出 12 条重要资讯。

---

1. [阿里巴巴发布 2.4 万亿参数开源权重 Qwen 3.8 模型](#item-1) ⭐️ 9.0/10
2. [保龄球馆老板用 1600 美元 ESP32 替换 12 万美元记分系统](#item-2) ⭐️ 8.0/10
3. [Claude Code 现已使用 Rust 重写的 Bun 运行时](#item-3) ⭐️ 8.0/10
4. [卖 2500 台 MIDI 录音机：硬件开发并不难](#item-4) ⭐️ 8.0/10
5. [AI 狂热正在侵蚀全球决策](#item-5) ⭐️ 7.0/10
6. [台积电对美投资增至 2650 亿美元，受 AI 需求和竞争推动](#item-6) ⭐️ 7.0/10
7. [AI 优化运动模糊，无人机实现近乎隐形](#item-7) ⭐️ 7.0/10
8. [数学家仍在寻找最快乘法算法](#item-8) ⭐️ 7.0/10
9. [硬核独立网：完全自主运营个人网站，每日成本仅 0.01 美元](#item-9) ⭐️ 7.0/10
10. [并行编程之道：原理与实践](#item-10) ⭐️ 7.0/10
11. [Lean 形式化验证入门教程发布](#item-11) ⭐️ 7.0/10
12. [研究 Linux 调度器，以及为何衡量指标至关重要](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [阿里巴巴发布 2.4 万亿参数开源权重 Qwen 3.8 模型](https://twitter.com/Alibaba_Qwen/status/2078759124914098291) ⭐️ 9.0/10

阿里巴巴发布了 Qwen 3.8，一个拥有 2.4 万亿参数的开源权重大型语言模型，直接与月之暗面 AI 最近发布的 Kimi K3 竞争，加剧了开源权重模型的竞赛。 此次发布加剧了开源权重 AI 的竞争，可能加速创新，并使前沿模型大众化，从而挑战如 GPT-4o 和 Claude 等闭源系统。 该模型以 Qwen3.8-Max-Preview 预览版发布，支持多模态，但详细的基准测试、许可证和活跃参数数量（暗示可能采用混合专家架构）尚未正式公布。

hackernews · nh43215rgb · 7月19日 08:44 · [社区讨论](https://news.ycombinator.com/item?id=48966120)

**背景**: 开源权重模型允许用户自由访问和修改模型的训练参数，与闭源 API 不同。混合专家（MoE）技术使得每次推理只激活部分参数，从而能以较低计算开销管理庞大的总参数量。几天前，月之暗面 AI 发布了 Kimi K3——一个 2.8 万亿参数的开源权重模型，促使阿里巴巴做出回应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ai21.com/glossary/foundational-llm/open-weights-model/">What is an Open-Weights Model? | AI21</a></li>
<li><a href="https://officechai.com/ai/alibaba-qwen-3-8/">Alibaba Announces 2.4 Trillion-Parameter Open-Weight Qwen 3.8 ...</a></li>
<li><a href="https://www.marktechpost.com/2026/07/19/alibaba-previews-qwen3-8-max-a-2-4-trillion-parameter-multimodal-model-days-after-moonshots-kimi-k3-open-weight-launch/">Alibaba Previews Qwen3.8-Max, a 2.4 Trillion-Parameter ...</a></li>

</ul>
</details>

**社区讨论**: 社区成员认为这对消费者是利好，一些人已在本地使用较小的 Qwen 模型。大家强烈希望 Qwen 3.8 能推出更小规模的版本，还有用户提到阿里巴巴云支付系统有问题，但期待开源发布。

**标签**: `#AI`, `#LLM`, `#open-weights`, `#Alibaba`, `#Qwen`

---

<a id="item-2"></a>
## [保龄球馆老板用 1600 美元 ESP32 替换 12 万美元记分系统](https://news.ycombinator.com/item?id=48968606) ⭐️ 8.0/10

一位保龄球馆老板使用 ESP32 微控制器、ESPNow 网状网络和树莓派构建了一个可工作的原型记分系统，每对球道成本仅 200 美元，并计划以 OpenLaneLink 项目开源硬件、固件和软件栈。 该项目凸显了开源硬件和软件大幅降低小众行业成本的潜力，让小企业能够绕过昂贵的供应商锁定并自定义系统，可能激励其他老旧设备领域进行类似改造。 系统采用 ESP32 节点构成 ESPNow 星形网状网络，各节点发射传感器事件并接受命令，RS485 作为有线后备。数据流至运行 Redis 和状态机的树莓派，任何 React 开发者均可构建自定义界面和动画。

hackernews · section33 · 7月19日 14:41

**背景**: ESP32 是一款低成本、低功耗的微控制器，内置 Wi-Fi 和蓝牙，广泛用于物联网项目。传统保龄球记分系统是昂贵的专有设备，依靠摄像头和传感器追踪球瓶并计分，每道成本常达数万美元。使用现代微控制器改造此类系统正成为一种降低成本、避免供应商锁定的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ESP32">ESP32</a></li>

</ul>
</details>

**社区讨论**: 社区反响非常积极，多位评论者分享了他们改造旧保龄球道或其他工业系统的经历。他们对成本降低和开源方法表示赞赏，部分人还提供了额外的技术见解或替代方案。

**标签**: `#ESP32`, `#IoT`, `#retrofitting`, `#embedded-systems`, `#hardware-hacking`

---

<a id="item-3"></a>
## [Claude Code 现已使用 Rust 重写的 Bun 运行时](https://simonwillison.net/2026/Jul/19/claude-code-in-bun-in-rust/#atom-everything) ⭐️ 8.0/10

Anthropic 的 Claude Code（版本 2.1.181，于 6 月 17 日发布）现已内置 Rust 移植版的 Bun 运行时，Simon Willison 通过检查二进制文件确认了这一点。 这展示了 AI 辅助完成从 Zig 到 Rust 的大规模生产级语言迁移，在数百万用户无感知的情况下提升了 Linux 启动速度 10%，并减少了内存相关 bug。 重写借助了 Claude 的预发布版本完成，目前使用的 Rust 版 Bun 为 canary 版本（v1.4.0），Claude Code 二进制文件中包含 563 个 .rs 源文件名。

rss · Simon Willison · 7月19日 03:54 · [社区讨论](https://news.ycombinator.com/item?id=48966569)

**背景**: Bun 是一个高速的一体化 JavaScript 运行时，最初使用 Zig 编写。Claude Code 是 Anthropic 推出的终端 AI 编程工具。2025 年 12 月 Anthropic 收购了 Bun，随后主导了从 Zig 到 Rust 的重写，旨在利用 Rust 的内存安全特性减少错误，并大量借助 AI 完成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bun.com/blog/bun-in-rust">Rewriting Bun in Rust | Bun Blog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Bun_(software)">Bun (software) - Wikipedia</a></li>
<li><a href="https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/">Rewriting Bun in Rust</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：有人质疑终端工具为何需要 JS 运行时；有人批评该项目在合并巨大 PR 时沟通不足、不够透明；也有开发者认可 Rust 相比 Zig 的内存安全优势，并视此次迁移为 AI 重写可行性的证明。

**标签**: `#bun`, `#rust`, `#claude-code`, `#ai-assisted-rewrite`, `#software-engineering`

---

<a id="item-4"></a>
## [卖 2500 台 MIDI 录音机：硬件开发并不难](https://chipweinberger.com/articles/20260719-hardware-is-not-so-hard) ⭐️ 8.0/10

作者销售了 2500 台 MIDI 录音机，并分享了挑战“硬件天生比软件难开发”观点的实际经验。 这一亲身经历为‘硬件难’的常见创业说法提供了有价值的反例，激励更多创造者考虑实体产品。 文章可能详细介绍了保持产品设计简单（如使用最少组件）并专注于狭窄应用场景的策略，从而使硬件开发变得可控。

hackernews · chipweinberger · 7月19日 10:34 · [社区讨论](https://news.ycombinator.com/item?id=48966713)

**背景**: MIDI（乐器数字接口）是允许电子乐器相互通信的技术标准。在创业领域，由于实体制造、供应链物流和生产后迭代困难，硬件通常被认为比软件更具挑战性。

**社区讨论**: 评论者指出，硬件难度随复杂性和产量增加而上升；一位满意的 JamCorder 客户称赞产品的简洁性和可靠性；其他人则强调了资金挑战以及风险投资对硬件回报的看法。

**标签**: `#hardware`, `#product-development`, `#MIDI`, `#lessons-learned`, `#startups`

---

<a id="item-5"></a>
## [AI 狂热正在侵蚀全球决策](https://simonwillison.net/2026/Jul/19/ai-mania/#atom-everything) ⭐️ 7.0/10

尼克·苏雷什的文章揭露了 AI 狂热如何驱使大公司的高管和工程师做出非理性决策，例如营收超 200 亿美元的公司高管从未使用过 AI 却制定了 AI 战略，以及工程师为讨好 AI token 排行榜用 Zig 重写代码。 这凸显了 AI 炒作与实际理解之间的危险脱节，可能导致资源浪费、技术债务和错失良机，对科技行业是一个警示。 具体事例包括：一位营收超 20 亿美元公司的高管从未用过 AI 却制定了 AI 战略；一名工程师为讨好 token 排行榜用 AI 将 Go 代码重写为 Zig；供应商因担心失去合同而不敢戳破客户不切实际的 AI 生产力宣称。

rss · Simon Willison · 7月19日 05:06

**背景**: Token 排行榜是一种追踪 AI 工具使用情况的指标，有时被公司用来衡量开发者的 AI 参与度；Zig 是一种系统编程语言，旨在成为 C 语言的现代替代品。文章源自尼克·苏雷什的博客，由技术评论家西蒙·威利森分享。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://whoburnedmore.com/">Who Burned More? AI Token Leaderboard</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>

</ul>
</details>

**标签**: `#AI`, `#hype`, `#corporate`, `#decision-making`, `#technology`

---

<a id="item-6"></a>
## [台积电对美投资增至 2650 亿美元，受 AI 需求和竞争推动](https://36kr.com/newsflashes/3903173412161415?f=rss) ⭐️ 7.0/10

台积电首席财务官黄仁昭宣布，公司将在美国追加投资 1000 亿美元，将对美投资承诺总额提升至 2650 亿美元，主要受到美国客户强劲需求以及来自英特尔和马斯克旗下 Terafab 的竞争压力推动。 这一巨额投资凸显了 AI 芯片需求的飙升以及台积电维持先进半导体制造主导地位的决心，同时也标志着在地缘政治和竞争挑战下，公司战略性地扩大在美生产。 台积电目前仍面临产能不足、无法满足所有客户订单的问题，因此正尽可能扩大产能；追加投资也旨在防止竞争对手夺走 AI 芯片需求机会。

rss · 36氪 · 7月19日 23:13

**背景**: Terafab 是由特斯拉、SpaceX 和英特尔联合开发的规划中的半导体制造工厂，目标是每年生产超过 1 太瓦的 AI 计算能力，全面建设的总投资估计高达 13 万亿美元，这对台积电构成了显著的竞争威胁。全球芯片短缺和 AI 热潮使得供应链紧张，推动代工厂扩大产能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Terafab">Terafab</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#AI`, `#investment`, `#TSMC`, `#supply chain`

---

<a id="item-7"></a>
## [AI 优化运动模糊，无人机实现近乎隐形](https://36kr.com/newsflashes/3903163375110018?f=rss) ⭐️ 7.0/10

美国西北大学的工程师研制出一款四旋翼无人机，通过 AI 优化的高速旋转产生运动模糊，利用人类视觉感知特点，使可见度降至传统无人机的十分之一。 这种全新的伪装方法绕开了传统材料，有望用于野生动物监测、生态调查和基础设施巡检，在不干扰环境的情况下实现隐蔽观察。 该无人机的几何结构是从两万种稳定飞行配置中通过 AI 优化选出的，重新排列了电机、螺旋桨、电路板和配重，以最大化运动模糊的错觉效果。

rss · 36氪 · 7月19日 23:03

**背景**: 运动模糊是快速移动的物体看起来模糊或透明的视觉现象，就像旋转的风扇叶片。人类视觉系统难以追踪高速运动，从而产生感知缺口，该无人机正是利用了这一点。传统的无人机伪装常采用着色或透明材料，而这种方法通过动态运动融入背景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mccormick.northwestern.edu/news/articles/2026/07/new-spinning-drone-hides-in-plain-sight/">New Spinning Drone Hides in Plain Sight</a></li>
<li><a href="https://bioengineer.org/stealthy-spinning-drone-blends-in-with-everyday-objects/">Stealthy Spinning Drone Blends In With Everyday Objects</a></li>

</ul>
</details>

**标签**: `#AI`, `#Drone`, `#Camouflage`, `#Motion Blur`, `#Human Visual Perception`

---

<a id="item-8"></a>
## [数学家仍在寻找最快乘法算法](https://www.scientificamerican.com/article/mathematicians-still-dont-know-the-fastest-way-to-multiply-numbers/) ⭐️ 7.0/10

《科学美国人》发表了一篇文章，探讨了确定大整数相乘最快算法的这一长期未解问题，并强调了当前实际方法与理论最优之间的差距。 乘法是计算中的基础操作，更快的算法可加速密码学、科学模拟和大数据处理。这一持续存在的差距反映了计算复杂性和算法设计中的深层挑战。 目前已知渐近最快的算法由哈维和范德霍文于 2019 年提出，达到 O(n log n)时间复杂度，但因常数因子极大而无法实用。实际效率最高的算法仍是肖恩哈格-施特拉森算法，复杂度为 O(n log n log log n)。目前尚未证明 O(n log n)是否为绝对下界。

rss · Lobste.rs · 7月19日 07:50

**背景**: 从历史上看，乘法算法从朴素的 O(n²)方法演进到卡拉楚巴的 O(n^1.58)，以及基于快速傅里叶变换的肖恩哈格-施特拉森算法（1971 年，复杂度 O(n log n log log n)）。2019 年，O(n log n)算法终被实现，但它是'银河算法'——仅在天文数字规模下才更快。O(n log n)是否为真正下界这一根本问题仍未解决，使乘法复杂度成为计算机科学中的经典开放问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Schönhage-Strassen_algorithm">Schönhage-Strassen algorithm</a></li>
<li><a href="https://www.unsw.edu.au/news/2019/04/david-harvey-s-algorithm-multiplies-integers-faster-than-all-pre">David Harvey 's algorithm multiplies integers faster than all previous...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multiplication_algorithm">Multiplication algorithm - Wikipedia</a></li>

</ul>
</details>

**标签**: `#mathematics`, `#algorithms`, `#computational complexity`, `#multiplication`, `#computer science`

---

<a id="item-9"></a>
## [硬核独立网：完全自主运营个人网站，每日成本仅 0.01 美元](https://www.neatnik.net/hardcore-indieweb) ⭐️ 7.0/10

新指南介绍了如何以每天仅 0.01 美元的成本，完全自主地托管和运行个人网站，实现极低成本的独立网络存在。 这种超低成本的方法使几乎任何人都能实现完全自主的网络发布，推动了数字主权，并向中心化平台的统治地位发起挑战。 该指南可能利用极其廉价的云服务或静态托管，配合自定义域名，通过低端 VPS 优惠或免费层服务将成本控制在每日 0.01 美元。

rss · Lobste.rs · 7月19日 04:07

**背景**: IndieWeb 运动鼓励通过个人网站而非企业社交媒体来掌控在线身份，强调数据所有权和开放标准。节俭计算倡导最小化计算资源消耗，实现可持续性。该指南融合了这些理念，实现了极致的成本效益。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/IndieWeb">IndieWeb</a></li>
<li><a href="https://arxiv.org/abs/2303.06642">[2303.06642] Frugal Computing -- On the need for low-carbon and sustainable computing and the path towards zero-carbon computing</a></li>
<li><a href="https://indieweb.org/">IndieWeb</a></li>

</ul>
</details>

**标签**: `#indieweb`, `#self-hosting`, `#frugal-computing`, `#web-development`, `#independence`

---

<a id="item-10"></a>
## [并行编程之道：原理与实践](https://smolnero.com/posts/the-zen-of-parallel-programming) ⭐️ 7.0/10

这篇文章对高效并行编程进行了反思性探索，侧重于核心原则和最佳实践，而非特定技术。 随着多核架构变得无处不在，理解并行编程范式对性能关键型软件至关重要；本文提炼了面向从业者的永恒见解。 文章可能涵盖并发模型、同步以及避免常见陷阱等主题，但摘要中未提供具体细节。

rss · Lobste.rs · 7月19日 20:19

**背景**: 并行编程涉及同时执行多个计算以提高性能，需要管理协调、数据共享和潜在的竞争条件。这种反思性的“禅”式方法可能强调简单性和基本真理。

**标签**: `#parallel-programming`, `#concurrency`, `#software-engineering`, `#best-practices`, `#performance`

---

<a id="item-11"></a>
## [Lean 形式化验证入门教程发布](https://hashcloak.com/blog/tutorial-introduction-to-formal-verification-with-lean-(part-1)) ⭐️ 7.0/10

一个使用 Lean 定理证明器进行形式化验证的新教程系列已发布，第一部分现已推出。 该教程通过引导式介绍现代证明助手 Lean，降低了学习形式化验证的门槛，形式化验证是开发高可靠性软件的关键技术。 该教程使用最新版本 Lean 4，它能生成 C 代码并包含卫生宏系统；内容涵盖形式化验证和定理证明的基础知识。

rss · Lobste.rs · 7月19日 17:35

**背景**: 形式化验证是通过数学方法证明软件或硬件相对于其规范的正确性。Lean 是一个由微软开发的证明助手和函数式编程语言，基于归纳构造演算。它允许用户编写可由计算机检查的形式化证明，从而确保正确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_theorem_prover">Lean theorem prover</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification</a></li>

</ul>
</details>

**标签**: `#formal verification`, `#lean`, `#theorem proving`, `#programming languages`, `#verification`

---

<a id="item-12"></a>
## [研究 Linux 调度器，以及为何衡量指标至关重要](https://pradyun.net/blog/metrics_matter.html) ⭐️ 7.0/10

一篇由 Pradyun 撰写的技术博客深入探讨了 Linux 调度器的行为，并强调了选择合适指标进行准确性能分析的重要性。 这对系统工程师和性能分析师很重要，因为错误的指标可能导致误导性的优化和糟糕的系统性能。 文章研究了不同 Linux 调度器（如 CFS 和 EEVDF）在各种负载下的行为，并警告不要仅依赖吞吐量等简单指标，而忽视公平性和延迟。

rss · Lobste.rs · 7月19日 00:45

**背景**: Linux 使用多种调度类，包括用于普通任务的完全公平调度器（CFS）和内核 6.6 中引入的更新版 EEVDF 调度器。衡量调度性能的指标包括周转时间、响应时间和公平性等。选择恰当的指标至关重要，因为针对某一指标优化的调度器可能在其他指标上表现不佳。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.kernel.org/scheduler/index.html">Scheduler — The Linux Kernel documentation</a></li>
<li><a href="https://linuxvox.com/blog/linux-scheduler/">Mastering the Linux Scheduler: An In-Depth Guide - linuxvox.com</a></li>
<li><a href="https://medium.com/geekculture/process-scheduling-in-linux-592028a5d545">Process Scheduling In Linux . The Conductor Of Processes | Medium</a></li>

</ul>
</details>

**标签**: `#linux`, `#scheduling`, `#performance`, `#metrics`, `#systems`

---