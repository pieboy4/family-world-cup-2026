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

## Phase 2.5 bonus log wording

- Bonus Log now shows the full total points earned for the match and the extra streak bonus.
- Example: `Poppy Match 74: 6 pts total — includes +3 streak bonus`.
- Existing scores, predictions and penalties are preserved.

## Phase 2.5 RC1 release-candidate validation

This build was packaged as a release candidate after regression checks for:
- data preservation,
- required helper functions,
- JavaScript syntax,
- normal view render simulation,
- edit-mode render simulation,
- default knockout view,
- group-stage filter availability,
- knockout scores, predictions and penalties.

## Phase 2.6 RC2 automatic knockout winner propagation

- Known winners from completed knockout matches automatically replace future `Winner Match X` placeholders.
- Known losers from completed knockout matches automatically replace future `Loser Match X` placeholders.
- The original placeholder is retained in small grey text for auditability.
- Search includes both original placeholder text and resolved team names.
- Existing historical scores, predictions, penalties and calculated points are preserved.
- This display feature does not mutate `data.json`.

## Phase 2.7 RC3 Match 89/90 fixture correction

- Corrected the Round of 16 fixture mapping:
  - Match 89 = Winner Match 74 vs Winner Match 77.
  - Match 90 = Winner Match 73 vs Winner Match 75.
- This preserves all historical scores, predictions, penalties and calculated points.
- Automatic winner propagation now displays:
  - Match 89 = Paraguay vs Winner Match 77.
  - Match 90 = Canada vs Morocco.
