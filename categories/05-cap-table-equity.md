# 05. 📋 Cap Table & Equity Management

> Track equity ownership, simulate dilution across rounds, manage option pools, model vesting schedules, and calculate exit waterfalls.

[← Back to main list](../README.md)

---

## Stage Coverage

| 🌱 Pre-Seed | 🌿 Seed | 🚀 Series A/B | 📈 Series C/D | 🏢 Late Stage |
|:---:|:---:|:---:|:---:|:---:|
| ✅ | ✅ | ✅ | ✅ | ✅ |

---

## Full-Featured Cap Table Platforms

### [captableinc/captable](https://github.com/captableinc/captable)
**Language:** TypeScript | **Stars:** ⭐ 3K+ | **Stages:** 🌍 All Stages

The #1 open-source cap table management platform — a complete alternative to Carta and Pulley. Full equity management from pre-seed through late stage.

**Key features:**
- Multi-round modeling with dilution simulation
- SAFE and convertible note tracking & conversion
- Employee option pool management (grants, vesting, exercises)
- Waterfall and exit scenario modeling
- Investor portal and shareholder communications
- 409A fair market value tracking
- Self-hostable with full source access

---

### [octolane-org/cap.octolane.com](https://github.com/octolane-org/cap.octolane.com)
**Language:** TypeScript | **Stars:** ⭐ 500+ | **Stages:** 🌱 🌿 🚀

Lightweight open-source cap table infrastructure for founders and early investors. Simpler than captable.io — great for pre-seed/seed stage.

---

## Open Standards & Interoperability

### [Open-Cap-Table-Coalition/Open-Cap-Format-OCF](https://github.com/Open-Cap-Table-Coalition/Open-Cap-Format-OCF)
**Language:** JSON Schema | **Stars:** ⭐ 1K+ | **Stages:** 🌍 All Stages

Industry-standard open JSON schema for cap table data interchange. Backed by Carta, Cooley, NVCA, and leading VC firms. Enables cap table data to move between platforms without vendor lock-in.

---

## Dilution & Waterfall Modeling

### [foresighthq/cap-table-tool](https://github.com/foresighthq/cap-table-tool)
**Language:** Python / JavaScript | **Stars:** ⭐ 400+ | **Stages:** 🌿 🚀 📈

Cap table + exit waterfall calculator. Tracks dilution across multiple rounds, models liquidation preferences, participation rights, and carve-outs.

---

### [metju90/capitalization-table](https://github.com/metju90/capitalization-table)
**Language:** JavaScript | **Stars:** ⭐ 100+ | **Stages:** 🌿 🚀

Equity calculator with liquidation preference waterfall and exit modeling. Good starter for building custom waterfall tools.

---

### [rickprice/CapTable](https://github.com/rickprice/CapTable)
**Language:** Rust | **Stars:** ⭐ 100+ | **Stages:** 🌍 All Stages

CLI cap table calculator with CSV input support. For engineers who want to model equity scenarios programmatically.

---

## Employee Equity & Option Management

### [rayshan/startup-equity-calculator](https://github.com/rayshan/startup-equity-calculator)
**Language:** JavaScript | **Stars:** ⭐ 150+ | **Stages:** 🌍 All Stages

Help employees and founders make informed equity decisions. Models stock option value under different exit scenarios.

---

### [Neufund/ESOP](https://github.com/Neufund/ESOP)
**Language:** Solidity | **Stars:** ⭐ 200+ | **Stages:** 🌿 🚀

On-chain ESOP implementation with cliff vesting, bonus options, and employee exit handling. For crypto-native startups.

---

## Fund-Level Equity Tools

### [urbantech/musacapital](https://github.com/urbantech/musacapital)
**Language:** Python | **Stars:** ⭐ 200+ | **Stages:** 🌱 🌿

Open-source tools specifically for emerging fund managers and angel syndicates. Combines basic cap table management with deal tracking for small funds.

---

## Dilution Simulation Reference

```python
# Simulate a SAFE conversion at Series A
def simulate_safe_conversion(
    pre_money_valuation,
    safe_amount,
    valuation_cap,
    discount_rate=0.20,
    existing_shares=10_000_000
):
    cap_price = valuation_cap / existing_shares
    round_price = pre_money_valuation / existing_shares
    discount_price = round_price * (1 - discount_rate)
    conversion_price = min(cap_price, discount_price)
    safe_shares = safe_amount / conversion_price
    total_shares = existing_shares + safe_shares
    return {
        "conversion_price": conversion_price,
        "safe_shares": safe_shares,
        "safe_ownership_pct": safe_shares / total_shares * 100
    }
```
