# Evrima Companion public tester

Evrima Companion is currently using a temporary public-testing installation method while the normal digitally signed Windows installer is being prepared.

> [!IMPORTANT]
> The GitHub package is the **v0.9.20.40 bootstrap**. After the first launch, use **Updates → Check for updates** and install the newest Stable version before testing. The current Stable version is **v0.9.20.48**.

## What you download

The GitHub Release contains a self-contained ZIP build kit. It includes the files and private build runtime needed to create the initial Companion executable locally on your PC.

**You do not need Python installed**, and the bundled runtime is not added to your Windows PATH.

## Install

1. Download the official tester ZIP from this repository's **Releases** page.
2. Before extracting it, right-click the ZIP → **Properties**. If Windows shows **Unblock**, tick it and click **Apply**.
3. Extract the whole ZIP to a normal folder.
4. Run **`BUILD AND INSTALL EVRIMA COMPANION.cmd`**.
5. Wait for the local build and installation to finish.
6. When Companion opens, go to **Updates → Check for updates** and install the newest Stable version.
7. Confirm you are no longer on v0.9.20.40 before testing.

Once Companion is installed successfully, the extracted bootstrap folder can be deleted.

## Why the GitHub version is older

The large GitHub ZIP is only the temporary initial installation route. Normal Companion updates are delivered through the built-in **Supabase Stable** update channel, so testers do not need to rebuild the application for every update.

The v0.9.20.40 bootstrap predates newer required-update behaviour. Its first update may therefore appear as a normal update rather than blocking use. **Accept the update to the newest Stable release.**

## Optional telemetry during testing

Telemetry is off by default. Enabling it helps show how Companion behaves on different PCs, which features are being used and where technical problems may be happening. This can reveal issues that never become a bug report.

It does not intentionally include map coordinates, screenshots, Steam/EOS identity, Party messages or personal files. Use **View exactly what is collected** in Companion for the current payload and see [PRIVACY.md](../PRIVACY.md) for full details.

## Windows security

Current tester builds are not yet signed with the project's future trusted code-signing certificate. Microsoft Defender SmartScreen may show an unrecognized-app warning and Windows 11 Smart App Control may block unknown unsigned software.

Using **Unblock** on the ZIP only removes the downloaded-file mark. It does **not** disable Defender, SmartScreen or Smart App Control.

Do not disable Windows security protections solely to run Evrima Companion. If Windows blocks the tester build without a normal continuation option, stop and report the exact Windows message.

## Bugs and build failures

If Companion opens, use the built-in **Report Bug** page whenever possible. If the bootstrap build itself fails, keep `build.log` from next to the launcher and see [SUPPORT.md](SUPPORT.md).

Do not post passwords, tokens, private keys or other secrets in a public issue.

Only use tester packages published by this repository. Do not use third-party mirrors or modified/repacked build kits.

## Long-term plan

This local-build method is temporary. The intended public release is a normal prebuilt Windows installer signed with a trusted code-signing certificate.

Evrima Companion is an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.
