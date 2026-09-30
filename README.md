# PROJECT V // GATEKEEPER

**Project V // Gatekeeper** is a local-first Windows network intelligence, application firewall, privacy visibility, and policy-control platform built around explicit user control and reversible enforcement.

> **Current release:** Gatekeeper **v1.0.0 Final**  
> **Platform:** Windows x64  
> **Repository model:** Public documentation + binary releases · Source code intentionally withheld

---

## What Gatekeeper is

Gatekeeper is designed to show what applications are communicating, where they are communicating, and what network policy is being enforced — without requiring a cloud account for normal operation.

It combines a Tauri desktop interface with a privileged local Gatekeeper Core service and Windows Filtering Platform (WFP) integration.

The design priorities are:

- local-first processing
- transparent network visibility
- explicit policy control
- reversible enforcement
- persistent local state
- safe recovery paths

## Core capabilities

Gatekeeper currently includes:

- live TCP/UDP network visibility
- process and executable attribution
- per-application network inspection
- native Windows Filtering Platform enforcement
- inbound/outbound/scope/endpoint policy controls
- global and per-app protection pause/resume
- policy profiles and reusable templates
- template assignment with SYNC / DRIFT tracking
- explicit Apply / Reapply behavior
- Learning Mode
- blocklist and allowlist intelligence
- native WFP block-event attribution
- persistent searchable Event Ledger
- DNS/direct-route/proxy/Tor privacy observations
- backup, rollback, and recovery controls
- authenticated local IPC with the privileged Gatekeeper Core service

## Network intelligence

Gatekeeper can observe and correlate:

- applications and processes
- TCP and UDP sockets
- remote IP addresses and ports
- listening ports
- Internet / LAN / loopback scope
- Windows WFP block events
- blocklist and allowlist matches
- application network behavior over time
- plaintext DNS-port observations
- DNS-over-TLS observations
- direct Internet paths
- local proxy / SOCKS / Tor candidates

The Event Ledger retains bounded local network history and supports search, filtering, per-application summaries, and CSV/JSON export.

## Firewall and protection

Gatekeeper uses a privileged local Core service for firewall authority.

The current architecture includes:

- native WFP application enforcement
- authenticated local IPC
- reversible application protection
- global Disable / Resume protection
- policy rehydration
- temporary decisions
- recovery journals
- emergency Gatekeeper-only cleanup
- protection-state persistence

Assigning or editing a policy does **not** silently alter enforcement. Staged policy changes require explicit Apply actions.

## Policy management

Gatekeeper includes reusable policy templates such as:

- Observe Only
- Browser
- Game
- Trusted LAN Only
- No Internet
- Locked Down

Custom templates and policy profiles can also be created.

Gatekeeper tracks whether an application's draft policy matches its assigned template and whether that draft has been explicitly applied.

## Privacy intelligence

Gatekeeper reports privacy observations that can be established from available Windows telemetry, including:

- plaintext DNS observations
- DNS-over-TLS observations
- direct Internet paths
- local proxy / SOCKS / Tor candidates

Gatekeeper intentionally does **not** claim visibility it does not have. For example, ordinary HTTPS traffic is not automatically classified as DNS-over-HTTPS, and the presence of a local Tor/SOCKS endpoint is not presented as proof that a specific application is protected by that route.

## Local-first design

Normal Gatekeeper monitoring and policy management do not require a Project V cloud account.

Policy state, templates, Event Ledger data, and application settings are maintained locally.

## Installer and portable builds

The standard Windows installer is the recommended configuration.

A desktop-portable build can also run from removable storage.

**Important:** the portable desktop executable does not make the privileged Gatekeeper Core service portable. Native firewall enforcement requires Gatekeeper Core to already be installed and running on the Windows computer.

## Current release

**Project V // Gatekeeper v1.0.0 Final** completed release-candidate regression, USB portable validation, hidden-background-process validation, TypeScript/Rust build validation, and final packaging validation on September 26, 2026.

See [RELEASE-NOTES-1.0.0.md](RELEASE-NOTES-1.0.0.md).

## Downloads

Official Windows binaries are distributed through **GitHub Releases**.

The v1.0.0 release package is intended to include:

- Windows installer
- desktop-portable ZIP
- SHA-256 manifest
- release notes

Verify downloaded files using the published SHA-256 manifest before running them.

## Screenshots

A visual gallery of the current Gatekeeper interface will be maintained here.

_Screenshots will be added from validated Gatekeeper builds._

## Repository policy

This repository is currently used for **validated Gatekeeper executable releases and public documentation**.

The Gatekeeper application source code is **not being published at this stage**.

This is intentional, not an incomplete repository. Source publication may be reconsidered later after additional stabilization, review, and a deliberate open-source decision.

Do not commit:

- API keys or credentials
- signing certificates or private keys
- local policy databases
- Event Ledger exports containing private data
- machine-specific logs
- local configuration containing secrets
- user-specific network history

## Security notice

Gatekeeper is security-oriented software, but it should not be interpreted as independently security-audited unless a specific external audit is published.

Unsigned builds may trigger Windows SmartScreen or publisher warnings.

See [SECURITY.md](SECURITY.md).

## Privacy

See [PRIVACY.md](PRIVACY.md).

## Documentation

- [Installation](docs/INSTALLATION.md)
- [Portable Build](docs/PORTABLE.md)
- [Feature Overview](docs/FEATURES.md)
- [Security Architecture](docs/SECURITY-ARCHITECTURE.md)
- [Release Verification](docs/RELEASE-VERIFICATION.md)

## License

Gatekeeper is **not open-source software**.

The public release is distributed under the **Project V Personal Use License**. Personal, non-commercial use is permitted under the license terms. Redistribution, resale, republishing, derivative distribution, and incorporation into another product are prohibited without prior written permission.

See [LICENSE.md](LICENSE.md).

---

**Project V // Gatekeeper**  
Visibility first. Identity second. Policy third. Enforcement only with a rollback path.
