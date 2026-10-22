# Crypto Project Deep Research

**发现值得研究的加密项目，分析基本面与 Token 价值捕获，交付中英文完整报告和社交媒体帖文。**

[English](README.md) · 简体中文

一套可复用的 Agent Skill，适用于加密项目、协议、Token、公链、DeFi、基础设施和 Crypto 公司。它指导 Agent 完成来源核验、协议经济、增长质量、供应稀释、估值与风险分析，并分别评价协议和 Token。

**Discover 热门项目发现**流程区分关注度上升与基本面改善，筛选下一步值得研究的候选。它不提供买入建议，也不自动对候选逐一执行完整深研。

核心问题：**价值从哪里来，谁为它付钱，谁最终获得价值，什么证据会推翻研究判断？**

## 你会得到什么

每次研究默认交付四个独立 Markdown 文件：

| 文件 | 内容 |
| --- | --- |
| `report.zh-CN.md` | 覆盖所选模式要求的中文完整研究报告。 |
| `report.en.md` | 证据、范围和结论一致的英文完整报告。 |
| `social-post.zh-CN.md` | 围绕关键发现、可独立阅读的中文社交媒体帖文。 |
| `social-post.en.md` | 按英文阅读习惯编辑、表达同一论点的英文帖文。 |

两份报告共享证据台账、差异/缺口表和计算底稿。帖文保留关键风险、假设、日期与直接来源；默认每种语言一篇通用长帖，也可指定平台、篇幅或串帖格式。生成后供你审阅和发布，不自动操作社交账户。明确指定单一语言或仅需部分产物时优先遵守。

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

可指定研究截止时间、输出语言、估值期限、币种和输出目录。默认当前时点、USD、12 个月估值期限，每次分别交付中文报告、英文报告、中文社交媒体帖文和英文社交媒体帖文。明确指定单一语言、仅报告、仅帖文或特定平台/篇幅时优先遵守。

例如，在保留双语完整报告的同时指定帖文形式：

```text
$crypto-project-deep-research Analyze: Zama https://www.zama.org/
保留中英文完整报告，将中英文社交媒体帖文分别写成适合 X 发布的串帖。
```

### Discover：发现研究候选

```text
$crypto-project-deep-research Discover: 最近 30 天值得研究的 DeFi 项目
Discover: Trending crypto projects in the past 7 days
Discover: 最近基本面改善但市场关注较低的项目
```

可选参数：时间窗口、赛道、链、已发币/未发币、流通市值范围、排除项目、候选数量、输出语言。默认**最近 30 天、全赛道、不限链、已发币与未发币均可、不设市值限制与排除项、10 个候选、中英文报告和帖文各一份**。输出注明截止时间与实际数据覆盖，不声称扫描整个市场。

需要缩小范围时，直接用自然语言补充条件：

```text
$crypto-project-deep-research Discover: 最近 7 天值得研究的 DeFi 项目。
链：Ethereum、Base；仅已发币项目。
流通市值：1 亿至 50 亿美元；排除 Aave。
最多输出 5 个研究候选，使用中文。
```

证据只能支持更少候选时，结果会说明缺额原因。未发币或市值未知的项目不能被默认视为满足数值市值范围。

候选允许多标签：**热度驱动、基本面改善、催化剂驱动、潜在预期差**。关注低不等于低估，涨幅大不代表值得投资。增长比较前一等长窗口，同时列绝对规模和变化，检查低基数、补贴、Sybil、刷量、价格效应与一次性事件。

产出包括候选表、独立的 **Attention / Fundamentals / Catalyst / Research Priority / Confidence** 评价、最多前三名研究卡片、来源/缺口底稿，以及可复制的 Analyze/Deep Dive 调用。Research Priority 不是预期收益或投资评级；缺数据用 N/A，必要时不排名，跨赛道排序须解释理由。详见 [Discover 执行流程](references/discover.md)。

**语言说明**：可执行指令和参考文件为中文；交付默认中英双语，英文报告为完整版本而非摘要。过程消息跟随用户语言。

## 研究产出

完整研究使用的[报告模板](references/report-template.md) 包含 **31 个模块**，覆盖：

1. 执行摘要、核心 Thesis、产品、市场和协议经济。
2. 基本面与增长质量，数据允许时分析 30D、90D、180D、1Y。
3. Tokenomics、价值捕获、潜在卖压情景、融资和 Treasury。
4. 竞争、护城河、去中心化、安全、治理和监管风险。
5. 可比、历史和情景估值，催化剂、风险及多空论证。
6. 11 项评分、最终 12 问、协议/Token 独立评级、Confidence 和完整来源。

报告同时提供**证据台账、差异/缺口表、计算底稿**，可作为附录或配套 Markdown/CSV 文件。不适用的部分解释原因，不用虚构数字填表。Discover 使用独立的简洁输出，不强制完整报告或投资评级；Analyze、Deep Dive、Compare、Update 保留原有行为。

两份完整报告均保留所选模式的内容要求。帖文从研究中提炼一条清楚的论证，不逐章压缩报告；英文摘要不能替代英文完整报告。详见[双语交付与社交媒体编辑](references/delivery-and-social.md)。

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
│   ├── report-template.md           # 完整 31 模块报告框架
│   ├── delivery-and-social.md       # 双语报告与社交媒体帖文
│   └── scoring.md                   # 评分、评级和 Confidence
├── README.md
└── README.zh-CN.md
```

## 使用条件与验证范围

这是**指令型 Skill**，不提供行情服务，不是交易机器人，也不是独立运行的程序。实时研究需要所在 Agent 提供联网、公开 API、区块链浏览器或连接器。商业数据不是强制依赖，来源不可访问时须说明。研究流程不需要钱包签名或交易。

Discover 不自动交易、不创建定时任务、不强制使用付费服务。缺乏可靠近期数据时披露限制，不编造热门榜单。

已检查结构、内部引用、元数据和计算示例。已于 **2026-10-22** 完成一次受限的 Zama Analyze 试跑，覆盖 31 模块框架、证据/缺口底稿和条件供给计算；这不代表已充分核验实时经济数据或合约状态。新增的**双语四文件交付尚未端到端试跑**。安装命令也未在当前环境中完成端到端安装测试。实际质量取决于数据可得性和执行 Agent，产出仍需复核。

已于 **2026-10-21** 用真实的最近 30 天 DeFi 请求试跑 Discover，覆盖等长窗口重算、来源限制、未排名观察项及误导信号剔除。这次有限筛选不代表全市场覆盖，也不替代完整项目研究验证。

评分与情景估值仅为研究工具，不构成投资建议、价格保证、法律意见或智能合约审计。
