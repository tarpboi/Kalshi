# Kalshi Trading Bot

**🌐 Language / 语言 / Язык:** [English](README.md) · [简体中文](README.zh-CN.md) · [Русский](README.ru.md)

[![Engine](https://img.shields.io/badge/engine-shared_core-6e40c9?style=flat-square)](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits)
[![Rust](https://img.shields.io/badge/rust-1.70+-orange.svg?style=flat-square&logo=rust)](https://www.rust-lang.org/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![CI](https://github.com/tarpboi/Kalshi/actions/workflows/ci.yml/badge.svg)](https://github.com/tarpboi/Kalshi/actions/workflows/ci.yml)

> **Kalshi trading bot** — CFTC-regulated (US). Part of the [Prediction Market Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits) suite: one execution core, one risk layer, every venue.

**Kalshi** is mapped to the shared engine, but its adapter isn't wired yet. This repo holds venue metadata; the trading code lives in the main toolkit, which executes on Polymarket today.

---

## Strategies on Kalshi

These are the strategies mapped to Kalshi. They run here once its adapter is wired — same risk controls, same TUI, full dry-run support.

| Strategy |
|----------|
| 💰 **Cross-Market Arbitrage** — lock the spread, not the direction |
| 🎯 **Resolution Sniper** — 95¢ near-certainty → guaranteed $1.00 payout |
| 📊 **Orderbook Imbalance** — the signal *is* the order book, no external feeds |
| 💰 **Market Making** — be the house, not the gambler (two-sided GTD, inventory skew) |
| 🎯 **Directional Arbitrage** — arb base (Up + Down < $1), tilted toward the side with more edge |
| 📈 **Spread Farming** — a thousand 0.5¢ wins compound into one number |
| 🏆 **Sports Execution** — click, filled, done — FAK |

> Want a strategy not listed here on Kalshi? Adapter coverage is demand-driven — [ask](https://t.me/tarpboi).

---

## Quickstart

The trading code lives in the main toolkit. Clone it, add your keys, and start in dry-run. It runs against Polymarket today.

```bash
git clone https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits.git
cd Prediction-Markets-Trading-Bot-Toolkits
cp config.yaml.example config.yaml        # add your keys
cargo run --release -- run copy-trading   # dry-run: enable_trading is false by default
```

---

## One engine, every venue

The execution core and risk layer live in the main toolkit:

### 👉 **[Prediction-Markets-Trading-Bot-Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits)** — the full suite

| | |
|---|---|
| **Order execution** | < 100ms end-to-end |
| **Event processing** | < 1ms per event |
| **Safety** | Circuit breaker · depth guard · dry-run · trade floor |
| **Venues** | 21 venues mapped |

Adding a venue means writing **one adapter** — not rebuilding a bot.

---

## Get access

| Platform | Link |
|----------|------|
| **Full toolkit** | [Prediction-Markets-Trading-Bot-Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits) |
| **Telegram** | [@tarpboi](https://t.me/tarpboi) |
| **Discussions** | [GitHub Discussions](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits/discussions) |

*Response time is typically within a few hours.*

---

## Related venues

[Polymarket](https://github.com/tarpboi/Polymarket) · [Predict.fun](https://github.com/tarpboi/Predict.fun) · [Interactive Brokers ForecastTrader](https://github.com/tarpboi/Interactive-Brokers-ForecastTrader) · [Limitless](https://github.com/tarpboi/Limitless-Exchange)

> Browse the full venue directory in the [main toolkit →](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits#venue-coverage)

---

## Disclaimer

> Trading prediction markets involves real financial risk. This software is provided as-is, without warranty. It is not financial advice. Always test with `enable_trading: false` before deploying real capital. Ensure compliance with Kalshi's terms of service and your local regulations.

---

<div align="center">

**Kalshi trading bot · built on the [Prediction Market Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits) engine**

[![Telegram](https://img.shields.io/badge/Telegram-@tarpboi-26A5E4?style=flat-square&logo=telegram)](https://t.me/tarpboi)

</div>
