# Ignacio Noguerol

**AI / Backend Engineer** · Python · FastAPI · Claude API · RAG
General Alvear, Mendoza, Argentina — open to remote roles

I build LLM-powered backends end to end: designing the flow, wiring the real
channel, and testing the parts that most people leave untested. Looking for my
first full-time role as an AI / LLM Engineer.

---

## What I actually know how to do

Anyone can call an LLM API. The part that took real work was learning to **test
one**, and that's what these two projects are about.

An agent's output is text, and "the reply sounds right" is not a test. Both
projects verify against concrete data — which tool the model called, with which
arguments, which slot came back — and never against tone. When a case turns out
to be genuinely about text, the answer isn't to relax the rule; it's to make the
text stop being variable.

---

## Projects

### [turnos-citas](https://github.com/nachixxs/turnos-citas) — WhatsApp appointment agent

A booking agent for a service business, built as a portfolio MVP over six
verifiable checkpoints. FastAPI + Claude API (tool use) + n8n + Google Sheets,
with all business data in a JSON config so the engine stays generic.

**148 tests**, plus verification scripts against the real Claude API (15/15) and
the real n8n flow (7/7).

The part worth reading is a bug I found in production. The bot told a customer
*"Thursday at 11 works, I have room"* — in a conversation path where no tool is
called and the calendar is never read. It had no way of knowing, and that time it
happened to be right, which is what makes a bug like that survive.

The interesting problem wasn't the fix, it was **how to verify it**. A blocklist
of phrases (`"I have room"`, `"that's free"`) doesn't work: the model dodges it
without trying, with a *"Perfect! What service do you need?"* that asserts exactly
the same thing. That catches the sentence you already saw, not the property.

I solved it by taking the text away from the model — the follow-up question
became a tool, and the text is now composed in code by a function that never
receives the requested date or time. It can't claim a slot is free because it
doesn't know. The test became exhaustive over all 7 possible outputs.

### [whatsapp-rag-agent](https://github.com/nachixxs/whatsapp-rag-agent) — restaurant agent with RAG

A real client engagement, built in 7 days. Takes table reservations and answers
menu and policy questions over a custom RAG pipeline, deciding message by message
which one applies. FastAPI + Claude API + Voyage AI embeddings + n8n.

The routing has no keyword matching anywhere: Claude gets two tools and whichever
one it picks *is* the classification.

Two things I'd point at:

- **The similarity threshold was measured, not guessed.** `0.45` comes from
  running real and out-of-scope questions through the embedding model: worst true
  match `0.5635`, best false match `0.3278`. The constant carries that
  measurement in a comment.
- **18 end-to-end test scripts** written the way customers actually type —
  lowercase, typos, emoji, data arriving across three messages. They're what
  surfaced the known limitations, which are documented with their status
  (corrected / accepted / open) instead of quietly dropped.

### [crypto-market-api](https://github.com/nachixxs/crypto-market-api) — REST API with sentiment analysis

Real-time crypto prices with sentiment analysis over news headlines. FastAPI +
PostgreSQL + SQLAlchemy/Alembic + HuggingFace Transformers, containerized with
Docker and with tests running in CI.

Here the focus was the backend fundamentals rather than the model: schema
migrations, a test suite, and a deployable container.

---

## Stack

**Working with, in shipped projects:**
Python · FastAPI · Claude API (tool use) · RAG (embeddings + semantic search) ·
Pydantic · pytest · PostgreSQL · Docker · n8n · WhatsApp Cloud API · Git

**Currently learning:**
pgvector · LangGraph · RAG evaluation · deployment on a VPS

---

## What I'm working on next

Going deeper on retrieval quality — chunking strategies and measuring whether a
RAG pipeline actually improved, instead of assuming it did.

---

## Contact

- **LinkedIn:** [ignacio-noguerol](https://www.linkedin.com/in/ignacio-noguerol-54aa942b0/)
- **Email:** ignacionogpa@gmail.com
- **X:** [@noguerolnacho_](https://x.com/noguerolnacho_)
