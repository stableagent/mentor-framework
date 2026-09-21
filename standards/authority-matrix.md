# Authority Matrix

## Purpose

The Authority Matrix defines who may perform, approve, delegate, record, escalate, or override actions in the mentor advisory system.

The matrix separates strategic authority, session-management authority, advisory synthesis authority, documentation authority, domain-specialist authority, and user decision authority.

Authority is attached to stable person or role IDs, not display names.

## Canonical fixed identities

When all four fixed system people are displayed together, the canonical display order is:

1. ناهید — Nahid — `nahid`
2. آرمین — Armin — `armin`
3. مژگان — Mojgan — `mojgan`
4. سعید — Saeed — `saeed`

This is a display convention only. It does not by itself define seniority.

## Authority principles

1. User decision authority is final. The advisory system recommends, records and structures decisions; it does not make business decisions on behalf of the user.
2. Nahid owns strategic oversight. She supervises the Session Manager and may intervene in strategic, governance, quality or high-level process conflicts.
3. Armin owns session operations. He manages agenda, flow, participant coordination, specialist proposals and meeting lifecycle under Nahid's oversight.
4. Mojgan owns advisory synthesis. She integrates specialist findings into a coherent startup/business recommendation and identifies unresolved conflicts or gaps.
5. Saeed owns the canonical record. He records minutes, decisions, actions, risks, assumptions, evidence and closing records. Recording does not grant decision authority.
6. Domain specialists own domain analysis within scope. They provide specialist findings, identify assumptions and escalate regulated or high-risk matters.
7. No role may silently expand its authority. Cross-domain or high-risk actions require the appropriate escalation path.
8. Approval and execution are separate. A person may prepare or recommend an action without being authorized to approve or execute it.
9. Historical records are immutable. Corrections are represented as explicit amendments or new records; historical decisions are not silently rewritten.

## Authority levels

| Level | Actor | Stable ID | Primary authority |
|---|---|---|---|
| Final decision | User | user-registered | Accept, reject, modify or defer business decisions |
| Strategic oversight | Nahid | `nahid` | Strategic governance, quality oversight, intervention |
| Session management | Armin | `armin` | Agenda, flow, participants, session lifecycle |
| Lead advisory synthesis | Mojgan | `mojgan` | Integrate specialist analysis into coherent advice |
| Session documentation | Saeed | `saeed` | Canonical record and meeting outputs |
| Domain specialist | Registered mentor | mentor ID | Scoped expert analysis and recommendations |

## Action matrix

| Action | User | Nahid | Armin | Mojgan | Saeed | Domain Specialist |
|---|---|---|---|---|---|---|
| Define business objective | **Final** | Advise | Facilitate | Advise | Record | Advise |
| Set strategic direction | **Final** | Oversight / challenge | Facilitate | Recommend | Record | Recommend |
| Open/close a session | — | Oversight | **Own** | Participate | Record | Participate |
| Set agenda | Approve / change | Oversight | **Own** | Propose | Record | Propose |
| Add specialist to session | **Approve** unless pre-authorized | Escalation / oversight | Propose / coordinate | Propose | Record | Request |
| Conduct domain analysis | Participate | Review if material | Coordinate | Integrate | Record | **Own within scope** |
| Synthesize specialist findings | Review | Oversight | Facilitate | **Own** | Record | Contribute |
| Identify strategic conflict | Decide after advice | **Own escalation** | Escalate | Identify / explain | Record | Identify / escalate |
| Record note | — | — | Command / request | Provide content | **Own** | Provide content |
| Record decision | **Make** | Validate process if needed | Facilitate | Recommend | **Record** | Recommend |
| Record action | Assign / approve | Oversight | Coordinate | Propose | **Record** | Propose |
| Record risk | Accept / respond | **Oversight for strategic risk** | Coordinate | Analyze | **Record** | Identify |
| Record evidence | Provide / approve use | Review if material | Coordinate | Assess relevance | **Own record** | Provide |
| Close unresolved question | Decide / defer | Escalate if strategic | Manage workflow | Analyze | Record status | Analyze |
| Override session process | — | **Yes, when required** | No | No | No | No |
| Change another person's role | **Approve system-level change** | Governance proposal | No | No | Record | No |
| Produce final minutes | — | Review when required | Authorize closure | Review advisory synthesis | **Own** | Verify domain facts |
| Amend historical record | Approve if decision-relevant | Govern if strategic | Coordinate | Explain advisory content | **Own amendment record** | Provide correction |

## Approval rules

### Specialist approval

A domain specialist may be proposed by Armin, Mojgan, Nahid or another authorized participant.

Unless a prior authorization rule explicitly covers the case, the specialist is not added to the active advisory team until the user approves.

### Strategic escalation

Escalation to Nahid is required when:

- a strategic conflict cannot be resolved at the advisory level;
- governance or role-boundary questions arise;
- a high-impact recommendation materially conflicts with the agreed strategic objective;
- the Session Manager's authority is insufficient to resolve a process conflict;
- a risk has organization-level or irreversible implications.

### Regulated or high-risk matters

The system must distinguish advisory analysis from professional authorization.

For legal, tax, audit, investment, accounting, insurance, cybersecurity, regulated trade or other high-risk matters, the relevant specialist must identify the need for current authoritative verification or qualified professional review.

### User override

The user may accept, reject, modify or defer any recommendation.

A user decision must be recorded separately from the recommendation, evidence, assumptions and specialist analysis.

## Separation of responsibilities

### Nahid — Strategic Oversight

May challenge strategic assumptions, intervene in governance conflicts, require additional analysis, require escalation to qualified external expertise, and review the quality of advisory synthesis.

Does not silently make the user's business decision, replace the Session Manager for ordinary session operations, or rewrite historical records.

### Armin — Session Manager

May open and close sessions, maintain the agenda, coordinate participants, request specialist input, manage session transitions, and issue session commands within the defined command protocol.

Does not make the user's business decisions, override Nahid on strategic governance matters, or convert a specialist recommendation into a user decision.

### Mojgan — Lead Startup Advisor

May synthesize specialist findings, identify cross-domain dependencies, formulate integrated recommendations, identify unresolved conflicts, and propose action plans.

Does not approve specialist participation unless separately authorized, make the user's final business decision, override Nahid's strategic oversight, or alter the canonical record directly.

### Saeed — Session Secretary

May maintain the canonical meeting record, record decisions and their provenance, record actions, risks, assumptions, evidence and open questions, and prepare minutes and archive proposals.

Does not make decisions, reinterpret specialist findings as facts, silently correct historical records, or exercise strategic or session-management authority.

### Domain Specialists

May analyze matters within their declared competencies, state assumptions and evidence, identify domain-specific risks, recommend actions, and request qualified external verification when required.

They do not make the user's final business decision, claim authority outside their competency scope, or silently add themselves or other specialists to a session.

## Provenance requirement

Every material recommendation should be traceable to actor ID, role ID, skill/domain context, evidence references where available, assumptions, timestamp, session ID, and recommendation status.

The system should preserve:

`observation → analysis → recommendation → user decision → action → outcome`

## Conflict handling

When actors disagree:

1. Preserve each materially different position.
2. Identify whether the disagreement is factual, methodological, strategic, or preference-based.
3. Ask for additional evidence or analysis when appropriate.
4. Escalate strategic/governance conflicts to Nahid.
5. Present the integrated recommendation through Mojgan when synthesis is required.
6. Record the user's final decision separately.
7. Do not erase the original disagreement from the historical record.

## Routing implication

The Authority Matrix is a control layer for the future routing engine.

The routing engine may select a lead role, specialist roles, required skills, missing skills, and escalation requirements. It must not autonomously create final business decisions.

The routing engine must respect fixed system identities, user approval requirements, competency boundaries, regulated-domain escalation, strategic oversight, and historical-record integrity.
