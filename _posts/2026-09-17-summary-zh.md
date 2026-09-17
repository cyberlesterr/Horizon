---
layout: default
title: "Horizon Summary: 2026-09-17 (ZH)"
date: 2026-09-17
lang: zh
---

> 从 61 条内容中筛选出 12 条重要资讯。

---

1. [OpenJDK 发布 JDK 27，Java 开发工具包最新主要版本](#item-1) ⭐️ 9.0/10
2. [小米为 MiMo 2.6 开放实时强化学习后训练看板](#item-2) ⭐️ 8.0/10
3. [黑客曝光 Flock 车牌识别摄像头中的硬编码凭证漏洞](#item-3) ⭐️ 8.0/10
4. [特斯拉发布无方向盘、无踏板、无后视镜的 Cybercab](#item-4) ⭐️ 8.0/10
5. [隐私集体 Autistici/Inventati 因政治动机断供而关闭](#item-5) ⭐️ 8.0/10
6. [Unicode 联盟发布 Unicode 标准 18.0.0 版本](#item-6) ⭐️ 8.0/10
7. [4B 蒸馏模型声称生成比 Postgres 快 81%的查询计划](#item-7) ⭐️ 7.0/10
8. [腾讯、字节、阿里「会战」AI 办公，Agent 格局生变](#item-8) ⭐️ 7.0/10
9. [小米一夜发布四款澎程汽车、三颗玄戒芯片与 15999 元折叠屏](#item-9) ⭐️ 7.0/10
10. [小鹏人形机器人 IRON 走下自动化产线](#item-10) ⭐️ 7.0/10
11. [Google Pixel 10 上的 C2PA 来源签名被成功伪造](#item-11) ⭐️ 7.0/10
12. [GNOME 51 桌面环境正式发布](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [OpenJDK 发布 JDK 27，Java 开发工具包最新主要版本](https://openjdk.org/projects/jdk/27/) ⭐️ 9.0/10

OpenJDK 正式发布了 JDK 27，这是 Java 开发工具包的最新主要版本，官方项目页面 openjdk.org/projects/jdk/27/ 作为该版本的发布入口。该页面列出了此版本包含的各项特性（JEP），并提供下载链接和构建信息。 Java 迄今仍是部署最广泛的服务端与企业级语言之一，因此每一个新的 JDK 主要版本发布对整个软件工程社区都是重大事件。这些版本持续带来语言、类库和 JVM 层面的渐进式改进，企业最终会逐步采纳，同时也为团队规划未来迁移到长期支持版本提供了特性储备。 与所有现代 OpenJDK 版本一样，JDK 27 遵循基于时间的六个月发布节奏，而非由特性驱动的排期，通常会将正式定稿的特性（JEP）与预览版或孵化器 API，以及部分被弃用或被移除的内容混合在一起。这类非 LTS 版本通常只获得较短的更新窗口，随后便被下一版本取代，因此项目页面上的 JEP 列表才是了解实际变更的权威依据。

rss · Lobste.rs · 9月16日 03:17

**背景**: OpenJDK 是 Java SE 平台的开源参考实现，由 Oracle 与更广泛的社区共同开发，几乎所有生产环境中的 Java 运行时都源自它。自 2017 年的 JDK 9 起，OpenJDK 改为每六个月发布一个新主要版本（分别在三月和九月），并且每三个版本中有一个被指定为长期支持（LTS）版本，例如 JDK 17、21 和 25。这种节奏意味着大多数开发者只会每隔一两个版本才升级，并用中间版本预览那些日后将进入 LTS 的特性。

**标签**: `#Java`, `#JDK`, `#OpenJDK`, `#Release`, `#Programming Languages`

---

<a id="item-2"></a>
## [小米为 MiMo 2.6 开放实时强化学习后训练看板](https://mimo.xiaomi.com/rl/) ⭐️ 8.0/10

小米在 mimo.xiaomi.com/rl/ 上线了一个公开的实时看板，直播其下一代模型 MiMo 2.6（页面显示为 mimo-v2.6-pro）的强化学习后训练过程，实时展示奖励曲线、rollout 采样和评测指标。页面当前显示该训练处于第 11 步左右，约 1,568 个 rollout 样本中有 1,312 个被接受，训练于 2026-09-15 10:32 UTC 启动。 对前沿模型团队来说，公开直播训练过程十分罕见——厂商通常会在正式发布前对后训练细节保密，因此此举进一步巩固了小米作为开源 AI 玩家的定位，也延续了其此前开源 MiMo-V2.5-Pro 的路线。它让开发者和研究者能提前看到一款有竞争力的编程模型究竟是如何被“调教”出来的，也可能抬高其他实验室在透明度方面的门槛。 该看板聚焦的是后训练（即预训练之后的强化学习/对齐阶段）而非预训练本身，因此它只暴露了 rollout 接受率和奖励曲线的进展，并未披露模型规模、架构或数据细节。社区评论者指出，上一代 MiMo-V2.5-Pro 在 DeepSWE 1.1 编程基准上仅得 19%，远落后于 Fable（70%）、Kimi K3（69%）和 Astra（74%）等模型，因此外界正密切关注 2.6 这一轮训练是否会在编程能力上实现跃升。

hackernews · r/LocalLLaMA · krackers · 9月16日 20:09 · [社区讨论](https://news.ycombinator.com/item?id=49732270)

**背景**: 大语言模型通常分两个阶段构建：先在海量文本语料上做预训练以学习通用规律，再通过监督微调、偏好优化或强化学习进行后训练以塑造模型行为。后训练是把原始基座模型变成可用的智能体或编程助手的关键环节，而它的奖励曲线通常属于内部资料，不会对外公开。小米的 MiMo 系列是该公司参与开源大模型竞赛的入口，此前发布的 MiMo-V2.5-Pro 是其迄今能力最强的开源模型，主打智能体能力、复杂软件工程和长周期任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mimo.xiaomi.com/rl/">mimo-v2.6 RL</a></li>
<li><a href="https://aiweekly.co/alerts/xiaomi-publishes-live-post-training-dashboard-for-mimo-26-rl-run-streams-real">Xiaomi opens live RL post-training dashboard for Mimo 2.6</a></li>
<li><a href="https://en.wikipedia.org/wiki/Post-training_of_large_language_models">Post-training of large language models</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的反应总体正面但相当务实：一位工程师表示自己每天用 MiMo-V2.5 做软件开发，投入产出比极高、成本远低于 Anthropic 级别的替代方案，并形容它能力不错，只是偶尔会陷入幻觉循环、多任务处理偏弱。其他人则对比基准分数（2.5-Pro 在 DeepSWE 1.1 上仅 19%，而 Fable、Kimi K3、Astra 均在 70% 以上），调侃训练成本之高，并讨论开源 AI 是否会从战略上威胁闭源实验室的商业模式。

**标签**: `#AI`, `#LLM`, `#open-source`, `#post-training`, `#Xiaomi`

---

<a id="item-3"></a>
## [黑客曝光 Flock 车牌识别摄像头中的硬编码凭证漏洞](https://www.wired.com/story/hackers-flock-camera-data-shows-how-system-works/) ⭐️ 8.0/10

Wired 与 404 Media 联合报道称，黑客成功入侵了 Flock Safety 的车牌识别摄像头，并在设备中发现了硬编码凭证（包括一个 API key）以及以明文形式存储的凭证，相关研究由 Micah Lee 发布。此后 Distributed Denial of Secrets 公布了摄像头的分区镜像文件，使被提取的文件系统公之于众。 Flock Safety 是美国最大的自动车牌识别（ALPR）供应商之一，其摄像头部署在数千个社区并被全国各地的警察部门使用，因此其硬件存在的系统性缺陷会动摇公众对整个大规模监控基础设施类别的信任。此次披露表明，任何能物理接触到这些安装在公共场所的摄像头的人，都可能提取数据或凭证，从而引发隐私与公共安全方面的双重担忧。 被硬编码的是 API key 而非管理员密码，但它似乎可用于请求那些以明文存储、看起来能够访问 Flock 服务器的凭证；不过攻击者以摄像头身份通过认证后究竟能做什么，目前仍不清楚。Flock 的漏洞披露政策也遭到批评：凡需要报告者“交互”设备或服务、或下载其数据的问题都被排除在外，实际上把大部分硬件类漏洞排除在受理范围之外。

hackernews · driverdan · 9月16日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=49726586)

**背景**: 自动车牌识别（ALPR）系统利用摄像头和光学字符识别软件自动抓取车牌号码，将其转换为可检索的文本，并与涉案车辆数据库进行比对。Flock Safety 是美国此类摄像头的主要供应商，其设备通常安装在公共场所，宣传卖点是帮助警方更快找到证据。硬编码凭证是一类广为人知的漏洞：如果攻击者能够逆向工程或通过物理方式提取固件，其中的 API key、密码等内嵌密钥就可能被还原并用于攻击后端服务器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Automatic_number-plate_recognition">Automatic number-plate recognition - Wikipedia</a></li>
<li><a href="https://www.beyondtrust.com/resources/glossary/hardcoded-embedded-passwords">What are Hardcoded Passwords/Embedded Credentials? | BeyondTrust</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论总体非常尖锐：有人认为硬编码凭证是“彻底无能”的表现，也有人指出 Flock 的漏洞披露政策主要是为了摆出负责任的姿态，而不是真心想了解漏洞。还有人把这归因于“纯粹的偷懒”和为缩短上市时间而牺牲安全启动与密钥管理，并强调对于部署在无防护公共场所的硬件，其威胁模型必须包含本地物理接触；另有评论者提到了 404 Media 的平行讨论以及 DDoSecrets 公布的分区镜像。

**标签**: `#security`, `#privacy`, `#surveillance`, `#vulnerability-disclosure`, `#iot`

---

<a id="item-4"></a>
## [特斯拉发布无方向盘、无踏板、无后视镜的 Cybercab](http://www.geekpark.net/news/370425) ⭐️ 8.0/10

9 月 3 日，特斯拉举办了一场没有直播、仅邀请少数人参加的小型发布会，正式展示没有方向盘、没有踏板、也没有侧后视镜的 Cybercab，并披露了其技术配置与初步商业化进展。特斯拉同时在官网挂出车队采购意向登记表，并允许奥斯汀用户通过去年上线的 Robotaxi 叫车应用预约体验 Cybercab，但目前该车尚未向普通客户开放销售。 自动驾驶出租车业务在特斯拉估值中已占极大比重：摩根士丹利对特斯拉 400 美元目标价中约有 120 美元来自该业务，而美国银行曾将其估值为 8440 亿美元，相当于特斯拉当时估值的一半左右。如果 Cybercab 真能按宣称的成本量产和运营，竞争焦点就会从技术演示转向规模化运营，直接挑战 Waymo 并重塑网约车行业格局。 Cybercab 采用线控刹车，且每个车轮都配备独立执行器以实现安全冗余，驱动形式为前轮驱动，搭载可支撑 50 万英里使用寿命的 4680 电芯、48V 低压电气架构，以及类似 HW4 的自动驾驶计算平台。其单车成本据推算已压至 2.3 万至 2.5 万美元，远低于一台含传感器与改装成本的 Waymo 车辆（约 7 万至 15 万美元），运营成本目标为每英里 0.2 至 0.25 美元；不过得州公开记录显示，截至 9 月 3 日特斯拉仅有 420 辆车注册用于无人驾驶运营、45 辆 Cybercab 获授权，而 Waymo 在美国 14 个城市约有 4000 辆无人驾驶车辆。

rss · 极客公园 · 9月16日 06:30

**背景**: 自动驾驶出租车（Robotaxi）指没有安全员、可提供付费载客服务的无人驾驶车辆，业内通常将其视为 SAE L4 级自动驾驶。特斯拉自 2016 年起就在描绘这样一张网络，并于 2024 年 10 月在洛杉矶一家电影制片厂展示了 Cybercab 原型，而这次发布的车型被定位为支撑该网络走量的产品。线控刹车是指用电子信号驱动刹车执行器、去除传统液压或机械踏板连接的技术，因此车辆可以完全不装刹车踏板；48V 低压电气架构则被越来越多车企采用，以减轻线束重量并支撑更多电子设备。行业争论的核心是技术路线：特斯拉坚持摄像头加人工智能的纯视觉方案，Waymo 则认为摄像头、激光雷达与毫米波雷达缺一不可，且 L2 系统无法直接放大成 L4。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sohu.com/a/790624760_430526">硬核科技论 | 没刹车了脚感还不变？线控刹车系统究竟怎么个事？_搜狐汽车_搜狐网</a></li>
<li><a href="https://www.autohome.com.cn/ask/1914029.html">线控刹车是什么意思-汽车之家</a></li>
<li><a href="http://www.cntronics.com/connect-art/80046357">关于 汽 车 48 V 电 气 架 构 ，这些趋势值得了解-互连技术- 电 子元件技术网</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#Cybercab`, `#自动驾驶`, `#Robotaxi`, `#电动汽车`

---

<a id="item-5"></a>
## [隐私集体 Autistici/Inventati 因政治动机断供而关闭](https://keepitfree.ai/announcements/a/i-shuts-down-stay-human/) ⭐️ 8.0/10

由志愿者运营的意大利集体 Autistici/Inventati（A/I）已被关闭，它此前托管着约 2 万个邮箱账户、5 千个邮件列表、1500 个网站以及大量博客。根据该公告和记者 Anne Roth 的说法，关闭并非源于针对该集体的法律程序，而是通过带有政治动机、绕过法律程序的“断供银行服务”（debanking）实现的。 这一事件表明，由活动人士独立运营的隐私基础设施未必会毁于技术攻击或法律诉讼，而可能因为被切断银行与支付渠道而瓦解——这正是它的单点故障。它促使社区把财务与社会层面的韧性，而不只是加密和服务器加固，视为任何承载政治敏感用户的服务必须具备的核心安全要求。 所谓 debanking（去银行化／断供银行服务），是指银行以客户构成财务、法律、监管或声誉风险为由关闭其账户；此处强调“绕过法律程序”，意味着账户是在政治压力下被关闭的，既没有正当程序，也没有公开的法律依据。从背景看，这发生在美国政府对 该集体采取更严厉行动之后，其中包括国务院将 Autistici/Inventati 指定为“特别指定全球恐怖分子”——该集体及其支持者认为这一标签实际上是针对合法的反法西斯、女权与酷儿行动主义。

rss · Lobste.rs · 9月16日 06:05

**背景**: Autistici/Inventati（常缩写为 A/I，与人工智能或算法毫无关系）是一个意大利黑客行动主义集体，2001 年由反全球化运动成员创立，他们还曾支持 Indymedia Italy 对热那亚八国集团峰会的报道。该集体为反对法西斯主义、军国主义、种族主义、性别歧视和恐同的左翼团体与活动人士，免费提供非营利的电子邮件、邮件列表、博客和网站托管服务。Debanking 一般指银行关闭其认为有风险的账户；当政府实际上命令或施压银行这么做时，它就变成了一种金融排斥工具，整个过程大多在幕后进行，账户持有人几乎得不到正当程序保障。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Debanking">Debanking - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Autistici/Inventati">Autistici/Inventati - Wikipedia</a></li>
<li><a href="https://www.cato.org/policy-analysis/understanding-debanking-evaluating-governmental-operational-political-religious">Understanding Debanking: Evaluating Governmental, Operational, Political, and Religious Financial Account Closures | Cato Institute</a></li>

</ul>
</details>

**社区讨论**: 该条目被提交到 Lobsters，并把讨论定位为探讨如何不仅在技术上、也在社会与财务层面保障平台安全，而讨论的起点正是提交者本人的评论。由于原始材料没有提供具体的评论内容，因此无法概括讨论中的具体观点。

**标签**: `#privacy`, `#censorship`, `#debanking`, `#infrastructure`, `#activism`

---

<a id="item-6"></a>
## [Unicode 联盟发布 Unicode 标准 18.0.0 版本](https://www.unicode.org/versions/Unicode18.0.0/) ⭐️ 8.0/10

Unicode 联盟发布了 Unicode 标准 18.0.0 版本，这是定义几乎所有现代软件中字符与文本编码方式的核心规范。官方发布页面主要起到公告作用，并将读者引向相关讨论帖，而非在页面本身详尽列出全部新增内容。 由于 Unicode 几乎是所有文本处理层的底层基础，一次大版本更新会波及字体、输入法、渲染引擎、正则表达式库、数据库以及搜索与排序逻辑。操作系统厂商、云服务商和应用开发者通常需要更新各自的 Unicode 数据表与工具链，以保持同步。 Unicode 各版本是累积式的：每次发布都会在码位空间中新增字符与文字系统，且往往包含新的 emoji，而已分配的码位保持稳定，因此既有数据仍可正常工作。实现方通常通过升级共享数据和库（如 ICU（International Components for Unicode）数据、字体表以及正则与排序表）来跟进新版本，而不必重写应用代码。

rss · Lobste.rs · 9月16日 17:38

**背景**: Unicode 是由 Unicode 联盟维护的字符编码标准，该联盟是一家总部位于美国加州山景城的非营利组织，其主要目标是取代 ASCII 等容量有限且彼此不兼容的旧式编码方案。上一个版本 17.0 定义了 159,801 个字符，涵盖日常、文学与历史文本中使用的 172 种文字系统。该标准已被 XML、Java 编程语言、Swift 以及现代操作系统广泛采用，其技术决策由 Unicode 技术委员会（UTC）作出，成员包括 Adobe、Apple、Meta、Google、Microsoft 和 Salesforce 等公司。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Unicode">Unicode - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Unicode_Consortium">Unicode Consortium</a></li>
<li><a href="https://learn.microsoft.com/en-us/globalization/encoding/unicode-standard">The Unicode standard - Globalization | Microsoft Learn</a></li>

</ul>
</details>

**标签**: `#unicode`, `#standards`, `#internationalization`, `#text-encoding`, `#release`

---

<a id="item-7"></a>
## [4B 蒸馏模型声称生成比 Postgres 快 81%的查询计划](https://rohanbansal.com/qorl) ⭐️ 7.0/10

一篇发布于 rohanbansal.com/qorl 的博客描述了一个通过蒸馏（从更大模型的“Astra”轨迹中学习）训练出的 4B 参数模型，用于生成数据库查询计划，并在一个 8GB 全内存基准上报告了 1.81 倍的几何平均加速和 44.7%的总延迟下降。作者为此花费约 800 美元从 Lambda 租用 2 块 H100 SXM 节点约 95 小时，并支付约 400 美元的 OpenAI API 费用来生成演示数据。 这是把小型蒸馏 LLM 应用于长期由算法密集型经典优化器主导领域的一次罕见尝试，也说明前沿模型的能力可以被压缩进一个廉价的 4B 模型。如果该方法能够泛化，可能会改变查询优化器的构建方式，并降低学习式优化研究的成本。 标题所宣称的成果依赖于一个很窄的实验环境——8GB 数据集完全放进内存、shared_buffers 被限制为其中一小部分、缓存经过预热、且只跑只读 SELECT——批评者认为这很容易过拟合；作者也承认蒸馏数据来自某个更大闭源模型的输出，这引发了数据来源方面的疑问。

hackernews · polyphilz · 9月16日 18:50 · [社区讨论](https://news.ycombinator.com/item?id=49731285)

**背景**: 查询优化是数据库决定一条 SQL 语句如何被物理执行（用哪些索引、连接顺序等）的环节，传统优化器依赖代价模型和启发式规则而非神经网络。知识蒸馏是一种把大型“教师”模型的知识迁移到更小的“学生”模型上的技术，使学生模型能在普通硬件上低成本运行。研究者多年来一直在探索“学习式查询优化器”（如 Neo），但基于 LLM 的计划生成仍基本处于实验阶段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/1904.03711">[1904.03711] Neo: A Learned Query Optimizer</a></li>
<li><a href="https://bolinding.github.io/papers/fnt24learnedqo-draft.pdf">Learned Query Optimizers</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论既有见地又持怀疑态度：有评论指出 8GB 全内存、缓存预热、只读的实验设置容易过拟合，未必适用于更真实的 OLTP 负载；也有人设想了 LLM 规划器在生产环境中“幻觉”漏掉一个索引、需要反复重跑的场景。还有人认为最优计划构建高度依赖数学和算法，解决方案空间会随即时索引（just-in-time indexes）而进一步膨胀，AlphaGo 式的神经启发式方法比“钝器”LLM 更合适。

**标签**: `#databases`, `#query-optimization`, `#llm`, `#postgres`, `#machine-learning`

---

<a id="item-8"></a>
## [腾讯、字节、阿里「会战」AI 办公，Agent 格局生变](http://www.geekpark.net/news/370431) ⭐️ 7.0/10

极客公园发布了一篇访谈式分析，创新工场联合首席执行官汪华与 Floatboat.ai 创始人兼 CEO 谭少卿在文中解读了腾讯、字节、阿里为何集体扑向 AI 办公 Agent：字节正式发布「豆包工作」并把 TRAE、扣子团队整体并入，7 月底飞书产品团队也已并入豆包；腾讯的 WorkBuddy 已跑出千万月活，阿里则在整合桌面 Agent、云端 Agent 与钉钉能力。 访谈中的核心观点是，Agent 打破了移动互联网「用户规模即价值」的旧逻辑：Claude Code 在月活不到千万时 ARR 据报道就已达到约 200 亿美金，这说明未来的高价值经济入口可能建立在法律、财务等专业工作流之上，而不在高日活的消费级流量里。正因如此，巨头此番投入更像是由恐惧驱动，而非由用户指标驱动；而它们砸钱的同时也无意中替整个市场完成了 Agent 普及教育，为创业公司打开了细分机会。 汪华把算力经济列为第二个驱动力：豆包这类 C 端产品因为推理负担极重，只能用压缩过的小模型，所以「有时觉得它智障」；而办公 Agent 恰好卡在理想区间，既能体现大模型真实能力，又不会因用户规模过大压垮算力，商业模式还能跑通。他还认为，近期发布的 GLM-5.3-Flash、DeepSeek-V4-Flash 等低价 Flash 模型把指令遵循能力提上去、把成本打下来，才让国产模型真正跨过了那道坎；而巨头在新战场唯一的壁垒其实只有钱，钱能兑换的仅仅是算力。

rss · 极客公园 · 9月16日 06:39

**背景**: 所谓 AI Agent，并不只是聊天，而是能替用户规划并执行多步骤任务的系统，比如写文档、做 PPT、跑代码；它通常由基础模型加上一层「Harness」（为模型提供工具、记忆与长程任务控制的脚手架）组成。在国内，豆包是字节的大众聊天机器人，TRAE 是字节的 AI 编程 IDE，扣子是它的 Agent 搭建平台，腾讯的 WorkBuddy 则是面向办公知识工作者的多智能体桌面工作台。2026 年初，一款被称作「小龙虾」的极客向 Agent 产品曾引发热潮，但用户需要自己配置 Linux 环境，受访者认为它属于重要但并非面向大众的过渡形态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.workbuddy.ai/">WorkBuddy - AI Agent for Everyday Office Work</a></li>
<li><a href="https://traeide.com/docs/what-is-trae-ide">What is Trae IDE ?</a></li>
<li><a href="https://docs.z.ai/guides/vlm/glm-5.3-flash">GLM - 5 . 3 - Flash - Overview - Z.AI DEVELOPER DOCUMENT</a></li>

</ul>
</details>

**标签**: `#AI Agents`, `#AI Office`, `#Industry Analysis`, `#LLM`, `#China Tech`

---

<a id="item-9"></a>
## [小米一夜发布四款澎程汽车、三颗玄戒芯片与 15999 元折叠屏](http://www.geekpark.net/news/370423) ⭐️ 7.0/10

在 9 月 7 日晚的秋季发布会上，小米一次性推出四款澎程系列车型（N70 Pro 20.99 万元、N70 Max 23.99 万元、N90 Max 26.99 万元、N90 Max 探索版 29.99 万元）、三颗自研玄戒芯片（O3、O100、D100），以及小米史上首款起售价破万的手机小米 18 Fold，起售价 10999 元，陶瓷版最高 15999 元。小米披露，澎程系列在开售后 4 分钟内锁单量突破 10000 台。 这是小米迄今为止最集中的一次战略展示：把汽车、芯片与高端消费电子放在同一条叙事线上，而两个半小时中有约一个半小时留给澎程汽车，明确显示造车已成为其核心增长押注。一次发布三颗自研芯片，其中两颗面向端侧 AI 与智能驾驶，使小米跻身少数试图打通“手机到汽车”全算力链的厂商之列。 玄戒 O3 采用 3nm 十核全大核架构（6 超大核+4 大核，最高主频 4.35GHz），小米称其是业界首个安兔兔跑分突破 500 万的 SoC，也是首个支持 LPDDR6 内存的芯片；玄戒 O100 采用全球首款 6nm 3D 晶圆级堆叠先进封装与混合键合工艺，带宽达 1.22TB/s、端侧推理速度 330 TPS；玄戒 D100 则被称为国内首款 3nm 智驾高算力 AI 芯片，拥有 160GB 统一内存。三颗芯片中只有 O3 会在本月随小米 18 Fold 上市，O100 与 D100 已完成研发验证，将于明年正式商用。

rss · 极客公园 · 9月16日 06:27

**背景**: 小米于 2021 年启动造车业务，此前以追求极致性能的 SU7 和 YU7 建立口碑。2026 年 7 月，小米发布继摩德纳平台之后的第二套整车技术架构“小米昆仑技术架构”，澎程系列正是基于该架构、主打大而平整且可变的车内空间，当时已首发 N90 Max。玄戒芯片线从 O1 起步，小米称其累计出货已超百万台；手机方面，小米 18 Fold 是公司首款中折叠旗舰，切入的是苹果首款折叠屏预计定价更高的高端折叠市场。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.donews.com/news/detail/5/6682739.html">小 米 发布三款 玄 戒 自研 芯 片 ，覆盖 AI...</a></li>
<li><a href="https://www.jingjiribao.cn/static/detail.jsp?id=673346">小 米 昆 仑 技 术 架 构 、澎程系列新车发布</a></li>
<li><a href="https://en.wikipedia.org/wiki/小米汽车">小米汽车</a></li>

</ul>
</details>

**标签**: `#小米`, `#电动汽车`, `#自研芯片`, `#折叠屏`, `#消费电子`

---

<a id="item-10"></a>
## [小鹏人形机器人 IRON 走下自动化产线](http://www.geekpark.net/news/370421) ⭐️ 7.0/10

9 月 8 日，小鹏宣布高阶通用人形机器人 IRON 完成自动化总装并正式下线，这台机器人不是工程师手工拼装，而是像汽车一样经过整条工业化产线完成自动化总装。小鹏称这是全球首条高阶人形机器人自动化产线，核心制程自动化率超过 80%。 这条消息标志着人形机器人行业的竞争主线正从炫技式 Demo 转向量产与商业化，接下来比拼的是产线、供应链、良率、成本、数据闭环和交付能力。对小鹏而言，这是其覆盖智能汽车、Robotaxi、人形机器人和飞行汽车的物理 AI 战略的一次集中兑现，也给仍在攻克量产的特斯拉、Figure 等对手抬高了门槛。 IRON 全身拥有 76 个自由度，单手 21 个自由度，采用全包覆柔性晶格，控制器、运动模组和灵巧手等核心部件均为自研，并搭载 3 颗小鹏自研图灵 AI 芯片，有效算力达 2250 TOPS，以端侧算力减少对云端连接与远程操控的依赖。需要注意的是，该消息整体偏公司宣传，缺少经过独立验证的技术参数与产线细节，也未回答「谁来买单」这一关键的 PMF 问题。

rss · 极客公园 · 9月16日 06:16

**背景**: 具身智能（Embodied AI）是指基于物理身体进行感知和行动的智能系统，它通过与环境的交互获取信息、做出决策并采取行动，与生活在服务器里的 ChatGPT 等「离身智能」不同。被英伟达黄仁勋反复提及的「物理 AI」，则指把 AI 真正嵌入机器人、自动驾驶、智能制造等物理系统。小鹏早在 2020 年就切入机器人赛道，2026 年 6 月何小鹏亲自兼任机器人业务 CEO，8 月该业务完成超 9 亿美元首轮融资，投后估值超 63 亿美元。这条路并不平坦：2025 年科技日 IRON 走「猫步」曾引发「真人套壳」质疑，团队不得不现场剪开腿部皮肤自证；2026 年 2 月 IRON 在深圳湾万象城首次公开亮相时又突然失衡摔倒。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://juejin.cn/post/7486670839923359796">什 么 是 具 身 智 能 ？ 具 身 智 能 （Embodied Intelligence...</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/1997089083625854818">一文读懂：黄仁勋重点布局的“物理AI”（Physic AI）</a></li>
<li><a href="https://baike.baidu.com/item/灵巧手/67387238">灵巧手（人形机器人末端执行器）_百度百科</a></li>

</ul>
</details>

**标签**: `#人形机器人`, `#小鹏`, `#具身智能`, `#量产制造`, `#机器人产业`

---

<a id="item-11"></a>
## [Google Pixel 10 上的 C2PA 来源签名被成功伪造](https://www.hackerfactor.com/blog/index.php?/archives/1102-C2PA-and-Pixel-Glitter-Milk.html) ⭐️ 7.0/10

Hacker Factor 博客发布的一篇新技术分析表明，Google Pixel 10 上的 C2PA（Content Credentials，内容凭证）实现所生成的来源签名可以被伪造，攻击者因此能够给并非由该设备真实拍摄的内容附上一个看起来完全有效的真实性清单。文章完整演示了这一伪造过程，证明该标准所宣称的密码学保证在这一软硬件组合上并不能抵御有决心的攻击者。 C2PA 是业界应对深度伪造和 AI 生成虚假信息的主要方案之一，背后有 Adobe、Google、微软等厂商支持，因此在一款旗舰手机上出现可实际利用的绕过手段，会直接动摇“带有签名内容凭证即代表照片真实”这一前提。如果来源签名在拍摄环节就能被伪造，该标准有可能沦为一种虚假的信任背书，而被平台、新闻机构和司法系统过度依赖。 C2PA 的工作方式是在文件中嵌入一份签名清单，记录内容由谁创建、何时创建、使用什么工具以及事后是否被修改，并通过签名把这份记录绑定到经过验证的身份或设备上。这一发现的要害在于：验证只能证明“某个密钥签署了该清单”，而不能证明图像真的来自摄像头传感器——因此，除非签名密钥由防篡改硬件保护，并且验证策略会检查该硬件证明，否则整条信任链都会失效。

rss · Lobste.rs · 9月16日 13:24

**背景**: C2PA 全称“内容来源与真实性联盟”（Coalition for Content Provenance and Authenticity），是一个制定开放、免版税技术标准的行业组织，用于给媒体内容附加经过密码学签名的来源元数据，其产物以“Content Credentials（内容凭证）”之名面向消费者宣传。与之相关的、由 Adobe 发起的“内容真实性倡议”（Content Authenticity Initiative）负责推动该标准的普及；近年多款旗舰手机（包括 Google 的 Pixel 系列）开始支持该标准，使照片携带可验证的来源记录。数字图像取证则是与之互补的领域，通过分析像素和元数据本身来侦测篡改，而 C2PA 签名本应让这项工作变得更容易。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Content_Authenticity_Initiative">Content Authenticity Initiative - Wikipedia</a></li>
<li><a href="https://c2pa.org/">C2PA | Verifying Media Content Sources</a></li>
<li><a href="https://www.ssl.com/products/content-authenticity/content-credentials/">Content Credentials C2PA Provenance - SSL.com</a></li>

</ul>
</details>

**标签**: `#C2PA`, `#content-provenance`, `#security`, `#image-forensics`, `#AI-misinformation`

---

<a id="item-12"></a>
## [GNOME 51 桌面环境正式发布](https://release.gnome.org/51/) ⭐️ 7.0/10

GNOME 项目在其官方发布站点 release.gnome.org 上公布了 GNOME 51 的正式发布公告，标志着这一桌面环境最新编号版本的到来。该公告页面是整个版本发布的官方入口，用于引导用户查看发行说明和获取方式，而提交链接本身并未展开具体的改动细节。 GNOME 是使用最广泛的 Linux 桌面环境之一，并且是 Fedora、Ubuntu、Debian 等主流发行版的默认桌面，因此一个新编号版本会在数月内惠及数百万桌面用户。每一次发布也同时影响着下游打包者、主题与扩展开发者，以及面向 GNOME 技术栈的应用开发者。 该提交除了指向 Lobsters 评论区的链接外，并没有提供实质性的发布内容，因此新功能、GTK 或 Shell 的改动、已知问题等具体信息都需要直接查阅官方发布页面。与其他 GNOME 版本一样，版本号按照固定的六个月的节奏递增，随后还会有用于修复缺陷与安全问题的小版本，用户通常通过发行版的升级周期或 GNOME OS 这类滚动测试镜像获得它。

rss · Lobste.rs · 9月16日 18:05

**背景**: GNOME 是面向 Linux 及其他类 Unix 系统的自由开源桌面环境，由全球志愿者社区开发，并由 GNOME 基金会协调。它提供 Shell、窗口管理、核心应用以及许多其他项目所依赖的 GTK 工具包。GNOME 采用基于时间的发布节奏，大约每年发布两个大版本，而 release.gnome.org 上的公告页面则是项目对每个版本最权威的官方总结。

**标签**: `#gnome`, `#linux`, `#desktop-environment`, `#open-source`, `#release`

---