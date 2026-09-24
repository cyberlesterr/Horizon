---
layout: default
title: "Horizon Summary: 2026-09-24 (ZH)"
date: 2026-09-24
lang: zh
---

> 从 53 条内容中筛选出 9 条重要资讯。

---

1. [OpenAI 发布 GPT-6 Sol 与 Luna，API 价格下调 50%](#item-1) ⭐️ 9.0/10
2. [Anthropic 称 Claude 自主发现类 CRISPR 的酶系统](#item-2) ⭐️ 7.0/10
3. [修复 Portobello 警察局塔钟的详细记录](#item-3) ⭐️ 7.0/10
4. [意大利议会投票通过重建核能监管框架](#item-4) ⭐️ 7.0/10
5. [平头哥发布真武 V900 芯片及全栈算力产品线](#item-5) ⭐️ 7.0/10
6. [Radicle 披露其 P2P 网络协议中的两个严重漏洞](#item-6) ⭐️ 7.0/10
7. [Futhark 博客主张：不要让类型系统去推理别名](#item-7) ⭐️ 7.0/10
8. [APNIC 博客报道：最新 BGP 劫持事件瞄准托管软件供应商](#item-8) ⭐️ 7.0/10
9. [Apache Parquet 引入 ALP 自适应无损浮点编码](#item-9) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6 Sol 与 Luna，API 价格下调 50%](http://www.geekpark.net/news/370829) ⭐️ 9.0/10

9 月 23 日，OpenAI 发布了 GPT-6 系列的两款新模型 GPT-6 Sol 和 GPT-6 Luna，二者采用与旗舰模型 GPT-6 Astra 类似的训练方法，把 Astra 在专业工作、事实性、编码、计算机使用和模型对齐方面的先进能力带入更快、更便宜的模型。两款模型的 API 价格比 GPT-5.6 的促销价再低 50%。 这次发布进一步加剧了前沿智能体模型之间的性价比竞争：在某些智能体基准测试中，OpenAI 以约为 Anthropic Claude Opus 5 每任务成本十分之一的价格提供了接近旗舰级的能力。更便宜、更快的模型降低了开发者构建长时运行自主智能体的门槛，而 token 成本和单任务成本往往正是这类应用能否落地的决定性因素。 在 AutomationBench 的跨应用业务流程测试中，GPT-6 Sol 在 xhigh 强度下表现优于 Claude Opus 5，而每任务成本仅为 Opus 5 的 9%；GPT-6 Luna 在 high 强度下比前代提升 5.4%，每任务成本降低 58%。在评估智能体的 Last Exam 测试中，Sol 在 max effort 状态下得分 56.4%，高于 Claude Opus 5 的最高分，且每任务成本低 60%；OpenAI 还改进了 GPT-6 的提示缓存，默认提供更高的缓存命中率以复用更多上下文，不过官方仍表示 GPT-6 Astra 是整体上最优秀的模型。

rss · 极客公园 · 9月23日 00:39

**背景**: GPT-6 系列是 OpenAI 的旗舰模型家族，其中 Astra 是能力最强、价格最高的档位，因此 Sol 和 Luna 被定位为用类似配方训练出的更廉价版本。AutomationBench 是 Zapier 推出的开放基准测试，用于衡量 AI 智能体能否完成真实业务流程，任务环境模拟了 CRM、日历、收件箱等 47 个 SaaS 工具，并检查智能体是否把环境留在正确的状态。Last Exam（更常被称为 Humanity's Last Exam）是一项高难度专家级题目基准，被广泛用于衡量前沿模型和智能体的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/zapier/AutomationBench">GitHub - zapier/AutomationBench: A benchmark for evaluating ...</a></li>
<li><a href="https://arxiv.org/abs/2604.18934">[2604.18934] AutomationBench - arXiv.org AutomationBench Leaderboard & Scores — September 2026 AutomationBench - arXiv.org AutomationBench: AI Agent Benchmarks | Zapier AutomationBench - Zapier AutomationBench/automationbench at main · zapier ... - GitHub</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-6`, `#AI模型`, `#API定价`, `#行业动态`

---

<a id="item-2"></a>
## [Anthropic 称 Claude 自主发现类 CRISPR 的酶系统](https://www.anthropic.com/news/claude-discovers-novel-enzyme-system) ⭐️ 7.0/10

Anthropic 公布了其首批研究项目之一的早期成果：Claude 自主发现了一个此前未被描述的酶系统，其旁边排列着一串重复 DNA 序列，模式与 CRISPR 相似。据该公司描述，该智能体在排查一个逆转录酶基因附近的原始 DNA 序列时，用“肉眼”识别出了一段串联重复阵列，并将其称为“类 CRISPR”重复阵列。 这一说法是 AI 智能体被归功于真实生物学发现（而非基准测试成绩）的高调案例，也让“AI 在科研中应被赋予多大自主权”的争论更加激烈。如果这类由智能体驱动的基因组挖掘能够被复现，它有望加快寻找新型基因编辑与防御系统的速度，但实际应用效果仍取决于递送等 AI 无法解决的问题。 该酶系统是在噬菌体（感染细菌的病毒）的 DNA 中发现的，其基因旁边是一长段类似 CRISPR 阵列的重复 DNA。评论者强调，这个酶本身其实是已知的类逆转录子（retron）逆转录酶，因此真正新的部分是其周围此前未被描述的基因组排布，而不是一个全新的蛋白家族。

hackernews · raahelb · 9月23日 18:06 · [社区讨论](https://news.ycombinator.com/item?id=49820134)

**背景**: CRISPR-Cas 是细菌和古菌的免疫机制：它们把曾经入侵过的病毒片段作为间隔序列保存在短重复序列之间，由此产生的 CRISPR RNA 会引导 Cas9 等酶去切割匹配的 DNA。逆转录酶则相反，它把 RNA 反向转录成 DNA，而逆转录子（retron）是细菌中把逆转录酶与非编码 RNA 配对的一类遗传元件。Anthropic 的说法是，一个只收到高层级提示的 AI 智能体自主挖掘了原始序列数据，并标记出把这类酶与类 CRISPR 重复序列联系起来的新排布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-discovers-novel-enzyme-system">Claude discovers a novel enzyme system with CRISPR-like repeats</a></li>
<li><a href="https://thenextweb.com/news/anthropic-claude-enzyme-system-crispr-like-repeats">Anthropic says Claude found a new enzyme system with CRISPR-like repeats</a></li>
<li><a href="https://en.wikipedia.org/wiki/CRISPR">CRISPR - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者总体上既感兴趣又持怀疑态度：有人指出治疗上的主要瓶颈是 CRISPR 的递送而非靶向效率，因此更克制的表述应是“Claude 识别出了已知逆转录酶周围一段此前未被描述的基因组排布”。也有人乐于通过智能体自己兴奋的对话记录来重温这一发现过程；部分人则质疑 Anthropic 究竟想创造人机协作的未来，还是完全自主发现的未来；还有评论者坦言不理解 LLM 为何能对生物化学进行推理。

**标签**: `#AI`, `#CRISPR`, `#genomics`, `#Anthropic`, `#scientific discovery`

---

<a id="item-3"></a>
## [修复 Portobello 警察局塔钟的详细记录](https://pointinthecloud.com/2026-04-11-211700.html) ⭐️ 7.0/10

pointinthecloud.com 上发布的一篇详细文章记录了苏格兰 Portobello 警察局大楼内钟表的维修与修复过程，该建筑最初是旧市政厅和公共图书馆，后来才用作警察局。这篇文章登上了 Hacker News 首页，获得 369 分和 84 条评论。 这篇文章说明小众的硬件修复工作同样能引起工程界的广泛兴趣，让 Hacker News 社区围绕实际维护改进展开讨论。它同时凸显了保存传统机械钟表机制的价值，而这类工作依赖于数量稀少、日益难以寻觅的专业钟表修复师和机械加工技艺。 这座钟是一台驱动三面外部表盘的机械塔钟（turret clock），需要攀爬布满灰尘的阁楼中木梯和陡峭台阶才能接近，据说至今仍靠手工上弦。这类由摆锤驱动的机械机芯依赖齿轮、重锤和擒纵机构而非电子元件，因此修复者要处理的是磨损的擒纵轮、灰尘和润滑问题，而不是电路。

hackernews · avidly · 9月23日 15:18 · [社区讨论](https://news.ycombinator.com/item?id=49817469)

**背景**: 塔钟（turret clock，又称 tower clock）是安装在钟楼、教堂、市政厅等公共建筑中的大型机械钟，通常由一套机芯驱动多个外部表盘。机芯指真正负责计时的那套齿轮、弹簧、重锤和擒纵机构，而摆锤和指针属于独立部件。由于这类钟往往有数百年历史、使用了早已停产的零件，修复时通常需要定制加工替换件并仰赖专门技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Portobello_Police_Station">Portobello Police Station - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Turret_clock">Turret clock - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Movement_(clockwork)">Movement (clockwork) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论区氛围热情且具建设性：一位读者建议在木梯踏板上加装自粘式砂纸状防滑条，作为成本低廉的安全改进；另一位提议在不改动钟体机构的前提下，安装一台低成本的 PoE 网络摄像机对准齿轮机构，实现远程监控。一位当地读者提到在 Hacker News 上看到父亲曾经工作的地方令他倍感亲切，也有人开玩笑说自己把“Portobello”误认成了蘑菇。

**标签**: `#clock-repair`, `#restoration`, `#hardware`, `#DIY`, `#hacker-news`

---

<a id="item-4"></a>
## [意大利议会投票通过重建核能监管框架](https://apnews.com/article/italy-nuclear-chernobyl-4891b6b7c7791ae84db6b0bf0f7cf567) ⭐️ 7.0/10

意大利议会投票通过了一项立法，建立了允许该国重新发展核能的监管框架，从而推翻了 1986 年切尔诺贝利事故后所通过的核能禁令。政府并不打算重启过去那种大型传统反应堆，而是把重点放在小型模块化反应堆（SMR）以及其他先进技术上。 对于一个实际上已数十年无核能的国家而言，这标志着国家能源政策的重大逆转，也显示出欧洲对 SMR 作为一种灵活、低碳电力来源的兴趣日益增长。一个七国集团经济体开辟新的监管路径，可能会鼓励投资，并加速先进反应堆设计方面的跨境合作。 该立法并未授权建设任何反应堆，仅是建立了未来项目能够被提出、评估和批准所需的监管基础。SMR 通常被定义为单模块电功率低于 300 MWe 的反应堆，而意大利尚未解决在日益以太阳能为主的电网中，这类电厂将如何融资和运营的问题。

hackernews · geox · 9月23日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=49819221)

**背景**: 意大利是最早采用商业核电的国家之一，但在 1986 年切尔诺贝利事故后举行的公投之后，关闭了本国核电厂并禁止了该技术。小型模块化反应堆是一类新兴的核裂变反应堆，设计上采用工厂预制模块化建造并运输到现场安装，相比大型轻水反应堆，有望缩短建设周期并具备非能动安全特性。它们已引起谷歌和微软等科技公司的浓厚兴趣，这些公司希望为其数据中心获得可靠的无碳电力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Small_Modular_Reactors_(SMRs)">Small Modular Reactors (SMRs)</a></li>
<li><a href="https://www.iaea.org/topics/small-modular-reactors">Small modular reactors ( SMR ) | IAEA</a></li>
<li><a href="https://www.nuscalepower.com/">NuScale Power | Small Modular Reactor ( SMR ) Nuclear Technology</a></li>

</ul>
</details>

**社区讨论**: 评论者参与度很高但意见分化：一些人欢迎这一逆转，认为这是对切尔诺贝利时代“凭直觉”所做决定的一次理性修正；另一些人则怀疑 SMR 项目在无补贴情况下能否实现净盈利，或是否会有投资者愿意出手。还有人担心该议题被政治化，以及在以太阳能为主的电网中反应堆将如何融资，同时也有人期待北约在能源方面加强合作。

**标签**: `#nuclear-energy`, `#energy-policy`, `#SMR`, `#Italy`, `#regulation`

---

<a id="item-5"></a>
## [平头哥发布真武 V900 芯片及全栈算力产品线](http://www.geekpark.net/news/370864) ⭐️ 7.0/10

在 9 月 22 日举行的 2026 杭州云栖大会上，阿里巴巴旗下平头哥半导体发布了新一代训推一体 AI 芯片真武 V900，并同时推出 ICN Switch 互联芯片、磐脉智能网卡、镇岳 SSD 主控、倚天 CPU 路线图，以及实现算、存、网全栈协同的超节点服务器。真武 V900 搭载 216GB 显存、片间互联带宽达 1200GB/s，单芯片性能是上一代真武 M890 的 3 倍，并原生支持 FP8 和 FP4 精度。 这次发布标志着 AI 硬件竞争从单颗芯片的指标比拼，转向面向 Agentic 推理时代的系统级协同设计：算力、互联、网络、存储与 CPU 需整体配合，因为在模型被拆到数十上百张卡后，芯片间的通信速度才真正决定吞吐表现。这同时也强化了中国自研 AI 芯片栈，使阿里能够主要依靠自研芯片与超节点架构来支撑万亿参数级模型的训练与推理。 平头哥称，仅需十多张真武 V900 即可部署一个万亿参数规模的大模型；V900 计划于 2027 年第一季度量产销售，真武 J900 则将于 2028 年第三季度推出，大致维持每年一代的迭代节奏，可与英伟达从 H 系列到 B 系列的切换周期类比。通过自研 ICN Switch 互联芯片连接后，V900 超节点具备原生内存语义和内存统一编址能力，可实现千卡全带宽高速互联；而此前的 M890 超节点已跑通 Qwen3.8、Kimi K3 等超 2 万亿参数规模模型。

rss · 极客公园 · 9月23日 05:55

**背景**: 如今万亿参数级大模型普遍采用混合专家（MoE）架构，把模型拆分成大量子专家，每个 Token 只调用其中一部分，从而在扩大模型容量的同时压低单次实际参与计算的参数量。这一架构虽缓解了计算量，却把模型分散到几十甚至上百张芯片上，使芯片间的数据交换速度，而非单芯片算力，成为训练和推理的瓶颈。正因如此，业界转向「超节点」形态：把 16 张以上加速卡通过超高带宽域互联，让它们像一颗「超级芯片」一样协同工作。这一概念由英伟达基于 NVLink 的设计带火，如今也成为平头哥路线图的核心。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sohu.com/a/1079601164_121019331">平头哥半导体发布AI芯片真武V900，号称目前算力性能最强中国自研AI芯...</a></li>
<li><a href="https://www.yingzheng.com/article/alibaba-pingtouhe-zhenwu-v900-ai-chip-launch-2026">阿里平头哥发布真武V900：性能三倍跃升，量产等到2027年</a></li>
<li><a href="https://developer.aliyun.com/article/1686026">深度长文！详解阿里云磐久AL128超节点服务器及互连架构</a></li>

</ul>
</details>

**标签**: `#AI Hardware`, `#Chip Design`, `#AI Infrastructure`, `#Data Center`, `#Alibaba T-Head`

---

<a id="item-6"></a>
## [Radicle 披露其 P2P 网络协议中的两个严重漏洞](https://radicle.dev/2026/09/23/disclosure-of-vulnerability-in-network-protocol.html) ⭐️ 7.0/10

Radicle 于 2026 年 9 月 23 日发布安全披露公告，公布了其节点网络协议中存在的两个严重漏洞，并建议用户停止通过其网络使用私有仓库。根据对该披露的报道，节点之间的流量未加密传输，这意味着任何能够监听到网络链路的人都可以读取传输中的数据。 Radicle 一直以去中心化、自主可控的代码托管替代方案为卖点，而这一漏洞会让私有仓库数据在传输过程中暴露，直接冲击了用户离开 GitHub 等中心化平台时所依赖的核心隐私承诺。该披露影响所有运行 Radicle 节点或在网络上托管私有代码的用户，在问题修复之前，还可能削弱人们对 P2P 代码协作整体模式的信任。 该披露描述了两个严重漏洞，并特别警告不要通过 Radicle 网络使用私有仓库，因为节点间流量缺乏加密，任何能监听网络链路的人都能读取其中的内容。在目前可获得的材料中，公告没有提供更多技术细节，所链接的讨论页面也尚无公开评论。

rss · Lobste.rs · 9月23日 14:34

**背景**: Radicle 是一个基于 Git 构建的开源点对点代码协作栈，定位为“主权锻造厂”（sovereign forge），即没有任何单一实体控制整个网络。其网络层通常被称为 Radicle Link，是一种 gossip 协议，消息在节点之间转发以构建用于仓库发现与复制的路由表。Radicle 采用本地优先的数据存储方式，因此理解节点如何在网络上交换数据，是评估此次披露影响的关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://radicle.dev/2026/09/23/disclosure-of-vulnerability-in-network-protocol">Disclosure of Vulnerability in the Network Protocol</a></li>
<li><a href="https://runtimewire.com/article/radicle-network-protocol-vulnerabilities-private-repositories">Radicle tells users to stop using private repositories over its network</a></li>
<li><a href="https://radicle.dev/guides/protocol">Radicle Protocol Guide</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#radicle`, `#p2p`, `#network-protocol`

---

<a id="item-7"></a>
## [Futhark 博客主张：不要让类型系统去推理别名](https://futhark-lang.org/blog/2026-09-22-aliasing.html) ⭐️ 7.0/10

Futhark 语言团队于 2026 年 9 月 22 日发表了一篇题为《Do not let your type system reason about aliasing》的博客文章，主张编程语言不应把类型系统当作推理别名（aliasing）的机制。该文随后被提交到 Lobsters，成为编程语言社区的一个讨论话题。 这篇文章触及语言设计的核心取舍：如果别名信息不进入类型系统，那么内存安全以及原地更新、并行化等编译优化所需的保证，就必须由其他机制来提供，例如效果系统、独立的所有权分析或运行时检查。对于正在设计编程语言、类型系统或编译器的开发者来说，这是对“把越来越多别名推理塞进类型里”这一趋势的一种重要反思。 这是一篇设计观点与经验分享类文章，而不是新版本、新工具或性能评测，因此应当把它当作一种论证来看待，而非可量化的成果。所提供的材料仅有博客链接和 Lobsters 讨论链接，没有评论正文，所以无法在此评估社区回应的具体内容。

rss · Lobste.rs · 9月23日 14:07

**背景**: 别名（aliasing）指的是同一块内存位置可以通过多个名字访问，例如两个指向同一对象的指针，这会让优化和对可变状态的推理变得复杂。过去十年间，用于追踪别名的类型系统——别名类型（alias types）、所有权（ownership）、区域（region）与权限（permission）系统——逐渐进入主流语言和工具，最典型的应用是通过借用检查来保证并发安全。Futhark 是一门小型、纯函数式、面向数据并行的数组语言，属于 ML 家族，由哥本哈根大学 DIKU 院系在 HIPERFIT 项目下开发，可把高层函数式数组代码编译为在 GPU 和多核 CPU 上高效运行的代码。由于这类编译高度依赖判断数组何时可以原地更新，别名问题对 Futhark 团队而言具有很强的工程现实意义。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Futhark_(programming_language)">Futhark (programming language)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Aliasing_(computing)">Aliasing (computing) - Wikipedia</a></li>
<li><a href="https://link.springer.com/chapter/10.1007/978-3-642-36946-9_21">A Retrospective on Aliasing Type Systems: 2012-2022 | Springer Nature Link</a></li>

</ul>
</details>

**标签**: `#programming languages`, `#type systems`, `#aliasing`, `#language design`, `#Futhark`

---

<a id="item-8"></a>
## [APNIC 博客报道：最新 BGP 劫持事件瞄准托管软件供应商](https://blog.apnic.net/2026/09/22/latest-bgp-hijack-targets-hosting-software-vendor/) ⭐️ 7.0/10

APNIC 博客发布了一篇报道，描述了一起最新的 BGP 劫持事件：与该托管软件供应商相关的路由被非法宣告，导致本应到达该厂商的流量被重定向。由于提交内容仅包含标题和链接，报道中涉及的具体受害方、被劫持的 IP 前缀以及劫持持续时间在此材料中并未展开说明。 BGP 劫持能够悄无声息地重定向或截获流量、造成服务中断，并侵蚀人们对互联网路由体系的信任；而托管或软件供应商之所以是尤为敏感的靶标，是因为其基础设施和下游客户都会受到波及。该事件再次表明，尽管 RPKI 等缓解手段日益普及，路由安全依然是长期存在、尚未解决的操作性风险。 BGP 在设计之初并未内置认证机制，因此某个网络可以宣告自己并不合法拥有的前缀，并被对等方接受；常见的应对措施包括通过 ROA 进行 RPKI 源认证、基于 IRR 的前缀过滤、最大前缀数限制以及持续的路由监控。由于该新闻条目没有提供技术分析，此次劫持的范围、涉事自治系统编号，以及流量究竟是被真正截获还是仅仅被错误路由，仅凭该来源尚无法确定。

rss · Lobste.rs · 9月23日 11:55

**背景**: 边界网关协议（BGP）是各自治系统用来交换“自己能到达哪些 IP 前缀”这一信息的路由协议，实际上把全球互联网缝合在一起。BGP 劫持（又称前缀劫持或路由劫持）是指通过污染这些路由表，非法接管成组的 IP 地址，使流量被送往错误的网络。APNIC 是负责为亚太地区分配并登记 IP 地址与自治系统编号的区域互联网注册管理机构，其博客经常讨论与网络运营者相关的运营和安全议题。该条目附有一个 Lobsters 讨论帖链接，但本次提交并未提供任何评论内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/BGP_hijacking">BGP hijacking - Wikipedia</a></li>
<li><a href="https://www.apnic.net/">APNIC</a></li>
<li><a href="https://www.thousandeyes.com/learning/glossary/bgp-route-hijacking">What is BGP Hijacking? Internet & IP Route Hijacking - ThousandEyes</a></li>

</ul>
</details>

**标签**: `#BGP`, `#BGP hijacking`, `#network security`, `#routing`, `#APNIC`

---

<a id="item-9"></a>
## [Apache Parquet 引入 ALP 自适应无损浮点编码](https://parquet.apache.org/blog/2026/09/22/alp-adaptive-lossless-floating-point-encoding-in-apache-parquet/) ⭐️ 7.0/10

Apache Parquet 项目发布了一篇博客，讲解面向该列式文件格式的自适应无损浮点编码（ALP），说明如何对 IEEE 754 浮点列进行无损压缩，而不是按原始 8 字节数值直接存储。文章将 ALP 定位为一种专门针对现有 Parquet 编码（字典、delta、RLE、位打包）处理效果不佳的数据类型的编码方案。 浮点列在分析型负载中非常常见，但历来压缩效果很差，会推高基于 Parquet 构建的数据湖与查询引擎的存储成本和 I/O 开销。一种能显著压缩 double 列的无损编码可以减少扫描字节数、加快查询速度，并降低 Spark、DuckDB、Trino 以及 pandas/pyarrow 等读取 Parquet 的系统的云存储账单。 ALP 的核心思路是：真实数据集中的大多数 double 最初都源自十进制小数。它寻找一对指数/因子参数，把数值精确映射为整数，再用标准整数编码进行压缩，并通过记录例外值来校验正确性，从而保证转换严格无损。当数据并非十进制形态时，该方案会自适应切换（例如使用 ALP-RD 这种借助高位字典的“真实 double”变体）或回退到其他编码；对于完全随机、不可压缩的 double，额外开销反而可能增加。

rss · Lobste.rs · 9月23日 19:23

**背景**: Apache Parquet 是 Apache Hadoop 生态中免费开源的列式存储格式，灵感来自 Google 的 Dremel，常与 ORC 相提并论；它按列分别存储，并对每一列单独施加编码与压缩，以便高效处理批量复杂数据。ALP（Adaptive Lossless floating-Point Compression，自适应无损浮点压缩）由 CWI 的研究人员在 2023 年 SIGMOD 论文中提出，在早期 PseudoDecimals 思路的基础上做了大幅增强，并在 cwida/ALP 仓库中开源了实现。Parquet 格式规范是带版本管理的，因此新的编码必须先在写入端与读取端各库之间达成一致并完成实现，才能真正被广泛使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/cwida/ALP">cwida/ALP - Adaptive Lossless Floating-Point Compression - GitHub</a></li>
<li><a href="https://dl.acm.org/doi/abs/10.1145/3626717">ALP: Adaptive Lossless floating-Point Compression - ACM Digital Library</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apache_Parquet">Apache Parquet</a></li>

</ul>
</details>

**标签**: `#Apache Parquet`, `#floating-point compression`, `#lossless encoding`, `#columnar storage`, `#data compression`

---