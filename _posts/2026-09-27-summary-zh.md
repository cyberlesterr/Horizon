---
layout: default
title: "Horizon Summary: 2026-09-27 (ZH)"
date: 2026-09-27
lang: zh
---

> 从 26 条内容中筛选出 6 条重要资讯。

---

1. [逆工程发现：Intel 8087 的正切算法不止是 CORDIC](#item-1) ⭐️ 8.0/10
2. [爱好者为已停产的 Steam Link 硬件装上了 NixOS](#item-2) ⭐️ 7.0/10
3. [2026 年 Rust 中 SIMD 的现状综述](#item-3) ⭐️ 7.0/10
4. [TLA⁺ 能否直接表达可达性属性？](#item-4) ⭐️ 7.0/10
5. [龙芯 LoongArch LA664 勘误：原子内存更新会被静默丢失](#item-5) ⭐️ 7.0/10
6. [KoboldCpp 内置轻量级 Agent 框架，系统提示仅 2k token](#item-6) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [逆工程发现：Intel 8087 的正切算法不止是 CORDIC](http://www.righto.com/2026/09/8087-tangent-cordic.html) ⭐️ 8.0/10

Ken Shirriff 发表了一篇针对 Intel 8087 浮点协处理器的新逆向工程分析，通过研究其硅片电路与微码，还原了正切指令 FPTAN 的实现方式。分析结论是：8087 并未只使用单纯的 CORDIC 算法，而是把 CORDIC 与另一种方法结合起来，以同时获得高精度与高性能。 这一发现说明，作为 x87 浮点系列奠基者之一、并直接影响了 IEEE 754 标准的 8087，其数值算法比常被简称为“CORDIC 协处理器”的说法更为精巧。对于硬件与底层软件工程师而言，这是一个具体案例，展示了在 1980 年代初缺乏硬件乘法器的条件下，如何权衡精度、速度与芯片面积。 文章指出，尽管 8087 没有硬件乘法器、只能依赖移位相加类运算，它计算一次正切约需 90 微秒，而单独使用 8086 则需要约 13,000 微秒。维基百科的资料显示，8087 的加法、减法等基本运算可能耗时超过 100 个机器周期，部分指令甚至超过 1,000 个周期，整颗芯片的算力约为 50,000 FLOPS，功耗约 2.4 瓦。

rss · Lobste.rs · 9月26日 19:01

**背景**: Intel 8087 于 1980 年发布，是 8086 系列微处理器的第一款浮点协处理器，用于加速加、减、乘、除、开方等浮点运算，同时还能处理指数、对数和三角函数等超越函数，性能提升幅度约为 20% 到 500% 以上。CORDIC（坐标旋转数字计算机，又称 Volder 算法）是一种逐位迭代的移位相加算法，仅靠加法、减法、移位和查找表即可计算三角、双曲、指数与对数函数，因此常用于没有硬件乘法器的硬件平台。8087 的研发工作直接推动了 IEEE 754-1985 浮点标准的诞生，而 1981 年 IBM PC 主板加入协处理器插槽后，其销量大幅增长。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.righto.com/2026/09/8087-tangent-cordic.html">Reverse-engineering the vintage Intel 8087's tangent ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Intel_8087">Intel 8087 - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/CORDIC_algorithm">CORDIC algorithm</a></li>

</ul>
</details>

**标签**: `#reverse-engineering`, `#hardware-architecture`, `#floating-point`, `#Intel-8087`, `#CORDIC`

---

<a id="item-2"></a>
## [爱好者为已停产的 Steam Link 硬件装上了 NixOS](https://feyor.sh/blog/infecting-the-steam-link-with-nixos/) ⭐️ 7.0/10

feyor.sh 上的一篇博文《Infecting the Steam Link with NixOS》介绍了如何在 Valve 已停产的 Steam Link 串流盒上安装并运行 NixOS 这一采用声明式配置的 Linux 发行版。文章记录了让一个通用、可复现管理的 Linux 系统在原本只用于游戏串流的 ARM 小型机顶盒上启动的完整过程。 这具体地证明了 NixOS 的声明式、可复现模式可以被移植到厂商已经放弃的封闭消费级嵌入式硬件上——而这类设备通常只能沦为电子垃圾。对 Nix 社区而言，这也说明该发行版正在从服务器和桌面走向 ARM 嵌入式目标平台，而可复现构建与原子回滚在这类场景中尤其有价值。 Steam Link 是一台资源受限的 ARM 设备，Valve 和 NixOS 项目都不提供官方支持，因此这类移植属于社区努力，需要处理引导加载程序和内核，而不是使用标准安装镜像。NixOS 的设计正是这一实验的吸引力所在：一份声明式配置文件即可生成整个系统，从而支持在其他机器上构建出完全相同的系统、原子升级，以及在改动导致无法启动时回滚到上一个可用的系统代（generation）。

rss · Lobste.rs · 9月26日 13:45

**背景**: NixOS 是围绕 Nix 包管理器构建的 Linux 发行版，而 Nix 采用纯函数式的方式来管理软件包和系统配置。用户无需手动编辑文件，而是用 Nix 语言声明想要的系统，NixOS 再据此构建完整的系统 profile，这正是可复现部署、原子升级与回滚得以实现的原因。相比之下，Steam Link 是 Valve 于 2015 年 11 月推出的小型硬件设备，用于通过局域网把 PC 上的游戏串流到电视；Valve 在 2018 年 11 月停止了该硬件的生产，转向为手机、智能电视和树莓派提供软件版 Steam Link 应用。把一套完整的发行版移植到这样一台被放弃的封闭设备上，是典型的嵌入式系统与复古计算式折腾。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/NixOS">NixOS</a></li>
<li><a href="https://en.wikipedia.org/wiki/Steam_Link">Steam Link</a></li>

</ul>
</details>

**标签**: `#NixOS`, `#Steam Link`, `#embedded systems`, `#Linux`, `#hacking`

---

<a id="item-3"></a>
## [2026 年 Rust 中 SIMD 的现状综述](https://shnatsel.github.io/state-of-simd-rust-2026/) ⭐️ 7.0/10

Rust 贡献者 shnatsel（Sergey Davidoff）发布了一篇类似国情咨文的综述文章《2026 年 Rust 中 SIMD 的现状》，系统梳理了 Rust 语言在 SIMD 能力、稳定化进展以及生态工具方面的最新情况。文章汇总了 std::arch 中已稳定的架构特定 intrinsics、可移植 SIMD（portable SIMD）项目的推进状态，以及第三方 crate 的成熟度。 SIMD 是数值计算、编解码、加密和解析类工作负载中榨取 CPU 吞吐量的主要手段，因此 Rust 的 SIMD 稳定化节奏直接影响性能敏感型项目是否愿意从 C 或 C++ 迁移到 Rust。对系统编程和性能优化方向的开发者而言，这篇综述是一个阶段性的参考坐标，用来判断哪些 SIMD API 可以安全地用于生产环境。 文章区分了两类 SIMD 路径：std::arch 中的目标特定 SIMD 暴露了如 x86 AVX/AES 之类的厂商 intrinsics，但只能在对应架构上编译；而 std::simd 中的可移植 SIMD 可在所有目标上编译，并保证语义一致。portable SIMD 项目组长期维护着一份稳定化前的关键阻塞问题清单，同时该 API 的文档直接由主分支发布，说明其设计仍在演进之中。

rss · Lobste.rs · 9月26日 08:28

**背景**: SIMD（单指令多数据）是一种 CPU 并行计算形式，一条指令可同时作用于多个数据元素，对于计算模式规整、重复度高的负载能带来大幅加速。Rust 历史上通过两条路径来支持 SIMD：一是 std::arch 中暴露的、尚处于 unstable 状态的厂商 intrinsics；二是由 Portable SIMD 项目组开发的、与硬件无关的可移植抽象。2018 年的 RFC 2325 提出了让 SIMD intrinsics 在稳定版 Rust 上可用的目标，这一持续多年的稳定化努力正是本文 2026 年回顾的背景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://doc.rust-lang.org/stable/std/simd/index.html">std::simd - Rust</a></li>
<li><a href="https://github.com/rust-lang/portable-simd">GitHub - rust-lang/portable-simd: The testing ground for the ...</a></li>
<li><a href="https://rust-lang.github.io/rfcs/2325-stable-simd.html">2325-stable-simd - The Rust RFC Book - GitHub Pages</a></li>

</ul>
</details>

**标签**: `#rust`, `#simd`, `#performance`, `#systems-programming`, `#compilers`

---

<a id="item-4"></a>
## [TLA⁺ 能否直接表达可达性属性？](https://ahelwer.ca/post/2026-09-26-reachability/) ⭐️ 7.0/10

Andrew Helwer 在其博客上发表了一篇题为《Can we have reachability properties in TLA+?》的文章，探讨“可达性属性”——即某个特定状态能否真正被到达——能否在 TLA+ 规范语言中被直接表达。这是一篇面向形式化方法实践者的技术性深入文章，而非工具发布或版本更新公告。 “可达性”问题（即“这个状态究竟有没有可能出现？”）是工程师在设计并发或分布式系统时最常提出的疑问之一，因此厘清 TLA+ 能否直接表达这类属性，会直接影响实践者如何编写规范以及如何解读模型检查器的输出结果。对于被 AWS、Microsoft 等公司用来排查设计缺陷的语言来说，此类表达能力上的缺口会影响工具的演进方向，也会影响结论如何传达给非专家读者。 在 TLA+ 的实际使用中，可达性通常是间接回答的：把目标状态谓词的“取反”声明为不变式（invariant），随后 TLC 模型检查器会报告一次“违反”，而其反例轨迹恰恰就是通往该状态的路径——也就是说答案是反向呈现的。文章的行文表明，讨论的核心是语言的表达能力与规范的书写风格，而非工具本身的缺陷。

rss · Lobste.rs · 9月26日 15:49

**背景**: TLA+ 是 Leslie Lamport 创造的一种形式化规范语言，用于对程序与系统（尤其是并发和分布式系统）建模，其核心理念是“用简单的数学才能最精确地描述事物”。规范以“动作的时序逻辑”书写，并由 TLC 模型检查器等工具进行验证，后者会穷尽式地探索从初始状态出发可达的所有状态。TLA+ 中的属性传统上分为两类：安全性属性（不变式，即“坏事永远不会发生”）与活性属性（即“好事最终会发生”）。而可达性分析——询问某个状态或状态集合能否从初始状态到达——是形式化验证中的标准技术；由于它本质上是一个“是否存在某条行为轨迹”的存在性命题，因此难以被干净地归入上述安全性/活性二分法之中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TLA+">TLA+ - Wikipedia</a></li>
<li><a href="https://lamport.azurewebsites.net/tla/tla.html">My TLA+ Home Page</a></li>
<li><a href="https://www.prover.com/formal-methods/reachability-analysis/">Reachability analysis as a way to validate requirements and ...</a></li>

</ul>
</details>

**标签**: `#TLA+`, `#formal methods`, `#reachability`, `#formal verification`, `#software engineering`

---

<a id="item-5"></a>
## [龙芯 LoongArch LA664 勘误：原子内存更新会被静默丢失](https://jia.je/hardware/2026/09/24/loongson-cpu-erratum-en/) ⭐️ 7.0/10

jia.je 上发布的一篇详细分析记录了中国龙芯 LoongArch LA664 CPU 核心上的一处硬件勘误：原子内存更新可能被静默丢弃，从而产生“丢失更新”。该问题由 Wang Miao 于 2026 年 2 月在 LoongArch 服务器上为 Debian 打包数学软件 normaliz 时发现，当时该软件自带的测试卡在一个无法退出的死循环中。 对原子性保证的静默破坏，直接动摇了无锁算法、自旋锁和 compare-and-swap 循环所依赖的基础契约，因此任何运行在受影响 LoongArch 硬件上的软件都可能在没有任何明显硬件故障提示的情况下卡死或产生数据损坏。虽然该架构在中国以外的生态规模较小，但“CPU 悄悄破坏原子读-改-写”这一类缺陷，对所有思考内存模型与非 x86/ARM 架构上并发正确性的人都具有普遍的启发意义。 该故障表现为一个读-改-写序列的更新根本没有落地，而这正是让 compare-and-swap 或 load-linked/store-conditional 重试循环无限自旋、而不是显式报错的行为。LA664 是较新的 LoongArch 核心，引入了新的原子指令和硬件页表遍历；相关社区工作还指出，LLVM 在 LoongArch 上的 16 字节原子实现是由 ll.d/sc.q 循环构成的，因此这些原语中的细微问题会传导到编译器生成的原子操作中。

rss · Lobste.rs · 9月26日 18:44

**背景**: LoongArch 是龙芯自研的指令集架构，其 64 位版本称为 LA64，而 LA664 是其较新的 CPU 核心之一。无锁编程依赖原子读-改-写指令，在 RISC 风格指令集中通常以 load-linked/store-conditional 对（LoongArch 上为 ll.d/sc.q）实现，硬件必须保证其不可分割地执行；一旦硬件丢失更新，那些“重试直到成功”的代码就会永远循环下去。LoongArch 仍在持续演进——例如 V1.1 版本新增了字节和半字原子内存访问指令——因此这类勘误对面向该平台的操作系统、编译器和库开发者都很重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jia.je/hardware/2026/09/24/loongson-cpu-erratum-en/">One CPU Atomic Instruction, One Packaging Infinite Loop: The ...</a></li>
<li><a href="https://loongson.github.io/LoongArch-Documentation/LoongArch-Vol1-EN.html">LoongArch Reference Manual - Volume 1: Basic Architecture</a></li>
<li><a href="https://lists.nongnu.org/archive/html/qemu-devel/2024-10/msg01888.html">[PATCH v2 1/5] target/ loongarch : Add a new cpu_type la 664</a></li>

</ul>
</details>

**标签**: `#hardware`, `#cpu-erratum`, `#loongarch`, `#memory-model`, `#concurrency`

---

<a id="item-6"></a>
## [KoboldCpp 内置轻量级 Agent 框架，系统提示仅 2k token](https://www.reddit.com/r/LocalLLaMA/comments/1wqlyp8/introducing_koboldcpp_agent_and_a_plea_for_help/) ⭐️ 7.0/10

KoboldCpp 现已内置 Agent Harness（智能体框架），用户只需在 GUI 启动器的 Admin 标签页中勾选一个复选框，或在启动参数中加入 --agent 即可启用，作为 Opencode、Codex、Claude Code 等工具的轻量级替代方案。它内置 9 个工具，包含全部工具的系统提示仅 2k token，还能连接第三方后端或任何兼容 OpenAI Chat Completions 的接口。 此前要使用智能体工具，用户往往需要搭建复杂的外部框架，而把一个极简 agent 直接集成进广受欢迎本地 LLM 图形界面，大幅降低了完全离线运行 agent 的门槛。这对本地 LLM 社区意义重大，因为 KoboldCpp 极小的提示占用意味着上下文窗口中更多空间可以留给用户的实际任务。 用户可通过加载 mcp.json 文件来扩展 agent，MCP 工具会被共享给 agent；但需注意 MCP 工具在 KoboldCpp 服务端执行，而 agent 工具在 agent 客户端执行。工具调用确认提供三种审批模式（on/auto/off），作者也明确提醒用户在批准工具调用时要保持谨慎。

reddit · r/LocalLLaMA · HadesThrowaway · 9月26日 09:13

**背景**: Agent harness（智能体框架，也称智能体脚手架）是围绕语言模型的一层软件基础设施，让模型能够作为 agent 行动：它负责管理工具调用、记忆、状态持久化和反馈循环，因为模型本身是无状态、只能输出文本的。常见的框架包括 Anthropic 的 Claude Code、OpenAI 的 Codex 以及开源的 OpenCode。KoboldCpp 是一个自包含的 GGUF/GGML 文本生成程序，基于 llama.cpp 构建，界面灵感来自最初的 KoboldAI。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Agent_harness">Agent harness</a></li>
<li><a href="https://github.com/LostRuins/koboldcpp">GitHub - LostRuins/koboldcpp: Run GGUF models easily with a ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenCode">OpenCode</a></li>

</ul>
</details>

**社区讨论**: 讨论整体十分正面：有评论称赞 KoboldCpp 拥有最好的 KV cache 前缀匹配，是单客户端场景下最好的 llama.cpp 图形界面，老用户也表示会马上试用这个新 agent。点赞最高的观点聚焦于“9 个工具加起来只要 2k token 的系统提示”，并指出其他框架在模型还没看到用户第一条消息前就消耗了大约十倍的 token。也有用户表示自己已经不用 KoboldCpp 了但依然很喜欢它，并打算试用新功能。

**标签**: `#Local LLM`, `#KoboldCpp`, `#Agent Framework`, `#LLM Tooling`, `#Open Source`

---