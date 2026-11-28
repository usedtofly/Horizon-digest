---
layout: default
title: "Horizon Summary: 2026-11-28 (ZH)"
date: 2026-11-28
lang: zh
---

> 从 30 条内容中筛选出 13 条重要资讯。

---

**科技新闻**
1. [OpenSec 披露 Linux 内核 nfsd 预认证堆溢出漏洞](#item-tech-news-1) ⭐️ 9.0/10
2. [DeepCrossAttention：Transformer 残差连接提速最高 3 倍](#item-tech-news-2) ⭐️ 7.0/10
3. [热门购物站点发现 WebRTC 盗卡脚本](#item-tech-news-3) ⭐️ 7.0/10
4. [形式化证明中的验证器健全性漏洞](#item-tech-news-4) ⭐️ 7.0/10
5. [多州起诉 SpaceX，指控 Grok 生成儿童性剥削及非自愿图像](#item-tech-news-5) ⭐️ 7.0/10
6. [AWS Trainium3 推理架构与微基准解析](#item-tech-news-6) ⭐️ 7.0/10
7. [八达通网络攻击波及 7500 名客户及 2.2 万商户](#item-tech-news-7) ⭐️ 7.0/10
8. [基岩版资源包漏洞已在 26.65 修复](#item-tech-news-8) ⭐️ 7.0/10
9. [微软推进 Windows 内置驱动替代第三方驱动](#item-tech-news-9) ⭐️ 7.0/10

**财经新闻**
1. [标普 500 进入回调，但不必然预示衰退](#item-finance-news-1) ⭐️ 7.0/10
2. [国常会部署资本市场稳市机制](#item-finance-news-2) ⭐️ 7.0/10
3. [央行下调大额存单认购门槛](#item-finance-news-3) ⭐️ 7.0/10
4. [市场监管总局约谈 15 家电动自行车企业](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OpenSec 披露 Linux 内核 nfsd 预认证堆溢出漏洞](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 9.0/10

OpenSec 报告称，Linux 内核 NFS 服务器 nfsd 的预认证堆溢出漏洞 CVE-2026-99362 可让未认证攻击者仅通过一条发往 tcp/2049 的连接越界写入内核堆并获取 root shell，CVSS 评分达 9.8。该问题据称自 2014 年的 Linux 3.16 起存在，影响启用 NFSv4.1 或 4.2 的文件服务器、NAS 和集群存储节点。OpenSec 称修复版本已发布于 Linux 6.12.117、6.18.61、7.3.2 和 7.4-rc1，处置方式是升级内核并重启；无法立即升级时，可用应用防火墙限制 tcp/2049 访问。CVE 于 2026 年 11 月 20 日公开，但目前信息仅来自 Telegram 转述及 OpenSec 原始研究链接，尚无独立验证。

telegram · zaihuapd · 11月27日 12:57

**「nfsd 漏洞的历史背景」** OpenSec 称，这一预认证堆溢出并非近期回归，而是自 2014 年的 Linux 3.16 起存在于 nfsd；受影响主机须启用 NFSv4.1 或 4.2，才会在处理发往 tcp/2049 的连接时暴露该路径。由于缺陷位于内核态的 NFS 服务代码，临时措施只能先限制 tcp/2049 的可达性，彻底修复仍需安装对应内核更新并重启。

**「受影响环境与处置」** 任何可从网络访问 tcp/2049 且启用 NFSv4.1 或 4.2 的 Linux 主机都面临风险；据 OpenSec，攻击者无需认证即可通过单次连接触发内核堆越界写入并取得 root shell，使用 NAS、文件服务器或集群存储节点的组织应优先排查这些主机。管理员应尽快将内核升级至 6.12.117、6.18.61、7.3.2 或 7.4-rc1 并重启；暂时无法升级时，应通过应用防火墙或网络访问控制限制 tcp/2049 的可达范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS2ROOT ( CVE - 2026 - 99362 ): pre-auth root in Linux nfsd | OpenSec</a></li>
<li><a href="https://security-tracker.debian.org/tracker/CVE-2026-99362">CVE - 2026 - 99362</a></li>
<li><a href="https://www.getpagespeed.com/server-setup/security/nfs2root-cve-2026-99362-centos-7">NFS2ROOT ( CVE - 2026 - 99362 ) on CentOS 7: Fixed Kernel</a></li>

</ul>
</details>

**标签**: `#Linux内核`, `#NFS安全`, `#远程代码执行`, `#CVE-2026-99362`, `#漏洞修复`

---

<a id="item-tech-news-2"></a>
### [DeepCrossAttention：Transformer 残差连接提速最高 3 倍](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 7.0/10

Google Research 提出 DeepCrossAttention，利用注意力机制改造 Transformer 的残差连接，并报告在模型质量可比的前提下最高可实现 3 倍加速。该方法面向 Transformer 模型推理优化，但现有材料没有提供模型、任务、硬件或基准配置，因此这一数字只能视为研究方报告的性能主张，不能外推到所有模型。所给材料也未说明实现是否开放、是否需要修改现有架构，或能否与其他推理优化技术叠加。

hackernews · ComputedCamp995 · 11月27日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50672565)

**「从顺序残差到跨注意力路由」** 传统 Transformer 通过残差连接将子层输出逐层加回隐藏状态，以稳定深层网络训练并改善收敛与模型质量。DeepCrossAttention（DCA）引入带可学习权重的跨注意力路由，使残差路径能够学习跨层或跨分支的信息交互；Google Research 的对照图将其与标准顺序残差结构进行了区分。

**「Transformer 训练效率的潜在收益」** 对训练 Transformer 模型的团队，DeepCrossAttention（DCA）提供了一条可量化的优化路线：论文的语言建模实验显示，在模型质量相当且参数增量可忽略的情况下，训练速度最高可提升至 3 倍；Google Research 的相关介绍称参数增幅低于 0.2%。这属于需要重新训练或改造架构的收益，并非现有模型可直接获得的通用推理加速，团队仍应在自身数据、模型规模和训练预算下复测质量与实际吞吐，不能将“最高 3 倍”视为固定表现。

**「社区讨论」** 评论者 yieldcrv 询问该方法能否与 MTP、Dflash 等推理加速方案叠加，以进一步提高每秒生成的 token 数；这仍是兼容性设想，并非已验证结果。pollorollo 则认为文中的方法对比不应使用折线图而应使用柱状图，评论并未独立复现“最高 3 倍”的结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://arxiv.org/html/2502.06785">DeepCrossAttention : Supercharging Transformer Residual ...</a></li>
<li><a href="https://aiweekly.co/alerts/googles-deepcrossattention-trains-transformers-up-to-3x-faster">Google&#x27;s DeepCrossAttention trains transformers up to 3x faster</a></li>
<li><a href="https://arxiv.org/abs/2502.06785">[2502.06785] DeepCrossAttention: Supercharging Transformer ...</a></li>

</ul>
</details>

**标签**: `#transformer architectures`, `#attention mechanisms`, `#model inference optimization`, `#Google Research`

---

<a id="item-tech-news-3"></a>
### [热门购物站点发现 WebRTC 盗卡脚本](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

2026 年 11 月 27 日发布的报道声称，在热门购物站点上发现利用 WebRTC 的信用卡盗刷脚本，可能使恶意第三方脚本接触支付卡数据。现有材料未列出具体受影响站点、脚本样本、实际泄露的数据或完整演示过程，也未提供缓解措施，因此无法确认影响范围及其是否针对移动设备实施了专门优化。

hackernews · scanr · 11月27日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50668145)

**「第三方脚本与 WebRTC」** 这类披露的关键背景是，购物网站加载的第三方脚本会在访客浏览器中运行，因此安全风险不仅取决于网站服务器是否遭到入侵，也取决于所嵌入代码能访问或处理哪些数据。讨论中有评论者认为，WebRTC 并非实施数据窃取所必需，攻击者也可能改用普通 HTTP 请求；这只是评论者提出的观点，现有材料并未说明脚本利用 WebRTC 的具体机制、受影响网站范围或验证结果。

**「支付数据外泄风险与防护重点」** 若报道所称脚本确实被植入热门购物站点，访问受影响页面的用户可能面临支付表单数据被窃取并外传的风险。外部研究已记录恶意脚本利用 WebRTC DataChannel 接收载荷和外传数据，并借此绕过 CSP 及仅检查 HTTP 流量的安全方案，因此商户不能只依赖 CSP，而应同时审查第三方脚本并监控 WebRTC 通信；不过现有材料未列出受影响站点、暴露的数据范围，也未证明用户数据已经外泄，不能据此断言所有购物网站均受影响。

**「争议集中在第三方脚本风险」** 一名评论者认为，问题并非 WebRTC 具备独有的攻击能力，而是这种行为较少受到监测，且同样的方法也可通过普通 HTTP 请求实现；另一名评论者主张将广告及其他嵌入内容沙箱化，或禁止其执行客户端 JavaScript。这些均为社区观点，现有材料不足以验证其技术判断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/03/webrtc-skimmer-bypasses-csp-to-steal.html">WebRTC Skimmer Bypasses CSP to Steal Payment Data from E ...</a></li>
<li><a href="https://rfxn.com/research/webrtc-skimmer-csp-bypass">WebRTC Skimmers: How Payment Thieves Bypass Content Security ...</a></li>
<li><a href="https://sansec.io/research/webrtc-skimmer">Novel WebRTC skimmer bypasses security controls at $100 ...</a></li>

</ul>
</details>

**标签**: `#web-security`, `#payment-security`, `#WebRTC`, `#third-party-scripts`, `#browser-security`

---

<a id="item-tech-news-4"></a>
### [形式化证明中的验证器健全性漏洞](https://cr.yp.to/proofs/falseccp.html) ⭐️ 7.0/10

文章讨论形式化证明中的验证器健全性漏洞：当检查器错误地接受无效证明时，“通过机器检验”并不等于命题为真，证明的可信度仍取决于验证器实现是否正确。文章主张使用独立、高可信度的验证实现交叉检查，以降低单个检查器缺陷造成假证明被接纳的风险。评论者补充称，Metamath 主证明库要求证明通过五种编程语言实现的五个独立验证器，而曾有案例分别利用 Lean 和当时版本 nanoda 的不同漏洞通过检验，说明实际风险还取决于多个验证器与人工审阅能否同时失效。

hackernews · \_tk\_ · 11月27日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=50667989)

**「背景：验证器的可靠性」** 形式化证明的可信链条依赖证明检查器的健全性：如果检查器存在漏洞，错误的证明项也可能被接受，因此“通过检查”本身并不等同于数学命题已被证明为真。该页面汇总了多个重要证明检查程序出现健全性漏洞的报告，并按报告数量排列，说明减少误接纳需要超越对单一检查器的信任。

**「机器验证的验收风险」** 对于使用 Lean、Metamath 等证明检查器作为验收门槛的团队，“检查通过”不能单独作为命题为真的保证，因为检查器中的健全性漏洞可能让错误证明被接受。关键证明应再由独立实现的高保证检查器复核，并把验证器本身作为需要独立审计的软件依赖。

**「评论者质疑风险是否被夸大」** dwheeler 认为文章对多验证器体系有所误导，并指出 Metamath 主证明库采用五个独立验证器；twotwotwo 也认为，单个验证器出错与成功欺骗数学家之间存在明显距离，因为这通常还需要其他验证器同时出错，并且输入不能立即显得不合常理。gr\_norm 认为此类健全性漏洞长期存在且数量有限，在还需进一步利用被验证程序缺陷的现实条件下风险较低；andai 则提醒，更常见的失败可能是规范理解错误，即证明虽忠实通过了检查，却证明了与真实意图相反的性质。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cr.yp.to/proofs/falseccp.html">False computer-checked proofs (djb)</a></li>
<li><a href="https://cr.yp.to/proofs/falseccp.html">False computer-checked proofs (djb)</a></li>
<li><a href="https://lean-lang.org/">Lean Programming Language</a></li>
<li><a href="https://us.metamath.org/mpeuni/mmset.html">Proof Explorer - Home Page - Metamath</a></li>

</ul>
</details>

**标签**: `#formal verification`, `#proof assistants`, `#theorem provers`, `#software correctness`, `#soundness bugs`

---

<a id="item-tech-news-5"></a>
### [多州起诉 SpaceX，指控 Grok 生成儿童性剥削及非自愿图像](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 7.0/10

美国多个州的总检察长已起诉 SpaceX（xAI 和 Grok 的母公司），寻求阻止 Grok 生成及推广儿童性剥削影像和非自愿私密影像。诉状指控 Grok 平台促成此类内容，但现有材料未提供具体模型版本、审核机制、案件编号或独立验证，因此这些指控不能视为已经证实的行为事实。

hackernews · DeepLogin · 11月27日 19:42 · [社区讨论](https://news.ycombinator.com/item?id=50670855)

**「州级诉讼背景」** 这起诉讼的州级背景是协同但分别立案：俄勒冈州总检察长丹·雷菲尔德已就 Grok 采取法律行动，弗吉尼亚州总检察长杰伊·琼斯与其合作提起的案件则是另起的一项相似诉讼；报道还称，两州是首批起诉 SpaceX 的州。相关指控聚焦 Grok 图像生成器被指允许用户生成并传播非自愿私密影像（NCII）、其他非自愿性化图像和儿童性虐待材料（CSAM），原告还称该生成器此前被错误宣传为总体安全。

**「诉讼可能迫使 Grok 收紧内容控制」** 对运营方而言，州总检察长的诉讼将此前的行政调查推进为法院程序：SpaceX 需要回应州方关于 Grok 生成和传播儿童性剥削及非自愿私密图像的指控；若法院准许停止相关行为的救济，Grok 的模型安全策略、输出控制和内容审核机制可能需要调整，但起诉本身并不代表指控已获证实。对潜在受害者而言，加州总检察长罗布·邦塔已于 2026 年 1 月 14 日启动对 xAI 和 Grok 的调查，并提供 oag.ca.gov/report 投诉入口，受影响者可据此提交个案。

**「社区争论聚焦用户责任与法律边界」** 评论者在治理重点上存在分歧：有人主张追究内容制作者而非只追究平台，也有人质疑此类内容此前是否已在 Grok 上普遍被禁。另有评论者声称，美国最高法院已保护个人为自身消费而制作、且不涉及真实儿童的 AI 儿童性虐待材料，并认为涉及真实人物的报复色情不在这一保护范围内；该法律说法在所给材料中未获核验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.doj.state.or.us/media-home/news-media-releases/ag-rayfield-takes-legal-action-against-grok-for-failing-to-block-child-exploitation/">Oregon Attorney General Rayfield and Virginia Attorney ...</a></li>
<li><a href="https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform">Attorneys General Jones and Rayfield File Suit Against SpaceX ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/23/oregon-virginia-spacex-grok-deepfake-lawsuits.html">SpaceX sued by 2 states over AI deepfake porn, Grok ... - CNBC</a></li>
<li>Attorney General Bonta Launches Investigation into xAI, Grok</li>

</ul>
</details>

**标签**: `#AI safety`, `#Grok`, `#xAI`, `#AI governance`, `#content moderation`

---

<a id="item-tech-news-6"></a>
### [AWS Trainium3 推理架构与微基准解析](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 7.0/10

SemiAnalysis 的深度分析称，AWS Trainium3 采用面向机器学习负载、以 tile 为核心的微架构，并通过描述符生成引擎（DGE）实现类似 Nvidia TMA 和 AMD MI455X TDM 的数据传输职责；其 UBenchX 微基准称，Trainium3 在较小消息尺寸下即可达到峰值 HBM 带宽利用率，而文中称 Nvidia GPU 无法做到。测试还覆盖 SRAM 暂存区的周期级延迟与带宽、机架级带宽和延迟、注意力指数以及不同 head\_dim 对 roofline 命中率的影响；在 AgentX 的真实编码代理会话回放中，作者称 Trainium3 PDS 配合 vLLM 的每美元总拥有成本表现优于除 Vera Rubin 外的其他受测加速器，InferenceX 摘要还称 Trainium3 和 TPU 在每 token 的 TCO 成本上可与 Nvidia GB300 抗衡甚至胜出。这些属于 SemiAnalysis 的基准结果和作者判断，并非 AWS 的出货或商业可用性公告；所给材料未提供具体性能数字、价格、实例可用区域或独立复现结果。

rss · Semianalysis · 11月27日 15:54

**「Trainium3 的硬件与系统基础」** Trainium3 是 AWS 的第四代 AI 芯片，也是其首款采用 3nm 工艺的专用 AI 芯片，并通过 EC2 Trn3 UltraServers 提供；每颗芯片包含 8 个大型核心，每个核心可并行运行 Tensor、Vector、Scalar 和 GPSIMD 四类引擎，AWS 宣称其 MXFP8 计算吞吐量最高可达 Trainium2 的 2 倍。Trn3 系统还采用 Gen1/Gen2 NeuronLink-v4 和 NeuronSwitch-v1 连接，相关 AWS Neuron 架构文档列出了芯片带宽及互联规格，为分析其片上微架构与机架级扩展提供了基础。

**「推理部署影响」** 对在 AWS 上部署编码智能体推理的组织，SemiAnalysis 的 AgentX 端到端会话回放显示，Trainium3 PDS 配合 vLLM 的每美元总拥有成本表现优于文中除 Vera Rubin 外的其他加速器，为评估其相对 Nvidia GB300 的成本效益提供了依据。该结论来自 SemiAnalysis 的 InferenceX/UBenchX 测试，虽有 AWS 架构团队协助校验，采购方仍应使用自身模型、上下文长度和 p90 交互延迟目标复测，不能直接外推到所有工作负载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aws.amazon.com/ec2/instance-types/trn3/">Gen AI Compute Instance - Amazon EC2 Trn3 UltraServers - AWS</a></li>
<li><a href="https://aws.amazon.com/ai/machine-learning/trainium/">AI Accelerator - AWS Trainium - AWS</a></li>
<li><a href="https://awsdocs-neuron.readthedocs-hosted.com/en/latest/about-neuron/arch/neuron-hardware/trn3-arch.html">Amazon EC2 Trn3 Architecture — AWS Neuron Documentation</a></li>
<li><a href="https://newsletter.semianalysis.com/p/trainium3-inferencex">AWS Challenger: Trainium3 Inference and Microarchitecture ...</a></li>
<li><a href="https://inferencex.semianalysis.com/compare-per-dollar/glm-5-3-gb300-vs-trn3">GB300 NVL72 vs Trainium3 PDS: GLM 5.3 744B | InferenceX</a></li>
<li><a href="https://inferencex.semianalysis.com/">AI Accelerator System Benchmark | AcceleratorX by SemiAnalysis</a></li>

</ul>
</details>

**标签**: `#AWS Trainium3`, `#AI accelerators`, `#ML microarchitecture`, `#AI inference`

---

<a id="item-tech-news-7"></a>
### [八达通网络攻击波及 7500 名客户及 2.2 万商户](https://www.hk01.com/article/60415794) ⭐️ 7.0/10

八达通 11 月 27 日表示，早上侦测到系统遭网络攻击，约 7,500 名客户的姓名、相片等个人资料受影响，部分自动增值服务资料可能包括银行编号及增值金额，但信用卡和银行户口资料不在受影响范围；约 2.2 万名商户的公司联络人姓名、职位、电邮地址及电话号码也受影响。八达通称主要服务运作正常，暂未发现客户财务损失，卡内及钱包余额仍受保障，少数功能可能因预防措施暂时受影响。公司将直接通知受影响客户，并已报警及通报私隐专员公署和运输及物流局；报道未交代攻击技术、根因或更广泛的系统性影响。

telegram · zaihuapd · 11月27日 13:11

**「个人资料与支付凭证的区分」** 理解这次事件的关键，是把“个人资料受影响”与“支付凭证或账户遭盗用”区分开来。八达通称受影响资料包括客户姓名、相片、自动增值服务相关的银行编号与增值金额，以及商户联络人的姓名、职位、电邮和电话，但不包括信用卡或银行户口资料；主要服务仍正常运作，暂未发现客户财务损失。

**「客户与商户需核验资料」** 约 7,500 名客户的姓名、相片及部分自动增值服务的银行编号和增值金额受影响，约 2.2 万名商户的公司联络人姓名、职位、电邮及电话号码亦遭暴露，相关人员面临资料滥用、冒充和诈骗风险。八达通表示信用卡和银行账户资料未受影响、主要服务及卡内与钱包余额仍正常，少数功能会因预防措施暂时受限；商户宜核对登记的联络资料，并谨慎处理任何临时要求转账或更改登记资料的信息。

**标签**: `#网络安全`, `#数据泄露`, `#支付系统`, `#八达通`

---

<a id="item-tech-news-8"></a>
### [基岩版资源包漏洞已在 26.65 修复](https://www.zaikei.co.jp/article/20261119/878386.html) ⭐️ 7.0/10

《我的世界》基岩版 26.52 至 26.63 的资源包漏洞已由 Mojang 在 26.65 修复。恶意资源包可利用 content.zipe 改动游戏界面框架 Ore UI 的文件并运行隐藏脚本，影响范围涵盖 PC、手机和主机，Java 版不受影响。附加组件开发者 8Crafter 表示更早版本也可能受影响，但现有材料尚未确认这一范围。

telegram · zaihuapd · 11月27日 18:04

**「自动下载是触发途径」** 该漏洞可借服务器的“资源包自动下载”功能传播；加入服务器或 Realm 的玩家即使没有手动安装资源包，也可能收到攻击者准备的恶意文件。

**「潜在后果与应对」** 恶意资源包可能删除玩家全部存档或获取其 IP；在 Windows 的特定条件下，还可能无提示打开任意 URI，并运行资源包内的批处理文件下载恶意软件。受影响玩家应升级至 26.65；AxmBro 提供的 Windows 只读工具可用于查找 content.zipe，但不能据此判断资源包是否恶意。

**标签**: `#Minecraft`, `#安全漏洞`, `#资源包`, `#恶意软件`, `#漏洞修复`

---

<a id="item-tech-news-9"></a>
### [微软推进 Windows 内置驱动替代第三方驱动](https://www.techspot.com/news/114721-microsoft-wants-replace-most-third-party-device-drivers.html) ⭐️ 7.0/10

微软在 Ignite 2026 大会上确认，正为整类硬件开发 Windows 内置驱动，目标是减少第三方代码进入系统内核。打印机是首批重点；近期推出的 Windows Ready Print 模式旨在取代旧式第三方打印驱动，微软产品经理 Mehmet Kucukgoz 表示 SoundWire、SDCA 音频驱动也将很快成为内置组件，而 I3C 总线、USB 以太网和 MIPI 摄像头驱动仍在开发中。微软同时推出驱动质量倡议（DQI），主张提升驱动可靠性、质量与安全标准，并鼓励第三方开发者和 OEM 优先采用内置驱动；具体落地时间、兼容性以及实际替代范围仍未明确，现阶段主要是计划而非所有相关驱动均已完成替换。

telegram · zaihuapd · 11月28日 02:09

**「背景」** Windows 过去需要 OEM 或第三方为特定硬件类别提供驱动，部分第三方代码可能进入系统内核。微软此次将通用硬件驱动直接纳入系统，并以 Windows Ready Print 作为先行案例，用内置打印功能替代旧式第三方打印驱动。

**「打印驱动部署与兼容性变化」** 对支持 Windows Ready Print 的打印机，自 2026 年 7 月起，新建打印机会默认使用该模式，用户和 IT 团队对传统打印驱动的安装、更新与维护工作将相应减少。现有打印部署应先验证 Ready Print 是否支持所需功能，因为该默认切换仅适用于受支持场景；音频和摄像头等内置驱动仍处于即将推出或开发阶段，不能据此立即停用相关第三方驱动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/windows-itpro-blog/introducing-windows-ready-print-and-modernized-driver-selection/4527563">Introducing Windows Ready Print and Modernized Driver Selection</a></li>
<li><a href="https://techcommunity.microsoft.com/blog/partnernews/introducing-windows-ready-print-and-modernized-driver-selection/4526895">Introducing Windows Ready Print and Modernized Driver ...</a></li>

</ul>
</details>

**标签**: `#Windows`, `#设备驱动`, `#内核安全`, `#硬件生态`, `#微软`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [标普 500 进入回调，但不必然预示衰退](https://www.cnbc.com/2026/11/27/the-sp-500-is-in-a-correction-bear-markets-and-recessions-dont-always-follow.html) ⭐️ 7.0/10

标普 500 指数于 11 月 20 日进入回调，单日下跌 3.7%至 6910.39 点，较 10 月 6 日收盘高点 7818.93 点低 11.6%。德意志银行策略师亨利·艾伦认为，目前尚未出现经济数据恶化或美联储政策明显转鹰，因此回调不必然预示衰退，但这属于其历史比较判断，并非已确认的宏观结论。

rss · CNBC Finance · 11月27日 13:21

**「背景」** 标普 500 的“熊市”指从近期高点下跌至少 20%；CNBC 梳理的 13 次历史熊市中，8 次与美国经济衰退期重叠、5 次没有，包括 1987 年和 2022 年。

**标签**: `#S&amp;P 500 correction`, `#recession risk`, `#Federal Reserve policy`, `#economic indicators`

---

<a id="item-finance-news-2"></a>
### [国常会部署资本市场稳市机制](https://www.tmtpost.com/nictation/8220182.html) ⭐️ 7.0/10

国务院常务会议要求加力发挥“国家队”稳市作用、优化中央汇金类“平准基金”功能，并推动上市公司分红回购及中长期资金入市；目前仍属方向性部署，尚未公布具体增量措施、实施时间和资金规模。

telegram · zaihuapd · 11月27日 05:35

**「背景」** 中央汇金是代表国家稳定资本市场的“国家队”，此次会议提出在既有稳市机制基础上，进一步强化其类“平准基金”功能和流动性保障。

**「对资本市场的影响」** 若后续配套政策落地，保险、企业年金和社保资金等中长期资金的入市支持可能扩大市场资金供给，而中央汇金类“平准基金”功能优化意在强化流动性保障；但目前尚无具体资金规模和时间表，实际效果仍不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cls.cn/detail/2546318">cls.cn/detail/2546318</a></li>
<li><a href="https://finance.sina.com.cn/roll/2026-11-27/doc-inkaczqf1072509.shtml">国常会：加力发挥“国家队”稳市作用，进一步优化中央汇金公司的类“平准...</a></li>
<li><a href="https://news.qq.com/rain/a/20261106A06JSI00">国务院：支持中央汇金公司发挥类平准基金作用，巩固完善资本市场稳市...</a></li>

</ul>
</details>

**标签**: `#中国资本市场`, `#中央汇金`, `#国家队稳市`, `#长期资金入市`, `#分红回购`

---

<a id="item-finance-news-3"></a>
### [央行下调大额存单认购门槛](https://www.news.cn/fortune/20261127/70789d77822242cc82216f51a416f872/c.html) ⭐️ 7.0/10

中国人民银行 11 月 27 日公布《大额存单管理办法》，将个人和机构认购起点分别降至 10 万元和 500 万元，较原门槛均下调一半，并自 2027 年 3 月 21 日起施行。新规同时要求金融机构自主确定存贷款利率，禁止通过高息揽储等不正当手段吸收存款。

telegram · zaihuapd · 11月27日 11:36

**「背景」** 此前规则下，个人和机构认购大额存单的起点分别为 20 万元和 1000 万元；新办法将两项门槛各下调一半，并废止 2015 年暂行办法及 2016 年第 13 号公告，自 2027 年 3 月 21 日起施行。

**「影响」** 门槛下调后，原本未达到旧标准的个人储户与机构可参与大额存单；银行则须自主确定存贷款利率，不得再以高息违规揽储。

**标签**: `#央行政策`, `#大额存单`, `#存款利率`, `#银行监管`

---

<a id="item-finance-news-4"></a>
### [市场监管总局约谈 15 家电动自行车企业](https://www.news.cn/20261127/0c8c665ce70c417b9263b39fa8a519f0/c.html?hl=zh-CN) ⭐️ 7.0/10

市场监管总局 11 月 27 日集中约谈雅迪、台铃、爱玛、九号、小牛等 15 家电动自行车企业，要求整改 CCC（强制性产品认证）飞行检查发现的质量管理、产品一致性及国家标准违规问题，并对确认存在缺陷的产品立即召回。

telegram · zaihuapd · 11月27日 12:06

**「背景」** 此次约谈源于近期监管部门在电动自行车 CCC 认证全覆盖飞行检查中发现的质量问题；CCC 认证是国家对产品安全与质量符合性实施的强制性认证。

**「退车与售后影响」** 15 家受访企业须整改并召回确认有缺陷的产品，且不得以折价退车或等待证书恢复为由拒绝退车，相关消费者的退车和售后保障将更明确，但召回规模及企业财务影响尚未公布。

**标签**: `#电动自行车`, `#市场监管`, `#CCC认证`, `#产品召回`, `#消费者保护`

---