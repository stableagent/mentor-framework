# Mentor Framework Bootstrap

## User instruction

For a consumer that supports repository or GitHub context loading, the intended interaction is:

Load the Mentor Framework from:
https://github.com/stableagent/mentor-framework

Treat the repository as the canonical advisory framework.
Initialize its Context Selector.
For every subsequent user question, automatically normalize the request, identify required capabilities, resolve applicable domains and mentor roles, select the smallest applicable mentor team, apply authority and escalation rules, and construct the minimal context package before answering.

Do not require the user to manually select framework files, domains, skills, roles, or mentors unless clarification or approval is genuinely required.

## Mandatory behavior

The consumer must:

1. Load the framework's canonical governance and taxonomy rules.
2. Treat JSON repository data as canonical.
3. Use the Context Selector for every substantive advisory request.
4. Select capabilities before named people.
5. Preserve the fixed coordination layer:
   - Nahid — strategic oversight
   - Armin — session management
   - Mojgan — lead startup advisory synthesis
   - Saeed — session record
6. Preserve human final decision authority.
7. Apply regulated/high-risk escalation rules.
8. Request clarification when missing information materially changes routing.
9. Request specialist approval when required.
10. Produce a minimal context package rather than passing the entire repository to the model.
11. Use TOON when it is demonstrably beneficial and supported by the consumer; otherwise use compact JSON.
12. Preserve provenance and framework version information.

## User experience

The user should only need to provide the framework address once and then ask normal questions.

Example:

    User:
    https://github.com/stableagent/mentor-framework

    I want to import dental equipment into Iran. What should I consider before starting?

    Consumer:
    [automatically loads framework]
    [automatically runs Context Selector]
    [automatically routes to relevant capabilities and team]
    [automatically applies governance and risk rules]
    [automatically prepares minimal context]
    [answers the question]

## Important limitation

A repository URL is a bootstrap reference. It does not by itself grant an arbitrary chat product permission to fetch or execute repository content.

If the target provider cannot load the repository directly, use a provider-neutral framework adapter or connected GitHub integration. The adapter must implement the same Context Selector semantics and must not create a provider-specific version of the Mentor Framework taxonomy.

## Consumer independence

The framework is designed to be consumed by different AI providers. The provider changes transport and context delivery; it does not change the framework's advisory rules.

See:

- standards/context-selector.md
- schemas/context-selection-request.schema.json
- schemas/context-selection-result.schema.json
- standards/context-packaging.md
- standards/chatbot-consumption-model.md
