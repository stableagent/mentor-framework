# Provider Adapter Standard

A provider adapter connects the technology-independent Mentor Framework Context Engine to a model provider or other advisory consumer.

## Boundary

The adapter MAY retrieve the framework, pin a revision, translate transport formats, supply provider instructions, attach selected context, select a provider-supported model, collect responses and store session state.

The adapter MUST NOT redefine domains, skills or roles; change authority; change fixed identities; remove required escalation; activate an unapproved specialist; create a global mentor ranking; treat model output as a framework decision; or replace canonical JSON with an independently edited representation.

## Provider-neutral interface

    bootstrap(repository, revision?)
    select(request, authorization, session?)
    package(selection, representation?)
    advise(context_package, user_request, provider_options)
    record(session_event)

The concrete programming language and transport are intentionally unspecified.

## Error contract

Adapters should distinguish bootstrap-unavailable, framework-validation-failed, clarification-required, approval-required, escalation-required, provider-unavailable, context-too-large and invalid-model-output.

Errors must not silently downgrade governance requirements.

## Model output

Provider output is advisory content. It does not modify framework taxonomy or authority.

Responses should preserve distinctions between verified facts, framework rules, specialist analysis, assumptions, estimates, recommendations and human decisions.

## Portability

The same selection request and framework revision should produce semantically equivalent routing regardless of provider. Provider-specific prompts are implementation details and must not become alternate framework specifications.
