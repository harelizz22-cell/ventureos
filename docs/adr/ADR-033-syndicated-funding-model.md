# ADR-033: Syndicated Funding Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Syndicated Funding Model decision.

## Status

Accepted

## Context

Future funding may involve multiple investors funding a Venture round together. VentureOS needs architecture for modeling syndicated funding without creating regulated workflows or investor fund custody.

## Decision

VentureOS adopts Syndicated Funding Model as a future first-class architecture concept.

The model is Opportunity -> Investment Readiness Review -> Investment Dossier -> Funding Round -> Investor Commitments -> Capital Target Reached -> Milestone-Based Execution -> Evidence-Based Capital Release -> Outcome Tracking.

## Alternatives Considered

- Model only single-investor funding.
- Treat commitments as unstructured notes.
- Implement syndicate behavior before compliance boundaries.

## Rationale

Syndicated funding affects capital targets, execution gating, investor communication, milestone release, governance, and outcome tracking. It needs architecture before implementation.

## Risks

- Investor commitments may be mistaken for legally binding transactions.
- Syndicated funding may imply securities coordination without approval.
- Capital target completion may trigger execution before governance review.

## Compliance Notes

Syndicated Funding Model does not authorize investor fund custody, securities transactions, public fundraising, or autonomous money movement.

Legal/compliance structure must define investor commitments and capital handling before regulated activity.

## Consequences

- Funding rounds may be modeled as capital target processes.
- Execution may depend on capital target completion when policy requires.
- Milestone-Based Capital Release becomes a required connected concern.

## Enforcement

Syndicated funding remains future architecture only until legal/compliance approval, Founder governance, and phase authorization exist.
