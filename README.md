# Soul Arcade II

An arcade-style name vibe reader — the standalone sequel. Type a name and get its vibe verdict, battle two names head-to-head, or guess the hidden daily name. Pure math, no mysticism, no personal data.

## How it works

- Type any English letters and get one of 101 fun verdicts
- The app maps the input deterministically — same input always gives the same verdict
- Three modes: **SOLO** (vibe verdicts), **VS** (rock-paper-scissors duels), **GUESS** (daily Wordle-style name)
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
