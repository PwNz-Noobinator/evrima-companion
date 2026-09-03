# Support and bug reporting

## Normal bugs

Use **Report Bug** inside Evrima Companion whenever the application can open far enough to do so. This is the preferred route because it creates a private project report and can include the technical context needed for troubleshooting without posting it publicly.

A successful report returns a `BUG-XXXXXXXX` reference. Keep that reference for follow-up.

### v0.9.20.42 report conversations

Starting with v0.9.20.42, each submitted bug report becomes a small private conversation thread inside Companion:

- the report receives an automatic **received** acknowledgement;
- developers can reply directly to that exact `BUG-XXXXXXXX`;
- the tester can answer inside the same report thread; and
- the report status and replies appear under **My reports & replies**.

If a developer asks a question about an existing report, **reply inside that report instead of submitting a second bug report**. This keeps one problem under one reference and helps prevent duplicate reports from swamping the queue.

Each report is protected by a private random reply key stored on the originating Companion installation. The backend stores only its hash. A report number by itself is therefore not sufficient to read or post to somebody else's conversation.

Developer replies cannot remotely collect new screenshots, files or diagnostics from the PC. If more information is needed, the user chooses what to type or explicitly send.

Do not put passwords, account credentials, private tokens or other secrets into a bug report or follow-up message.

## If bug submission fails

If the in-app bug reporter itself shows an error, note the exact message and the Companion version. If Companion can still open normally, retry once after confirming the network connection. If it continues to fail, use the fallback route described below and state that the in-app reporter failed before the report number was created.

## Temporary tester build problems

During the current public-testing phase, the initial GitHub download is a ZIP build kit that builds the normal Companion executable locally before installation.

Before extracting the tester ZIP, right-click it → **Properties**. If Windows shows an **Unblock** checkbox, tick it and click **Apply**, then extract the ZIP. Windows can otherwise carry the downloaded-file mark onto the included `.cmd` launcher and block or warn when you try to run it.

If you already extracted the ZIP and Windows refuses to run `BUILD AND INSTALL EVRIMA COMPANION.cmd`, check **Properties** on the original ZIP or the blocked launcher for **Unblock**, use it if shown, then extract/run again.

If the Build/Start Companion launcher fails after it has actually started, report:

- the tester-package version;
- Windows version;
- the exact error text shown by the build launcher;
- which step failed, if one is displayed; and
- whether Windows security displayed a separate warning or block message.

Do not post passwords, tokens, private keys, complete Windows user paths or other private data publicly.

See [TESTER_BUILD.md](TESTER_BUILD.md) for the temporary build workflow.

## SmartScreen / Smart App Control

Current tester software is not yet signed with the project's future trusted code-signing certificate.

Microsoft Defender SmartScreen may display an unrecognized-app warning for unsigned software. Windows 11 Smart App Control may block unknown unsigned code when Windows cannot establish that it is safe.

Windows' **Unblock** option is different: it removes the downloaded-file mark from a file the user intentionally downloaded. It does not turn off Defender, SmartScreen or Smart App Control.

The temporary local-build workflow is **not guaranteed to avoid those protections**. Do not disable Smart App Control, Microsoft Defender, SmartScreen or other Windows security protections solely to run Evrima Companion.

If Windows blocks the tester build without offering a normal permitted continuation path, stop and report:

- the exact Windows message;
- Windows version;
- whether the message identifies SmartScreen, Smart App Control or another organization/application-control policy; and
- the tester-package version.

A User Account Control (UAC) prompt is separate from SmartScreen and Smart App Control.

## If the installed app will not start

If Evrima Companion has installed but cannot open far enough to reach **Report Bug**:

1. Check `%LOCALAPPDATA%\IsleCompanion` for the most recent startup/error report.
2. Do not post passwords, tokens, private access keys, or a complete Windows user path publicly.
3. A GitHub issue may be used only as a fallback for a startup/release problem that prevents the in-app reporter from being used. Include the Companion version, Windows version, what happened, and the `BUG-XXXXXXXX` reference if one exists.

## Updates

During the temporary tester-build phase, GitHub provides the initial tester package while installed Companion updates continue through the Supabase Stable release channel.

A tester normally should not need to rebuild the GitHub package for routine Companion updates.

v0.9.20.42 adds a dedicated required-update presentation for future releases marked mandatory by the Stable channel. The public v0.9.20.40 bootstrap predates that blocking UI, so its first hop to a newer required build still uses its older update-confirmation behaviour.

## Security or privacy-sensitive reports

Do **not** publish security-sensitive information or personal data in a public GitHub issue. Use the in-app **Report Bug** page, choose **Other**, describe the problem, and avoid attaching unnecessary diagnostic information.

For a privacy access/deletion request, start the description with `PRIVACY REQUEST` and include the relevant `BUG-XXXXXXXX` reference(s).

See [PRIVACY.md](../PRIVACY.md) for the current data-use description.
