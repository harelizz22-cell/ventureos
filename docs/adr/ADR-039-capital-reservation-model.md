# ADR-039: Capital Reservation Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Capital Reservation Model decision.

## Status

Accepted

## Context

Capital allocation can create competing claims on the same budget or funding source. Without reservation architecture, VentureOS may overcommit capital or approve conflicting allocations.

## Decision

VentureOS adopts Capital Reservation and Conflict Model as a required architecture workstream.

The model must define capital reservations, competing allocations, reservation expiry, approval race conditions, overcommit prevention, and allocation audit.

## Consequences

- Capital reservations become governance records.
- Allocation conflict detection becomes required before implementation.
- Approval race conditions and expiry must be auditable.

## Enforcement

Capital reservations do not move money or execute investments. Any future allocation implementation must prevent overcommit and preserve allocation audit.
