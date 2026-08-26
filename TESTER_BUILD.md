# Temporary tester build distribution

Evrima Companion is currently using a temporary tester-distribution method while trusted code signing for the normal Windows installer is being prepared.

This is **not** the intended long-term installation method.

## What testers download

The temporary GitHub Release is a **self-contained ZIP build kit**, not a finished unsigned Companion EXE.

The ZIP contains:

- the exact Companion files required to build that tester version;
- a private Python/build runtime used only for the local build;
- the required build dependencies;
- Companion assets and third-party components required by the app;
- the applicable licence/privacy/notices files;
- one `BUILD AND INSTALL EVRIMA COMPANION.cmd` launcher.

The tester does **not** need Python installed and the bundled build runtime is not added to the user's Windows PATH.

Maintainer-only publishing material is deliberately excluded. The public kit does not contain the Supabase release uploader, release splitter, internal QA tests or other development-only release tools.

Runtime code required by the installed Companion remains included, including normal Supabase updates, Party/Friends, bug reporting and other application features.

## Tester experience

1. Download the official tester ZIP from this repository's **Releases** page.
2. Extract the whole ZIP.
3. Double-click **`BUILD AND INSTALL EVRIMA COMPANION.cmd`**.
4. The included private build runtime creates `IsleCompanion.exe` locally on that PC.
5. The newly built EXE starts automatically.
6. Companion's existing install flow copies itself into the user's local Programs folder, registers the app, creates the desktop/Start Menu shortcuts and launches the installed Companion.
7. Once Companion has opened successfully, the extracted tester-build folder can be deleted.

The private build environment is only there to create the first local EXE. It is not Companion's runtime after installation.

## Updates after installation

The ZIP is only the initial installation route during this temporary testing phase.

After installation, normal Companion updates come through the existing **Supabase Stable update channel**. Testers do not rebuild every update manually.

## Windows security warning

Current tester builds are not yet signed with the project's future trusted code-signing certificate.

The temporary local-build workflow is being used because locally produced test executables have behaved differently from the same type of unsigned executable downloaded directly from the internet during project testing. This **does not guarantee** that Windows will allow the resulting EXE to run and should not be treated as a security bypass.

Depending on the PC and Windows configuration:

- Microsoft Defender SmartScreen may still show an unrecognized-app/reputation warning;
- Windows 11 Smart App Control may still block unknown unsigned code;
- organization-managed PCs may apply additional application-control policies;
- User Account Control (UAC) is separate from SmartScreen and Smart App Control.

**Do not disable Smart App Control, Microsoft Defender, SmartScreen or other Windows security protections solely to run Evrima Companion.**

If Windows blocks the tester build without a normal permitted continuation path, stop and report the Windows version and exact message shown.

## Long-term plan

This ZIP/local-build method is temporary. The intended public release remains a normal **prebuilt, digitally signed Windows installer** downloaded from the official Evrima Companion release page.

When trusted signing is ready, these temporary build-kit instructions will be retired.

## Bugs and build failures

- If Companion opens: use its built-in **Report Bug** page whenever possible.
- If the build itself fails: keep `_build_output\build.log` and see [SUPPORT.md](SUPPORT.md).
- Do not post passwords, tokens, private keys or other secrets in a public issue.

Only use tester packages published by this repository. Do not use third-party mirrors or modified/repacked build kits.

Evrima Companion is an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.
