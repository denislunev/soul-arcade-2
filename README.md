# Soul Arcade II — GitHub Pages deploy

Upload these **6 files** to your `soul-arcade-2` repo so they sit at the **root of the served folder** (the one that becomes `https://denislunev.github.io/soul-arcade-2/`):

```
index.html      <- the game (GitHub Pages serves index.html automatically)
manifest.json   <- PWA manifest (name, icons, standalone)
sw.js           <- service worker (network-first: fresh when online, offline from cache)
icon-192.png    <- app icon
icon-512.png    <- app icon
privacy.html    <- privacy policy (link from social/store if needed)
```

## Steps (repo `soul-arcade-2`, served at `/soul-arcade-2/`)

1. Open your `soul-arcade-2` GitHub repo.
2. Upload all 6 files into the repo root (replace any existing index.html / manifest.json).
3. Commit.
4. In the repo: **Settings -> Pages** -> set source to your main branch (root), save. Wait ~1 minute.
5. Open `https://denislunev.github.io/soul-arcade-2/` on your phone - it should load, and Chrome should offer **Add to Home screen** (installable PWA).

## Verify the player counter

1. Open the game once (this sends the daily ping).
2. Open `https://soul-arcade-2-stats.denis33a1.workers.dev/stats` -> should show `players_today: 1, total_players: 1`.
3. In the game: tap **STATS** -> bottom shows **WORLDWIDE** with the same numbers.

## Updating later (avoids stale versions)

The service worker is **network-first**, so online users always get the freshest `index.html`. For a clean cache flush on a new release, bump the version string in `sw.js`:

```
const CACHE = 'soul-arcade-2-v9_18';   ->   'soul-arcade-2-v9_19';
```

Old caches self-delete on next visit.

## Notes

- `start_url` and `scope` are `.` (relative), so it works under the `/soul-arcade-2/` subpath without edits.
- The stats Worker is cross-origin and is **not** cached by the service worker - counts stay live.
- The game's share link points to `https://denislunev.github.io/soul-arcade-2` (already set in index.html).
- Your first game stays separate; this is the standalone "II" build everywhere.
- Privacy policy is at `https://denislunev.github.io/soul-arcade-2/privacy.html`.
