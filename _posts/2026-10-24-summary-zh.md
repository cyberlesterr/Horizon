---
layout: default
title: "Horizon Summary: 2026-10-24 (ZH)"
date: 2026-10-24
lang: zh
---

> 从 45 条内容中筛选出 5 条重要资讯。

---

1. [月之暗面发布 Kimi K3.1 Pro 及高速版 Highspeed](#item-1) ⭐️ 8.0/10
2. [安全研究人员称借助 AI 红队演练成功攻破 iPhone](#item-2) ⭐️ 8.0/10
3. [OpenSSL 4.1.0 发布，新增 DTLS 1.3 支持](#item-3) ⭐️ 8.0/10
4. [Block 发布 Dessa：号称最逼真的全双工语音模型，可在 MacBook 本地运行](#item-4) ⭐️ 7.0/10
5. [技术博客提出反直觉观点：内存可能很慢，磁盘却可以很快](#item-5) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [月之暗面发布 Kimi K3.1 Pro 及高速版 Highspeed](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

月之暗面（Moonshot AI）在 Kimi API 上线了 Kimi K3.1 Pro，这是全新 K3.1 系列的首个模型，同时推出了速度更快的伴随版本 Kimi K3.1 Pro Highspeed。官方称 K3.1 Pro 是其迄今最强的 3T 级模型，拥有 100 万 token 上下文窗口，并在编程、3D 创作、金融研究及其他智能体任务上有显著提升。 此次发布让一个面向开放权重路线的中国前沿模型在质量与价格上直接对标闭源领先者，早期社区测试显示它与 Claude Sonnet 5.5 大致持平而成本不到一半。如果月之暗面兑现发布完整权重的承诺，将显著扩大开发者可自行部署的前沿智能体编程能力边界。 K3.1 Pro 目前尚未开放权重，月之暗面表示后续会发布完整模型权重；公司还称有意将其攻击性网络能力控制在自身流水线可达到的水平之下，并计划逐步提升开放权重中的网络能力。社区测评显示它在 Pac-Man 基准上得分 93（与 Claude Sonnet 5.5 持平），耗时 11 分钟、成本 0.68 美元，而后者为 14 分钟、1.61 美元；在 16 个场景的集合中，每个 Three.js 场景成本约 0.19 美元。

hackernews · Jowsey · 10月23日 16:59 · [社区讨论](https://news.ycombinator.com/item?id=50212065)

**背景**: Kimi 是中国 AI 实验室月之暗面（Moonshot AI）的模型系列，上一代 Kimi K3 是拥有 2.8 万亿参数的开源权重多模态模型，基于 Kimi Delta Attention（KDA）与 Attention Residuals 构建，上下文窗口为 100 万 token。所谓“开放权重”指模型参数对外公开、任何人可下载并自行部署，这对成本、隐私与定制化都至关重要。社区基准如 Pac-Man bakeoff（让模型写一个可玩的吃豆人游戏）和 Three.js eval（让模型生成 3D 场景并由人类盲评投票）虽属非正式评测，却广受关注，常与 Artificial Analysis 智能指数一同被引用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-1-pro-quickstart">Kimi K3.1 Pro - Kimi API Platform</a></li>
<li><a href="https://www.unite.ai/moonshot-ai-releases-kimi-k3-1-pro-first-model-in-new-k3-1-series/">Moonshot AI Releases Kimi K3.1 Pro, First Model in New K3.1 ...</a></li>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3">moonshotai/ Kimi -K3 · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论总体偏务实：有人指出 K3.1 Pro 在 Pac-Man 基准上与 Claude Sonnet 5.5 持平而成本约为其四成；也有人称自己订阅每月 99 美元的套餐后，单次会话仅 47 分钟就撞上 5 小时配额上限，提醒实际可用额度远低于预期。还有人觉得 Kimi 比美国模型更直白、更好辩，并质疑月之暗面的安全表述——即它本可以打造更强的攻击性网络能力却选择不发布。

**标签**: `#LLM`, `#Kimi`, `#AI model release`, `#benchmarks`, `#AI safety`

---

<a id="item-2"></a>
## [安全研究人员称借助 AI 红队演练成功攻破 iPhone](https://blog.calif.io/p/iphone) ⭐️ 8.0/10

安全研究团队在 blog.calif.io 发布了一篇题为《今天我们攻破了我们一开始就打算攻破的东西：iPhone》的文章，声称团队实现了对 iPhone 的漏洞利用目标，并附上了演示视频。该文在 Hacker News 上引发热议（约 707 分、467 条评论），读者围绕越狱、Lockdown 模式以及前沿实验室的访问权限计划如何影响谁能开展此类研究展开了讨论。 一条可信的端到端 iPhone 漏洞利用链意义重大，因为 iOS 是加固程度最高的主流消费级平台，每一次被攻破的演示都会影响数十亿用户对移动安全风险的认知。讨论还揭示出政策层面的问题：如果高级漏洞利用越来越依赖对前沿模型的特权访问，那么圈子之外的研究者可能在结构上处于劣势。 该成果主要以演示视频的形式呈现，而非完整的技术文档，因此文章并未清楚说明是否实现了从初始入口到后渗透持久化的完整链条，也没有说明针对的是哪个 iOS 版本。评论区特别追问苹果的 Lockdown 模式能否缓解所展示的攻击路径，以及被攻破的设备是否仍能接收（或被强制跳过）苹果的系统更新。

hackernews · pavel_lishin · 10月23日 16:21 · [社区讨论](https://news.ycombinator.com/item?id=50211474)

**背景**: Lockdown 模式是苹果随 iOS 16 推出的可选极限安全设置，它通过屏蔽大多数消息附件类型、限制部分网页技术并禁用某些有线连接等功能来大幅缩小攻击面，代价是牺牲日常便利性。越狱指利用漏洞获得 iOS 的 root 级控制权并安装 App Store 之外的软件，随着苹果加入指针认证、签名系统卷和快速安全响应等多层缓解措施，这一做法已变得困难得多。AI 红队演练指以对抗方式使用模型来发现漏洞和不安全行为，如今多家前沿实验室会将最强模型置于类似“可信网络访问”的计划之后，只向经过审查的防御方开放。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.apple.com/en-us/105120">About Lockdown Mode - Apple Support</a></li>
<li><a href="https://votal.ai/glossary/ai-red-teaming">AI Red Teaming : Definition , Scope, and Continuous Testing | VotalAI</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞演示令人印象深刻，同时提出三点主要担忧：生态锁定意味着越狱后的 iPhone 可能被切断 iCloud 和 iMessage 服务，几乎沦为 iPod touch；前沿实验室的“可信访问”计划更像是研究壁垒而非安全保障，把独立研究者排除在外；以及 Lockdown 模式针对这些具体漏洞利用的真实有效性仍未得到验证。

**标签**: `#security`, `#iOS exploitation`, `#jailbreaking`, `#AI red-teaming`, `#zero-days`

---

<a id="item-3"></a>
## [OpenSSL 4.1.0 发布，新增 DTLS 1.3 支持](https://github.com/openssl/openssl/releases/tag/openssl-4.1.0) ⭐️ 8.0/10

OpenSSL 4.1.0 已发布，作为一次功能版本更新，为这一广泛使用的密码库新增了 DTLS 1.3 支持、GREASE 以及针对特定架构的优化。 由于 OpenSSL 支撑着无数操作系统、服务器和应用中的 TLS 与密码学操作，新版本可能影响庞大的软件供应链；DTLS 1.3 支持对 WebRTC、VPN 和物联网等基于 UDP 的安全通信尤为重要。 发布说明标记了可能不兼容的变更和四个 DTLS 问题，因此维护者应在采用前审阅升级说明；该版本还包含 GREASE 和针对特定架构的性能优化工作。

rss · Lobste.rs · 10月23日 15:18

**背景**: OpenSSL 是一个实现 TLS/SSL 和通用密码学的开源工具包，用于保护 HTTPS、电子邮件、VPN 以及许多其他协议。DTLS 是 TLS 针对 UDP 等数据报传输的变体，适用于实时媒体和资源受限的物联网设备等场景，因为 TCP 的可靠传输在这些场景中会造成问题。从 3.x 到 4.x 的过渡涉及架构变更和下游迁移成本，因此重大版本发布需要提前规划。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/openssl/openssl/releases">Releases · openssl/openssl - GitHub</a></li>
<li><a href="https://runtimewire.com/article/openssl-4-1-0-dtls-13-release">OpenSSL 4.1.0 adds DTLS 1.3 support to its cryptographic library</a></li>
<li><a href="https://openssl-library.org/post/2026-09-09-openssl-4.1-alpha/">OpenSSL 4.1 Alpha Release Announcement | OpenSSL Library</a></li>

</ul>
</details>

**标签**: `#openssl`, `#cryptography`, `#security`, `#release`, `#open-source`

---

<a id="item-4"></a>
## [Block 发布 Dessa：号称最逼真的全双工语音模型，可在 MacBook 本地运行](https://block.xyz/dessa) ⭐️ 7.0/10

Block 推出了 Dessa，称其为迄今最逼真的全双工语音模型，能够边听边说，而非传统的轮流发言。该公司表示，Dessa 可在 MacBook Pro M4 Max 或更高配置上本地运行，且仅用一台 NVIDIA GB200 NVL72 就完成了训练。 如果低延迟和高表现力真的能在消费级硬件上成立，实时语音智能体就可能变得廉价、私密并可在本地部署，而不必依赖大型云端集群。与此同时，一个如此逼真却没有强推理能力支撑的语音模型，也直接指向身份冒充和语音诈骗风险，这正是讨论的焦点所在。 Block 声称 Dessa 学习语言所用的词量比大型语言模型少数百倍，训练配方相当高效，但公告并未给出模型规模、参数量以及具体的延迟数据。外界关注的焦点是演示对话，而质疑者认为，诸如发笑或抢话打断之类的行为更像是刻意训练出的“打断”，而非自然的对话节奏。

hackernews · dsr12 · 10月23日 19:09 · [社区讨论](https://news.ycombinator.com/item?id=50213925)

**背景**: 大多数语音助手采用轮次制：一方说完，另一方再说，中间留有停顿。全双工模型则是在生成语音的同时持续聆听，这才是人类真实的交谈方式，因此可以做到“嗯嗯”这类附和、重叠说话以及快速打断。NVIDIA GB200 NVL72 是一种机架级系统，将数十颗 Blackwell GPU 与 Grace CPU 互联，因此仅用一台这样的系统训练出一个模型，对现代语音模型而言算力投入相当小。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2605.20755">[2605.20755] DuplexSLA: A Full-Duplex Spoken Language Model ...</a></li>
<li><a href="https://www.alphaxiv.org/abs/2609.36903">MultiTalk: Scaling Full - Duplex Speech Models to Long... | alphaXiv</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者对“MacBook 本地推理 + 富有表现力的低延迟对话”这一组合印象深刻，认为这对较小规模的 AI 团队是一项了不起的成就。但许多人对演示本身持怀疑态度，认为被训练成尽可能频繁地打断别人显得很做作，短回答之后的那声笑也缺乏说服力。还有人更尖锐地区分了“语音作为通往智能系统的接口”和“语音本身就是产品”，认为一个如此逼真却并不聪明的模型，主要用途就是冒充真人；也有人表示，如果在电话里遇到这种技术，自己根本分辨不出是 AI。

**标签**: `#speech-models`, `#full-duplex`, `#AI`, `#local-inference`, `#Hacker News`

---

<a id="item-5"></a>
## [技术博客提出反直觉观点：内存可能很慢，磁盘却可以很快](https://www.bitflux.ai/blog/memory-is-slow-part3/) ⭐️ 7.0/10

Bitflux 博客系列文章“Memory is Slow”的第三篇《Memory is slow, Disk is fast》提出，在現代硬件与负载条件下，“内存一定比磁盘快”这一传统假设会失效。该文被分享到 Lobste.rs 社区，并引发了围绕内存与存储性能权衡的技术讨论。 开发者在做缓存策略、数据结构选型和 I/O 架构设计时，往往依赖“内存快、磁盘慢”这一经验法则，因此一个有说服力的反例可能会改变系统在吞吐量和延迟上的设计思路。这对从事数据库、缓存和高性能数据管道开发的工程师尤其相关，因为在那些场景中，访问模式和并行度往往比设备的原始延迟更重要。 该文的核心论证在于区分延迟（latency）与带宽（bandwidth），并说明访问模式、预取（prefetching）、队列深度（queue depth）和并行度如何能让存储设备在整体表现上超过内存访问。这篇文章是系列文章的第三部分，其结论建立在前面几篇的基础上，而非一个独立完整的基准测试。

rss · Lobste.rs · 10月23日 20:44

**背景**: 传统上，计算机系统被描述为一个存储层次结构：寄存器和 CPU 缓存最快，DRAM 较慢但仍比存储快几个数量级，而磁盘或 SSD 位于最底层，延迟以微秒到毫秒计。这种排序催生了诸如“把热数据放在内存中”“把 I/O 视为昂贵兜底”等常见的工程经验法则。该博客文章挑战的正是这一模型的简化版本，指出“快”与“慢”取决于衡量的是哪个指标（延迟、带宽，还是并发下的有效吞吐量），也取决于工作负载如何访问数据。

**标签**: `#systems`, `#memory`, `#storage`, `#performance`, `#hardware`

---