# Evrima Companion v0.9.20.40 — Public Tester

This is the first wider public tester package for Evrima Companion.

Evrima Companion is still **pre-release software**. This build is being shared to expand testing while the normal digitally signed installer is being prepared.

## Install

1. Download **`Evrima-Companion-v0.9.20.40-Public-Tester.zip`** from the Assets section below.
2. Extract the **entire ZIP** to a normal folder.
3. Double-click **`BUILD AND INSTALL EVRIMA COMPANION.cmd`**.
4. Wait while the Companion EXE is built locally on your PC.
5. The normal Companion install process will start automatically, create the desktop/Start Menu shortcuts and launch Companion.

**You do not need Python installed.** The tester ZIP contains its own private build runtime and does not add Python to your Windows PATH.

Once Companion is installed, normal updates are delivered through Companion's **Supabase update channel**. You do not need to rebuild the app for every update.

## Main features

- Official and unofficial Evrima server browser with search, region/full/empty filters and favourites.
- Saved per-server dinosaur profiles.
- Desktop Vulnona map overlay.
- Automatic in-game location OCR plus manual-coordinate fallback.
- Saved waypoints.
- Party/Friends with live map positions, individual trails and custom markers.
- **Party Survival Vitals sharing** so group members can see each other's dinosaur, server, Health, Growth, Food and Water.
- Survival Vitals HUD with automatic active-character detection, Lock/Unlock, resizing, Refresh and Close/reopen controls.
- Phone/tablet **Second Screen** map with QR-code connection over the local network.
- Multiple interface languages and UI accent settings.
- Built-in automatic updates and bug reporting.
- Graphics/adaptive optimisation tools included as **Work In Progress** testing features.

## Windows security notice

This tester build is currently unsigned. Microsoft Defender SmartScreen may display an unrecognized-app warning and Windows 11 Smart App Control may still block unknown unsigned code.

The local-build tester package is **not guaranteed to bypass Windows security controls**. Do not disable Smart App Control, Microsoft Defender or SmartScreen solely to run Evrima Companion. If Windows blocks it without offering a normal continuation option, please report the exact Windows message.

## Reporting bugs

If Companion opens, please use the built-in **Report Bug** page whenever possible. Successful reports return a `BUG-XXXXXXXX` reference.

If the tester build itself fails before Companion can open, see the repository's `SUPPORT.md` instructions.

## Checksum

A SHA-256 checksum file is included as a separate Release asset for anyone who wants to verify the tester ZIP before use.

Evrima Companion is an unofficial fan-made utility and is **not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle**.
