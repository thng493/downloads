<div align="center">

# vxcloud downloads

### Official downloads &amp; release mirror for **vxcloud** — the AI multi‑cloud platform

Get the **vxcli** CLI, the **vxcloud Desktop** app, the **web build**, and the
**browser extension** — checksum‑verified, free, and **no account required**.

[![Latest release](https://img.shields.io/github/v/release/prodxcloud/downloads?sort=date&label=latest&color=6f42c1)](https://github.com/prodxcloud/downloads/releases)
[![Total downloads](https://img.shields.io/github/downloads/prodxcloud/downloads/total?color=2ea44f)](https://github.com/prodxcloud/downloads/releases)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Website](https://img.shields.io/badge/website-vxcloud.io-0a7ea4)](https://vxcloud.io)

[**Website**](https://vxcloud.io) · [**Download page**](https://vxcloud.io/download) · [**Docs**](https://vxcloud.io/docs) · [**All releases**](https://github.com/prodxcloud/downloads/releases)

</div>

---

## What is this?

This repository is the **canonical download mirror** for [vxcloud](https://vxcloud.io) —
an AI‑driven multi‑cloud platform for provisioning infrastructure, deploying apps over
SSH, and running governed AI agents across **AWS, Azure, GCP, and private clouds**.

Every official build is published here as a **GitHub Release**, so you can always grab a
**direct, checksum‑verified download** even if `vxcloud.io` is unavailable. It mirrors:

| Product | What it is | Latest download |
|---|---|---|
| 🖥️ **vxcli** | The multi‑cloud command‑line tool (Linux · macOS · Windows, amd64 + arm64) | [vxcli releases →](https://github.com/prodxcloud/downloads/releases?q=vxcli) |
| 💻 **vxcloud Desktop** | The vxcloud AI assistant as a native desktop app (Windows · macOS) | [desktop releases →](https://github.com/prodxcloud/downloads/releases?q=vxcloud-desktop) |
| 🧩 **Browser extension** | "vxcomputer Companion" — a side‑panel agent that drives your browser (Chrome · Firefox) | [extension releases →](https://github.com/prodxcloud/downloads/releases?q=vxcomputer-extension) |
| 🌐 **Web build** | The complete static site, for self‑hosting a vxcloud mirror | [web releases →](https://github.com/prodxcloud/downloads/releases?q=web) |

> 👉 Most users should install from the official site: **<https://vxcloud.io/download>**.
> This repo is the **fallback / direct‑link mirror** and the source of truth for checksums.

---

## ⬇️ Install

### vxcli — the multi‑cloud CLI

One line, no package manager, checksum‑verified, installs to your user dir (no `sudo`):

```bash
# macOS / Linux
curl -fsSL https://vxcloud.io/download/cli/install.sh | sh
```

```powershell
# Windows (PowerShell 5.1+)
irm https://vxcloud.io/download/cli/install.ps1 | iex
```

Then check it:

```bash
vxcli version
```

**Prefer a direct binary?** Grab one from the latest
[`vxcli-*` release](https://github.com/prodxcloud/downloads/releases?q=vxcli) — e.g.:

```
.../releases/download/vxcli-<version>/vxcli_<version>_linux_amd64
.../releases/download/vxcli-<version>/vxcli_<version>_darwin_arm64
.../releases/download/vxcli-<version>/vxcli_<version>_windows_amd64.exe
```

`chmod +x` the file and move it onto your `PATH` (it answers to `vxcli`, `vx`, or `vxcloud`).

### vxcloud Desktop

Download the installer from the latest
[`vxcloud-desktop-*` release](https://github.com/prodxcloud/downloads/releases?q=vxcloud-desktop)
or from **<https://vxcloud.io/download/desktop>**:

- **Windows** — `vxcloud-desktop-<version>-x64-setup.exe` (per‑user, no admin).
  First run is unsigned → click **More info → Run anyway**.
- **macOS** — `.dmg` (Apple Silicon &amp; Intel). Unsigned → right‑click → **Open**.

### Browser extension (vxcomputer Companion)

Download `vxcomputer-companion-<version>.zip` from the latest
[`vxcomputer-extension-*` release](https://github.com/prodxcloud/downloads/releases?q=vxcomputer-extension), then:

1. **Chrome / Edge** — unzip, open `chrome://extensions`, enable **Developer mode**,
   click **Load unpacked**, and select the folder.
2. **Firefox** — open `about:debugging` → **This Firefox** → **Load Temporary Add‑on**.

### Web build (self‑host a mirror)

```bash
# Download + extract the full static site, then serve it with any static host:
curl -fsSLO https://github.com/prodxcloud/downloads/releases/download/web-<version>/vxcloud-web-<version>.tar.gz
mkdir vxcloud-site && tar -xzf vxcloud-web-<version>.tar.gz -C vxcloud-site
npx serve vxcloud-site      # or nginx / S3 / any CDN
```

---

## ✅ Verify your download

Every release ships a `checksums.txt` (SHA‑256). Verify before you run anything:

```bash
# macOS / Linux
sha256sum -c checksums.txt            # or: shasum -a 256 -c checksums.txt
```

```powershell
# Windows
Get-FileHash .\vxcli_<version>_windows_amd64.exe -Algorithm SHA256
# compare the hash against the line in checksums.txt
```

---

## 🛟 Why a separate downloads repo?

So a download **always works** — even during an incident. `vxcloud.io` is the primary
origin (CDN), but if the site or its object storage is ever unreachable, GitHub Releases
is an **independent failure domain** with no bandwidth caps, giving every user a stable,
direct, integrity‑checked link. Binaries are **release assets only** — never committed to
git — so clones stay tiny.

## 🔢 Versioning

Releases use **per‑product tags** so one repo can hold everything cleanly:

| Tag pattern | Example |
|---|---|
| `vxcli-<version>` | `vxcli-2026.6.13-1516` |
| `vxcloud-desktop-<version>` | `vxcloud-desktop-2026.6.13-1516` |
| `web-<version>` | `web-2026.6.13-1516` |
| `vxcomputer-extension-<extversion>` | `vxcomputer-extension-1.2.3` |

vxcli, desktop, and the web build share one **date‑stamped** version (`YYYY.M.D-HHMM`)
that tracks the vxcloud node release, so you can tell which builds belong together. The
browser extension keeps its own Chrome‑valid semver.

---

## 🔗 Links

- 🌐 **Website** — <https://vxcloud.io>
- ⬇️ **Download page** — <https://vxcloud.io/download>
- 📚 **Documentation** — <https://vxcloud.io/docs>
- 🏢 **prodxcloud** — <https://prodxcloud.com>
- 🐙 **All releases** — <https://github.com/prodxcloud/downloads/releases>

---

## 📄 License

The contents of **this repository** (README, layout, release metadata) are released under
the [MIT License](LICENSE).

The downloadable **products** (vxcli, vxcloud Desktop, the browser extension, and the web
build) are part of the vxcloud platform and provided for use with vxcloud; their use is
governed by the vxcloud terms at <https://vxcloud.io>.

<div align="center">

© 2026 Joel O. Wembo · [prodxcloud](https://prodxcloud.com) — made for builders shipping to every cloud ☁️

</div>
