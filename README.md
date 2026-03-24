<div align="center">


# 💥 SlapBook

### *Slap your MacBook. Watch it shatter. Hear it scream.*

A macOS menu bar app that listens to your MacBook's built-in accelerometer —
the moment it detects a slap, it shatters your screen and reacts like **Talking Tom** on a bad day.

<br>

[![macOS 13+](https://img.shields.io/badge/macOS-13%2B-black?style=for-the-badge&logo=apple)](https://www.apple.com/macos/)
[![Swift 5.9](https://img.shields.io/badge/Swift-5.9-orange?style=for-the-badge&logo=swift)](https://swift.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-green?style=for-the-badge)]()

<br>

```
   you: *slap*

   MacBook: 😱 "MY SCREEN! MY BEAUTIFUL SCREEN!"
            💥 [shatters dramatically]
```

<br>

</div>

---

## ✨ What It Does

| Feature | Description |
|--------|-------------|
| 🪨 **Accelerometer Detection** | Reads your MacBook's Sudden Motion Sensor at 60Hz — no battery drain |
| 💥 **Procedural Crack Rendering** | Every shatter is unique: random impact points, branching cracks, shatter polygons, LCD bleed lines |
| 🎙️ **Talking Tom Voice Reactions** | 24 unique voice lines across 4 intensity levels — the harder the slap, the more unhinged the reaction |
| 🔊 **System Sound Effects** | Layered impact sounds that match slap intensity |
| 🖥️ **Multi-Display** | Shatters ALL connected screens simultaneously |
| 🎚️ **4 Intensity Levels** | Light tap to legendary bonk — each triggers different cracks + different reactions |
| 📊 **Slap Counter** | Tracks your destruction in the menu bar |
| ⚙️ **Preferences** | Adjustable sensitivity slider + toggle voice reactions |

---

## 🎭 Reaction Levels

| Intensity | Trigger | Visual | Voice Reaction |
|-----------|---------|--------|----------------|
| 😮 **Light** | Gentle tap | 1 impact point, thin cracks | *"Excuse me?!"* / *"Rude!"* |
| 😱 **Medium** | Real slap | 1–2 impacts, branching cracks | *"MY SCREEN! MY BEAUTIFUL SCREEN!"* |
| 🤯 **Hard** | Aggressive thump | 2–3 impacts, dense shattering | *"I AM CALLING THE LAPTOP POLICE."* |
| 💀 **Legendary** | Full commit | 3–5 impacts, color distortion, full chaos | *"MY ANCESTORS ARE SCREAMING."* |

---

## 🚀 Install

### One-line install (recommended)

```bash
git clone https://github.com/YOUR_USERNAME/slapbook.git && cd slapbook && bash install.sh
```

That's it. The script will:
- ✅ Check Swift + macOS version
- ✅ Build the app in release mode
- ✅ Install to `/Applications/SlapBook.app`
- ✅ Optionally launch at login
- ✅ Launch immediately

> **Requires:** macOS 13 Ventura or later · Xcode Command Line Tools

Install Xcode CLI tools if you haven't:
```bash
xcode-select --install
```

### Manual build

```bash
cd SlapBook
swift build -c release
.build/release/SlapBook
```

---

## 🗑️ Uninstall

```bash
rm -rf /Applications/SlapBook.app
# Remove auto-start (if enabled):
launchctl unload ~/Library/LaunchAgents/com.slapbook.app.plist
rm ~/Library/LaunchAgents/com.slapbook.app.plist
```

---

## 🏗️ How It Works

```
MacBook Accelerometer (IOKit, ~60Hz)
           │
           ▼
    SlapDetector.swift
    ┌──────────────────────────────┐
    │  Read x/y/z acceleration     │
    │  Δmagnitude > threshold?     │
    │  Map delta → SlapIntensity   │
    └──────────────┬───────────────┘
                   │ .light / .medium / .hard / .legendary
                   ▼
         AppDelegate.handleSlap()
         ┌────────────────────────┐
         │  Update slap counter   │
         │  Animate menu icon     │
         └────────┬───────────────┘
          ┌───────┴───────────┐
          ▼                   ▼
   SoundEngine.swift    OverlayWindowController.swift
   ┌──────────────┐     ┌──────────────────────────────┐
   │ Impact sound │     │ CrackOverlayView (CoreGraphics)│
   │ TTS reaction │     │  • Radial branching cracks    │
   │ 24 phrases   │     │  • Shatter polygons           │
   └──────────────┘     │  • LCD bleed lines            │
                        │  • Color distortion (legendary)│
                        │  • Screen shake animation     │
                        │  • Emoji + text reaction label│
                        └──────────────────────────────┘
                                    │
                            click or timeout
                                    │
                                 Dismiss
```

---

## 📁 Project Structure

```
slapbook/
├── install.sh                          ← One-command installer
├── README.md
└── SlapBook/
    ├── Package.swift
    ├── Resources/
    │   └── Info.plist
    └── Sources/SlapBook/
        ├── main.swift                  ← Entry point
        ├── AppDelegate.swift           ← Menu bar + orchestration
        ├── SlapDetector.swift          ← IOKit SMS accelerometer polling
        ├── SoundEngine.swift           ← Talking Tom voice reactions
        ├── OverlayWindowController.swift ← Cracked screen renderer
        └── PreferencesWindowController.swift
```

---

## ⚠️ Apple Silicon Note

Apple Silicon Macs need a private entitlement to access SMS directly. SlapBook **automatically falls back** to a keyboard shortcut:

```
Shift + Ctrl + S  →  trigger the effect manually
```

For a fully signed build with SMS on Apple Silicon, see the [entitlements guide](docs/entitlements.md).

---

## 🤝 Contributing

PRs welcome! Some ideas if you want to contribute:

- [ ] More voice reaction lines
- [ ] Custom sound file support
- [ ] Animated emoji face overlay (actual Talking Tom style)
- [ ] Haptic feedback via Taptic Engine
- [ ] Sparkle auto-updater integration
- [ ] App icon `.icns`

---

## 📄 License

MIT — go wild. Just don't actually break your MacBook.

---

<div align="center">

Made with 💥 and questionable judgment

**[⭐ Star this repo](https://github.com/YOUR_USERNAME/slapbook)** if it made you laugh

</div>
