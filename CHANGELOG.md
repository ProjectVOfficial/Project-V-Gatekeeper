# Changelog

Notable public Gatekeeper changes are documented here.

## 1.0.0 — Pending Final Release

Final 1.0 release is pending completion of release-candidate regression, portable-build validation, installer validation, and final packaging.

## 1.0.0-rc.1 — Release Candidate

### Release hardening

- feature freeze
- unified release-candidate source validation
- production build and packaging workflow
- release-readiness preflight
- safe diagnostics export
- user-facing version cleanup
- stale placeholder cleanup
- portable desktop candidate packaging

### RC hotfixes

- RC1a: encoding-safe Core boundary checker
- RC1b: TypeScript compile repair for removed placeholder fallback
- RC1c: hidden background PowerShell process spawning in packaged desktop builds

### Features carried into RC

- live TCP/UDP connection visibility
- per-application inspector
- protected-application controls
- native WFP enforcement
- authenticated Core IPC
- reversible policy enforcement
- policy templates and assignment management
- SYNC / DRIFT state
- explicit Apply / Reapply controls
- policy backup and rollback
- Learning Mode
- blocklist and allowlist intelligence
- WFP audit attribution
- persistent Event Ledger
- Event Intelligence accuracy hardening
- Privacy Intelligence
- release-readiness preflight

## Earlier Development

Gatekeeper evolved through staged foundations covering application identity, Core service authority, Windows Filtering Platform integration, policy management, Learning Mode, blocklist intelligence, Event Ledger, privacy intelligence, and release hardening.

The public repository intentionally does not publish the private development source tree or every internal development patch.
