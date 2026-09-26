# Installing Project V // Gatekeeper

## Recommended Installation

The normal Windows installer is the recommended Gatekeeper configuration because privileged firewall enforcement depends on the Gatekeeper Core service.

## Requirements

- Windows x64
- administrator rights for privileged Core/service installation
- Windows Filtering Platform available
- sufficient permission for Gatekeeper's firewall-control operations

## Installation Flow

1. Download the official Gatekeeper installer from the repository's **Releases** page.
2. Verify the SHA-256 value against the published release manifest.
3. Run the installer.
4. Approve Windows elevation when required.
5. Launch Gatekeeper.
6. Open **Settings** and review the Release Readiness panel.

A healthy protected installation should report the expected Core, authenticated IPC, WFP registration, recovery, and master-protection checks as passing.

## Windows Warnings

Development, release-candidate, or unsigned builds may trigger Windows SmartScreen or unknown-publisher warnings.

A warning is not proof that a file is malicious, but users should verify the release source and SHA-256 value before proceeding.

## Firewall State

Gatekeeper is designed to manage its own enforcement state and avoid silently deleting unrelated Windows firewall rules.

Use Gatekeeper's own protection, cleanup, and recovery controls rather than manually deleting Gatekeeper-managed state unless performing documented recovery.

## Uninstall / Recovery

Before uninstalling a test build, use the appropriate Gatekeeper cleanup or disable controls if you want active Gatekeeper enforcement removed.

Release-specific uninstall and migration notes should be included with each stable release.
