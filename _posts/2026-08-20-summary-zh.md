---
layout: default
title: "Horizon Summary: 2026-08-20 (ZH)"
date: 2026-08-20
lang: zh
---

> 从 63 条内容中筛选出 10 条重要资讯。

---

1. [Stripe 以约 70 亿美元收购 OpenRouter](#item-1) ⭐️ 9.0/10
2. [Go 1.27 发布：引入泛型方法、UUID 标准包和后量子密码学](#item-2) ⭐️ 9.0/10
3. [宇树往事：从 2017 年机器狗到超 4000 亿市值上市](#item-3) ⭐️ 9.0/10
4. [关于气象气球的玩笑式域名购买演变成地缘政治纷争](#item-4) ⭐️ 8.0/10
5. [用几何与 CUDA 编程定位一个神秘岛屿](#item-5) ⭐️ 8.0/10
6. [Simon Willison：AI 编程时代，代码行数依然是有效生产力指标](#item-6) ⭐️ 8.0/10
7. [王兴兴在宇树上市宴上首谈机器人「大脑」技术路线](#item-7) ⭐️ 8.0/10
8. [Mastodon 5.0 发布：“为未来发展奠定基础”](#item-8) ⭐️ 8.0/10
9. [将 SmolVM 用作不受信任的 Python 与 JavaScript 沙箱的测试](#item-9) ⭐️ 7.0/10
10. [利用 Rosetta 2 打包恶意软件：一种新的规避技术](#item-10) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Stripe 以约 70 亿美元收购 OpenRouter](https://openrouter.ai/blog/announcements/openrouter-is-joining-stripe/) ⭐️ 9.0/10

Stripe 正在收购广受欢迎的人工智能模型路由代理 OpenRouter，据报道交易价值超过 70 亿美元。这一公告证实了此前的报道，并标志着迄今为止最大规模的人工智能基础设施收购之一。 这笔收购验证了模型路由与聚合的商业模式，表明即使不拥有模型，分发层也能具有极高价值。这也使 Stripe 在人工智能基础设施领域获得了一个重要的切入点，可以将模型计量、按用量计费和智能体支付直接整合到其平台中。 OpenRouter 通过单一 API 向众多大型语言模型提供商提供访问，具备自动故障转移、在满足性能最低要求下优先选择最便宜提供商以及统一计费等功能。据报道，这笔交易价值超过 70 亿美元，但官方尚未确认具体条款。

hackernews · rvz · 8月19日 17:32 · [社区讨论](https://news.ycombinator.com/item?id=49364559)

**背景**: OpenRouter 是一种人工智能模型路由代理，也被称为 LLM 网关，它为开发者提供统一 API，用于访问来自不同提供商的多个模型。这避免了供应商锁定，让提供商在价格和质量上竞争，并通过自动故障转移帮助开发者降低成本、提高可靠性。随着人工智能使用量的增长，这类路由器正在成为管理成本以及将人工智能接入实际计费和支付系统的关键基础设施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://inworld.ai/resources/what-is-an-ai-router">What Is an AI Router? LLM Model Routing Explained (2026)</a></li>
<li><a href="https://inworld.ai/resources/ai-model-routing-cost-reduction">AI Model Routing Explained: Cut LLM Costs (2026) - Inworld AI</a></li>

</ul>
</details>

**社区讨论**: 评论者大多称赞 OpenRouter 是一款出色的产品，并希望 Stripe 能够成为一个好的管理者。一些人表达了对行业整合加剧和中间商增多的担忧，认为像开放银行这样的协议形式会更可取。还有几人强调了性能感知路由等高级功能，另有人指出该项目在 Hacker News 上的创始帖子最初只获得 6 个点赞和 0 条评论。

**标签**: `#AI`, `#Acquisitions`, `#Stripe`, `#OpenRouter`, `#API`

---

<a id="item-2"></a>
## [Go 1.27 发布：引入泛型方法、UUID 标准包和后量子密码学](https://go.dev/blog/go1.27) ⭐️ 9.0/10

Go 1.27 已正式发布，新增了泛型方法、简化的泛型函数调用、标准 UUID 包和重写的 JSON 引擎。它还通过 crypto/mldsa 包更新了后量子密码学支持。 这是 Go 语言的重要里程碑，填补了泛型在方法上长期存在的使用缺口，并提供了内置的 UUID 解决方案，减少了对第三方库的依赖。后量子密码学更新帮助生态应对量子计算的威胁，与 NIST 的标准化工作保持一致。 泛型方法现在允许在方法声明上使用类型参数，泛型函数调用时也无需显式指定类型参数。浮点数解析和格式化改用 Russ Cox 的新 uscale 算法，标准 uuid 包为 github.com/google/uuid 提供了内置替代方案。

hackernews · Lobste.rs · 8月19日 18:33 · [社区讨论](https://news.ycombinator.com/item?id=49365405)

**背景**: Go 是由 Google 开发的一种静态类型、编译型编程语言，于 2009 年首次发布。泛型在 Go 1.18 中引入，但此前方法不能声明自己的类型参数，直到这次更新才解除限制。后量子密码学指为抵御未来量子计算机攻击而设计的算法；NIST 于 2024 年发布了首批三个最终 PQC 标准，其中 ML-DSA（crypto/mldsa）是新的签名算法之一。社区此前常依赖第三方库 google/uuid，标准包的加入简化了依赖管理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gopherguides.com/articles/golang-generic-methods">Generic Methods Arrive in Go 1.27 - Gopher Guides</a></li>
<li><a href="https://en.wikipedia.org/wiki/Post-quantum_cryptography">Post-quantum cryptography</a></li>
<li><a href="https://northeasttimes.com/2026/08/02/go-1-27-brings-generic-methods-post-quantum-crypto-and-a-new-json-engine/">Go 1.27 brings generic methods, post-quantum crypto and a new JSON engine - Northeast Times</a></li>

</ul>
</details>

**社区讨论**: 评论中既有热情也有担忧。一些开发者赞赏泛型方法改进和后量子密码学方面的前瞻性工作，还有人预测会出现一波将 google/uuid 替换为新标准包的拉取请求。另一位评论者表示不喜欢 Go 的错误处理风格，这是常见的批评点。

**标签**: `#Go`, `#Programming Languages`, `#Software Release`, `#Generic Methods`, `#Post-Quantum Crypto`

---

<a id="item-3"></a>
## [宇树往事：从 2017 年机器狗到超 4000 亿市值上市](http://www.geekpark.net/news/369047) ⭐️ 9.0/10

在宇树科技上市当天，一位早期投资人发表了一篇回忆文章，回顾了宇树从 2017 年车库里的一台机器狗起步，到如今市值超 4000 亿元上市公司的历程。 宇树的 IPO 为方兴未艾的具身智能与机器人行业树立了宝贵的价值锚点。这位早期投资人的内部视角揭示了宇树成功的关键：在资本不看好的“错误季节”中坚持电驱技术路线与工程精益，最终以极致性价比赢得全球认可。 文章披露了多个细节：宇树首款四足机器人名为 Laikago，致敬替人类探索太空的莱卡犬；投资人于 2017 年 10 月 21 日首次在杭州一个“车库”式办公室见到创始人王兴兴，当时公司没有门牌、没有 BP、也没有明星创始人加持。王兴兴最终以约为波士顿动力 1%的造价成本，做出了全球性价比最高的四足和人形机器人本体。

rss · 极客公园 · 8月19日 12:19

**背景**: 宇树科技由王兴兴创立，是一家专注于腿足式机器人的中国企业；其首款四足机器人 Laikago 面向科研市场，配备 12 个无刷直流电机，具备在不平地面行走和抗扰动能力。文章以波士顿动力和 MIT 机器猎豹为参照，凸显宇树早期产品在成本与完成度上的优势。“具身智能”指 AI 通过物理身体感知并作用于真实世界的技术方向，自 2023 年前后成为投资热点。这一回顾也折射出中国创业叙事从移动互联网向硬科技转变的大背景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://robotsguide.com/robots/laikago/">Laikago - ROBOTS: Your Guide to the World of Robotics</a></li>
<li><a href="https://news.mit.edu/2019/mit-mini-cheetah-first-four-legged-robot-to-backflip-0304">Mini cheetah is the first four-legged robot to do a backflip</a></li>
<li><a href="https://en.wikipedia.org/wiki/Embodied_intelligence">Embodied intelligence</a></li>

</ul>
</details>

**标签**: `#embodied AI`, `#robotics`, `#Unitree IPO`, `#startup investing`, `#entrepreneurship`

---

<a id="item-4"></a>
## [关于气象气球的玩笑式域名购买演变成地缘政治纷争](https://sprocketfox.io/xssfox/2026/08/19/sondehub-and-war/) ⭐️ 8.0/10

在 2026 年 8 月的一篇博客文章中，安全研究员 xssfox 讲述了一次与 SondeHub（一个追踪气象气球的公民科学网络）有关的玩笑式域名购买，如何引起军方和情报界的注意。这个故事展示了一个轻松爱好如何与现实中的地缘政治紧张局势相碰撞。 这件事之所以重要，是因为开放、众包的无线电追踪数据对 OSINT 和军事监测越来越有价值，使业余爱好者意外地处于敏感位置。它凸显了开放数据时代民用科学与国家安全之间日益模糊的界限。 文章提到，无线电探空仪发射机制造商如 Meteolabor 以“战略考虑”为由解释发射机在电池耗尽后为何关机，这暗示了军事敏感性。作者还讲述了因相关数据被联系调查一起肇事逃逸事件的经历，这与 OSINT 驱动的调查相呼应。

hackernews · kareiva · 8月19日 11:21 · [社区讨论](https://news.ycombinator.com/item?id=49360015)

**背景**: 气象气球携带无线电探空仪，这是一种小型电池供电仪器，在上升过程中测量气压、温度和湿度，并通过无线电发送数据。像 SondeHub 这样的项目让志愿者用廉价接收器解码并汇总这些信号，形成开放的实时地图。OSINT 是把这类公开数据转化为可用情报的做法，因此这类数据会引起军方和政府关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-source_intelligence">Open-source intelligence - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Radiosonde">Radiosonde - Wikipedia</a></li>
<li><a href="https://www.noaa.gov/jetstream/upperair/radiosondes">Radiosondes | National Oceanic and Atmospheric Administration</a></li>

</ul>
</details>

**社区讨论**: 评论者反响热烈且怀旧，有人分享了十年前和朋友发射气象气球的经历，还有人表示很高兴在文章中看到“habhub”。不少读者欣赏这种由人撰写而非 LLM 生成的行文风格；一位基础设施团队成员也表示，他们同样收到过来自.mil、.gov 和 GeoTLD 域名的各种奇怪请求。

**标签**: `#geopolitics`, `#radio tracking`, `#weather balloons`, `#open data`, `#OSINT`

---

<a id="item-5"></a>
## [用几何与 CUDA 编程定位一个神秘岛屿](https://yassa9.github.io/osint/gralhix-004/) ⭐️ 8.0/10

一篇技术文章详细记录了如何利用几何分析和 CUDA 加速计算，从一张照片中定位一座未知岛屿。社区评论将该方法与地形轮廓匹配和行星着陆系统联系起来，验证了该方法的可行性。 这表明 GPU 加速的几何计算可以成为 OSINT 分析人员自动定位地点的实用工具。同时也显示出导航与太空探索中使用的技术，如何启发解决日常照片定位难题。 文章使用 CUDA 将几何搜索并行化以遍历可能的地点；有评论者指出，从照片中太阳在左侧且时值正午，可推断视角朝向偏西。这一推断缩小了搜索范围，最终结果也确实如此。

hackernews · yassa9 · 8月19日 12:19 · [社区讨论](https://news.ycombinator.com/item?id=49360545)

**背景**: CUDA 是 NVIDIA 推出的并行计算平台与编程模型，它将 C++扩展以在 GPU 上运行通用计算，使成千上万个线程能同时执行数据并行任务，非常适合计算密集型的搜索与图像分析。在 OSINT 中，照片定位通常依赖视觉线索、地图数据以及和已知影像比对；通过 GPU 加速自动化这些比对，能帮助快速测试大量候选地点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/even-easier-introduction-cuda/">An Even Easier Introduction to CUDA (Updated) - NVIDIA Developer Introduction to CUDA Programming - GeeksforGeeks 1.1. Introduction — CUDA Programming Guide Tutorial 01: Say Hello to CUDA - CUDA Tutorial - Read the Docs CUDA Tutorial - GeeksforGeeks CUDA Tutorial</a></li>
<li><a href="https://www.geeksforgeeks.org/electronics-engineering/introduction-to-cuda-programming/">Introduction to CUDA Programming - GeeksforGeeks</a></li>
<li><a href="https://kit.exposingtheinvisible.org/en/geolocation.html">Geolocation Methods: A step by step guide — The Kit 1.0 documentation</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞这篇文章读起来很过瘾，让人想起早年 Hacker News 上由人撰写的帖子，并将其与导弹的地形轮廓匹配（TERCOM）导航及 JPL 的“火星 2020”着陆系统联系起来。还有人指出，仅凭太阳位置和拍摄时间就能推断出大致方向；也有用户调侃说，这篇文章正好排在另一篇关于“避免打造可被警察国家利用的技术”的帖子旁边，显得有些讽刺。

**标签**: `#geolocation`, `#CUDA`, `#computer-vision`, `#OSINT`, `#geometry`

---

<a id="item-6"></a>
## [Simon Willison：AI 编程时代，代码行数依然是有效生产力指标](https://simonwillison.net/2026/Aug/19/conceptual-integrity-and-counting-lines-of-code/) ⭐️ 8.0/10

Simon Willison 在《Talking Postgres》播客中提出，对 AI 编程智能体而言，代码行数（LOC）可以成为有意义的生产力指标，直接挑战了长期以来把 LOC 视为无效衡量标准的观点。他还讨论了智能体会如何侵蚀软件的“概念完整性”，并把智能体驱动的软件增长比作“温彻斯特神秘屋”。 这一细致且反主流的观点挑战了软件工程界最根深蒂固的共识之一，为衡量 AI 辅助开发的生产力提供了务实的思考框架。它对团队规模、绩效评估以及企业如何采用编程智能体都有直接影响，因为 Willison 认为真正的瓶颈正在从“写代码”转向“认知容量”。 Willison 指出，在智能体出现之前，每天能写出几百行生产级代码就算很好的状态；而智能体可以让一名工程师每天产出上千行“已调试、可维护、经过测试”的代码——前提是工程师本人具备足够的技能和经验。他警告说，由于智能体让“新增房间”变得极其廉价，软件会迅速失去概念完整性并变得更难做决策，因此纪律现在必须来自工程师自身，而不是来自时间成本的自然限制。

rss · Simon Willison · 8月19日 22:46

**背景**: “概念完整性”（conceptual integrity）出自 Fred Brooks 的《人月神话》（The Mythical Man-Month），指优秀软件具有内在一致性，使其可预测、连贯、易于推理。代码行数（LOC）长期以来被视为糟糕的生产力指标，因为代码量更多往往意味着质量更差；但 Willison 将讨论重新放到 AI 时代，强调在同等质量下产出数量出现数量级差异仍然具有意义。基于 LLM 的编程智能体是一类快速演进的 AI 工具，能够自主生成、调试和修改代码，并且已经在重塑软件开发生命周期。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2508.00083">A Survey on Code Generation with LLM-based Agents</a></li>
<li><a href="https://medium.com/nerd-for-tech/ensuring-conceptual-integrity-in-software-development-fd0b746f44c0">Ensuring Conceptual Integrity in Software Development | Medium</a></li>
<li><a href="https://www.lossless.group/more-about/conceptual-integrity">Conceptual Integrity | Lossless Group</a></li>

</ul>
</details>

**标签**: `#AI coding`, `#software engineering`, `#productivity`, `#LLM agents`, `#Simon Willison`

---

<a id="item-7"></a>
## [王兴兴在宇树上市宴上首谈机器人「大脑」技术路线](http://www.geekpark.net/news/369051) ⭐️ 8.0/10

8 月 19 日，宇树科技正式登陆科创板，上市首日股价一度较发行价涨超 6 倍，市值突破 4400 亿元人民币。当天午宴上，创始人王兴兴首次明确阐述了公司机器人「大脑」的技术路线，强调要搭建一个让 AI 进入机器人研发全过程的闭环系统。 这一表态显示宇树正从「身体最强」的硬件优势转向以 AI 驱动的具身智能系统级竞争。对机器人和 AI 行业而言，创始人对「大脑」路线的公开定调，意味着竞争焦点可能从单一模型转向「模型—工具—仿真—真机—评价」的全链路整合，有望加速机器人技能的自我进化。 王兴兴描述的路径是：AI 自动检索最新论文和开源代码、生成训练程序，程序进入仿真环境，并借助视频生成模型构造训练素材；完成仿真后部署到实体机器人上测试，再根据表现实现自我进化。他认为只做一个 AI 模型或视频模型已不足以形成竞争力，下一阶段真正重要的是把模型、工具、仿真、真机和评价连接成一个系统。

rss · 极客公园 · 8月19日 12:29

**背景**: 宇树科技是中国知名的人形机器人与四足机器人公司，以硬件和运动控制能力著称。所谓机器人「大脑」，通常指控制机器人的 AI 模型；行业中，视觉-语言-动作（VLA）模型将视觉、语言理解与物理动作输出结合，用于直接控制机器人，而世界模型则帮助智能体预测环境动态并进行规划。王兴兴所说的系统化路线，本质上属于具身智能范畴——让 AI 不仅做大脑，还参与机器人的设计、训练和迭代。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://reflexvla.github.io/">Reflex: Enabling Fast and Predictive Vision - Language - Action Models</a></li>
<li><a href="https://www.emergentmind.com/topics/world-models.md">emergentmind.com/topics/ world - models .md</a></li>
<li><a href="https://generalistai.com/blog/gen-0">Generalist - GEN-0 / Embodied Foundation Models That Scale with Physical Interaction</a></li>

</ul>
</details>

**标签**: `#Unitree`, `#humanoid robots`, `#robotics`, `#AI`, `#IPO`

---

<a id="item-8"></a>
## [Mastodon 5.0 发布：“为未来发展奠定基础”](https://blog.joinmastodon.org/2026/08/5.0-laying-the-foundation/) ⭐️ 8.0/10

Mastodon 宣布其开源社交媒体平台推出 5.0 版本，并将该版本描述为“为未来发展奠定基础”。公告本身内容不多，主要指向 Lobsters 上的讨论帖。 Mastodon 是联邦宇宙（fediverse）中使用最广泛的平台之一，因此其重大版本发布会影响整个去中心化社交网络生态。“打基础”的定位表明，这一版本可能为未来 Mastodon 及基于 ActivityPub 的社区确定技术方向。 该公告未包含变更日志、路线图或功能列表，只附加了一个讨论帖链接。Mastodon 的去中心化模式依赖 ActivityPub 协议实现服务器之间的联邦互通。

rss · Lobste.rs · 8月19日 00:03

**背景**: Mastodon 是一个免费开源社交网络平台，运行于许多可相互联通的独立服务器上。它是联邦宇宙（fediverse）的组成部分；联邦宇宙是一组通过开放协议（主要是 W3C 标准的 ActivityPub）进行通信的社交服务集合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Fediverse">Fediverse</a></li>
<li><a href="https://en.wikipedia.org/wiki/ActivityPub">ActivityPub</a></li>
<li><a href="https://activitypub.rocks/">ActivityPub Rocks!</a></li>

</ul>
</details>

**标签**: `#mastodon`, `#social media`, `#open source`, `#fediverse`, `#software release`

---

<a id="item-9"></a>
## [将 SmolVM 用作不受信任的 Python 与 JavaScript 沙箱的测试](https://simonwillison.net/2026/Aug/19/smolmachines-untrusted-sandbox/) ⭐️ 7.0/10

Simon Willison 记录了一项研究任务：让 Claude Fable 5 评估 smolvm 作为硬件事隔离沙箱，用于运行不受信任的 Python 和 JavaScript，并限制 CPU、内存、网络与文件系统访问。由于 Claude Code for web 环境缺少 KVM 支持而无法直接运行 smolvm，Claude 改用临时 GitHub Actions 工作流来执行测试。 这项研究意义在于：基于 microVM 的沙箱技术为安全执行用户提交的代码（如数据转换任务）提供了有前景的路径，既避免了完整容器的开销，也规避了共享进程沙箱的风险。同时，它也展示了 AI 代理能够自主寻找替代执行环境，绕过基础设施限制。 评估过程中遇到了嵌套虚拟化问题：Claude Code for web 容器没有/dev/kvm，也没有 vmx/svm CPU 标志。作为变通方案，Claude 创建了一个临时 GitHub Actions 工作流（ubuntu runner 暴露/dev/kvm），安装 smolvm 并运行测试套件，然后在最终提交前删除该工作流。

rss · Simon Willison · 8月19日 23:16

**背景**: smolvm 是一个便携、轻量、自带一切的虚拟机项目，能在毫秒级启动 microVM，并为每个工作负载提供独立的 VM 和客户机内核。它面向在硬件事隔离虚拟机中运行不受信任代码等场景，可在笔记本、云端或自托管环境中使用。其安全模型通过为每个工作负载提供独立 VM 来强化来宾/主机边界，但它本身并非加固的多用户控制平面。使用 smolvm 的关键前提是 KVM 支持，而在嵌套或容器化环境中可能无法使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/smol-machines/smolvm">GitHub - smol-machines/smolvm: Portable, lightweight, self-contained virtual machine. · GitHub</a></li>
<li><a href="https://smolmachines.com/">smol machines — the same smol machine on your laptop, in the cloud, or self-hosted</a></li>

</ul>
</details>

**标签**: `#sandboxing`, `#Python`, `#JavaScript`, `#security`, `#research`

---

<a id="item-10"></a>
## [利用 Rosetta 2 打包恶意软件：一种新的规避技术](https://kernelkennel.com/blog/summercon2026-rosetta/) ⭐️ 7.0/10

一名安全研究人员在 Summercon 2026 上发表了题为“在 Rosetta 2 中打包恶意软件”的演讲，详细说明了如何滥用苹果的 Rosetta 2 翻译层进行恶意软件打包。相关文章描述了利用 Rosetta 的动态二进制翻译来隐藏恶意代码的技术。 这项研究为 Apple Silicon Mac 引入了新的规避途径，因为 Rosetta 透明的翻译过程可被重新用于混淆恶意负载。主要依赖静态分析的安全工具可能难以检测或分析通过该层翻译的打包二进制文件，这对 macOS 防御构成了重大挑战。 该演讲可能重点介绍如何利用 Rosetta 2 的动态二进制翻译来取代传统打包器，从而使生成的二进制文件更难进行静态检查。它可能还会讨论局限性，例如 Rosetta 用于在 Apple Silicon 上运行 Intel 应用的预期用途，以及针对此类打包恶意软件的潜在检测方法。

rss · Lobste.rs · 8月19日 22:05

**背景**: Rosetta 2 是苹果为 macOS 开发的动态二进制翻译器，允许基于 Intel 的应用程序在 Apple Silicon 芯片上运行，对用户来说基本透明。恶意软件打包是一种常见的混淆技术，通过压缩或加密可执行文件来改变其文件签名，从而逃避基于签名的检测。这项研究将这两个概念结合起来，利用 Rosetta 自身的翻译层作为打包机制，给 macOS 上的安全工具带来了新的挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rosetta_(software)">Rosetta (software) - Wikipedia</a></li>
<li><a href="https://developer.apple.com/documentation/apple-silicon/about-the-rosetta-translation-environment">About the Rosetta translation environment - Apple Developer</a></li>
<li><a href="https://attack.mitre.org/techniques/T1027/002/">Obfuscated Files or Information: Software Packing, Sub-technique T1027.002 - Enterprise | MITRE ATT&CK®</a></li>

</ul>
</details>

**标签**: `#security`, `#malware`, `#macOS`, `#Rosetta 2`, `#reverse engineering`

---