# Bollinger Band Mean Reversion with Meta-Labeling

This project implements a **Bollinger Band mean-reversion strategy** on E-mini S&P 500 futures data and applies **meta-labeling** to improve the quality of trading decisions.

The key idea is to separate two decisions:

1. **What direction should the trade take?**
2. **Should the trade be taken at all?**

The Bollinger Band strategy acts as the **primary model** and determines the trade side. A Random Forest then acts as the **secondary model**, filtering those signals and deciding whether to trade or pass.

---

## Project Objective

The objective is to demonstrate how a traditional trading strategy can be combined with machine learning using a meta-labeling framework.

Instead of asking the machine-learning model to predict market direction directly, the workflow is:

```text
Bollinger Band Signal
        ↓
Long / Short Decision
        ↓
Triple-Barrier Labeling
        ↓
Meta-Labels
        ↓
Random Forest
        ↓
Trade / Pass