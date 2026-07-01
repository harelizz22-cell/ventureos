# Milestone Funding

Parent: `docs/architecture/treasury-domain.md`

Source Of Truth: This file is the source of truth for Milestone Funding architecture.

## Purpose

Milestone Funding releases capital in stages so VentureOS can preserve capital, verify progress, and stop or adjust funding when evidence changes.

## Funding Flow

Budget Approved -> Milestone 1 -> Review -> Milestone 2 -> Review -> Milestone 3 -> Completion

Each stage requires evidence, policy evaluation, lifecycle state verification, and applicable approvals before capital can be released.

## Partial Funding

Partial funding allows a portion of approved capital to be released while the remainder stays reserved, held back, or pending review.

Rules:

- Partial releases must be linked to a milestone and capital lifecycle state.
- Partial release does not imply future release approval.

## Holdbacks

Holdbacks preserve capital until defined conditions are met.

Rules:

- Holdback amount and conditions must be explicit.
- Holdbacks must remain visible in Founder Financial Dashboard.
- Holdbacks must not be counted as Available capital.

## Re-Budgeting

Re-budgeting changes the approved funding plan.

Rules:

- Re-budgeting requires Policy Engine evaluation.
- Material increases or scope changes require Founder approval where policy requires it.
- Re-budgeting must preserve original audit and create a new Decision record.

## Fund Cancellation

Funding may be cancelled when milestones fail, evidence weakens, risk increases, compliance blocks, runway worsens, or Founder policy changes.

Rules:

- Cancellation must record reason, authority, affected lifecycle records, and capital returned or closed.
- Cancelled funding must not remain silently reserved.

## Unused Capital Return

Unused capital must return through a governed lifecycle transition.

Rules:

- Returned capital must reference the original allocation, release, or spend record.
- Returned capital must be reconciled before becoming Available.

## Governance Rules

- No money can move without Policy Engine evaluation.
- Every release must link to milestone evidence.
- Treasury controls release state but does not evaluate venture attractiveness.
- Founder retains final governance for high-value, exceptional, or policy-defined funding actions.

## Placeholder Status

This is architecture documentation only. It does not define payment processing, fund custody, securities activity, financial integrations, schemas, or implementation.
