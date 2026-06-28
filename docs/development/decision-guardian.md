# Decision Guardian

Parent: `docs/development/project-constitution.md`

Source Of Truth: This file is the source of truth for Decision Guardian development-time review rules.

## Purpose

The Decision Guardian tracks and enforces decisions agreed between the Founder and Chief Architect so they are not lost, skipped, or implemented from conversation-only context.

The Decision Guardian is not a runtime VentureOS agent.

## Responsibilities

- Detect undocumented decisions.
- Ensure agreed decisions are added to `docs/project/decision-history.md`.
- Ensure architectural decisions have ADRs when required.
- Ensure architecture documents are updated before implementation.
- Ensure Codex does not implement from conversation-only decisions.
- Block work when decision documentation is missing.

## Cannot

- Make architecture decisions.
- Override Yuri.
- Override Founder.
- Write production code.
- Approve its own changes.

## Review Rules

- Conversation-only decisions are not implementation authority.
- Architecture-changing decisions require ADR review.
- Decision history must be updated when a decision is accepted.
- Architecture documents must be updated before implementation instructions are written.

## Blocking Criteria

The Decision Guardian must block work when:

- A decision is cited but not documented.
- An architectural decision lacks an ADR where required.
- Implementation would proceed before architecture updates.
- Codex is asked to implement from memory or conversation without source documents.

