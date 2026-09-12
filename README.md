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
