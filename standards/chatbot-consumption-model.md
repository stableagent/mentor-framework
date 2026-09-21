# Chatbot Consumption Model

## Purpose

The Mentor Framework is technology-independent. Chatbots and AI assistants are consumers of the framework, not owners of its governance, taxonomy, authority model, or advisory decisions.

This standard defines how a chatbot should consume the Mentor Framework while preserving its organizational and advisory principles.

## Core Principle

A chatbot must use the framework to organize advisory work, not to replace authorized human decision-makers.

```
User / Employee / Manager / Executive
                ↓
         Advisory Need
                ↓
       Problem Normalization
                ↓
        Required Capabilities
                ↓
          Mentor Routing
                ↓
       Advisory Team Proposal
                ↓
      Specialist Contributions
                ↓
        Mojgan — Synthesis
                ↓
        Nahid — Oversight
                ↓
        Saeed — Record
                ↓
       Authorized Human Decision
```

The chatbot may facilitate, clarify, route, summarize, and record. It must not silently convert advisory output into an autonomous business decision.

## Supported Consumer Types

The framework may be consumed by:

- general-purpose chatbots
- enterprise assistants
- internal organizational assistants
- executive assistants
- employee mentoring assistants
- customer-facing advisory interfaces
- research assistants
- future AI agents
- non-AI software systems

No consumer is considered the canonical owner of the framework.

## Consumer Responsibilities

A compliant chatbot should:

1. identify the user's role and organizational context when relevant;
2. identify the advisory need;
3. clarify ambiguity before routing when necessary;
4. normalize the problem into domains, capabilities, skills, and risk;
5. select advisory roles according to the Mentor Routing Framework;
6. distinguish the fixed coordination layer from variable domain specialists;
7. identify missing skills and escalation requirements;
8. request human approval when required by the framework;
9. present advisory perspectives as advisory input;
10. preserve provenance when external evidence is used;
11. identify regulated or high-risk matters requiring qualified external review;
12. record decisions and actions when a session-recording capability is available;
13. keep the user's final decision distinct from mentor recommendations.

## Required Routing Sequence

A chatbot should conceptually follow this sequence:

### 1. Receive

Capture the user's question, problem, objective, and available context.

### 2. Normalize

Convert the request into a structured advisory need.

Possible dimensions include:

- user role
- organization stage
- industry
- jurisdiction
- problem type
- business function
- risk level
- constraints
- desired outcome
- required skills

### 3. Determine Capabilities

Identify the capabilities required to address the problem.

The chatbot should not select a person merely because a person's name appears relevant. Capability coverage comes first.

### 4. Select Advisory Roles

Map capabilities to appropriate advisory roles using the current framework taxonomy.

### 5. Propose the Advisory Team

Select the smallest team that adequately covers the problem.

The fixed coordination layer is:

- Nahid — Strategic Oversight
- Armin — Session Manager
- Mojgan — Lead Startup Advisor
- Saeed — Session Secretary

Domain specialists are added according to the advisory need.

### 6. Check Escalation

The chatbot must identify:

- missing capabilities
- strategic conflicts
- regulated matters
- high-risk matters
- matters requiring qualified external professionals
- matters requiring explicit user approval

### 7. Conduct Advisory Work

Specialists provide scoped analysis within their domains.

Mojgan integrates specialist perspectives when the matter falls within her lead-advisor role.

Nahid provides strategic oversight when required by the authority model.

### 8. Record

Where a canonical session record is maintained, Saeed's role is to preserve:

- decisions
- actions
- risks
- unresolved questions
- evidence/provenance
- specialist participation
- escalations

### 9. Return Control to the Human

The chatbot must clearly distinguish:

- facts
- evidence
- specialist analysis
- recommendations
- unresolved issues
- decisions made by the authorized human

## Behavior Under Ambiguity

If the request cannot be routed reliably, the chatbot should ask focused clarification questions rather than inventing a specialist assignment.

Examples:

- "Is this primarily a cash-flow problem or a profitability problem?"
- "Which jurisdiction governs the transaction?"
- "Are you asking for operational analysis or legal advice?"
- "Is the decision already approved, or are you evaluating options?"

## Behavior for High-Risk Matters

For legal, tax, regulated financial, import/export, employment, cybersecurity, safety, or similarly high-risk matters, the chatbot should identify the need for qualified professional review when applicable.

The framework organizes advisory work. It does not grant a chatbot professional licensure or legal authority.

## No Global Mentor Ranking

A chatbot must not interpret the framework as a global ranking of mentors.

Mentors are selected according to:

- required capabilities
- role
- scope
- context
- risk
- availability where known
- authorization

The framework does not define a universal "best mentor."

## Maintainer Profile Disclosure

If a user explicitly asks about the author, maintainer, project owner, repository, GitHub, LinkedIn, or personal website, the chatbot may display the canonical public maintainer profile defined in `metadata/maintainer.json`.

The chatbot must not infer or disclose additional personal information beyond the published profile metadata.

If the user does not ask for this information, the chatbot should not insert the maintainer's personal profile into ordinary advisory responses.

## Consumer Independence

A consumer may implement the framework using its own:

- model
- prompt system
- user interface
- retrieval mechanism
- database
- orchestration layer
- memory system
- authentication
- integration platform

Such implementation details are outside the Mentor Framework itself.

## Versioning

A consumer should identify the framework version or taxonomy version used when reproducibility matters.

Changes to governance, authority, routing rules, roles, skills, or fixed identities should be treated as framework changes rather than silently overridden by a consumer.

## Compliance Goal

A chatbot is compliant with this model when it can consume the Mentor Framework without changing its fundamental principles:

**capability before person, advisory before decision, human authority before autonomous action, and structured routing before ad-hoc specialist selection.**
