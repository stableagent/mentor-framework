# Context Packaging Standard

## Purpose

Mentor Framework is designed to be consumed by AI systems without loading the entire framework into every conversation.

The consumer MUST select the smallest context package that is sufficient for the current advisory task.

This standard is technology-independent. It applies to ChatGPT, Gemini, Claude, DeepSeek, Perplexity, Grok, Qwen, Copilot, custom agents, and non-AI consumers.

## Core rule

> Select capability first, context second, people third.

The consumer MUST NOT start by loading every mentor, every domain, or the entire repository.

Preferred pipeline:

~~~text
User Request
    ↓
Problem Normalization
    ↓
Relevant Domains
    ↓
Required Skills
    ↓
Relevant Roles
    ↓
Relevant Mentor Teams
    ↓
Applicable Governance / Escalation Rules
    ↓
Minimal Context Package
    ↓
TOON projection when beneficial
    ↓
AI reasoning
~~~

## Progressive context levels

### Level 1 — Routing

Load only:

- request classification
- relevant domains
- required skills
- risk level
- jurisdiction
- applicable routing rules

Goal: identify the appropriate capability set.

### Level 2 — Team formation

Add:

- relevant mentor-team templates
- lead role
- specialist roles
- skill coverage
- approval requirements
- escalation requirements

Goal: construct the smallest appropriate advisory team.

### Level 3 — Advisory work

Add only the knowledge needed to answer the specific advisory question:

- applicable methods
- domain guidance
- specialist inputs
- relevant evidence
- constraints
- governance rules

Goal: perform the advisory work without unrelated framework context.

### Level 4 — Record

Add:

- decisions
- actions
- risks
- unresolved questions
- provenance
- meeting metadata

Goal: produce a durable advisory record.

## Context package structure

A context package SHOULD contain:

1. framework version
2. taxonomy version
3. context profile
4. normalized request
5. selected domains
6. required skills
7. selected roles
8. selected team templates
9. applicable authority rules
10. applicable escalation rules
11. relevant specialist records
12. provenance
13. representation format

Optional fields include a model-specific context budget and tokenizer metadata.

Token budgets MUST NOT be treated as universal because tokenization differs between providers and models.

## Format policy

Canonical structured data lives in JSON.

TOON is a derived projection for LLM consumption. It is NOT a second source of truth.

Use:

- Markdown for human instructions and explanations.
- JSON for canonical structured data and interoperability.
- TOON when structured data is repetitive and the consumer supports it efficiently.
- Compact JSON when it is smaller or clearer than TOON.

For large uniform arrays, TOON with tab delimiters SHOULD be considered when supported by the target consumer.

## Context minimization rules

The consumer SHOULD:

- load only relevant domains
- load only required skills
- select the smallest applicable team
- use stable IDs rather than repeating long descriptions
- avoid duplicating the same information in JSON and TOON
- avoid sending complete registries when a filtered subset is sufficient
- avoid loading unrelated governance rules
- keep examples small
- progressively disclose additional context only when needed
- measure actual token usage when optimization matters

The consumer MUST preserve enough context to avoid incorrect routing or unsafe omission.

## Governance constraints

Context minimization MUST NOT remove required governance.

The following must remain available when applicable:

- authority rules
- approval rules
- escalation rules
- regulated/high-risk review requirements
- provenance requirements
- record integrity requirements

Human decision authority remains final.

The AI MUST NOT turn context selection into autonomous business decision-making.

## Validation

A generated TOON projection MUST be validated against its canonical JSON source.

Malformed, incomplete, or truncated TOON MUST NOT silently replace canonical data.

When a consumer cannot reliably parse TOON, it SHOULD fall back to compact JSON rather than inventing a different representation.

## Anti-patterns

Do not:

- load the whole repository for every question
- send all domains for a finance question
- send all mentors before identifying required skills
- select a mentor based on a global ranking
- duplicate canonical JSON and its complete TOON projection in the same prompt
- omit governance rules merely to save tokens
- allow context minimization to hide a relevant risk or escalation rule

## Example

For:

> I want to import medical equipment into Iran. What should I investigate before starting?

The initial package should focus on:

- entrepreneurship-founder
- import
- international-trade
- compliance
- finance-financial-modeling

and skills such as:

- business-model
- import-procedure
- customs-documentation
- regulatory-compliance
- landed-cost
- financial-modeling

Only after routing should the consumer load the detailed import/export, finance, legal/compliance, and startup team definitions.

## Success criteria

A context package is successful when it:

1. contains enough information to route and answer the current question correctly;
2. excludes unrelated framework information;
3. preserves mandatory governance;
4. preserves provenance;
5. can be reproduced from canonical framework data;
6. uses TOON when it provides a measured efficiency benefit;
7. does not make the AI the final business decision-maker.
