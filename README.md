# Observio Releases

Public host for **Observio** macOS app releases and the Sparkle auto-update appcast.

- **Source code** lives in a separate private repository.
- This repo holds only the Sparkle feeds (`appcast.xml`, `appcast-stable.xml`) and the
  signed `.dmg` release assets attached to each GitHub Release.
- Every build is **EdDSA-signed**; Sparkle verifies the signature against the public key
  baked into the app, so public hosting is tamper-proof.

The app's update feed is served from `https://observio.hexadexa.io/appcast.xml`
(a Cloudflare redirect to the raw appcast in this repo). No authentication is required.
