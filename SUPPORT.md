# Support and bug reporting

## Normal bugs

Use **Report Bug** inside Evrima Companion whenever the application can open far enough to do so. This is the preferred route because it creates a private project report and can optionally include a sanitized diagnostic snapshot.

Diagnostics are **off by default** and can be previewed before submission. A successful report returns a `BUG-XXXXXXXX` reference; keep that reference for follow-up.

## If the app will not start

If Evrima Companion cannot open far enough to reach **Report Bug**:

1. Check `%LOCALAPPDATA%\IsleCompanion` for the most recent startup/error report.
2. Do not post passwords, tokens, private access keys, or a complete Windows user path publicly.
3. A GitHub issue may be used only as a fallback for a startup/release problem that prevents the in-app reporter from being used. Include the Companion version, Windows version, what happened, and the `BUG-XXXXXXXX` reference if one exists.

## Security or privacy-sensitive reports

Do **not** publish security-sensitive information or personal data in a public GitHub issue. Use the in-app **Report Bug** page, choose **Other**, describe the problem, and leave diagnostics disabled unless they are genuinely needed.

For a privacy access/deletion request, start the description with `PRIVACY REQUEST` and include the relevant `BUG-XXXXXXXX` reference(s).
