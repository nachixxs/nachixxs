# Ignacio Noguerol

AI and backend engineer in Mendoza, Argentina (UTC−3). I'm the technical co-founder of
**Accelerate.ai**, an agency that builds custom management systems for small businesses, with AI where
it saves time. Open to remote AI engineer and backend roles.

## Projects

Each README covers the problem, the design decisions with what they cost, and how the result was
tested. All data in them is fictional.

- **[whatsapp-order-agent](https://github.com/nachixxs/whatsapp-order-agent)**: takes print-shop orders
  over WhatsApp, writes each one to Google Sheets once the customer confirms, and hands prices, deadlines
  and stock to a person in Chatwoot. Claude tool use with one tool per turn, while Python writes every
  reply. A rewrite that turned 120 defenses from an earlier bot into 55 rules, each with a test; routing
  evals at 100 % on three runs (17 of 17 critical cases, US$ 0.35 per run).
  *FastAPI, Claude API, SQLite, Chatwoot, Docker.*
- **[quiniela-system](https://github.com/nachixxs/quiniela-system)**: a cash ledger and cash counts for a
  lottery agency, designed to replace seven paper notebooks. Append-only, multi-tenant ledger with
  balances computed by pure functions, idempotent writes, and an assistant that explains a count
  difference. A simulated case study built from the cash routine I run every day as manager of an agency.
  *FastAPI, PostgreSQL, React, TypeScript, Playwright.*
- **[accelerate-ai-web](https://github.com/nachixxs/accelerate-ai-web)**: the agency's one-page site,
  not live yet. Mobile-first, hand-written CSS and scroll-driven animations that leave the page complete
  without JavaScript. A Playwright and axe suite (256 checks) covers 360, 768 and 1280 px in Chromium,
  Firefox and WebKit.
  *Astro, CSS, Playwright.*

## Stack

Python, FastAPI, Pydantic, SQLAlchemy, Alembic, pytest · PostgreSQL, SQLite · Claude API (tool use), RAG ·
React, TypeScript, Astro · Docker, GitHub Actions, Playwright · WhatsApp Cloud API, Chatwoot

## Contact

[LinkedIn](https://www.linkedin.com/in/ignacio-noguerol-54aa942b0/) ·
[ignacionogpa@gmail.com](mailto:ignacionogpa@gmail.com) ·
[WhatsApp](https://wa.me/5492625634845) (for businesses that need a system)
