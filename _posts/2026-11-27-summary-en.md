---
layout: default
title: "Horizon Summary: 2026-11-27 (EN)"
date: 2026-11-27
lang: en
---

> From 41 items, 8 important content pieces were selected

---

**Technology News**
1. [Neuralink Receives FDA Clearance for ALS Brain-Interface Trial](#item-tech-news-1) ⭐️ 8.0/10
2. [AMD-Specific llama.cpp Fork Targets gfx906 LLM Inference](#item-tech-news-2) ⭐️ 7.0/10
3. [Google’s MCP Plan Leaves Gmail Sending Unsupported](#item-tech-news-3) ⭐️ 7.0/10
4. [Nvidia reportedly pauses Southeast Asian AI-server shipments amid tighter export controls](#item-tech-news-4) ⭐️ 7.0/10
5. [ASML CEO Warns China Embargo Could Spur Domestic Lithography](#item-tech-news-5) ⭐️ 7.0/10

**Technology Blog**
1. [Who Decides Whether Writing Is AI?](#item-tech-blog-1) ⭐️ 5.0/10

**Financial News**
1. [Semiconductor exports overtake oil and gas](#item-finance-news-1) ⭐️ 8.0/10
2. [Netherlands Opposes Proposed U.S. Curbs on ASML China Sales](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Neuralink Receives FDA Clearance for ALS Brain-Interface Trial](https://www.bloomberg.com/news/articles/2026-11-25/neuralink-gets-clearance-for-brain-implant-trial-in-als-patients?srnd=phx-technology) ⭐️ 8.0/10

Neuralink said it received FDA clearance to begin the LINK pivotal trial in the United States, an implantable brain-computer interface study intended to recruit people with amyotrophic lateral sclerosis \(ALS\) and translate brain signals into computer-control commands. The supplied Bloomberg report says Neuralink has implanted devices in more than 30 paralysis patients worldwide through earlier studies and describes LINK as the first FDA-approved pivotal trial of its kind in the United States. The item does not provide the trial protocol, primary endpoints, enrollment targets, timeline, or underlying FDA documentation, so its claimed U.S. first and the precise regulatory scope cannot be independently confirmed from the supplied material.

telegram · zaihuapd · Nov 26, 07:15

**「Neuralink’s Earlier Trial Path」** Neuralink’s first application to begin human trials was rejected by the FDA in 2022, prompting additional animal testing to address safety concerns before the company’s early human-implant work. LINK is described as building on that work with more than 30 participants; its pivotal designation places it in the later evidence-gathering stage intended to inform a future device-approval application, rather than the earlier safety-validation phase.

**「Practical impact」** Patients with ALS in the United States can now enroll in Neuralink’s LINK pivotal study of an implanted brain-computer interface that translates brain signals into computer-control commands. The trial is intended to generate evidence for a future medical-device marketing application, but the implant remains investigational: FDA clearance to conduct the study is not authorization to sell the device commercially.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Neuralink">Neuralink - Wikipedia</a></li>
<li><a href="https://www.engadget.com/2329008/neuralink-receives-fda-approval-for-brain-implant-trial-in-als-patients/">Neuralink Receives FDA Approval For &#x27;Pivotal&#x27; Brain Implant Trial In.....</a></li>
<li><a href="https://neuralink.com/updates/neuralink-receives-fda-approval-to-launch-link-pivotal-study/">Neuralink Receives FDA Approval to Launch LINK Pivotal Study</a></li>
<li><a href="https://casrai.org/news/neuralink-link-pivotal-trial-als-fda-clearance-2026">Neuralink LINK: First US Pivotal BCI Trial in ALS — CASRAI</a></li>

</ul>
</details>

**Tags**: `#脑机接口`, `#Neuralink`, `#FDA临床试验`, `#渐冻症`, `#医疗器械`

---

<a id="item-tech-news-2"></a>
### [AMD-Specific llama.cpp Fork Targets gfx906 LLM Inference](https://devnull.land/amd-specific-llama-cpp) ⭐️ 7.0/10

An AMD-specific fork of llama.cpp specializes in local LLM inference on gfx906-series accelerators, targeting the high memory bandwidth and large VRAM of that older datacenter hardware. The supplied report does not identify a tagged release or compatible ROCm version and provides no independently reproduced benchmark, so the evidence supports a specialized community optimization rather than a broadly validated product. Related community builds are reported to run quantized 27B models at high throughput and with long context, but those results should not be treated as verified measurements of this fork.

hackernews · julianlam · Nov 26, 17:11 · [Discussion](https://news.ycombinator.com/item?id=50657265)

**「Why AMD gfx906 matters」** The fork targets AMD’s circa-2018 gfx906 datacenter accelerators, which a commenter described as lacking tensor cores and native BF16 support but providing unusually fast HBM2 memory, with 32 GB of VRAM and roughly 1 TB/s of bandwidth. This memory-heavy, lower-compute hardware is the basis for the project’s effort to make large-model inference practical on these AMD GPUs.

**「More deployment options for older AMD GPUs」** For developers running llama.cpp on gfx906 cards such as the Radeon VII, MI50, and MI60, the fork adds gfx906-specific tuning and controllable pipeline parallelism that upstream llama.cpp does not provide, including support for mixed ROCm and Vulkan systems. Users should still validate the exact quantization and multi-GPU configuration: one gfx906 ROCm fork documents missing GPUDirect P2P Row Split support on MI50 and warns that incompatible quantization formats can produce garbled output.

**「Community Discussion」** Commenters argue that gfx906 cards&\#x27; 32 GB HBM2 capacity and roughly 1 TB/s bandwidth can be valuable for LLM inference despite the absence of tensor cores and native bf16. One Radeon R9700 user reports 2,400 tokens/s prefill and 150 tokens/s decode for a 4-bit Qwen3.8-27B, plus three concurrent 200k-context streams entirely in VRAM, while an MI100 user says ROCm tuning and Nvidia-kernel ports doubled or tripled Qwen3.8 performance; these are anecdotal results from related AMD projects, not independent validation of the highlighted fork.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/milpster/gfx906-llama-cpp">GitHub - milpster/gfx906-llama-cpp</a></li>
<li><a href="https://github.com/taobaoww2010-alt/llama-cpp-rocm-gfx906">GitHub - taobaoww2010-alt/llama-cpp-rocm-gfx906: llama.cpp ...</a></li>

</ul>
</details>

**Tags**: `#llama.cpp`, `#AMD GPUs`, `#gfx906`, `#LLM inference`, `#open source`

---

<a id="item-tech-news-3"></a>
### [Google’s MCP Plan Leaves Gmail Sending Unsupported](https://techstackups.com/articles/google-workspace-ai-agents-mcp/) ⭐️ 7.0/10

Google reportedly plans to route AI agents connecting to Google Workspace through Google’s Model Context Protocol \(MCP\) servers rather than alternative access paths. The report highlights a practical limitation of the Gmail MCP server: it cannot send email, restricting agents that need to compose and deliver messages. The supplied account describes an announced policy rather than a shipped, independently verified rollout and provides no effective date or detailed enforcement terms.

hackernews · ritzaco · Nov 26, 09:44 · [Discussion](https://news.ycombinator.com/item?id=50653477)

**「How Workspace MCP servers work」** The Model Context Protocol \(MCP\) is a standardized interface that lets AI agents connect to external services and invoke tools. Google’s hosted Workspace MCP servers expose Gmail, Drive, Calendar, and other services to agents, while sensitive operations such as sending email or sharing files can be gated behind server-driven human approval through MCP form elicitation.

**「Impact on Workspace agent integrations」** Developers connecting agents to Gmail, Calendar, Drive, and other Workspace services must account for server-driven human-in-the-loop approvals: Google’s MCP servers use form elicitation before sensitive actions such as sending email, changing shared calendar events, sharing or trashing files, and accessing shared data. Agents that cannot complete this approval exchange will be unable to perform those operations unattended, so third-party MCP clients should implement elicitation or route supported actions through Google’s hosted Workspace tools.

**「Safety Versus Workarounds」** perdy argued that partner-only access is more likely a business decision because MCP elicitation can pause a tool call for human confirmation, while Schnitz predicted agents would fall back to browser automation, which they considered messy and wasteful. sp1nningaway reported using NeoMutt with SMTP and IMAP for more reliable Gmail-agent access, and physicsguy compared restricted APIs that penalize client-side workarounds; these were individual opinions and experiences rather than independent verification.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.google.com/workspace/guides/configure-mcp-servers">Configure the Google Workspace MCP servers</a></li>
<li><a href="https://developers.google.com/workspace/gmail/api/guides/configure-mcp-server">Configure the Gmail MCP server | Google for Developers</a></li>
<li><a href="https://workspaceupdates.googleblog.com/2026/11/mcp-servers-cli-standardized-usage-tiers-now-available.html">Google Workspace Updates: Simplifying agent access while ...</a></li>
<li><a href="https://developers.google.com/workspace/gmail/api/guides/configure-mcp-server">Configure the Gmail MCP server | Google for Developers</a></li>
<li><a href="https://workspaceupdates.googleblog.com/2026/11/mcp-servers-cli-standardized-usage-tiers-now-available.html">Google Workspace Updates: Simplifying agent access while ...</a></li>

</ul>
</details>

**Tags**: `#Google Workspace`, `#Model Context Protocol`, `#AI agents`, `#Gmail automation`, `#platform lock-in`

---

<a id="item-tech-news-4"></a>
### [Nvidia reportedly pauses Southeast Asian AI-server shipments amid tighter export controls](https://www.ft.com/content/7838a715-07d4-4605-aa60-21f5af2b2370) ⭐️ 7.0/10

Nvidia reportedly asked major manufacturing partners to pause AI-server shipments to Malaysia, Singapore, Thailand, and Indonesia; Dell and Supermicro reportedly told buyers that affected orders could not leave their factories. The Financial Times, citing three people, linked the freeze to new U.S. export controls intended to prevent advanced Nvidia processors from reaching Chinese AI companies through the four countries. The rules require regional cloud-service providers to obtain export licenses within 90 days and verify that customers do not include restricted Chinese entities. It remains unclear whether the shipment pause is temporary.

telegram · zaihuapd · Nov 26, 07:38

**「Export-control context」** The four Southeast Asian countries have served as transshipment hubs for Chinese AI companies seeking Nvidia’s most advanced processors, which cannot be exported directly to mainland China. The U.S. Commerce Department’s new rules require regional cloud providers to obtain export licenses within 90 days and verify that end customers do not include restricted Chinese entities, creating the compliance context for the reported shipment pause.

**「AI-server deployment now depends on export clearance」** Buyers and data-center operators in Malaysia, Singapore, Thailand, and Indonesia now face an export-licensing and end-user screening step before receiving Nvidia-equipped AI servers. Regional cloud providers have 90 days to obtain the required licenses and verify that customers do not include restricted Chinese entities; Dell and Supermicro’s affected orders cannot leave the factory, so operators unable to demonstrate compliance may need to defer deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.zerohedge.com/ai/nvidia-halts-ai-chip-shipments-four-southwest-asian-countries">&quot;Causing Sheer Chaos&quot;: Nvidia Halts AI Chip Shipments ... | ZeroHedge</a></li>
<li><a href="https://www.reuters.com/world/asia-pacific/nvidia-halts-chip-shipments-southeast-asia-ft-reports-2026-11-26/">Nvidia halts server shipments to four Southeast Asian ...</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/nvidia-stops-ai-gpu-shipments-160000782.html?fr=sycsrp_catchall">Nvidia stops AI GPU shipments to Southeast Asia amid ...</a></li>

</ul>
</details>

**Tags**: `#AI accelerators`, `#export controls`, `#Nvidia`, `#AI supply chains`, `#Southeast Asia`

---

<a id="item-tech-news-5"></a>
### [ASML CEO Warns China Embargo Could Spur Domestic Lithography](https://www.semafor.com/article/11/25/2026/asml-makes-the-case-for-selling-chips-to-china) ⭐️ 7.0/10

ASML CEO Christophe Fouquet said on Semafor’s Future Proof podcast that completely blocking chip-equipment sales to China would encourage China to triple investment in domestic lithography, while arguing that controls should protect the most advanced technology rather than exclude China entirely. Fouquet claimed ASML had supplied nearly all lithography equipment sold in China for almost 30 years and that its machines sold there lag the latest process technology by more than a decade. His comments came as the proposed US MATCH Act sought to extend restrictions to immersion DUV systems and maintenance services; the stance is executive advocacy, not a new policy or technical breakthrough.

telegram · zaihuapd · Nov 26, 12:19

**「Export-control context」** ASML is the sole manufacturer of the lithography machines used for leading-edge chips, making restrictions on China’s access to EUV systems a central issue. The MATCH Act remains a proposal to broaden existing US controls from EUV to immersion DUV equipment and maintenance services, rather than an enacted total ban. ASML says its China lithography market share has been close to 100% for nearly 30 years, although the systems it sells there lag its most advanced technology by more than a decade.

**「Procurement and service-continuity risk」** If the proposed MATCH Act is enacted and allies align their rules within its 150-day window, Chinese chipmakers could lose access to sales and servicing for ASML’s older DUV systems that remain legal today. This creates a procurement and service-continuity concern for fabs using those tools, although the restriction is proposed rather than already in force.

<details><summary>References</summary>
<ul>
<li><a href="https://www.semafor.com/article/11/26/2026/dutch-lawmakers-condemn-us-legislation-curbing-chip-exports">Dutch lawmakers condemn US technology curbs | Semafor</a></li>
<li><a href="https://wccftech.com/asml-ceo-warns-total-chip-export-ban-will-backfire-push-china-domestic-rivals/">ASML CEO Warns Total Chip Export Ban Will Backfire ... - Wccftech</a></li>
<li><a href="https://www.trendforce.com/news/2026/08/25/news-u-s-may-push-near-total-asml-china-ban-on-duv-sales-and-servicing-amid-chinas-domestic-lithography-push/">[News] U.S. May Push Near-Total ASML China Ban on DUV Sales ...</a></li>
<li><a href="https://www.thedefensenews.com/US-Pushes-Bill-to-Compel-Netherlands-to-Halt-Remaining-ASML-Machine-Sales-and-Service-to-China/">US Pushes Bill to Compel Netherlands to Halt Remaining ASML ...</a></li>

</ul>
</details>

**Tags**: `#半导体制造`, `#光刻机`, `#出口管制`, `#ASML`, `#芯片供应链`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Who Decides Whether Writing Is AI?](https://seangoedecke.com/who-gets-to-decide-if-something-is-written-by-ai/) ⭐️ 5.0/10

rss · Sean Goedecke · Nov 27, 00:00

**「Background」** AI-content disputes are increasingly tests of authority: who may exclude a writer from a prize, fail a student, or remove work from public discourse? Goedecke argues that hostility to detectors such as Pangram is often less about detection accuracy than about rejecting concentrated technological gatekeeping.

**「Solution」** He acknowledges that Pangram and its third-party tests report false positives and false negatives, even on the same dataset, while treating Pangram as the best available detector. His counterargument is that the alternative—community self-policing—is worse: self-appointed anti-AI readers frequently misread stylistic clues, while ordinary investigation can be defeated by lying, post-hoc drafts, and convincing evidence of a human writing process. Skilled AI writing can leave drafts and contemporaneous conversations, he says, while C2PA and other cryptographic provenance approaches do not provide a plausible attestation path for this problem. He therefore favors using the strongest available detection tools, but argues that if a reader distrusts Pangram’s corporate power, the remedy should be open-source detectors or government-built public platforms rather than inconsistent human judgment. The post provides no independent error-rate analysis, implementation evidence, or substantial treatment of false-positive harms, so the comparative reliability claim remains largely conceptual and anecdotal.

**「Takeaway」** The larger thesis is that opposition to AI detection may often be opposition to technological authority itself; if AI-generated work must be identified, that power should be transparent and publicly accountable rather than left to community consensus.

**Tags**: `#AI detection`, `#content provenance`, `#algorithmic gatekeeping`, `#technology governance`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Semiconductor exports overtake oil and gas](https://www.cnbc.com/2026/11/26/semiconductor-chips-are-the-new-oil-heres-why.html) ⭐️ 8.0/10

Semiconductor export value surpassed oil and gas exports for the first time, according to a Deutsche Bank analysis of International Trade Centre data. On a four-quarter rolling basis, semiconductors reached about $1.61 trillion in the first quarter of 2026 versus $1.53 trillion for oil and gas, and the gap widened in the second quarter as AI demand rose and oil supply was disrupted.

rss · CNBC Finance · Nov 26, 17:52

**「Background」** AI-driven data-center construction has increased demand for chips, while oil and gas exports were hurt by disruptions that cut daily flows through the Strait of Hormuz by nearly 77% from Q4 2025 to Q2 2026. Historically, oil exporters recycled surpluses into U.S. government debt; Deutsche Bank argues Asian chip exporters may increasingly direct earnings toward U.S. technology companies, startups and data centers instead.

**「Impact」** Deutsche Bank analysts say Asian chip-export earnings could increasingly flow into U.S. tech stocks, startups and data centers instead of government bonds, making financial markets more sensitive to technology-sector valuations and potentially raising volatility and debt yields.

<details><summary>References</summary>
<ul>
<li><a href="https://www.dbresearch.com/PROD/IE-PROD/PROD0000000000659135.pdf">Chipping in: how chips have become a huge driver of the dollar</a></li>
<li><a href="https://www.investing.com/news/stock-market-news/how-are-ai-chip-flows-reshaping-dollar-dominance-deutsche-bank-explains-5043246">How are AI chip flows reshaping dollar dominance? Deutsche ...</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#global trade`, `#artificial intelligence`, `#commodity exports`, `#macroeconomics`

---

<a id="item-finance-news-2"></a>
### [Netherlands Opposes Proposed U.S. Curbs on ASML China Sales](https://www.bloomberg.com/news/articles/2026-11-26/netherlands-plans-to-fight-rollout-of-proposed-us-curbs-on-asml) ⭐️ 7.0/10

Dutch trade minister Sjoerd Sjoerdsma said the Netherlands will oppose the proposed MATCH Act, which could allow the U.S. to restrict semiconductor-equipment sales to China unless allied countries tighten export controls. The government is working with the EU, Germany and France to remove the provisions; China accounts for about 20% of ASML’s sales this year.

telegram · zaihuapd · Nov 26, 14:56

**「Background」** Existing U.S. controls already restrict sales to China of ASML’s most advanced chipmaking machines; the proposed MATCH Act could go further by limiting maintenance and support for machines already sold to Chinese chipmakers.

**「Potential business impact」** If enacted, the proposed curbs could limit ASML’s China-bound semiconductor-equipment sales; ASML has guided that China will represent about 20% of its 2026 revenue, creating material exposure while potentially restricting equipment availability for customers in China.

<details><summary>References</summary>
<ul>
<li><a href="https://mrkt30.com/asml-match-act/">Why the MATCH Act Could Be a Real Problem for ASML - MRKT3.0</a></li>
<li><a href="https://keepingupwith.ai/articles/netherlands-opposes-match-act-at-risk-to-asmls-china-business/">Netherlands Opposes MATCH Act at Risk to ASML &#x27;s China Business</a></li>
<li><a href="https://hooooit.com/chips-act-export-controls-global-fab-equipment/">The Quiet Chokehold: How CHIPS Act Export Controls Are... - Hooooit</a></li>
<li><a href="https://www.techpowerup.com/351847/united-states-government-may-restrict-asmls-duv-tool-exports-to-china">United States Government May Restrict ASML &#x27;s DUV Tool Exports to...</a></li>

</ul>
</details>

**Tags**: `#ASML`, `#对华出口管制`, `#MATCH Act`, `#荷兰`, `#半导体设备`

---