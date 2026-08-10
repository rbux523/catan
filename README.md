# Catan Dice Tracker

A lightweight, browser-based tracker for Catan dice rolls. Record each roll as it happens, compare the game against expected two-dice probabilities, and explore streaks, droughts, and turn-by-turn history.

## Pages

- `index.html` — live game tracker with roll buttons, distribution chart, current leaders, active droughts, recent rolls, undo, and new-game controls.
- `advanced-stats.html` — sortable per-number statistics, leaderboard cards, streaks, droughts, and the full roll log.

## Use it

Open `index.html` in a modern browser, then tap or click the rolled total from 2–12. Each game's history is stored in its URL, so the browser's normal copy or share action sends the exact game state.

- **Undo** removes the most recently recorded roll.
- **New game** opens a fresh game in a new tab, leaving the current game untouched.
- **View advanced stats** carries the same game history into the detailed view.

## Example games

- [Example game 1](https://rbux523.github.io/catan/index.html#r=2584b8ab8666994bb6649962455367577326457bb959bbb86a7696a2385738c779938bb7)
- [Example game 2](https://rbux523.github.io/catan/index.html#r=a95599b79b898c69586787b8933898776675956a38835677647ab676753bb47a5bc48779)
- [Example game 3](https://rbux523.github.io/catan/index.html#r=ab43397673665597778576bb86899b4699a5a49957b7a567baa6975c7b5587a59459845b)
- [Example game 4](https://rbux523.github.io/catan/index.html#r=a88476a5477a285769625654ca9927765bcb6757b7a37a57c96739738a94a7843876886b)
- [Example game 5](https://rbux523.github.io/catan/index.html#r=44a787aa7c584879ba77a876883cb779b9942838578a4a86495a6787b2c7a6b84a584378)

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
