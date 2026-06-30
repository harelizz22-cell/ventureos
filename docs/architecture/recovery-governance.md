# Recovery Governance

Parent: `docs/architecture/execution-reliability.md`

Source Of Truth: This file is the source of truth for Recovery Governance architecture.

## Purpose

Define who may initiate recovery, when recovery may run automatically, when recovery requires governance, and how recovery preserves safety, auditability, compliance, capital discipline, and Founder control.

## Who May Initiate Recovery

Recovery may be initiated by:

- Runtime Kernel after governed failure detection
- Recovery Manager
- Policy Engine outcome
- Founder
- Approved delegated reviewer
- Incident process
- Compliance reviewer where required
- Architecture Guardian where architecture safety is affected

Agents may request recovery only through governed execution paths. Agents may not self-approve recovery.

## Automatic Recovery

Automatic recovery may be allowed only for low-risk, idempotent, bounded, policy-approved cases.

Automatic recovery must not affect capital, regulated activity, customer-visible commitments, production assets, legal/compliance-sensitive records, or irreversible state unless explicitly governed.

## Governed Recovery

Governed recovery is required when recovery affects:

- Policy-sensitive action
- Approval-sensitive action
- Production asset
- Customer state
- Evidence, Decision, or Audit integrity
- Capital reservation or allocation
- Compliance-sensitive domain
- Security-sensitive domain
- External provider or tool side effect

## Founder Approval Cases

Founder approval is required when recovery may:

- Change ownership-sensitive assets
- Affect capital allocation
- Affect investment, acquisition, funding, or marketplace concerns
- Override a prior Founder Decision
- Create material business risk
- Create irreversible state
- Expand autonomy
- Affect regulated financial, legal, medical, security, or biotech boundaries

## Compliance Review Cases

Compliance review is required when recovery touches:

- Regulated financial activity
- Investor marketplace or funding activity
- Securities-sensitive communication
- Legal records
- Medical, biotech, security, or regulated domain workflows
- Cross-jurisdictional obligations
- Data retention or deletion obligations

## Capital-Sensitive Recovery

Capital-sensitive recovery includes recovery that affects budgets, reservations, invoices, purchases, investment recommendations, funding milestones, spending commitments, or money movement.

Capital-sensitive recovery must pass Policy Engine, Cost Governance, Capital Governance, and Founder or delegated approval where required.

Recovery must not move money or execute investments autonomously.

## Recovery Audit

Recovery audit records must include:

- Recovery initiator
- Failure category
- Recovery type
- Policy snapshot
- Approval status
- Evidence used
- Recovery plan
- Recovery execution status
- Recovery result
- Residual risk
- Related Events
- Related Decisions

## Recovery Replay

Recovery replay may use Event replay to rebuild state, diagnose incidents, coordinate compensation, or verify recovery.

Recovery replay must mark replayed Events, preserve original Event identity, and must not rewrite historical Evidence, Decisions, or Audit records.

## Recovery Safety

Recovery must fail closed when:

- Policy Engine is unavailable
- Required approval is missing
- Evidence is insufficient
- Idempotency cannot be proven
- Recovery impact is unknown
- Compliance review is required but missing
- Capital sensitivity is unresolved
- Recovery could rewrite history

## Rule

Recovery is governed system behavior. It must not bypass Policy, Evidence, approval, audit, compliance, capital governance, or Founder authority.

## Placeholder Status

This is architecture documentation only. It does not define recovery services, incident tools, workflow engines, schemas, APIs, integrations, or implementation.
