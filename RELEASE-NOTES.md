# Keg release notes

Newest first. Downloads: https://github.com/JKS-sys/keg-07-nov-2026-releases/releases/latest · https://ipconfig.co.network/keg

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
