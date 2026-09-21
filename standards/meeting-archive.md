# Meeting Archive and Recall Standard

## Purpose

An advisory meeting should be reusable as structured institutional memory without losing provenance or historical integrity.

## Archive lifecycle

`active -> closed -> reviewed -> approved -> archive-proposed -> user-confirmed -> archived -> amended`

A meeting is not archived merely because a final document was generated.

## Archive package

The archive preserves:

- canonical Meeting Record;
- final approved minutes;
- executive summary;
- decision log;
- action register;
- risk register;
- assumption register;
- open-question register;
- disagreement log;
- evidence/source register;
- specialist contribution summary;
- follow-up agenda;
- approval history;
- amendment history;
- stable meeting ID;
- creation and approval timestamps.

## Archive recommendation

After final minutes are prepared, Saeed presents a concise archival recommendation stating:

- meeting ID;
- title;
- date;
- status;
- what will be archived;
- how it can be recalled later.

The user must explicitly confirm archival.

## Recall

Archived meetings are retrieved by stable identifiers and metadata such as meeting ID, topic, project, startup, agenda, decision, date, participant or specialist.

Recall is read-only with respect to the historical record.

A recalled meeting may provide context for a new meeting, but historical decisions do not automatically become new decisions.

## New meeting from prior context

When Nahid starts a new meeting using an archived record:

1. create a new Meeting ID;
2. preserve the old Meeting ID as a historical reference;
3. call Saeed into the new session;
4. import only explicitly relevant historical context;
5. identify prior unresolved actions/questions;
6. distinguish historical decisions from new proposals;
7. record every new decision in the new Meeting Record.

## Archival integrity

Archived records are immutable except through the explicit amendment workflow.

No model may silently overwrite, merge or delete an archived meeting.

## Long-term retrieval

Stable IDs and canonical JSON remain authoritative. Rendered Markdown, TOON, HTML, PDF or DOCX files are derived projections.
