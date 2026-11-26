---
layout: default
title: "Horizon Summary: 2026-11-26 (EN)"
date: 2026-11-26
lang: en
---

> From 36 items, 12 important content pieces were selected

---

**Technology News**
1. [A Much Shorter Lean Formalization of Anthropic’s GRH Work](#item-tech-news-1) ⭐️ 8.0/10
2. [1Password Says Vaults Stayed Intact in Account-Data Incident](#item-tech-news-2) ⭐️ 8.0/10
3. [Minecraft Java Font Flaw Enables RCE; Community Fix Available](#item-tech-news-3) ⭐️ 8.0/10
4. [FCC Clears SpaceX’s 1M-Satellite Starmind Constellation](#item-tech-news-4) ⭐️ 8.0/10
5. [Aaronson links 9/4 matrix multiplication to AI-assisted discovery](#item-tech-news-5) ⭐️ 7.0/10
6. [Google publishes Cogentic papers on integer factorization and discrete logarithms](#item-tech-news-6) ⭐️ 7.0/10
7. [OpenAI expands cybersecurity push with GPT-6 Cyber and Daybreak](#item-tech-news-7) ⭐️ 7.0/10
8. [Tencent Releases Quantized Hy4 Flash for 64 GB Mac mini](#item-tech-news-8) ⭐️ 7.0/10
9. [Asian Data Centers Seek U.S. Buyers for AI Compute](#item-tech-news-9) ⭐️ 7.0/10
10. [OpenAI Tests Private Inference for Select Customers](#item-tech-news-10) ⭐️ 7.0/10

**Financial News**
1. [U.S. government reportedly acquired 10% of Intel without payment](#item-finance-news-1) ⭐️ 8.0/10
2. [U.S. Proposes New Tariffs on 14 Trading Partners](#item-finance-news-2) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [A Much Shorter Lean Formalization of Anthropic’s GRH Work](https://github.com/lsernau/grh-lean) ⭐️ 8.0/10

A GitHub project, \`lsernau/grh-lean\`, claims to reduce the Lean formalization of Anthropic’s generalized Riemann hypothesis work from roughly 17 million lines to about 76,000 lines—a 99.56% reduction intended to make the proof easier to inspect. The project reportedly separates “known math” from “new math” and adds human-readable documentation, but the supplied material does not independently confirm that the shorter artifact is mathematically equivalent to the original or otherwise validated. One commenter describes the readable proof as roughly 300,000 lines, so the exact size is not consistent across the available accounts.

hackernews · nb-t · Nov 25, 21:48 · [Discussion](https://news.ycombinator.com/item?id=50648050)

**「Earlier Proof Scale」** The backdrop is Anthropic mathematician Levent Alpöge’s original Lean 4 formalization of the generalized Riemann hypothesis, reported as roughly 17 million lines and released on November 20. The lsernau/grh-lean repository presents two shorter editions of the same five theorems—a readable edition of about 300,000 lines and a compact edition of about 76,000 lines—while MIT’s companion page documents the shorter project and keeps the original proof’s checks separate. These descriptions establish the repository sizes and editions, but do not independently verify the mathematical correctness of the claimed shorter proof.

**「A smaller artifact is easier to audit」** The reported reduction from roughly 17 million lines to 76,000 gives reviewers a far smaller Lean 4/Mathlib proof to inspect; a separate GRH Lean Check also reports that the RH and GRH statements occupy 16 lines and that the dependencies are genuine upstream releases, making verification more practical. Shorter code is not a substitute for mathematical explanation, however: a commenter still called for a conventional paper presenting the core argument, so teams should treat the rewrite as an auditability improvement rather than evidence that the proof has already been understood in prose.

**「Community Discussion」** Commenters welcomed the claimed readability and the separation of “known math” from “new math,” but questioned whether producing compact Lean code demonstrates genuine understanding of the proof. One participant called for a conventional mathematical paper and an explanation of the core argument from a mathematician, while another asked whether the project had already overcome Terence Tao’s concern that enormous proofs can contain little conceptual insight.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/lsernau/grh-lean">GitHub - lsernau/grh-lean: A short Lean 4 proof of the ...</a></li>
<li><a href="https://math.mit.edu/~drew/shortgrh/">Shorter GRH Lean proof: verification files - MIT Mathematics</a></li>
<li><a href="https://stackfutures.com/blog/anthropic-riemann-lean-proof-17m-to-76k-lines-shorter-grh-nov-2026/">The Riemann Hypothesis Lean Proof Just Shrank From 17 Million ...</a></li>
<li><a href="https://github.com/lsernau/grh-lean">GitHub - lsernau / grh - lean : A short Lean 4 proof of the Generalized...</a></li>
<li><a href="https://news.ycombinator.com/item?id=50648050">Much shorter version of GRH Lean verification from Anthropic</a></li>
<li><a href="https://mrubinst.github.io/grh-lean-verification/">GRH Lean Check</a></li>

</ul>
</details>

**Tags**: `#Lean`, `#formal verification`, `#GRH`, `#theorem proving`, `#mathematics`

---

<a id="item-tech-news-2"></a>
### [1Password Says Vaults Stayed Intact in Account-Data Incident](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password said attackers accessed internal systems and stole some customer account metadata, including names, email addresses, account IDs, and account creation and recent-login timestamps; the company said customer vaults and their contents were not affected. The company began investigating on November 19 after determining that a compromised employee enterprise GitHub account had been used to access source code and push malicious code to backend services, resulting in data downloads, but it did not disclose the number of affected customers. 1Password disabled the implicated accounts, rotated or revoked potentially exposed internal credentials, strengthened verification for invitation and recovery emails, and advised customers that they did not need to change their 1Password account credentials but should watch for phishing.

hackernews · lxhrstn · Nov 25, 17:18 · [Discussion](https://news.ycombinator.com/item?id=50644817)

**「How the GitHub-to-backend attack path works」** The incident illustrates a software-supply-chain intrusion path: compromising an employee’s corporate GitHub account can provide access to source code and a route for pushing malicious changes into backend services, where the code can retrieve administrative customer data. 1Password says this was the path it investigated beginning November 19, and it distinguishes the affected account metadata from customers’ vaults and their contents, which the company says were not affected \(tool-1-1\).

**「Heightened targeted-phishing risk」** The concrete consequence is increased phishing risk rather than vault compromise: 1Password says the exposed information included customer names, email addresses, and non-secret account metadata, while customer vault contents were never accessed. Users do not need to change their account credentials, but should access 1Password directly and treat unexpected share, invitation, or recovery emails containing personal details as possible phishing; one Hacker News commenter reported receiving such a tailored email without establishing that the incident supplied the data.

**「Community Reactions」** One commenter reported receiving a sophisticated phishing email that appeared to use leaked personal details and imitate a 1Password vault-sharing notification, although they did not establish a direct connection to the incident. Other participants said the announcement did not sufficiently explain whether malicious code could reach production and whether repository branch protections were missing or bypassed.

<details><summary>References</summary>
<ul>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving 1Password’s backend ...</a></li>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving... | 1 Password</a></li>
<li><a href="https://news.ycombinator.com/item?id=50644817">1 Password Security Incident | Hacker News</a></li>

</ul>
</details>

**Tags**: `#1Password`, `#security incident`, `#SaaS security`, `#credential phishing`, `#incident response`

---

<a id="item-tech-news-3"></a>
### [Minecraft Java Font Flaw Enables RCE; Community Fix Available](https://github.com/bikini/minecraft2shell) ⭐️ 8.0/10

The public minecraft2shell proof of concept reportedly triggers an out-of-bounds write in FreeType 2.14.3 and earlier when a malicious TrueType font is loaded from a server resource pack, enabling arbitrary code execution on a Windows Minecraft Java Edition 26.3 client. The disclosure affects Java Edition 1.20.5 through 1.21.10 and 26.1 through 26.4 snapshots; Java Edition 1.20.4 and earlier and Bedrock Edition are reportedly unaffected. Mojang is still using lwjgl-freetype 3.4.3 and has not issued an official patch, while the community’s m2sfix 1.0.0 temporarily disables font hinting through a Java agent or mod; until a patch is available, players are advised not to install resource packs and to disable resource-pack permissions on multiplayer servers.

telegram · zaihuapd · Nov 25, 12:46

**「Background」** The flaw is in the native font-rendering layer rather than Minecraft&\#x27;s Java gameplay code: Java clients process TrueType fonts from server resource packs through LWJGL&\#x27;s bundled FreeType, identified in the report as lwjgl-freetype 3.4.3. FreeType 2.14.3 and earlier are vulnerable, with the affected range beginning at Java Edition 1.20.5; Java Edition 1.20.4 and earlier and Bedrock Edition are reported unaffected.

**「Practical mitigation」** Until Mojang releases a patch, affected Java Edition users should avoid installing resource packs and set multiplayer servers&\#x27; resource-pack permission to &quot;Disabled&quot;; the public PoC demonstrates native code execution in the signed Java 26.3 Windows client with bundled FreeType 2.14.3 x64. The community m2sfix 1.0.0 Java agent or mod provides a temporary workaround by disabling hinting, but it is not an official replacement for a patched lwjgl-freetype library.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/bikini/minecraft2shell">GitHub - bikini/ minecraft 2 shell : Minecraft to native RCE · GitHub</a></li>

</ul>
</details>

**Tags**: `#Minecraft`, `#Remote Code Execution`, `#FreeType`, `#Font Security`, `#Vulnerability Disclosure`

---

<a id="item-tech-news-4"></a>
### [FCC Clears SpaceX’s 1M-Satellite Starmind Constellation](https://www.geekwire.com/2026/fcc-clears-spacex-million-satellites-starmind-data-center/) ⭐️ 8.0/10

According to GeekWire, the FCC authorized SpaceX to deploy up to 1 million Starmind satellites for an on-orbit data-processing network operating at altitudes of 500 to 1,002 kilometers. The approval requires communications backup, regular progress reporting and a detailed orbital-debris mitigation plan; the first satellite must operate by 2033, and the full constellation by 2040. The FCC also rejected objections from Amazon, Viasat and the American Astronomical Society. This is a secondary media account rather than the FCC’s primary order, so the report has not been independently verified here.

telegram · zaihuapd · Nov 26, 04:45

**「Proposal and phased deployment」** SpaceX filed its Starmind proposal with the FCC earlier in 2026. The authorization carries a phased deployment schedule rather than an immediate requirement to place all one million satellites in orbit: BBC reported that deployment must begin by November 2033, reach 10% by November 2035 and 50% by November 2038, while SpaceX has said it aims to launch the first satellite next year.

**「No immediate Starmind capacity」** Developers and customers should not treat the authorization as immediate Starmind capacity: the first satellite is due by 2033 and the full constellation by 2040, subject to reporting, communications-backup, and debris-mitigation requirements. For link planning, SpaceX also states that it will not routinely use Ka-band, limiting it to backup and emergency support, so routine Ka-band service cannot be assumed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cwp836l8n1jgo">US approves SpaceX plan to send a million data satellites to space</a></li>
<li><a href="https://nypost.com/2026/11/25/business/fcc-approves-elon-musks-spacex-to-launch-1-million-satellites-for-data-centers-in-space/">FCC approves Elon Musk&#x27;s SpaceX to launch 1 million satellites for...</a></li>
<li>DA-26-1273A1.txt - Federal Communications Commission</li>

</ul>
</details>

**Tags**: `#太空数据中心`, `#SpaceX`, `#FCC`, `#卫星星座`, `#轨道基础设施`

---

<a id="item-tech-news-5"></a>
### [Aaronson links 9/4 matrix multiplication to AI-assisted discovery](https://scottaaronson.blog/?p=10379) ⭐️ 7.0/10

Scott Aaronson’s post highlights a linked result, “The matrix multiplication exponent is nine fourths,” which gives the matrix-multiplication exponent an upper bound of ω = 9/4 = 2.25. Aaronson uses the result to argue that AI-assisted mathematical discovery is already a consequential and underappreciated capability. The supplied excerpt does not identify the AI system, explain its role, or independently validate the paper, so the post’s broader claims should not be treated as established by the excerpt alone.

hackernews · Kotlopou · Nov 25, 19:11 · [Discussion](https://news.ycombinator.com/item?id=50646108)

**「Why the exponent matters」** The matrix multiplication exponent, ω, summarizes the asymptotic arithmetic cost of multiplying n×n matrices, with lower values indicating algorithms that scale better as n grows. The linked nine-fourths result concerns that scaling and provides an upper bound; it does not prove that still faster algorithms are impossible. The AI-assisted-discovery framing concerns the construction’s provenance, while its correctness depends on a checkable mathematical argument.

**「Practical outcomes are the stronger test」** One commenter argued that AI’s impact should be judged by outcomes such as making Deutsche Bahn run on time, rather than by the drama surrounding mathematical proofs; they noted that some useful solutions may already exist but remain unexploited. This is an opinion rather than a measured result, but it suggests a concrete evaluation concern: claims about AI-assisted discovery should be tested against deployed, user-visible improvements.

**「Community Debate」** Commenters disputed what the mathematical result implies about broader AI capability. jsLavaGoat argued that competence in axiomatic mathematics does not imply solving science generally or becoming an existential threat, while nickysielicki maintained that there is no current evidence that labs have broken cryptosystems and that such a secret would likely leak; Nevermark instead argued that people systematically underreact to large technological changes.

<details><summary>References</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50646108">Holy shit holy shit holy shit holy shit : The magnitude... | Hacker News</a></li>

</ul>
</details>

**Tags**: `#AI-assisted discovery`, `#matrix multiplication`, `#AI safety`, `#algorithms`

---

<a id="item-tech-news-6"></a>
### [Google publishes Cogentic papers on integer factorization and discrete logarithms](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) ⭐️ 7.0/10

Google Research released a collection of Cogentic research papers covering integer factorization, discrete logarithms, and other computational mathematics problems. The supplied item does not include the papers’ abstracts, algorithms, benchmarks, or independent verification, so it does not establish that the work produced new factoring or discrete-log records or practical cryptographic gains. The release is best described as publication of primary research papers rather than a demonstrated cryptographic break.

hackernews · rgwohlbold · Nov 25, 13:33 · [Discussion](https://news.ycombinator.com/item?id=50642086)

**「Background」** The papers build on Cogentic, described in an earlier arXiv paper as a multi-agent harness for automated proof discovery on open research problems. The collection applies that general framework to specific computational-mathematics tasks, including a paper stored under the \`deterministic\_factoring\_l34\` directory, although the supplied result does not expose its abstract or findings.

**「Cryptographic impact remains unverified」** Cryptography implementers should treat these results as unverified theoretical claims rather than immediately usable algorithms: the papers include a claimed unconditional integer-factorization bound of L\_N\[1/3, O\(1\)\], deterministic subexponential factoring, and a sub-quasi-polynomial discrete-logarithm algorithm for finite fields of fixed characteristic. Public Lean proofs and outside review of the headline factoring claim are still pending, so there is not yet a verified basis for changing deployment choices or security plans.

**「Community discussion」** martythemaniak compared the recent wave of mathematical advances with AlphaGo’s ability to explore enormous search spaces, while fidotron cited a social-media rumor that the Cogentic release was the tip of a larger effort. These are speculative interpretations; the supplied discussion contains no technical assessment of the papers’ methods or results.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/google-research/google-research/blob/master/cogentic_research_papers/deterministic_factoring_l34/paper.pdf">github .com/ google - research / google - research /blob/master/ cogentic ...</a></li>
<li><a href="https://arxiv.org/abs/2609.40324">Cogentic : Multi-Agent Orchestration for Automated Proof Discovery</a></li>
<li><a href="https://magica.com/news/google-cogentic-six-math-papers-factoring-proof-claim">Google Cogentic claims new factoring bound in six math papers ...</a></li>
<li><a href="https://daily.dev/posts/google-releases-cogentic-papers-on-integer-factorization-discrete-logs-and-more-0lfmvr55g">Google Releases Cogentic Papers on Integer Factorization ...</a></li>

</ul>
</details>

**Tags**: `#AI for mathematics`, `#cryptography`, `#integer factorization`, `#Google Research`, `#algorithms`

---

<a id="item-tech-news-7"></a>
### [OpenAI expands cybersecurity push with GPT-6 Cyber and Daybreak](https://www.theinformation.com/newsletters/ai-agenda/openais-roadmap-making-cyber-bigger-coding-remains-blurry) ⭐️ 7.0/10

OpenAI has launched GPT-6 Cyber for security research and expanded its Daybreak trusted-access program, which by September reportedly included thousands of verified defenders and roughly 2,000 approved organizations and workspaces. The tools support vulnerability discovery, codebase analysis, and binary reverse engineering, while company executives claim cybersecurity represents an underestimated market above $300 billion and could become a larger OpenAI business than coding. The report does not provide benchmarks, technical details, or evidence of commercial scale, and it says OpenAI’s competitive position against Anthropic and Google remains unclear.

telegram · zaihuapd · Nov 25, 04:51

**「Background」** OpenAI’s cybersecurity expansion builds on Trusted Access for Cyber, introduced on February 5, 2026 as a trust-based framework for widening access to advanced cyber capabilities while adding safeguards against misuse. By November 5, OpenAI had introduced GPT-6 Cyber for finding exploitable vulnerabilities and developing fixes within authorized scope, alongside Daybreak, which includes $1 billion in subsidized access, training, technical support, and partnerships for qualifying critical-infrastructure and public-interest organizations.

**「Practical impact」** For organizations evaluating OpenAI’s cyber products, GPT-6 Cyber’s reported API price—60% higher for input and roughly 33% higher for output than GPT-5.6 Cyber—makes workload-cost comparisons important before scaling vulnerability research. Daybreak is intended to automate vulnerability detection, patch validation, and secure software development for enterprises and governments, but adopters should validate those capabilities in their own environments because the source provides no independent performance benchmarks or commercial validation.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/trusted-access-for-cyber/">Introducing Trusted Access for Cyber - OpenAI</a></li>
<li><a href="https://openai.com/daybreak/">Daybreak | OpenAI for cybersecurity</a></li>
<li><a href="https://openai.com/index/introducing-gpt-6-cyber/">GPT‑6 Cyber: Advancing the frontier of aligned cybersecurity ...</a></li>
<li><a href="https://venturebeat.com/technology/openai-launches-gpt-6-cyber-with-stronger-exploit-research-and-higher-api-price-than-anthropic-and-google">OpenAI launches GPT-6 Cyber with stronger exploit research ...</a></li>
<li><a href="https://www.csoonline.com/article/4170029/openai-introduces-daybreak-cyber-platform-takes-on-anthropic-mythos.html">OpenAI introduces Daybreak cyber platform, takes on Anthropic ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#网络安全`, `#生成式AI`, `#漏洞研究`

---

<a id="item-tech-news-8"></a>
### [Tencent Releases Quantized Hy4 Flash for 64 GB Mac mini](https://mp.weixin.qq.com/s/o0xxShVQX6g2UllrrEv1WQ) ⭐️ 7.0/10

Tencent Hunyuan open-sourced GGUF quantized weights for its 224B-parameter Hy4 flash model through the AngelSlim compression toolkit, giving local-model developers access to the release. The original weights are approximately 410.27 GiB, while the smallest IQ2-AH version is 125.73 GiB—about 30% of the original—and Tencent says it can run on a 64 GB Mac mini with the Strata offload framework. Tencent reports 89 tokens per second at a 10K context on a 48 GB VRAM device and 47 tokens per second at a 32K context for Q3\_K on an M5 Max with 128 GB; in DeepSWE v1.1 and other reported evaluations, Q3\_K trailed the original model by no more than 0.4 points. These performance and quality figures are vendor-reported, and the brief source provides no independent validation or detailed methodology.

telegram · zaihuapd · Nov 25, 09:29

**「Background」** AngelSlim is Tencent Hunyuan&\#x27;s model-compression and acceleration toolkit, and its Hy4-flash-GGUF repository on Hugging Face already listed the quantized shards — including a Q3\_K file page dated November 18, 2026 — together with instructions for running the model through llama.cpp, several days before the November 25 announcement. GGUF quantization shrinks weights at the cost of some accuracy, and offloading frameworks such as Strata go a step further by holding weights in system memory and streaming layers into the compute device on demand, which is what makes a 224B-parameter model usable on a 64 GB Mac mini that could never hold the full model in GPU memory. Aibase separately reported the same size figures \(about 410.27 GiB for the original weights, roughly 30% for the smallest quant\), consistent with the primary account.

**「Local deployment with offloading」** Developers can now evaluate Hy4 flash locally on a 64 GB Mac mini by combining the GGUF weights with Strata offloading, but even the 125.73 GiB IQ2-AH build exceeds system memory, so deployment is not fully resident. The published speeds and evaluation results are configuration-specific and should be tested on the intended hardware rather than treated as universal Mac mini benchmarks.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/AngelSlim/Hy4-flash-GGUF">AngelSlim/Hy4-flash-GGUF · Hugging Face</a></li>
<li><a href="https://huggingface.co/AngelSlim/Hy4-flash-GGUF/blob/main/Hy4-flash-Q3_K-00001-of-00002.gguf">Hy4-flash-Q3_K-00001-of-00002.gguf · AngelSlim/Hy4-flash-GGUF ...</a></li>
<li><a href="https://www.aibase.com/news/32527">Tencent Hunyuan open-sources Hy4 flash GGUF quantized weights ...</a></li>

</ul>
</details>

**Tags**: `#LLM quantization`, `#GGUF`, `#model offloading`, `#open-source AI`, `#Apple Silicon`

---

<a id="item-tech-news-9"></a>
### [Asian Data Centers Seek U.S. Buyers for AI Compute](https://www.bloomberg.com/news/articles/2026-11-25/asia-data-centers-sound-out-us-clients-to-replace-china-demand) ⭐️ 7.0/10

The U.S. tightened a policy gap that had allowed Chinese technology companies to obtain Nvidia’s most advanced chips, prompting data-center operators in parts of Asia to seek U.S. customers for excess AI computing capacity. Liquid Compute CEO Ronit Jain said new export rules covering advanced AI accelerators are disrupting providers whose businesses depended on renting capacity to Chinese customers. The supplied Bloomberg excerpt, relayed through Telegram, does not specify the rule’s effective date, exact scope, affected countries, or the scale of redirected capacity.

telegram · zaihuapd · Nov 25, 11:35

**「Export controls disrupted Asian AI-cloud demand」** The policy backdrop is the U.S. export-control regime for advanced AI accelerators marketed through Southeast Asia. By narrowing a route Chinese technology firms had used to access Nvidia’s newest chips, the rules left regional data centers that planned to rent capacity to Chinese customers vulnerable to unused supply; follow-up reporting specifically cites excess Nvidia B300 capacity in this market.

**「Data-center operators face redirected demand and tighter financing scrutiny」** Asian data-center operators must now replace expected Chinese demand by marketing excess compute capacity to US buyers, according to Liquid Compute CEO Ronit Jain; the tighter export rules are disrupting providers that had planned to rent capacity to Chinese customers. The restrictions are also affecting financing, with TrendForce reporting that global banks are increasing scrutiny of Southeast Asian data-center clients, making customer due diligence more consequential for AI-chip-linked deals.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-25/asia-data-centers-sound-out-us-clients-to-replace-china-demand">Asia Data Centers Sound Out US Clients to Replace China ...</a></li>
<li><a href="https://www.explainx.ai/blog/asia-neoclouds-remarket-b300-us-western-buyers-banks-november-2026">Asia DCs Offload B300 to US: Banks Review Loans - explainx.ai</a></li>
<li><a href="https://thenextweb.com/news/asia-data-centres-b300-prices-us-buyers-chip-rules">Asian data centres look to US buyers as US chip rules bite ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-25/asia-data-centers-sound-out-us-clients-to-replace-china-demand">Asia Data Centers Sound Out US Clients to Replace China Demand</a></li>
<li><a href="https://www.trendforce.com/news/2026/11/25/news-global-banks-reportedly-push-southeast-asian-data-center-clients-to-reveal-ai-chip-users-amid-u-s-curbs/">[News] Global Banks Reportedly Push Southeast Asian Data Center ...</a></li>

</ul>
</details>

**Tags**: `#AI芯片`, `#出口管制`, `#AI算力`, `#数据中心`

---

<a id="item-tech-news-10"></a>
### [OpenAI Tests Private Inference for Select Customers](https://x.com/sama/status/2125638790593274259) ⭐️ 7.0/10

Sam Altman said OpenAI is testing a private inference service with a small number of customers as the latest offering in its OpenAI Private Intelligence series. He claimed the service can support zero data retention while automatically conducting safety reviews through Private Safety Processing, with OpenAI staff unable to access the underlying content. The test remains limited, and the announcement provides no technical architecture, audit methodology, customer details, or performance data to substantiate those privacy claims.

telegram · zaihuapd · Nov 26, 01:44

**「Background」** OpenAI frames Private Inference as the latest product in its Private Intelligence series, with privacy controls layered around model use. Its zero-data-retention setup is paired with Private Safety Processing, which the company says can automate safety review while preventing OpenAI staff from accessing the underlying content.

**「Enterprise deployment impact」** For eligible API customers covered by OpenAI’s Zero Data Retention terms, prompts and responses are not retained after processing, while Private Safety Processing can conduct automated safety review without exposing underlying content to OpenAI personnel. Private Inference is still a limited-customer preview, however, so organizations should confirm preview eligibility, retention boundaries, and review terms before sending sensitive enterprise data.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/offering-zero-data-retention-for-frontier-models/">Offering Zero Data Retention for frontier models | OpenAI</a></li>
<li><a href="https://scalevise.com/resources/openai-private-intelligence-data-controls-rollout/">OpenAI Private Intelligence: Data Controls and Rollout</a></li>

</ul>
</details>

**Tags**: `#私有推理`, `#AI 隐私`, `#零数据保留`, `#企业 AI`, `#OpenAI`

---

## Financial News

<a id="item-finance-news-1"></a>
### [U.S. government reportedly acquired 10% of Intel without payment](https://www.wired.com/story/inside-trumps-demands-to-another-chips-ceo/) ⭐️ 8.0/10

A Telegram post citing court filings says the U.S. Department of Commerce warned Intel in August 2025 that refusing to surrender 10% of its shares would bring “unpredictable consequences.” Intel’s board then transferred the stake, which President Trump said gave the U.S. government full ownership and control without payment; the reported value was about $11 billion.

telegram · zaihuapd · Nov 25, 13:25

**「Background」** Court-filing coverage said the stake demand was tied to Intel’s pending release of CHIPS Act grants—federal subsidies for domestic semiconductor manufacturing.

**「Impact」** If the court-file account is accurate, the federal government’s 10% equity stake gives it shareholder voting influence over Intel, directly linking the chipmaker’s corporate governance to U.S. industrial policy.

<details><summary>References</summary>
<ul>
<li>Lawsuit reveals Trump&#x27;s alleged strong-arming of Intel — troubled chipmaker allegedly forced to give White House 10% stake for release of CHIPS Act funds - Yahoo</li>
<li>Wired: Commerce Lawyer Warned Intel CFO Rejecting US 10% Stake Would Carry &#x27;Unpredictable Consequences&#x27; | AI Weekly</li>
<li><a href="https://en.wikipedia.org/wiki/Corporate_governance">Corporate governance - Wikipedia</a></li>
<li><a href="https://www.nytimes.com/2025/11/25/us/politics/trump-intel-steel-minerals-china.html">Trump Administration Is Taking Billions in Stakes in Firms Like Intel ...</a></li>

</ul>
</details>

**Tags**: `#英特尔`, `#美国商务部`, `#政府持股`, `#芯片产业`, `#公司治理`

---

<a id="item-finance-news-2"></a>
### [U.S. Proposes New Tariffs on 14 Trading Partners](https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html) ⭐️ 8.0/10

The U.S. plans country-specific tariffs under Section 301 on China, the EU and 12 other partners, with China facing an additional 20% on top of its existing 25%; that additional rate could rise to 40% if China does not comply with the October 2025 Busan trade truce. The proposal does not specify an effective date, a complete product list or the rates for the other partners.

telegram · zaihuapd · Nov 25, 13:59

**「Background」** Section 301 of the 1974 Trade Act is the U.S. trade-law mechanism cited for imposing country-specific tariffs after investigations; the proposal comes months after the Supreme Court struck down much of President Trump’s earlier tariffs. For China, the comparison point is the 25% tariff added in 2018, while the higher proposed rate is tied to whether Beijing honors the October 2025 trade truce.

**「Business impact」** If implemented, the proposed tariffs would raise U.S. import costs for businesses buying goods or inputs from China, the EU and 12 other partners, potentially pressuring margins and requiring supply-chain adjustments; China’s additional tariff is proposed at 20% on top of the 25% imposed in 2018 and could rise to 40% if it does not comply with the October 2025 trade truce.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html">U . S . unveils new Section 301 tariffs targeting China , EU and others</a></li>
<li><a href="https://nypost.com/2026/11/25/business/us-proposes-new-tariffs-on-14-trading-partners-including-china-japan-eu-and-india/">US proposes new tariffs on 14 trading partners — including China ...</a></li>
<li><a href="https://globalimportblog.bakermckenzie.com/2026/11/25/us-ustr-proposes-section-301-tariffs-on-14-economies-over-structural-excess-capacity/">US: USTR Proposes Section 301 Tariffs on 14 Economies Over ...</a></li>
<li><a href="https://invezz.com/news/2026/11/25/trump-new-tariffs-14-economies-2026/">Trump proposes new tariffs on China, EU and 12 other partners</a></li>

</ul>
</details>

**Tags**: `#美国关税`, `#中美贸易`, `#第301条`, `#贸易政策`, `#全球供应链`

---