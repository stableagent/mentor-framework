# Mentor Team Selection Standard

## Purpose

This standard defines how the advisory system converts a business problem into a temporary, scoped mentor team.

Selection is capability-based, not person-preference-based.

## Fixed system layer

The fixed system layer is always available:

1. ناهید — Nahid — `nahid`: strategic oversight
2. آرمین — Armin — `armin`: session management
3. مژگان — Mojgan — `mojgan`: lead startup advisory synthesis
4. سعید — Saeed — `saeed`: canonical session record

These identities are not selected by the routing engine as ordinary specialists.

## Team structure

A routed team contains:

- `lead_role`: the primary advisory role;
- `lead_person_id`: optional registered mentor capable of filling the lead role;
- `members`: specialist roles/persons required for the current problem;
- `required_skills`: capabilities the team must cover;
- `covered_skills`: capabilities covered by selected members;
- `missing_skills`: capabilities not currently covered;
- `escalations`: regulated, high-risk or strategic conditions;
- `approval_required`: whether user approval is required before adding a specialist.

## Selection rules

1. Select capabilities before people.
2. Prefer the smallest team that covers the stated problem without creating a material skill gap.
3. Do not select a specialist solely because the person exists in the registry.
4. A person's current availability, authorization and declared competency must be checked separately from role matching.
5. A specialist addition requires user approval unless an explicit pre-authorization rule covers the case.
6. High-risk domains require current authoritative verification or qualified professional review.
7. Strategic conflicts escalate to Nahid.
8. Mojgan integrates cross-domain specialist findings.
9. Armin coordinates the active session.
10. Saeed records the routing rationale and resulting team.
11. The routing engine must not rank people or claim that one mentor is globally better than another.
12. The routing engine must not make the user's business decision.

## Coverage model

Each required skill is evaluated as:

- `covered`: at least one selected member has the skill;
- `partially-covered`: related competency exists but the exact skill is missing;
- `missing`: no selected member is mapped to the skill;
- `requires-external-review`: the skill is present but the matter requires current authoritative or licensed review.

Coverage must be explainable through role/skill mappings.

## Team lifecycle

```
routing request
  ↓
normalize context
  ↓
identify required skills
  ↓
select lead role
  ↓
select specialist roles
  ↓
calculate coverage
  ↓
detect escalation / missing skills
  ↓
request user approval when required
  ↓
activate approved team
  ↓
run session
  ↓
Mojgan synthesizes
  ↓
Saeed records
```

## No-ranking rule

The selection engine returns a valid coverage set and its rationale. It does not produce:

- winner/loser labels;
- quality scores for people;
- global mentor rankings;
- personality judgments;
- predictions about which person will produce the best business outcome.

## Output contract

Every selection result should contain:

- request ID;
- lead role;
- members;
- required skills;
- coverage;
- rationale;
- missing skills;
- escalation requirements;
- approval status;
- provenance.

## Change control

Taxonomy changes must be versioned. Historical routing results retain the taxonomy version used at the time of selection.
