---
layout: default
title: "Horizon Summary: 2026-07-04 (ZH)"
date: 2026-07-04
lang: zh
---

> 从 75 条内容中筛选出 13 条重要资讯。

---

1. [论文称市场竞争力等价于 P≠NP](#item-1) ⭐️ 9.0/10
2. [Guix 的 substitute 和 pull 命令存在严重漏洞](#item-2) ⭐️ 9.0/10
3. [LongCat-2.0：基于 AI ASIC 训练的 1.6 万亿 MoE 模型](#item-3) ⭐️ 9.0/10
4. [欧洲议会间谍调查成员遭飞马间谍软件攻击](#item-4) ⭐️ 8.0/10
5. [Current AI 发布开源 AI 差距地图](#item-5) ⭐️ 8.0/10
6. [课程创作者报告因 AI 导致销量下降 50%以上](#item-6) ⭐️ 8.0/10
7. [Clickhouse 正在赢得可观测性之战](#item-7) ⭐️ 8.0/10
8. [KDE Plasma 沙箱逃逸漏洞：任意代码执行](#item-8) ⭐️ 8.0/10
9. [本地运行 SOTA 大模型指南](#item-9) ⭐️ 7.0/10
10. [工厂不过是房间：一种令人耳目一新的视角](#item-10) ⭐️ 7.0/10
11. [硅基流动赴港 IPO，毛利率为负](#item-11) ⭐️ 7.0/10
12. [理想汽车重组：产品团队并入研发](#item-12) ⭐️ 7.0/10
13. [生数科技发布 Vidu S1 实时交互模型](#item-13) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [论文称市场竞争力等价于 P≠NP](https://arxiv.org/abs/2602.20415) ⭐️ 9.0/10

arXiv 上的一篇新论文（2602.20415）声称，市场具有竞争力当且仅当 P≠NP，从而在经济市场理论与计算机科学中的基本 P vs NP 问题之间建立了直接联系。 如果正确，这一结果将连接经济学和计算复杂性两大领域，可能重塑我们对市场效率和算法交易极限的理解。它还表明，证明 P≠NP（或 P=NP）可能具有具体的经济学意义。 该论文发布在 arXiv 上，尚未经过同行评审。这一主张非常新颖，但需要严格验证；如果存在缺陷，可能是对经济背景下复杂性类别的误解。

rss · Lobste.rs · 7月3日 15:42

**背景**: P vs NP 问题询问的是，每个能快速验证解的问题是否也能快速求解。它是七个千禧年大奖难题之一，悬赏 100 万美元。经济学中的市场竞争力通常与价格发现和资源配置的效率有关，这些可以建模为计算问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/P_vs_NP_problem">P vs NP problem</a></li>
<li><a href="https://en.wikipedia.org/wiki/P_versus_NP_problem">P versus NP problem - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Lobsters 社区讨论（文章中有链接）可能包含对该论文有效性的质疑和辩论，因为其主张很大胆。输入中未提供具体评论。

**标签**: `#P vs NP`, `#computational complexity`, `#economics`, `#market theory`, `#theoretical computer science`

---

<a id="item-2"></a>
## [Guix 的 substitute 和 pull 命令存在严重漏洞](https://guix.gnu.org/en/blog/2026/guix-substitute-pull-vulnerabilities/) ⭐️ 9.0/10

GNU Guix 项目宣布 'guix substitute' 和 'guix pull' 命令存在严重安全漏洞，攻击者可能利用这些漏洞执行任意代码或破坏系统。用户应立即进行修补。 这些漏洞影响所有用户用于包管理和系统更新的核心 Guix 命令，可能导致远程代码执行或供应链攻击。立即修补对于维护系统完整性至关重要。 这些漏洞已在官方 Guix 博客上披露，Lobsters 讨论提供了技术分析和社区影响评估。预计后续将公布具体技术细节和补丁。

rss · Lobste.rs · 7月3日 06:45

**背景**: Guix 是 GNU/Linux 系统的函数式包管理器，支持透明的源码/二进制部署。'guix substitute' 命令从远程服务器下载预构建的二进制文件以加速安装，而 'guix pull' 用于更新 Guix 发行版和工具。这两个命令都是 Guix 运行的基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://guix.gnu.org/manual/stable/en/html_node/Substitutes.html">Substitutes (GNU Guix Reference Manual)</a></li>
<li><a href="https://guix.gnu.org/manual/devel/en/html_node/Invoking-guix-pull.html">Invoking guix pull (GNU Guix Reference Manual)</a></li>

</ul>
</details>

**社区讨论**: Lobsters 讨论包括对漏洞及其潜在影响的技术分析，一些评论者对其严重性表示担忧，并敦促立即采取行动。大家一致认为需要及时修补。

**标签**: `#security`, `#guix`, `#vulnerability`, `#package management`

---

<a id="item-3"></a>
## [LongCat-2.0：基于 AI ASIC 训练的 1.6 万亿 MoE 模型](https://www.reddit.com/r/LocalLLaMA/comments/1umo8zu/longcat_2_model_weights_have_been_published/) ⭐️ 9.0/10

LongCat-2.0 已发布并开放权重，这是一个拥有 1.6 万亿总参数、每个 token 约激活 480 亿参数的混合专家（MoE）语言模型。该模型在超过 35 万亿个 token 上训练，使用了数万个 AI ASIC 超级计算集群，展示了在替代硬件上进行前沿规模训练的能力。 此次发布证明，大规模前沿 AI 模型可以在非 GPU 硬件（AI ASIC）上训练，可能减少对 NVIDIA GPU 的依赖。同时，它推进了开源 MoE 模型的发展，拥有巨大的参数量，使更广泛的研究和部署成为可能。 该模型采用 MoE 架构，总参数达 1.6 万亿，但每个 token 仅激活约 480 亿参数，推理效率高。训练在美团 AI ASIC 超级计算集群（可能为华为 CloudMatrix-384）上进行，未出现回滚或不可恢复的损失尖峰。

reddit · r/LocalLLaMA · RhubarbSimilar1683 · 7月3日 19:49

**背景**: 混合专家（MoE）是一种神经网络架构，将模型划分为多个“专家”，每个输入仅激活其中一部分，从而在较低计算成本下实现大总参数量。AI ASIC 是为 AI 工作负载设计的定制芯片，是 GPU 的替代方案。该模型由美团（一家中国科技公司）开发，凸显了国产硬件的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://quasa.io/media/meituan-trains-the-first-frontier-scale-llm-entirely-on-chinese-domestic-chips-longcat-2-0">Meituan Trains the First Frontier-Scale LLM Entirely on Chinese...</a></li>
<li><a href="https://www.scmp.com/tech/tech-trends/article/3358854/china-debuts-biggest-ai-model-trained-local-chips-meituan-releases-longcat-20">Meituan claims China’s biggest AI model trained on local chips</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区评论有限，包括对模型名称的玩笑以及请求量化版本。一条评论强调了在替代硬件上训练的重要性，指出该模型致力于国产芯片。

**标签**: `#LLM`, `#MoE`, `#AI ASIC`, `#large-scale training`, `#open weights`

---

<a id="item-4"></a>
## [欧洲议会间谍调查成员遭飞马间谍软件攻击](https://citizenlab.ca/research/member-of-committee-investigating-spyware-hacked-with-pegasus/) ⭐️ 8.0/10

公民实验室确认，一名参与调查间谍软件的欧洲议会委员会成员在 2022 年和 2023 年多次被飞马间谍软件成功感染。 这一事件表明，即使是调查间谍软件的欧盟高级官员也无法免受监控，凸显了针对民主机构的跨境间谍软件行动的规模和复杂性。 2022 年 10 月的首次感染与针对欧洲流亡记者的飞马行动重叠，表明一个有权在多个欧洲国家进行监控的客户参与了此事。感染同时泄露了个人医疗信息和政府机密文件。

hackernews · Lobste.rs · 7月3日 20:38 · [社区讨论](https://news.ycombinator.com/item?id=48779683)

**背景**: 飞马是由以色列 NSO 集团开发的强大间谍软件，能够远程入侵移动设备。它仅出售给政府客户，并被广泛用于监控记者、活动家和政治家。公民实验室是研究数字威胁对人权影响的领先研究机构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pegasus_(spyware)">Pegasus (spyware)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Citizen_Lab">Citizen Lab</a></li>
<li><a href="https://citizenlab.ca/">The Citizen Lab - The Citizen Lab</a></li>

</ul>
</details>

**社区讨论**: 评论者提到希腊持续的间谍软件丑闻，认为此次攻击可能与国内监控有关，而非直接针对欧洲议会。其他人指出，多个欧盟成员国滥用飞马，导致以色列公司已与部分国家断绝关系。

**标签**: `#cybersecurity`, `#spyware`, `#Pegasus`, `#surveillance`, `#European Parliament`

---

<a id="item-5"></a>
## [Current AI 发布开源 AI 差距地图](https://simonwillison.net/2026/Jul/3/open-source-ai-gap-map/#atom-everything) ⭐️ 8.0/10

Current AI（一家于 2025 年 2 月在巴黎 AI 行动峰会上成立的非营利组织）发布了开源 AI 差距地图 v0.1，索引了 421 个产品，涵盖软件、模型、数据集和硬件，以可视化开源 AI 生态系统。 该地图提供了开源 AI 领域的结构化全面概览，有助于识别投资和开发方面的差距与机遇，对于指导该非营利组织已承诺的 4 亿美元资金至关重要。 该地图详细列出了来自 228 个组织的 266 个软件工具、85 个模型、50 个数据集和 20 个硬件项目，底层数据以 MIT 许可证发布在 GitHub 上，包括 1,184 个 YAML 文件，并追踪了 16,185 个 GitHub 仓库。

rss · Simon Willison · 7月3日 22:04

**背景**: Current AI 是一个全球性的非营利合作伙伴关系，已承诺投入 4 亿美元，旨在构建 AI 的公共选项。差距地图旨在系统性地编目开源 AI 生态系统，将产品按三个层次（模型组件、产品/用户体验和基础设施）分为 14 个类别。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jul/3/open-source-ai-gap-map/">Open Source AI Gap Map | Simon Willison’s Weblog</a></li>

</ul>
</details>

**标签**: `#open source`, `#AI`, `#ecosystem mapping`, `#non-profit`, `#Current AI`

---

<a id="item-6"></a>
## [课程创作者报告因 AI 导致销量下降 50%以上](https://simonwillison.net/2026/Jul/3/josh-w-comeau/#atom-everything) ⭐️ 8.0/10

Josh W. Comeau 报告称，他的新课程《Whimsical Animations》预计销量仅为典型发布时的三分之一，现有课程销量较去年下降超过 50%，他将此归因于 AI 引发的开发者就业不确定性以及 LLM 取代付费教育内容。 这提供了来自知名课程创作者的一手具体数据，显示 AI 如何颠覆开发者教育市场，且得到多位创作者的证实，预示着可能重塑开发者学习方式和内容创作者变现模式的更广泛趋势。 Comeau 的第三门课程《Whimsical Animations》是一门交互式在线课程，专注于培养实用动画技能；他指出，LLM 现在可以提供个性化辅导，降低了购买付费课程的动机，同时未经同意或补偿地消耗创作者的内容。

rss · Simon Willison · 7月3日 21:25

**背景**: Josh W. Comeau 是一位知名的前端开发者和教育者，此前曾创建过 CSS 和 React 方面的热门课程。像 GPT-4 这样的大型语言模型（LLM）的兴起，使得能够回答问题并解释概念的个性化辅导系统成为可能，这可能与结构化课程形成竞争。许多开发者还担心 AI 会取代软件工程岗位，导致他们减少学习新技能的投资。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://whimsy.joshwcomeau.com/">Whimsical Animations, a new course from Josh W. Comeau</a></li>
<li><a href="https://courseflix.net/course/whimsical-animations">Whimsical Animations — Online Course by Josh Comeau</a></li>
<li><a href="https://coderprog.com/whimsical-animations-josh-comeau/">Whimsical Animations – CoderProg</a></li>

</ul>
</details>

**标签**: `#AI impact`, `#developer education`, `#online courses`, `#job market`, `#LLMs`

---

<a id="item-7"></a>
## [Clickhouse 正在赢得可观测性之战](https://matduggan.com/clickhouse-is-winning-the-observability-wars/) ⭐️ 8.0/10

一篇分析文章指出，ClickHouse 已成为可观测性工作负载的领先数据库，在性能和采用率上超越了竞争对手。 这一趋势标志着基础设施监控的转变，因为 ClickHouse 的列式存储和高压缩率能够实现更快的查询以及更低的日志、指标和追踪成本。 ClickHouse 的查询功能和高压缩率使得越来越多的用户将其用于存储可观测性数据，官方博客中关于构建可观测性解决方案的文章也强调了这一点。

rss · Lobste.rs · 7月3日 05:25

**背景**: 可观测性是指通过外部输出来理解系统内部状态的能力，依赖于日志、指标和追踪。传统数据库通常难以处理可观测性数据的体量和多样性，从而推动了像 ClickHouse 这样的专用解决方案的兴起。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://clickhouse.com/blog/storing-log-data-in-clickhouse-fluent-bit-vector-open-telemetry">Building an Observability Solution with ClickHouse - Part 1 -</a></li>
<li><a href="https://clickhouse.com/blog/storing-traces-and-spans-open-telemetry-in-clickhouse">Building an Observability Solution with ClickHouse - Part 2 -</a></li>
<li><a href="https://www.ibm.com/think/topics/observability">What is observability? - IBM</a></li>

</ul>
</details>

**标签**: `#Clickhouse`, `#observability`, `#databases`, `#infrastructure`, `#monitoring`

---

<a id="item-8"></a>
## [KDE Plasma 沙箱逃逸漏洞：任意代码执行](https://blog.kimiblock.top/2026/07/01/arbitrary-code-execution-in-kde-plasma/) ⭐️ 8.0/10

一篇博客文章披露了 KDE Plasma（流行的 Linux 桌面环境）中的任意代码执行漏洞，这些漏洞允许逃逸沙箱。 该漏洞可能允许攻击者逃逸沙箱限制并获得对用户系统的完全访问权限，影响众多依赖 KDE Plasma 的 Linux 用户。 具体技术细节尚未完全披露，但该漏洞涉及打破 KDE Plasma 中的沙箱保护，可能导致任意代码执行。

rss · Lobste.rs · 7月3日 02:39

**背景**: KDE Plasma 是 Linux 及其他类 Unix 系统的自由开源桌面环境。沙箱是一种安全机制，通过隔离应用程序来限制漏洞利用造成的损害。任意代码执行漏洞允许攻击者在目标系统上运行恶意代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kde.org/plasma-desktop/">Plasma - KDE Community</a></li>
<li><a href="https://en.wikipedia.org/wiki/Arbitrary_code_execution">Arbitrary code execution - Wikipedia</a></li>
<li><a href="https://noc.org/help/docs/what-is-an-arbitrary-code-execution-vulnerability/">What is an Arbitrary Code Execution Vulnerability? - NOC Help</a></li>

</ul>
</details>

**社区讨论**: Lobsters 社区的讨论可能包含技术分析和对影响的担忧，但未提供具体评论。

**标签**: `#security`, `#KDE`, `#vulnerability`, `#sandbox`, `#desktop`

---

<a id="item-9"></a>
## [本地运行 SOTA 大模型指南](https://github.com/jamesob/local-llm) ⭐️ 7.0/10

Jamesob 在 GitHub 上发布了一份实用指南，详细介绍了如何在本地硬件上构建和运行最先进的大语言模型，包括具体的硬件建议和成本估算。 该指南帮助开发者和爱好者了解在本地运行高性能大语言模型的可行性和成本，这对于隐私保护、离线使用以及避免云 API 费用至关重要。 该指南的顶级配置估计花费 4 万至 5.5 万美元，使用四块单价 1.2 万美元的 GPU，并依赖量化技术来降低内存需求。

hackernews · livestyle · 7月3日 15:03 · [社区讨论](https://news.ycombinator.com/item?id=48775921)

**背景**: 在本地运行大语言模型需要大量显存，通常超出消费级硬件的限制。量化技术通过降低模型精度（例如从 FP16 降到 INT8）使模型适配可用内存，但可能降低输出质量。像 Llama 和 DeepSeek 这样的开放权重模型允许本地部署，但要达到接近前沿的性能需要昂贵的多 GPU 配置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/aanoskov/local_llms_quantized">GitHub - aanoskov/ local _llms_quantized: This repository demonstrates...</a></li>
<li><a href="https://e-verse.com/learn/run-your-llm-locally-state-of-the-art-2025/">Ultimate Guide: Run DeepSeek, Llama & LLMs Locally in 2025 | e-verse</a></li>
<li><a href="https://www.ibm.com/think/topics/quantization">What is Quantization? | IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者就本地配置的性价比展开辩论：有人指出 4 万美元可以支付 16.8 年的 Claude Opus 订阅费，而另一些人则建议中端方案，如 2 块 RTX 3090 或配备 48GB 统一内存的 M5 MacBook Pro。也有人对 4 万美元配置能媲美 Claude Opus 的说法表示怀疑，因为类似模型需要 40 万美元的硬件。

**标签**: `#LLM`, `#local deployment`, `#hardware`, `#deep learning`, `#open source`

---

<a id="item-10"></a>
## [工厂不过是房间：一种令人耳目一新的视角](https://interconnected.org/home/2026/07/03/factories) ⭐️ 7.0/10

一篇随笔提出，工厂本质上只是人们制造物品的房间，挑战了关于工厂复杂性的假设，鼓励以更简单、更易接近的视角看待制造业。 这种视角可能通过降低感知到的入门门槛来民主化制造业，激励更多个人和小团队开始生产。它也促使我们重新思考如何设计和优化生产空间。 这篇随笔及其社区讨论（178 分，73 条评论）包含了来自实际经营过小工厂的从业者的见解，既强调了亲手制造的乐趣，也指出了挑战。评论者指出，虽然“房间”概念令人解放，但劳动保护、业务持续性等现实因素使情况复杂化。

hackernews · arbesman · 7月3日 15:13 · [社区讨论](https://news.ycombinator.com/item?id=48776035)

**背景**: 这篇随笔建立在揭开工业生产神秘面纱的悠久传统之上，让人想起《万物运转的秘密》这类解释日常物品制造原理的书籍。它挑战了工厂需要巨额资本投入和专用机械的观念，认为许多商品可以在简单的空间里用基本工具制造出来。

**社区讨论**: 评论者分享了个人经历：有人经营过小工厂并深感其价值，而另一个人观察到“仅是一个房间”的做法未能维持稳定的业务。还有评论者将快餐厨房比作高效的工厂，认为如果没有自我施加的限制，其他消费品也能达到类似的规模。

**标签**: `#manufacturing`, `#production`, `#engineering`, `#innovation`, `#essay`

---

<a id="item-11"></a>
## [硅基流动赴港 IPO，毛利率为负](https://36kr.com/p/3879814941437956?f=rss) ⭐️ 7.0/10

硅基流动（SiliconFlow）于 2025 年第二季度最后一天以 18C 未商业化公司身份向港交所递交上市申请，招股书显示用户增长迅猛，但 2025 年毛利率为-24%。 此次 IPO 申请凸显了 AI 推理基础设施市场激烈的价格竞争和资本密集型特点，即使是领先的 token 供应商也难以盈利。同时，这也是对港交所为未商业化特专科技公司设计的 18C 上市规则的一次考验。 2025 年，硅基流动收入 5533 万元，但销售成本高达 6863 万元，相当于每卖出 1 元 token 要花 1.24 元成本。公司 2025 年净亏损达 3.45 亿元，研发开支占收入的 378%。

rss · 36氪 · 7月3日 11:12

**背景**: 硅基流动是一家 AI 推理基础设施公司，聚合英伟达、AMD 以及昇腾、沐曦等异构算力，提供标准化的 token 服务。它作为 token 供应平台运营，提供无服务器 token 服务和专属实例。公司成立于 2023 年 8 月，增长迅速，截至 2026 年 4 月注册用户已超 1000 万。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.hkex.com.hk/Listing/Rules-and-Resources/Guidance/IPO/Listing-of-Specialist-Technology-Companies?sc_lang=en">Listing of Specialist Technology Companies - HKEX</a></li>
<li><a href="https://www.lowrisktradesmart.org/en/blog/hong-kong-chapter-18c-specialist-tech-ipo-guide">Hong Kong Chapter 18C IPO — How Specialist Tech Companies ...</a></li>
<li><a href="https://www.siliconflow.com/blog/8-key-insights-on-ai-infra-from-the-co-founder-of-siliconflow">8 Key Insights on AI Infra from the co-founder of SiliconFlow</a></li>

</ul>
</details>

**标签**: `#AI Infrastructure`, `#IPO`, `#Startup`, `#Token Supply`, `#Business Model`

---

<a id="item-12"></a>
## [理想汽车重组：产品团队并入研发](https://36kr.com/p/3877919172047111?f=rss) ⭐️ 7.0/10

理想汽车计划将产品部的关键职能拆分并入研发部门，具体将电动本体定义团队并入整车研发，自动驾驶终端产品团队并入基座模型研发团队。 此次重组旨在通过去除中间环节来精简产品决策流程，有望加快产品迭代、提升效率，帮助理想汽车在日益拥挤的电动汽车市场中重获竞争力。 调整将产品决策链从三个部门（产品线、产品部、研发）缩减为两个（产品线和研发）。产品部将继续负责空间智能和智能眼镜等业务，而电动本体和自动驾驶的核心产品定义团队则转入研发。

rss · 36氪 · 7月3日 10:45

**背景**: 理想汽车此前在 2022 年学习华为，采用了三层产品决策结构，但导致了官僚主义和决策缓慢。CEO 李想承认公司效率落后于竞争对手，因此推动回归创业型管理模式，聚焦效率提升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://36kr.com/p/3877919172047111">理 想 组织再 动 刀：去中间环节，整 车 和智 驾 产 品 回归研发｜36氪独家-36...</a></li>
<li><a href="https://m.21jingji.com/article/20260703/herald/094484a41c67c2623d8f17a4418f5b74.html">理 想 汽 车 “ 动 刀”产品部 - 21财经</a></li>
<li><a href="https://m.cnmo.com/news/812457.html">传 理 想 汽 车 新一轮 组 织 架 构 调整： 产 品 核心团队拆分并入研发_CNMO</a></li>

</ul>
</details>

**标签**: `#理想汽车`, `#组织架构调整`, `#产品研发`, `#电动汽车`, `#自动驾驶`

---

<a id="item-13"></a>
## [生数科技发布 Vidu S1 实时交互模型](https://36kr.com/newsflashes/3879857819201798?f=rss) ⭐️ 7.0/10

生数科技正式发布了 Vidu S1 实时交互模型，该模型支持实时视频通话、语音控制视频走向，并可创建个性化交互角色。 Vidu S1 将实时视频生成与交互功能相结合，是多模态 AI 的重要进展，可在虚拟助手、娱乐和客户服务等领域实现实际应用。 Vidu S1 支持 540P（960x540）高清分辨率、25FPS 帧率（最高 42FPS），可基于真人、动漫、萌宠等任意初始形象及个性化音色创建交互角色。

rss · 36氪 · 7月3日 11:55

**背景**: Vidu S1 由专注多模态大模型的中国 AI 公司生数科技开发，基于其此前 Vidu 系列模型，并通过系统级优化实现持续稳定的实时交互视频生成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.prnewswire.com/news-releases/shengshu-technology-unveils-vidu-s1-bringing-real-time-interactive-generation-to-ai-video-302817626.html">ShengShu Technology Unveils Vidu S1, Bringing Real-Time ...</a></li>
<li><a href="https://www.vidu.com/vidu-stream">Vidu S1 AI Video Model</a></li>
<li><a href="https://juejin.cn/post/7362824067772629003">当前最强国产Sora！ 清华团队突破16...</a></li>

</ul>
</details>

**标签**: `#AI`, `#video generation`, `#real-time interaction`, `#multimodal`

---