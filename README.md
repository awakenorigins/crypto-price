# crypto-price — Live cryptocurrency prices + candlestick charts

> Fetch the current price and percentage change for any crypto token and generate a dark-theme candlestick chart image. Supports Hyperliquid and CoinGecko as data sources.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
crypto-price retrieves live token prices and generates candlestick chart images via a single Python script. It queries Hyperliquid API first (preferred for HYPE and Hyperliquid tokens) and falls back to CoinGecko for everything else. Results are cached for 5 minutes to avoid redundant API calls. Output includes current price, period percentage change, a path to the generated PNG chart, and a formatted text summary.

## Features
- **Price** — current USD/USDT price
- **Change** — percentage change over the selected period
- **Chart** — dark-theme 8×8 candlestick PNG (`/tmp/crypto_chart_{SYMBOL}_{timestamp}.png`)
- **Durations** — `30m`, `3h`, `12h`, `24h` (default), `2d`
- **Sources** — Hyperliquid API (preferred) + CoinGecko (fallback)
- **Cache** — 300s to avoid rate limits

## Usage / Quick Start
```bash
python3 scripts/get_price_chart.py HYPE
python3 scripts/get_price_chart.py BTC 3h
python3 scripts/get_price_chart.py ETH 30m
python3 scripts/get_price_chart.py SOL 2d
```

## Trigger Keywords (OpenClaw)
token price, crypto price, price chart, cryptocurrency market data, HYPE price, BTC chart

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
