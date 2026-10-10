---
layout: default
title: "Horizon Summary: 2026-10-10 (ZH)"
date: 2026-10-10
lang: zh
---

> 从 65 条内容中筛选出 8 条重要资讯。

---

1. [Cloudflare 收购 Deno，计划终止 Deno 运行时开发](#item-1) ⭐️ 9.0/10
2. [Python 3.15.0 正式发布，成为最新主要版本](#item-2) ⭐️ 9.0/10
3. [OpenAI 解雇三名安全研究员，当事人否认行为不当](#item-3) ⭐️ 8.0/10
4. [谷歌开源 ML Drift：面向端侧推理的跨平台 GPU 引擎](#item-4) ⭐️ 8.0/10
5. [Matthew Green：公钥加密有 15%概率失去信任](#item-5) ⭐️ 7.0/10
6. [Unison 语言的部署平台 Unison Cloud 现已开源](#item-6) ⭐️ 7.0/10
7. [LLVM 的 RISC-V 后端把无分支代码编译成了分支](#item-7) ⭐️ 7.0/10
8. [matklad 主张自旋锁通常是错误默认选择](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Cloudflare 收购 Deno，计划终止 Deno 运行时开发](https://deno.com/blog/cloudflare) ⭐️ 9.0/10

Cloudflare 宣布收购 Deno，并表示将在接下来一年内继续维护 Deno 运行时，每月发布包含缺陷修复和安全更新的版本，之后将彻底终止对运行时的开发。Deno 仍会保持开源，但其后续开发将取决于是否有其他团队接手维护。 Deno 是与 Node.js、Bun 并列的三大 JavaScript/TypeScript 服务端运行时之一，其开发实质中止将重塑运行时格局，可能促使用户回流到 Node.js 或 Bun。这笔交易也引发了更广泛的思考：当风险投资支持的开源项目被大型云厂商收购后，开源可持续性将何去何从。 Cloudflare 承诺仅提供为期一年的月度维护版本（缺陷修复与安全更新），此后 Deno 运行时开发即告停止，但源代码仍保持开源，允许他人 fork 或继续开发。这次收购被普遍视为对 Deno 团队的“人才收购”（acqui-hire），而 Cloudflare 的 workerd 运行时有可能吸收 Deno 的安全与沙箱机制。

hackernews · ilreb · 10月9日 13:03 · [社区讨论](https://news.ycombinator.com/item?id=50019911)

**背景**: Deno 是由 Node.js 原作者 Ryan Dahl 创建的 JavaScript 与 TypeScript 运行时，初衷是修复 Node.js 长期存在的设计问题，例如权限模型和模块处理方式。它开箱即支持 TypeScript、npm 兼容以及默认安全（未经显式授权便无法访问文件、网络或环境变量）。Deno 由获得风险投资的 Deno Land 公司开发，团队还打造了 Deploy 平台以及 celld 项目——Durable Objects 模式的开源实现。Cloudflare 运营着无服务器边缘平台，其 workerd 运行时和 Workers 产品与 Deno 处于同一 JavaScript 执行领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deno.com/">Deno , the drop-in JavaScript runtime for Node developers</a></li>
<li><a href="https://blog.logrocket.com/dev/what-is-deno/">What is Deno , and how is it different from Node.js? - LogRocket Blog</a></li>
<li><a href="https://betterstack.com/community/guides/scaling-nodejs/nodejs-vs-deno-vs-bun/">Node.js vs Deno vs Bun: Comparing JavaScript Runtimes</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（1021 分、528 条评论）整体充满惋惜与批评：许多开发者称 Deno 是自己最喜欢的运行时，对创新戛然而止感到难过；也有人指责团队追逐风投资金，而没有选择接受捐赠或付费模式。一个反复出现的观点是，Deno 转向优先兼容 npm 使项目变得臃肿，也标志着其最初极简愿景的丧失，还有人认为这条新闻的标题更应写成“Deno 通过人才收购被实质关停”。

**标签**: `#Deno`, `#Cloudflare`, `#JavaScript`, `#Runtimes`, `#Open Source`

---

<a id="item-2"></a>
## [Python 3.15.0 正式发布，成为最新主要版本](https://www.python.org/downloads/release/python-3150/) ⭐️ 9.0/10

Python 3.15.0 已在 python.org 官方下载页正式发布，这是 CPython 参考实现的下一个重要功能版本。发布页面提供了常规的下载资源与发布说明，相关消息也在 Lobsters 社区引发了讨论。 作为全球使用最广泛的编程语言之一，Python 每一个新的次要版本发布都会影响整个生态：库作者需要适配支持，Linux 发行版和云厂商需要打包，CI 流水线与教程也会逐步切换默认版本。因此 Python 3.15.0 将成为未来一年大量 Python 工具链、文档和教学资料所对标的新基准。 CPython 的功能版本按年度节奏发布，新的版本线通常以一个正式版开始，随后是一系列错误修复补丁版本（如 3.15.1、3.15.2 等），最终才转入仅提供安全修复的维护阶段。对于固定 Python 版本的项目来说，应尽早规划兼容性测试，因为最新版本可能会引入弃用变更、默认行为调整，以及第三方 wheel 包支持滞后的问题。

rss · Lobste.rs · 10月9日 17:07

**背景**: Python 的参考实现 CPython 遵循 PEP 602 确定的年度发布周期，大约每年 10 月发布一个新的次要版本。每个次要版本都会带来新的语言语法、标准库变化以及性能优化；此后旧版本会先进入错误修复阶段，再转为数年的仅安全更新阶段。用户可以通过源码压缩包、Windows 和 macOS 官方二进制安装包，或者操作系统自带的包管理器来安装这些版本。

**标签**: `#Python`, `#programming languages`, `#release`, `#software engineering`, `#open source`

---

<a id="item-3"></a>
## [OpenAI 解雇三名安全研究员，当事人否认行为不当](https://techcrunch.com/2026/10/08/fired-openai-safety-researchers-dispute-misconduct-claims-warn-of-chilling-effect/) ⭐️ 8.0/10

OpenAI 以“不当处理研究信息”为由解雇了三名从事 AI 安全工作的研究员。被解雇的员工否认这一不当行为指控，并发布了公开信，警告此举将对公司内外的 AI 安全工作产生寒蝉效应。 这场争议让外界聚焦于头部 AI 实验室如何在商业推进速度与内部安全监督之间取舍，也可能让研究员不敢再提出顾虑。由于 OpenAI 的安全文化被视为整个行业的风向标，此事件很可能影响其他实验室、监管机构以及潜在求职者对 AI 安全岗位的看法。 该事件已引来 CNBC 和 BBC 的后续报道，被解雇的研究员还发布公开信陈述己方说法。OpenAI 将解雇定性为研究信息处理问题，而研究员则认为被开除是因为他们“把安全放在优先位置”，双方在事实认定和动机解释上均存在分歧。

hackernews · trakkstar · 10月9日 10:00 · [社区讨论](https://news.ycombinator.com/item?id=50018350)

**背景**: 大型实验室内部的 AI 安全研究员通常负责对齐研究、风险评估以及模型发布前后的内部审查，这类工作容易与产品和商业团队产生张力。在科技行业的劳资争议中，公开信是常见手段，当内部申诉渠道被认为无效时，员工会借此争取公众和同行的支持。此处的“寒蝉效应”指其他员工可能因担心遭遇同样后果而自我审查、不敢上报风险。

**社区讨论**: 评论区大多对 OpenAI 的说法持怀疑态度：有人将其比作核能行业对风险的迟来反思，也有人指出，公司如此公开地开除对受聘审计人员直言不讳的员工，实在令人侧目。还有人贴出了研究员的公开信和 BBC 报道，并以黑色幽默调侃说，说不定是某群失控的 LLM 视这些安全研究员为威胁，才策划了这场解雇。

**标签**: `#OpenAI`, `#AI safety`, `#AI governance`, `#tech ethics`, `#labor disputes`

---

<a id="item-4"></a>
## [谷歌开源 ML Drift：面向端侧推理的跨平台 GPU 引擎](https://github.com/google-ai-edge/ml-drift) ⭐️ 8.0/10

谷歌 AI Edge 团队以 Apache 2.0 许可证开源了 ML Drift，这是一款专为端侧 AI/ML 推理打造的高性能跨平台 GPU 计算引擎。它屏蔽了 OpenGL ES、OpenCL、Metal 与 WebGPU 这些底层硬件的复杂细节，并作为谷歌 LiteRT 运行时内部的核心 GPU 加速引擎。 统一的跨平台 GPU 抽象层有望让开发者更容易在 Android、iOS 和 Web 上部署实时 ML 与生成式 AI 功能，而无需编写针对特定厂商的 GPU 代码。由于它同时为 LiteRT 提供动力，此次开源也巩固了谷歌在端侧 AI 技术栈中相对于其他推理运行时的地位。 谷歌声称其相比现有开源 GPU 推理引擎实现了数量级的性能提升，但博客主要展示的是移动端数据，并未在 CUDA 和 Vulkan 上与 vLLM 或 llama.cpp 进行对比。ML Drift 既可以作为 LiteRT 的后端，也能作为独立库用于自定义图形和推理运行时。

reddit · r/LocalLLaMA · pmttyji · 10月9日 15:50 · [社区讨论](https://www.reddit.com/r/LocalLLaMA/comments/1x1owzm/github_googleaiedgemldrift_gpuaccelerated_aiml/)

**背景**: LiteRT（原 TensorFlow Lite）是谷歌用于在边缘平台部署 ML 与生成式 AI 模型的高性能端侧运行时。端侧 GPU 对外暴露的计算 API 差异很大——Android 上常见 OpenCL 和 OpenGL ES，苹果设备使用 Metal，而 WebGPU 则是取代 WebGL 的较新跨平台 Web 标准。ML Drift 正是让一套推理引擎通过统一内核语言同时适配这些 API 的中间层。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/LiteRT">LiteRT</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebGPU">WebGPU</a></li>
<li><a href="https://github.com/google-ai-edge/litert">GitHub - google-ai-edge/LiteRT: LiteRT, successor to ...</a></li>

</ul>
</details>

**社区讨论**: 评论区主要聚焦于尚未被验证的性能声明，指出尽管谷歌声称实现了“数量级”提升，却缺少在 CUDA/Vulkan 上与 vLLM 或 llama.cpp 的对比。不少人解释了为何选择 OpenCL 而非 Vulkan：Adreno 的 OpenCL 驱动能以较低成本实现 fp16 配 fp32 累加，并把权重存放在纹理内存中，而 Vulkan 的 subgroup/coopmat 支持在不同 Mali 版本间参差不齐。他们也指出一个缺点——libOpenCL.so 从来不是 NDK 库，需要通过 dlopen 加载，且部分设备上根本不存在，从而被迫回退到 GLES。

**标签**: `#on-device-ml`, `#gpu-inference`, `#google-ai-edge`, `#litert`, `#opencl-vulkan`

---

<a id="item-5"></a>
## [Matthew Green：公钥加密有 15%概率失去信任](https://simonwillison.net/2026/Oct/9/matthew-green/) ⭐️ 7.0/10

密码学家 Matthew Green 公开给出了对最坏情况的粗略概率估计：大约 1% 的概率我们实际上就生活在“Minicrypt”之中——一个公钥加密在数学上不可能实现的世界；以及大约 15% 的概率我们会实质性地对当今依赖的公钥算法失去信心。他认为，AI 制造出密码学“意外”的速度，与人类替换标准的速度之间相差“好几个数量级”，因此只有当准备工作提前完成时才可能从中恢复。 公钥加密支撑着 HTTPS/TLS、代码签名、即时通讯应用、软件更新以及几乎所有数字信任机制，因此一旦信任崩塌，将是基础设施级别的事件，而不只是某个小众研究问题。Green 的核心观点是：标准机构和部署周期都按人类的时间尺度运转，这意味着安全社区必须在漏洞被确认之前很久就预先制定应急方案与迁移路径。 Green 自称是刻意扮演“小丑”角色的人，愿意提出那些“不够体面”的极端假设，因为其他人都不愿触碰；其中 1% 的 Minicrypt 估计是两者中更极端的一个——若真如此，任何类型的公钥方案都不可能存在，而不只是当前部署的这些。15% 这一数字指的是对现有算法失去信心，这属于社会与工程层面的失效模式，即使没有已被证明的数学破解也可能发生。

rss · Simon Willison · 10月9日 15:02

**背景**: Minicrypt 源自 Russell Impagliazzo 于 1995 年发表的论文《A Personal View of Average Case Complexity》，该文勾勒了五种可能的计算世界。在 Minicrypt 中，单向函数是存在的——因此对称加密、哈希和伪随机生成器都可正常工作——但公钥加密不可能实现；而公钥加密可行的世界被称为 Cryptomania。RSA、椭圆曲线密码学以及较新的后量子方案等现代标准，都隐含假设我们生活在 Cryptomania 之中，这也是为什么 Green 的假设被视为一种最坏情形，而非现实预测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Russell_Impagliazzo">Russell Impagliazzo - Wikipedia</a></li>
<li><a href="https://fanpu.io/blog/2022/impagliazzos-five-worlds/">Impagliazzo's Five Worlds, or The Computational (Im ...</a></li>
<li><a href="https://blog.computationalcomplexity.org/2004/06/impagliazzos-five-worlds.html">Computational Complexity: Impagliazzo 's Five Worlds</a></li>

</ul>
</details>

**标签**: `#cryptography`, `#public-key encryption`, `#AI risk`, `#security`, `#standards`

---

<a id="item-6"></a>
## [Unison 语言的部署平台 Unison Cloud 现已开源](https://www.unison-lang.org/blog/unison-cloud-open-source/) ⭐️ 7.0/10

为 Unison 编程语言打造的托管部署平台 Unison Cloud 已正式开源，任何人都可以自行托管和运行该平台。此前它仅作为托管服务提供，此次开源标志着向社区实验和自托管方向转变。 将 Unison Cloud 开源使开发者能够自行托管部署层，并自由试验 Unison 新颖的内容寻址代码模型在分布式系统中的应用，这可能有助于在函数式编程社区中扩大其采用范围。它还减少了对单一厂商来运行基于 Unison 的云应用的依赖。 Unison Cloud 的设计目标是让你通过一次函数调用即可部署到云端，像调用本地函数一样调用服务，并像访问内存数据结构一样方便地访问带类型的存储，所有这些都由类型检查器进行验证。此次发布支持自托管和更广泛的实验，不过其受众仍主要局限于函数式编程和分布式系统领域这一相对小众的群体。

rss · Lobste.rs · 10月9日 15:32

**背景**: Unison 是一门静态类型的函数式编程语言，以其内容寻址（content-addressed）代码模型而闻名：代码通过其内容的哈希值来标识，而不是通过名称或文件位置，这简化了重构和分布式执行。Unison Cloud 则是与之配套的托管平台，它把云部署变成普通的函数调用，其中的服务和带类型存储都由与代码其余部分相同的类型系统进行检查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.unison-lang.org/">The Unison language</a></li>
<li><a href="https://www.unison.cloud/">The Unison™ Cloud Platform | Deploy to the cloud with a ...</a></li>

</ul>
</details>

**标签**: `#programming-languages`, `#unison`, `#open-source`, `#cloud-computing`, `#functional-programming`

---

<a id="item-7"></a>
## [LLVM 的 RISC-V 后端把无分支代码编译成了分支](https://00f.net/2026/10/09/llvm-compiles-branch-free-code-into-branches-on-risc-v/) ⭐️ 7.0/10

00f.net 上的一篇博客文章分析了 LLVM 的 RISC-V 后端如何把本应无分支的代码转换成实际包含分支指令的机器码，记录了一个出人意料的代码生成怪异行为。文章逐步追踪编译器的降级决策，说明为什么原本无分支的源码经过 RISC-V 后端之后无法保持无分支。 无分支代码是避免分支预测失败、获得可预测性能的常用技巧，因此如果编译器悄悄重新引入分支，程序员的性能假设就会悄然失效。这对面向 RISC-V 的编译器工程师和系统开发者尤其重要，因为 RISC-V 基础指令集没有条件传送指令，除非启用可选的扩展，否则这类降级选择几乎无法避免。 根本原因在于 RISC-V 的基础整数指令集（RV32I/RV64I）没有条件传送指令，因此像 select 这样的操作必须降级为比较加分支，除非在目标架构字符串中启用了可选的 Zicond 扩展（它提供 czero.eqz 和 czero.nez）。因此文章揭示的是该目标架构本身的普遍局限，而非单纯的编译器缺陷；读者应检查自己的 -march 设置是否包含实现真正无分支代码所需的扩展。

rss · Lobste.rs · 10月9日 19:31

**背景**: 无分支代码用算术或位运算技巧代替条件判断，使指令流呈直线执行，这在分支预测失败代价高昂的 CPU 上很有帮助。RISC-V 是一个开放、可扩展的指令集架构，其精简的基础整数指令集刻意不包含条件传送等功能，而把这些留给可选的扩展。LLVM 是编译器基础设施，其 RISC-V 后端位于 llvm/lib/Target/RISCV，负责把通用中间表示翻译成 RISC-V 机器码，并且必须为那些基础指令集不直接支持的操作选择降级方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://llvm.org/docs/RISCVUsage.html">User Guide for RISC - V Target - LLVM</a></li>
<li><a href="https://en.wikipedia.org/wiki/Branch-free_code">Branch-free code</a></li>
<li><a href="https://github.com/lowRISC/riscv-llvm">GitHub - lowRISC/ riscv - llvm : RISC - V support for LLVM projects...</a></li>

</ul>
</details>

**标签**: `#LLVM`, `#RISC-V`, `#compilers`, `#code-generation`, `#systems`

---

<a id="item-8"></a>
## [matklad 主张自旋锁通常是错误默认选择](https://matklad.github.io/2020/01/02/spinlocks-considered-harmful.html) ⭐️ 7.0/10

在 2020 年 1 月 2 日发表的博客文章《Spinlocks Considered Harmful》中，rust-analyzer 的作者 matklad 认为自旋锁在并发代码中通常是错误的默认选择，并阐明了它真正适用的少数场景。该文随后在 Lobsters 上被重新提起，并引发了颇具深度的技术讨论。 同步原语的选择是每位系统与并发程序员都要反复面对的决策，而默认选项会悄然决定延迟、吞吐量与正确性。文章主张：除非有实测依据，否则应优先使用配条件变量的阻塞式互斥锁，而不是自旋，这有助于避免难以排查的 CPU 空转和优先级反转一类的问题。 自旋锁会让等待线程在循环中忙等而非休眠，因此会空耗 CPU 周期，只有在临界区极短、竞争很低时才有收益；它也不提供公平性或进展保证，且正确的实现必须处理好内存序（acquire/release 语义）。内核代码是典型的例外，因为无事可做的 CPU 可能别无选择只能自旋，但即便在内核中，也绝不能持有自旋锁进行可能阻塞的操作。

rss · Lobste.rs · 10月9日 13:33

**背景**: 自旋锁是一种锁：等待线程会在忙循环中反复轮询锁是否可用（即“自旋”），而不是被操作系统挂起，这种行为称为忙等待。互斥锁则会把等待线程阻塞，让 CPU 去执行其他工作，通常还会搭配条件变量来等待状态变化。这一权衡之所以重要，是因为等待时间极短时自旋可省去上下文切换的开销，但若锁被长时间持有或竞争激烈，自旋就会浪费 CPU，甚至导致其他线程饥饿。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Spinlock">Spinlock - Wikipedia</a></li>
<li><a href="https://www.baeldung.com/cs/mutex-vs-spinlock-concurrent-parallel-distributed-programming">Differences Between Mutex and Spinlock - Baeldung</a></li>
<li><a href="https://stackoverflow.com/questions/5869825/when-should-one-use-a-spinlock-instead-of-mutex">synchronization - When should one use a spinlock ... - Stack Overflow</a></li>

</ul>
</details>

**标签**: `#concurrency`, `#spinlocks`, `#systems-programming`, `#rust`, `#performance`

---