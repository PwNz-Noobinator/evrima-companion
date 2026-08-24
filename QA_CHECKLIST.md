# Evrima Companion v0.9.20.36 release-candidate checklist

This checklist is for the current small tester group. It does **not** claim that every Windows version, phone, browser, network or hardware combination has been certified. Mark only what was actually tested; anything else can remain **Not tested** for the public prerelease.

## 1. Build and install

- [ ] `build_exe.bat` completes without error.
- [ ] `dist\IsleCompanionSetup.exe` exists.
- [ ] `dist\IsleCompanion\IsleCompanion.exe` exists as the onedir application payload.
- [ ] `BUILD_DEPENDENCIES.txt` was created.
- [ ] `licenses\runtime\RUNTIME_LICENSE_INDEX.md` was created.
- [ ] `dist\github-release\0.9.20.36` contains the setup EXE, portable ZIP, checksums, manifest and legal documents.
- [ ] Running `dist\IsleCompanionSetup.exe` shows the freeware/licence confirmation, updates the canonical Companion install and starts it.
- [ ] Companion reports version `0.9.20.36`.
- [ ] Existing settings/profiles survive updating from `.35`.

## 2. Public-cleanup / legal UI

- [ ] The old global Rex/Stego progress bar is gone.
- [ ] Normal status messages still explain background work.
- [ ] Credits contains **Licences & privacy**.
- [ ] Companion licence opens.
- [ ] Third-party notices open.
- [ ] Licence files open.
- [ ] Privacy notice opens.
- [ ] Unofficial/non-affiliation wording is visible and does not imply endorsement by The Isle/Afterthought.
- [ ] Installed application folder exposes Qt/PySide runtime files rather than hiding them inside the Companion EXE.
- [ ] `LICENSE.txt`, `THIRD_PARTY_NOTICES.md`, `PRIVACY.md`, `QT_LGPL_COMPLIANCE.md` and `licenses` are present in the installed application folder.

## 3. Bug reporter privacy and operation

- [ ] Diagnostics are optional and OFF by default.
- [ ] **Preview diagnostic snapshot** shows the sanitized JSON before submission.
- [ ] Preview does not show your Windows username/home path, passwords, access tokens or service-role keys.
- [ ] A report can be submitted with diagnostics OFF.
- [ ] A report can be submitted with diagnostics ON.
- [ ] Successful reports return a `BUG-XXXXXXXX` reference.

## 4. Servers and dinosaur data

- [ ] Official server list loads.
- [ ] Unofficial/community server view loads if used.
- [ ] Filters/search work.
- [ ] Current dinosaur detection works when a valid current Prelobby cache exists.
- [ ] A server with no valid current cache does not resurrect stale automatic dinosaur data.

## 5. Desktop map / OCR

- [ ] Vulnona overlay opens normally.
- [ ] Small preset is approximately 300x300.
- [ ] Medium preset is approximately 400x400.
- [ ] Large preset is approximately 550x550.
- [ ] Manual coordinates move an already-open map in place.
- [ ] Automatic OCR works when Status Report is opened with Tab.
- [ ] Left-click use does not obviously break OCR capture.
- [ ] Own marker appears.
- [ ] Own connecting trail appears after moving between locations.
- [ ] Party/Friend marker trails still appear if Party is tested.
- [ ] Refresh map clears stale trail/history as intended.

## 6. Second Screen

- [ ] QR/pairing page opens.
- [ ] Phone/tablet on the same LAN can open the Second Screen page, if available to test.
- [ ] Own marker appears on the phone map without Party mode.
- [ ] Marker updates as the PC location changes.
- [ ] Party/Friend markers appear on the phone if Party is tested.
- [ ] Keep-awake works automatically where supported, or the fallback control is offered.

## 7. Party / Friends

- [ ] Create/join room works.
- [ ] Display name/marker settings work.
- [ ] Location updates reach another tester.
- [ ] Leaving/disconnecting stops new Party/Friend updates.

## 8. Updater migration

Supabase should remain at published bridge `0.9.20.35`; normal `.36` binaries are GitHub-hosted.

- [ ] `.36` can contact/check Supabase without crashing and treats `.35` as older/current fallback metadata.
- [ ] `.36` can contact/check GitHub Releases without crashing.
- [ ] If one update source is unavailable, the other does not make the whole updater fail unnecessarily.
- [ ] Automated tests confirm GitHub is preferred when both sources advertise the same newer version.
- [ ] Automated tests confirm a Supabase `force_install` rollback remains an emergency override.
- [ ] Wrong size/SHA-256 update metadata is rejected by automated tests.

## 9. Basic failure sanity checks

Only perform what is practical. These are not mandatory certifications.

- [ ] Starting with The Isle closed does not crash Companion.
- [ ] Closing the map helper does not crash Companion.
- [ ] A temporary network failure produces a useful error instead of corrupting settings.
- [ ] Closing/reopening Companion retains expected settings.

## 10. Release approval

- [ ] No known blocker remains that makes the public prerelease unsafe or unusable.
- [ ] Known limitations are documented rather than hidden.
- [ ] Visible wording, credits and branding are approved.
- [ ] This exact compiled candidate is approved for publication.

Do not rebuild after approving the candidate unless the affected checks are repeated. The approved `IsleCompanionSetup.exe` must be the same file whose SHA-256 is uploaded to GitHub.
