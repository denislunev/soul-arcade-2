# Soul Arcade II

An arcade-style name vibe reader — the standalone sequel. Type a name and get its vibe verdict, battle two names head-to-head, or guess the hidden daily name. Pure math, no mysticism, no personal data.

## How to play

The game has three modes — tap the pill to switch:

- **SOLO** — type any name and tap **SCAN VIBE**. You get a fun arcade verdict for that name. Some scans trigger rare visual effects (the golden one is special). Collect different verdicts to unlock stickers.
- **VS** — type two names and tap **COMPARE VIBES**. They battle with rock-paper-scissors: rock beats scissors, scissors beat paper, paper beats rock. The winner is highlighted.
- **GUESS** — guess the hidden daily name in 6 tries (Wordle-style). The letter count is shown up front. After each guess, letters turn **green** (right spot), **yellow** (in the name, wrong spot), or **dark** (not in the name). Solve it in 1–2 tries for a golden celebration. A new name drops every day — keep your streak alive.

Tap **? HOW TO PLAY** inside the game any time for the same rules. Tap **COLLECTION** for stickers and **STATS** for your progress and the worldwide player count.

## How it works

- Type any English letters and get one of 101 fun verdicts
- The app maps the input deterministically — same input always gives the same verdict
- Collect stickers, build daily streaks, and unlock visual effects
- No phone numbers, no AI, no tracking

## Tech stack

- Single-file HTML + CSS + vanilla JavaScript
- Installable PWA (manifest + service worker, works offline)
- LocalStorage for personal progress (never uploaded)
- Anonymous player counter via a Cloudflare Worker (stores only numbers)
- Privacy-safe viral loop via one-way hash in shared URLs

## Live demo

Play here: https://denislunev.github.io/soul-arcade-2/

## Privacy

See [privacy.html](privacy.html) — the app collects no personal data. Only an anonymous player count (numbers only) is kept.

## License

Copyright (c) 2026 Denis Lunev. All rights reserved.
