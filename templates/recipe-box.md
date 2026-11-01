# 🍳 Recipe Box

Your own searchable recipe collection. Save recipes by chat, then ask your assistant what
you can make with what's in the fridge.

## Setup prompt

Copy this into ChatData Sync:

> I want to keep a recipe box. For each recipe I want the name, the main ingredients, the
> category (breakfast, dinner, dessert, etc.), the prep or cook time, the number of
> servings, a source or link, and the full instructions or notes. I want to be able to
> find recipes by ingredient or category.

## Suggested fields to review

| Field | Type | Example |
| --- | --- | --- |
| Recipe | text | Lemon chicken |
| Ingredients | text | chicken, lemon, garlic, thyme |
| Category | choice | breakfast / lunch / dinner / dessert / snack |
| Time | number | 35 (minutes) |
| Servings | number | 4 |
| Source | text | grandma / link |
| Instructions | text | Sear chicken, add lemon… |

## Example commands

- "Save a recipe: Lemon chicken — chicken, lemon, garlic, thyme. Dinner, 35 minutes, serves 4."
- "Which recipes use chicken?"
- "Show me dessert recipes."
- "What can I make in under 20 minutes?"
- "Find that pasta recipe I saved."

## Tips

- List ingredients in a simple comma-separated style so "which recipes use chicken" works well.
- Keep **Category** values consistent for clean filtering.
- Use your actual saved field names and types; see the [template setup guidance](README.md).

---

[← All templates](README.md) · [Try ChatData Sync](https://chatdatasync.com/)
