# Mentor Skills Architecture Standard

## 1. Purpose

This document defines the structural contract for the Mentor Skills knowledge system.

## 2. Entity hierarchy

```
Domain
  └── Role
        └── Skill
              ├── Competency
              ├── Framework
              ├── Methodology
              ├── Metric
              ├── Tool
              └── Escalation Rule
```

These entities must not be conflated.

### Domain

A broad capability area such as Product, Finance, Operations or Technology.

### Role

A mentor responsibility such as Product Mentor, Finance Mentor or Lead Startup Advisor.

### Skill

A reusable capability such as Product Strategy, Financial Modeling or Customer Discovery.

### Competency

An observable level or capability statement describing what proficient performance looks like.

### Framework

A named structured way of analyzing or solving a problem.

### Methodology

A repeatable process for performing work.

### Metric

A measurable indicator used for diagnosis, monitoring or decision support.

### Tool

A software or operational instrument used to perform a task.

### Escalation Rule

A condition under which the system must defer to a qualified specialist, current authoritative source or additional evidence.

## 3. Advisory architecture

A complete advisory system is composed of:

```
User Context
    ↓
Problem / Intent
    ↓
Relevant Skills
    ↓
Candidate Mentor Roles
    ↓
Virtual Mentor Team
    ↓
Specialist Analysis
    ↓
Lead Advisor Synthesis
    ↓
Decision Support
    ↓
Action Plan
    ↓
Metrics / Review
```

The Lead Advisor coordinates and synthesizes. It does not need to be an expert in every domain.

## 4. Context dimensions

Mentor routing may consider:

- user role;
- startup stage;
- startup type;
- business model;
- geography/jurisdiction;
- current problem;
- required skills;
- risk level;
- evidence quality;
- urgency.

## 5. Separation of knowledge and delivery

Core knowledge must not contain provider-specific prompt syntax.

Adapters may transform canonical data into:

- system prompts;
- user context;
- RAG documents;
- TOON context;
- tool instructions;
- provider-specific skill formats.

## 6. Source of truth

Canonical structured data is JSON.

TOON files are generated projections. They must never be edited manually as an independent source of truth.

Markdown may describe the same concepts for human readers but does not override canonical structured data.
