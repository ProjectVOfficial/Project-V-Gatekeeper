# Changelog

Notable public Gatekeeper changes are documented here.

## 1.0.0 — Final Release — 2026-09-26

Project V // Gatekeeper 1.0.0 completed its release-candidate cycle and final packaging validation.

### Final release status

- final source validation passed
- TypeScript validation passed
- Rust/Tauri build validation passed
- installer packaging completed successfully
- desktop-portable packaging completed successfully
- USB portable runtime validation passed
- recurring background PowerShell console flashing fixed and revalidated
- release identity finalized as 1.0.0

### Core capabilities

- live TCP/UDP connection visibility
- process and executable attribution
- per-application inspector
- protected-application controls
- native Windows Filtering Platform enforcement
- authenticated Gatekeeper Core IPC
- reversible global and per-application protection
- policy templates and assignment management
- SYNC / DRIFT state
- explicit Apply / Reapply controls
- policy backup and rollback
- Learning Mode
- blocklist and allowlist intelligence
- WFP audit attribution
- persistent searchable Event Ledger
- Event Intelligence accuracy hardening
- Privacy Intelligence
- release-readiness preflight
- safe diagnostics export
- installer and desktop-portable release packaging

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

## Earlier Development

Gatekeeper evolved through staged foundations covering application identity, Core service authority, Windows Filtering Platform integration, policy management, Learning Mode, blocklist intelligence, Event Ledger, privacy intelligence, and release hardening.

The public repository intentionally does not publish the private development source tree or every internal development patch.
