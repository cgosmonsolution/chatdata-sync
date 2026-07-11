# Agentic Workflows with ChatData Sync

ChatData Sync isn't just a place to store records — it's a **tool your AI agent can call**.
In the [ChatGPT app](https://chatgpt.com/apps/chatdata-sync/asdk_app_6a260ccbce68819189d814e03106a38a)
(and with Claude), the assistant can read, write, search, summarize, and even
create new trackers on its own as part of a larger task. That turns a simple chat into an
**agentic workflow**: you state a goal, and the agent does several steps against your
private data to reach it.

This page collects agent-style use cases — each one chains multiple tool calls into a
single, natural request.

> **What the agent can do under the hood:** look up records (`list_records`,
> `search_records`), answer counts and totals (`summarize_records`), add and update
> entries (`create_record`, `update_record`), discover your trackers (`list_trackers`),
> and spin up a brand-new tracker mid-conversation (`create_tracker`) — all scoped to
> your account.

---

## 1. The Morning Operations Briefing

**You say:** *"Give me my morning briefing."*

**The agent does:**
1. Lists your trackers to see what's relevant (`list_trackers`).
2. Pulls everything unpaid from your invoice tracker (`search_records`).
3. Checks your bills tracker for anything due this week.
4. Summarizes totals (`summarize_records`).
5. Hands you one tidy briefing: who owes you, what's due, what's overdue, and the dollar totals.

**Why it's agentic:** one request, several trackers, multiple reads, one synthesized answer.

---

## 2. End-of-Job Auto-Logging

**You say:** *"Just finished a 90-minute tutoring session with Sarah, $60, she'll pay Friday."*

**The agent does:**
1. Creates the session record with client, duration, amount, and status = invoiced (`create_record`).
2. Pulls Sarah's history to confirm the rate matches (`search_records`).
3. Totals what Sarah now owes and what you've earned this week (`summarize_records`).
4. Confirms: *"Logged. Sarah owes $120 across 2 sessions. You're at $480 this week."*

**Why it's agentic:** it writes, then reads back context, then reports — without you asking three times.

---

## 3. Receipt-to-Record

**You say:** *(paste or photo)* *"Add this — oil change receipt."*

**The agent does:**
1. Reads the receipt details (shop, date, mileage, cost, services).
2. Maps them to your car maintenance fields.
3. Creates the record and sets the next-service-due estimate (`create_record`).
4. Tells you when the next service is due based on the mileage interval.

**Why it's agentic:** unstructured input in, structured private record out, plus a forward-looking reminder.

---

## 4. Cross-Tracker Reconciliation

**You say:** *"Which clients are behind, and draft a friendly nudge for each."*

**The agent does:**
1. Reads your clients tracker and your invoices tracker (`list_records` across both).
2. Cross-references to find clients with unpaid or overdue invoices.
3. Pulls each client's contact and last service.
4. Drafts a personalized, friendly payment reminder per client — ready for you to send.

**Why it's agentic:** it joins two trackers, filters, and produces an action — not just a list.

---

## 5. Spin Up a Tracker On the Fly

**You say:** *"I'm starting to flip furniture on the side — help me keep track."*

**The agent does:**
1. Recognizes there's no tracker for this yet.
2. Creates a new "Furniture Flips" tracker with sensible fields — item, cost, sale price, profit, status (`create_tracker`).
3. Logs your first piece (`create_record`).
4. Offers to total your profit anytime.

**Why it's agentic:** the agent provisions new structured memory mid-conversation, then starts using it immediately.

---

## 6. The Weekly Audit Agent

**You say:** *"Do my Sunday review."*

**The agent does:**
1. Sweeps every tracker for overdue items — unpaid invoices, bills due, maintenance past due, plants needing water (`search_records`, `summarize_records`).
2. Ranks them by urgency and dollar impact.
3. Proposes a short action list for the week.
4. Optionally marks completed items as you confirm them (`update_record`).

**Why it's agentic:** recurring, multi-tracker, and it closes the loop by updating records.

---

## 7. Field Voice Logging

**You say (out loud, hands full):** *"Logged a dog-walking visit for the Johnsons, 30 minutes, $25, paid cash."*

**The agent does:**
1. Structures the spoken sentence into fields.
2. Creates the record (`create_record`).
3. Confirms briefly so you can keep moving.

**Why it's agentic:** natural speech becomes a clean, queryable record with zero forms — ideal for on-site work.

---

## 8. Smart Restock from Your Recipe Box

**You say:** *"I want to make three chicken dinners this week — what should I buy?"*

**The agent does:**
1. Searches your recipe box for chicken dinners (`search_records`).
2. Picks three and gathers their ingredients.
3. Consolidates them into a single shopping list.
4. Optionally logs your meal plan for the week.

**Why it's agentic:** it queries your private data, reasons over it, and produces a practical output.

---

## Why this matters

Most "AI memory" is passive — it remembers facts. ChatData Sync is **active memory an agent
can operate**: read it, reason over it, write back to it, and even extend it with new
trackers, all inside one conversation. Your data stays private and scoped to your account
the entire time.

**Ready to try it?** [Open the ChatGPT app](https://chatgpt.com/apps/chatdata-sync/asdk_app_6a260ccbce68819189d814e03106a38a)
or start at [chatdatasync.com](https://chatdatasync.com/).

---

[← All templates](README.md) · [How it works](https://chatdatasync.com/how-it-works.html) · [Claude MCP](https://chatdatasync.com/integrations/claude-mcp.html)
