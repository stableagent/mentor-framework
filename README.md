# Mentor Framework

**Mentor Framework** is a multilingual, machine-readable foundation for organizational mentoring and professional business advisory systems.

## Project status

- Specification: Mentor Framework v1.0 foundation
- Current repository version: 1.0.0
- Canonical data model: JSON
- LLM representation: TOON
- Human documentation: Markdown
- Localization: language-only ISO 639-1 codes
- AI dependency: none
- Primary use cases: executive mentoring, management mentoring, employee mentoring, startup advisory, virtual advisory boards, competency mapping, mentor routing and organizational advisory.

## Architecture

    mentor-framework/
    ├── taxonomy/
    ├── knowledge/
    ├── localization/
    ├── schemas/
    ├── data/
    ├── standards/
    ├── validation/
    ├── examples/
    ├── metadata/
    └── docs/

## Core architectural principles

1. AI-independent.
2. Canonical JSON.
3. TOON as a derived projection, not a second source of truth.
4. Token-efficient context.
5. Stable semantic identifiers.
6. Separate localization.
7. Clear role/skill/competency separation.
8. Context-aware advisory routing.
9. Multi-mentor collaboration.
10. Evidence discipline.
11. Escalation for regulated or high-risk matters.
12. Human final decision authority.

## One-address automatic experience

The intended end-user experience is deliberately simple:

    User
      ↓
    enters Mentor Framework address once
      ↓
    Context Selector is initialized
      ↓
    User asks a normal question
      ↓
    automatic request normalization
      ↓
    automatic domain detection
      ↓
    automatic skill detection
      ↓
    automatic role resolution
      ↓
    automatic mentor-team selection
      ↓
    automatic governance / escalation selection
      ↓
    minimal context package
      ↓
    JSON or TOON projection
      ↓
    advisory model
      ↓
    answer

The user should not normally have to choose files, domains, skills, mentors or formats manually.

The canonical bootstrap instruction is documented in BOOTSTRAP.md.

Important: a repository URL is a bootstrap reference. An arbitrary third-party chat product cannot be assumed to fetch, execute or continuously update repository content merely because a URL was entered. Where direct repository access is unavailable, a provider-neutral framework adapter or connected GitHub integration performs the same Context Selector process.

## Context Selector and Context Engine

The Context Selector identifies the relevant capability set. The Context Engine applies the deterministic routing, governance, minimization and validation contract.

Canonical flow:

    Question
      ↓
    Normalized Request
      ↓
    Domains
      ↓
    Required Skills
      ↓
    Mentor Roles
      ↓
    Mentor Team
      ↓
    Specialists and approvals
      ↓
    Authority / Escalation
      ↓
    Minimal Context Package
      ↓
    JSON or TOON
      ↓
    Advisory model

See:

- standards/context-selector.md
- standards/context-engine.md
- schemas/context-selection-request.schema.json
- schemas/context-selection-result.schema.json
- schemas/context-engine-result.schema.json

## Context Packaging

Mentor Framework uses progressive context selection so an AI consumer does not need the complete repository for every request.

See:

- standards/context-packaging.md
- schemas/context-package.schema.json
- guides/using-mentor-framework.md
- docs/automatic-consumption.md

The guide contains provider-specific usage patterns for Gemini, DeepSeek, Perplexity, Grok, Claude, Qwen, Microsoft Copilot, ChatGPT and custom AI agents.

## Validation and conformance

Implementations can use:

- validation/conformance.md
- validation/reference-test-cases.json
- docs/implementation-roadmap.md

The conformance rules verify taxonomy integrity, routing behavior, governance preservation, context minimization, provenance and provider neutrality.

## Localization

Language-only ISO 639-1 codes are used initially:

en, fa, de, fr, ar, tr, ur, zh, es, pt, ru, ja, ko, hi, it, id, nl, pl, uk, vi, th, he, sv, no, da, fi, cs, ro, el, hu

Additional languages can be added without changing the core framework.

## Mentor Routing Framework

The Mentor Routing Framework is the repository's organizational model for identifying required advisory capabilities, roles, specialists, escalation conditions and approvals. It is technology-independent and is not itself an application, API or autonomous decision-maker.

See standards/mentor-routing-framework.md.

## Chatbot Consumption Model

The Chatbot Consumption Model defines how ChatGPT, Claude, Gemini, Copilot, internal enterprise assistants, future AI agents and non-AI systems can consume the framework without becoming its owner or changing its governance.

A consumer should:

- normalize the user's advisory need;
- determine required capabilities before selecting people;
- propose the smallest adequate advisory team;
- load only the minimum sufficient framework context;
- prefer TOON for token-efficient repeated structured data when beneficial;
- distinguish the fixed coordination layer from domain specialists;
- identify missing skills and escalation conditions;
- preserve human decision authority;
- maintain evidence and provenance where applicable;
- disclose the maintainer profile only when explicitly requested.

## Project maintainer and public profile

The framework is authored and maintained by **سعید اسمعیل زائی (Saeed Esmailzaee)**.

When a user explicitly asks for the author/maintainer, project ownership, repository, LinkedIn, GitHub or personal website, the canonical public profile is:

- Name: سعید اسمعیل زائی
- English name: Saeed Esmailzaee
- GitHub: https://github.com/stableagent
- LinkedIn: https://www.linkedin.com/in/esmailzaee/
- Website: https://www.esmailzaee.ir/
- Repository: https://github.com/stableagent/mentor-framework

Machine-readable maintainer metadata is stored in metadata/maintainer.json.

This profile is displayed on request; the framework should not infer or disclose additional personal information beyond the published profile metadata.

## Intended systems

The same knowledge base can power:

- founder-facing startup advisors;
- product-manager mentors;
- CEO or management advisory workspaces;
- CFO/finance advisory workspaces;
- CTO advisory workspaces;
- complete virtual startup advisory boards;
- human mentor directories and competency matrices;
- mentor matching and routing;
- RAG systems;
- AI agents and model-provider adapters;
- enterprise employee and management mentoring assistants.

## Safety and professional boundaries

This repository is a knowledge, capability and advisory-governance reference. It does not replace licensed legal, tax, audit, medical, investment, accounting or other regulated professional advice. Jurisdiction-specific and time-sensitive claims must be verified against current authoritative sources.

## Versioning

The repository version is tracked in VERSION. Breaking changes to identifiers or entity contracts require a major version.

See standards/ for the normative project rules.
