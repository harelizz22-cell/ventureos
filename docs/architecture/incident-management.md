# Incident Management

Parent: `docs/architecture/observability-architecture.md`

Source Of Truth: This file is the source of truth for Incident Management architecture.

## Purpose

Incident Management defines how VentureOS detects, classifies, owns, escalates, recovers, verifies, audits, and learns from operational incidents.

## Incident Lifecycle

Required lifecycle:

1. Detected.
2. Classified.
3. Owned.
4. Triaged.
5. Contained.
6. Recovered.
7. Verified.
8. Post-mortem completed.
9. Closed.

Historical incident records must not be rewritten. Corrections must be appended.

## Severity

Severity describes impact.

Severity levels:

- SEV-1: Critical impact to governance, capital, security, tenant isolation, audit integrity, or broad runtime availability.
- SEV-2: Significant operational degradation, repeated execution failure, policy degradation, treasury alert, or affected portfolio operations.
- SEV-3: Limited Venture, Workflow, Capability, Agent, or dependency degradation.
- SEV-4: Low-impact warning, minor diagnostic issue, or informational condition.

## Priority

Priority describes response urgency.

Priority must consider severity, customer or Founder impact, capital sensitivity, compliance risk, security risk, recovery complexity, and Enterprise Value impact.

## Escalation

Escalation must route incidents to the required owner and approval path.

Escalation cases include:

- Policy Engine unavailable.
- Treasury lifecycle inconsistency.
- Capital-sensitive recovery.
- Cross-Organization or cross-Venture data exposure.
- Audit integrity concern.
- AI output governance violation.
- Repeated execution failure.
- Compliance-sensitive issue.

Founder-visible escalation is required for critical governance, capital, security, tenant isolation, or Enterprise Value risk.

## Ownership

Each incident must have one accountable owner.

Ownership record must include:

- Owner.
- Scope.
- Severity.
- Priority.
- Current state.
- Required approvals.
- Recovery owner where different.
- Audit references.

## Post-Mortem

Post-mortem is required for material incidents.

Post-mortem must include:

- What happened.
- Impact.
- Root cause.
- Timeline.
- Detection path.
- Recovery path.
- What worked.
- What failed.
- Follow-up actions.
- Evidence, Decision, Audit, and incident links.

Post-mortems must preserve the distinction between facts, assumptions, analysis, and recommendations.

## Recovery Verification

Recovery verification confirms that incident recovery succeeded and no unsafe state remains.

Verification must check:

- Policy availability.
- Runtime state.
- Execution state.
- Treasury state when affected.
- Evidence, Decision, and Audit linkage.
- Tenant isolation when affected.
- Follow-up incident or risk creation where needed.

## Audit Linkage

Incidents must link to:

- Triggering signals.
- Related Events.
- Related Executions.
- Policy outcomes.
- Evidence records.
- Decision records.
- Audit records.
- Recovery records.
- Post-mortem records.

## Placeholder Status

This is architecture documentation only. It does not define incident tooling, paging systems, ticketing integrations, schemas, services, dependencies, or implementation.
