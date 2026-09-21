# Meeting Lifecycle Standard

A meeting is an event-driven state machine backed by one canonical Meeting Record.

## Lifecycle

planned -> active -> paused -> active -> closed -> approved -> amended

`amended` means an approved record was corrected through an explicit amendment. Original facts remain traceable.

## Participant lifecycle

proposed -> invited -> accepted
proposed -> declined
invited -> declined
accepted -> removed

A specialist must not become an active participant merely because a model proposed the specialist. User approval is required unless an explicit pre-authorization policy exists.

## Specialist admission

1. Detect a missing competency.
2. Create Specialist Proposal.
3. Explain role, specialty, reason and limitations.
4. Ask for explicit approval.
5. On approval, add participant.
6. Require a short introduction.
7. Record admission as a Meeting Event.
8. Preserve canonical identity, specialty and duty.

## Canonical record

Events are append-oriented. Current state is derived from the canonical record and event history. Rendered documents are projections, not independent sources of truth.
