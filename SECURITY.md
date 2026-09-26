# Security Policy

Project V // Gatekeeper is security-sensitive software. Reports involving firewall enforcement, authenticated IPC, WFP behavior, privilege boundaries, policy bypass, unsafe rollback, or executable identity handling are treated as security issues.

## Supported Versions

During the 1.0 release-candidate period, only the newest published release candidate is supported for security testing.

After 1.0.0 Final, the current stable release will receive priority for security fixes.

## Reporting a Vulnerability

Please **do not publish exploit details in a public GitHub issue** before Project V has had a reasonable opportunity to investigate.

For a suspected vulnerability:

1. Open a GitHub issue containing only a minimal non-sensitive description and request a private security contact path, or use GitHub's private vulnerability reporting feature if it is enabled for this repository.
2. Include the Gatekeeper version, Windows version, whether the Core service was installed/running, and the smallest reproducible sequence.
3. Do not include authentication tokens, private logs, personal network data, or sensitive identifiers in a public issue.

## Particularly Important Areas

Reports are especially useful when they involve:

- unintended firewall bypass or over-blocking
- WFP filter persistence or cleanup failures
- privilege escalation
- unsafe Core IPC authentication behavior
- policy state being applied without explicit user action
- recovery-journal failure
- unsafe rollback behavior
- executable identity confusion
- release binary tampering
- secrets or authentication material exposed in diagnostics

## Security Architecture

Gatekeeper uses a privileged local Core service for firewall authority and authenticated local IPC. Dynamic WFP enforcement is designed with fail-open and recovery considerations, while policy state is retained separately for rehydration.

See [docs/SECURITY-ARCHITECTURE.md](docs/SECURITY-ARCHITECTURE.md).

## Scope Note

Gatekeeper has not been represented as independently audited unless a specific external audit is published here.

A successful internal test or release-readiness check is not equivalent to an independent penetration test or formal security audit.
