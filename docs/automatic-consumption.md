# Automatic Consumption

Mentor Framework is designed so an end user can provide the repository address once and then ask ordinary questions.

## Contract

The consumer must treat the address as a bootstrap reference:

https://github.com/stableagent/mentor-framework

After bootstrap, every substantive request follows the Context Engine.

## User-visible behavior

The user should not be asked which file contains the answer, which mentor to choose, which domain to select, or whether JSON or TOON should be used.

The consumer asks a clarification question only when missing information materially changes routing or when authorization is genuinely required.

## Internal behavior

bootstrap → load canonical snapshot → validate snapshot → initialize selector → receive user request → context-selection-request → Context Engine → context-selection-result → context-package → provider projection → advisory model → response.

## Provider adapter boundary

A provider adapter connects to the target model/provider, supplies instructions where supported, attaches selected context, converts representation if required, and collects the model response. It is NOT allowed to alter Mentor Framework semantics.

## Session continuity

The consumer should retain framework commit/version, normalized request, selection result, approved specialists, decisions, action items and provenance. Follow-up questions should reuse relevant session context instead of rebuilding unrelated context.

## Failure behavior

If framework loading fails, do not pretend it was loaded and do not silently substitute an unrelated mentor taxonomy.

If routing fails, return the smallest useful clarification; do not fabricate a mentor and do not silently omit governance.

If a specialist requires approval, keep the role visible and mark activation approval-required.

If external review is required, preserve the escalation in the result and response.

## Security and trust

Consumers should pin or verify framework versions where possible. They should not execute arbitrary repository code merely because the repository contains it. Only declared data contracts, standards and trusted implementation components should be executed.

## Minimal-context objective

Optimize for maximum relevant capability + complete governance + minimum unnecessary context, rather than maximum repository content.
