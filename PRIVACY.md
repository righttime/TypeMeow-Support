# TypeMeow Privacy Policy

**Last updated: July 2026**

## Overview

TypeMeow ("the App") is a macOS menu bar application that tracks your typing speed and displays an animated animal companion. Your privacy is fundamental to this app's design — not an afterthought.

## What We Collect

**Nothing.**

More specifically:

| Data Type | Collected? | Details |
|-----------|------------|---------|
| Keystroke content (what you type) | ❌ Never | The app never reads, stores, or transmits the characters you type |
| Key codes (which key) | ❌ Not stored | Raw key codes are counted in-memory only, never persisted |
| Active application name | ❌ Never | The app does not know which app you are typing in |
| Typing speed (KPM) | ⚠️ Local only | Keystrokes Per Minute is calculated in-memory and optionally saved to a local stats file on your Mac |
| Daily/weekly averages | ⚠️ Local only | Stored in `~/Library/Application Support/TypeMeow/.noindex/stats.json` — on your Mac only, never transmitted |
| App preferences | ⚠️ Local only | Stored in macOS UserDefaults (`com.fotogrammer.TypeMeow`) — on your Mac only |
| Crash reports | ❌ None | No crash reporting framework is included |
| Analytics / telemetry | ❌ None | No analytics SDK, no usage tracking |
| Device information | ❌ None | No device fingerprinting |

## Network Activity

**The App makes zero network calls.** There is no server, no cloud service, no API endpoint, no analytics backend. The App functions 100% offline.

You can verify this yourself using any network monitoring tool (e.g., Little Snitch, Lulu, or Activity Monitor's Network tab) — TypeMeow will show zero connections.

## Data Storage

All data is stored locally on your Mac:

| Data | Location | Purpose |
|------|----------|---------|
| Typing statistics | `~/Library/Application Support/TypeMeow/.noindex/stats.json` | Daily/weekly KPM averages |
| Preferences | `~/Library/Preferences/com.fotogrammer.TypeMeow.plist` | App settings |
| Placeholder images | `~/Library/Application Support/TypeMeow/.placeholder/` | Generated fallback images |

The `.noindex` directory ensures statistics are excluded from Spotlight indexing. The stats file is created with `0600` permissions (owner read/write only) and includes a SHA-256 checksum for integrity verification.

## Permissions

The App requires one macOS permission:

- **Input Monitoring** — Required to count keystrokes globally (across all applications). This permission is granted by you in System Settings → Privacy & Security → Input Monitoring. The App uses this permission **solely to count key events** — it never reads key content.

## Data Deletion

You can delete all stored data at any time:

1. **In-app**: Settings → Data tab → "Delete Statistics…"
2. **Manual**: Delete `~/Library/Application Support/TypeMeow/`
3. **Full reset**: Run `defaults delete com.fotogrammer.TypeMeow`

The in-app deletion performs a secure 1-pass random overwrite before unlinking the file.

## Children's Privacy

The App does not knowingly collect any data from anyone, including children under 13.

## Changes to This Policy

If this policy changes, the updated version will be posted here with a revised "Last updated" date. Since the App collects no data and makes no network calls, significant changes are unlikely.

## Contact

For privacy concerns or questions:
- 📧 [Open an Issue](https://github.com/righttime/TypeMeow-Support/issues)

---

*Your typing is yours. That's not a slogan — it's the architecture.*
