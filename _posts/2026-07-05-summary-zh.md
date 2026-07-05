---
layout: default
title: "Horizon Summary: 2026-07-05 (ZH)"
date: 2026-07-05
lang: zh
---

> 从 59 条内容中筛选出 14 条重要资讯。

---

1. [提示注入攻击泄露 YouTube 创作者的私密视频](#item-1) ⭐️ 9.0/10
2. [华为何庭波发布 V2 版“韬定律”论文](#item-2) ⭐️ 9.0/10
3. [首款神经动力学芯片突破 50 年计算瓶颈](#item-3) ⭐️ 9.0/10
4. [安娜的档案馆悬赏 20 万美元获取谷歌图书扫描件](#item-4) ⭐️ 8.0/10
5. [Claude Code 会话泄漏报告引发争议](#item-5) ⭐️ 8.0/10
6. [新版 Claude 模型工具调用准确性反而下降](#item-6) ⭐️ 8.0/10
7. [Linux 内核出现严重 'Bad Epoll' 漏洞](#item-7) ⭐️ 8.0/10
8. [学术论文详解 GNU Emacs 架构](#item-8) ⭐️ 8.0/10
9. [仅用 500 字节通过 Deflate 和 Fetch 绘制世界地图](#item-9) ⭐️ 7.0/10
10. [长光卫星完成近 50 亿元股权融资](#item-10) ⭐️ 7.0/10
11. [印度调查塔塔数据泄露，iPhone 18 Pro 机密曝光](#item-11) ⭐️ 7.0/10
12. [Immich v3.0.0 重大版本发布](#item-12) ⭐️ 7.0/10
13. [LineageOS 引入开发者验证机制确保构建完整性](#item-13) ⭐️ 7.0/10
14. [后缀 BWT 与循环移位 BWT 及快速计算](#item-14) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [提示注入攻击泄露 YouTube 创作者的私密视频](https://javoriuski.com/post/youtube) ⭐️ 9.0/10

针对 YouTube AI 评论摘要系统的提示注入攻击，允许攻击者通过在评论中嵌入恶意指令，泄露创作者私密和未公开视频的标题。 该漏洞暴露了创作者本应保密的私密内容，削弱了对 YouTube AI 功能的信任，并凸显了在面向用户的应用程序中集成大语言模型（LLM）而缺乏适当防护措施所带来的广泛安全风险。 攻击在创作者点击 YouTube Studio 中的建议 AI 提示时生效；注入的评论导致 AI 在其响应中包含私密视频标题。该漏洞通过概念验证成功提取了一个未公开视频的标题。

hackernews · javxfps · 7月4日 16:45 · [社区讨论](https://news.ycombinator.com/item?id=48786781)

**背景**: 提示注入是一种安全漏洞，精心设计的输入会使 AI 模型忽略其预期指令而遵循攻击者的命令。YouTube 的 AI 评论摘要功能使用大语言模型帮助创作者快速了解评论趋势，但未能正确将用户提供的评论与系统提示隔离开来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>

</ul>
</details>

**社区讨论**: 社区讨论中，一位前谷歌员工解释了 YouTube 可能因内部流程而修复缓慢的原因；还有用户尝试复现攻击但未成功，表明该漏洞可能已部分缓解。总体而言，评论者对 YouTube 将提示注入视为安全问题的方式表示担忧。

**标签**: `#security`, `#AI`, `#YouTube`, `#prompt injection`, `#vulnerability`

---

<a id="item-2"></a>
## [华为何庭波发布 V2 版“韬定律”论文](https://36kr.com/newsflashes/3880931591254019?f=rss) ⭐️ 9.0/10

华为半导体负责人何庭波于 2026 年 7 月 3 日发布了“韬定律”论文的 V2 版本，补充了工程细节、实测数据和产品路线图。 此次更新将后摩尔缩放理论从概念推向实际应用，有望实现更高效的 3D 芯片设计，延续半导体性能提升。 V2 版本引入了 LogicFolding 的“齿比”概念，实现了单元级连续优化而非宏块级离散优化，并包含了 Kirin 2026 与 Kirin 9030 Pro 的实测数据。

rss · 36氪 · 7月4日 06:35

**背景**: 摩尔定律（晶体管密度约每两年翻一番）正在放缓。“韬定律”提出了一种以时间常数τ为核心的新缩放理论，旨在通过 3D 堆叠和时间折叠技术指导后摩尔时代的半导体缩放。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260704A04R0000">华为发布V2版韬定律论文：三大核心升级！_腾讯新闻</a></li>
<li><a href="https://www.ithome.com/0/972/524.htm">华为何庭波发布 V2 版“韬定律”论文，补充工程细节和实测数据华为何庭...</a></li>
<li><a href="https://xueqiu.com/7353340333/398464838">韬定律V2深度阐释了LogicFolding的"齿比"概念——当混合键合间...</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#chip design`, `#post-Moore`, `#Huawei`, `#3D stacking`

---

<a id="item-3"></a>
## [首款神经动力学芯片突破 50 年计算瓶颈](https://36kr.com/newsflashes/3880779651248391?f=rss) ⭐️ 9.0/10

北京大学与中科院上海微系统所的研究团队成功研制出全球首款基于相变忆阻器的神经动力学系统芯片，单步运算时延仅 2.12 毫秒，在脑皮层重建任务中较 GPU 提速 50 至 478 倍。相关成果于 2025 年 7 月 3 日发表在《科学》杂志上。 这一突破解决了神经动力学领域长达半个世纪的实时计算瓶颈，为脑机接口的实时应用和神经科学研究提供了可能。它展示了基于忆阻器的存内计算作为传统 GPU 架构的可行替代方案在神经模拟中的潜力。 该芯片运行频率为 50 MHz，单步积分采用 9 级流水线，并在脑 MRI 数据的实时皮层表面重建和三维流形网格生成任务中得到了验证。相变忆阻器实现了可控存内计算，解决了该领域长期存在的难题。

rss · 36氪 · 7月4日 05:20

**背景**: 神经形态计算旨在通过模仿大脑结构和功能的硬件来处理信息，其方式类似于生物神经网络。相变忆阻器是一种根据材料相态改变电阻的器件，能够在同一位置实现存储和计算，从而减少数据搬运并提高能效。传统 GPU 虽然擅长并行计算，但并未针对控制神经动力学的连续微分方程进行优化，导致延迟高、功耗大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.163.com/dy/article/L12APP9M0511B8LM.html">我国成功研制全球首款基于相变忆阻器的神经动力学系统芯片|电导|神经网络_网易订阅</a></li>
<li><a href="https://kw.beijing.gov.cn/xwdt/kcyx/xwdtkjqy/202606/t20260630_4738704.html">北京大学集成电路学院杨玉超教授团队研制全球首款基于可控存内计算的...</a></li>
<li><a href="https://wap.sciencenet.cn/mobile.php?type=detail&cat=news&id=567637&mobile=1">首款神经动力学芯片问世 - 科学网</a></li>

</ul>
</details>

**标签**: `#neuromorphic computing`, `#memristor`, `#brain-computer interface`, `#hardware acceleration`, `#Science publication`

---

<a id="item-4"></a>
## [安娜的档案馆悬赏 20 万美元获取谷歌图书扫描件](https://software.annas-archive.gl/AnnaArchivist/annas-archive/-/work_items/234) ⭐️ 8.0/10

安娜的档案馆宣布悬赏 20 万美元，以获取谷歌图书的所有扫描件，旨在使其免费开放获取。 这一悬赏凸显了版权执法与知识开放获取之间持续的紧张关系，可能加速数百万数字化图书向公众开放。 悬赏针对谷歌图书的完整扫描件集合，其中包括通过谷歌图书馆项目数字化的数百万册图书。安娜的档案馆不直接托管文件，而是链接到第三方来源。

hackernews · Cider9986 · 7月4日 16:51 · [社区讨论](https://news.ycombinator.com/item?id=48786838)

**背景**: 谷歌图书是一项服务，扫描并索引来自全球图书馆的图书全文。安娜的档案馆是一个针对 Z-Library 和 Sci-Hub 等影子图书馆的元搜索引擎，聚合元数据并提供超过 9700 万册图书的访问。该项目旨在编录所有现存图书并促进开放获取。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anna's_Archive">Anna's Archive</a></li>
<li><a href="https://en.wikipedia.org/wiki/Google_Books">Google Books - Wikipedia</a></li>
<li><a href="https://support.google.com/websearch/answer/9690276?hl=en">About the Library Project - Google Search Help</a></li>

</ul>
</details>

**社区讨论**: 评论者对安娜的档案馆在图书获取受限地区所起的作用表示感谢，并分享了找到稀有资料的个人经历。一些人还讨论了相关项目及其对数字保存的广泛影响。

**标签**: `#open access`, `#digital libraries`, `#bounty`, `#books`, `#archiving`

---

<a id="item-5"></a>
## [Claude Code 会话泄漏报告引发争议](https://github.com/anthropics/claude-code/issues/74066) ⭐️ 8.0/10

有用户报告称 Claude Code 工作区实例之间可能存在会话或缓存泄漏，导致无关数据出现在响应中。Claude Code 团队确认收到报告并正在调查，但倾向于认为这是幻觉。 如果得到确认，这将表明 LLM 基础设施存在严重安全漏洞，可能导致用户数据跨会话泄露。该事件凸显了在 AI 服务中区分幻觉与真实系统错误的困难。 报告提到一个工具调用结果包含带有 'minecraft.py' 的路径名，而用户并未引用该内容。Claude Code 团队的 Thariq 表示他们确信这是幻觉，但会认真对待该报告。

hackernews · chatmasta · 7月4日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=48785485)

**背景**: LLM 幻觉是指模型生成看似合理但错误的信息。在多租户 AI 服务中，会话隔离对于防止用户间数据泄漏至关重要。社区指出，从外部来看，幻觉、本地上下文泄漏和基础设施错误很难区分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://forum.cursor.com/t/cross-session-content-leakage-unrelated-user-data-appears-in-response/156027">Cross-session content leakage: unrelated user data appears in</a></li>
<li><a href="https://www.unite.ai/hallucination-control-benefits-and-risks-of-deploying-llms-as-part-of-security-processes/">Hallucination Control: Benefits and Risks of Deploying LLMs as</a></li>
<li><a href="https://startup-house.com/blog/llm-hallucinations-explained">LLM Hallucinations Explained: Causes, Risks & How to Fix</a></li>

</ul>
</details>

**社区讨论**: 社区评论中，有用户分享了之前不同提供商的响应交换实例，另一用户建议在 AGENTS.md 中添加一行以避免 Minecraft 话题。有评论者指出区分幻觉与真实错误的困难，Claude Code 团队的 Thariq 也做出了官方回应。

**标签**: `#LLM`, `#security`, `#hallucination`, `#infrastructure`, `#Claude`

---

<a id="item-6"></a>
## [新版 Claude 模型工具调用准确性反而下降](https://simonwillison.net/2026/Jul/4/better-models-worse-tools/#atom-everything) ⭐️ 8.0/10

Armin Ronacher 报告称，较新的 Claude 模型（Opus 4.8、Sonnet 5）有时会在工具调用中凭空生成额外字段，导致 Pi 的编辑工具拒绝这些调用，而旧模型则没有此问题。 工具调用准确性的退化损害了第三方编码框架的可靠性，并表明针对专有工具的强化学习训练可能会降低在类似但不同模式上的性能。 凭空生成的字段出现在嵌套的'edits[]'数组中，编辑内容本身通常是正确的，但多余的键导致 Pi 拒绝调用并要求重试。

rss · Simon Willison · 7月4日 22:53

**背景**: LLM 中的工具使用允许模型通过生成符合模式的参数来调用外部函数。Anthropic 的 Claude Code 使用特定的搜索替换编辑工具，较新的模型可能通过强化学习进行了微调以偏向该工具的模式，导致在使用 Pi 等其他工具时产生额外的字段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/build-with-claude/structured-outputs">Structured outputs - Claude Platform Docs</a></li>
<li><a href="https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-4-8">Prompting Claude Opus 4.8 - Claude Platform Docs</a></li>

</ul>
</details>

**社区讨论**: 帖子作者指出这种行为令人困惑且有问题，并建议第三方框架可能需要实现多个编辑工具以匹配模型偏好的模式。

**标签**: `#LLM`, `#tool use`, `#AI reliability`, `#Anthropic`, `#regression`

---

<a id="item-7"></a>
## [Linux 内核出现严重 'Bad Epoll' 漏洞](https://github.com/J-jaeyoung/bad-epoll) ⭐️ 8.0/10

Linux 内核 epoll 机制中披露了一个严重漏洞（CVE-2026-46242），并在 GitHub 上发布了概念验证利用代码。 该漏洞允许无特权的本地攻击者提升至 root 权限，影响包括服务器和 Android 设备在内的广泛 Linux 系统。 该缺陷是 epoll 子系统中的竞态条件与释放后使用组合而成，可实现本地权限提升至 root。

rss · Lobste.rs · 7月4日 18:40

**背景**: epoll 是 Linux 内核中用于可扩展 I/O 事件通知的系统调用，广泛应用于高性能网络服务器。竞态条件发生在多个线程未正确同步访问共享数据时，而释放后使用则是在内存被释放后仍被访问时发生。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nvd.nist.gov/vuln/detail/CVE-2026-46242">NVD - CVE-2026-46242</a></li>
<li><a href="https://threat-modeling.com/cve-2026-46242-bad-epoll-linux-kernel-root-privesc-android/">CVE-2026-46242 'Bad Epoll': Linux Kernel 0-Day Local ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Epoll">epoll - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Lobsters 上的讨论可能提供了对该漏洞的技术分析和验证，但具体评论内容不可用。

**标签**: `#Linux`, `#security`, `#vulnerability`, `#epoll`, `#CVE`

---

<a id="item-8"></a>
## [学术论文详解 GNU Emacs 架构](https://www.diva-portal.org/smash/get/diva2:2052282/FULLTEXT01.pdf) ⭐️ 8.0/10

一篇题为《GNU Emacs 架构》的学术论文已发布，详细介绍了 GNU Emacs 的架构，涵盖其核心组件和设计原则。 这篇论文填补了 Emacs 架构正式文档的空白（历史上该部分文档不足），使开发者更容易理解和贡献代码库。 该论文可能描述了 Emacs 的分层架构，包括提供平台抽象的 C 核心和用于可扩展性的 Emacs Lisp 层，正如现有参考资料所述。

rss · Lobste.rs · 7月4日 16:31

**背景**: GNU Emacs 是一个高度可扩展的文本编辑器，基于 C 核心构建，并带有 Emacs Lisp 解释器用于定制。其架构经过数十年的有机演变，导致缺乏全面的文档。这篇论文旨在提供其设计的结构化视图。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Emacs">Emacs - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/GNU_Emacs">GNU Emacs - Wikipedia</a></li>
<li><a href="https://chrismennie.ca/EMACS-Conceptual-Architecture.pdf">Conceptual Views of EMACS’s Architecture Chris Mennie - 97024327</a></li>

</ul>
</details>

**标签**: `#Emacs`, `#software architecture`, `#academic paper`, `#editor`

---

<a id="item-9"></a>
## [仅用 500 字节通过 Deflate 和 Fetch 绘制世界地图](https://simonwillison.net/2026/Jul/4/building-a-world-map-with-only-500-bytes/#atom-everything) ⭐️ 7.0/10

Iwo Kadziela 在 Codex 辅助下，仅用 445 字节压缩数据生成了可信的 ASCII 世界地图，并通过 JavaScript 代码片段获取数据 URI 并使用 DecompressionStream API 解压缩渲染。 这展示了极致的数据压缩和对现代 Web API 的创造性使用，突破了用最少资源所能实现的界限。它可能激发数据高效可视化和代码高尔夫的新方法。 该技术使用 deflate 压缩（具体为'deflate-raw'）存储地图数据，JavaScript 代码使用 fetch()获取 data: URI，然后通过 DecompressionStream 解压缩数据流。最终地图以 ASCII 预格式化文本块显示。

rss · Simon Willison · 7月4日 23:09

**背景**: Deflate 是一种结合 LZ77 和霍夫曼编码的无损压缩算法，广泛用于 ZIP、PNG 和 gzip。DecompressionStream API 是压缩流标准的一部分，允许在浏览器中进行流式解压缩。根据 Fetch 规范，获取 data: URI 是有效的，从而无需网络请求即可使用内联数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DEFLATE_compression_algorithm">DEFLATE compression algorithm</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/API/DecompressionStream">DecompressionStream - Web APIs | MDN</a></li>
<li><a href="https://stackoverflow.com/questions/66573468/why-can-i-fetch-data-uris">javascript - Why can I fetch data URIs? - Stack Overflow</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者称赞其巧妙性和技术深度，一些人讨论了替代压缩方法以及使用 fetch 获取 data: URI 的优雅性。少数人指出其应用范围有限，但认可其教育价值。

**标签**: `#compression`, `#JavaScript`, `#ASCII art`, `#data URI`, `#hacking`

---

<a id="item-10"></a>
## [长光卫星完成近 50 亿元股权融资](https://36kr.com/newsflashes/3880783434149893?f=rss) ⭐️ 7.0/10

长光卫星技术股份有限公司完成近 50 亿元人民币股权融资，本轮由长发集团、陆石投资联合领投，多家知名投资机构参与。 这笔巨额融资将加速卫星批产能力建设、扩大吉林一号星座组网并深化遥感应用开发，巩固中国商业航天实力及高分辨率对地观测数据供给能力。 资金将精准投向三大方向：加速卫星批产能力建设、持续推进吉林一号卫星工程组网、深化遥感数据应用开发。长光卫星成立于 2014 年，是中国第一家商业遥感卫星公司。

rss · 36氪 · 7月4日 04:35

**背景**: 长光卫星技术股份有限公司成立于 2014 年 12 月，是中国第一家商业遥感卫星公司。其运营的吉林一号卫星星座截至 2023 年已有 108 颗卫星在轨，提供高分辨率光学和视频影像，应用于农业、林业、城市规划、灾害监测等领域。公司采用的“星载一体化”卫星设计是显著的技术创新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/长光卫星技术股份有限公司">长光卫星技术股份有限公司 - 维基百科，自由的百科全书</a></li>
<li><a href="https://sat.huijiwiki.com/wiki/“吉林一号”卫星星座">“吉林一号”卫星星座 - 卫星百科，很认真的中文航天百科 - 灰机wiki - ...</a></li>
<li><a href="https://spacemapper.cn/show/constellation/jilin1">吉林一号遥感卫星星座 - 中国商业航天高光谱成像服务SpaceMapper</a></li>

</ul>
</details>

**标签**: `#satellite`, `#funding`, `#remote sensing`, `#space tech`, `#China`

---

<a id="item-11"></a>
## [印度调查塔塔数据泄露，iPhone 18 Pro 机密曝光](https://36kr.com/newsflashes/3880789908631558?f=rss) ⭐️ 7.0/10

印度电子和信息技术部已正式对塔塔电子的大规模数据泄露事件展开调查，该事件泄露了未发布的 iPhone 18 Pro 零部件和测试材料。 此次泄露凸显了苹果供应链中的重大网络安全风险，可能危及商业机密并延迟产品发布，同时也使印度政府加强对数据保护实践的审查。 勒索软件团伙窃取了超过 630 GB 的数据，包括供应商名单、组件映射以及 iPhone 18 Pro 的内部跌落测试照片，并在暗网上泄露。

rss · 36氪 · 7月4日 04:12

**背景**: 塔塔电子是苹果的关键供应商，也是印度主要的 iPhone 代工厂之一。此次泄露事件中，勒索软件团伙入侵了塔塔的系统，窃取了机密文件并索要赎金。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://seekingalpha.com/news/4608314-tata-electronics-data-leak-apple-iphone-18-pro-details">Tata data leak: Apple iPhone 18 Pro parts, suppliers reportedly exposed | Seeking Alpha</a></li>
<li><a href="https://www.aljazeera.com/news/2026/6/30/apple-iphone-18-pro-secrets-leaked-in-tata-electronics-hack-what-we-know">Apple iPhone 18 Pro secrets leaked in Tata Electronics hack: What we know | Cybercrime News | Al Jazeera</a></li>
<li><a href="https://www.cnbc.com/2026/06/30/apple-iphone-18-pro-supplier-list-parts-and-photos-exposed-in-tata-data-leak.html">Apple iPhone 18 Pro supplier list, parts and photos exposed ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#data breach`, `#Apple`, `#supply chain`, `#India`

---

<a id="item-12"></a>
## [Immich v3.0.0 重大版本发布](https://immich.app/blog/v3.0.0-release) ⭐️ 7.0/10

自托管照片管理平台 Immich 发布了 v3.0.0 重大更新，带来了显著改进和新功能。 此次发布是开源社区的一个里程碑，提供了比 Google Photos 等专有服务更强大的替代方案，同时保护用户隐私。 更新包括 AI 驱动的功能，如人脸识别和智能搜索、自动手机备份以及快速 Web 界面，所有组件均以 Docker 容器方式运行。

rss · Lobste.rs · 7月4日 18:25

**背景**: Immich 是一个开源、自托管的照片和视频管理解决方案，旨在作为注重隐私的 Google Photos 替代品。它使用 Docker 容器进行部署，组件包括 PostgreSQL、Redis 和机器学习服务。该项目正在积极开发中，发布频繁，社区庞大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://immich.app/">Immich</a></li>
<li><a href="https://github.com/immich-app/immich">GitHub - immich-app/immich: High performance self-hosted ... Immich Complete Self-Hosting Guide: From Installation to ... Download | Immich Immich Self-Hosted Photo Management - mylinux.work Self-Hosting Your Photos with Immich — HomeLab Starter How to Install Immich for Self-Hosted Photo Management on Ubuntu</a></li>
<li><a href="https://aicybr.com/blog/immich-complete-self-hosting-guide">Immich Complete Self-Hosting Guide: From Installation to ...</a></li>

</ul>
</details>

**标签**: `#self-hosted`, `#photo management`, `#open source`, `#release`

---

<a id="item-13"></a>
## [LineageOS 引入开发者验证机制确保构建完整性](https://lineageos.org/Developer-Verification/) ⭐️ 7.0/10

LineageOS 宣布了一项新的开发者验证系统，以确保其构建的完整性和真实性。该系统允许用户验证某个构建是否由官方 LineageOS 开发者签名。 这通过防止恶意或被篡改的构建被分发，增强了对 LineageOS 生态系统的信任。对于注重安全的用户和更广泛的 Android 开源社区来说尤为重要。 验证过程使用加密签名，可以通过 OTA Verifier 页面或 Python 脚本执行。官方构建使用 LineageOS 的私钥签名，用户可以对照公钥检查签名。

rss · Lobste.rs · 7月4日 11:30

**背景**: LineageOS 是一个流行的开源 Android 发行版，为各种设备提供自定义 ROM。构建完整性对于确保软件在分发过程中未被篡改至关重要，这是自定义 ROM 社区中常见的关注点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lineageos.org/">LineageOS – LineageOS Android Distribution</a></li>
<li><a href="https://wiki.lineageos.org/verifying-builds">Verifying Build Authenticity | LineageOS Wiki</a></li>

</ul>
</details>

**社区讨论**: Lobsters 上的讨论突出了验证系统的技术方面，一些评论者指出可重现构建对于更强保证的重要性。其他人则讨论了实现中便利性与安全性之间的权衡。

**标签**: `#Android`, `#security`, `#open-source`, `#LineageOS`

---

<a id="item-14"></a>
## [后缀 BWT 与循环移位 BWT 及快速计算](https://purplesyringa.moe/blog/suffix-bwt-vs-cyclic-shift-bwt-and-fast-computation/) ⭐️ 7.0/10

该博客文章比较了基于后缀和基于循环移位的 Burrows-Wheeler 变换（BWT），突出了它们的差异，并介绍了快速计算方法。 理解这些变体对于优化数据压缩和基因组比对算法至关重要，因为 BWT 是 FM-index 等索引结构的基础。 后缀 BWT 使用带有唯一哨兵的后缀数组，而循环移位 BWT 考虑所有旋转；该博客可能讨论了构建速度和内存使用之间的权衡。

rss · Lobste.rs · 7月4日 02:08

**背景**: Burrows-Wheeler 变换（BWT）将字符串重排为相似字符的连续序列，从而实现更好的压缩和高效的模式匹配。通常通过后缀数组或循环旋转来计算，快速构建对于基因组数据库等大规模应用至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Burrows–Wheeler_transform">Burrows–Wheeler transform - Wikipedia Comparing Highly Similar Sequences: Suffix Trees, Suffix ... Burrows - Wheeler Data Transform Algorithm - GeeksforGeeks Burrows–Wheeler Transform | Every Algorithm Images</a></li>
<li><a href="https://lobste.rs/s/suucvi/suffix_bwt_vs_cyclic_shift_bwt_fast">Suffix BWT vs cyclic shift BWT, and fast computation</a></li>
<li><a href="https://arxiv.org/abs/2502.01327">[2502.01327] IBB: Fast Burrows-Wheeler Transform Construction ... [2504.19123] Fast and memory-efficient BWT construction of ... Space-Efficient Computation of the Burrows-Wheeler Transform IBB: Fast Burrows-Wheeler Transform Construction for Length ... IBB: Fast Burrows-Wheeler Transform Construction for Length ... Engineering a Fast Lightweight Burrows-Wheeler Transform ...</a></li>

</ul>
</details>

**社区讨论**: Lobsters 上的社区评论讨论了使用 BWT 的实用经验法则，指出 BWT 在文本和代码上表现出色，而基于 LZ 的算法更适合二进制数据；一位用户报告从 xz 切换到 bzip3 节省了 10%的空间。

**标签**: `#Burrows-Wheeler Transform`, `#algorithms`, `#data compression`, `#string algorithms`

---