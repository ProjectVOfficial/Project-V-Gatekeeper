# Gatekeeper Security Architecture

This document is a high-level public description. It intentionally does not publish the private source implementation.

## Desktop / Core Separation

Gatekeeper separates the desktop UI from privileged firewall authority.

The desktop communicates with a local Gatekeeper Core service through authenticated local IPC.

## Windows Filtering Platform

Gatekeeper uses Windows Filtering Platform (WFP) for native enforcement paths.

The design includes Gatekeeper-owned WFP registration and managed enforcement state.

## Explicit Enforcement

Gatekeeper distinguishes between:

- observed state
- saved/staged policy
- assigned policy template
- explicitly applied enforcement

Template assignment or draft editing does not by itself imply live enforcement.

## Reversible Protection

Gatekeeper supports system-wide and per-application pause/resume semantics intended to suspend enforcement while preserving saved policy state.

## Recovery

Gatekeeper includes crash/recovery state for supported enforcement operations so interrupted changes can be detected and handled rather than silently abandoned.

## Fail-Open Considerations

Dynamic WFP enforcement paths are designed with Core/session-loss behavior in mind. A stopped or unavailable Core should not leave an undocumented dynamic filtering session pretending to be healthy.

## Diagnostics

Release-readiness and safe-diagnostics exports are intended to report operational state without intentionally exporting authentication tokens or complete policy contents.

Users should still review diagnostic files before sharing them.

## Boundaries

Gatekeeper does not claim that:

- all network traffic can always be attributed perfectly;
- privacy-routing guarantees can be inferred from ordinary socket telemetry;
- internal validation equals independent third-party security audit.

Those distinctions are intentional.
