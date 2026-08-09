# Catan Dice Tracker

A lightweight, browser-based tracker for Catan dice rolls. Record each roll as it happens, compare the game against expected two-dice probabilities, and explore streaks, droughts, and turn-by-turn history.

## Pages

- `index.html` — live game tracker with roll buttons, distribution chart, current leaders, active droughts, recent rolls, undo, and new-game controls.
- `advanced-stats.html` — sortable per-number statistics, leaderboard cards, streaks, droughts, and the full roll log.

## Use it

Open `index.html` in a modern browser, then tap or click the rolled total from 2–12. The tracker automatically saves the current game in browser `localStorage`.

- **Undo** removes the most recently recorded roll.
- **New game** clears the saved game after confirmation.
- **View advanced stats** opens the detailed view using the same saved game data.

## How expected values work

The tracker uses normal two six-sided dice probabilities. For example, a 7 has six combinations out of 36 and is expected more often than a 2 or 12, which each have one combination out of 36.

Expected count is calculated as:

```text
total rolls × (ways to roll that number ÷ 36)
```

## Run locally

No build step or dependencies are required. Open `index.html` directly, or serve the repository with any static-file server.

```bash
python3 -m http.server
```

Then visit `http://localhost:8000`.

## Deploy with GitHub Pages

This repository is static HTML, CSS, JavaScript, and image assets, so it can be deployed directly through GitHub Pages.

1. Push the repository to GitHub.
2. In the repository, open **Settings → Pages**.
3. Choose the branch and `/ (root)` as the publishing source.
4. Visit the published URL once deployment completes.

The project includes Open Graph and Twitter metadata plus `social-preview.png`, so shared GitHub Pages links can display a rich preview image.

## Project assets

- `favicon.svg` — browser tab icon.
- `social-preview.png` — social-sharing preview artwork.
