# Treasury Domain

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Treasury Domain architecture.

## Purpose

Treasury is the only domain responsible for protecting, reserving, releasing, tracking, and reconciling capital.

Treasury never evaluates ideas. Treasury never creates strategy. Treasury never bypasses Policy Engine.

## Domain Rules

- No money can move without Policy Engine evaluation.
- Founder retains final governance for capital-sensitive actions.
- Treasury remains independent from AI reasoning, Strategic Review, Opportunity Score, Investment Engine, and Capital Allocation Engine.
- Treasury records capital state changes but does not decide business attractiveness.
- Every financial action is auditable.
- No autonomous money movement is allowed.
- Tokens are financial resources.
- Treasury must receive token usage records from AI Gateway and Cost Governance where token usage affects financial reporting, budget state, or capital discipline.
- Treasury must receive AI model cost information where AI Model Registry and AI Gateway model selection affect financial reporting, budget state, or capital discipline.
- Treasury must be notified for capital-sensitive recovery before recovery starts and after recovery completes, fails, compensates, rolls back, or is abandoned.
- Treasury must receive token reservation, release, expiry, and over-consumption records where AI token usage affects budget state or financial reporting.

## Treasury Controller

Purpose: Coordinate Treasury activities and enforce capital lifecycle discipline.

Responsibilities:

- Coordinate capital reservations, approvals, releases, recovery, and closure.
- Require Policy Engine evaluation before capital state transitions.
- Preserve segregation between recommendation systems and capital control.

Non-responsibilities:

- Idea evaluation.
- Strategy creation.
- Investment recommendation.
- Autonomous execution of payments or securities transactions.

Inputs:

- Approved capital requests.
- Policy Engine outcomes.
- Founder or governed approval records.
- Capital lifecycle state.
- Token usage records where AI costs affect budget or financial reporting.
- Model cost information where AI model choice affects budget or financial reporting.
- Capital-sensitive recovery requests, Evidence, approval path, compensation or rollback plan, and outcome.
- Token reservation records, reservation releases, reservation expiry, and token over-consumption events.

Outputs:

- Treasury action records.
- Capital lifecycle events.
- Audit records.
- Escalation requests.
- Token cost visibility records where applicable.
- Model cost visibility records where applicable.
- Capital-sensitive recovery visibility records.
- Token reservation visibility records.

Security requirements:

- Access must be scoped by Organization, Portfolio, Venture, actor, role, and policy.
- Capital-sensitive actions require strong actor identity and tamper-evident audit.

Governance requirements:

- Policy Engine must approve or require approval before action.
- Founder approval is required for high-value, exceptional, or irreversible financial actions.

Failure handling:

- Fail closed when policy, approval, ledger state, or lifecycle state cannot be verified.
- Create an incident for unresolved or inconsistent financial state.

Audit requirements:

- Record actor, request, policy version, approvals, evidence links, prior state, new state, timestamp, and correlation ID.

## Capital Custodian

Purpose: Protect records of available, reserved, committed, approved, released, spent, recovered, cancelled, and closed capital.

Responsibilities:

- Maintain authoritative capital balances and lifecycle state.
- Prevent double allocation.
- Reconcile financial state against approved records.

Non-responsibilities:

- Recommending where capital should be allocated.
- Holding funds in a regulated custodial sense unless future legal/compliance structure authorizes it.

Inputs:

- Capital state transition requests.
- Approved reservation and release records.
- Reconciliation evidence.

Outputs:

- Capital balance state.
- Reconciliation exceptions.
- Allocation conflict alerts.

Security requirements:

- Immutable ledger linkage is required for state changes.
- High-value balance changes require elevated approval.

Governance requirements:

- Every balance change must be policy-evaluated and auditable.
- No capital can be allocated twice.

Failure handling:

- Freeze affected capital when balance integrity is uncertain.
- Escalate conflicts to Treasury Controller and Policy Engine.

Audit requirements:

- Preserve complete balance history without overwriting prior records.

## Budget Controller

Purpose: Govern budget limits, holds, spend envelopes, and unused capital return.

Responsibilities:

- Track budget approval, reservation, release, spend, holdback, cancellation, and return.
- Enforce budget caps and available-capital constraints.
- Surface budget variance and overrun risk.

Non-responsibilities:

- Selecting ventures or opportunities.
- Optimizing expected return.

Inputs:

- Approved budgets.
- Milestone funding plans.
- Spend reports.
- Policy limits.

Outputs:

- Budget state.
- Overrun warnings.
- Unused capital return records.

Security requirements:

- Budget changes require actor authorization and policy-scoped permissions.

Governance requirements:

- Budget increases, re-budgeting, and cancellations require governed approval.

Failure handling:

- Freeze releases when spend or budget state cannot be verified.

Audit requirements:

- Record budget baseline, changes, approvals, release history, spend verification, and unused capital return.

## Capital Release Manager

Purpose: Release approved capital only when lifecycle, milestone, policy, and approval requirements are satisfied.

Responsibilities:

- Validate release readiness.
- Enforce milestone funding gates.
- Coordinate holdbacks and partial releases.
- Block releases when policy, evidence, compliance, or approval is incomplete.

Non-responsibilities:

- Creating milestone strategy.
- Deciding venture attractiveness.

Inputs:

- Approved funding plan.
- Milestone evidence.
- Policy Engine outcome.
- Founder or governed approval.

Outputs:

- Release decision record.
- Released capital state event.
- Blocked release reason.

Security requirements:

- Release actions require strong authorization and tamper detection.

Governance requirements:

- Capital release must pass Policy Engine and required approvals.

Failure handling:

- Fail closed on incomplete approval, stale evidence, missing milestone proof, ledger mismatch, or compliance uncertainty.

Audit requirements:

- Record release amount, source reservation, milestone, policy result, approver, evidence, and recipient scope.

## Treasury Auditor

Purpose: Verify that every capital movement is authorized, traceable, complete, and consistent.

Responsibilities:

- Review capital lifecycle records.
- Detect missing approvals, ledger gaps, duplicate allocations, and policy mismatches.
- Produce audit findings and escalation records.

Non-responsibilities:

- Approving capital movement.
- Editing historical audit records.

Inputs:

- Capital ledger entries.
- Evidence, Decision, and Audit records.
- Policy snapshots.
- Reconciliation reports.

Outputs:

- Audit findings.
- Exception reports.
- Incident recommendations.

Security requirements:

- Auditor access is read-oriented and policy-scoped.
- Audit records are append-only.

Governance requirements:

- Material exceptions require escalation and Founder visibility.

Failure handling:

- Escalate suspected tampering, missing approvals, duplicate allocation, or ledger inconsistency.

Audit requirements:

- Auditor actions are themselves auditable.

## Treasury Security

Purpose: Protect financial workflows from unauthorized access, tampering, fraud, and anomalous activity.

Responsibilities:

- Enforce multi-step approvals, segregation of duties, anomaly detection, fraud detection, and emergency lock.
- Verify cryptographic audit trail and immutable ledger requirements.

Non-responsibilities:

- Business recommendation.
- Policy creation.

Inputs:

- Financial action requests.
- Actor identity and authorization records.
- Ledger integrity signals.
- Anomaly signals.

Outputs:

- Security approval, denial, or escalation.
- Emergency lock events.
- Fraud and anomaly alerts.

Security requirements:

- High-value actions require additional approval and integrity checks.
- Emergency lock must fail closed.

Governance requirements:

- Security overrides require explicit policy and audit.

Failure handling:

- Lock affected capital path on suspected fraud, tampering, identity compromise, or ledger corruption.

Audit requirements:

- Record security checks, alerts, decisions, lock actions, and release from lock.

## Treasury Risk Engine

Purpose: Evaluate financial risk before and after capital decisions.

Responsibilities:

- Assess cash runway, concentration risk, depletion risk, funding dependency, downturn exposure, cost growth, and budget overrun risk.
- Provide risk findings to Policy Engine, Founder Financial Dashboard, and Capital Allocation Governance.

Non-responsibilities:

- Making final capital decisions.
- Moving money.

Inputs:

- Capital balances.
- Budget plans.
- Portfolio exposure.
- Spend trends.
- Stress simulation scenarios.

Outputs:

- Risk scores.
- Risk explanations.
- Mitigation recommendations.
- Escalation triggers.

Security requirements:

- Risk inputs and outputs must preserve Organization, Portfolio, Venture, and actor scope.

Governance requirements:

- High-risk capital actions require governed review and may require Founder approval.

Failure handling:

- Fail closed for capital-sensitive actions when risk state cannot be evaluated.

Audit requirements:

- Record assumptions, data freshness, policy version, risk output, and recommendation rationale.

## Capital Stress Simulator

Purpose: Simulate adverse financial scenarios before capital is committed or released.

Responsibilities:

- Model market crash, venture failure, double budget, zero revenue, delayed launch, fundraising failure, and multiple simultaneous failures.
- Produce recommended actions, capital preservation strategy, confidence, and remaining runway.

Non-responsibilities:

- Executing mitigation.
- Replacing Founder decision-making.

Inputs:

- Portfolio state.
- Capital lifecycle state.
- Budget plans.
- Scenario definitions.
- Risk assumptions.

Outputs:

- Scenario results.
- Recommended actions.
- Capital preservation strategy.
- Confidence and remaining runway.

Security requirements:

- Simulation outputs must not expose unauthorized portfolio or venture details.

Governance requirements:

- Simulation results inform Decisions but do not become Evidence automatically.

Failure handling:

- Mark simulation invalid when inputs are stale, incomplete, unauthorized, or inconsistent.

Audit requirements:

- Record scenario, assumptions, input freshness, model version, outputs, and user-visible warnings.

## Placeholder Status

This is architecture documentation only. It does not define financial integrations, payment rails, custodial accounts, securities workflows, schemas, secrets, or implementation.
