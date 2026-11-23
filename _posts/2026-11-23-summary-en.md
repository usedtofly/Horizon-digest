---
layout: default
title: "Horizon Summary: 2026-11-23 (EN)"
date: 2026-11-23
lang: en
---

> From 35 items, 9 important content pieces were selected

---

**Technology News**
1. [XNU Linux Targets OS X GUI Userspace on Linux](#item-tech-news-1) ⭐️ 7.0/10
2. [OpenAI Links Perplexity to Model Intelligence](#item-tech-news-2) ⭐️ 7.0/10
3. [GL.iNet Issues November 2026 Security Notice](#item-tech-news-3) ⭐️ 7.0/10
4. [Windows Server 2028 reportedly drops default WoW64 support](#item-tech-news-4) ⭐️ 7.0/10

**Technology Blog**
1. [Flailing Well: Experimentation Under Uncertainty](#item-tech-blog-1) ⭐️ 6.0/10
2. [Reading OpenAI’s Perplexity Graph](#item-tech-blog-2) ⭐️ 6.0/10

**Financial News**
1. [Asian markets adjust trading rules after U.S. tech selloff](#item-finance-news-1) ⭐️ 8.0/10
2. [Super El Niño and a 49 million hunger forecast](#item-finance-news-2) ⭐️ 7.0/10
3. [Ant Group Leads Simplexity Robotics Funding Round](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [XNU Linux Targets OS X GUI Userspace on Linux](https://github.com/AFK-surf/xnulinux) ⭐️ 7.0/10

The XNU Linux repository presents an experimental effort to run the full OS X GUI userspace on Linux, aimed at compatibility and systems-engineering experimentation rather than a demonstrated general-purpose desktop. The available material identifies no release, supported macOS version, required hardware, kernel changes, or performance results, leaving practical usability unverified and establishing no near-term availability.

hackernews · mmastrac · Nov 23, 03:49 · [Discussion](https://news.ycombinator.com/item?id=50607261)

**「What XNU Is」** XNU \(“X is Not Unix”\) is Apple’s hybrid kernel, combining the Mach kernel with components from FreeBSD and the IOKit C++ API for drivers. XNU Linux builds on that foundation to run macOS userspace alongside Linux on Apple Silicon through kernel and graphics bridging.

**「Hardware and licensing constrain adoption」** For developers evaluating the project as a desktop replacement, the immediate limitation is portability: one participant&\#x27;s hands-on assessment says it still requires Apple hardware, so it should be treated as an experimental route rather than a way to run the OS X GUI on ordinary Linux PCs. Distribution also requires care because a relevant project issue records that Apple-derived code under the APSL is GPL-incompatible, requiring integrators to preserve licensing separation instead of assuming the code can be merged into GPL-licensed components.

**「Community Questions the Approach」** One commenter argues that macOS applications’ dependence on version-matched system libraries could allow the userspace to run above Linux with little or no kernel work. Others question the approach: one says the project still needs Apple hardware and favors improving GNUstep, while another asks whether people actually want the macOS userspace; a separate commenter raises locked-down Apple hardware as a potential future barrier.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/apple-opensource/xnu/blob/master/README.md">xnu/README.md at master · apple-opensource/xnu · GitHub</a></li>
<li><a href="https://news.lavx.hu/article/xnulinux-loads-macos-kernel-into-linux-on-apple-silicon">xnulinux Loads macOS Kernel Into Linux on Apple Silicon</a></li>
<li>Code from Apple under the APSL is incompatible with the GPL · Issue #542 - GitHub</li>

</ul>
</details>

**Tags**: `#XNU`, `#Linux`, `#OS X userspace`, `#operating-system compatibility`, `#systems engineering`

---

<a id="item-tech-news-2"></a>
### [OpenAI Links Perplexity to Model Intelligence](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI published an essay arguing that improving language models’ ability to predict and compress data, measured through perplexity, can provide a simple indicator of advances in intelligence and reasoning. The proposal connects next-token prediction, compression, and cross-entropy, but it remains an analytical perspective rather than a shipped model, benchmark release, or independently validated measure of reasoning.

hackernews · acossta · Nov 22, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50601525)

**「Background」** Perplexity measures how surprising a model finds the tokens it must predict; lower values indicate more accurate next-token predictions, and the logarithm of perplexity corresponds to cross-entropy loss. OpenAI’s essay builds on this metric to argue for greater transparency into pretraining progress and for using shared evaluation data to compare models and inform common safety standards.

**「A Cross-Vendor Perplexity Baseline」** Microsoft is already using OpenAI’s proposed evaluation: Mustafa Suleyman reports that MAI-2 Base scored 0.819 log-perplexity on OpenAI’s held-out set, which he says places it in the same ballpark as the GPT-5.6 Sol base model. This gives developers a concrete cross-vendor baseline for comparing pretraining progress, although comparisons require the same evaluation set and should not replace task-specific testing of post-trained systems.

**「Community Discussion」** Commenters defined perplexity as next-token surprise and connected prediction efficiency with compression and learned world models; one linked that view to a 2008 paper. Another welcomed the simple benchmark after expecting cross-entropy to become less important with reinforcement learning, while a separate commenter claimed Microsoft had reported an MAI-2 Base log-perplexity of 0.819 on OpenAI’s held-out set, a figure not independently verified here.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence - OpenAI</a></li>
<li>Mustafa Suleyman on X: &quot;We fully support OpenAI&#x27;s transparency initiative. Thanks to ...</li>

</ul>
</details>

**Tags**: `#language-model evaluation`, `#perplexity`, `#AI reasoning`, `#cross-entropy`

---

<a id="item-tech-news-3"></a>
### [GL.iNet Issues November 2026 Security Notice](https://www.gl-inet.com/en-us/blogs/blog/glinet-security-notice-2026-11-20) ⭐️ 7.0/10

GL.iNet issued a security notice dated November 20, 2026, amid discussion of possible malware or compromise involving some of its network devices. The supplied excerpt does not identify affected models, the attack method, severity, or whether any particular device was confirmed compromised, so the incident&\#x27;s scope remains unestablished. Because no specific remediation steps are present in the supplied material, users should consult the original advisory before changing firmware, credentials, or cloud-access settings.

hackernews · gregsadetsky · Nov 22, 23:06 · [Discussion](https://news.ycombinator.com/item?id=50604988)

**「Firmware Choice and Compromise Context」** Commenters say many GL.iNet routers support OpenWrt-based replacement firmware, so a possible mitigation involving firmware and cloud access cannot be assumed to apply to every GL.iNet product; they specifically note that KVMs are not covered by that workaround. A linked forum claim that the devices may have been compromised since at least last year is an unverified lead rather than confirmation, and the supplied material does not identify affected models, versions, or the incident&\#x27;s scope.

**「Update affected GL.iNet firmware」** Users of the GoodCloud/KVM routers covered by the notice should install the latest stable security firmware for their exact model promptly, even if the notice’s checks show no signs of infection. GL.iNet says this update removes the malware identified in the incident without requiring a factory reset; users should select firmware by model rather than assume compatibility across devices.

**「Community Reaction」** One commenter praised GL.iNet for providing guidance in the user&\#x27;s own language, while others recommended disabling cloud connectivity or using OpenWrt where supported. Another commenter alleged that the compromise may have extended back at least a year, but that allegation is not independently verified by the supplied material.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gl-inet.com/blogs/blog/glinet-security-notice-2026-11-20">GL.iNet Security Notice 2026-11-20</a></li>
<li><a href="https://forum.gl-inet.com/t/2026-11-20-gl-inet-security-notice-goodcloud-kvm-routers/73056">2026-11-20: GL.iNet Security Notice - GoodCloud / KVM ...</a></li>

</ul>
</details>

**Tags**: `#network-device-security`, `#router-firmware`, `#IoT-security`, `#OpenWrt`

---

<a id="item-tech-news-4"></a>
### [Windows Server 2028 reportedly drops default WoW64 support](https://www.windowslatest.com/2026/11/23/32-bit-apps-days-are-numbered-as-microsoft-strips-support-bit-by-bit-starting-with-windows-server-2028-but-windows-11-is-safe-for-now/) ⭐️ 7.0/10

Microsoft plans to omit the WoW64 compatibility subsystem by default in Windows Server 2028, preventing 32-bit applications from running out of the box. Administrators can restore WoW64 as an optional feature, generally through PowerShell or DISM on Server Core; Microsoft says the default removal is intended to reduce the attack surface and block 32-bit malware. Windows Server 2028 is planned for fall 2027 alongside Windows 11 27H2, while Windows 11 will retain WoW64 for now and Microsoft has announced no removal plan for it.

telegram · zaihuapd · Nov 23, 03:03

**「Background」** WoW64 is the compatibility subsystem that allows 64-bit Windows to execute 32-bit x86 applications, so making it an optional Feature on Demand changes the baseline for software that still requires 32-bit binaries rather than eliminating support outright. Microsoft announced Windows Server 2028 as its next Windows Server release at Ignite 2026; the preview also emphasizes a hardened Server Core configuration and a new security baseline, providing context for the reported optional-WoW64 approach.

**「Deployment impact」** Under Microsoft’s announced plan, organizations running 32-bit applications on Windows Server 2028 will need to install the WoW64 on-demand feature before deployment or migrate those applications, because they will not run on a default installation. Server Core administrators should plan to add WoW64 with PowerShell or DISM and validate any dependent services or legacy components.

<details><summary>References</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/windows-server/get-started/whats-new-windows-server-2028">Windows Server 2028 Preview: New features | Microsoft Learn</a></li>
<li><a href="https://techcommunity.microsoft.com/discussions/windowsserverinsiders/windows-server-2028-preview-resources---windows-server-vnext/4574213">Windows Server 2028 preview resources - Windows Server vNext</a></li>
<li><a href="https://techcommunity.microsoft.com/blog/windowsservernewsandbestpractices/windows-server-2028-a-trusted-foundation-for-an-evolving-enterprise/4574112">Windows Server 2028: A trusted foundation for an evolving ...</a></li>
<li><a href="https://thecommunity.ru/microsoft/windows/server/12123-windows-server-2028-po-umolchaniju-ne-budet-podderzhivat-32-bitnye-prilozhenija.html">Windows Server 2028 по умолчанию не будет поддерживать...</a></li>

</ul>
</details>

**Tags**: `#Windows Server 2028`, `#WoW64`, `#32位应用兼容性`, `#按需功能`, `#遗留软件迁移`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Flailing Well: Experimentation Under Uncertainty](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 23, 00:00

**「Background」** Sean Goedecke argues that when requirements or possible solutions are unclear, waiting for complete understanding is typically less effective than rapidly testing options. The hard part is avoiding “flailing badly”: producing weak ideas, harming credibility, overcommitting to one plan, or missing feedback that shows an effort is failing.

**「Solution」** His proposed method is to try many things, watch feedback closely, and ruthlessly abandon options that are not producing positive signals; feedback can come both from knowledgeable colleagues and from reality, such as user metrics or latency improvements. Product flailing means testing several plausible features around a central idea until one gains traction, illustrated by Goedecke’s experience at GitHub Models, where failed experiments coexisted with the AI-inference-from-GitHub-Actions-token idea that seeded “Continuous AI.” Engineering flailing means making speculative changes to tangled, large, or fast-changing systems, observing whether they help, then digging into the winners; AI agents, he notes, can help produce multiple refactors for comparison. Organizational flailing applies when the problem is interpersonal or structural rather than technical: automate small pieces of work, take on tasks, or propose broader plans, while staying especially alert because continuing with a failing effort can redirect anger toward the engineer. He frames the discomfort of repeated failure as a psychological barrier, arguing that sensitivity to feedback and willingness to drop failing plans make experimentation useful rather than reckless.

**「Takeaway」** Goedecke’s thesis is that deliberate, feedback-driven “flailing” is a practical way to create information and find traction under uncertainty, provided teams act on negative feedback and avoid overcommitting to any one attempt.

**Tags**: `#experimentation`, `#feedback loops`, `#technical decision-making`, `#product development`, `#engineering management`

---

<a id="item-tech-blog-2"></a>
### [Reading OpenAI’s Perplexity Graph](https://seangoedecke.com/notes-on-openais-perplexity-reveal/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 23, 00:00

**「Background」** OpenAI’s graph plots perplexity over time across its released models, offering unusual visibility into a frontier lab’s training; but perplexity measures held-out-text prediction on a chosen dataset, making it an imperfect proxy for deployed-model capability.

**「Solution」** Goedecke says the curve is still useful if pretraining creates capabilities and reinforcement learning mainly elicits them, though it says nothing about whether post-training successfully elicits them or uses chain-of-thought effectively. He sees few shared bases, weighing against rumors that GPT-4o and GPT-4.1 seeded many models, and notes that 4.1 and o3 share one despite sharply different usefulness. GPT-4.5’s similar perplexity to GPT-5.3-Codex despite being less useful could mean OpenAI stopped scaling pretrained models or hit a wall, but the graph cannot decide. The acceleration after GPT-5.2, he argues, contradicts the claim that frontier labs have abandoned pretraining for RL. His experience diverges from the curve: GPT-3.5 to GPT-4 was obvious, later gains felt uneven, and o3 and GPT-5.3-Codex were the biggest leaps; RL quality, chain-of-thought use, and sycophancy are invisible to this metric. For alignment, he welcomes disclosure but says common thresholds require dataset details, and researchers need metrics for unreleased models to detect sudden alarming gains.

**「Takeaway」** The author’s main point is that OpenAI’s pretrained foundations still improved rapidly, while the same graph demonstrates why perplexity cannot by itself explain post-trained model behavior or provide meaningful cross-lab comparison.

**Tags**: `#language-model evaluation`, `#perplexity`, `#pretraining and post-training`, `#AI transparency`, `#model scaling`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Asian markets adjust trading rules after U.S. tech selloff](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

The report says U.S. technology stocks fell sharply on Friday, with the Nasdaq down 5.28% and the Philadelphia Semiconductor Index down nearly 11%. Asian authorities responded: mainland China cut the minimum margin-financing requirement to 80%, South Korea eased daily buyback-order limits for three months from Nov. 24, and Taiwan barred below-market short selling and raised its securities-lending margin from 130% to 150% from Nov. 23.

telegram · zaihuapd · Nov 22, 13:24

**「Background」** The Asian policy responses followed a severe U.S. technology sell-off: the Nasdaq 100 fell 5.6% in the latest session and 10.4% over the week, its worst week in more than six years, according to Guancha.

**「Impact」** The reported rule changes directly alter trading conditions for Asian investors: mainland China cut the minimum margin-borrowing collateral ratio to 80%, South Korea temporarily eased daily buyback-order limits from Nov. 24, and Taiwan raised the short-selling margin requirement from 130% to 150% and banned below-market short selling from Nov. 23.

<details><summary>References</summary>
<ul>
<li><a href="https://www.guancha.cn/GuoJi%C2%B7ZhanLue/2026_11_21_909399.shtml">AI恐慌爆发，华尔街震荡， 美 国 科 技 股 跌 入熊市</a></li>

</ul>
</details>

**Tags**: `#美股科技股`, `#半导体市场`, `#亚洲股市`, `#卖空监管`, `#市场稳定措施`

---

<a id="item-finance-news-2"></a>
### [Super El Niño and a 49 million hunger forecast](https://www.wired.com/story/how-this-years-super-el-nino-will-worsen-global-hunger/) ⭐️ 7.0/10

Berkeley Earth climate scientist Zeke Hausfather said the central Pacific warming anomaly used to gauge El Niño strength reached 3.5°C in October, exceeding the previous record of about 2.75°C, and he forecast a roughly 4°C peak in early winter. The World Food Programme warned in August that the event could push 49 million more people into acute food insecurity by the end of 2027, raising the projected total to 274 million, while global aid funding in 2025 was 30% below its 2022 peak.

telegram · zaihuapd · Nov 22, 14:09

**「Background」** El Niño can alter rainfall and heat in farming regions; in Guatemala, July rainfall was as much as 85% below average, delaying planting and disrupting crops. In August, the World Food Programme projected that this event could push 49 million more people into acute food insecurity—meaning an immediate risk of not having enough food—by the end of 2027, bringing the total to 274 million.

**「Impact」** If the forecast super El Niño intensifies drought, an additional 49 million people could face acute food insecurity by the end of 2027, while global aid funding—30% below its 2022 peak in 2025—is limiting food-assistance capacity in vulnerable countries such as Somalia.

<details><summary>References</summary>
<ul>
<li><a href="https://e360.yale.edu/features/super-el-nino-agriculture">How This Year&#x27;s Super El Niño Will Worsen Global Hunger - Yale E360</a></li>
<li><a href="https://www.nytimes.com/2026/08/12/climate/el-nino-early-onset-effects.html">Effects of Record -Breaking El Niño Are Happening on 3 Continents...</a></li>
<li><a href="https://www.wired.com/story/how-this-years-super-el-nino-will-worsen-global-hunger/">How This Year’s Super El Niño Will Worsen Global Hunger | WIRED</a></li>

</ul>
</details>

**Tags**: `#厄尔尼诺`, `#粮食安全`, `#世界粮食计划署`, `#气候冲击`, `#人道主义援助`

---

<a id="item-finance-news-3"></a>
### [Ant Group Leads Simplexity Robotics Funding Round](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 7.0/10

Ant Group led Simplexity Robotics’ $100 million pre-Series A funding round, giving the Chinese embodied-AI company a $1.6 billion post-money valuation, chairman and co-founder Wang Kai told Bloomberg. Existing investors Alibaba, Tencent, HongShan and BlueRun Ventures also participated, while Bloomberg reported that Chinese humanoid robot makers account for about 97% of global shipments.

telegram · zaihuapd · Nov 23, 02:02

**「Background」** Simplexity Robotics was founded in Hangzhou in July 2025 by a core team from Li Auto; by March 2026, it had completed five funding rounds totaling RMB 2 billion and reached a post-money valuation above $1 billion.

**Tags**: `#具身智能`, `#融资`, `#蚂蚁集团`, `#人形机器人`, `#中国科技`

---