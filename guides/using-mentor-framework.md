# Using Mentor Framework with AI Assistants

## Purpose

This guide explains how a human user or AI agent can use Mentor Framework with mainstream AI assistants.

Supported consumer patterns include:

- Gemini
- DeepSeek
- Perplexity
- Grok
- Claude
- Qwen
- Microsoft Copilot
- ChatGPT
- custom AI agents and API integrations

The exact interface, file limits, project features, and model capabilities can change over time. This guide therefore separates the framework method from provider-specific UI instructions.

## The universal method

Do not begin by uploading the whole repository.

Use this sequence:

1. Obtain the current Mentor Framework repository.
2. Start with the README and the relevant standard.
3. Identify the user's problem.
4. Normalize the problem.
5. Identify relevant domains.
6. Identify required skills.
7. Select the smallest applicable mentor team.
8. Load only the relevant governance and escalation rules.
9. Build a minimal context package.
10. Use TOON for repetitive structured data when supported and beneficial.
11. Ask the AI to analyze the problem using the supplied framework context.
12. Keep final business authority with the human user.

## Recommended files to provide

For a first setup, provide:

- README.md
- standards/chatbot-consumption-model.md
- standards/mentor-team-selection.md
- standards/mentor-routing-framework.md
- standards/authority-matrix.md
- standards/format-and-token-efficiency.md
- standards/context-packaging.md

Do not automatically provide every taxonomy file.

For a specific problem, add only the relevant:

- taxonomy domain
- specialty matrix
- mentor team
- role
- routing example
- schema
- specialist record

## Recommended first prompt

Use this as the initial instruction:

> You are a consumer of Mentor Framework, not its owner. Use the attached framework files as the authoritative framework context. Do not load or reproduce unrelated framework data. First normalize my request, identify the relevant domains and required skills, then select the smallest applicable mentor team. Respect the authority matrix, escalation rules, and approval requirements. Use capability-first routing rather than choosing people by preference or ranking. Use the minimum context required for this task. Keep final business decisions with me.

## Routing prompt

After the framework is available:

> Analyze my request as a Mentor Framework routing request.
>
> Return:
> 1. normalized problem
> 2. relevant domains
> 3. required skills
> 4. risk level
> 5. jurisdiction
> 6. applicable mentor team
> 7. lead role
> 8. proposed specialists
> 9. missing skills
> 10. approval requirements
> 11. escalation requirements
>
> Do not provide a final business decision.

## Advisory prompt

After routing:

> Use the selected Mentor Framework context to analyze the problem.
>
> Separate:
> - established facts
> - evidence
> - specialist analysis
> - assumptions
> - options
> - risks
> - unresolved questions
> - proposed next actions
>
> Do not convert an advisory recommendation into a final business decision.

## TOON workflow

When using a consumer that can reliably process TOON:

1. Keep canonical framework data in JSON.
2. Filter the relevant records.
3. Convert only the selected records to TOON.
4. Send the TOON projection as context.
5. Tell the AI what the fields mean.
6. Validate important outputs against canonical JSON.
7. Do not maintain a separate manually edited TOON database.

A simple pattern:

~~~text
Canonical JSON
    ↓
Filter
    ↓
Minimal dataset
    ↓
TOON
    ↓
AI context
~~~

## Platform-specific usage

### 1. Gemini

For Gemini Apps, the practical persistent setup is a Gem. Google documents adding files under a Gem's Knowledge section and adding detailed instructions.

Recommended setup:

- Create a dedicated Gem such as Mentor Framework Advisor.
- Put the universal instruction in the Gem instructions.
- Add the small core standards to Knowledge.
- Do not add every taxonomy file initially.
- For each problem, add only the relevant domain/team/context files.
- Ask Gemini to perform routing before advisory analysis.

Suggested Gem instruction:

> You are a Mentor Framework consumer. Follow capability-first routing, minimal context packaging, authority rules, escalation rules, and human decision authority. Do not rank mentors. Do not make the user's business decision. Use only the relevant attached framework context.

### 2. DeepSeek

Use the same universal workflow in the DeepSeek chat interface or through the DeepSeek API.

For a chat:

- provide the smallest relevant framework files;
- give the universal instruction;
- route first;
- provide additional context only after routing.

For API-based integrations, keep the canonical JSON repository outside the model prompt and generate a filtered context package for each request.

Do not assume that every DeepSeek product surface supports persistent project knowledge or arbitrary file formats in the same way. Provider capabilities change, so the API/chat interface should be checked before implementation.

### 3. Perplexity

Use a dedicated conversation or workspace/project capability when available.

Recommended pattern:

- give the core Mentor Framework instructions;
- attach only the relevant framework files;
- use Perplexity's web research for current external evidence when required;
- keep Mentor Framework itself as the governance/routing layer;
- distinguish framework rules from external research.

For current or regulated subjects, explicitly ask for current authoritative sources.

Example:

> First route this problem using Mentor Framework. Then research current external evidence. Keep framework rules, external evidence, specialist analysis, and your own assumptions separate.

### 4. Grok

Grok supports file uploads in its web and mobile applications, and xAI documents file-based workflows for documents, JSON, Markdown, code, and other data.

Recommended pattern:

- attach README plus the relevant standards;
- add only the domain/team files required for the current problem;
- explicitly tell Grok what each attachment represents;
- ask it to route before answering.

For API integrations, xAI's Files API can attach uploaded files to chat requests; xAI also documents automatic attachment search for file-based requests.

Example:

> README.md is the framework overview. standards/context-packaging.md defines context selection. taxonomy/mentor-teams.json contains team templates. Use these as framework rules. Do not treat unrelated files as relevant context.

### 5. Claude

Use a Claude Project when persistent project knowledge is available.

Recommended project structure:

- project instructions: universal Mentor Framework instruction;
- project knowledge: core standards;
- per-conversation attachments: only the relevant taxonomy/team/context package.

The same progressive disclosure principle applies: persistent knowledge should contain stable framework rules, while request-specific data should be added only when needed.

Do not rely on a provider-specific project feature as part of the Mentor Framework itself. The framework remains portable.

### 6. Qwen

Use Qwen's available file/project/chat capabilities when present, but keep the same provider-neutral architecture.

Recommended:

- store the stable Mentor Framework instruction in the persistent instruction/project area if available;
- attach the minimal relevant files;
- use JSON as the canonical interchange format;
- use TOON only if the selected Qwen interface or integration reliably supports it;
- otherwise use compact JSON.

For API integrations, implement the context selector outside the model and send only the generated package.

### 7. Microsoft Copilot

Microsoft documents file upload in Copilot, including JSON and Markdown among supported text/markup formats, with limits that can vary by Copilot product.

For the consumer Copilot experience:

1. Use the + control to add files.
2. Add the core framework instructions.
3. Add the relevant domain/team files.
4. Give the routing prompt.
5. Continue with advisory analysis after routing.

For Microsoft 365/Copilot environments, use the applicable organization file and knowledge features where available.

Do not upload the entire repository merely because the product accepts multiple files.

## ChatGPT

ChatGPT follows the same framework method:

- keep the core standards available;
- attach only the relevant framework files;
- use routing first;
- build the minimal context package;
- use TOON when beneficial;
- preserve human decision authority.

If a future ChatGPT integration directly consumes the repository, the integration should implement the same context-selection rules rather than sending the repository wholesale.

## Custom AI Agent

For a custom agent, implement:

~~~text
Repository
    ↓
Indexer / Registry
    ↓
Request Classifier
    ↓
Context Selector
    ↓
Minimal Context Package
    ↓
JSON / TOON Projection
    ↓
LLM
~~~

Conceptual internal operations:

~~~text
classify_request()
select_domains()
select_skills()
select_roles()
select_teams()
select_governance()
build_context_package()
project_to_toon_if_beneficial()
validate_context()
run_advisory()
record_session()
~~~

These are conceptual operations, not requirements for a particular programming language.

## Example end-to-end interaction

User:

> I want to start importing dental equipment into Iran. I have suppliers abroad but I do not know the regulatory, customs, financial, and logistics requirements.

The consumer should first return a routing analysis:

~~~text
Problem:
startup/import planning

Domains:
import
international-trade
compliance
finance-financial-modeling
logistics
entrepreneurship-founder

Required skills:
business-model
import-procedure
customs-documentation
regulatory-compliance
landed-cost
trade-finance
logistics-planning

Potential team:
import-export
legal-compliance
finance-accounting
operations-supply-chain
startup-core

Risk:
high

Approval:
required for specialist activation where not pre-authorized

External review:
required where regulated or jurisdiction-specific professional review is necessary
~~~

Only then should the consumer load the detailed team and specialist context.

## What not to do

### Bad

> Here is the entire Mentor Framework repository. Answer every future question using all of it.

This wastes context and makes relevance harder to control.

### Better

> Here is the framework overview and context-selection standard. First classify my problem and tell me which framework records are actually required. Do not load unrelated records.

### Best for a custom integration

Keep the repository outside the model and generate a request-specific context package.

## Provider portability

Mentor Framework does not depend on:

- a specific LLM
- a specific AI vendor
- a specific project feature
- a specific tokenizer
- a specific chat UI
- a specific API

Provider-specific instructions are an integration layer.

The framework's canonical rules remain provider-independent.

## Maintainer disclosure

The framework may expose the maintainer's public profile when explicitly requested.

The consumer SHOULD NOT insert maintainer information into ordinary advisory answers unless requested.

## Final checklist

Before sending a request to an AI consumer:

- [ ] Did I classify the problem?
- [ ] Did I identify the relevant domains?
- [ ] Did I identify required skills?
- [ ] Did I select capabilities before people?
- [ ] Did I select the smallest applicable team?
- [ ] Did I preserve required governance?
- [ ] Did I preserve escalation requirements?
- [ ] Did I avoid unrelated context?
- [ ] Did I use TOON only where it is beneficial and supported?
- [ ] Did I preserve canonical JSON as the source of truth?
- [ ] Did I keep final decision authority with the human?
