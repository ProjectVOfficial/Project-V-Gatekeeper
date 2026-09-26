# Gatekeeper Desktop-Portable Build

Gatekeeper can provide a desktop-portable executable suitable for removable storage.

## Important Architecture Boundary

The desktop-portable executable is **not** a fully portable privileged firewall stack.

Native Gatekeeper enforcement requires the **Gatekeeper Core service** to already be installed and running on the Windows machine.

The portable build can therefore be useful as a removable Gatekeeper desktop interface on a machine that already has the required Core installation.

## USB Usage

1. Download the official portable ZIP from GitHub Releases.
2. Verify its SHA-256 value.
3. Extract the ZIP to the USB drive.
4. Run the Gatekeeper desktop executable.
5. Review Settings / Release Readiness to confirm the local Core service is available.

## Background Windows

Release builds should run recurring telemetry and status helpers without flashing visible PowerShell console windows.

If repeated console windows appear during passive monitoring, report the exact Gatekeeper version and whether the build was installer or portable.

## Data Persistence

Some application state may be stored in the Windows user's normal application/local storage rather than solely beside the portable executable.

"Desktop portable" therefore means the executable can be carried and launched from removable storage; it does not imply that every state file, privileged service, or Windows integration is contained on the removable drive.
