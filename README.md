# Evrima Companion

**Unofficial companion utility for The Isle: Evrima.**

Evrima Companion is a Windows desktop app providing server browsing, per-server dinosaur information, map/overlay tools, automatic location OCR, a phone/tablet Second Screen, Party/Friend markers, automatic updates and built-in bug reporting.

> **Pre-release project:** Evrima Companion is still in wider public testing. A public `1.0` release has not been declared and compatibility has not been certified across every Windows version, PC configuration, phone or mobile browser.

## Download

Public builds are distributed only through **GitHub Releases** for this repository. If the Releases page is empty, the current release candidate has not been approved for public distribution yet.

For v0.9.20.36 and later public builds, the normal Windows download is:

- `IsleCompanionSetup.exe` — installs the application for the current Windows user.
- `EvrimaCompanion-<version>-windows-x64.zip` — the same application in portable/onedir form, primarily provided for transparency and Qt/PySide LGPL library replacement/relinking rights.

Each release also carries SHA-256 checksums and a release manifest. Current pre-release builds are not code-signed, so Windows may display a SmartScreen/reputation warning.

Do not download Evrima Companion from third-party mirrors or re-hosted installers.

## Main features

- Official and unofficial Evrima server browser.
- Per-server dinosaur profiles.
- Read-only detection of current matching Evrima Prelobby character data where available.
- Vulnona Map Overlay integration.
- Automatic map-location OCR from the in-game Status Report.
- Manual location entry as a permanent fallback.
- Saved waypoints.
- Separate local-player and Party/Friend marker trails.
- Second Screen map for a phone/tablet on the same local network.
- Party/Friend realtime markers.
- Automatic update checking.
- Built-in bug reporting.

## Basic use

1. Download `IsleCompanionSetup.exe` from an official GitHub Release.
2. Run the installer and review/accept the freeware licence prompt.
3. Use **Servers** to browse Evrima servers and view/save dinosaur information.
4. Use **Map** for overlay controls, automatic/manual location, waypoints, Party/Friends and Second Screen.
5. Use **Report Bug** inside the Companion if something fails or behaves incorrectly.
6. Use **Updates** to check for newer versions.

## Bug reports

Please use the **Report Bug** page inside Evrima Companion whenever possible. A successful submission returns a `BUG-XXXXXXXX` reference.

The diagnostic attachment is **optional and off by default**. You can preview the exact sanitized diagnostic JSON before deciding whether to include it. The sanitizer is designed to redact known passwords/tokens, the Windows username/home path and configured client keys. Do not type passwords, account credentials or other secrets into the report description.

If the application cannot start far enough to use its Report Bug page, see [SUPPORT.md](SUPPORT.md).

## Privacy

Second Screen PC-to-phone synchronisation stays on the user's local network. Optional/network features can contact Supabase, GitHub, VulnonaMAP and public/session-discovery infrastructure used by Evrima.

See [PRIVACY.md](PRIVACY.md) for what is processed, what stays local, optional bug-report diagnostics, retention criteria and the privacy-request route.

## Licence

Evrima Companion's project-owned application/code/assets are **proprietary freeware**. Official unmodified builds may be used for personal, non-commercial use. The Companion source code is **not published in this repository**.

Selling, commercial exploitation, modified/derivative distribution and re-hosting of project-owned Evrima Companion material are not permitted without prior written permission, subject to applicable law and the independent rights attached to third-party components.

See [LICENSE](LICENSE) for the complete project-owned terms.

Third-party software keeps the rights granted by its own licence. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) and the [licence index](licenses/README.md).

## Qt / PySide6 LGPL compliance

Starting with v0.9.20.36, the public Windows application is packaged as **onedir**, so the Qt/PySide shared libraries remain visible and replaceable. The single-file setup program is a Qt-free installer/bootstrapper around that onedir application.

Public release assets include the exact build inventory, third-party licence pack, and corresponding Qt Base + Qt for Python/PySide source archives for the exact version used by that release.

See [QT_LGPL_COMPLIANCE.md](QT_LGPL_COMPLIANCE.md).

## Testing status

The project currently has a small tester group. Untested combinations are not presented as certified. The release-candidate checklist is public so testers can report exactly what they did and did not test:

[QA_CHECKLIST.md](QA_CHECKLIST.md)

## Third-party projects

Evrima Companion integrates with, redistributes separately, or acknowledges projects including Vulnona Map Overlay, VulnonaMAP, Qt/PySide6, Python, Requests, websocket-client, python-qrcode/Pillow, PresentMon and GameDig. The exact relationship and licence for each is documented in the third-party notices.

## Unofficial project

Evrima Companion is a fan-made utility. It is **not affiliated with, sponsored by, or endorsed by Afterthought LLC or the developers/publishers of The Isle**.

The Isle and all third-party names/trademarks remain the property of their respective owners.
