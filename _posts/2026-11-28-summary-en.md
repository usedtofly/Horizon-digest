---
layout: default
title: "Horizon Summary: 2026-11-28 (EN)"
date: 2026-11-28
lang: en
---

> From 30 items, 13 important content pieces were selected

---

**Technology News**
1. [OpenSec Reports Pre-Auth Linux nfsd Flaw and Fixes](#item-tech-news-1) ⭐️ 9.0/10
2. [Google&\#x27;s DeepCrossAttention Reports Up to 3x Faster Transformers](#item-tech-news-2) ⭐️ 7.0/10
3. [WebRTC Skimming Scripts Reportedly Found on Shopping Sites](#item-tech-news-3) ⭐️ 7.0/10
4. [Verifier bugs can admit false machine-checked proofs](#item-tech-news-4) ⭐️ 7.0/10
5. [State attorneys general sue SpaceX over Grok image-generation allegations](#item-tech-news-5) ⭐️ 7.0/10
6. [AWS Trainium3 Tile Architecture and Benchmark Claims](#item-tech-news-6) ⭐️ 7.0/10
7. [Octopus says cyberattack affected customer and merchant records](#item-tech-news-7) ⭐️ 7.0/10
8. [Minecraft Bedrock Resource-Pack Flaw Fixed in 26.65](#item-tech-news-8) ⭐️ 7.0/10
9. [Microsoft Expands Built-In Windows Drivers Across More Hardware Categories](#item-tech-news-9) ⭐️ 7.0/10

**Financial News**
1. [S&amp;P 500 enters correction without clear recession signal](#item-finance-news-1) ⭐️ 7.0/10
2. [China calls for stronger state-backed market support](#item-finance-news-2) ⭐️ 7.0/10
3. [China’s central bank halves large-denomination CD minimums](#item-finance-news-3) ⭐️ 7.0/10
4. [China summons 15 e-bike makers over compliance failures](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenSec Reports Pre-Auth Linux nfsd Flaw and Fixes](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 9.0/10

OpenSec reported CVE-2026-99362, a pre-authentication heap overflow in the Linux kernel’s nfsd server, with a CVSS score of 9.8. According to the disclosure, a single connection to TCP port 2049 can trigger an out-of-bounds kernel heap write and obtain a root shell on systems running Linux 3.16 or later with NFSv4.1 or NFSv4.2 enabled, including NAS, file-server and cluster-storage hosts. Fixes were listed for Linux 6.12.117, 6.18.61, 7.3.2 and 7.4-rc1; operators are advised to upgrade and reboot, while restricting access to TCP/2049 is presented only as a temporary mitigation when an immediate update is not possible. The CVE was publicly disclosed on November 20, 2026, but the supplied material contains only a Telegram account linked to the OpenSec research and no independent verification.

telegram · zaihuapd · Nov 27, 12:57

**「NFS server attack surface and history」** The vulnerable component is nfsd, the Linux kernel’s NFS server implementation, which processes NFSv4.1 and NFSv4.2 requests over TCP port 2049. OpenSec reports that the flaw has existed since Linux 3.16 in 2014, making it relevant to long-running NFS deployments that expose those protocol versions but have not adopted a kernel containing the published fix.

**「Operational impact and mitigation」** OpenSec reports that any Linux host serving NFSv4.1 or NFSv4.2 on reachable tcp/2049 is exposed to a pre-authentication kernel heap overflow that can grant a root shell, affecting file servers, NAS appliances, and cluster storage nodes. Operators should upgrade to Linux 6.12.117, 6.18.61, 7.3.2, or 7.4-rc1 and reboot; if an immediate upgrade is impossible, they should restrict tcp/2049 access with a host or application firewall.

<details><summary>References</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS2ROOT ( CVE - 2026 - 99362 ): pre-auth root in Linux nfsd | OpenSec</a></li>
<li><a href="https://security-tracker.debian.org/tracker/CVE-2026-99362">CVE - 2026 - 99362</a></li>

</ul>
</details>

**Tags**: `#Linux内核`, `#NFS安全`, `#远程代码执行`, `#CVE-2026-99362`, `#漏洞修复`

---

<a id="item-tech-news-2"></a>
### [Google&\#x27;s DeepCrossAttention Reports Up to 3x Faster Transformers](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 7.0/10

Google Research introduced DeepCrossAttention, an attention-based approach to transformer residual connections, and reported up to 3x faster execution while maintaining comparable model quality. The supplied material does not specify the models, hardware, workloads, or benchmark methodology behind that figure, and the comments provide no independent validation, so the speedup remains a Google claim rather than an established general result.

hackernews · ComputedCamp995 · Nov 27, 23:06 · [Discussion](https://news.ycombinator.com/item?id=50672565)

**「Background」** Conventional residual networks propagate information sequentially through each layer, while DeepCrossAttention uses learnable, attention-based routing to combine residual features rather than relying only on that fixed sequence. Residual connections are used in deep neural networks because they stabilize training and can improve convergence and model quality.

**「Potential training-time savings」** For teams training transformer language models, DeepCrossAttention could reduce the time needed to reach a fixed quality target by up to 3x in the paper’s reported experiments, while adding a negligible number of parameters. The result concerns training time rather than inference latency, so teams should benchmark their own workloads before treating it as an equivalent inference-speed improvement.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://arxiv.org/html/2502.06785">DeepCrossAttention : Supercharging Transformer Residual ...</a></li>
<li><a href="https://arxiv.org/abs/2502.06785">[2502.06785] DeepCrossAttention: Supercharging Transformer ...</a></li>

</ul>
</details>

**Tags**: `#transformer architectures`, `#attention mechanisms`, `#model inference optimization`, `#Google Research`

---

<a id="item-tech-news-3"></a>
### [WebRTC Skimming Scripts Reportedly Found on Shopping Sites](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

A report alleges that credit-card skimming scripts using WebRTC were found on popular shopping sites, potentially exposing payment data entered on affected pages. However, the supplied item names no affected sites and provides no technical demonstration, test results, or mitigations, leaving the allegation’s scope and validity unverified. The disclosure indicates a possible third-party-script and monitoring gap rather than establishing a WebRTC-specific browser vulnerability.

hackernews · scanr · Nov 27, 15:40 · [Discussion](https://news.ycombinator.com/item?id=50668145)

**「Background」** Third-party JavaScript included by a shopping site generally executes with the embedding page’s privileges, making every included script part of the site’s payment-data security boundary. WebRTC in the allegation is a possible exfiltration channel rather than necessarily a vulnerability in WebRTC itself; one commenter noted that ordinary HTTP requests could provide a similar channel.

**「CSP alone is not enough」** Shopping-site operators cannot rely on Content Security Policy \(CSP\) alone: earlier research documented a WebRTC DataChannel skimmer that received payloads and exfiltrated payment data while bypassing CSP and HTTP-based security tools \(tool-3-1, tool-3-3\). The practical response is to audit third-party checkout scripts and monitor for WebRTC DataChannel abuse using published detection signatures and mitigation guidance \(tool-3-2\), although the supplied item does not identify the affected sites or quantify how many shoppers were exposed.

**「Community Debate」** Hacker News commenters argued that WebRTC may be less frequently monitored and that ordinary HTTP requests could serve the same purpose, making third-party JavaScript the more fundamental risk; these are opinions, not findings verified by the report. Some favored ad blocking or browser sandboxing that prevents third-party scripts from executing, while others emphasized that sites must decide which external code they embed.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/03/webrtc-skimmer-bypasses-csp-to-steal.html">WebRTC Skimmer Bypasses CSP to Steal Payment Data from E ...</a></li>
<li><a href="https://rfxn.com/research/webrtc-skimmer-csp-bypass">WebRTC Skimmers: How Payment Thieves Bypass Content Security ...</a></li>
<li><a href="https://sansec.io/research/webrtc-skimmer">Novel WebRTC skimmer bypasses security controls at $100 ...</a></li>

</ul>
</details>

**Tags**: `#web-security`, `#payment-security`, `#WebRTC`, `#third-party-scripts`, `#browser-security`

---

<a id="item-tech-news-4"></a>
### [Verifier bugs can admit false machine-checked proofs](https://cr.yp.to/proofs/falseccp.html) ⭐️ 7.0/10

The article examines how soundness bugs in proof-checking software can let invalid derivations pass, meaning that a checker&\#x27;s acceptance does not by itself establish that the mathematics or program is correct. It calls for independent, high-assurance verification rather than treating a single checker as authoritative; this is an analysis of verifier risk, not an announcement of a new false theorem entering an accepted proof database.

hackernews · \_tk\_ · Nov 27, 15:26 · [Discussion](https://news.ycombinator.com/item?id=50667989)

**「Proof-checker soundness」** A proof checker is sound only if it rejects every invalid derivation; an implementation bug can therefore let a false theorem pass machine checking without making the underlying mathematics true. The referenced survey catalogs reported soundness bugs in several proof-checking programs and orders them by the number of reports, framing verifier reliability as a matter of software correctness and trust.

**「Require independent verification」** Teams using proof assistants such as Lean or Metamath should not treat acceptance by one checker as definitive evidence of truth, because reported soundness bugs have allowed false statements to pass machine checking. Before relying on such results for code certification or publication, teams should require re-verification with independently implemented tools and human review of the claim’s plausibility.

**「One bug may not be enough」** Commenters disputed how easy such exploitation is: one said Metamath&\#x27;s main proof databases require five independently written verifiers in five languages, while another argued that soundness bugs are rare and must also be shaped to the program being verified. One commenter cited a DeepMind researcher&\#x27;s bogus proof that passed both Lean and a then-week-old nanoda by triggering a different bug in each; another warned that a formally verified implementation can still satisfy the wrong specification.

<details><summary>References</summary>
<ul>
<li><a href="https://cr.yp.to/proofs/falseccp.html">False computer-checked proofs (djb)</a></li>
<li><a href="https://cr.yp.to/proofs/falseccp.html">False computer-checked proofs (djb)</a></li>
<li><a href="https://lean-lang.org/">Lean Programming Language</a></li>
<li><a href="https://us.metamath.org/mpeuni/mmset.html">Proof Explorer - Home Page - Metamath</a></li>

</ul>
</details>

**Tags**: `#formal verification`, `#proof assistants`, `#theorem provers`, `#software correctness`, `#soundness bugs`

---

<a id="item-tech-news-5"></a>
### [State attorneys general sue SpaceX over Grok image-generation allegations](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 7.0/10

State attorneys general have sued SpaceX, the parent company of xAI and Grok, alleging that the platform facilitates the generation and promotion of child sexual exploitation imagery and non-consensual images. The available report does not provide the complaint, jurisdictions, requested remedies, or supporting evidence, and the allegations have not been adjudicated.

hackernews · DeepLogin · Nov 27, 19:42 · [Discussion](https://news.ycombinator.com/item?id=50670855)

**「Early state lawsuits」** Virginia and Oregon are the first states to sue SpaceX over alleged safety failures in Grok&\#x27;s image generator; Oregon filed a separate but similar action, while Virginia&\#x27;s suit was brought with Oregon&\#x27;s collaboration. The lawsuits also allege that xAI falsely marketed the generator as generally safe, but those allegations have not yet been adjudicated.

**「Legal and reporting impact」** The concrete escalation is from regulatory scrutiny to litigation: California’s attorney general opened an xAI/Grok investigation on January 14, 2026 and directed potential victims to report harm at oag.ca.gov/report; the later state lawsuit could subject SpaceX/xAI to court-ordered remedies if the claims are sustained. Affected users have a concrete reporting channel, but the available material identifies no injunction, required model change, or compliance deadline, so no particular technical safeguard can yet be treated as court-mandated.

**「Community discussion」** Commenters questioned whether such outputs were already broadly prohibited and whether enforcement should focus on the people generating them; one commenter also claimed that a U.S. Supreme Court ruling protects AI-generated child sexual abuse material made for personal consumption. That legal assertion was not independently verified here and should not be treated as established.

<details><summary>References</summary>
<ul>
<li><a href="https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform">Attorneys General Jones and Rayfield File Suit Against SpaceX ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/23/oregon-virginia-spacex-grok-deepfake-lawsuits.html">SpaceX sued by 2 states over AI deepfake porn, Grok ... - CNBC</a></li>
<li>Attorney General Bonta Launches Investigation into xAI, Grok</li>

</ul>
</details>

**Tags**: `#AI safety`, `#Grok`, `#xAI`, `#AI governance`, `#content moderation`

---

<a id="item-tech-news-6"></a>
### [AWS Trainium3 Tile Architecture and Benchmark Claims](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 7.0/10

A SemiAnalysis deep dive describes AWS Trainium3 as a tile-centric accelerator built specifically for machine learning, with Descriptor Generation Engines handling data movement. Its UBenchX tests reportedly found that Trainium can reach peak HBM bandwidth utilization at small message sizes, which the authors say Nvidia GPUs cannot match; broader InferenceX and AgentX testing also reports competitive or better cost-per-token and total-cost-of-ownership results against Nvidia GB300 and other accelerators. These are SemiAnalysis-authored findings rather than an AWS product announcement: AWS architects helped explain and validate the experiments, but the supplied excerpt contains no complete cost tables, pricing, availability details, or deployment requirements.

rss · Semianalysis · Nov 27, 15:54

**「Trainium lineage and platform context」** Trainium3 is the fourth generation of AWS’s Trainium accelerators and appears in EC2 Trn3 UltraServers; AWS describes it as its first 3nm AI chip, aimed at agentic, reasoning, and video-generation workloads. The platform uses AWS Neuron, with Gen1 and Gen2 NeuronLink-v4 and NeuronSwitch-v1 connectivity. Each Trainium3 chip has eight large cores and Tensor, Vector, Scalar, and GPSIMD engines, with AWS claiming up to 2× the MXFP8 compute throughput of Trainium2.

**「Impact for inference buyers」** For organizations selecting accelerators for production inference, SemiAnalysis reports that Trainium3 PDS with vLLM outperformed every tested accelerator except Vera Rubin on performance per dollar across its p90-interactivity/TCO frontier, while Trainium’s Descriptor Generation Engines reached peak HBM bandwidth utilization at small message sizes. This makes Trainium3 a concrete non-NVIDIA option to evaluate for agentic and latency-sensitive workloads, but because AWS Annapurna and Trainium personnel helped validate the experiments, buyers should reproduce the open-source InferenceX and UBenchX results with their own models, frameworks, and total-cost assumptions.

<details><summary>References</summary>
<ul>
<li><a href="https://aws.amazon.com/ec2/instance-types/trn3/">Gen AI Compute Instance - Amazon EC2 Trn3 UltraServers - AWS</a></li>
<li><a href="https://aws.amazon.com/ai/machine-learning/trainium/">AI Accelerator - AWS Trainium - AWS</a></li>
<li><a href="https://awsdocs-neuron.readthedocs-hosted.com/en/latest/about-neuron/arch/neuron-hardware/trn3-arch.html">Amazon EC2 Trn3 Architecture — AWS Neuron Documentation</a></li>
<li><a href="https://newsletter.semianalysis.com/p/trainium3-inferencex">AWS Challenger: Trainium3 Inference and Microarchitecture ...</a></li>
<li><a href="https://inferencex.semianalysis.com/compare-per-dollar/glm-5-3-gb300-vs-trn3">GB300 NVL72 vs Trainium3 PDS: GLM 5.3 744B | InferenceX</a></li>
<li><a href="https://inferencex.semianalysis.com/">AI Accelerator System Benchmark | AcceleratorX by SemiAnalysis</a></li>

</ul>
</details>

**Tags**: `#AWS Trainium3`, `#AI accelerators`, `#ML microarchitecture`, `#AI inference`

---

<a id="item-tech-news-7"></a>
### [Octopus says cyberattack affected customer and merchant records](https://www.hk01.com/article/60415794) ⭐️ 7.0/10

Octopus disclosed that it detected a cyberattack on the morning of November 27, affecting the personal data of about 7,500 customers and 22,000 merchants. Customer records included names and photographs; some Auto-Load-related records may have included bank account numbers and top-up amounts, but no credit-card or bank-account information was affected. The affected merchant records covered company contacts’ names, titles, email addresses, and phone numbers. Octopus said core services were operating normally, it had found no customer financial loss, and wallet or stored-value balances remained protected, although some features were temporarily unavailable as a precaution; the company reported the incident to police and notified Hong Kong’s Privacy Commissioner and Transport and Logistics Bureau.

telegram · zaihuapd · Nov 27, 13:11

**「Context」** Octopus holds customer identity records, merchant contact details and, for some customers, bank numbers associated with Autopius top-up services. The disclosure distinguishes these records from credit-card and bank-account data, which the company said were not affected.

**「Action for affected users」** Octopus says it will directly notify the roughly 7,500 affected customers, who should scrutinize unsolicited payment or account-related requests because names, photographs, contact details and, for some users, automatic-top-up bank numbers were exposed. Merchant contacts affected by the breach should similarly watch for impersonation attempts; Octopus reports that credit-card and bank-account data were not included, no financial loss was found, and main services remained operational, although some functions may be temporarily unavailable due to preventive measures.

**Tags**: `#网络安全`, `#数据泄露`, `#支付系统`, `#八达通`

---

<a id="item-tech-news-8"></a>
### [Minecraft Bedrock Resource-Pack Flaw Fixed in 26.65](https://www.zaikei.co.jp/article/20261119/878386.html) ⭐️ 7.0/10

Minecraft Bedrock Edition versions 26.52 through 26.63 are affected by a resource-pack vulnerability, and Mojang has fixed it in version 26.65 across PC, mobile, and console; Java Edition is not affected. Add-on developer 8Crafter reported that a resource pack containing content.zipe can modify Ore UI interface files and run hidden scripts, including through packs automatically downloaded after joining a server or Realm. The report also says earlier Bedrock versions may be vulnerable and cites potential consequences including deletion of all saves, disclosure of player IP addresses, and, under specific Windows conditions, silently opening a URI and running a bundled batch file to download malware.

telegram · zaihuapd · Nov 27, 18:04

**「How the Exploit Works」** 8Crafter publicly disclosed the issue on November 15 before Mojang released the 26.65 fix. The attack path uses Bedrock’s resource-pack system: a pack containing content.zipe can alter Ore UI, the game’s interface framework, to execute hidden scripts, and affected players may receive such a pack without manually installing it if automatic downloads are enabled for servers or Realms.

**「What Players Should Do」** Players using an affected Bedrock version should update to 26.65 or newer before joining untrusted servers or Realms with automatic resource-pack downloads enabled. On Windows, AxmBro’s read-only detector can locate content.zipe, but it cannot determine whether the detected resource pack is malicious.

**Tags**: `#Minecraft`, `#安全漏洞`, `#资源包`, `#恶意软件`, `#漏洞修复`

---

<a id="item-tech-news-9"></a>
### [Microsoft Expands Built-In Windows Drivers Across More Hardware Categories](https://www.techspot.com/news/114721-microsoft-wants-replace-most-third-party-device-drivers.html) ⭐️ 7.0/10

At Ignite 2026, Microsoft said it is developing built-in Windows drivers for entire hardware categories to reduce reliance on third-party code in the Windows kernel, benefiting driver developers and OEMs through lower maintenance requirements. Printers are the initial focus, with the recently introduced Windows Ready Print mode intended to replace legacy third-party printer drivers. Windows product manager Mehmet Kucukgoz said built-in SoundWire and SDCA audio drivers will arrive soon, while I3C bus, USB Ethernet, and MIPI camera drivers are in development. Microsoft also introduced the Driver Quality Initiative to raise driver reliability, quality, and security, but the rollout schedule, compatibility, and effects on existing third-party drivers remain unspecified.

telegram · zaihuapd · Nov 28, 02:09

**「Background」** Microsoft’s strategy depends on Windows first offering a usable driver for an entire device class, allowing OEMs and driver developers to rely on the operating system instead of separate vendor implementations. Windows Ready Print is the printer-side example, while SoundWire, SDCA, I3C, USB Ethernet, and MIPI camera drivers are still in development, making the transition incremental rather than an immediate replacement of all third-party drivers.

**「Deployment impact」** Starting in July 2026, new Windows printer installations will default to Windows Ready Print where supported; Microsoft says this simplifies setup and reduces the need for traditional driver management. Because support is conditional and Microsoft has also published an end-of-servicing plan for third-party printer drivers, IT teams should verify printer compatibility and vendor-specific feature requirements before replacing existing driver workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/windows-hardware/drivers/print/end-of-servicing-plan-for-third-party-printer-drivers-on-windows">End of servicing plan for third-party printer drivers on Windows</a></li>
<li><a href="https://techcommunity.microsoft.com/blog/windows-itpro-blog/introducing-windows-ready-print-and-modernized-driver-selection/4527563">Introducing Windows Ready Print and Modernized Driver Selection</a></li>

</ul>
</details>

**Tags**: `#Windows`, `#设备驱动`, `#内核安全`, `#硬件生态`, `#微软`

---

## Financial News

<a id="item-finance-news-1"></a>
### [S&amp;P 500 enters correction without clear recession signal](https://www.cnbc.com/2026/11/27/the-sp-500-is-in-a-correction-bear-markets-and-recessions-dont-always-follow.html) ⭐️ 7.0/10

The S&amp;P 500 entered a correction on Nov. 20, closing at 6,910.39, 11.6% below its Oct. 6 record close of 7,818.93. CNBC found that 8 of 13 S&amp;P 500 bear markets overlapped with recessions, but Deutsche Bank strategist Henry Allen said no recession, worsening economic data or hawkish Federal Reserve shift is evident so far; the November flash composite PMI was 54.6, and interest-rate pricing has shifted slightly dovish.

rss · CNBC Finance · Nov 27, 13:21

**「Background」** A stock-market correction is a decline of at least 10% from a recent high, while a bear market requires a 20% decline; CNBC’s analysis found that five of 13 S&amp;P 500 bear markets occurred without a recession, including in 1987 and 2022. A recession is a broad, sustained contraction in economic activity, so neither market decline automatically means one has begun.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Recession">Recession - Wikipedia</a></li>
<li><a href="https://www.britannica.com/money/bull-market-vs-bear-market">Bull vs. Bear Market Definitions | Britannica Money</a></li>

</ul>
</details>

**Tags**: `#S&amp;P 500 correction`, `#recession risk`, `#Federal Reserve policy`, `#economic indicators`

---

<a id="item-finance-news-2"></a>
### [China calls for stronger state-backed market support](https://www.tmtpost.com/nictation/8220182.html) ⭐️ 7.0/10

At the Nov. 27, 2026 State Council executive meeting chaired by Premier Li Qiang, officials called for a stronger state-backed “national team” role, optimized stabilization-fund functions at Central Huijin, and policies bringing insurance, enterprise annuity and social-security funds into the stock market. They also urged listed companies to increase dividends and buybacks and called for stronger enforcement against fraud and illegal share sales, but announced no funding size, timetable or detailed new measures.

telegram · zaihuapd · Nov 27, 05:35

**「Background」** China already uses countercyclical policy—public measures intended to cushion markets when economic conditions weaken—so the meeting’s call to implement existing measures and plan additional ones extends that framework rather than announcing a fully specified policy package.

**「Market impact」** If implemented as directed, expanded liquidity support from Central Huijin and policies encouraging insurers, pension and social-security funds to enter the market could support liquidity and stability for investors, though no funding scale or timetable was specified.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cls.cn/detail/2546318">cls.cn/detail/2546318</a></li>
<li><a href="https://finance.sina.com.cn/roll/2026-11-27/doc-inkaczqf1072509.shtml">国常会：加力发挥“国家队”稳市作用，进一步优化中央汇金公司的类“平准...</a></li>
<li><a href="https://news.qq.com/rain/a/20261106A06JSI00">国务院：支持中央汇金公司发挥类平准基金作用，巩固完善资本市场稳市...</a></li>

</ul>
</details>

**Tags**: `#中国资本市场`, `#中央汇金`, `#国家队稳市`, `#长期资金入市`, `#分红回购`

---

<a id="item-finance-news-3"></a>
### [China’s central bank halves large-denomination CD minimums](https://www.news.cn/fortune/20261127/70789d77822242cc82216f51a416f872/c.html) ⭐️ 7.0/10

The People’s Bank of China lowered the minimum for large-denomination certificates of deposit to RMB 100,000 for individuals and RMB 5 million for institutions, from RMB 200,000 and RMB 10 million respectively. Effective March 21, 2027, the rules also require banks to set deposit and loan rates independently and prohibit using above-market rates to attract deposits.

telegram · zaihuapd · Nov 27, 11:36

**「Background」** The PBOC’s 2015 interim rules and 2016 No. 13 announcement previously set minimum purchases of RMB 200,000 for individuals and RMB 10 million for institutions; the replacements take effect on March 21, 2027.

**「Impact」** From March 21, 2027, individual investors holding at least RMB 100,000 and institutions holding at least RMB 5 million will be eligible to buy large-denomination certificates of deposit, expanding banks’ fundraising options while separate rules prohibit high-interest deposit solicitation.

**Tags**: `#央行政策`, `#大额存单`, `#存款利率`, `#银行监管`

---

<a id="item-finance-news-4"></a>
### [China summons 15 e-bike makers over compliance failures](https://www.news.cn/20261127/0c8c665ce70c417b9263b39fa8a519f0/c.html?hl=zh-CN) ⭐️ 7.0/10

China’s market regulator summoned 15 electric-bicycle companies, including Yadea, Tailing, Aima, Ninebot and Niu, after compulsory-certification spot checks found quality-control weaknesses and sales of products that failed mandatory national standards. The companies were ordered to rectify the problems and recall products confirmed to be defective, but no company-specific penalties or recall volumes were disclosed.

telegram · zaihuapd · Nov 27, 12:06

**「Background」** The meeting followed China compulsory product certification \(CCC\) inspections that found weaknesses in quality assurance and product consistency, along with products sold in violation of mandatory national standards.

**「Impact」** The 15 manufacturers must tighten quality controls and recall confirmed defective products, while affected buyers are protected from forced discounted trade-ins and refund refusals based on promises that certification will soon be restored.

**Tags**: `#电动自行车`, `#市场监管`, `#CCC认证`, `#产品召回`, `#消费者保护`

---