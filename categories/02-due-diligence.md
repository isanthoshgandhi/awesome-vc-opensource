# 02. 🔬 Due Diligence & Data Rooms

> Tools for evaluating companies, organizing structured diligence processes, securing documents, and running data rooms.

[← Back to main list](../README.md)

---

## Stage Coverage

| 🌱 Pre-Seed | 🌿 Seed | 🚀 Series A/B | 📈 Series C/D | 🏢 Late Stage |
|:---:|:---:|:---:|:---:|:---:|
| ✅ | ✅ | ✅ | ✅ | ✅ |

---

## Data Room & Document Sharing

### [mfts/papermark](https://github.com/mfts/papermark)
**Language:** TypeScript | **Stars:** ⭐ 5K+ | **Stages:** 🌍 All Stages

The #1 open-source DocSend alternative. Secure document sharing with detailed analytics — see who viewed which page, for how long. AES-256 encrypted. Perfect for VC data rooms.

**Key features:**
- Page-level analytics (view time per slide)
- Password protection & email verification
- Data room with folder structure
- Custom domains
- Team collaboration
- Self-hostable with Next.js + PostgreSQL

**Build with it:** Deploy as your fund's branded data room portal for portfolio companies and LP communications.

---

### [documenso/documenso](https://github.com/documenso/documenso)
**Language:** TypeScript | **Stars:** ⭐ 9K | **Stages:** 🌍 All Stages

Open-source DocuSign alternative. E-sign NDAs, term sheets, subscription agreements, and all diligence documents. Self-hostable with full audit trails.

**Key features:**
- Digital signatures with audit log
- Multiple signers and sequential signing
- Template library for recurring document types
- API-first for workflow automation
- Self-hosted on your infrastructure

---

### [OpenSignLabs/OpenSign](https://github.com/OpenSignLabs/OpenSign)
**Language:** TypeScript | **Stars:** ⭐ 3.5K | **Stages:** 🌿 🚀

Free, self-hosted document e-signing platform. Good for smaller funds wanting DocuSign functionality without the cost.

---

### [docusealco/docuseal](https://github.com/docusealco/docuseal)
**Language:** Ruby | **Stars:** ⭐ 8K+ | **Stages:** 🌍 All Stages

Open-source document signing with a focus on simplicity. Drag-and-drop form builder, multiple signing methods, and embeddable signing flows.

---

## Document Processing & Organization

### [Stirling-Tools/Stirling-PDF](https://github.com/Stirling-Tools/Stirling-PDF)
**Language:** Java | **Stars:** ⭐ 40K | **Stages:** 🌍 All Stages

Self-hosted PDF Swiss Army Knife. Merge, split, compress, OCR, redact, and watermark documents. Essential for data room preparation.

**Key features:**
- 50+ PDF operations
- OCR via Tesseract
- Redaction and watermarking
- Merge/split/compress
- Docker deployment

---

### [AppFlowy-IO/AppFlowy](https://github.com/AppFlowy-IO/AppFlowy)
**Language:** Dart / Rust | **Stars:** ⭐ 60K | **Stages:** 🌍 All Stages

Open-source Notion alternative. Build structured due diligence wikis, company assessment templates, checklists, and founder profiles. Self-hosted for full data control.

---

## Checklists & Scoring Frameworks

### [joelparkerhenderson/startup-assessment](https://github.com/joelparkerhenderson/startup-assessment)
**Language:** Markdown | **Stars:** ⭐ 500+ | **Stages:** 🌱 🌿 🚀

Comprehensive startup scorecard with evaluation criteria across 8 dimensions: team, product, market, traction, financials, competition, technology, and business model.

---

### [Tyler-KD/due-diligence-checklist](https://github.com/Tyler-KD/due-diligence-checklist)
**Language:** Markdown | **Stars:** ⭐ 100+ | **Stages:** 🌱 🌿

Structured due diligence checklist for early-stage investments. Covers legal, financial, technical, team, and market sections.

---

### [KatherineMichel/tech-and-funding-toolkit](https://github.com/KatherineMichel/tech-and-funding-toolkit)
**Language:** Markdown | **Stars:** ⭐ 1K+ | **Stages:** 🌍 All Stages

Curated toolkit with VC economics references, DD frameworks, and funding resources. Useful reference for building diligence playbooks.

---

## Secrets & Access Management

### [Infisical/infisical](https://github.com/Infisical/infisical)
**Language:** TypeScript | **Stars:** ⭐ 15K+ | **Stages:** 🌍 All Stages

Secure secrets management platform. Use for managing data room access credentials, API keys for portfolio company integrations, and secure sharing of sensitive DD materials.

---

## Standard DD Checklist (Pre-Seed → Series A)

```markdown
## Team
- [ ] Founder backgrounds verified (LinkedIn, references)
- [ ] Cap table reviewed
- [ ] Prior company history checked

## Product
- [ ] Demo / product walkthrough completed
- [ ] Technical architecture reviewed
- [ ] IP ownership confirmed

## Market
- [ ] TAM/SAM/SOM model reviewed
- [ ] Competitive landscape mapped
- [ ] Customer interviews conducted (3-5 minimum)

## Financials
- [ ] P&L reviewed (12 months)
- [ ] Burn rate and runway confirmed
- [ ] Unit economics validated (CAC, LTV, payback)
- [ ] Bank statements verified

## Legal
- [ ] Incorporation documents reviewed
- [ ] IP assignments confirmed
- [ ] Prior funding documents reviewed
- [ ] Employment agreements checked
- [ ] No undisclosed liabilities
```
