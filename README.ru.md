# Торговый бот Kalshi

**🌐 Language / 语言 / Язык:** [English](README.md) · [简体中文](README.zh-CN.md) · [Русский](README.ru.md)

[![Engine](https://img.shields.io/badge/engine-shared_core-6e40c9?style=flat-square)](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits)
[![Rust](https://img.shields.io/badge/rust-1.70+-orange.svg?style=flat-square&logo=rust)](https://www.rust-lang.org/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![CI](https://github.com/tarpboi/Kalshi/actions/workflows/ci.yml/badge.svg)](https://github.com/tarpboi/Kalshi/actions/workflows/ci.yml)

> **Торговый бот Kalshi** — Регулируется CFTC (США). Часть набора [Prediction Market Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits): одно ядро исполнения, один слой риска, все площадки.

Площадка **Kalshi** сопоставлена с общим движком, но её адаптер пока не подключён. Этот репозиторий хранит метаданные площадки; торговый код находится в основном наборе, где сегодня есть адаптеры для Predict.fun и Polymarket.

---

## Стратегии на Kalshi

Это стратегии, сопоставленные с Kalshi. Они заработают здесь, когда адаптер будет подключён — те же риск-контроли, тот же TUI, полная поддержка dry-run.

| Стратегия |
|----------|
| 💰 **Межрыночный арбитраж** — фиксируйте спред, а не направление |
| 🎯 **Снайпер разрешения** — покупка почти определённых исходов перед завершением, удержание до выплаты |
| 📊 **Дисбаланс стакана** — сигнал *и есть* стакан заявок, без внешних фидов |
| 💰 **Маркет-мейкинг** — котировки с двух сторон с перекосом против своего инвентаря |
| 🎯 **Направленный арбитраж** — заявки Yes + No на сумму меньше $1 с перекосом в сторону большего эджа |
| 📈 **Сбор спреда** — захват спреда бид-аск, по одному кругу за раз |
| 🏆 **Спортивное исполнение** — ввели, исполнено, готово, из терминала |

> Нужна стратегия, не указанная здесь для Kalshi? Покрытие адаптеров определяется спросом — [напишите](https://t.me/tarpboi).

---

## Быстрый старт

Торговый код находится в основном наборе. Клонируйте его, добавьте ключи и начните с dry-run. Сегодня в нём есть адаптеры для Predict.fun и Polymarket.

```bash
git clone https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits.git
cd Prediction-Markets-Trading-Bot-Toolkits
cp config.yaml.example config.yaml        # add your keys
cargo run --release -- run copy-trading   # dry-run: enable_trading is false by default
```

---

## Один движок, все площадки

Ядро исполнения и слой риска находятся в основном наборе:

### 👉 **[Prediction-Markets-Trading-Bot-Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits)** — полный набор

| | |
|---|---|
| **Исполнение ордеров** | < 100 мс от начала до конца |
| **Обработка событий** | < 1 мс на событие |
| **Безопасность** | Предохранитель · защита глубины · dry-run · минимум сделки |
| **Площадки** | Сопоставлено площадок: 21 |

Добавить площадку — значит написать **один адаптер**, а не пересобирать бота.

---

## Получить доступ

| Платформа | Ссылка |
|----------|------|
| **Полный набор** | [Prediction-Markets-Trading-Bot-Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits) |
| **Telegram** | [@tarpboi](https://t.me/tarpboi) |
| **Обсуждения** | [GitHub Discussions](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits/discussions) |

*Обычно отвечаем в течение нескольких часов.*

---

## Связанные площадки

[Polymarket](https://github.com/tarpboi/Polymarket) · [Predict.fun](https://github.com/tarpboi/Predict.fun) · [Interactive Brokers ForecastTrader](https://github.com/tarpboi/Interactive-Brokers-ForecastTrader) · [Limitless](https://github.com/tarpboi/Limitless-Exchange)

> Полный каталог площадок — в [основном наборе →](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits#venue-coverage)

---

## Отказ от ответственности

> Торговля на рынках предсказаний сопряжена с реальным финансовым риском. ПО предоставляется «как есть», без гарантий, и не является финансовой консультацией. Всегда тестируйте с `enable_trading: false` перед вводом реального капитала. Соблюдайте условия использования Kalshi и местное законодательство.

---

<div align="center">

**Торговый бот Kalshi · построен на движке [Prediction Market Toolkits](https://github.com/tarpboi/Prediction-Markets-Trading-Bot-Toolkits)**

[![Telegram](https://img.shields.io/badge/Telegram-@tarpboi-26A5E4?style=flat-square&logo=telegram)](https://t.me/tarpboi)

</div>
