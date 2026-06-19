# bardtek-podcast-redirect

Branded landing page for **https://podcast.bardtek.com → the "Ed's 100 Rules"
podcast**. Navy + gold, owl emblem — consistent with the Bard Technical
Solutions site.

Served by GitHub Pages with the custom domain `podcast.bardtek.com` (see
`CNAME`). `index.html` is a static landing page (no auto-redirect) with
click-through buttons to the podcast on YouTube and the rules on GitHub.

## To re-point the podcast link

Edit the button `href` in `index.html`:

- **YouTube** — the `.btn--primary` link uses the channel-ID URL
  (`youtube.com/channel/UCwCyx0-goMeBGd4H1t8J9fg`), stable even if the
  `@handle` changes.
- **Spotify** — a ready-made button is commented out near the YouTube one.
  When the show is live on Spotify, uncomment it and set the `href`.

## Files

- `index.html` — the landing page (self-contained; inline CSS).
- `assets/owl.png` — Bard Technical Solutions owl emblem (logo + favicon).
- `CNAME` — `podcast.bardtek.com`.

## DNS

In the `bardtek.com` zone (Google Cloud DNS):

```
podcast   CNAME   edhaynes.github.io.   TTL 3600
```

## HTTPS

GitHub Pages provisions a Let's Encrypt cert for the custom domain after it is
set in **Settings → Pages**. If `https://` ever serves a `*.github.io` cert
(name mismatch / browser security warning), clear and re-enter the custom
domain in Pages settings to re-trigger cert provisioning, then enable
**Enforce HTTPS**.
