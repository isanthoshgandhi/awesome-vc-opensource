# 08. 📉 Startup Metrics & KPIs

> SaaS metrics, unit economics, AARRR framework, burn rate, growth measurement, and cohort analysis tools.

[← Back to main list](../README.md)

---

## Stage Coverage

| 🌱 Pre-Seed | 🌿 Seed | 🚀 Series A/B | 📈 Series C/D | 🏢 Late Stage |
|:---:|:---:|:---:|:---:|:---:|
| ✅ | ✅ | ✅ | — | — |

---

## SaaS Metrics Dashboards

### [mike-paper/pulse](https://github.com/mike-paper/pulse)
**Language:** TypeScript | **Stars:** ⭐ 1K+ | **Stages:** 🌿 🚀

Open-source SaaS metrics platform. Pulls from Stripe to calculate real-time MRR, ARR, churn, and growth rate. One of the best open-source options for startups reporting metrics to investors.

**Key features:**
- Stripe integration for revenue metrics
- Automatic MRR, ARR, churn calculation
- Slack and email reporting
- Beautiful charts and dashboards

---

### [MekuHQ/saasboard](https://github.com/MekuHQ/saasboard)
**Language:** React / TypeScript | **Stars:** ⭐ 1.2K+ | **Stages:** 🌿 🚀

Free open-source SaaS KPI dashboard. Pre-built components for: MRR, ARR, Churn Rate, NRR, CAC, LTV, and Payback Period.

---

### [alexdevero/saas-metrics](https://github.com/alexdevero/saas-metrics)
**Language:** JavaScript | **Stars:** ⭐ 500+ | **Stages:** 🌍 All Stages

All core SaaS metrics implemented in one library: MRR, ARR, churn rate, NRR, CAC, LTV, NPS. Drop-in formulas for any analytics stack.

---

## AARRR / Pirate Metrics

### [stephenlb/startup-metrics-dashboard](https://github.com/stephenlb/startup-metrics-dashboard)
**Language:** JavaScript | **Stars:** ⭐ 600+ | **Stages:** 🌱 🌿

Dave McClure's AARRR Pirate Metrics framework — the standard model for measuring early-stage startup health. Tracks all 5 layers:
- **A**cquisition: How do users find you?
- **A**ctivation: First great user experience?
- **R**etention: Do users come back?
- **R**eferral: Do users tell others?
- **R**evenue: How do you make money?

---

## Unit Economics

### [paragsasturkar/Calculating-LTV](https://github.com/paragsasturkar/Calculating-LTV)
**Language:** Python | **Stars:** ⭐ 150+ | **Stages:** 🌿 🚀

LTV (Lifetime Value) vs CAC (Customer Acquisition Cost) ratio analysis. The single most important metric for SaaS health evaluation by VCs.

```python
LTV = (ARPU * Gross_Margin) / Churn_Rate
CAC = Total_Sales_Marketing_Spend / New_Customers_Acquired
LTV_CAC_Ratio = LTV / CAC  # Target: > 3x
Payback_Period = CAC / (ARPU * Gross_Margin)  # Target: < 12 months
```

---

### [ericandrewlewis/startup-financial-model](https://github.com/ericandrewlewis/startup-financial-model)
**Language:** Python | **Stars:** ⭐ 150+ | **Stages:** 🌱 🌿

CAC, LTV, payback period, gross margin calculator. Pre-seed to seed stage — essential unit economics for first investor meetings.

---

## Cohort & Retention Analysis

### [groveco/cohort-analysis](https://github.com/groveco/cohort-analysis)
**Language:** Python | **Stars:** ⭐ 400+ | **Stages:** 🌿 🚀

Python cohort retention analysis library. Calculates LTV curves, retention rates by cohort, and churn forecasts. Powers the retention curves VCs look for in Series A decks.

---

## Burn Rate & Runway

### [jayrbolton/dontdie](https://github.com/jayrbolton/dontdie)
**Language:** JavaScript | **Stars:** ⭐ 200+ | **Stages:** 🌱 🌿

Startup survival calculator. Models cash burn, hiring plans, revenue projections, and answers: "how long until we run out of money?" Critical for pre-seed and seed diligence.

---

## VC Benchmarks Reference

```
SaaS Metrics — VC Benchmarks by Stage

🌿 Seed Stage:
- MRR Growth: 15-20% month-over-month
- Burn Multiple: < 2x (ideally < 1x)
- Runway: 18+ months post-raise

🚀 Series A:
- ARR: $1M - $3M
- ARR Growth: 3x year-over-year
- NRR: > 100% (ideally > 120%)
- Gross Margin: > 60%
- LTV:CAC: > 3x
- CAC Payback: < 18 months

📈 Series B/C:
- ARR: $10M+
- NRR: > 120%
- Rule of 40 Score: Growth Rate% + EBITDA% > 40
- Gross Margin: > 70%

🏢 Late Stage / Pre-IPO:
- ARR: $100M+
- EBITDA positive or clear path
- Rule of 40: > 40
- FCF Margin improving
```
