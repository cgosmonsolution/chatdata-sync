# 💼 Client & Invoice Tracker

A lightweight CRM for solo service businesses — pet sitters, tutors, handymen, cleaners,
and freelancers. Log clients, jobs, and sessions by chat, then ask what's unpaid.

## Setup prompt

Copy this into ChatData Sync:

> I run a small service business and want to track my clients and the work I do for them.
> For each job or session I want the client name, the service or job description, the date,
> the duration or quantity, the rate, the total amount, the payment status (unpaid, paid,
> invoiced), and notes. I also want basic client contact info like phone or email.

## Fields it builds

| Field | Type | Example |
| --- | --- | --- |
| Client | text | Sarah M. |
| Contact | text | sarah@example.com |
| Service / job | text | Math tutoring session |
| Date | date | 2026-06-19 |
| Duration / qty | number | 1.5 (hours) |
| Rate | currency | $40/hr |
| Total | currency | $60.00 |
| Status | choice | unpaid / invoiced / paid |
| Notes | text | Covered algebra ch. 4 |

## Example commands

- "Log a 1.5-hour tutoring session with Sarah today at $40/hour, unpaid."
- "Add a dog-walking visit for the Johnsons, $25, paid."
- "What's still unpaid this week?"
- "How much did I earn from Sarah this month?"
- "Total my unpaid invoices."
- "Show every job I did in June."

## Tips

- One row per job or session keeps your earnings and unpaid totals exact.
- Use a consistent **Client** name so "earned from Sarah" groups correctly.
- Real-world example: see the [tutoring field story](https://chatdatasync.com/use-cases/tutor-field-story.html).

---

[← All templates](README.md) · [Service business use case](https://chatdatasync.com/use-cases/service-business-tracker.html) · [Try ChatData Sync](https://chatdatasync.com/)
