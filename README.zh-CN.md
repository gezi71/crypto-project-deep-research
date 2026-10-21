# Crypto Project Deep Research

**以证据为先的加密项目深度研究：从协议基本面到 Token 价值捕获。**

[English](README.md) · 简体中文

一套可复用的 Agent Skill，适用于加密项目、协议、Token、公链、DeFi、基础设施和 Crypto 公司。它指导 Agent 完成来源核验、协议经济、增长质量、供应稀释、估值与风险分析，并分别评价协议和 Token。

核心问题：**价值从哪里来，谁为它付钱，谁最终获得价值，什么证据会推翻研究判断？**

## 研究范围

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

也支持中文自然语言请求。同名项目或 Token 容易混淆时，请补充官网，或链与合约地址。

可指定研究截止时间、输出语言、估值期限、币种和输出目录。默认当前时点、中文、USD、12 个月估值期限。如需英文报告，附加 `Write the report in English.` 即可。

**语言说明**：可执行指令和参考文件目前为中文；README 提供中英双语，Skill 指示 Agent 跟随用户指定的报告语言。

## 研究产出

[完整报告模板](references/report-template.md) 包含 **31 个模块**，覆盖：

1. 执行摘要、核心 Thesis、产品、市场和协议经济。
2. 基本面与增长质量，数据允许时分析 30D、90D、180D、1Y。
3. Tokenomics、价值捕获、潜在卖压情景、融资和 Treasury。
4. 竞争、护城河、去中心化、安全、治理和监管风险。
5. 可比、历史和情景估值，催化剂、风险及多空论证。
6. 11 项评分、最终 12 问、协议/Token 独立评级、Confidence 和完整来源。

报告同时提供**证据台账、差异/缺口表、计算底稿**，可作为附录或配套 Markdown/CSV 文件。不适用的部分解释原因，不用虚构数字填表。

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
├── SKILL.md                         # 入口、流程、四种模式和交付检查
├── agents/openai.yaml               # 显示信息与默认调用提示
├── references/
│   ├── evidence.md                  # 来源、时间、核验和底稿
│   ├── analysis-methods.md          # 经济、供应、Treasury 和估值公式
│   ├── sector-metrics.md            # 按业务类型选择指标
│   ├── report-template.md           # 完整 31 模块报告框架
│   └── scoring.md                   # 评分、评级和 Confidence
├── README.md
└── README.zh-CN.md
```

## 使用条件与验证范围

这是**指令型 Skill**，不提供行情服务，不是交易机器人，也不是独立运行的程序。实时研究需要所在 Agent 提供联网、公开 API、区块链浏览器或连接器。商业数据不是强制依赖，来源不可访问时须说明。研究流程不需要钱包签名或交易。

已检查结构、内部引用、元数据和计算示例，**尚未验证一次完整的真实项目研究**。安装命令用于分发说明，未在当前环境中完成端到端安装测试。实际质量取决于数据可得性和执行 Agent，产出仍需复核。

评分与情景估值仅为研究工具，不构成投资建议、价格保证、法律意见或智能合约审计。
