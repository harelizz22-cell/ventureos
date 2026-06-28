# ADR-001: Architecture Source of Truth

## Status

Accepted

## Context

VentureOS requires one authoritative architecture reference to prevent undocumented implementation drift.

## Decision

`docs/architecture/ventureos-v2-architecture-master.md` is the master architecture source of truth.

## Consequences

Architecture-impacting changes must update the master architecture before phase specifications or implementation work proceeds.

## Governance Notes

This decision supports auditability and prevents production code from outrunning approved architecture.

