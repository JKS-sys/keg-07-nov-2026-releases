# Keg release notes

Newest first. Downloads: https://github.com/JKS-sys/keg-07-nov-2026-releases/releases/latest · https://ipconfig.co.network/keg

## Keg 1.0.2 — 16 Nov 2026

- Programs that died on start with "Assertion failed … alloc_pages_vprot" (a limit of the Game Porting Toolkit's Wine 7.7): Find out why now names it and switches the bottle to the CrossOver-sources engine in one click, downloading the engine first if needed.

## Keg 1.0.1 — 16 Nov 2026

- Works with the accounts API's new daily database budget: when writes are paused until 00:00 UTC, the release still builds and publishes the app (the server is redeployed on the next release), and Keg's server answers in a plain sentence instead of an error; crash reports are skipped for the day.
- Fixed: a Windows program opened from Finder (double-click, Open With, the Dock icon) or dropped on Keg's window did nothing. Keg now asks which bottle to run it in and starts it; .bat files run through cmd.
- No more permission questions: each bottle keeps its own Desktop, Documents and Downloads (Bottles → Private folders, on by default), and exports go to Keg's own folder instead of Documents.
- Logs: a health ring, counts that filter when clicked, a strip chart of where errors happened, a find box, and lines coloured part by part — with sounds for opening, filtering and searching.
- Owner Panel: an Analysis page with a world map of installs, the busiest countries, installs per day, and bars by system, version and plan.
- Small windows: the Owner Panel's tabs and action bar scroll sideways instead of covering the table; every page is checked down to 380 × 300.
- Website: the product page fetches its data and layout side by side, and the buy page connects to the payment form sooner.
- Eleven new sounds, each with its own drawn scene.
- FEATURES.md lists what Keg Free and Keg Pro include, in a format the website reads; a release check keeps it in step with the app.
- "A game as a Mac app" is now a Pro feature in the app, as the README already said; Pro features are also refused in the engine, not only hidden.

## Keg 1.0.0 — 07 Nov 2026

- The Worker's hourly job now runs from the ipconfig accounts API's scheduled jobs, so it needs none of Cloudflare's 5 cron triggers.

- CrossOver: a per-bottle Wine engine — the Game Porting Toolkit build, a community build of CodeWeavers' published CrossOver Wine sources (`winecx`), or the Wine inside an installed CrossOver.app under the user's own licence; the CrossOver sources mirrored in vendor/winecx.
- First release of Keg: bottles (make, duplicate, delete, per-bottle Windows version, renderer, HUD, MetalFX, DLSS-via-MetalFX, ray tracing, Retina, MSync/ESync, AVX, debug log, environment), the Game Porting Toolkit engine with Apple's D3DMetal, DXMT and DXVK renderers, winetricks, Rosetta 2 and Apple's own GPTK image import, eight stores installed in a click (Steam, Epic Games Store, GOG Galaxy, Battle.net, EA app, Ubisoft Connect, Rockstar Games Launcher, itch.io), a library that finds Steam, Epic and GOG games with an honest verdict, "Will it run?" with the kernel anti-cheat list, one-click fixes and "Find out why", logs for every program, a controller console (Pro), a game as its own Mac app in the Games category (Pro), Windows VM apps through FreeRDP's RemoteApp (Pro), accounts, activation codes and Razorpay (₹110 / month, ₹1,100 / year), the Owner Panel, crash reports, a self-updater, sounds with scenes, fourteen library layouts, light and dark gold themes.

### Install

Keg is a Mac app (Apple silicon — M1 and later). One download: `Keg_<version>_aarch64.dmg`.

- **With Pour:** `curl -fsSL https://ipconfig.co.network/pour/install | sh` then `pour install --cask keg`
- **By hand:** open the DMG and drag Keg into Applications. First launch: `xattr -cr /Applications/Keg.app` (Keg is self-signed, not notarized).
- Per-app volume and the equaliser need macOS 14.4 or later.
- Earlier Windows, Linux, ChromeOS, FreeBSD and Intel Mac builds stay on the releases page but are no longer updated.
