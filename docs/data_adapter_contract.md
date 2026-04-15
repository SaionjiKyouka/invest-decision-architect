# 数据适配器接口约定

这个文件不是代码实现，而是为了以后接真实数据源时不返工。

## 一、股票数据接口

输入：
- ticker
- market
- currency

输出字段建议：
- name
- sector
- industry
- price
- market_cap
- enterprise_value
- pe_ttm
- pb
- ps_ttm
- ev_ebit
- ev_ebitda
- fcf_yield
- revenue_ttm
- ebit_ttm
- net_income_ttm
- fcf_ttm
- gross_margin
- operating_margin
- net_margin
- roe
- roic
- debt_to_equity
- net_debt_to_ebitda
- interest_coverage
- revenue_cagr_5y
- eps_cagr_5y
- shares_outstanding_trend
- dividends_record
- buyback_record

## 二、基金 / ETF 数据接口

输入：
- ticker
- fund_name

输出字段建议：
- asset_type
- strategy
- benchmark
- expense_ratio
- aum
- avg_daily_volume
- top_holdings
- sector_weights
- country_weights
- duration
- yield
- tracking_error
- total_return_1y
- total_return_3y
- total_return_5y
- volatility_3y
- max_drawdown_5y
- distribution_policy

## 三、持仓复盘输入接口

用户侧应允许输入：
- ticker
- buy_price
- buy_date
- thesis
- current_position_pct
- max_drawdown_tolerance

## 四、组合构建输入接口

用户侧应允许输入：
- capital
- monthly_contribution
- age
- risk_tolerance
- horizon_years
- needs_income
- account_type

## 五、降级兼容原则

当真实数据源未接入时：
- 不返回伪造字段
- 缺什么就明确标空
- 允许进入框架分析模式
- 禁止把缺失字段自动补成默认值

## 六、未来可接入的数据源方向

- Yahoo Finance 类行情源
- Alpha Vantage / Finnhub / Polygon 等API
- SEC / 公司年报 / 交易所公告
- ETF issuer 官方页面
- fund factsheet / annual report

## 七、最重要的约束

这个 Skill 的强项应该是：
- 决策结构
- 风险识别
- 结论约束

而不是：
- 假装自己已经拿到全部数据
