# prodxcloud / downloads

Artifact **mirror** for the vxcloud platform — a fallback download channel for when
`vxcloud.io` / S3 is unavailable. Everything here is published as **GitHub Releases**,
organized by per-product tags.

## What's here

| Product | Tag pattern | Assets |
|---|---|---|
| vxcli (CLI) | `vxcli-<version>` | `vxcli_<version>_<os>_<arch>` (linux/darwin/windows × amd64/arm64) + `checksums.txt` |
| vxcloud Desktop | `vxcloud-desktop-<version>` | `vxcloud-desktop-<version>-x64-setup.exe` (+ `.dmg`) + `checksums.txt` |
| Web build | `web-<version>` | `vxcloud-web-<version>.tar.gz` |
| Architecture / IaC | `iac-<version>` | bundles + `checksums.txt` |

Versions follow the fleet node version (`vxnode/stable.json`), e.g. `2026.6.13-1516`.

## Download

Browse all: <https://github.com/prodxcloud/downloads/releases>

Pin a version:
```
https://github.com/prodxcloud/downloads/releases/download/vxcli-2026.6.13-1516/vxcli_2026.6.13-1516_linux_amd64
https://github.com/prodxcloud/downloads/releases/download/vxcloud-desktop-2026.6.13-1516/vxcloud-desktop-2026.6.13-1516-x64-setup.exe
```
Verify against the `checksums.txt` in each release (sha256).

## Primary vs mirror

Primary distribution is <https://vxcloud.io/download/>, served from the `vxcloud_web` build.
This repo is the mirror, published by `vxcloud_web/distribute.{ps1,sh}` via `gh release`.
Binaries are Release assets only — never committed to git.
