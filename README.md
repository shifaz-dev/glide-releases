# Glide — Offline Speech-to-Text

Press a shortcut, speak, and your words are typed into whatever app you're using —
**fully on your own computer**, no cloud, no account, no data leaving your machine.

### → [**Download the latest version**](../../releases/latest)

Once installed, Glide **updates itself automatically**.

---

## How it works

When you hold your shortcut and talk, Glide:

1. **Records** audio from your microphone
2. **Trims silence** with voice-activity detection
3. **Transcribes** the speech to text using a local AI model running on your own
   CPU/GPU (with GPU acceleration when available)
4. **Types the text** into whatever app currently has focus

Everything happens locally — your voice never leaves your device.

---

## First-time setup

1. **Grant permissions.** Glide needs your **microphone**. On **macOS** it also
   needs **Accessibility** permission so it can type into other apps (System
   Settings → Privacy & Security → Accessibility).
2. **Download a model.** On first launch Glide asks you to pick a transcription
   model and downloads it (see [Choosing a model](#choosing-a-model)). Models are
   a few hundred MB to a couple GB and download once.
3. **Set your shortcut** (Settings → the *Shortcut* card). This is the key you'll
   hold to talk.

That's it — you're ready.

---

## Using Glide

- **Hold** your shortcut, **speak**, then **release** → your words are typed at the
  cursor.
- Glide lives in your **system tray/menu bar**. Open its window any time to change
  settings; it keeps running in the background.
- **Push-to-Talk** (hold to record, release to stop) is the default. You can turn
  it off to use **toggle mode** instead (press once to start, again to stop).

---

## Choosing a model

The **model** is the AI that turns your speech into text. Glide offers many, and
they trade off three things:

| | Meaning |
|---|---|
| **Accuracy score** | How correct the transcription is (higher = better) |
| **Speed score** | How fast it transcribes (higher = faster, lighter on your PC) |
| **Size** | Download size + memory use |

In the app, each model shows its **accuracy** and **speed** score so you can
compare at a glance. General guidance:

- **Newer / faster computer** → pick a **higher-accuracy** model.
- **Older / slower computer** → pick a **higher-speed** model (transcription
  finishes quicker, uses less memory).
- **English only?** → the **Parakeet** models are English-focused and give great
  accuracy *and* speed — a strong default.
- **Other languages / mixed languages?** → the **Whisper** models are
  multilingual.
- **Very low-end machine?** → the tiny **Moonshine** models are extremely fast
  (with somewhat lower accuracy).

You can download several and switch between them any time from the **Model** card —
no re-setup needed. If a transcription is wrong too often, try a higher-accuracy
model; if it feels slow, try a faster one.

---

## Key settings explained

| Setting | What it does |
|---|---|
| **Shortcut** | The key you hold (or toggle) to record. |
| **Push To Talk** | Hold to record, release to stop. Turn off for press-once-to-start / press-again-to-stop. |
| **Model** | Which AI transcribes your speech (see above). |
| **Microphone** | Which input device to listen to. |
| **Paste automatically** | Whether Glide types the text into the active app for you. Off = it's only copied, and you paste it yourself. |
| **Auto-submit** | Presses **Enter** after pasting — handy for chat boxes and search bars. |
| **Language** | The language you're speaking, to help the model. |
| **Translate to English** | Automatically translates other languages into English as it transcribes. |
| **Voice Activity Detection** | Automatically ignores silence so pauses aren't transcribed as noise. |
| **Mute While Recording** | Mutes your system audio while you're dictating. |
| **Keep Mic Open** | Holds the mic open ~30s between transcriptions for faster back-to-back use (may affect Bluetooth audio quality). |
| **Append Trailing Space** | Adds a space after each pasted transcription. |
| **Audio Feedback / Sound Theme** | Play a sound when recording starts and stops. |
| **Custom Words** | Teach Glide names/terms/jargon it keeps mishearing. |
| **History** | Review (and re-copy) your past transcriptions. |

Most people only ever set the **shortcut**, pick a **model**, and choose their
**microphone** — the rest have sensible defaults.

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
   "unidentified developer" prompt because Glide isn't notarized yet — expected;
   you only confirm once.

### 🪟 Windows
1. Download **`…-setup.exe`** (recommended) or the **`.msi`**. Choose `x64` for
   most PCs, `arm64` for ARM devices.
2. Run it. **SmartScreen** may warn "unknown publisher" → **More info** → **Run
   anyway**. Expected, since the build isn't code-signed yet.

---

## Updates & safety

Glide checks for new versions and updates itself in place — you only download it
once. Every build is **cryptographically signed**, and the app verifies that
signature before installing any update, so updates can't be tampered with or
spoofed.

This repository hosts Glide's release builds and the auto-update manifest
(`latest.json`).
