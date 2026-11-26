---
layout: default
title: "Horizon Summary: 2026-11-26 (ZH)"
date: 2026-11-26
lang: zh
---

> 从 36 条内容中筛选出 12 条重要资讯。

---

**科技新闻**
1. [grh-lean 将 Anthropic 的 GRH 验证缩至约 7.6 万行](#item-tech-news-1) ⭐️ 8.0/10
2. [1Password 安全事件导致客户账户信息被窃](#item-tech-news-2) ⭐️ 8.0/10
3. [Minecraft Java 版资源包字体 RCE 漏洞](#item-tech-news-3) ⭐️ 8.0/10
4. [FCC 批准 SpaceX 部署最多 100 万颗 Starmind 卫星](#item-tech-news-4) ⭐️ 8.0/10
5. [矩阵乘法指数九分之四引发 AI 发现争议](#item-tech-news-5) ⭐️ 7.0/10
6. [Google 发布 Cogentic 计算数学论文集](#item-tech-news-6) ⭐️ 7.0/10
7. [OpenAI 加码 GPT-6 Cyber 与 Daybreak](#item-tech-news-7) ⭐️ 7.0/10
8. [腾讯开源 Hy4 flash 量化权重，Strata 支持 64GB Mac mini](#item-tech-news-8) ⭐️ 7.0/10
9. [亚洲数据中心转向美国客户消化算力](#item-tech-news-9) ⭐️ 7.0/10
10. [OpenAI 面向少量客户测试私有推理](#item-tech-news-10) ⭐️ 7.0/10

**财经新闻**
1. [美商务部据报施压英特尔交出 10%股权](#item-finance-news-1) ⭐️ 8.0/10
2. [美国拟按国别加征新关税](#item-finance-news-2) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [grh-lean 将 Anthropic 的 GRH 验证缩至约 7.6 万行](https://github.com/lsernau/grh-lean) ⭐️ 8.0/10

GitHub 项目 lsernau/grh-lean 发布了一个更短、强调可读性的 Lean 形式化版本，针对 Anthropic 的广义黎曼假设（GRH）验证工作。项目称其把原约 1700 万行缩减到约 7.6 万行，降幅约 99.56%，旨在让研究人员更容易审查和理解这一大型证明工件。现有材料未提供独立的数学验证，代码规模缩减也不代表核心论证已经得到清楚解释。

hackernews · nb-t · 11月25日 21:48 · [社区讨论](https://news.ycombinator.com/item?id=50648050)

**「原 1700 万行证明的精简背景」** Anthropic 数学家 Levent Alpöge 于 11 月 20 日发布的原始 Lean 4 证明约有 1700 万行代码，这正是本次精简所针对的前身。新的 GitHub 仓库提供两个覆盖同样五个定理的独立项目：可读版约 30 万行，紧凑版约 7.6 万行；MIT Mathematics 页面同时说明，原 1700 万行证明的检查结果被放在另一页面。

**「降低 Lean 证明的审查门槛」** 相较于讨论中约 1700 万行的 Anthropic 证明工件，公开仓库提供了更短的 Lean 4 版本，使数学审查者和 Lean 开发者能够直接审阅精简后的证明，并核对仓库声明使用的 \`propext\`、\`Classical.choice\` 和 \`Quot.sound\` 三项公理。公开的独立检查页报告已检查该形式化、且依赖来自 Mathlib 上游正式版本；相关团队在引用或审计前应实际运行该检查，但代码更短并不意味着核心数学论证已获数学界独立验证。

**「社区讨论」** spootydooty 认为约 30 万行的版本通过区分“已知数学”和“新数学”并加入面向人的文档，有助于理解证明，但这与摘要所称的约 7.6 万行并不一致。gre 询问代码精简是否回应了 Tao 一个月前对“庞大但缺乏洞见的证明”的担忧，AIShill101 则希望数学家把核心论证写成真正的数学论文并在国际会议上报告；这些属于评论者的判断与建议，而非验证结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/lsernau/grh-lean">GitHub - lsernau/grh-lean: A short Lean 4 proof of the ...</a></li>
<li><a href="https://math.mit.edu/~drew/shortgrh/">Shorter GRH Lean proof: verification files - MIT Mathematics</a></li>
<li><a href="https://stackfutures.com/blog/anthropic-riemann-lean-proof-17m-to-76k-lines-shorter-grh-nov-2026/">The Riemann Hypothesis Lean Proof Just Shrank From 17 Million ...</a></li>
<li><a href="https://github.com/lsernau/grh-lean">GitHub - lsernau / grh - lean : A short Lean 4 proof of the Generalized...</a></li>
<li><a href="https://news.ycombinator.com/item?id=50648050">Much shorter version of GRH Lean verification from Anthropic</a></li>
<li><a href="https://mrubinst.github.io/grh-lean-verification/">GRH Lean Check</a></li>

</ul>
</details>

**标签**: `#Lean`, `#formal verification`, `#GRH`, `#theorem proving`, `#mathematics`

---

<a id="item-tech-news-2"></a>
### [1Password 安全事件导致客户账户信息被窃](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password 确认，攻击者入侵员工的企业 GitHub 账户，取得源代码访问权限并向后台服务推送恶意代码，随后下载了部分客户的账户信息；公司称客户保险库及其中内容未受影响。泄露字段包括姓名、邮箱地址、账户标识、创建及最近登录时间，受影响用户数量尚未披露。1Password 已停用涉事账户、轮换或撤销可能暴露的内部凭证，并加强邀请和恢复邮件的验证码验证；公司称用户无需更改账户，但需警惕利用相关资料制作的高质量钓鱼邮件。

hackernews · lxhrstn · 11月25日 17:18 · [社区讨论](https://news.ycombinator.com/item?id=50644817)

**「事件背景」** 理解这起事件的关键，是区分客户后台管理数据与加密保险库内容：1Password 于 2026 年 11 月 19 日开始调查员工企业 GitHub 账户失陷，攻击者随后借该账户取得源代码并向后台服务推送恶意代码，导致部分客户管理数据被下载。1Password 表示保险库及其中的内容未受影响，但这仅说明该入侵路径未触及加密保险库，并不代表后台客户数据没有泄露。

**「账户资料泄露增加定向钓鱼风险」** 此次被下载的是姓名、邮箱、账户标识、创建及最近登录时间等客户元数据，可被用于制作更逼真的定向钓鱼或冒充请求；1Password 明确称客户保险库及其内容从未被访问或提供给攻击者，因此不应认定库内密码已经泄露。用户目前无需更改账户，但应特别核查异常的共享链接、邀请、账户恢复邮件和登录请求，避免点击链接或提交凭据。

**「社区讨论」** 评论者认为，员工 GitHub 账户被攻破后仍能向生产服务推送代码，暴露了 SaaS 环境的严重凭据与代码发布风险；一名使用本地保险库的长期用户也担忧，恶意代码可能被用于攻击在线保险库通信。另有用户称事件后收到包含其个人资料和可用保险库分享链接的钓鱼邮件，但邮件是否确实源自此次泄露尚无法确认；其他评论者还指出，公告没有充分说明主分支保护是否启用或如何被绕过。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving 1Password’s backend ...</a></li>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving... | 1 Password</a></li>

</ul>
</details>

**标签**: `#1Password`, `#security incident`, `#SaaS security`, `#credential phishing`, `#incident response`

---

<a id="item-tech-news-3"></a>
### [Minecraft Java 版资源包字体 RCE 漏洞](https://github.com/bikini/minecraft2shell) ⭐️ 8.0/10

据 11 月 22 日公开的 minecraft2shell 项目披露，恶意服务器资源包中的特制 TrueType 字体可触发 FreeType 2.14.3 及更早版本的原生越界写，并在受影响的 Minecraft Java 版 Windows 客户端实现任意代码执行。报告称 Java 版 1.20.5 至 1.21.10 以及 26.1 至 26.4 快照受影响，1.20.4 及更早版本和基岩版不受影响；该项目已提供公开 PoC。Mojang 目前仍使用 lwjgl-freetype 3.4.3，官方尚未发布补丁。社区于 11 月 24 日发布 m2sfix 1.0.0，可通过 Java agent 或 mod 关闭 hinting；修复前应避免添加资源包、将多人游戏服务器的资源包权限设为“禁用”，或安装该临时修复。

telegram · zaihuapd · 11月25日 12:46

**「资源包字体的原生解析链路」** 理解这一漏洞的关键是，Java 版客户端会通过 lwjgl-freetype 3.4.3 调用 FreeType 解析资源包中的 TrueType 字体；报告指出，FreeType 2.14.3 及更早版本可被恶意字体触发原生越界写。受影响范围从 Java 版 1.20.5 开始，而 1.20.4 及更早版本和基岩版不受影响，因此风险点位于 Java 客户端处理资源包字体的原生代码链路，而非所有 Minecraft 客户端。

**「风险范围与临时应对」** 受影响范围是 Java 版 1.20.5—1.21.10 和 26.1—26.4 快照；1.20.4 及更早版本和基岩版不在报告的受影响范围内。服务器资源包中的特制 TrueType 字体可触发 FreeType 越界写并获得客户端代码执行权，但公开 PoC 明确验证的是 Mojang 签名的 Java 26.3 Windows 客户端及其内置 FreeType 2.14.3 x64，尚不能等同于对所有受影响版本的独立验证。正式补丁发布前，玩家应禁用服务器资源包权限且不要安装资源包，或按项目说明使用 m2sfix 1.0.0 Java agent 或 mod 关闭 hinting；社区补丁只是临时缓解措施，并非 Mojang 官方修复。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/bikini/minecraft2shell">GitHub - bikini/ minecraft 2 shell : Minecraft to native RCE · GitHub</a></li>

</ul>
</details>

**标签**: `#Minecraft`, `#Remote Code Execution`, `#FreeType`, `#Font Security`, `#Vulnerability Disclosure`

---

<a id="item-tech-news-4"></a>
### [FCC 批准 SpaceX 部署最多 100 万颗 Starmind 卫星](https://www.geekwire.com/2026/fcc-clears-spacex-million-satellites-starmind-data-center/) ⭐️ 8.0/10

据 GeekWire 报道，美国联邦通信委员会（FCC）批准 SpaceX 部署最多 100 万颗 Starmink 数据中心卫星，用于构建在轨数据处理网络；这是美国首次批准此类太空数据中心星座，卫星运行轨道高度为 500 至 1002 公里。授权要求提供通信备份、定期提交进展报告并制定轨道碎片减缓详细方案，首颗卫星须在 2033 年前投入运行，整个星座须在 2040 年前全部运行。FCC 同时驳回了亚马逊、Viasat 和美国天文学会提出的反对意见。

telegram · zaihuapd · 11月26日 04:45

**「Starmind 许可的分阶段部署」** Starmind 源自 SpaceX 于 2026 年向 FCC 提交的许可申请；获批并不等于可以立即发射全部卫星。BBC 对许可证里程碑的梳理显示，部署须在 2033 年 11 月前启动、2035 年 11 月前完成 10%、2038 年 11 月前完成 50%，而 SpaceX 表示计划在 2027 年发射首颗卫星。

**「部署时间与频谱协调限制」** 这项批准不会立即带来可用的在轨数据处理容量：首颗 Starmind 卫星须不晚于 2033 年投入运行，整个星座须在 2040 年前全部运行，因此近期服务规划不能把 SpaceX 的授权视为已部署能力。FCC 文件显示，SpaceX 表示除有限的备份和应急支持外，不计划让 Starmind 卫星使用 Ka 频段，依赖常规 Ka 带宽的运营方不应将该星座计入日常新增容量；此外，尽管 FCC 驳回了美国天文学会关于光污染和射电干扰的异议，地面观测站仍可能需要在后续部署中协调观测安排并采取干扰缓解措施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cwp836l8n1jgo">US approves SpaceX plan to send a million data satellites to space</a></li>
<li><a href="https://nypost.com/2026/11/25/business/fcc-approves-elon-musks-spacex-to-launch-1-million-satellites-for-data-centers-in-space/">FCC approves Elon Musk&#x27;s SpaceX to launch 1 million satellites for...</a></li>
<li>DA-26-1273A1.txt - Federal Communications Commission</li>
<li>FCC Clears SpaceX to Launch 1 Million Starmind Data Center Satellites - BASENOR</li>

</ul>
</details>

**标签**: `#太空数据中心`, `#SpaceX`, `#FCC`, `#卫星星座`, `#轨道基础设施`

---

<a id="item-tech-news-5"></a>
### [矩阵乘法指数九分之四引发 AI 发现争议](https://scottaaronson.blog/?p=10379) ⭐️ 7.0/10

Scott Aaronson 的文章转引题为《矩阵乘法指数是九分之四》的论文结果，并将其与 AI 辅助数学发现联系起来，认为相关能力进展及其影响被严重低估。该结果的具体指标是矩阵乘法指数 ω=9/4；但现有材料未说明论文作者、证明细节、验证状态或 AI 的具体贡献，因此不能据此确认 AI 已能自主完成此类数学发现。

hackernews · Kotlopou · 11月25日 19:11 · [社区讨论](https://news.ycombinator.com/item?id=50646108)

**「背景」** 矩阵乘法指数 ω 通常定义为使 n×n 矩阵相乘的代价降至 O\(n^ω\) 的指数下确界，因此“九四分之二”首先意味着已知的通用上界达到 2.25，并不等于已经证明 ω 的精确值就是 9/4。该结果的重要性在于它改变了渐近计算复杂度上界，而不只是让某次具体的矩阵运算跑得更快。

**「理论收益不等于实际加速」** 九分之四的结果意味着矩阵乘法可由 O\(n^2.25\) 的渐进算法处理，算法研究者需要据此更新复杂度比较；但它并不等于“2.25 倍加速”，材料也未给出隐藏常数、适用规模或硬件基准，因此生产团队不应直接据此改写 GEMM 内核。HN 中一名评论者把“让德国铁路准点运行”视为更有意义的 AI 成效，这也说明数学突破要转化为实际影响，仍需通过可测量的服务和业务指标验收。

**「评论分歧」** 评论区的核心分歧是，数学能力提升能否外推到广泛科学与灾难性后果：jsLavaGoat 认为 AI 擅长分析性和先验性数学，但这不意味着它能解决所有科学问题，更不能直接推出 AI 会消灭人类；nickysielicki 则认为目前没有实验室已攻破密码系统的证据，并承认这只是低信心的判断。Nevermark 认为人类会因无法想象变化量级而系统性低估这场“认知接力”，sunir 则援引 Bruno Latour 的“计算中心”概念说明科学突破对组织及知识基础设施的依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50646108">Holy shit holy shit holy shit holy shit : The magnitude... | Hacker News</a></li>

</ul>
</details>

**标签**: `#AI-assisted discovery`, `#matrix multiplication`, `#AI safety`, `#algorithms`

---

<a id="item-tech-news-6"></a>
### [Google 发布 Cogentic 计算数学论文集](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) ⭐️ 7.0/10

Google 在 Google Research 的 GitHub 仓库发布了一组 Cogentic 研究论文，主题包括整数因数分解、离散对数以及其他计算数学问题。目前可确认的是论文集合已经公开；现有材料没有提供论文摘要、具体结论或可复现实验，因此尚无法判断这些成果相对既有方法的创新性、实际性能及其对密码学分析的影响。

hackernews · rgwohlbold · 11月25日 13:33 · [社区讨论](https://news.ycombinator.com/item?id=50642086)

**「Cogentic 的研究基础」** Cogentic 的原始论文将其定义为一种面向开放研究问题的多智能体自动证明发现框架，通过编排多个智能体协作探索证明。此次 Google 论文集展示了该框架在整数分解、离散对数及其他计算数学问题上的具体应用，但现有材料未提供论文摘要、评审状态或实验数据，尚不足以判断其相对既有算法的实际突破。

**「实际影响与验证要求」** 这批论文为密码学和计算数学研究者提供了可审查的具体主张，包括时间复杂度为 L\_N\[1/3, O\(1\)\] 的无条件整数因数分解结果，以及固定特征有限域上的次拟多项式离散对数算法；若这些界限经独立验证，才可能改变相关算法的理论性能评估。目前 Google 的因数分解结论仍属于理论复杂度主张，公开 Lean 证明和外部评审尚待完成，因此不能据此认定现有系统已获得实用破解能力，也不宜立即调整安全参数；研究者应先核查证明、适用假设与复现结果，再评估兼容性或迁移需求。

**「社区将其视为数学突破浪潮的一部分」** 部分评论者将 Cogentic 论文与 AlphaGo、Navier–Stokes 方程、Riemann 假设和 Erdős 问题等案例并列，认为 AI 与资金投入正在改变数学研究的可能性，也有人猜测这次发布只是更大趋势的开端。不过，这些均是社区中的观点或未经证实的传闻，并未构成对 Cogentic 具体方法和成果的直接评价。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.40324">Cogentic : Multi-Agent Orchestration for Automated Proof Discovery</a></li>
<li><a href="https://magica.com/news/google-cogentic-six-math-papers-factoring-proof-claim">Google Cogentic claims new factoring bound in six math papers ...</a></li>
<li><a href="https://daily.dev/posts/google-releases-cogentic-papers-on-integer-factorization-discrete-logs-and-more-0lfmvr55g">Google Releases Cogentic Papers on Integer Factorization ...</a></li>

</ul>
</details>

**标签**: `#AI for mathematics`, `#cryptography`, `#integer factorization`, `#Google Research`, `#algorithms`

---

<a id="item-tech-news-7"></a>
### [OpenAI 加码 GPT-6 Cyber 与 Daybreak](https://www.theinformation.com/newsletters/ai-agenda/openais-roadmap-making-cyber-bigger-coding-remains-blurry) ⭐️ 7.0/10

OpenAI 已推出面向安全研究的 GPT-6 Cyber，并扩大“网络安全受信访问”计划 Daybreak；截至 2026 年 9 月，报道称该计划覆盖数千名经过验证的防御者以及约 2,000 个获批组织和工作空间，可用于漏洞发现、代码库分析与二进制逆向。公司 CFO 认为外界对 3,000 亿美元以上网络安全市场规模的估计仍被严重低估，总裁格雷格·布罗克曼则称网络安全可能成为比编程更大的业务板块。不过，这些判断来自公司高管及《The Information》的转述，目前仍缺少与 Anthropic、Google 竞争相关的技术基准、详细产品信息及规模化商业化验证。

telegram · zaihuapd · 11月25日 04:51

**「OpenAI 网络安全布局的背景」** 这条路线并非只有单一模型：OpenAI 于 2026 年 2 月发布“Trusted Access for Cyber”，以信任机制扩大前沿网络安全能力的使用，同时强化防止滥用的约束；11 月 5 日推出的 GPT‑6 Cyber 则被定位为在授权范围内发现可利用漏洞并制定修复方案的模型。配套的 Daybreak 面向公用事业、州及地方政府、社区银行、非营利组织和开源项目开放注册，OpenAI 承诺以 10 亿美元补贴其访问、培训、技术支持与合作项目。

**「采购与落地影响」** 对计划将模型接入漏洞研究、代码库分析或二进制逆向流程的团队，API 成本已成为选型重点：据 VentureBeat 报道，GPT-6 Cyber 的输入和输出价格分别比 GPT-5.6 Cyber 高约 60% 和 33%，采购前应按现有工作负载测算总费用。Daybreak 则被定位为面向企业与政府的漏洞检测、补丁验证和安全开发自动化平台，但目前没有规模化效果基准，潜在用户还需确认组织审批资格及其与现有漏洞管理流程的集成效果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/trusted-access-for-cyber/">Introducing Trusted Access for Cyber - OpenAI</a></li>
<li><a href="https://openai.com/daybreak/">Daybreak | OpenAI for cybersecurity</a></li>
<li><a href="https://openai.com/index/introducing-gpt-6-cyber/">GPT‑6 Cyber: Advancing the frontier of aligned cybersecurity ...</a></li>
<li><a href="https://venturebeat.com/technology/openai-launches-gpt-6-cyber-with-stronger-exploit-research-and-higher-api-price-than-anthropic-and-google">OpenAI launches GPT-6 Cyber with stronger exploit research ...</a></li>
<li><a href="https://www.csoonline.com/article/4170029/openai-introduces-daybreak-cyber-platform-takes-on-anthropic-mythos.html">OpenAI introduces Daybreak cyber platform, takes on Anthropic ...</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#网络安全`, `#生成式AI`, `#漏洞研究`

---

<a id="item-tech-news-8"></a>
### [腾讯开源 Hy4 flash 量化权重，Strata 支持 64GB Mac mini](https://mp.weixin.qq.com/s/o0xxShVQX6g2UllrrEv1WQ) ⭐️ 7.0/10

腾讯混元通过 AngelSlim 开源了 224B 参数 Hy4 flash 的 GGUF 量化权重：原始权重约 410.27 GiB，最小的 IQ2-AH 版本为 125.73 GiB，约为原版的 30%。据发布方数据，借助 Strata offload 框架，64 GB Mac mini 可运行该模型；48 GB 显存设备在 10K 上下文下生成速度为 89 token/s，M5 Max 128 GB 上的 Q3\_K 版本在 32K 上下文下为 47 token/s。发布方还称 Q3\_K 在 DeepSWE v1.1 等评测中与原模型得分差距不超过 0.4 分，但现有来源未提供完整评测方法或独立验证。

telegram · zaihuapd · 11月25日 09:29

**「量化与卸载的技术前提」** 要让 224B 参数模型进入本地推理，必须同时处理权重体积和设备内存：此次 IQ2-AH 量化虽将权重从约 410.27 GiB 降至 125.73 GiB，但仍超过 64 GB，因此“在 Mac mini 上运行”还依赖 Strata 的 offload 路径，而非仅靠量化将模型全部装入内存。AngelSlim 的官方 Hy4-flash-GGUF 页面还提供了通过 llama.cpp 在 macOS、Linux 上使用这些权重的说明，为现有本地推理工具链提供了接入方式。

**「本地运行条件与复测要求」** 这为开发者提供了在 64 GB Mac mini 上运行 224B 模型的量化与卸载路径，但实际使用需要 Strata offload 支持，不能把 125.73 GiB 的 IQ2-AH 权重视为可完整驻留 64 GB 内存；若按发布方数据采用 Q3\_K，还应自行复测任务得分和速度，因为当前性能与 DeepSWE 差距主要由厂商数据支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/AngelSlim/Hy4-flash-GGUF">AngelSlim/Hy4-flash-GGUF · Hugging Face</a></li>
<li><a href="https://huggingface.co/AngelSlim/Hy4-flash-GGUF/blob/main/Hy4-flash-Q3_K-00001-of-00002.gguf">Hy4-flash-Q3_K-00001-of-00002.gguf · AngelSlim/Hy4-flash-GGUF ...</a></li>
<li><a href="https://www.aibase.com/news/32527">Tencent Hunyuan open-sources Hy4 flash GGUF quantized weights ...</a></li>

</ul>
</details>

**标签**: `#LLM quantization`, `#GGUF`, `#model offloading`, `#open-source AI`, `#Apple Silicon`

---

<a id="item-tech-news-9"></a>
### [亚洲数据中心转向美国客户消化算力](https://www.bloomberg.com/news/articles/2026-11-25/asia-data-centers-sound-out-us-clients-to-replace-china-demand) ⭐️ 7.0/10

美国政府收紧了曾让中国科技公司获得英伟达最先进芯片的漏洞，促使亚洲多地数据中心争相把原本面向中国客户、如今面临过剩的算力转售给美国买家。Liquid Compute 首席执行官 Ronit Jain 称，针对先进 AI 加速器出口的新规正冲击依赖中国客户的数据中心服务商；但现有报道未说明具体规则、受影响规模，也未提供独立佐证。

telegram · zaihuapd · 11月25日 11:35

**「此前的芯片出口漏洞与算力需求」** 此前，美国针对英伟达先进 AI 加速器的出口规则存在漏洞，使中国科技公司能够获得其最先进芯片；亚洲部分新型云数据中心因此预期通过中国客户消化新增的 B300 算力。华盛顿收紧规则后，原本由中国客户承接的 B300 容量转为过剩供给，租赁价格下行，促使这些数据中心转向美国和西欧买家。

**「算力客户转向与审查收紧」** 原本依赖中国客户消化算力的亚洲数据中心服务商需要调整客户结构，将过剩算力转售给美国买家；TrendForce 还报道称，全球银行因美国 AI 芯片出口管制加强了对东南亚数据中心客户的审查，影响已延伸至融资交易。现有材料未披露转售规模、适用芯片型号或具体审查标准，运营商能否合规并完全替代中国需求仍不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-25/asia-data-centers-sound-out-us-clients-to-replace-china-demand">Asia Data Centers Sound Out US Clients to Replace China ...</a></li>
<li><a href="https://www.explainx.ai/blog/asia-neoclouds-remarket-b300-us-western-buyers-banks-november-2026">Asia DCs Offload B300 to US: Banks Review Loans - explainx.ai</a></li>
<li><a href="https://thenextweb.com/news/asia-data-centres-b300-prices-us-buyers-chip-rules">Asian data centres look to US buyers as US chip rules bite ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-25/asia-data-centers-sound-out-us-clients-to-replace-china-demand">Asia Data Centers Sound Out US Clients to Replace China Demand</a></li>
<li><a href="https://www.trendforce.com/news/2026/11/25/news-global-banks-reportedly-push-southeast-asian-data-center-clients-to-reveal-ai-chip-users-amid-u-s-curbs/">[News] Global Banks Reportedly Push Southeast Asian Data Center ...</a></li>

</ul>
</details>

**标签**: `#AI芯片`, `#出口管制`, `#AI算力`, `#数据中心`

---

<a id="item-tech-news-10"></a>
### [OpenAI 面向少量客户测试私有推理](https://x.com/sama/status/2125638790593274259) ⭐️ 7.0/10

OpenAI 正在与少量客户测试其“OpenAI Private Intelligence”系列最新产品 Private Inference（私有推理），旨在以更强的隐私保护支持企业将前沿 AI 用于更多工作场景。OpenAI 称，在零数据保留（ZDR）方案中启用私有安全处理（Private Safety Processing）后，安全审查可自动完成，且公司员工无法接触底层内容。目前该项目仍处于有限测试阶段，现有信息未提供技术架构、审计方式、客户范围或性能数据，因此这些隐私保证的实际范围与效果尚待验证。

telegram · zaihuapd · 11月26日 01:44

**「私有推理的隐私基础」** 理解这次测试的关键，是 OpenAI Private Intelligence 系列所采用的两层隐私机制：零数据保留（ZDR）意味着相关数据不被保留，私有安全处理（Private Safety Processing）则用于自动完成安全审查，并据称使 OpenAI 员工无法接触底层内容。此次“私有推理”被描述为该系列的最新产品，但仍处于面向少量客户的测试阶段，尚未公布技术架构、审计方法或性能数据。

**「对企业数据访问的影响」** 对符合资格的 API 客户，采用零数据保留（ZDR）后，请求处理完成时 OpenAI 不保留提示词或模型响应；配合私有安全处理（Private Safety Processing），安全审查可自动完成，OpenAI 员工无法接触底层内容。这可降低敏感企业数据被留存或人工查看的风险，但私有推理目前仍仅面向少量客户测试，并非普遍可用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/offering-zero-data-retention-for-frontier-models/">Offering Zero Data Retention for frontier models | OpenAI</a></li>
<li><a href="https://scalevise.com/resources/openai-private-intelligence-data-controls-rollout/">OpenAI Private Intelligence: Data Controls and Rollout</a></li>

</ul>
</details>

**标签**: `#私有推理`, `#AI 隐私`, `#零数据保留`, `#企业 AI`, `#OpenAI`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美商务部据报施压英特尔交出 10%股权](https://www.wired.com/story/inside-trumps-demands-to-another-chips-ceo/) ⭐️ 8.0/10

据 Telegram 转述的 WIRED 报道，2025 年 8 月美国商务部律师在与英特尔首席财务官通话时，以“无法预测的后果”施压，要求董事会交出 10%股权，英特尔数日后同意。报道还称，美国政府未支付对价，而这批股份目前价值约 110 亿美元；由于缺少 WIRED 原文及完整法律背景，事实范围仍待核实。

telegram · zaihuapd · 11月25日 13:25

**「背景」** 此事发生在英特尔落实美国《芯片法案》补助期间；据诉状相关报道，商务部要求政府持股与放行相关芯片生产补助直接挂钩。

**「潜在影响」** 若法庭文件所述属实，英特尔现有股东的持股比例将因无偿让渡约 10%股权而被稀释，公司也未获得任何股权对价；美国商务部由此成为重要股东，凸显政府通过持股介入芯片产业与公司治理的路线。

<details><summary>参考链接</summary>
<ul>
<li>Lawsuit reveals Trump&#x27;s alleged strong-arming of Intel — troubled chipmaker allegedly forced to give White House 10% stake for release of CHIPS Act funds - Yahoo</li>
<li><a href="https://www.nytimes.com/2025/11/25/us/politics/trump-intel-steel-minerals-china.html">Trump Administration Is Taking Billions in Stakes in Firms Like Intel ...</a></li>

</ul>
</details>

**标签**: `#英特尔`, `#美国商务部`, `#政府持股`, `#芯片产业`, `#公司治理`

---

<a id="item-finance-news-2"></a>
### [美国拟按国别加征新关税](https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html) ⭐️ 8.0/10

美国政府拟依据《贸易法》第 301 条，对中国、欧盟、日本、印度等 14 个贸易伙伴按国别加征新关税；中国拟在 2018 年已加征的 25%关税基础上再加征 20%，若未遵守 2025 年 10 月达成的贸易休战协议，税率可能升至 40%。具体商品范围、生效日期和正式文件尚未提供。

telegram · zaihuapd · 11月25日 13:59

**「背景」** 作为背景，美国是在对所谓制造业“结构性产能过剩”展开调查后提出这轮方案；中国此前的比较基准是 2018 年已加征的 25%关税，若不遵守 2025 年 10 月在釜山达成的贸易休战协议，拟议的额外关税可能从 20%升至 40%。

**「潜在影响」** 若提议按计划实施，拟受影响的美国进口商及下游企业将承担更高的进口成本，并可能调整采购和供应链安排；对华商品的额外关税拟为 20%，若中国不遵守 2025 年 10 月釜山贸易休战协议则可能升至 40%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html">U . S . unveils new Section 301 tariffs targeting China , EU and others</a></li>
<li><a href="https://nypost.com/2026/11/25/business/us-proposes-new-tariffs-on-14-trading-partners-including-china-japan-eu-and-india/">US proposes new tariffs on 14 trading partners — including China ...</a></li>
<li><a href="https://globalimportblog.bakermckenzie.com/2026/11/25/us-ustr-proposes-section-301-tariffs-on-14-economies-over-structural-excess-capacity/">US: USTR Proposes Section 301 Tariffs on 14 Economies Over ...</a></li>
<li><a href="https://invezz.com/news/2026/11/25/trump-new-tariffs-14-economies-2026/">Trump proposes new tariffs on China, EU and 12 other partners</a></li>

</ul>
</details>

**标签**: `#美国关税`, `#中美贸易`, `#第301条`, `#贸易政策`, `#全球供应链`

---