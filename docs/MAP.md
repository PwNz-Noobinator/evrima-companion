# Evrima Companion Live Map & Location Tools

[Back to main README](../README.md)

Evrima Companion includes desktop map and live-location tools for **The Isle: Evrima**, built around the Vulnona Gateway map.

## Live map location

Companion can take the player's live Asset Location and hand it directly to the map without relying on OCR. The same verified location path is also used by Prime Tracker so map movement and Prime-zone detection stay in sync.

Manual coordinates remain available as a fallback.

## Desktop map overlay

The desktop map supports:

- live location updates
- manual coordinate entry
- saved waypoints
- marker customisation
- opacity controls
- size and position controls
- lock/unlock behaviour
- reopening the map after it is closed

The map can remain open after The Isle exits rather than being forcibly tied to the game process lifecycle.

## Vulnona Gateway branch

Companion targets the current supported Gateway map branch and checks the map runtime state when opening or handing off locations. Prime Tracker can also refresh its known zone geometry from VulnonaMAP data.

## OCR status

OCR remains implemented as a development fallback, but it is currently **disabled and locked off** in Stable. Companion's working live location path no longer depends on OCR, so map location updates and Prime tracking can function without it.

## Party markers

When Party/Friends is in use, the map can show group members' shared positions, individual trails and marker choices. Users can disable their own location sharing.

## Second Screen

The same Companion location state can be sent to the local-network Second Screen map on a phone or tablet. The phone map can be used with the desktop overlay open or independently of it.

## Related guides

- [Prime Tracker](PRIME_TRACKER.md)
- [Party / Friends](PARTY.md)
- [Second Screen](SECOND_SCREEN.md)
- [Survival Vitals](SURVIVAL_VITALS.md)
- [FAQ](FAQ.md)

Evrima Companion is an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.
