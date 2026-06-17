# bardtek-podcast-redirect

Branded vanity redirect: **https://podcast.bardtek.com → the "Ed's 100 Rules"
YouTube channel**.

Served by GitHub Pages with the custom domain `podcast.bardtek.com` (see
`CNAME`). `index.html` redirects to the channel-ID URL
(`youtube.com/channel/UCwCyx0-goMeBGd4H1t8J9fg`), which is stable even if the
`@handle` changes.

## To re-point the podcast link

Edit the URL in `index.html` (three places: `<link rel=canonical>`, the
`<meta refresh>`, and the `location.replace` script) and push. Nothing else
links the raw channel URL, so this is the single source of truth.

## DNS

In the `bardtek.com` zone (Google Cloud DNS):

```
podcast   CNAME   edhaynes.github.io.   TTL 3600
```
