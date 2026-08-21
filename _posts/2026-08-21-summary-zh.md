---
layout: default
title: "Horizon Summary: 2026-08-21 (ZH)"
date: 2026-08-21
lang: zh
---

> 从 67 条内容中筛选出 12 条重要资讯。

---

1. [恶意 Rust crate arrayref 在构建时执行恶意负载](#item-1) ⭐️ 9.0/10
2. [朱雀三号实现我国首次火箭陆地回收](#item-2) ⭐️ 9.0/10
3. [Bun 1.4 发布：JavaScript 运行时迎来重大更新](#item-3) ⭐️ 9.0/10
4. [AliExpress 静默 WebAudio 指纹采集破坏蓝牙多点连接](#item-4) ⭐️ 8.0/10
5. [一篇关于学校本可以让生物课变得精彩的随笔](#item-5) ⭐️ 8.0/10
6. [训练 125M 参数的 Transformer 在 iPhone 上自动续写钢琴曲](#item-6) ⭐️ 8.0/10
7. [用 Bun 1.4 的 Bun.WebView 构建类似 shot-scraper 的 JSON API](#item-7) ⭐️ 8.0/10
8. [Stripe 以 80 亿美元收购 AI 路由平台 OpenRouter](#item-8) ⭐️ 8.0/10
9. [Odin 内联汇编挑战汇编无类型的传统观点](#item-9) ⭐️ 8.0/10
10. [开源 OPKSSH：将单点登录引入 SSH 认证](#item-10) ⭐️ 8.0/10
11. [支付宝押注智能体商业：广告位时代落幕，改收中介费](#item-11) ⭐️ 7.0/10
12. [为什么将 Rust 编译为 WebAssembly 会很慢：技术深度剖析](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [恶意 Rust crate arrayref 在构建时执行恶意负载](https://safedep.io/arrayref-proc-macro1-rust-build-time-malware/) ⭐️ 9.0/10

一个被入侵的维护者账户向 crates.io 发布了 Rust crate arrayref（0.3.10）、internment（0.8.7）和 append-only-vec（0.1.9）的恶意版本。这些版本都添加了一个拼写相似的依赖项，其构建脚本会在 cargo build 期间下载并执行远程负载；受影响的版本已被删除。 这一事件凸显了 Rust 生态系统中供应链攻击的风险：构建脚本以开发者权限运行，可能窃取凭据、源代码和签名密钥。它影响到依赖这些流行 crate 的无数下游项目，并引发了对 crates.io 事件响应以及 Cargo 缺乏沙箱隔离的紧迫质疑。 恶意负载是通过一个拼写相似的构建时依赖（proc-macro1，也出现为 proc-macro-en）引入的，而不是直接放在 crate 源码中。Rust 安全响应团队表示原作者可能并非恶意行为者；他们的电脑或凭据很可能被入侵，作为预防措施该账户已被锁定。

hackernews · abhisek · 8月20日 13:23 · [社区讨论](https://news.ycombinator.com/item?id=49374269)

**背景**: Rust crate 可以包含一个构建脚本（build.rs），Cargo 会在构建该 crate 之前编译并运行它，并以运行 cargo build 的开发者的权限执行。这使得构建脚本成为供应链恶意软件的有力载体，因为恶意依赖项可以从开发者机器上窃取机密。RustSec 咨询数据库是社区跟踪此类漏洞的仓库，但社区评论者指出，在这条新闻发布之前，arrayref 没有提交任何安全公告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.rust-lang.org/2026/08/20/supply-chain-attack-on-arrayref/">Supply chain attack on arrayref | Rust Blog</a></li>
<li><a href="https://www.stepsecurity.io/blog/arrayref-rust-crate-supply-chain-attack">Rust Supply-Chain Attack: arrayref, internment, and append-only-vec Poisoned by the proc-macro1 Build-Time Dropper - StepSecurity</a></li>
<li><a href="https://thehackernews.com/2026/08/rust-supply-chain-attack-puts-build.html">Rust Supply Chain Attack Puts Build -Time Malware in Crates with 245...</a></li>

</ul>
</details>

**社区讨论**: 评论者批评 GitHub 和 crates.io 的事件响应不力，指出恶意版本消失后没有下架（yank）标记，也没有安全公告。一些人呼吁 Cargo 对 build.rs 脚本进行沙箱隔离，并引用了之前的尝试；另一些人则认为标准库应更“内置电池”，以减少依赖链；还有人质疑在包管理器允许此类攻击的情况下，Rust 的安全性还剩下多少。

**标签**: `#rust`, `#security`, `#supply-chain`, `#malware`, `#crates.io`

---

<a id="item-2"></a>
## [朱雀三号实现我国首次火箭陆地回收](http://www.geekpark.net/news/369056) ⭐️ 9.0/10

2026 年 8 月 19 日，朱雀三号遥二运载火箭在东风商业航天创新试验区发射升空，一子级在甘肃民勤县朱雀三号着陆场成功着陆。这是继 7 月长征十号乙海上网系回收之后，我国首次成功实现入轨火箭一子级陆地可控回收。 这一成功是我国重复使用火箭技术的重大里程碑，表明国内运载火箭已具备类似 SpaceX Falcon 9 的垂直回收能力。它有望大幅降低发射成本，加快卫星互联网星座的组网进程。 朱雀三号是蓝箭航天研制的两级不锈钢液氧甲烷运载火箭，箭体直径 4.5 米，整流罩直径 5.2 米。一子级配备九台天鹊-12A 发动机，推力可在 40%至 110%之间调节，并通过栅格舵和着陆腿实现垂直回收。

rss · 极客公园 · 8月20日 00:39

**背景**: 可重复使用火箭通过回收、翻新并再次使用一子级，大幅降低单次发射成本。在此之前，我国已于 7 月用长征十号乙演示了海上网系回收，而朱雀三号采用的是类似 SpaceX 的着陆腿陆地垂直回收方式。该火箭使用液氧甲烷推进剂和不锈钢箭体，兼具低成本、耐高温和便于工业化制造等优势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/朱雀三号运载火箭">朱雀三号运载火箭 - 维基百科，自由的百科全书</a></li>
<li><a href="https://baike.baidu.com/item/朱雀三号/63824007">朱雀三号_百度百科 朱雀三号运载火箭 - 维基百科，自由的百科全书 朱雀三号遥二运载火箭 - 百度百科 中国首型民营重复使用运载火箭诞生！朱雀三号运载火箭成功回收 朱雀三号 - 卫星百科，很认真的中文航天百科 - 灰机wiki - 北京嘉闻杰... 朱雀三号遥二运载火箭发射成功_腾讯新闻</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2057587900053709143">四种火箭回收方式全面解析 - 知乎</a></li>

</ul>
</details>

**标签**: `#aerospace`, `#rocket recovery`, `#reusable rockets`, `#China space`, `#technology breakthrough`

---

<a id="item-3"></a>
## [Bun 1.4 发布：JavaScript 运行时迎来重大更新](https://bun.com/blog/bun-v1.4) ⭐️ 9.0/10

Bun 1.4 已发布，官方称这是广受欢迎的 JavaScript 运行时的一个重要新版本。该版本在 Bun 官方博客上被重点介绍，并在 Lobsters 上引发了社区讨论。 作为广泛使用的 JavaScript 运行时，Bun 的新版本会影响许多开发者的工作流程以及更广泛的 Web 开发生态。社区的高度关注表明，Bun 1.4 可能会带来值得关注的改进或变化。 此次公告可在 Bun 官方博客上查看，新闻还附带了 Lobsters 上的评论讨论链接。现有内容中并未提供具体的功能、更新日志条目或破坏性变更细节。

rss · Lobste.rs · 8月20日 14:37

**背景**: Bun 是一种现代 JavaScript 运行时，能够在浏览器之外运行 JavaScript，与 Node.js 类似，同时它还内置了打包器、测试运行器和包管理器等工具。像 1.4 这样的新版本通常意味着 Bun 为在其项目中依赖它的开发者带来了改进或修复。

**标签**: `#bun`, `#javascript`, `#runtime`, `#release`, `#web-development`

---

<a id="item-4"></a>
## [AliExpress 静默 WebAudio 指纹采集破坏蓝牙多点连接](https://blog.laserphile.com/2026/08/aliexpress-webpage-keeping-multipoint.html) ⭐️ 8.0/10

根据最新调查，AliExpress 网站会运行基于 WebAudio 的静默指纹采集脚本，在后台播放人耳听不到的声音。该行为会无意中破坏蓝牙多点连接（multipoint）功能，使已连接的耳机或助听器无法在设备间切换音频，还可能导致异常耗电。 这件事的意义在于，它揭示了一种既侵犯隐私、又会实际影响硬件行为的全新追踪技术，而不仅仅是浏览器隐私问题。数百万用户可能因此遇到蓝牙设备异常或续航下降，同时也反映出网站滥用音频 API 进行追踪的趋势日益严重。 其原理是通过 WebAudio API 渲染一段音频信号，再测量硬件和驱动输出时的微小差异，从而生成独特的设备标识。由于这段音频是静音的，浏览器不会显示音量图标，用户毫不知情，而蓝牙音频流会持续占用 multipoint 连接。

hackernews · Lobste.rs · 8月20日 10:08 · [社区讨论](https://news.ycombinator.com/item?id=49372583)

**背景**: WebAudio 指纹是一种浏览器指纹技术，通过 Web Audio API 提取设备音频组件中的熵值来识别设备。蓝牙多点连接（multipoint）允许一副耳机或助听器同时保持与两台设备的连接，从而在通话和媒体播放之间切换。AliExpress 的脚本似乎会无限期保持一个音频会话，干扰 multipoint 的切换逻辑，也可能让移动浏览器在后台持续运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://web-tracking.allenchou.cc/docs/browser-fingerprinting/techniques/audio-fingerprinting/">WebAudio Fingerprinting | Web Tracking 筆記</a></li>
<li><a href="https://shokz.com/blogs/news/bluetooth-multipoint-vs-dual-audio">Bluetooth Multipoint vs Dual Audio: What's the Difference?</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了亲身经历：有人发现后台网站导致手机异常耗电，有人注意到多种网站会让助听器改变环境噪声放大程度，还有人将汽车音响乱报语音指令的问题追溯到后台运行的 AliExpress iOS 应用。另一些评论者从技术角度指出，Firefox 已部分缓解 WebAudio 指纹，并希望浏览器能在播放静音音频时显示可见的“扬声器”图标。

**标签**: `#privacy`, `#fingerprinting`, `#webaudio`, `#bluetooth`, `#security`

---

<a id="item-5"></a>
## [一篇关于学校本可以让生物课变得精彩的随笔](https://jsomers.net/i-should-have-loved-biology/) ⭐️ 8.0/10

2020 年由 jsomers 发表的随笔《我本应爱上生物》指出，生物学通常以死记硬背的方式教授，从而扼杀了让这门学科真正迷人的惊奇感和探索感。这篇文章在 Hacker News 上获得高分，引发了关于教学法和求知欲的深入讨论。 这篇文章之所以引人共鸣，是因为它批判了一种普遍存在的教育失败——把天生美丽的学科变成死记硬背的练习。它对教育者、学生以及任何关心如何培养真正求知欲而非顺从的人都具有重要意义。 据称，这篇文章用生动的生物过程实例来展示该领域在概念层面上的魅力所在。评论者将文章论点与 Seymour Papert 和 Jean Piaget 的教育思想联系起来，指出知识通过与环境的互动而增长，而传统学校教育往往压制这种互动。

hackernews · tyre · 8月20日 17:50 · [社区讨论](https://news.ycombinator.com/item?id=49377853)

**背景**: 在传统的生物课上，学生常常记忆术语、路径和分类，却没有领会生命系统背后的美感。这篇随笔的核心论点是，如果以好奇心和惊奇感去接触生物学，它可以像任何其他学科一样令人着迷。它触及了一个长期争论：教育应该优先灌输事实，还是培养探索精神，以及为什么许多人因为学科的教学方式而远离科学。

**社区讨论**: 评论者提出了各种观点：一位数据科学家警告说，在研究中，'诱人'的任务往往会沦为机械的螺丝钉般的工作；而另一位生物学家则表示，即使教学不好，他自己的好奇心依然保持。还有人指出，同样的问题也存在于物理学和化学的教学中，并且这篇随笔是 Hacker News 上常被重新挖掘的经典。

**标签**: `#biology`, `#education`, `#pedagogy`, `#intellectual-curiosity`, `#essay`

---

<a id="item-6"></a>
## [训练 125M 参数的 Transformer 在 iPhone 上自动续写钢琴曲](https://simedw.com/2026/08/20/midi-autocomplete/) ⭐️ 8.0/10

一个 125M 参数的 Transformer 模型被训练用于实时自动续写 MIDI 钢琴演奏，在 iPhone 15 上达到每秒约 108 个音符的速度。该应用免费试用，并且完全在设备端运行。 这是基于 Transformer 的序列预测在音乐领域的新颖应用，类似于 GitHub Copilot 等代码自动补全工具。它表明生成式 AI 模型可以在消费级移动硬件上高效运行，为尊重隐私的创意工具开辟了新的可能性。 该模型基于 Transformer 架构，使用 MIDI 数据进行训练，并通过 Apple 的 Core ML 框架集成到 iOS 应用中。作者指出，很多方法没有成功，并且该模型进行的是音符级预测，而非词元级语言建模。

hackernews · simedw · 8月20日 12:04 · [社区讨论](https://news.ycombinator.com/item?id=49373456)

**背景**: Transformer 是一类基于自注意力机制的神经网络架构，于 2017 年提出，是 GPT 等大型语言模型的基础。MIDI 是一种标准协议，以音符开、音符关、力度等事件数据来表示音乐演奏，因此非常适合序列建模。Core ML 是 Apple 用于在设备端运行机器学习模型的框架，利用 CPU、GPU 和神经引擎；设备端推理可降低延迟并提升隐私性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Core_ML">Core ML</a></li>
<li><a href="https://en.wikipedia.org/wiki/Transformer_(neural_network)">Transformer (neural network)</a></li>
<li><a href="https://medium.com/@damjanprvulovic/midi-musical-instrument-digital-interface-a-technical-overview-1b718e9d5f61">MIDI ( Musical Instrument Digital Interface ): A Technical... | Medium</a></li>

</ul>
</details>

**社区讨论**: 评论区整体非常积极，有人建议将项目做成 VST 或 Max for Live 插件。有人指出了该项目与古典作曲训练方法之间的历史相似之处，还有人将其类比为基于 AI 的 UX 设计工具，认为品味和探索仍然至关重要。另有一位评论者询问预训练和后续训练所用数据集的大小，而作者在帖子中没有提及这一点。

**标签**: `#machine-learning`, `#music-generation`, `#transformer`, `#on-device-AI`, `#MIDI`

---

<a id="item-7"></a>
## [用 Bun 1.4 的 Bun.WebView 构建类似 shot-scraper 的 JSON API](https://simonwillison.net/2026/Aug/20/bun-webview-json-api/) ⭐️ 8.0/10

Simon Willison 构建了一个 TypeScript 服务端原型，演示了 Bun 1.4 新增的 Bun.WebView API——可以通过 JSON API 加载网页并在其中执行 JavaScript。这个服务端受其 shot-scraper javascript 命令行工具启发，实测在 cgroup 限制的容器中运行完整 Chrome 大约需要 192MB-256MB 内存。 Bun.WebView 将浏览器自动化能力内置到 Bun 核心，许多场景下不再需要 Puppeteer、Playwright 或单独下载浏览器。该实验的重要意义在于量化了基于 JSON 的无头浏览器服务的内存占用，为在受限环境中部署此类端点的开发者提供了参考。 Bun.WebView 支持通过 macOS WebKit 或基于 Chrome DevTools Protocol (CDP) 的本地 Chromium 进程工作；每个进程只会启动一个 Chrome 实例，后续 WebView 会复用该实例。Simon 的服务端实现已发布在 GitHub 上，并利用 cgroups 测试了容器内存占用。

rss · Simon Willison · 8月20日 15:37

**背景**: Bun 是一个快速的 JavaScript 运行时和工具集；1.4 版本是项目从 Zig 重写为 Rust 后第一个稳定版本，新增了 Bun.Image、Bun.markdown、Bun.cron()、Bun.Terminal 以及并行 run/test 命令等功能。shot-scraper 是 Simon Willison 开发的命令行工具，用于自动截图和在网页中执行 JavaScript。传统上这类自动化需要 Puppeteer 等独立的浏览器自动化库，而 Bun.WebView 的目标是将其变成运行时内置能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bun.com/docs/runtime/webview">WebView | Bun Docs</a></li>
<li><a href="https://bun.com/reference/bun/WebView">Bun.WebView object | API Reference | Bun</a></li>
<li><a href="https://shot-scraper.datasette.io/">shot - scraper</a></li>

</ul>
</details>

**标签**: `#Bun`, `#JavaScript`, `#WebView`, `#JSON API`, `#Rust rewrite`

---

<a id="item-8"></a>
## [Stripe 以 80 亿美元收购 AI 路由平台 OpenRouter](https://www.ifanr.com/1675718?utm_source=rss&utm_medium=rss&utm_campaign=) ⭐️ 8.0/10

Stripe 已完成对 AI 模型路由平台 OpenRouter 的收购，交易金额超过 80 亿美元。该收购消息最初由彭博社和《华尔街日报》在 2026 年 8 月报道。 这笔交易标志着 AI 基础设施领域的一次重大整合，将 OpenRouter 对数百个 AI 模型的统一访问与 Stripe 的支付生态系统相结合。它使 Stripe 成为 AI API 分发和变现的关键中间方，影响到依赖 AI 服务的开发者和企业。 OpenRouter 提供单一 API 网关，可访问来自 Google、OpenAI、xAI、Mistral 和 Anthropic 等提供商的 500 多个 AI 模型，并采用透明的按使用付费定价。Stripe 很可能将支付和计费功能整合到这个路由层，从而简化开发者为多家供应商的 AI 推理付款的流程。

rss · 爱范儿 · 8月20日 01:54

**背景**: OpenRouter 是一家美国 AI 公司，运营着一个将请求路由到大型语言模型和其他生成式 AI 模型的平台，为开发者提供统一的 API 和合并计费功能。Stripe 是一家主要的支付公司，为数百万企业处理在线交易；此次收购将其业务扩展到快速增长的 AI 基础设施领域，其中基于使用量的 AI 模型计费正成为一个重要市场。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenRouter">OpenRouter</a></li>
<li><a href="https://grokipedia.com/page/openrouter">OpenRouter</a></li>
<li><a href="https://openrouter.ai/pricing">Pricing | OpenRouter</a></li>

</ul>
</details>

**标签**: `#Stripe`, `#OpenRouter`, `#收购`, `#AI基础设施`, `#支付`

---

<a id="item-9"></a>
## [Odin 内联汇编挑战汇编无类型的传统观点](https://www.gingerbill.org/article/2026/08/20/designing-odins-inline-asm/) ⭐️ 8.0/10

本文介绍了 Odin 内联汇编的设计，它通过带类型注解的上下文无关语法，展示了汇编语言也可以有类型。这直接反驳了“汇编天生无类型”这一普遍看法。 通过挑战底层编程中的一个基本假设，这一设计可能影响未来编译器和系统语言处理安全性与验证的方式。它还将实用的内联汇编与学术上的类型化汇编语言（TAL）概念联系了起来。 Odin 的内联汇编采用上下文无关语法，但各指令集架构（ISA）之间并不共享助记符，仅语法本身是通用的。该设计为操作数添加了类型注解，与类型化汇编语言的研究方向相似。

rss · Lobste.rs · 8月20日 17:22

**背景**: 汇编语言是一种指令与机器码高度对应的低级语言，传统上被视为无类型。类型化汇编语言（TAL）通过为汇编添加数据类型注解，使类型检查器能够静态验证类型安全，从而无需虚拟机即可实现可信执行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gingerbill.org/article/2026/08/20/designing-odins-inline-asm/">Everyone Says Assembly Is Untyped—Everyone Is Wrong - gingerBill</a></li>
<li><a href="https://odin-lang.org/docs/inline-asm/">Inline asm Templates Overview | Odin Programming Language</a></li>
<li><a href="https://en.wikipedia.org/wiki/Typed_assembly_language">Typed assembly language - Wikipedia</a></li>

</ul>
</details>

**标签**: `#assembly`, `#type-systems`, `#odin`, `#language-design`, `#inline-asm`

---

<a id="item-10"></a>
## [开源 OPKSSH：将单点登录引入 SSH 认证](https://www.ethanheilman.com/x/33/index.html) ⭐️ 8.0/10

OpenPubkey 项目宣布开源 OPKSSH（OpenPubkey SSH），该工具将单点登录（SSO）与 SSH 认证集成。用户无需手动管理 SSH 密钥，即可使用现有的 OpenID Connect（OIDC）凭据登录 SSH 服务器。 此举解决了系统管理和云安全中的一个重大痛点：SSH 密钥管理的复杂性。通过支持基于 SSO 的 SSH，它有望简化访问控制，并提升组织和个人开发者的安全性。 OPKSSH 利用 OpenPubkey 协议，将用户或工作负载生成的公钥与 OIDC 身份绑定，且无需引入可信第三方。管理员可通过 JSON 策略文件定义哪些 OIDC 身份允许以哪些主体登录。

rss · Lobste.rs · 8月20日 15:24

**背景**: 传统的 SSH 认证依赖加密密钥对，而在大量服务器和用户之间管理这些密钥非常困难。OpenID Connect（OIDC）是一种广泛采用的身份认证标准，Google、GitHub 和 Microsoft 等身份提供商都使用该标准。OpenPubkey 是一个 Linux 基金会项目，最初由 Docker 和 BastionZero 宣布，它扩展了 OIDC，使得身份提供商的断言可用于其他协议的认证，例如 SSH。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/openpubkey/opkssh">GitHub - openpubkey/ opkssh : opkssh (OpenPubkey SSH ) · GitHub</a></li>
<li><a href="https://github.com/openpubkey/openpubkey">GitHub - openpubkey / openpubkey : Reference implementation of...</a></li>
<li><a href="https://www.docker.com/blog/how-to-use-openpubkey-to-solve-key-management-via-sso/">How to Use OpenPubkey to Solve Your Key Management... | Docker</a></li>

</ul>
</details>

**标签**: `#ssh`, `#sso`, `#security`, `#open-source`, `#authentication`

---

<a id="item-11"></a>
## [支付宝押注智能体商业：广告位时代落幕，改收中介费](http://www.geekpark.net/news/369078) ⭐️ 7.0/10

在支付宝 AI 生态合作伙伴大会上，支付宝展示了以智能体“阿宝”为核心的智能体商业愿景：通过意图理解直接完成点单、订机票、寄快递等服务。蚂蚁集团 CEO 韩歆毅预测，智能体商业将在未来 6 到 12 个月内爆发，平台收费模式正从广告位转向“中介费”。 这标志着数字商业分发方式的根本转变：商家不再靠购买流量和 SEO 排名取胜，而需要被 AI 意图理解体系选中。这可能会重塑整个行业的营销预算和平台商业模式，影响所有依赖广告发现机制的企业。 支付宝披露，“阿宝”上线两个月已完成万余项服务的 AI 化接入，覆盖出行、餐饮、文旅、政务等八大场景，麦当劳、瑞幸等品牌已陆续接入。推荐机制正从“拍卖逻辑”变为“委托逻辑”，排序依据从“谁出价高”变成“谁被理解得准”，有差异化的服务会被优先匹配。

rss · 极客公园 · 8月20日 03:26

**背景**: 支付宝近几个月一直在建设 AI 支付基础设施。2026 年 5 月，它推出了 Token Pay 和 AI 钱包，让用户可以为智能体消耗的 Token 付费，并宣称已完成 3 亿笔 AI 智能体支付。这次大会则是从支付通道进一步延伸到智能体的商业化模式，试图让智能体成为取代搜索和 App 时代流量逻辑的新分发层。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.zhihu.com/question/2042905314777724273">支付宝发布全球首个 Token Pay 服务和 AI 钱包产品，有哪些信息值得注意？ - 知乎</a></li>
<li><a href="https://m.mpaypass.com.cn/news/202605/26154457.html">支付宝推出Token支付综合解决方案Token Pay-移动支付网</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#Alipay`, `#intelligent commerce`, `#business models`, `#AI monetization`

---

<a id="item-12"></a>
## [为什么将 Rust 编译为 WebAssembly 会很慢：技术深度剖析](https://00f.net/2026/08/19/why-compiling-rust-to-webassembly-is-slow/) ⭐️ 7.0/10

一篇新的技术文章解释了为什么将 Rust 编译为 WebAssembly 会很慢，剖析了 LLVM WebAssembly 后端的作用以及 Cranelift 等替代代码生成器的潜力。文章探讨了根本原因并提出了可能的优化方向。 编译速度直接影响 Rust 和 WebAssembly 项目的开发者生产力，因此理解这些瓶颈可以推动工具链的改进。随着 WebAssembly 从浏览器扩展到边缘计算和服务器环境，更快的构建时间对整个生态系统都至关重要。 文章可能涉及 LLVM WebAssembly 后端（属于上游 LLVM 的一部分），并指出 Cranelift 可以充当 Rust 调试构建的代码生成后端。文中还可能提到 wasm-bindgen，它是工具链的一部分，用于促进 Wasm 模块与 JavaScript 之间的高级别交互。

rss · Lobste.rs · 8月20日 12:32

**背景**: Rust 主要通过 LLVM 编译为 WebAssembly，使用了一个已并入上游 LLVM 的 WebAssembly 专用后端。Cranelift 是另一种代码生成器，用于 Rust 的调试构建；它生成的代码比 V8 的 TurboFan 慢约 2%，但编译速度快得多，因此很适合开发工作流。wasm-bindgen 等工具负责处理 Rust 生成的 WebAssembly 与 JavaScript 之间的胶水层，这进一步增加了构建流程的复杂性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://v8.dev/blog/emscripten-llvm-wasm">Emscripten and the LLVM WebAssembly backend · V8</a></li>
<li><a href="https://github.com/bytecodealliance/wasmtime/blob/main/cranelift/README.md">wasmtime/ cranelift /README.md at main · bytecodealliance/wasmtime</a></li>
<li><a href="https://lwn.net/Articles/964735/">Cranelift code generation comes to Rust [LWN.net]</a></li>

</ul>
</details>

**标签**: `#rust`, `#webassembly`, `#compilation`, `#performance`, `#toolchain`

---