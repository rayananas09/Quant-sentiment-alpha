# Quant Sentiment Alpha (VADER vs FinBERT)

A quant research project that tests whether "financial news sentiment" contains predictive information about "next-day returns", and compares a generic sentiment baseline (VADER) against a finance-specific transformer model (FinBERT).

## What this project does
- Downloads market data for (SPY, AAPL, MSFT) (via `yfinance`)
- Computes 1-day forward returns as the prediction target
- Pulls real  SPY-related headlines (Yahoo Finance feed)
- Builds daily sentiment factors:
  - **VADER** (baseline)
  - **FinBERT** (finance-trained NLP)
- Runs an equal-weighted multi asset backtest
- Evaluates performance with standard metrics (Sharpe, drawdown, etc)
- Compares **VADER vs FinBERT** signal quality

## Key result
FinBERT produced materially stronger performance than the VADER baseline on the tested window.

| Model  | Sharpe Ratio |

| VADER  | 0.786 |
| FinBERT| 6.481 |


