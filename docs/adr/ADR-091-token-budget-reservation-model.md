# ADR-091: Token Budget Reservation Model

Parent: `docs/architecture/ai-token-governance.md`

Status: Accepted

## Context

Token budgets can be overrun by concurrent execution unless budget capacity is reserved before use.

## Decision

Adopt token reservation before execution, reservation expiry, reservation release, over-consumption behavior, AI Gateway enforcement after reservation, race condition handling, and inheritance rules from Organization to Execution.

## Alternatives

- Check token budget only after execution.
- Use soft monitoring without reservation.
- Reserve only at Organization level.

## Rationale

Tokens are financial resources and must not be consumed through race conditions or stale budget assumptions.

## Risks

Reservations may temporarily reduce available token budget until released.

## Consequences

AI Gateway, Resource Coordinator, Treasury, and AI Token Governance must preserve reservation state and release behavior.

## Enforcement

The most restrictive applicable token limit wins unless an approved governance override exists.
