<div align="center">

# Evrima Companion

**The Isle: Evrima companion app for Windows — server browser, map/OCR tools, dinosaur tracking, Party/Friends, Survival Vitals and Second Screen.**

[![Public Tester](https://img.shields.io/badge/Public%20Tester-v0.9.20.40-orange?style=flat-square)](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)
[![Platform](https://img.shields.io/badge/platform-Windows-0078d4?style=flat-square&logo=windows)](https://github.com/PwNz-Noobinator/evrima-companion)
[![Downloads](https://img.shields.io/github/downloads/PwNz-Noobinator/evrima-companion/total?style=flat-square&label=release%20downloads)](https://github.com/PwNz-Noobinator/evrima-companion/releases)

**[Download the public tester](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)** · **[Changelog](CHANGELOG.md)** · **[Tester guide](TESTER_BUILD.md)** · **[Support](SUPPORT.md)** · **[Privacy](PRIVACY.md)**

</div>

---

Evrima Companion is an unofficial Windows companion utility for **The Isle: Evrima**. It combines an Evrima server browser, dinosaur profiles, a desktop map overlay, automatic location OCR, live Party/Friends tracking, Survival Vitals and a phone/tablet Second Screen map in one app.

**Current public GitHub tester/bootstrap: v0.9.20.40.** Installed testers receive normal application updates through the **Supabase Stable** channel, so the large GitHub bootstrap ZIP does not need to be rebuilt for every application update.

> [!IMPORTANT]
> **Check for updates immediately after installing.** The GitHub download is the v0.9.20.40 bootstrap and may not be the newest Companion build. After Companion opens for the first time, go to **Updates → Check for updates** and install the newest Stable version before testing or using Companion. **Current Stable: v0.9.20.43.**

**Current Stable: v0.9.20.43.** It adds standalone map lifecycle improvements, optional Prime Tracker full-growth ETA in Survival Vitals and Party data, startup notifications for normal Stable updates, persistent telemetry consent with privacy-minimised feature-use events, locked resolved/closed bug-report threads and stronger emergency-rollback safeguards. The public GitHub bootstrap remains v0.9.20.40 until there is a reason to replace the bootstrap kit itself.

## Quick feature overview

| Feature | What it does |
|---|---|
| **Server Browser** | Browse Official and Unofficial Evrima servers with search, filters, favourites, ping and player counts. |
| **Dinosaur Profiles** | Save dinosaur, growth, location, sex, mutations and notes per server, with Prime full-growth ETA when enabled and available. |
| **Map Overlay** | Desktop Vulnona map overlay with OCR location updates, manual coordinates, waypoints, opacity and size controls; it can stay open after The Isle exits. |
| **Party / Friends** | Share live positions, individual trails, markers and selected Survival Vitals with your group, including optional Prime full-growth ETA. |
| **Survival Vitals** | Compact HUD for Health, Growth, Food and Water with automatic active-character detection and optional Prime full-growth ETA. |
| **Second Screen** | Use a phone or tablet as a live Companion map over your local Wi-Fi/LAN. |
| **Prime Tracker** | Automatic Sanctuary/Migration/Patrol visit tracking plus growth-rate and full-growth ETA estimates. |
| **Bug Report Threads** | Automatic acknowledgement, developer replies and tester follow-ups attached to one `BUG-XXXXXXXX`; resolved/closed threads are read-only. |
| **Optional Telemetry** | Opt-in, inspectable compatibility and content-free feature-use telemetry; consent persists across normal updates. |
| **Languages & Appearance** | Multiple interface languages plus configurable UI accent colour. |
| **Graphics / Optimiser** | Experimental work remains in development; the WIP tabs are kept disabled/hidden in normal tester use. |

---

## Download & install

**[Download Evrima Companion v0.9.20.40 — Public Tester](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)**

The GitHub tester package is the **initial installation route**. Once Companion is installed, routine updates are delivered through the **Supabase Stable update channel**.

1. Download **`Evrima-Companion-v0.9.20.40-Public-Tester.zip`** from the release Assets.
2. **Before extracting it**, right-click the downloaded ZIP → **Properties**. If Windows shows **Unblock**, tick it and click **Apply**.
3. Extract the entire ZIP to a normal folder.
4. Double-click **`BUILD AND INSTALL EVRIMA COMPANION.cmd`**.
5. Wait while the normal Companion executable is built locally and the install process starts automatically.
6. **Important:** when Companion opens, go to **Updates → Check for updates** and install the newest Stable version before you start testing or using it.

> [!IMPORTANT]
> **Do not assume the version in the GitHub ZIP is the newest version.** GitHub provides the bootstrap installer; normal Companion releases are delivered through the built-in Stable updater.

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
- Where Evrima provides the data, Companion can automatically read the current dinosaur's **growth, health, hunger and thirst** from the game's normal local character data.
- When Prime Tracker is enabled and enough growth samples are available, Dinosaur Profiles can show an estimated ETA to **100% growth**.
- Favourite servers for quick access later.
- **Launch The Isle** from Companion. Companion does not claim to bypass EOS/session handling to directly join a selected server.

### Map & automatic location

- Integrated **Vulnona Map Overlay** for the desktop.
- Press **Tab in-game** and Companion can automatically read your Asset Location and update the map.
- Manual coordinates remain available as a fallback.
- Lock/unlock the map, choose its size and adjust its opacity.
- Optionally open the map automatically with The Isle.
- The desktop map can remain open and usable after The Isle exits; it closes only when you close it or Companion explicitly shuts it down.
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
- Party members can optionally see each other's dinosaur, server, Health, Growth, Food and Water in Survival Vitals.
- When Prime Tracker is enabled and an estimate is available, Party vitals can also carry a bounded **full-growth ETA** without adding coordinates, Party codes, server names, dinosaur names or other new identity/location data to that ETA payload.

### Survival Vitals

Survival Vitals is a separate compact HUD that follows the character you are currently playing.

- Shows **Health, Growth, Food and Water** without requiring Tab/OCR.
- Automatically follows the active dinosaur/server as Evrima writes its local character data.
- Works **solo**, or can display Party/Friends' shared vitals alongside your own.
- With Prime Tracker enabled, local and Party cards can optionally show an estimated ETA to **100% growth** when enough growth data exists.
- Lock it to make it fixed and mouse click-through while playing.
- Unlock it to move or resize it, including while The Isle is running.
- Remembers position, size and lock state.
- Includes manual **Refresh** and **Close** controls and can be reopened from Companion.
- Failed/partial character-data reads are retried automatically instead of leaving the HUD permanently stuck.

### Prime Tracker — v0.9.20.43 Stable

Prime Tracker uses the same live Gateway coordinates already used by the map rather than creating a second location system.

- Tracks unique **Sanctuary**, **Migration**, **Mass Migration** and **Patrol Zone** visits for the current dinosaur life.
- A zone does not need to be active at the moment of the visit; Companion tracks known places where that zone can occur.
- Checks the movement segment between consecutive location samples, so a zone crossed between two Tab/location readings can still be detected.
- Keeps per-life progress across normal restarts and provides a manual **Reset current Prime run** fallback.
- Keeps conditions that cannot be inferred from available local data as explicit manual objectives.
- Measures observed growth change over time and estimates ETA to **75%** and **100%** growth.
- v0.9.20.43 can surface the **100% growth ETA** in Dinosaur Profiles, local Survival Vitals and Party Survival Vitals when Prime Tracker is enabled.
- Shows brief click-through progress notifications when automatic objectives are detected.
- Refreshes Prime zone geometry from VulnonaMAP when available and falls back to a bundled Gateway snapshot if the live refresh cannot be reached.

Prime rules are game/community data and may change with game patches; the game remains authoritative.

### Second Screen phone/tablet map

- Start the phone map from Companion and connect using the displayed **QR code**.
- Runs over your **local Wi-Fi/LAN**.
- Works while the desktop overlay is open or independently of the desktop overlay.
- Receives your latest map position and displays Party/Friend markers and trails.

### Bug reports, acknowledgements & replies — v0.9.20.43 Stable

The built-in bug reporter uses private project reports rather than requiring testers to post diagnostics publicly.

- Every successful submission gets a `BUG-XXXXXXXX` reference.
- New reports receive an automatic **received** acknowledgement.
- **My reports & replies** shows report status and the conversation attached to that report.
- Developers can reply to the exact report, and the tester can answer inside the same thread instead of opening another bug report just to continue the conversation.
- Each report has a private random local reply key. The backend stores only its hash, so knowing another person's report number alone is not enough to read or post to their thread.
- Once a report is marked **resolved** or **closed**, the tester reply controls are disabled and the backend rejects further tester replies to that thread.
- Developer replies cannot silently pull screenshots, files or new diagnostics from the PC.

See [SUPPORT.md](SUPPORT.md) for reporting guidance.

### Optional technical telemetry — v0.9.20.43 Stable

Telemetry is **off by default** and requires an explicit user choice.

When enabled, Companion can submit privacy-minimised compatibility data such as Companion version, Windows version/build, CPU/GPU models, installed RAM, display resolution/scaling, language and known game resolution, plus short bounded technical events.

v0.9.20.43 stores telemetry consent independently from ordinary UI settings, so normal application updates do **not** ask again. A new consent prompt is required only if the telemetry consent-policy version changes.

When telemetry is enabled, Companion can also submit coarse **feature-use events** for areas such as the map overlay, automatic map-location path, Party, Survival Vitals and Second Screen. These events are intentionally content-free: they do not include map coordinates, Party codes, server names, dinosaur names or user-entered content.

The Settings page includes **View exactly what is collected**, so the current technical payload can be inspected directly. Companion telemetry does not intentionally include names, Windows usernames, Steam/EOS identity, computer names, map coordinates, Party codes, screenshots/OCR images, personal files or hardware serial numbers.

Raw telemetry events are retained for **90 days** and stale installation summaries for **365 days**. Turning telemetry off stops future telemetry submissions. See [PRIVACY.md](PRIVACY.md) for the complete data-use description.

### Languages & appearance

The Companion currently includes:

**English, Estonian, Finnish, Swedish, German, French, Spanish, Polish, Dutch, Portuguese, Italian, Norwegian and Danish.**

You can also change the Companion's UI accent colour from Settings.

### Graphics & performance tools — WIP

Graphics/Optimiser work is not treated as a finished public feature. The WIP tabs are deliberately kept **disabled/hidden** in normal tester use while those tools are developed and validated. Their underlying development code is retained for future work.

### Updates

- Built-in automatic update checking.
- During this tester phase, installed Companion updates are delivered through the **Supabase Stable update channel**.
- Update files are integrity-checked before installation.
- v0.9.20.43 checks for a newer Stable release during normal startup and can prompt for an ordinary update without making it mandatory; normal updates include a **Not now** path.
- Releases explicitly marked mandatory by the Stable channel still use the required-update flow.
- Emergency rollback handling requires explicit rollback lineage in Stable metadata rather than treating an arbitrary newer QA candidate as a rollback target.

The already-published v0.9.20.40 bootstrap predates the newer blocking required-update UI, so its first hop to a newer mandatory build still uses the older update-confirmation behaviour. Once a user is on a client containing the newer logic, future mandatory updates can be presented as required before normal app use continues.

---

## Windows security notice

Current tester builds are not yet signed with the project's future trusted code-signing certificate. Microsoft Defender SmartScreen may display a reputation warning, and Windows 11 Smart App Control may block unknown unsigned code.

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
