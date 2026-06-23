# 2026 World Cup Guide

A bilingual web page that shows what's at stake in every match of the 2026 FIFA World Cup. Results, group standings, win probabilities, and knockout bracket, from group stages to the final.

It works on a phone or a laptop, switches between US English and Latin American Spanish, and can be added to a home screen for an app-like experience.

## Why it exists

I built this to keep my family and friends up-to-date during the World Cup, and to show them what to watch and why. A 48-team tournament is hard to follow: twelve groups, three rounds of group games, and a result in one group can change who advances from another. A score on its own leaves out the context. Portugal beating Uzbekistan 5–0 also put Portugal top of their group and knocked Uzbekistan out, but the score alone doesn't say that. This page helps puts it all into prespective, and it's impact on the rest of the tournament.

## Tabs

- **Today** — the day's matches, each with what's at stake and what the two teams are playing for, win probabilities, and the relevant group table, all updated after every match.
- **Schedule** — every match by day, with results added after every match, and win probabilities for upcoming matches.
- **Standings** — all twelve groups, with info on who's advancing, in contention, and in danger.
- **Bracket** — qualified, eliminated, and still-in-contention teams, plus the knockout rounds.
- **More** — what this is, how the tournament works, web page update schedule, help with adding to home screens, and more.

## Updates

I update it by hand after each match. Reload the page once a game ends for the latest.

## How it was built

Claude helped me create the UI/UX using skills from shadcn and cal.com (coss). It also wrote most of the code, the bilingual copy with localizations and correct transliteration terminology based on my input, and how the data was intepreted and presented to the static web page. I chose to manually update everything after each match to avoid any unnecessary costs and complexities. As mentioned above, this was more to experiment with skills, and github pages to help myself and other's better understand and follow the World Cup, rather than optomizing and automating. A fun little vibe-coded web page for following the World Cup with family and friends.

The Claude skills used:
- **frontend-design** — the interface and design-system styling.
- **shadcn/ui blocks** — component patterns for the layout.
- **cal.com (coss) UI** — the overall look and design language.
- **humanizer** — applied to the English and Spanish copy to keep it natural.

## Technical notes

- One self-contained `index.html`: HTML, CSS, and vanilla JavaScript. No build step, no framework, no backend.
- Match data lives in JavaScript objects near the top of the file and is edited by hand.
- Bilingual through a translation object; the language toggle needs no reload.
- Installable to a home screen via a web app manifest and icon set.
- `noindex` tags and a `robots.txt` keep the page out of search results.
- Hosted free on GitHub Pages.

## Disclaimer

Unofficial fan-made page. Not affiliated with FIFA, Adidas, or any official World Cup partner. FIFA World Cup™, team names, national flags, and the Adidas Trionda ball design are trademarks of their respective owners. Match data is sourced from publicly available sports data for informational purposes only.
