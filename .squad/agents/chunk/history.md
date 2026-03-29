# Project Context

- **Owner:** Rames
- **Project:** Classic Snake game — fully playable in the browser. Open index.html and play.
- **Stack:** HTML, CSS, vanilla JavaScript, Canvas API. Single file. No frameworks, no build tools, no dependencies.
- **Spec:** 20×20 grid, arrow/WASD controls, score + high score (localStorage), pause/resume, mobile touch buttons, speed increases every 5 food items. Dark background, green snake, red food, retro grid lines.
- **Created:** 2026-03-29

## Learnings

<!-- Append new learnings below. Each entry is something lasting about the project. -->

### 2026-03-29 — Initial QA Review
- **Verified:** All spec requirements implemented correctly — core gameplay, visuals, technical requirements, and all stretch goals
- **Edge cases tested:** 180° reversal prevention works correctly (checks current `direction` not `nextDirection`), food spawning validates against snake body, pause disabled during game over, speed increase has sensible floor
- **Code quality:** Clean state machine with 4 states (start/playing/paused/gameOver), proper direction buffering prevents missed inputs, collision detection efficient and correct
- **Pattern learned:** Direction buffering (`nextDirection` vs `direction`) is critical for responsive controls — queues input without allowing 180° exploits
- **Result:** APPROVED — no bugs found, production-ready implementation
