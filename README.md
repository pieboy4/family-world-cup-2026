# Family World Cup 2026 Predictor — Phase 2 Final

Upload `index.html`, `data.json`, and `README.md` to the existing GitHub Pages repository.

## Links

- Public view-only page: normal GitHub Pages URL
- Dietrich edit page: add `?edit=1`

## Workflow

1. Open the edit link.
2. Enter predictions and scores visually.
3. Click `Export data.json`.
4. Replace `data.json` in GitHub.
5. Commit changes.
6. Family refreshes the public link.

## Phase 2 Final features

- Group-stage predictions and scores preserved from existing data.json.
- Full Round of 32 populated.
- Knockout stage uses W/L only.
- Knockout bonus system:
  - Correct = 3
  - 2nd consecutive correct, non-leader = 6
  - 3rd consecutive correct, non-leader = 8
  - Wrong resets streak
  - Streak resets after third correct
  - Current leader excluded from streak bonuses
- Leaderboard shows base, KO bonus, total and streak.
- Bonus log included.
- Printable tournament bulletin included.

- Correct predictions are highlighted red on completed matches, including historical group-stage games.

- Printable Tournament Bulletin + Knockout Rules is collapsed by default.
- Default match view shows knockout stage only; group-stage matches remain available via filters.

## Phase 2.3 scoring/streak fix

- Knockout scoring is processed strictly in FIFA match-number order.
- Unfinished knockout matches are ignored for streak and bonus calculations.
- Drawn knockout matches only count once the Penalties box contains W or L.
- Penalty results display as Result: W (Pens) or Result: L (Pens).
- Leader is excluded from streak bonuses and does not build a visible KO bonus streak.
- Leaderboard now shows Last Bonus as well as active KO Streak.
- Existing historical scores, predictions and penalties are preserved.

## Phase 2.4 render fix

- Restored missing helper functions required for match rendering: teamHtml, flagFor, isPlaceholder and validChoices.
- Fixed the JavaScript error `teamHtml is not defined`.
- Kept FIFA match-number ordering.
- Kept default view as Knockout stage only.
- Preserved all existing scores, predictions and penalties from the uploaded data.json.
