# 🌱 Garden & Plant Log

Track what you planted, when you watered, and what's ready to harvest. Great for vegetable
gardens, houseplants, and anyone who keeps forgetting which plant needs what.

## Setup prompt

Copy this into ChatData Sync:

> I want to keep a garden and plant log. For each plant I want the name, the location
> (bed, pot, room), the date planted, how often it needs watering, the last watered date,
> the expected harvest or bloom date, its current status (healthy, needs water, struggling),
> and notes. I also want to log watering and care events over time.

## Fields it builds

| Field | Type | Example |
| --- | --- | --- |
| Plant | text | Cherry tomatoes |
| Location | text | Raised bed 2 |
| Planted | date | 2026-04-12 |
| Watering schedule | text | Every 2 days |
| Last watered | date | 2026-06-18 |
| Harvest / bloom | date | 2026-07-20 |
| Status | choice | healthy / needs water / struggling |
| Notes | text | Staked, lots of flowers |

## Example commands

- "Add cherry tomatoes in raised bed 2, planted April 12th, water every 2 days."
- "I watered the tomatoes and the basil today."
- "Which plants need water?"
- "What's ready to harvest this month?"
- "Show me everything in raised bed 2."

## Tips

- Update **Last watered** by chat each time — then "which plants need water" stays useful.
- Use one row per plant; log recurring care in the notes or as new dated entries.

---

[← All templates](README.md) · [Personal & everyday tracking](https://chatdatasync.com/use-cases/personal-tracker.html) · [Try ChatData Sync](https://chatdatasync.com/)
