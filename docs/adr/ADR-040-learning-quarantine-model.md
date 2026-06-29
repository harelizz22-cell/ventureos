# ADR-040: Learning Quarantine Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Learning Quarantine Model decision.

## Status

Accepted

## Context

Learning records can influence future recommendations. If learning is disputed, wrong, stale, or withdrawn, VentureOS needs a governed way to stop that learning from silently affecting decisions while preserving audit history.

## Decision

VentureOS adopts Learning Quarantine Model as a required architecture workstream.

The model must define disputed learning records, quarantined learning records, withdrawn learning records, impact on future recommendations, audit preservation, and rollback of learning influence.

## Consequences

- Learning influence can be reduced or removed without rewriting history.
- Disputed learning remains auditable.
- Future recommendations must respect quarantine and withdrawal state.

## Enforcement

Quarantined or withdrawn learning must not silently influence future recommendations. Audit preservation remains mandatory.
