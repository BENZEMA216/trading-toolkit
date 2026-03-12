# BENZEMA216 Trading Toolkit

> Personal trading toolkit — 4 tools covering the full trading lifecycle.

## Tools

| Tool | What it does | Phase |
|------|-------------|-------|
| [stock-analyst](https://github.com/BENZEMA216/stock-analyst) | 盘前五大指标 + 量化模块（粒子滤波/蒙卡期权/VaR） | Pre-market |
| [benzema216-council](https://github.com/BENZEMA216/benzema216-council) | 21位中美投资大师群体智能决策（B216 Score） | Decision |
| [candlestick-pdf-tool](https://github.com/BENZEMA216/candlestick-pdf-tool) | K线图 PDF 生成 + Gemini 技术分析 | Analysis |
| [tradingcoach](https://github.com/BENZEMA216/tradingcoach) | 交易复盘：多券商导入 + 8维评分 + AI 行为分析 | Post-trade |

## Workflow

```
         盘前                    决策                    执行                    复盘
    ┌──────────┐          ┌──────────────┐         ┌──────────┐         ┌──────────────┐
    │  stock-  │   VIX    │  benzema216  │  B216   │  candle- │   K线   │   trading-   │
    │ analyst  │─── OK ──▶│   council    │─ Score ─▶│stick-pdf │─ chart ─▶│    coach     │
    │          │  五大指标  │  21位大师投票  │  +0.3↑  │          │  技术面  │  8维评分复盘  │
    └──────────┘          └──────────────┘         └──────────┘         └──────────────┘
     /stock-analyst         /b216                                        tradingcoach
```

## Claude Code Skills

All tools are available as Claude Code skills — no API key needed:

```bash
# 盘前分析
/stock-analyst

# 投资大师决策会
/b216 想买小米，怎么看？

# 统一入口（路由到子工具）
/trading pre-market
/trading council 持仓: AAPL 100股，想买 TSLA
```

## Quick Start

```bash
# Clone all tools
gh repo clone BENZEMA216/stock-analyst
gh repo clone BENZEMA216/benzema216-council
gh repo clone BENZEMA216/candlestick-pdf-tool
gh repo clone BENZEMA216/tradingcoach

# Or install individual tools
cd benzema216-council && pip install -e .
cd stock-analyst && pip install -r requirements.txt
cd candlestick-pdf-tool && npm install
cd tradingcoach && pip install -r requirements.txt && cd frontend && npm install
```

## Philosophy

不追求全自动交易。每个环节都需要人的判断，工具负责提供**信息密度更高的输入**和**结构化的分析框架**。

- **盘前**: 5 个宏观指标判断市场温度，不做预测
- **决策**: 21 位大师各抒己见，群体智慧 > 个人直觉
- **分析**: K 线技术面补充基本面盲区
- **复盘**: 量化交易行为，找到系统性偏差
