# 07. 🏦 Fund Operations & LP Reporting

> Fund administration, capital calls, distributions, waterfall calculations, carried interest, NAV calculations, and LP communications.

[← Back to main list](../README.md)

---

## Stage Coverage

| 🌱 Pre-Seed | 🌿 Seed | 🚀 Series A/B | 📈 Series C/D | 🏢 Late Stage |
|:---:|:---:|:---:|:---:|:---:|
| ✅ | ✅ | ✅ | ✅ | ✅ |

> ⚠️ **Note:** True open-source LP management software is sparse — most production tools are commercial. The tools below are building blocks for custom solutions.

---

## Accounting & Financial Records

### [simonmichael/hledger](https://github.com/simonmichael/hledger)
**Language:** Haskell | **Stars:** ⭐ 3K+ | **Stages:** 🌍 All Stages

Plain-text, double-entry accounting system used by small VC funds and family offices. Track capital accounts per LP, manage fund P&L, and generate balance sheets.

**Build with it:** Track LP capital contributions, called capital, distributions, and running NAV using plain-text ledger files. Version-controlled in git.

```
; Example fund ledger entry
2026-01-15 Capital Call - LP John Smith
    Assets:Cash:Fund                 $500,000
    Equity:LP:JohnSmith             -$500,000
```

---

### [ledger/ledger](https://github.com/ledger/ledger)
**Language:** C++ | **Stars:** ⭐ 5K+ | **Stages:** 🌍 All Stages

The original plain-text accounting tool. Battle-tested for financial record keeping. Many small funds use Ledger + git for fund bookkeeping, tracking capital calls, management fees, and distributions.

---

## Exit Waterfall & Carried Interest

### [foresighthq/cap-table-tool](https://github.com/foresighthq/cap-table-tool)
**Language:** Python / JavaScript | **Stars:** ⭐ 400+ | **Stages:** 🌍 All Stages

Exit waterfall calculator integrated with cap table. Models liquidation preferences, participation rights, anti-dilution, and carried interest splits.

**Waterfall structure it models:**
1. Return of capital to LPs
2. Preferred return / hurdle rate to LPs
3. Carry catch-up to GP
4. Remaining split (80/20 LP/GP typical)

---

## LP Document Management & Signing

### [docusealco/docuseal](https://github.com/docusealco/docuseal)
**Language:** Ruby | **Stars:** ⭐ 8K+ | **Stages:** 🌍 All Stages

Self-hosted e-signature platform for LP subscription agreements, capital call notices, K-1 distribution letters, and side letter management.

---

### [documenso/documenso](https://github.com/documenso/documenso)
**Language:** TypeScript | **Stars:** ⭐ 9K | **Stages:** 🌍 All Stages

Open-source DocuSign alternative. Automate LP document signing workflows with audit trail and multi-party signing support.

---

## Emerging Fund Manager Tools

### [urbantech/musacapital](https://github.com/urbantech/musacapital)
**Language:** Python | **Stars:** ⭐ 200+ | **Stages:** 🌱 🌿

Specifically built for emerging fund managers and angel syndicates. Includes LP management, basic capital call tracking, and fund-level reporting tools.

---

### [Illyism/saasbooks](https://github.com/Illyism/saasbooks)
**Language:** TypeScript | **Stars:** ⭐ 300+ | **Stages:** 🌿 🚀

Connects Stripe and Mercury Bank data to generate financial insights. Adaptable for portfolio company financial reporting that rolls up to fund-level dashboards.

---

## Fund Economics Reference

```
Standard VC Fund Economics:
├── Management Fee: 2% of committed capital (years 1-5), then 2% of invested
├── Carried Interest: 20% of profits above hurdle rate
├── Hurdle Rate: 8% preferred return to LPs (typical)
├── Waterfall: European (whole-fund) vs American (deal-by-deal)
└── Fund Life: 10 years (5 invest + 5 harvest, with 2-year extension option)

Key LP Metrics:
├── DPI: Cash returned / Capital invested (realized multiple)
├── TVPI: (Cash + NAV) / Capital invested (total value multiple)
├── IRR: Annualized return accounting for timing of cash flows
├── MOIC: Total value / Invested capital (simple multiple)
└── J-Curve: Expected negative returns in early years before positive inflection
```
