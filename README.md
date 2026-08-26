# Evrima Companion

**Unofficial companion utility for The Isle: Evrima.**

Evrima Companion is a Windows desktop app providing server browsing, per-server dinosaur information, map/overlay tools, automatic location OCR, Survival Vitals, a phone/tablet Second Screen, Party/Friend markers, automatic updates and built-in bug reporting.

> **Pre-release project:** Evrima Companion is still in public testing. A public `1.0` release has not been declared and compatibility has not been certified across every Windows version or PC configuration.

## Current public-testing distribution

During the current testing phase, GitHub is being used as the **initial tester entry point**, while normal Companion application updates continue to be delivered through the existing **Supabase update channel**.

The temporary GitHub tester download is planned as a **ZIP build kit**, not a prebuilt unsigned Companion installer. The tester extracts the ZIP and runs the supplied Build/Start launcher. The kit builds the normal Companion installer locally on that Windows PC, then the normal installer installs Companion, creates the desktop shortcut and launches the application.

This is a temporary testing arrangement while trusted code signing for the normal downloadable installer is prepared. The long-term plan remains a normal prebuilt, signed Windows installer.

See [TESTER_BUILD.md](TESTER_BUILD.md) for the complete tester workflow and Windows security notes.

## Download

Use only the **GitHub Releases** page belonging to this repository.

For the temporary public-testing phase:

- download the official Evrima Companion tester ZIP;
- extract the whole ZIP before running anything;
- double-click the supplied Build/Start Companion launcher;
- allow it to build the normal installer locally;
- continue through the normal Companion install flow.

Do not download Evrima Companion from third-party mirrors or repackaged copies.

## Windows security notice

Current tester builds are not yet signed with the project's future trusted code-signing certificate.

Microsoft Defender SmartScreen may warn about unknown unsigned software, and Windows 11 Smart App Control may block unknown unsigned code when Windows cannot establish that it is safe. The temporary local-build package is intended to improve tester accessibility based on the project's testing experience, but it **does not guarantee that SmartScreen or Smart App Control will allow the result to run**.

Do **not** disable Smart App Control, Microsoft Defender, SmartScreen or other Windows security protections solely to run Evrima Companion. If Windows blocks the tester build with no normal permitted continuation path, stop and report the exact message instead.

A User Account Control (UAC) elevation prompt is separate from SmartScreen and Smart App Control.

More detail: [TESTER_BUILD.md](TESTER_BUILD.md).

## Main features in v0.9.20.40

### Server and dinosaur tools

- Browse both official and unofficial Evrima servers.
- View per-server dinosaur profiles and save useful dinosaur information.
- Read-only detection of matching Evrima Prelobby/current-character data where available.
- Automatic active character/server detection from live TempData activity for Survival Vitals.
- Corrected profile health data based on probe-verified TempData interpretation.

### Survival Vitals

- Automatic TempData-based **Health, Growth, Food and Water** monitoring without needing the in-game Tab/Status Report OCR path.
- Compact frameless Survival Vitals HUD.
- Persistent **Lock / Unlock** control:
  - locked = fixed in place and mouse click-through;
  - unlocked = interactive and draggable, including while Evrima is running.
- Remembers window position, size and lock state between sessions.
- Resizable while unlocked.
- Manual **Refresh** control.
- **Close** control with the ability to reopen Survival Vitals from Companion controls.
- Failed or partial TempData reads are retried instead of permanently stalling the vitals feed.
- Existing vitals cards update in place rather than rebuilding the whole HUD every refresh.
- Solo vitals use with optional Party/Friends sharing support where enabled.

### Map and overlay

- Vulnona Map Overlay integration.
- Desktop map can be closed independently without closing Evrima Companion.
- Same-session automatic overlay relaunch is suppressed after a deliberate close until the user explicitly reopens it or The Isle restarts.
- Saved waypoints.
- Separate local-player and Party/Friend marker trails.
- Overlay controls and persistent user positioning/settings.
- Improved overlay process relaunch handling and launch diagnostics.

### Automatic location OCR

- Automatic map-location OCR from the in-game Status Report.
- OCR capture is calculated from the actual Evrima game-client resolution.
- Normally captures only the Asset Location region instead of an entire high-resolution monitor frame.
- Native capture resources and temporary OCR images are released/cleaned after use.
- Manual location entry remains available as a permanent fallback.

### Second Screen and Party/Friends

- Second Screen map for a phone or tablet on the same local network.
- Can be used alongside the desktop overlay or as the separate map display while Companion is running.
- Party/Friend realtime markers and separate marker trails.
- PC-to-phone Second Screen synchronisation remains local-network based.

### Updates and recovery

- Automatic update checking.
- Installed tester updates currently come through the **Supabase Stable** release channel.
- Update packages are checked against expected SHA-256 and byte-size metadata before installation.
- Existing dual-source update-discovery capability is retained for the future signed GitHub-distribution path, but Supabase is the active tester update source during the temporary build-kit phase.
- Existing rollback/recovery behaviour is retained.

### Bug reporting and diagnostics

- Built-in bug reporter returning `BUG-XXXXXXXX` references.
- Optional sanitized diagnostic attachment that can be previewed before submission.
- Low-frequency Companion resource diagnostics for investigating game/performance/VRAM-related reports without continuous heavy telemetry.
- Overlay diagnostics are reset per launch session to reduce stale-error confusion.

### UI and project quality-of-life

- Persistent Companion settings used by map/overlay and Survival Vitals controls.
- Numeric update-download progress retained without the old global dinosaur progress animation.
- Eevee29 Runner and Kassia easter eggs operate independently.
- Public freeware licence, privacy information, Credits and third-party licence documentation are included with the project.

## Changes added since this GitHub repository opened

This repository was created on **24 August 2026**. User-facing development continued immediately afterward:

- **v0.9.20.35** — added verified dual-source update discovery, checksum/size verification for GitHub-compatible updates, and expanded public licence/privacy/Credits documentation.
- **v0.9.20.36** — allowed the desktop map to be deliberately closed without closing Companion and prevented unwanted immediate relaunch.
- **v0.9.20.37** — restored the Eevee29 Runner easter egg and separated it from the Kassia easter egg logic.
- **v0.9.20.38** — introduced Survival Vitals with TempData-based Health, Growth, Food and Water monitoring plus active character/server detection.
- **v0.9.20.39** — redesigned Survival Vitals as a compact HUD, improved OCR capture efficiency, reduced duplicate background polling, added resource diagnostics and hardened overlay relaunch diagnostics.
- **v0.9.20.40** — added persistent vitals Lock/Unlock, resizing, saved geometry, Refresh and Close controls, plus automatic retry/recovery when a TempData read fails part-way through a game write.

See [CHANGELOG.md](CHANGELOG.md) for the concise public testing history.

## Basic use

1. Download and extract the current official tester ZIP from GitHub Releases.
2. Run its Build/Start Companion launcher.
3. The locally built normal installer installs Evrima Companion and creates the desktop shortcut.
4. Use **Servers** to browse Evrima servers and view/save dinosaur information.
5. Use **Map** for overlay controls, automatic/manual location, waypoints, Party/Friends and Second Screen.
6. Use **Survival Vitals** for the current local character's available vitals data.
7. Use **Report Bug** inside the Companion if something fails or behaves incorrectly.

## Updates

The GitHub tester package is only the initial installation route during this temporary phase.

After Companion is installed, normal tester updates are delivered through the project's existing **Supabase release channel**. Testers should not need to rebuild Companion for routine application updates.

The application's existing updater code may retain support for other release sources for future signed-public-release work, but Supabase is the active tester update path for this phase.

## Bug reports

Please use the **Report Bug** page inside Evrima Companion whenever possible. A successful submission returns a `BUG-XXXXXXXX` reference.

The diagnostic attachment is optional and can be previewed before submission. Do not type passwords, account credentials, private keys or other secrets into a bug report.

If the application or tester build cannot start far enough to use its Report Bug page, see [SUPPORT.md](SUPPORT.md).

## Privacy

Second Screen PC-to-phone synchronisation stays on the user's local network. Optional/network features can contact Supabase, GitHub, VulnonaMAP and public/session-discovery infrastructure used by Evrima.

See [PRIVACY.md](PRIVACY.md) for the project's data-use and privacy information.

## Licence and temporary build-kit source

Evrima Companion's project-owned application/code/assets are **proprietary freeware**. Official unmodified builds may be used for personal, non-commercial use under the supplied licence.

The documentation repository itself is not intended to become the project's normal public source-code repository. During the temporary local-build testing phase, however, an official tester **release asset may contain the project-owned source/build inputs required to build that specific unmodified tester version locally**. Their inclusion for local building does not grant permission to redistribute modified versions or override the supplied proprietary licence.

Third-party software keeps the rights granted by its own licence. See [LICENSE](LICENSE), [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) and the [licence index](licenses/README.md).

## Qt / PySide6 LGPL compliance

Qt/PySide components remain subject to their own LGPL terms regardless of the Companion's proprietary project-owned licence. Public tester packages and installed builds must continue to preserve the replacement/relinking and source-availability rights required by the applicable third-party licences.

The Companion does not intentionally ship modified Qt/PySide library source, and the proprietary application licence does not restrict rights granted by LGPLv3 for LGPL-covered libraries.

## Testing status

The project currently has a small QA/tester group and this temporary GitHub tester package is intended to widen testing before the signed public installer is ready.

Untested combinations are not presented as certified. Please report reproducible problems through the in-app bug reporter whenever possible.

## Third-party projects

Evrima Companion integrates with, redistributes separately, or acknowledges projects including Vulnona Map Overlay, VulnonaMAP, Qt/PySide6, Python, Requests, websocket-client, python-qrcode/Pillow, PresentMon and GameDig. The exact relationship and licence for each is documented in the third-party notices.

## Unofficial project

Evrima Companion is a fan-made utility. It is **not affiliated with, sponsored by, or endorsed by Afterthought LLC or the developers/publishers of The Isle**.

The Isle and all third-party names/trademarks remain the property of their respective owners.
