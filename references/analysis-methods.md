# 经济、供应与估值

## 1. 资金流与收入

按实际项目改画，每条边标资产、期间金额、证据和控制权：

```text
用户支付（交易费 / 利息 / 服务费）
  → 协议合约或运营主体
    → LP / 贷款人 / 验证者 / Operator（供应侧收入）
    → Treasury / 公司（保留收入）
    → 持币人（实际分红 / 已执行回购 / 销毁）
基金会 / Treasury / 新增发行
  → 用户或供应侧（激励，单列，不能伪装外部需求）
```

对账起点为 `User Fees = Supply-side Revenue + Protocol Revenue`，但不同平台定义不同，必须先映射。公司费用、链上费用、利息、清算收入分别核对，避免重复归集。

| 指标 | 定义/公式 | 限制 |
| --- | --- | --- |
| Fees | 用户支付毛额 | 成交额、存款、Token 销售收入不是 Fees。 |
| Protocol Revenue | 扣供应侧后协议/运营主体保留收入 | 核对是否含 Treasury 和持币人分配。 |
| Take Rate | 同期 Revenue / 适当业务基数 | DEX 可用 Volume；借贷余额与流量不可混用；另列 Revenue/Fees 保留比例。 |
| Gross Margin | (收入 − 已定义直接成本) / 收入 | 保留收入率不自动等于会计毛利率。 |
| 净经济收益估算 | Revenue − 未扣运营成本 − 未扣激励成本 | 披露现金/Token 成本边界，不冒充审计 Earnings。 |
| Annualized Revenue | 区间收入 / 天数 × 365 | Estimate；同时列 30D/90D 运行率及 TTM，剔除或单列异常事件。 |
| Revenue / Incentives | 同期同币种收入 / 激励成本 | 激励为零无有限倍数；未知不可算。 |
| Fees / Token Emissions | 同期 Fees / 排放 USD 成本 | 按排放时价格计量；仅有快照价格时标估算和敏感性。 |

补贴可能来自基金会、协议和第三方。排放是经济稀释成本，未必是现金流出；已扣费用不能再扣一次。总奖励与新发行分别计量。

## 2. 增长质量

- 列 30D/90D/180D/1Y 期间收入/费用/交易量、期末存量、前一等长窗口变化，有序列时补月度走势。
- TVL USD 变化拆为价格、净流入、收益累积与统计范围变化；不把 TVL 增长直接称为资金流入。
- 地址不等于人数，披露机器人、Sybil、交易所、多链去重与代理调用限制。优先真实付费、留存和重复使用证据。
- 比较激励前后、无激励产品与 cohort 留存；相关不等于因果。
- Organic Growth Ratio 无统一定义；仅能辨别 cohort/激励时才定义代理，如“未接受已识别激励的活跃地址 / 全部活跃地址”，注明未知组、标签漏检。不能称其为真实有机用户比例。
- 无法识别补贴受益人时不算有机比例，用定性证据与代理说明。

## 3. 供应、解锁和卖压

同一快照：P=USD/Token，C0=流通，T0=总供应，M=可信最大供应。

```text
MC = P × C0
FDV = P × M（仅当存在有限可信上限）
Fully-issued proxy = P × T0（无上限时仅为总供应口径代理）
Forward diluted value(H) = P × T_H（明确期限与发行/销毁假设）
Circulating share = C0 / M（M 不适用另列 C0/T0）
Circulating inflation(H) = (C_H − C0) / C0
Net issuance rate(H) = (T_H − T0) / T0
```

无限供应不虚构 M。数据商 FDV 若用 T0，保留但标定义，不与 Max Supply 口径混用。

1. 分配列 Team、Investors、Community、Treasury、Foundation、Ecosystem、Airdrop；分类互斥，核对总和，避免基金会/生态 Treasury 重复。
2. 记录受益人、cliff、线性/分段规则、起止/时区、可撤销权；区分已归属、可领取、已领取、已进入流通。
3. 未来 3/6/12/24 个月列**累计**解锁、其中已计流通部分、流通增量假设、排放、销毁、C_H，累计列不能相加。
4. 解锁改变可转让性，不一定增加总供应；同一批 Token 的铸造、预铸解锁不能双计。
5. 卖压逐项看团队、投资者、基金会、Treasury、空投、验证者、挖矿和流动性激励。交易所充值不等于已卖出。
6. `Potential Sell Tokens = Σ 可出售数量 × 假设出售比例`，仅为情景；USD 值标价格假设。无出售比例依据则给范围，不编精确概率。
7. 与可信现货量、订单簿深度比较。名义成交量可能刷量，卖压/成交额不能机械映射跌幅。

## 4. Token 价值捕获

Fee Sharing、Buyback、Burn、Staking Yield、Validator Requirement、Governance、Collateral、Gas、Security、Liquidity Requirement 逐项填写：

| 机制 | 已运行/待执行/提案/叙事/不适用 | 付款人/资产 | 受益人 | 合约或法定权利 | 控制者/可撤销性 | 执行证据 | 价值泄漏/限制 |
| --- | --- | --- | --- | --- | --- | --- | --- |

- 逐段追踪“使用 → 支付 → 协议留存 → 持币人价值”，链条断裂则收入倍数不能证明 Token 便宜。
- Real Yield 来自可持续外部收入，Token Emission Yield 来自分配/发行；混合时拆比例、价格、锁定、罚没及复投假设。
- 使用 Token 支付不等于长期持有需求；检查周转、gas 抽象、替代抵押物、可绕开的质押。
- 回购可能抵消发行，不保证稀缺；销毁不是现金分红；治理权不自动赋予 Treasury/公司收入所有权。
- Revenue ×10 分别测试现行与拟议机制的受益人；没有分配路径不能假设强制分红。

## 5. 融资与 Treasury

- 逐轮列日期、金额/币种、股权/SAFT/Token/混合、估值、投资者、权利、来源。
- 只有能归属到具体 Token 数量与权利时，才算 `Token Entry Price = Token 对应投资额 / 获得 Token 数量`。股权估值不是 Token FDV；混合轮不能全当 Token 成本。
- 公司收入不能直接支持无公司收入权的 Token 估值。
- Treasury 列钱包/实体、限制、负债、Stablecoins、ETH/BTC、其他资产、Native Token。客户存款、抵押物、桥储备不是可支配资产。
- Liquid Treasury 与 Native Token Treasury 分开；自家 Token 单列数量/名义市值，不全部当可变现现金，可列明确折扣情景。
- `Runway(月) = 可动用净流动资产 / 可持续月净现金消耗`。净消耗≤0 无有限跑道；费用未知不可算。考虑脱锚、受限和不可用资产。

## 6. 可比与历史估值

同时列 FDV/Revenue、MC/Revenue、FDV/Fees、MC/TVL、FDV/TVL；不适用写原因。收入统一 TTM 或相同年化窗口，分母≤0 不报有意义的正倍数。

- Fees 是活动代理、TVL 是资产/使用代理，不代表持币人收益。
- P/S、P/E 只在收入/盈利对应被估值权益时使用，否则标诊断代理。
- EV/Revenue 仅在债务、现金、资产与权利边界可定义时用，不能机械 `FDV − DAO Treasury`。
- 同赛道仍需调整增长、风险、价值捕获、供应和流动性。要求的竞争表列均保留，非适用不强填。
- 历史用当时价格×当时对应供应，配同期可知收入，不用今天供应回填。最大供应也应当时已知。
- 有 1–2 年数据时给时间序列/分位，定义 Low/Normal/High 及结构变化；跌离 ATH 不等于便宜。

## 7. Bear / Base / Bull

每列说明估值日期 H、Users、Volume、Market Share、Take Rate、Revenue、成本、价值捕获比例、Multiple、C_H、T_H/M、假设来源；不适用说明。Users×人均收入与 Volume×Take Rate 若是同一收入不能相加。

选择一种主模型，保证权利/指标/供应一致：

```text
流通模型：可归属于流通权益的年度指标 × 对应 MC 倍数 = Implied MC_H
Price_H = Implied MC_H / C_H
Implied FDV_H = Price_H × M（或明确 T_H 代理）

完全稀释模型：面向全部稀释权益的年度指标 × 对应 FDV 倍数 = Implied FDV_H
Price_H = Implied FDV_H / M（或明确 T_H 代理）
Implied MC_H = Price_H × C_H
```

不能 FDV/C_H 或 MC/M。未验证价值捕获的收入模型只能称条件情景，不是 Token 基本价值结论。回购、销毁、分红对同一价值不能重复计价。

各情景说明倍数依据、供给推导、执行依赖、相对现价幅度与限制。缺数据给变量/缺口，不输出虚假数字；不给单一目标价，无依据不给精确概率。

### 公式自检（纯虚构，非市场数据）

P=$2、C0=100m、M=500m、90D Revenue=$9m：MC=$200m，FDV=$1bn，90D 年化 Revenue=$36.5m，FDV/年化 Revenue≈27.40×。

12 个月有 20m 尚未计流通的预铸解锁、10m 独立新增发行、2m 从流通销毁：C12=128m，流通增幅=28%。Total Supply 仅加新增发行减销毁，不能再加预铸解锁。

完全稀释模型假设 FDV=$600m、M=500m：Price=$1.20；若 C_H=128m，MC=$153.6m。此例只核对公式，不证明估值方法适合任何实际 Token。
