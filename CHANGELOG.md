# Evrima Companion Public Testing Changelog

This changelog tracks user-visible changes made after the public GitHub repository was created on 24 August 2026. Internal release tooling, QA-only changes and private development workflow details are intentionally omitted.

## v0.9.20.42 — development candidate — 27 August 2026

**Not yet published as Stable.** v0.9.20.42 supersedes the unreleased v0.9.20.41 development candidate and keeps all of its planned user-facing work.

- Added **Prime Tracker** for the current dinosaur life.
- Automatically tracks unique Sanctuary, Migration, Mass Migration and Patrol Zone visits from the same live coordinates already used by the map.
- Zone visits do not require the zone to be active at that moment; Companion checks known places where those zone types can occur.
- Added movement-segment crossing detection so a zone crossed between two location samples can still be counted.
- Added persistent per-life Prime progress, manual non-detectable conditions and a manual **Reset current Prime run** fallback.
- Added observed growth-rate measurement with ETA estimates to 75% and 100% growth.
- Added brief click-through Prime progress notifications.
- Added live VulnonaMAP Prime-zone refresh with a bundled Gateway fallback.
- Added explicit **opt-in technical telemetry**, disabled by default.
- Added a first-run telemetry disclosure, Settings control and **View exactly what is collected** payload viewer.
- Telemetry can include Windows build, CPU/GPU models, installed RAM, display resolution/scaling, Companion version/language and known game resolution, plus bounded technical events.
- Telemetry intentionally excludes names, Windows usernames, Steam/EOS identity, computer names, map coordinates, Party codes, screenshots/OCR images, personal files and hardware serial numbers.
- Raw telemetry events are retained for 90 days; stale installation summaries are retained for 365 days.
- Added **My reports & replies** with secure per-report local reply keys. The backend stores only a SHA-256 hash of each key.
- New bug reports now receive an automatic **received** acknowledgement.
- Developers can reply directly to a specific `BUG-XXXXXXXX` report inside Companion.
- Testers can reply inside that same report thread instead of creating duplicate reports just to continue a conversation.
- Report numbers alone are not enough to read or post to another installation's report thread.
- Fixed the new reply-enabled bug-report submission RPC failing because `pgcrypto.digest()` was outside the function's restricted search path.
- Fixed Graphics (WIP) and Optimiser (WIP) tabs being re-enabled accidentally after required-update state was cleared. They remain disabled/hidden in normal tester use.
- Added required-update presentation for future releases marked mandatory by the Stable channel: dedicated popup, required-install action and normal app tabs disabled until the update is installed.
- The already-published v0.9.20.40 bootstrap predates that blocking UI, so its first hop to a newer mandatory build still uses its older confirmation behaviour.
- Optimised Supabase release-retention verification with an incremental checkpoint while retaining an explicit full-audit path.
- v0.9.20.42 is planned to be published through the Supabase Stable channel as a **required update** after Windows/in-game validation is complete.

## v0.9.20.40 — 25 August 2026

- Added a persistent Survival Vitals **Lock / Unlock** control matching the overlay interaction model.
- Locked vitals are fixed in place and mouse click-through; unlocked vitals are interactive and draggable, including while Evrima is running.
- Survival Vitals now remembers lock state, position, width and height between sessions.
- Added user resizing while unlocked.
- Added **Refresh** and **Close** controls, with reopen support from Companion controls.
- Fixed a TempData race where one partial/failed read could make vitals stop updating; failed reads now retry automatically.
- Manual Refresh forces a safe re-read of the active/pending TempData record.

## v0.9.20.39 — 25 August 2026

- Redesigned Survival Vitals as a compact frameless HUD with clearer Health, Growth, Food and Water indicators.
- Added click-through behaviour while locked/in-game and movement when interactive.
- Automatic OCR now calculates capture coordinates from the actual Evrima game-client resolution.
- OCR normally captures only the Asset Location region rather than an entire high-resolution monitor frame.
- Improved cleanup of native capture resources and temporary OCR images.
- Reduced duplicate background polling by centralising game-process state and using TempData change events for profile refreshes.
- Survival Vitals now updates existing cards in place instead of recreating the entire HUD every second.
- Added low-frequency Companion resource diagnostics for investigating game/performance/VRAM-related reports.
- Improved overlay relaunch/session diagnostics and cleanup.

## v0.9.20.38 — 25 August 2026

- Added **Survival Vitals**.
- Added automatic TempData-based Health, Growth, Food and Water monitoring without requiring Tab/Status Report OCR.
- Added a compact standalone vitals window.
- Added automatic active character/server detection from TempData activity.
- Added solo use with optional Party/Friends sharing support.
- Corrected the Dinosaur Profile health field after probe verification.

## v0.9.20.37 — 25 August 2026

- Restored the Eevee29 Runner easter egg after it was accidentally disabled by the Kassia easter egg.
- Eevee29 and Kassia now use independent counters/timers so both work separately.

## v0.9.20.36 — 24 August 2026

- The desktop map can now be closed without closing Evrima Companion.
- After a deliberate map close, automatic same-session relaunch is suppressed until the user explicitly reopens it or The Isle restarts.

## v0.9.20.35 — 24 August 2026

- Added dual-source update discovery across Supabase and GitHub Releases, choosing the newest valid version.
- Added SHA-256 and byte-size verification for GitHub-compatible update downloads.
- Expanded public freeware licensing, privacy, Credits and third-party documentation.
- Removed the old global Rex/Stego progress animation while retaining numeric update-download progress.

## Current distribution note

During the temporary public testing phase, GitHub provides the initial tester build-kit ZIP. Once Companion is installed, routine tester updates continue through the Supabase Stable release channel. A new large GitHub tester ZIP is not required for each normal application update unless the bootstrap kit itself changes. The long-term distribution target remains a normal prebuilt installer signed with a trusted code-signing certificate.
