# Fantasy Baseball 2026 – HR & K Tracker

Live stats tracker that auto-updates every Sunday at 10pm PST using the free MLB Stats API.

## Deploy to Netlify (5 minutes)

1. **Create a GitHub repo** and push this folder to it:
   ```bash
   git init
   git add .
   git commit -m "Fantasy Baseball Tracker 2026"
   git remote add origin https://github.com/YOUR_USERNAME/fantasy-baseball-2026.git
   git push -u origin main
   ```

2. **Go to [netlify.com](https://netlify.com)** → "Add new site" → "Import an existing project"

3. **Connect your GitHub repo** and deploy with these settings:
   - Build command: *(leave blank)*
   - Publish directory: `.`

4. **Done!** Share the Netlify URL with your league.

## How it works

- Pulls live stats from `statsapi.mlb.com` — MLB's free public API, no key needed
- The page auto-refreshes stats every Sunday at 10pm PST
- Leaderboards rank all 8 managers by total HRs (batters) and total Ks (pitchers)
- Each team shows their 9 batters (HR tracking) and 4 pitchers (K tracking)

## Updating rosters mid-season

If you need to update a player (injury, trade, drop), edit the `TEAMS` array in `index.html`.
Each player has a `name`, `pos`, and `id` (MLB player ID from statsapi.mlb.com).

To find a player's MLB ID:
```
https://statsapi.mlb.com/api/v1/people/search?names=PLAYER+NAME&sportId=1
```
