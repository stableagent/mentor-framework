# Naming Standard

## IDs

Use lowercase kebab-case.

Examples:

- `product-management`
- `financial-modeling`
- `customer-discovery`
- `startup-strategy`

IDs are semantic identifiers, not translations.

## Names

Use the internationally recognizable English canonical name.

Localized display names belong under `localization/`.

## File names

Use the entity ID as the file name:

```
product-management.json
financial-modeling.json
customer-discovery.json
```

## References

References use IDs, never localized names.

Correct:

```json
{"related_skills":["customer-discovery","market-validation"]}
```

Incorrect:

```json
{"related_skills":["کشف مشتری"]}
```

## Language codes

Use language-only ISO 639-1 codes:

`en`, `fa`, `de`, `fr`, `ar`, etc.

Regional tags such as `fa-IR` are intentionally out of scope for v1.0.
