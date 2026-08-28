# Evrima Companion Survival Vitals

Survival Vitals is Evrima Companion's compact HUD for **The Isle: Evrima**. It follows the active dinosaur from Evrima's local character data and can display core survival information without requiring OCR.

## What Survival Vitals shows

The HUD can display:

- Health
- Growth
- Food
- Water
- Prime growth ETA when available

Companion automatically follows the character currently being played when Evrima updates its local character data.

## Growth ETA behaviour

When Prime Tracker is enabled and enough growth samples exist:

- below 75% growth, Survival Vitals shows the estimated time to 75%
- at 75% growth and above, it switches to estimated time to 100% growth

This avoids showing a distant full-growth timer during the earlier part of the dinosaur's growth.

## Active-character detection

Survival Vitals watches Evrima's local TempData character records. Pre-existing files are not automatically treated as the current character at game start; Companion waits for current-session activity before considering a record active.

Partial or temporarily unreadable character-data writes are retried rather than permanently freezing the HUD after one failed read.

Lifecycle handling also clears the active state when the current dinosaur leaves or dies, preventing stale Growth or Prime ETA from remaining attached to a departed character.

## HUD controls

Survival Vitals can be:

- locked for a fixed, click-through HUD while playing
- unlocked for moving and resizing
- manually refreshed
- closed and reopened from Companion

Its position, size and lock state are remembered between normal sessions.

## Party support

Survival Vitals works solo and can also display selected vitals shared by Party/Friends members. Shared Party vitals can include Prime ETA when that data is available and sharing is enabled.

## Does Survival Vitals use OCR?

No. Survival Vitals reads Evrima's local character data. OCR is currently disabled and locked off in Stable and is not required for Health, Growth, Food or Water tracking.

## Diagnostics

The built-in bug reporter can include Survival Vitals technical state such as whether the game session is running, whether an active snapshot exists, retry counts and character-detection state. This helps diagnose stalls without requiring users to manually locate internal files.

## Related guides

- [Prime Tracker](PRIME_TRACKER.md)
- [Party / Friends](PARTY.md)
- [Live Map & Location Tools](MAP.md)
- [Second Screen](SECOND_SCREEN.md)
- [FAQ](FAQ.md)

Evrima Companion is an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.
