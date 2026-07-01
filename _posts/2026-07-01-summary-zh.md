---
layout: default
title: "Horizon Summary: 2026-07-01 (ZH)"
date: 2026-07-01
lang: zh
---

> 从 78 条内容中筛选出 14 条重要资讯。

---

1. [Anthropic 发布 Claude Sonnet 5，聚焦代理能力](#item-1) ⭐️ 8.0/10
2. [Claude Code 隐写标记请求](#item-2) ⭐️ 8.0/10
3. [Anthropic 推出面向数据科学与研究的 Claude Science](#item-3) ⭐️ 8.0/10
4. [中国最严电池安全令正式施行](#item-4) ⭐️ 8.0/10
5. [机器学习与量子理论发现两种新型超导体](#item-5) ⭐️ 8.0/10
6. [谷歌发布 Gemini Omni，实现多模态内容生成](#item-6) ⭐️ 8.0/10
7. [OpenAI 据称将 AI 推理成本减半](#item-7) ⭐️ 8.0/10
8. [在 TypeScript 中解析而非验证](#item-8) ⭐️ 8.0/10
9. [局部推理实现全局属性验证](#item-9) ⭐️ 8.0/10
10. [2025 年 Linux 图形栈深度解析](#item-10) ⭐️ 8.0/10
11. [Soatok 的非正式威胁模型指南](#item-11) ⭐️ 8.0/10
12. [Meta 的 Brain2Qwerty v2 从非侵入性脑信号解码句子](#item-12) ⭐️ 8.0/10
13. [PageStorm 14B 模型：专为长篇创意写作打造](#item-13) ⭐️ 8.0/10
14. [shot-scraper video：用 Playwright 记录智能体演示](#item-14) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Anthropic 发布 Claude Sonnet 5，聚焦代理能力](https://www.anthropic.com/news/claude-sonnet-5) ⭐️ 8.0/10

Anthropic 发布了 Claude Sonnet 5，该模型旨在比前代更具代理性且速度更快，在规划、工具使用和自主任务执行方面能力有所提升。 此次发布标志着 Anthropic 向代理型 AI 的推进，可能为编码、研究和自动化等领域带来更自主的工作流程。然而，早期用户反馈显示，与 Opus 模型相比，其成本效益和可靠性参差不齐。 基准测试显示，Sonnet 5 的性能与 GLM-5.2 相当，但成本翻倍，速度也翻倍。根据独立评估，它在常识问答、组合工具调用任务以及某些谜题解决场景中表现不佳。

hackernews · marinesebastian · 6月30日 17:59 · [社区讨论](https://news.ycombinator.com/item?id=48736605)

**背景**: Claude Sonnet 是 Anthropic 的一系列 AI 模型，定位为旗舰 Opus 模型的更快、更具成本效益的替代品。代理型 AI 指的是能够自主感知、推理并采取行动以实现目标的系统，超越了简单的指令-响应交互。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent - Wikipedia</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained | MIT Sloan</a></li>
<li><a href="https://cloud.google.com/discover/what-is-agentic-ai">What is agentic AI? Definition and differentiators | Google Cloud</a></li>

</ul>
</details>

**社区讨论**: 社区情绪复杂：一些用户发现 Sonnet 5 在中等努力水平下的每任务成本高于 Opus，而另一些用户则报告它无法自主生成代码，浪费 token。少数用户欣赏其速度，但指出其在常识问答和工具调用方面的弱点。

**标签**: `#AI`, `#LLM`, `#Claude`, `#Anthropic`, `#agentic`

---

<a id="item-2"></a>
## [Claude Code 隐写标记请求](https://thereallo.dev/blog/claude-code-prompt-steganography) ⭐️ 8.0/10

一位开发者发现，Anthropic 的 Claude Code 根据 API 基础 URL 和时区，在系统提示中静默嵌入隐写标记，以标记来自中国企业的流量，用于检测模型蒸馏行为。 这引发了使用 Claude Code 的开发者的严重透明度担忧，因为该工具在用户机器上执行未公开的行为，可能削弱对 AI 编码助手的信任。 这些标记通过 Unicode 字符嵌入系统提示中，检测逻辑检查 API 基础 URL 和时区以识别中国用户。Anthropic 尚未公开披露此行为。

hackernews · Lobste.rs · 6月30日 15:44 · [社区讨论](https://news.ycombinator.com/item?id=48734373)

**背景**: 隐写术是将信息隐藏在其他数据中以避免检测的做法。模型蒸馏是指使用大型 AI 模型的输出来训练更小、更便宜的模型，一些公司试图阻止这种行为。Claude Code 是一个本地运行的编码助手工具，它向 Anthropic 的 API 发送请求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://byteiota.com/claude-code-is-marking-requests-what-anthropic-hid/">Claude Code Is Marking Requests: What Anthropic Hid</a></li>
<li><a href="https://www.aimadetools.com/blog/claude-code-steganography-explained/">Claude Code Is Steganographically Marking Requests: What It Means</a></li>
<li><a href="https://www.datacamp.com/blog/distillation-llm">LLM Distillation Explained: Applications, Implementation ...</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：一些人批评 Anthropic 缺乏透明度且实现粗糙，而另一些人则认为意图（防止中国公司进行模型蒸馏）明确且对普通开发者无害。一些人建议使用 Codex CLI 等开源替代方案以避免此类问题。

**标签**: `#AI`, `#security`, `#steganography`, `#developer tools`, `#ethics`

---

<a id="item-3"></a>
## [Anthropic 推出面向数据科学与研究的 Claude Science](https://claude.com/product/claude-science) ⭐️ 8.0/10

Anthropic 推出了 Claude Science，这是一款专为数据科学和研究设计的工具，它运行本地服务器并提供基于 Web 的用户界面，同时集成了机构数据库和高性能计算集群。 此次发布面向科学研究社区，支持在本地安全地进行 AI 辅助的敏感数据分析，有望加速制药和计算生物学等领域的发现。 Claude Science 采用本地服务器架构，连接到基于浏览器的用户界面，因此适用于严格受限的机构环境。它集成了数据库和计算工具，例如机构的高性能计算集群。

hackernews · lebovic · 6月30日 17:07 · [社区讨论](https://news.ycombinator.com/item?id=48735770)

**背景**: 像 Claude 这样的大型语言模型正越来越多地用于科学研究，但幻觉问题——模型生成看似合理但虚假的数据——仍然是一个挑战。Claude Science 的本地架构旨在解决受监管行业中的安全性和数据隐私问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/engineering/desktop-extensions">Claude Desktop Extensions: One-click MCP server installation</a></li>
<li><a href="https://support.claude.com/en/articles/15167101-get-started-with-claude-compliance-api-integrations">Get started with Claude Compliance API integrations</a></li>
<li><a href="https://getaigovernance.net/blog/anthropic-claude-compliance-api-28-enterprise-security-integrations">Anthropic Launches 28 Enterprise Security Integrations for ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论既表达了兴奋也提出了质疑。一位用户指出，LLM 可能编造看似真实的数据和虚假的数据库连接器，质疑 Claude Science 如何防范这一点。另一位构建了相关 HPC 工具的用户称赞了其集成能力，但也承认存在局限性。一位领域专家测试了其在 RNAi 设计中的表现，认为其能力尚可但不出色，且在指出缺陷后 AI 能自我承认。

**标签**: `#AI`, `#data science`, `#research tools`, `#Anthropic`, `#LLM applications`

---

<a id="item-4"></a>
## [中国最严电池安全令正式施行](https://36kr.com/p/3876318522077442?f=rss) ⭐️ 8.0/10

2026 年 7 月 1 日，中国强制性国家标准《电动汽车安全要求》（GB 18384-2025）和《电动汽车用动力蓄电池安全要求》（GB 38031-2025）正式实施，引入了物理断电装置和底部撞击测试等更严格的要求。 这些标准通过强制要求物理断电而非软件控制断电，显著提升了电动汽车的防火安全，可能减少救援延误并防止火灾。该法规影响所有在中国运营的电动汽车制造商，而中国是全球最大的电动汽车市场。 新标准要求驾驶员可通过一个动作操作的物理断电装置，并新增了底部撞击和快充循环安全测试。热扩散要求从“着火前 5 分钟提供报警信号”收紧为“不起火、不爆炸，烟气不对乘员造成伤害”。

rss · 36氪 · 6月30日 23:55

**背景**: 中国的电动汽车电池安全标准随着电动汽车产业的蓬勃发展而快速演进。以往的标准允许基于软件的断电方式，在碰撞或火灾中可能失效。新的 GB 38031-2025 标准于 2025 年 3 月发布，是针对实际火灾风险和提升应急响应能力的一次重大升级。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.chinesestandard.net/PDF-EN/GB38031-2025EN-P13P-H10896H-184581.pdf">PDF GB 38031-2025 English PDF - chinesestandard.net</a></li>
<li><a href="https://kuruibms.com/blog/gb38031-2025-battery-safety-standard-guide.html">GB38031-2025 Battery Safety Standard: Complete Upgrade Guide (2025)</a></li>

</ul>
</details>

**标签**: `#electric vehicles`, `#battery safety`, `#Apple`, `#data leak`, `#regulation`

---

<a id="item-5"></a>
## [机器学习与量子理论发现两种新型超导体](https://36kr.com/newsflashes/3876292099387654?f=rss) ⭐️ 8.0/10

由芬兰阿尔托大学领导的国际团队利用一种结合机器学习与量子理论的新方法，从海量材料组合中筛选出两种新型超导材料，大幅提升了超导材料的发现效率。相关论文于 3 月 29 日发表在《物理评论研究》期刊上。 这一突破加速了新型超导材料的寻找，可能使我们更接近室温超导，从而彻底改变能量传输、磁悬浮和量子计算等领域。该方法展示了材料发现的一种强大新途径。 该团队将机器学习算法与量子理论计算相结合，用于预测和筛选候选材料，从数百万种可能性中缩小到两种有前景的超导体。新闻未披露所发现材料的具体成分，但该方法可推广到其他材料体系。

rss · 36氪 · 6月30日 23:38

**背景**: 超导体是在低于某一临界温度时电阻为零并排出磁场的材料。室温超导体能在 0°C 或更高温度下工作，是物理学长期追求的目标，因为它能实现无损耗电网和强电磁铁。传统的发现方法依赖试错，既缓慢又昂贵。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/超導體">超导体 - 维基百科，自由的百科全书</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/室溫超導體">室温超导体 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#superconductors`, `#materials science`, `#quantum theory`

---

<a id="item-6"></a>
## [谷歌发布 Gemini Omni，实现多模态内容生成](https://36kr.com/newsflashes/3876293824737544?f=rss) ⭐️ 8.0/10

在 I/O 开发者大会上，谷歌发布了全新的 Gemini Omni 模型，该模型能够理解并处理文本、图像、音频和视频输入，生成连贯的视频内容，并支持对话式编辑。 这一进步降低了多媒体内容创作的门槛，用户可以通过自然语言编辑视频，可能改变创作者、营销人员和开发者的工作流程。 Gemini Omni 基于 Gemini 的世界理解和原生多模态能力，能够组合不同输入类型并生成基于现实世界知识的视频。该模型支持通过对话进行编辑，如更换角色、调整光线或改变场景。

rss · 36氪 · 6月30日 23:29

**背景**: 多模态 AI 模型能够处理和生成文本、图像、音频和视频等多种格式的内容。谷歌的 Gemini 系列一直在进化以处理此类任务，Gemini Omni 代表了向无缝对话式内容创作迈进的一步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni/">Introducing Gemini Omni</a></li>
<li><a href="https://deepmind.google/models/gemini-omni/">Gemini Omni — Google DeepMind</a></li>
<li><a href="https://gemini.google/overview/video-generation/">Gemini Omni – Create & edit videos as easy as having a conversation</a></li>

</ul>
</details>

**标签**: `#AI`, `#multimodal`, `#Google`, `#video generation`, `#Gemini`

---

<a id="item-7"></a>
## [OpenAI 据称将 AI 推理成本减半](https://36kr.com/newsflashes/3876288840331266?f=rss) ⭐️ 8.0/10

OpenAI 工程师内部透露，公司通过一系列全新的系统底层优化，成功将 AI 模型的推理成本降低了 50%以上。 这一显著的成本降低可能使大规模 AI 部署更加经济，有望加速各行业的采用，并加剧 AI 提供商之间的竞争。 据报道，这些优化是系统层面的，而非算法层面，具体技术细节尚未公开。该消息来自内部人士，尚未得到官方确认。

rss · 36氪 · 6月30日 23:24

**背景**: AI 推理成本已成为大语言模型部署中的主导因素，随着使用规模扩大，其成本往往超过训练成本。常见的优化技术包括量化、知识蒸馏、前缀缓存和推测解码，这些技术可以在保持质量的同时降低成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.programming-helper.com/tech/ai-inference-optimization-2026-techniques-reducing-llm-costs-10x">AI Inference Optimization 2026: How Quantization, Distillation, and ...</a></li>
<li><a href="https://www.spheron.network/blog/ai-inference-cost-economics-2026/">AI Inference Cost Economics in 2026: GPU FinOps Playbook</a></li>
<li><a href="https://neuron-science.github.io/inference_optimization/docs/section-3/">Systems-Level Inference Optimization | Inference Optimization</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI`, `#cost reduction`, `#inference`, `#optimization`

---

<a id="item-8"></a>
## [在 TypeScript 中解析而非验证](https://cekrem.github.io/posts/parse-dont-validate-typescript/) ⭐️ 8.0/10

本文展示了如何在 TypeScript 中使用品牌类型和运行时验证库（如 Zod）来应用“解析而非验证”模式，克服 TypeScript 类型系统的限制。 这种方法通过使非法状态不可表示来提高类型安全性和代码正确性，在大型 TypeScript 代码库中尤其有价值，因为无效数据导致的运行时错误很常见。 文章使用品牌类型为验证过的数据创建不同的类型，并结合 Zod 模式进行运行时解析，确保只有经过正确验证的数据才能用于后续函数。

rss · Lobste.rs · 6月30日 15:02

**背景**: “解析而非验证”是一种设计原则，主张在边界处将不可信输入转换为结构化类型，而不是在代码中散布验证检查。TypeScript 中的品牌类型在编译时给类型添加一个品牌，没有运行时开销，从而在类型层面区分已验证和未验证的数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://contemplating.dev/posts/parse-dont-validate/">Parse, don't validate - contemplating.dev</a></li>
<li><a href="https://deviq.com/principles/parse-dont-validate/">Parse, Don't Validate – DevIQ</a></li>
<li><a href="https://www.learningtypescript.com/articles/branded-types">Branded Types - Learning TypeScript</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论普遍称赞该文章的实用方法，一些评论者指出该模式可以扩展到具有类似类型系统约束的其他语言。少数人讨论了验证库带来的运行时开销与安全性收益之间的权衡。

**标签**: `#TypeScript`, `#type safety`, `#functional programming`, `#validation`, `#software design`

---

<a id="item-9"></a>
## [局部推理实现全局属性验证](https://tratt.net/laurie/blog/2026/local_reasoning_for_global_properties.html) ⭐️ 8.0/10

该文章提出了一种新颖的方法，利用局部推理技术来验证软件系统中的全局属性，有望降低形式化验证的复杂性。 这项工作可能使形式化验证对大型软件系统更具可扩展性和实用性，通过高效推理全局不变量，影响编程语言理论和软件工程。 该方法可能涉及将全局属性分解为可独立检查的局部不变量，类似于并发和分布式系统验证中的技术。

rss · Lobste.rs · 6月30日 09:58

**背景**: 形式化验证旨在数学上证明系统满足某些属性。全局属性（如安全性、活性）通常需要对整个系统状态进行推理，计算开销很大。局部推理通过关注单个组件及其交互来分解这一过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dl.acm.org/doi/10.5555/1770351.1770363">Local proofs for global safety properties | Proceedings of the 19th international conference on Computer aided verification</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification - Wikipedia</a></li>

</ul>
</details>

**标签**: `#programming languages`, `#formal verification`, `#software engineering`, `#reasoning`

---

<a id="item-10"></a>
## [2025 年 Linux 图形栈深度解析](https://roscidus.com/blog/blog/2025/06/24/graphics/) ⭐️ 8.0/10

2025 年发布了一篇对 Linux 图形栈的详细调查，涵盖了驱动、合成器和渲染管线。 这篇深度文章为复杂且不断演进的 Linux 图形生态系统提供了宝贵见解，帮助开发者和爱好者理解当前的挑战与进展。 文章探讨了内核 DRM、Mesa、Wayland 合成器和 GPU 驱动之间的相互作用，并提供了关于性能和兼容性的实际观察。

rss · Lobste.rs · 6月30日 06:34

**背景**: Linux 图形栈由多层组成：内核 DRM（直接渲染管理器）、Mesa（用户空间 OpenGL/Vulkan 实现）以及管理窗口渲染的合成器（如 KWin、Mutter）。Wayland 已成为现代显示协议，取代 X11，由合成器处理渲染策略。理解这一栈对于优化 Linux 图形性能至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Compositing_manager">Compositing manager - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Graphics_pipeline">Graphics pipeline - Wikipedia</a></li>
<li><a href="https://openlib.io/egl-gbm-and-drm-pipelines-a-deep-architectural-journey-through-modern-linux-rendering-without-a-window-system/">EGL, GBM, and DRM Pipelines: A Deep Architectural Journey ...</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论强调了文章的全面性和实用价值，一些评论者就不同合成器和驱动栈之间的权衡展开了辩论。

**标签**: `#Linux`, `#graphics`, `#systems`, `#open source`

---

<a id="item-11"></a>
## [Soatok 的非正式威胁模型指南](https://soatok.blog/2026/06/30/soatoks-informal-guide-to-threat-models/) ⭐️ 8.0/10

Soatok 发布了一篇面向软件开发者的非正式、实用的威胁建模指南，强调了威胁建模在安全设计中的重要性。该指南为可能不熟悉威胁建模的开发者提供了易于理解的建议。 该指南通过使威胁建模更易于理解，有助于弥合安全专家与开发者之间的差距，可能改善整个软件行业的安全实践。它解决了开发者缺乏足够安全知识来有效建模威胁这一常见挑战。 该指南发布在 Soatok 的博客上，并在 Lobsters 上引发了讨论，表明社区对此感兴趣。它是更广泛的、面向开发者的实用安全资源趋势的一部分。

rss · Lobste.rs · 6月30日 13:12

**背景**: 威胁建模是一种结构化过程，用于识别潜在威胁并在系统设计中确定应对措施的优先级。它回答诸如“我最容易受到攻击的地方在哪里？”和“我需要做什么来防范这些威胁？”等问题。许多开发者由于缺乏安全培训而觉得威胁建模具有挑战性，但像 Soatok 这样的指南旨在使其更易于理解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Threat_modeling">Threat modeling</a></li>
<li><a href="https://owasp.org/www-community/Threat_Modeling">Threat Modeling - OWASP Foundation</a></li>
<li><a href="https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html">Threat Modeling - OWASP Cheat Sheet Series Threat Modeling - OWASP Foundation Threat modeling - Security - MDN GitHub - awslabs/threat-designer: Threat Designer is a ... What Is Threat Modeling? - Palo Alto Networks Security by design: Security principles and threat modeling</a></li>

</ul>
</details>

**社区讨论**: Lobsters 上的讨论可能验证了该指南的价值，评论者分享了额外的见解或个人威胁建模经验。虽然没有提供具体评论，但社区参与表明该指南受到好评。

**标签**: `#threat modeling`, `#security`, `#software engineering`, `#best practices`

---

<a id="item-12"></a>
## [Meta 的 Brain2Qwerty v2 从非侵入性脑信号解码句子](https://www.producthunt.com/products/meta) ⭐️ 8.0/10

Meta FAIR 发布了 Brain2Qwerty v2，这是一种非侵入式脑机接口，能够从连续的 MEG 记录中解码整个打出的句子，无需围绕按键进行分段。 这一进展可能使有语言障碍的人无需进行侵入性手术即可进行交流，并展示了非侵入式脑机接口在实际应用中的潜力。 该系统平均词错误率为 39%，最佳参与者为 22%，使用单个连续 MEG 窗口异步工作。

rss · Product Hunt · 6月30日 04:22

**背景**: 脑机接口（BCI）将大脑活动转化为指令。像 MEG 这样的非侵入式 BCI 无需手术即可记录脑信号，但从中解码语音一直具有挑战性。Brain2Qwerty v2 在先前工作的基础上，直接从 MEG 信号解码打出的句子。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/facebookresearch/brain2qwerty/blob/main/brain2qwerty_v2/README.md">brain2qwerty/brain2qwerty_v2/README.md at main - GitHub</a></li>
<li><a href="https://explainx.ai/blog/meta-brain2qwerty-v2-non-invasive-brain-to-text-decoder-2026">Meta Brain2Qwerty v2: Reading Your Thoughts Without Surgery</a></li>
<li><a href="https://www.cnbctv18.com/technology/brain2qwerty-explained-meta-ai-can-turn-thoughts-into-text-no-brain-implant-needed-19934684.htm">Brain2Qwerty explained: Meta's AI can turn thoughts into ... - CNBCTV18</a></li>

</ul>
</details>

**标签**: `#brain-computer interface`, `#non-invasive`, `#decoding`, `#AI`, `#accessibility`

---

<a id="item-13"></a>
## [PageStorm 14B 模型：专为长篇创意写作打造](https://i.redd.it/lyowrx2jmfah1.png) ⭐️ 8.0/10

PageStorm 是一个基于 Mistral3 14B 微调的 140 亿参数模型，专为长篇创意写作设计，在 256K 序列长度上使用 1500 亿 token 进行训练。它在全部 7 项叙事基准测试中超越 GPT-5.5，并在 7 项中的 4 项上超越 Opus 4.8。 该模型解决了生成连贯长篇叙事这一尚未充分探索的任务，并引入了基于叙事理论的新基准。其成功表明，专门的微调可以在创意写作中超越通用前沿模型，尽管长上下文稳定性仍是一个挑战。 该模型通过谷歌 TPU 研究云的 V6e-256 TPU 集群训练，采用分阶段生成流水线，从单个提示生成完整小说。已知的局限是长上下文生成不稳定，较长的书籍不可避免地会陷入重复循环。

reddit · r/LocalLLaMA · XMasterDE · 6月30日 14:43 · [社区讨论](https://www.reddit.com/r/LocalLLaMA/comments/1ujr69g/pagestorm_a_model_built_for_creative_book_writing/)

**背景**: 像 GPT-4 和 GPT-5.5 这样的大型语言模型擅长短文本，但由于连贯性和重复问题，在长篇创意写作方面存在困难。PageStorm 是一个专用模型，在名为 LongPage 的数据集上微调，以改善数十万 token 范围内的叙事结构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/markldn/pagestorm-research-preview-14b-full-book-Q8_0-GGUF">markldn/pagestorm-research-preview-14b-full-book-Q8_0-GGUF ...</a></li>
<li><a href="https://benchlm.ai/models/gpt-5-5">GPT-5.5 Benchmarks 2026: Scores, Rankings & Performance</a></li>
<li><a href="https://arxiv.org/html/2510.13191v1">Grounding Long-Context Reasoning with Contextual ...</a></li>

</ul>
</details>

**社区讨论**: 作者（XMasterDE）提供了技术细节并承认了重复循环的局限，计划扩大模型规模并加入强化学习后训练。有用户询问 GGUF 格式，但作者表示这不是标准聊天模型，需要特殊封装，不过提供了推理代码库。

**标签**: `#LLM`, `#creative writing`, `#long context`, `#benchmark`, `#open source`

---

<a id="item-14"></a>
## [shot-scraper video：用 Playwright 记录智能体演示](https://simonwillison.net/2026/Jun/30/shot-scraper-video/#atom-everything) ⭐️ 7.0/10

shot-scraper 1.10 新增了 'video' 命令，它接受一个 storyboard.yml 文件，并使用 Playwright 录制 Web 应用程序操作的视频，从而让编码智能体能够生成其工作的可视化证明。 该工具解决了 AI 智能体工作流中的一个关键挑战：验证智能体是否确实执行了预期操作。通过生成可复现的视频演示，它提高了使用编码智能体的开发者的信任度和调试效率。 storyboard.yml 文件定义了服务器设置、视口、光标可见性、等待条件、JavaScript 覆盖（例如剪贴板模拟）以及一系列包含暂停、点击和输入等操作的场景。该命令支持通过 cookie 文件进行身份验证，并输出 WebM 或 MP4 视频。

rss · Simon Willison · 6月30日 16:54

**背景**: shot-scraper 是一个命令行工具，利用浏览器自动化库 Playwright 对网页进行截图。新的 video 命令将这一能力扩展到录制完整会话，使其适用于演示 Web 应用程序功能或智能体行为。Playwright 本身原生支持视频录制，但 shot-scraper video 提供了一个更高级的、由 YAML 驱动的接口，专为智能体演示而设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jun/30/shot-scraper-video/">Have your agent record video demos of its work with shot ...</a></li>
<li><a href="https://letsdatascience.com/news/shot-scraper-launches-video-command-in-110-07962b66">shot-scraper launches video command in 1.10 | Let's Data Science</a></li>
<li><a href="https://digg.com/tech/46k6q4wt">Shot-Scraper Adds Video Recording Support Using YAML ...</a></li>

</ul>
</details>

**社区讨论**: 社区反响积极，用户称赞其清晰的 storyboard-as-config 方法及其在开发工作流中的实用性。一些人指出该工具填补了智能体工具链中的一个实际空白，但未出现重大分歧或担忧。

**标签**: `#developer-tools`, `#testing`, `#automation`, `#playwright`, `#ai-agents`

---