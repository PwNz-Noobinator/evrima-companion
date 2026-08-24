# Qt / PySide6 LGPL compliance information

Evrima Companion uses the community edition of **Qt for Python / PySide6** under the **GNU Lesser General Public License version 3 (LGPLv3)** for the Qt/PySide components used by the application.

The proprietary Evrima Companion licence does **not** replace or restrict the LGPL rights that apply to Qt/PySide6.

## What is provided with each public Windows release

The public Windows application is packaged as **PyInstaller onedir**, not as a Qt-containing one-file application. The installer itself is a small Qt-free bootstrapper. This keeps the Qt/PySide shared libraries visible beside the installed application so a recipient can replace them with an interface-compatible modified build.

The public release process is designed to provide:

1. a prominent notice that Qt/PySide6 is used under LGPLv3;
2. copies of LGPLv3 and GPLv3;
3. an exact build dependency inventory showing the PySide6/Qt version used;
4. collected licence/notice files from the installed runtime packages;
5. corresponding Qt Base, Qt SVG and Qt for Python/PySide6 source archives for the exact version used by that release, uploaded as GitHub Release assets alongside the application; and
6. a portable onedir ZIP containing the same replaceable-library application payload installed by `IsleCompanionSetup.exe`.

For the current application code, the Qt modules directly imported by Evrima Companion are QtCore, QtGui and QtWidgets. These are provided by Qt Base. The Windows build installs **PySide6-Essentials only**, rather than the PySide6 meta-package that also installs the large Addons wheel. PySide6 Essentials also places the LGPL-covered **Qt SVG** runtime in the Windows bundle, so `Qt6Svg.dll` is an explicitly reviewed dependency. The PyInstaller build excludes unused QML/Quick/PDF/VirtualKeyboard bindings, and the post-build audit fails if any Qt DLL outside the reviewed Qt Base + Qt SVG set is present.

The release process prepares the matching `qtbase`, `qtsvg`, and Qt for Python/PySide source archives. If later code introduces another Qt module, the release legal audit must be updated before publication.

## Library modification and reverse engineering

Nothing in the Evrima Companion proprietary licence prohibits replacement/modification of LGPL-covered Qt/PySide components or reverse engineering that the LGPL requires to be permitted for debugging those modifications.

A public release must not remove these rights through an installer, EULA, access control mechanism or distribution-platform term.

## Exact source information

The exact source archive names and SHA-256 values are generated from the Windows build's recorded PySide6 version during preparation of the GitHub release. The source archives are obtained from Qt's official download service and then uploaded with the release so recipients are not dependent solely on an external link remaining available.

## No changes to Qt/PySide6

Evrima Companion does not intentionally ship modified Qt/PySide6 library source. If a future release modifies an LGPL-covered library, the modified corresponding source and required build information must be published with that release.

## Licence texts

See:

- `licenses/LGPL-3.0.txt`
- `licenses/GPL-3.0.txt`
- the build-generated runtime licence collection under `licenses/runtime/`

This file is a project compliance notice, not a substitute for the LGPL itself.
