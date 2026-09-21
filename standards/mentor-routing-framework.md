# Mentor Routing Framework

## 1. Purpose

The **Mentor Routing Framework** is the organizational framework used to determine which advisory capabilities, roles and mentors should participate in a mentoring or management consultation.

It is not an application, API, software engine or autonomous decision-maker.

The framework is designed for organizations in which experienced mentors support:

- founders and entrepreneurs;
- CEOs and senior executives;
- managers and department leaders;
- employees and key personnel;
- teams and cross-functional initiatives;
- organization-wide strategic, operational and transformation matters.

The framework organizes human expertise into a coherent advisory structure.

## 2. Core principle

The framework answers:

> **Which capabilities and advisory roles are required for this problem, who is qualified to provide them, how should their contributions be coordinated, and where is additional authority or external professional review required?**

It does not answer:

> **What business decision should the organization make?**

The final business decision remains with the responsible executive, manager, founder, board or other authorized decision-maker.

## 3. Advisory architecture

The framework has a fixed coordination layer and a variable specialist layer.

```
Organization / Person
        │
        ▼
Advisory Need
        │
        ▼
Mentor Routing Framework
        │
        ├── Required capabilities
        ├── Advisory roles
        ├── Relevant specialists
        ├── Risk / regulation
        ├── Escalation
        └── Approval
        │
        ▼
Advisory Team
        │
        ├── Nahid — Strategic Oversight
        ├── Armin — Session Manager
        ├── Mojgan — Lead Startup Advisor
        ├── Saeed — Session Secretary
        └── Domain Specialists
        │
        ▼
Integrated Advisory
        │
        ▼
Decision by authorized human
```

## 4. Fixed coordination layer

The following identities form the canonical coordination layer.

### Nahid — Strategic Oversight

Stable ID: `nahid`

Responsibilities:

- strategic oversight;
- protection of advisory quality;
- resolution of strategic conflicts;
- supervision of the session-management layer;
- escalation of organization-level or critical issues.

Nahid does not replace the decision authority of the organization's responsible person.

### Armin — Session Manager

Stable ID: `armin`

Responsibilities:

- organize the consultation;
- establish and maintain the agenda;
- coordinate participants;
- manage specialist participation;
- control transitions and session flow;
- coordinate closure and follow-up.

Armin manages the process rather than acting as the final business decision-maker.

### Mojgan — Lead Startup Advisor

Stable ID: `mojgan`

Responsibilities:

- integrate specialist perspectives;
- identify relationships and conflicts between domains;
- convert separate expert contributions into a coherent advisory view;
- identify assumptions, dependencies and unresolved questions;
- support the responsible decision-maker with an integrated perspective.

Mojgan is the synthesis layer, not the owner of the organization's final decision.

### Saeed — Session Secretary

Stable ID: `saeed`

Responsibilities:

- maintain the canonical consultation record;
- record decisions and decision owners;
- record action items and deadlines;
- preserve assumptions, evidence, risks and open questions;
- maintain provenance and historical continuity.

## 5. Variable specialist layer

Specialists are selected according to the capabilities required by the issue.

Examples include:

- finance and accounting;
- import, export and international trade;
- operations;
- warehouse and inventory;
- procurement;
- supply chain;
- market research;
- product management;
- UX;
- marketing and growth;
- sales;
- legal and compliance;
- technology;
- cybersecurity;
- AI and data;
- HR and organization;
- international expansion;
- risk and crisis;
- fundraising and investment;
- exit and M&A.

The existence of a mentor in the registry does not by itself justify involving that mentor.

## 6. Capability-first routing

Routing starts with the problem, not with a person's name.

```
Problem
  ↓
Problem type
  ↓
Required capabilities
  ↓
Advisory roles
  ↓
Qualified available mentors
  ↓
Risk / jurisdiction review
  ↓
Advisory team
```

This prevents person-driven routing and keeps the framework independent of any particular mentor roster.

## 7. Mentor Role vs Skill vs Competency

These concepts must remain separate.

| Concept | Meaning |
|---|---|
| Domain | Broad professional area |
| Role | Responsibility performed in the advisory process |
| Skill | Reusable capability |
| Competency | Demonstrable proficiency in a capability |
| Framework | Structured way of analyzing or solving a class of problems |
| Methodology | Repeatable process |
| Mentor | Person who provides one or more capabilities |
| Team | Temporary or standing combination of advisory roles |
| Escalation Rule | Condition requiring additional authority or external review |

A mentor may have many skills. A role may be filled by different mentors. A team may contain several roles.

## 8. Advisory team composition

A consultation may contain:

1. the fixed coordination layer;
2. a lead advisory role;
3. one or more domain specialists;
4. external qualified professionals when required.

The smallest team that provides adequate capability coverage should normally be preferred.

This is a coverage principle, not a ranking of people.

## 9. Approval and authority

Adding a specialist requires explicit approval unless a documented pre-authorization rule applies.

Approval states:

- `not-required`
- `pending-user`
- `approved`
- `declined`
- `pre-authorized`

The framework distinguishes:

- recommendation;
- approval;
- execution;
- recording;
- escalation;
- final decision authority.

These responsibilities must not be conflated.

## 10. Risk and professional boundaries

Some matters require current authoritative information or qualified external professionals.

Examples include:

- legal opinions;
- tax advice;
- audit and regulated accounting matters;
- regulated investment advice;
- insurance matters;
- jurisdiction-specific trade regulation;
- cybersecurity incidents;
- regulated data processing;
- other matters governed by professional licensing or current law.

The framework may identify the need for such review but must not represent a mentor's general expertise as a substitute for required professional authority.

## 11. Strategic escalation

Escalation to Nahid is appropriate when:

- strategic objectives conflict;
- authority boundaries are unclear;
- a critical issue may have organization-wide or irreversible consequences;
- the advisory team cannot establish a defensible capability or authority boundary;
- cross-domain disagreement cannot be resolved at the session-management level.

Escalation does not transfer final decision authority away from the responsible human decision-maker.

## 12. Consultation lifecycle

```
Need identified
      ↓
Context clarified
      ↓
Required capabilities identified
      ↓
Roles selected
      ↓
Specialists identified
      ↓
Risk / jurisdiction reviewed
      ↓
Approval obtained where required
      ↓
Armin coordinates consultation
      ↓
Specialists provide domain analysis
      ↓
Mojgan integrates perspectives
      ↓
Nahid provides strategic oversight when required
      ↓
Saeed records the canonical outcome
      ↓
Responsible human makes or confirms decisions
      ↓
Actions and follow-up are tracked
```

## 13. Organizational scope

The framework is not limited to startup founders.

It can be used for:

### Executive advisory

- CEO;
- founders;
- board-level preparation;
- C-level executives;
- strategic initiatives.

### Management advisory

- department heads;
- operations managers;
- product managers;
- finance managers;
- HR managers;
- project and program leaders.

### Employee advisory

- individual development;
- role transitions;
- performance challenges;
- cross-functional problems;
- escalation preparation.

### Organization-wide advisory

- restructuring;
- international expansion;
- transformation;
- crisis response;
- operational redesign;
- major technology initiatives;
- M&A preparation.

Startup mentoring remains an important use case, but it is one application of the broader organizational advisory framework.

## 14. Evidence and provenance

Advisory records should distinguish:

- verified facts;
- assumptions;
- estimates;
- hypotheses;
- interpretations;
- recommendations;
- decisions.

Each significant recommendation should be traceable to the capabilities and evidence used to formulate it.

Historical consultation records must remain interpretable under the taxonomy version that existed when they were created.

## 15. No ranking principle

The framework must not create a global ranking of mentors.

It should answer:

> Which mentor or combination of mentors satisfies the required capability and authority constraints?

It should not answer:

> Which mentor is the best?

A mentor may be a suitable match for one problem and not another without implying a global quality judgment.

## 16. Technology independence

The framework is intentionally independent of:

- Django;
- REST APIs;
- databases;
- AI model providers;
- agent frameworks;
- cloud platforms;
- programming languages.

Software may implement or consume this framework later, but the framework remains the normative organizational model.

## 17. Relationship to the repository

The repository separates:

- normative standards;
- taxonomy;
- mentor identities;
- skills and competencies;
- advisory team definitions;
- routing rules;
- schemas;
- examples.

The repository therefore serves as the canonical knowledge and governance foundation for the mentor organization.

## 18. Versioning

Changes to roles, skills, authority rules, fixed identities or routing rules must be versioned.

Historical consultation records must preserve the relevant taxonomy and framework versions.

Breaking changes to stable identifiers or authority contracts require a major version.

