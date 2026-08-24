# Evrima Companion privacy and data use

Evrima Companion is designed to keep normal game and map processing local wherever practical. It does not sell user data.

## What stays local

- Saved Companion settings and per-server dinosaur profiles.
- OCR screenshots/crops and rolling diagnostic files unless the user chooses to submit a bug report.
- Second Screen pairing and live PC-to-phone map state. Second Screen is served over the user's local network and is not routed through a Companion cloud service.
- The user's local game/config files used by supported Companion features.

## Services contacted by the Companion

### Supabase
Supabase remains the backend for Party/Friend realtime transport and in-app bug reports. During the v0.9.20.35 updater transition it also remains an update source/fallback for existing installations.

Party/Friend use may transmit the room/party state needed for the feature, including the user's chosen display information and shared map/location updates while connected.

When the user submits an in-app bug report, the Companion sends the description entered by the user together with the limited diagnostic fields prepared by the bug-report system. A report is not submitted unless the user presses the submit button.

### GitHub
Starting with v0.9.20.35, the Companion can check the public Evrima Companion GitHub Releases feed and download update executables from GitHub. Standard network request information such as the user's IP address and request metadata will therefore be visible to GitHub in the normal way for web downloads.

### VulnonaMAP / Vulnona Map Overlay
Map pages/resources are provided by VulnonaMAP and the separately licensed Vulnona Map Overlay. The Companion does not claim ownership of those services or components.

### Epic Online Services
The server browser uses public/session-discovery infrastructure associated with The Isle: Evrima to retrieve server information. The Companion does not use or request official-server RCON credentials.

### PresentMon
If the user explicitly installs/updates PresentMon through the Companion, the tool is downloaded from its official GitHub release source. PresentMon is used only by the currently disabled/work-in-progress optimiser feature.

## What the Companion does not intentionally do

- It does not sell personal data.
- It does not read game process memory.
- It does not inject code into The Isle.
- It does not attempt to bypass or tamper with Easy Anti-Cheat.
- It does not request or bypass official-server RCON credentials.

## Bug reports

For the most useful diagnostics, use the **Report Bug** page inside Evrima Companion. Review the description before submitting and avoid entering passwords, account credentials, or other secrets.

This document describes the intended behaviour of the current pre-release software and may be updated as features change.
