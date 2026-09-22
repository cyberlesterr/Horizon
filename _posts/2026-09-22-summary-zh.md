---
layout: default
title: "Horizon Summary: 2026-09-22 (ZH)"
date: 2026-09-22
lang: zh
---

> 从 64 条内容中筛选出 9 条重要资讯。

---

1. [NASA 火星采样返回任务实际上已被取消](#item-1) ⭐️ 8.0/10
2. [Bryan Cantrill 剖析 Sun Microsystems 究竟错在哪里](#item-2) ⭐️ 8.0/10
3. [xAI 发布 Grok 4.7：参数量增加约四成，价格保持不变](#item-3) ⭐️ 8.0/10
4. [光纤被切断导致通信中断，FAA 暂停美国东海岸航班](#item-4) ⭐️ 8.0/10
5. [TypeSafe AI 发布首个“System One”决策模型 Jev](#item-5) ⭐️ 8.0/10
6. [Project Zero 详解悬空 COM 对象注册利用技术](#item-6) ⭐️ 8.0/10
7. [《你只拥有注意力》：一篇关于注意力经济的随笔](#item-7) ⭐️ 7.0/10
8. [Jev：只做判断不出文字的模型，数天催生近五百个项目](#item-8) ⭐️ 7.0/10
9. [书评：《并行编程难吗，难的话该怎么办？》](#item-9) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [NASA 火星采样返回任务实际上已被取消](https://www.science.org/content/article/nasa-s-mars-sample-return-mission-dead) ⭐️ 8.0/10

由 NASA 与欧洲空间局（ESA）联合推进的“火星采样返回”（MSR）计划实际上已被叫停，该计划的目的是把“毅力号”火星车在火星上封存的岩石和土壤样本管带回地球。项目此前一再延期，成本估算已膨胀到约 110 亿美元，样本返回时间被推迟到最早 2040 年前后，NASA 最终选择停止为原有架构继续投入资金。 MSR 一直是行星科学界十年调查中排在首位的旗舰项目，它的取消意味着在近期内把火星物质带回地面实验室进行生命探测研究的最清晰路径被切断。这同时也把火星采样返回的领先位置让给了中国——其天问三号采用双次发射方案，瞄准 2028—2029 年的火星发射窗口——并让 NASA 喷气推进实验室（JPL）的定位、人员规模以及与 ESA 的合作前景都成为疑问。 原有架构依赖多次发射，包括样本取回着陆器、火星上升飞行器，以及由 ESA 建造、使用 Ariane 6/64 火箭发射的地球返回轨道器；NASA 此前已在研究更便宜的替代方案，例如基于 Starship 或 New Glenn 的架构以及单次发射设计。作为规模对比，“毅力号”封存的样本总重约 1.1 磅，而阿波罗计划带回的月球岩石多达 842 磅；NASA 监察长办公室（OIG）此前的审计报告也已批评该项目的成本与管理问题。

hackernews · Muhammad523 · 9月21日 19:14 · [社区讨论](https://news.ycombinator.com/item?id=49791939)

**背景**: 火星采样返回是一个讨论多年的多任务系统工程：先由火星车在火星上采集并封存岩石、土壤和大气样本，之后再由后续航天器取回并送回地球，以便用远比火星车所载设备强大的实验室仪器进行研究。NASA 的“毅力号”自 2021 年起就在杰泽罗陨石坑钻取并密封这类样本管，MSR 于 2022 年作为 NASA 与 ESA 的合作项目正式获批。其科学目标是天体生物学层面的——判定火星是否曾经存在生命，同时把样本带回做细致的地质与大气分析。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mars_sample-return_mission">Mars sample-return mission</a></li>
<li><a href="https://metapress.com/nasa-halts-mars-sample-return-mission-budget-overruns-2026/">NASA Halts Mars Sample Return Mission Amid Budget Overruns</a></li>
<li><a href="https://www.space.com/nasa-revamp-mars-sample-return-plan">NASA's Mars sample return plan is getting a major overhaul ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍把这看作项目管理而非科学上的失败：不少人指责 JPL 领导层把成本推到约 110 亿美元、交付时间拖到 2040 年，并且围绕 Ariane 64 这类老旧火箭设计架构，而不是采用 Starship 或 New Glenn 等更便宜的商业重型运载方案。也有人强调国际竞争，提到中国的天问三号和一再推迟的 ExoMars“罗莎琳德·富兰克林”号火星车；还有一种反复出现的观点认为，NASA 应把钱投向可复用运载能力或等待载人任务，而不是花约 200 亿美元只带回几磅石头。

**标签**: `#NASA`, `#Mars Sample Return`, `#space exploration`, `#JPL`, `#space policy`

---

<a id="item-2"></a>
## [Bryan Cantrill 剖析 Sun Microsystems 究竟错在哪里](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

DTrace 联合创造者、曾在 Sun Microsystems 工作多年的工程师 Bryan Cantrill 在其个人博客上发表了一篇题为《What Sun got wrong》的回顾文章，分析了导致该公司衰落的一系列战略与技术失误。这篇文章登上 Hacker News 首页，获得约 482 分和 264 条评论。 这篇文章是来自内部人士对计算史上最具影响力的系统公司之一的罕见“尸检”，而它出现的时机恰逢业界重新争论供应商锁定、专有硬件，以及仅靠工程 excellence 能否支撑一家企业。许多工程师和创业者把它与当下超大规模云厂商和 AI 基础设施格局作类比，因此广泛传阅。 这是一篇亲身经历者的第一人称叙述，作者经历了 Sun 的 SPARC 与 Solaris 时代，因此文中既有技术层面的细节（比如一度被取消的 Solaris on x86 计划、与 Google 未达成的合作），也有商业批评；Hacker News 的讨论还补充了 Sun 那种流程繁琐、以报价驱动的销售模式与 Dell 之间的对比轶事。

hackernews · Lobste.rs · 9月21日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=49787436)

**背景**: Sun Microsystems 成立于 1982 年，以出售基于自家 SPARC 处理器和 Solaris 操作系统的高性能 Unix 工作站与服务器而闻名，Solaris 孕育了 DTrace、ZFS 等被广泛采用的技术。Solaris 是一款专有 Unix 操作系统，Sun 于 2005 年通过 OpenSolaris 项目以 CDDL 许可证开放了大部分源代码。在经历 2000 年代的困境后，Sun 于 2010 年被 Oracle 收购，此后 Oracle 裁撤了大部分 Solaris 团队，并实质上再次关闭了内核源码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Solaris_operating_system">Solaris operating system</a></li>
<li><a href="https://en.wikipedia.org/wiki/Sun_Microsystems">Sun Microsystems - Wikipedia</a></li>
<li><a href="https://spectrum.ieee.org/after-the-sun-microsystems-sets-the-real-stories-come-out">After the Sun (Microsystems) Sets, the Real Stories Come Out - IEEE Spectrum</a></li>

</ul>
</details>

**社区讨论**: 评论者大体认同文中的批评，并补充了亲历细节：有人回忆 1990 年代末从 Sun 或 DEC 采购意味着没完没了的报价修改和销售会议，光是服务器导轨和电源线就比一台送货上门的 Dell 服务器还贵。其他人列举了具体失误——2002 年一度取消 Solaris on x86，以及因坚持要了解 Google 的服务器数量而错失 2002 年的合作；还有人认为 Sun 从来就没真正对经营生意感兴趣，并有人把 Sun 在互联网泡沫时期的估值与今天 AI 股票的高倍数相提并论。

**标签**: `#Sun Microsystems`, `#tech history`, `#systems engineering`, `#Solaris`, `#SPARC`

---

<a id="item-3"></a>
## [xAI 发布 Grok 4.7：参数量增加约四成，价格保持不变](https://x.ai/news/grok-4-7) ⭐️ 8.0/10

xAI 发布了 Grok 4.7，这是其前沿大模型的一次迭代更新，据称权重规模比 Grok 4.6 增加约 40%，而 API 价格保持不变，仍为每百万输入 token 2 美元、每百万输出 token 6 美元。该版本比原定时间推迟了近两周发布，并且恰好在传闻中 Anthropic 的 Opus 5.5 上线前一天推出。 这次发布说明前沿模型的竞争越来越依赖通过更大规模的训练榨取增量收益，而不是推出全新架构；xAI 选择维持价格不变，也意味着竞争对手将继续承受利润压力。对需要在 Grok、Claude/Opus 等顶级模型之间选择用于编程和智能体工作流的开发者来说，又多了一个可评估的选项，不过社区反馈显示这次提升未必具有决定性。 早期用户反馈称 Grok 4.7 明显比前代更慢、也更耗 token，一些人据此认为该模型在推理阶段消耗了额外算力以拉升基准测试排名。在本次可获得的材料中，xAI 并未公布详细的基准测试分数，而在模型更大的情况下维持价格不变，意味着单次请求的利润率被压缩。

hackernews · meetpateltech · 9月21日 15:50 · [社区讨论](https://news.ycombinator.com/item?id=49788838)

**背景**: Grok 是埃隆·马斯克旗下 xAI 打造的大语言模型系列，通过 X 平台、Grok 应用和 API 对外提供服务；Grok 4 于 2025 年 7 月发布，Grok 4.6 则在 2026 年 8 月推出，在 Artificial Analysis 智能指数上得分 61。xAI 已确认正在孟菲斯的 Colossus 2 超级集群上训练 Grok 5，包含约 6 万亿和 10 万亿参数两个混合专家（MoE）版本。“前沿大模型（Frontier LLM）”是业内对当前规模最大、能力最强模型的统称，而这类模型的基准测试分数一直存在争议，因为结果对提示词模板、数据污染、评分方式和基准饱和都非常敏感。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://datanorth.ai/news/xai-releases-grok-4-6">xAI releases Grok 4.6 flagship model - DataNorth AI</a></li>
<li><a href="https://arxiv.org/abs/2602.11286">[2602.11286] Grok in the Wild: Characterizing the Roles and ... SpaceXAI — Creators of Grok, the AI Chatbot Grok in the Wild: Characterizing the Roles and Uses of Large ... Grok 4 — Grokipedia Grok 3 — Grokipedia What Is Grok 5? xAI's 6T–10T Parameter Model - kie.ai</a></li>
<li><a href="https://johnplake.github.io/llm-consistency-survey/benchmark-reliability.html">Benchmark Reliability - LLM Consistency: A Literature Survey</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的整体情绪偏向怀疑：有评论者认为，发布推迟且在权重增加 40% 的情况下价格不变，说明 xAI 自己对结果并不满意；另一位用户则表示 Grok 4.6 在编程和智能体场景中已经达不到其“智能下限”，而 4.7 更慢、更贵。也有人对不断加快的发布节奏持乐观态度，期待 Grok 5 带来更大跃升；此外还有多位用户对基准测试分数是否仍能可靠反映真实能力表达了普遍质疑。

**标签**: `#AI`, `#LLM`, `#xAI`, `#Grok`, `#model release`

---

<a id="item-4"></a>
## [光纤被切断导致通信中断，FAA 暂停美国东海岸航班](https://www.reuters.com/world/us/faa-halts-some-us-east-coast-flights-due-communication-issues-2026-09-21/) ⭐️ 8.0/10

据路透社报道，一条光纤被切断导致通信系统中断后，美国联邦航空管理局（FAA）暂停了东海岸多个繁忙机场的航班。当运维人员尝试切换到备用线路时，却发现备用光纤本身也已断裂，从而使中断时间进一步延长。 这起事件表明，一处物理光缆故障就足以让主要航空枢纽的航班停摆，造成连锁性的经济损失，并引发公众对这套关键系统安全性的担忧。它也让人们质疑：关键的航空基础设施是否具备足够的冗余与监控能力，来抵御现实中常见的故障。 此次故障的关键在于：备用光纤在真正被启用之前就已经不可用，这意味着该隐患可能潜伏了数天、数周甚至更久，因为备用链路显然没有被持续监控。业界通常认为，对于重要业务来说仅有两条独立光纤路径是不够的，因为两条路径同时被切断是众所周知的风险。

hackernews · allanbreyes · 9月21日 18:41 · [社区讨论](https://news.ycombinator.com/item?id=49791509)

**背景**: 光纤承载了绝大多数长途通信，而它在物理上很容易遭到挖掘机施工、道路作业等地面活动的破坏。因此，关键业务网络通常会设计冗余路径和自动切换机制，以便主链路中断时把流量转移到备用线路。空中交通管制高度依赖管制中心、雷达站与塔台之间的这类通信链路；一旦链路失效，管制员就无法安全地调配飞机，FAA 便只能发布地面停飞指令，让飞机停留在机场。

**社区讨论**: 评论者的整体情绪相当悲观且批评性较强：有人指出，备用光纤直到切换时才发现已断裂，说明这套性命攸关的系统缺少健康状态监控；也有人认为两条独立路径根本不够，重叠切断是众所周知且本可管理的风险。还有人提到现实中误挖光缆有多常见，调侃说只要在野地里埋一小段光纤，一小时内就会有挖掘机司机出现；也有人指出，据称 FAA 一套新的空中交通管制系统正好在这段时间开始部署。

**标签**: `#aviation`, `#infrastructure`, `#fiber-optics`, `#reliability`, `#FAA`

---

<a id="item-5"></a>
## [TypeSafe AI 发布首个“System One”决策模型 Jev](https://simonwillison.net/2026/Sep/21/jev/) ⭐️ 8.0/10

TypeSafe AI 发布了 Jev，这是其称为“System One 模型”的全新模型类别中的首个产品：这类模型接受文本或半结构化状态作为输入，但不输出文本，而是返回浮点数形式的结果，包括置信度分数、是/否概率、多选项概率分布以及评分。Jev 的定价为每百万输入 token 0.042 美元，输出免费，比 OpenAI 的 GPT-5 Nano（每百万 token 0.05 美元）还要便宜。 这次发布可能预示着模型市场的一次分化：开发者不必再用庞大的生成式大模型处理所有任务，而是可以针对纯分类工作（如垃圾内容识别、打标签、优先级排序和搜索结果重排）调用快速、廉价的决策模型。如果这一思路被广泛接受，可能会改变 AI 的定价方式，以及它被嵌入普通软件流水线而非聊天界面的方式。 Jev 支持三类问题：名为“Noul”（即伯努利 Bernoulli）的是/否问题，返回 0 到 1 之间的置信度；选择问题，返回在所给选项上的概率分布；以及评分问题，返回沿数字区间取值的浮点数；针对同一份状态的多条问题会被并行计算。代价是不透明性——模型只返回一个数字，不提供自然语言解释，因此偏见与可解释性方面的担忧难以审计。

rss · Simon Willison · 9月21日 23:09

**背景**: 标准大语言模型输入文本、输出文本，而服务商通常对输出 token 的收费高于输入 token。“System One”这一名称源自心理学中的双过程理论：系统一（System 1）思维快速而直觉，系统二（System 2）则缓慢而刻意。TypeSafe AI 将 Jev 定位为一次“前沿智能函数调用”：输入非结构化状态，输出带类型的概率化决策，目标是直接由代码调用，而不是给人阅读。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">Introducing System One Models & Jev - TypeSafe AI Blog</a></li>
<li><a href="https://docs.typesafe.ai/concepts/system-one">System One - TypeSafe AI</a></li>
<li><a href="https://jevai.net/">Jev AI — Decisions at machine speed</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上认可这一思路，但对命名存在分歧：Maggie Appleton 在 X 上认为“decision models（决策模型）”比“System One models”更清晰，本文作者也表示赞同。在 Hacker News 上，TypeSafe 的 CEO 确认“Noul”是 Bernoulli（伯努利）的缩写；社区提出的主要担忧是，Jev 让机器学习更进一步走向不透明的黑箱，在诸如求职者排序等应用场景中存在偏见风险。

**标签**: `#LLM`, `#AI models`, `#decision models`, `#TypeSafe AI`, `#Jev`

---

<a id="item-6"></a>
## [Project Zero 详解悬空 COM 对象注册利用技术](https://projectzero.google/2026/09/windows-dangling-com.html) ⭐️ 8.0/10

Google 的 Project Zero 发布文章，描述了一种名为“悬空 COM 对象注册”（dangling COM object registrations）的新型 Windows 利用技术。文章指出，利用这类悬空注册的一个直接方法，就是向特权 COM 服务发送一个自定义 OBJREF，并在其中指定该悬空对象所对应的 CLSID。 COM 支撑着 Windows 上大量的进程间与服务间通信，因此一种能把失效注册重定向到特权服务的利用技术，可能为提权或沙箱逃逸提供新的原语。Project Zero 这类深度技术文章往往会同时影响微软的修补优先级，以及防御方对长期残留、难以追踪的注册表状态的加固思路。 其核心原语是向特权 COM 服务发送一个自定义 OBJREF，并指定悬空对象对应的 CLSID，从而让该服务去解析并激活一个受攻击者控制或影响的对象。该技术的前提是目标机器上确实存在悬空注册，例如对象已被注销、或拥有它的进程已经退出，但引用仍然可用；文章属于利用技术研究而非完整漏洞公告，因此现有摘要中没有涉及具体受影响版本、缓解措施以及微软的回应。

rss · Lobste.rs · 9月21日 18:21

**背景**: COM（Component Object Model，组件对象模型）是微软的二进制接口标准：组件被注册到 Windows 注册表中（例如 CLSID 相关键），客户端从注册表查找组件，跨进程或跨机器调用时则由 DCOM 使用 OBJREF 结构来传递对象引用。所谓“悬空”注册，指的是对象已被注销、或承载它的进程已经退出，但残留的注册表或引用信息仍能被解析出来。Project Zero 是 Google 于 2014 年 7 月公布的漏洞研究团队，专门在浏览器、移动操作系统和共享库等被广泛使用的软件中寻找并公开披露零日漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://projectzero.google/2026/09/windows-dangling-com.html">Windows Exploitation Techniques: Dangling COM Object Registrations</a></li>
<li><a href="https://learn.microsoft.com/en-us/windows/win32/com/registering-com-applications">Registering COM Applications - Win32 apps | Microsoft Learn</a></li>
<li><a href="https://en.wikipedia.org/wiki/Project_Zero">Project Zero - Wikipedia</a></li>

</ul>
</details>

**标签**: `#security`, `#windows`, `#exploitation`, `#vulnerability-research`, `#project-zero`

---

<a id="item-7"></a>
## [《你只拥有注意力》：一篇关于注意力经济的随笔](https://alicegg.tech/2026/09/21/attention) ⭐️ 7.0/10

一篇题为《你只拥有注意力》（Attention is all you have）的随笔发表在个人博客 alicegg.tech 上，作者认为现代应用和平台真正争夺并加以利用的稀缺资源不是数据或金钱，而是人类的注意力。这篇文章在 Hacker News 上获得了 552 分和 158 条评论，读者们在讨论中分享了关于无意识刷屏（doomscrolling）、戒断社交媒体以及尝试更有意识地消费媒体内容的亲身经历。 这篇随笔集中表达了人们日益增长的一种不安：数字健康正在被产品设计本身所牺牲，而 Hacker News 讨论的规模与质量说明，这种批评已经远远超出了小众的隐私或效率圈子。它的走红表明，人们对 RSS、有意识的浏览方式以及远离应用等替代方案仍有强烈需求，而这些主题正日益影响开发者和用户评估消费级产品的方式。 这篇文章是个人随笔与文化批评，而非技术发布或产品公告，因此没有基准测试或数据支撑，其价值主要体现在观点框架和由此引发的讨论上。标题显然是在戏仿 2017 年的 Transformer 论文《Attention Is All You Need》——该论文用自注意力机制取代循环结构，成为现代大语言模型的基础；颇具讽刺意味的是，如今大量掠夺注意力的推荐系统恰恰运行在这类模型之上。

hackernews · Lobste.rs · 9月21日 14:26 · [社区讨论](https://news.ycombinator.com/item?id=49787726)

**背景**: 所谓“注意力经济”，是指在内容无限供给的环境下，人类注意力才是有限且可变现的稀缺资源；依靠参与度而非订阅费驱动收入的平台会争夺这份注意力，通常手段是最大化用户停留时长和广告曝光。本文标题化用了 2017 年 Google 的 Vaswani 等人发表的论文《Attention Is All You Need》，该论文提出了完全基于注意力机制、摒弃循环和卷积的 Transformer 架构，而这一架构正是当今大语言模型的基础。理解这层文字游戏，有助于解释为何以工程师为主的 Hacker News 读者会对一篇谈专注与分心的随笔反应如此热烈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1706.03762">[1706.03762] Attention Is All You Need</a></li>
<li><a href="https://en.wikipedia.org/wiki/Attention_Is_All_You_Need">Attention Is All You Need - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者大多认同文章的判断：有人称戒掉社交媒体是今年最好的决定之一，有人承认自己常花数小时无意识地刷 Hacker News 和 YouTube 却几乎没留下印象，还有人建议在开机前先列好要做的事情。cube00 提出了一个值得注意的反驳，认为文章忽视了 Lycos、Yahoo!、MSN 等早期门户主页早已塞满标题党链接和广告；econ 则惋惜 Mosaic 的全文历史搜索和 Firefox 中的 RSS 支持相继消失，并将网站组织功能不再受重视归咎于广告收入的驱动。

**标签**: `#attention-economy`, `#digital-wellbeing`, `#social-media`, `#technology-criticism`, `#productivity`

---

<a id="item-8"></a>
## [Jev：只做判断不出文字的模型，数天催生近五百个项目](http://www.geekpark.net/news/370758) ⭐️ 7.0/10

智能家居平台 Home Assistant 上出现了一个名为 HA-Jev 的插件，它调用前 OpenAI 研究员 Diogo Almeida 发布的新模型 Jev，来判断洗衣机里的衣服是否被遗忘：模型不输出任何文字分析，只返回一个概率值，当置信度超过 0.8 时手机弹出取衣提醒。Jev 上线不过数天，全球开发者围绕它已经砸出近五百个开源项目，覆盖上下文压缩、手机自动化、数据库过滤和游戏智能体等场景。 这一项目尖锐地揭示了生成式 AI 的普遍低效：行业习惯动用百亿甚至千亿参数的庞然大物，去回答一个本只需要「判断」而非流畅文本的简单二值问题。如果 Jev 这类轻量判断模型被广泛接受，AI 智能体与自动化流程的成本和延迟都可能大幅下降，工程师设计系统的方式也会随之改变——不再什么问题都塞给一次完整的大模型调用。 据文章介绍，Jev 单次判断只需几十毫秒，成本约 0.000015 美元，并且完全不生成任何字符。文中给出的具体案例包括：把接近 100 万 token 的上下文在约 1 秒内压缩到 8.6 万 token；手机操作代理在真实 Android 手机上用 9 个步骤、21 秒完成一次 Uber 下单流程；以及用 13 分钟清洗 9081 条产品匹配数据，总账单仅 32 美分。

rss · 极客公园 · 9月21日 11:02

**背景**: Home Assistant 是一款免费开源的智能家居平台，充当本地智能家居中枢，可接入上千种设备与服务，并且不依赖厂商云端。而 GPT-5、Claude 这类大语言模型的设计目标是生成流畅的自然语言，因此用它们做一个「是/否」判断，意味着要为一长串推理过程付费，再写正则表达式之类的代码把答案抠出来。所谓「System One（系统一）」指的是人类快而直觉的思考模式，与缓慢审慎的推理相对，在这里指代一个只输出概率、不做自我解释的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Home_Assistant">Home Assistant</a></li>
<li><a href="https://en.wikipedia.org/wiki/Edge_AI">Edge AI</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#Home Assistant`, `#Edge AI`, `#Efficiency`

---

<a id="item-9"></a>
## [书评：《并行编程难吗，难的话该怎么办？》](https://ahelwer.ca/post/2026-09-21-concurrency-textbook/) ⭐️ 7.0/10

博客 ahelwer.ca 发表了一篇书评，评述 Paul E. McKenney 的免费教材《Is Parallel Programming Hard, And, If So, What Can You Do About It?》，梳理了书中讨论的并发难题以及作者推荐的实用解决技术。该文章被归入 parallel-programming、concurrency、systems 等标签，并已在 Lobste.rs 上引发讨论。 这本常被称为“perfbook”的教材，是少数免费且持续更新的共享内存并行编程参考书之一，因此一篇详细书评能帮助开发者判断它是否值得投入时间阅读。随着 CPU 核心数不断增加，书中所描述的并发陷阱会影响所有编写性能敏感系统代码的人。 该书由 kernel.org 免费发布，提供双栏、单栏和电子书版 PDF，当前版本标注为 v2026.06.21a；较早的 v2023.06.11a 版本也以 arXiv 论文 1701.00854 的形式存档。作者明确表示，本书的目的是帮助读者“在不把自己逼疯的前提下”编写共享内存并行程序，并强调书中的内容只是进一步研究的基础，而非一座已经建成的教堂。

rss · Lobste.rs · 9月21日 14:28

**背景**: 本书作者 Paul E. McKenney 是资深的 Linux 内核开发者，以创建并维护 RCU（read-copy-update，读-拷贝-更新）这一内核中广泛使用的同步机制而闻名。并发指的是多个线程或核心同时访问同一块内存，它出了名地难以驾驭，因为数据竞争、死锁等故障依赖时序，很难复现和调试。该书涵盖锁、内存屏障、原子操作、RCU 类技术以及验证工具，已成为系统程序员常用的免费参考书。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html">Is Parallel Programming Hard, And, If So, What Can You Do About It?</a></li>
<li><a href="https://arxiv.org/abs/1701.00854">[1701.00854] Is Parallel Programming Hard, And, If So, What Can You Do About It? (Release v2023.06.11a)</a></li>

</ul>
</details>

**标签**: `#parallel-programming`, `#concurrency`, `#textbook-review`, `#systems`, `#software-engineering`

---