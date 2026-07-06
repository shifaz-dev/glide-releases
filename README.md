# Glide — Offline Speech-to-Text

Press a shortcut, speak, and your words are typed into whatever app you're using —
**fully on your own computer**, no cloud, no account, no data leaving your machine.

### → [**Download the latest version**](../../releases/latest)

Once installed, Glide **updates itself automatically**.

**Jump to:** [Install](#install) · [How it works](#how-it-works) ·
[Setup](#first-time-setup) · [Using Glide](#using-glide) ·
[Choosing a model](#choosing-a-model) · [Settings](#settings-explained)

---

## Install

Grab the file for your system from the [latest release](../../releases/latest).
`x64` / `amd64` = Intel/AMD chips · `arm64` / `aarch64` = ARM chips (Apple
Silicon, ARM laptops).

| OS | Download | Notes |
|---|---|---|
| 🐧 **Linux** | `…_amd64.AppImage` (any distro), or `.deb` / `.rpm` | AppImage: `chmod +x` then run |
| 🍎 **macOS** | `.dmg` — `x64` (Intel) or `aarch64` (Apple Silicon) | First launch: right-click → **Open** (not yet notarized) |
| 🪟 **Windows** | `…-setup.exe` or `.msi` — `x64` or `arm64` | SmartScreen → **More info** → **Run anyway** (not yet signed) |

---

## How it works

When you hold your shortcut and talk, Glide:

1. **Records** audio from your microphone
2. **Trims silence** with voice-activity detection
3. **Transcribes** the speech to text using a local AI model on your own CPU/GPU
   (with GPU acceleration when available)
4. **Types the text** into whatever app currently has focus

Everything happens locally — your voice never leaves your device, and it works
with no internet connection.

---

## First-time setup

1. **Grant permissions.** Glide needs your **microphone**. On **macOS** it also
   needs **Accessibility** permission so it can type into other apps (System
   Settings → Privacy & Security → Accessibility).
2. **Download a model.** On first launch Glide asks you to pick a transcription
   model and downloads it (see [Choosing a model](#choosing-a-model)). Models are
   a few hundred MB to a couple GB and download once.
3. **Set your shortcut** (Settings → the *Shortcut* card) — the key you hold to talk.

---

## Using Glide

- **Hold** your shortcut, **speak**, then **release** → your words are typed at the
  cursor.
- Glide lives in your **system tray / menu bar**. Open its window any time to change
  settings; it keeps running in the background.
- **Push-to-Talk** (hold to record, release to stop) is the default. Turn it off for
  **toggle mode** (press once to start, again to stop).

---

## Choosing a model

The **model** is the AI that turns your speech into text. Glide offers many, and
they trade off three things:

| | Meaning |
|---|---|
| **Accuracy score** | How correct the transcription is (higher = better) |
| **Speed score** | How fast it transcribes (higher = faster, lighter on your PC) |
| **Size** | Download size + memory use |

In the app, each model shows its **accuracy** and **speed** score. General guidance:

- **Newer / faster computer** → pick a **higher-accuracy** model.
- **Older / slower computer** → pick a **higher-speed** model.
- **English only?** → **Parakeet** models are English-focused with great accuracy
  *and* speed — a strong default.
- **Other / mixed languages?** → **Whisper** models are multilingual.
- **Very low-end machine?** → tiny **Moonshine** models are extremely fast (lower
  accuracy).

Download several and switch any time from the **Model** card — no re-setup. Wrong
too often? Pick a higher-accuracy model. Feels slow? Pick a faster one.

---

## Settings explained

| Setting | What it does |
|---|---|
| **Shortcut** | The key you hold (or toggle) to record. |
| **Push To Talk** | Hold to record, release to stop. Off = press-once-to-start / press-again-to-stop. |
| **Model** | Which AI transcribes your speech (see above). |
| **Microphone** | Which input device to listen to. |
| **Paste automatically** | Whether Glide types the text into the active app. Off = it's only copied and you paste it yourself. |
| **Auto-submit** | Presses **Enter** after pasting — handy for chat boxes and search bars. |
| **Language** | The language you're speaking, to help the model. |
| **Translate to English** | Translates other languages into English as it transcribes. |
| **Voice Activity Detection** | Ignores silence so pauses aren't transcribed as noise. |
| **Mute While Recording** | Mutes system audio while you dictate. |
| **Keep Mic Open** | Holds the mic open ~30s between transcriptions for faster back-to-back use (may affect Bluetooth quality). |
| **Append Trailing Space** | Adds a space after each pasted transcription. |
| **Audio Feedback / Sound Theme** | Play a sound when recording starts and stops. |
| **Custom Words** | Teach Glide names / terms / jargon it keeps mishearing. |
| **History** | Review and re-copy your past transcriptions. |

Most people only set the **shortcut**, pick a **model**, and choose their
**microphone** — the rest have sensible defaults.

---

## Updates & safety

Glide checks for new versions and updates itself in place — you only download it
once. Every build is **cryptographically signed**, and the app verifies that
signature before installing any update, so updates can't be tampered with or
spoofed.

This repository hosts Glide's release builds and the auto-update manifest
(`latest.json`).
