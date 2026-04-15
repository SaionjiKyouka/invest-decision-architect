# adapters

这个目录用于以后接入真实数据源。

当前阶段先放接口骨架说明，不放真实密钥，不绑定具体供应商。

## 计划中的适配器
- stock_data_adapter_spec.yaml
- fund_data_adapter_spec.yaml
- position_input_schema.json
- portfolio_input_schema.json

## 原则
- 接口先行
- 数据源可替换
- 缺字段就显式留空
- 不做伪造回填
