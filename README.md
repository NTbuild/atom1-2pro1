# atom1-2pro1 — MENDES header

A website header with iPods. A ring turns behind a single iPod whose screen counts up to 100%. Then four more iPods burst out from behind it and curve into an arc, float and settle. MENDES writes itself across the top, the menu rises from the bottom bar and the ring grows larger and brighter.
Once it has settled, scroll, drag or use the arrow keys to turn the arc (or click an iPod), and the one that comes to the front flips round to face you. The front iPod's screen shows a small player.

The ring, wordmark and menu follow blink.capital's intro: its ring video and bloom, the letter-by-letter wordmark in Guida Mono Pro, the frosted menu rising 50px over 3 s. The iPods are built in three.js; their screens play the NomadaToast clips.

- `index.html` — the header, one file, no build step (three.js loads from jsDelivr)
- `assets/ring.mp4` — from blink.capital (the user states permission to copy that site)
- `assets/fonts/GuidaMonoPro-Regular.woff2` — not in this repo: Guida Mono Pro is a commercial font. With a licence, drop the file in `assets/fonts/`; without it the wordmark falls back to a system monospace
- `assets/screens/` — 10-second 4:3 loops cut from Project 3's tape videos (Tino Assets), with first-frame posters

Serve it over http, not `file://`, since the screens are videos drawn into WebGL:

```bash
python3 -m http.server 5175 --directory .
```

Then open http://localhost:5175. Clips, timings, the arc's lean, float and flip live in `CONFIG` at the top of the script. Desktop first.

The blink.capital mirror used as the motion reference is in `../Archive/blink.capital mirror`.
