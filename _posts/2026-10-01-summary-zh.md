---
layout: default
title: "Horizon Summary: 2026-10-01 (ZH)"
date: 2026-10-01
lang: zh
---

> 从 47 条内容中筛选出 9 条重要资讯。

---

1. [谷歌发布新一代前沿模型 Gemini 4 Argon](#item-1) ⭐️ 8.0/10
2. [EDG 将其商用 C/C++ 编译器前端开源](#item-2) ⭐️ 8.0/10
3. [VUSEC 公开 Branch Target Reuse：针对 JIT 引擎的新型 Spectre-v2 攻击](#item-3) ⭐️ 8.0/10
4. [CO₂Jump：让文本与图像生成保持一致的免训练采样器](#item-4) ⭐️ 8.0/10
5. [Xenova 在 Hugging Face 开源 200 多个 WebGPU 机器学习内核](#item-5) ⭐️ 8.0/10
6. [OpenAI 发布个人 AI 智能体 dots，并重构会员定价体系](#item-6) ⭐️ 7.0/10
7. [Hillel Wayne 解析 TLA+ 能验证什么、不能验证什么](#item-7) ⭐️ 7.0/10
8. [Nicholas Nethercote 谈 2026 年 9 月如何加速 Rust 编译器](#item-8) ⭐️ 7.0/10
9. [Backblaze 发布 2026 年第二季度硬盘故障率报告](#item-9) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [谷歌发布新一代前沿模型 Gemini 4 Argon](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/) ⭐️ 8.0/10

谷歌在其官方博客上发布了新一代前沿模型 Gemini 4 Argon，该消息迅速在 Hacker News 上引发热议，获得 861 分和 577 条评论。公告中提到，谷歌将继续从早期测试者处收集反馈并迭代护栏（guardrails），随后会“尽快”向开发者、企业和普通消费者开放。 这次发布为前沿 AI 实验室之间快速交替领先的循环又增添了一个例证，评论者借此论证该领域正变得更加分散——分布在超大规模云厂商、新兴云（neocloud）与创业公司之间，而非集中在单一赢家手中。对开发者而言，这也强化了一个务实建议：既然能力领先者每隔几个月就会更替，模型和供应商的选择就应保持可替换性。 Argon 目前尚未全面开放：谷歌表示仍在与早期测试者一起迭代护栏，之后才会向开发者、企业和消费者发布；一些评论者嘲讽这种分阶段做法是 Gemini“摆脱不了发不出模型的指控”。社区讨论还提到 Argon 智能体被用于在谷歌内部将 C/C++ 代码库迁移到 Rust，另有一条配套的 HN 帖文对“Gemini 4 Argon (High)”的智能水平、性能和价格做了分析。

hackernews · bradleyg223 · 9月30日 20:04 · [社区讨论](https://news.ycombinator.com/item?id=49913571)

**背景**: Gemini 是谷歌的多模态 AI 模型系列，而“前沿模型”通常指某家实验室在特定时期推出的能力最强、规模最大的那一类模型。在当前的 AI 格局中，谷歌、OpenAI、Anthropic 等主要实验室往往相隔数月就推出新一代旗舰模型，因此每次发布都会被从两方面评判：一是模型本身的原始能力，二是它如何改变竞争格局。“护栏”（guardrails）则指模型面向公众开放前施加的安全过滤与行为限制，它们常常会推迟正式发布的时点。

**社区讨论**: Hacker News 的评论者大多把这次发布视为对 Dario Amodei“集中化”（concentrating）论点的反证，认为 AI 能力正在向超大规模云厂商、新兴云和创业公司扩散，而非固化在先行者手中。一些人强调务实结论：要让模型和供应商保持可替换，并牢牢掌握自己的技能与基础设施；另一些人则惊叹于智能体出人意料的行为（例如逆向工程 GPU 驱动的内核接口以修复 ROCm 支持），同时批评其迟迟不开放正式发布、护栏工作仍未完成。

**标签**: `#AI/ML`, `#LLM`, `#Google Gemini`, `#model release`, `#AI competition`

---

<a id="item-2"></a>
## [EDG 将其商用 C/C++ 编译器前端开源](https://github.com/edgcpp/compiler) ⭐️ 8.0/10

在 2025 年 11 月于美国 Kona 举行的 ISO C++ 标准会议上，Edison Design Group（EDG）宣布公司将逐步结束运营，并会将其编译器前端开源；相关代码现已发布在 GitHub 仓库 edgcpp/compiler 中，其中包含前端以及 C 和 C++ 后端，另有 edgcpp.org 网站提供迁移说明与文档。 EDG 的前端是目前仅存的四个 C++ 前端之一（另外三个是 Clang、GCC 和 MSVC），并且被广泛授权使用——它是 Visual Studio IntelliSense 的底层实现，Intel 编译器在转向 Clang 之前也使用它，NVIDIA CUDA 编译器和众多代码分析工具同样依赖它。将一个成熟且经过商业验证的前端开源，为编译器研究者、工具开发者和教育工作者提供了一个此前无法获取的稀有参考实现。 EDG 在历史上颇为特殊：它是唯一实现了 C++98 `export template` 特性的前端，而该特性的实际使用经验也影响了后来的讨论，最终导致它在 C++11 中被废弃并移除。其前端支持 C++98/03、C++11、C++14 和 C++17，同时也支持 C89/C99 与 Embedded C，并正在推进 C++20 相关特性；不过，由于公司已宣布将于 2026 年关闭，此次放出的代码实际上已处于开发终点。

rss · Lobste.rs · 9月30日 22:06

**背景**: 编译器前端负责对源代码进行预处理和语法解析，并生成供后续阶段使用的中间表示，这也是许多商业编译器厂商选择授权 EDG 前端、而不是自行编写解析器的原因。EDG 由 J. Stephen Adamczyk 于 1988 年在新泽西州创立，其团队成员包括 John Spicer、Daveed Vandevoorde 等知名 C++ 专家。长期以来，该公司是向编译器与工具厂商出售 C++（早期还包括 Java 和 Fortran）前端授权，而不是自己发布编译器产品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Edison_Design_Group">Edison Design Group</a></li>
<li><a href="https://www.edg.com/c">The C++ Front End</a></li>
<li><a href="https://en.cppreference.com/cpp/language/templates">Templates - cppreference.com</a></li>

</ul>
</details>

**标签**: `#C++`, `#compilers`, `#open-source`, `#EDG`, `#tooling`

---

<a id="item-3"></a>
## [VUSEC 公开 Branch Target Reuse：针对 JIT 引擎的新型 Spectre-v2 攻击](https://www.vusec.net/projects/btr/) ⭐️ 8.0/10

阿姆斯特丹自由大学 VUSEC 实验室与圣安娜高等研究院的研究人员公开了名为 Branch Target Reuse（BTR）的新型 Spectre-v2 攻击技术，该论文已被 ACM CCS 2026 接收。研究团队在 Linux 内核的 BPF JIT、Oracle GraalVM 以及浏览器 JIT 引擎等多个目标上完成了验证，且涉及多家 CPU 厂商。 JIT 引擎广泛存在于所有主流浏览器和众多语言运行时之中，因此一种能够绕过现有 Spectre-v2 缓解措施并泄露内存的攻击，重新点燃了很多人以为已被控制的威胁类别。它可能被用于从 JavaScript 跨站窃取数据，或泄露内核内存，从而迫使浏览器厂商、运行时维护者和内核开发者重新审视 JIT 代码生成策略。 根据公开信息，BTR 利用了 JIT 编译代码会复用共享分支目标这一特性，使攻击者不再需要像经典 Spectre-v2 那样精细控制分支目标注入；据报道，即使在现有缓解措施启用的情况下，它仍能泄露 Linux 内核内存。由于根因在于生成代码本身而不仅是 CPU 微码，防御很可能需要在 JIT 编译器内部加固，而这通常会带来性能开销。

rss · Lobste.rs · 9月30日 18:06

**背景**: Spectre 是 2017 年公开的一类 CPU 推测执行漏洞；其中的 Spectre-v2 变体（CVE-2017-5715，即分支目标注入）会诱使分支预测器推测执行错误路径，其产生的缓存侧效应可能泄露私有数据。JIT（即时编译）引擎在运行时把字节码编译为本地机器码，被 JavaScript 引擎、Oracle GraalVM 以及 Linux 内核的 eBPF 子系统广泛使用。这类引擎会生成大量结构规整、间接分支目标可预测的代码，因此对这类攻击极具吸引力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.vusec.net/projects/btr/">Branch Target Reuse : Spectre-v2 Attacks in JIT Engines</a></li>
<li><a href="https://thehackernews.com/2026/09/new-spectre-v2-btr-attack-leaks-linux.html">New Spectre-v2 BTR Attack Leaks Linux Memory Despite Existing ...</a></li>
<li><a href="https://www.phoronix.com/news/Branch-Target-Reuse-BTR">Branch Target Reuse , BTR: New Spectre V2 Attack... - Phoronix</a></li>

</ul>
</details>

**标签**: `#security`, `#Spectre`, `#JIT`, `#side-channel`, `#CPU vulnerabilities`

---

<a id="item-4"></a>
## [CO₂Jump：让文本与图像生成保持一致的免训练采样器](https://www.reddit.com/gallery/1wtyl5m) ⭐️ 8.0/10

一篇 NeurIPS 2026 论文（由 Google、Google DeepMind 与石溪大学合作完成）提出了 CO₂Jump（自纠正耦合马尔可夫跳跃过程），这是一种无需额外训练的采样器，可让同时生成的文本与图像保持一致。该采样器利用文本置信度和跨模态注意力来引导图像更新，并可将低置信度的 token 重新掩码，从而在生成过程中修正此前的决策。 联合文本-图像生成模型可能出现“文字说对了、图却画错了”的情况，而单纯并行生成两种模态并不能保证二者一致。一个无需训练、同时提升编辑质量与图文对齐度的采样器，有望让联合多模态生成在自动生成教学内容、视觉推理等场景中更加可靠。 CO₂Jump 每个去噪步骤只需一次模型前向传播，且不引入额外训练，因为所有对比实验都使用同一个针对任务微调过的模型；在 8 到 512 个采样步骤范围内，它是所比较的采样器中唯一在编辑质量和图文对齐度上同时单调提升的方法。作者还发布了三个数据集——JEdit-1M、JMaze-200K 和 JNono-200K——并在图像编辑、迷宫求解和非 ogram（数织）任务上进行评测，其中“联合准确率”要求文本答案和生成图像同时正确。

reddit · r/MachineLearning · Upstairs_Theme2785 · 9月30日 07:28 · [社区讨论](https://www.reddit.com/r/MachineLearning/comments/1wtyl5m/concurrent_image_understanding_and_generation/)

**背景**: 许多扩散式多模态模型会同时生成文本和图像，但由于文本分支与视觉分支各自独立决策，两者可能相互矛盾。马尔可夫跳跃过程是一类随机过程：它在某个状态停留一段随机时间后“跳跃”到另一个状态；这里借用了该思想，让采样器在另一模态的证据与之冲突时能够“跳跃”，即修正或撤回某个 token。跨模态注意力则是计算不同模态之间动态依赖关系的机制，使一个模态能够影响另一个模态的更新方式。非 ogram（数织）是一种图形逻辑谜题，网格边缘的数字约束了每行每列需填充的格子数量，因此非常适合作为“文本答案与图像必须完全吻合”的测试任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.13188">[2607.13188] Concurrent Image Understanding and Generation ...</a></li>
<li><a href="https://www.mathematik.uni-muenchen.de/~jansen/jump-processes.pdf">MARKOV JUMP PROCESSES - LMU</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nonogram">Nonogram</a></li>
<li><a href="https://www.emergentmind.com/topics/cross-modal-attention">Cross - Modal Attention Mechanisms</a></li>

</ul>
</details>

**社区讨论**: 目前社区讨论较少但态度积极：一位评论者看好其在教育内容生成中的潜力，例如为数学题配图或为早期识字课文配图；另一位则对“广义信息智能”表达了兴奋之情。讨论中尚未出现批评性反驳或技术性质疑。

**标签**: `#multimodal generation`, `#diffusion models`, `#AI/ML`, `#NeurIPS`, `#image understanding`

---

<a id="item-5"></a>
## [Xenova 在 Hugging Face 开源 200 多个 WebGPU 机器学习内核](https://v.redd.it/0tyz8p6a7osh1) ⭐️ 8.0/10

Xenova 开源了一套 WebGPU 内核集合，覆盖 200 多种常见的机器学习算子，全部可以在浏览器中完全本地、高性能地运行。团队还计划把这些优化反向贡献到 Transformers.js、ONNX Runtime Web、LiteRT.js 等浏览器端机器学习运行时中。 浏览器端本地 AI 推理一直受限于缺少经过手工调优的高速 GPU 算子，因此一个覆盖广泛的开源内核库有望显著提升网页内模型的运行速度，并减少对云端推理的依赖。如果这些优化按计划进入 Transformers.js、ONNX Runtime Web 和 LiteRT.js，大量 Web 机器学习开发者无需改动自己的代码即可受益。 这些内核发布在 Hugging Face 的内核中心 huggingface.co/kernels?platform=webgpu，并配有技术博客 huggingface.co/blog/webgpu-kernels。它们面向 WebGPU 的计算路径而非较旧的 WebGL 方案；由于上游集成尚未完成，目前要享受这些优化仍需直接使用这套独立内核集合。

reddit · r/LocalLLaMA · xenovatech · 9月30日 16:02 · [社区讨论](https://www.reddit.com/r/LocalLLaMA/comments/1wu8tpg/we_just_opensourced_the_worlds_fastest_webgpu/)

**背景**: WebGPU 是一项 W3C 标准 API，让 JavaScript（以及 Rust、C++ 等语言）能够高效访问设备的 GPU，底层映射到 Vulkan、Metal 或 Direct3D 12，目标是取代 WebGL 成为 Web 的主流图形标准。Chrome 和 Edge 在 2023 年 4 月率先支持 WebGPU，Safari 26 于 2025 年 6 月加入，Firefox 141 则在 2025 年 7 月跟进，如今主流浏览器均已提供该能力。这里的“内核（kernel）”指的是实现单个算子（如矩阵乘法或卷积）的高度优化的 GPU 小函数，机器学习模型正是由这些算子组合而成。Transformers.js 是 Hugging Face 的 JavaScript 库，其 API 与 Python 版 transformers 基本一致，可让相同的预训练模型直接在浏览器或 Node.js 中运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebGPU">WebGPU</a></li>
<li><a href="https://huggingface.co/docs/transformers.js/index">Transformers . js · Hugging Face</a></li>
<li><a href="https://github.com/huggingface/transformers.js">GitHub - huggingface/ transformers . js : State-of-the-art Machine...</a></li>

</ul>
</details>

**社区讨论**: 讨论整体偏轻松而非技术性：有人询问视频和音频是怎么制作的，有人请求用“给五岁小孩解释”的方式说明 WebGPU（包括它到底是用本地 GPU 还是云端资源），还有人发段子和表情包。唯一较有实质意义的观点是期待未来网页应用能加载约 0.8GB 的决策模型并实时运行，例如用于 AI 参与的联机游戏。

**标签**: `#WebGPU`, `#Local AI`, `#Kernel Optimization`, `#Browser Inference`, `#Hugging Face`

---

<a id="item-6"></a>
## [OpenAI 发布个人 AI 智能体 dots，并重构会员定价体系](http://www.geekpark.net/news/372005) ⭐️ 7.0/10

北京时间 9 月 30 日凌晨，OpenAI 举办其宣称规模最大的一届开发者大会，一次性发布 25 项更新，核心是名为 dots 的个人 AI 智能体，由 GPT-6 Astra 驱动，自带云端运行环境、可连接数千款应用并持续自主完成任务，面向 Pro 及企业套餐用户开放。同一场大会上，OpenAI 还重构了 ChatGPT 会员体系：200 美元/月的 Pro 200 售价不变但新用户额度减半，同时新增 500 美元/月的 Pro 500 套餐，额度为 Plus 的 25 倍并独家开放 Astra Ultrafast 高速模式。 这次发布意味着 OpenAI 正从售卖模型调用转向售卖常驻的「AI 员工」，计价逻辑从 token 数量转为按交付工作量与运行速度收费，并试图把 ChatGPT 打造成人与智能体协作的统一入口。叠加其年化经常性收入已接近 700 亿美元、较三季度初增长超 70% 的消息，这将进一步激化与 Anthropic 的竞争，也刺激字节跳动豆包等中国厂商加速推出代号「Spell」的个人助理产品。 最具争议的是定价调整：尽管 GPT-6.1 Sol 等新模型的 API 价格大幅下调，但套餐内可用额度同步缩减，且高速的 Astra Ultrafast 模式消耗额度更快，引发开发者不满。OpenAI 同时推进平台化改造，新增插件生态、ChatGPT 账号登录、跨应用额度通用、团队资料空间、动态文档、新版 Codex 云端开发环境，并面向企业推出可直接采购第三方商业软件的软件市场，被外界比作微信小程序与账号体系。

rss · 极客公园 · 9月30日 00:25

**背景**: 所谓 AI 智能体（AI Agent），是指能代替用户执行多步操作（浏览网页、调用工具、读写文件）而不只是聊天问答的系统，OpenAI 此次推出的 dots 被描述为自带云端电脑与浏览器、可常驻运行的智能体。Ultrafast 是 OpenAI 最快的 API 服务层级，此前展示过让 GPT-5.6 Sol 提速至最高 14 倍、每秒输出约 750 个 token。豆包是字节跳动旗下的 AI 助手，代号「Spell」的项目被视为把其手机端积累的个人智能体能力延伸为独立应用，与 Meta、OpenAI 的同类动作相呼应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://open-ai-dots.com/">OpenAI Dots — Always-On AI Agents</a></li>
<li><a href="https://openai.com/index/gpt-6-astra/">GPT-6 Astra: A new generation of intelligence | OpenAI</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2088284569229333990">加入个人AI Agent大战！豆包被曝将推个人助理产品“Spell”，4月已内测</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI Agent`, `#SpaceX`, `#科技新闻`, `#定价策略`

---

<a id="item-7"></a>
## [Hillel Wayne 解析 TLA+ 能验证什么、不能验证什么](https://buttondown.com/hillelwayne/archive/what-tla-can-and-cant-check/) ⭐️ 7.0/10

知名形式化方法顾问、《Practical TLA+》作者 Hillel Wayne 发表了一篇题为《What TLA+ can and can't check》的解析文章，系统梳理了 TLA+ 工具链能够验证哪些属性、以及其保证在何处失效。这篇文章并未发布新工具或新版本，而是针对工程师在使用 TLA+ 设计并发与分布式系统时经常遇到的验证边界问题，给出了一次聚焦的技术澄清。 工程师常常高估模型检查所能提供的保证，把 TLA+ 检查通过等同于「代码是正确的」；厘清这些边界有助于团队避免盲目自信和误用工具。随着形式化方法在分布式系统与云基础设施领域越来越受关注，准确理解一门规格语言能保证什么、不能保证什么，对工程决策正变得愈发重要。 TLA+ 用集合论表达安全性属性（坏事永远不会发生）、用时序逻辑表达活性属性（好事终将发生），TLC 模型检查器则在有限状态模型上、在有限步数内穷举系统的所有可能行为来验证这些属性。关键在于，它检查的是规格而非实现，因此除非通过精化映射把规格与真实代码对应起来，或者用 TLAPS 写出机器可验证的证明，否则模型检查通过并不能直接保证上线的程序与设计一致。

rss · Lobste.rs · 9月30日 14:02

**背景**: TLA+ 是由 Leslie Lamport 创建、1999 年问世的规格语言，用于并发与分布式系统的设计、文档化和验证。它的规格并非用自然语言描述，而是用严谨的逻辑与数学语言书写，因此可以进行有限模型检查——模型检查器会穷举系统在若干执行步数内的所有可能行为，并查找对安全性、活性等目标属性的违反。2009 年出现的类伪代码方言 PlusCal 可以转译成 TLA+，便于描述顺序算法。更广义地说，形式化方法是指用数学上严谨的技术对软硬件系统进行规格化、开发、分析和验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TLA+">TLA+</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_checking">Model checking</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_methods">Formal methods</a></li>

</ul>
</details>

**标签**: `#TLA+`, `#formal-methods`, `#verification`, `#distributed-systems`, `#model-checking`

---

<a id="item-8"></a>
## [Nicholas Nethercote 谈 2026 年 9 月如何加速 Rust 编译器](https://nnethercote.github.io/2026/09/30/how-to-speed-up-the-rust-compiler-in-september-2026.html) ⭐️ 7.0/10

Nicholas Nethercote 发表了题为《How to speed up the Rust compiler in September 2026》的博文，介绍了近期用于加快 rustc 编译速度的技术与改动。这是他长期追踪 Rust 编译器性能的周期性更新系列中的最新一篇，而非某个单独的新版本或新功能发布。 编译速度一直是 Rust 开发者的痛点，尤其是在大型代码库和增量重建场景下，因此 rustc 任何实质性的提速都会直接改善开发者的日常效率。Nethercote 的这类文章之所以被广泛阅读，是因为它记录了哪些优化真正带来了收益以及原因，为编译器团队和外部贡献者留下了可参考的经验。 这篇文章是面向编译器工程师和 Rust 贡献者的技术深潜，内容属于渐进式更新——汇总的是累积的优化成果，而不是某个标志性的突破。由于 rustc 是自举（self-hosting）编译器，且通常通过 Cargo 间接调用，这类改动必须保证整个编译器自举过程的正确性，并在真实项目的 crate 上验证后才能合入。

rss · Lobste.rs · 9月30日 02:08

**背景**: rustc 是 Rust 编程语言的官方编译器，由 Rust 项目开发，采用 Apache 2.0 与 MIT 双许可证发布；它把 Rust 源代码翻译为本地机器码，并且自身就是用 Rust 编写的，每个新版本都由上一个稳定版编译而成。大多数开发者不会直接调用 rustc，而是使用 Rust 的标准构建工具与包管理器 Cargo，由它带着合适的选项去调用编译器。rustc 最广为人知的两点是：在编译期强制内存安全与线程安全的类型系统，以及能指向出错源码位置、常常还附带修复建议的错误信息；这种重量级的静态分析正是 Rust 构建显得较慢的重要原因之一。Nicholas Nethercote 是 Rust 编译器性能领域知名的人物，他的周期性博文更新是关注 rustc 速度的人常用的参考。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rust_compiler">Rust compiler</a></li>

</ul>
</details>

**标签**: `#Rust`, `#compiler optimization`, `#performance`, `#programming languages`, `#software engineering`

---

<a id="item-9"></a>
## [Backblaze 发布 2026 年第二季度硬盘故障率报告](https://www.backblaze.com/blog/backblaze-drive-stats-for-q2-2026/) ⭐️ 7.0/10

Backblaze 发布了 2026 年第二季度 Drive Stats 报告，基于其数据中心大规模硬盘集群，公布了硬盘故障率与可靠性数据。 Backblaze 季度 Drive Stats 被广泛引用，是少数基于大规模真实环境运行的硬盘故障数据来源之一，能帮助存储工程师、系统管理员和采购者比较不同厂商在真实负载下的可靠性，而不仅依赖厂商规格和实验室测试。 该报告基于 Backblaze 数十万块 24/7 运行的生产硬盘，底层数据集通常包含硬盘型号、容量、故障计数和 S.M.A.R.T.属性；不过，结果反映的是 Backblaze 特定工作负载，未必能推广到所有环境。

rss · Lobste.rs · 9月30日 14:28

**背景**: Backblaze 是一家云存储和备份服务商，定期发布其数据中心硬盘故障率统计。由于这些 Drive Stats 报告长期跟踪真实生产环境中的硬盘，而非仅依赖厂商可靠性规格或短期实验室测试，因此已成为存储社区的重要参考。该公司还公开原始数据（包括 S.M.A.R.T.属性），便于研究人员和管理员自行分析。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.backblaze.com/cloud-storage/resources/hard-drive-test-data">Hard Drive Reliability & Test Data | Backblaze</a></li>
<li><a href="https://huggingface.co/datasets/backblaze/Drive_Stats">backblaze / Drive _ Stats · Datasets at Hugging Face</a></li>

</ul>
</details>

**标签**: `#hard drives`, `#storage reliability`, `#Backblaze`, `#data centers`, `#hardware`

---