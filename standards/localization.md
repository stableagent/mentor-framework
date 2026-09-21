# Localization Standard

## Principle

Localization changes presentation language, not identity.

A single skill has one stable ID and many localized representations.

Example:

```
skill_id: product-market-fit

en → Product-Market Fit
fa → تناسب محصول با بازار
de → Product-Market-Fit
fr → Adéquation produit-marché
```

## Required fields

A localized entry may contain:

- `entity_id`
- `language`
- `name`
- `description`
- `aliases`
- `notes`
- `status`
- `source`
- `reviewed_at`

## Translation status

Use one of:

- `draft`
- `machine-translated`
- `human-reviewed`
- `verified`

## Terminology

Canonical framework and metric names should remain recognizable in their original international form when translation could make the concept ambiguous.

A localized explanation can be translated fully while retaining the canonical term in parentheses where useful.
