# Third-party notices

Evrima Companion is proprietary freeware, but it uses, redistributes, downloads or interoperates with third-party software and services under separate licences. Those third-party licences continue to apply to their respective components and are not replaced by the Evrima Companion licence.

Each public Windows build generates an exact dependency inventory and a runtime licence collection from the environment used to build that executable. Those generated files are included with the build/release materials.

## Vulnona Map Overlay

- Project: Vulnona Map Overlay
- Author: Muhahahahe
- Upstream: https://gitlab.com/muhahahahe/vulnona-map-overlay
- Bundled installer: `Vulnona Map Overlay_1.1.3_x64-setup.exe`
- Licence: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)

The installer is redistributed unchanged as a separate Windows application. Its upstream licence, README and checksum information are preserved under `third_party/vulnona-map-overlay/`.

Evrima Companion may install, launch, configure and close this separate helper for supported map/OCR functionality. The helper remains third-party software.

## VulnonaMAP

- Project: VulnonaMAP
- Creator: Coco.N
- Website: https://vulnona.com/game/map/

Evrima Companion uses live VulnonaMAP website/resources for supported map features. The Companion does not bundle or claim ownership of VulnonaMAP basemap imagery. Second Screen can temporarily proxy required public map resources through the user's PC over the user's LAN so the phone browser and Companion state can share one local origin.

## Qt / PySide6 / Shiboken6

- Project: Qt for Python / PySide6
- Upstream: https://doc.qt.io/qtforpython-6/
- Community licence options: LGPLv3 / GPLv3 (with upstream component-specific licensing as applicable)

Evrima Companion uses the LGPL option for the Qt/PySide runtime used by the application. The proprietary Companion licence expressly preserves all rights that the LGPL grants to recipients.

Copies of LGPLv3/GPLv3 are included under `licenses/`. The build records the exact PySide6, PySide6_Essentials, PySide6_Addons and Shiboken6 versions that were installed. Public GitHub release preparation also obtains and uploads the corresponding Qt Base and Qt for Python/PySide source archives for the exact PySide6 version used.

See `QT_LGPL_COMPLIANCE.md` for the project compliance process.

## Python

- Project: CPython / Python
- Upstream: https://www.python.org/
- Licence: Python Software Foundation License Version 2 and incorporated-software licences as applicable

PyInstaller-built Windows releases contain a Python runtime. The build records the exact Python version and copies the Python installation's licence file into the generated runtime licence collection.

## Requests

- Project: Requests
- Upstream: https://github.com/psf/requests
- Licence: Apache License 2.0

## Requests runtime dependencies

The Requests installation normally brings HTTP/runtime dependencies which are separately licensed. The exact installed versions are recorded by each Windows build. The release process collects their licence files automatically. Current expected packages include:

- urllib3 — MIT
- idna — BSD-3-Clause
- charset-normalizer — MIT
- certifi — Mozilla Public License 2.0 (MPL-2.0)

The project-owned Companion licence does not restrict rights granted by those licences.

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
- Licence expression: MIT-CMU, plus any applicable third-party notices shipped by Pillow

Used by QR/image paths. The build-generated licence collection preserves the licence/notice files from the exact installed Pillow distribution.

## PyInstaller

- Project: PyInstaller
- Upstream: https://pyinstaller.org/
- Licence: GPL-2.0-or-later with the PyInstaller bootloader exception, with some files under other documented licences

PyInstaller is the build tool used to create the Windows executable. Its bootloader exception permits generated executable bundles to be distributed under the application's own licence, subject to the licences of bundled dependencies. The exact PyInstaller/build-tool versions are recorded in the build inventory and their available licence/notice files are collected.

## PresentMon

- Project: PresentMon
- Upstream: https://github.com/GameTechDev/PresentMon
- Licence: MIT

PresentMon is not bundled in the normal Companion executable. If the user explicitly chooses the install/update action for the work-in-progress optimiser, the Companion downloads the official x64 release from the PresentMon GitHub project.

## GameDig

- Project: GameDig / node-gamedig
- Upstream: https://github.com/gamedig/node-gamedig
- Licence: MIT

GameDig's public The Isle: Evrima/Epic adapter was used as an implementation/reference source for the Companion's public EOS server-discovery work. GameDig is not presented as Companion-owned software.

## GitHub and Supabase

GitHub and Supabase are external services used by optional/network functionality and release infrastructure. Their names and service terms remain their own. Inclusion here does not imply endorsement of Evrima Companion.

## Build-generated runtime licence collection

Before a Windows release is built, the release tooling creates `licenses/runtime/` from the actual Python/build environment. It copies discoverable `LICENSE`, `COPYING`, `NOTICE` and related licence files for the runtime/build packages used by Companion and generates an index containing exact package versions and declared licence metadata.

The public-release legal gate fails if required licence documents, the runtime licence index, build dependency inventory or Qt LGPL compliance material are missing.

## Trademarks and third-party names

The Isle, VulnonaMAP, Vulnona Map Overlay, Qt, Python, GitHub, Supabase, Epic Online Services, PresentMon and other third-party names remain the property of their respective owners. Inclusion in this notice does not imply sponsorship or endorsement.

Evrima Companion is an unofficial fan-made utility and is not affiliated with, sponsored by, or endorsed by Afterthought LLC or the developers/publishers of The Isle.
