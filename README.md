# algotrading-studies

This repo contains small, self-contained experiments in algorithmic trading and financial ML.

## Current notebooks

- `notebooks/meta_gradient_boosting.ipynb`  
  End-to-end ML research pipeline on daily META stock data:
  - Download OHLCV data from Yahoo Finance
  - Engineer technical features (RSI, EMA, ATR, Bollinger Bands, MACD, rolling stats, lags, calendar features)
  - Define a forward-looking “good trade within 20 days given TP/SL” label
  - Train a Gradient Boosting classifier with time-series cross-validation
  - Inspect feature importances and backtest a simple long/flat strategy vs. buy-and-hold

## Setup

```bash
python -m venv .venv
source .venv/bin/activate  # on Windows: .venv\Scripts\activate
pip install -r requirements.txt
