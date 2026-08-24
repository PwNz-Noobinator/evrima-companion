# Evrima Companion privacy and data use

Evrima Companion is designed to keep normal game, OCR and map processing local wherever practical. The project does not sell user data.

This document describes what the current pre-release build can process and which external services it contacts.

## Data that normally stays on the user's PC

- Companion settings and per-server dinosaur profiles.
- Local map/OCR screenshots, crops and rolling diagnostic files.
- The local game/config files read by supported Companion features.
- Second Screen pairing information and PC-to-phone map state. Second Screen is served directly across the user's local network and is not routed through a Companion cloud relay.

## Bug reports

Bug reports are submitted only when the user presses **Submit report**.

The report always contains the information the user types into the form, including the optional tester/display name, category, problem description and reproduction steps.

A sanitized diagnostic snapshot is **optional and off by default**. The user can preview the exact snapshot before sending it. If enabled, the snapshot can include:

- Companion and Windows/runtime information;
- recent application/error state;
- limited server/map/overlay/OCR diagnostic state;
- recent normalized map coordinates when they are relevant to OCR/map diagnostics; and
- a random Companion installation identifier used to correlate reports from the same installation.

The sanitizer removes or masks known passwords, tokens, API/service-role style values, publishable client keys, the Windows home path and Windows username before submission. Diagnostics are intentionally bounded in size and do not upload the complete rolling diagnostic archive.

If the diagnostic option is left disabled, the random installation identifier and diagnostic snapshot are not sent with that report.

Bug reports are sent to the project's Supabase backend. Standard network information such as the source IP address may also be processed by Supabase as part of providing the service.

Do not type passwords, account credentials, private access tokens or other secrets into a bug report.

## Party / Friends

Supabase is also used for the optional Party/Friend realtime feature. While connected, the service can receive the room/party state needed to provide that feature, including the user's chosen display information and map/location updates intentionally shared with that room.

Leave the Party/Friend room to stop sending new Party/Friend state.

## Updates

### GitHub

Starting with v0.9.20.35, Evrima Companion can check the public GitHub Releases feed and download update files from GitHub. Standard web-request information such as IP address and request metadata is processed by GitHub in the normal course of serving those requests.

### Supabase transition source

During the v0.9.20.35 transition, Supabase remains an update source/fallback so installations that pre-date GitHub update support can receive the bridge release. Supabase continues to be used for Party/Friends and bug reports after update binaries move to GitHub.

## VulnonaMAP / Vulnona Map Overlay

Map pages/resources are provided by VulnonaMAP and the separately licensed Vulnona Map Overlay. The Companion does not claim ownership of those services or components.

Second Screen may proxy the public map resources needed by the phone browser through the user's PC over the local network. This is used so the phone map and Companion state can share the local Second Screen origin.

## Epic Online Services

The server browser uses public/session-discovery infrastructure associated with The Isle: Evrima to retrieve server information. The Companion does not request or bypass official-server RCON credentials.

## PresentMon

If the user explicitly installs or updates PresentMon through the Companion, it is downloaded from its official GitHub release source. PresentMon is used only by the currently work-in-progress optimiser feature.

## What Evrima Companion does not intentionally do

- It does not sell personal data.
- It does not read game process memory.
- It does not inject code into The Isle.
- It does not attempt to bypass or tamper with Easy Anti-Cheat.
- It does not request or bypass official-server RCON credentials.
- It does not upload OCR screenshots merely because OCR was used; screenshots remain local unless future behaviour is explicitly changed and documented.

## Third-party privacy terms

GitHub, Supabase, VulnonaMAP, Epic Online Services and other third-party services operate under their own privacy terms. Evrima Companion cannot control the independent logging or retention practices of those services.

## Changes

This notice may be updated as the Companion changes. A release should ship the privacy notice that describes that release's behaviour.

## Retention and privacy requests

Evrima Companion does not require a Companion account. Party/Friend location updates are intended as live room state rather than a permanent location-history feature. Bug-report records and any diagnostics the user chooses to attach are retained only while they remain useful for investigating defects, validating fixes, preventing duplicate reports, or maintaining necessary release history; they may be deleted or de-identified earlier. A fixed automated retention period is not currently configured.

To request access to or deletion of a bug report you submitted, use **Report Bug**, choose **Other**, write `PRIVACY REQUEST` at the start of the description, include the `BUG-XXXXXXXX` reference(s) you want reviewed, and leave diagnostics disabled unless they are genuinely needed for the request. Do not post private information in a public GitHub issue.

Because the Companion normally has no user account and deliberately minimizes identifying information, the project may be unable to identify data as belonging to a particular person unless the requester provides the relevant report reference or other information sufficient to locate it.

External providers such as Supabase and GitHub may process normal service/network logs under their own privacy terms and retention policies, including processing in countries outside the user's own country.
