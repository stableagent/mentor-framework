# Format and Token Efficiency Policy

## Purpose

Mentor Framework is designed to be consumed by humans, software systems and LLM-based assistants. Its data formats therefore have different responsibilities.

The framework must minimize unnecessary context and token consumption without sacrificing semantic correctness, deterministic structure or validation.

## Source of Truth

**Canonical JSON is the source of truth.**

JSON is used for:

- canonical data storage;
- schema validation;
- deterministic interchange;
- machine processing;
- version control.

TOON is a **derived LLM-context representation** of canonical JSON. It must not become a second independently maintained source of truth.

## LLM Context Format

When structured framework data is supplied to an LLM, TOON SHOULD be preferred when it reduces token usage for the relevant dataset and the consumer supports TOON.

TOON is particularly appropriate for:

- arrays of uniform objects;
- mentor registries;
- skills;
- role-to-skill mappings;
- domain-to-specialty mappings;
- routing tables;
- mentor-team definitions;
- session records with repeated structures;
- other tabular or semi-tabular data.

TOON is less advantageous for every possible structure. Consumers SHOULD measure token usage for irregular or very small structures and may use compact JSON when it is smaller or operationally safer.

## Token Efficiency Rules

Consumers SHOULD:

1. send only the fields required for the current task;
2. avoid repeating schema descriptions when a compact representative example is sufficient;
3. avoid duplicating the same taxonomy in multiple prompt sections;
4. load domain-specific subsets instead of the entire framework when possible;
5. prefer stable IDs over repeatedly transmitting long descriptions;
6. use TOON for repeated uniform records;
7. use tab delimiters for large tabular TOON payloads when supported;
8. keep examples small, generally 2–5 rows, when examples are used only to teach the format;
9. validate generated TOON in strict mode before treating it as structured data;
10. preserve the canonical JSON representation outside the LLM context.

## Context Selection

A chatbot SHOULD NOT send the entire Mentor Framework to the model for every request.

The preferred pattern is:

```
User Request
    ↓
Problem Normalization
    ↓
Relevant Domains
    ↓
Relevant Roles
    ↓
Required Skills
    ↓
Relevant Mentor Teams
    ↓
Minimal Context Package
    ↓
LLM
```

The objective is **minimum sufficient context**, not maximum context.

## Progressive Disclosure

Consumers SHOULD use progressive context loading:

### Level 1 — Routing

Load only the information necessary to determine the relevant capabilities and advisory roles.

### Level 2 — Team Formation

Load the relevant mentor-team definitions and specialist mappings.

### Level 3 — Advisory Work

Load the specific methodologies, knowledge, evidence and specialist context required for the selected team.

### Level 4 — Record

Load only the session data needed to preserve decisions, actions, risks and provenance.

This prevents large general-purpose knowledge bases from being injected into every conversation.

## Representation Policy

The same conceptual data may exist in:

```
JSON
  ↓
TOON projection
  ↓
LLM context
```

The LLM-facing representation may be optimized for token efficiency, but semantic meaning, stable IDs and field relationships MUST remain equivalent to canonical JSON.

## Measurement

Token savings MUST NOT be assumed to be universal.

TOON's published benchmarks show substantial savings against formatted JSON on tested datasets, while the magnitude varies by structure and tokenizer. Consumers SHOULD measure actual token counts and, where latency matters, time-to-first-token and throughput for their selected model and tokenizer.

The current published TOON specification is v4.1 (2026-07-25), a stable working draft. Consumers implementing TOON SHOULD pin and test against a specific compatible version.

## Delimiter Policy

For large tabular payloads, consumers MAY use tab-delimited TOON because tabs can tokenize efficiently and reduce delimiter/quoting overhead.

The selected delimiter MUST be declared by the TOON representation and MUST be interpreted according to the applicable TOON specification.

## Validation

Generated or modified TOON SHOULD be decoded and validated in strict mode before being persisted or passed to another system as authoritative structured data.

A malformed or truncated TOON payload MUST NOT silently replace canonical JSON.

## Human Documentation

Markdown remains the preferred format for:

- architecture;
- standards;
- explanations;
- policies;
- tutorials;
- human-readable examples.

Human documentation SHOULD NOT duplicate large machine-readable datasets.

## Format Decision Rule

Use the smallest representation that preserves the required semantics:

```
Human explanation  → Markdown
Canonical data     → JSON
LLM structured data → TOON when beneficial
Small/simple data  → compact JSON when smaller or simpler
Large uniform data → TOON, preferably tab-delimited
```

The goal is not to use TOON everywhere. The goal is to minimize context cost while preserving correctness and interoperability.
