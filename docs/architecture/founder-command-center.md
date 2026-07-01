# Founder Command Center

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Founder Command Center architecture.

## Purpose

Founder Operating Console is the primary product entry. Founder Command Center is the primary screen inside that console.

The Founder Command Center is the founder-facing control surface for approvals, portfolio and venture status, evidence review, decisions, risks, spending thresholds, capability status, execution status, and production asset health.

## Founder Visibility Requirement

The Founder Operating Console must answer within five seconds:

- Where is my money?
- Where is my risk?
- Where is my growth?
- What requires my approval?
- What is blocked?
- What changed today?
- What is the expected outcome?

The Founder should never need to inspect logs to understand business health.

## Rule

The Founder Command Center must preserve founder authority and decision auditability.

The Founder Command Center must scale from a flat pending queue to prioritized triage as Venture count grows.

AI may recommend prioritization, but may not approve decisions on behalf of the Founder unless Autonomy Policy explicitly allows it.

Future investor marketplace and funding views must show Investment Readiness, dossier status, funding readiness, compliance status, investor communication records, capital target status, milestone release recommendations, and risk without enabling autonomous money movement.

Founder Command Center must surface Strategic Review recommendations, dissent summary, required approvals, Investment Memo status, Runtime Kernel execution state, approval waits, recovery state, and resource blocks where meaningful.

Founder Financial Dashboard is the founder-facing financial visibility layer inside Founder Command Center. It must show cash available, capital reserved, capital committed, capital released, expected runway, burn rate, portfolio allocation, ROI, Enterprise Value trend, investment pipeline, financial risk score, and upcoming funding decisions.

Founder Financial Dashboard does not move money, approve capital by itself, or bypass Policy Engine.
