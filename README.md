# Evrima Companion

**An unofficial Windows companion app for The Isle: Evrima.**

Evrima Companion brings server browsing, dinosaur tracking, a desktop map overlay, automatic location updates, Party/Friends, Survival Vitals and a phone/tablet map into one app.

**Current tester version: v0.9.20.40**  
This is still pre-release software and is being opened to more testers before a signed public installer is ready.

## What can it do?

### Servers & dinosaur profiles

- Browse **Official** and **Unofficial** Evrima servers.
- Search by server name and filter by **region**, **full/empty servers** and **favourites**.
- See player count, ping, region, map and server version.
- Save a dinosaur profile for each server, including dinosaur, growth, location, sex, mutations and notes.
- Where Evrima provides the data, Companion can automatically read the current dinosaur's **growth, health, hunger and thirst** from the game's local character data.
- Favourite servers for quick access later.
- Launch The Isle directly from Companion.

### Map & automatic location

- Integrated **Vulnona Map Overlay** for the desktop.
- Press **Tab in-game** and Companion can automatically read your Asset Location and update the map.
- Manual coordinates are always available as a fallback.
- Lock/unlock the map, change its size and adjust its opacity.
- Optionally start/stop the map automatically with The Isle.
- Close the map without closing Companion and reopen it whenever you want.
- Save, edit, delete and copy **waypoints**.
- Choose your own local marker colour.

### Party / Friends

Create a Party code and give it to your friends, or join somebody else's Party.

- See Party members' **live map locations**.
- See separate trails for each player.
- Choose your display name, trail colour and marker symbol.
- Control how much location history is shown.
- Turn your own location sharing on or off.
- Party markers work on both the **desktop map** and **Second Screen phone/tablet map**.
- **Survival Vitals can also be shared with the Party**, letting Party members see each other's dinosaur, server, Health, Growth, Food and Water in the Survival Vitals window.

### Survival Vitals

Survival Vitals is a separate compact HUD that follows the character you are currently playing.

- Shows **Health, Growth, Food and Water** without needing to press Tab or use OCR.
- Automatically follows the active dinosaur/server as Evrima writes its character data.
- Works completely **solo**, or can display **your Party/Friends' shared vitals alongside your own**.
- Each Party row shows the player's name, dinosaur, server and how recently Evrima updated the snapshot.
- Lock it to make it fixed and mouse click-through while playing.
- Unlock it to move or resize it, even while The Isle is running.
- Remembers its position, size and lock state.
- Includes manual **Refresh** and **Close** controls and can be reopened from Companion.
- Failed/partial character-data reads are retried automatically instead of leaving the HUD permanently stuck.

### Second Screen phone/tablet map

Use a phone or tablet as another Companion map screen while you play.

- Start the phone map from Companion and connect using the displayed **QR code**.
- Runs over your **local Wi-Fi/LAN**.
- Works while the desktop overlay is open or completely independently of the desktop overlay.
- Receives your latest map position.
- Displays Party/Friend markers and trails as well.

### Languages & appearance

The Companion currently includes:

**English, Estonian, Finnish, Swedish, German, French, Spanish, Polish, Dutch, Portuguese, Italian, Norwegian and Danish.**

You can also change the Companion's UI accent colour from Settings.

### Graphics & performance tools — WIP

These tools are included for testing but are still marked **Work In Progress**:

- Detect The Isle's graphics configuration.
- Save/restore known setups and create backups.
- Adaptive performance mode with configurable target and priority.
- PresentMon integration and performance telemetry tools.

They should not be treated as finished/certified optimisation features yet.

### Updates & bug reporting

- Built-in automatic update checking.
- During this tester phase, installed Companion updates are delivered through the **Supabase Stable update channel**.
- Update files are integrity-checked before installation.
- Built-in **Report Bug** page with `BUG-XXXXXXXX` report numbers.
- Optional sanitized diagnostics help diagnose problems without requiring testers to hunt through log folders manually.

## Temporary tester download method

We are preparing a temporary GitHub tester package while trusted code signing is being arranged.

Instead of downloading a finished unsigned Companion installer, testers will download a ZIP containing everything required to build the normal installer **locally on their own Windows PC**.

The intended process is:

1. Download the official tester ZIP from this repository's **Releases** page.
2. **Before extracting it, right-click the downloaded ZIP → Properties. If Windows shows an `Unblock` checkbox, tick it and click Apply.** This prevents Windows' downloaded-file mark from unnecessarily blocking the included build launcher after extraction.
3. Extract the entire ZIP to a normal folder.
4. Double-click **`BUILD AND INSTALL EVRIMA COMPANION.cmd`**.
5. It builds the normal Companion executable locally, then Companion's normal install flow creates the desktop/Start Menu shortcuts and launches it.

If you already extracted the ZIP before unblocking it and Windows refuses to run the launcher, check **Properties** on the downloaded ZIP or the blocked launcher and use **Unblock** if Windows offers it, then extract/run again.

After that initial installation, normal Companion updates come through **Supabase** — testers will not need to rebuild every update manually.

The long-term plan is still to replace this temporary method with a normal **prebuilt, digitally signed Windows installer**.

## Windows security notice

Current tester builds are not yet signed with the project's future trusted code-signing certificate. Microsoft Defender SmartScreen may still display a reputation warning, and Windows 11 Smart App Control may still block unknown unsigned code.

Using Windows' **Unblock** option only removes the downloaded-file mark from the file you intentionally downloaded; it does not disable Defender, SmartScreen or Smart App Control.

The local-build tester package is **not guaranteed to bypass Windows security controls**. Do not disable Smart App Control, Defender or SmartScreen solely to run Companion. If Windows blocks it without offering a normal continuation option, report the exact message so it can be investigated.

See [TESTER_BUILD.md](TESTER_BUILD.md) for more detail.

## Reporting problems

Whenever Companion opens normally, please use its built-in **Report Bug** page. If Companion cannot start or the tester package itself fails, see [SUPPORT.md](SUPPORT.md).

## More information

- [Public testing changelog](CHANGELOG.md)
- [Tester build instructions](TESTER_BUILD.md)
- [Support](SUPPORT.md)
- [Privacy](PRIVACY.md)
- [Licence](LICENSE)
- [Third-party notices](THIRD_PARTY_NOTICES.md)

Evrima Companion is proprietary freeware for personal, non-commercial use. Third-party components remain under their own licences.

**Evrima Companion is an unofficial fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.**
