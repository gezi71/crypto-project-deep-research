# Crypto Project Deep Research

**研究引擎优先，发布层可选：保持研究纪律，按需写作与配图。**

[English](README.md) · 简体中文

一套可复用的 Agent Skill，适用于加密项目、协议、Token、公链、DeFi、基础设施和 Crypto 公司。它指导 Agent 完成来源核验、协议经济、增长质量、供应稀释、估值与风险分析，并分别评价协议和 Token。

**Discover 热门项目发现**流程区分关注度上升与基本面改善，筛选下一步值得研究的候选。它不提供买入建议，也不自动对候选逐一执行完整深研。

核心问题：**价值从哪里来，谁为它付钱，谁最终获得价值，什么证据会推翻研究判断？**

## 你会得到什么

Analyze、Deep Dive、Compare、Update 默认交付 **Research Package（研究包）**：研究笔记、证据台账、差异/缺口表、计算底稿、数据/来源表、Thesis、Bull/Base/Bear、估值、风险、未解决问题与 Confidence。研究完成后停止，不自动生成公开文章。

只有明确请求文章或发布用途时，才进入可选发布层；以下能力全部保留：

| 文件 | 内容 |
| --- | --- |
| `article.zh-CN.md` | 围绕核心问题展开、有观点和叙事的中文研究长文。 |
| `article.en.md` | 论证深度、关键证据和反方一致的英文完整长文。 |
| `social-post.zh-CN.md` | 聚焦一个重要发现、可独立阅读的中文短文。 |
| `social-post.en.md` | 按英文阅读习惯表达同一发现与关键限制的短文。 |

所请求的文章保持原有质量标准：从值得关心的问题开头，展开证据、因果和反方，给出判断与观察方向。仅生成请求的语言和形式；笼统“写篇文章”采用沟通语言的长文。Discover 默认交付 Candidate Shortlist 及核验底稿后停止；同样只有明确请求时才生成文章。

研究包与文章均可零图、一图或多图，无图数配额。图表只有实质改善理解、验证、比较或沟通时才生成；来源、日期/期间、单位、分母、CSV、复现脚本与目检要求不变。不自动发布。

## 研究范围

- **候选发现**：近期信号、实际数据覆盖、热度与基本面的独立评价，以及继续研究的优先级。
- **身份核验**：官网、链、合约、版本、迁移，以及同名项目和资产。
- **业务基本面**：用户需求、产品、市场规模、竞争与结构性护城河。
- **经济实质**：区分 Fees、Protocol Revenue、供应侧收入、激励和有机增长证据。
- **Token 分析**：价值捕获、分配、归属计划，以及未来 3/6/12/24 个月累计供应变化。
- **估值**：同时分析 MC 与 FDV，进行可比、历史和 Bear/Base/Bull 情景估值，明确供应假设。
- **控制与风险**：团队、融资、Treasury、治理、去中心化、安全、监管和流动性。
- **研究判断**：最强多空论证、催化剂、红旗、预期差、Thesis 证伪条件与信心水平。

框架严格区分 **Protocol Quality、Business Quality、Token Quality、Token Valuation**。协议成功不代表持币人一定受益。

## 安装

使用 [Skills CLI](https://skills.sh/)：

```bash
npx skills add gezi71/crypto-project-deep-research --skill crypto-project-deep-research
```

按安装器提示选择 Agent 与安装范围。该命令需要 Node.js/npm 和网络连接。

也可以克隆仓库，让 Agent 读取 `SKILL.md`：

```bash
git clone https://github.com/gezi71/crypto-project-deep-research.git
```

请保留完整目录，入口依赖 `references/` 中的文件。也可将完整文件夹放入所用 Agent 支持的技能目录。

## 使用

在 Codex 中显式调用技能，并指定模式和项目：

```text
$crypto-project-deep-research Analyze: Aave
```

| 模式 | 示例 | 行为 |
| --- | --- | --- |
| Analyze | `Analyze: Aave` | 覆盖所有适用模块的完整研究。 |
| Deep Dive | `Deep Dive: Ethereum` | 增加实施证据、指标溯源、敏感性与反证分析。 |
| Compare | `Compare: Aave vs Morpho` | 对各项目使用一致的框架、时点、定义和估值假设。 |
| Update | `Update: Aave` | 与有日期的旧报告比较并重评 Thesis；没有基线时建立当前研究，明确无法确认变化。 |
| Discover | `Discover: 最近 30 天值得研究的 DeFi 项目` | 披露候选池和数据覆盖，核验信号，选择进一步研究的对象。 |

也支持中文自然语言请求。同名项目或 Token 容易混淆时，请补充官网，或链与合约地址。

可指定研究截止时间、输出语言、估值期限、币种和输出目录。默认当前时点、USD、12 个月估值期限。完整研究默认停在研究包：`Analyze: Aave` 不生成文章；`Analyze: Aave + write an English long-form article` 研究后只增加 `article.en.md`。自然语言意图明确即可，无须固定语法。明确指定逐模块报告、语言、篇幅或平台时按要求执行。

例如，明确请求双语长文，同时指定双语短文采用 X 串帖形式：

```text
$crypto-project-deep-research Analyze: Zama https://www.zama.org/
生成中英文长文；将中英文短文分别写成适合 X 发布的串帖。
```

### Discover：发现研究候选

```text
$crypto-project-deep-research Discover: 最近 30 天值得研究的 DeFi 项目
Discover: Trending crypto projects in the past 7 days
Discover: 最近基本面改善但市场关注较低的项目
```

可选参数：时间窗口、赛道、链、已发币/未发币、流通市值范围、排除项目、候选数量、输出语言。默认**最近 30 天、全赛道、不限链、已发币与未发币均可、不设市值限制与排除项，以沟通语言交付候选清单**。无固定候选数，用户指定数量视为上限。输出注明截止时间与实际数据覆盖，不声称扫描整个市场。

需要缩小范围时，直接用自然语言补充条件：

```text
$crypto-project-deep-research Discover: 最近 7 天值得研究的 DeFi 项目。
链：Ethereum、Base；仅已发币项目。
流通市值：1 亿至 50 亿美元；排除 Aave。
最多输出 5 个研究候选，使用中文。
```

宁可少而可信，不用弱线索填满名单。上限 5 个但仅 3 个合格时交付 3 个；零候选也合法，明确“暂无足够强的候选”，并说明检查范围与剔除原因。未发币或市值未知的项目不能被默认视为满足数值市值范围。

候选允许多标签：**热度驱动、基本面改善、催化剂驱动、潜在预期差**。关注低不等于低估，涨幅大不代表值得投资。增长比较前一等长窗口，同时列绝对规模和变化，检查低基数、补贴、Sybil、刷量、价格效应与一次性事件。

Discover 是研究优先级流程，不是发布流程。每个候选包含项目/赛道、带日期与具体证据的 Why Now、基本面信号、Token/价值捕获相关性、主要不确定性、关键研究问题、优先级、Confidence 和建议下一步；可用表格、卡片或段落。热门、涨价、社交讨论和叙事强度只能作为线索，不能单独充当基本面依据。

产出包括候选清单、独立的 **Attention / Fundamentals / Catalyst / Research Priority / Confidence** 评价、最多前三名研究卡片、来源/缺口底稿，以及可复制的 Analyze/Deep Dive 调用。Research Priority 表示“值得下一步调查”，不是预期收益或投资评级；缺数据用 N/A，必要时不排名，跨赛道排序须解释理由。Discover 回答下一步值得研究谁，Analyze 才建立完整研究和投资 Thesis。筛选级核验不支持 Buy/Sell/Avoid、低估/高估或明确赢家结论。下一步可为 Research、Watch、Low Priority、Drop，并给理由、关键问题与缺口；不自动执行 Analyze。

Discover 完成不意味着生成文章。只有明确请求“筛选后写文章”“做成 newsletter”“生成 social post”或“给我英文长文”等时，才进入可选发布层，仅生成所需版本。默认不配图，只有明显帮助候选比较或判断时才画，无数量配额。详见 [Discover 执行流程](references/discover.md)。

**语言说明**：可执行指令和参考文件为中文；研究包默认跟随沟通语言；文章语言与形式按请求。请求双语长文时，英文保持同等论证深度，不只是中文摘要。Discover 清单也默认跟随沟通语言，用户指定优先。过程消息跟随用户语言。

## 研究产出

完整研究使用的[底稿框架](references/report-template.md) 包含 **31 个模块**，覆盖：

1. 执行摘要、核心 Thesis、产品、市场和协议经济。
2. 基本面与增长质量，数据允许时分析 30D、90D、180D、1Y。
3. Tokenomics、价值捕获、潜在卖压情景、融资和 Treasury。
4. 竞争、护城河、去中心化、安全、治理和监管风险。
5. 可比、历史和情景估值，催化剂、风险及多空论证。
6. 11 项评分、最终 12 问、协议/Token 独立评级、Confidence 和完整来源。

31 模块是**覆盖与审计框架，不是固定推理顺序**。先识别核心经济问题与 Thesis 关键变量，沿因果链深查，再审计覆盖、补实质缺口。研究深度允许不对称：critical 深入、relevant 标准、low materiality 简述、not applicable 写 N/A 及原因、data unavailable 写缺口及影响。笔记可按项目逻辑组织，以覆盖矩阵映射全部模块，无须 31 个固定章节。

完整框架在 `research-notes.md` 中覆盖，另附**证据台账、差异/缺口表和计算底稿**，用 Markdown/CSV 保存。缺失或不适用项目在底稿说明；Discover 保留独立的筛选框架，不引入完整项目评级。公开文章按论点组织，无需复制模块标题。用户明确索要逐模块尽调报告时再交付该形式。

11 项整数分项评分保留为诊断工具；摘要优先呈现协议/业务质量、Token 价值捕获、增长、估值、稀释/治理风险及 Confidence 的定性画像。Overall Score 可省略，仅作次要的整数粗略诊断，保留原有证据门槛；不能替代 Thesis 或估值、自动导出 Buy/Avoid，或作为唯一排名依据。Compare 比较各维度，不比较小数差异。旧研究包和小数总分继续可读，无须迁移。

请求双语长文时，两篇长文保留核心论证、关键证据、最强反方和影响结论的不确定性。短文聚焦一个独立成立的发现，不将每个研究模块压成一句话；易读不能以事实失真为代价。详见[双语长短文写作规则](references/delivery-and-social.md)。

## 证据与计算规则

- 原始来源优先，关键指标尝试独立交叉验证。
- 区分 `Fact`、`Estimate`、`Interpretation`、`Assumption`。
- 动态数据注明时点或期间，披露冲突与缺失。
- 地址不等于用户，Fees 不等于持币人收益，解锁不等于实际出售。
- 无限供应资产不虚构最大供应，未发币公司不虚构 Token 估值。
- 估值权利、指标定义和供应分母一致，避免重复计算 Treasury、回购或销毁。
- 验证协议收入如何传导给持币人，不默认存在价值捕获。

## 目录结构

```text
.
├── SKILL.md                         # 入口、流程、五种模式和交付检查
├── agents/openai.yaml               # 显示信息与默认调用提示
├── references/
│   ├── evidence.md                  # 来源、时间、核验和底稿
│   ├── discover.md                  # 候选发现、筛选与研究优先级
│   ├── analysis-methods.md          # 经济、供应、Treasury 和估值公式
│   ├── sector-metrics.md            # 按业务类型选择指标
│   ├── report-template.md           # 完整 31 模块研究底稿
│   ├── delivery-and-social.md       # 双语长文与短文写作
│   ├── scoring.md                   # 评分、评级和 Confidence
│   └── data-charts.md               # 按需配图、数据与可复现性
├── README.md
└── README.zh-CN.md
```

## 使用条件与验证范围

这是**指令型 Skill**，不提供行情服务，不是交易机器人，也不是独立运行的程序。实时研究需要所在 Agent 提供联网、公开 API、区块链浏览器或连接器。商业数据不是强制依赖，来源不可访问时须说明。研究流程不需要钱包签名或交易。

Discover 不自动交易、不创建定时任务、不强制使用付费服务。缺乏可靠近期数据时披露限制，不编造热门榜单。

已检查结构、内部引用、元数据和计算示例。已于 **2026-10-22** 完成一次受限的 Zama Analyze 试跑，覆盖 31 模块框架、证据/缺口底稿和条件供给计算；这不代表已充分核验实时经济数据或合约状态。本次 Research First 流程已通过结构、链接检查和手工指令走查，**尚未端到端试跑**。仓库没有现成的自动化研究测试套件。安装命令也未在当前环境中完成端到端安装测试。实际质量取决于数据可得性和执行 Agent，产出仍需复核。

已于 **2026-10-21** 用真实的最近 30 天 DeFi 请求试跑 Discover，覆盖等长窗口重算、来源限制、未排名观察项及误导信号剔除。这次有限筛选不代表全市场覆盖，也不替代完整项目研究验证。

评分与情景估值仅为研究工具，不构成投资建议、价格保证、法律意见或智能合约审计。
