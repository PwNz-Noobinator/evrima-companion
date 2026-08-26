# Temporary tester build distribution

Evrima Companion is currently using a temporary distribution method while trusted code signing for the normal Windows installer is being prepared.

This is a **pre-release tester workflow**, not the intended long-term installation method.

## What testers download

For the temporary public-testing phase, the GitHub Release download is a ZIP build kit rather than a prebuilt unsigned `IsleCompanionSetup.exe`.

The tester ZIP is intended to contain everything needed to produce the normal Companion installer on the tester's own Windows PC, including the required Companion build files, the required build dependencies, applicable licence notices, and an official Python runtime/installer where required by the build process.

The public tester package must not contain maintainer-only release publishing tools, Supabase upload scripts, internal QA/release tooling, private configuration, credentials or secrets.

Runtime code required for normal Companion features remains included. This includes the application's normal update and bug-report functionality.

## Intended tester experience

The target workflow is:

1. Download the official tester ZIP from this repository's GitHub Releases page.
2. Extract the complete ZIP to a normal folder.
3. Double-click the supplied **Build/Start Companion** launcher.
4. The launcher prepares the bundled build environment and builds the normal Companion installer locally.
5. The locally built installer starts automatically.
6. The normal Companion installer installs the application, creates the normal desktop shortcut and launches Evrima Companion.
7. After installation, testers use the installed Companion normally. They do not need to rebuild it for routine updates.

Once installed, application updates continue to be delivered through the Companion's existing **Supabase update channel** during this temporary phase. GitHub is the initial tester-package entry point, not the active application-update source for this phase.

## Windows security warning

Current tester builds are not yet signed with the project's future trusted code-signing certificate.

The temporary local-build workflow is being used because the project has observed that locally produced development/test executables can behave differently from an identical unsigned executable downloaded directly from the internet. It is **not a guarantee that Windows security will allow the result to run**, and it must not be treated as a method for bypassing Windows security controls.

Depending on the PC and Windows configuration:

- Microsoft Defender SmartScreen may show an unrecognized-app/reputation warning for unsigned software.
- Windows 11 Smart App Control may block unknown unsigned code when Microsoft cannot establish that it is safe.
- Organization-managed Windows PCs may apply additional application-control policies.
- A normal User Account Control (UAC) prompt is separate from SmartScreen and Smart App Control and may appear when an operation legitimately requires elevation.

**Do not disable Smart App Control, Microsoft Defender, SmartScreen, or other security protections solely to run Evrima Companion.**

If Windows blocks the tester build without offering a normal permitted continuation path, stop and report the Windows version, the exact message shown and the Companion tester-package version. The long-term solution is trusted code signing, not asking testers to weaken Windows security.

## Long-term distribution plan

This local-build ZIP is temporary.

The intended public-release model remains:

- a normal prebuilt Windows installer;
- signed with an appropriate trusted code-signing certificate;
- downloaded directly from the official Evrima Companion release page;
- normal automatic updates without requiring testers to rebuild the application.

When that signed distribution path is ready, the temporary local-build instructions will be retired.

## Updates and bug reports

After the initial local build/install, testers should use Companion normally.

- **Updates:** delivered through the existing Supabase release channel during this temporary testing phase.
- **Bug reports:** use **Report Bug** inside Evrima Companion whenever possible.
- **Build/startup failures:** see [SUPPORT.md](SUPPORT.md).

Do not post passwords, tokens, private keys or other secrets in public issues or bug descriptions.

## Official downloads only

Only use tester packages published by this repository. Do not use third-party mirrors, repackaged copies or modified build kits.

Evrima Companion remains an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.
