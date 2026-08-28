# Evrima Companion FAQ

## What is Evrima Companion?

**Evrima Companion** is an unofficial Windows companion app for **The Isle: Evrima**. It combines a server browser, live map tools, Survival Vitals, Prime Tracker, growth ETA estimates, Party/Friends tracking, dinosaur profiles and a phone/tablet Second Screen.

It is a fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.

## Is Evrima Companion free?

Yes. Evrima Companion is proprietary freeware for personal, non-commercial use.

## Does Evrima Companion have a live map for The Isle: Evrima?

Yes. Companion integrates a desktop Vulnona map overlay and can feed it the current live Asset Location. Manual coordinates remain available as a fallback.

The current Stable location path does **not** depend on OCR.

## Does Evrima Companion track dinosaur growth?

Yes. **Survival Vitals** can read the active dinosaur's Growth, Health, Food and Water from Evrima's local character data when available.

**Prime Tracker** observes growth changes over time and can estimate growth ETA. In Survival Vitals and Party displays, the ETA targets **75% growth first**, then switches to **100% / full growth** once the dinosaur reaches 75%.

## What is Prime Tracker?

Prime Tracker is Companion's tracker for Prime-related progress during the current dinosaur life. It can automatically detect visits to known **Sanctuary, Migration, Mass Migration and Patrol Zone** locations from the same live coordinates used by the map.

It checks movement between location samples rather than only testing a single point, and uses tolerant geometry for the different zone shapes found on Gateway.

## Does Evrima Companion work with friends?

Yes. **Party / Friends** lets players join a Party code and optionally share live map positions, individual trails, markers and selected Survival Vitals data.

## Can I use Evrima Companion on my phone?

The Windows Companion runs on the PC, but **Second Screen** lets a phone or tablet display the live Companion map over the same local Wi-Fi/LAN. The phone does not replace the Windows application; it acts as an additional map screen.

## Does Evrima Companion need OCR?

No. OCR is currently **disabled and locked off** in Stable. Current map-location and Prime functionality uses the working non-OCR live location path.

OCR recovery work remains in development for possible future use.

## Does Evrima Companion need Python installed?

No. The temporary public tester/bootstrap package contains its own private build runtime for the initial local build. It does not require a separate Python installation and does not add Python to the user's Windows PATH.

## Where do I download Evrima Companion?

The official public tester/bootstrap is available from this repository's **GitHub Releases** page:

- [Evrima Companion releases](https://github.com/PwNz-Noobinator/evrima-companion/releases)
- [Current public bootstrap: v0.9.20.40](https://github.com/PwNz-Noobinator/evrima-companion/releases/tag/v0.9.20.40)

The GitHub ZIP is the initial installation route. After installation, normal Companion releases are delivered through the built-in **Supabase Stable** update channel.

## Why is the GitHub download version older than the current Stable version?

The GitHub v0.9.20.40 package is a bootstrap/build kit. It does not need to be republished for every routine Stable update.

After installing it, open Companion and use **Updates → Check for updates** to move to the newest Stable build.

## Is Evrima Companion digitally signed?

Not yet. The current public testing route is temporary while trusted code signing for the intended normal Windows installer is being prepared.

Do not disable Microsoft Defender, SmartScreen or Smart App Control solely to run Companion. See [TESTER_BUILD.md](TESTER_BUILD.md) for the current tester distribution details.

## How do I report an Evrima Companion bug?

If Companion opens, use the built-in **Report Bug** page. Successful reports receive a `BUG-XXXXXXXX` reference and can support acknowledgement, developer replies and tester follow-ups.

If Companion cannot start or the temporary build kit fails before the app opens, see [SUPPORT.md](SUPPORT.md).

## Where can I see recent changes?

See the [public testing changelog](CHANGELOG.md) for the current Stable changes and recent development history.
