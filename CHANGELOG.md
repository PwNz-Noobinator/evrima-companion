# Evrima Companion Public Testing Changelog

This changelog tracks user-visible changes made after the public GitHub repository was created on 24 August 2026. Internal release tooling, QA-only changes and private development workflow details are intentionally omitted.

## v0.9.20.49 — development candidate — 4 September 2026

- Added persistent **Dinosaur Life Memory** per server so reconnecting or switching servers does not automatically reset a tracked life.
- Added total active playtime for the current dinosaur across game/Companion sessions plus a separate current-session timer.
- Added last-seen species, server, growth/vitals and verified live map position persistence for local **Where was I?** recovery.
- Restored positions from a previous session are kept local and are not broadcast to Party members as though they were fresh live locations.
- Added strong-evidence new-life detection for species changes and meaningful same-species growth resets, while avoiding false splits on ordinary reconnects.
- Added a **Dinosaur Life** page with current-life details, archived life history, maximum growth, total tracked time and longest-life statistics.
- Added crash-safe atomic/periodic life-state persistence and optional AFK-aware playtime using Windows last-input age only; Companion does not record which keys/buttons were pressed.
- Added optional local Companion backup/restore for settings, profiles, waypoints, Prime state, Party settings and dinosaur-life history. Telemetry identity/consent, private bug-report reply data and diagnostics/logs are deliberately excluded.
- Audited settings persistence so unknown/newer preference keys are preserved across rewrites and Survival Vitals can reopen automatically if the user left it enabled.
- Preserved the v0.9.20.48 telemetry identity migration unchanged.

## v0.9.20.48 — Stable — 1 September 2026

- Repaired telemetry installation identity so telemetry no longer reuses Party/Friends player identity as the installation identifier.
- Added a dedicated per-machine random telemetry UUID stored in local application data and kept separate from distributable release files.
- Added one-time telemetry identity migration support so upgraded installations can move to a new unique ID while retaining the previous ID for continuity/history.
- Added backend migration records and a `telemetry_identity_migrated` event so duplicated legacy identities can be detected and separated after upgrade.
- Added release-package safeguards that fail the build if runtime identity/settings state is accidentally included in a distributable package.
- Added regression coverage for unique fresh-install identities and update-time identity persistence/migration.

## v0.9.20.47 — Stable — 28 August 2026

- OCR is now **disabled and locked off** in the normal UI/config while the non-OCR live location path is used for current map and Prime functionality.
- Retained OCR recovery improvements internally for later re-enable/testing.
- Fixed Party connection state so a dropped socket clears the connected state immediately instead of leaving a stale connected indicator.
- Added **Survival Vitals** diagnostic state to built-in bug reports.
- Added **Prime Tracker** diagnostic state to built-in bug reports while deliberately excluding map coordinates from Prime diagnostics.

## v0.9.20.46 — Stable — 28 August 2026

- Improved Prime zone recognition across circle, polygon and open/path-style geometries.
- Added tolerant edge/crossing checks rather than relying on one narrow Patrol-path corridor model.
- Area-like unclosed multi-point zones can be treated as filled areas while genuinely thin route-style zones remain corridors.
- Survival Vitals and Party Prime ETA now show **ETA to 75% growth while below 75%**, then automatically switch to **full-growth ETA** after reaching 75%.

## v0.9.20.45 — Stable — 28 August 2026

- Wired the verified live Asset Location path directly into Prime Tracker before the normal map/Party/Second Screen fanout.
- Prime zone crossings no longer depend on the older OCR path.
- Removed Prime observation from manual map-coordinate navigation so moving the map manually cannot award Prime objectives.

## v0.9.20.44 — Stable — 28 August 2026

- Fixed dead/departed dinosaurs retaining stale Growth and Prime ETA in Dinosaur Profiles.
- Inactive TempData records are no longer treated as the active character.
- Prime active-life state is cleared when Survival Vitals has lifecycle evidence that the character has left/died.
- Stale map movement is no longer credited to an inactive Prime run.
- Persisted Prime run history is retained for normal reconnect/restart continuity.

## v0.9.20.43 — Stable — 28 August 2026

- The desktop map can remain open after The Isle exits.
- Added optional Prime full-growth ETA to Survival Vitals, Party data and Dinosaur Profiles.
- Added startup notifications for normal Stable updates with a **Not now** path for non-forced updates.
- Telemetry consent now persists independently from ordinary UI settings; normal updates do not reprompt unless the consent-policy version changes.
- Added privacy-minimised content-free feature-use telemetry for map, automatic location, Party, Survival Vitals and Second Screen use.
- Resolved/closed built-in bug-report threads are now read-only in both the UI and backend.
- Hardened emergency rollback handling so rollback requires explicit release lineage rather than treating an arbitrary newer candidate as a rollback target.

## v0.9.20.42 — development candidate — 27 August 2026

This development candidate introduced the core work that was subsequently published and refined in the v0.9.20.43+ Stable series.

- Added **Prime Tracker** for the current dinosaur life.
- Automatically tracks unique Sanctuary, Migration, Mass Migration and Patrol Zone visits from the same live coordinates already used by the map.
- Added movement-segment crossing detection so a zone crossed between two location samples can still be counted.
- Added persistent per-life Prime progress, manual non-detectable conditions and a manual **Reset current Prime run** fallback.
- Added observed growth-rate measurement with ETA estimates to 75% and 100% growth.
- Added brief click-through Prime progress notifications.
- Added live VulnonaMAP Prime-zone refresh with a bundled Gateway fallback.
- Added explicit **opt-in technical telemetry**, disabled by default.
- Added a first-run telemetry disclosure, Settings control and **View exactly what is collected** payload viewer.
- Added **My reports & replies** with secure per-report local reply keys.
- New bug reports receive an automatic acknowledgement and can carry developer/tester replies in the same thread.
- Added required-update presentation for future releases marked mandatory by the Stable channel.

## v0.9.20.40 — 25 August 2026

- Added a persistent Survival Vitals **Lock / Unlock** control matching the overlay interaction model.
- Locked vitals are fixed in place and mouse click-through; unlocked vitals are interactive and draggable, including while Evrima is running.
- Survival Vitals remembers lock state, position, width and height between sessions.
- Added user resizing while unlocked.
- Added **Refresh** and **Close** controls, with reopen support from Companion controls.
- Fixed a TempData race where one partial/failed read could make vitals stop updating; failed reads now retry automatically.
- Manual Refresh forces a safe re-read of the active/pending TempData record.

## v0.9.20.39 — 25 August 2026

- Redesigned Survival Vitals as a compact frameless HUD with clearer Health, Growth, Food and Water indicators.
- Added click-through behaviour while locked/in-game and movement when interactive.
- Automatic OCR calculated capture coordinates from the actual Evrima game-client resolution at this stage of development.
- Improved cleanup of native capture resources and temporary OCR images.
- Reduced duplicate background polling by centralising game-process state and using TempData change events for profile refreshes.
- Survival Vitals updates existing cards in place instead of recreating the entire HUD every second.
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
- Eevee29 and Kassia use independent counters/timers so both work separately.

## v0.9.20.36 — 24 August 2026

- The desktop map can be closed without closing Evrima Companion.
- After a deliberate map close, automatic same-session relaunch is suppressed until the user explicitly reopens it or The Isle restarts.

## v0.9.20.35 — 24 August 2026

- Added dual-source update discovery across Supabase and GitHub Releases, choosing the newest valid version.
- Added SHA-256 and byte-size verification for GitHub-compatible update downloads.
- Expanded public freeware licensing, privacy, Credits and third-party documentation.
- Removed the old global Rex/Stego progress animation while retaining numeric update-download progress.

## Current distribution note

GitHub provides the initial **v0.9.20.40 public tester/bootstrap** package. Once Companion is installed, routine tester updates continue through the Supabase Stable release channel. A new large GitHub tester ZIP is not required for each normal application update unless the bootstrap kit itself changes.

The long-term distribution target remains a normal prebuilt installer signed with a trusted code-signing certificate.
