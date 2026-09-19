# Evrima Companion v0.9.20.40 — Public Tester Bootstrap

This package is the temporary public bootstrap for Evrima Companion.

> [!IMPORTANT]
> **v0.9.20.40 is not the current Stable Companion.** After the first launch, go to **Updates → Check for updates** and install the newest Stable version before testing. Current Stable: **v0.9.20.55**.

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
- Dinosaur Guide with quick-reference diet, growth and species information plus offline reference data.
- Live desktop Gateway map and waypoints.
- Survival Vitals HUD for Health, Growth, Food and Water.
- Prime Tracker with zone progress and growth ETA.
- Persistent Dinosaur Life Memory, active playtime, life history and last-known state/location recovery.
- Party/Friends location, selected vitals and shared-pin support.
- Phone/tablet Second Screen with Map, Dinosaur and Party views over the local network.
- Built-in private bug reports and reply threads.
- Multiple interface languages and appearance settings.
- Optional privacy-minimised technical telemetry.
- Persistent map/navigation tools, Companion hotkeys, Quick Bar with selectable Health/Food/Water and other live information, and sortable Server Browser columns.
- Optional Growth/Prime milestone and low Food/Water notifications.
- Optional uninstall feedback and telemetry-retention/deletion choice during uninstall.

OCR is currently disabled in Stable because current map/location and Prime functionality uses the working non-OCR live location path.

## Current Stable — v0.9.20.55

v0.9.20.55 expands the **Quick Bar** so it can show live **Health, Food and Water** alongside its existing selectable information.

The map sidebar visibility option now hides only the sidebar and no longer causes the map itself to close or become unable to reopen.

Map breadcrumb/trail history now resets when Companion confirms a dinosaur life has ended because of death/respawn or a dinosaur change, so a new life starts with a clean trail.

## Optional telemetry

Telemetry is off by default. If enabled, it helps us see how Companion works across different PCs, which features are being used and where technical problems may be happening during public testing.

It does not intentionally include map coordinates, screenshots, Steam/EOS identity, Party messages or personal files. Optional error telemetry is limited to coarse feature/error categories, and v0.9.20.54 avoids treating expected background Party reconnect/network outcomes as application errors. The current payload can be inspected inside Companion before enabling it.

## Windows security

The tester build is currently unsigned. SmartScreen or Smart App Control may warn or block it depending on the Windows configuration.

Using Windows **Unblock** does not disable Defender, SmartScreen or Smart App Control. Do not disable Windows security protections solely to run Companion.

## Reporting bugs

If Companion opens, use the built-in **Report Bug** page whenever possible. If the bootstrap fails before Companion can open, see `docs/SUPPORT.md` in the repository.

## Checksum

A SHA-256 checksum file is provided as a separate Release asset.

Evrima Companion is an unofficial fan-made utility and is **not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle**.
