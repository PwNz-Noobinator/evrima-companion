# Third-party notices

Evrima Companion is proprietary freeware, but it uses and/or interacts with third-party software under separate licences. Those third-party licences continue to apply to their respective components and are not replaced by the Evrima Companion licence.

## Vulnona Map Overlay

- Project: Vulnona Map Overlay
- Author: Muhahahahe
- Upstream: https://gitlab.com/muhahahahe/vulnona-map-overlay
- Bundled installer: `Vulnona Map Overlay_1.1.3_x64-setup.exe`
- Licence: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)

The installer is redistributed unchanged as a separate Windows application. Its upstream licence, README, and checksum information are preserved with the Companion release.

## VulnonaMAP

- Project: VulnonaMAP
- Creator: Coco.N
- Website: https://vulnona.com/game/map/

Evrima Companion uses the live VulnonaMAP website/resources for supported map features. The Companion does not bundle or claim ownership of VulnonaMAP basemap imagery.

## Qt / PySide6

- Project: Qt for Python / PySide6
- Upstream: https://doc.qt.io/qtforpython-6/
- Upstream licensing includes LGPLv3, GPLv3 and commercial options.

Evrima Companion uses the LGPL option for the Qt/PySide runtime used by the application. Rights granted by Qt/PySide licences are not restricted by the Evrima Companion proprietary licence.

## Python

- Project: CPython / Python
- Upstream: https://www.python.org/
- Licence: Python Software Foundation License Version 2 and incorporated-software licences as applicable.

PyInstaller-built releases contain a Python runtime.

## Requests

- Project: Requests
- Upstream: https://github.com/psf/requests
- Licence: Apache License 2.0

## websocket-client

- Project: websocket-client
- Upstream: https://github.com/websocket-client/websocket-client
- Licence: Apache License 2.0

## qrcode

- Project: python-qrcode
- Upstream: https://github.com/lincolnloop/python-qrcode
- Licence: BSD-3-Clause

Used to render the temporary Second Screen LAN pairing QR code.

## Pillow

- Project: Pillow
- Upstream: https://github.com/python-pillow/Pillow
- Licence: MIT-CMU, with additional bundled third-party notices as documented by Pillow.

## PyInstaller

- Project: PyInstaller
- Upstream: https://pyinstaller.org/
- Licence: GPL-2.0-or-later with the PyInstaller bootloader exception, with some files under Apache-2.0 as documented upstream.

PyInstaller is the build tool used to create the Windows executable. Its bootloader exception permits generated executable bundles to be distributed under the application's own licence, subject to the licences of bundled dependencies.

## PresentMon

- Project: PresentMon
- Upstream: https://github.com/GameTechDev/PresentMon
- Licence: MIT

PresentMon is not bundled in the normal Companion executable. It is downloaded only if the user explicitly uses the work-in-progress optimiser installation action.

## GameDig

- Project: GameDig / node-gamedig
- Upstream: https://github.com/gamedig/node-gamedig
- Licence: MIT

GameDig's public The Isle: Evrima/Epic adapter was used as an implementation/reference source for the Companion's public EOS server-discovery work.

## Additional runtime dependencies

The compiled Windows build may contain transitive dependencies required by the packages above. Each compiled release records the exact Windows package versions used so newly introduced dependencies can be reviewed before promotion out of pre-release status.

## Trademarks and third-party names

The Isle, VulnonaMAP, Vulnona Map Overlay, Qt, Python, GitHub, Supabase, Epic Online Services, PresentMon and other third-party names remain the property of their respective owners. Inclusion in this notice does not imply endorsement of Evrima Companion by those projects or organisations.
