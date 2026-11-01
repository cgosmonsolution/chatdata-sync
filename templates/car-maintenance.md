# 🚗 Car Maintenance Tracker

Keep a complete service history for one or more vehicles — and let your assistant tell you
what's due, what you've spent, and when each job last happened.

## Setup prompt

Copy this into ChatData Sync:

> I want to track car maintenance for my vehicles. For each service record I want to keep
> the vehicle (name or plate), the service type (oil change, tire rotation, brakes, etc.),
> the date, the mileage, the cost, the shop or who did it, and any notes. I also want to
> note the next service due date or due mileage so I can ask what is due.

## Suggested fields to review

| Field | Type | Example |
| --- | --- | --- |
| Vehicle | text | "Civic" / "8XYZ123" |
| Service type | text | Oil change |
| Date | date | 2026-06-19 |
| Mileage | number | 62,400 |
| Cost | number (USD) | 58.00 |
| Performed by | text | Quick Lube on 5th |
| Next due (date) | date | 2026-12-19 |
| Next due (mileage) | number | 67,400 |
| Notes | text | Used synthetic oil |

## Example commands

Once connected, just talk to your assistant:

- "Log today's oil change on the Civic at 62,400 miles, $58 at Quick Lube."
- "What maintenance has the Civic had this year?"
- "How much have I spent on the truck in total?"
- "When is the next oil change due?"
- "Show me everything overdue."

## Tips

- Add a row per service event — that's what powers the "what's due" and "total spent" answers.
- Track multiple vehicles in one tracker by using a clear **Vehicle** name on every record.
- Confirm currency, mileage units, and service intervals; the assistant should not
  invent maintenance advice. Due dates do not automatically schedule reminders.
- Use your actual saved field names and types; see the [template setup guidance](README.md).

---

[← All templates](README.md) · [Try ChatData Sync](https://chatdatasync.com/)
