# Evrima Companion Public Testing Changelog

This changelog tracks user-visible changes made after the public GitHub repository was created on 24 August 2026. Internal release tooling, QA-only changes and private development workflow details are intentionally omitted.

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

During the temporary public testing phase, GitHub is intended to provide the initial tester build-kit ZIP. Once Companion is installed, routine tester updates continue through the Supabase Stable release channel. The long-term distribution target remains a normal prebuilt installer signed with a trusted code-signing certificate.
