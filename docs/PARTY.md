# Evrima Companion Party / Friends

[Back to main README](../README.md)

Party / Friends lets Evrima Companion users share selected live gameplay information with a group while playing **The Isle: Evrima**.

## Companion Accounts & Friends (v0.9.20.58)

Companion now also has separate, optional **Account** and **Friends** pages under Social. Players can register without a personal email address, find each other by their full Companion usernames, exchange friend requests and block or remove contacts.

Accepted friends can see online status, current server and current dinosaur **only when the player enables those sharing options**. Invisible Mode hides presence information. Sharing is disabled by default. From v0.9.20.64, friend-request and account changes refresh automatically while signed in, with background checks as a fallback.

### Automatic same-server Friends — v0.9.20.60

When both accepted friends are playing on the **same server** and are sharing their server, Companion automatically groups them under **Map & overlays → Party & phone**. There is no Party code to enter for this account-based grouping.

Live map markers are a separate, optional feature. Under **Friends**, both players must enable **Share current server with accepted friends** and **Share live map position with accepted friends on my server**, and neither player may be Invisible. Sharing is **off by default**. Companion sends only recent verified live-game coordinates, not saved, manually entered or outdated locations. Shared friend markers can be shown on the desktop map and the local-network Second Screen.

The account-based Friends system does **not** share technical diagnostics and does not automatically turn on Party-code sharing. The manual **Party** system below remains available for trails, shared pins and selected vitals.

## Party codes

A player can create a Party code and give it to friends, or join somebody else's Party code from Companion.

## Shared map information

Party members can share:

- live map position
- individual movement trails
- display name
- marker symbol
- trail colour

Each user controls whether their own location sharing is enabled.

Party markers can appear on both the desktop map and the local-network Second Screen map.

## Shared Survival Vitals

Party members can optionally share selected dinosaur information such as:

- dinosaur
- server
- Health
- Growth
- Food
- Water
- Prime growth ETA when available

Prime ETA follows the same staged behaviour used by Survival Vitals: ETA to 75% first, then full-growth ETA after 75% growth.

## Connection handling

Companion tracks Party transport state separately from the visible Party code. When a remote connection is lost, the connected state is cleared rather than leaving the UI reporting a live connection that no longer exists.

## Privacy and control

Party is an explicit group feature. Location sharing can be disabled by the user, and Companion's privacy-minimised telemetry does not intentionally include Party codes or map coordinates.

## Related guides

- [Survival Vitals](SURVIVAL_VITALS.md)
- [Prime Tracker](PRIME_TRACKER.md)
- [Live Map & Location Tools](MAP.md)
- [Second Screen](SECOND_SCREEN.md)
- [FAQ](FAQ.md)

Evrima Companion is an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.
