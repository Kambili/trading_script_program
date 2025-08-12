# Intraday Break–Retrace Backtester

A small, testable Python project that backtests a **15-minute “daily high/low break + retrace”** strategy across multiple instruments.

## Project Purpose
Automate and study a trading idea: when price **breaks** the previous day’s high/low, wait for a **retrace** back to that level and then enter. This repo fetches intraday data, runs the rules, and saves results.

## Features
- Fetch 15-minute OHLC from Yahoo Finance (and Binance for crypto)
- Robust normalization of data to a consistent OHLC+UTC index
- Exact “break + retrace within N bars before cutoff” rules
- Summary stats (trades, win rate, avg return, Sharpe-like) + per-trade details
- Reproducible outputs (CSV/JSON/plots) to `backtest_output/`

## Quick Start

### Requirements
- Python 3.10+ (recommended 3.11 or 3.12)
- Git

### Setup
```bash
# clone
git clone https://github.com/<your-username>/intraday-break-retrace-backtester.git
cd intraday-break-retrace-backtester

# create & activate virtual env
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

# install direct dependencies
pip install -r requirements.txt
