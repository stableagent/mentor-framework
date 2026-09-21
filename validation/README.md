# Validation

Validation must occur at three levels.

## 1. Schema validation

Validate each structured entity against the appropriate JSON Schema.

## 2. Referential validation

Verify that:

- referenced domain IDs exist;
- referenced skill IDs exist;
- referenced role IDs exist;
- framework, methodology, metric and tool IDs exist;
- localization entries reference existing entity IDs;
- IDs are unique.

## 3. Semantic validation

Check for:

- duplicate concepts under different IDs;
- inconsistent naming;
- invalid role/skill relationships;
- orphaned skills;
- missing canonical descriptions;
- localization without a canonical entity;
- deprecated references in active entities.

Generated TOON must be regenerated after canonical data changes.
