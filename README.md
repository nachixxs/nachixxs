# Ignacio Noguerol

I build custom software for small businesses: management systems that replace paper
notebooks and scattered spreadsheets, with AI added where it actually saves time. I'm the
technical co-founder of **Accelerate.ai**, an AI automation agency for small businesses
based in Mendoza, Argentina, and I'm open to remote AI / backend engineering roles.

## For businesses: Accelerate.ai

We build a system around how your business already works: cash and sales records, orders,
appointments, stock, customer accounts and reports, in one place instead of five notebooks
and a spreadsheet. You don't adapt your business to generic software; the system adapts to
you, and keeps changing as your business does.

When it helps, the system includes an AI assistant, for example so customers can book or
order over WhatsApp. The assistant is one part of the system, not the product.

- **Free process audit first.** A 30–45 minute call to find where your team loses the most time.
- **One clear proposal.** What it costs to build, what it costs per month, and a delivery date.
- **Built in 1–3 weeks**, with a mid-way demo so you can adjust it before it's done.
- **Monthly support.** We fix what breaks and adapt the system as your business changes.

We work in Spanish and English. → **[Message us on WhatsApp](https://wa.me/5492625634845)** · [email](mailto:ignacionogpa@gmail.com)

## For engineering teams

Selected work. Every repo has a README that explains the design decisions, and runs on
fictional data.

| Project | What it shows |
|---|---|
| [quiniela-system](https://github.com/nachixxs/quiniela-system) | Custom management system for a lottery agency that replaces seven paper cash notebooks: a multi-tenant, append-only ledger, a pure-function cash-count engine, idempotent writes, argon2 auth. FastAPI, PostgreSQL, React and TypeScript, with CI against a real PostgreSQL, Playwright E2E and Docker. |
| [turnos-citas](https://github.com/nachixxs/turnos-citas) | Appointment booking system with a WhatsApp assistant as its front end, built on Claude tool use. It checks real availability before confirming, and a whole class of text bugs is made structurally impossible. 148 tests run in CI without credentials or network. |
| [whatsapp-order-agent](https://github.com/nachixxs/whatsapp-order-agent) | Order-taking system for a small business, in progress: a WhatsApp assistant collects the order, writes it to Google Sheets only after the customer confirms, and hands the conversation to a person in Chatwoot when it needs human judgment. A from-scratch rewrite that turns 120 production defenses into 55 numbered rules, each one with a test, under a hard line budget. |
| [restaurant-rag-assistant](https://github.com/nachixxs/restaurant-rag-assistant) | Restaurant bookings and FAQ answers over WhatsApp, with RAG on Voyage AI embeddings. The similarity threshold was measured, not guessed, and Claude tool use routes each message between booking and FAQ. |

**Stack:** Python, FastAPI, Pydantic, SQLAlchemy, Alembic, pytest · PostgreSQL · React,
TypeScript, Astro · Claude API (tool use), RAG, Voyage AI · n8n, WhatsApp Cloud API,
Google Sheets API · Docker, GitHub Actions

## Contact

[LinkedIn](https://www.linkedin.com/in/ignacio-noguerol-54aa942b0/) · [ignacionogpa@gmail.com](mailto:ignacionogpa@gmail.com) · [WhatsApp](https://wa.me/5492625634845)
