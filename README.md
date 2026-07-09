# Observio

**A modern IPTV player for Mac and iPhone/iPad** — live TV, movies and series, a full program guide, and catch‑up, in a clean native interface. Bring your own provider; Observio is the player.

This repository hosts the public macOS release downloads and the automatic‑update feed.

## Download (macOS)

Get the latest build from the [**Releases**](../../releases/latest) page:

- **Apple Silicon** (M1 or newer) — `Observio-<version>-arm64.dmg`
- **Intel** — `Observio-<version>-x86_64.dmg`

Open the DMG, drag **Observio** into **Applications**, and launch it. Builds are signed with a Developer ID and notarized by Apple. Requires **macOS 14 (Sonoma)** or later.

> iPhone and iPad ship separately through the App Store / TestFlight.

## What Observio does

- **Live TV** with a fast, filterable channel list, favorites, and a full EPG program guide.
- **Video on demand** — browse movies and series with automatic artwork, and resume exactly where you left off across devices and providers.
- **Catch‑up / archive** playback for providers that support it.
- **Media‑server libraries** — connect **Emby**, **Plex**, or **Jellyfin** and browse your libraries alongside live TV.
- **Multiple playback engines**, chosen automatically per stream: a built‑in **Native** engine with Metal‑accelerated deinterlacing for interlaced (1080i) sports, **MPV** for broad codec coverage, and Apple's **AVPlayer** for HLS/VOD.
- **Chromecast**, subtitle import, downloads, and a picture‑quality vs. smooth‑playback control.
- Works with **Xtream Codes**, plain **M3U** playlists, **Stalker** portals, and **HDHomeRun** tuners.

Observio does not provide any channels, streams, or content — you supply your own provider or playlist.

## Automatic updates

Observio keeps itself up to date via [Sparkle](https://sparkle-project.org). You'll be prompted in‑app when a new version ships — with the full changelog — or you can check any time from **Settings → Updates**. Updates are cryptographically signed (EdDSA) and verified before install.

## Support & feedback

- **Report a bug** from inside the app: **Help → Report a Bug** (it attaches diagnostics for you).
- Release notes for every version live on the [Releases](../../releases) page and in‑app under **Settings → Release Notes**.

---

More at [observio.hexadexa.io](https://observio.hexadexa.io).
