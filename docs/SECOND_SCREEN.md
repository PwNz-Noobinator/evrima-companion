# Evrima Companion Second Screen

[Back to main README](../README.md)

Second Screen lets Evrima Companion display a live **The Isle: Evrima** map on a phone or tablet connected to the same local network as the PC running Companion.

## How it works

Companion runs the Second Screen service locally on the PC. The phone or tablet connects over the user's Wi-Fi/LAN using the connection details shown by Companion.

A QR code is provided so the local page can be opened without manually typing the address.

## What the phone/tablet map can show

Second Screen can receive:

- the player's latest map position
- Party/Friends markers
- Party movement trails
- map state from Companion

The phone is acting as an additional Companion display rather than exposing the map publicly on the internet.

## Desktop overlay is optional

Second Screen can be used while the desktop Vulnona overlay is open, but it does not require the desktop overlay to be visible. As long as Companion is running and the relevant location path is active, the phone/tablet map can operate independently.

## Network requirement

The phone or tablet must be able to reach the PC over the local network. Normal home Wi-Fi/LAN setups usually satisfy this requirement, while guest-network isolation or firewall rules can prevent the devices from seeing each other.

Second Screen is intended as a local-network feature, not a cloud-hosted public tracking page.

## OCR requirement

Second Screen does not need OCR specifically. Companion can feed its current non-OCR live Asset Location path into the same location state used by the phone/tablet map.

## Related guides

- [Live Map & Location Tools](MAP.md)
- [Party / Friends](PARTY.md)
- [Prime Tracker](PRIME_TRACKER.md)
- [Survival Vitals](SURVIVAL_VITALS.md)
- [FAQ](FAQ.md)

Evrima Companion is an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.
