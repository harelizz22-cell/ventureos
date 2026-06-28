# ADR-009: Claude Red Team Review #001

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for accepted decisions from Claude Red Team Review #001.

## Status

Accepted

## Context

Claude Red Team Review #001 identified documentation architecture gaps after Architecture Audit #003. The review focused on capability-first consistency, portfolio-first consistency, organization layer correctness, event-driven architecture gaps, execution orchestrator ownership, governance bypass risks, agent-first regression, missing ADRs, documentation contradictions, and unclear source-of-truth hierarchy.

## Findings

- Architecture vocabulary needed official definitions.
- Execution governance needed a fail-closed Policy Engine rule.
- Authority hierarchy needed to distinguish founder authority from business structure.
- Capability Registry primacy and Agent Registry secondary status needed stronger enforcement.
- Primary architecture documentation contained a future work note.
- Runtime autonomy levels needed explicit behavior.
- Evidence, Decision, and Audit ledger integrity rules needed separation.
- Cost governance needed to be recorded as an architectural concern.

## Accepted Decisions

- Add official architecture definitions to the primary architecture documentation.
- Record that all execution paths must pass through the Policy Engine.
- Record that if the Policy Engine is unavailable, VentureOS fails closed.
- Clarify Founder as highest authority and Organization as the start of business structure.
- Strengthen capability-first registry enforcement.
- Move future work out of the primary architecture document into project-management tracking.
- Expand runtime autonomy levels from Level 0 through Level 5.
- Record Evidence Ledger, Decision Ledger, and Audit Ledger as separate concerns.
- Add Cost Governance.

## Rejected Recommendations

None. All approved Red Team findings in this batch were accepted for documentation updates.

## Architect Rationale

The accepted findings reduce ambiguity before implementation begins. They preserve founder authority, prevent governance bypass, protect the capability-first architecture, and strengthen auditability without adding production code or implementation detail.

## Enforcement

Future documentation and implementation planning must use these decisions unless superseded by Founder and Chief Architect approval.

