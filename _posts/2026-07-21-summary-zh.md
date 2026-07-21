---
layout: default
title: "Horizon Summary: 2026-07-21 (ZH)"
date: 2026-07-21
lang: zh
---

> 从 90 条内容中筛选出 16 条重要资讯。

---

1. [4 家编码 Agent 供应商发现 7 个沙箱逃逸漏洞](#item-1) ⭐️ 9.0/10
2. [Rust 在 Morello 上实现全时内存安全，甚至包括 unsafe 代码](#item-2) ⭐️ 9.0/10
3. [中国的开放权重 AI 模型挑战西方专有巨头](#item-3) ⭐️ 8.0/10
4. [黑客清除罗马尼亚土地注册数据库](#item-4) ⭐️ 8.0/10
5. [LED 拯救夜空的潜力](#item-5) ⭐️ 8.0/10
6. [编程代理使家庭设备逆向工程成本低廉](#item-6) ⭐️ 8.0/10
7. [Ben Thompson 提议立法：允许训练数据收集，禁止蒸馏禁令](#item-7) ⭐️ 8.0/10
8. [OpenAI 2022 年邮件曝光：计划用开源模型打压竞争对手](#item-8) ⭐️ 8.0/10
9. [Filippo Valsorda 提出不透明且可互操作的通行密钥记录格式](#item-9) ⭐️ 8.0/10
10. [Linux 内核 0day 漏洞利用之旅：从受限 UAF 到物理内存读写](#item-10) ⭐️ 8.0/10
11. [基于 LLM 的验证消除 Linux nftables 中的漏洞](#item-11) ⭐️ 8.0/10
12. [月泉仿生获数亿元融资，仿生灵巧手万台量产](#item-12) ⭐️ 7.0/10
13. [青心意创推出毛绒人形机器人 Amoo 及 Dino OS 操作系统](#item-13) ⭐️ 7.0/10
14. [清华系量子计算企业「两仪万象」获数亿融资，打破原子捕获世界纪录](#item-14) ⭐️ 7.0/10
15. [博顿光电获超亿元融资，垄断超导及光通信离子束装备](#item-15) ⭐️ 7.0/10
16. [Inkling：面向微调的 975B 开源多模态模型](#item-16) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [4 家编码 Agent 供应商发现 7 个沙箱逃逸漏洞](https://www.pillar.security/blog/the-week-of-sandbox-escapes) ⭐️ 9.0/10

安全研究人员在四家不同供应商的编码 Agent 中发现了七个沙箱逃逸漏洞。 这些漏洞表明编码 Agent 存在系统性安全缺陷，可能在 AI 辅助开发环境中造成未经授权的代码执行和数据泄露风险。 具体供应商和技术细节尚未披露，但这一发现凸显了 AI 编码工具中强化沙箱隔离的必要性。

rss · Lobste.rs · 7月20日 14:33

**背景**: 编码 Agent 是 AI 驱动的工具，可在受控环境中（即沙箱）协助开发者生成、编辑或执行代码，以防止恶意操作。沙箱逃逸漏洞允许攻击者突破这一受限环境并在主机系统上执行任意代码，可能导致严重的安全事件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/components-of-a-coding-agent">Components of A Coding Agent - by Sebastian Raschka, PhD</a></li>
<li><a href="https://www.csoonline.com/article/4198993/servicenows-sandbox-escape-rce-hole-now-exploited-in-the-wild.html">ServiceNow’s sandbox escape RCE hole now exploited in the ...</a></li>

</ul>
</details>

**标签**: `#security`, `#sandbox-escape`, `#vulnerabilities`, `#coding-agents`, `#AI`

---

<a id="item-2"></a>
## [Rust 在 Morello 上实现全时内存安全，甚至包括 unsafe 代码](https://drops.dagstuhl.de/storage/00lipics/lipics-vol263-ecoop2023/LIPIcs.ECOOP.2023.39/LIPIcs.ECOOP.2023.39.pdf) ⭐️ 9.0/10

一篇研究论文表明，将 Rust 与搭载 CHERI 的 Morello 架构结合，利用硬件能力即使在`unsafe`代码块中也能实现全面的内存安全。 这一结合可能大幅增强软件安全性，消除 Rust 中高风险 unsafe 代码的内存安全漏洞，将对未来的系统设计和语言实现产生影响。 该工作展示了 CHERI 基于能力的保护可以在 Rust 的静态检查被绕过时强制执行时空内存安全，但需要修改过的 Rust 编译器和运行时。

rss · Lobste.rs · 7月20日 14:33

**背景**: Morello 是 Arm 推出的一种原型架构，集成了 CHERI（能力硬件增强 RISC 指令），通过能力（capability）提供硬件强制的内存保护。Rust 通过所有权和借用机制确保内存安全，但`unsafe`代码块会禁用这些检查。该论文提出将两者结合，即使在 unsafe 代码中也能实现全时内存安全。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.arm.com/architecture/cpu/morello">Arm Morello Program</a></li>
<li><a href="https://www.cl.cam.ac.uk/research/security/ctsrd/cheri/">Capability Hardware Enhanced RISC Instructions (CHERI)</a></li>

</ul>
</details>

**标签**: `#rust`, `#memory-safety`, `#morello`, `#cheri`, `#secure-systems`

---

<a id="item-3"></a>
## [中国的开放权重 AI 模型挑战西方专有巨头](https://werd.io/american-ai-is-locked-down-and-proprietary-its-losing/) ⭐️ 8.0/10

中国公司正越来越多地发布高性能的开放权重 AI 模型，这些模型正在被初创企业和公司采用，威胁着 OpenAI 和 Anthropic 等专有模型的市场份额。 这种转变降低了 AI 部署成本，支持定制化，并可能使 AI 开发民主化，从而可能改变全球 AI 的力量平衡和创新格局。 开放权重模型可免费使用和微调，但需要自行托管，会产生推理成本；它们并非完全开源，训练数据和代码通常仍为私密。

hackernews · r/LocalLLaMA · benwerd · 7月20日 14:21 · [社区讨论](https://news.ycombinator.com/item?id=48979269)

**背景**: 开放权重模型提供公开的神经网络参数，允许用户在自己的硬件上运行模型。这与隐藏模型内部结构并按使用量计费的专有 API 形成对比。历史上，像 Linux 和个人电脑这样的开放生态系统曾颠覆封闭、高利润的系统，许多人认为在 AI 领域这一模式正在重演，中国正引领开放权重潮流。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>

</ul>
</details>

**社区讨论**: 许多评论者认为开放权重将长期胜出，引用历史模式和成本优势，但有人对广泛采用中国模型的说法提出质疑，指出美国模型仍占主导地位且硬件成本依然高昂。

**标签**: `#open-weights`, `#AI`, `#China`, `#business-strategy`, `#competition`

---

<a id="item-4"></a>
## [黑客清除罗马尼亚土地注册数据库](https://news.risky.biz/risky-bulletin-hacker-wipes-romanias-entire-land-registry-database/) ⭐️ 8.0/10

一名黑客清除了罗马尼亚的土地注册数据库，但离线备份避免了数据完全丢失；该机构正在重建网络，并计划于 7 月 22 日前将应用迁移到政府云平台。 此事件暴露了政府 IT 基础设施的重大漏洞，这些漏洞因腐败和裙带关系而加剧，同时凸显了为国家数据库保留离线备份以防止灾难性社会后果的重要性。 安全公司 KELA 确认黑客是来自阿尔及利亚的 Zakaria Mahdjoub；尽管黑客声称删除了备份，但离线副本得以幸存，该机构正在特别电信服务的协调下迁移至罗马尼亚政府云。

hackernews · speckx · 7月20日 13:28 · [社区讨论](https://news.ycombinator.com/item?id=48978605)

**背景**: 罗马尼亚土地注册局（ANCPI）是一个关键的国家数据库，包含对法律和经济交易至关重要的财产所有权和地籍记录。该系统长期受腐败困扰，IT 合同授予缺乏安全专业知识的裙带关系者。若备份失效，此次入侵可能导致房地产交易瘫痪并动摇产权制度。

**社区讨论**: 评论者对离线备份挽救注册数据表示庆幸，但指出系统性腐败和裙带关系是安全薄弱的根本原因。他们还提到黑客被确认为阿尔及利亚人，并类比了韩国数据中心类似事件的教训，强调政府 IT 不安全的全球性风险。

**标签**: `#cybersecurity`, `#critical-infrastructure`, `#data-breach`, `#government-IT`, `#corruption`

---

<a id="item-5"></a>
## [LED 拯救夜空的潜力](https://spectrum.ieee.org/led-light-pollution) ⭐️ 8.0/10

黑客新闻讨论探讨了如何通过适当的 LED 工程设计（如自适应照明和减少眩光）大幅减少光污染并保护夜空。 光污染破坏生态系统和人类健康，并遮蔽夜空；改进的 LED 设计为减轻这些广泛影响提供了实际解决方案。 关键的技术细节包括使用存在传感器实现自适应照明、遮蔽灯光以减少眩光，并实现均匀照明而不向上散射光线。

hackernews · defrost · 7月20日 13:07 · [社区讨论](https://news.ycombinator.com/item?id=48978350)

**背景**: 光污染是过多人造光导致夜空变亮的现象，通常来自设计不良的户外照明。LED 比传统灯具更节能、更可控，但若设计不当，可能加剧眩光和天空辉光。波特尔暗空分类法从 1（最暗）到 9（市中心）衡量夜空亮度。

**社区讨论**: 评论者分享了个人经历：温室毁坏夜空、带有传感器的自适应公园照明、需要更好的减少眩光标准，以及实施不当的矩形照明导致人行道变暗。总体情绪是对当前做法感到沮丧，但对精心设计的 LED 持乐观态度。

**标签**: `#light-pollution`, `#LED-lighting`, `#night-sky`, `#environment`, `#sustainability`

---

<a id="item-6"></a>
## [编程代理使家庭设备逆向工程成本低廉](https://simonwillison.net/2026/Jul/20/cheap-reverse-engineering/#atom-everything) ⭐️ 8.0/10

编程代理大幅降低了逆向工程和自动化家庭设备的成本与心理负担，使得编写可丢弃的自动化代码变得可行。 这改变了个人自动化的投入产出比，鼓励人们在没有长期维护担忧的情况下动手改造，可能催生一波新的自制智能设备集成。 自主 AI 编程代理能够独立生成、测试和迭代代码，使得逆向工程变成一种低成本的、可丢弃的工作；即使 API 失效，代码也可以无遗憾地丢弃并重新生成。

rss · Simon Willison · 7月20日 19:24

**背景**: 编程代理是一种自主 AI 系统，能在极少人工干预下规划、编写、测试和修改代码，不同于需要逐步指导的传统编程助手。它们支持快速原型和可丢弃代码，这与 AI 辅助编程降低软件创作成本的趋势相符。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cloud.google.com/discover/what-is-agentic-coding">What is agentic coding? How it works and use cases | Google Cloud</a></li>
<li><a href="https://www.openhands.dev/blog/what-are-coding-agents">What Are Coding Agents? A Developer's Guide to Agentic Coding (2026) | Jun 02, 2026</a></li>

</ul>
</details>

**标签**: `#reverse engineering`, `#coding agents`, `#home automation`, `#software development`, `#cost reduction`

---

<a id="item-7"></a>
## [Ben Thompson 提议立法：允许训练数据收集，禁止蒸馏禁令](https://simonwillison.net/2026/Jul/20/afraid-of-chinese-models/#atom-everything) ⭐️ 8.0/10

Ben Thompson 提出了一项美国立法改革的两部分内容：明确将训练数据收集视为合理使用，并禁止服务条款中限制模型蒸馏的规定，旨在促进创新，帮助美国开放模型与中国模型竞争。 该提议解决了 AI 实验室在训练使用未授权数据的同时却禁止蒸馏的虚伪做法，并可能消除阻碍 AI 进步的法律障碍。此举还可能平衡与中国 AI 模型的竞争环境，后者受益于宽松政策和大规模开源发布。 该法律将明确禁止公司通过服务条款禁止蒸馏，因为蒸馏仅涉及查询 API。此外，阿里巴巴发布了 Qwen 3.8 Max，一个具有 2.4 万亿参数的开源权重模型，可能受到了习近平鼓励开源讲话的影响。

rss · Simon Willison · 7月20日 17:09

**背景**: 知识蒸馏是一种机器学习技术，其中较小的“学生”模型通过 API 查询等方式从较大的“教师”模型学习。在 AI 行业中，一些公司在其服务条款中禁止蒸馏，但他们自己的模型却依赖合理使用原则，在海量有版权的数据上进行训练。这造成了有争议的双重标准。合理使用是一种法律原则，允许为了研究或教育等目的，在未经许可的情况下有限地使用受版权保护的材料。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/knowledge-distillation">What is Knowledge distillation? | IBM</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qwen3.8-Max">Qwen3.8-Max</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#distillation`, `#open source AI`, `#fair use`, `#competition`

---

<a id="item-8"></a>
## [OpenAI 2022 年邮件曝光：计划用开源模型打压竞争对手](https://simonwillison.net/2026/Jul/20/sam-altman/#atom-everything) ⭐️ 8.0/10

在马斯克诉奥特曼案中披露的一封 2022 年邮件显示，OpenAI 曾考虑发布一个具备 GPT-3 能力的开源语言模型，以压制竞争对手并增加新 AI 创业公司融资难度。 这一揭露暴露了领先 AI 公司如何策略性地将开源发布作为竞争壁垒，引发了关于开源贡献真实意图及其对 AI 生态系统影响的伦理问题。 邮件提到发布一个大致具有 GPT-3 能力、可在消费级硬件上本地运行的模型，并特别指出 Stability（很可能指 Stability AI）作为要抢先的潜在竞争对手。

rss · Simon Willison · 7月20日 03:47

**背景**: GPT-3 是 OpenAI 开发的大型语言模型，以文本生成能力著称。在 2022 年 10 月这封邮件发出时，Stability AI 因其开源图像模型 Stable Diffusion 而备受关注，并预期将进入语言模型领域推出 StableLM。该邮件作为马斯克诉奥特曼案的一部分被披露，该案涉及 OpenAI 发展方向争议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.digitalogy.co/blog/top-open-source-large-language-models/">Top Open Source Large Language Models in 2025 | Digitalogy Blog</a></li>
<li><a href="https://openai.com/">OpenAI | Research & Deployment</a></li>

</ul>
</details>

**标签**: `#ai-ethics`, `#sam-altman`, `#generative-ai`, `#open-source`

---

<a id="item-9"></a>
## [Filippo Valsorda 提出不透明且可互操作的通行密钥记录格式](https://words.filippo.io/passkey-record/) ⭐️ 8.0/10

密码学专家 Filippo Valsorda 提出了一种新的通行密钥记录格式，该格式对依赖方不透明且可跨平台互操作，能够在无需向服务器泄露用户凭据的情况下实现安全的跨平台认证。 该提案解决了通行密钥生态中的一个关键缺口：缺乏一种既能保护隐私和安全又标准化的可移植记录格式。它可能通过确保用户在不牺牲安全性或隐私的情况下在不同服务提供商之间自由迁移凭据，从而极大地推动无密码认证的采用。 该格式利用了成熟的密码学原语，如 HPKE 和基于 OPRF 的 OPAQUE 协议，以确保记录被加密且只能用用户持有的秘密解密，使服务器无法使用。它还包括密钥恢复和与现有 FIDO2 凭据互操作的机制。

rss · Lobste.rs · 7月20日 22:46

**背景**: 通行密钥是一种基于 FIDO2 和 WebAuthn 的无密码认证方法，使用公钥密码学替代共享秘密。OPAQUE 协议是一种口令认证密钥交换协议，允许客户端在不透露口令的情况下向服务器进行身份认证，使用不经意伪随机函数（OPRF）。目前，通行密钥记录通常存储在特定平台的孤岛中（如 iCloud 钥匙串、Google 密码管理器），使得跨平台互操作变得困难。Valsorda 的提案旨在创建一种既对服务器不透明又能在不同系统之间互操作的记录格式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Passkeys">Passkeys</a></li>
<li><a href="https://blog.cloudflare.com/opaque-oblivious-passwords/">OPAQUE : The Best Passwords Never Leave your Device</a></li>

</ul>
</details>

**标签**: `#passkeys`, `#cryptography`, `#OPAQUE`, `#authentication`, `#interoperability`

---

<a id="item-10"></a>
## [Linux 内核 0day 漏洞利用之旅：从受限 UAF 到物理内存读写](https://1day.dev/posts/linux-kernel-0day.html) ⭐️ 8.0/10

一篇详细的技术文章展示了如何将 Linux 内核中一个受限的 use-after-free 漏洞提升为强大的物理内存读写原语，实现完全的任意物理内存访问。 物理内存访问能够绕过内核保护实现完整的系统控制；这项研究揭示了即使受限的 UAF 漏洞也可能导致严重攻击，为攻击者和防御者都提供了宝贵的见解。 文章可能逐步介绍了漏洞利用技术，包括内核堆操纵和地址空间布局分析，以将一个受限的 UAF 转化为不受限的物理内存读写能力。

rss · Lobste.rs · 7月20日 20:15

**背景**: use-after-free（UAF）是一种内存破坏漏洞，即内存被释放后仍被引用，导致不稳定或可利用的条件。物理内存读写原语允许直接访问物理地址，绕过虚拟内存保护，从而修改关键内核数据。Linux 内核是操作系统的核心，管理硬件和进程，因此内核级别的漏洞利用可能危及整个系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://plackyhacker.github.io/kernel/physical-read-write.html">Physical Memory Read/Write Primitive</a></li>
<li><a href="https://cybersecuritynews.com/use-after-free-vulnerability/">What is Use-After-Free Vulnerability? - Impact and Mitigation</a></li>
<li><a href="https://learn.snyk.io/lesson/use-after-free/">Use after free vulnerability | Tutorial & Examples | Snyk Learn Exploit Published for Linux Kernel nf_tables CVE-2026-23111 CVE-2026-50688: Windows 10 1607 Use-After-Free Vulnerability Demystifying Use-After-Free Vulnerabilities: A Deep Dive into ... 16-Year-Old Linux KVM Flaw Lets Guest VMs Escape to Host on ...</a></li>

</ul>
</details>

**标签**: `#linux-kernel`, `#exploitation`, `#use-after-free`, `#security`, `#vulnerability-research`

---

<a id="item-11"></a>
## [基于 LLM 的验证消除 Linux nftables 中的漏洞](https://www.basis.ai/blog/verified-nftables/) ⭐️ 8.0/10

Basis AI 详细介绍了他们如何使用基于 LLM 的验证来形式化验证 Linux 内核的 nftables 网络栈，识别并消除了这一关键子系统中的漏洞。 将 LLM 应用于广泛使用的 Linux 内核组件的形式化验证，可以显著增强网络安全和可靠性，展示了 AI 在系统软件保障方面的新用途。 该方法利用大型语言模型生成和检查形式化规范，但博客文章未披露具体的性能指标或发现的漏洞数量。

rss · Lobste.rs · 7月20日 13:57

**背景**: nftables 是 Linux 内核中现代的数据包过滤和分类框架，取代了 iptables。形式化验证通过数学方法证明软件的正确性，这是一个严格但传统上劳动密集的过程。基于 LLM 的验证是一种新兴技术，它利用语言模型自动完成部分形式化推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nftables">Nftables</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification</a></li>

</ul>
</details>

**标签**: `#LLM`, `#verification`, `#Linux`, `#networking`, `#bug-detection`

---

<a id="item-12"></a>
## [月泉仿生获数亿元融资，仿生灵巧手万台量产](https://36kr.com/p/3899174356387718?f=rss) ⭐️ 7.0/10

月泉仿生完成数亿元 Pre-A+轮融资，由长发基金、华控基金等投资，用于提升产能和研发。公司已实现仿生灵巧手万台量产并获得过亿元订单。 这标志着灵巧手从实验室走向量产商业化，有望解决传统刚性手性能、成本和可靠性难以兼顾的瓶颈，加速人形机器人落地。 其 Y-Hand M1 重仅 299.7 克，集成 26 个自由度、握力 200 牛；M2 拥有全球最高的 38 自由度。另提供负载 50 公斤、寿命百万次的工业刚性手，以及覆盖 4–22mm 的全自研电机。

rss · 36氪 · 7月21日 00:00

**背景**: 传统机器人手多为刚性结构，难以柔顺操作易损物品。2017 年吉林大学任雷教授首创“仿生拉压体机器人”理论，模仿人体骨骼肌肉协同工作，硬质构件承压、柔性构件承拉，实现类人柔顺与力量兼备的操控。月泉仿生基于该理论构建了从电机到人形整机的全栈产品线。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.jlu.edu.cn/info/1306/59161.htm">吉林大学仿生科学与工程学院任雷教授国际首创仿生拉压体机器人理论与...</a></li>
<li><a href="https://baike.baidu.com/item/仿生拉压体机器人理论与技术/67555929">仿生拉压体机器人理论与技术_百度百科</a></li>

</ul>
</details>

**标签**: `#robotics`, `#bionic hand`, `#humanoid robot`, `#biomimetic`, `#startup financing`

---

<a id="item-13"></a>
## [青心意创推出毛绒人形机器人 Amoo 及 Dino OS 操作系统](https://36kr.com/p/3903761449617027?f=rss) ⭐️ 7.0/10

青心意创发布了 80 厘米高的毛绒人形机器人 Amoo，以及 Dino OS 统一操作系统，旨在通过三层架构（Infra、Brain、Module）和双脑交互设计解决机器人软件碎片化问题。 此举切中了消费级机器人缺乏统一操作系统、难以稳定持续升级的痛点，有望推动行业从硬件比拼转向人机交互体验的竞争，让开发者能更专注于情感交互而非底层重复建设。 Dino OS 采用零拷贝数据共享和算力隔离技术保障安全关键任务。其‘双脑闭环’设计由负责场景理解和任务拆解的‘慢脑’、提供即时社交反馈的‘快脑’，以及实时运动控制的‘小脑’组成。

rss · 36氪 · 7月20日 09:12

**背景**: 传统机器人软件开发碎片化严重，开发者常需拼凑感知、决策、控制等不同模块，导致系统不稳定且维护成本高。ROS（机器人操作系统）虽作为中间件被广泛使用，但未能完全统一硬件抽象与实时控制。自研 OS 如 Dino OS 试图提供类似 PC 时代的统一平台，有望成为行业标准，降低开发门槛。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.esbf.org/wp-content/uploads/2014/11/201411_WHX.pdf">A Roadmap for U.S. Robotics</a></li>

</ul>
</details>

**标签**: `#robotics`, `#operating systems`, `#AI`, `#humanoid robots`, `#product launch`

---

<a id="item-14"></a>
## [清华系量子计算企业「两仪万象」获数亿融资，打破原子捕获世界纪录](https://36kr.com/p/3903756643255940?f=rss) ⭐️ 7.0/10

清华系量子计算公司两仪万象完成由君联资本领投的数亿元 A+轮融资。该团队利用光镊技术成功捕获 11000 个原子，打破了此前由加州理工大学保持的 6100 个原子世界纪录。 这一突破及融资彰显了中国在中性原子量子计算竞争中的上升势头，该路线有望实现大规模量子比特。这体现了投资者信心，并可能加速大规模纠错量子计算机的研发。 该公司采用光镊囚禁超冷铷原子，通过快速 FPGA 动态重排、里德堡激发和全连通两比特门操控，单双比特门保真度达全球顶尖水平。自研了量子纠错解码器、集成原子源和光学超表面，部分元件产品已产生营收。

rss · 36氪 · 7月20日 09:08

**背景**: 中性原子量子比特通过光镊捕获铷等原子，具有长相干时间和可扩展性。里德堡态是原子的高激发态，可实现强相互作用用于量子门操控。量子纠错解码器用于解读错误症状并纠正量子比特，是克服退相干的关键。该技术路线被视为实现大规模量子计算的可行路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/里德伯原子">里德伯原子 - 维基百科，自由的百科全书</a></li>
<li><a href="https://baike.baidu.com/item/超表面/17590482">超表面_百度百科</a></li>

</ul>
</details>

**标签**: `#quantum computing`, `#startup funding`, `#atomic technology`, `#world record`, `#Tsinghua University`

---

<a id="item-15"></a>
## [博顿光电获超亿元融资，垄断超导及光通信离子束装备](https://36kr.com/p/3903739699005058?f=rss) ⭐️ 7.0/10

中国离子束设备制造商博顿光电完成了超亿元人民币的 B+轮融资。该公司是国内唯一具备 REBCO 高温超导带材 IBAD 离子源及全套镀膜设备供货能力的企业，市占率接近 100%，并已在光通信和量子计算领域与头部客户实现合作。 此次融资凸显国产离子束技术在核聚变、AI 驱动光通信和量子计算等领域的关键作用，原子级精密加工正成为必需。它也表明中国在减少对进口高端制造设备依赖方面取得进展。 博顿的离子源已通过国外头部半导体设备厂商验证，公司已承担四项国家级重大科技专项。其年营收增长率超过 50%，产品用于光学滤光片、MEMS 和先进封装等领域。

rss · 36氪 · 7月20日 08:51

**背景**: 离子束加工利用聚焦离子束进行超高精度材料去除或沉积，可达亚纳米精度。IBAD（离子束辅助沉积）对于生长 REBCO 高温超导带材所需的氧化镁种子层等缓冲层至关重要，这类带材可用于聚变反应堆的高场磁体。在光通信中，离子束刻蚀和沉积用于制造铌酸锂波导等高性能薄膜器件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/离子束辅助沉积">离子束辅助沉积 - 维基百科，自由的百科全书</a></li>
<li><a href="https://dgjsxb.ces-transaction.com/fileup/HTML/2024-21-6591.htm">REBCO高温超导多芯带材的制备技术及性能研究进展</a></li>
<li><a href="https://www.eet-china.com/mp/a428260.html">薄 膜 铌 酸 锂 光 波 导 器件-电子工程专辑</a></li>

</ul>
</details>

**标签**: `#ion-beam`, `#superconductors`, `#optical-communication`, `#funding`, `#manufacturing-technology`

---

<a id="item-16"></a>
## [Inkling：面向微调的 975B 开源多模态模型](https://www.producthunt.com/products/tinker-2) ⭐️ 7.0/10

一个名为 Inkling 的 9750 亿参数开源权重多模态模型在 Product Hunt 上发布，专为微调应用而设计。 开源权重的大型模型使研究人员和开发者能够针对特定任务定制先进 AI，推动了多模态 AI 的民主化。9750 亿参数的规模使其成为最大的公开可用模型之一。 该模型是开源权重而非完全开源，即仅训练好的参数公开，训练代码和数据可能不公开。其巨大规模可能需要高效的微调技术。该 Product Hunt 列表缺乏技术深度、基准测试或原始文档。

rss · Product Hunt · 7月20日 04:25

**背景**: 开源权重指的是公开提供已训练模型的参数，但不一定公开训练代码或数据，相比闭源模型提供了更多透明度。多模态模型能够处理并整合文本、图像、音频等不同类型的数据。微调是指利用额外数据将预训练模型适配到特定任务的过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multimodal_model">Multimodal model</a></li>
<li><a href="https://www.ai21.com/glossary/foundational-llm/open-weights-model/">What is an Open-Weights Model? | AI21</a></li>

</ul>
</details>

**标签**: `#open-source`, `#multimodal`, `#AI`, `#large-language-model`, `#fine-tuning`

---