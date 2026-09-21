# Context Selector Standard

## Purpose

The Context Selector is the automatic decision layer between a user's natural-language request and the minimal Mentor Framework context required to answer that request.

The intended user experience is:

    User enters the Mentor Framework address once
            ↓
    Framework is loaded
            ↓
    User asks any advisory question
            ↓
    Context Selector automatically analyzes the request
            ↓
    Relevant domains
            ↓
    Required skills
            ↓
    Applicable mentor roles
            ↓
    Smallest applicable mentor team
            ↓
    Authority / governance / escalation rules
            ↓
    Minimal Context Package
            ↓
    JSON or TOON projection
            ↓
    Advisory model
            ↓
    Mojgan synthesis + Nahid oversight + Saeed record
            ↓
    Human decision

The user should not normally need to select framework files, domains, mentors, or skills manually.

## Design principle

The selector is capability-first, not person-first.

It must answer:

1. What is the user actually asking?
2. What capabilities are required?
3. Which framework domains contain those capabilities?
4. Which mentor roles cover them?
5. Which team template is applicable?
6. Which governance and escalation rules apply?
7. What is the smallest sufficient context package?
8. Which representation is most efficient for the target consumer?

It must not begin by choosing a named mentor and then justify that choice.

## Automatic selection pipeline

### Stage 0 — Framework bootstrap

The consumer loads the Mentor Framework from its canonical repository address.

The bootstrap layer must identify:

- framework identity
- framework version
- canonical taxonomy version
- authority model
- context selector rules
- context package schema
- format/token-efficiency policy

The bootstrap layer should cache immutable or version-pinned framework metadata when the consumer supports caching.

### Stage 1 — Request normalization

Convert the user's natural-language request into a normalized advisory request.

Extract when available:

- user role
- organization type
- startup/company type
- business model
- lifecycle stage
- problem type
- jurisdiction
- risk level
- required outcome
- constraints
- approved specialist IDs
- relevant existing context

Do not invent missing facts.

Unknown values remain unknown and may trigger clarification.

### Stage 2 — Domain identification

Map the normalized request to one or more taxonomy domains.

The selector may return:

- primary domains
- secondary domains
- confidence or evidence for each mapping

Domain selection must be based on the substance of the problem, not keywords alone.

Example:

A request about importing dental equipment into Iran may involve:

- import
- international-trade
- landed-cost
- trade-finance
- legal-compliance
- supply-chain

The exact domain set depends on the normalized request.

### Stage 3 — Required capability extraction

Map the request to the smallest set of capabilities required to answer it responsibly.

Capabilities are more granular than domains.

Examples:

- financial-modeling
- cash-flow-management
- unit-economics
- import-procedure
- customs-documentation
- landed-cost
- trade-finance
- problem-validation
- customer-interviews
- product-discovery
- ux-research

The selector must distinguish:

- required
- recommended
- optional

Only required capabilities should normally determine the minimum team.

### Stage 4 — Role resolution

Map required capabilities to mentor roles using the canonical specialty matrix.

Role resolution must remain independent of individual mentor names.

Example:

    cash-flow-management
            ↓
    finance-mentor

A named person is selected only after role resolution.

### Stage 5 — Team resolution

Select the smallest applicable mentor team template that covers the required capabilities.

Selection rules:

1. Prefer complete capability coverage.
2. Minimize unnecessary specialists.
3. Prefer a predefined team template when one exists.
4. Preserve the fixed coordination layer.
5. Do not globally rank mentors.
6. Do not select a person merely because they are available.
7. Preserve regulated/high-risk escalation requirements.

### Stage 6 — Specialist resolution

Resolve named specialists only when needed.

Specialist activation must respect:

- approved specialist IDs supplied by the user
- pre-authorized specialists
- specialist activation policies
- authority rules
- regulated/high-risk requirements

If a suitable specialist is not approved or pre-authorized, the result should say approval-required rather than silently activating the person.

### Stage 7 — Governance resolution

The selector automatically adds the governance rules relevant to the selected team.

At minimum, the context package should preserve:

- final human decision authority
- Nahid strategic oversight
- Saeed session management
- Mojgan advisory synthesis
- Saeed session record responsibility
- domain-scoped specialist authority
- escalation requirements
- external professional review requirements where applicable

Governance context has higher priority than optional advisory examples.

### Stage 8 — Context minimization

The selector must remove irrelevant framework content.

It should not send the entire repository to the advisory model for every request.

Preferred priority:

1. mandatory authority rules
2. applicable safety/governance rules
3. normalized request
4. required domains
5. required skills
6. applicable mentor roles
7. applicable team definition
8. approved/pre-authorized specialist records
9. relevant examples
10. optional background material

This produces the Minimal Context Package.

### Stage 9 — Representation selection

The semantic context remains identical regardless of representation.

Supported representations:

- JSON
- TOON
- Markdown

Rules:

- Canonical repository data remains JSON.
- TOON is a derived representation for structured LLM context when it is actually more efficient.
- Markdown is preferred for human-readable explanatory material.
- Compact JSON may be used when it is smaller or simpler than TOON.
- The selector must not assume TOON always saves tokens.
- Actual tokenization should be measured when token efficiency materially matters.

### Stage 10 — Validation

Before delivery to the advisory model:

1. Validate the context package against its schema.
2. Confirm all referenced IDs exist in the canonical taxonomy.
3. Confirm authority rules are present.
4. Confirm the selected team covers required capabilities or explicitly reports missing skills.
5. Confirm escalation requirements are preserved.
6. Confirm provenance/version metadata is present.
7. Validate TOON when TOON is selected.
8. Reject or regenerate malformed context rather than silently continuing.

## Selection result

A selector result should contain, at minimum:

- request ID
- framework version
- taxonomy version
- normalized request
- selected domains
- required skills
- selected roles
- selected team
- selected specialists
- authority rules
- escalation rules
- missing skills
- approval status
- selection rationale
- excluded context
- provenance
- representation

## Ambiguity handling

The selector must not fabricate missing facts.

If ambiguity materially changes routing, it should return:

    routing_status = clarification-required

The clarification request should identify the smallest missing fact needed to continue.

If ambiguity does not materially affect routing, the selector may continue while explicitly recording the uncertainty.

## Risk handling

Risk is a routing attribute, not a reason to bypass the framework.

For regulated or high-risk matters:

- preserve the relevant domain specialist
- preserve the escalation rule
- require qualified external review where the framework specifies it
- do not represent a mentor's analysis as professional legal, tax, medical, financial, or other regulated authorization

## No global mentor ranking

The selector must never produce:

- best mentor
- worst mentor
- top mentor
- mentor score
- global mentor ranking

It resolves capability coverage and applicable authority.

## Determinism and traceability

Given the same:

- framework version
- taxonomy version
- normalized request
- authorization state
- selector rules

the selector should produce the same routing result unless an explicitly versioned external dependency changes.

Every selection should be explainable through:

    request
    → domains
    → skills
    → roles
    → team
    → specialists
    → governance
    → context package

## Provider independence

The semantic selector belongs to Mentor Framework.

A provider adapter may change:

- transport
- authentication
- context attachment mechanism
- tokenization measurement
- JSON/TOON packaging

It must not change:

- authority hierarchy
- mentor identities
- capability taxonomy
- routing semantics
- escalation requirements

This allows the same framework to be consumed by ChatGPT, Gemini, DeepSeek, Perplexity, Grok, Claude, Qwen, Microsoft Copilot, or a custom agent without maintaining a different advisory logic for each provider.

## One-address user experience

The intended user experience is:

1. User enters the canonical Mentor Framework address.
2. The consumer loads the framework bootstrap information.
3. The framework is initialized.
4. User asks a normal question.
5. Context Selector performs all routing and context selection automatically.
6. The user receives an advisory response without manually selecting mentors or files.

The framework therefore treats the repository address as a bootstrap reference, not as a request for the user to manually browse the repository.

## Important implementation boundary

A repository URL alone cannot force an arbitrary third-party chat product to continuously fetch, execute, or update repository content.

Therefore the framework defines two consumption modes:

### Mode A — Provider-supported bootstrap

If the provider can directly access the repository URL or connected GitHub resource, the consumer may load the framework automatically.

### Mode B — Framework adapter / custom agent

For fully automatic behavior independent of provider limitations, a small provider-neutral adapter performs:

    Repository
    → Bootstrap
    → Context Selector
    → Context Package
    → Provider adapter
    → LLM

The adapter is an implementation of the framework, not part of the framework's advisory taxonomy.

This distinction prevents the framework from depending on a specific AI vendor.

## Success condition

The user should be able to think only about the business problem.

They should not have to think about:

- which file to open
- which domain to select
- which mentor to call
- which specialist to add
- which governance file applies
- whether JSON or TOON is required
- how much context to send

Those decisions belong to the Context Selector and its provider adapter.
