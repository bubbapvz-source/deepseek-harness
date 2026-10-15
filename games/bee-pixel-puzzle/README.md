# Bee Pixel Puzzle

Single-file browser game recreated from the "Level 200" reference screenshot.
Open `index.html` directly in a browser; there is no build step and no dependencies.

## Rules

- The picture (a pixel-art NES-style controller) starts hidden.
- Each colored block shows a number N and paints the N picture cells of its color that it owns.
- Only the block at the bottom of each column can be tapped; removing it exposes the block above.
- Every block owns a fixed set of cells, so any tap order completes the level.
- The level is won when all picture cells are painted. "Next level" generates the next seeded layout.

## Controls

- `❚❚` pauses; `» 2x` toggles faster bee and flight animation.

## Generation

Level N uses a seeded PRNG (`level * 7919 + 17`), so each level layout is reproducible.
