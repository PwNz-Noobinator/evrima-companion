# Evrima Companion FAQ

[Back to main README](../README.md)

## What is Evrima Companion?

**Evrima Companion** is an unofficial Windows companion app for **The Isle: Evrima**. It combines a server browser, live map tools, Survival Vitals, Prime Tracker, growth ETA estimates, a Dinosaur Guide, Party/Friends tracking, dinosaur profiles and a phone/tablet Second Screen.

It is a fan-made project and is not affiliated with, sponsored by or endorsed by Afterthought LLC or the developers/publishers of The Isle.

## Is Evrima Companion free?

Yes. Evrima Companion is proprietary freeware for personal, non-commercial use.

## Does Evrima Companion have a live map?

Yes. Companion integrates a desktop Vulnona map overlay and can feed it the current live Asset Location. Manual coordinates remain available as a fallback. The current Stable location path does **not** depend on OCR.

## Does Evrima Companion track dinosaur growth?

Yes. **Survival Vitals** can read the active dinosaur's Growth, Health, Food and Water from Evrima's local character data when available. **Prime Tracker** observes growth changes over time and can estimate growth ETA.

## Why do Survival Vitals or the Quick Bar sometimes update late?

Companion reads dinosaur information from The Isle's local character data. The game does not always write fresh values immediately, so Health, Growth, Food, Water and related information can sometimes update with a noticeable delay.

Companion can only refresh those values after The Isle has written newer data; the delay is therefore not always something Companion can remove.

## What is the Dinosaur Guide?

The **Dinosaur Guide** provides quick-reference information for the current playable roster, including diet, growth information and useful species details. It includes an offline reference snapshot, can refresh cached reference information, and can automatically follow the dinosaur Companion currently detects.

## What is Prime Tracker?

Prime Tracker follows Prime-related progress during the current dinosaur life. It can automatically detect visits to known **Sanctuary, Migration, Mass Migration and Patrol Zone** locations using the same live coordinates as the map.

## Does Evrima Companion work with friends?

Yes. **Party / Friends** lets players join a Party code and optionally share live map positions, individual trails, markers, shared pins and selected Survival Vitals data. It also supports navigation to Party members, optional separation warnings and persistent Party state across Companion restarts until the player deliberately leaves or disbands.

## Do I need a Companion account?

No. From v0.9.20.58, creating an account is optional. You can register with a username and password without providing a personal email address. The first-launch prompt also offers **Skip for now**.

## How do the new online Friends features work?

Use **Account & Friends** to find players by their full Companion username, send or accept friend requests, remove friends and block players. Friends can see your online status, server or dinosaur only when you choose to share that information. **Invisible Mode** is available, and all sharing is off by default.

The new Friends system is separate from the existing Party code feature, which continues to offer optional shared map positions, trails and vitals.

## What if I forget my Companion account password?

Account recovery uses the four recovery words shown when you create your account. Store them somewhere safe; do not share them with other players.

## Can I use it on my phone or tablet?

The Companion itself runs on Windows, but **Second Screen** runs in a normal browser over the same local Wi-Fi/LAN. It provides dedicated **Map, Dinosaur and Party** views, including live dinosaur information, Party positions, saved/shared pins and navigation controls.

## Does Evrima Companion need OCR?

No. OCR is currently **disabled and locked off** in Stable. Current map-location and Prime functionality uses the working non-OCR live location path.

## Why does Companion ask about telemetry?

Telemetry is optional and **off by default**. If you enable it, it helps us see how Companion is working on different PCs, which features are being used and where problems may be happening during public testing.

It does **not** intentionally collect your map location, screenshots, Steam/EOS account, Party messages or personal files. Optional error telemetry uses coarse feature/error categories rather than detailed user content, and v0.9.20.54 avoids treating expected background Party reconnect/network outcomes as application errors.

You can use **View exactly what is collected** before enabling telemetry and turn it off again at any time. When uninstalling, users with existing telemetry can choose whether to keep the technical usage history or request its deletion.

See [PRIVACY.md](../PRIVACY.md) for the full details.

## Does Evrima Companion need Python installed?

No. The temporary public tester/bootstrap package contains its own private build runtime for the initial local build. It does not require a separate Python installation or add Python to the user's Windows PATH.

## Where do I download Evrima Companion?

Use the official [GitHub Releases](https://github.com/PwNz-Noobinator/evrima-companion/releases) page. The current public GitHub package is the **v0.9.20.40 bootstrap**.

After the first launch, go to **Updates → Check for updates** and install the newest Stable version before testing. The current Stable version is **v0.9.20.61**.

## What changed in v0.9.20.61?

v0.9.20.61 adds the client-side infrastructure for account-targeted Beta updates. Once the private update service is enabled, approved testers will be able to receive eligible update offers through Companion without restarting or manually refreshing. Installed Beta builds display **(Beta)** beside their version; regular Stable builds retain the existing version label. Stable and Beta users continue to use the same Friends, Party and map-sharing systems.

The private update service still requires activation before Beta distribution becomes available. Until then, continue using Stable normally.

## What changed in v0.9.20.60?

v0.9.20.60 improves notifications and the Friends system. Notification boxes expand to fit their text; friend online notifications now appear for accepted friends who share online presence; and incoming friend requests update without needing to press **Refresh**. Signed-in Companion checks Friends status approximately every 15 seconds.

Accepted friends playing on the same server are grouped automatically under **Map & overlays → Party & phone**. This does not require a Party code. To see each other's live map markers, **both players must enable server sharing and live map-position sharing** in Account & Friends, and neither may be Invisible. Map sharing is **off by default**, and only recent, verified live-game coordinates are eligible. The existing manual Party system remains separate.

## How do I enable automatic friend map markers?

Sign in to Companion, open **Account & Friends**, and enable **Share current server with accepted friends** and **Share live map position with accepted friends on my server**. Each friend must enable the same options and turn off Invisible Mode. You must both be playing on the same server. The shared marker appears on the desktop and Second Screen map when a fresh, verified location is available.

Being friends or sharing online status alone does **not** enable map-position sharing.

## What changed in v0.9.20.59?

v0.9.20.59 redesigns the Companion's layout. **Servers**, **Map & overlays**, and **Updates** remain easy to reach, while the sidebar now groups other features into expandable **Dinosaur**, **Social**, and **Settings & help** menus.

Inside **Map & overlays**, the controls are separated into **Map controls**, **HUD & vitals**, **Party & phone**, and **Waypoints** tabs. **Settings** has its own General, Hotkeys, Dinosaur, Maintenance, and Telemetry & privacy tabs. Dinosaur Guide, Dinosaur Life, Prime Tracker, server profiles, account features and bug reports also have cleaner layouts.

The redesign keeps the existing visual theme and Companion functionality. Existing settings and optional telemetry choices are preserved.

## What changed in v0.9.20.58?

v0.9.20.58 adds optional Companion accounts, an online friends system, privacy-controlled presence sharing, beta applications, username reports and private privacy enquiries. The Quick Bar now sits at the top centre of the primary display and passes mouse clicks through to the game.

The Horde Testing and Oviraptor support added in v0.9.20.57 remains available.

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
