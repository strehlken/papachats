# Checkpoint — 20260505

## Repo
- `strehlken/papachats` (public), GitHub Pages on `main` / root.
- Live: https://strehlken.github.io/papachats/
- Remote uses SSH alias `git@github-strehlken:strehlken/papachats.git`.

## Style
- Inherited the existing palette/fonts from `20260505.html` (cream `#f6f0e6`, burgundy `#7a2a2a`, gold `#b58a3e`; Fraunces / Lora / JetBrains Mono).
- Did **not** apply global Brandon Grotesque / `#f7f8fa` defaults — project style was established first; per global rule, inherit don't override.
- Favicon: inline SVG data URI ("P" in burgundy on cream) on both pages.

## Layout choices
- `index.html` is the landing page; dated entries live at `YYYYMMDD.html` and are linked from a list on the index. Bare `20260505.html` URL still works on its own.
- Hero image (`images/papa_as_obi_wan.jpeg`, 1024×768) is CSS-cropped to top half via `aspect-ratio: 1024 / 384` + `object-position: center top`. Original file untouched — tune the second number to change the crop.

## Link previews (OG / Twitter)
- Both pages reference `images/papa-chats-preview.png` (2482×558) via absolute URLs in `og:image` and `twitter:image` (relative paths get rejected by most unfurlers).
- Image is wider than the OG sweet spot (1.91:1) — iMessage handles it well; Twitter/Slack may letterbox or center-crop. A 1200×630 version would be the safest universal size if that becomes a concern.
- Cache busting: if a URL was pasted before meta tags were added, scrapers will keep serving the stale preview. Use FB Sharing Debugger / Twitter Card Validator, or append `?v=1` once.
