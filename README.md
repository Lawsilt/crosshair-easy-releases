# Crosshair Easy — Official Release Assets

This repository hosts the official Windows release assets for **Crosshair Easy**. It
contains no source code.

Every stable release provides exactly three assets:

| Asset | Purpose |
|---|---|
| `CrosshairEasySetup.exe` | Windows installer bundle (64-bit) |
| `update.json` | Signed update manifest: product, platform, version, installer name, size and SHA-256 |
| `update.json.sig` | Detached ECDSA P-256 / SHA-256 signature (IEEE P1363, base64) over the exact bytes of `update.json` |

The desktop application verifies `update.json.sig` against a public key embedded in the
shipped build before downloading anything for execution, and re-verifies the installer's
size and SHA-256 immediately before launch. Unsigned, altered or mismatched artifacts are
rejected.

Download the latest release:
https://github.com/Lawsilt/crosshair-easy-releases/releases/latest
