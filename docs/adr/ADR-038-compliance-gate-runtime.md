# ADR-038: Compliance Gate Runtime

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Compliance Gate runtime decision.

## Status

Accepted

## Context

Future regulated capabilities, investor marketplace capabilities, and enhanced-review domains require an enforceable runtime compliance mechanism, not only documentation warnings.

## Decision

VentureOS adopts Compliance Gate as a required future runtime architecture concept.

Compliance Gate must include Compliance Gate Registry, Policy Engine evaluation, restricted capability categories, legal approval records, investment marketplace gating, and regulated domain gating.

## Consequences

- Compliance gates become explicit runtime architecture.
- Legal approval records become required for restricted capabilities.
- Investor marketplace and regulated domains remain blocked until compliance requirements are satisfied.

## Enforcement

No restricted capability may execute unless Compliance Gate and Policy Engine requirements are satisfied. This ADR does not approve regulated financial workflows or implementation.
