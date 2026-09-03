# Evrima Companion FAQ

[Back to main README](../README.md)

## What is Evrima Companion?

**Evrima Companion** is an unofficial Windows companion app for **The Isle: Evrima**. It combines a server browser, live map tools, Survival Vitals, Prime Tracker, growth ETA estimates, Party/Friends tracking, dinosaur profiles and a phone/tablet Second Screen.

It is a fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.

## Is Evrima Companion free?

Yes. Evrima Companion is proprietary freeware for personal, non-commercial use.

## Does Evrima Companion have a live map?

Yes. Companion integrates a desktop Vulnona map overlay and can feed it the current live Asset Location. Manual coordinates remain available as a fallback. The current Stable location path does **not** depend on OCR.

## Does Evrima Companion track dinosaur growth?

Yes. **Survival Vitals** can read the active dinosaur's Growth, Health, Food and Water from Evrima's local character data when available. **Prime Tracker** observes growth changes over time and can estimate growth ETA.

## What is Prime Tracker?

Prime Tracker follows Prime-related progress during the current dinosaur life. It can automatically detect visits to known **Sanctuary, Migration, Mass Migration and Patrol Zone** locations using the same live coordinates as the map.

## Does Evrima Companion work with friends?

Yes. **Party / Friends** lets players join a Party code and optionally share live map positions, individual trails, markers and selected Survival Vitals data.

## Can I use it on my phone or tablet?

The Companion itself runs on Windows, but **Second Screen** lets a phone or tablet display the live Companion map over the same local Wi-Fi/LAN.

## Does Evrima Companion need OCR?

No. OCR is currently **disabled and locked off** in Stable. Current map-location and Prime functionality uses the working non-OCR live location path.

## Why does Companion ask about telemetry?

Telemetry is optional and **off by default**. If you enable it, it helps us see how Companion is working on different PCs, which features are being used and where problems may be happening during public testing.

It does **not** intentionally collect your map location, screenshots, Steam/EOS account, Party messages or personal files. You can use **View exactly what is collected** before enabling it and turn it off again at any time.

See [PRIVACY.md](../PRIVACY.md) for the full details.

## Does Evrima Companion need Python installed?

No. The temporary public tester/bootstrap package contains its own private build runtime for the initial local build. It does not require a separate Python installation or add Python to the user's Windows PATH.

## Where do I download Evrima Companion?

Use the official [GitHub Releases](https://github.com/PwNz-Noobinator/evrima-companion/releases) page. The current public GitHub package is the **v0.9.20.40 bootstrap**.

After the first launch, go to **Updates → Check for updates** and install the newest Stable version before testing. The current Stable version is **v0.9.20.48**.

## Why is the GitHub download older than Stable?

The GitHub v0.9.20.40 package is the temporary bootstrap/build kit. Normal application updates are delivered through Companion after installation, so the large bootstrap ZIP does not need to be rebuilt for every Stable release.

## Is Evrima Companion digitally signed?

Not yet. The current public testing route is temporary while trusted code signing for the intended normal Windows installer is being prepared. Do not disable Microsoft Defender, SmartScreen or Smart App Control solely to run Companion.

See [TESTER_BUILD.md](TESTER_BUILD.md) for details.

## How do I report a bug?

If Companion opens, use the built-in **Report Bug** page. Successful reports receive a `BUG-XXXXXXXX` reference and support developer replies and tester follow-ups.

If Companion cannot start or the temporary build kit fails before the app opens, see [SUPPORT.md](SUPPORT.md).

## Where can I see recent changes?

See the [public testing changelog](../CHANGELOG.md).
