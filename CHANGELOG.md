# The World Cup Guide — Changelog

## v2.0.0 — 2026-06-23

### Major rebuild

- **New name:** "The World Cup Guide" (EN) / "La Guía del Mundial" (ES)
- **Trionda ball icon** embedded as PWA icon and favicon — works on iOS home screen, Android home screen, and browser tab
- **Add to home screen** instructions added to the More tab (iOS Safari + Android Chrome steps)
- **Celebration page:** When `CFG.tournamentOver = true` and `CFG.winner` is set, the page shows a full-screen overlay with spinning trophy, winner flag, team colors as background gradient, and falling confetti. Activated by setting two values at the top of the JS — no other changes needed.
- **Score spacing:** Scores now shown with wider letter-spacing and a subtle background chip (`2 – 0` style) for readability
- **Disclaimer** added to More tab — credits FIFA, Adidas, Trionda trademark. Clean and clear.
- **Security:** `noindex, nofollow, noarchive, nosnippet, noimageindex` meta tags added — page will not appear in Google or be archived
- **No "live" states:** Removed all live/real-time indicators. Page only shows results and upcoming. Users refresh after matches.
- **RAE country names:** All Spanish country translations corrected per RAE/DPD standards (Catar, Irak, Bosnia y Herzegovina, EE. UU., R. D. del Congo, etc.)
- **Counter.dev:** Analytics snippet included but commented out — uncomment and replace `YOUR_ID` to activate

### Files to upload to GitHub
- `index.html` — main page
- `favicon.ico` — browser tab icon (Trionda ball)
- `icon.png` — higher-res icon for sharing/bookmarks

---

## v1.5.0 — 2026-06-22 (evening)

- France 1–0 Iraq result added
- Iraq marked as eliminated
- Group I standings updated (France 6 pts, Norway 3 pts)
- Norway vs Senegal and Jordan vs Algeria stakes written

## v1.4.0 — 2026-06-22 (afternoon)

- Argentina 2–0 Austria result added
- Argentina marked as qualified
- Group J standings updated
- Light mode redesign
- Bilingual EN/ES toggle added
- All 12 group standings added
- Schedule tab added

## v1.3.0 — 2026-06-21

- MD2 Groups G & H results added
- Spain, Egypt added to standings
- Belgium 0–0 Iran, Uruguay 2–2 Cape Verde, New Zealand 1–3 Egypt results

## v1.2.0 — 2026-06-20

- MD2 Groups E & F results added
- Germany, Netherlands, Japan added to standings
- Initial GitHub Pages deployment

## v1.1.0 — 2026-06-19

- First matchday results (Türkiye 0–1 Paraguay)
- Win probabilities sourced from SportRadar models

## v1.0.0 — 2026-06-18

- Initial build
- Today's stakes tab
- Group I & J focus

---

## How to update after a match

1. Tell Claude: "Please update the page" (or "update with [specific result]")
2. Claude fetches the latest scores and standings from live data
3. Download the new `index.html`
4. Go to your GitHub repo → Add file → Upload files
5. Drop in the new `index.html` → Commit changes
6. Live within ~60 seconds

## How to activate the celebration page (after the final)

In `index.html`, find this near the top of the `<script>` block:

```js
const CFG = {
  updated: { ... },
  tournamentOver: false,
  winner: null
};
```

Change it to:

```js
const CFG = {
  updated: { en: "Updated Jul 19 · Final", es: "Actualizado 19 Jul · Final" },
  tournamentOver: true,
  winner: {
    name: "Argentina",          // English name
    nameEs: "Argentina",        // Spanish name
    flag: "🇦🇷",               // Flag emoji
    color1: "#74acdf",          // Primary team color
    color2: "#ffffff"           // Secondary team color
  }
};
```

Upload the file and everyone who visits sees the celebration page immediately.
