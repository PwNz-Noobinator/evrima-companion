<div align="center">

# Evrima Companion

**A Windows companion app for The Isle: Evrima — live map tools, server browser, Survival Vitals, Prime Tracker, Party/Friends and Second Screen.**

[![Public Tester](https://img.shields.io/badge/Public%20Tester-v0.9.20.40-orange?style=flat-square)](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)
[![Stable](https://img.shields.io/badge/Stable-v0.9.20.48-brightgreen?style=flat-square)](https://github.com/PwNz-Noobinator/evrima-companion)
[![Platform](https://img.shields.io/badge/platform-Windows-0078d4?style=flat-square&logo=windows)](https://github.com/PwNz-Noobinator/evrima-companion)
[![Downloads](https://img.shields.io/github/downloads/PwNz-Noobinator/evrima-companion/total?style=flat-square&label=release%20downloads)](https://github.com/PwNz-Noobinator/evrima-companion/releases)

**[Download](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)** · **[Feature guides](#feature-guides)** · **[Changelog](CHANGELOG.md)** · **[Support](docs/SUPPORT.md)** · **[Privacy](PRIVACY.md)**

</div>

> [!CAUTION]
> ### Update after your first launch
> The GitHub download is the **v0.9.20.40 bootstrap**. The current Stable version is **v0.9.20.48**.
>
> After Companion opens, go to **Updates → Check for updates** and install the newest Stable version before testing. Do not evaluate or report current Companion behaviour while still on v0.9.20.40.

Evrima Companion brings the tools you are likely to want while playing **The Isle: Evrima** into one application. It is currently in public testing and is an unofficial fan-made project.

## What it does

| Feature | What it does |
|---|---|
| **Server Browser** | Browse Official and Unofficial Evrima servers with search, filters, favourites, ping and player counts. |
| **Dinosaur Profiles** | Keep per-server dinosaur details, growth, location, mutations, notes and Prime ETA when available. |
| **Live Map** | Desktop Gateway map with automatic live location, manual coordinates, waypoints, sizing and opacity controls. |
| **Survival Vitals** | Compact Health, Growth, Food and Water HUD that follows the active dinosaur. |
| **Prime Tracker** | Track Sanctuary, Migration, Mass Migration and Patrol visits and estimate growth ETA. |
| **Dinosaur Life Memory** | Development builds track a dinosaur life across sessions with active playtime, last-known state/location, crash-safe recovery and history. |
| **Party / Friends** | Share live positions, trails, markers and selected Survival Vitals with your group. |
| **Second Screen** | Put the live Companion map on a phone or tablet over your local Wi-Fi/LAN. |
| **Bug Reports** | Private in-app reports with acknowledgements, developer replies and tester follow-ups. |
| **Languages & Appearance** | Multiple interface languages and configurable UI accent colour. |

## Screenshots

### In-game overlays
[![Evrima Companion map overlay and Survival Vitals](docs/screenshots/evrima-companion-gameplay.png)](docs/screenshots/evrima-companion-gameplay.png)

### Server browser & dinosaur profile
[![Evrima Companion server browser and dinosaur profile](docs/screenshots/evrima-companion-servers.png)](docs/screenshots/evrima-companion-servers.png)

### Map controls
[![Evrima Companion map controls](docs/screenshots/evrima-companion-map.png)](docs/screenshots/evrima-companion-map.png)

## Download & install

**[Download Evrima Companion v0.9.20.40 — Public Tester](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)**

1. Download `Evrima-Companion-v0.9.20.40-Public-Tester.zip` from the release Assets.
2. Before extracting, right-click the ZIP → **Properties**. If Windows shows **Unblock**, tick it and click **Apply**.
3. Extract the entire ZIP.
4. Run **`BUILD AND INSTALL EVRIMA COMPANION.cmd`**.
5. Wait for the local build and installation to finish.
6. When Companion opens, go to **Updates → Check for updates** and install the newest Stable version.
7. Confirm you are no longer running v0.9.20.40 before testing.

**Python is not required.** The bootstrap contains its own private build runtime.

### Requirements

- 64-bit Windows
- The Isle: Evrima for game-linked features
- A local network connection for Second Screen

## Current Stable — v0.9.20.48

The current Stable line includes Prime Tracker, Survival Vitals, live non-OCR Asset Location tracking, Party/Friends improvements, Second Screen, growth ETA, private bug-report conversations and telemetry identity repair.

OCR is currently **disabled and locked off** in Stable because the current live location and Prime paths no longer depend on it.

See the [changelog](CHANGELOG.md) for version-by-version details.

## Development candidate — v0.9.20.50

v0.9.20.50 is the current development candidate. It carries forward the v0.9.20.49 persistence and Dinosaur Life Memory work, then adds a substantial UI/UX redesign focused on making Companion feel less blocky and less like a QA/debug interface.

The redesign replaces the old top-heavy tab layout with a left navigation rail, opens up page structure, reduces unnecessary boxed/card treatment, improves spacing and control hierarchy, rewrites technical player-facing copy, corrects the custom title-bar controls so they use the existing stone-bezel artwork cleanly, and fixes default-size clipping in the Server Browser/Dinosaur Profile layout and Map controls.

The public GitHub bootstrap remains v0.9.20.40 and the current Supabase Stable channel remains v0.9.20.48 until v0.9.20.50 is explicitly published there.

## Optional telemetry

Telemetry is **off by default**.

If you enable it, it helps us see how Evrima Companion is working on different PCs, which features are being used and where problems may be happening during public testing. That makes it easier to find issues that might otherwise go unnoticed and decide what needs attention.

It does **not** intentionally collect your map location, screenshots, Steam/EOS account, Party messages or personal files. You can use **View exactly what is collected** before enabling it and turn telemetry off at any time.

From v0.9.20.48, telemetry uses a dedicated random per-machine installation UUID that is separate from Party/Friends identity. See [PRIVACY.md](PRIVACY.md) for the full technical details and retention periods.

## Feature guides

- [Live Map & Location Tools](docs/MAP.md)
- [Survival Vitals](docs/SURVIVAL_VITALS.md)
- [Prime Tracker](docs/PRIME_TRACKER.md)
- [Party / Friends](docs/PARTY.md)
- [Second Screen](docs/SECOND_SCREEN.md)
- [Frequently Asked Questions](docs/FAQ.md)

## Updates

Installed Companion builds use the **Supabase Stable** update channel. Update packages are integrity-checked before installation.

The public v0.9.20.40 bootstrap predates newer required-update behaviour, so its first update may appear as a normal update rather than blocking use. **Accept the update to the newest Stable version.** Once on a newer Stable build, the current updater behaviour applies.

## Reporting problems

If Companion opens, use the built-in **Report Bug** page whenever possible. It creates a private project report and gives you a `BUG-XXXXXXXX` reference for replies and follow-up.

If the app cannot open or the bootstrap itself fails, see [Support](docs/SUPPORT.md).

Feature ideas can be posted through GitHub Discussions. Keep security-sensitive information, private diagnostics, passwords and tokens out of public issues or discussions.

## Windows security

Current tester builds are not yet signed with the project's future trusted code-signing certificate. SmartScreen or Smart App Control may therefore warn or block the software depending on the Windows configuration.

Using **Unblock** on the downloaded ZIP does not disable Windows security protections. Do not disable Defender, SmartScreen or Smart App Control solely to run Companion. See [Tester build guide](docs/TESTER_BUILD.md).

## Project information

- [Public testing changelog](CHANGELOG.md)
- [Tester build guide](docs/TESTER_BUILD.md)
- [Support](docs/SUPPORT.md)
- [Privacy](PRIVACY.md)
- [Security](SECURITY.md)
- [Third-party notices](docs/THIRD_PARTY_NOTICES.md)
- [Licence](LICENSE)

Evrima Companion is proprietary freeware for personal, non-commercial use under the repository [LICENSE](LICENSE). Third-party components retain their own licences and terms.

Evrima Companion is an unofficial fan-made utility and is **not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle**.
