# Kalshi 交易机器人

**🌐 Language / 语言 / Язык:** [English](README.md) · [简体中文](README.zh-CN.md) · [Русский](README.ru.md)

[![Engine](https://img.shields.io/badge/engine-shared_core-6e40c9?style=flat-square)](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits)
[![Rust](https://img.shields.io/badge/rust-1.70+-orange.svg?style=flat-square&logo=rust)](https://www.rust-lang.org/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![CI](https://github.com/tarpboi/Kalshi/actions/workflows/ci.yml/badge.svg)](https://github.com/tarpboi/Kalshi/actions/workflows/ci.yml)

> **Kalshi 交易机器人** — 受 CFTC 监管（美国）。隶属 [Prediction Market Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits) 套件：一个执行核心，一个风控层，覆盖所有平台。

**Kalshi** 已映射到共享引擎，但适配器尚未接入。本仓库保存平台元数据；交易代码位于主工具包，目前仅在 Polymarket 上执行。

---

## Kalshi 上的策略

以下是映射到 Kalshi 的策略。适配器接入后即可在此运行 — 相同的风控、相同的 TUI、完整的空跑（dry-run）支持。

| 策略 |
|----------|
| 💰 **跨市场套利** — 锁定价差，而非方向 |
| 🎯 **结算狙击** — 95 美分接近确定性 → 保证 1.00 美元结算 |
| 📊 **订单簿失衡** — 信号本身*就是*订单簿，无需外部数据源 |
| 💰 **做市** — 做庄家，而非赌徒（双边 GTD，库存偏移） |
| 🎯 **方向性套利** — 套利底仓（Up + Down < $1），向更有优势的一侧倾斜 |
| 📈 **价差收割** — 上千笔 0.5 美分的小赢累积成一个大数字 |
| 🏆 **体育执行** — 点击、成交、完成 — FAK |

> 想要 Kalshi 上未列出的策略？适配器覆盖按需驱动 — [联系我们](https://t.me/tarpboi)。

---

## 快速开始

交易代码位于主工具包。克隆它、填入密钥，并从空跑开始。目前运行于 Polymarket。

```bash
git clone https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits.git
cd Prediction-Markets-Trading-Bot-Toolkits
cp config.yaml.example config.yaml        # add your keys
cargo run --release -- run copy-trading   # dry-run: enable_trading is false by default
```

---

## 一个引擎，覆盖所有平台

执行核心与风控层都位于主工具包中：

### 👉 **[Prediction-Markets-Trading-Bot-Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits)** — 完整套件

| | |
|---|---|
| **订单执行** | 端到端 < 100 毫秒 |
| **事件处理** | 每事件 < 1 毫秒 |
| **安全** | 熔断器 · 深度保护 · 空跑 · 最小交易额 |
| **平台** | 已映射 21 个平台 |

新增一个平台只需编写**一个适配器** — 而非重建整个机器人。

---

## 获取访问权限

| 平台 | 链接 |
|----------|------|
| **完整工具包** | [Prediction-Markets-Trading-Bot-Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits) |
| **Telegram** | [@tarpboi](https://t.me/tarpboi) |
| **讨论区** | [GitHub Discussions](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits/discussions) |

*通常在数小时内回复。*

---

## 相关平台

[Polymarket](https://github.com/tarpboi/Polymarket) · [Predict.fun](https://github.com/tarpboi/Predict.fun) · [Interactive Brokers ForecastTrader](https://github.com/tarpboi/Interactive-Brokers-ForecastTrader) · [Limitless](https://github.com/tarpboi/Limitless-Exchange)

> 在[主工具包 →](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits#venue-coverage)中浏览完整平台目录

---

## 免责声明

> 交易预测市场涉及真实的财务风险。本软件按“原样”提供，不附带任何担保，亦不构成投资建议。在投入真实资金前，请务必使用 `enable_trading: false` 进行测试。请确保遵守 Kalshi 的服务条款及您所在地区的法律法规。

---

<div align="center">

**Kalshi 交易机器人 · 基于 [Prediction Market Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits) 引擎构建**

[![Telegram](https://img.shields.io/badge/Telegram-@tarpboi-26A5E4?style=flat-square&logo=telegram)](https://t.me/tarpboi)

</div>
