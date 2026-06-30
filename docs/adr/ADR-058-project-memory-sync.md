# ADR-058: Project Memory Sync

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Project Memory Sync decision.

## Status

Accepted

## Context

VentureOS has accumulated substantial architecture context across phases, audits, ADRs, and session handoffs. A future ChatGPT/Yuri session must be able to resume without restarting, inventing missing architecture, or losing source-of-truth order.

## Decision

VentureOS adopts `docs/project/yuri-session-restart.md` as the project memory restart document for future Yuri sessions.

Project context, session handoff, decision history, focus, milestones, and risks must be updated during Phase 2 workstream completion.

## Alternatives considered

- Rely only on chat history.
- Rely only on `session-handoff.md`.
- Let future sessions infer architecture from scattered documents.

## Rationale

A dedicated restart document reduces context loss, preserves reading order, and helps future sessions continue from the accepted architecture.

## Risks

- Restart material may drift if not updated after major workstreams.
- The restart document may be mistaken for a replacement source of truth.
- Future sessions may skip required reading order.

## Consequences

- Future Yuri sessions have a concise resume path.
- Source-of-truth hierarchy remains explicit.
- No new strategic concepts should be added until Phase 2 is completed and reviewed.

## Enforcement

Future major architecture sessions should update project memory documents when project state changes materially.
