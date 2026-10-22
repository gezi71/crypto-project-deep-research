# 完整研究报告模板

按以下顺序覆盖全部模块；可结合项目调整篇幅，但不能静默省略。每项重要事实/数据就近附来源、日期/期间与 Fact/Estimate/Interpretation/Assumption。表格是工作骨架，交付时填实、写限制，不保留空行占位。

默认将本模板分别用于中文和英文完整报告；两份报告内容覆盖与关键判断一致。另按 [delivery-and-social.md](delivery-and-social.md) 生成中英文帖文，不以帖文或英文摘要替代完整报告；用户指定交付范围优先。

## 报告头部

- 项目、Symbol、模式、类别、研究截止时间/时区、抓取时间、估值期限、币种。
- 官网、Docs、X、GitHub、链/chain ID、合约/原生资产、版本和研究边界。
- 数据可得性与重要限制。

## 1. Executive Summary

简明回答：项目是什么、解决什么问题、为何值得研究、关键数据、最大优势、最大风险、Token 价值捕获、估值水平。

列核心指标快照：Price、MC、FDV及其定义、流通/总/最大供应、适用的使用指标、Revenue、持币人可获得价值、下一重大解锁；逐项标日期。

**Core Thesis**：1–3 句话陈述价值创造、归属、定价与关键依赖。

## 2. What Problem Does It Solve?

需求、旧解决方式、区块链必要性/营销包装、选择理由、Switching Cost，以及“如果明天消失，哪些用户受到什么影响”。

## 3. Product

核心产品/外围产品、结构、用户流程、使用场景、用户类型、体验和成熟度。明确亲自体验、Docs 推断或第三方描述；未体验不能声称实测。

## 4. Market

赛道、当前规模、增长、趋势、Crypto Native 与潜在 TradFi/Web2 市场。TAM 用可服务客户×需求/支出等自下而上估算，区分 TAM/SAM/现实可得份额，不照抄项目宣传。

## 5. Business Model / Protocol Economics

资金流图：用户 → 协议 → LP/Validator/Operator → Treasury/持币人；激励另列。

表中拆 Fees、Revenue、Protocol Revenue、Supply-side Revenue、Take Rate、Gross Margin、Costs、Incentives、Token Emissions；解释口径与收入最终归属。

## 6. Fundamental Metrics

应用 sector-metrics 的对应指标。列 30D、90D、180D、1Y、前一等长窗口变化、数据范围和来源。存量列期末，流量列期间总额；DAU/MAU 等明确聚合。窗口缺失明确写出。

回答哪些数据能证明需求、付费、留存和经济可持续，避免只报单日快照。

## 7. Quality of Growth

用户/收入/TVL 增长，价格/净流入效应，补贴、空投、挖矿、Sybil，激励结束后的留存。计算可支持的 Revenue/Incentives、Fees/Token Emissions；有机比例必须先定义，无法估计说明原因。

## 8. Tokenomics

Max/Total/Circulating Supply 及方法；Team、Investors、Community、Treasury、Foundation、Ecosystem、Airdrop 的互斥分配表；cliff、vesting 规则及证据。

| 期限 | 累计解锁 | 解锁中未计流通部分 | 独立新增排放 | 从流通销毁/其他变动 | 预计流通 C_H | 相对当前流通增幅 | 假设/来源 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 3个月 | | | | | | | |
| 6个月 | | | | | | | |
| 12个月 | | | | | | | |
| 24个月 | | | | | | | |

## 9. Token Value Capture

逐项检查 Fee Sharing、Buyback、Burn、Staking Yield、Validator Requirement、Governance、Collateral、Gas、Security、Liquidity Requirement，使用 analysis-methods 的机制表。

拆分 Real Yield / Token Emission Yield、当前执行/未来提案。明确“协议成功是否必然使持币人受益”“收入增长 10 倍，持币人获得什么”。

## 10. Token Supply Pressure

团队、投资者、基金会、Treasury、空投、验证者、挖矿/流动性激励的潜在供应；Annual Token Inflation、潜在出售情景、流动性承接与来源。解锁不等于出售。

## 11. Team

Founder、核心团队、技术/行业经验、过往项目与交付。匿名、失败项目、Rug 历史/指控、争议分别核查；列事实、回应、未知，避免无来源指控。

## 12. Investors & Funding

| 日期/轮次 | 金额/币种 | 工具/权利 | 估值及对象 | 投资者 | Token 成本是否可计算 | 来源 |
| --- | --- | --- | --- | --- | --- | --- |

仅有依据时估算 VC Entry Valuation、Token Entry Price，与同权利/供应口径的当前 MC/FDV 比较。不把股权融资等同 Token 成本。

## 13. Treasury

Size、钱包/实体、Stablecoins、Native Token、ETH/BTC、受限资产、负债、支出。Liquid Treasury 与 Token Treasury 分表，给 Runway 或无法计算的原因。不以自家 Token 全额市价算现金。

## 14. Competition

3–5 个真实竞争对手；不足解释。

| Project | TVL | Volume | Revenue | Users/地址定义 | MC/FDV | Market Share/边界 | Growth/期间 | Token Value Capture | 时点/来源 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

保留不适用列并说明，选择真正决定竞争的比较指标。回答用户为何选择本项目。

## 15. Moat

检查 Network Effects、Liquidity、Data、Brand、Distribution、Developer Ecosystem、Switching Cost、Technology、Regulatory Advantage、Capital Efficiency。区分 Temporary Advantage / Structural Moat，每项给维持条件与可侵蚀证据。

## 16. Decentralization

Validator Count/控制集中、Sequencer、Admin Keys、Multisig 阈值与签名人独立性、Timelock、Token 集中、团队和 Upgrade Control；给实际控制链条而非仅节点数量。

## 17. Security

审计/版本/范围/未解决项、Bug Bounty、Oracle、Bridge、合约、经济与多签风险。未公开事故不等于无风险，不能声称完成代码审计。

| 事故日期 | 损失/计量口径 | Root Cause | Compensation | 修复/协议变化 | 来源/仍存风险 |
| --- | --- | --- | --- | --- | --- |

## 18. Governance

提案流程、Voting、参与、分布、鲸鱼/基金会控制、委托、quorum、否决权、实际执行。判断治理是否真正控制费用、升级、Treasury，区分链上约束与多签代执行。

## 19. Regulation

按相关司法辖区/日期检查证券属性争议、Stablecoin、Derivatives、KYC/AML、地域限制和业务可持续影响。区分立法、提案、执法主张、判决；只做风险分析，不作未经证实的法律定性。

## 20. Relative Valuation

同时列 MC/FDV；FDV/Revenue、MC/Revenue、FDV/Fees、MC/TVL、FDV/TVL；适用时 P/E、P/S、EV/Revenue。统一期间、供应和权利，解释增长/风险/捕获差异，不用低倍数直接等同便宜。

## 21. Historical Valuation

数据允许时列 1 年/2 年 FDV、Revenue Multiple、TVL Multiple，说明 Low/Normal/High 判断依据、分位与口径变更。缺数据保留限制，不反向补造历史。

## 22. Scenario Valuation

Bear / Base / Bull 并排，明确 Users、Volume、Revenue、Market Share、Multiple、Supply、持币人归属与全部假设；不适用写明。

每列推导 Implied MC、Implied FDV、Implied Token Value，注明估值期限与现价时点。使用 analysis-methods 的一致公式。Deep Dive 加二维敏感性；无可靠输入给模型和缺口，不给单点价格预测。

## 23. Catalysts

按 0–3 个月、3–12 个月、1–3 年分组。

| 事件/日期或区间 | 已确认/计划/推测 | 前置依赖 | 改变什么指标或权利 | 已计价证据/未知 | 来源/落空风险 |
| --- | --- | --- | --- | --- | --- |

检查 Mainnet、产品上线、Token Upgrade、Fee Switch、Buyback、ETF、Listing、Partnership、Regulation、New Chain、Institutional Adoption；相关才展开。合作由双方或真实集成核验，不能把传闻写确定日期。

## 24. Risks

至少 5–10 个实质风险，覆盖 Technology、Competition、Tokenomics、Regulation、Liquidity、Centralization、Governance、Execution、Market；可合并相关风险但不遗漏重要暴露。

| 风险 | 发生路径 | Probability/期限/依据 | Impact/受影响权益 | 领先信号 | 缓释/剩余风险 | 证据 |
| --- | --- | --- | --- | --- | --- | --- |

无概率统计依据使用 High/Medium/Low 的定性分类，不编精确概率。

## 25. Red Flag Checklist

每项状态为 已发现 / 未发现（说明检查范围）/ 未知 / 不适用，附证据与严重性，不用未勾选暗示安全。

- Extreme FDV；Low Circulating Supply；Large Unlock。
- Fake Volume；Incentive-dependent TVL；Unsustainable Yield。
- Insider Concentration；Anonymous Team；Admin Key。
- Token Has No Value Capture；Revenue Very Low。
- Treasury Selling；Excessive Marketing；Dubious Partnerships。

“高/低/极端”需要同赛道、供应、历史或经济阈值依据；匿名、管理密钥等是风险线索，不能单项自动判定欺诈。

## 26. Bull Case vs Bear Case

分别给最强论证：关键因果链、支持证据、必要假设、反证。禁止 Strawman，也不能把所有利好当已实现。

## 27. Consensus & Variant Perception

Consensus View、Bull Consensus、Bear Consensus 的样本/时期/来源及代表性。没有可靠共识数据就说明。

Variant Perception：市场可能忽略/高估什么、为什么、什么新证据会验证、何时反映。观点不同本身不是信息优势，不编造“市场都认为”。

## 28. Scorecard

按 scoring.md 输出 Project Quality、Product、Growth、Economics、Tokenomics、Token Value Capture、Moat、Team、Decentralization、Valuation、Risk 的 0–10 或 N/A，逐项附证据、理由和信心。

给 Overall Score、计算方式/覆盖率，并重申评分为研究框架，不代表投资建议。Risk 高分=更安全，Valuation 高分=价格更有吸引力。

## 29. 最终 12 问

1. 这个项目真正的核心是什么？
2. 是否拥有真实用户？
3. 是否拥有真实收入？
4. 收入增长是否健康？
5. Token 是否捕获价值？
6. Tokenomics 是否健康？
7. 最大潜在卖压是什么？
8. 最大竞争优势是什么？
9. 最大风险是什么？
10. 当前估值合理吗？
11. 什么情况下 Bull Case 成立？
12. 什么情况下 Thesis 被证伪？

逐项明确回答，可答未知并说明缺什么证据；不要重复摘要代替回答。

## 30. Research Verdict & Confidence

分别给 `Protocol: [Verdict]` 与 `Token: [Verdict]`，仅用 Exceptional / Strong / Interesting / Neutral / Weak / Avoid。未发币时 Token 标“不适用（未发行）”，不强给评级。

附 Business Quality、Token Quality、Token Valuation 的独立说明。Confidence 只用 High / Medium / Low，列可靠数据、缺失、冲突和依赖假设，以及可能改变 Verdict 的条件。

监测表给指标、当前基线/日期、触发条件、频率、核验来源；频率只是研究计划，不自动创建提醒或定期任务。

## 31. Source Appendix & Research Workpapers

完整来源按 Official / On-chain / Financial Data / Third Party Research / News / Interviews 分类，列标题、直链、发布/数据日期、抓取时间与支持命题。报告正文仍须就近引用。

附证据台账、差异/缺口表、计算底稿，或链接同目录实际文件。不得生成未使用的装饰性来源。
