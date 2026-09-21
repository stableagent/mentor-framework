# Routing Engine Standard

## Purpose

The Routing Engine transforms a normalized startup/advisory request into an explainable mentor-team proposal.

It is a deterministic capability-routing layer. It is not an autonomous business decision maker.

## Inputs

Required context:

- `user_role`
- `startup_type`
- `stage`
- `problem_type`
- `jurisdiction`
- `risk_level`
- `required_skills`

Optional context:

- business model;
- industry;
- target market;
- current constraints;
- budget;
- timeline;
- existing team;
- already-approved specialists;
- prior session context.

## Normalization

The engine must normalize:

- aliases to canonical IDs;
- free-text problem descriptions to problem types;
- skills to canonical skill IDs;
- jurisdiction to a canonical jurisdiction identifier where possible;
- risk to one of `low`, `medium`, `high`, `critical`.

Unknown values are retained as unresolved inputs rather than silently guessed.

## Algorithm

1. Validate the routing request.
2. Resolve known taxonomy IDs.
3. Derive additional required skills from `problem_type`, `startup_type`, `stage`, `jurisdiction` and `risk_level`.
4. Merge explicit and derived skills.
5. Identify candidate lead roles.
6. Select a lead role using role coverage, not person preference.
7. Identify specialist roles required to cover remaining skills.
8. Apply jurisdiction and regulated-domain constraints.
9. Calculate skill coverage.
10. Detect missing skills and external-review requirements.
11. Determine whether specialist approval is required.
12. Produce an explainable team proposal.
13. Hand the proposal to Armin for session coordination and to Mojgan for integrated advisory synthesis after activation.
14. Record the routing result through Saeed.

## Lead-role rules

For normal startup advisory work, `lead-startup-advisor` is the integration role.

A specialist role may be the operational lead for a narrowly scoped domain session, but the overall advisory synthesis remains under the lead startup advisory layer unless the user explicitly defines another structure.

## Escalation rules

Escalate to Nahid when:

- strategic objectives conflict;
- governance or authority boundaries are unclear;
- a critical risk has irreversible or organization-level consequences;
- the routing engine cannot produce a safe coverage explanation.

Require current authoritative or qualified professional review for regulated or high-risk matters such as:

- tax;
- accounting/audit;
- legal;
- investment;
- insurance;
- regulated import/export;
- cybersecurity incidents;
- other jurisdiction-specific regulated activity.

## Approval

The engine may propose specialists automatically.

Activation requires user approval unless a documented pre-authorization rule applies.

Approval status must be explicit:

- `not-required`
- `pending-user`
- `approved`
- `declined`
- `pre-authorized`

## Determinism and explainability

Given the same taxonomy version, normalized request and authorization context, the engine should produce the same role-level selection.

Every selected role must have a rationale referencing:

- required skill(s);
- matching domain;
- problem context;
- jurisdiction/risk constraints when applicable.

## No autonomous decision making

The routing engine may decide which advisory capabilities are required. It may not decide:

- whether the business should proceed;
- whether an investment should be accepted;
- whether a legal position is correct;
- whether a commercial offer should be signed;
- any other final business decision reserved for the user.

## Versioning

Routing results must retain:

- taxonomy version;
- routing-rule version;
- request ID;
- timestamp;
- selected roles;
- approval state.

Historical results must remain interpretable after taxonomy changes.
