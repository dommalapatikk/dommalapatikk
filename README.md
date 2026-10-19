### Hi, I'm Kiran 👋

Senior Product Manager · Bern, Switzerland · 18+ years in product, strategy, and digital transformation across B2B SaaS, MedTech, and telco.

---

### What I'm building

Two personal products, built in my own time to stay hands-on with modern product and AI engineering.

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

**[Compare Insurance](https://compare-insurance.vercel.app)** — Find your lowest health premium · [code](https://github.com/dommalapatikk/compare-insurance)

> Which basic health insurance is cheapest for me next year, and what do I give up for it?

Every autumn, Swiss residents can switch their compulsory basic insurance (Grundversicherung) before the deadline. Compare Insurance takes a postcode, birth year and accident cover, and ranks the official 2027 premiums with a guided advisor that never invents a premium: every number comes from the comparison engine.

**The product:**
- Search by postcode or municipality; the premium region is resolved behind the scenes
- Age category derived from birth year; gender is not collected
- Every deductible from CHF 300 to 2,500, across the official models: Standard, FLEX, PRAXIS, TEL-DIG and PHARM
- Up to ten ranked offers, with savings against a clearly stated baseline
- A guided advisor chat: premiums, rankings and savings come only from the comparison tool; guidance comes from official BAG and ch.ch sources

**The engineering:**

| | |
|---|---|
| **Frontend** | Next.js 16 (App Router) · React 19 · TypeScript · feature-modular architecture |
| **Backend** | Python · FastAPI · domain-driven design (framework-free domain layer, ports and adapters) |
| **Database** | Supabase (PostgreSQL) catalogue of normalised 2027 premiums |
| **Data** | Official federal data only: BAG / Priminfo premiums and regions, swisstopo postcodes · pinned raw files with SHA-256 checksums |
| **AI advisor** | LangChain / LangGraph tool-calling agent on OpenAI: three tools (premium comparison, location search, official guidance) reuse the same use case as the HTTP API, so the chat and the comparison can never disagree |
| **Quality gates** | GitHub Actions on every push: pytest, Vitest, architecture and user-facing-copy checks, type check, build · weekly parity check against the official Priminfo calculator |
| **Hosting** | Vercel (frontend and API) |

**The PM case study:**

Documented end-to-end — [PRD](https://github.com/dommalapatikk/compare-insurance/blob/main/docs/PRD.md), [UX spec](https://github.com/dommalapatikk/compare-insurance/blob/main/docs/UX_SPEC.md), [architecture](https://github.com/dommalapatikk/compare-insurance/blob/main/docs/ARCHITECTURE.md), [API spec](https://github.com/dommalapatikk/compare-insurance/blob/main/docs/API_SPEC.md), [observability](https://github.com/dommalapatikk/compare-insurance/blob/main/docs/OBSERVABILITY.md), and [data sources](https://github.com/dommalapatikk/compare-insurance/blob/main/data/SOURCES.md).

---

### How they were built

Both are personal projects, built in my own time with [Claude Code](https://claude.ai/code) and agentic AI harnesses of specialised agents. basketch: 19 agents — product, design, architecture, tech lead, builder, code reviewer, QA, SRE — with LLM-as-judge review. Compare Insurance: 8 agents — product manager, UX researcher, designer, tech lead, engineer, code reviewer, QA, and a challenger that grills every plan before commitment — working through a written ten-stage operating model from discovery to release. Both are set up around the same loop: an agreed design, a failing test first, independent code review, QA, then my approval before anything goes live.

---

### Background

- **Frontify AG** (2022–2026) — Senior Product Manager · Analytics, access & user management
- **Ypsomed AG** (2019–2022) — Director, Product Management · Digital & IoT analytics cloud
- **Swisscom AG** (2011–2019) — Solution design, delivery, SAFe release train, strategy
- **MBA** — University of St. Gallen (HSG)

---

<sub>Based in Bern · [LinkedIn](https://linkedin.com/in/kirandommalapati) · [basketch](https://basketch.vercel.app/en) · [Compare Insurance](https://compare-insurance.vercel.app)</sub>
