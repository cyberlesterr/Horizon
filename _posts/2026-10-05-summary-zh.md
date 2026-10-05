---
layout: default
title: "Horizon Summary: 2026-10-05 (ZH)"
date: 2026-10-05
lang: zh
---

> 从 34 条内容中筛选出 8 条重要资讯。

---

1. [Strata 在 RTX 4090 上以 100+ tokens/s 运行 125B Qwen3.8-Flash-Next](#item-1) ⭐️ 8.0/10
2. [为什么更多开发者不“使用平台”？](#item-2) ⭐️ 8.0/10
3. [爱好者用廉价 eBay 矿机 FPGA 运行 Qwen3.5 9B/27B INT4 大模型](#item-3) ⭐️ 8.0/10
4. [Jev 点燃「决策模型」新品类，中国团队扎堆开源跟进](#item-4) ⭐️ 7.0/10
5. [Tavus 发布 Griffin：实时 AI 数字人骗过近半数测试者](#item-5) ⭐️ 7.0/10
6. [Claude Code 的 Mods 机制把终端变成了可扩展的游乐场](#item-6) ⭐️ 7.0/10
7. [用 SSH 和 nginx 搭建自托管 HTTP 隧道](#item-7) ⭐️ 7.0/10
8. [魔改 Go 编译器，加速 IPv4 到 IPv6 地址映射](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Strata 在 RTX 4090 上以 100+ tokens/s 运行 125B Qwen3.8-Flash-Next](https://github.com/Niko1221/Strata) ⭐️ 8.0/10

一个名为 Strata 的新推理栈由 Niko1221 发布在 GitHub 上，声称可以在单张消费级 RTX 4090 上以每秒 100 个以上 token 的速度运行 125B 参数的 Qwen3.8-Flash-Next 模型，并且已有用户报告在同一块显卡上实测到 124 tokens/s。Strata 被描述为一个专门为单一模型打造的推理引擎，在本地主机上提供兼容 OpenAI/Anthropic 的 API，并可选支持图像输入。 如果这些说法成立，那么运行 125B 级混合专家模型的硬件门槛将从租用数据中心 GPU 降到一台桌面游戏 PC，这对本地大模型社区而言是一次重大转变。不过这股热情也受到质疑的抑制：人们担心这种速度是以模型质量为代价换来的，因为低于 4-bit 的量化普遍被认为会损害精度。 Qwen3.8-Flash-Next 是一个 125B 的 MoE 模型，每个 token 仅激活约 6B 参数，另外还带有 51B 的 n-gram 嵌入和 4B 的 MTP 组件，这正是低内存推理得以可行的重要原因。需要注意的是，有报道称在游戏 PC 上运行大约需要 64GB 系统内存，而且 Strata 是高度针对单一模型定制的，并非通用推理运行时。

hackernews · snehesht · 10月4日 12:51 · [社区讨论](https://news.ycombinator.com/item?id=49953495)

**背景**: 大语言模型通常以 16 位或 8 位精度存储，而量化技术会把权重压缩到 4 位甚至更低，从而让超大模型塞进有限的显存——一个 FP16 下需要 140GB 的 70B 模型，在 4-bit 下可以降到约 35GB。混合专家（MoE）架构进一步帮助了这一点，因为每个 token 只使用一小部分参数，所以名义上 125B 的模型实际运行速度远快于其总规模所暗示的水平。Strata 是与 llama.cpp 以及较新的 ds4 等项目同场竞技的成员之一，目标都是让这个特定的 Qwen 模型在消费级硬件上高效运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Niko1221/Strata">GitHub - Niko1221/ Strata : Qwen3.8-Flash-Next (125B MoE) on...</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-Flash-Next">Qwen / Qwen 3 . 8 - Flash - Next · Hugging Face</a></li>
<li><a href="https://www.youtube.com/watch?v=m0VHx73SAG0">The New Way to Run 125 B Models 6× Faster Than... - YouTube</a></li>

</ul>
</details>

**社区讨论**: 社区情绪褒贬不一：一位用户证实了在 RTX 4090 上实测 124 tokens/s 的真实性能，而另一位用户在 50 张图片的视觉基准测试中发现，在完全相同的 GGUF 与视觉适配器权重下，Strata 的中位定位误差（154.8 像素）是 llama.cpp（46.5 像素）的三倍多，引发了对基准可靠性的怀疑。多位评论者对低于 4-bit 的量化表示怀疑，也有人指出自己已经在 RTX 6000 Pro 上用 ds4 的 4-bit 量化取得了不错的效果，因此质疑 Strata 的取舍是否值得。

**标签**: `#local-llm-inference`, `#quantization`, `#Qwen`, `#consumer-gpu`, `#inference-optimization`

---

<a id="item-2"></a>
## [为什么更多开发者不“使用平台”？](https://nolanlawson.com/2026/10/03/why-dont-more-developers-use-the-platform/) ⭐️ 8.0/10

Nolan Lawson 的文章探讨了为什么开发者更青睐 React 等框架而非原生 Web 平台 API，并引发了 Hacker News 上关于开发者体验、Web 组件、浏览器 API 质量以及 LLM 编码偏见的丰富讨论。

hackernews · vinhnx · 10月4日 04:10 · [社区讨论](https://news.ycombinator.com/item?id=49950554)

**标签**: `#web-platform`, `#javascript`, `#frontend-frameworks`, `#web-components`, `#developer-experience`

---

<a id="item-3"></a>
## [爱好者用廉价 eBay 矿机 FPGA 运行 Qwen3.5 9B/27B INT4 大模型](https://www.reddit.com/gallery/1wxken1) ⭐️ 8.0/10

一位 Reddit 用户将 Qwen3.5 架构直接实现在 FPGA 逻辑（fabric）中，并在 eBay 上淘来的二手矿机硬件上运行 9B 与 27B 的 INT4 模型，例如售价 280 美元的 SQRL FK33（XCVU33P，8GB HBM2）以及 375 美元的 SQRL Jungle Cat 板卡。在两张运行于 75MHz 的 FK33 上，Qwen3.5-9B INT4 模型可达到约每秒 2 个 token；作者表示若要提升时钟频率，还需进一步做 RTL 优化并提高核心电压。 这表明前沿水平的 9B-27B 大模型可以在几百美元的退役加密货币矿机 FPGA 上运行，为本地推理提供了一条绕开昂贵 GPU 及其显存瓶颈的路径。该项目同时说明，借助 AI 编程助手，个人爱好者如今也能为冷门硬件编写复杂的硬件描述语言（HDL）代码。 HBM2 带宽是核心瓶颈：FK33 提供约 400GB/s，但 75MHz 的 fabric 频率远低于 HBM 控制器时钟，因此每个计算单元需要多个宽端口才可能接近饱和；此外 Jungle Cat Lite 既缺少快速加载权重的通路，也缺少 GTY 通道所需的时钟生成电路（可通过焊接少量元件解决）。作者的下一步目标是基于定制载板、采用 4 片 XCVU35P、共 32GB HBM2 的理想推理引擎，而目前权重仍需通过以太网 bitstream 方式加载。

reddit · r/LocalLLaMA · I_am_purrfect · 10月4日 16:51 · [社区讨论](https://www.reddit.com/r/LocalLLaMA/comments/1wxken1/qwen35_arch_implementation_in_fpga_fabric_for/)

**背景**: FPGA 是可重新配置的芯片，其逻辑可为特定工作负载重新布线；像 SQRL FK33 这类退役的加密货币矿机板卡把 Xilinx UltraScale+ FPGA 与 HBM2 显存堆栈结合在一起，这正是它们在 eBay 上颇具吸引力的原因。INT4 量化将每个模型权重压缩到 4 位，相比 FP16 可将显存占用减少约四倍，因此 9B 或 27B 模型只需数 GB 即可容纳。GTY 收发器是高速串行链路（UltraScale 中最高可达 30.5Gb/s），用于板卡之间以及板卡与网络的互连，从而实现多卡扩展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.0x04.net/~mwk/xidocs/ug/ug578-ultrascale-gty-transceivers.pdf">UltraScale Architecture GTY Transceivers User Guide (UG578)</a></li>
<li><a href="https://apxml.com/courses/quantized-llm-deployment/chapter-1-advanced-llm-quantization-fundamentals/low-bit-quantization-techniques">Low-Bit LLM Quantization ( INT 4 , NF4, FP4)</a></li>

</ul>
</details>

**社区讨论**: 评论区总体非常热情，称这项工作“疯狂”并真正推动了爱好者社区的发展。最具技术含量的回复建议将每个计算单元固定绑定到其本地 HBM 伪通道，因为跨越 VU35P 内置 AXI 交换结构的横向跳转会严重侵蚀有效带宽，并指出在 75MHz 下需要每个单元配备多个宽端口才可能接近 400GB/s；另一人开玩笑说在地毯上作业有静电风险，还有人表示这块板子便宜到几乎值得买一块，看看如今的 AI 编程助手能用 VHDL 做出什么。

**标签**: `#FPGA`, `#LLM inference`, `#quantization`, `#hardware acceleration`, `#Qwen`

---

<a id="item-4"></a>
## [Jev 点燃「决策模型」新品类，中国团队扎堆开源跟进](http://www.geekpark.net/news/372081) ⭐️ 7.0/10

9 月 15 日，前 OpenAI 研究员 Diogo Almeida 创办的 TypeSafe AI 发布 Jev——一款不生成文字、只对预设问题返回带概率结构化结果的「System One 模型」。两周内 OpenAI 推出 Decisions API，Cloudflare 于 10 月 1 日开源 Clef，亚马逊放出 Strands Decider；国内上海人工智能实验室开源多模态决策模型 Intern-Decision，成立不到五个月的上海公司 StartLux（原点星辉）于 9 月 30 日发布开源的 StartLux-Decision，并宣称在 Decision Index 0.2.1 上以 63.88 分超过 Jev 的 57.91 分。 这标志着「决策模型」作为一个独立品类正在成型：它把「判断」从「生成」中剥离出来，做成廉价、高频的基础设施，与过去两年一味拉长推理链的「系统二」路线形成互补，因为真实 Agent 任务里密集发生的是大量琐碎判断而非深度推理。另一个关键点是中国团队几乎不约而同选择开源权重与本地部署，而 Cloudflare 的 Clef、亚马逊的 Strands Decider 以及 APUS 的方案都基于中国开源基座 Qwen 训练，中国开源基座已成为这轮热潮中全球玩家共用的「躯干」。 Jev 定价为每百万输入 token 0.042 美元、输出免费，Vercel 披露其上线 24 小时内 AI Gateway 上 13% 的付费用户就用上了它，是此前任何模型发布速度的两倍，但 Jev 是闭源托管模型，无公开权重、不能本地部署。StartLux 的分数属于团队基于公开工具、对照 9 月 28 日榜单快照完成的自测，其发布第二天 Cloudflare 就宣称 Clef 在同一榜单领先；至于 36 局赢下 35 局的国际象棋演示，本来就不是决策模型的主战场，更像吸引眼球的展示。

rss · 极客公园 · 10月4日 11:41

**背景**: 「System One」之名取自丹尼尔·卡尼曼的《思考，快与慢》，书中把人的思维分为快速直觉的系统一和慢速审慎的系统二，而过去两年大模型几乎都在朝系统二的方向卷，推理链更长、思考更深。TypeSafe 称 Jev 为 System One 模型，是因为它完全不生成文本，而是接收一个状态加上一组预设问题（单选、打分或判断正误），直接返回软件可直接使用的带概率结构化答案。模型以经济学家杰文斯命名，暗指杰文斯悖论：一样东西越便宜，需求反而越大。上海人工智能实验室的 Intern-Decision 开源了 0.8B、2B、4B 三档并主打多模态，StartLux 则一口气提供 0.8B 到 27B 五档规格并配齐量化文件，直接瞄准本地部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://typesafe.ai/">Home - TypeSafe AI</a></li>
<li><a href="https://blog.cloudflare.com/clef-decision-models/">Introducing Clef: our open-source decision models, and new RL ...</a></li>
<li><a href="https://www.startlux.com/">StartLux 原 点 星 辉 ｜让AI运行在个人设备与工作站</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#decision models`, `#LLM`, `#System One`, `#industry trends`

---

<a id="item-5"></a>
## [Tavus 发布 Griffin：实时 AI 数字人骗过近半数测试者](http://www.geekpark.net/news/372075) ⭐️ 7.0/10

10 月 1 日，美国 AI 视频公司 Tavus 发布了名为 Griffin 的模型，并将其定义为全球首个「人类交互模型」（Human Interaction Model，简称 HIM）——一个全双工、视频到视频的模型，能够同时看、听、说并做出动作。在一项一分钟视频通话测试中，54 名参与者里有 26 人（约 48%）事后认为自己是在和真人聊天，而 Tavus 上一代系统在同样测试中只在 41 人中骗过 1 人，比例仅 2.4%。 从 2.4% 到 48% 的拟人化跃升，意味着数字人赛道的竞争焦点正从「脸像不像」转向「会不会像人一样聊天」，这对所有做对话智能体、客服机器人、培训模拟或视频内容的团队都有影响。它同时带来了新的欺骗性担忧——因为近半数用户在一段短通话里根本分不清屏幕对面是不是真人。 Griffin 放弃了「语音识别 → 大语言模型 → 语音合成 → 形象驱动」的级联流水线，转而采用一个统一模型，同时处理感知、对话和富有表现力的视频生成，因此能在用户说话时重叠发声，避免了过去那种「愣一秒再开口」的机械感。演示片段显示它能指导还原魔方、辅导焊接主板并玩「西蒙说」游戏，身体动作与背景据称均为实时生成；但这些都属于 Tavus 自己挑选的宣传素材，缺乏独立验证，而 48% 这一数字也仅来自 54 人的小样本测试。

rss · 极客公园 · 10月4日 05:27

**背景**: 目前市面上绝大多数实时 AI 数字人采用「级联」架构：语音识别先把你说的话转成文字，大语言模型生成回复，语音合成把文字念出来，最后形象驱动模型让一张脸跟着声音动起来。每一次交棒都会增加延迟并丢掉信息——语气、表情、手里拿的东西在转写那一步就被扔掉了，这也是这类系统通常必须等你说完才能回应的原因。Tavus 上一代方案由三个模型组成：Phoenix-4.5 负责渲染人脸，Sparrow-2 负责判断何时该说话，Raven-1 负责感知用户情绪，已被 15 万开发者和企业使用。Griffin 则试图做到「全双工、视频到视频」，在一次处理中同时完成听、说和动作，更像打电话而不是对讲机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tavus.io/griffin">Griffin: The First Human Interaction Model | Tavus</a></li>
<li><a href="https://www.businesswire.com/news/home/20261001092598/en/Tavus-Introduces-Griffin-the-First-Face-to-Face-Human-Interaction-Model-Unlocking-the-Future-of-Conversational-AI/">Tavus Introduces Griffin, the First Face-to-Face Human ...</a></li>
<li><a href="https://www.tavus.io/">Tavus: The Human Computing Company</a></li>

</ul>
</details>

**标签**: `#AI avatars`, `#digital humans`, `#real-time video generation`, `#multimodal AI`, `#human-computer interaction`

---

<a id="item-6"></a>
## [Claude Code 的 Mods 机制把终端变成了可扩展的游乐场](http://www.geekpark.net/news/372074) ⭐️ 7.0/10

Claude Code 推出了名为 Mods 的新扩展机制，本质是打包在插件里的小型 TypeScript 函数；该机制由 Claude Code 负责人 Boris Cherny 于 9 月中旬放出，10 月 1 日正式写入更新日志并默认开启。此后短短两周内，社区涌现出大量 mod，包括像素宠物、移植版 Doom、仿 Chrome 断网小恐龙、4-7-8 呼吸引导，以及用另一个 26 万参数模型实时讲故事的 Storytime。 Anthropic 自己的 /diff 变更面板和 AGENTS.md 支持就是用同一套 Mods 机制写出来的，这意味着它不是换皮肤的小权限，而是一次真正的平台化举动——官方与第三方开发者用的是同一套工具。再加上几天前推出的 Claude Marketplace 和插件提交门户，Anthropic 在约十天内凑齐了一个完整的应用商店体系。 mod 能在对话旁边开面板、在输入框上方画横条、重写提示词、在命令执行前拦截工具调用，甚至把请求转交给另一个模型处理；用户甚至可以直接让 Claude Code 给自己写一个 mod。代价也在官方文档里写得很直白：mod 拥有与 Claude Code 本身相同的机器访问权限，代码由发布者而非 Anthropic 编写，官方还专门留了一页说明企业管理员如何管控 mod。

rss · 极客公园 · 10月4日 05:16

**背景**: Claude Code 是 Anthropic 推出的终端 AI 编程智能体，运行在命令行界面中，可以代替用户在本机执行工具和命令。这里的 mod 指包含几行 TypeScript 的插件，能挂钩到工具的界面和工具调用流程，作用类似《我的世界》的模组扩展基础游戏。这个类比很关键：Minecraft 的模组文化始于玩家自行破解、官方后来才拥抱，而 Anthropic 是一开始就主动开口子。竞品 OpenAI 的 Codex 也提供 /pet 宠物和插件/技能打包能力，但公开资料显示其界面渲染与工具调用拦截并未开放给第三方。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://code.claude.com/docs/en/plugins/mods/overview">Mods overview - Claude Code Docs</a></li>
<li><a href="https://claude.com/blog/claude-code-mods">Customize Claude Code with mods in TypeScript | Claude by ...</a></li>
<li><a href="https://claude-mods.com/">Claude Mods: a directory of mods for Claude Code</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#AI developer tools`, `#modding`, `#LLM agents`, `#developer ecosystem`

---

<a id="item-7"></a>
## [用 SSH 和 nginx 搭建自托管 HTTP 隧道](https://vincent.bernat.ch/en/blog/2026-http-over-ssh) ⭐️ 7.0/10

Vincent Bernat 发布了一篇技术指南，介绍如何用 SSH 远程端口转发结合 nginx 搭建自托管 HTTP 隧道，该文在 Lobste.rs 上引发讨论。文章展示了如何用服务器上已有的标准工具替代商业隧道服务，构建一套完全自主可控的方案。 开发和运维人员若要把内网或家庭实验室服务暴露到公网，通常会依赖 ngrok、Cloudflare Tunnel 等第三方隧道服务，这会带来费用、速率限制以及对第三方供应商的依赖。一套有文档记录的 SSH 加 nginx 方案，为团队提供了免费且可审计的替代选择，复用他们本就信任并掌控的现有基础设施。 该方案的核心是 SSH 远程端口转发（即 -R 选项），它允许位于 NAT 或防火墙之后的机器在远端 SSH 服务器上开启监听端口，再由 nginx 作为对外的反向代理和 TLS 终结层。实际落地时有几个注意点：需要借助 autossh 或 systemd 自动重启来保证断线后隧道持续可用；SSH 转发是在远端主机而非客户端侧绑定端口；还要在代理链中正确传递 Host、X-Forwarded-For 等请求头。

rss · Lobste.rs · 10月4日 19:08

**背景**: HTTP 隧道通过代理服务器在两台计算机之间建立网络链路，使流量能够穿越原本会阻断它的防火墙、NAT 和访问控制列表。SSH 原生就支持这一能力，其端口转发有三种模式：本地转发（-L）、远程转发（-R）和动态转发（-D），分别对应不同的方向和用途，其中远程转发正是把本地服务暴露给远端主机的那一种。nginx 是广泛使用的 Web 服务器与反向代理，可以终结 TLS、按域名或路径路由，并把请求转发到隧道的监听端口，因此它经常与 SSH 转发搭配出现在自托管方案中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/HTTP_tunnel">HTTP tunnel - Wikipedia</a></li>
<li><a href="https://linuxize.com/post/how-to-setup-ssh-tunneling/">SSH Tunnel: Local, Remote, and Dynamic Port Forwarding</a></li>
<li><a href="https://www.digitalocean.com/community/tutorials/ssh-port-forwarding">SSH Port Forwarding: Local, Remote, and Dynamic Explained</a></li>

</ul>
</details>

**标签**: `#ssh`, `#nginx`, `#http-tunnels`, `#self-hosted`, `#networking`

---

<a id="item-8"></a>
## [魔改 Go 编译器，加速 IPv4 到 IPv6 地址映射](https://vincent.bernat.ch/en/blog/2026-go-netip-addrto6) ⭐️ 7.0/10

Vincent Bernat 发布了一篇技术深度文章，讲述他如何同时魔改 Go 编译器与标准库中的 net/netip 包，使 IPv4 地址转换为其 IPv6（IPv4 映射）表示形式变成一个快速且不产生内存分配的操作。文章既介绍了网络层面的动机，也剖析了为此所需的编译器内部机制。 Go 被广泛用于高吞吐网络服务，而 HTTP、TLS 等协议越来越希望在两代 IP 协议族之间使用统一、单一的地址表示，因此位于热点路径上的每次连接或每个数据包的地址转换都会成为可观测的开销。这篇文章展示了一名工程师通过改动工具链本身能把 Go 优化到什么程度，也记录了一种有可能被 Go 上游维护者采纳的优化思路。 netip.Addr 是一个小型、可比较的 24 字节值类型，其内部就以内嵌于 IPv6 的 IPv4 形式（IPv4-in-IPv6）保存 IPv4 地址，因此映射到 IPv6 本质上只是位级别的重新解释，而不是内存分配或方法调用。由于这一优化依赖内联、后端代码生成等编译器内部机制，它需要打过补丁的工具链，而非单纯修改库代码，这也限制了它被直接发布或合入上游的难易程度。

rss · Lobste.rs · 10月4日 18:49

**背景**: Go 1.18 引入了 net/netip 包，作为旧版 net.IP 类型的现代化替代：netip.Addr 不可变、可比较（能作为 map 的键），且占用内存更少，因此对性能敏感的网络代码纷纷转向它。IPv4 映射的 IPv6 地址位于 ::ffff:0:0/96 前缀内，它让双栈应用无论底层走 IPv4 还是 IPv6，都始终以 IPv6 格式处理地址。Go 编译器本身是一条经典的多阶段流水线——扫描器、解析器、类型检查器以及基于 SSA 的后端；Eli Bendersky 的《为 Go 添加一条新语句》等文章已经展示了开发者可以如何修改这条流水线来引入新行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pkg.go.dev/net/netip">netip package - net / netip - Go Packages</a></li>
<li><a href="https://blog.ip2location.com/knowledge-base/ipv4-mapped-ipv6-address/">IPv4-mapped IPv6 address - IP2Location.com</a></li>
<li><a href="https://eli.thegreenplace.net/2019/go-compiler-internals-adding-a-new-statement-to-go-part-1">Go compiler internals : adding a new statement to Go - Part 1 - Eli...</a></li>

</ul>
</details>

**标签**: `#Go`, `#networking`, `#compiler-internals`, `#IPv6`, `#performance-optimization`

---