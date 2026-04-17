# restova-guide

Private GitHub Pages host for the Restova post-op recovery guide.
Accessible only via the QR code printed on each kit.

## Live URL

`https://restovaco.github.io/restova-guide/r/zkk3ne8e2vzn/`

Do not share this URL publicly. It is embedded in the kit's QR code.

## Structure

- `/` — Pages root (serves a blank "Not found" page)
- `/r/<slug>/` — The actual guide (unguessable path)
- `robots.txt` — Disallow all crawlers
- `404.html` — Custom 404 matching brand tone
- `.nojekyll` — Skip Jekyll processing

## Privacy posture

- `noindex, nofollow, noarchive, nosnippet, noimageindex` meta on the guide
- `robots.txt` disallow all (reinforces the meta)
- `no-referrer` meta so outbound links don't leak the URL
- Unguessable 12-char slug path (~4.7 quadrillion combinations)
- Root serves a blank "Not found" — nothing hints at a guide

This is not auth-gated. Anyone with the exact URL can view it. The QR code
is the only intended distribution channel.

## Updating the guide

1. Edit `r/zkk3ne8e2vzn/index.html`
2. Commit + push to `main`
3. GitHub Pages rebuilds in ~1 minute

## If the URL ever leaks

Rotate the slug: rename the `r/<slug>/` directory to a new 12-char slug,
regenerate the QR code pointing to the new URL, push. Old URL 404s.
