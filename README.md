### Hi, I'm Kiran 👋

Senior Product Manager · Bern, Switzerland · 18+ years in product, strategy, and digital transformation across B2B SaaS, MedTech, and telco.

---

### What I'm working on

**[basketch](https://basketch.vercel.app/en)** — Swiss weekly deals, side by side · [code](https://github.com/dommalapatikk/basketch)

> What's on sale this week, at which store — side by side?

Swiss shoppers spread their groceries across several chains, but every chain publishes its promotions separately. basketch collects the weekly deals from seven retailers in one place, compares the stores category by category, and turns the deals you pick into a shopping list you can forward.

**The product:**
- Weekly deals from 7 Swiss retailers: Migros, Coop, LIDL, ALDI, Denner, SPAR, Volg
- A weekly verdict per category: which store has the deepest average discount
- A shopping list grouped by store with an estimated total, shareable via WhatsApp, copy or email
- English and German · no app, no login, no account

**The engineering:**

| | |
|---|---|
| **Frontend** | Next.js 16 (App Router) · React 19 · TypeScript · Tailwind CSS 4 |
| **Database** | Supabase (PostgreSQL + Row-Level Security) |
| **Data pipeline** | TypeScript, domain-driven collection module with one adapter per retailer · Python OCR step · GitHub Actions cron three times a week |
| **AI categorisation** | LangGraph (LangChain) classification agent: Gemini (free tier) classifies each deal, a GPT-5 nano judge via OpenRouter checks the result (LLM-as-judge) |
| **Operations** | Runs unattended: dead-man health check, workflow keep-alive, per-retailer telemetry |
| **Hosting** | Vercel · auto-deploy from GitHub |
| **Testing** | Test-driven: 2,100+ automated tests (Vitest + pytest) |
| **Cost** | Free tiers throughout, plus one paid service (the AI judge) capped at USD 5/month |

**The PM case study:**

basketch is documented end-to-end — [PRD](https://github.com/dommalapatikk/basketch/blob/main/docs/prd.md), [competitive analysis](https://github.com/dommalapatikk/basketch/blob/main/docs/competitive-analysis.md) (13 competitors), [business model canvas](https://github.com/dommalapatikk/basketch/blob/main/docs/business-model-canvas.md), [technical architecture](https://github.com/dommalapatikk/basketch/blob/main/docs/technical-architecture.md), and [use cases](https://github.com/dommalapatikk/basketch/blob/main/docs/use-cases.md).

---

### How it was built

A personal project, built in my own time with [Claude Code](https://claude.ai/code) and an agentic AI harness of 19 specialised agents — product, design, architecture, tech lead, builder, code reviewer, QA, SRE — with LLM-as-judge review. Every change follows the same loop: root-cause analysis, an agreed design, a failing test first, independent review, QA, then my approval before it goes live.

---

### Background

- **Frontify AG** (2022–2026) — Senior Product Manager · Analytics, access & user management
- **Ypsomed AG** (2019–2022) — Director, Product Management · Digital & IoT analytics cloud
- **Swisscom AG** (2011–2019) — Solution design, delivery, SAFe release train, strategy
- **MBA** — University of St. Gallen (HSG)

---

<sub>Based in Bern · [LinkedIn](https://linkedin.com/in/kirandommalapati) · [basketch](https://basketch.vercel.app/en)</sub>
