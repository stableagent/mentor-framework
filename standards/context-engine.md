# Context Engine Standard

The Context Engine is the normative execution model for the Context Selector. It turns the repository's canonical taxonomy and governance data into a request-specific context package.

It is implementation-neutral: a Python service, TypeScript service, AI agent, RAG pipeline, or another implementation may realize it, provided it conforms to this contract.

## Execution contract

Input: canonical framework snapshot, context-selection request, selector rules, authorization state.

Output: context-selection result, minimal context package, optional TOON projection.

The engine MUST NOT modify canonical taxonomy data during request processing.

## Pipeline

request → normalize → classify domains → extract required skills → resolve roles → select team → resolve specialists → apply authority → apply escalation → minimize context → select representation → validate → emit result.

## Deterministic resolution rules

1. Exact capability coverage precedes broad semantic similarity.
2. Complete coverage precedes incomplete coverage.
3. Fewer unnecessary specialists precedes larger teams.
4. Predefined team templates precede ad-hoc composition.
5. Approved or pre-authorized specialists precede approval-required specialists only when capability coverage is otherwise equivalent.
6. Regulated/high-risk escalation cannot be removed to reduce team size.
7. No person receives a global quality score or ranking.

If equivalent candidates remain, preserve all materially equivalent options or return approval-required rather than inventing a preference.

## Fixed coordination layer

The engine automatically preserves: nahid — strategic-oversight; saeed — session-manager; mojgan — lead-startup-advisor. Session recording is a system function with stable function ID `session-recorder`, not a second fixed person.

These are coordination/governance identities, not a global ranking.

## Specialist activation

A specialist may be emitted as active only when explicitly approved, pre-authorized by an applicable rule, or fixed by the framework. Otherwise emit the role as approval-required.

## Clarification

Return clarification-required when missing information can materially change jurisdiction, risk classification, required capability, team composition, authority, escalation, or specialist activation. Ask only for the smallest missing fact.

## High-risk and regulated requests

The engine MUST preserve the relevant external-review requirement. It must not convert advisory routing into professional authorization.

## Context minimization

Every emitted field must have a reason to exist in the current context. Omit unrelated domains, skills, mentor records, examples, duplicate descriptions and provider-specific material not required by the target consumer.

## Provenance

Every result must identify framework version and taxonomy version. Implementations SHOULD also record the exact framework commit used.

## Provider neutrality

The engine determines semantics. Provider adapters determine transport and formatting only. No adapter may override authority, fixed identities, routing semantics, escalation or specialist approval policy.

## Conformance

An implementation conforms when it can reproduce the same semantic routing result from the same versioned input and authorization state, subject only to explicitly versioned external classification dependencies.
