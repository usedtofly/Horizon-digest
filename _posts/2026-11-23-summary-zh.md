---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 35 条内容中筛选出 9 条重要资讯。

---

**科技新闻**
1. [XNU Linux：在 Linux 上运行 OS X 图形用户态](#item-tech-news-1) ⭐️ 7.0/10
2. [OpenAI 以困惑度衡量模型智能进展](#item-tech-news-2) ⭐️ 7.0/10
3. [GL.iNet 发布 2026-11-20 安全通知](#item-tech-news-3) ⭐️ 7.0/10
4. [Windows Server 2028 默认移除 WoW64](#item-tech-news-4) ⭐️ 7.0/10

**科技博客**
1. [不确定时，多做实验](#item-tech-blog-1) ⭐️ 6.0/10
2. [解读 OpenAI 困惑度曲线](#item-tech-blog-2) ⭐️ 6.0/10

**财经新闻**
1. [亚洲多地调整交易规则应对市场波动](#item-finance-news-1) ⭐️ 8.0/10
2. [厄尔尼诺海温创纪录，粮食援助承压](#item-finance-news-2) ⭐️ 7.0/10
3. [蚂蚁集团领投 Simplexity Robotics 1 亿美元融资](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [XNU Linux：在 Linux 上运行 OS X 图形用户态](https://github.com/AFK-surf/xnulinux) ⭐️ 7.0/10

XNU Linux 是一个实验性项目，目标是在 Linux 上运行完整的 OS X 图形用户态，涉及操作系统兼容、内核适配与系统工程。现有材料未交代其实现范围、硬件依赖或实际可用性，因此近期的实用成熟度仍不明确，技术讨论也尚不能证明它已成为可用的 Linux 替代方案。

hackernews · mmastrac · 11月23日 03:49 · [社区讨论](https://news.ycombinator.com/item?id=50607261)

**「背景：XNU 内核与 macOS 用户态的前提」** XNU 是 Apple 公开的混合内核，它以卡内基梅隆的 Mach 内核为主体，融合了 FreeBSD 组件，并通过 IOKit 提供编写驱动的 C++ 接口（Apple 开源 XNU 仓库的 README 说明）。与 Linux 依赖稳定系统调用接口不同，macOS 应用需要与系统自带、随系统版本同步演进的框架库动态链接，因此 Hacker News 讨论中用户 miki123211 据此认为 macOS 用户态有可能在真实 Linux 之上运行而几乎不需要内核改动——这正是此类移植实验赖以成立的技术前提。

**「实际可用性与许可边界」** 该项目目前的实际影响更接近技术可行性验证，而非可在普通 Linux PC 上直接部署的桌面替代品：评论者认为，其可行性来自 macOS 应用依赖系统自带动态库而非稳定的系统调用 ABI；另一位参与者则称它仍需要 Apple 硬件。开发者若计划合并或分发相关代码，还需审查许可证边界，因为已有 GitHub issue 讨论了 Apple APSL 代码与 GPL 的不兼容问题。

**「社区讨论」** 有评论者认为，macOS 缺乏 Linux 式的稳定系统调用接口、应用需动态链接系统随附的库，因此其用户态或许能以很少甚至无需内核改动的方式运行在 Linux 上；这一判断未获当前材料验证。另有人指出项目可能仍需 Apple 硬件，并表示更希望改进 GNUstep。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/apple-opensource/xnu/blob/master/README.md">xnu/README.md at master · apple-opensource/xnu · GitHub</a></li>
<li>Code from Apple under the APSL is incompatible with the GPL · Issue #542 - GitHub</li>

</ul>
</details>

**标签**: `#XNU`, `#Linux`, `#OS X userspace`, `#operating-system compatibility`, `#systems engineering`

---

<a id="item-tech-news-2"></a>
### [OpenAI 以困惑度衡量模型智能进展](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI 提出，语言模型预测并压缩数据的能力可通过困惑度衡量，而困惑度的持续改善可作为模型智能与推理进步的简单指标。该观点把模型能力评估重新聚焦到预测性能本身，但它仍是一项分析框架和研究主张，并非 OpenAI 此次发布了新的产品功能或独立验证的评测结果。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**「困惑度作为模型评估指标」** 这里的“困惑度”（perplexity）是从模型对下一个 token 的预测不确定性导出的语言模型指标，与交叉熵损失等价；在相同评测条件下，较低的困惑度通常表示预测表现更好。OpenAI 在文中主张将这一指标用于跨开发者比较预训练进展，并为共享安全标准提供参考，首先从提高自身预训练过程的透明度开始。

**「为跨厂商模型评测提供共同尺度」** 微软已支持 OpenAI 的透明度倡议，承诺在同一个保留评测集上公布预训练进展；其 MAI-2 Base 的 log-perplexity 为 0.819，与 GPT-5.6 Sol 基座模型处于同一量级。模型开发者和评测团队可据此使用共同保留集报告结果，以比较不同厂商基座模型的预测效率，但这一指标本身不应被当作完整的智能或推理能力排名。

**「评论聚焦指标含义与跨模型比较」** 评论者将困惑度解释为模型预测下一个词元时的惊讶程度：均匀随机预测对应词表大小的困惑度，完全确定的预测对应 1；另有评论者认为预测与压缩能力可能反映模型从原始数据中提炼世界模型的过程。一位评论者还援引 Mustafa Suleyman 的帖子称，Microsoft 已在获准使用的共同留出评测集上报告 MAI-2 Base，其 log-perplexity 为 0.819，并称其与 GPT-5.6 Sol 基础模型处于相近水平；这是社区转述的厂商数据，并非本文提供的独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence - OpenAI</a></li>
<li>Mustafa Suleyman on X: &quot;We fully support OpenAI&#x27;s transparency initiative. Thanks to ...</li>
<li>Suleyman says MAI-2 Base is in GPT-5.6 Sol&#x27;s ballpark—mind the metric - Digg</li>

</ul>
</details>

**标签**: `#language-model evaluation`, `#perplexity`, `#AI reasoning`, `#cross-entropy`

---

<a id="item-tech-news-3"></a>
### [GL.iNet 发布 2026-11-20 安全通知](https://www.gl-inet.com/en-us/blogs/blog/glinet-security-notice-2026-11-20) ⭐️ 7.0/10

GL.iNet 于 2026 年 11 月 20 日发布安全通知，面向其网络设备用户。现有材料未提供通知正文，也未说明受影响型号、攻击方式、恶意软件或入侵范围、严重程度及所需修复措施，因此无法确认用户是否需要更新固件、修改账号或禁用云端访问。核实官方处置步骤前，也不应将评论区的相关说法视为已确认的设备失陷事实。

hackernews · gregsadetsky · 11月22日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50604988)

**「此前时间线仍待核实」** 一名社区评论者称，GL.iNet 设备可能至少从上一年起就存在恶意软件，并附有论坛讨论链接；这一说法来自评论者，并非厂商已确认的事件时间线。准确理解 2026-11-20 安全公告，仍需核对受影响的设备型号、恶意代码入侵路径，以及是否涉及厂商云端账户或远程访问凭据。

**「受影响设备需立即更新固件」** 使用受影响型号的 GL.iNet 用户应尽快安装与具体型号对应的最新稳定安全固件，即使检查未发现感染迹象也应更新。该固件可直接移除此次事件识别的恶意软件，且无需恢复出厂设置；安装前仍需确认型号与固件兼容性。

**「用户讨论云端依赖与替代固件」** 一名评论者称赞 GL.iNet 的本地化通知清楚说明了事件和处置方式，并表示将继续选择该品牌；不过，当前材料没有通知正文可供核实。多名用户主张禁用云服务或改用 OpenWrt，另有用户声称设备可能“自去年起已被入侵”，但这一说法仅附论坛链接、尚未得到独立证实；评论还指出并非所有 GL.iNet 产品都能由 OpenWrt 替代，KVM 被列为令人担忧的例外。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gl-inet.com/blogs/blog/glinet-security-notice-2026-11-20">GL.iNet Security Notice 2026-11-20</a></li>
<li><a href="https://forum.gl-inet.com/t/2026-11-20-gl-inet-security-notice-goodcloud-kvm-routers/73056">2026-11-20: GL.iNet Security Notice - GoodCloud / KVM ...</a></li>

</ul>
</details>

**标签**: `#network-device-security`, `#router-firmware`, `#IoT-security`, `#OpenWrt`

---

<a id="item-tech-news-4"></a>
### [Windows Server 2028 默认移除 WoW64](https://www.windowslatest.com/2026/11/23/32-bit-apps-days-are-numbered-as-microsoft-strips-support-bit-by-bit-starting-with-windows-server-2028-but-windows-11-is-safe-for-now/) ⭐️ 7.0/10

微软在 Ignite 2026 上宣布，Windows Server 2028 将默认不再包含 WoW64 兼容子系统，因此新装系统默认无法运行 32 位应用。该版本计划于 2027 年秋季与 Windows 11 27H2 一同发布，管理员可通过按需功能（FoD）手动装回 WoW64，在 Server Core 上通常可使用 PowerShell 或 DISM 添加。微软称这一调整旨在减少攻击面并阻止 32 位恶意软件；Windows 11 目前仍保留 WoW64，微软尚未公布移除计划。

telegram · zaihuapd · 11月23日 03:03

**「WoW64 与服务器安全基线」** WoW64 是 64 位 Windows 运行 32 位 x86 应用的兼容层；它是否预装，直接决定依赖 32 位组件的服务器工作负载能否开箱运行。微软在 Ignite 2026 将 Windows Server 2028 定位为 Windows Server 的下一版本，并在官方预览中把默认强化的 Server Core 与新的安全基线列为其核心设计方向。

**「服务器兼容性影响与应对」** 据微软公布的时间表，Windows Server 2028 将默认不包含 WoW64，因此依赖 32 位组件的业务在部署或升级前可能直接启动失败；管理员应先盘点相关依赖，并通过按需功能恢复 WoW64（Server Core 可使用 PowerShell 或 DISM），或改用兼容的 64 位版本。该变化目前仍是未来版本的发布计划，Windows 11 现阶段仍保留 WoW64，微软尚未公布其移除计划。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/windows-server/get-started/whats-new-windows-server-2028">Windows Server 2028 Preview: New features | Microsoft Learn</a></li>
<li><a href="https://techcommunity.microsoft.com/discussions/windowsserverinsiders/windows-server-2028-preview-resources---windows-server-vnext/4574213">Windows Server 2028 preview resources - Windows Server vNext</a></li>
<li><a href="https://techcommunity.microsoft.com/blog/windowsservernewsandbestpractices/windows-server-2028-a-trusted-foundation-for-an-evolving-enterprise/4574112">Windows Server 2028: A trusted foundation for an evolving ...</a></li>
<li><a href="https://thecommunity.ru/microsoft/windows/server/12123-windows-server-2028-po-umolchaniju-ne-budet-podderzhivat-32-bitnye-prilozhenija.html">Windows Server 2028 по умолчанию не будет поддерживать...</a></li>

</ul>
</details>

**标签**: `#Windows Server 2028`, `#WoW64`, `#32位应用兼容性`, `#按需功能`, `#遗留软件迁移`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [不确定时，多做实验](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 6.0/10

rss · Sean Goedecke · 11月23日 00:00

**「背景」** 当需求、系统或团队关系都不清晰时，作者认为等待完整理解并非最优解，单线深入可能只是在错误方向上投入。他把这种主动试错称为“乱试”，但提醒漫无目的的尝试会损害声誉，成败取决于能否从反馈中迅速转向。

**「方案」** 他的做法是同时试验多个方案，细听专家和现实指标（如延迟、用户指标）的反馈，并立刻放弃没有正向、甚至没有“惊喜”反馈的选项；多备路线也能减少对单次尝试的投入。产品上，已退役的 GitHub Models 中许多功能和集成失败，但用 GitHub Actions token 运行 AI 推理意外获得黏性，成为 Continuous AI 的种子；新产品应先广泛试探，再重投有牵引力的方向。工程上，他主张对纠缠、庞大或快速变化的系统并行提出推测性改动，观察表现后只深化确有改善者，AI 代理也可用于快速生成多个重构候选。组织上，他用自动化、接手任务或长期方案打破团队失联或不满难以表达的僵局；这里尤其要敏锐捕捉人的反馈，迅速撤回失败行动才能建立信任。作者主要用个人经历和示例支撑这些主张，未提供量化比较，也未充分展开失败成本与风险边界。

**「启示」** 作者的核心主张是：不确定时不要把自己绑定在单一计划上，而应并行试探、敏锐读取反馈并快速止损，再把资源集中到真正奏效的方向。

**标签**: `#experimentation`, `#feedback loops`, `#technical decision-making`, `#product development`, `#engineering management`

---

<a id="item-tech-blog-2"></a>
### [解读 OpenAI 困惑度曲线](https://seangoedecke.com/notes-on-openais-perplexity-reveal/) ⭐️ 6.0/10

rss · Sean Goedecke · 11月23日 00:00

**「背景」** OpenAI 发布了其已发布模型的困惑度曲线，作者认为这是前沿实验室罕见地公开内部训练指标，对安全透明度意义重大。困惑度只衡量模型对特定留出文本的预测，作者因此提醒：不同数据集的曲线不可直接比较。

**「方案」** 作者指出，前沿模型据传闻仅将一半或更少的训练时间和算力用于预训练，其余主要投入 RL；因此困惑度最多间接反映底座能力，看不到思维链使用、迎合性等后训练收益。图中极少有模型共享同一基础困惑度，他据此质疑“许多模型来自同一底座后训练”的传闻，并指出 GPT-4.1 与 o3 共享底座。GPT-4.5 与 GPT-5.3-Codex 困惑度相近却实用感悬殊，令他猜测 OpenAI 遇到预训练扩展墙或主动停止扩大底座；而 GPT-5.2 后的加速下降，则反驳了实验室已放弃预训练的流行说法。对齐方面，除非持续公布未发布底座的数据，否则外部无法监测可能的危险突变，跨实验室阈值也必须先披露留出集细节。体验上，GPT-3.5 到 GPT-4 的跃升及随后直到 GPT-5.5 的停滞大致符合他的感受，但他未感到 GPT-5.5 大跃升；他认为 o3 和 GPT-5.3-Codex 才是关键跃升，差异可能来自 RL 对思维链和迎合性的改善。

**「启示」** 作者的核心判断是：曲线显示 OpenAI 的预训练底座仍在快速进步，但困惑度受评测集限制且不覆盖完整能力，不能单独用来判定模型血缘、扩展瓶颈或对齐风险。

**标签**: `#language-model evaluation`, `#perplexity`, `#pretraining and post-training`, `#AI transparency`, `#model scaling`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [亚洲多地调整交易规则应对市场波动](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

报道称，美国 AI 科技股出现大规模抛售，纳斯达克指数单日下跌 5.28%，费城半导体指数跌近 11%。亚洲多地调整交易和卖空规则：中国内地下调融资保证金最低比例至 80%，韩国自 11 月 24 日起放宽上市公司每日回购订单数量限制 3 个月，中国台湾地区自 11 月 23 日起全面禁止在平盘价以下卖空，并将融券保证金比例从 130%升至 150%。

telegram · zaihuapd · 11月22日 13:24

**「背景」** 此前，有关人工智能板块恐慌的报道显示，以科技股为主的纳斯达克 100 指数单日下跌 5.6%、全周累计下跌 10.4%，为六年来最差一周；亚洲多地随后调整融资保证金、卖空和稳定机制，以应对这轮波动。

**「市场影响」** 按报道，中国内地融资交易者因最低保证金降至 80%可减少保证金资金占用；中国台湾地区融券保证金升至 150%、禁止平盘以下卖空并鼓励出借机构暂停新增借券，将限制当地卖空及部分对冲操作；韩国放宽回购订单限制并加强信用交易监控，将影响上市公司回购安排和交易审查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.guancha.cn/GuoJi%C2%B7ZhanLue/2026_11_21_909399.shtml">AI恐慌爆发，华尔街震荡， 美 国 科 技 股 跌 入熊市</a></li>

</ul>
</details>

**标签**: `#美股科技股`, `#半导体市场`, `#亚洲股市`, `#卖空监管`, `#市场稳定措施`

---

<a id="item-finance-news-2"></a>
### [厄尔尼诺海温创纪录，粮食援助承压](https://www.wired.com/story/how-this-years-super-el-nino-will-worsen-global-hunger/) ⭐️ 7.0/10

据伯克利地球气候学家 Zeke Hausfather，用于衡量厄尔尼诺强度的中热带太平洋升温指标截至 10 月已达 3.5℃，高于此前约 2.75℃的纪录，预计初冬升至约 4℃。世界粮食计划署 8 月警告，本轮厄尔尼诺可能到 2027 年底前使另外 4900 万人陷入急性粮食不安全、总数达到 2.74 亿，而全球援助资金 2025 年较 2022 年峰值下降了 30%。

telegram · zaihuapd · 11月22日 14:09

**「背景」** 世界粮食计划署今年 8 月已警告，本轮厄尔尼诺可能到 2027 年底令急性粮食不安全人口增加 4900 万、总数达到 2.74 亿，其影响途径包括降雨异常和农作物生长受扰。与此同时，全球援助资金 2025 年较 2022 年峰值下降 30%；索马里遭遇类似旱情时，该机构可覆盖的人数从 1000 万降至不足 100 万。

**「旱灾地区粮食援助覆盖收缩」** 全球援助资金从 2022 年峰值至 2025 年下降 30%且仍在下滑，削弱世界粮食计划署等机构在旱灾地区发放粮食的能力；在索马里类似旱情下，该机构可覆盖人数从 2022 年的 1000 万降至不足 100 万，依赖援助的家庭面临更大的粮食支持缺口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://e360.yale.edu/features/super-el-nino-agriculture">How This Year&#x27;s Super El Niño Will Worsen Global Hunger - Yale E360</a></li>
<li><a href="https://www.nytimes.com/2026/08/12/climate/el-nino-early-onset-effects.html">Effects of Record -Breaking El Niño Are Happening on 3 Continents...</a></li>
<li><a href="https://www.wired.com/story/how-this-years-super-el-nino-will-worsen-global-hunger/">How This Year’s Super El Niño Will Worsen Global Hunger | WIRED</a></li>

</ul>
</details>

**标签**: `#厄尔尼诺`, `#粮食安全`, `#世界粮食计划署`, `#气候冲击`, `#人道主义援助`

---

<a id="item-finance-news-3"></a>
### [蚂蚁集团领投 Simplexity Robotics 1 亿美元融资](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 7.0/10

蚂蚁集团领投中国具身智能公司 Simplexity Robotics 的 1 亿美元 Pre-A 轮融资，将公司投后估值推至 16 亿美元，高于今年 3 月披露的逾 10 亿美元。

telegram · zaihuapd · 11月23日 02:02

**「背景」** Simplexity Robotics 于 2025 年 7 月在杭州成立，核心团队来自理想汽车；截至 2026 年 3 月，公司已披露成立半年内完成五轮融资、累计融资 20 亿元人民币，投后估值超过 10 亿美元。

**「影响」** 这轮融资将支持 Simplexity Robotics 扩展人形机器人业务，直接影响其与宇树、优必选等成熟厂商争夺中国市场的能力。

**标签**: `#具身智能`, `#融资`, `#蚂蚁集团`, `#人形机器人`, `#中国科技`

---