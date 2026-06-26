# 2026 World Cup Guide

A bilingual web page that shows what's at stake in every match of the 2026 FIFA World Cup. Results, group standings, win probabilities, and the knockout bracket, from the group stage to the final.

## Why it exists

I built this to keep my family and friends up to date during the World Cup, and to show them what to watch and why. The 2026 World Cup is the largest yet, with 48 teams in twelve groups of four, each playing three group games, making it very difficult to follow. The top two from every group advance, along with the eight best third-placed teams, and those third-placed teams are ranked against each other across all twelve groups. So a result in one group can change who advances from another, and a team can still go through after finishing third in its group. Context is very important, and I wanted to highlight that and make it easy to understand. This page puts each result in perspective and shows its impact on the rest of the tournament.

## Tabs

- **Today** — the day's matches, each with what the two teams are playing for, win probabilities, and the relevant group table, all updated after every match.
- **Schedule** — every match by day, with results added as they finish and win probabilities for upcoming matches.
- **Standings** — all twelve groups, showing who's advancing, in contention, and in danger.
- **Bracket** — qualified, eliminated, and still-in-contention teams, plus the knockout rounds.
- **More** — what this is, how the tournament works, the update schedule, help with adding it to a home screen, and more.

## Updates

Updated after each match. Reload the page once a game ends for the latest.

## How it was built

The idea behind this entire project was interpretation, and turning raw results, standings, and probabilities into plain-language explanations of what each match means and what's at stake, in both US English and Latin American Spanish. A 48-team World Cup throws out a lot of numbers, and the goal was to give users the context behind them, not just the scores.

Claude helped me write most of the code, as well as the integration of the interface and design system. I chose to update the data manually after each match, instead of scraping it live. Although, not the cleanest or quickest approach, it kept the project fairly simple and mostly free to run, with the data intepretation by Claude being the biggest cost. This is a personal project for following the World Cup with family and friends, so I never worried about scalability.

## Technical notes

- One self-contained `index.html`: HTML, CSS, and vanilla JavaScript. No build step, no framework, no backend.
- Match data lives in JavaScript objects near the top of the file and is edited after each match.
- Bilingual through a single translation object; the language toggle needs no reload.
- Installable to a home screen via a web app manifest and icon set.
- Privacy-friendly analytics through GoatCounter — no cookies, no personal data.
- `noindex` tags and a `robots.txt` keep the page out of search results.
- Hosted free on GitHub Pages.

## Disclaimer

Unofficial fan-made page. Not affiliated with FIFA, Adidas, or any official World Cup partner. FIFA World Cup™, team names, national flags, and the Adidas Trionda ball design are trademarks of their respective owners. Match data is sourced from publicly available sports data for informational purposes only.
