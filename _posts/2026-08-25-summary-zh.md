---
layout: default
title: "Horizon Summary: 2026-08-25 (ZH)"
date: 2026-08-25
lang: zh
---

> 从 65 条内容中筛选出 13 条重要资讯。

---

1. [Mozilla 宣布在 Firefox 中支持 JPEG XL](#item-1) ⭐️ 9.0/10
2. [Emacs 31.1 发布：经典编辑器的重大更新](#item-2) ⭐️ 9.0/10
3. [微软画图和照片应用在 AI 编辑输出中嵌入隐形 GUID 水印](#item-3) ⭐️ 8.0/10
4. [整个旧金山市被重制为可玩的 3D 游戏](#item-4) ⭐️ 8.0/10
5. [seL4 在 AArch64 上的安全证明完成](#item-5) ⭐️ 8.0/10
6. [AI 依赖或致编程专业能力崩溃，引发争论](#item-6) ⭐️ 8.0/10
7. [开发者常用的 Hugging Face 或以 130 亿美元出售](#item-7) ⭐️ 8.0/10
8. [控制与复杂性：系统设计的核心张力](#item-8) ⭐️ 8.0/10
9. [让你的 SQLite 数据库变成可直接执行的 Linux 程序](#item-9) ⭐️ 7.0/10
10. [AstraTennis 时刻：人形机器人全球直播中打真实网球](#item-10) ⭐️ 7.0/10
11. [AI 音乐转向质量之争，音潮选了一条最难的路](#item-11) ⭐️ 7.0/10
12. [DeepSeek 上线多模态 V4-Flash-Vision-Exp，实测《牛来》小游戏](#item-12) ⭐️ 7.0/10
13. [Sloc Cloc and Code 4.0 新增热点分析，定位最需关注的代码文件](#item-13) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Mozilla 宣布在 Firefox 中支持 JPEG XL](https://hacks.mozilla.org/2026/08/intent-to-ship-jpeg-xl/) ⭐️ 9.0/10

Mozilla 宣布计划在 Firefox 浏览器中支持 JPEG XL。该公告于 2026 年 8 月通过 Mozilla Hacks 发布，将把下一代图像格式带入主流网络浏览器。 与 JPEG、PNG 和 WebP 等现有格式相比，JPEG XL 具有更优越的压缩效率和现代特性。在 Firefox 中支持它可能显著降低网页加载时间和带宽消耗，惠及网络上的用户和开发者。 JPEG XL 支持渐进式解码，只需加载 1%的数据即可显示图像。它还提供无损压缩和高动态范围支持，而这些特性在基于视频编解码器的格式中通常是不具备的。

rss · Lobste.rs · 8月24日 16:25

**背景**: JPEG XL 是一种免版税图像格式，旨在取代 JPEG、PNG 和 GIF 等旧格式。它由 JPEG 委员会开发，以更高的压缩比提供更高质量的图像，并支持广色域等现代成像需求。Mozilla 的发布意向表明 Firefox 可能会在实现后默认启用 JPEG XL，进一步推动该格式在网上的普及。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jpegxl.info/">JPEG XL : Superior Image Compression</a></li>
<li><a href="https://cloudinary.com/blog/how_jpeg_xl_compares_to_other_image_codecs">How JPEG XL Compares to Other Image Codecs</a></li>
<li><a href="https://www.loc.gov/preservation/digital/formats/fdd/fdd000536.shtml">JPEG XL Image Encoding</a></li>

</ul>
</details>

**标签**: `#JPEG XL`, `#web-standards`, `#browser`, `#image-format`, `#Mozilla`

---

<a id="item-2"></a>
## [Emacs 31.1 发布：经典编辑器的重大更新](https://lists.gnu.org/archive/html/info-gnu-emacs/2026-08/msg00004.html) ⭐️ 9.0/10

自由软件基金会在 info-gnu-emacs 邮件列表上宣布发布 Emacs 31.1，这是 GNU Emacs 文本编辑器的最新主要版本。该版本包含新功能、错误修复以及编辑器核心和软件包方面的改进。 新版 Emacs 重大发布意义重大，因为 Emacs 仍然是最具影响力和被广泛使用的开源编辑器之一，深深嵌入许多开发者的工作流中。此次更新将影响整个 Emacs 社区，包括第三方软件包的维护者和日常用户。 此次发布是通过 GNU 邮件列表档案发布的，Lobsters 上提供了社区讨论。作为标准的 GNU Emacs 版本，它提供了新功能和大量更改，但公告摘要中未包含具体细节。

rss · Lobste.rs · 8月24日 10:52

**背景**: Emacs 是文本编辑器家族，以其可扩展性著称，用户可以使用 Lisp 编程语言的方言定制编辑器的几乎每个方面。GNU Emacs 于 1985 年首次发布，是最流行的实现，至今仍由自由软件基金会积极开发。像 31.1 这样的主要版本号通常意味着相对于之前的 30.x 系列有重大的功能添加和改进。

**标签**: `#emacs`, `#release`, `#editor`, `#open-source`

---

<a id="item-3"></a>
## [微软画图和照片应用在 AI 编辑输出中嵌入隐形 GUID 水印](https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/) ⭐️ 8.0/10

一名安全研究人员对 Windows 11 的微软画图和照片应用进行了逆向工程，发现它们会悄悄向任何使用 AI 工具修改的图像中嵌入一个由服务器颁发的隐形 GUID 水印——即使 AI 模型完全在本地运行也是如此。该隐藏水印与可选的可见水印无关，并且用户无法禁用。 这一发现引发了严重的隐私与匿名性担忧，因为嵌入的 GUID 可以追溯到用户的微软账户，使原始创作者在法律请求下可以被识别。这也加剧了围绕隐形水印、内容出处和 AI 辅助创作工具中用户同意的持续争论。 在微软画图和照片应用中，当进行 AI 操作时都会应用这一隐形水印，它与 C2PA 内容凭据一起嵌入到图像像素中。目前尚不清楚诸如 AI 背景移除等操作是否也会触发该水印，但单独的可见水印设置并不能控制这个隐藏水印。

hackernews · ComputerGuru · 8月24日 15:28 · [社区讨论](https://news.ycombinator.com/item?id=49421158)

**背景**: C2PA（内容来源与真实性联盟）是一个行业标准，用于通过内容凭据追踪数字媒体的来源和编辑历史。隐形水印是一种将不可感知的数据直接嵌入图像像素的技术。微软的应用虽然可以在本地运行 AI 模型，但显然仍会联系服务器获取一个唯一的 GUID，并把它隐藏到输出图像中；这使微软（或拥有法律授权的其他方）能够将该图像关联到特定用户。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/">Microsoft Paint and Photos Embed Server-Issued GUIDs ... :: Xusheng Li</a></li>
<li><a href="https://byteiota.com/ms-paint-invisible-server-guid-watermark-ai-image/">MS Paint Embeds Invisible Server GUIDs in Every AI Image | byteiota</a></li>
<li><a href="https://en.wikipedia.org/wiki/Content_Authenticity_Initiative">Content Authenticity Initiative - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者既表达了担忧也表现出怀疑：一些人强调，与微软账户绑定的隐藏唯一标识符是对互联网匿名性的严重威胁，而另一些人则指出微软过去在水印实现上曾有过不严谨之处，并可能误触发水印。还有用户呼吁在微软澄清这一行为之前，避免使用画图或其他启用 LLM 的 Windows 应用。

**标签**: `#watermarking`, `#privacy`, `#microsoft`, `#image manipulation`, `#AI`

---

<a id="item-4"></a>
## [整个旧金山市被重制为可玩的 3D 游戏](https://sf.thijs.gg/) ⭐️ 8.0/10

一个新的网页项目将整个旧金山市渲染为可导航的 3D 环境，用户可以在其中驾驶和探索。该体验由开发者 cdngdev 在 Twitter 上发布，并引起了广泛关注。 该项目展示了现代 Web 技术如何处理城市规模的 3D 渲染，使沉浸式城市探索直接在浏览器中成为可能。它可能激发其他城市类似的数字孪生或游戏化复刻，也体现了地图数据与互动娱乐之间日益增长的交叉。 该体验在浏览器中运行，包含驾驶机制和可收集的金币，但尚无结构化的游戏循环。一些 Safari 用户报告页面会冻结浏览器，社区成员建议未来可添加街道名称、地标标签和基于地址的传送等功能。

hackernews · centrosphere · 8月24日 17:05 · [社区讨论](https://news.ycombinator.com/item?id=49422784)

**背景**: 这是一个基于浏览器的整座城市 3D 渲染，利用 Web 技术实现无需本地游戏引擎的交互式探索。该项目将地理数据转化为游戏化环境，是融合地图与实时图形的一种创意编码。虽然具体技术管线未被说明，但社区评论暗示它可能使用了建筑足迹、高程数据和街道级图像。

**社区讨论**: 评论者反应积极，一位前居民表示，这种复刻让他们在重游熟悉地点时感到激动。用户还建议增加街道名称、地址传送和 MMO 模式等增强功能，同时一些 Safari 用户报告页面会导致浏览器冻结。整体情绪热情，但也包含实用的可用性反馈。

**标签**: `#3D rendering`, `#city modeling`, `#interactive map`, `#creative coding`, `#web technology`

---

<a id="item-5"></a>
## [seL4 在 AArch64 上的安全证明完成](https://proofcraft.systems/news-2026/#2026-08-21) ⭐️ 8.0/10

seL4 微内核针对 AArch64（ARM 64 位）架构的正式安全证明已完成。这将其经过验证的机密性、完整性和可用性保证扩展到了一个主要的处理器架构。 这是高可信操作系统的重要里程碑，因为 AArch64 为绝大多数智能手机、平板电脑、服务器和嵌入式设备提供算力。它使经过形式化验证的安全内核在国防、汽车和关键基础设施中的 ARM 系统上成为现实选择。 该证明仅涵盖非 MCS（非混合关键性）配置，并且仅限于单核（unicore）运行。它也没有解决时序侧信道攻击，这仍然是一个活跃的研究领域。

hackernews · snvzz · 8月24日 11:32 · [社区讨论](https://news.ycombinator.com/item?id=49418255)

**背景**: seL4 是一个开源的、高可信的、基于能力（capability）的微内核，源自 L4 微内核家族，其安全属性经过了数学形式化验证。形式化验证使用数学证明来表明系统满足其规范，而不是仅仅依靠测试。AArch64（也称为 ARM64）是 ARM 架构家族的 64 位执行状态，广泛用于各种设备。完成 AArch64 证明需要在 ARM32 上最初 seL4 验证的基础上，付出多年的大量工程和研究努力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SeL4">SeL4</a></li>
<li><a href="https://en.wikipedia.org/wiki/AArch64">AArch64</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification</a></li>

</ul>
</details>

**社区讨论**: 评论者承认了这一里程碑，但指出了重要的注意事项：证明不包括 MCS 且仅限单核，时序侧信道攻击仍然是威胁。其他人讨论了 seL4 的实际用户，如 GenodeOS、LionsOS，以及一家将其用作虚拟机监控程序（hypervisor）的未具名中国汽车制造商。有评论者认为，安全社区需要原生 seL4/Linux 组合来真正改善系统安全，因为安全启动虚拟化平台如今已很常见。

**标签**: `#seL4`, `#formal verification`, `#microkernel`, `#AArch64`, `#security`

---

<a id="item-6"></a>
## [AI 依赖或致编程专业能力崩溃，引发争论](https://larsfaye.com/articles/ai-coding-will-prevent-expertise) ⭐️ 8.0/10

Lars Faye 的一篇文章指出，依赖 AI 编码工具会阻碍开发者形成深度专业能力，在 Hacker News 上引发激烈讨论，获得 426 分和 424 条评论。该文对当前将 AI 生成代码视为生产力提升的主流观点提出了质疑。 如果这一观点成立，软件行业可能会迎来一代无法调试、维护或深入理解代码的开发者，损害代码质量和长期可维护性。这场争论之所以重要，是因为企业界正在大规模强制使用 AI 编码工具，这堪称行业的关键转折点。 讨论中区分了“氛围编程”与“引导式编程”，后者将 LLM 融入常规编辑流程，消除繁琐环节同时保留人的理解。支持文章观点的人认为，深度专业能力需要阻力与刻意练习，而 AI 按需生成代码恰恰消除了这些要素。

hackernews · Lobste.rs · 8月24日 15:52 · [社区讨论](https://news.ycombinator.com/item?id=49421554)

**背景**: 大型语言模型（LLM）是在海量文本上训练的神经网络，能够理解并生成自然语言，是 ChatGPT、Claude、Gemini 等聊天机器人的核心技术。如今这些模型也驱动着编码助手，可以直接根据自然语言提示生成代码，从而降低了开发者记忆 API 或理解语言内部机制的必要性。这篇文章触及了一个日益受到关注的忧虑：这类工具虽然短期能提升生产力，却可能侵蚀构建可靠软件所需的专业能力。其核心论点是：专业能力不仅是知识，更是通过克服阻力和解决难题而形成的技能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/large-language-models">What are large language models (LLMs)? - IBM</a></li>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/large-language-model-llm/">Large Language Model (LLM) - GeeksforGeeks</a></li>

</ul>
</details>

**社区讨论**: 评论大多认同文章的担忧，一位企业开发者指出，领导层强制要求“如果你还在手写代码，那就是在做错事”，导致代码产出速度快到人类无法审查。也有人持不同意见，称赞“引导式编程”既高效又高质量，还有人认为真正的工程师会主动寻求挑战，LLM 只是把挑战转移到了另一个层面。少数评论警告称，“蛇吞自己尾巴”的局面不可持续——最终只剩下少数工程师在审查大量质量低劣的 AI 生成代码。

**标签**: `#AI coding`, `#software engineering`, `#expertise`, `#LLMs`, `#developer productivity`

---

<a id="item-7"></a>
## [开发者常用的 Hugging Face 或以 130 亿美元出售](https://www.ifanr.com/1676393?utm_source=rss&utm_medium=rss&utm_campaign=) ⭐️ 8.0/10

8 月 23 日，外媒报道称 Hugging Face 正在探索出售，估值可能达到 130 亿美元甚至更高，并已聘请投行试探潜在买家的兴趣。这几乎是 2023 年 D 轮融资时 45 亿美元估值的近三倍。 这笔潜在收购表明，在模型与用户之间的 AI “中间层”正成为大公司战略争夺的焦点，此前 Stripe 刚以超过 80 亿美元收购了 OpenRouter。Hugging Face 若被出售，可能重塑开源 AI 生态，并影响数百万依赖该平台的开发者。 Hugging Face 托管着超过 100 万个社区贡献的模型、数十万个数据集，月活访客约 1800 万，注册用户约 500 万，并有超过 2000 家企业付费使用其 Enterprise Hub。其年经常性收入估计在 4000 万到 7000 万美元之间，按报道的求购价计算，市销率超过 180 倍。

rss · 爱范儿 · 8月24日 03:35

**背景**: Hugging Face 是一家总部位于纽约的公司，常被称为“AI 界的 GitHub”，提供流行的 Transformers 库和 Model Hub，开发者可以在上面分享和下载预训练模型、数据集及 AI 演示应用。在当前 AI 生态中，“中间层”公司负责连接基础模型与真实应用，其价值主要来自生态位和开发者渠道。但与 GitHub 上的代码不同，Hugging Face 上托管的模型本质上是可下载的文件，迁移成本低，因此锁定效应较弱。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hugging_Face">Hugging Face - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.ibm.com/think/topics/hugging-face">What is Hugging Face? | IBM</a></li>
<li><a href="https://www.36kr.com/p/2302371149228807">大模型中间件-构建AI应用的必备软件 - 36氪</a></li>

</ul>
</details>

**标签**: `#AI`, `#Hugging Face`, `#acquisition`, `#developer tools`

---

<a id="item-8"></a>
## [控制与复杂性：系统设计的核心张力](https://ferd.ca/control-and-complexity-tension-in-systems-design.html) ⭐️ 8.0/10

在一篇新文章中，系统工程师 Fred Hebert 探讨了控制与复杂性之间的固有权衡，指出增强可控性的努力往往引入新的复杂性和脆弱性。 这篇文章重新审视了分布式系统中的调试与可运维性讨论，提醒人们过度设计控制机制反而会削弱可靠性。它可能会引起软件工程师和 SRE 的共鸣，尤其是那些应对级联故障和过度复杂编排的人。 这篇文章基于作者在分布式系统和 BEAM/Erlang 生态中的经验。它讨论了重试、超时和编排等机制如何在增加控制力的同时增加复杂性，并最终主张更青睐简单设计。

rss · Lobste.rs · 8月24日 11:58

**背景**: 在软件系统中，“控制”指的是通过监督树、熔断器和配置开关等机制来指导和规范系统行为的能力。复杂性则是系统内相互依赖和隐藏状态的程度，使系统难以推理。Fred Hebert 是知名的 Erlang/OTP 专家，长期撰写关于构建可靠、自愈系统的话题。这篇文章延续了系统社区中关于“正式控制机制何时弊大于利”的长期讨论。

**标签**: `#systems design`, `#complexity`, `#control`, `#distributed systems`, `#software engineering`

---

<a id="item-9"></a>
## [让你的 SQLite 数据库变成可直接执行的 Linux 程序](https://simonwillison.net/2026/Aug/24/your-executable-is-a-sqlite-database/) ⭐️ 7.0/10

Farid Zakaria 展示了一种 Linux 模式，可以让 SQLite 数据库文件直接作为二进制程序执行。该技巧将 ELF 组件嵌入 SQLite 表中，并通过内核的 binfmt_misc 机制由自定义解释器 self-exec 触发执行。 SQLite 文件头偏移 68 字节处的 4 字节 application ID 被设为“SELF”（Structured Executable & Linkable Format）。ELF 的各个组成部分按给定 schema 存放到 SQLite 表中，并通过类似 ':self:M:68:SELF::/usr/local/bin/self-exec:' 的 binfmt_misc 注册，让内核调用用 C 编写的解释器来执行这类文件。

rss · Simon Willison · 8月24日 11:38

**背景**: SQLite 的 application ID 是一个文件头字段，供把 SQLite 当作文件格式的应用程序使用，让 file 等工具能识别具体类型而不只是“SQLite 数据库”。ELF 是 Linux 可执行文件的标准二进制格式，通常包含机器码、头部和段。binfmt_misc 是 Linux 内核特性，可通过把魔法字节模式关联到解释器，让内核执行任意格式的文件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stackoverflow.com/questions/21929457/sqlite-how-to-use-pragma-application-id">SQLite: how to use PRAGMA application_id? - Stack Overflow</a></li>
<li><a href="https://en.wikipedia.org/wiki/Executable_and_Linkable_Format">Executable and Linkable Format - Wikipedia</a></li>
<li><a href="https://github.com/ibm-research/fusedos-linux/blob/master/Documentation/binfmt_misc.txt">fusedos- linux / binfmt _ misc .txt at master · ibm-research/fusedos- linux</a></li>

</ul>
</details>

**标签**: `#sqlite`, `#linux`, `#elf`, `#binfmt_misc`, `#executable`

---

<a id="item-10"></a>
## [AstraTennis 时刻：人形机器人全球直播中打真实网球](http://www.geekpark.net/news/369283) ⭐️ 7.0/10

8 月 22 日，在第二届世界人形机器人运动会上，银河通用的人形机器人在全球直播中与顶尖人类球员进行了一场完全自主的网球表演赛，这是全球首次大型人机体育赛事直播。该机器人完成了发球、正反手击球、摔倒后自主站起等动作，并在双打中与人类队友实时协作，由公司自研的具身智能大模型「银河星脑」和训练平台「银河星坊」驱动。 这标志着数字智能向物理智能的重要跨越，将人工智能的能力从 AlphaGo 在棋盘上的符号博弈拓展到真实世界的动态体育竞技。它证明具身智能能够应对高速、不可预测的物理交互，有望加速人形机器人在复杂任务中的商业化落地和现实部署。 据报道，「银河星脑」是全球首个将大脑、小脑与神经控制集于一模的模型，分别处理比赛理解、动作规划与身体执行。「银河星坊」平台将不完美的人类数据转化为高质量训练数据，并通过多智能体自我对弈生成千万次虚拟网球训练，相当于让机器人积累了数十年的练习时间。

rss · 极客公园 · 8月24日 07:25

**背景**: 具身智能指通过传感器和执行器与物理世界交互、具备感知、决策和行动能力的智能系统。传统机器人训练依赖遥操作数据，但在网球等高水平技能场景中难以获取，因此银河通用采用虚拟环境训练与仿真到真实的迁移。这场表演赛被比作 2016 年 AlphaGo 战胜李世石，但战场从棋盘转移到了物理世界。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/item/银河星脑/67439702">银河星脑 - 百度百科</a></li>
<li><a href="https://developer.cloud.tencent.com/article/2731003">银河通用亮相2026世界机器人大会 端到端具身大模型实现虚实训练闭环-...</a></li>
<li><a href="https://blog.csdn.net/cv_autobot/article/details/143879548">一文读懂基于大模型的具身智能技术-CSDN博客</a></li>

</ul>
</details>

**标签**: `#具身智能`, `#人形机器人`, `#人工智能`, `#机器人运动`

---

<a id="item-11"></a>
## [AI 音乐转向质量之争，音潮选了一条最难的路](http://www.geekpark.net/news/369273) ⭐️ 7.0/10

音潮于 8 月 14 日发布 V4.0，这是一次底层架构的全方位重构，聚焦指令理解、情绪落地和曲风细分；此前该团队已连续两年拿下 WAIC 官方主题曲。该公司从一开始就基于中文底座、使用壁仞国产 GPU 训练模型，刻意避开 Suno、Udio 基于英语底座的技术路线。 这标志着 AI 音乐从'能不能生成'阶段转向'该怎么生成'阶段，作品的可感知质量与人类意义比单纯的产能更重要。在产能过剩导致大量 AI 歌曲被淹没的背景下，深度语言/文化本地化与可控性可能成为中国 AI 音乐公司出海竞争的关键优势。 文章引用 Deezer 数据：AI 歌曲每日涌入量已达 7.5 万首，占新增上传的 44%，但实际播放占比仅 1%–3%。TIDAL 已上线 AI 透明度标签，IFPI 则要求'人类实质性参与'才能进入官方榜单；音潮表示 V4.0 解锁了 10 语种全覆盖和纯音乐生成的全面开放。

rss · 极客公园 · 8月24日 07:17

**背景**: 2023–2024 年前后，Suno、Udio 等 AI 音乐工具兴起，用户只需输入文字提示即可生成完整歌曲，但这些工具大多建立在以英语为中心的模型之上。汉语是声调语言，与英语的重音节奏体系本质不同，因此在英语底座上修修补补生成的中文歌往往缺乏'味道'。与此同时，平台和版权方开始应对 AI 歌曲洪流：例如 TIDAL 规定，完全由 AI 生成的录音会带有'AI'标签，且不会进入编辑推荐；IFPI 则强调商业认可的作品需要'人类实质性参与'。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tidal.com/ai-policy">Tidal AI Policy | TIDAL</a></li>
<li><a href="https://support.tidal.com/hc/en-us/articles/48031883413521-AI-Policy">AI Policy – TIDAL Support</a></li>

</ul>
</details>

**标签**: `#AI音乐`, `#大模型`, `#产业分析`, `#内容创作`

---

<a id="item-12"></a>
## [DeepSeek 上线多模态 V4-Flash-Vision-Exp，实测《牛来》小游戏](http://www.geekpark.net/news/369278) ⭐️ 7.0/10

8 月 21 日，DeepSeek 正式发布其首个多模态模型 DeepSeek-V4-Flash-Vision-Exp，并已通过 API 平台开放调用，模型 ID 为 'deepseek-v4-flash-vision-exp'。该模型支持 base64 内联、外部 URL 和新上线的 Files API 三种图片传入方式。 此次发布填补了 DeepSeek 模型家族在多模态能力上的空白，此前开发者需要依赖第三方多模态模型。它每张图片仅消耗最多 384 个 token，不到 GPT 或 Claude 的一半，这可能会显著降低开发者构建多模态 Agent 工作流的成本。 名称中的 'Exp' 表明这是一个实验性版本；官方基准显示其纯文本能力与 V4-Flash 正式版持平，而在需要视觉理解的 Agent 基准上据称已接近 Opus-4.8。定价与 V4-Flash 文本价格一致，没有额外的视觉处理溢价，Files API 则免费供开发者上传图片并重复引用。

rss · 极客公园 · 8月24日 07:14

**背景**: DeepSeek 是一家以文本大语言模型而知名的中国 AI 公司。多模态 AI 整合了图像、文本和音频等多种数据类型，从而获得更全面的理解与生成能力。新模型采用了 DeepSeek 此前公布的「Thinking with Visual Primitives」框架，将视觉元素压缩为类似空间坐标的原语，而不是密集的图像分块，这解释了其极低的 token 消耗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-vision-exp">DeepSeek V 4 Flash Vision Exp - API Pricing & Providers | OpenRouter</a></li>
<li><a href="https://zenmux.ai/deepseek/deepseek-v4-flash-vision-exp">deepseek / deepseek - v 4 - flash - vision - exp - ZenMux</a></li>
<li><a href="https://apidog.com/blog/deepseek-v4-flash-vision-api/">How to Use the DeepSeek V 4 - Flash - Vision API (Image Input Guide)</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#multimodal`, `#AI API`, `#model release`

---

<a id="item-13"></a>
## [Sloc Cloc and Code 4.0 新增热点分析，定位最需关注的代码文件](https://boyter.org/posts/sloc-cloc-code-hotspots-finding-files-that-need-attention/) ⭐️ 7.0/10

Sloc Cloc and Code (scc) 4.0 已发布，新增了热点分析功能，帮助开发者找出代码库中最需要关注的文件。这一新功能标志着该工具已不只是一款简单的代码计数工具。 这一更新意义重大，因为它让 scc 转变为一种代码分析工具，可以指导维护和重构工作。采用指标驱动工作流的开发者将能更好地优先处理代码库中的热点文件。 scc 4.0 在此前功能的基础上进行了扩展，包括代码行数统计、复杂度计算和 COCOMO 估算。新增的热点分析功能旨在让开发者优先关注最需要处理的文件。

rss · Lobste.rs · 8月24日 23:04

**背景**: Sloc Cloc and Code (scc) 是一款用 Go 编写的高速、准确的源代码计数器，与 cloc、sloccount 和 tokei 类似。它可以统计多种编程语言的代码行、空行、注释行和物理行，并提供复杂度计算和 COCOMO 估算。该工具还支持 searchcode.com，并广泛应用于开源和开发工作流中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/boyter/scc">GitHub - boyter/scc: Sloc, Cloc and Code: scc is a very fast ...</a></li>
<li><a href="https://sourceforge.net/projects/sloc-cloc-and-code-scc.mirror/">Sloc Cloc and Code (scc) download | SourceForge.net Sloc Cloc and Code (scc) for Claude Code | mdskills.ai Sloc Cloc and Code (scc) - Browse /v3.5.0 at SourceForge.net scc (Sloc, Cloc, and Code) - research.tedneward.com Sloc Cloc and Code - ULOC Unique Lines of Code - Boyter</a></li>

</ul>
</details>

**标签**: `#code analysis`, `#developer tools`, `#metrics`, `#open source`, `#CLI`

---