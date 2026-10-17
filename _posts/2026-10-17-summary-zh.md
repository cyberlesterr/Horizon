---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 66 条内容中筛选出 7 条重要资讯。

---

1. [Claude 破解 NIST ECDSA 曲线种子来源：源自 lrand48 随机数生成器](#item-1) ⭐️ 9.0/10
2. [特斯拉发布搭载 SpaceX 火箭推进器、可悬浮飞行的新一代 Roadster](#item-2) ⭐️ 8.0/10
3. [PS5LM 让破解版 PS5 原生运行 llama.cpp 与 GGUF 模型](#item-3) ⭐️ 8.0/10
4. [研究人员利用存在 37 年的 OpenBSD 内核漏洞获取 root](#item-4) ⭐️ 8.0/10
5. [Linus Torvalds 为 AI 辅助的 Linux 内核贡献定下规则](#item-5) ⭐️ 8.0/10
6. [估值曾达 50 亿美元的 AI 独角兽 Character.AI 申请破产，2000 万美元向迪士尼出售 IP 许可](#item-6) ⭐️ 7.0/10
7. [豆包 SAEP 公示结束：155 款应用拒绝 AI 屏幕自动化](#item-7) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Claude 破解 NIST ECDSA 曲线种子来源：源自 lrand48 随机数生成器](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic 报告称，其 AI 模型 Claude 逆向破解了 NIST ECDSA 曲线（P-192、P-224、P-256、P-384 和 P-521）种子的来源，证明这些种子并非任何哈希算法的输出，而只是 C 标准库中 lrand48 伪随机数生成器以 Unix 时间戳为种子生成的值。这一发现解决了困扰密码学界数十年的谜团，不过第五个二进制种子 B-163 仍无法解释，外界怀疑是发布过程中的录入笔误。 二十多年来，这些来历不明的种子一直助长着外界对美国国家安全局（NSA）故意挑选 NIST 曲线以植入后门的猜测，如今证明它们只是普通的时间戳随机数生成器输出，消除了人们对广泛部署标准的重大信任疑虑。同时，这也是 AI 辅助研究解决人类密码学家多年未能攻克难题的一次重要示范。 该发现确认了种子的生成方式，但并未说明最终曲线是如何被选定的：几个月间生成的其他候选值都已被丢弃、无法观测，因此原则上仍不排除通过搜索特定时间戳来挑选具备特定属性的曲线。lrand48 本身是一个 48 位线性同余随机数生成器，除 B-163 之外，所有受测种子都与它的输出吻合。

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**背景**: ECDSA 是应用最广泛的椭圆曲线密码标准，NIST 于 2000 年将其纳入 FIPS 186-2 数字签名标准，其中列出了一系列不同规模和安全性级别的标准曲线。每条曲线由若干参数以及一个据称是随机的“种子”定义，任何人都可以通过对该种子做哈希来验证参数确实是由随机过程生成的，而不是被人为挑选以暗藏弱点。由于原始种子从未公布且无法复现，研究者长期怀疑这些曲线可能被刻意设计过，而 NSA 在标准制定中的角色更加深了这种担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/ecdsa-curve-origins">Claude reveals ECDSA curve origins \ Anthropic</a></li>
<li><a href="https://saweis.net/posts/nist-curve-seed-origins.html">How were the NIST ECDSA curve parameters generated?</a></li>
<li><a href="https://linux.die.net/man/3/lrand48">lrand48 (3) - Linux man page</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对结果表示欢迎，调侃“13 年的阴谋论”原来只是 srand48(time(NULL))，并称赞 Anthropic 选择更高金额的赏金并捐给 ISRG。最有分量的保留意见来自部分评论者：他们认为这只证实了种子的生成方法，而非曲线的挑选过程，因为被丢弃的候选值无法观测，仍不能排除有人通过定向搜索时间戳来获得特定曲线；也有人指出，异常的 B-163 种子最合理的解释就是发布时出现了笔误。

**标签**: `#cryptography`, `#ECDSA`, `#NIST curves`, `#AI research`, `#security`

---

<a id="item-2"></a>
## [特斯拉发布搭载 SpaceX 火箭推进器、可悬浮飞行的新一代 Roadster](https://www.tesla.com/roadster) ⭐️ 8.0/10

特斯拉发布了新一代 Roadster，该车搭载源自 SpaceX 的冷气推进器与燃烧式火箭推进器，使车辆能够获得额外加速、实现悬浮，甚至飞行，相关演示出现在特斯拉的宣传视频和推文中。据报道该车分为两种配置：一种使用冷气推进器（无燃烧），仅用于提供额外向前加速度；另一种使用真正的燃烧式火箭发动机，已出现在视频中，且据称仅限受邀用户购买。 这一发布模糊了消费级汽车工程与航空航天推进技术之间的界限，成为电动汽车行业中最不寻常的高关注度产品宣称之一，并重新引发了关于“技术上可行”与“商业上可售”之间差距的争论。同时，它也放大了外界对特斯拉长期做法的质疑——即为一款可能永远不会量产的车型收取多年期、无利息的预订金。 冷气推进器通过将储存的加压（通常为惰性）气体经喷嘴膨胀排出产生推力，整个过程不发生燃烧，因此结构简单可靠，但推力与效率都明显低于传统火箭发动机。由于这类系统依赖有限的压缩气体储量以及沉重的储罐、阀门和管路，社区评论者估计该车可能只能完成一次跳跃或几秒钟的推力输出就需要补充，而且车内空间可能被硬件大量占据。

hackernews · shekhar101 · 10月16日 01:32 · [社区讨论](https://news.ycombinator.com/item?id=50112657)

**背景**: 冷气推进器被视为最简单的火箭发动机形式：它仅由储气罐、调节阀、推进喷嘴和极少的管路组成，广泛用于 CubeSat 等小型航天器的姿态控制与轨道机动，因为它避免了燃烧式发动机带来的高温、污染和火工品风险。相比之下，燃烧式火箭推进器通过燃烧推进剂产生大得多的推力，但温度更高、结构也复杂得多。特斯拉多年来一直在为新一代 Roadster 收取预订金，这也是本次发布讨论中“预订金模式”成为焦点话题的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cold_gas_thruster">Cold gas thruster - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/Cold_gas_thruster">Cold gas thruster</a></li>

</ul>
</details>

**社区讨论**: 社区情绪在由衷惊叹与尖锐质疑之间交织：有评论者称把大型风扇和火箭发动机装进高性能汽车是了不起的工程成就，不少人对它真的能飞、还能垂直行驶或吸附在天花板上感到意外。也有人质疑其经济性与实用性，指出压缩气体储量极为有限、储罐与管路会带来空间和重量代价，而且燃烧版本还是“仅限受邀”。反复出现的批评是：特斯拉实际上是在为一款可能永远不会实现的车型收取多年预订金，被形容为“免费贷款”。

**标签**: `#Tesla`, `#electric-vehicles`, `#SpaceX`, `#engineering`, `#aerospace`

---

<a id="item-3"></a>
## [PS5LM 让破解版 PS5 原生运行 llama.cpp 与 GGUF 模型](https://github.com/cobanov/PS5LM) ⭐️ 8.0/10

GitHub 上的 PS5LM（cobanov/PS5LM）项目让破解后的 PlayStation 5 能够原生运行基于 llama.cpp 的 GGUF 模型推理，把一台封闭的游戏主机变成通用的本地大模型机器。社区成员表示它可以跑一个约 270 亿参数的 Qwen 模型（2 bit 量化），质量一般但足以胜任长时间运行的任务。 它表明一台大众消费级游戏主机也能充当极低成本、长期在线的本地推理设备，进一步印证了黑客把封闭设备改造成通用计算机的趋势。这对想要极便宜 token 生成的爱好者有实际意义，而对索尼这类并不乐见此事的厂商则构成了压力。 该方案需要一台已破解的 PS5，而主机定制的 AMD APU 与统一内存架构正是 LLM 推理可行的关键；据社区讨论，基于 AMD 精简版“Cyan Skillfish”APU、在 eBay 上约 150–200 美元的 BC250 主板可能同样可用。2 bit 量化用明显的模型质量换取显存占用与速度，因此其价值在于低风险任务上的吞吐量，而非高质量推理。

hackernews · Anon84 · 10月16日 18:32 · [社区讨论](https://news.ycombinator.com/item?id=50122431)

**背景**: llama.cpp 是一个开源的 C/C++ 推理库，配合 GGML 张量库，能在多种硬件上以极低配置成本高效运行大语言模型。GGUF 是随其一同诞生的模型文件格式，如今已成为分发量化大模型的事实标准，被 Ollama、LM Studio、GPT4All、koboldcpp 等工具原生支持。所谓“破解的 PS5”，是指绕过主机原有安全限制、可以运行未签名或自制程序的主机，这也是在其上加载 llama.cpp 的前提。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Llama.cpp">llama.cpp - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/GGUF">GGUF - Wikipedia</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp">GitHub - ggml-org/llama.cpp: LLM inference in C/C++</a></li>

</ul>
</details>

**社区讨论**: 评论者总体热情高涨，但在风险上存在分歧：有人主张项目不应托管在 GitHub，因为索尼随时可能下架页面，应该默认使用自有域名。也有人更关注实用性，指出 PS5 每天电费仅约 70 美分，却能产出约 200 万输出 token，非常适合监控服务器错误率、查看安防录像或控制浇水之类的长期低智能任务；还有人提到更便宜的 AMD BC250 主板，并认为由大模型驱动的游戏 NPC 终将成为标配。

**标签**: `#llama.cpp`, `#PS5`, `#GGUF`, `#local-llm`, `#hardware-hacking`

---

<a id="item-4"></a>
## [研究人员利用存在 37 年的 OpenBSD 内核漏洞获取 root](https://calif.io/research/big-fish) ⭐️ 8.0/10

安全公司 Calif 公布了一个本地提权漏洞利用的概念验证，通过将大约 37 年前的整数溢出漏洞与另一个内核缺陷串联，可在 OpenBSD 7.9 上获得 root 权限。主漏洞位于 SysV 共享内存 attach 计数器（shmat）中，可追溯到最初的 BSD 源代码，该利用还绕过了 OpenBSD 的 KARL 内核地址随机化以及 SMAP、SMEP 硬件保护机制。 OpenBSD 以极其严格的安全审计闻名，因此一个建立在几十年前代码之上的 root 漏洞利用，动摇了“经过长期审查的成熟代码库天然安全”这一假设。它还表明，KARL、SMAP、SMEP 等现代内核加固机制可以被逻辑层缺陷与内存破坏原语的组合所击破，这对每一位 OpenBSD 管理员以及所有思考纵深防御的人都意义重大。 核心原语是共享内存 attach 路径中一个有符号 16 位 short 计数器，攻击者通过 fork 出 259 个进程使其溢出，再与一个 use-after-free 的竞态以及 IP 组播选项处理中的越界写组合，从而触达内核内存。防御方应在授予本地访问权限前核实内核勘误补丁，因为该修复以 OpenBSD 内核补丁形式发布，而非完整版本升级。

hackernews · Lobste.rs · 10月16日 14:44 · [社区讨论](https://news.ycombinator.com/item?id=50118977)

**背景**: OpenBSD 是一个以安全为核心目标的类 Unix 操作系统，其开发者长期宣称默认安装下极少出现远程漏洞，其代码也是自由软件世界中审计最密集的之一。存在漏洞的代码来自 System V 共享内存——一种古老的进程间通信 API，每个被 attach 的内存段都会维护一个引用计数；由于该计数器原本是 16 位有符号整数，足够多的并发 attach 就会使其回绕为负值。KARL 是 OpenBSD 在启动时随机化内核地址的机制，而 SMAP 和 SMEP 是阻止内核执行或读取用户态内存的 CPU 特性，因此同时绕过这三者正是该利用引人关注之处。此外，该漏洞在 1999 年 8 月 NetBSD 重写这段代码时被无意间修复，也就是说它仅因历史偶然才一直留在 OpenBSD 中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/researchers-demonstrate-openbsd-root.html">Researchers Demonstrate OpenBSD Root Exploit Chaining 37-Year ...</a></li>
<li><a href="https://cybersecuritynews.com/37-year-old-kernel-openbsd-flaw/">37-Year-Old Kernel Flaw Exploited to Gain Root Access on ...</a></li>
<li><a href="https://cloudnews.tech/ai-is-finding-os-bugs-at-a-new-scale-and-linux-is-feeling-the-pressure/">AI Is Finding OS Bugs at a New Scale, and Linux Is... | Cloud News</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了文章采用“OpenBSD 发行版”风格的配图，并调侃是否会推出主题曲；有人指出该漏洞在 1999 年 8 月 NetBSD 的一次重写中被无意修复。讨论的核心是模糊测试或静态分析是否真能发现这类漏洞，多数人倾向于认为它需要对利用原语进行人工推理，而非依赖自动化工具，这也凸显出仅靠代码审查极难捕捉此类缺陷。

**标签**: `#OpenBSD`, `#kernel security`, `#vulnerability research`, `#exploitation`, `#static analysis`

---

<a id="item-5"></a>
## [Linus Torvalds 为 AI 辅助的 Linux 内核贡献定下规则](https://lore.kernel.org/lkml/CAHk-=whTs09_ozN+e09GU68N1wPP56MUzDjrg9rnKxQUa0A_4Q@mail.gmail.com/) ⭐️ 8.0/10

Linus Torvalds 在 Linux 内核邮件列表发帖，阐述了应当如何处理 AI 辅助提交的代码，并针对审查、署名与维护者信任等问题表态。此举恰逢内核新的贡献者规则出台：允许使用 AI 工具，但要求通过 "Assisted-by" 提交标签进行披露，并由真人完成 Signed-off-by。 Torvalds 的表态分量极重，因为他是内核的最终裁决者，能够为这一全球最重要的开源项目之一确立政策与社区规范，而其他项目往往会效仿。这直接影响每一位内核贡献者与维护者：他们必须决定接受多少 AI 生成的代码、如何标注来源，以及由此产生的审查负担由谁承担。 按照正在形成的惯例，贡献者可以使用任何 AI 工具，但必须在提交上打上 "Assisted-by" 标签；同时只有真人才能签署 Developer Certificate of Origin（开发者原创声明），AI 无法认证代码的作者身份或再分发权利。仍有若干问题悬而未决：披露到什么程度才算充分；大量 AI 辅助补丁是否会加剧本已吃紧的维护者审查瓶颈；以及未披露的 LLM 协助是否应被视为信任问题，而不仅仅是流程细节。

rss · Lobste.rs · 10月16日 02:50

**背景**: Linux 内核要求每个提交都带有一行 "Signed-off-by"，作为 Developer Certificate of Origin（开发者原创声明）的一部分；这是一项法律声明，表示提交者有权以合适的开源许可证贡献该代码，而且这项声明只能由自然人做出。与此同时，内核的代码提交量正处于历史高位，但负责审查与合并的人手几乎没有增长，这就形成了众所周知的维护者瓶颈——稀缺资源是审查能力，而非写代码的能力。能够批量生成看似合理补丁的 AI 编程助手，由此在署名、许可证合规以及谁来为正确性背书等方面提出了棘手问题。类似的讨论正在整个开源界展开：一些项目采用强制性的 "Assisted-by" 披露，而另一些项目（如 QGIS）则直接禁止 AI 辅助贡献。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://allthingsopen.org/articles/open-source-ai-contributions-assisted-by-git-trailer-standard">Assisted-by: How open source projects are drawing the line on ...</a></li>
<li><a href="https://www.linkedin.com/posts/atulgg_httpslnkdingn2wy8jb-i-read-above-activity-7451579481632296960-Nh0p">Linux kernel AI policy: humans must sign off on... | LinkedIn</a></li>
<li><a href="https://lwn.net/Articles/703005/">On Linux kernel maintainer scalability [LWN.net]</a></li>

</ul>
</details>

**标签**: `#Linux Kernel`, `#AI-Assisted Development`, `#Open Source`, `#Linus Torvalds`, `#Developer Policy`

---

<a id="item-6"></a>
## [估值曾达 50 亿美元的 AI 独角兽 Character.AI 申请破产，2000 万美元向迪士尼出售 IP 许可](http://www.geekpark.net/news/372437) ⭐️ 7.0/10

当地时间 10 月 12 日，Character.AI 在美国特拉华州法院提交《破产法》第 11 章重组申请，披露的资产与负债均在 5000 万至 1 亿美元区间，并进入法院监督下的资产拍卖流程。迪士尼已提前以底价竞购方（stalking horse bidder）身份签约，出价 2000 万美元买下部分知识产权的非独占永久许可，并由其雇佣的前员工提供过渡期技术服务，拍卖窗口预计在 11 月底至 12 月初收尾。 这家由 Transformer 论文核心作者创办、巅峰估值 50 亿美元的公司轰然倒下，折射出生成式 AI 消费应用在成本、版权与商业化方面的结构性困境。同时它也显示，迪士尼这类大型版权方正从起诉 AI 平台，转向直接收购其对话技术本身。 这笔交易只包含 IP 许可及相关债权，不涉及公司主体、产品 App 和用户资产，说明迪士尼对继续运营 Character.AI 这个平台兴趣不大。如果最终没有更高出价者接盘，平台将关停，数千万用户创建的角色与对话记录都可能变成无法访问的数据。

rss · 极客公园 · 10月16日 02:22

**背景**: Character.AI 由前谷歌工程师 Noam Shazeer 和 Daniel De Freitas 于 2021 年创立，二人正是对话模型 LaMDA 的开发者，产品 2022 年公开上线，允许用户自建角色并与之聊天。2023 年 3 月，a16z 领投 1.5 亿美元 A 轮，彼时公司尚无收入，估值 10 亿美元；到 2023 年 9 月，市场传闻其将以超过 50 亿美元估值融资。2024 年谷歌以约 27 亿美元获得其技术许可，并把 Shazeer 和约 30 名研究员接回 DeepMind，这种所谓「反向人才收购」让公司失去了创始人和自研模型，沦为一家产品公司。所谓「stalking horse bidder」是破产拍卖中的常见机制，即首个出价方定下底价，后续买家可在法院监督下出更高价竞得。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Character.ai">Character.ai</a></li>
<li><a href="https://grokipedia.com/page/Character.ai">Character.ai</a></li>

</ul>
</details>

**标签**: `#Character.AI`, `#AI startup`, `#bankruptcy`, `#generative AI`, `#business model`

---

<a id="item-7"></a>
## [豆包 SAEP 公示结束：155 款应用拒绝 AI 屏幕自动化](http://www.geekpark.net/news/372436) ⭐️ 7.0/10

10 月 14 日，豆包手机助手推出的《屏幕自动化操作声明协议》（SAEP）正式结束 30 天公示期，随之公布的拒绝名单显示共有 155 款第三方应用明确拒绝 AI 自动化操作，其中腾讯 66 款、阿里 23 款、美团 11 款、快手 14 款，连 Kimi、DeepSeek 等 AI 赛道同类产品也在列。名单当日经历两轮更新，首批发布 153 款，补全长尾应用后最终确定为 155 款。 这是移动端首次以正式协议的形式，把 AI Agent 能否操作应用这件事摆上台面，而头部平台的集体拒绝，则是超级 App 在 AI Agent 时代第一次公开对自身应用边界与流量主权表态。它意味着系统级 AI 自动化将不再由 AI 厂商单方面技术适配决定，而要在 AI 厂商、开发者和用户之间形成博弈与协商，可能显著影响手机端跨应用 AI Agent 的落地速度与形态。 按照 SAEP 规则，公示期内所有第三方应用默认不开放 AI 操作，只有主动声明同意的应用才会被支持；公示期结束后，未明确提交拒绝声明的应用将按风险层级逐步开放权限，而已明确拒绝的应用始终不会被 AI 自动化操作，开发者后续也可随时调整声明状态。技术上，该能力基于系统级权限在后台完成屏幕读取与交互，区别于需占用前台的普通无障碍工具，且权限仅针对 AI 自动化操作，完全不影响应用本身的正常手动使用。

rss · 极客公园 · 10月16日 02:18

**背景**: 能操作手机界面的 AI Agent（业内常称为 CUA，即 Computer Operation Agent，目前主流走 GUI 技术路线）需要读取屏幕并模拟点击来跨应用完成任务，这与成熟平台的风控体系天然冲突。字节跳动在 2025 年 12 月联合中兴努比亚推出豆包手机助手技术预览版，搭载于努比亚 M153 工程样机，随后用户很快反馈微信、淘宝、闲鱼等应用出现登录异常、频繁人机验证和闪退，豆包官方因此主动限制了刷分激励类、金融类应用与竞技游戏场景下的自动操作。2026 年 9 月 14 日消费者版本与 SAEP 同步发布，努比亚 NaviX Ultra 一同发售；不到两周后，大量用户反馈登录《王者荣耀》触发“设备环境异常”，账号被强制下线甚至短时封禁，理由是“使用第三方辅助工具”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://eu.36kr.com/en/p/3987162000210692">Doubao Smartphone vs Super App Walled Gardens: The Second...</a></li>
<li><a href="https://eu.36kr.com/en/p/3984764117007111">Doubao Smartphone Official Launch Tomorrow: Can AI Now Help You...</a></li>
<li><a href="https://www.opoinstall.com/fr/blog/nubia-navix-ultra-os-agent-routing">Nubia lance le smartphone IA NaviX Ultra ? - Opoinstall</a></li>

</ul>
</details>

**标签**: `#AI Agents`, `#Mobile Ecosystem`, `#Screen Automation`, `#Platform Policy`, `#China Tech`

---