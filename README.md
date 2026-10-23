# atom1-2pro1 — MENDES header

A website header with iPods. A ring turns behind a single iPod whose screen counts up to 100%. Then the other iPods burst out from behind it into a tilted row, float and settle, while the ring pushes out with them, larger and brighter. MENDES writes itself across the top and the menu rises from the bottom bar.

The row is agrumeafarm.it's jar slider (used with permission) with iPods for jars, driven by its own numbers: the 10° row, the sizes, blur and brightness by distance from the middle, the wheel and drag glide with a fling, each iPod swinging, leaning and turning on its own spring as it travels, nearby iPods turning toward the pointer, and one full spin over 2 s only when the pointer rests on an iPod. Click an iPod to bring it to the middle. The middle iPod's screen shows a small player.

The ring, wordmark and menu follow blink.capital's intro: its ring video and bloom, the letter-by-letter wordmark in Guida Mono Pro, the frosted menu rising 50px over 3 s. The ring also turns with the row, as the circle behind the jars does. The iPods are built in three.js; their screens play the NomadaToast clips.

- `index.html` — the header, one file, no build step (three.js loads from jsDelivr)
- `assets/ring.mp4` — from blink.capital (the user states permission to copy that site)
- `assets/fonts/GuidaMonoPro-Regular.woff2` — not in this repo: Guida Mono Pro is a commercial font. With a licence, drop the file in `assets/fonts/`; without it the wordmark falls back to a system monospace
- `assets/screens/` — 10-second 4:3 loops cut from Project 3's tape videos (Tino Assets), with first-frame posters

Serve it over http, not `file://`, since the screens are videos drawn into WebGL:

```bash
python3 -m http.server 5175 --directory .
```

Then open http://localhost:5175. Clips, timings, the ring and the slider's numbers (`CONFIG.slider`) live at the top of the script. Desktop first.

The blink.capital mirror used as the motion reference is in `../Archive/blink.capital mirror`.
