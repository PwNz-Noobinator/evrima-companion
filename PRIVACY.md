# Evrima Companion privacy and data use

Evrima Companion is designed to keep normal game, OCR and map processing local wherever practical. The project does not sell user data.

The public GitHub bootstrap is currently **v0.9.20.40**. Installed testers receive newer application versions through the Supabase Stable update channel.

## Data that normally stays on the user's PC

- Companion settings and per-server dinosaur profiles.
- Local map/OCR screenshots, crops and rolling diagnostic files.
- The local game/config files read by supported Companion features.
- Prime Tracker per-life progress and local growth samples in telemetry-capable builds.
- From v0.9.20.49 development builds, Dinosaur Life Memory: server/species, accumulated active-play time, last-seen growth/vitals, life history and the last verified live map position used for local **Where was I?** recovery.
- Dinosaur Guide cached reference data, including its bundled/offline reference snapshot and refreshed cache.
- Bug-report reply ownership keys. The backend stores only a hash of each reply key.
- Second Screen pairing information and PC-to-phone map state. Second Screen is served directly across the user's local network and is not routed through a Companion cloud relay.
- The current random telemetry installation UUID and any one-time previous-installation UUID retained locally for telemetry identity migration.

## Local backup/restore — v0.9.20.49+

The optional manual Companion backup contains selected local settings/state such as profiles, waypoints, Prime state, Party settings and Dinosaur Life Memory. It is created only when the user chooses **Export backup** and remains on the user's chosen local path.

The backup deliberately excludes the telemetry installation identity, telemetry consent file, private bug-report reply ownership data and diagnostics/logs. Restoring a backup creates local rollback copies of files that are being replaced.

## Dinosaur Guide reference data — v0.9.20.54+

The Dinosaur Guide includes bundled offline reference data and can refresh its cached community reference information from **Evrima Quick Guide** (`evrimaquickguide.com`).

A refresh contacts that external website in the normal way, so its hosting/network providers may process ordinary request information such as an IP address and request metadata. Companion does not intentionally send the user's map coordinates, Party content, Steam/EOS identity, personal files or telemetry installation identifier as part of the Dinosaur Guide reference request.

The refreshed reference data is cached locally so the guide can continue working when the source is unavailable.

## Optional technical telemetry — v0.9.20.42+

Telemetry is **off by default** and requires an explicit user choice. It can be changed later in **Settings → Privacy & telemetry**.

### Why telemetry is useful

If enabled, telemetry helps us see how Evrima Companion is working on different PCs, which features are being used and where technical problems may be happening during public testing. It helps identify compatibility or feature issues that might otherwise go unnoticed and shows where improvements are needed.

It is not intended to track what you do in The Isle. Map coordinates, location history, Party messages, screenshots, Steam/EOS identity and personal files are not intentionally included.

The Settings page includes **View exactly what is collected**, so the current technical snapshot can be inspected before telemetry is enabled.

When enabled, the technical snapshot can include:

- A randomly generated Companion installation UUID. It is not derived from hardware.
- Companion version and telemetry schema version.
- Windows version/build and processor architecture.
- CPU model, GPU model(s) and installed RAM.
- Display resolution, DPI/scaling information and, when already known to Companion, The Isle game resolution.
- Companion language.
- Short bounded technical/feature events such as application start, feature use or telemetry state changes.
- Privacy-safe error events limited to a coarse Companion feature/component and non-sensitive error category. Expected normal background outcomes such as an unavailable remembered Party room or ordinary reconnect/network failure are not intended to be treated as application errors from v0.9.20.54 onward.

From v0.9.20.48, telemetry installation identity is kept separate from Party/Friends player identity. A dedicated random per-machine telemetry UUID is stored in local application data rather than in the distributable package. On the first v0.9.20.48+ identity migration, Companion can send the previous random installation UUID together with the new random installation UUID so the backend can preserve continuity and detect legacy duplicate identities. This migration link is not derived from hardware and does not add a hardware fingerprint.

Telemetry does **not intentionally include**:

- Name, email address or Windows username.
- Computer name, MAC address, drive/BIOS/GPU serial numbers or a hardware fingerprint.
- Steam or Epic Online Services account identity.
- Map coordinates, location history, waypoints or Party codes.
- Party/Friend messages or shared location content.
- Screenshots, OCR images or screen captures.
- Personal file contents or file listings.
- Bug-report descriptions unless the user separately submits a bug report.

Raw telemetry event rows are automatically removed after **90 days**. Installation summary records that have not contacted the service for **365 days** are removed automatically. Turning telemetry off stops future telemetry submissions.

Supabase hosts the Companion telemetry backend. Standard network infrastructure may process connection information such as an IP address while handling a request, but Evrima Companion does not intentionally place an IP address into its telemetry payload or telemetry tables.

A persistent random installation identifier is used to distinguish one installation from another over time. It is deliberately random and not generated from hardware identifiers. v0.9.20.48 introduced a one-time identity migration so existing installations can move to a corrected per-machine identifier while retaining a previous random identifier only as a continuity link.

## Bug reports

Bug reports are submitted only when the user presses **Submit report**.

The report contains the information the user types into the form, including the optional tester/display name, category, problem description and reproduction steps.

Where the reporter offers a sanitized diagnostic snapshot, it is intended to contain only bounded technical information relevant to troubleshooting. Depending on the build and the selected reporting options, this can include:

- Companion and Windows/runtime information;
- recent application/error state;
- limited server/map/overlay/OCR diagnostic state;
- recent normalized map coordinates when they are relevant to OCR/map diagnostics; and
- a random Companion installation identifier used to correlate reports from the same installation.

The sanitizer removes or masks known passwords, tokens, API/service-role style values, publishable client keys, the Windows home path and Windows username before submission. Diagnostics are intentionally bounded in size and do not upload the complete rolling diagnostic archive.

Bug reports are sent to the project's Supabase backend. Standard network information such as the source IP address may also be processed by Supabase as part of providing the service.

Do not type passwords, account credentials, private access tokens or other secrets into a bug report.

## Bug-report acknowledgements and conversations — v0.9.20.42+

Every successfully submitted report receives an automatic acknowledgement and is attached to a private in-app report thread.

Each report receives a random local reply key. Companion keeps that key on the originating installation; Supabase stores only its SHA-256 hash with the report. Companion uses the `BUG-XXXXXXXX` report number plus the private local key to prove that the installation owns the thread.

Knowing another user's report number alone is therefore not enough to read or post to that report conversation.

Developer replies cannot remotely pull new diagnostics, screenshots, files or other data from the user's PC. If more information is requested, the tester chooses what to type or explicitly send.

## Party / Friends

Supabase is also used for the optional Party/Friend realtime feature. While connected, the service can receive the room/party state needed to provide that feature, including the user's chosen display information and map/location updates intentionally shared with that room.

Leave the Party/Friend room to stop sending new Party/Friend state.

## Companion Social accounts and Friends — v0.9.20.58

Companion accounts are **optional**. Registration uses a display name and password, with a unique four-digit username tag; no personal email address is required. Supabase Auth uses an internally generated non-deliverable email alias for authentication. Passwords are handled by Supabase Auth, rather than stored in local Companion settings. A saved refresh session is encrypted locally using Windows DPAPI.

When you register, Supabase stores your account ID, display name and tag, name-change history, social preferences and account creation time. Account recovery uses four randomly generated recovery words shown to you at registration. The words are not retained in plaintext on the server: a salted verifier is stored, and recovery attempts are rate-limited.

The service stores friend requests, friendships, blocks and sharing permissions. Accepted friends may see online presence, current server or current dinosaur **only if you explicitly enable sharing**. Invisible Mode hides that information.

### Optional live map sharing with accepted Friends — v0.9.20.60

Account-based Friends can be grouped automatically when playing on the same server, provided both have enabled server sharing. To share **live map coordinates**, both accepted friends must **separately opt in** to sharing their current server and live map position, and neither may be Invisible. Location sharing remains **off by default** and is not enabled by becoming friends.

If enabled, the Companion Social service can receive and temporarily retain the latest verified live-game coordinates, map identifier and update timestamp alongside the user's current server/presence data. Those coordinates are supplied only to accepted, unblocked friends who are on the same server, with **mutual consent** and sufficiently recent location data. The Companion does not intentionally send saved, manually entered or stale coordinates through this feature. Visibility stops when the sharing preference is disabled, the user becomes Invisible, or the live presence/location expires.

The account-based Friends feature does not share private diagnostic data or make the user part of a Party-code room. The older optional Party feature operates separately.

Accounts can also be used to submit username reports, beta programme applications and feedback, and private privacy enquiries. The information you choose to submit is associated with your account so that the developer can reply or moderate. Existing bug reports and opted-in telemetry may be linked only through the respective ownership-verification process; creating an account does **not** enable telemetry or change your consent.

Deleting an account removes its profile, friendships and directly dependent social records. Independently submitted bug reports and opted-in diagnostic telemetry are not automatically erased when an account is deleted; they remain subject to their own retention and deletion procedures. Privacy enquiries can be submitted through the Companion.

Supabase and its network infrastructure may process standard request information, including IP addresses, for service security and abuse prevention. Companion does not intentionally store raw IP addresses in social profile records or sell user data.

## Updates

### GitHub

The public GitHub repository provides release/download information and the temporary public bootstrap tester package. Standard web-request information such as IP address and request metadata is processed by GitHub in the normal course of serving those requests.

### Supabase Stable update channel

Installed Companion builds use Supabase for the Stable application update channel. Update checks can therefore contact Supabase even when telemetry is disabled; telemetry consent is separate from the updater.

From v0.9.20.61, signed-in Companion clients can also contact the private update service to check whether their account is eligible for an update. Once enabled, this service uses the existing authenticated account session to check Beta eligibility and returns temporary download links for authorised releases. The update check is separate from optional telemetry; it does not require telemetry consent.

The GitHub bootstrap ZIP does not need to be rebuilt for each normal application update.

## VulnonaMAP / Vulnona Map Overlay

Map pages/resources are provided by VulnonaMAP and the separately licensed Vulnona Map Overlay. The Companion does not claim ownership of those services or components.

Second Screen may proxy the public map resources needed by the phone browser through the user's PC over the local network. Prime Tracker can refresh known Gateway zone geometry from VulnonaMAP when available and use a bundled cached fallback if the live refresh cannot be reached.

## Epic Online Services

The server browser uses public/session-discovery infrastructure associated with The Isle: Evrima to retrieve server information. The Companion does not request or bypass official-server RCON credentials.

## PresentMon

If the user explicitly installs or updates PresentMon through Companion, it is downloaded from its official GitHub release source. PresentMon is used only by work-in-progress optimiser/performance features. Local PresentMon performance files are separate from the optional Supabase telemetry described above.

## What Evrima Companion does not intentionally do

- It does not sell personal data.
- It does not read game process memory.
- It does not inject code into The Isle.
- It does not attempt to bypass or tamper with Easy Anti-Cheat.
- It does not request or bypass official-server RCON credentials.
- It does not upload OCR screenshots merely because OCR was used; screenshots remain local unless future behaviour is explicitly changed and documented.

## Third-party privacy terms

GitHub, Supabase, VulnonaMAP, Evrima Quick Guide, Epic Online Services and other third-party services operate under their own privacy terms. Evrima Companion cannot control the independent logging or retention practices of those services.

## Retention and privacy requests

Evrima Companion accounts are optional. Party location updates are intended as live room state rather than a permanent location-history feature.

Telemetry retention is described above. Bug-report records, report-thread messages and diagnostics the user chooses to submit are retained while useful for investigating defects, validating fixes, preventing duplicate reports or maintaining necessary release history; they may be deleted or de-identified earlier.

To request access to or deletion of a bug report you submitted, use **Report Bug**, choose **Other**, write `PRIVACY REQUEST` at the start of the description, and include the relevant `BUG-XXXXXXXX` reference(s). Do not post private information in a public GitHub issue.

For legacy bug reports and optional telemetry records that have not been linked to a Companion account, the project may be unable to establish ownership unless the requester supplies the relevant report reference or other verification information.

External providers such as Supabase and GitHub may process normal service/network logs under their own terms and retention policies, including processing in countries outside the user's own country.

## Changes

This notice may be updated as Companion changes. A release should ship the privacy notice that describes that release's behaviour.
