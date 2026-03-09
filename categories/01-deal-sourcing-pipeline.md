# 01. 🔍 Deal Sourcing & Pipeline

> Tools for discovering, tracking, qualifying, and managing investment opportunities from first contact to term sheet.

[← Back to main list](../README.md)

---

## Stage Coverage

| 🌱 Pre-Seed | 🌿 Seed | 🚀 Series A/B | 📈 Series C/D | 🏢 Late Stage |
|:---:|:---:|:---:|:---:|:---:|
| ✅ | ✅ | ✅ | ✅ | ✅ |

---

## CRM & Deal Flow Tracking

### [twentyhq/twenty](https://github.com/twentyhq/twenty)
**Language:** TypeScript | **Stars:** ⭐ 18K | **Stages:** 🌍 All Stages

Modern open-source CRM. Fully customizable data model makes it ideal for VC deal pipelines. Track companies, founders, meetings, and deal stages with a beautiful UI.

**Key features:**
- Custom objects & fields — model your exact deal stages
- Kanban and list views for pipeline management
- Email & calendar integration
- API-first, self-hostable
- Active development with large community

---

### [frappe/crm](https://github.com/frappe/crm)
**Language:** Python / JavaScript | **Stars:** ⭐ 2.5K | **Stages:** 🌱 🌿 🚀

Full-featured open-source CRM built on Frappe Framework. Customizable deal pipelines with tasks, notes, email threads, and reporting built in. Good for small to mid-size VC teams.

**Key features:**
- Stage-based deal pipeline with drag-and-drop
- Multi-user with role-based access control
- Email integration and activity tracking
- Reporting and analytics built-in

---

### [MicroPyramid/Django-CRM](https://github.com/MicroPyramid/Django-CRM)
**Language:** Python | **Stars:** ⭐ 1.5K | **Stages:** 🌿 🚀

Django REST + SvelteKit CRM with multi-tenant architecture and PostgreSQL backend. Good foundation for building a custom VC deal tracker on top of.

---

### [monicahq/monica](https://github.com/monicahq/monica)
**Language:** PHP / Vue | **Stars:** ⭐ 21K | **Stages:** 🌱 🌿

Personal relationship management CRM — ideal for angel investors managing founder relationships. Track conversations, reminders, and relationship history per founder.

---

## Deal Flow Intelligence & Signal Tracking

### [wizenheimer/subsignal](https://github.com/wizenheimer/subsignal)
**Language:** Python | **Stars:** ⭐ 500+ | **Stages:** 🌍 All Stages

Open-source deal flow monitoring infrastructure. Tracks companies of interest, detects product changes, hiring signals, funding news, and competitive intelligence.

**Key features:**
- Subscribe to company signals (hiring, pricing, product changes)
- Webhook-based event delivery
- Configurable signal sources
- Self-hosted on any cloud

---

### [VCInvestmentTool](https://github.com/chenhe95/VCInvestmentTool)
**Language:** Python | **Stars:** ⭐ 200+ | **Stages:** 🌿 🚀

NLP-powered tool to analyze startups from public data sources. Uses natural language processing to extract and score company information for initial screening.

---

## Investor & Deal Directories

### [octolens/awesome-oss-investors](https://github.com/octolens/awesome-oss-investors)
**Language:** Markdown | **Stars:** ⭐ 1K+ | **Stages:** 🌍 All Stages

Curated list of venture capital firms and angel investors who invest in commercial open-source startups. Great reference for OSS founders seeking the right investors.

---

### [swyxio/devtools-angels](https://github.com/swyxio/devtools-angels)
**Language:** Markdown | **Stars:** ⭐ 500+ | **Stages:** 🌱 🌿

Directory of active angel investors in developer tools and infrastructure. Lists individuals with their check sizes, focus areas, and how to reach them.

---

## How to Build a VC Deal Sourcing Tool

```
Stack recommendation:
- CRM backbone: Twenty CRM (TypeScript/API-first)
- Signal layer: Subsignal (Python)
- Data enrichment: Clearbit API / Apollo.io / LinkedIn
- Scoring: VCInvestmentTool NLP model
- Notifications: Slack webhooks
```
