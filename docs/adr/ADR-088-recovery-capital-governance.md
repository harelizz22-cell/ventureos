# ADR-088: Recovery Capital Governance

Parent: `docs/architecture/recovery-governance.md`

Status: Accepted

## Context

Recovery can affect capital state through reservations, releases, spend, refunds, compensation, or rollback.

## Decision

Capital-sensitive recovery requires Treasury notification, Evidence, approval path, compensation or rollback capital handling, and audit records.

## Alternatives

- Treat recovery as operational only.
- Allow automatic capital recovery.
- Handle capital recovery only inside Treasury implementation.

## Rationale

Recovery must not bypass capital governance or rewrite capital history.

## Risks

Recovery may slow when capital impact is uncertain.

## Consequences

Recovery Governance, Treasury Domain, and Capital Lifecycle must preserve capital-sensitive recovery records.

## Enforcement

Capital-sensitive recovery fails closed or escalates when Treasury, Evidence, approval, lifecycle state, or audit path cannot be verified.
