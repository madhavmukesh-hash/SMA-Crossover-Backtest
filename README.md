# SMA-Crossover-Backtest
A disciplined backtest of a simple SMA crossover strategy highlighting the gap between intuitive signals and realized performance under realistic assumptions.

# SMA Crossover Strategy — Empirical Evaluation

This repository presents a rigorous backtest of a Simple Moving Average (SMA) crossover trading strategy applied to equity market data.

The objective is not to optimize or “improve” the strategy, but to evaluate its performance under a clean and realistic research framework.

---

## Research Objectives

- Implement a technically correct SMA crossover strategy
- Construct returns using a log-return framework
- Account for transaction costs and position changes
- Compare performance against a buy-and-hold benchmark
- Evaluate both absolute and relative performance
- Quantify risk using drawdown and downside-risk metrics

---

## Methodology Overview

- **Returns** are computed in log space to ensure additivity  
- **Signals** generate long and short positions with lagged execution to avoid look-ahead bias  
- **Transaction costs** are applied per trade, including full position reversals  
- **Equity curves** are constructed via exponentiation of cumulative log returns  
- **Relative equity** measures compounded excess performance over buy-and-hold  

---

## Performance Evaluation

The strategy is evaluated using:

- Cumulative equity curves
- Relative equity vs benchmark
- Maximum drawdown
- Sharpe ratio
- Sortino ratio

---

## Key Result

After accounting for transaction costs, the SMA crossover strategy **fails to outperform buy-and-hold**, and exhibits weak risk-adjusted performance.

This result reinforces a core principle of quantitative research:  
> Simple technical rules rarely survive realistic implementation assumptions.

---

## Scope and Limitations

- Single-asset backtest
- No parameter optimization
- No regime conditioning
- No leverage or dynamic sizing

These choices are intentional to preserve interpretability and avoid overfitting.

---

## Disclaimer

This project is intended for educational and research purposes only.  
It does not constitute financial advice or a production-ready trading system.
