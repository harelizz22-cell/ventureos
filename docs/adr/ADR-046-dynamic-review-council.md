# ADR-046: Dynamic Review Council

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Dynamic Review Council decision.

## Status

Accepted

## Context

Different opportunities require different review perspectives depending on type, risk, domain, capital required, jurisdiction, and regulatory sensitivity.

## Decision

VentureOS adopts Dynamic Review Council as the architecture mechanism for assembling opportunity-specific review participants.

## Alternatives considered

- Use one fixed review group for every opportunity.
- Let one Agent produce all review perspectives.
- Skip domain-specific review unless Founder asks manually.

## Rationale

Dynamic composition improves fit between opportunity risk and review expertise while preserving governance and Evidence requirements.

## Risks

- Council composition may miss required expertise.
- Agents may be mistaken for final approvers.
- Regulated opportunities may require enhanced review that is not yet defined.

## Consequences

- Council composition depends on opportunity type, risk, domain, required capital, jurisdiction, and regulatory sensitivity.
- Agents are participants only.
- Specialized experts may be required for medical, regulatory, security, legal/compliance, or investment review.

## Enforcement

Council participants do not self-approve, bypass Policy Engine, or bypass Evidence requirements.
