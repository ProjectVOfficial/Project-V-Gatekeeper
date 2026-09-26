# PROJECT V // GATEKEEPER

**Local-first Windows network intelligence, application firewall policy, WFP enforcement, privacy visibility, and reversible network control.**

> **Status:** Gatekeeper 1.0 Release Candidate  
> **Platform:** Windows x64  
> **Source model:** Proprietary / source-closed public release repository

Project V // Gatekeeper is a Windows-first network visibility, application-policy, and firewall-control platform designed to show what applications are communicating, where they are communicating, and what network policy is being enforced.

Gatekeeper combines a Tauri desktop interface with a privileged local Gatekeeper Core service and Windows Filtering Platform (WFP) integration. Its design emphasizes local processing, explicit user control, reversible enforcement, persistent policy state, and clear separation between observation and enforcement.

## What Gatekeeper Does

Gatekeeper provides:

- live TCP/UDP network visibility
- process and executable attribution
- per-application network inspection
- native Windows Filtering Platform enforcement
- inbound, outbound, scope, and endpoint policy controls
- per-application and global protection pause/resume
- policy profiles and reusable policy templates
- template assignment with SYNC / DRIFT tracking
- explicit Apply / Reapply policy controls
- Learning Mode
- blocklist and allowlist intelligence
- native WFP block-event attribution
- persistent searchable Event Ledger
- privacy intelligence for DNS, direct-route, and local proxy/Tor observations
- policy backup, rollback, and recovery controls
- authenticated local IPC with the privileged Gatekeeper Core service

## Network Intelligence

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

## Firewall & Protection

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

Gatekeeper is designed so that assigning or editing a policy does **not** silently alter enforcement. Explicit Apply actions are required for staged policy changes.

## Policy Management

Gatekeeper includes reusable built-in policy templates such as:

- Observe Only
- Browser
- Game
- Trusted LAN Only
- No Internet
- Locked Down

Custom templates and policy profiles can also be created.

Gatekeeper tracks whether an application's draft policy matches its assigned template and whether that draft has been explicitly applied.

## Privacy Intelligence

Gatekeeper reports privacy observations that can be established from available Windows telemetry, including:

- plaintext DNS observations
- DNS-over-TLS observations
- direct Internet paths
- local proxy / SOCKS / Tor candidates

Gatekeeper intentionally does **not** claim visibility it does not have. For example, ordinary HTTPS traffic is not automatically classified as DNS-over-HTTPS, and the presence of a local Tor/SOCKS endpoint is not presented as proof that a particular application is protected by that route.

## Local-First Design

Normal Gatekeeper monitoring and policy management do not require a Project V cloud account.

Policy state, templates, Event Ledger data, and application settings are maintained locally.

## Installer and Portable Builds

The standard Windows installer is the recommended configuration.

A desktop-portable build can also run from removable storage.

**Important:** the portable desktop executable does not make the privileged Gatekeeper Core service portable. Native firewall enforcement requires Gatekeeper Core to already be installed and running on the Windows computer.

## Current Release Status

Gatekeeper is currently in the final 1.0 release-candidate validation cycle.

The release candidate has completed feature freeze and is undergoing final packaging, portable-build, regression, and clean-release validation before 1.0.0 Final.

## Downloads

Official Windows binaries will be published under **GitHub Releases** after final validation.

When releases are available, verify downloaded files using the published SHA-256 manifest before running them.

## Security Notice

Gatekeeper is security-oriented software, but it should not be interpreted as independently security-audited unless a specific external audit is published.

Unsigned development or release-candidate builds may also trigger Windows SmartScreen or publisher warnings.

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
