# Data and Output Format Standard

## Canonical source

JSON is the canonical machine-readable source of truth.

## Derived formats

- TOON: compact LLM context representation.
- Markdown: human-readable documentation.
- YAML: configuration/interchange when required.
- HTML: browser presentation.
- PDF: archival/presentation output.
- DOCX: editable professional document.

No derived format is independently maintained.

## Conversion rule

JSON -> TOON/Markdown/YAML/HTML/PDF/DOCX

A conversion must preserve IDs, roles, names, specialties, duties, decisions, actions, risks, evidence and provenance.

## TOON policy

TOON is an optimization layer for model context, not a database format. The repository follows `standards/toon-compatibility.json`.

If a consumer cannot reliably parse TOON, send canonical JSON.

## Localization

Canonical IDs remain language-neutral. Presentation language is selected separately. Persian is supported without changing IDs.

## Professional documents

Every meeting output declares: draft, reviewed, approved, or amended.
An approved document is never silently overwritten.
