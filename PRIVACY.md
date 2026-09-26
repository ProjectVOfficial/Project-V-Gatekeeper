# Privacy

Project V // Gatekeeper is designed as a local-first Windows network intelligence and firewall-control application.

## Local Processing

Normal Gatekeeper monitoring and policy management operate locally on the Windows computer.

Gatekeeper does not require a Project V cloud account for normal network visibility or local firewall-control features.

## Local Data

Depending on enabled features, Gatekeeper may locally retain information such as:

- application and executable names/paths
- process identifiers
- local and remote IP addresses
- local and remote ports
- protocol and connection-state information
- WFP block-event metadata
- policy and template assignments
- Learning Mode observations
- blocklist/allowlist match history
- Event Ledger history
- privacy observations
- release-readiness diagnostics

This information can reveal sensitive details about applications and network activity. Users should protect exported diagnostics and Event Ledger files accordingly.

## Event Ledger

The Event Ledger is designed with bounded retention controls. Users can adjust supported retention settings and clear retained history from within Gatekeeper.

## Exports

Gatekeeper can create local exports such as CSV, JSON, privacy reports, and safe diagnostics.

Exports are created at the user's request and should be treated as potentially sensitive files.

## Privacy Intelligence Boundaries

Gatekeeper reports only observations supported by the telemetry available to it.

For example:

- ordinary HTTPS traffic is not automatically classified as DNS-over-HTTPS;
- the presence of a local proxy, SOCKS endpoint, or Tor listener is not presented as proof that a specific application is routed through it;
- a lack of observed plaintext DNS does not prove that all DNS activity is encrypted.

## Network Access

Some optional features, such as user-configured blocklist feed retrieval, may access external URLs selected or enabled by the user.

Those external services are governed by their own privacy policies.

## Project V Telemetry

The public Gatekeeper release should not be described as transmitting analytics, account telemetry, or Event Ledger contents to Project V unless a future version explicitly adds and documents such functionality.

## Security Logs

The privileged Gatekeeper Core may maintain local operational or recovery logs required for firewall control and crash-safe recovery.

Users should review files before sharing diagnostics publicly.

## Changes

If a future Gatekeeper version adds cloud services, remote synchronization, crash reporting, or analytics, this document should be updated before that functionality is released.
