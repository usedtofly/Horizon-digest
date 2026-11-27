---
layout: default
title: "Horizon Summary: 2026-11-27 (ZH)"
date: 2026-11-27
lang: zh
---

> 从 41 条内容中筛选出 8 条重要资讯。

---

**科技新闻**
1. [Neuralink 启动渐冻症脑机接口关键试验](#item-tech-news-1) ⭐️ 8.0/10
2. [AMD gfx906 专用 llama.cpp 分支引发推理优化讨论](#item-tech-news-2) ⭐️ 7.0/10
3. [Google 据报要求 Workspace 代理使用 MCP，但 Gmail 不能发信](#item-tech-news-3) ⭐️ 7.0/10
4. [英伟达据报暂停东南亚四国 AI 服务器出货](#item-tech-news-4) ⭐️ 7.0/10
5. [ASML CEO 反对全面限制对华芯片设备出口](#item-tech-news-5) ⭐️ 7.0/10

**科技博客**
1. [谁有权判定作品是否由 AI 写成](#item-tech-blog-1) ⭐️ 5.0/10

**财经新闻**
1. [半导体出口价值首次超过油气](#item-finance-news-1) ⭐️ 8.0/10
2. [荷兰反对美国拟议限制 ASML 对华销售法案](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Neuralink 启动渐冻症脑机接口关键试验](https://www.bloomberg.com/news/articles/2026-11-25/neuralink-gets-clearance-for-brain-implant-trial-in-als-patients?srnd=phx-technology) ⭐️ 8.0/10

Neuralink 宣布获得 FDA 许可，将在美国开展名为“LINK”的渐冻症患者植入式脑机接口关键临床试验，招募对象为渐冻症患者，目标是直接把大脑信号转换为计算机控制指令。报道将其称为“美国首个获批的此类关键试验”，并称试验数据将用于未来申请医疗器械上市许可，但这一“首个”表述尚未得到独立核实。报道还称 Neuralink 此前已在全球为逾 30 名瘫痪患者植入设备，不过目前未提供试验设计、主要终点、时间表或 FDA 原始文件，具体监管范围和试验方案仍不明确。

telegram · zaihuapd · 11月26日 07:15

**「此前的临床与监管基础」** 植入式脑机接口的核心，是把大脑信号转换为计算机可执行的指令；Neuralink 并非从零开始，其在 2022 年首次人体试验申请曾遭 FDA 拒绝，随后补充动物试验以回应安全问题。此次 LINK 试验获批前，Neuralink 称已开展涉及 30 多名参与者的早期植入研究，而该试验被定位为面向重度瘫痪患者（包括渐冻症患者）的美国首个关键性试验。

**「LINK 试验向渐冻症患者开放招募」** Neuralink 宣布获 FDA 许可启动美国首个植入式脑机接口关键试验 LINK，面向渐冻症患者且已开放招募，符合条件的患者可按试验要求寻求参与。对研究参与者和医疗决策者而言，试验由此进入以验证疗效和安全性为核心的关键阶段，并可为未来医疗器械上市申请提供数据；但相关设备仍属于研究性器械，本次许可不代表 Neuralink 已获准常规商业使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Neuralink">Neuralink - Wikipedia</a></li>
<li><a href="https://interestingengineering.com/health/neuralink-fda-approval-link-pivotal-brain-implant-trial">Neuralink gets FDA approval for first pivotal brain implant trial</a></li>
<li><a href="https://www.engadget.com/2329008/neuralink-receives-fda-approval-for-brain-implant-trial-in-als-patients/">Neuralink Receives FDA Approval For &#x27;Pivotal&#x27; Brain Implant Trial In.....</a></li>
<li><a href="https://neuralink.com/updates/neuralink-receives-fda-approval-to-launch-link-pivotal-study/">Neuralink Receives FDA Approval to Launch LINK Pivotal Study</a></li>
<li><a href="https://casrai.org/news/neuralink-link-pivotal-trial-als-fda-clearance-2026">Neuralink LINK: First US Pivotal BCI Trial in ALS — CASRAI</a></li>
<li><a href="https://www.engadget.com/2329008/neuralink-receives-fda-approval-for-brain-implant-trial-in-als-patients/">Neuralink receives FDA approval for &#x27;pivotal&#x27; brain implant ...</a></li>

</ul>
</details>

**标签**: `#脑机接口`, `#Neuralink`, `#FDA临床试验`, `#渐冻症`, `#医疗器械`

---

<a id="item-tech-news-2"></a>
### [AMD gfx906 专用 llama.cpp 分支引发推理优化讨论](https://devnull.land/amd-specific-llama-cpp) ⭐️ 7.0/10

据项目描述，这个专用的 llama.cpp 分支针对 AMD gfx906 加速卡优化大模型推理，主要面向希望利用该架构大显存和高内存带宽运行本地模型的开发者。讨论者称，gfx906 属于约 2018 年的数据中心卡系列，没有 Tensor Core 或原生 BF16，需要依靠软件优化弥补计算能力。现有材料未列出分支版本、改动范围或独立测试，因此不能把社区报告的吞吐量视为已验证的分支性能。

hackernews · julianlam · 11月26日 17:11 · [社区讨论](https://news.ycombinator.com/item?id=50657265)

**「gfx906 的硬件特点」** 该项目针对的是 AMD 约 2018 年的 gfx906 数据中心 GPU 系列；据评论者称，这些显卡没有 Tensor Core 或原生 BF16，但配备 32GB HBM2 显存和约 1TB/s 带宽，优势在于大容量与高带宽，而非峰值计算能力。llama.cpp 可作为多种模型和硬件后端的通用推理框架，但要充分利用这类显卡，仍需针对 AMD 后端调整计算内核；相关讨论中提到的 vicuna.cpp 等实验也采用了移植或重写 GPU kernel 的思路。

**「gfx906 的部署收益与兼容风险」** 对于使用 Radeon VII、MI50、MI60 或 ROCm＋Vulkan 混合配置的用户，该专用分支补足了上游 llama.cpp 尚未提供的 gfx906 调优和可控流水线并行，在模型接近显存上限、需要拆分到不同 GPU 时提供了可行的部署路径。实际部署前仍应验证 P2P 与量化组合：另一份 gfx906/ROCm 实现明确注明 MI50 不支持 GPUDirect P2P Row Split，并警告部分量化格式可能产生乱码，不能直接假定所有模型和量化配置都兼容。

**「社区性能报告仍待复现」** 评论者 rao-v 认为 gfx906 的主要价值是 32GB 显存和约 1 TB/s 的 HBM2 带宽，并称已有开发者围绕这类缺少 Tensor Core、原生 BF16 的设备优化 llama.cpp。性能数据均为用户自报：malicz 称 Radiance 在其 r9700 上运行 4-bit Qwen3.8-27b 时达到 2400 tok/s prefill 和 150 tok/s decode，并可让 3 路代理流各自携带 200k context 驻留显存；fiddlerwoaroof 则称在 MI100 上移植并优化 ROCm 内核后，Qwen3.8 的速度提高至原来的 2—3 倍，但这些结果尚无独立复现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/milpster/gfx906-llama-cpp">GitHub - milpster/gfx906-llama-cpp</a></li>
<li><a href="https://github.com/taobaoww2010-alt/llama-cpp-rocm-gfx906">GitHub - taobaoww2010-alt/llama-cpp-rocm-gfx906: llama.cpp ...</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#AMD GPUs`, `#gfx906`, `#LLM inference`, `#open source`

---

<a id="item-tech-news-3"></a>
### [Google 据报要求 Workspace 代理使用 MCP，但 Gmail 不能发信](https://techstackups.com/articles/google-workspace-ai-agents-mcp/) ⭐️ 7.0/10

据该报道，Google 计划要求与 Google Workspace 连接的 AI 代理通过 Google 提供的 MCP 服务器调用相关服务，而不是由代理直接访问底层账户能力。报道同时指出，其 Gmail MCP 服务器不能发送邮件，因此依赖 Gmail 完成发信的自动化流程将出现功能缺口。所给材料没有披露实施日期、适用范围或强制执行方式，因此这应视为已报道的计划，而非已经全面落地并经独立验证的能力。

hackernews · ritzaco · 11月26日 09:44 · [社区讨论](https://news.ycombinator.com/item?id=50653477)

**「相关技术背景」** Google 的 Workspace MCP 服务器建立在开放的 Model Context Protocol（MCP）标准之上，将 Gmail、Drive、Docs、Sheets、Calendar 等服务的能力封装为 AI 代理可调用的预置工具。Google 文档称，代理可读取邮件和文件、创建草稿及安排会议，而发送邮件等敏感操作会通过 MCP 的表单 elicitation 机制暂停工具调用，先取得用户确认。

**「对代理自动化的影响」** 对于需要让 AI 代理发送 Gmail 邮件或操作 Drive、Docs、Calendar 等 Workspace 数据的开发者，敏感操作会先经过服务端的人机协作审批：Google 的 Gmail MCP 服务器使用 MCP form elicitation，在发送邮件等动作前暂停并请求用户确认。因此，现有无人值守的“代理直接发送邮件”流程不能假定能原样迁移，集成时需要处理审批交互、授权以及调用暂停等状态。

**「限制原因与替代路径引发争议」** 有评论者认为，MCP 的 elicitation 机制本就可暂停工具调用并请求用户确认，因此将 Gmail 发信工具设为合作方专属更像商业策略，而非必要的安全措施。另有评论者称，使用 NeoMutt 及 SMTP、IMAP 让代理访问 Gmail 在其测试中更可靠，并质疑 Google 如何识别或阻止这种直接访问方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.google.com/workspace/guides/configure-mcp-servers">Configure the Google Workspace MCP servers</a></li>
<li><a href="https://developers.google.com/workspace/gmail/api/guides/configure-mcp-server">Configure the Gmail MCP server | Google for Developers</a></li>
<li><a href="https://workspaceupdates.googleblog.com/2026/11/mcp-servers-cli-standardized-usage-tiers-now-available.html">Google Workspace Updates: Simplifying agent access while ...</a></li>
<li><a href="https://developers.google.com/workspace/gmail/api/guides/configure-mcp-server">Configure the Gmail MCP server | Google for Developers</a></li>
<li><a href="https://workspaceupdates.googleblog.com/2026/11/mcp-servers-cli-standardized-usage-tiers-now-available.html">Google Workspace Updates: Simplifying agent access while ...</a></li>

</ul>
</details>

**标签**: `#Google Workspace`, `#Model Context Protocol`, `#AI agents`, `#Gmail automation`, `#platform lock-in`

---

<a id="item-tech-news-4"></a>
### [英伟达据报暂停东南亚四国 AI 服务器出货](https://www.ft.com/content/7838a715-07d4-4605-aa60-21f5af2b2370) ⭐️ 7.0/10

据《金融时报》报道，英伟达已要求主要制造合作伙伴暂停向马来西亚、新加坡、泰国和印度尼西亚发运 AI 服务器；戴尔、美超微等组装英伟达芯片整机的厂商已通知四国买家，相关订单不能出厂。三名知情人士称，此举与美国新一轮先进芯片出口管制有关，但是否仅为临时措施尚不清楚。美国商务部上周公布的新规要求区域云服务商在 90 天内取得出口许可，并核验客户不含受限制的中国实体；这四个国家此前也是中国 AI 企业获取英伟达最先进处理器的中转地。

telegram · zaihuapd · 11月26日 07:38

**「出口管制与中转规则」** 理解此次叫停的关键背景是：马来西亚、新加坡、泰国和印度尼西亚此前被中国 AI 企业用作获取英伟达最先进处理器的中转地，而相关芯片不得直接出口至中国大陆。美国商务部上周出台的新规要求区域云服务商在 90 天内取得出口许可，并核查最终客户是否包含受限制的中国实体。

**「交付暂停与许可要求」** 据报道，英伟达要求戴尔、美超微等制造伙伴停止向马来西亚、新加坡、泰国和印度尼西亚发运搭载其芯片的 AI 服务器，相关订单已被通知不能出厂，意味着当地买家无法按原计划收货。当地云服务商还需在 90 天内取得出口许可，并核实客户不含受限制的中国实体；由于冻结是否仅为临时措施尚不明确，运营方应暂缓依赖未获许可的交付，并准备许可申请与客户合规审查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.zerohedge.com/ai/nvidia-halts-ai-chip-shipments-four-southwest-asian-countries">&quot;Causing Sheer Chaos&quot;: Nvidia Halts AI Chip Shipments ... | ZeroHedge</a></li>
<li><a href="https://www.ft.com/content/7838a715-07d4-4605-aa60-21f5af2b2370?syn-25a6b1a6=1">Nvidia halts chip shipments to south-east Asia</a></li>
<li><a href="https://www.reuters.com/world/asia-pacific/nvidia-halts-chip-shipments-southeast-asia-ft-reports-2026-11-26/">Nvidia halts server shipments to four Southeast Asian ...</a></li>
<li><a href="https://www.ft.com/content/7838a715-07d4-4605-aa60-21f5af2b2370?syn-25a6b1a6=1">Nvidia halts chip shipments to south-east Asia - Financial Times</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/nvidia-stops-ai-gpu-shipments-160000782.html?fr=sycsrp_catchall">Nvidia stops AI GPU shipments to Southeast Asia amid ...</a></li>

</ul>
</details>

**标签**: `#AI accelerators`, `#export controls`, `#Nvidia`, `#AI supply chains`, `#Southeast Asia`

---

<a id="item-tech-news-5"></a>
### [ASML CEO 反对全面限制对华芯片设备出口](https://www.semafor.com/article/11/25/2026/asml-makes-the-case-for-selling-chips-to-china) ⭐️ 7.0/10

在 Semafor《Future Proof》节目中，ASML CEO 富凯反对全面限制对华芯片设备出口，主张管制应保护最先进的技术，但不能将中国完全排除在外。他认为，中国购买的 ASML 设备落后最先进制程十多年，全面封锁反而会促使中国加倍、甚至三倍投入光刻机自研。争议焦点是美国推动的 MATCH 法案拟将管制从 EUV 扩大到浸没式 DUV 和维护服务，荷兰政府与 ASML 均表示反对；目前披露的是 CEO 的政策观点及二次转述，并非已经生效的新禁令或技术突破。

telegram · zaihuapd · 11月26日 12:19

**「出口管制背景」** 这场争论针对的并非已经生效的全面禁令，而是美国推动的 MATCH 法案是否把对华限制从 EUV 进一步扩展到浸没式 DUV 和维护服务。荷兰议员已要求政府反对这项进一步收紧芯片制造设备出口的立法；ASML 是制造尖端芯片所用设备的世界唯一制造商，因此其产品与政策立场处于管制核心。

**「在华 DUV 供应与服务面临限制风险」** 如果美国推动的 MATCH 法案要求荷兰等关键盟友在 150 天内对齐其出口政策，ASML 对华业务受影响范围将从 EUV 扩大到目前仍获准销售的浸没式 DUV 设备及相关维护服务。中国晶圆厂因此需要提前评估在装设备的备件与维护连续性，并准备设备采购替代方案；该法案目前仍是拟议中的政策风险，并非已经生效的禁令。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.semafor.com/article/11/26/2026/dutch-lawmakers-condemn-us-legislation-curbing-chip-exports">Dutch lawmakers condemn US technology curbs | Semafor</a></li>
<li><a href="https://www.thedefensenews.com/US-Pushes-Bill-to-Compel-Netherlands-to-Halt-Remaining-ASML-Machine-Sales-and-Service-to-China/">US Pushes Bill to Compel Netherlands to Halt Remaining ASML ...</a></li>
<li><a href="https://nltimes.nl/2026/08/20/us-preparing-force-netherlands-ban-asml-selling-china">U.S. preparing to force Netherlands to ban ASML from selling ...</a></li>

</ul>
</details>

**标签**: `#半导体制造`, `#光刻机`, `#出口管制`, `#ASML`, `#芯片供应链`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [谁有权判定作品是否由 AI 写成](https://seangoedecke.com/who-gets-to-decide-if-something-is-written-by-ai/) ⭐️ 5.0/10

rss · Sean Goedecke · 11月27日 00:00

**「背景」** 围绕 AI 写作的争议常把注意力引向检测工具 Pangram 是否可靠、是否侵犯隐私，但作者认为真正的问题是：谁有权决定作品能否进入文学奖项、教育和公共讨论等人类空间。对 Pangram 的敌意或许主要源于对科技公司控制社会权力的不满，而非反对检测本身。

**「方案」** 在这一权力框架下，反对用工具裁定 AI 写作可以理解：把仲裁权交给另一家科技公司，无法消除人们担心的技术集中，也可能延续软件替代社区判断的既有趋势。但作者主张，当目标是阻止 AI 内容进入人类文化领域时，社区自我治理更糟：反 AI 者未必熟悉 AI 文本特征，常把“AI 腔”误判成人写，也把礼貌、流畅的长文误判为 AI。因此他赞成使用现有最强检测工具，并在不信任 Pangram 公司时转向开源方案或由政府自建检测平台；同时认为普通调查难以应对熟练的 AI 写作，因为过程草稿、创作后生成等证据问题，且不存在可靠的通用密码学认证路径。不过，这一论证主要是概念和经验判断：Pangram 及第三方测试仍报告误报与漏报，其跨内容类型能力及替代方案效果也未获独立误差率分析支持。

**「启示」** 作者的结论是：若拒绝 AI 的正当理由是防范科技权力扩张，就不应把鉴别责任交给更不熟悉 AI 的社区；更合理的方向可能是可审计、权力制衡的检测机制，而非回避工具。

**标签**: `#AI detection`, `#content provenance`, `#algorithmic gatekeeping`, `#technology governance`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [半导体出口价值首次超过油气](https://www.cnbc.com/2026/11/26/semiconductor-chips-are-the-new-oil-heres-why.html) ⭐️ 8.0/10

德银根据国际贸易中心数据分析称，按连续四个季度滚动总额计算，2026 年一季度全球半导体出口约 1.61 万亿美元，首次超过油气的 1.53 万亿美元；二季度两者分别约为 1.60 万亿美元和 1.47 万亿美元，而霍尔木兹海峡供应中断压低油气流量进一步扩大了差距。

rss · CNBC Finance · 11月26日 17:52

**「背景」** 此前全球出口贸易长期由石油主导；这项比较采用国际贸易中心数据，并按过去四个季度的滚动出口总额，衡量半导体与石油和天然气贸易的规模。

**「潜在影响」** 德意志银行分析师称，亚洲芯片出口国的部分收益若更多流向美国科技股、初创企业和数据中心，可能使美元更易受科技板块估值及全球资本流动变化影响，并加大美元波动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.dbresearch.com/PROD/IE-PROD/PROD0000000000659135.pdf">Chipping in: how chips have become a huge driver of the dollar</a></li>
<li><a href="https://www.investing.com/news/stock-market-news/how-are-ai-chip-flows-reshaping-dollar-dominance-deutsche-bank-explains-5043246">How are AI chip flows reshaping dollar dominance? Deutsche ...</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#global trade`, `#artificial intelligence`, `#commodity exports`, `#macroeconomics`

---

<a id="item-finance-news-2"></a>
### [荷兰反对美国拟议限制 ASML 对华销售法案](https://www.bloomberg.com/news/articles/2026-11-26/netherlands-plans-to-fight-rollout-of-proposed-us-curbs-on-asml) ⭐️ 7.0/10

荷兰外贸与发展合作大臣斯乔德·斯约兹马 11 月 26 日表示，荷兰不接受美国拟议的 MATCH Act 限制 ASML 对华销售，正联合欧盟及德国、法国游说删除相关条款。报道称，中国约占 ASML 今年销售额的 20%；该法案尚未通过，外界预计国会将于 12 月中旬表决。

telegram · zaihuapd · 11月26日 14:56

**「背景」** 美国现行出口管制已限制 ASML 最先进的极紫外光刻（EUV）设备，MATCH Act 拟扩大限制范围，并要求荷兰、日本等盟友配合，否则美国可单方面限制其半导体设备销售；荷兰政府此前已反对该法案的域外管辖效力。

**「潜在产业影响」** 若 MATCH Act 按提案实施，ASML 对华芯片制造设备销售可能受限；中国约占其 2026 年销售额的 20%，中国芯片制造商获取相关设备的渠道也可能因此收窄。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mrkt30.com/asml-match-act/">Why the MATCH Act Could Be a Real Problem for ASML - MRKT3.0</a></li>
<li><a href="https://keepingupwith.ai/articles/netherlands-opposes-match-act-at-risk-to-asmls-china-business/">Netherlands Opposes MATCH Act at Risk to ASML &#x27;s China Business</a></li>
<li><a href="https://hooooit.com/chips-act-export-controls-global-fab-equipment/">The Quiet Chokehold: How CHIPS Act Export Controls Are... - Hooooit</a></li>
<li><a href="https://www.techpowerup.com/351847/united-states-government-may-restrict-asmls-duv-tool-exports-to-china">United States Government May Restrict ASML &#x27;s DUV Tool Exports to...</a></li>

</ul>
</details>

**标签**: `#ASML`, `#对华出口管制`, `#MATCH Act`, `#荷兰`, `#半导体设备`

---