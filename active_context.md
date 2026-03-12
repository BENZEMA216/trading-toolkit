# Active Context

> trading-toolkit — 4 工具统一入口

## 当前状态
- v0.1.0 已推送 GitHub (2026-03-12)
- `/trading` skill 已安装本地
- benzema216-council 0.1.0 已发布 PyPI
- 全部 5 个 repo GitHub topics 已补齐

## 下一步：回测框架

已讨论 B216 Council 回测方案，核心挑战是 LLM 知识污染（模型知道历史结果）。

提议的方案（待用户确认）：
1. **质量测试优先**（不测预测准确度，测推理质量）：一致性、分化合理性、极端检测、边缘区分
2. **前瞻测试**：用 knowledge cutoff 之后的交易积累样本
3. **半盲测试**：用冷门/虚构标的降低知识污染

计划建 `trading-toolkit/backtest/` 目录，包含测试脚本 + 15 个测试用例 YAML。

## 待办
- [ ] 用户确认后建回测框架
- [ ] PyPI token 已泄露，需用户删除旧 token

