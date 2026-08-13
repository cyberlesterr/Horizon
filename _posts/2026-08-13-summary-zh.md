---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 61 条内容中筛选出 12 条重要资讯。

---

1. [Qwen 发布巨型开源权重 MoE 模型 Qwen3.8-2.4T](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Pro 0813 正式发布，定位旗舰模型](#item-2) ⭐️ 8.0/10
3. [Tailscale 将数据库损坏追因到 16 年前的 SQLite WAL 重置漏洞](#item-3) ⭐️ 8.0/10
4. [xAI 发布新前沿模型 Grok 4.6，引发热议](#item-4) ⭐️ 8.0/10
5. [为什么小尺寸 JPEG 在 Chrome 中显示不同](#item-5) ⭐️ 8.0/10
6. [Signal 推出自动密钥验证，抵御中间人攻击](#item-6) ⭐️ 8.0/10
7. [发现 KVM guest-to-host 堆破坏漏洞——但他人抢先一步](#item-7) ⭐️ 8.0/10
8. [马斯克携 Cursor 团队打造的 24 小时 AI 智能体回归](#item-8) ⭐️ 7.0/10
9. [DeepSeek V4 Pro 实测：能力逼近 Fable 5，暗藏大招](#item-9) ⭐️ 7.0/10
10. [AI 入口开始收费：豆包抽佣、千问开放平台](#item-10) ⭐️ 7.0/10
11. [Manus 恢复独立、Gemini 月活破 10 亿、林俊旸创办 AI 公司](#item-11) ⭐️ 7.0/10
12. [Homelab 遭入侵：事后复盘分享安全教训](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Qwen 发布巨型开源权重 MoE 模型 Qwen3.8-2.4T](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) ⭐️ 9.0/10

Qwen 发布了 Qwen3.8-2.4T-A95B，这是一个混合专家（MoE）模型，总参数 2.4 万亿，激活参数 950 亿，提供 BF16 和 FP8 两种格式。模型卡声称其性能介于 Opus 4.8 和 Fable 5 之间，接近前沿水平。 作为迄今最大的开放权重 MoE 发布之一，它可能为愿意投入大量硬件资源的研究者和企业带来接近前沿的性能。同时它也加剧了开放权重领域的竞争，引发社区在量化和部署方面的努力。 BF16 版本需要约 4.9TB 的存储空间，FP8 变体和社区 1-bit 量化版本（约 397GB）使部署更为可行。与相关的 Qwen3.8-Max 不同，开放权重版本缺少视觉输入和 100 万 token 上下文支持，且其许可证限制年收入超过 5000 万美元的企业的商业使用。

hackernews · r/LocalLLaMA · Philpax · 8月12日 15:01 · [社区讨论](https://news.ycombinator.com/item?id=49273478)

**背景**: 混合专家（MoE）是一种神经网络架构，将模型划分为专门的子网络（即专家），每次输入只激活其中一部分。这使得模型可以拥有巨大的总参数量，同时保持相对较低的计算成本。开放权重模型会公开发布其训练后的参数，任何人都可以下载、运行和修改，这与完全专有的系统不同。Qwen 是阿里巴巴开发的一系列大语言模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://www.ibm.com/think/topics/mixture-of-experts">What is mixture of experts? | IBM</a></li>

</ul>
</details>

**社区讨论**: 社区反应热烈但喜忧参半。一些人赞赏技术成就和量化进展，指出 1-bit 版本可能让 Opus 级别性能进入消费级硬件；另一些人则指出 BF16 权重体积不切实际以及许可限制较多。与 Kimi k3 和 DeepSeek V4-Pro 的对比，以及开放权重版本缺少视觉和更长上下文支持，也是反复被提及的话题。

**标签**: `#AI`, `#LLM`, `#Qwen`, `#MoE`, `#open-source`

---

<a id="item-2"></a>
## [DeepSeek V4 Pro 0813 正式发布，定位旗舰模型](https://openrouter.ai/deepseek/deepseek-v4-pro-0813) ⭐️ 8.0/10

DeepSeek 发布了旗舰模型的生产版本 DeepSeek V4 Pro 0813，结束了持续近四个月的预览期。该版本于 2026 年 8 月 12 日以通用可用版本（GA）形式发布，并可通过 OpenRouter 访问。 这是 LLM 领域的一次重要发布，引发了社区的高度关注和实际使用反馈。部分用户报告该模型在编码和开发任务上表现强劲且价格极低，这可能在成本效益方面给竞争对手带来压力，并改变市场预期。 该模型是一个大规模专家混合（MoE）系统，定价为每百万输入 token 0.435 美元、每百万输出 token 0.87 美元，上下文窗口为 1,048,576 个 token，最大输出 384,000 个 token。不过，OpenRouter 页面缺少详细的基准测试数据，所提供的图表也因缺少标签和比例尺而受到批评。

hackernews · explosion-s · 8月12日 16:04 · [社区讨论](https://news.ycombinator.com/item?id=49274600)

**背景**: DeepSeek 是一家总部位于杭州的中国人工智能公司，专注于开发大型语言模型。专家混合（MoE）架构会将 token 路由到专门的子网络，从而在保持推理成本可控的同时实现非常大的参数量。V4 Pro 0813 经历了约四个月的预览期，现被定位为该公司的旗舰生产模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-pro-0813">DeepSeek V4 Pro 0813 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.unite.ai/deepseek-ships-v4-pro-as-its-flagship-model-leaves-preview/">DeepSeek Ships V4 Pro as Its Flagship Model Leaves Preview – Unite.AI</a></li>
<li><a href="https://news.ycombinator.com/item?id=49274600">DeepSeek V4 Pro 0813 | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 社区反馈褒贬不一。部分用户批评页面呈现不佳、图表没有标签或比例尺，声称看后更加困惑；也有用户报告了积极的真实使用结果：一位用户表示模型在流量模拟器中找到了显著改进且未引入新问题，另一位用户则对比称 DeepSeek 运行 12 分 02 秒花费 0.12 美元但存在 bug，而 Grok 4.6 运行 3 分 18 秒花费 1.41 美元且无 bug，凸显了 DeepSeek 在成本上的优势。

**标签**: `#deepseek`, `#llm`, `#ai`, `#model-release`, `#hackernews`

---

<a id="item-3"></a>
## [Tailscale 将数据库损坏追因到 16 年前的 SQLite WAL 重置漏洞](https://tailscale.com/blog/sqlite-wal-reset-bug) ⭐️ 8.0/10

Tailscale 将持续的数据库损坏归因于 SQLite 写前日志（WAL）重置逻辑中的一个竞态条件，SQLite 开发者估计该漏洞至少已存在 16 年。该公司资助了一个开源的 VFS 垫片（shim），它能够迅速隔离该竞态，并帮助在将来检测类似问题。 这一发现揭示了 SQLite（全球部署最广泛的数据库引擎之一）中一个长期隐藏的数据损坏隐患。这也展示了公司如何资助针对性的开源工具来排查微妙的基础设施问题，从而让更广泛的生态受益。 该漏洞是重置 WAL 索引时出现的竞态条件；即使在单写者设计下，如果检查点（checkpoint）在不同的连接上运行，也仍可能触发。Tailscale 资助的 VFS 垫片能够拦截文件操作，从而复现并检测此类情况，该公司还详细写下了调试过程。

hackernews · Lobste.rs · 8月12日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49272832)

**背景**: SQLite 使用写前日志（WAL）机制，在写入的同时允许并发读取，并通过一个 WAL 索引文件（包含 mxFrame、nBackfill 等字段）来跟踪帧与回填状态。当这些字段被不当更新时，WAL 重置竞态就会破坏数据库；而 SQLite 的 VFS 抽象层允许开发者拦截文件系统调用，因此可以构造校验和或诊断垫片。尽管 SQLite 的测试覆盖极其广泛，该漏洞仍在十多年里未被发现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tailscale.com/blog/sqlite-wal-reset-bug">How Tailscale helped find the SQLite WAL - Reset bug</a></li>
<li><a href="https://www.sqlite.org/vfs.html">The SQLite OS Interface or " VFS "</a></li>
<li><a href="https://antithesis.com/blog/2026/wal-reset-bug/">Breaking the WAL | Antithesis</a></li>

</ul>
</details>

**社区讨论**: 评论者指出一个讽刺的事实：SQLite 庞大的测试套件——9200 万行测试、59000% 的分支覆盖率——依然没有捕获该漏洞，并引用 Dijkstra 的名言：测试只能证明 bug 的存在，而不能证明其不存在。其他人则称赞 Tailscale 资助了一个高度针对性的开源调试工具，并写出了精彩的复盘；一位读者对单写者设计为何仍会触发竞态感到好奇，并表示文章的解释令人满意。

**标签**: `#SQLite`, `#debugging`, `#databases`, `#Tailscale`, `#open-source`

---

<a id="item-4"></a>
## [xAI 发布新前沿模型 Grok 4.6，引发热议](https://x.ai/news/grok-4-6) ⭐️ 8.0/10

xAI 在 x.ai 上发布了新的前沿 AI 模型 Grok 4.6。这一发布在 Hacker News 上引发了关于其能力、定价以及与 GPT-5.6-Sol、Claude 4.8/5 等对手竞争地位的广泛讨论。 Grok 4.6 可能通过更低的 API 价格和在 Cursor 等平台上的慷慨使用额度，以基准领先的性能加剧 AI 市场竞争。它标志着 xAI 的快速迭代和推理基础设施的壮大，给其他前沿实验室带来压力，也为开发者提供了另一个可信的选择。 Hacker News 讨论指出，xAI 的 API 添加了默认系统提示，覆盖了用户的指令，可能导致模型拒绝讨论系统提示。一些评论者还质疑基准测试的真实性，指出各大实验室在两个月内迅速推出 Fable 级别的模型，而其他人则称赞 Grok 4.5 简洁快速的使用体验。

hackernews · iLuddite · 8月12日 15:32 · [社区讨论](https://news.ycombinator.com/item?id=49274027)

**背景**: xAI 是埃隆·马斯克的人工智能公司，以 Grok 系列聊天机器人和大语言模型而闻名，该系列始于 2023 年的 Grok-1，此后经历了 Grok 3、Grok 4.5 直至现在的 Grok 4.6。前沿模型代表任何特定时间最先进的 AI 系统，使用海量数据集训练并执行复杂的多步推理任务。xAI 在自身推理能力上大量投资，从而能提供有竞争力的定价和在多个平台上的可用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_(chatbot)">Grok (chatbot) - Wikipedia</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论呈现出两极分化的观点：一些人质疑基准测试的真实性和模型相似性，认为可能存在蒸馏或基准测试造假，而另一些人则欢迎 Grok，认为它快速、简洁且具有竞争力，能带来良性竞争。还有一个值得注意的技术抱怨是 API 的默认系统提示会覆盖用户指令，给开发者带来实际摩擦。

**标签**: `#AI`, `#Grok`, `#xAI`, `#LLM`, `#frontier models`

---

<a id="item-5"></a>
## [为什么小尺寸 JPEG 在 Chrome 中显示不同](https://guillaumetech.github.io/posts/jpg-scaling-chrome/) ⭐️ 8.0/10

这篇文章解释了 Chrome 的降采样解压优化会在图片显示较小时以较低分辨率解码 JPEG，而 Firefox 会先完整解码再缩放，从而导致可见的渲染差异。 这对于期望跨浏览器图片渲染一致的 Web 开发者和浏览器工程师来说很重要。小图标等图片可能会因浏览器不同而明显更模糊或更清晰，影响设计还原度和用户体验。 这种差异源于 Chrome 为了性能而牺牲部分画质的优化路径，它使用部分 JPEG 解码。正如评论者指出的，Chrome 的缩放算法往往更模糊，而 Firefox 的更锐利但可能产生轻微振铃伪影。

hackernews · Lobste.rs · 8月12日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=49272549)

**背景**: JPEG 是一种有损压缩格式，通常用于照片，它依赖于离散余弦变换（DCT）系数。在缩小图像时，解码器可以解码所有系数再对结果进行缩放，也可以只解码小尺寸输出所需的系数。Chrome 为了速度选择了后者，而 Firefox 选择了前者，导致小图片的视觉效果不同。相关的 Stack Overflow 问题显示，用户多年来已注意到 Chrome 中缩放图片模糊的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stackoverflow.com/questions/37906602/blurry-downscaled-images-in-chrome">html - Blurry downscaled images in Chrome - Stack Overflow</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为这个问题确实存在，有人指出 PNG 也受影响，甚至导致 Electron 应用中的图标显示异常。其他人建议使用合适尺寸的图片或矢量格式，还有评论者提供了一个 Firefox 相关 bug 的链接。也有人争论这种差异主要是由于解压优化还是仅仅因为缩放算法不同。

**标签**: `#jpeg`, `#chrome`, `#browser`, `#image-scaling`, `#firefox`

---

<a id="item-6"></a>
## [Signal 推出自动密钥验证，抵御中间人攻击](https://signal.org/blog/automatic-key-verification/) ⭐️ 8.0/10

Signal 推出了自动密钥验证（Automatic Key Verification）功能，利用密钥透明度机制自动校验安全码，以保护消息和通话免受中间人攻击。该功能已在 Signal 官方博客上发布，并开始向用户推送。 这一功能意义重大，因为它免去了用户手动验证安全码的负担，让普通用户也能获得强大的中间人攻击防护。它针对的是 Signal 自有服务器被攻破或内部人员作恶的风险，而 Signal 是全球使用最广泛的安全通信应用之一。 该功能基于密钥透明度（key transparency）技术构建；当自动密钥验证不可用时，用户仍需手动比对安全码。它专门针对服务器层面的密钥替换攻击，而非联系人设备被攻破等其他威胁。

rss · Lobste.rs · 8月12日 07:10

**背景**: Signal 的每一对一聊天都有一串安全码，用户可以借此验证自己的消息确实受到保护。此前，用户需要当面比对这串数字或扫描二维码，但实际完成验证的人很少。自动密钥验证利用密钥透明度的理念持续校验这些密钥，以发现是否有人试图调换公钥。Signal 早在 2016 年就引入了二维码和数字比对的新版安全码设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://signal.org/blog/automatic-key-verification/">Signal >> Blog >> Introducing Automatic Key Verification</a></li>
<li><a href="https://support.signal.org/hc/en-us/articles/10223569377562-Automatic-Key-Verification">Automatic Key Verification – Signal Support</a></li>
<li><a href="https://www.techtimes.com/articles/324045/20260812/signal-launches-automatic-key-verification-stop-server-level-wiretapping.htm">Signal Launches Automatic Key Verification to Stop Server-Level...</a></li>

</ul>
</details>

**标签**: `#security`, `#encryption`, `#Signal`, `#key-verification`, `#messaging`

---

<a id="item-7"></a>
## [发现 KVM guest-to-host 堆破坏漏洞——但他人抢先一步](https://blog.himanshuanand.com/2026/08/i-found-a-kvm-guest-to-host-heap-corruption-bug-and-someone-else-got-there-first/) ⭐️ 8.0/10

博主 Himanshu Anand 发布了一篇文章，描述其独立发现的一个 KVM guest-to-host 堆破坏漏洞。作者承认在文章发布之前，已有其他研究者率先报告了同一个漏洞。 KVM 中的 guest-to-host 堆破坏漏洞是严重的虚拟化安全问题，因为恶意 guest 可能借此逃逸到宿主机，进而危及同主机上的所有虚拟机。对于依赖 KVM 虚拟化的云服务商和企业而言，此类漏洞可能破坏多租户隔离，因此影响重大。 这篇文章似乎重点分析 KVM guest-to-host 边界处的堆内存破坏漏洞的技术细节，尽管作者并非第一个发现该漏洞的人。这篇分析仍有价值，因为它提供了如何识别和理解这类漏洞的技术深度。

rss · Lobste.rs · 8月12日 18:05

**背景**: KVM（Kernel-based Virtual Machine）是 Linux 内核中的一个自由开源虚拟化模块，它使 Linux 内核能够充当 hypervisor，并且需要处理器支持 Intel VT 或 AMD-V 等硬件虚拟化扩展。堆破坏是一类内存安全漏洞，程序在动态分配内存的边界之外写入数据，可能导致崩溃或任意代码执行。在虚拟化环境中，guest-to-host 漏洞尤其危险，因为攻陷 guest 虚拟机的攻击者可能突破 VM 边界，进而访问宿主机，影响所有其他 guest 虚拟机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine">Kernel-based Virtual Machine - Wikipedia</a></li>
<li><a href="https://www.redhat.com/en/topics/virtualization/what-is-KVM">What is KVM?</a></li>
<li><a href="https://www.zdnet.com/article/virtualization-what-are-the-security-risks/">Virtualization : What are the security risks? | ZDNET</a></li>

</ul>
</details>

**标签**: `#KVM`, `#security`, `#virtualization`, `#heap corruption`, `#vulnerability`

---

<a id="item-8"></a>
## [马斯克携 Cursor 团队打造的 24 小时 AI 智能体回归](https://www.ifanr.com/1674851?utm_source=rss&utm_medium=rss&utm_campaign=) ⭐️ 7.0/10

马斯克宣布重返 AI 智能体领域，推出了一款据称由 Cursor 团队打造、可 24 小时不间断工作的 AI 智能体。爱范儿对此进行了报道，但文章提供的技术细节非常有限。 这一发布标志着马斯克借助 Cursor 在 AI 辅助编程方面的专长，重新发力快速发展的 AI 智能体市场。此举可能加剧自主 AI 工具之间的竞争，并改变开发者和企业对全天候自动化的利用方式。 该智能体据称由 Cursor 团队打造，Cursor 是知名 AI 代码编辑器的开发商，近期被 SpaceX 以 600 亿美元收购并归入 SpaceXAI 子公司。原始报道缺乏关于该智能体功能、定价或发布日期的详细信息，因此仍需独立验证。

rss · 爱范儿 · 8月12日 22:55

**背景**: AI 智能体是一种软件系统，能够自主设定步骤、调用工具并完成任务，几乎无需人工干预。Cursor 由 Anysphere 于 2022 年创立，是一款 AI 编程智能体和软件开发环境，到 2026 年初估值达到 293 亿美元，年经常性收入超过 30 亿美元。将 Cursor 纳入马斯克的 SpaceXAI，表明其战略意图是将前沿编程 AI 与马斯克更广泛的 AI 布局相结合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cursor_(code_editor)">Cursor (code editor)</a></li>
<li><a href="https://cursor.com/">Cursor : AI coding agent</a></li>

</ul>
</details>

**标签**: `#AI`, `#Agent`, `#Musk`, `#Cursor`, `#AI tools`

---

<a id="item-9"></a>
## [DeepSeek V4 Pro 实测：能力逼近 Fable 5，暗藏大招](https://www.ifanr.com/1674965?utm_source=rss&utm_medium=rss&utm_campaign=) ⭐️ 7.0/10

一篇 DeepSeek V4 Pro 的实测文章称，这款旗舰模型的能力已接近 Anthropic 的 Claude Fable 5，并揭示了一个未公开的大招。测评强调了 DeepSeek 在 AI Agent 能力上的快速进展。 这表明 DeepSeek 正在缩小与西方顶尖实验室在推理和 Agent 任务上的差距，加剧了 AI 行业的竞争。与 Fable 5 的对标意味着 DeepSeek V4 Pro 可能成为开发者的一个重要的开源权重替代方案。 DeepSeek V4 Pro 是一个混合专家模型，总参数 1.6T，激活参数 49B，支持 1M token 上下文窗口和三种思考模式。评测尚未披露大招的具体细节，但指出 Agent 能力是核心进步。

rss · 爱范儿 · 8月12日 22:55

**背景**: DeepSeek 是一家中国 AI 实验室，以发布开源权重的模型（如 DeepSeek-R1、DeepSeek-V3）而闻名。Anthropic 的 Claude Fable 5 于 2026 年 6 月发布，被描述为几乎所有测试基准上都达到最先进水平，因此成为 DeepSeek 新旗舰型号的天然对标目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_(product)">DeepSeek (product)</a></li>
<li><a href="https://ollama.com/library/deepseek-v4-pro">deepseek - v 4 - pro</a></li>
<li><a href="https://www.anthropic.com/news/claude-fable-5-mythos-5">Claude Fable 5 and Claude Mythos 5 \ Anthropic</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI Model`, `#AI Agent`, `#Review`, `#Machine Learning`

---

<a id="item-10"></a>
## [AI 入口开始收费：豆包抽佣、千问开放平台](http://www.geekpark.net/news/368740) ⭐️ 7.0/10

8 月 10 日，字节跳动旗下豆包 AI 助手开始对经其推荐并在抖音来客成交的酒店订单收取 12%佣金（含 11.4%软件服务费和 0.6%支付手续费）；同日，阿里千问开放平台上線，顺丰、自如、盈米基金等企业以 AI 智能体形式接入。 这标志着 AI 助手从单纯的获客工具，开始转向可变现的“新入口”，探索交易与服务收费模式。中国 AI 助手首次出现具体商业化路径，可能重塑流量定价和平台格局。 豆包的 12%费率介于抖音主站约 8%和携程/美团 15%–20%酒店佣金之间，且官方表示目前无付费推广、不能影响排序。千问则完全不介入交易环节，支付和履约均在合作伙伴自身体系内完成，千问只提供入口和 AI 能力。

rss · 极客公园 · 8月12日 09:14

**背景**: 豆包是字节跳动在 2023 年 8 月推出的 AI 助手，到 2024 年底已成为中国最受欢迎的 AI 聊天机器人，月活约 6000 万；文章引用的最新数据显示其月活已超 3.8 亿。千问（通义千问）是阿里的大语言模型系列，公司通过开放平台将其扩展为生态入口。文章指出，AI 助手一直被行业视为未来“唯一的入口”，但此前变现模式始终不明朗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Doubao">Doubao - Wikipedia</a></li>
<li><a href="https://www.qianwen.com/">qianwen.com - 千问-阿里 AI 助手</a></li>

</ul>
</details>

**标签**: `#AI`, `#Monetization`, `#Business Model`, `#China`, `#AI Assistants`

---

<a id="item-11"></a>
## [Manus 恢复独立、Gemini 月活破 10 亿、林俊旸创办 AI 公司](http://www.geekpark.net/news/368700) ⭐️ 7.0/10

本次快讯涵盖三条重磅 AI 消息：Manus 宣布脱离 Meta、恢复独立公司运营；谷歌 Gemini 应用月活跃用户突破 10 亿；林俊旸正式创办 AI 公司 Pragmatik Labs（语用科技），估值 20 亿美元。 Gemini 成为谷歌最快突破 10 亿用户的产品，显示 AI 助手的消费者普及速度惊人。Manus 恢复独立以及林俊旸获巨额融资的新公司，则体现了 AI 智能体赛道持续的活力与资本热度。 Manus 将删除部分司法辖区用户在 2025 年 12 月 29 日及之后产生的数据，删除时间为北京时间 2026 年 8 月 23 日 08:00 至 8 月 24 日，数据将存储在美国和新加坡。林俊旸的 Pragmatik Labs 由高榕创投和红杉中国共同领投，腾讯和上海未来产业基金支持，估值约 20 亿美元。

rss · 极客公园 · 8月12日 00:35

**背景**: Manus 是一款自主 AI 智能体，能够独立执行研究、数据处理等复杂任务。Gemini 是谷歌推出的跨应用 AI 助手，2025 年 8 月月活跃用户达到 10 亿。林俊旸 1993 年出生，曾是阿里最年轻的 P10 技术专家、千问团队技术负责人，与唐杰、杨植麟、姚顺雨并称“基模四杰”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Manus_AI">Manus AI</a></li>
<li><a href="https://www.ithome.com/0/988/555.htm">从阿里离职五个月后，林俊旸官宣创办 AI 公司语用科技 Pragmatik Labs...</a></li>
<li><a href="https://news.qq.com/rain/a/20260812A05ETI00">林俊旸创办AI公司获腾讯投资_腾讯新闻</a></li>

</ul>
</details>

**标签**: `#AI`, `#Gemini`, `#Manus`, `#tech news`, `#industry`

---

<a id="item-12"></a>
## [Homelab 遭入侵：事后复盘分享安全教训](https://phunky.cafe/my-homelab-got-hacked/) ⭐️ 7.0/10

一位 Homelab 运营者发布了事后复盘文章，分析了其家庭服务器环境是如何被入侵的，包括攻击路径与经验教训。这篇总结作为公开资源分享给自托管社区。 这份事件报告为其他自托管用户提供了安全陷阱和修复策略的具体实例。它强调了 Homelab 是真实的攻击目标，记录事件有助于提升整个社区的安全实践。 该新闻条目仅提供了标题和 Lobsters 讨论帖链接，因此本次分析无法获取入侵的确切技术细节。根据摘要，复盘涵盖了入侵是如何发生的以及从中吸取的教训。

rss · Lobste.rs · 8月12日 15:50

**背景**: Homelab 是一种个人服务器环境，爱好者可在其中自托管应用、试验基础设施并学习运维技能。事后复盘是对事件的结构化记录，涵盖时间线、影响、根本原因和预防措施。由于 Homelab 服务通常暴露在互联网上，它们面临与生产系统类似的威胁，因此安全性至关重要。

**标签**: `#security`, `#homelab`, `#postmortem`, `#self-hosting`, `#incident-response`

---