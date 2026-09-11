# Evrima Companion v0.9.20.40 — Public Tester Bootstrap

This package is the temporary public bootstrap for Evrima Companion.

> [!IMPORTANT]
> **v0.9.20.40 is not the current Stable Companion.** After the first launch, go to **Updates → Check for updates** and install the newest Stable version before testing. Current Stable: **v0.9.20.53**.

## Install

1. Download `Evrima-Companion-v0.9.20.40-Public-Tester.zip` from the Assets section.
2. Before extracting, right-click the ZIP → **Properties**. If Windows shows **Unblock**, tick it and click **Apply**.
3. Extract the entire ZIP.
4. Run **`BUILD AND INSTALL EVRIMA COMPANION.cmd`**.
5. Wait for the local build and installation to finish.
6. Open **Updates → Check for updates** in Companion and install the newest Stable version.

**Python is not required.** The tester ZIP contains its own private build runtime.

## What Companion includes

Current Stable builds include:

- Official and Unofficial Evrima server browser.
- Saved dinosaur profiles.
- Live desktop Gateway map and waypoints.
- Survival Vitals HUD for Health, Growth, Food and Water.
- Prime Tracker with zone progress and growth ETA.
- Persistent Dinosaur Life Memory, active playtime, life history and last-known state/location recovery.
- Party/Friends location, selected vitals and shared-pin support.
- Phone/tablet Second Screen with Map, Dinosaur and Party views over the local network.
- Built-in private bug reports and reply threads.
- Multiple interface languages and appearance settings.
- Optional privacy-minimised technical telemetry.
- Persistent map/navigation tools, Companion hotkeys, Quick Bar and sortable Server Browser columns.
- Optional uninstall feedback and telemetry-retention/deletion choice during uninstall.

OCR is currently disabled in Stable because current map/location and Prime functionality uses the working non-OCR live location path.

## Current Stable — v0.9.20.53

v0.9.20.53 expands Party/Friends and Second Screen.

Second Screen now provides dedicated Map, Dinosaur and Party views with live dinosaur information, Party positions, saved/shared pins and navigation controls. Players can navigate to Party members, receive optional separation warnings, share Party pins and preserve Party state across Companion restarts until they deliberately leave or disband.

The release also adds privacy-safe optional error telemetry using coarse feature/error categories only. During uninstall, players can optionally submit a reason and, when telemetry exists, choose whether to keep the existing technical usage history or request its deletion. Retained telemetry is marked inactive rather than appearing as a current installation.

## Optional telemetry

Telemetry is off by default. If enabled, it helps us see how Companion works across different PCs, which features are being used and where technical problems may be happening during public testing.

It does not intentionally include map coordinates, screenshots, Steam/EOS identity, Party messages or personal files. v0.9.20.53 also limits optional error telemetry to coarse feature/error categories. The current payload can be inspected inside Companion before enabling it.

## Windows security

The tester build is currently unsigned. SmartScreen or Smart App Control may warn or block it depending on the Windows configuration.

Using Windows **Unblock** does not disable Defender, SmartScreen or Smart App Control. Do not disable Windows security protections solely to run Companion.

## Reporting bugs

If Companion opens, use the built-in **Report Bug** page whenever possible. If the bootstrap fails before Companion can open, see `docs/SUPPORT.md` in the repository.

## Checksum

A SHA-256 checksum file is provided as a separate Release asset.

Evrima Companion is an unofficial fan-made utility and is **not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle**.
