# Regional Index Pools (RWA DeFi)

**Децентрализованный протокол для инвестирования в токенизированные региональные экономические индексы на Solana**

![CI](https://github.com/Marakaya/regional-index-pools/actions/workflows/ci.yml/badge.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Solana](https://img.shields.io/badge/Solana-Devnet-9945FF?style=for-the-badge&logo=solana)
![Hackathon](https://img.shields.io/badge/Hackathon-2026-FF0060?style=for-the-badge)

---

## 🌐 Live Demo

**Frontend:** https://regional-index-pools.vercel.app

---

## 🎯 О проекте

**Regional Index Pools** — DeFi-протокол для токенизации реальных региональных экономик (RWA).

```
┌─────────────────────────────────────────────────────────────┐
│                      INVESTOR                               │
│  💰 $100 USDC → LP-токены → 📈 до 12.5% APY            │
└─────────────────────┬───────────────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────────────┐
│                   REGIONAL POOL                             │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐       │
│  │ Real Estate │  │  Treasury   │  │  IP / Tech  │       │
│  │    40%      │  │    30%      │  │    30%      │       │
│  └─────────────┘  └─────────────┘  └─────────────┘       │
└─────────────────────────────────────────────────────────────┘
```

---

## 🧱 Архитектура

```
┌─────────────────────────────────────────────────────────────┐
│                        FRONTEND                             │
│   Next.js + Tailwind CSS + Framer Motion                    │
│   https://regional-index-pools.vercel.app                  │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│                    ANCHOR PROGRAM                           │
│   Program: RWIPool                                         │
│   Devnet: RwaPooL111111111111111111111111111111111111      │
└─────────────────────────────────────────────────────────────┘
```

---

## 📜 Смарт-контракт

Program ID: `RwaPooL111111111111111111111111111111111111`

### Account структуры:

```
Pool:       [authority, mint, lp_mint, total_deposits, total_shares, apy, region]
Investor:   [wallet, pool, shares, total_deposited, kyc_verified, whitelisted]
```

### Функции:

| Функция | Описание |
|---------|----------|
| `initializePool` | Создание регионального пула |
| `initializeInvestor` | Регистрация инвестора с KYC |
| `deposit` | Депозит USDC, получение LP токенов |
| `withdraw` | Вывод: сжигание LP → USDC + доход |

---

## 🚀 Quick Start

### Prerequisites:
- Node.js 18+
- Rust
- Anchor CLI
- Solana CLI

```bash
# Clone
git clone https://github.com/Marakaya/regional-index-pools
cd regional-index-pools

# Install dependencies
npm install

# Build programs
anchor build

# Run tests
anchor test

# Start frontend
npm run dev
```

---

## 📊 Региональные пулы (MVP)

| Пул | Регион | APY | TVL | Инвесторов |
|-----|--------|-----|-----|-----------|
| 🌏 СКФО | Северо-Кавказский ФО | 12.5% | $890K | 142 |
| 🌊 ЦФО | Центральный ФО | 9.8% | $650K | 98 |
| 🏭 СЗФО | Северо-Западный ФО | 10.2% | $420K | 76 |
| ⚡ УрФО | Уральский ФО | 11.5% | $340K | 54 |

---

## 🎨 UI/UX

- 🌙 Dark theme
- 💜 Violet/Cyan accents
- 📊 Real-time графики
- 🔒 KYC verification
- 💰 Portfolio dashboard
- ✨ Framer Motion анимации

---

## 👥 Команда

| Участник | Роль | Контакт |
|---------|------|---------|
| Kulakova Kate | Founder & Product Lead | [Telegram](https://t.me/) |
| Zaytseva Daria | Founder & Lead Engineer | [Telegram](https://t.me/) |

---

## 📄 Лицензия

MIT License — see [LICENSE](LICENSE)

---

## 🔗 Полезные ссылки

- [Solana Docs](https://docs.solana.com)
- [Anchor Framework](https://www.anchor-lang.com)
- [Solana Playground](https://beta.solpg.io)
- [Phantom Wallet](https://phantom.app)
- [Solflare Wallet](https://solflare.com)

---

**Hackathon MVP** | Solana | 2026 National Hackathon
