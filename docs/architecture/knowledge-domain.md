# Knowledge Domain

Parent: `docs/architecture/domain-model.md`

Source Of Truth: This file is the source of truth for Knowledge Domain architecture.

## Purpose

The Knowledge Domain is the central knowledge system for VentureOS.

It owns knowledge assets and retrieval capabilities. It does not absorb Enterprise Knowledge Graph, Organizational Memory, Learning Engine, or Reasoning Engine responsibilities.

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

## Related Architecture Components

- Enterprise Knowledge Graph is the relationship model across approved knowledge and architecture entities.
- Organizational Memory is the durable history layer.
- Reasoning Engine consumes approved knowledge and memory to produce reasoning outputs.
- Learning Engine converts outcomes into reusable learning.

These are separate concerns. Knowledge Domain remains the owning Domain for knowledge assets and retrieval capabilities, but each related component has its own source-of-truth document.

## Rule

Knowledge must preserve source, context, auditability, and relationship to evidence or decisions where meaningful.

When Knowledge is referenced as Evidence for a Decision, the referenced Knowledge version must be immutable or snapshot-pinned.

Evidence must never depend on mutable current-state content.

Reasoning outputs may not become Evidence automatically. They may become Candidate Evidence only through AI Output Classification and Evidence Promotion governance.

Knowledge referenced as Evidence must satisfy Evidence Freshness and Quality Model requirements, including source quality, timestamp, freshness, suitability, and corroboration where meaningful.

## Placeholder Status

This is an architecture placeholder. It does not define storage, schema, embeddings, or implementation.
