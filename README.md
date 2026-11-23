<div align="center">

# ChatData Sync

### Private structured memory for ChatGPT, Claude, Gemini CLI, and compatible agents

Describe what you want to keep track of in plain English. Your AI assistant logs it,
updates it, finds it, and answers questions about it — without building a backend.

[**Open the app →**](https://chatdatasync.com/app) &nbsp;·&nbsp;
[**Open ChatData Sync in ChatGPT →**](https://chatgpt.com/apps/chatdata-sync/asdk_app_6a260ccbce68819189d814e03106a38a) &nbsp;·&nbsp;
[**See how it works →**](https://chatdatasync.com/how-it-works.html)

[![Website](https://img.shields.io/badge/Website-chatdatasync.com-0f766e?style=flat-square)](https://chatdatasync.com/)
[![ChatGPT](https://img.shields.io/badge/ChatGPT-Available-10a37f?style=flat-square)](https://chatgpt.com/apps/chatdata-sync/asdk_app_6a260ccbce68819189d814e03106a38a)
[![Pricing](https://img.shields.io/badge/Pricing-from%20%240-1d4ed8?style=flat-square)](https://chatdatasync.com/pricing-details.html)

</div>

---

## What is ChatData Sync?

**ChatData Sync is an assistant-agnostic, private structured memory and tracker
layer.** Create trackers from plain-English descriptions or spreadsheets, then let
authorized assistants save, find, update, and summarize the same records: your
clients, repairs, recipes, invoices, and garden logs.

You describe your workflow in plain English. ChatData Sync builds the structure for you
and connects it to your assistant. From then on, you just talk:

> "Log today's oil change at 62,400 miles, $58."
>
> "What's still unpaid this week?"
>
> "Which recipes use chicken?"

Your assistant saves, updates, finds, counts, and summarizes — all from natural language,
all against data that stays yours.

Your assistant can change. Your organized records stay yours. ChatData Sync owns
storage, structure, permissions, and record operations; the connected assistant
owns conversation, reasoning, and any separately configured workflows.
Compatible MCP or REST clients can connect, but each host determines which
connection methods and tools it supports.

This public repository contains product documentation, reusable templates, and
the Gemini CLI extension. It does not contain the private application backend,
customer records, or credentials.

## Who it's for

- **Solo service businesses** — pet sitters, tutors, handymen, freelancers tracking
  clients, jobs, sessions, and invoices through conversation.
- **Side hustlers** who want a lightweight CRM without building one.
- **Everyday life** — recipes, car and home maintenance, home projects, hobbies,
  health habits, garden care.
- **Power users** who already live in AI chats and want their assistant to remember.

## How it works

1. **Start** — [Sign in](https://chatdatasync.com/app?start=1), describe your tracker,
   choose a template, or import a CSV/Excel file.
2. **Review** — Check the suggested sections, fields, and any import notes, then
   create the tracker. Review optional row imports before saving.
3. **Connect** — If you're using ChatGPT, start with the hosted app below. For
   other assistants, follow your tracker's **Connect** guide. Grant only the
   access the assistant needs.
4. **Verify** — Ask the assistant to list the sections in your test tracker
   without making changes. If your workflow also needs write access, verify a
   harmless test entry separately.

## Works with your assistant

| Assistant | How |
| --- | --- |
| **ChatGPT** | Open the [ChatData Sync app in ChatGPT](https://chatgpt.com/apps/chatdata-sync/asdk_app_6a260ccbce68819189d814e03106a38a), where available. Follow the [ChatGPT setup guide](https://chatdatasync.com/use-cases/chatgpt-tracker). |
| **Claude** | Connect over MCP. See the [Claude MCP integration](https://chatdatasync.com/integrations/claude-mcp.html). |
| **Gemini CLI** | Install this repository as a native Streamable HTTP MCP extension. See [Gemini CLI setup](GEMINI-CLI.md). |
| **Custom agents and compatible MCP/REST clients** | Use the [system-agnostic connection guide](https://chatdatasync.com/integrations/agents.html) and the live [MCP endpoint](https://chatdatasync.com/api/mcp). |

### Connect through the ChatGPT app

Sign in to ChatData Sync when prompted. On the authorization screen, select only
the tracker or trackers you need and review the permissions before approving.
Back in ChatGPT, try: “Using ChatData Sync, list the sections in my sample tracker.
Don’t change anything.”

**Already using custom GPT Actions?** OpenAI's standard retirement date is
December 11, 2026; follow the notice for the account or workspace that owns the
GPT. Custom Actions do not transfer when you migrate a GPT. Check that you can
access the hosted app and separately test the tools you rely on. See the
[OpenAI migration FAQ](https://help.openai.com/en/articles/20001519-custom-gpt-retirement-and-migration-faq).

### Install the Gemini CLI extension

```shell
gemini extensions install https://github.com/cgosmonsolution/chatdata-sync
```

Enter a named, tracker-specific connection key at Gemini's **sensitive setting
prompt**, never in chat or command-line arguments. No npm install, Node bridge,
or build step is needed. See [setup, tool scope, and troubleshooting](GEMINI-CLI.md).

This is a **Gemini CLI extension**, not a consumer Gemini web-app integration,
Google Chat bot, or Google Workspace Marketplace listing. The repository is
discoverable by the Gemini CLI gallery through its `gemini-cli-extension` topic;
gallery indexing and acceptance are controlled by Google, not guaranteed here.

## What can you do today?

- **Create trackers without backend tooling.** Describe a goal, use voice during
  setup, or import CSV/TSV/Excel files up to 10 MB. Each usable Excel sheet becomes
  a section. Review inferred types and import notes; rows are saved in batches,
  and an interrupted import may leave earlier batches saved.
- **Browse and correct entries in the app.** Use tables, cards, charts, record
  details, and private attachments. Edit a record's fields without rebuilding it.
- **Share a tracker with a visual workspace.** Invite collaborators with **Can
  view** or **Can edit** access. They can open the tracker, browse entries and
  attachments, and export CSV; editors can also change or delete entries and
  manage attachments. Layout, sharing, backups, and history restoration remain
  owner-only. A collaborator's assistant connection never expands their access.
- **Control every assistant connection.** Restrict actions, sections, fields, and
  expiry; pause, rotate, or revoke connections independently. Choose direct writes
  or **review-before-saving**. Proposed changes awaiting approval are not saved
  records; approval rechecks current permissions and revisions.
- **Keep context and meaning consistent.** Connected agents read the live tracker
  layout, units, choices, and declared links. Owners can review and approve drafted
  agent guides; scoped section skills are available to compatible hosts.
- **Get evidence-backed counts and sums.** Structured summaries use exact filters
  and can group by declared links between sections. Preserve the returned canonical
  answer and completeness warnings. Reusing the same query and answer ID can detect
  changed answers across assistants; this is not a locked snapshot.
- **Choose how to search.** Exact retrieval is the default. Optional semantic
  search ranks a bounded authorized candidate set using configured AI and safety
  providers; it is not a complete index of every historical record.
- **Keep files with records.** Save supported documents, spreadsheets, text files,
  and images as private attachments. ChatGPT's attachment tool requires a
  host-provided file parameter; arbitrary download URLs are not accepted.
  Do not assume every assistant supports the same upload workflow.
- **Review history and recover mistakes.** Inspect saved record versions, restore
  a selected version as a new revision, and recover deleted records within 30 days.
  Retained copies and history still consume storage; expiry is not automatic erasure.
- **Take your data with you.** Every plan includes CSV export. Owners can export
  and import versioned JSON backups with layout, records, history, and attachment
  manifests. Manifests do not contain file bytes; download important files separately.
  Exports are not atomic snapshots, and multi-batch imports can partially complete.
- **Synchronize compatible agents.** The MCP change journal lets clients retrieve
  authorized record and layout changes since a checkpoint. File-only changes are
  not journaled. Optional signed external notifications require platform delivery
  to be enabled and an owner-configured destination; they are not reminders.

### What is not automatic?

Saving a due date does **not** schedule a reminder, recording a bill does **not**
pay it, and drafting a message does **not** send it. Scheduled tracker emails
require reminder configuration; external automation needs separately connected
tools. AI can make mistakes, so review important writes and returned totals.

The full MCP service offers more tools than the conservative Gemini extension.
This extension exposes seven core record tools, not tracker creation, layout
changes, semantic search, history, change polling, or attachment uploads.
Use the appropriate host connection guide for those additional capabilities.

## Privacy and ownership

- **Private by default.** Tracker-specific credentials authorize one tracker.
  Invitations and explicit connection permissions determine who can see or edit it.
- **You stay in control.** Revoke assistant access at any time, and export everything
  to CSV whenever you want.
- **Broader access is explicit.** Cross-tracker work and creating new trackers
  require an owner-authorized, account-wide connection, not a tracker-specific key.
- **Your records are not sold or used to train AI models by ChatData Sync.**
  Tracker design, voice transcription, optional semantic search, and connected
  assistants involve providers under their respective terms.

Read the [security overview](https://chatdatasync.com/security.html) and the
[privacy policy](https://chatdatasync.com/legal/privacy-policy.html).

## Pricing

ChatData Sync charges per tracker, with bundle discounts.

| Plan | Monthly price | Tracking spaces | Assistant actions/month | Shared record and file storage |
| --- | --- | --- | --- | --- |
| **Free** | $0 | 1 | 200 | 1 GB |
| **Single Tracker** | $6.99 per paid tracker | 1 per subscription, plus included free tracker | 500 pooled | 5 GB |
| **Side Hustle** | $19 | 3 | 1,500 | 10 GB |
| **Growing Business** | $49 | 10 | 6,000 | 25 GB |
| **Team** | $99 | 25 | 20,000 | 50 GB |

All plans include CSV export and AI assistant connections.
See [full pricing](https://chatdatasync.com/pricing-details.html).

There is **no fixed per-tracker record cap**: records and files use shared private
storage. Metered assistant actions are record changes, counted per entry for bulk
writes; reads, searches, summaries, and dashboard browsing do not use that allowance.
Extra Single Tracker subscriptions do not multiply the pooled action allowance.

Current add-ons: **Storage Boost** (+10 GB for $5/month, subject to the account
storage ceiling), **Action top-up** (+500 for $5 once in the current billing
period), and **Action add-on** (+1,000 for $7/month). Annual options and current
checkout terms are on the pricing page.

## How it compares

- **vs Airtable** — ChatData Sync focuses on plain-English tracker setup and scoped
  assistant record operations rather than a general-purpose database workspace.
- **vs Notion** — ChatData Sync focuses on structured tracker records and authorized
  assistant access rather than a general-purpose document workspace.
- **vs Zapier** — Zapier connects existing apps via triggers; ChatData Sync is a private
  data layer, not a workflow connector. They're complementary.

[See the full comparison →](https://chatdatasync.com/vs-airtable.html)

## Templates

Ready-to-use tracker setups you can copy into ChatData Sync in seconds — each is a
plain-English prompt plus suggested fields to review and example chat commands.

| Template | Good for |
| --- | --- |
| [🚗 Car Maintenance](templates/car-maintenance.md) | Any vehicle owner |
| [🧾 Household Bills](templates/household-bills.md) | Every household |
| [💼 Client & Invoice Tracker](templates/client-invoice-tracker.md) | Pet sitters, tutors, handymen, freelancers |
| [🍳 Recipe Box](templates/recipe-box.md) | Home cooks |
| [🌱 Garden & Plant Log](templates/garden-plant-log.md) | Gardeners & plant parents |

[Browse all templates →](templates/) — and contributions are welcome.

## Agentic workflows

ChatData Sync is a **tool your AI agent can call**, not just passive storage. A connected
assistant can read context, retrieve records, summarize, and write permitted
changes as part of a multi-step request. Cross-tracker briefings and creating new
trackers need explicit account-wide owner authorization and host tool support.
MCP tracker creation starts with a basic layout; custom sections and fields are
separate additive steps.

[See 8 agentic workflow examples →](templates/agentic-workflows.md)

## What's new

Documentation refreshed November 1, 2026:

- Gemini CLI extension package with native HTTP transport and sensitive-key setup.
- Assistant-agnostic positioning and connection-specific permission guidance.
- Shared visual tracker workspace, spreadsheet import, private attachments, and
  owner-reviewed agent guides.
- Review-before-saving, version recovery, portable backups, and change checkpoints.
- Canonical summary evidence, bounded optional semantic search, and storage-based limits.

The extension package is published here; gallery indexing and an authenticated
Gemini end-to-end smoke test are not claimed as completed.

## Learn more

- [How it works](https://chatdatasync.com/how-it-works.html)
- [Use cases](https://chatdatasync.com/use-cases/)
- [Field story: 3 months of tutoring, logged entirely through ChatGPT](https://chatdatasync.com/use-cases/tutor-field-story.html)
- [FAQ](https://chatdatasync.com/faq.html)
- [White paper](https://chatdatasync.com/white-paper.html)
- [Docs](https://chatdatasync.com/docs.html)
- [Real customer workflows and editable starters](https://chatdatasync.com/use-cases/user-workflows.html)
- [First tracker walkthrough](https://chatdatasync.com/first-tracker/)
- [Gemini CLI extension setup](GEMINI-CLI.md)
- [System-agnostic agent connections](https://chatdatasync.com/integrations/agents.html)

## About

ChatData Sync is owned and operated by **Smarter Way to Apply** — [smarterwaytoapply.com](https://smarterwaytoapply.com).

Built by [Charles Anthony Gosmon](https://cgosmon.com). For support, email [support@smarterwaytoapply.com](mailto:support@smarterwaytoapply.com).

> **Note:** This repository is the public home for ChatData Sync — product overview,
> documentation links, and resources. The application source code is maintained
> privately. For questions, see the [contact page](https://chatdatasync.com/contact.html).
