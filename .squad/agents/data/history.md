# Project Context

- **Owner:** Rames
- **Project:** Classic Snake game — fully playable in the browser. Open index.html and play.
- **Stack:** HTML, CSS, vanilla JavaScript, Canvas API. Single file. No frameworks, no build tools, no dependencies.
- **Spec:** 20×20 grid, arrow/WASD controls, score + high score (localStorage), pause/resume, mobile touch buttons, speed increases every 5 food items. Dark background, green snake, red food, retro grid lines.
- **Created:** 2026-03-29

## Learnings

<!-- Append new learnings below. Each entry is something lasting about the project. -->

### 2026-03-29 — Initial Implementation
- Built complete snake game in single self-contained `index.html` (root directory)
- All core features implemented: 20×20 grid canvas, arrow/WASD controls, score + high score persistence, pause/resume, mobile touch buttons, speed ramping
- All stretch goals included: start screen with "Press Enter to Start", trailing fade effect on snake body, crunch sound via Web Audio API (no external files)
- Game loop uses `setInterval` with dynamic speed adjustment every 5 food items
- 180° reversal prevention works by checking current direction before accepting input
- Mobile controls are CSS grid-based touch buttons, only visible on screens ≤768px
- Rendering optimizations: grid lines drawn once per frame, snake head gets glow effect, food pulses with sin wave
- High score persists via `localStorage` under key `snakeHighScore`
- Canvas is 600×600px (30px per cell × 20 grid), centered with retro green-on-dark aesthetic
- **QA APPROVED by Chunk (2026-03-29):** All 11 core requirements + 7 visual requirements + 3 stretch goals verified. Zero bugs. Production-ready.
