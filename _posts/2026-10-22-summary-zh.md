---
layout: default
title: "Horizon Summary: 2026-10-22 (ZH)"
date: 2026-10-22
lang: zh
---

> 从 56 条内容中筛选出 8 条重要资讯。

---

1. [PyPI 上的 LiteLLM 1.107.0 遭入侵，被植入凭证窃取器与后门](#item-1) ⭐️ 9.0/10
2. [DuckDB 2.0.0 LTS“Cinnamon Teal”发布：新增客户端-服务器模式与触发器](#item-2) ⭐️ 9.0/10
3. [PHP 8.2.35 发布，修复“PHP2Shell”严重远程代码执行漏洞](#item-3) ⭐️ 9.0/10
4. [Railway 平台披露安全事件，解密后的环境变量疑似泄露](#item-4) ⭐️ 8.0/10
5. [GitLab 发布关键补丁，修复 CVSS 10.0 可未认证触发的正则编译器漏洞](#item-5) ⭐️ 8.0/10
6. [eMudhra 的 CA 密钥熵值过低，毫秒级即被破解](#item-6) ⭐️ 8.0/10
7. [谷歌发布官方 Rust 风格指南](#item-7) ⭐️ 7.0/10
8. [CVE-2026-107891：musl libc 的 regcomp 整数溢出可导致堆损坏](#item-8) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [PyPI 上的 LiteLLM 1.107.0 遭入侵，被植入凭证窃取器与后门](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) ⭐️ 9.0/10

发布到 PyPI 的 LiteLLM 1.107.0 版本遭到入侵，安装该版本时会向用户机器投放凭证窃取器和后门，而不是正常的库代码。据报道该恶意版本被较快地控制住，但在此之前已在 Python 与 LLM 工具生态中引发广泛关注。 LiteLLM 是被广泛部署的 LLM 网关和 Python SDK，通常管理着多家模型供应商的 API 密钥，因此其版本被污染后，泄露的恰恰是攻击者最想要的凭证。由于据报这已是同一项目在大约一年内的第二次类似入侵，这进一步说明基于 PyPI 的依赖信任模型以及“直接升级就完事”的日常习惯存在结构性风险。 据报该载荷同时包含凭证窃取器和后门，这意味着受影响的環境应被视为完全失陷，而不只是被装了一个吵闹的挖矿类软件包。防御方应固定并核验 LiteLLM 版本，检查 lockfile 与已安装的分发包中是否出现 1.107.0，并轮换在该版本运行过的主机上可被访问到的所有 API 密钥和云凭证。

hackernews · abhisek · 10月21日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=50181114)

**背景**: LiteLLM 由 BerriAI 开发，是一个开源 AI 网关和 Python SDK，提供统一的、兼容 OpenAI 的接口来调用一百多家不同的 LLM 供应商，既可以作为自托管代理运行，也可以作为库被导入使用。PyPI 是 Python 官方的第三方软件包仓库，也是 pip 默认的下载来源，因此任何发布到其上的恶意产物都可能被数量庞大的下游项目和 CI 流水线拉取。这类供应链攻击针对的是分发通道本身而非代码漏洞，攻击者一旦拿到某个流行软件包的发布凭证，就顺带继承了用户对该包已有的信任。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LiteLLM">LiteLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/PyPI">PyPI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Supply_chain_security">Supply chain security</a></li>

</ul>
</details>

**社区讨论**: 评论者更关注系统性问题而非载荷细节：有人认为一旦“权限弹窗疲劳”出现，像 LuLu 这类沙箱和防火墙规则就起不了作用；另一人则指出这已是大约一年内第二次严重的 LiteLLM 攻击事件，并提到自己重新审计依赖以确认没有任何项目引入它。讨论中反复出现的是疲惫与无奈的情绪——既惊讶于一个拥有数万次提交的项目也会以这种方式被攻破，也为本次事件似乎被较快控制住而感到庆幸。

**标签**: `#supply-chain-security`, `#pypi`, `#litellm`, `#malware`, `#dependency-management`

---

<a id="item-2"></a>
## [DuckDB 2.0.0 LTS“Cinnamon Teal”发布：新增客户端-服务器模式与触发器](https://duckdb.org/2026/10/21/announcing-duckdb-200) ⭐️ 9.0/10

DuckDB 团队于 2026 年 10 月 21 日发布 DuckDB 2.0.0 LTS，代号“Cinnamon Teal”（Spatula cyanoptera），带来大幅可扩展性提升、客户端-服务器架构以及 SQL 触发器。社区反馈称，其扩展能力已从此前约 64 vCPU 的上限提升到约 128–192 vCPU。 客户端-服务器能力使 DuckDB 从纯嵌入式库变为可作为共享分析服务器部署的产品，有望替代中小型组织依赖的多服务器数据栈。结合在高核心数云实例上的近线性扩展能力，DuckDB 已成为可信赖的“开箱即用数据仓库”，而不再只是快速的本地查询引擎。 实践者反馈称，超过约 192 vCPU 后速度仍无明显提升，因此扩展性依然存在上限而非无限。DuckDB 还自带名为“Quack”的通信协议，但客户端支持有限，因此多数用户通过 PostgreSQL 通信协议、ADBC 或 Arrow Flight 连接服务器。

hackernews · nnx · 10月21日 14:01 · [社区讨论](https://news.ycombinator.com/item?id=50181136)

**背景**: DuckDB 是一个开源 SQL 数据库管理系统，面向 OLAP（在线分析处理）负载，即以读取和聚合为主的分析型查询，而非事务处理。它的显著特点是像 SQLite 一样在宿主应用进程内运行，因此在 Python 和 R 的本地分析场景中广受欢迎。LTS 意为长期支持，DuckDB 1.4 是其首个 LTS 版本，2.0.0 延续了这一模式并提供更长的维护周期。嵌入式引擎历来是单进程运行，因此通过 PostgreSQL 通信协议提供客户端-服务器模式是一次重大的架构转变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://duckdb.org/2026/10/21/announcing-duckdb-200">Announcing DuckDB 2.0.0 LTS “Cinnamon Teal” – DuckDB</a></li>
<li><a href="https://duckdb.org/">An analytical SQL database management system – DuckDB</a></li>
<li><a href="https://en.wikipedia.org/wiki/Online_analytical_processing">Online analytical processing - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者热情高涨，讨论多聚焦生产实践：一位用户称 DuckDB 2.0 在 EC2 上能把 128–192 个 vCPU 跑满，并借此扩展 Splink 实体链接工具；另一位用户则将其 alpha 版本作为小型组织的集中式分析服务器，并借助扩展通过 PostgreSQL 通信协议或 Arrow Flight 连接。多人称客户端-服务器架构是“颠覆性的”，并认为触发器补齐了让 DuckDB 成为“开箱即用数据仓库”的最后一块拼图。

**标签**: `#duckdb`, `#databases`, `#analytics`, `#release`, `#olap`

---

<a id="item-3"></a>
## [PHP 8.2.35 发布，修复“PHP2Shell”严重远程代码执行漏洞](https://github.com/php/php-src/releases/tag/php-8.2.35) ⭐️ 9.0/10

PHP 8.2.35 已作为一次协同安全更新发布，修复了核心 PHP 中的“PHP2Shell”系列严重漏洞，这些漏洞可使未经身份验证的攻击者执行任意代码或泄露敏感的进程内存。此次披露由 Wiz、Calif 与 OpenAI 协同完成，社区成员指出该漏洞据称是通过 AI 辅助研究发现。 PHP 支撑着公共互联网的很大一部分，因此运行时自身出现 CVSS 9.2 的未授权远程代码执行漏洞，属于运维人员所能面对的最严重后果之一，迫使共享主机、CMS 部署和容器镜像全面紧急打补丁。该漏洞据称由 AI 辅助发现，这也加剧了一个更广泛的争论：机器驱动的漏洞发现将以多快速度超越打补丁的流程。 PHP2Shell 包含两个相关漏洞，均涉及 PHP 对异常请求终止的处理，都被归类为 CWE-824（访问未初始化指针），CVSS v4.0 评分为 9.2，且无需身份验证或用户交互即可触发。Cloudflare 已针对受影响的 PHP 运行时行为部署了 WAF 防护规则；评论者还报告了发布过程中的摩擦，包括 8.4.27 标签最初出现时缺少可用的 amd64 镜像。

hackernews · tuyuri · 10月21日 13:45 · [社区讨论](https://news.ycombinator.com/item?id=50180873)

**背景**: PHP 是一种广泛使用的服务端脚本语言，驱动着大量网站和 Web 框架，因此 PHP 运行时自身的缺陷会同时影响众多应用，而不只是某一个项目。远程代码执行（RCE）是一类漏洞，攻击者可通过网络在远程机器上运行任意命令或代码，通常是软件缺陷所能造成的最严重后果。PHP2Shell 通过协同漏洞披露（CVD）流程处理，即研究者、厂商与基础设施提供商约定在补丁和缓解措施就绪前对细节保密。在本例中，缓解措施既包括上游 PHP 版本发布，也包括第三方 Web 应用防火墙规则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.php2shell.com/">PHP 2 Shell — AI uncovers critical vulnerabilities in the backbone of...</a></li>
<li><a href="https://www.imperva.com/blog/php2shell-vulnerability-updates/">PHP 2 Shell : When PHP Runs Out of Memory at the Wrong... | Imperva</a></li>
<li><a href="https://blog.cloudflare.com/php-vulnerabilities-waf-protection/">Cloudflare deploys protections against php 2 shell vulnerability</a></li>

</ul>
</details>

**社区讨论**: Hacker News 讨论帖极为活跃（955 分、529 条评论），从业者称这可能是 20 年来最严重的 PHP 安全事件，但同时表示并未抢先下线服务器，并批评了此次发布流程的处理方式。评论者交叉引用了三个相关讨论帖（PHP 基金会的安全公告、最初的 PHP2Shell 技术文章，以及被编号为 CVE-2026-109618/-109619 的 session.upload_progress 堆释放后使用漏洞），还有人推测可能仍有第二个漏洞尚未披露。其他人则详细记录了运维时间线，指出公告发布约两个半小时后镜像仍不可用。

**标签**: `#PHP`, `#security`, `#RCE`, `#vulnerability-disclosure`, `#AI-security-research`

---

<a id="item-4"></a>
## [Railway 平台披露安全事件，解密后的环境变量疑似泄露](https://blog.railway.com/p/security-disclosure-wednesday-october-21st) ⭐️ 8.0/10

云 PaaS 服务商 Railway 于 10 月 21 日（周三）发布安全披露公告，承认发生了一起疑似导致客户解密后环境变量泄露的安全事件。社区成员随即报告称，已有第三方在实际使用窃取到的密钥，开源社媒排程工具 Postiz 的创始人表示，他的服务正因为泄露的密钥而被攻击者搞垮。 在 PaaS 平台上，环境变量通常存放数据库凭据、API token 和第三方服务密钥，一旦泄露，攻击者可以直接横向进入客户的基础设施和数据，而不只是影响平台本身。Railway 承载了许多小型团队和独立开发者的生产服务，这些用户往往没有专职安全人员，因此影响范围远超服务商自身，所有受影响的用户都需要立即轮换凭据。 这份披露在技术细节上相当简略：没有明确说明攻击入口、暴露时间窗口以及受影响项目的数量，评论者还指出 Railway 在客户公开爆料之前一直保持沉默。攻击者似乎能够读取解密后的环境变量，这意味着入侵触及了密钥解密环节，而不只是加密存储的静态数据，这是更为严重的失效形式。

hackernews · Lobste.rs · 10月21日 21:58 · [社区讨论](https://news.ycombinator.com/item?id=50188228)

**背景**: Railway 是一个平台即服务（PaaS），开发者只需连接 GitHub 仓库、Docker 镜像或本地代码，平台便负责构建、部署、托管与可观测性，并提供托管数据库。与多数 PaaS 一样，它把数据库连接串、API 密钥等应用配置以环境变量的形式保存，静态加密、运行时解密后注入容器。这种设计使解密密钥和运行时注入链路成为高价值攻击目标：任何能读取解密后数值的人，就等于拿到了应用持有的全部密钥。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tech.vibequant.cc/tech/paas-railway-railway-getting-start-en/">Railway .com Getting Started Guide — VibeQuant</a></li>
<li><a href="https://www.huntress.com/blog/railway-paas-m365-token-replay-campaign">Threat Actors Abuse Railway .com PaaS as Microsoft 365... | Huntress</a></li>
<li><a href="https://www.appsdeveloperblog.com/aws-lambda-environment-variables-encryption-decryption/">AWS Lambda Environment Variables - Encryption & Decryption</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（105 条评论）基本是在印证而非质疑这起事件：多位用户称看到 Railway 的 Discord 中有人确认，存放在 Railway 上的密钥已被第三方使用，这支持了“解密后的环境变量可被读取”的推测。评论者还把它放到当天密集爆发的安全事件背景中——PHP 远程代码执行漏洞（php2shell）与 eMudhra 证书泄露——不少人担心这种节奏正成为新常态，并把它与上周末 opencode 遭遇的攻击相提并论。

**标签**: `#security`, `#data-breach`, `#cloud-infrastructure`, `#secrets-management`, `#paas`

---

<a id="item-5"></a>
## [GitLab 发布关键补丁，修复 CVSS 10.0 可未认证触发的正则编译器漏洞](https://docs.gitlab.com/releases/patches/patch-release-gitlab-19-5-1-released/) ⭐️ 8.0/10

GitLab 发布了一个计划外的关键补丁版本 19.5.1，修复编号为 CVE-2026-110264 的漏洞。该漏洞严重程度为最高级（CVSS 10.0），无需登录认证即可被触发，并可导致自建 GitLab 实例上的远程代码执行。据媒体报道，受影响的自建版本最早可追溯至 GitLab 7.0，而 GitLab.com 与 GitLab Dedicated 已运行修复后的代码。 GitLab 是部署最广泛的 DevOps 平台之一，自建实例通常存放源代码、CI/CD 凭据和流水线密钥，因此一个可未认证触发的代码执行漏洞对软件供应链而言几乎是最危险的情形。由于攻击端点无需任何账号即可访问，任何暴露在外的实例都可能成为自动化攻击的目标，管理员必须尽快升级。 该安全公告部分处于保密状态，技术细节披露有限，但据报道漏洞涉及正则表达式编译器中的整数溢出；独立分析认为 GitLab 的 CI/CD 正则编译路径使用了 Ruby 的 Onigmo 正则引擎，其中的整数溢出可被转化为原生代码执行。评论者还指出，这已是数周内至少第二个（按某些统计为第三个）与正则相关的 GitLab CVE，且 GitLab 公告中提供了检查日志以发现利用尝试的方法。

hackernews · Lobste.rs · 10月21日 19:01 · [社区讨论](https://news.ycombinator.com/item?id=50185869)

**背景**: GitLab 是一个集代码托管、问题跟踪与 CI/CD 流水线于一体的 DevOps 平台，既有托管服务版本，也提供由客户自行部署的社区版/企业版。正则表达式在 CI/CD 配置中随处可见（例如作业规则和路径匹配），因此 GitLab 需要借助底层正则引擎来编译用户提供的模式——在 Ruby 场景中就是 Onigmo。正则编译器是规模庞大的 C 代码，其中的整数溢出等内存安全缺陷可能破坏内存，最坏情况下可让攻击者在服务器上执行任意代码。GitLab 近几周已多次修复正则引擎相关缺陷，这也是外界将本次发布视为一种“模式”而非孤立事件的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/gitlab-warns-of-max-severity-rce-flaw-in-regex-compiler-engine/">GitLab warns of max severity code execution vulnerability</a></li>
<li><a href="https://thehackernews.com/2026/10/critical-gitlab-flaw-cvss-100-could.html">Critical GitLab Flaw (CVSS 10.0) Could Allow Unauthenticated ...</a></li>
<li><a href="https://www.rapid7.com/blog/post/ra-gitlab-ci-cd-regex-integer-overflow-technical-analysis-cve-2026-97229/">Rapid7 Analysis: GitLab CI/CD Regex Integer Overflow (CVE ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者对如此严重的漏洞竟然还不是当天最大的安全新闻感到不安，多位评论者指出这已是几周内至少第二个与正则相关的 GitLab CVE，同时称赞 GitLab 在公告中说明了如何检查日志以发现利用尝试。也有人强调这个关键 CVE 似乎处于保密状态，仅提到正则编译器中的整数溢出，并将其与同日发布的 musl libc 正则编译器整数溢出 CVE 相类比，还质疑根本原因究竟在 GitLab 还是在 Ruby 本身。

**标签**: `#security`, `#gitlab`, `#cve`, `#vulnerability-disclosure`, `#regex`

---

<a id="item-6"></a>
## [eMudhra 的 CA 密钥熵值过低，毫秒级即被破解](https://scotthelme.co.uk/eight-bits-of-trust-emudhras-ca-keys-cracked-in-milliseconds/) ⭐️ 8.0/10

eMudhra 的八个中间 CA 私钥被发现其实都是小于 256 的整数（其中一个甚至就等于 4），因此可以在毫秒级时间内完成因式分解。该问题几乎是用 Google 的 paranoid_crypto 工具“开箱即用”发现的，披露方还附带了签名证明，其他人随后已独立验证了全部 8 个密钥。 一个被主流信任存储收录的证书颁发机构实际上不具备任何密码学强度，这意味着任何人都能用它签发出可链接到受信任根的证书，从而动摇所有依赖方的 TLS 安全。这也暴露出 web PKI 信任模型在多大程度上依赖 CA 的运维水平，而这类细节几乎无人做深入审计。 Chrome 在证书透明度（CT）日志中没有发现被滥用的伪造证书，但修复意味着要刷新所有携带 CA 证书包的组件——操作系统的 ca-certificates、certifi、Node、Homebrew，以及重建容器基础镜像。有开发者用公布的证书链测试本地信任库后发现，12 条链中仍有 6 条能通过验证；而无法打补丁的设备则会继续无限期地信任这些已被攻破的中间证书。

hackernews · Lobste.rs · 10月21日 09:08 · [社区讨论](https://news.ycombinator.com/item?id=50177916)

**背景**: Web PKI 依赖浏览器和操作系统内置的根证书存储：根 CA 授权中间 CA，再由中间 CA 的私钥为服务器在 TLS 握手时出示的终端证书签名。RSA 的安全性建立在“分解由两个大素数相乘得到的模数非常困难”这一前提上，因此如果一个私钥本身就是很小的整数、或者含有极小的因子，它几乎提供不了任何保护。证书透明度（CT）日志则让研究者和浏览器厂商能够在事后发现并追查错误签发的证书。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/10/eight-emudhra-ca-keys-compromised.html">Eight eMudhra CA Keys Compromised, Triggering Emergency Fixes...</a></li>
<li><a href="https://dev.to/frankchu/eight-ca-private-keys-were-integers-under-256-i-recovered-all-eight-in-11-milliseconds-4o1f">Eight CA private keys were integers under 256.... - DEV Community</a></li>
<li><a href="https://datatracker.ietf.org/doc/html/draft-barreira-wpkops-trustmodel-00">Trust models of the Web PKI (Internet-Draft, 2013)</a></li>

</ul>
</details>

**社区讨论**: 社区反应在震惊之余带着黑色幽默：有高赞评论感叹“回头看，信任 100 个证书颁发机构也许本来就太多了”，也有人强调真正棘手的是那些无法打补丁的物联网和嵌入式设备。还有评论提出可以用这些弱密钥伪造证书来解锁或越狱锁定的硬件设备，并指出这种事似乎已经有人在做了。

**标签**: `#security`, `#TLS/PKI`, `#certificate-authority`, `#cryptography`, `#supply-chain`

---

<a id="item-7"></a>
## [谷歌发布官方 Rust 风格指南](https://google.github.io/styleguide/rustguide.html) ⭐️ 7.0/10

谷歌在 google.github.io/styleguide/rustguide.html 发布了官方的 Rust 风格指南，内容涵盖命名规范、导入方式、模块组织，以及针对 Chromium 的特定规则（例如对超小 crate 与模块嵌套的建议）。这份文档把谷歌内部 Rust 团队遵循的约定整理并公开，成为一份有权威性的参考。 借助 Chromium 和 Android，谷歌是工业界最大的 Rust 使用方之一，因此它公开的约定影响力超出自家代码库，为其他团队提供了一个跨项目、连贯一致的模仿范本，而不必再从零散的 rustfmt 和 clippy 配置里拼凑风格。这也直接介入了 Rust 生态关于「何为地道风格」的讨论——Rust 官方风格指南主要面向格式化，许多 API 层面的约定仍留给社区实践。 指南中包含 Chromium 专属规则，不鼓励深层模块嵌套、倾向使用非常小的 crate，并建议将类型名导入后不加限定地使用，而不是写全限定路径。它是一份风格文档，而非语言或工具链变更，因此没有任何条目由编译器强制，团队完全可以对个别建议持不同意见。

hackernews · Lobste.rs · 10月21日 19:11 · [社区讨论](https://news.ycombinator.com/item?id=50186010)

**背景**: Rust 官方风格指南主要关注格式化，大部分由 rustfmt 自动完成，而模块布局、导入风格、类型命名等问题更多依赖约定而非规则。Chromium 对 Rust 的支持大约从 2023 年正式开始，谷歌出于内存安全的考虑公开承诺把 Rust 引入浏览器代码库，而这种 C++/Rust 混合构建带来额外约束，例如必须使用 rust_static_library 这个 GN 模板。因此像谷歌这样的大型使用方最终会编写自己的风格指南，以保证成千上万名贡献者的代码保持一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://chromium.googlesource.com/chromium/src/+/HEAD/docs/rust/README.md">Chromium Docs - Getting Started with Rust in Chromium</a></li>
<li><a href="https://security.googleblog.com/2023/01/supporting-use-of-rust-in-chromium.html">Supporting the Use of Rust in the Chromium Project</a></li>
<li><a href="https://doc.rust-lang.org/style-guide/">Introduction - The Rust Style Guide</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍欢迎把各项约定集中在一处，认为它比从谷歌和 Meta 的项目里逆向推断风格更连贯、更可靠。主要反对意见集中在两点：一是 Chromium 偏好超小 crate 且禁止模块嵌套，有评论者将其比作 2010 年代「函数越小越好」的风潮，结果层层抽象反而让代码难以看懂；二是导入类型名后不加限定，有人认为这会丢失上下文，像 Source 这种泛化名字不查导入就不知所云。还有读者分享了一个实用的 rust-analyzer 技巧：在 trait 上方加上 #[rust_analyzer::prefer_underscore_import]，IDE 默认就会以 `as _` 的形式导入扩展 trait。

**标签**: `#rust`, `#style-guide`, `#google`, `#software-engineering`, `#code-quality`

---

<a id="item-8"></a>
## [CVE-2026-107891：musl libc 的 regcomp 整数溢出可导致堆损坏](https://www.openwall.com/lists/oss-security/2026/10/21/18) ⭐️ 7.0/10

CVE-2026-107891 披露了 musl libc 的 regcomp（POSIX 正则表达式编译函数）实现中存在多个整数溢出漏洞，这些问题可能导致分配大小计算错误，并引发越界堆写入。该通告于 2026 年 10 月 21 日发布在 oss-security 邮件列表中。 musl libc 广泛用于嵌入式 Linux 系统、Alpine 等容器基础镜像以及静态链接二进制程序，因此核心例程中的内存破坏漏洞可能影响大量已交付的软件。由于 regcomp 会处理模式字符串，能够影响被编译正则表达式的攻击者可能触发堆破坏，这使得该问题值得 musl 相关产品尽快排查。 该漏洞被描述为 regcomp 中的多个整数溢出，会导致分配大小错误和越界堆写入，但现有通告摘要并未说明受影响的 musl 版本、触发条件或修复提交。诸如利用是否要求恶意正则表达式模式，以及对典型应用的实际影响等问题，仍需从完整通告或上游补丁中确认。

rss · Lobste.rs · 10月21日 17:40

**背景**: musl 是由 Rich Felker 创建的轻量级、符合标准的 Linux C 标准库，作为 glibc 的替代方案；其 MIT 许可证和静态链接特性使其在嵌入式系统和精简容器镜像中很受欢迎。regcomp 是 POSIX 函数，负责将正则表达式模式编译为 regexec 使用的内部形式，其解析器必须根据不可信或应用提供的模式计算缓冲区及数据结构大小。此类大小计算中的整数溢出可能导致分配不足，随后写入超出堆缓冲区末尾，这是典型的内存安全弱点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Musl_libc">Musl libc</a></li>
<li><a href="https://www.musl-libc.org/intro.html">musl - Introduction</a></li>
<li><a href="https://linux.die.net/man/3/regcomp">regcomp (3): POSIX regex functions - Linux man page</a></li>

</ul>
</details>

**标签**: `#security`, `#cve`, `#musl`, `#libc`, `#memory-safety`

---