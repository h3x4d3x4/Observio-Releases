# Observio for Mac

Observio is a live TV and media player for Mac, iPhone, iPad and Android. It plays your own IPTV playlists and provider logins (M3U, Xtream Codes, Stalker portals), Plex, Emby and Jellyfin libraries, and HDHomeRun tuners, with a full TV Guide, catch-up, movies and series, and a full-screen TV Mode. Observio does not provide any channels or content; you bring your own sources.

This repository hosts the macOS release downloads and the automatic-update feeds. The source code is private.

Website: [observio.hexadexa.io](https://observio.hexadexa.io)

## Download

Get the latest version from the [Releases page](https://github.com/h3x4d3x4/Observio-Releases/releases/latest). Each release has two disk images:

| Your Mac | File |
|---|---|
| Apple silicon (M1 or later) | `Observio-<version>-arm64.dmg` |
| Intel | `Observio-<version>-x86_64.dmg` |

Not sure which one you have? Open **Apple menu > About This Mac**: it lists either a "Chip" (Apple silicon) or a "Processor" (Intel).

Open the disk image, drag **Observio** into **Applications**, and launch it.

## Requirements

- macOS 13 Ventura or later
- Apple silicon or Intel Mac

Observio is free to try. See [observio.hexadexa.io](https://observio.hexadexa.io) for details.

## Updates

Observio updates itself in the app using [Sparkle](https://sparkle-project.org). It checks automatically, shows the release notes, and installs with one click. You can also check any time with **Observio > Check for Updates…**.

Two update feeds are published from this repository:

| Feed | URL | Contents |
|---|---|---|
| Stable | `https://observio.hexadexa.io/appcast-stable.xml` | Stable releases |
| Beta | `https://observio.hexadexa.io/appcast.xml` | Stable releases and test builds |

Both addresses redirect to [`appcast-stable.xml`](appcast-stable.xml) and [`appcast.xml`](appcast.xml) in this repository. Every update is signed with an EdDSA key, and Sparkle verifies the signature before installing.

## Verifying downloads

Observio is signed with an Apple Developer ID, and every disk image is notarized by Apple with the notarization ticket attached, so macOS checks it when you open it. To check yourself:

```sh
# The disk image carries Apple's notarization ticket
xcrun stapler validate Observio-<version>-arm64.dmg

# The installed app is signed and accepted by Gatekeeper
spctl --assess --type execute -v /Applications/Observio.app
codesign --verify --deep --strict -v /Applications/Observio.app
```

## Release notes

- Each version's notes are on the [Releases page](https://github.com/h3x4d3x4/Observio-Releases/releases).
- The full history across all platforms is at [observio.hexadexa.io/changelog](https://observio.hexadexa.io/changelog).
- The update window in the app shows the notes for the version on offer.

## Other platforms

- **iPhone and iPad:** distributed through Apple, not from this repository. See [observio.hexadexa.io](https://observio.hexadexa.io) for availability.
- **Android, Android TV, Google TV and Fire TV:** see [Observio for Android](https://github.com/h3x4d3x4/Observio-Android-Releases) and the install guide at [observio.hexadexa.io/android](https://observio.hexadexa.io/android).

## Support and privacy

- Help and FAQ: [observio.hexadexa.io/support](https://observio.hexadexa.io/support)
- Privacy policy: [observio.hexadexa.io/privacy](https://observio.hexadexa.io/privacy)
- Report a problem from inside the app with **Help > Report a Bug…** (it can attach diagnostic logs), or email [andrei@hexadexa.dev](mailto:andrei@hexadexa.dev).

Open-source components bundled with the app, and their licenses, are listed in the app under **Settings > About > Open Source Licenses**.

---

Observio is made by [Hexadexa](https://hexadexa.io).
