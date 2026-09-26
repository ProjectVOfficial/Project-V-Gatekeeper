# Verifying Gatekeeper Releases

Official Gatekeeper releases should provide SHA-256 hashes for distributed installer and portable artifacts.

## PowerShell Verification

From PowerShell:

```powershell
Get-FileHash .\Project-V-Gatekeeper-1.0.0-Setup.exe -Algorithm SHA256
```

For a portable archive:

```powershell
Get-FileHash .\Project-V-Gatekeeper-1.0.0-Desktop-Portable.zip -Algorithm SHA256
```

Compare the resulting hash to the value published with the GitHub Release.

## Authenticode

If a release is code-signed, Windows can show signature information through file Properties or PowerShell.

Unsigned release-candidate builds may legitimately report no trusted publisher signature.

Do not treat a missing signature as equivalent to a hash mismatch. They are separate verification mechanisms.

## Source of Download

Prefer files attached directly to the official Project V // Gatekeeper GitHub Release.

Avoid third-party mirrors unless Project V explicitly identifies them as authorized distribution sources.

## Modified Copies

The Project V Personal Use License does not grant permission to redistribute modified Gatekeeper binaries.

A binary obtained from an unofficial mirror should not be assumed to match the official Project V release.
