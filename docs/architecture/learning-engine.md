# Learning Engine

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Learning Engine architecture.

## Purpose

The Learning Engine converts outcomes into reusable knowledge.

It helps VentureOS improve future recommendations, hypotheses, thesis refinement, Opportunity Scores, capital allocation, and Enterprise Value analysis without weakening evidence, governance, or Founder control.

Learning Engine answers: "What did we learn from outcomes?"

It does not replace Organizational Memory, Enterprise Knowledge Graph, Reasoning Engine, or Knowledge Domain.

## Learns From

The Learning Engine must learn from:

- Successful ventures
- Failed ventures
- Killed opportunities
- Bad investments
- Strong investments
- Founder overrides
- Budget decisions
- Pricing experiments
- Acquisition outcomes

## Evidence-Backed Learning

Learning updates must link to Evidence, Decisions, Audit, and outcome records where meaningful.

Learning may recommend updates to Knowledge, Thesis, Opportunity Score assumptions, capital allocation assumptions, or strategic constraints, but it does not silently rewrite historical records.

Financial Feedback Loop is defined in `docs/architecture/financial-feedback-loop.md`.

Capital allocation outcomes must become evidence-backed learning through expected ROI, actual ROI, variance analysis, attribution, and lessons learned.

## Rule

Learning updates must be evidence-backed and auditable.

Learning recommendations do not override Founder approval, governance, evidence requirements, or source-of-truth documentation.

Learning never automatically changes policy.

No completed Venture may exit the lifecycle without producing organizational learning.

## Separation Of Concerns

- Organizational Memory answers: "What happened and what do we remember?"
- Enterprise Knowledge Graph answers: "How are facts, Evidence, Decisions, Ventures, Markets, and outcomes connected?"
- Reasoning Engine answers: "What can we infer from what we know?"
- Knowledge Domain owns knowledge assets and retrieval capabilities.

These are separate concerns. Do not merge them.

## Placeholder Status

This is an architecture placeholder. It does not define models, algorithms, embeddings, schemas, automation, UI, or implementation.
