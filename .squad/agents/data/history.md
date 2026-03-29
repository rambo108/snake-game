# Project Context

- **Owner:** Rames
- **Project:** Classic Snake game — fully playable in the browser. Open index.html and play.
- **Stack:** HTML, CSS, vanilla JavaScript, Canvas API. Single file. No frameworks, no build tools, no dependencies.
- **Spec:** 20×20 grid, arrow/WASD controls, score + high score (localStorage), pause/resume, mobile touch buttons, speed increases every 5 food items.
- **Theme:** Minecraft — dirt-brown background, Creeper-green snake with pixel-art face, red apple food, stone-gray grid, "You Died!" death screen, square-wave pickup sound.
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

### 2026-03-29 — Minecraft Theme Retheme
- Full visual retheme to Minecraft style; zero gameplay logic changes
- Snake body uses Creeper green (#5DA130) with 3D block edge rendering (highlight top/left, shadow bottom/right)
- Snake head draws a Creeper face via 5×5 pixel grid (6px per pixel) — eyes, nose bridge, mouth
- Food is a pixel-art red apple with stem + leaf, using layered rectangles for highlight/shadow
- Canvas background: dirt brown (#59422D) with per-cell texture variation via deterministic hash
- Grid lines: stone-gray at low alpha for subtle block separation
- Page background: earthy brown (#3C2A14) with CSS repeating-linear-gradient block grid
- Canvas border: multi-layer stone-gray box-shadow simulating Minecraft UI frame
- Overlays: dark earth-toned semi-transparent bg; title in Creeper green; death screen "You Died!" in red (#AA0000) via `.death` CSS class
- Touch buttons: stone-gradient with beveled border-color trick (lighter top/left, darker bottom/right)
- Sound changed from sine sweep to square-wave rising bloop (chiptune Minecraft pickup style)
- Score display: yellow (#FFFF55) with letter-spacing and text-shadow for blocky feel
- Approach: all pixel art drawn programmatically with canvas fillRect — no external assets
- `overlayTitle.className` used to toggle between default (green) and death (red) h1 styles
