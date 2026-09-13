# Moon Cresta

A browser-based homage to the 1980 Nichibutsu arcade classic *Moon Cresta*, built as a single self-contained HTML5 canvas game (`index.html`, no build step, no dependencies beyond a Google web font).

## Play

Open `index.html` in a browser.

- **Move:** Arrow keys or `A` / `D`
- **Fire:** `Space`
- **Pause:** `P`
- Touch controls supported on mobile (tap lower half to steer, upper half to fire).

## The docking mechanic

The defining feature of the original game: clear a formation and a bonus unit descends from the top of the screen. Line your ship up underneath it as it passes your altitude to **dock** — fusing it onto your ship, widening your firepower (single shot → twin shot → three-way spread), and advancing your ship through stages 1 → 2 → 3.

Getting hit while fused peels off the outermost segment instead of costing a life outright; only a hit while flying as a bare stage‑1 ship costs a life.

## Structure

Enemy waves scale in size, speed, and enemy "class" toughness as you progress; enemies enter in a swooping formation pattern, hold position with light formation drift and pot-shots, then periodically peel off into dive-bombing runs before looping back.

Score and high score (persisted via `localStorage`) are shown in the HUD along with the current wave and remaining lives.

---

# Zac's Timestable Space Station

A single-file times tables game for a UK Year 4 child (`zacs-timestable-space-station.html`, no build step, no dependencies beyond Google Fonts). Open the file in a browser, or play it at the published link.

## Play

Pick a table (×2 to ×12), a **Random Mix** across all tables, or a **Boss Mix** of the facts Year 4 finds hardest (6, 7, 8, 9, 11, 12). Ten questions a round, answered on a keypad. Score, live accuracy and streak sit in the HUD; the debrief gives accuracy, score, average answer speed, a rank and a list of every fact missed.

## Design rules behind the maths

- **Multipliers run 2–12, not 1–12.** `×1` is not a fact worth one of ten slots and it inflates accuracy.
- **Facts are sampled without replacement**, so a round never repeats a question and never escalates 1, 2, 3…
- **One attempt per question.** Accuracy is first-attempt only, so the figure means something. Missed facts return in an optional **Fix-It round** that does not touch the recorded score.
- **A wrong answer shows a strategy, not a cross** — `4 × 12` prompts "4 × 10 = 40, plus 4 × 2 = 8" rather than just the answer.
- **Turbo timer** (off by default) gives 6 seconds a question, matching the statutory Year 4 Multiplication Tables Check.
- **Flip it round** (on by default) asks both `12 × 3` and `3 × 12`, so commutativity gets rehearsed.

Best accuracy per table and a running tally of missed facts persist via `localStorage`; the home screen surfaces the six facts missed most often as **Facts to nail**.
