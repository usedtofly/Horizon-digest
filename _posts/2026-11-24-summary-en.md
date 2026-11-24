---
layout: default
title: "Horizon Summary: 2026-11-24 (EN)"
date: 2026-11-24
lang: en
---

> From 38 items, 14 important content pieces were selected

---

**Technology News**
1. [Nvidia Board Reinstates Jensen Huang as CEO](#item-tech-news-1) ⭐️ 8.0/10
2. [Ladybird’s first alpha is installable on macOS and Linux](#item-tech-news-2) ⭐️ 8.0/10
3. [GLM-5.4 Introduces Z.ai&\#x27;s First Loop Transformer](#item-tech-news-3) ⭐️ 8.0/10
4. [Codex2api 3.1.10–3.1.12 releases reported compromised](#item-tech-news-4) ⭐️ 8.0/10
5. [Anthropic Publishes a Lean 4 Proof Claim for VP ≠ VNP](#item-tech-news-5) ⭐️ 8.0/10
6. [NariQ offers 10 GB Qwen3.8-27B quantizations](#item-tech-news-6) ⭐️ 7.0/10
7. [Stalwart Claims Drop-in Compatibility with Microsoft Exchange](#item-tech-news-7) ⭐️ 7.0/10
8. [New York Restricts Car Subscription and Post-Purchase Fees](#item-tech-news-8) ⭐️ 7.0/10
9. [ChatGPT Rolls Out GPT-6.2 Sol to Paid Tiers](#item-tech-news-9) ⭐️ 7.0/10
10. [Huawei reports HarmonyOS 5–7 exceed 100 million devices](#item-tech-news-10) ⭐️ 7.0/10
11. [Shenzhou-24 Targets Nov. 25 Launch with Pakistani Astronaut](#item-tech-news-11) ⭐️ 7.0/10

**Technology Blog**
1. [Day-0 vLLM Support for ERNIE 5.5 Flash Preview](#item-tech-blog-1) ⭐️ 8.0/10

**Financial News**
1. [Nvidia restores Jensen Huang as CEO, lifting U.S. stocks](#item-finance-news-1) ⭐️ 8.0/10
2. [Anthropic IPO selloff clouds Chinese AI listing plans](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Nvidia Board Reinstates Jensen Huang as CEO](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 8.0/10

Nvidia’s board reinstated co-founder Jensen Huang as CEO, reversing his earlier removal from the role. In the announcement text quoted in the discussion, the board said it received input from senior U.S. government officials and was confident that Huang’s reinstatement posed no national security risk; commenters described the decision as unanimous. The supplied material does not explain the original ouster, identify any board changes, or specify consequences for Nvidia’s AI-chip products or export-control policy.

hackernews · jaz · Nov 23, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50611576)

**「Background」** NVIDIA develops GPUs, systems on chips, and software APIs used in artificial intelligence and high-performance computing, so its chief executive’s decisions directly affect the company’s AI-chip strategy. The report concerns Huang’s return to that leadership role, while the supplied material does not establish the precise timing or stated reasons for his earlier removal.

**「Leadership continuity and governance scrutiny」** Nvidia’s leadership uncertainty has ended abruptly: the company reinstated Huang days after its board rejected his offer to return and said it had no intent to reinstate him. Customers, developers, and investors can therefore plan around Huang remaining in charge rather than a succession transition, although the board’s stated consultation with senior U.S. government officials means China- and export-policy decisions under his leadership will face heightened governance scrutiny.

**「Community Discussion」** Commenters debated whether the episode demonstrated effective board oversight or outside influence over a nominally independent board; one commenter invoked Delaware’s Caremark standard and the Justice Department’s decision not to prosecute as likely protection from individual board liability. Another commenter criticized the contrast between U.S. pressure on ASML and Japanese chipmakers to join China sanctions and what they described as Nvidia receiving preferential treatment, while others argued that there was no evidence of criminal conduct by Huang or Nvidia.

<details><summary>References</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/Nvidia">Nvidia - Wikipedia</a></li>
<li><a href="https://www.nvidia.com/">World Leader in Artificial Intelligence Computing | NVIDIA</a></li>
<li>Nvidia rejects Jensen Huang&#x27;s offer to return as CEO despite pressure from Silicon Valley</li>
<li>Nvidia board does not intend to reinstate… | UCapital News</li>

</ul>
</details>

**Tags**: `#NVIDIA`, `#Executive Leadership`, `#AI Semiconductors`, `#Corporate Governance`, `#Export Controls`

---

<a id="item-tech-news-2"></a>
### [Ladybird’s first alpha is installable on macOS and Linux](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

Ladybird released its first alpha, making the browser installable on macOS and Linux without compiling it; most core components—including HTML parsing, CSS, layout, JavaScript, and WebAssembly—are implemented by the project, while HarfBuzz, Skia, ffmpeg, and SQLite remain external dependencies. Simon Willison reported that it felt fast and lightweight and successfully handled advanced WebAssembly examples using ffmpeg and Pyodide, but Datasette Lite failed because the service-worker API \`navigator.serviceWorker.startMessages\` was unavailable; project lead Andreas Kling also warned that some sites will fail and crashes remain possible. The project’s October results included a new JavaScript JIT, a Cranelift-based WebAssembly engine that it credited with a 7x JetStream 3 improvement, and an AI-assisted Web Platform Tests increase from roughly 2.12 million to 2.18 million passing subtests in five days. The final chart placed Ladybird at 2,184,722 passing subtests, ahead of Safari’s 2,172,990 but below Firefox and Chrome, so the release indicates substantial compatibility progress without establishing production-level reliability.

hackernews · janvdberg · Nov 23, 16:13 · [Discussion](https://news.ycombinator.com/item?id=50614249)

**「Project background」** Ladybird grew out of the SerenityOS project and carries code from that earlier operating-system effort into its browser engine. It implements core browser technologies—including HTML parsing, CSS, layout, JavaScript, and WebAssembly—while using established external components such as HarfBuzz, Skia, ffmpeg, and SQLite.

**「Practical effect」** Users on macOS and Linux can now install the alpha and test it without building the source, while developers can target concrete gaps such as service-worker behavior and submit crash or broken-site reports. It should still be treated as an experimental browser rather than a dependable daily driver because compatibility failures and crashes are explicitly acknowledged.

**「Community reaction」** Testers were broadly positive: commenter freakynit said many sites rendered correctly with only minor jerky scrolling, while alentred reported success on difficult news and Proxmox/NoVNC pages and considered NoVNC unusually snappy compared with Firefox. Other commenters remained cautious about daily-driver suitability, while drnick1 argued that Ladybird should adopt stronger fingerprinting resistance, more granular permissions, and restrictions on page behaviors such as disabling selection or paste; those points were user opinions rather than established capabilities.

**Tags**: `#web browsers`, `#browser engineering`, `#web compatibility`, `#fingerprinting privacy`, `#alpha releases`

---

<a id="item-tech-news-3"></a>
### [GLM-5.4 Introduces Z.ai&\#x27;s First Loop Transformer](https://z.ai/blog/glm-5.4) ⭐️ 8.0/10

Z.ai released GLM-5.4 for coding, built on its first loop-transformer design: a group of weight-shared layers runs multiple iterations per forward pass, refining hidden states without increasing the parameter count. The model was not available as open weights, and tester Simon Willison found that it required a Coding Plan subscription because it was not yet exposed through the regular API; the plan&\#x27;s key nevertheless worked with Z.ai&\#x27;s existing OpenAI-compatible Responses API endpoint. His low-, high-, and max-effort pelican tests resembled GLM-5.3, so this account supports the new architecture and access path but does not establish independently verified performance gains.

hackernews · foohis · Nov 23, 10:06 · [Discussion](https://news.ycombinator.com/item?id=50609685)

**「How loop transformers add depth」** Z.ai describes a standard Transformer as running each layer once per forward pass, while its loop-transformer design reruns a group of weight-shared layers for multiple iterations to refine hidden states without increasing the parameter count. The preceding GLM-5.3 was described by Z.ai as the lab’s flagship, making 5.4 the move from that generation to the company’s first looped model.

**「Access and tooling constraints」** GLM-5.4 is not yet available as open weights, so developers cannot deploy it locally like the GLM releases that are typically distributed under MIT or Apache 2.0 licenses. API users must currently rely on Z.ai’s Coding Plan, which lists GLM-5.4 as supported; in the reported hands-on test, its API key worked through the OpenAI-compatible Responses API, but the existing llm-zai plugin lacked model support, requiring the separate llm-glm plugin until compatibility catches up.

**「Community discussion」** Commenters welcomed Z.ai&\#x27;s unusually detailed architectural disclosure and saw looped, shared-weight execution as a plausible response to inference memory-bandwidth limits, though they noted unresolved design questions. One commenter reported that Chinese models&\#x27; extended &quot;marathon thinking&quot; can repeatedly second-guess simple tasks and substantially increase completion time, but that remains anecdotal rather than a controlled efficiency comparison.

<details><summary>References</summary>
<ul>
<li>Z.ai API Platform — Start building with GLM-5.3</li>
<li><a href="https://en.wikipedia.org/wiki/GLM_%28AI%29">GLM (AI) - Wikipedia</a></li>
<li><a href="https://z.ai/subscribe">GLM Coding Plan — AI Coding Powered by GLM -5.4 &amp; GLM -5.3-Flash...</a></li>

</ul>
</details>

**Tags**: `#large language models`, `#loop transformers`, `#coding models`, `#AI architecture`

---

<a id="item-tech-news-4"></a>
### [Codex2api 3.1.10–3.1.12 releases reported compromised](https://github.com/WormW/codex2api-incident-2026-11) ⭐️ 8.0/10

A Telegram report alleges that a compromised Codex2api maintainer account pushed tags outside the main branch, causing releases 3.1.10 through 3.1.12 to contain malicious code. Version 3.1.11 reportedly removed authentication, enabling passwordless remote command execution, while a workflow exfiltrated 16 GitHub Actions secrets and potentially affected at least 21 repositories under the same account. The report remains unverified; it advises users who installed those versions to stop using them, roll back to 3.1.9, and rotate GitHub tokens, SSH keys, database credentials, DeepSeek credentials, and other related secrets.

telegram · zaihuapd · Nov 23, 11:21

**「Product context」** Codex2API is described as a Go and React/Vite reverse-proxy and management system that turns a pool of upstream Codex accounts, accessed with refresh or access tokens, into a unified OpenAI-compatible API. The Telegram-linked report concerns how alleged malicious release versions may have affected that deployment and its automation credentials, but the compromise remains an unverified allegation rather than an independently confirmed finding.

**「Containment Steps」** The report says the affected Codex2api builds exposed 16 GitHub Actions secrets and may have affected at least 21 repositories under the maintainer account; anyone who installed or updated versions 3.1.10–3.1.12 should immediately stop using them, roll back to 3.1.9, and rotate or revoke GitHub tokens, SSH keys, database credentials, DeepSeek keys, and every other secret available to those workflows. StepSecurity’s analysis of a separate GitHub Actions secret-stealing campaign warns that attackers can retain cloud access after credential rotation, so maintainers should also review workflow activity and cloud-account access as a precaution, though this does not independently confirm the Codex2api allegation.

<details><summary>References</summary>
<ul>
<li><a href="https://deepwiki.com/james-6-23/codex2api">james-6-23/ codex2api | DeepWiki</a></li>
<li><a href="https://www.stepsecurity.io/blog/wfx-phantom-the-github-actions-secret-stealer">WFX Phantom: The GitHub Actions Secret Stealer... - StepSecurity</a></li>

</ul>
</details>

**Tags**: `#software supply chain security`, `#GitHub Actions`, `#credential compromise`, `#malicious release`, `#Codex2api`

---

<a id="item-tech-news-5"></a>
### [Anthropic Publishes a Lean 4 Proof Claim for VP ≠ VNP](https://github.com/anthropics/formal-math/blob/main/vp-vnp/README.md) ⭐️ 8.0/10

Anthropic released a paper titled “VP ≠ VNP over every field” and a Lean 4 formalization, saying an internal research Claude model discovered the result and wrote both the paper and code. The paper claims a superpolynomial arithmetic-circuit lower bound for the Hamiltonian-cycle polynomial, which—if the formal statement matches the intended theorem—would show that VP is a proper subclass of VNP over every field and resolve Valiant’s 1979 algebraic-complexity conjecture; it does not address P versus NP. The repository reports checks against three standard axioms and a review using the nanoda kernel, with no \`sorry\` outside reserved files, but no human mathematician has yet read the proof in full, and Appendix Q lists discrepancies that require independent review.

telegram · zaihuapd · Nov 24, 06:02

**「Background」** VP and VNP are classes defined using polynomial-size arithmetic circuits, and Valiant’s algebraic-complexity conjecture proposes that VP is a proper subclass of VNP. This is an analogue of P versus NP, not the same problem: arithmetic circuits must operate over a field and its extensions, so a proof of VP ≠ VNP would not settle P versus NP.

**「Impact」** Researchers can now inspect Anthropic’s paper and Lean 4 development for the claimed superpolynomial arithmetic-circuit lower bound and the resulting statement VP ⊊ VNP. Before treating the algebraic-complexity result as resolved, independent mathematicians must verify the theorem and reconcile Appendix Q’s documented differences between the formalized statement and the intended proposition; the kernel checks and absence of admitted \`sorry\` placeholders do not by themselves establish correctness, and the claim does not resolve P versus NP.

<details><summary>References</summary>
<ul>
<li><a href="https://www.alphaxiv.org/abs/2611.vp-vnp-arithmetic-lower-bounds">VP VNP Over Every Field | alphaXiv</a></li>
<li><a href="https://www.youtube.com/watch?v=UuOiRi9T-9c">Claude &#x27;s VP VNP Proof: 47 Years Open, Still Unchecked... - YouTube</a></li>

</ul>
</details>

**Tags**: `#AI 数学发现`, `#定理证明`, `#Lean 4`, `#计算复杂性`, `#Claude`

---

<a id="item-tech-news-6"></a>
### [NariQ offers 10 GB Qwen3.8-27B quantizations](https://huggingface.co/nari-labs/Qwen3.8-27B-NariQ-GGUF) ⭐️ 7.0/10

For local-inference users, Nari Labs published NariQ, GGUF quantizations of Qwen3.8-27B at 3 bits per weight and below, including a roughly 10 GB file that currently requires the custom nari-llama.cpp fork. The project’s self-reported results show the 3-bit version slightly exceeding BF16 on DeepSWE \(41.0 versus 39.8\) and Terminal-Bench 2.1 \(63.8 versus 62.6\), while the 2-bit version fell to 28.6 and 52.4; NariQ also reports 64K context-length tests and RTX PRO 6000 decode speed comparable to other quantizations. These measurements support the vendor’s “near-BF16” claim for the 3-bit and 2.5-bit variants, but they are model-card results rather than independent validation, and the 2-bit version shows materially larger benchmark losses.

hackernews · toebee · Nov 23, 13:42 · [Discussion](https://news.ycombinator.com/item?id=50611402)

**「Quantization and the BF16 baseline」** BF16 serves as the higher-precision reference against which NariQ’s 3-bit, 2.5-bit, and 2-bit GGUF variants are compared; lower bit widths reduce storage and memory requirements but can discard information needed for accuracy. The releases currently require nari-labs’ custom llama.cpp fork rather than the standard runtime, which is a prerequisite for reproducing the reported results.

**「Lower-memory local inference」** NariQ’s roughly 10 GB releases make Qwen3.8-27B substantially more practical for local inference, with the paper reporting BF16-level performance for the 3.0- and 2.5-bit variants on DeepSWE and Terminal-Bench. However, users need the custom \`nari-labs/nari-llama.cpp\` fork rather than stock llama.cpp, and the supplied results show that the 2-bit build can degrade materially—for example, DeepSWE falls from 41.0 at 3 bit to 28.6—so users should test their own workloads and consider 2.5 or 3 bit.

**「Benchmark validity and Mac performance」** rao-v welcomed the testing across multiple long-horizon task types but remained wary that compute-heavy quantization-aware training can overfit benchmarks; WithinReason argued that harness differences, rather than model quality, explain most of the gains. jedbrooke reported decoding at about 3.8 tokens per second for the 3.0-bpw file and 4.9 tokens per second for 2.0 bpw on an 18 GB M3 Pro, while asking whether the model could fit on a 16 GB Mac; other commenters questioned what information lower-bit quantization actually discards.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.26157">NariQ : Sub-3-Bit Quantization for Long-Horizon Agentic Tasks</a></li>
<li><a href="https://arxiv.org/html/2611.26157v1">NariQ : Sub-3-Bit Quantization for Long-Horizon Agentic Tasks</a></li>

</ul>
</details>

**Tags**: `#LLM quantization`, `#Qwen3.8-27B`, `#local inference`, `#GGUF`, `#llama.cpp`

---

<a id="item-tech-news-7"></a>
### [Stalwart Claims Drop-in Compatibility with Microsoft Exchange](https://stalw.art/blog/microsoft-exchange-replacement/) ⭐️ 7.0/10

Stalwart announced that its mail server is now a “drop-in replacement” for Microsoft Exchange, aimed at organizations seeking to self-host email and reduce Exchange licensing and migration barriers. The supplied material does not specify the supported Exchange versions, protocols, client matrix, migration procedure, or compatibility-test results, so the breadth of the claim remains unverified. Practical replacement depends on reliable Outlook and other client support, operational requirements, and regulatory compliance.

hackernews · shaunpud · Nov 23, 22:32 · [Discussion](https://news.ycombinator.com/item?id=50620349)

**「Background」** The key prerequisite is that Outlook and other Exchange-era clients do not talk plain IMAP: they rely on Microsoft&\#x27;s proprietary stack — MAPI over HTTP, Exchange Web Services, ActiveSync and Autodiscover — so an alternative server can only be an Exchange substitute if it answers those protocols. According to Stalwart&\#x27;s own announcement, version 1.2.0 is the release in which the open-source mail server added exactly those four protocols, letting Outlook, Apple Mail and mobile devices connect to it as they would to an Exchange server; the vendor&\#x27;s own framing is therefore what underpins the &quot;drop-in replacement&quot; claim, rather than an independently audited compatibility certification.

**「Operational Impact」** Administrators evaluating a move away from on-premises Exchange now have Stalwart as a possible alternative, but should test their required Outlook and mail-client workflows before treating “drop-in” as equivalent functionality. Migration planning must also account for archival obligations and the proprietary protocols the replacement continues to support.

**「Community Caveats」** Commenters challenged the “drop-in” label: hobo123 asked how Outlook users would work if Outlook drops on-premises Exchange support, while traceroute66 cited Outlook’s IMAP changes and the wider Microsoft ecosystem as reasons the promise may be oversold. Commenter rmoriz said Stalwart’s regular and OSS plans lack the immutable 10-year archiving capability required by Germany’s GoBD rules, while andreashaerter argued that supporting MAPI and similar proprietary protocols preserves lock-in; these are community assertions and opinions rather than independently verified findings.

<details><summary>References</summary>
<ul>
<li><a href="https://stalw.art/blog/microsoft-exchange-replacement/">Stalwart is now a drop-in replacement for Microsoft Exchange</a></li>

</ul>
</details>

**Tags**: `#Stalwart`, `#Microsoft Exchange`, `#email interoperability`, `#self-hosted email`

---

<a id="item-tech-news-8"></a>
### [New York Restricts Car Subscription and Post-Purchase Fees](https://www.governor.ny.gov/news/money-your-pockets-governor-hochul-signs-bill-restricting-exploitative-vehicle-subscription) ⭐️ 7.0/10

New York Gov. Kathy Hochul has signed legislation restricting automakers’ subscription and post-purchase fees for cars. Reported exemptions preserve charges for navigation updates, infotainment, satellite radio, in-vehicle Wi-Fi, telematics, roadside assistance, software-dependent driver assistance or automation, and connected services that require cellular or other data networks to continue operating. A commenter dates the law’s effect to February 27, 2027, but the supplied source material does not independently confirm that date.

hackernews · DeepLogin · Nov 24, 02:27 · [Discussion](https://news.ycombinator.com/item?id=50622774)

**「Background」** Understanding the change requires distinguishing recurring car-subscription or post-purchase fees from payments for connected-car functions such as navigation updates, infotainment, satellite radio, in-vehicle Wi-Fi, telematics, roadside assistance, and software-dependent driver assistance or automation. The reported exemptions for these networked or software-dependent features mean the policy may restrict fees for some vehicle amenities without reaching services that require continued cellular or data-network operation.

**「Industry impact」** Automakers and dealerships offering car subscriptions or post-purchase features in New York will need to review each charge against the new restrictions and the exemptions for software-dependent and connected services, including driver assistance, automation, and telematics. This constrains monetization of covered fees without banning all connected-car subscriptions, making feature-by-feature pricing and compliance review necessary before implementation.

**「Community Discussion」** One commenter argues that the broad exemptions largely spare SiriusXM and Tesla’s enhanced cruise-control features, while another suggests the law is intended to protect dealerships’ share of post-purchase revenue. A third commenter warns that the automation and connected-service carve-outs could invite new fees, such as requiring cellular connectivity for otherwise ordinary features.

**Tags**: `#connected cars`, `#automotive software`, `#technology regulation`, `#subscription fees`

---

<a id="item-tech-news-9"></a>
### [ChatGPT Rolls Out GPT-6.2 Sol to Paid Tiers](https://x.com/ChatGPT/status/2124942186425069836) ⭐️ 7.0/10

ChatGPT’s official account announced on November 23 that GPT-6.2 Sol had launched in the Chat tab and begun rolling out to Plus, Pro, Business, and Enterprise users. OpenAI claims the model handles complex instructions better, recognizes finer details in photos, narrows online-search results using criteria such as price or location, and more appropriately offers follow-up suggestions. These improvements are vendor claims; the announcement provides no benchmarks, implementation details, or independent verification.

telegram · zaihuapd · Nov 24, 00:44

**「Background」** The announcement presents GPT-6.2 Sol as a model update within ChatGPT’s existing Chat interface and paid subscription tiers, rather than a separate product launch. Because no predecessor comparison, benchmarks, implementation details, or independent validation were provided, the magnitude of its differences from earlier ChatGPT models remains unquantified.

**「What the GPT-6.2 Sol rollout means for paid ChatGPT users」** Paid ChatGPT accounts — Plus, Pro, Business and Enterprise — begin receiving GPT-6.2 Sol in the Chat tab as of Nov 23, so everyday conversations, photo Q&amp;A and live web lookups on those tiers run on the new model, while the announcement as relayed names only these paid tiers and states nothing about free-tier access or timing. For users who rely on ChatGPT as a general-purpose assistant for tasks such as reading text and signs in photos, narrowing shopping results by price or location, or setting up proactive follow-ups like price-drop reminders, the claimed changes sit directly in those workflows, and Business/Enterprise teams should re-test image and search prompts after the switch because output on them may differ from the previous default. The only evidence for those improvements is OpenAI&\#x27;s own release description — no benchmark, side-by-side comparison, or third-party test was supplied — so teams that depend on stable prior-model output should validate behavior rather than assume the new model is uniformly better.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ChatGPT">ChatGPT - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#ChatGPT`, `#GPT-6.2`, `#model rollout`, `#multimodal AI`

---

<a id="item-tech-news-10"></a>
### [Huawei reports HarmonyOS 5–7 exceed 100 million devices](https://www.xinhuanet.com/20261124/68842538167d4e59a875056d5eb885ad/c.html) ⭐️ 7.0/10

Huawei announced that the number of phones, tablets, and computers running HarmonyOS 5, 6, or 7 has surpassed 100 million. The company said the ecosystem offers more than 460,000 applications and services and has registered over 12 million developers; separately, open-source HarmonyOS has attracted more than 14,000 contributors and produced over 120 industry distributions. The announcement did not explain its device-count methodology or provide independent validation, leaving the milestone as a company-reported figure.

telegram · zaihuapd · Nov 24, 01:46

**「Background」** Huawei first released HarmonyOS in 2019 and introduced the native version of the operating system in October 2024. The device milestone reported in November 2026 follows more than two years of expansion of that native platform across phones, tablets, and computers.

**「Developer reach and compatibility」** For app and service developers, Huawei&\#x27;s reported base of more than 100 million HarmonyOS 5, 6, and 7 phones, tablets, and PCs creates a larger distribution target, with over 460,000 apps and services available. Teams should validate support across those OS versions and not interpret the combined figure as 460,000 standalone native apps; the milestone is a company-reported count without an independent adoption audit or detailed methodology.

<details><summary>References</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=_5gPa5blq9s">HarmonyOS Hits 100 Million Devices – What’s Next for... - YouTube</a></li>
<li><a href="https://forgeeks.dev/harmonyos-100-million-devices/">Huawei says HarmonyOS will pass 100 million devices by 2026</a></li>

</ul>
</details>

**Tags**: `#HarmonyOS`, `#operating systems`, `#open source`, `#device ecosystem`, `#Huawei`

---

<a id="item-tech-news-11"></a>
### [Shenzhou-24 Targets Nov. 25 Launch with Pakistani Astronaut](https://www.news.cn/20261124/3b116eb35c404cd7b897b23a50099b5b/c.html) ⭐️ 7.0/10

China’s crewed spaceflight program announced that Shenzhou-24 is targeting an 8:18 a.m. launch on Nov. 25, 2026, from Jiuquan, carrying Chinese astronauts Tang Hongbo and Wu Yi and Pakistani astronaut Muhammad Jishan Ali \(穆罕默德·齐尚·阿里\). It would be the first Chinese crewed mission with a foreign astronaut, with Ali becoming the first foreign astronaut to visit Tiangong and Tang Hongbo serving as commander. The spacecraft is planned to use a 3.5-hour autonomous fast rendezvous-and-docking procedure with the Tianhe core module’s forward port, and the report says Ali will return aboard Shenzhou-23 with Zhang Zhiyuan and Li Jiaying; these details remain pre-launch plans rather than confirmed flight results.

telegram · zaihuapd · Nov 24, 04:08

**「Background」** Shenzhou 24 forms part of Tiangong’s resident-crew rotation: accompanying coverage says Shenzhou 23 astronaut Zhu Yangzhu will remain in orbit for a one-year residence experiment during the Shenzhou 24 period. The announced commander, Tang Hongbo, previously flew on Shenzhou 12 and Shenzhou 17.

**「Operational Impact」** The station program’s operational plan must accommodate the first foreign astronaut in a Chinese crewed mission while fitting Shenzhou-24 into the specified 3.5-hour autonomous docking sequence at Tianhe’s forward port. Until the mission is flown, stakeholders should treat the launch date, docking procedure and return assignment as announced targets, not verified outcomes.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-cn/%E6%B1%A4%E6%B4%AA%E6%B3%A2">汤 洪 波 - 维基百科， 自 由的百科全书</a></li>
<li><a href="https://www.guancha.cn/ZhengZhi/2026_11_24_909706.shtml">“天宫”将迎来首位外籍航天员，朱杨柱执行一年期在轨驻留试验任务</a></li>

</ul>
</details>

**Tags**: `#载人航天`, `#神舟二十四号`, `#国际合作`, `#自主交会对接`, `#巴基斯坦航天员`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Day-0 vLLM Support for ERNIE 5.5 Flash Preview](https://vllm.ai/blog/2026-11-24-ernie-5-5-flash-preview) ⭐️ 8.0/10

rss · vLLM Blog · Nov 24, 00:00

**「Background」** The post reports a day-0 vLLM deployment of ERNIE 5.5 Flash Preview, a thinking, tool-using sparse mixture-of-experts model whose 1M-token context makes inference cost across activated compute, KV-cache footprint, and long-context indexing the central engineering constraint.

**「Solution」** ERNIE 5.5 Flash has 280B total parameters but activates 14B per token across 43 layers, combining 37 HCA and six MLA-DSA layers, 512 routed experts using top-10 selection plus a shared expert, MXFP4 W4A8 expert weights, and FP8 for other weights. Because its new attention and MoE structures would otherwise create many intermediate tensors, the teams wrote fused kernels that precompute fixed weights and collapse router GEMMs, piecewise output activation, gating, normalization, RoPE, cache writes, and other stages; the authors report per-kernel gains of 1.55×–6.53× alongside fewer memory round trips and launches. FlashIndexer adds a token-conditioned lightweight head router, distilled against full DSA selections, plus threshold pre-filtering before top-2048 selection; the authors measure a 1.4× indexer speedup at 1M context without changing downstream sparse attention. Post-training aligns fake quantization exactly with inference for W4A8 weights, while a three-layer DSpark draft model proposes up to seven tokens per step; after staged training and on-policy distillation, the vendors report mean acceptance length above 4.0 on coding and agent workloads. Serving uses the official vllm==0.32.0 wheel plus an auto-discovered vLLM-ERNIE plugin for model code and kernels, while parallelism, Mooncake-based prefill-decode disaggregation, CPU KV offload, speculative decoding, and the OpenAI-compatible server remain in upstream vLLM, with no fork or model-specific image required. However, the post provides no reproducible benchmark setup, ablations, or accuracy measurements, leaving its performance and “lossless” claims vendor-reported.

**「Takeaway」** The authors’ central argument is that architecture-aware fusion, sparse-index routing, quantization-aware training, and speculative decoding can make an unusually large MoE practical in vLLM, while a plugin keeps model-specific engineering separate from the upstream serving stack.

**Tags**: `#vLLM plugins`, `#sparse attention`, `#mixture-of-experts inference`, `#GPU kernel fusion`, `#speculative decoding`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Nvidia restores Jensen Huang as CEO, lifting U.S. stocks](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo-market-rally.html) ⭐️ 8.0/10

Nvidia reinstated Jensen Huang as CEO, and major U.S. equity indexes surged Monday after the S&amp;P 500 fell more than 9% from the Nov. 12 departure announcement through Friday; strategists remain divided on whether the relief rally marks a lasting bottom.

rss · CNBC Finance · Nov 23, 18:00

**「Background」** The sell-off began amid concerns about AI data-center financing, approvals after the midterm elections and whether hyperscaler capital spending had peaked, then accelerated after Huang&\#x27;s Nov. 12 departure.

**「Impact」** Nvidia and AI-linked stocks received a short-term lift as Huang&\#x27;s return reduced leadership uncertainty, although doubts about the pace of AI infrastructure spending remained.

**Tags**: `#Nvidia`, `#Jensen Huang`, `#U.S. equities`, `#AI trade`, `#market correction`

---

<a id="item-finance-news-2"></a>
### [Anthropic IPO selloff clouds Chinese AI listing plans](https://www.bloomberg.com/news/articles/2026-11-23/china-s-next-ai-deals-clouded-by-selloff-after-anthropic-ipo) ⭐️ 7.0/10

Bloomberg reports that DeepSeek, Moonshot AI and StepFun are preparing or considering share sales, but a technology-stock selloff following Anthropic’s record $119.5 billion IPO has clouded their listing plans. Chinese technology stocks have lost a combined $1.7 trillion since late June, with the IPO described as the selloff’s trigger.

telegram · zaihuapd · Nov 23, 09:31

**「Background」** DeepSeek, Moonshot AI and StepFun are Anthropic competitors weighing or preparing share sales amid a broader Chinese AI IPO push driven by investor appetite, model advances and supportive government policies; StepFun was reported in February 2026 to be seeking a Hong Kong Stock Exchange listing.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/StepFun">StepFun - Wikipedia</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-23/china-s-next-ai-deals-clouded-by-selloff-after-anthropic-ipo">China ’s Next AI Deals Clouded by Selloff After Anthropic IPO</a></li>
<li><a href="https://www.outlookbusiness.com/deeptech/deepseek-moonshot-gigaai-why-chinas-ai-startups-are-rushing-for-ipo">DeepSeek , Moonshot , GigaAI: Why China &#x27;s AI Startups Are Rushing...</a></li>

</ul>
</details>

**Tags**: `#Anthropic IPO`, `#Chinese tech stocks`, `#AI listings`, `#DeepSeek`, `#Moonshot AI`

---