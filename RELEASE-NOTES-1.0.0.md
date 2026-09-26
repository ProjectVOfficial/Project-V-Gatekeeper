# Project V // Gatekeeper 1.0.0 Final

**Release date:** September 26, 2026  
**Platform:** Windows x64  
**Release channel:** Stable

Project V // Gatekeeper 1.0.0 is the first stable release of the Project V local-first Windows network-intelligence and application-firewall platform.

## Highlights

Gatekeeper 1.0.0 combines live Windows network visibility with explicit, reversible application policy and privileged Windows Filtering Platform enforcement.

The release includes:

- live TCP/UDP application network visibility
- process and executable attribution
- per-application inspection
- native WFP policy enforcement
- privileged Gatekeeper Core service
- authenticated local IPC
- global and per-app protection pause/resume
- reusable application policy templates
- policy assignment with SYNC / DRIFT tracking
- explicit Apply / Reapply operations
- Learning Mode
- blocklist and allowlist intelligence
- WFP block-event attribution
- persistent searchable Event Ledger
- Privacy Intelligence
- policy backup and rollback
- release-readiness preflight
- safe diagnostic export
- installer and desktop-portable packaging

## Release-Candidate Fixes Carried Into Final

The 1.0 RC cycle identified and resolved several release-specific issues:

- encoding-sensitive source-check validation
- stale removed-placeholder TypeScript reference
- visible background PowerShell windows in packaged/portable builds

The PowerShell-window issue was corrected at the centralized Rust/Tauri process-launch layer using hidden Windows background-process creation while retaining non-interactive telemetry behavior.

## Portable Build

The desktop-portable build was validated from removable USB storage.

During the final RC validation run:

- Gatekeeper launched successfully from the USB
- normal monitoring continued
- recurring PowerShell windows did not flash
- the portable application remained operational during the validation period

The portable desktop application does **not** make Gatekeeper Core portable. Privileged firewall enforcement still requires Gatekeeper Core to be installed and running on the Windows host.

## Verification

Verify official release artifacts against the SHA-256 manifest published with the GitHub Release.

See [docs/RELEASE-VERIFICATION.md](docs/RELEASE-VERIFICATION.md).

## Security Boundary

Gatekeeper 1.0.0 is security-oriented software but is not represented as independently security-audited unless a separate external audit is published.

## License

Gatekeeper is proprietary software distributed under the [Project V Personal Use License](LICENSE.md).

Personal, non-commercial use is permitted under that license. Redistribution, resale, republishing, derivative distribution, and incorporation into another product require prior written permission.
