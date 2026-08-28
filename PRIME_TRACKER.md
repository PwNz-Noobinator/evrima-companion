# Evrima Companion Prime Tracker

Prime Tracker is Evrima Companion's growth and objective tracker for **The Isle: Evrima**. It uses the same live Gateway location path used by Companion's map tools to follow Prime-related zone visits for the dinosaur life you are currently playing.

## What Prime Tracker tracks

Prime Tracker can automatically record visits to known:

- Sanctuary locations
- Migration zones
- Mass Migration zones
- Patrol Zones

The tracker checks movement between consecutive location samples rather than looking only at a single point. This helps detect a zone that was crossed between two readings.

Zone geometry is refreshed from VulnonaMAP when available, with a bundled Gateway snapshot used as a fallback. Detection supports circles, closed polygons and open/path-style shapes with tolerance around their boundaries.

## Growth ETA

Prime Tracker measures observed growth change over time and can estimate:

- ETA to 75% growth
- ETA to 100% growth

In Survival Vitals and Party vitals, the displayed estimate is staged: while the dinosaur is below 75% growth, Companion shows the ETA to 75%. Once 75% is reached, it switches to full-growth ETA.

Dinosaur Profiles can show full-growth ETA when enough growth data is available.

These are estimates based on observed growth rate, not guaranteed game timers. Diet, buffs, game updates, server rules or other gameplay factors can change actual growth speed.

## Per-life tracking

Prime progress is tied to the current dinosaur life. Companion can preserve the run across normal application restarts, while lifecycle handling prevents a dead or departed dinosaur from remaining as the active Prime run.

A manual **Reset current Prime run** control remains available as a fallback.

## Does Prime Tracker require OCR?

No. Current Prime tracking uses Companion's non-OCR live Asset Location path. OCR is presently disabled and locked off in Stable while its recovery implementation remains in development.

## Privacy

Prime diagnostics used by the built-in bug reporter expose technical tracker state such as whether a run is active, zone catalogue counts and catalogue source. Prime diagnostic snapshots are designed not to add the player's actual map coordinates.

## Related guides

- [Survival Vitals](SURVIVAL_VITALS.md)
- [Live Map & Location Tools](MAP.md)
- [Party / Friends](PARTY.md)
- [Second Screen](SECOND_SCREEN.md)
- [FAQ](FAQ.md)

Evrima Companion is an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.
