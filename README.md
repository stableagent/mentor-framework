# Mentor Skills

**Mentor Skills** is a multilingual, machine-readable taxonomy and knowledge foundation for professional startup mentoring and business advisory systems.

## Project status

- **Specification:** Mentor Skills v1.0 foundation
- **Canonical data model:** JSON
- **LLM representation:** TOON
- **Human documentation:** Markdown
- **Localization:** language-only ISO 639-1 codes
- **AI dependency:** none
- **Primary use cases:** human mentors, AI mentors, mentor routers, virtual advisory boards, competency mapping, startup diagnostics, APIs, RAG and agent systems.

## Architecture

```
mentor-skills/
├── taxonomy/          # domains, roles, skills, competencies and relationships
├── knowledge/         # frameworks, methodologies, metrics, models and playbooks
├── localization/     # language-specific human-readable names and descriptions
├── schemas/           # JSON Schemas and data contracts
├── data/              # canonical JSON and generated TOON representations
├── standards/         # naming, IDs, versioning and format rules
├── validation/        # validation and conformance rules
├── examples/          # implementation examples
└── docs/              # architecture and usage documentation
```

## Core architectural principles

1. **AI-independent:** the taxonomy does not depend on a particular model provider or native skill system.
2. **Canonical JSON:** JSON is the source-of-truth interchange representation.
3. **TOON as a projection:** TOON is generated from canonical JSON for LLM context where its compact representation is useful. TOON is not maintained as a second source of truth.
4. **Stable identifiers:** semantic IDs are language-neutral and stable across translations.
5. **Localization is separate:** language changes do not create new skills, roles or domains.
6. **Role/skill separation:** a mentor role is a professional responsibility; a skill is a capability; a competency describes proficiency; a framework is a reusable method.
7. **Context-aware advisory:** mentor selection can depend on user role, startup type, startup stage, problem and required skills.
8. **Multi-mentor collaboration:** the system can compose a virtual advisory team and use a Lead Advisor to synthesize specialist perspectives.
9. **Evidence discipline:** facts, assumptions, estimates, hypotheses and opinions must remain distinguishable.
10. **Escalation:** regulated or high-risk matters require appropriate qualified professionals and current jurisdiction-specific verification.

## Formats

JSON is used for APIs, validation, storage interchange and programmatic processing.

TOON follows the current TOON specification and is intended primarily as a compact representation for LLM prompts and context. The current TOON specification is a working draft, so this repository pins its compatibility policy rather than treating TOON as the canonical storage format.

Markdown is used for human-facing documentation.

## Localization

Language-only ISO 639-1 codes are used initially:

`en, fa, de, fr, ar, tr, ur, zh, es, pt, ru, ja, ko, hi, it, id, nl, pl, uk, vi, th, he, sv, no, da, fi, cs, ro, el, hu`

Additional languages can be added without changing the core taxonomy.

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
- AI agents and model-provider adapters.

## Safety and professional boundaries

This repository is a knowledge and capability reference. It does not replace licensed legal, tax, audit, medical, investment, accounting or other regulated professional advice. Jurisdiction-specific and time-sensitive claims must be verified against current authoritative sources.

## Versioning

The taxonomy, schemas and generated representations are versioned independently where appropriate. Breaking changes to identifiers or entity contracts require a major version.

See `standards/` for the normative project rules.
