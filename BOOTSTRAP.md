# Mentor Framework Bootstrap Contract

Canonical address:
https://github.com/stableagent/mentor-framework

## Purpose

This document defines the single-address bootstrap contract for consumers of Mentor Framework.

## Bootstrap instruction

A consumer that supports repository retrieval should:

1. Resolve the repository at the canonical address.
2. Pin a framework version or commit for the session.
3. Load the normative bootstrap documents and schemas.
4. Validate the canonical data contracts.
5. Initialize the Context Selector and Context Engine.
6. Accept the user's next message as an advisory request.
7. Never require the user to manually choose domains, skills, mentors or context files unless the consumer cannot perform automatic selection.
8. Ask a clarification question only when the missing information materially changes routing, authority, risk or escalation.
9. Preserve human decision authority.

## Minimum bootstrap set

Load, at minimum:

- README.md
- BOOTSTRAP.md
- standards/context-selector.md
- standards/context-engine.md
- standards/context-packaging.md
- standards/chatbot-consumption-model.md
- standards/authority-matrix.md
- standards/mentor-team-selection.md
- standards/mentor-routing-framework.md
- schemas/context-selection-request.schema.json
- schemas/context-selection-result.schema.json
- schemas/context-package.schema.json
- schemas/context-engine-result.schema.json
- taxonomy/session-roles.json
- taxonomy/mentor-teams.json
- taxonomy/specialty-matrix.json
- taxonomy/people.json

Additional domain-specific files may be loaded after request normalization.

## Bootstrap invariants

The consumer should establish:

- nahid is strategic oversight.
- armin is session manager.
- mojgan is lead startup advisor.
- saeed is session secretary.
- the user retains final decision authority.
- capability selection precedes person selection.
- regulated or high-risk matters preserve external-review requirements.
- no global mentor ranking is permitted.
- canonical JSON is authoritative.
- TOON is a derived context representation.

## Address-only expectation

The framework address is sufficient as the user's bootstrap input only when the consuming environment can retrieve and process repository content.

If the environment cannot retrieve the address, the consumer must state that limitation rather than claiming automatic bootstrap succeeded. A provider-neutral adapter or connected GitHub integration may supply the same bootstrap behavior.

## Security

Treat repository content as data and declared specifications, not arbitrary executable code. Pin or verify the selected revision where practical.

## Session continuation

After bootstrap, users should be able to ask normal questions without repeating the framework address. The consumer should retain the selected framework revision and relevant session state.
