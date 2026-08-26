# Support and bug reporting

## Normal bugs

Use **Report Bug** inside Evrima Companion whenever the application can open far enough to do so. This is the preferred route because it creates a private project report and can optionally include a sanitized diagnostic snapshot.

Diagnostics are optional and can be previewed before submission. A successful report returns a `BUG-XXXXXXXX` reference; keep that reference for follow-up.

## Temporary tester build problems

During the current public-testing phase, the initial GitHub download may be a ZIP build kit that builds the normal Companion installer locally before installation.

If the Build/Start Companion launcher fails before the normal Companion installer is created, report:

- the tester-package version;
- Windows version;
- the exact error text shown by the build launcher;
- which step failed, if one is displayed;
- whether Windows security displayed a separate warning or block message.

Do not post passwords, tokens, private keys, complete Windows user paths or other private data publicly.

See [TESTER_BUILD.md](TESTER_BUILD.md) for the temporary build workflow.

## SmartScreen / Smart App Control

Current tester software is not yet signed with the project's future trusted code-signing certificate.

Microsoft Defender SmartScreen may display an unrecognized-app warning for unsigned software. Windows 11 Smart App Control may block unknown unsigned code when Windows cannot establish that it is safe.

The temporary local-build workflow is **not guaranteed to avoid those protections**. Do not disable Smart App Control, Microsoft Defender, SmartScreen or other Windows security protections solely to run Evrima Companion.

If Windows blocks the tester build without offering a normal permitted continuation path, stop and report:

- the exact Windows message;
- Windows version;
- whether the message identifies SmartScreen, Smart App Control or another organization/application-control policy;
- the tester-package version.

A User Account Control (UAC) prompt is separate from SmartScreen and Smart App Control.

## If the installed app will not start

If Evrima Companion has installed but cannot open far enough to reach **Report Bug**:

1. Check `%LOCALAPPDATA%\IsleCompanion` for the most recent startup/error report.
2. Do not post passwords, tokens, private access keys, or a complete Windows user path publicly.
3. A GitHub issue may be used only as a fallback for a startup/release problem that prevents the in-app reporter from being used. Include the Companion version, Windows version, what happened, and the `BUG-XXXXXXXX` reference if one exists.

## Updates

During the temporary tester-build phase, GitHub provides the initial tester package while installed Companion updates continue through the existing Supabase release channel.

A tester normally should not need to rebuild the GitHub package for routine Companion updates.

## Security or privacy-sensitive reports

Do **not** publish security-sensitive information or personal data in a public GitHub issue. Use the in-app **Report Bug** page, choose **Other**, describe the problem, and leave diagnostics disabled unless they are genuinely needed.

For a privacy access/deletion request, start the description with `PRIVACY REQUEST` and include the relevant `BUG-XXXXXXXX` reference(s).
