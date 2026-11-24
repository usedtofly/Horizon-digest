---
layout: default
title: "Horizon Summary: 2026-11-24 (ZH)"
date: 2026-11-24
lang: zh
---

> 从 38 条内容中筛选出 14 条重要资讯。

---

**科技新闻**
1. [英伟达董事会恢复黄仁勋 CEO 职务](#item-tech-news-1) ⭐️ 8.0/10
2. [Ladybird 发布首个 Alpha 预览版](#item-tech-news-2) ⭐️ 8.0/10
3. [GLM-5.4 发布：首个循环 Transformer 编码模型](#item-tech-news-3) ⭐️ 8.0/10
4. [Codex2api 3.1.10–3.1.12 疑似含后门](#item-tech-news-4) ⭐️ 8.0/10
5. [Anthropic 公开 Claude 发现的 VP≠VNP Lean 4 证明](#item-tech-news-5) ⭐️ 8.0/10
6. [NariQ：约 10GB 的 Qwen3.8-27B 低比特量化](#item-tech-news-6) ⭐️ 7.0/10
7. [Stalwart 宣称可直接替代 Microsoft Exchange](#item-tech-news-7) ⭐️ 7.0/10
8. [纽约州限制汽车订阅及购后收费](#item-tech-news-8) ⭐️ 7.0/10
9. [ChatGPT 向付费用户推送 GPT-6.2 Sol](#item-tech-news-9) ⭐️ 7.0/10
10. [鸿蒙终端设备突破 1 亿台](#item-tech-news-10) ⭐️ 7.0/10
11. [神舟二十四号拟搭载首位巴基斯坦航天员](#item-tech-news-11) ⭐️ 7.0/10

**科技博客**
1. [ERNIE 5.5 Flash 的 vLLM 插件化首日支持](#item-tech-blog-1) ⭐️ 8.0/10

**财经新闻**
1. [黄仁勋复任英伟达 CEO 带动美股反弹](#item-finance-news-1) ⭐️ 8.0/10
2. [Anthropic IPO 后中国 AI 上市计划承压](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [英伟达董事会恢复黄仁勋 CEO 职务](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 8.0/10

英伟达董事会宣布恢复黄仁勋的 CEO 职务，逆转此前将其免职的决定；黄仁勋将重新主导公司的 AI 芯片和出口管制相关决策。董事会称，决策过程中听取了美国政府高级官员的意见，并据此认定黄仁勋复任不会带来国家安全风险，但现有材料未披露这些意见的具体内容，也未说明复任后的任期或职责安排。此次治理反转使董事会独立性、政府介入半导体政策以及黄仁勋个人责任成为主要争议。

hackernews · jaz · 11月23日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=50611576)

**「背景」** “复任”意味着黄仁勋此前已离开英伟达 CEO 职位，本次是董事会恢复其原有职务，而非首次任命。英伟达主要开发 GPU、SoC 和 API，业务覆盖人工智能、高性能计算等领域，因此这一变化属于公司高层治理的逆转，现有材料并未说明此前离任的具体原因和日期。

**「暂无需技术适配，关注政策口径」** 现有材料未宣布驱动、SDK、GPU 或网络产品的接口、版本或兼容性变更，客户和开发者无需仅因这次复职调整技术方案；目前可确认的影响集中在治理与政策沟通，即 Nvidia 的战略重新由黄仁勋主导。六天前，Nvidia 仍拒绝其回归，董事会也公开表示无意复职，因此这种迅速反转意味着企业客户后续仍需核实产品路线图和出口政策口径，不宜将高管变动直接视为规格更新。

**「评论者质疑董事会决策的独立性」** 一些评论者认为，董事会声明中最具实质性的内容是“听取美国政府高级官员意见”，并据此质疑复任决定是否真正独立于政府；也有人援引特拉华州 Caremark 问责标准以及其所称的司法部不追诉立场，推测董事个人责任可能降低。另一些评论者将英伟达获得政府认可与要求 ASML、日本芯片企业配合对华制裁相提并论，认为政策标准不一致，也有人认为现有材料并不能证明英伟达或黄仁勋违法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/Nvidia">Nvidia - Wikipedia</a></li>
<li>Nvidia rejects Jensen Huang&#x27;s offer to return as CEO despite pressure from Silicon Valley</li>
<li>Nvidia board does not intend to reinstate… | UCapital News</li>

</ul>
</details>

**标签**: `#NVIDIA`, `#Executive Leadership`, `#AI Semiconductors`, `#Corporate Governance`, `#Export Controls`

---

<a id="item-tech-news-2"></a>
### [Ladybird 发布首个 Alpha 预览版](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

Ladybird 发布首个 Alpha 版本，macOS 和 Linux 用户现在可直接下载安装，无需自行编译。它自行实现了 HTML 解析、CSS 引擎、布局、JavaScript 和 WebAssembly 等大部分关键组件，同时依赖 HarfBuzz、Skia、FFmpeg 和 SQLite。Simon Willison 的试用显示，包括基于 WebAssembly 运行 FFmpeg 的工具和 Pyodide REPL 在内的多数站点可正常工作，但 Datasette Lite 因 service worker 相关 API 报错而无法启动；项目方也明确称 Alpha 阶段仍会有网站失效和偶发崩溃。Ladybird 公布的 2026 年 10 月数据还称其 Web Platform Tests 通过数达到 2,184,722，略低于 Firefox 的 2,189,315、高于 Safari 的 2,172,990；这是项目方披露的测试结果，不等同于全面兼容性保证。

hackernews · janvdberg · 11月23日 16:13 · [社区讨论](https://news.ycombinator.com/item?id=50614249)

**「项目背景」** Ladybird 源自 SerenityOS，并非 Chromium、WebKit 或 Gecko 的分支；项目自行实现了 HTML 解析、CSS 引擎、布局、JavaScript 和 WebAssembly 等大部分 Web 平台组件，仅在文本排版、二维图形、视频和数据库等环节依赖 HarfBuzz、Skia、FFmpeg 和 SQLite。此前项目将部分 LibJS 代码迁至 Rust，并通过编码代理补齐 Web Platform Tests 和引擎功能，此次 alpha 建立在这些兼容性改进之上。

**「适合试用，不宜立即替代主力浏览器」** macOS 和 Linux 用户现在可以低门槛安装 Ladybird 进行兼容性测试，但其 Alpha 定位、已知站点失效和崩溃风险意味着它暂不宜取代关键工作的主力浏览器；测试时应保留可用的替代浏览器，并按浏览器内提示报告失效站点，崩溃报告是否上传可由用户决定。

**「兼容性获好评，隐私与路线仍有分歧」** 多位试用者对复杂站点和 NoVNC 的兼容性表示赞赏，另有人只遇到轻微的滚动顿挫；但也有人怀念 SerenityOS 式的自研库路线，并质疑项目是否会认真处理指纹识别和细粒度权限，Alpha 阶段应采取哪些防护措施尚无明确共识。这些均为社区意见，而非已经验证的安全结论。

**标签**: `#web browsers`, `#browser engineering`, `#web compatibility`, `#fingerprinting privacy`, `#alpha releases`

---

<a id="item-tech-news-3"></a>
### [GLM-5.4 发布：首个循环 Transformer 编码模型](https://z.ai/blog/glm-5.4) ⭐️ 8.0/10

中国 AI 实验室 Z.ai 发布了面向通用编码的 GLM-5.4，这是其首个采用循环 Transformer 架构的模型。按 Z.ai 的说明，一组共享权重的层会在一次前向传播中迭代多次，以增加网络深度而不增加参数量。GLM-5.4 尚未开放权重，也无法通过常规 Z.ai API 套餐访问；作者使用 Coding Plan 订阅取得密钥，并通过与常规接口相同的 OpenAI 兼容 Responses API 端点（https://api.z.ai/api/v1）调用该模型。作者在低、高和 max 推理档生成的“骑车鹈鹕”SVG 与 GLM-5.3 相近，而 GLM-5.1 和 5.2 的输出风格明显不同；不过这只是单项定性测试，尚不足以证明 GLM-5.4 的编码能力或通用性能取得突破。

hackernews · foohis · 11月23日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=50609685)

**「背景」** 循环 Transformer 的关键并非在一次前向传播中堆叠更多独立层，而是让一组共享权重的层重复运行、继续精炼隐藏状态；按 Z.ai 的描述，这样可增加网络的有效计算深度而不增加参数量。此前，Thinking Machines Lab 已在 11 月 20 日发布的 Inkling 2 Mini 中采用同类做法，让模型的中间层为每个 token 运行三次，因此 GLM-5.4 是这一近期架构方向的一次新应用，而非该概念的首次出现。

**「实际接入影响」** 在此次发布时，GLM-5.4 不能通过常规 Z.ai API 调用，开发者需订阅 Coding Plan；官方也尚未发布开放权重，因此无法以官方权重进行本地部署。Coding Plan 与常规 API 共用同一 OpenAI 兼容 Responses API 端点，套餐密钥可直接调用 5.4，并可用于 Claude Code、Cline、OpenCode 等编码工具；但现有 llm-zai 插件尚未支持该模型，需改用作者提供的 llm-glm 插件或等待兼容更新。

**「社区讨论」** 评论者对 Z.ai 公开架构细节表示赞赏，并认为循环 Transformer 是在不增加参数量的情况下扩展模型深度的自然方向；另一位评论者则批评部分中国模型在简单任务上反复自我怀疑的“马拉松式思考”，认为这会显著增加完成时间，除非推理吞吐量足够高。也有评论者从显存带宽瓶颈出发解释循环计算的价值，但现有来源没有提供独立性能测量来验证这些观点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://z.ai/subscribe">GLM Coding Plan — AI Coding Powered by GLM -5.4 &amp; GLM -5.3-Flash...</a></li>

</ul>
</details>

**标签**: `#large language models`, `#loop transformers`, `#coding models`, `#AI architecture`

---

<a id="item-tech-news-4"></a>
### [Codex2api 3.1.10–3.1.12 疑似含后门](https://github.com/WormW/codex2api-incident-2026-11) ⭐️ 8.0/10

一份经 Telegram 转发的 GitHub 事件复盘称，Codex2api 作者账号疑遭入侵，攻击者绕过 main 分支推送标签，使 v3.1.10–v3.1.12 的 Release 构建疑似包含后门；该说法目前主要来自群内报告及事故仓库，尚无独立验证。报告特别指称 v3.1.11 移除了鉴权，可被无密码远程执行命令，另有 workflow 将仓库中的 16 个 GitHub Actions secrets 外传，影响可能波及同一账号下的至少 21 个仓库。报告建议立即停用受影响版本、回退至 v3.1.9，并轮换 GitHub token、SSH 密钥、数据库及 DeepSeek 等所有可能相关的凭据。

telegram · zaihuapd · 11月23日 11:21

**「Codex2API 与 Actions 信任边界」** Codex2API 是一个基于 Go 和 React/Vite 构建的反向代理与管理系统，可将多个上游 Codex 账户的 Refresh Token 或 Access Token 封装为兼容 OpenAI API 的统一服务。此次报告涉及的不只是 API 服务本身，而是其 GitHub Release 发布链路以及仓库的 GitHub Actions secrets；这些凭据可能让攻击者从持续集成环节扩大到仓库或其他外部服务。具体受影响版本和波及范围目前仍只是 Telegram 报告中的指控，尚待独立验证。

**「受影响用户需立即处置」** 已安装或升级至疑似受污染的 Codex2api 3.1.10–3.1.12 的用户应立即停用并回退至 3.1.9，同时轮换 GitHub token、SSH 密钥、数据库凭据和 DeepSeek 密钥；报告还称同一账号下至少 21 个仓库可能受波及，但尚未独立验证。处置时还应检查 GitHub Actions workflow 与运行记录是否被回退或删除，因为针对另一类 Actions 密钥窃取工具的研究发现，攻击者可能在凭据轮换后仍保留云端访问并迅速抹除运行痕迹。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepwiki.com/james-6-23/codex2api">james-6-23/ codex2api | DeepWiki</a></li>
<li><a href="https://www.stepsecurity.io/blog/wfx-phantom-the-github-actions-secret-stealer">WFX Phantom: The GitHub Actions Secret Stealer... - StepSecurity</a></li>

</ul>
</details>

**标签**: `#software supply chain security`, `#GitHub Actions`, `#credential compromise`, `#malicious release`, `#Codex2api`

---

<a id="item-tech-news-5"></a>
### [Anthropic 公开 Claude 发现的 VP≠VNP Lean 4 证明](https://github.com/anthropics/formal-math/blob/main/vp-vnp/README.md) ⭐️ 8.0/10

Anthropic 在 \`Anthropics/formal-math\` 仓库公开了论文《VP ≠ VNP over every field》及配套 Lean 4 形式化证明，称哈密顿圈多项式的超多项式算术电路下界由其内部研究用 Claude 模型发现，论文和代码均由 AI 撰写。若该结果成立，它将证明 VP 是 VNP 的真子类并解决 Valiant 1979 年的代数复杂度猜想，但这一结论仅针对算术电路复杂度，并不等同于解决 P 与 NP 问题。仓库称证明经过三项标准公理审计及 nanoda 内核独立复核，除预留文件外没有 \`sorry\`；不过尚无人类数学家完成通读，Lean 只能验证证明与形式化陈述是否一致，不能确认形式化陈述完全对应文字中的目标命题，附录 Q 还列出了待核查的出入，因此目前应将其视为可公开检验、但尚待独立审阅的研究结果，而非已经确认的突破。

telegram · zaihuapd · 11月24日 06:02

**「VP 与 VNP 的代数复杂度背景」** 理解这项工作的前提是 Leslie Valiant 于 1979 年提出的代数复杂度猜想，即在所有域上是否都有 VP = VNP；它常被视为 P 与 NP 猜想的代数对应物。它研究的是必须对域及其扩张中的所有输入而不仅是 0 和 1 有效的算术电路，因此这里的 VP≠VNP 与 P≠NP 不是同一个命题。

**「结果仍需独立审阅」** 理论计算机科学与形式化方法社区目前获得的是可供核查的论文和 Lean 4 证明工件，而不是已经确认的 VP≠VNP 定理；研究者引用前应核对形式化陈述与论文命题是否一致，并等待独立数学家审阅附录 Q 所列差异。即使命题最终成立，其影响也仅限于算术电路模型中的 VP 与 VNP 分离，并不等于解决 P 与 NP。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.alphaxiv.org/abs/2611.vp-vnp-arithmetic-lower-bounds">VP VNP Over Every Field | alphaXiv</a></li>
<li><a href="https://www.youtube.com/watch?v=UuOiRi9T-9c">Claude &#x27;s VP VNP Proof: 47 Years Open, Still Unchecked... - YouTube</a></li>

</ul>
</details>

**标签**: `#AI 数学发现`, `#定理证明`, `#Lean 4`, `#计算复杂性`, `#Claude`

---

<a id="item-tech-news-6"></a>
### [NariQ：约 10GB 的 Qwen3.8-27B 低比特量化](https://huggingface.co/nari-labs/Qwen3.8-27B-NariQ-GGUF) ⭐️ 7.0/10

Nari Labs 在 Hugging Face 提供 NariQ，将 Qwen3.8-27B 制成 3-bit、2.5-bit 和 2-bit GGUF 量化，3-bit 文件约 10GB，面向内存受限的本地推理用户。项目方自报这些版本在智能体、代码、数学、多语言推理和图像理解上接近 BF16；例如 DeepSWE 四档分数为 39.8/41.0/41.9/28.6，Terminal-Bench 2.1 为 62.6/63.8/60.2/52.4（依次为 BF16/3-bit/2.5-bit/2-bit）。所列 64K 上下文分数为 70.7/77.5/85.0/74.8（依次为 3-bit/2.5-bit/2-bit/Unsloth UD-IQ3\_XXS），但这些结果尚非独立验证。当前运行必须使用 nari-labs/nari-llama.cpp 定制分支；项目方只称在 RTX PRO 6000 上解码速度与其他量化相当，未提供具体速度或完整硬件对比。

hackernews · toebee · 11月23日 13:42 · [社区讨论](https://news.ycombinator.com/item?id=50611402)

**「背景」** 低比特量化的基本思路是用 2–3 bit 近似存储每个模型权重，从而将 BF16（通常每个权重占 16 bit）的模型压缩为更小的 GGUF 文件，降低本地推理的内存门槛；验证重点不只是压缩率，还包括编码、数学、多语言、代理和图像任务是否出现明显退化。NariQ 当前依赖 nari-labs 的定制 llama.cpp 分支，因此其速度结果需要结合这一特定运行时环境解读。

**「本地部署与兼容性」** 对本地推理用户，3 bpw 的 Qwen3.8-27B 权重可压缩至约 10 GB 的单个文件，降低了模型存储门槛；但当前必须从源码构建 nari-labs 的定制 llama.cpp 分支，不能直接使用标准构建。NariQ 论文报告 3.0 和 2.5 bpw 在 DeepSWE、Terminal Bench、AIME 与 RealWorldQA 上接近 BF16，但 2.0 bpw 在 DeepSWE 和 Terminal Bench 上分别从 3 bpw 的 41.0、63.8 降至 28.6、52.4，因此实际选型应优先验证 3.0 或 2.5 bpw，并针对自身工作负载复测。

**「社区质疑与实机反馈」** 一位支持者认为项目方测试了多类长时智能体任务并提到“held-out”数据，比常见的高算力 QAT 量化更可信；另一派则认为分数优势可能来自评测 harness 差异，并担忧这类方法会针对基准过拟合，真实使用未必接近 BF16。一名评论者称，在 18GB M3 Pro 的 Metal 构建上，3.0bpw 约为 3.8 tok/s、2.0bpw 约为 4.9 tok/s，明显慢于 CUDA，并希望看到 16GB Mac 与 Bonsai 2 27B 的对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.26157">NariQ : Sub-3-Bit Quantization for Long-Horizon Agentic Tasks</a></li>
<li><a href="https://arxiv.org/html/2611.26157v1">NariQ : Sub-3-Bit Quantization for Long-Horizon Agentic Tasks</a></li>

</ul>
</details>

**标签**: `#LLM quantization`, `#Qwen3.8-27B`, `#local inference`, `#GGUF`, `#llama.cpp`

---

<a id="item-tech-news-7"></a>
### [Stalwart 宣称可直接替代 Microsoft Exchange](https://stalw.art/blog/microsoft-exchange-replacement/) ⭐️ 7.0/10

Stalwart 宣称其邮件服务器现可作为 Microsoft Exchange 的直接替代品，面向考虑以开源自托管方案替换 Exchange 的运维团队。现有材料仅支持这一兼容性声明，未说明具体协议、客户端支持范围、部署条件或独立测试结果，因此不能将其视为 Outlook、迁移流程和合规归档均已无条件兼容。

hackernews · shaunpud · 11月23日 22:32 · [社区讨论](https://news.ycombinator.com/item?id=50620349)

**「直接替代的技术前提」** “直接替代”在邮件服务器语境中，关键不是只更换管理界面，而是让现有客户端和移动设备继续使用熟悉的连接协议。Stalwart 1.2.0 的公告称其支持 MAPI over HTTP、Exchange Web Services、ActiveSync 和 Autodiscover，因此 Outlook、Apple Mail 和移动设备可像连接 Exchange 服务器一样接入；这些协议兼容性构成其“drop-in replacement”说法所依赖的技术基础。

**「实际影响」** 自托管管理员可以把 Stalwart 纳入 Exchange 替换方案，以评估减少许可成本和迁移工作的可行性；但正式迁移前仍需针对实际 Outlook 客户端、所依赖的协议以及备份和归档要求进行兼容性与合规测试。

**「社区讨论」** 多位评论者认为“直接替代”的说法需要收窄：有人指出 Outlook 对本地 Exchange 支持的变化，以及新版 Outlook 同步 IMAP 邮件的行为，意味着客户端迁移和数据边界仍要单独处理。另有评论者称，德国 GoBD 合规场景要求邮件不可删除或篡改并保留最长 10 年，而 Stalwart 常规及 OSS 方案尚未提供相应功能；另有意见认为，支持 MAPI 等微软协议虽可能节省许可费，却会延续协议锁定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stalw.art/blog/microsoft-exchange-replacement/">Stalwart is now a drop-in replacement for Microsoft Exchange</a></li>

</ul>
</details>

**标签**: `#Stalwart`, `#Microsoft Exchange`, `#email interoperability`, `#self-hosted email`

---

<a id="item-tech-news-8"></a>
### [纽约州限制汽车订阅及购后收费](https://www.governor.ny.gov/news/money-your-pockets-governor-hochul-signs-bill-restricting-exploitative-vehicle-subscription) ⭐️ 7.0/10

纽约州长凯茜·霍舒尔签署法案，限制汽车订阅费以及购车后向消费者收取的追加费用。豁免范围包括导航与信息娱乐系统更新、卫星广播、车载 Wi‑Fi、远程信息处理、道路救援、依赖软件的驾驶辅助或驾驶自动化功能，以及依靠蜂窝或其他数据网络持续运行的车联网服务。因此，该政策并非全面禁止车载软件收费，具体影响将取决于某项收费是否落入这些豁免；现有材料未提供完整法条和实施细则。

hackernews · DeepLogin · 11月24日 02:27 · [社区讨论](https://news.ycombinator.com/item?id=50622774)

**「联网汽车收费监管」** 车辆订阅和购车后附加费，是指车企或经销商在售车后，对联网功能、驾驶辅助等持续服务另行收费的商业模式。此次规则的背景关键是按功能性质划界：一般订阅及购车后费用受到限制，但导航更新、卫星广播、车载 Wi‑Fi、远程信息处理、软件依赖型驾驶辅助或自动化，以及需依靠蜂窝或其他数据网络持续运行的服务被列为豁免，因此并非全面禁止车载软件的持续收费。

**「车载订阅收费模式受限」** 纽约州的车企和经销商需要重新审查汽车订阅及购车后收费设计，避免对受限制的项目续费；但导航更新、信息娱乐、卫星广播、车载 Wi-Fi、远程信息处理、路边援助以及依赖通信网络运行的驾驶辅助或自动化功能仍可能获得豁免。这意味着禁令直接压缩基础车辆功能相关收费空间，却不会全面阻断联网汽车服务变现。

**「评论者质疑豁免带来的规避空间」** 有评论者据此认为 SiriusXM 卫星广播和特斯拉增强巡航控制等业务可能不受直接影响，也有人猜测立法动机与经销商无法参与这些收费有关。另一名评论者警告，厂商可能利用驾驶自动化豁免推出“联网座椅加热”等功能，从而削弱限制效果；这些均属于社区推测，而非已确认的立法意图。

**标签**: `#connected cars`, `#automotive software`, `#technology regulation`, `#subscription fees`

---

<a id="item-tech-news-9"></a>
### [ChatGPT 向付费用户推送 GPT-6.2 Sol](https://x.com/ChatGPT/status/2124942186425069836) ⭐️ 7.0/10

据 ChatGPT 官方账号 11 月 23 日公告，GPT-6.2 Sol 已上线 Chat 标签页，并开始向 Plus、Pro、Business 和 Enterprise 用户推送。官方称，新版本在处理复杂指令、识别照片中的文字和路牌符号、按价格或位置筛选联网搜索结果，以及判断是否主动提供后续建议方面有所改进。目前这些能力尚无基准测试、部署细节或独立验证，实际可用范围也可能因用户套餐和推送进度而异。

telegram · zaihuapd · 11月24日 00:44

**「理解模型上线与推送」** 要理解这条消息，关键是区分“模型版本上线”与“所有账号立即可用”：公告描述的是在现有 ChatGPT 聊天页中提供 GPT-6.2 Sol，并按 Plus、Pro、Business 和 Enterprise 等付费层级推送。材料未提供与此前模型的基准对照或第三方测试，因此复杂指令处理、图像识别、联网筛选和主动建议方面的改进仍应视为官方声明，而非已独立验证的性能结论。

**「付费用户需验证新模型表现」** 对 Plus、Pro、Business 和 Enterprise 用户，实际变化是 ChatGPT 的 Chat 标签页开始推送 GPT-6.2 Sol；使用 Windows、Mac、iPhone 或 Android 客户端的用户应以各自账户中实际显示的版本为准。依赖复杂指令、联网检索、图片细节识别或主动后续建议的团队应开展自身任务回归测试，因为这些改进目前仅为官方说法，尚无独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://chatgpt.com/download/">Download ChatGPT</a></li>

</ul>
</details>

**标签**: `#ChatGPT`, `#GPT-6.2`, `#model rollout`, `#multimodal AI`

---

<a id="item-tech-news-10"></a>
### [鸿蒙终端设备突破 1 亿台](https://www.xinhuanet.com/20261124/68842538167d4e59a875056d5eb885ad/c.html) ⭐️ 7.0/10

华为终端有限公司宣布，搭载 HarmonyOS 5、6、7 的手机、平板和电脑设备已超过 1 亿台，鸿蒙应用与服务可获取数量超过 46 万项。华为同时称，平台注册开发者已超 1200 万人，开源鸿蒙拥有 1.4 万余名贡献者和 120 余个行业发行版；合作伙伴贡献的超过 160 项创新能力已被超过 1600 款应用集成调用，相关功能使用量在一年内增长 90 倍。上述数字均来自华为公告，报道未披露终端设备统计口径，也未提供独立验证。

telegram · zaihuapd · 11月24日 01:46

**「鸿蒙的发展脉络与统计口径」** 鸿蒙操作系统于 2019 年首次发布，2024 年 10 月发布原生鸿蒙。此次“终端设备破 1 亿台”的统计覆盖搭载 HarmonyOS 5、6、7 的手机、平板和电脑，并非仅指某一个版本的装机规模。

**「开发者需验证多版本适配」** 搭载 HarmonyOS 5、6、7 的设备已超过 1 亿台，因此面向该生态发布或更新应用的开发者应将三个版本纳入兼容性测试，不能把“设备破亿”直接视为所有应用均已完成稳定适配。通报未公布各版本的设备占比、活跃度或稳定性数据，外部分析也将开发者是否会持续投入应用构建与维护列为仍待验证的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://forgeeks.dev/harmonyos-100-million-devices/">Huawei says HarmonyOS will pass 100 million devices by 2026</a></li>

</ul>
</details>

**标签**: `#HarmonyOS`, `#operating systems`, `#open source`, `#device ecosystem`, `#Huawei`

---

<a id="item-tech-news-11"></a>
### [神舟二十四号拟搭载首位巴基斯坦航天员](https://www.news.cn/20261124/3b116eb35c404cd7b897b23a50099b5b/c.html) ⭐️ 7.0/10

中国载人航天工程新闻发言人张静波 11 月 24 日在酒泉宣布，神舟二十四号瞄准 11 月 25 日 8 时 18 分发射。乘组由汤洪波、武毅和巴基斯坦航天员穆罕默德·齐尚·阿里组成，汤洪波任指令长；阿里将成为首位到访中国空间站的外籍航天员。飞船将采用 3.5 小时自主快速交会对接，对接天和核心舱前向端口；阿里之后将与张志远、黎家盈乘神舟二十三号返回。

telegram · zaihuapd · 11月24日 04:08

**「乘组轮换与留轨任务」** 此次任务涉及连续两次飞行任务的乘组衔接：据观察者网报道，神舟二十三号乘组航天员朱杨柱将继续留轨执行神舟二十四号载人飞行任务，外籍航天员则计划随神舟二十三号载人飞船返回。因此，神舟二十四号的发射还涉及此前乘组的延长驻留与后续返程安排。

**「首次纳入外籍航天员」** 阿里将先乘神舟二十四号进入中国空间站，并按安排与张志远、黎家盈乘神舟二十三号返回，形成中国载人航天工程首次由外籍航天员参与的乘组往返流程。8 时 18 分的发射时间和 3.5 小时自主快速交会对接方案目前均为计划安排，实际执行仍需视任务和发射窗口确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.guancha.cn/ZhengZhi/2026_11_24_909706.shtml">“天宫”将迎来首位外籍航天员，朱杨柱执行一年期在轨驻留试验任务</a></li>

</ul>
</details>

**标签**: `#载人航天`, `#神舟二十四号`, `#国际合作`, `#自主交会对接`, `#巴基斯坦航天员`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [ERNIE 5.5 Flash 的 vLLM 插件化首日支持](https://vllm.ai/blog/2026-11-24-ernie-5-5-flash-preview) ⭐️ 8.0/10

rss · vLLM Blog · 11月24日 00:00

**「背景」** ERNIE 5.5 Flash Preview 是 280B 总参数、每 token 激活 14B 的稀疏 MoE 模型，支持 1M token 上下文；难点是同时控制长上下文成本并快速接入 serving 框架。

**「方案」** 作者为 VHA、Multi-Router Latent MoE、MultiMax 等结构定制融合内核，将可预计算项折入权重，以减少中间张量访存和内核启动；其称融合内核比朴素实现快 1.55×–6.53×。FlashIndexer 用依赖当前 token 的轻量路由头筛选稀疏索引头，以原 DSA 选择蒸馏，并预筛 2048 个 top-k 候选；约 1B token 微调后，作者报告 1M 上下文加速 1.4×。W4A8 QAT 对齐训练与推理的量化规则，FP8 KV cache 与 DSA 的 FP4 索引计算进一步降低开销；随权重提供的 3 层 DSpark 草稿模型每步最多提议 7 个 token，作者称真实编码和复杂 Agent 负载的平均接受长度超过 4.0。部署采用独立 vLLM-ERNIE 插件，与官方 vllm==0.32.0 同环境安装并自动注册，无须分叉、专用镜像或 nightly wheel；并行、PD 分离和 CPU KV offload 则复用 vLLM 能力。不过文章缺少可复现的端到端基准、消融和精度评估，因此这些性能数字应视为厂商自报。

**「启示」** 此次首日支持的核心，是把模型结构、量化训练、稀疏索引与推测解码的协同优化，同可独立发布的 vLLM 插件化接入结合起来。

**标签**: `#vLLM plugins`, `#sparse attention`, `#mixture-of-experts inference`, `#GPU kernel fusion`, `#speculative decoding`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [黄仁勋复任英伟达 CEO 带动美股反弹](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo-market-rally.html) ⭐️ 8.0/10

英伟达董事会全票恢复黄仁勋为总裁兼首席执行官并重新加入董事会，周一美股三大指数随即大涨；此前标普 500 从 11 月 12 日至周五跌逾 9%，三大指数周五均进入较高点回落至少 10%的调整区间。策略师对反弹能否持续看法不一，尚不能据此确认市场已经见底。

rss · CNBC Finance · 11月23日 18:00

**「背景」** 本轮抛售在黄仁勋离任消息公布前已因 AI 建设融资、中期选举后的数据中心审批及云巨头资本开支可能见顶等担忧启动，离任消息公布后进一步加速。英伟达还称，针对黄仁勋是否曾成为外国情报活动目标的独立董事调查将继续。

**「影响」** 黄仁勋复任暂时减轻了英伟达及 AI 交易相关股票的抛售压力，但策略师称反弹能否持续仍取决于云巨头的资本开支速度。

**标签**: `#Nvidia`, `#Jensen Huang`, `#U.S. equities`, `#AI trade`, `#market correction`

---

<a id="item-finance-news-2"></a>
### [Anthropic IPO 后中国 AI 上市计划承压](https://www.bloomberg.com/news/articles/2026-11-23/china-s-next-ai-deals-clouded-by-selloff-after-anthropic-ipo) ⭐️ 7.0/10

据彭博报道，Anthropic 完成规模达 1195 亿美元的创纪录 IPO 后全球股市加速下跌，中国科技股市值自 6 月底以来累计蒸发 1.7 万亿美元。报道认为，这轮跌势可能使正在筹备或考虑发行股份的 DeepSeek、月之暗面和阶跃星辰更难推进上市计划。

telegram · zaihuapd · 11月23日 09:31

**「背景」** 在此轮抛售前，DeepSeek、月之暗面等中国 AI 初创公司正加快首次公开发行（IPO），推动因素包括投资者需求、模型突破和政策支持。阶跃星辰也已于 2026 年 2 月被报道寻求在香港联交所上市；这三家公司均被视为 Anthropic 的竞争对手。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/StepFun">StepFun - Wikipedia</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-23/china-s-next-ai-deals-clouded-by-selloff-after-anthropic-ipo">China ’s Next AI Deals Clouded by Selloff After Anthropic IPO</a></li>
<li><a href="https://www.outlookbusiness.com/deeptech/deepseek-moonshot-gigaai-why-chinas-ai-startups-are-rushing-for-ipo">DeepSeek , Moonshot , GigaAI: Why China &#x27;s AI Startups Are Rushing...</a></li>

</ul>
</details>

**标签**: `#Anthropic IPO`, `#Chinese tech stocks`, `#AI listings`, `#DeepSeek`, `#Moonshot AI`

---