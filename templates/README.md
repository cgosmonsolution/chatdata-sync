# ChatData Sync Templates

Ready-to-use tracker setups you can copy into ChatData Sync in seconds. Each template
is just plain English — paste the **setup prompt** into ChatData Sync, review the fields
it builds, connect your assistant, and start logging by chat.

> New here? Start at **[chatdatasync.com](https://chatdatasync.com/)** or get the
> **[ChatGPT app](https://chatgpt.com/apps/chatdata-sync/asdk_app_6a260ccbce68819189d814e03106a38a)**.

## How to use a template

1. [Sign in to ChatData Sync](https://chatdatasync.com/app?start=1) and describe a new tracker.
2. Paste the template's **Setup prompt**.
3. Review the suggested fields and adjust anything you like.
4. Follow the **Connect** guide for ChatGPT, Claude, [Gemini CLI](../GEMINI-CLI.md),
   or another compatible assistant.
5. Talk to your assistant using the **Example commands**.

Template fields are suggestions, not a guaranteed generated contract. Review your
actual sections, saved field identifiers, types, units, and choices. The assistant
must read `get_sync_context` before record operations and use that live layout.
Amounts are numeric fields with an agreed currency such as USD, not a separate
`currency` type. Names and display examples are not literal tool argument values.

Saving a due date or watering schedule does not create an automatic reminder.
Configure reminders separately. Updates and deletions need confirmation, current
revisions, and write permission; review-mode proposals are not saved until approved.

## Templates

| Template | Good for | What you track |
| --- | --- | --- |
| [🚗 Car Maintenance](car-maintenance.md) | Any vehicle owner | Service history, mileage, cost, what's due |
| [🧾 Household Bills](household-bills.md) | Every household | Bills, due dates, paid/unpaid, totals |
| [💼 Client & Invoice Tracker](client-invoice-tracker.md) | Pet sitters, tutors, handymen, freelancers | Clients, jobs, sessions, payment status |
| [🍳 Recipe Box](recipe-box.md) | Home cooks | Recipes, ingredients, meal ideas |
| [🌱 Garden & Plant Log](garden-plant-log.md) | Gardeners & plant parents | Plants, watering, planting and harvest dates |

## Agentic workflows

See [**Agentic Workflows with ChatData Sync**](agentic-workflows.md) — eight ways your
compatible agent can read, write, and summarize as part of a multi-step request.
Cross-tracker work and creating trackers require explicit account-wide owner access
and additional tools not included in the core Gemini extension.

## Contributing a template

Have a setup that works well? Open an issue or a pull request with your template using the
same format (Setup prompt · Fields · Example commands). Useful, real-world templates are
welcome.

---

Published by [Smarter Way to Apply](https://smarterwaytoapply.com) · Built by [Charles Anthony Gosmon](https://cgosmon.com) · [chatdatasync.com](https://chatdatasync.com/)

Support: [support@smarterwaytoapply.com](mailto:support@smarterwaytoapply.com).
