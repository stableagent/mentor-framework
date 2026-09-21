# Versioning Standard

Mentor Skills uses semantic versioning for public taxonomy contracts.

## Major

Increment when:

- a stable ID is removed;
- an entity meaning materially changes;
- required schema fields become incompatible;
- reference semantics change.

## Minor

Increment when:

- new domains, roles, skills or knowledge entities are added;
- optional fields are added;
- new languages are added.

## Patch

Increment for:

- typo fixes;
- documentation corrections;
- translation corrections that do not change meaning;
- non-breaking metadata corrections.

## Generated representations

JSON remains canonical. Generated TOON and other projections inherit the source taxonomy version and additionally record their encoder/specification version.
