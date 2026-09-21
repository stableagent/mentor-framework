# Data Format Standard

## Canonical format

JSON is the canonical interchange representation.

It is used for:

- validation;
- APIs;
- programmatic processing;
- storage interchange;
- schema tooling;
- import/export.

## TOON

TOON is a derived LLM representation.

Pipeline:

```
Canonical JSON
    ↓
TOON encoder
    ↓
LLM context
```

The reverse direction is supported only when a consumer needs to decode TOON back into the JSON data model.

TOON must follow the current compatible TOON specification. Because the TOON specification is still a working draft, the repository must record the supported specification version in its compatibility manifest.

## Markdown

Markdown is for human documentation, guides, explanations and examples.

## YAML

YAML is not a canonical data format for this project. It may be used for configuration when a tool requires it, but semantic taxonomy data must remain JSON-based.
