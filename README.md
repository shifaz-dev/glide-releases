# Glide — Downloads

**Offline speech-to-text for your desktop.** Press a shortcut, speak, and your
words are typed into whatever app you're using — fully on-device, no cloud, no
account.

### → [**Download the latest version**](../../releases/latest)

Once installed, Glide **updates itself automatically** — it checks for new
releases and installs them in place, so you only need to download it once.

---

## Install

Pick the file for your system on the [latest release](../../releases/latest).
`x64` / `amd64` = Intel/AMD chips · `arm64` / `aarch64` = ARM chips (Apple
Silicon, ARM laptops).

### 🐧 Linux
- **AppImage** (`…_amd64.AppImage`) — works on **any** distribution. Recommended.
  ```bash
  chmod +x Glide_*_amd64.AppImage
  ./Glide_*_amd64.AppImage
  ```
- **`.deb`** — Debian / Ubuntu / Mint (`sudo apt install ./Glide_*.deb`)
- **`.rpm`** — Fedora / RHEL / openSUSE (`sudo dnf install ./Glide-*.rpm`)

### 🍎 macOS
1. Download the **`.dmg`** for your chip (`x64` = Intel, `aarch64` = Apple Silicon).
2. Open it and drag **Glide** into Applications.
3. **First launch:** right-click Glide → **Open** → **Open**. macOS shows an
   "unidentified developer" prompt because Glide isn't notarized yet — this is
   expected; you only confirm once.

### 🪟 Windows
1. Download **`…-setup.exe`** (recommended) or the **`.msi`**. Choose `x64` for
   most PCs, `arm64` for ARM devices.
2. Run it. **SmartScreen** may warn "unknown publisher" → click **More info** →
   **Run anyway**. Expected, since the build isn't code-signed yet.

---

## Is it safe?

Every download is **cryptographically signed** with Glide's private key (the
`.sig` files), and the app verifies that signature before installing any update —
so updates can't be tampered with or spoofed.

This repository hosts Glide's release builds and the auto-update manifest
(`latest.json`).
