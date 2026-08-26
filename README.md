<div align="center">

# Evrima Companion

**The Isle: Evrima companion app for Windows — server browser, map overlay, dinosaur tracking, Party/Friends, Survival Vitals and Second Screen.**

[![Public Tester](https://img.shields.io/badge/Public%20Tester-v0.9.20.40-orange?style=flat-square)](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)
[![Platform](https://img.shields.io/badge/platform-Windows-0078d4?style=flat-square&logo=windows)](https://github.com/PwNz-Noobinator/evrima-companion)
[![Downloads](https://img.shields.io/github/downloads/PwNz-Noobinator/evrima-companion/total?style=flat-square&label=release%20downloads)](https://github.com/PwNz-Noobinator/evrima-companion/releases)

**[Download the public tester](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)** · **[Changelog](CHANGELOG.md)** · **[Tester guide](TESTER_BUILD.md)** · **[Support](SUPPORT.md)**

</div>

---

Evrima Companion is an unofficial Windows companion utility for **The Isle: Evrima**. It combines an Evrima server browser, dinosaur profiles, a desktop map overlay, automatic location OCR, live Party/Friends tracking, Survival Vitals and a phone/tablet Second Screen map in one app.

**Current public tester: v0.9.20.40** — pre-release software while a normal digitally signed installer is being prepared.

## Quick feature overview

| Feature | What it does |
|---|---|
| **Server Browser** | Browse Official and Unofficial Evrima servers with search, filters, favourites, ping and player counts. |
| **Dinosaur Profiles** | Save dinosaur, growth, location, sex, mutations and notes per server. |
| **Map Overlay** | Desktop Vulnona map overlay with OCR location updates, manual coordinates, waypoints, opacity and resize controls. |
| **Party / Friends** | Share live positions, individual trails, markers and selected Survival Vitals with your group. |
| **Survival Vitals** | Compact HUD for Health, Growth, Food and Water with automatic active-character detection. |
| **Second Screen** | Use a phone or tablet as a live Companion map over your local Wi-Fi/LAN. |
| **Languages & Appearance** | Multiple interface languages plus configurable UI accent colour. |
| **Updates & Bug Reports** | Built-in update checking, integrity verification and `BUG-XXXXXXXX` report references. |
| **Graphics / Optimiser** | Experimental performance and configuration tools currently marked **Work In Progress**. |

---

## Download & install

**[Download Evrima Companion v0.9.20.40 — Public Tester](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)**

The GitHub tester package is the **initial installation route**. Once Companion is installed, normal app updates are delivered automatically through the **Supabase Stable update channel**, so testers do not need to rebuild the app for every update.

1. Download **`Evrima-Companion-v0.9.20.40-Public-Tester.zip`** from the release Assets.
2. **Before extracting it**, right-click the downloaded ZIP → **Properties**. If Windows shows **Unblock**, tick it and click **Apply**.
3. Extract the entire ZIP to a normal folder.
4. Double-click **`BUILD AND INSTALL EVRIMA COMPANION.cmd`**.
5. Wait while the normal Companion executable is built locally and the install process starts automatically.

**Python is not required.** The tester package includes its own private build runtime.

If you already extracted the ZIP and Windows refuses to run the launcher, check **Properties** on the original ZIP or the blocked launcher for **Unblock**, use it if shown, then extract/run again.

### Requirements

- **64-bit Windows**.
- **The Isle: Evrima** for game-linked features.
- A local network connection if you want to use **Second Screen** on a phone or tablet.
- No separate Python installation is required.

---

## Features in detail

### Servers & dinosaur profiles

- Browse **Official** and **Unofficial** Evrima servers.
- Search by server name and filter by **region**, **full/empty servers** and **favourites**.
- See player count, ping, region, map and server version.
- Save a dinosaur profile for each server, including dinosaur, growth, location, sex, mutations and notes.
- Where Evrima provides the data, Companion can automatically read the current dinosaur's **growth, health, hunger and thirst** from the game's local character data.
- Favourite servers for quick access later.
- Launch The Isle directly from Companion.

### Map & automatic location

- Integrated **Vulnona Map Overlay** for the desktop.
- Press **Tab in-game** and Companion can automatically read your Asset Location and update the map.
- Manual coordinates are always available as a fallback.
- Lock/unlock the map, change its size and adjust its opacity.
- Optionally start/stop the map automatically with The Isle.
- Close the map without closing Companion and reopen it whenever you want.
- Save, edit, delete and copy **waypoints**.
- Choose your own local marker colour.

### Party / Friends

Create a Party code and give it to your friends, or join somebody else's Party.

- See Party members' **live map locations**.
- See separate trails for each player.
- Choose your display name, trail colour and marker symbol.
- Control how much location history is shown.
- Turn your own location sharing on or off.
- Party markers work on both the **desktop map** and **Second Screen phone/tablet map**.
- **Survival Vitals can also be shared with the Party**, letting Party members see each other's dinosaur, server, Health, Growth, Food and Water in the Survival Vitals window.

### Survival Vitals

Survival Vitals is a separate compact HUD that follows the character you are currently playing.

- Shows **Health, Growth, Food and Water** without needing to press Tab or use OCR.
- Automatically follows the active dinosaur/server as Evrima writes its character data.
- Works completely **solo**, or can display **your Party/Friends' shared vitals alongside your own**.
- Each Party row shows the player's name, dinosaur, server and how recently Evrima updated the snapshot.
- Lock it to make it fixed and mouse click-through while playing.
- Unlock it to move or resize it, even while The Isle is running.
- Remembers its position, size and lock state.
- Includes manual **Refresh** and **Close** controls and can be reopened from Companion.
- Failed/partial character-data reads are retried automatically instead of leaving the HUD permanently stuck.

### Second Screen phone/tablet map

Use a phone or tablet as another Companion map screen while you play.

- Start the phone map from Companion and connect using the displayed **QR code**.
- Runs over your **local Wi-Fi/LAN**.
- Works while the desktop overlay is open or completely independently of the desktop overlay.
- Receives your latest map position.
- Displays Party/Friend markers and trails as well.

### Languages & appearance

The Companion currently includes:

**English, Estonian, Finnish, Swedish, German, French, Spanish, Polish, Dutch, Portuguese, Italian, Norwegian and Danish.**

You can also change the Companion's UI accent colour from Settings.

### Graphics & performance tools — WIP

These tools are included for testing but are still marked **Work In Progress**:

- Detect The Isle's graphics configuration.
- Save/restore known setups and create backups.
- Adaptive performance mode with configurable target and priority.
- PresentMon integration and performance telemetry tools.

They should not be treated as finished/certified optimisation features yet.

### Updates & bug reporting

- Built-in automatic update checking.
- During this tester phase, installed Companion updates are delivered through the **Supabase Stable update channel**.
- Update files are integrity-checked before installation.
- Built-in **Report Bug** page with `BUG-XXXXXXXX` report numbers.
- Optional sanitized diagnostics help diagnose problems without requiring testers to hunt through log folders manually.

---

## Windows security notice

Current tester builds are not yet signed with the project's future trusted code-signing certificate. Microsoft Defender SmartScreen may still display a reputation warning, and Windows 11 Smart App Control may still block unknown unsigned code.

Using Windows' **Unblock** option only removes the downloaded-file mark from the file you intentionally downloaded; it does not disable Defender, SmartScreen or Smart App Control.

The local-build tester package is **not guaranteed to bypass Windows security controls**. Do not disable Smart App Control, Defender or SmartScreen solely to run Companion. If Windows blocks it without offering a normal continuation option, report the exact message so it can be investigated.

See [TESTER_BUILD.md](TESTER_BUILD.md) for more detail.

---

## Reporting problems

Whenever Companion opens normally, please use its built-in **Report Bug** page. If Companion cannot start or the tester package itself fails, see [SUPPORT.md](SUPPORT.md).

## Project links

- [Releases](https://github.com/PwNz-Noobinator/evrima-companion/releases)
- [Public testing changelog](CHANGELOG.md)
- [Tester build instructions](TESTER_BUILD.md)
- [Support](SUPPORT.md)
- [Privacy](PRIVACY.md)
- [Licence](LICENSE)
- [Third-party notices](THIRD_PARTY_NOTICES.md)

---

Evrima Companion is proprietary freeware for personal, non-commercial use. Third-party components remain under their own licences.

**Evrima Companion is an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.**
