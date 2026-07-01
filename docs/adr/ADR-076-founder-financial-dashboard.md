# ADR-076: Founder Financial Dashboard

Status: Accepted

Date: 2026-07-01

## Context

Founder control requires clear financial visibility across cash, reserves, commitments, release, spend, runway, portfolio allocation, return, Enterprise Value, pipeline, risk, and upcoming funding decisions.

## Decision

Adopt Founder Financial Dashboard as the founder-facing financial visibility layer inside Founder Command Center.

It must show cash available, capital reserved, capital committed, capital released, expected runway, burn rate, portfolio allocation, ROI, Enterprise Value trend, investment pipeline, financial risk score, and upcoming funding decisions.

## Rationale

Founder governance cannot be preserved if the Founder lacks timely financial visibility.

## Consequences

- Financial facts, assumptions, forecasts, and AI recommendations must be clearly distinguished.
- Security alerts, emergency locks, and capital freezes must be Founder-visible.
- Dashboard does not approve or move money.

## Enforcement

Dashboard actions must route through Policy Engine and Treasury Domain. Founder approvals must be recorded in Decision Ledger and Audit Ledger.
