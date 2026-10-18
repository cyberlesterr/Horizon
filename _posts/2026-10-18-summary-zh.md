---
layout: default
title: "Horizon Summary: 2026-10-18 (ZH)"
date: 2026-10-18
lang: zh
---

> 从 41 条内容中筛选出 5 条重要资讯。

---

1. [DeepSeek 发布 V4.1-Flash-1017，称编码基准领先 Sol 5.6](#item-1) ⭐️ 9.0/10
2. [全球太阳能发电量首次超过核电](#item-2) ⭐️ 8.0/10
3. [Xolotl 单卡 4090 运行 552B DeepSeek-V4.1-Flash](#item-3) ⭐️ 8.0/10
4. [九年攻关：Xbox 360 硬件故障注入破解回顾](#item-4) ⭐️ 7.0/10
5. [PwnEscape：Linux IPv4 漏洞可实现 KVM 虚拟机逃逸](#item-5) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [DeepSeek 发布 V4.1-Flash-1017，称编码基准领先 Sol 5.6](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017) ⭐️ 9.0/10

DeepSeek 发布了 DeepSeek-V4.1-Flash-1017，这是 V4.1-Flash 模型在 2026 年 10 月 17 日的快照版本，并已上线其网站、应用、API 和 OpenRouter。官方称该版本在推理、编码和智能体任务上有显著提升，并在 11 项编码基准中的 10 项上超过 Sol 5.6。 此次发布进一步表明，快速、低成本的开源权重模型能在实际编码任务中与闭源前沿系统竞争，为开发者的智能体工作流提供了可信替代方案。它也加剧了关于开放性、基准透明度和监管是否会巩固闭源模型厂商优势的争论。 DeepSeek 将 V4.1-Flash-1017 描述为 V4.1-Flash 的小版本更新，但带来了实质性改进，输出更短、任务完成更快，在性能与成本上形成帕累托改进。HN 上一次针对 200 多个文件的 C++ 脏代码库的实际对比发现，DeepSeek 找到的相关问题更少且耗时更长，而其他用户则强调服务商的 token/s、TTFT 和可见的思维链是关键优势。

hackernews · theykk · 10月17日 08:21 · [社区讨论](https://news.ycombinator.com/item?id=50129045)

**背景**: DeepSeek 是一家中国 AI 实验室，以发布能力较强的开放权重模型著称，外部开发者可以检查、托管和微调这些模型，而不必只依赖闭源 API。V4.1-Flash-1017 定位在快速/Flash 层级，因此延迟和吞吐与原始基准分数同样重要。智能体编码指基于大语言模型的智能体在代码库中规划、修改、运行测试和审查代码，这类工作负载中首 token 延迟、每秒 token 数和可解释的推理过程会显著影响可用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/news/news261017/">DeepSeek - V 4 . 1 - Flash - 1017 : Wish-Driven Programming Made Real</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4.1-flash-1017">DeepSeek V 4 . 1 Flash 1017 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agentic_coding">Agentic coding</a></li>

</ul>
</details>

**社区讨论**: HN 评论者普遍称赞 DeepSeek 在实际使用中感觉更快、更开放，提到服务商的 token/s、TTFT、可见的思维链以及更少随意的网络安全审查拦截，即使基准分数并非全面高于 Sol 或 Gemini。一些人认为此次发布恰好说明闭源模型厂商为何可能欢迎监管门槛，并主张多元模型生态至关重要。实际体验报告则褒贬不一：一次脏代码库审查发现 GPT-5.6/6.1 Sol 更准确也更快，而另一些人表示正重新转回 DeepSeek 写代码，同时保留 Opus/Sol 做规划和审查。

**标签**: `#llm`, `#deepseek`, `#model-release`, `#benchmarks`, `#open-models`

---

<a id="item-2"></a>
## [全球太阳能发电量首次超过核电](https://www.pv-magazine.com/2026/09/29/solar-surpasses-nuclear-power-globally-for-first-time/) ⭐️ 8.0/10

全球太阳能光伏发电量（按实际太瓦时计算）首次超过核电。全球太阳能装机容量同比增长 27%、增加 510 GW，达到 2,383 GW；而核电装机容量仅增加 1.5 GW 至 399.5 GW，在运核电容量甚至下降了约 0.5 GW。风电同样创纪录地新增 159 GW，达到 1,291 GW（增长 14%）；从 2025 年 3 月到 2026 年 6 月，太阳能或风能各自单独每月都超过核电发电量，并在 2026 年 3 月、4 月和 5 月双双独立超越核电。 这是能源转型中的一个标志性里程碑：太阳能曾经只是边缘性电源，如今其发电量已超过长期以能量密度和稳定性著称的核电，尽管核电的容量系数远高于太阳能（2024 年核电超过 92%，太阳能约为 23%）。这说明真正重塑全球电力供应、并对化石能源发电形成压力的，是可再生能源的增长速度，而不仅仅是其装机规模。 该比较基于实际发电的太瓦时数，而非常规装机容量，这一点很关键，因为 1 GW 核电站的年发电量大约是 1 GW 太阳能电站的四倍。评论者指出，下一个重要里程碑——太阳能发电量超过水电——按目前增速仍需数年才能实现，而风电的发电量也即将超过核电。

hackernews · xbmcuser · 10月17日 14:01 · [社区讨论](https://news.ycombinator.com/item?id=50131256)

**背景**: 装机容量指电站在满功率运行时能发出的功率（以瓦计），而发电量是随时间实际输出的能量（瓦时）；两者之比就是容量系数。核电站几乎连续运行，因此容量系数很高；太阳能只能在白天且天气条件合适时发电，容量系数低得多。正因如此，规模较小的核电装机仍能发出相当的电量，也正因如此，太阳能依靠大量新增装机在发电量上取得领先才格外引人注目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Capacity_factor">Capacity factor - Wikipedia Empirical Comparison Between Nuclear and Solar Power Is Nuclear Cheaper Than Solar? What the Data Shows Renewable Energy Power Output: Capacity Factors, Wind vs ...</a></li>
<li><a href="https://www.eia.gov/tools/faqs/faq.php?id=101&t=3">What is the difference between electric generation capacity ...</a></li>
<li><a href="https://www.iso-ne.com/about/what-we-do/capacity-vs-energy-primer">Capacity vs. Energy: A Primer - iso-ne.com</a></li>

</ul>
</details>

**社区讨论**: 讨论理性且少有炒作：评论者强调这里比较的是实际发电的太瓦时数，澄清了容量系数的区别，并指出风电也即将超过核电。有人惋惜核电数十年的停滞不前；也有人提出，更艰难的未解难题是脱碳用作化工原料（而非仅作燃料）的碳氢化合物，因为电解和合成过程存在巨大的能量损失。

**标签**: `#energy`, `#solar-power`, `#nuclear-power`, `#renewable-energy`, `#climate-tech`

---

<a id="item-3"></a>
## [Xolotl 单卡 4090 运行 552B DeepSeek-V4.1-Flash](https://www.reddit.com/r/LocalLLaMA/comments/1x8m0jj/xolotl_strata_based_deepseekv41flash_552b_on_a/) ⭐️ 8.0/10

开发者发布了基于 Strata 的推理引擎 Xolotl，可在单张 24GB RTX 4090 上运行完整的 552B DeepSeek-V4.1-Flash，报告解码速度约 27 tok/s、512K 上下文下预填充 180–320 tok/s。更新版无审查 1017 量化模型正在准备中，预计几天内发布。 如果结果可复现，这表明 MoE 专家卸载能让 552B 级模型在消费级硬件上可用，显著降低本地大模型的门槛。它也反映出围绕 VRAM/RAM/NVMe 分层推理与低比特量化的工具竞争正在升温。 测试平台为 24GB 显存、90GB DDR4 内存和 NVMe 硬盘，引擎按 token 流式加载所需专家；报告成绩包括 HumanEval 21/21、工具调用 10/10 和智能体修 bug 循环 3/3，但这些均为作者自报、尚未独立验证。当前无审查 GSQ 量化版本为 152 GiB，而 1017 更新是 510GB 下载，因仅架构和分词器一致，需要重新校准和完整量化。

reddit · r/LocalLLaMA · /u/indrasmirror · 10月17日 21:40

**背景**: 混合专家（MoE）模型包含许多专门化的“专家”子网络，但每个 token 只激活其中少数几个，因此完整权重集可能远超单张 GPU 的显存容量。Strata 是一个开源本地推理引擎，通过把不活跃专家动态卸载到 CPU 内存或 NVMe、只把活跃专家留在显存中，让消费级 PC 运行大型 MoE 模型。GSQ 是 ISTA Das Lab 提出的训练后标量量化方法，可把权重压缩到约每参数 2–3 比特，同时尽量减小精度损失。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Niko1221/Strata">GitHub - Niko1221/Strata: Qwen3.8-Flash-Next on any consumer ...</a></li>
<li><a href="https://stratallm.org/">Strata LLM – Run 125B+ MoE Models on 12GB VRAM Consumer GPUs ...</a></li>
<li><a href="https://arxiv.org/abs/2604.18556">[2604.18556] GSQ: Highly-Accurate Low-Precision Scalar ... GitHub - IST-DASLab/GSQ: Gumbel-Softmax post-training ... GSQ - a ISTA-DASLab Collection - Hugging Face GSQ: Highly-Accurate Low-Precision Scalar Quantization for ... What Are GSQ and RCO? Das Lab's New LLM Quantization Method ISTA-DASLab/Qwen3.8-27B-GSQ-RCO-GGUF · Hugging Face Qwen3-8-27B at 11.8GB: Do GSQ and RCO Quantization Actually ...</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#inference-engine`, `#quantization`, `#model-offloading`, `#deepseek`

---

<a id="item-4"></a>
## [九年攻关：Xbox 360 硬件故障注入破解回顾](https://kennedn.com/blog/posts/glitching/) ⭐️ 7.0/10

一位逆向工程爱好者发布技术回顾，讲述自己历时九年通过硬件故障注入（glitching）破解 Xbox 360 的完整过程，从最初研究一直记录到最终可用的改装方案。 尽管 Xbox 360 的 reset glitch 攻击早在 2011 年就已公开，但详细的第一人称复现记录对硬件安全学习者仍很有价值，因为它展示了时序控制、故障注入与主机启动安全机制在实践中的相互作用。 该攻击通过在启动阶段向主机的复位线注入精确定时的电信号毛刺，使 CPU 跳过签名校验；2011 年的原始方法使用 Xilinx CoolRunner II CPLD 等可编程逻辑器件，对时序精度要求极高。这篇博客属于个人复现回顾，并非披露新的安全漏洞，并且依赖较老的 Xbox 360 硬件以及焊接和编程等动手操作。

rss · Lobste.rs · 10月17日 16:13

**背景**: Xbox 360 的设计目标是只运行微软签名的代码，并在启动过程中设置了多层硬件与密码学校验。2011 年，黑客 Gligli 和 Tiros 公开了 reset glitch hack（RGH），利用故障注入扰乱启动流程，从而绕过这些校验。硬件故障注入是一种主动攻击方式：通过故意干扰电源、时钟或复位信号，让芯片错误执行指令。该技术后来成为 Xbox 360 改装和自制软件运行的重要基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hackaday.com/2024/10/19/a-robust-guide-to-the-xbox-360-glitch-hack/">A Robust Guide To The Xbox 360 Glitch Hack - Hackaday</a></li>
<li><a href="https://github.com/kooscode/srgh-matrix-trinity">GitHub - kooscode/srgh-matrix-trinity: XBOX 360 advanced ... xbox 360 – Hackaday A Robust Guide To The Xbox 360 Glitch Hack - Hackaday Modder finishes nine-year Xbox 360 voltage glitch mod with a ... GitHub - JakobRangel/Xbox-360-RGH3-Exploitation Xbox stuck on glitching RGH. : r/360hacks - Reddit</a></li>
<li><a href="https://en.wikipedia.org/wiki/Fault_injection">Fault injection - Wikipedia</a></li>

</ul>
</details>

**标签**: `#hardware hacking`, `#Xbox 360`, `#glitching`, `#reverse engineering`, `#security`

---

<a id="item-5"></a>
## [PwnEscape：Linux IPv4 漏洞可实现 KVM 虚拟机逃逸](https://pwn.ai/blog/pwnescape) ⭐️ 7.0/10

安全公司 pwn.ai 公开了 PwnEscape（CVE-2026-99999），这是一个严重的 Linux 内核漏洞，可让恶意虚拟机客户机逃逸到宿主机；AlmaLinux 已于 2026 年 10 月 16 日发布可供测试的修复内核，SUSE 等厂商也相继发布了安全公告。尽管被冠以“KVM 逃逸”之名，该漏洞实际位于宿主机的 IPv4 网络协议栈中，而非 KVM 本身。 可用的客户机到宿主机逃逸打破了虚拟化最核心的隔离保证，因此任何运行不可信虚拟机或多租户虚拟机的宿主机——公有云厂商、VPS 服务商以及容器或沙箱平台——都可能面临宿主机层面代码执行的风险。由于该漏洞同样影响宿主机上的本地用户，即使未做虚拟化的普通 Linux 服务器也可能需要打补丁。 根因是围绕 CHECKSUM_PARTIAL 标志的信任边界缺陷：客户机可以提供不受信任的校验和元数据，在校验之后篡改 IPv4 报文头，从而改写与安全相关的数据包字段并破坏约 32 字节的宿主机内存。据 TuxCare 称，该缺陷在内核网络协议栈中潜伏了约 18 年而未被发现，SUSE 也指出目前除打补丁外没有其他缓解手段。

rss · Lobste.rs · 10月17日 18:24

**背景**: KVM 是内置于 Linux 内核的虚拟化管理程序，可让一台机器运行多个相互隔离的虚拟机，而“客户机到宿主机逃逸”指虚拟机内部的代码突破隔离、在宿主机上执行。Linux 通过校验和卸载来节省 CPU 开销：借助 CHECKSUM_PARTIAL 标志，客户机告知宿主机某个数据包的校验和仍需部分计算，宿主机便会在自己的内核中检查并补全这些数据包。pwn.ai 称其通过一项百万美元沙箱挑战、借助实验性的 Omega-Pwn 工具发现了该漏洞；尽管“CVE-2026-99999”这一编号看起来像占位符，但 SUSE、AlmaLinux 和 TuxCare 均已发布公告予以确认。

**标签**: `#security`, `#virtualization`, `#KVM`, `#CVE`, `#exploitation`

---