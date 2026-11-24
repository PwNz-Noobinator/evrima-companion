# Evrima Companion v0.9.20.40 — Public Tester Bootstrap

This package is the temporary public bootstrap for Evrima Companion.

> [!IMPORTANT]
> **v0.9.20.40 is not the current Stable Companion.** After the first launch, go to **Updates → Check for updates** and install the newest Stable version before testing. Current Stable: **v0.9.20.64**.

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

- Redesigned interface with expandable sidebar menus, focused Map and Settings tabs, and clearer layouts inside each page.

- Official and Unofficial Evrima server browser.
- Saved dinosaur profiles.
- Dinosaur Guide with quick-reference diet, growth and species information plus offline reference data.
- Live desktop Gateway map and waypoints.
- Survival Vitals HUD for Health, Growth, Food and Water.
- Prime Tracker with zone progress and growth ETA.
- Persistent Dinosaur Life Memory, active playtime, life history and last-known state/location recovery.
- Party location, selected vitals and shared-pin support.
- Optional Companion accounts with persistent sign-in, recovery words and account management.
- Online Friends with friend requests, blocking, online presence, Invisible Mode and privacy-controlled server/dinosaur sharing.
- Beta programme applications, username reporting and private privacy enquiries.
- Phone/tablet Second Screen with Map, Dinosaur and Party views over the local network.
- Built-in private bug reports and reply threads.
- Multiple interface languages and appearance settings.
- Optional privacy-minimised technical telemetry.
- Persistent map/navigation tools, Companion hotkeys, a top-centred click-through Quick Bar with selectable Health/Food/Water and other live information, and sortable Server Browser columns.
- Optional Growth/Prime milestone and low Food/Water notifications.
- Optional uninstall feedback and telemetry-retention/deletion choice during uninstall.

OCR is currently disabled in Stable because current map/location and Prime functionality uses the working non-OCR live location path.

## Current Stable — v0.9.20.64

**v0.9.20.64 is available through Companion's built-in Stable update channel.**

This release brings together the compatibility improvements and stability fixes from the recent development builds.

- Separate **Account** and **Friends** pages, with automatic account, friend-request and Beta status updates.
- Sign in and recover using your username alone when it is unique. If several accounts share a name, use the full username including its four-digit tag.
- Improved account recovery, including developer-issued single-use recovery codes valid for 30 minutes, persistent reset notices and replacement recovery words after a successful reset.
- Request and download account data privately through **Privacy & Data**.
- Improved background processing, shutdown stability, bug-report reply checks and dinosaur-life tracking.
- Updated Prime Tracker map-version discovery and warnings when older zone data is used.
- Correct version information in Windows executable properties.

**Prime Tracker notice:** Migration, mass migration and patrol tracking may be inaccurate following the latest Evrima update until matching Vulnona map data is available. Live location tracking, Survival Vitals and growth estimates remain available, subject to the existing local-data limitations.

Approved Beta testers can receive eligible account-targeted update offers. Stable and Beta installations continue to use the same Friends, Party and map-sharing features.

### Previous release — v0.9.20.63

Improved background account and update checks, worker cleanup and application shutdown to address unexpected crashes. Added local crash diagnostics to assist troubleshooting.

### Earlier release — v0.9.20.60

v0.9.20.60 fixed several problems with **notifications and Friends**. Notifications now adjust to longer messages, and an older notification timer no longer cuts short a newer message. Accepted friends can trigger an online alert when they have enabled online visibility, while incoming friend requests appear automatically without a manual refresh. Signed-in Companion clients check their Friends information roughly every **15 seconds**.

**Friends on the same server** are now grouped automatically under **Map & overlays → Party & phone**, without requiring a Party code. Friends' map positions can also appear on the desktop map or Second Screen, but **both people must explicitly enable server and live location sharing**, and neither may use Invisible Mode. Location sharing is **off by default**; only recent, verified live-game positions are eligible. The existing manual Party system remains available.

v0.9.20.59's interface redesign and previous Companion functionality remain included.

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
