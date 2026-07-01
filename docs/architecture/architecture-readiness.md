# Architecture Readiness

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Architecture Readiness architecture.

## Purpose

Architecture Readiness defines measurable categories used to decide whether VentureOS architecture is ready for implementation planning, internal readiness review, and external Claude Red Team review.

Readiness does not authorize implementation. It informs review.

## Governance

Readiness Criteria:

- Source-of-truth hierarchy is clear.
- Policy before execution is documented.
- Founder authority is preserved.

Success Criteria:

- Governance bypass paths are identified and blocked architecturally.
- Approval, denial, fail-closed, and audit requirements are documented.

Blocking Conditions:

- Any execution path can self-approve.
- Founder authority is unclear.
- Governance records are optional.

## Security

Readiness Criteria:

- Tenant isolation, identity, access, treasury security, and secrets boundaries are documented.

Success Criteria:

- Cross-Organization, cross-Portfolio, and cross-Venture boundaries are explicit.
- Sensitive financial, AI, knowledge, and audit paths fail closed.

Blocking Conditions:

- Unauthorized data access path remains undefined.
- Security incident escalation is missing.

## Runtime

Readiness Criteria:

- Runtime Kernel, Execution API, scheduling, reliability, recovery, events, and resource coordination are documented.

Success Criteria:

- Execution lifecycle, retries, recovery, idempotency, timeouts, incidents, and audit linkage are defined.

Blocking Conditions:

- Runtime can execute without policy.
- Recovery can bypass governance.

## Knowledge

Readiness Criteria:

- Knowledge Domain, Enterprise Knowledge Graph, Organizational Memory, Learning Engine, Reasoning Engine, and AI output classification are separated.

Success Criteria:

- Reasoning remains recommendation-only.
- Learning and Evidence promotion are governed and auditable.

Blocking Conditions:

- AI or reasoning output becomes Evidence automatically.
- Knowledge ownership or classification is unclear.

## Treasury

Readiness Criteria:

- Treasury Domain, Capital Lifecycle, Capital Allocation Governance, Treasury Security, Milestone Funding, Portfolio Governance, Treasury Risk Engine, Capital Stress Simulator, and Founder Financial Dashboard are documented.

Success Criteria:

- No money can move without Policy Engine evaluation.
- No capital can be allocated twice.
- Every dollar has a lifecycle.

Blocking Conditions:

- Recommendation systems can release capital.
- Capital state is not auditable.

## Policy

Readiness Criteria:

- Policy Engine consistency, policy snapshots, evaluator disagreement, fail-closed behavior, and governance lag are documented.

Success Criteria:

- Every governed execution records policy version or snapshot.

Blocking Conditions:

- Policy version cannot be reconstructed.
- Policy disagreement allows permissive execution.

## Evidence

Readiness Criteria:

- Evidence freshness, quality, suitability, source, timestamp, confidence, and corroboration requirements are documented.

Success Criteria:

- Evidence must exist before Decision.
- Stale or unsuitable evidence is handled explicitly.

Blocking Conditions:

- Decisions can proceed without Evidence where Evidence is required.
- Evidence and Audit concerns are merged.

## AI

Readiness Criteria:

- AI Gateway, AI Output Classification, reasoning boundaries, autonomy governance, and AI diagnostics are documented.

Success Criteria:

- AI output lifecycle is Draft -> Recommendation -> Candidate Evidence -> Verified Evidence.
- AI does not self-approve autonomy expansion.

Blocking Conditions:

- AI output enters Evidence Ledger directly.
- AI can bypass policy or Founder authority.

## Portfolio

Readiness Criteria:

- Organization, Portfolio, Venture, diversification, enterprise value, capital allocation, cross-Venture intelligence, and portfolio governance are documented.

Success Criteria:

- Portfolio-first operation is preserved.
- Cross-Venture intelligence remains governed.

Blocking Conditions:

- Single-Venture assumptions control implementation.
- Raw Venture data leaks without policy.

## Operations

Readiness Criteria:

- Observability, health, incident management, operational dashboard, diagnostics, and readiness scorecard are documented.

Success Criteria:

- Health, incidents, operations, and readiness can be reviewed before implementation planning.

Blocking Conditions:

- Operational failure cannot be diagnosed.
- Incidents have no owner, severity, recovery verification, or audit linkage.

## Documentation

Readiness Criteria:

- Each concern has one source of truth and ADR coverage where required.

Success Criteria:

- Project Dashboard, Yuri Session Restart, Project Context, Session Handoff, Decision History, Phase 2 Blueprint, Architecture Scorecard, and Phase 2 Completion Checklist are updated.

Blocking Conditions:

- Source-of-truth conflicts remain unresolved.
- Phase 2 review cannot be restarted from documentation alone.

## Placeholder Status

This is architecture documentation only. It does not define scoring automation, implementation gates, CI checks, services, integrations, dependencies, or production code.
