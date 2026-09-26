# Gatekeeper Feature Overview

## Live Monitor

Gatekeeper provides live Windows network visibility with application/process attribution and connection inspection.

## Application Inspector

Per-application views expose connection activity, application identity, policy state, and relevant enforcement controls.

## Protected Applications

Protected Applications provides centralized visibility into applications with active or saved Gatekeeper protection state.

## Policy Management

Gatekeeper supports:

- per-application policy drafts
- reusable policy profiles
- reusable policy templates
- built-in and custom templates
- template assignment
- SYNC / DRIFT detection
- explicit Apply Draft
- Re-stage + Apply
- bulk assignment management
- bulk apply/reapply operations
- policy backup
- rollback state

## Learning Mode

Learning Mode observes application network behavior and can assist with building more informed policies without silently converting observation into enforcement.

## Blocklist Intelligence

Gatekeeper can maintain user-configured blocklists/allowlists, correlate matches, and integrate active native enforcement where supported.

## WFP Audit Attribution

Native Windows WFP block events can be surfaced with filter/application attribution where available.

## Event Ledger

The Event Ledger provides persistent bounded local network-event history, search/filter controls, application intelligence summaries, endpoint accounting, and CSV/JSON export.

## Privacy Intelligence

Gatekeeper can surface:

- plaintext DNS observations
- DNS-over-TLS observations
- direct Internet observations
- local proxy / SOCKS / Tor candidates

These are observations, not guarantees of privacy or routing.

## Release Readiness

The release-hardening layer can check operational prerequisites such as Core installation/running state, authenticated IPC readiness, WFP registration, recovery state, and master protection.
