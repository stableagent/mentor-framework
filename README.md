# Mentor Framework

**Mentor Framework** is a multilingual, machine-readable foundation for organizational mentoring and professional business advisory systems.

## Project status

- Specification: Mentor Framework v1.0 foundation
- Current repository version: 1.0.1
- Canonical data model: JSON
- LLM representation: TOON
- Human documentation: Markdown
- Localization: language-only ISO 639-1 codes
- AI dependency: none
- Primary use cases: executive mentoring, management mentoring, employee mentoring, startup advisory, virtual advisory boards, competency mapping, mentor routing and organizational advisory.

## One-address automatic experience

The intended end-user experience is deliberately simple:

    User
      ↓
    enters Mentor Framework address once
      ↓
    Context Selector initializes
      ↓
    User asks a normal question
      ↓
    automatic normalization
      ↓
    automatic domain / skill / role resolution
      ↓
    automatic mentor-team selection
      ↓
    automatic authority / escalation processing
      ↓
    minimal context package
      ↓
    JSON or TOON
      ↓
    advisory model
      ↓
    answer

The user should not normally have to choose files, domains, skills, mentors or formats manually.

The canonical bootstrap instruction is in BOOTSTRAP.md. The machine-readable manifest is FRAMEWORK-MANIFEST.json.

Important: a repository URL is a bootstrap reference. An arbitrary third-party chat product cannot be assumed to fetch, execute or continuously update repository content merely because a URL was entered. Where direct repository access is unavailable, a provider-neutral adapter or connected GitHub integration must perform the same Context Engine process.

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

The repository is the normative framework, not a provider-specific chatbot application.

## Canonical Taxonomy Registries

The canonical taxonomy is split into people, advisory roles and skills. `taxonomy/people.json` defines fixed identities and mentors; `taxonomy/advisory-roles.json` defines role IDs; `taxonomy/skills.json` defines stable skill IDs. Specialty and team registries reference these IDs.

## Context Selector and Context Engine

The Context Selector identifies the relevant capability set. The Context Engine applies deterministic routing, governance, minimization and validation.

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

## Provider Adapter

The provider adapter is deliberately outside the framework semantics. It connects the Context Engine to ChatGPT, Gemini, Claude, DeepSeek, Grok, Qwen, Perplexity, Copilot or a custom agent.

See standards/provider-adapter.md.

Adapters must not redefine taxonomy, authority, fixed identities, escalation or specialist approval.

## Session lifecycle

    bootstrap → initialize → request → normalize → route
    → approve/escalate → advise → synthesize → decide
    → record → follow-up → close

See standards/session-lifecycle.md.

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

## Core principles

1. AI-independent.
2. Canonical JSON.
3. TOON is a derived projection, not a second source of truth.
4. Token-efficient minimal context.
5. Stable semantic identifiers.
6. Separate localization.
7. Clear role/skill/competency separation.
8. Capability-first routing.
9. Multi-mentor collaboration.
10. Evidence discipline.
11. External review for regulated or high-risk matters.
12. Human final decision authority.
13. No global mentor ranking.
14. Provider adapters cannot override framework governance.

## Fixed coordination layer

- nahid — strategic oversight
- saeed — session manager (Persian: سعید; English: Steeve)
- mojgan — lead startup advisor (Persian: مژگان; English: Mojgan)
- session recording — system function; no fixed person

The display order is not a ranking. Fixed identities are resolved by stable IDs; role duties must not be reassigned dynamically.

## Localization

Language-only ISO 639-1 codes are used initially:

en, fa, de, fr, ar, tr, ur, zh, es, pt, ru, ja, ko, hi, it, id, nl, pl, uk, vi, th, he, sv, no, da, fi, cs, ro, el, hu

## Maintainer

The framework is authored and maintained by **سعید اسمعیل زائی (Saeed Esmailzaee)**.

Public maintainer profile is disclosed only when explicitly requested:

- GitHub: https://github.com/stableagent
- LinkedIn: https://www.linkedin.com/in/esmailzaee/
- Website: https://www.esmailzaee.ir/
- Repository: https://github.com/stableagent/mentor-framework

Machine-readable metadata: metadata/maintainer.json.

## Safety and professional boundaries

This repository is a knowledge, capability and advisory-governance reference. It does not replace licensed legal, tax, audit, medical, investment, accounting or other regulated professional advice. Jurisdiction-specific and time-sensitive claims must be verified against current authoritative sources.

## Versioning

The repository version is tracked in VERSION. Breaking changes to identifiers or entity contracts require a major version.

See CHANGELOG.md and standards/ for normative project rules.
