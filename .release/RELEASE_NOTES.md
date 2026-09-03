# Evrima Companion v0.9.20.40 — Public Tester Bootstrap

This package is the temporary public bootstrap for Evrima Companion.

> [!IMPORTANT]
> **v0.9.20.40 is not the current Stable Companion.** After the first launch, go to **Updates → Check for updates** and install the newest Stable version before testing. Current Stable: **v0.9.20.48**.

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
- Party/Friends location and selected vitals sharing.
- Phone/tablet Second Screen over the local network.
- Built-in private bug reports and reply threads.
- Multiple interface languages and appearance settings.
- Optional privacy-minimised technical telemetry.

OCR is currently disabled in Stable because current map/location and Prime functionality uses the working non-OCR live location path.

## Optional telemetry

Telemetry is off by default. If enabled, it helps us see how Companion works across different PCs, which features are being used and where technical problems may be happening during public testing.

It does not intentionally include map coordinates, screenshots, Steam/EOS identity, Party messages or personal files. The current payload can be inspected inside Companion before enabling it.

## Windows security

The tester build is currently unsigned. SmartScreen or Smart App Control may warn or block it depending on the Windows configuration.

Using Windows **Unblock** does not disable Defender, SmartScreen or Smart App Control. Do not disable Windows security protections solely to run Companion.

## Reporting bugs

If Companion opens, use the built-in **Report Bug** page whenever possible. If the bootstrap fails before Companion can open, see `SUPPORT.md` in the repository.

## Checksum

A SHA-256 checksum file is provided as a separate Release asset.

Evrima Companion is an unofficial fan-made utility and is **not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle**.
