<div align="center">

# 💥 SlapBook

### *Slap your MacBook. Watch it shatter. Hear it scream.*

A macOS menu bar app that listens to your MacBook's built-in accelerometer —
the moment it detects a slap, it shatters your screen and reacts like **Talking Tom** on a bad day.

[![macOS 13+](https://img.shields.io/badge/macOS-13%2B-black?style=for-the-badge&logo=apple)](https://www.apple.com/macos/)
[![Swift 5.9](https://img.shields.io/badge/Swift-5.9-orange?style=for-the-badge&logo=swift)](https://swift.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-green?style=for-the-badge)]()
```
   you: *slap*
   MacBook: 😱 "MY SCREEN! MY BEAUTIFUL SCREEN!"
            💥 [shatters dramatically]
```

</div>

---

## ✨ Features

| Feature | Description |
|--------|-------------|
| 🪨 **Accelerometer Detection** | Reads your MacBook's Sudden Motion Sensor at 60Hz — no battery drain |
| 💥 **Procedural Crack Rendering** | Every shatter is unique: random impacts, branching cracks, LCD bleed lines |
| 🎙️ **Talking Tom Voice Reactions** | 24 unique voice lines across 4 intensity levels |
| 🔊 **Sound Effects** | Layered impact sounds matching slap intensity |
| 🖥️ **Multi-Display** | Shatters ALL connected screens simultaneously |
| 📊 **Slap Counter** | Tracks your destruction in the menu bar |
| ⚙️ **Preferences** | Sensitivity slider + voice reaction toggle |

---

## 🎭 Intensity Levels

| Level | Trigger | Reaction |
|-------|---------|----------|
| 😮 Light | Gentle tap | *"Excuse me?!"* |
| 😱 Medium | Real slap | *"MY SCREEN! MY BEAUTIFUL SCREEN!"* |
| 🤯 Hard | Aggressive thump | *"I AM CALLING THE LAPTOP POLICE."* |
| 💀 Legendary | Full commit | *"MY ANCESTORS ARE SCREAMING."* |

---

## 🚀 Install
```bash
git clone https://github.com/YOUR_USERNAME/slapbook.git
cd slapbook
bash install.sh
```

> Requires macOS 13+ and Xcode Command Line Tools.
> Don't have them? Run `xcode-select --install` first.

---

## 🗑️ Uninstall
```bash
rm -rf /Applications/SlapBook.app
launchctl unload ~/Library/LaunchAgents/com.slapbook.app.plist
rm ~/Library/LaunchAgents/com.slapbook.app.plist
```

---

## ⌨️ Apple Silicon / No Accelerometer?

SlapBook auto-detects and falls back to a keyboard shortcut:
```
Shift + Ctrl + S → trigger manually
```

---

## 📁 Structure
```
slapbook/
├── install.sh
└── SlapBook/
    ├── Package.swift
    └── Sources/SlapBook/
        ├── main.swift
        ├── AppDelegate.swift
        ├── SlapDetector.swift
        ├── SoundEngine.swift
        ├── OverlayWindowController.swift
        └── PreferencesWindowController.swift
```

---

## 📄 License

MIT — go wild. Just don't actually break your MacBook.

---

<div align="center">

Made with 💥 and questionable judgment

**Star this repo** if it made you laugh ⭐

</div>
```

---

## 🚀 First Commit Message
```
🚀 init: SlapBook v1.0 — slap your Mac, shatter the screen, Talking Tom reacts
```

---

## 🏷️ Release Title & Tag
```
Tag:    v1.0.0
Title:  💥 SlapBook v1.0 — First Shatter
```

**Release notes:**
```
## What's new
- 🪨 Accelerometer slap detection via IOKit (60Hz)
- 💥 Procedural cracked screen with 4 intensity levels
- 🎙️ 24 Talking Tom-style voice reactions
- 🔊 Layered system sound effects
- 🖥️ Multi-display support
- 📊 Slap counter in menu bar
- ⚙️ Sensitivity slider + sound toggle
- 🚀 One-line bash installer
- ⌨️ Keyboard fallback for Apple Silicon (Shift+Ctrl+S)
```

---

## 🐦 Launch Tweet
```
just shipped SlapBook 💥

slap your MacBook → broken screen effect + Talking Tom screams at you

built in Swift, zero deps, one-line install

github.com/YOUR_USERNAME/slapbook

#Swift #macOS #OpenSource #buildinpublic
```

---

## 🐱 Product Hunt
**Tagline:**
```
Slap your MacBook. Watch it shatter. Hear it scream.
```
**Description:**
```
SlapBook is a tiny macOS menu bar app that uses your MacBook's built-in accelerometer to detect slaps. Hit it and you get: a full-screen procedural cracked glass effect, Talking Tom-style voice reactions (24 phrases across 4 intensity levels), layered sound effects, and a slap counter. Free, open source, zero dependencies.
