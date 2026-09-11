---
layout: default
title: "Horizon Summary: 2026-09-11 (ZH)"
date: 2026-09-11
lang: zh
---

> 从 56 条内容中筛选出 12 条重要资讯。

---

1. [Calif Research 展示 WeWorm：借助 AI 打造的微信通话零点击蠕虫](#item-1) ⭐️ 9.0/10
2. [DeepSeek 发布 V4-1 Flash：552B 多模态 MoE，支持百万级上下文](#item-2) ⭐️ 9.0/10
3. [Shopify 从 React Native 回归原生 Swift 与 Kotlin](#item-3) ⭐️ 8.0/10
4. [OpenAI 被质疑使用未署名数学成果，研究人员追问信任问题](#item-4) ⭐️ 8.0/10
5. [Rust 成为微软的一级（Tier-1）语言](#item-5) ⭐️ 8.0/10
6. [索尼因数字游戏"所有权"问题面临诉讼：玩家是否真正拥有已购游戏](#item-6) ⭐️ 8.0/10
7. [trynix.dev 让任何 Nix 软件包在浏览器 QEMU 虚拟机中启动](#item-7) ⭐️ 8.0/10
8. [Forgejo 16.0.4 修复严重远程代码执行漏洞](#item-8) ⭐️ 8.0/10
9. [OpenJDK 提出 JEP 544：Java 代码提前编译](#item-9) ⭐️ 8.0/10
10. [Raymond Chen 揭秘 Windows XP 如何为你的初始用户头像选图](#item-10) ⭐️ 7.0/10
11. [微信悄然测试「小微 AI 社交」，迈出 Agent 间沟通第一步](#item-11) ⭐️ 7.0/10
12. [Suno v6：首个与音乐产业合作打造的 AI 音乐模型](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Calif Research 展示 WeWorm：借助 AI 打造的微信通话零点击蠕虫](https://simonwillison.net/2026/Sep/10/calif-research/) ⭐️ 9.0/10

Calif Research 公开发布了 WeWorm 的演示，称其是首个经由微信通话在 iOS 和 Android 两端传播的零点击蠕虫，受害者在完全不接听电话、不触碰手机的情况下也会被攻陷。该团队表示，他们借助 AI 在约两天内找到漏洞并写出首个远程代码执行（RCE）利用程序，随后又用大约一周时间构建出完整的蠕虫。 如果这些说法成立，这标志着 AI 辅助攻击性安全研究的一次转折：这种规模的蠕虫过去需要更大的团队耗时数月才能完成，而如今它瞄准的是在两大主流移动平台上拥有十几亿用户的通讯应用。这也给手机厂商和腾讯带来压力，要求它们更快修补那些无需任何用户交互即可触发的通话协议栈漏洞。 相关报道称该攻击链利用了微信 VoIP 通话协议栈中的内存破坏漏洞，受影响范围可能覆盖 iOS 与 Android 上约 14 亿个微信账号；即使受害者接听电话也听不到任何声音，而此次发布的只是概念验证演示，并非真实攻击活动的证据。Calif Research 表示仅发布演示，人类团队的职责限于选定目标和安全测试，因此漏洞的实际修补状态以及与厂商的协调情况仍是关键待解问题。

rss · Simon Willison · 9月10日 00:56

**背景**: 零点击漏洞利用是指无需受害者做任何操作即可触发——在这里，仅仅收到一通微信语音通话就够了，而大多数攻击都需要用户打开文件或点击链接。远程代码执行（RCE）意味着攻击者能通过网络在目标设备上运行自己的代码，正是这种能力把单个漏洞升级为完整的账号劫持。蠕虫则进一步具备自我传播能力：被感染的设备会被用来攻击受害者的联系人，从而使感染在无人干预的情况下指数级扩散。微信是腾讯旗下占据主导地位的中文通讯与通话应用，因此其通话协议栈中的缺陷会波及 iOS 和 Android 上极其庞大的用户群。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://calif.io/research/weworm">WeWorm | Calif</a></li>
<li><a href="https://cybersecuritynews.com/weworm-first-0-click-worm/">WeWorm – First 0-Click Worm Spreading Through WeChat Calls ...</a></li>
<li><a href="https://www.techtimes.com/articles/327153/20260910/wechat-zero-click-worm-built-ai-days-voip-bug-put-billion-accounts-risk.htm">WeChat Zero-Click Worm Built By AI In Days: VoIP Bug Put ...</a></li>

</ul>
</details>

**标签**: `#ai-security-research`, `#zero-click-exploit`, `#wechat`, `#remote-code-execution`, `#worm`

---

<a id="item-2"></a>
## [DeepSeek 发布 V4-1 Flash：552B 多模态 MoE，支持百万级上下文](https://www.reddit.com/gallery/1wcbid7) ⭐️ 9.0/10

DeepSeek 发布了 DeepSeek-V4.1-Flash，这是一个多模态混合专家（MoE）模型，主干参数量为 552B，支持最长一百万个 token 的上下文，并已在 Hugging Face 上以开放权重形式公开（huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash）。该发布迅速在 Reddit 上引发大量讨论，获得约 1282 个赞、93% 的点赞率。 这是中国团队又一次重量级的开放权重发布，性能已接近前沿水平，尤其在智能体编程（agentic coding）方面，从而持续对闭源模型厂商形成压力，也扩大了开发者可自行托管或通过低成本 API 调用的选择空间。超大稀疏模型、100 万 token 上下文与激进的 KV cache 压缩相结合，说明长上下文推理正在从理论走向实用。 社区成员指出，该模型在预填充（prefill）阶段仅激活约 8B 参数、解码（decode）阶段约 16B 参数，这正是尽管主干高达 552B 却依然能低成本提供服务的原因；同时还提到它采用了 QAT KV cache 量化与 FP4，并引入了 N-gram/Engram 结构。实际部署仍是门槛：有评论称它无法装进双 DGX Spark，需要把 256GB 内存的服务器升级到 384GB，另有评论提到 Hugging Face 上的权重约为 485B 参数。

reddit · r/LocalLLaMA · tiguidoio · 9月10日 06:54 · [社区讨论](https://www.reddit.com/r/LocalLLaMA/comments/1wcbid7/deepseek_v41_flash_is_out/)

**背景**: 混合专家（MoE）模型包含许多独立的“专家”子网络以及一个路由器，每个 token 只会被路由到其中少数几个专家，因此总参数量很大，但每个 token 实际消耗的算力较小。“多模态”指模型除文本外还能处理图像等其他模态的信息；“开放权重”则意味着训练好的参数可以被下载，任何人都能自行运行、微调或本地部署，而不必只通过 API 调用。上下文长度指模型一次能考虑多少输入内容，而 KV cache 是生成过程中为保存这些上下文所占用的显存/内存，因此社区称 100 万 token 上下文仅需约 900MB 缓存才格外引人注目。在 DeepSeek 的命名中，“Flash”通常代表推理更快、服务成本更低的版本，而非最小的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.plainenglish.io/mixture-of-expert-architecture-7be02b74f311">Mixture of Expert Architecture. Definitions and Applications included...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multimodal_large_language_model">Multimodal large language model</a></li>
<li><a href="https://awesomeagents.ai/tools/best-open-weights-models-2026/">Best Open-Weights AI Models 2026: Llama, DeepSeek, Qwen</a></li>

</ul>
</details>

**社区讨论**: 社区情绪整体偏正面，但在实用性上存在分歧：不少用户为又一次强力的开放权重发布叫好，称赞其 KV cache 压缩效果以及接近前沿的智能体编程基准成绩；也有人抱怨模型规模太大、自己的硬件根本跑不动。多位评论者质疑“Flash”这一命名是否还合适，因为参数量增加且改用 FP8、N-gram 与 FP4 QAT；还有评论认为按 sqrt(P x A) 的粗略估算，该模型能力大致相当于同等训练的 62B 稠密模型，并表示自己更想要稠密版本。

**标签**: `#DeepSeek`, `#LLM`, `#Mixture-of-Experts`, `#Multimodal`, `#Open Weights`

---

<a id="item-3"></a>
## [Shopify 从 React Native 回归原生 Swift 与 Kotlin](https://shopify.engineering/back-to-native) ⭐️ 8.0/10

Shopify 工程团队发布文章，解释为何放弃 React Native，转而用 iOS 的 Swift 和 Android 的 Kotlin 原生技术重写其移动应用。该消息在 Hacker News 上引发热烈讨论（约 704 分、467 条评论），话题集中在跨平台与原生开发的取舍、AI 辅助重写的可行性以及长期维护成本。 Shopify 是公开从 React Native 回退的重量级公司之一，这为“共享代码库是用短期速度换取长期性能、体验打磨和平台专精人才”的观点提供了有力佐证。这一决定及社区反响，可能影响其他大型产品公司在跨平台框架与纯原生技术栈之间的选择。 Swift 与 Kotlin 各自需要专门的平台技能，而且与 Kotlin Multiplatform 不同，Swift 没有官方的一等方案用于跨移动平台共享业务逻辑，这会提高人员配置与代码重复的成本。评论者还指出，LLM 代码生成可能降低此类重写的成本，但质疑者认为复杂性应当被驯服，而不是被放大。

hackernews · Lobste.rs · 9月10日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49643982)

**背景**: React Native 是 Meta 推出的跨平台框架，允许开发者用一套 JavaScript/React 代码同时构建 iOS 和 Android 应用，这使企业过去能复用在 Web 端的开发者来做移动端，从而以更低成本更快上线。其代价是应用需经过桥接层或 JavaScript 运行时而非纯平台代码执行，可能影响渲染性能、平台专属体验以及对最新原生 API 的使用。原生开发则在 iOS 上使用苹果的 Swift/Objective-C、在 Android 上使用谷歌的 Kotlin/Java，能完全掌控平台能力，但需要维护两套代码库和两类人才。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://reactnative.dev/">React Native · Learn once, write anywhere</a></li>
<li><a href="https://kotlinlang.org/docs/multiplatform/native-and-cross-platform.html">Cross-platform and native app development: How do you choose? | Kotlin Multiplatform Documentation</a></li>
<li><a href="https://www.sketchflow.ai/blog/engineering/native-code-vs-cross-platform-why-your-mobile-app-needs-real-swift-and-kotlin">Why Native Code Beats Cross-Platform for Mobile Apps</a></li>

</ul>
</details>

**社区讨论**: 总体舆论倾向于支持迁离 React Native，一位 iOS 工程师表示这一决定印证了其长期以来对共享代码库的怀疑。多位评论者分享了自己的迁移经历：有人用 LLM 智能体在一夜之间移植了约 15–20 个页面，并借助 Maestro 做测试；也有人反驳“是 LLM 才让迁移变得可负担”的说法，指出自己早在 2026 年之前完成的重写基本没有借助 AI。反复出现的提醒是：AI 会让人倾向于不断叠加复杂度，而非控制复杂度。

**标签**: `#React Native`, `#Mobile Development`, `#Swift`, `#Kotlin`, `#Software Engineering`

---

<a id="item-4"></a>
## [OpenAI 被质疑使用未署名数学成果，研究人员追问信任问题](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

研究人员在 Mastodon、X 和 Bluesky 上就“能否放心把未发表的数学工作交给 OpenAI”提出伦理与信任方面的质疑：据称数学家与 OpenAI 模型之间的一次协作，最终产出了未对相关研究人员署名的成果。该讨论最初发自 mathstodon.xyz 实例，随后被 Hacker News 转载，获得约 594 个赞和 594 条评论。 如果学术研究者与 AI 公司分享未发表的想法后可能失去署名权，那么 AI 实验室目前赖以获取专家反馈的非正式协作模式就难以为继，数学家可能干脆不再参与。这场争议还牵动一个更广泛的争论：AI 系统在解决开放问题上究竟应得多少功劳，其输出究竟是真正的推理，还是对人类输入的回收再利用。 据报道，OpenAI 坚称用于得出该结果的模型并未在这些协作聊天记录上训练；批评者则指出，在 OpenAI 得知某个重要数学证明可能已进入该模型训练数据后不久，公司仍从一个尚在训练中的模型生成了 3000 亿个输出 token，时机令人生疑。核心技术分歧在于：该成果究竟来自预训练阶段对共享对话的记忆，还是来自在可验证数学任务上做强化学习时模型自主发现的全新技巧；此外，OpenAI 向大量研究者提供免费模型访问权限，也使“用户”与“合作者”的界限变得模糊。

hackernews · pred_ · 9月10日 06:49 · [社区讨论](https://news.ycombinator.com/item?id=49639408)

**背景**: Mathstodon.xyz 是一个面向数学从业者的 Mastodon 实例，其网页界面支持 LaTeX 渲染，因此这场技术讨论最初在此发酵，随后扩散到 X 和 Bluesky。在学术数学界，标注贡献者、引用已有工作是基本的职业规范，未经署名地使用他人想法被视为严重的不当行为。与此同时，主流 AI 公司通常在服务条款中写明用户对话可能被用于改进模型，并常常向研究者提供免费或折扣的前沿模型访问权限，这种组合使得“咨询”与“训练数据”之间的界限变得难以分辨。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mathstodon.xyz/">A Mastodon instance for maths people. We have LaTeX rendering in...</a></li>
<li><a href="https://atprotocol.dev/bluesky-and-did-plc/">Bluesky and DID PLC</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上同情这些研究者：得票最高的类比是把 OpenAI 比作一个人类合作者——从共同讨论中拿走想法后独自发表且不署名，这在人类身上显然是不道德的。另一些人认为两件事可以同时成立：聊天记录确实可能通过预训练微妙地塑造模型的隐层表示，而在可验证数学任务上做强化学习，也确实可能产生与任何具体共享想法无关、事实上超越人类的技巧。还有一派怀疑整个前提，追问 AI 究竟是在推进开放问题，还是研究者的最新提示词只是泄漏进了训练数据；也有人认为在得知关键信息后仍用尚在训练的模型跑出 3000 亿 token，这种时机安排难免让人怀疑是“平行建构”。

**标签**: `#AI ethics`, `#research integrity`, `#OpenAI`, `#mathematics`, `#attribution`

---

<a id="item-5"></a>
## [Rust 成为微软的一级（Tier-1）语言](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 8.0/10

微软正式将 Rust 认定为一级（Tier-1）编程语言，这一认定意味着内部团队拥有一条从本地开发直达生产环境的成熟路径。根据公告，一级语言地位涵盖安全工具链构建、高效的开发者工具、质量工作流、深度平台集成以及合规支持。 这一认定表明，内存安全的系统级编程已在全球最大的操作系统与工具厂商之一成为主流，可能影响微软未来构建 Windows 和 Azure 的方式。它也让外界更加确信，在全新系统项目上，Rust 已是 C++ 和 C# 的有力竞争者，而非小众实验。 评论者指出，微软计划借助自动化工具在 2030 年前将约 10 亿行代码转换为 Rust，目标是实现“1 名工程师、1 个月、100 万行代码”，同时 DARPA 资助的项目将 C 到 Rust 的转换工作分配给六个不同团队。讨论中另一个值得注意的细节是，微软似乎已用 MSVC 的后端替换了 LLVM，这将是 Windows 上 Rust 编译器工具链的一次重大变化。

hackernews · Lobste.rs · 9月10日 13:39 · [社区讨论](https://news.ycombinator.com/item?id=49643546)

**背景**: Rust 是一门系统级编程语言，其编译器会在编译期强制执行内存与线程安全规则，从而消除缓冲区溢出、释放后使用（use-after-free）等困扰 C 和 C++ 代码的整类缺陷。微软长期发现内存安全问题占其安全漏洞的大多数，因此更安全的系统语言具有战略吸引力。所谓“一级（Tier-1）”并非性能排名，而是指一门语言在公司内部获得的官方工程支持、工具链与平台集成级别。迁移遗留的 C/C++ 代码之所以困难，是因为正确的转换需要让既有行为显式化，以便 Rust 编译器和静态分析工具能够进行验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/">Guest Post: Rust Is Tier-1 Language at Microsoft</a></li>
<li><a href="https://blog.jetbrains.com/rust/2026/07/27/cpp-to-rust-migration/">C++ to Rust Migration: By Luca Palmieri from Mainmatter</a></li>
<li><a href="https://locka99.gitbooks.io/a-guide-to-porting-c-to-rust/content/">Introduction · A Guide to Porting C and C++ code to Rust</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论总体积极，评论者认为此举证明 Rust 已是成熟、严肃的竞争者，而非快速迭代的“新兵”语言，并指出所有拥有 C/C++ 工具链的主要操作系统厂商如今都已向内存安全选项多元化布局。一些人援引微软提出的 2030 年前完成 10 亿行代码自动化迁移的目标，以及 DARPA 的 C 到 Rust 转换工作作为具体证据；也有人就 Rust 与 Zig、Odin 等较新的“更好的 C”语言的成熟度展开辩论，还有评论者认为从 LLVM 切换到 MSVC 后端才是真正的头条新闻。

**标签**: `#rust`, `#microsoft`, `#systems-programming`, `#memory-safety`, `#language-adoption`

---

<a id="item-6"></a>
## [索尼因数字游戏"所有权"问题面临诉讼：玩家是否真正拥有已购游戏](https://consumerrights.wiki/w/Sony_PlayStation_digital_game_ownership_lawsuit) ⭐️ 8.0/10

一个消费者权益维基页面整理了索尼自家网站上关于玩家"拥有"其数字游戏的表述，并附带了针对 PlayStation 用户是否真正拥有已下载游戏的诉讼内容，该页面正在 Hacker News 上热传。引用的法庭文件显示，索尼在驳回起诉的动议中主张数字购买并不赋予用户对某一份副本的排他所有权，并以两名原告分别在不同日期购买同一款游戏（《生化危机：安魂曲》）的假设例子作为论据。 该案触及数字所有权的核心问题：商店中的购买究竟属于真实财产，还是仅仅是可以被撤销的授权，这会影响所有销售可下载内容的平台。案件同时凸显出服务条款中的强制仲裁条款与集体诉讼豁免权如何将此类纠纷挡在法庭之外，使消费者难以通过集体行动维权。 根据讨论内容，PlayStation 服务条款在第 14 条中设置了具有约束力的仲裁协议与集体诉讼豁免条款，并要求不愿受其约束的用户在接受协议后 30 天内以书面形式通知索尼。该维基页面的目的是汇总索尼自家网站上声称玩家"拥有"数字游戏的表述，这些表述可能与其法律抗辩相互矛盾。

hackernews · haunter · 9月10日 12:18 · [社区讨论](https://news.ycombinator.com/item?id=49642531)

**背景**: 数字游戏、电影及其他可下载内容通常是以授权方式而非完全产权的方式出售，这也是商店日后能够从用户库中移除已购内容的原因。索尼此前曾因从 PlayStation 内容库中移除用户已购的 Discovery 视频而遭到消费者强烈反对，而本次诉讼则是美国围绕最终用户许可协议与仲裁条款的众多纠纷之一。Consumer Rights Wiki 这一消费者权益维基专门记录此类案件以及企业用来界定买家实际所得权利的合同措辞。

**社区讨论**: 评论者普遍对索尼持批评态度：有人主张针对个人的强制仲裁本身就应当被认定为非法，因为其唯一作用就是剥夺消费者和劳动者的权利。其他人则用纸质书作类比——买一本书得到的是其中一册，而非唯一的一册——并指出索尼的抗辩可能会打开它自己不愿打开的大门；还有用户表示对该公司感情矛盾，并提及其当年在客户电脑上植入 rootkit 的事件。

**标签**: `#digital-ownership`, `#Sony`, `#consumer-rights`, `#arbitration`, `#gaming`

---

<a id="item-7"></a>
## [trynix.dev 让任何 Nix 软件包在浏览器 QEMU 虚拟机中启动](https://simonwillison.net/2026/Sep/10/trynix/) ⭐️ 8.0/10

Farid Zakaria 发布了 trynix.dev：它借助 qemu-wasm 在浏览器中通过 WebAssembly 运行一个 x86_64 Linux 虚拟机，并能用过去 13 年间的任意 Nix 软件包启动该虚拟机。软件包是可 URL 寻址的，访问 https://trynix.dev/?pkg=python3%403.6.2 并点击“Load”就能得到一个运行 2017 年 Python 3.6.2 的交互式 shell；他还发布了 trynix-preview —— 一个会在 Pull Request 下评论启动链接的 GitHub Action。 它把长达 13 年的软件包历史中的任意时间点变成无需安装、无需服务器的交互式环境，可能改变开发者评审 Pull Request 和检视旧软件的方式。这也说明基于 WebAssembly 的整机模拟正从演示走向实用的交付手段。 该虚拟机是在 WebAssembly 之上模拟出的 x86_64 机器而非原生硬件，因此启动和 I/O 性能取决于模拟开销，以及把相应的 Nix 闭包下载进浏览器虚拟文件系统的速度。项目建立在 ktock 的 qemu-wasm 之上，而 trynix-preview 通过评论中的链接把这一能力延伸到 CI 场景。

rss · Simon Willison · 9月10日 23:44

**背景**: Nix 是 Eelco Dolstra 于 2003 年创建的一种纯函数式包管理器，它把每个软件包视为存放在密码学哈希路径下的不可变值，从而实现可复现构建，并允许同一软件的多个版本共存。可复现构建是指确保二进制文件能够由源代码和构建环境逐比特地重新生成，从而提供一条从源码到二进制的、可被独立验证的路径。qemu-wasm 则把通用机器模拟器 QEMU 编译成 WebAssembly，使完整的 Linux 系统可以在一个浏览器标签页中运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ktock/qemu-wasm">GitHub - ktock/ qemu - wasm : QEMU on browser · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nix_(package_manager)">Nix (package manager)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Reproducible_builds">Reproducible builds</a></li>

</ul>
</details>

**标签**: `#nix`, `#webassembly`, `#qemu`, `#reproducible-builds`, `#virtualization`

---

<a id="item-8"></a>
## [Forgejo 16.0.4 修复严重远程代码执行漏洞](https://codeberg.org/forgejo/forgejo/src/branch/forgejo/release-notes-published/16.0.4.md) ⭐️ 8.0/10

Forgejo 发布了 16.0.4 补丁版本，修复了一个严重的远程代码执行（RCE）安全漏洞，并敦促用户立即升级。相关发布说明已发布在 Codeberg 的 forgejo/release-notes-published 分支上。 自托管平台上的远程代码执行漏洞一旦被利用，攻击者便可在服务器上运行任意代码，可能泄露源代码、凭据、CI 密钥以及与之相连的内部系统。由于 Forgejo 被大量组织自行托管，同时也是 Codeberg 等公共实例的基础，未及时打补丁的管理员将持续面临高危风险。 目前公开内容仅将该漏洞归类为远程代码执行问题，并未披露受影响的组件或利用前提等技术细节。该修复以 16.0.x 系列中的小型补丁形式发布，因此升级属于改动量很小的直接替换式更新。

rss · Lobste.rs · 9月10日 17:40

**背景**: Forgejo 是一个跨平台、开源且轻量级的自托管软件开发平台（forge），使用 Git 进行源代码版本管理，并提供问题跟踪、代码审查、持续集成、看板与 Wiki 等功能。它是从 Gitea 分叉而来的社区驱动项目，使用 Go 语言编写，自 2024 年 8 月起采用 GPLv3 许可证，通常由组织自行部署，Codeberg 等公共实例也基于它运行。远程代码执行（RCE）是一类攻击方式，攻击者往往无需用户交互即可远程在目标系统上运行恶意代码，通常被视为最严重的漏洞类型之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Forgejo">Forgejo</a></li>
<li><a href="https://forgejo.org/">Forgejo – Beyond coding. We forge .</a></li>
<li><a href="https://www.crowdstrike.com/en-us/cybersecurity-101/cyberattacks/remote-code-execution/">What is Remote Code Execution (RCE)? | CrowdStrike</a></li>

</ul>
</details>

**标签**: `#security`, `#forgejo`, `#git`, `#vulnerability`, `#self-hosted`

---

<a id="item-9"></a>
## [OpenJDK 提出 JEP 544：Java 代码提前编译](https://openjdk.org/jeps/544) ⭐️ 8.0/10

OpenJDK 发布的 JEP 544 提出为 Java 平台引入提前编译（AOT），目标是让经过优化的应用原生代码在 HotSpot JVM 启动时即可立即使用，从而改善启动时间和预热时间。其做法是在一次“训练运行”中把应用代码编译为原生代码，并把这些原生代码存入 AOT 缓存，供后续生产运行直接加载。 与 Go、Rust 或 GraalVM 原生镜像相比，JVM 的启动与预热延迟长期是 Java 的短板；OpenJDK 若提供官方的 AOT 路径，可能会显著改变无服务器函数、命令行工具、微服务以及短生命周期负载的部署选择。由于 JEP 是变更进入 Java 平台的正式渠道，该提案的推进意味着提前编译正被视为 JDK 的主流特性，而非实验性附加功能。 该设计基于“训练运行”：原生代码在一次剖析／优化的训练运行中生成，随后持久化进 AOT 缓存，因此性能表现取决于这次训练运行是否具有代表性。更早的草案（如 JEP draft 8313278）设想把 AOT 编译后的代码加载到匹配的 JVM 中，从而绕过解释器，并根据编译模式完全跳过 C1 或 C2 编译，这也意味着 JVM 与构建的兼容性约束，以及构建和部署流程上的改动。

rss · Lobste.rs · 9月10日 17:31

**背景**: JEP（JDK Enhancement Proposal，JDK 增强提案）是用于提出、跟踪和传达 Java 平台重大变更的正式文档；重大语言特性、JVM 改进和 API 新增通常都先以 JEP 形式出现，之后才可能成为 Java 规范请求（JSR）。传统上，HotSpot 先由解释器执行 Java 字节码，并使用即时编译（JIT）编译器——C1 负责快速生成轻度优化的代码，C2 负责高度优化的代码——在运行时编译热点方法，这就是 Java 应用启动慢、预热后才快的原因。提前编译则是在程序执行之前（通常在构建期）把 Java 这类高层语言编译成更底层的原生代码，从而减少运行时的编译开销。JEP 544 与 OpenJDK 的 Project Leyden 方向一致，后者探索把工作从运行时前移到训练运行和构建期等更早阶段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openjdk.org/jeps/544">JEP 544: Ahead-of-Time Code Compilation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ahead-of-time_compilation">Ahead-of-time compilation - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/JDK_Enhancement_Proposal">JDK Enhancement Proposal - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Java`, `#JVM`, `#AOT compilation`, `#OpenJDK`, `#performance`

---

<a id="item-10"></a>
## [Raymond Chen 揭秘 Windows XP 如何为你的初始用户头像选图](https://devblogs.microsoft.com/oldnewthing/20260909-00/?p=112683) ⭐️ 7.0/10

在 2026 年 9 月发表于其博客 "The Old New Thing" 的文章中，Raymond Chen 解释了 Windows XP 如何从 "%ALLUSERSPROFILE%\Application Data\Microsoft\User Account Pictures\Default Pictures" 目录中的文件里随机挑选新账户的初始用户头像。该例程以 GetTickCount() 的当前值作为 RtlRandomEx 随机数发生器的种子，并采用一趟式随机选择算法来选定文件。 这篇文章是 Chen 记录早已被遗忘的 Windows 内部实现细节的典型案例，并在社区引发广泛共鸣：Hacker News 上的讨论帖获得了数百点赞同和大量评论。它的意义不在于带来实际改动，而在于提醒人们：在一个被海量部署的操作系统中，看似平凡的设计决策背后也可能隐藏着微妙的工程权衡，同时它还引出了关于人类与计算机如何理解随机性的更广泛讨论。 据文章所述，该选择过程使用以 GetTickCount() 作为种子的 RtlRandomEx，这意味着其结果是由一个计时输入决定的，而非来自密码学意义上的强熵源。评论者还在 GitHub 上贴出了该例程实际泄漏的 NT 源代码，表明该算法只是对目录列表进行一次简单的单向扫描，而不是统计意义上的均匀洗牌。

hackernews · Lobste.rs · 9月10日 09:04 · [社区讨论](https://news.ycombinator.com/item?id=49640646)

**背景**: Windows XP 引入了重新设计的欢迎屏幕和开始菜单，会在每个用户账户旁显示一张小头像。新账户会自动获得一组内置默认图片中的一张（例如足球、棋子或花朵），直到用户自行更换；这些图片存放在所有用户配置文件下的共享 Default Pictures 文件夹中。Raymond Chen 是微软资深工程师，他的博客 "The Old New Thing" 专门解释 Windows 为何会有某些行为，其文章经常深入挖掘这类冷门的历史实现细节。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://devblogs.microsoft.com/oldnewthing/20260909-00/?p=112683">What algorithm did Windows XP use to choose your initial user picture? - The Old New Thing</a></li>
<li><a href="https://devblogs.microsoft.com/oldnewthing/20040401-00/?p=39933">The martial arts logon picture - The Old New Thing</a></li>
<li><a href="https://windowswallpaper.miraheze.org/wiki/Windows_XP">Windows XP - Windows Wallpaper Wiki - Miraheze</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上很喜欢这篇文章：有人称 Raymond Chen 的每篇 Windows 内部机制文章都"像个小圣诞节"，还有人贴出了该例程实际泄漏的 NT 源代码。一个反复出现的主题是工程意识：一位开发者指出，这类边界情况通常会被日常工作量的噪声淹没；另一位则观察到，随机挑选一件事对人类来说轻而易举，但对计算机来说需要一套完全不同且并不直观的流程。也有人打趣说，Chen 发布这类内部知识前是否需要获得许可。

**标签**: `#Windows internals`, `#Raymond Chen`, `#algorithms`, `#retro computing`, `#software history`

---

<a id="item-11"></a>
## [微信悄然测试「小微 AI 社交」，迈出 Agent 间沟通第一步](http://www.geekpark.net/news/370155) ⭐️ 7.0/10

微信近期开始小范围测试一项名为「小微 AI 社交」的功能：用户只需把自己的诉求告诉自己的「小微」，小微便会找到对方的小微、说明沟通话题并向对方本人请求授权，获得同意后两个 Agent 先行交流，只有在需要用户作出选择或确认时才分别回来提醒各自的主人。据极客公园实测，两个小微之间的交流不会出现在双方原有的微信聊天框中，而是留在小微内部的独立空间里。 微信及 WeChat 合并月活跃账户数已达约 14.39 亿，加上积累十余年的真实熟人关系链，让它绕开了数字分身类产品最难解决的冷启动问题，因此成为测试「Agent 代理社交」最现实的平台。如果这一实验成立，社交平台连接的对象可能从「人和人」扩展为「人的代理与人的代理」，微信也有机会从超级 App 进一步变成 Agent 寻找联系人、协调条件并调用服务的运行环境。 这与「帮我给某某发一条微信」有本质区别：代发消息时说什么仍由用户决定，AI 只负责点击发送；而在 A2A 测试中，用户交给 AI 的是一个目的，如何发起询问、交换哪些信息、怎样归纳分歧，部分沟通过程已交给两个 AI 完成。该功能目前仍处于小范围灰度测试阶段，入口分散、能力表现并不稳定；微信方面也承认，AI 嵌入太浅难以形成独立价值，嵌入太深又可能打扰原有体验，例如在视频号看内容后搜索信息时，明确的搜索需求可能被导向「问 AI」。

rss · 极客公园 · 9月10日 13:36

**背景**: 「小微」是微信内置的 AI 助手，位于微信首页左上角，今年 6 月起扩大灰度测试，支持文字或语音交流，可以搜索资料、总结文件、处理图片、设置提醒，也能调起小程序完成点外卖、打车、订票等任务。所谓 A2A（Agent-to-Agent），指的是两个 AI 代理直接代表各自的主人进行沟通，此前已有类似探索，例如基于聊天应用运行的免费开源自主 Agent 项目 OpenClaw，以及 Elys、Second Me 等用用户经历、兴趣和表达习惯训练数字分身的社交产品。腾讯总裁刘炽平在今年 8 月的业绩电话会上曾提到，未来用户可以直接向微信中的 Agent 发送复杂指令，更长远看，每个用户、小程序和商家都可能拥有自己的 Agent，并通过相互通信完成任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenClaw">OpenClaw - Wikipedia</a></li>
<li><a href="https://baike.baidu.com/en/item/Elys/1451010">Elys（An AI-native application developed by Natural Selection.）_Baiduwiki</a></li>
<li><a href="https://home.second.me/">Second Me - My AI Identity</a></li>

</ul>
</details>

**标签**: `#WeChat`, `#AI Agents`, `#Social AI`, `#Agent-to-Agent`, `#Product Experiment`

---

<a id="item-12"></a>
## [Suno v6：首个与音乐产业合作打造的 AI 音乐模型](https://www.producthunt.com/products/suno) ⭐️ 7.0/10

Suno 发布了 v6，并将其描述为该公司首个与音乐产业合作打造的 AI 音乐模型。该消息以一条简短的产品发布信息出现在 Product Hunt 上，标语为“首个与音乐产业共同打造的 Suno 模型”。 如果 Suno 关于“与音乐产业合作”的说法成立，这意味着生成式音乐初创公司与版权方之间的关系正从对立转向授权与合作，可能为 AI 音乐工具获取训练数据和商业授权树立行业规范。对音乐人、唱片公司和平台而言，这可能意味着更清晰的权利归属，以及更合法的 AI 音乐发行路径。 该发布页面本身没有提供任何技术细节——没有音频质量、曲目长度、模型架构、训练数据、可用性或定价等信息，因此尚不清楚具体有哪些产业伙伴参与，以及合作涵盖哪些内容。Suno 的上一代模型 v5.5 曾以支持最长 8 分钟的歌曲、44.1kHz 音质、歌曲编辑器、音轨分离和音频上传等功能作为卖点。

rss · Product Hunt · 9月10日 05:13

**背景**: Suno 是一个生成式 AI 音乐平台，最初由位于马萨诸塞州剑桥市的 Suno 公司开发，可根据文本提示生成带有人声和器乐的音乐作品。在 v6 之前，其对外宣传的最先进模型是 v5.5，支持更长的曲目、更高保真的音频以及音轨分离等编辑工具。生成式音乐工具一直因训练中使用受版权保护的录音而受到唱片业的审视，因此一款明确宣称“与音乐产业共同打造”的模型格外引人关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Suno_(platform)">Suno (platform) - Wikipedia</a></li>
<li><a href="https://suno.com/">Suno | AI Music Generator</a></li>
<li><a href="https://melolab.ai/models/suno">Suno V5.5 AI Music Model by Suno | MeloLab</a></li>

</ul>
</details>

**标签**: `#AI music`, `#generative AI`, `#Suno`, `#music industry`, `#product launch`

---