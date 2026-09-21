# Meeting & Session Architecture Standard

A Mentor Skills advisory session is a managed professional meeting, not merely a chat transcript.

## Core roles

### Session Manager

The Session Manager owns the meeting lifecycle:

- opens and closes the session;
- maintains agenda and objectives;
- tracks time and meeting state;
- detects when another specialist may be useful;
- proposes specialist invitations;
- asks for explicit user approval before adding a new specialist;
- records accepted and declined invitations;
- keeps the meeting focused.

The Session Manager does not silently add participants.

### Lead Advisor

The Lead Advisor coordinates specialist reasoning and synthesizes recommendations. It is distinct from the Session Manager.

### Specialist Mentor

A Specialist Mentor contributes expertise within one or more declared skills.

When joining a session, a specialist should briefly state:

- role;
- relevant expertise;
- why the expertise is relevant to the current agenda;
- important limitations or assumptions.

The introduction should be concise and should not derail the meeting.

### Session Secretary

The Session Secretary is responsible for structured meeting records.

It captures decisions, actions, evidence, assumptions, questions, disagreements, risks, commitments and follow-ups. It does not invent facts or silently convert discussion into decisions.

## Participant lifecycle

```
Session
  ↓
Session Manager identifies a knowledge gap
  ↓
Specialist invitation proposal
  ↓
User approval
  ↓
Specialist joins
  ↓
Brief introduction
  ↓
Specialist contribution
  ↓
User may retain or remove specialist
  ↓
Session continues
  ↓
Secretary continuously records structured notes
  ↓
Session close
  ↓
Validated meeting document
```

## User control

Specialist addition requires explicit user confirmation unless the user has configured an explicit pre-authorization policy.

The system must distinguish:

- proposed participant;
- invited participant;
- accepted participant;
- declined participant;
- removed participant.

## Secretary invocation

The user may address the Session Secretary at any point.

Examples:

- "منشی، دستور جلسه را ثبت کن."
- "منشی، تا اینجا تصمیم‌های قطعی را جمع‌بندی کن."
- "منشی، این مورد را به عنوان Action Item ثبت کن."
- "منشی، اختلاف نظرها را جداگانه ثبت کن."
- "منشی، صورت‌جلسه موقت بساز."

The Secretary may return to note-taking after completing the requested secretary task.

## Meeting outputs

A completed session may produce:

- executive summary;
- detailed minutes;
- decision log;
- action-item register;
- risk register;
- assumption register;
- open-question register;
- disagreement / dissent log;
- evidence and source register;
- specialist contribution summary;
- follow-up agenda;
- final advisory report.

These are views over the same canonical meeting record, not unrelated documents.
