# ADR-086: Policy Engine Degradation Model

Parent: `docs/architecture/policy-engine-consistency-model.md`

Status: Accepted

## Context

Claude Red Team Review identified that Policy Engine failure was documented, but partial degradation states were not explicit enough for runtime governance.

## Decision

Adopt Policy Engine degraded mode states, reduced evaluator behavior, stale snapshot behavior, elevated latency behavior, degraded-but-acceptable thresholds, degraded-to-fail-closed thresholds, and degraded evaluation audit records.

## Alternatives

- Treat any degradation as total outage.
- Allow degraded execution without thresholds.
- Leave degradation behavior to implementation.

## Rationale

VentureOS needs conservative fail-closed governance while still allowing low-risk reversible execution when policy confidence remains provable.

## Risks

Thresholds may be misunderstood as permission to continue risky execution during degraded governance.

## Consequences

Runtime components must classify degraded policy states and preserve degraded evaluation audit records.

## Enforcement

Capital-sensitive, compliance-sensitive, autonomy-expanding, production-asset, cross-Organization, irreversible, or Founder-approval-sensitive execution fails closed when required policy confidence cannot be proven.
