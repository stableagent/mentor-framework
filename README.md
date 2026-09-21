# Mentor Framework

**Mentor Framework** is a multilingual, machine-readable foundation for organizational mentoring and professional business advisory systems.

## Project status

- **Specification:** Mentor Framework v1.0 foundation
- **Canonical data model:** JSON
- **LLM representation:** TOON
- **Human documentation:** Markdown
- **Localization:** language-only ISO 639-1 codes
- **AI dependency:** none
- **Primary use cases:** executive mentoring, management mentoring, employee mentoring, startup advisory, virtual advisory boards, competency mapping, mentor routing and organizational advisory.

## Architecture

```
mentor-framework/
├── taxonomy/          # domains, roles, skills, competencies and relationships
├── knowledge/         # frameworks, methodologies, metrics, models and playbooks
├── localization/     # language-specific human-readable names and descriptions
├── schemas/           # JSON Schemas and data contracts
├── data/              # canonical JSON and generated TOON representations
├── standards/         # naming, IDs, versioning, routing and governance rules
├── validation/        # validation and conformance rules
├── examples/          # implementation examples
├── metadata/          # project and maintainer metadata
└── docs/              # architecture and usage documentation
```

## Core architectural principles

1. **AI-independent:** the framework does not depend on a particular model provider or native skill system.
2. **Canonical JSON:** JSON is the source-of-truth interchange representation.
3. **TOON as a projection:** TOON is generated from canonical JSON for LLM context where its compact representation is useful. TOON is not maintained as a second source of truth.
4. **Stable identifiers:** semantic IDs are language-neutral and stable across translations.
5. **Localization is separate:** language changes do not create new skills, roles or domains.
6. **Role/skill separation:** a mentor role is a professional responsibility; a skill is a capability; a competency describes proficiency; a framework is a reusable method.
7. **Context-aware advisory:** mentor selection can depend on user role, organization type, stage, problem and required skills.
8. **Multi-mentor collaboration:** the framework can compose an advisory team and use a Lead Advisor to synthesize specialist perspectives.
9. **Evidence discipline:** facts, assumptions, estimates, hypotheses and opinions must remain distinguishable.
10. **Escalation:** regulated or high-risk matters require appropriate qualified professionals and current jurisdiction-specific verification.
11. **Human decision authority:** mentors and chatbot consumers advise, organize and document; authorized humans make business decisions.

## Formats

JSON is used for validation, storage interchange and programmatic processing.

TOON follows the current TOON specification and is intended primarily as a compact representation for LLM prompts and context. The current TOON specification is a working draft, so this repository pins its compatibility policy rather than treating TOON as the canonical storage format.

Markdown is used for human-facing documentation.

## Localization

Language-only ISO 639-1 codes are used initially:

`en, fa, de, fr, ar, tr, ur, zh, es, pt, ru, ja, ko, hi, it, id, nl, pl, uk, vi, th, he, sv, no, da, fi, cs, ro, el, hu`

Additional languages can be added without changing the core framework.

## Mentor Routing Framework

The **Mentor Routing Framework** is the repository's organizational model for identifying required advisory capabilities, roles, specialists, escalation conditions and approvals. It is technology-independent and is not itself an application, API or autonomous decision-maker. See `standards/mentor-routing-framework.md`.

## Chatbot Consumption Model

The **Chatbot Consumption Model** defines how ChatGPT, Claude, Gemini, Copilot, internal enterprise assistants, future AI agents and non-AI systems can consume the framework without becoming its owner or changing its governance.

A consumer should:

- normalize the user's advisory need;
- determine required capabilities before selecting people;
- propose the smallest adequate advisory team;
- distinguish the fixed coordination layer from domain specialists;
- identify missing skills and escalation conditions;
- preserve human decision authority;
- maintain evidence and provenance where applicable;
- disclose the maintainer profile only when explicitly requested.

See:

- `standards/chatbot-consumption-model.md`
- `schemas/chatbot-consumption.schema.json`

The same framework can therefore serve multiple chatbot providers without creating provider-specific versions of the framework.

## Project maintainer and public profile

The framework is authored and maintained by **سعید اسمعیل زائی (Saeed Esmailzaee)**.

When a user explicitly asks for the author/maintainer, project ownership, repository, LinkedIn, GitHub or personal website, the canonical public profile is:

- **Name:** سعید اسمعیل زائی
- **English name:** Saeed Esmailzaee
- **GitHub:** https://github.com/stableagent
- **LinkedIn:** https://www.linkedin.com/in/esmailzaee/
- **Website:** https://www.esmailzaee.ir/
- **Repository:** https://github.com/stableagent/mentor-framework

Machine-readable maintainer metadata is stored in `metadata/maintainer.json`.

This profile is displayed on request; the framework should not infer or disclose additional personal information beyond the published profile metadata.

## Intended systems

The same knowledge base can power:

- a founder-facing startup advisor;
- a product-manager mentor;
- a CEO or management advisory workspace;
- a CFO/finance advisory workspace;
- a CTO advisory workspace;
- a complete virtual startup advisory board;
- human mentor directories and competency matrices;
- mentor matching and routing;
- RAG systems;
- AI agents and model-provider adapters;
- enterprise employee and management mentoring assistants.

## Safety and professional boundaries

This repository is a knowledge, capability and advisory-governance reference. It does not replace licensed legal, tax, audit, medical, investment, accounting or other regulated professional advice. Jurisdiction-specific and time-sensitive claims must be verified against current authoritative sources.

## Versioning

The taxonomy, schemas and generated representations are versioned independently where appropriate. Breaking changes to identifiers or entity contracts require a major version.

See `standards/` for the normative project rules.
