# Mentor Framework Conformance

## Purpose

Conformance verifies that an implementation consumes the framework without changing its semantic rules.

## Required checks

### Repository integrity

- canonical repository resolves to stableagent/mentor-framework;
- framework version is recorded;
- canonical JSON files parse successfully;
- JSON Schemas parse successfully;
- all referenced role IDs exist in the role registry;
- all referenced person IDs exist in the people registry;
- all team IDs exist in mentor-teams.json;
- all domain IDs exist in the specialty matrix;
- all fixed identities agree across session roles, people and authority documents.

### Routing integrity

- capability selection occurs before person selection;
- required skills are distinguishable from recommended skills;
- smallest sufficient team is preferred;
- missing coverage is explicitly reported;
- specialist approval is respected;
- regulated/high-risk escalation is preserved;
- clarification is requested when ambiguity materially changes routing;
- no global mentor ranking is generated.

### Governance integrity

- human final decision authority remains intact;
- Nahid remains strategic oversight;
- Saeed remains session manager;
- Mojgan remains lead startup advisor;
- Saeed remains session manager;
- historical records are not silently rewritten;
- provenance is retained.

### Context integrity

- context is progressively selected;
- unrelated repository content is excluded;
- governance is not removed to save tokens;
- JSON remains canonical;
- TOON is derived and validated;
- malformed TOON falls back to canonical JSON.

## Required reference scenarios

At minimum, implementations should test:

1. founder finance question;
2. import/export question with regulated jurisdiction;
3. product validation question;
4. ambiguous question requiring clarification;
5. question requiring a specialist approval;
6. high-risk question requiring external review;
7. follow-up question using existing session context.

## Pass condition

A conforming implementation produces semantically equivalent routing and governance results from the same versioned framework snapshot, request and authorization state.
