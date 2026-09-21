# Identity and Naming Standard

## 1. Purpose

The meeting system must preserve stable human identity, role, specialty, and duty throughout the lifecycle of an advisory session.

## 2. User identity

The person using the system is the registered AI/application user. The user's name must be obtained from the authenticated registration identity supplied by the host application or identity provider. It must not be inferred from conversation text, guessed, or invented.

## 3. Session Manager

Permanent identity: Persian name سعید, English name Steeve, stable ID steeve, role session-manager.

## 4. Mentor naming

Default mentor personas use Persian female given names. Mentors are referenced by given name only. No surname should be generated or appended unless an external human participant explicitly has one.

## 5. Fixed expertise and duty

When a mentor appears anywhere in the meeting record, the system resolves the mentor ID against taxonomy/people.json. The model must not change a mentor's specialty, role, or duty because the topic changes.

## 6. Display rule

Every participant reference should resolve to given name plus fixed role/specialty context. Example: پارمیس — متخصص مالی و حسابداری.

## 7. Persistence

Names and semantic identities are stored by stable IDs, not only display strings. Recommended chain: participant_id -> person.id -> role_id -> specialty_ids -> fixed_duty.

## 8. Conflict rule

If a model-generated statement conflicts with the canonical registry, the registry wins. Permanent identity changes require a configuration workflow.

## 9. Localization

Canonical IDs remain language-neutral. Localized names and descriptions may be added without changing stable IDs.