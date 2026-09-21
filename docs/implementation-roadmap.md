# Implementation Roadmap

Mentor Framework is now specification-first. The repository itself remains technology-independent.

## Phase 1 — Foundation

Completed:

- taxonomy, domain, advisory-role and skill registries
- mentor roles and people registry
- fixed coordination hierarchy
- authority matrix
- mentor team templates
- specialty matrix
- routing request/result contracts
- context package contract
- chatbot consumption model
- token-efficiency policy
- Context Selector standard
- Context Engine standard
- automatic one-address bootstrap contract
- automatic-consumption contract
- reference routing examples
- conformance requirements

## Phase 2 — Reference implementation

The next implementation layer may be built as a provider-neutral Context Engine. It should:

1. load a version-pinned framework snapshot;
2. validate canonical JSON and schemas;
3. normalize a natural-language request;
4. map domains to skills;
5. resolve roles and team templates;
6. apply specialist authorization;
7. apply governance and escalation;
8. build the minimal context package;
9. project to JSON or TOON;
10. validate the output;
11. expose a provider-neutral interface to model adapters.

## Phase 3 — Provider adapters

Adapters may then connect the same engine to ChatGPT, Gemini, Claude, DeepSeek, Grok, Qwen, Perplexity, Copilot and custom agents. Provider adapters must not fork the framework taxonomy or governance.

## Phase 4 — Session and record layer

Add durable session state, decision records, action tracking, risk registers, evidence provenance and immutable amendments.

## Phase 5 — Production hardening

Add authentication, authorization, audit logs, version pinning, observability, rate limits, caching, failure recovery, security review and automated conformance tests.

## Completion criterion

The end user provides the framework address once, asks ordinary questions, and does not manually select files, domains, skills, mentors or context formats. Clarification or approval appears only when genuinely required by the framework rules.
