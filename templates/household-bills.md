# 🧾 Household Bills Tracker

Stop wondering what's unpaid. Track every recurring bill, its due date, and whether it's
been paid — then ask your assistant what's still owed this week.

## Setup prompt

Copy this into ChatData Sync:

> I want to track my household bills. For each bill I want the name (electric, internet,
> rent, streaming, etc.), the amount, the due date, the status (unpaid, paid, overdue),
> the category (utilities, housing, subscriptions, insurance), and an optional note for
> the account or confirmation number.

## Suggested fields to review

| Field | Type | Example |
| --- | --- | --- |
| Bill | text | Electric — City Power |
| Amount | number (USD) | 128.40 |
| Due date | date | 2026-06-27 |
| Status | choice | unpaid / paid / overdue |
| Category | choice | utilities / housing / subscriptions / insurance |
| Note | text | Autopay on card ending 1234 |

## Example commands

- "Add the electric bill, $128.40, due June 27th, unpaid."
- "Mark the internet bill as paid."
- "What's still unpaid this week?"
- "How much do I owe this month in total?"
- "List everything that's overdue."
- "What did I spend on subscriptions last month?"

## Tips

- Keep one row per bill per cycle so totals and "what's due" stay accurate.
- Use the **Status** field consistently — it's what makes "unpaid this week" work.
- Confirm the date range and use the saved due-date field, not record creation
  time. A due date does not schedule a reminder, and marking paid does not pay a bill.
- Use your actual saved field names and types; see the [template setup guidance](README.md).

---

[← All templates](README.md) · [Try ChatData Sync](https://chatdatasync.com/)
