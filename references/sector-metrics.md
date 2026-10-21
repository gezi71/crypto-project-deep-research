# 按项目类型选择指标

只加载与对象相关的行。多产品按业务分部拆开后合并；不能用非适用指标填满报告。所有指标仍遵守日期、定义和核验规则。

| 类型 | 使用与收入重点 | 增长/安全/价值捕获检查 |
| --- | --- | --- |
| Spot DEX / 聚合器 | 真实交易量、付费交易者、交易笔数、流动性、滑点、Fees、LP 收入、Protocol Revenue、Take Rate、路由份额 | 洗量/自成交、MEV、补贴 LP、聚合器转发重复计量、Fee Switch 执行、协议与前端收入分离。 |
| 衍生品 / Perp | Volume、Open Interest、交易者、保证金/存款、Fees、清算、保险基金、坏账、LP PnL | OI 是存量不是交易量；交易者盈亏不是稳定协议收入；Oracle、ADL、市场操纵、极端行情。 |
| Lending / CDP | Deposits、借款余额、借款流量、利用率、利差、利息/费用、保留收入、坏账 | 循环借贷、抵押集中、清算深度、Oracle、风险参数、无补贴利率及净利差。 |
| Stablecoin | 净发行与流通、赎回、二级脱锚、储备、抵押率、资产期限、持有人、收益来源 | 抵押与净资产不能同 TVL 相加；储备所有权、证明/审计差异、赎回优先权、链上与银行风险。 |
| L1 | 真实付费活动、活跃地址、交易费、验证者收入/发行、质押、稳定币供给、开发者、应用留存 | 投票/系统交易剔除、机器人、状态增长、停机、客户端/质押集中、排放与销毁。TPS 与提交数不是需求。 |
| L2 / Rollup | 付费交易、地址、费用、排序器收入、L1/DA 成本、经济利润、桥接净流量、TVL/TVS | TVS 与 TVL 分开；证明/挑战机制、逃生路径、排序器、升级权、DA、公司收入与 Token 权利。 |
| Bridge / Interoperability | 桥接 Volume、净流入、独立用户/消息、费用、保留收入、锁定资产 | 往返刷量、跨链重复、信任模型、验证者/多签、跨链安全与消息真实性。 |
| Liquid Staking / Restaking | 底层净质押、赎回、独立存款人、基础质押收益、服务收入、Take Rate、Operator/AVS | 凭证与底层重复 TVL、多层再质押、罚没、退出流动性、积分补贴；基础链发行收益不自动归本项目 Token。 |
| Oracle / 数据 / DePIN / 存储 | 实际付费客户、请求/任务/数据量、真实容量利用、合同/链上支付、运营收入、Operator 成本 | “集成”不等于付费客户；供给上线不等于需求；硬件补贴、Token 支付补贴与现金收入分开。 |
| RWA / Tokenization | 净资产、发行/赎回、底层收益、管理费、活跃投资者、违约、到期结构 | 法律追索、托管/破产隔离、准入、估值滞后、链下审计、Token 与底层权利映射。 |
| 游戏 / 消费 / NFT | 留存、付费用户、ARPU、非 Token 收入、真实销售、创作者供给、复用 | 机器人/空投、NFT 自成交、Token 价格驱动消费、平台费和创作者收益分离。 |
| Crypto 公司 / 未发币基础设施 | 收入、客户、留存、毛利、现金消耗、融资、股权结构、合规 | 自营 Token、股权和客户资产分离；无 Token 不计算虚构 Token FDV；私营披露不足影响 Confidence。 |

至少检查用户需求清单中的 DAU/MAU、Active Addresses、Transactions、Volume、TVL、Deposits、OI、Borrow Volume、Stablecoin Supply、Bridge Volume，并按对象标适用或原因；不适用的指标不必建立空表。

财务至少检查 Fees、Revenue、Protocol Revenue、Annualized Revenue、Expenses、Incentives、Token Emissions、Earnings。盈利不可核实时写限制，不能由“收入减发行”直接称审计利润。

开发者数与 GitHub Commits 检查独立贡献、版本发布、审计修复与应用使用，不以提交次数替代技术质量。
