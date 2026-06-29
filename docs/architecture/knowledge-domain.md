# Knowledge Domain

Parent: `docs/architecture/domain-model.md`

Source Of Truth: This file is the source of truth for Knowledge Domain architecture.

## Purpose

The Knowledge Domain is the central knowledge system for VentureOS.

## Owns

- Research
- Documents
- Evidence
- Founder Notes
- Lessons Learned
- Architecture Documents
- ADRs
- Business Memory
- Conversation Summaries
- Future Semantic Memory

## Rule

Knowledge must preserve source, context, auditability, and relationship to evidence or decisions where meaningful.

When Knowledge is referenced as Evidence for a Decision, the referenced Knowledge version must be immutable or snapshot-pinned.

Evidence must never depend on mutable current-state content.

## Placeholder Status

This is an architecture placeholder. It does not define storage, schema, embeddings, or implementation.
