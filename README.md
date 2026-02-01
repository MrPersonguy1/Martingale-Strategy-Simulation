# Martingale-Strategy-Simulation
Martingale Trading Strategy Simulator

This project is a Python-based simulator that stress-tests a Martingale trading strategy on real stock market data. It evaluates how position sizing, stop-loss logic, and capital constraints impact long-term performance and risk.

The simulator runs on 5 years of historical data and supports both fixed stop loss and trailing stop loss modes while enforcing a finite starting capital ($10,000) — no unlimited money assumptions.

📈 Strategy Rules

Take Profit (TP): +5%

Close position

Reset size to 1 share

Reset direction to LONG

Stop Loss (SL): −2%

Close position

Reverse direction (LONG ↔ SHORT)

Increase position size using a multiplier (Martingale-style)

Capital Constraint

If the required position size exceeds available capital:

Force exit

Reset to 1 share

Reverse direction

Continue trading

🧠 Features

Fixed vs Trailing Stop Loss comparison

Configurable Martingale multipliers (e.g. 1.3x, 1.5x, 2x, 3x)

Full trade-by-trade simulation

Equity curve & max drawdown tracking

Annotated price charts with:

Buy / Sell / Short markers

Position sizes

TP (green) and SL (red) exits

Risk statistics:

Win rate

Max position size

Losing streaks

Capital drawdowns

📊 Stocks Tested

Apple (AAPL)

Microsoft (MSFT)

Google (GOOGL)

Plus additional large-cap equities

⚠️ Key Insight

This project demonstrates how Martingale strategies can appear profitable short-term but carry extreme tail risk, rapidly growing position sizes, and severe drawdowns — even with modest stop losses.

🚀 Requirements

Python 3

pandas

numpy

matplotlib

yfinance (or equivalent data source)

📌 Disclaimer

This project is for educational and research purposes only. It is not financial advice.
