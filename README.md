# Workout
Workout App v1
# Forge

A no-fuss workout tracker. One HTML file. Drop it on GitHub Pages and it works.

## What it does

- **Comes loaded with your routine** — Push/Pull/Lower 5-day split with optional 6th day (the one you sent me, days 1–6)
- **Track workouts** — tap to log weight, reps, optional RPE. Rest timer fires automatically after every set.
- **Free-text rep targets** — "near failure", "30-60 sec", "8-12/leg" all work as rep targets, not just numeric ranges
- **Custom exercises anywhere** — three places to add them: inside the routine editor's exercise picker, inside the in-session "Add exercise" sheet, and from Settings → Add custom exercise. Pick a muscle group and equipment type.
- **Auto-rotation** — Home tab's "Up next" cycles through your days based on history, skipping Day 3 (Rest) automatically
- **Review history** — every session saved with full set-by-set detail and total volume
- **Export/Import** — back up your data as JSON
- **Offline** — once loaded, no network needed. Everything in localStorage.

## Your seeded routine

- **Day 1** — Upper A (chest + delts + lats)
- **Day 2** — Lower A (glute + quad)
- **Day 3** — Rest / Cardio / Mobility (notes shown, no logging)
- **Day 4** — Upper B (back + arms + chest support)
- **Day 5** — Lower B (athletic lower + abs)
- **Day 6** — Delts + Arms + Abs specialization (optional)

Every exercise from your spec is pre-seeded — Smith variants, low-to-high cable fly, neutral-grip pulldown, single-arm cable pulldown, FFE Smith lunge, FFE split squat, Smith hip thrust, cable hamstring curl, stability ball hamstring curl, farmer carries, rope pushdown, overhead cable triceps extension, rear delt cable fly, cable lateral raise, cable crunch, hanging leg raise.

## Deploy to GitHub Pages

1. Create a new GitHub repo (e.g. `forge`)
2. Drop `index.html` in the root
3. Settings → Pages → Source: `main` branch, `/` (root) → Save
4. Wait ~1 minute, visit `https://YOUR-USERNAME.github.io/forge/`
5. On iPhone: open in Safari → Share → **Add to Home Screen** — launches fullscreen like a native app

## Local testing

Just open `index.html` in any browser. No build step, no server, no dependencies.

```bash
# Or run a local server (Python):
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Adding a custom exercise mid-workout

In Train, tap **+ Add exercise** at the bottom of the session → **+ Add custom exercise** at the top of the sheet → type the name, pick muscle group and equipment → tap Add. It drops straight into your current session AND stays in the library for future use.

## Data & backups

Everything saves to `localStorage` under the key `forge_v1`. Clearing your browser data will wipe it — use **Settings → Download backup** before clearing. The backup file restores from any device or browser.

## Editing your routine

Routines tab → tap the pencil icon on the routine card. From there you can:
- Rename the routine, change goal, change days/week
- Add/remove/rename days
- Add/remove/reorder exercises within each day
- Edit sets and reps target (free-text, so "near failure" works)

Or tap the three-dot menu on a routine card to duplicate or delete it.
