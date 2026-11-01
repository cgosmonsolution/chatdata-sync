# 💼 Client & Invoice Tracker

A lightweight CRM for solo service businesses — pet sitters, tutors, handymen, cleaners,
and freelancers. Log clients, jobs, and sessions by chat, then ask what's unpaid.

## Setup prompt

Copy this into ChatData Sync:

> I run a small service business and want to track my clients and the work I do for them.
> For each job or session I want the client name, the service or job description, the date,
> the duration or quantity, the rate, the total amount, the payment status (unpaid, paid,
> invoiced), and notes. I also want basic client contact info like phone or email.

## Suggested fields to review

| Field | Type | Example |
| --- | --- | --- |
| Client | text | Sarah M. |
| Contact | text | sarah@example.com |
| Service / job | text | Math tutoring session |
| Date | date | 2026-06-19 |
| Duration / qty | number | 1.5 (hours) |
| Rate | number (USD/hour) | 40 |
| Total | number (USD) | 60.00 |
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

- Use one row per job or session and structured summaries. Check completeness
  warnings and confirm whether "earned" means work performed or payments received.
- Use a consistent **Client** name for filtering. Grouped linked summaries require
  a declared reference to a separate client section, not a join inferred from names.
- Rate times duration is not an automatic calculated field. Confirm and save the
  total explicitly; tracking an invoice does not create or collect a payment.
- Use your actual saved field names and types; see the [template setup guidance](README.md).
- Real-world example: see the [tutoring field story](https://chatdatasync.com/use-cases/tutor-field-story.html).

---

[← All templates](README.md) · [Service business use case](https://chatdatasync.com/use-cases/service-business-tracker.html) · [Try ChatData Sync](https://chatdatasync.com/)
