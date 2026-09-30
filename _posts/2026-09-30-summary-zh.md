---
layout: default
title: "Horizon Summary: 2026-09-30 (ZH)"
date: 2026-09-30
lang: zh
---

> 从 54 条内容中筛选出 10 条重要资讯。

---

1. [AMD 以 82 亿美元全股票收购 World Labs](#item-1) ⭐️ 9.0/10
2. [OpenAI 发布 GPT-6.1 Sol：以五分之一价格提供接近 Astra 的智能](#item-2) ⭐️ 8.0/10
3. [America.gov](#item-3) ⭐️ 8.0/10
4. [网络与移动端对话式 AI 智能体的隐私分析](#item-4) ⭐️ 8.0/10
5. [Anthropic：GLM-5.3 与 Claude Mythos Preview 跨过二进制漏洞利用门槛](#item-5) ⭐️ 8.0/10
6. [Anthropic 招股书：2 万亿美元估值背后的 7 个关键细节](#item-6) ⭐️ 8.0/10
7. [研究人员称可从不受信任应用获取 OnePlus 15 的 root 权限](#item-7) ⭐️ 8.0/10
8. [Manus 2.0 正式发布：Cascade 框架、云电脑与个人助手 Cue 齐登场](#item-8) ⭐️ 7.0/10
9. [Nura（原 postmarketOS）公布通往可日常使用的主线 Linux 手机路线图](#item-9) ⭐️ 7.0/10
10. [ESPARGOS 的 ESP-SDR 让廉价 ESP32 芯片实现原始 IQ 采集](#item-10) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [AMD 以 82 亿美元全股票收购 World Labs](http://www.geekpark.net/news/372000) ⭐️ 9.0/10

AMD 宣布以约 82 亿美元的全股票交易收购李飞飞创办的空间智能公司 World Labs，交易预计在 2026 年底前完成交割，尚需通过监管审批。交割后，李飞飞将出任 AMD 执行副总裁兼首席科学家，直接向 CEO 苏姿丰汇报。 这是 AMD 历史上第二大收购，仅次于收购赛灵思，标志着 AI 基础设施竞争正从「卖芯片」转向「掌握前沿模型人才与洞察」。这也让 AMD 直接切入世界模型与物理 AI 战场——而英伟达已凭借 CUDA、Cosmos 世界模型以及收购 Hugging Face、Groq 等布局占据了先机。 AMD 将这笔交易定位为不是买收入，而是在研发链条最上游装一个传感器：World Labs 的模型经验将帮助 AMD 理解推理、机器人、仿真和物理 AI 等工作负载如何演变，从而塑造未来的芯片路线图。82 亿美元不到 AMD 市值的 1%（其市值在 9 月首次突破 1 万亿美元），且双方此前已在 AMD GPU 上合作进行了为期一年的模型训练与推理优化。

rss · 极客公园 · 9月29日 11:21

**背景**: World Labs 由李飞飞及同事于 2024 年创立，专注于构建能够感知、生成并与 3D 世界交互的大型世界模型，已推出 Marble 三维场景产品和 Atlas 多模态世界模型。与主要依赖文本训练的大语言模型不同，世界模型从视频、图像和三维数据中学习物理规律、物体交互与空间动态，业内普遍认为这是人形机器人、自动驾驶等物理 AI 的前提。AMD 卖的是 CPU、GPU 和数据中心系统而非模型，在 AI 加速器市场份额约 13%，而英伟达估计占约 81%，因此接触前沿模型研究被视为提前数年预判算力需求的手段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/world-labs">World Labs</a></li>
<li><a href="https://en.wikipedia.org/wiki/World_model_(artificial_intelligence)">World model (artificial intelligence)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Physical_AI">Physical AI</a></li>

</ul>
</details>

**标签**: `#AMD`, `#World Labs`, `#李飞飞`, `#AI基础设施`, `#收购`

---

<a id="item-2"></a>
## [OpenAI 发布 GPT-6.1 Sol：以五分之一价格提供接近 Astra 的智能](https://openai.com/index/introducing-gpt-6-1-sol/) ⭐️ 8.0/10

OpenAI 发布了 GPT-6.1 Sol，这是一款定位低于旗舰型号 GPT-6 Astra 的模型，声称在编码、计算机操作和专业工作方面提供接近 Astra 的智能，而标准 API 输入和输出 token 价格仅约为 Astra 的五分之一。该版本距离 GPT-6 Sol 发布仅数天，缓存输入价格低至每百万 token 0.10 美元——比标准输入价格低 95%，比 GPT-6 Sol 的缓存价格低 50%。 此次发布表明，token 价格而非纯粹的模型能力正成为前沿实验室之间的主要竞争战场，直接对 Anthropic 等对手在成本效益上形成压力。对于开发者和企业而言，更低的缓存价格可能让 Codex 等高频编码智能体工作流变得经济得多。 Artificial Analysis 的独立基准测试显示，GPT-6.1 Sol 在 xhigh 推理强度设置下得分比 GPT-6 Astra 高一分，而每任务成本不到后者的 15%，相比 GPT-6 Sol（max）提升了六分；值得注意的是，xhigh 比 max 强度设置高出三分。它在仅仅七天后就取代了 GPT-6 Sol，暗示这是一次快速纠偏而非计划中的代际升级。

hackernews · crorella · 9月29日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=49896586)

**背景**: OpenAI 的 GPT-6 系列分为两个层级：高端旗舰 Astra 和价格更亲民的 Sol 系列。“接近 Astra 的智能”是 OpenAI 用来描述以极小成本接近旗舰性能的模型的说法。缓存输入价格指的是重复使用已处理过的提示 token 时享受的折扣费率，这对反复发送大上下文的智能体工作流尤为重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT - 6 . 1 Sol | OpenAI</a></li>
<li><a href="https://artificialanalysis.ai/articles/gpt-6-1-sol-replaces-gpt-6-sol-after-just-7-days-with-near-astra-intelligence">GPT-6.1 Sol replaces GPT-6 Sol after just 7 days, with near - Astra ...</a></li>
<li><a href="https://openrouter.ai/openai/gpt-6.1-sol">GPT - 6 . 1 Sol - API Pricing & Providers | OpenRouter</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一且以怀疑为主：有用户称 GPT-6 Sol 表现令人失望，以至于他们转而使用 Anthropic 的 Opus 5.5；还有人推测 Sol 6.1 是泄露的“Astra-Minor”模型的临时改名。也有人认为真正的看点是缓存价格比 GPT-6 Sol 便宜 50%，而一位评论者则感叹价格成为主要战场对行业和投资者而言是不祥之兆。

**标签**: `#AI`, `#LLM`, `#OpenAI`, `#Model Release`, `#Pricing`

---

<a id="item-3"></a>
## [America.gov](https://america.gov/) ⭐️ 8.0/10

美国政府推出了 America.gov，这是一个由 Google Gemini 驱动的人工智能门户，旨在帮助公民浏览和获取政府服务，引发了关于其潜力和实施的实质性讨论。

hackernews · plesiv · 9月29日 14:04 · [社区讨论](https://news.ycombinator.com/item?id=49893509)

**标签**: `#government`, `#AI`, `#public services`, `#LLM`, `#civic tech`

---

<a id="item-4"></a>
## [网络与移动端对话式 AI 智能体的隐私分析](https://jorgegarciaherrero.com/wp-content/interactivos/20260916-Prompt-like-a-butterfly-sting-like-a-tracker-(clean).pdf) ⭐️ 8.0/10

一篇题为《Prompt like a Butterfly, Sting like a Tracker》的新论文对网页端和移动端的对话式 AI 智能体进行了隐私分析，记录了诸如未完成的提示词被部分上传至服务器、仅凭 URL 中的 UUID 即可访问历史对话，以及跟踪与数据泄露风险等问题。该研究伴随着一场 Hacker News 讨论被曝光，讨论获得 406 分和 128 条评论。 随着对话式 AI 助手成为撰写消息、搜索和编程的日常工具，这些智能体的隐私状况影响着数亿用户，而他们默认自己打字打到一半的想法和历史对话是私密的。这些发现也卷入了更广泛的行业争论：关于跟踪、训练数据复用，以及闭源托管式助手是否值得托付敏感的用户输入。 该分析同时覆盖网页端与移动端智能体的攻击面，强调的是具体弱点而非抽象风险，其中包括 ChatGPT 网页客户端会在用户点击发送之前，就把未完成的提示词周期性地发送到 `conversation/prepare` 端点。社区评论者还点名了 Perplexity 等服务：只要拿到对话 URL 中的 UUID，就能看到完整的聊天记录，这反映出业界普遍把“不可猜测的标识符”误等同于真正的访问控制。

hackernews · damaru2 · 9月29日 09:03 · [社区讨论](https://news.ycombinator.com/item?id=49890226)

**背景**: 对话式 AI 智能体是基于大语言模型的助手，例如 ChatGPT 和 Perplexity，它们通过网页或移动应用与用户保持连续对话。“提示词泄露”（prompt leaking）是一类相关风险，指定义模型人格与约束条件的隐藏系统提示词被提取出来，既可能由对抗性用户发起，也可能因产品自身的数据链路而无意中发生。该领域的隐私研究不只关注模型输出，而是审视整条客户端—服务器链路：哪些数据离开了设备、何时离开，以及数据在传输和存储中如何受到保护。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learnprompting.org/docs/prompt_hacking/leaking">Prompt Leaking : Understanding Risks in GenAI Models</a></li>
<li><a href="https://www.promptingguide.ai/prompts/adversarial-prompting/prompt-leaking">Prompt Leaking in LLMs | Prompt Engineering Guide</a></li>
<li><a href="https://aisecurityandsafety.org/en/guides/prompt-leaking/">Prompt Leaking : The Complete Guide to System Prompt Extraction...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对托管式 AI 助手持怀疑态度：有人指出 ChatGPT 网页客户端会把未完成的提示词发送到 `conversation/prepare` 端点，可能暴露用户的写作节奏和思路演变过程；另一位则认为像 Perplexity 那样把 UUID 放在 URL 里的设计会泄露完整对话。一些人将此与近期私密 Codex 会话和未发表草稿被牵连进训练数据的案例直接联系起来，由此得出结论：开源、本地运行的模型是更安全的路径。还有人用轻松的口吻调侃，用户向聊天机器人倾诉秘密，就像《辛普森一家》里 Milhouse 把所有秘密都告诉 Willie 一样。

**标签**: `#privacy`, `#AI agents`, `#security`, `#tracking`, `#HCI`

---

<a id="item-5"></a>
## [Anthropic：GLM-5.3 与 Claude Mythos Preview 跨过二进制漏洞利用门槛](https://simonwillison.net/2026/Sep/29/anthropic-frontier-red-team/) ⭐️ 8.0/10

Anthropic 的前沿红队（Frontier Red Team）在其内部的 Binary Exploitation 基准测试中随机抽取 100 个任务对多个模型进行了评估，结果显示 GLM-5.3 在 4% 的试验中实现了完整的控制流劫持，Claude Mythos Preview 的比例为 6%。而此前的模型，如 Claude Opus 4.6 和 GLM-5.2，在这些任务中一次都没有成功。 这标志着一个有意义的能力门槛被跨过：模型开始能够自动化真实漏洞利用开发中的核心环节，而这类能力具有明显的两用性质，既可能加速攻击，也可能加速防御性的漏洞研究。值得注意的是，开源中国模型 GLM-5.3 已经与 Anthropic 的前沿预览模型处于同一量级，说明高级网络能力正在扩散，而非集中在少数实验室手中。 成功率仍然很低——在 100 个抽样任务中仅为 4% 和 6%——而且该基准是 Anthropic 的内部评估而非公开测试，因此这些数字无法与其他漏洞利用生成基准直接比较。所谓“完整的控制流劫持”，具体指模型取得了目标程序指令指针的控制权，这是把内存破坏漏洞转化为可用漏洞利用的关键一步。

rss · Simon Willison · 9月29日 22:20

**背景**: 二进制漏洞利用是指通过操纵已编译程序，使其以有利于攻击者的方式违反信任边界；其经典基础是控制流劫持，即攻击者借助缓冲区溢出、格式化字符串漏洞等缺陷夺取程序的指令指针。1988 年的 Internet Worm 等历史性攻击就基于这类原语，而栈金丝雀（stack canary）、DEP、ASLR 等现代缓解措施正是为了加大其难度而存在。Anthropic 的前沿红队是该公司内部专门对前沿模型进行危险能力压力测试的团队；GLM 则是中国智谱 AI 的模型系列，而“Preview”版本指尚未正式发布、仅向有限测试者开放的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://users.ece.cmu.edu/~dbrumley/courses/18487-f13/powerpoint/05-controlflow-defense.pdf">Control Flow Hijack Defenses Canaries, DEP, and ASLR David Brumley</a></li>
<li><a href="https://trailofbits.github.io/ctf/exploits/binary1.html">Binary Exploits 1 - CTF Field Guide</a></li>
<li><a href="https://crypto.stanford.edu/cs155old/cs155-spring11/lectures/03-ctrl-hijack.pdf">Control Hijacking Attacks Note: project 1 is out</a></li>

</ul>
</details>

**标签**: `#anthropic`, `#ai-security`, `#cybersecurity`, `#generative-ai`, `#benchmarks`

---

<a id="item-6"></a>
## [Anthropic 招股书：2 万亿美元估值背后的 7 个关键细节](http://www.geekpark.net/news/371994) ⭐️ 8.0/10

当地时间 9 月 28 日，外媒披露了 Anthropic 的 IPO 招股书草案。Anthropic 今年 6 月以公益公司身份向美国证交会秘密递交了 S-1 注册声明，草案显示其估值目标超过 2 万亿美元（约为其 5 月自估 9650 亿美元的两倍以上），2025 年净亏损约 420 亿美元，收入则从 3.86 亿美元增至 45.9 亿美元。 这使 Anthropic 成为 ChatGPT 引爆这轮 AI 浪潮近四年来，第一家把完整账本摊给公众投资人的前沿大模型实验室，意味着 AI 竞赛的资金来源正从风投、主权财富基金和科技巨头转向公开市场。它披露的估值、亏损、客户集中度和治理结构，将成为衡量整个 AI 资本格局的参照基准。 420 亿美元的净亏损中约 340 亿美元是会计费用，反映的是未来可能转换成 Anthropic 股票的融资工具估值上升，而非实际经营支出——也就是说 Anthropic 越值钱，账面「亏」得越多。真正的经营数据是收入增长 1088% 至 45.9 亿美元，经营亏损从 29.8 亿美元扩大到 80.6 亿美元；此外去年近四分之一收入来自两个未披露名称的客户，且公司在风险因素中承认许多大客户没有签订长期合同。

rss · 极客公园 · 9月29日 09:12

**背景**: Anthropic 于 6 月秘密递交 S-1，这是让公司在正式公开前先获得证交会反馈的常规路径；完整财务数据要到路演前至少 15 天才公开，因此这份被外媒看到的草案仍可能调整，Anthropic 也拒绝置评。招股书覆盖的是 2025 财年，而 Anthropic 真正的爆发发生在 2026 年：年化收入（用某一个月收入乘以 12 推算）据报道从 2025 年底约 90 亿美元升到今年 5 月的约 470 亿美元，7 月底已超过 650 亿美元。文件还披露了一套多层股权结构：由包括 CEO Dario Amodei 在内的七位联合创始人控制的 Founder LLC，以一股 F 类股票拥有 50.1% 的总投票权，而代理顾问机构 ISS 和 Glass Lewis 历来建议反对这类安排。

**社区讨论**: 在美国散户论坛 wallstreetbets 上，最高赞评论质疑「2 万亿估值，配 40 亿收入？」。这个反应很直观，但拿错了分母：招股书里的 45.9 亿美元对应的是 2025 财年，是 Anthropic 在 2026 年爆发前的最后一张快照，资本市场给出的 2 万亿美元估值押注的其实是之后的增长曲线，而非去年全年成绩。

**标签**: `#Anthropic`, `#IPO`, `#AI行业`, `#财务披露`, `#大模型`

---

<a id="item-7"></a>
## [研究人员称可从不受信任应用获取 OnePlus 15 的 root 权限](https://blog.nns.ee/2026/09/24/oneplus-root/) ⭐️ 8.0/10

2026 年 9 月 24 日发布在 blog.nns.ee 的一篇安全博客文章，详细描述了如何从一个普通的“不受信任应用”出发，最终在 OnePlus 15 上获得 root 权限。文章声称这条提权路径可以从运行于标准 Android 应用沙箱内的应用实现，而不需要解锁引导加载程序（bootloader）或进行物理接触攻击。 Android 的整套安全模型都建立在把普通应用限制在 SELinux 的 untrusted_app 域之内，因此“应用直达 root”意味着这道隔离边界在该设备上失效。若属实，这将影响所有 OnePlus 15 用户，并引发外界质疑：采用同一芯片组或同一厂商系统软件的其他机型是否也存在同样缺陷。 Root 意味着获得完整的 uid 0 系统控制权，从而能够绕过应用沙箱、读取其他应用的私有数据；其标准补救措施是厂商发布安全补丁，而不是用户侧的自救手段。不过所提供的摘录只包含一个 Lobsters 讨论帖的链接，并未说明存在漏洞的具体组件、受影响的 OxygenOS 版本，也未说明是否已通报 OnePlus 或是否已修复。

rss · Lobste.rs · 9月29日 17:25

**背景**: 在 Android 上，每个应用通常以自己的独立 Linux 用户身份运行，并被置于受限的 SELinux 域（untrusted_app）中，因此无法触碰系统文件或其他应用的数据。获得 root 就是取得凌驾于这些限制之上的超级用户权限（uid 0），而历史上正是各种提权漏洞让攻击者无需解锁引导加载程序即可越过这条界线。OnePlus 15 是近期发布的旗舰机型，运行基于 Android 的 OxygenOS/ColorOS 系统，厂商通常通过月度或季度安全更新来修复此类缺陷。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stackoverflow.com/questions/44743797/selinux-android-message-interpretation">SElinux Android message interpretation - Stack Overflow</a></li>
<li><a href="https://zimperium.com/blog/privilege-escalation-preventing-mobile-apps-from-taking-over-on-android">Privilege Escalation: Preventing Mobile Apps from Taking Over on Android</a></li>
<li><a href="https://cloudfuzz.github.io/android-kernel-exploitation/chapters/linux-privilege-escalation.html">Linux Privilege Escalation · Android Kernel Exploitation</a></li>

</ul>
</details>

**标签**: `#android`, `#security`, `#root`, `#exploit`, `#vulnerability`

---

<a id="item-8"></a>
## [Manus 2.0 正式发布：Cascade 框架、云电脑与个人助手 Cue 齐登场](http://www.geekpark.net/news/371493) ⭐️ 7.0/10

Manus 在官网和社交平台正式公布 2.0 版本更新，推出自研的 Cascade Agent 框架、可选购买的「云电脑」、升级版自动化流程、重构的 Manus Studio（新增专业视频编辑器与游戏开发环境）、用手机指挥电脑的远程控制能力，以及一款全新的个人 Agent 应用 Cue，覆盖手机与桌面端并共享 Manus 的基础设施。官方公众号同时表示，正在组建团队开发面向国内市场的产品，与国产模型厂商及生态伙伴的合作也在稳步推进。 Manus 2.0 不是单一功能更新，而是试图把个人助手、云端执行、内容创作、游戏开发和远程控制等几乎所有热门 AI 场景打包进一个平台，这抬高了其他争夺通用型 AI 助手市场的创业公司的竞争门槛。官方明确表态要做面向国内市场的产品并与国产模型厂商合作，也说明 Manus 把本地化视为突破现有用户规模的关键。 Manus 宣称新的 Cascade 框架将任务 Token 消耗减少 23.2%、任务完成时间缩短 28.2%、运行成本降低 32%，其思路是项目开始时尽量轻量，只有当任务真正需要时才按需接入专业能力，以免「同样的活又慢又贵」。Studio 的视频编辑器目前主要面向 30 到 60 秒的产品短广告、数据动态图表、教程和 Vlog，不需要剪辑经验；游戏项目则可一键发布成网页供他人游玩，多人联机则通过购买云电脑充当全天候在线的服务器来实现。

rss · 极客公园 · 9月29日 05:27

**背景**: Manus 是一款通用型 AI Agent 产品，因能在云端沙箱中自主完成多步骤任务而受到广泛关注；Computer Use 指的是让 AI 直接操作用户电脑图形界面、而不只是回答问题或生成文本的能力。云电脑（Cloud Computer）是 Manus 提供的持久化 Ubuntu 虚拟机，即使用户离线也能让机器人和脚本持续运行，取代了会话结束后就关闭的临时沙箱。像 Cue 这样的个人 Agent，通常指跨设备绑定单个用户、持续处理日常事务而非只响应单次指令的助手。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://manus.im/blog/introducing-manus-2-0">Introducing Manus 2.0</a></li>
<li><a href="https://manus.im/blog/manus-cloud-computer">Introducing Cloud Computer: Lowering the Barrier to Building</a></li>
<li><a href="https://help.manus.im/en/articles/15392111-what-is-the-cloud-computer">What is the Cloud Computer? | Manus Help Center</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#Manus`, `#product launch`, `#personal assistant`, `#cloud computing`

---

<a id="item-9"></a>
## [Nura（原 postmarketOS）公布通往可日常使用的主线 Linux 手机路线图](https://postmarketos.org/blog/2026/09/29/road-to-main-category/) ⭐️ 7.0/10

原名 postmarketOS 的移动 Linux 发行版 Nura 发布了一篇题为《通往可日常使用的主线手机之路》的博客文章，阐述了让手机运行主线 Linux 内核、并可当作日常设备使用的路径。文章定位为面向项目「main」类别的路线图，而非产品发布或某项具体技术突破。 能否把 Linux 手机当作日常主力机使用，是移动 Linux 走出极客圈子的核心障碍；而转向主线内核意味着设备可以从上游获得安全与功能更新，而不必依赖被厂商放弃的定制内核分支。这对关注长生命周期、开放、可维修智能手机的人群意义重大，也牵动整个 Nura/postmarketOS 社区以及 KDE Plasma Mobile 等相关项目。 这条新闻本身几乎没有技术细节：正文仅包含一个指向 Lobste.rs 评论帖的链接，因此博客文章中提到的具体里程碑、内核版本或支持设备无法在此核实。可确认的项目背景是其为每款智能手机提供十年生命周期的目标，以及它基于轻量级的 Alpine Linux 发行版。

rss · Lobste.rs · 9月29日 19:20

**背景**: postmarketOS（简称 pmOS）是一款面向智能手机等移动设备的自由开源操作系统，基于 Alpine Linux，自 2016 年起开发、2017 年首次发布，到 2026 年已更名为 Nura。它可以运行 Phosh、Plasma Mobile、GNOME、MATE、XFCE 等多种移动界面。「主线（mainline）」指的是使用由内核开发者维护的上游 Linux 内核，与之相对的是 Android 手机上那种经过大量补丁、往往陈旧的厂商内核，或者 Halium 方案——后者通过复用 Android 驱动，让 Linux 用户空间跑在 Android 内核之上；KDE Plasma Mobile 已宣布放弃 Halium 支持，转而聚焦基于主线内核的手机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PostmarketOS">PostmarketOS</a></li>
<li><a href="https://nura.eco/">Nura // real Linux distribution for phones</a></li>
<li><a href="https://liliputing.com/kde-plasma-mobile-ends-halium-support-shifts-focus-to-phones-running-mainline-linux-kernel-en/">KDE Plasma Mobile ends Halium support, shifts focus to... - Liliputing</a></li>

</ul>
</details>

**标签**: `#postmarketOS`, `#mainline Linux`, `#mobile Linux`, `#daily-drivable`, `#open source phones`

---

<a id="item-10"></a>
## [ESPARGOS 的 ESP-SDR 让廉价 ESP32 芯片实现原始 IQ 采集](https://espargos.net/espsdr/) ⭐️ 7.0/10

ESPARGOS 项目发布了 ESP-SDR，在 espargos.net/espsdr/ 上展示了如何利用乐鑫（Espressif）的低成本 ESP32 微控制器直接采集原始 IQ 基带采样，从而把这款 Wi-Fi 芯片变成一个简易的软件定义无线电接收机。 传统 SDR 硬件（如 USRP 设备或 RTL-SDR 电视棒）价格从几十美元到上千美元不等，而如今用几美元的微控制器就能获取原始基带采样，这有望大幅降低无线研究、Wi-Fi 感知实验和业余 SDR 项目的入门成本。 该方法利用了 ESP32 集成的 2.4 GHz Wi-Fi 射频前端及其对基带数据的内部访问能力，但也继承了芯片本身的限制：仅支持 2.4 GHz 单频段、采样率与带宽有限、没有通用宽带射频前端，因此它更适合研究与教学用途，而无法取代专用 SDR 硬件。

rss · Lobste.rs · 9月29日 22:13

**背景**: 软件定义无线电（SDR）是指把传统上由模拟硬件实现的混频器、滤波器、放大器、调制器和解调器等部件改由通用处理器上的软件来完成，从而使同一套硬件能够处理多种不同的无线协议。原始 IQ 采集指的是在解调之前记录基带信号的同相（I）与正交（Q）分量，让软件可以自由地分析或解码任意波形。ESP32 是乐鑫（Espressif）推出的热门廉价 Wi-Fi/蓝牙微控制器，广泛用于物联网设备，传统上它只对外提供解码后的数据包或信道状态信息（CSI），而不提供原始采样。ESPARGOS 正是基于此类 ESP32 硬件构建的开源无线研究平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Software-defined_radio">Software-defined radio</a></li>

</ul>
</details>

**标签**: `#SDR`, `#ESP32`, `#Embedded Systems`, `#Wireless`, `#IQ Capture`

---