# Post-Trade Workflow

交易执行后的复盘流程。

## Flow

```
1. 记录交易 (tradingcoach)
   ├── 导入券商 CSV（富途/老虎/中信/华泰）
   └── 或手动录入

2. 质量评分 (8 维)
   ├── Entry timing
   ├── Exit timing
   ├── Trend alignment
   ├── Risk management
   ├── Position sizing
   ├── Holding period
   ├── Plan adherence
   └── Behavioral score

3. 技术面复盘 (candlestick-pdf-tool)
   ├── K 线图 PDF
   └── 关键形态标注

4. 决策回顾
   ├── 当时 B216 Score 是多少？
   ├── 哪些大师对了？哪些错了？
   └── 下次同类交易的改进点
```

## Weekly Review

每周末汇总：
- 本周胜率 / 盈亏比
- Brier Score（预测准确度）
- 最大亏损交易的根因
- 行为模式偏差（追涨/恐慌卖出/过早止盈）
