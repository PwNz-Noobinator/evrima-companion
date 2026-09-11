# Evrima Companion Public Testing Changelog

This changelog covers player-visible changes made during public testing. Internal development, QA and release-tooling changes are omitted unless they directly affect users.

## v0.9.20.53 — Stable — 11 September 2026

- Expanded Second Screen into Map, Dinosaur and Party tabs for phone/tablet use over the local network.
- Second Screen now shows live dinosaur details including species, growth, Prime ETA, session time, total dinosaur-life playtime, server and last-known information.
- Added phone/tablet controls for navigation and map pins without needing to tab back to the PC.
- Added navigation to Party members with direction and distance.
- Added optional Party separation warnings.
- Added shared Party pins and Party positions to Second Screen.
- Party state can now persist across Companion restarts until the player deliberately leaves or disbands the Party.
- Added privacy-safe optional error telemetry using coarse feature/error categories only.
- Added optional uninstall feedback with a separate uninstall reason record.
- During uninstall, players with existing telemetry can choose to keep their technical usage history or request its deletion. Retained installations are marked inactive rather than appearing as current users.

## v0.9.20.52 — Stable — 9 September 2026

- Added a central hotkey manager with persistent keybinds and duplicate/conflict warnings.
- Added a configurable emergency shortcut to hide or restore Companion overlays.
- Map sidebar, lock state, position and size now persist between sessions.
- Added configurable breadcrumb trails and last-known location recovery until fresh live coordinates are available.
- Added persistent personal map pins.
- Added waypoint navigation with direction and distance to the selected destination.
- Added automatic last-location markers when a tracked dinosaur life ends.
- Added an optional draggable Quick Bar for selected live information such as growth, Prime ETA, session time and server.
- Added sortable Server Browser columns with remembered ascending/descending order while keeping existing search, filters and favourites.

## v0.9.20.51 — Stable — 7 September 2026

- Fixed the main Companion window becoming stuck at maximised size after using the custom maximise control.
- Restore now reliably returns the window to its previous normal size, including after restarting Companion.
- Added automatic recovery for affected v0.9.20.50 installations that had already saved incorrect window dimensions.

## v0.9.20.50 — Stable — 4 September 2026

- Redesigned the main Companion interface around a persistent left-side navigation rail.
- Reduced visual clutter and unnecessary boxed sections across the app.
- Improved spacing, headings, controls and page structure for a more consistent layout.
- Reworked the Map page into clearer behaviour, appearance and position/setup sections.
- Improved the Servers and Dinosaur Profile layouts so they fit correctly at the default window size.
- Reworked waypoint editing to use the available space more effectively.
- Improved the custom title-bar controls and their alignment.
- Moved Support and Uninstall into Settings.
- Reworded technical or developer-oriented interface text into clearer player-facing language.

## v0.9.20.49 — Stable — 4 September 2026

- Added persistent **Dinosaur Life Memory** so a tracked dinosaur can continue across Companion and game sessions.
- Added total active playtime for the current dinosaur plus a separate current-session timer.
- Added **Where was I?** recovery for the last known species, server, growth, vitals and map position.
- Added more reliable new-life detection so normal reconnects do not unnecessarily reset a tracked dinosaur.
- Added a **Dinosaur Life** page with current-life details, archived history and personal statistics.
- Added crash-safe life tracking and optional AFK-aware playtime.
- Added optional local backup and restore for Companion settings and player-created data.
- Improved settings persistence, including automatic reopening of Survival Vitals when previously enabled.

## v0.9.20.48 — Stable — 1 September 2026

- Improved telemetry installation identity so different PCs remain separate and updates retain continuity more reliably.
- Kept telemetry identity separate from Party/Friends identity.
- Added safer upgrade handling for existing telemetry installations.
- Added release-package safeguards to prevent local identity or settings data from being included in public builds.

## v0.9.20.47 — Stable — 28 August 2026

- Disabled OCR in Stable while the current non-OCR live location system is in use.
- Fixed Party connection status so disconnected sessions no longer remain incorrectly shown as connected.
- Expanded built-in bug reports with Survival Vitals and Prime Tracker diagnostic information while excluding map coordinates.

## v0.9.20.46 — Stable — 28 August 2026

- Improved Prime zone recognition for different zone shapes and route layouts.
- Survival Vitals and Party now show ETA to 75% growth while below 75%, then switch automatically to full-growth ETA.

## v0.9.20.45 — Stable — 28 August 2026

- Connected Prime Tracker directly to the live non-OCR location system.
- Manual map-coordinate changes no longer count toward Prime progress.

## v0.9.20.44 — Stable — 28 August 2026

- Fixed stale Growth and Prime ETA values remaining on Dinosaur Profiles after a dinosaur had died or left.
- Improved active-dinosaur detection so old character data is not mistaken for the current dinosaur.
- Prime progress now handles dinosaur-life changes more reliably while preserving valid progress across ordinary reconnects and restarts.

## v0.9.20.43 — Stable — 28 August 2026

- The desktop map can remain open after The Isle closes.
- Added optional full-growth Prime ETA to Survival Vitals, Party and Dinosaur Profiles.
- Added startup notifications for available Stable updates, including a **Not now** option for non-required updates.
- Improved telemetry consent persistence so normal updates do not repeatedly ask for permission.
- Added optional privacy-minimised feature-use telemetry for major Companion features.
- Resolved or closed built-in bug reports are now read-only.
- Improved emergency rollback handling for safer update recovery.

## v0.9.20.42 — Development Candidate — 27 August 2026

This development candidate introduced the main systems later published and refined in the v0.9.20.43+ Stable releases.

- Added **Prime Tracker** for the current dinosaur life.
- Added automatic tracking for Sanctuary, Migration, Mass Migration and Patrol Zone visits using live map coordinates.
- Added persistent Prime progress and growth-rate-based ETA estimates.
- Added brief Prime progress notifications.
- Added live Prime-zone data refresh with a bundled Gateway fallback.
- Added optional technical telemetry, disabled by default, with a clear consent screen and payload viewer.
- Added **My reports & replies** for private in-app bug-report conversations.
- Added support for future required updates when a release is marked mandatory.

## v0.9.20.40 — 25 August 2026

- Added persistent **Lock / Unlock** controls to Survival Vitals.
- Survival Vitals now remembers its position, size and lock state between sessions.
- Added user resizing while unlocked.
- Added **Refresh** and **Close** controls with reopen support from Companion.
- Improved Survival Vitals reliability when game data is temporarily unavailable.

## v0.9.20.39 — 25 August 2026

- Redesigned Survival Vitals as a compact HUD with clearer Health, Growth, Food and Water information.
- Added click-through behaviour while locked and dragging while unlocked.
- Improved automatic game-resolution handling for the location system used at the time.
- Reduced unnecessary background work and improved live HUD updating.
- Improved overlay session cleanup and diagnostics.

## v0.9.20.38 — 25 August 2026

- Added **Survival Vitals**.
- Added automatic Health, Growth, Food and Water monitoring from Evrima's local character data.
- Added a compact standalone vitals window.
- Added automatic active dinosaur/server detection.
- Added solo use with optional Party/Friends vitals sharing.
- Corrected the Dinosaur Profile health value.

## v0.9.20.36 — 24 August 2026

- The desktop map can now be closed without closing Evrima Companion.
- After closing the map manually, Companion no longer immediately reopens it during the same game session.

## v0.9.20.35 — 24 August 2026

- Improved update discovery across the available Companion update sources.
- Added integrity checks for supported update downloads.
- Expanded licence, privacy, Credits and third-party documentation.
- Simplified the update download progress display.

## Current distribution

GitHub currently provides the initial **v0.9.20.40 public tester/bootstrap** package. Once Companion is installed, normal Stable updates are delivered through the built-in update system.

The long-term distribution target remains a normal prebuilt Windows installer signed with a trusted code-signing certificate.
