# Classic Snake Game — AI Agent Brief

**Project:** Build a fully playable classic Snake game in the browser using HTML, CSS, and vanilla JavaScript. No frameworks, no build tools — just open `index.html` and play.

## Gameplay Rules

- Snake starts at the center of the grid, moving right, length of 3 segments
- Player controls direction with arrow keys (or WASD)
- A food item appears at a random empty cell
- Eating food grows the snake by 1 segment and increases the score by 10
- Snake dies if it hits a wall or its own body
- Game shows a "Game Over" screen with final score and a restart option
- Speed increases slightly every 5 food items eaten

## Visual Requirements

- Grid-based canvas (20×20 cells recommended)
- Dark background, bright green snake, red food
- Display current score in the top-left corner
- Display high score (persisted in `localStorage`) in the top-right corner
- Subtle grid lines for retro feel
- Smooth, centered layout that works on any screen size

## Technical Requirements

- Single `index.html` file containing all HTML, CSS, and JS (self-contained)
- Use `<canvas>` element for rendering
- Game loop via `setInterval` with adjustable tick rate
- Prevent 180° reversals (e.g., can't go left while moving right)
- Pause/resume with Spacebar, show "PAUSED" overlay
- Mobile-friendly: add on-screen arrow buttons for touch devices

## File Structure

```
snake-game/
└── index.html    ← everything in one file
```

## Stretch Goals (optional, only if core is solid)

- Add a start screen with a "Press Enter to Start" prompt
- Add a trailing fade effect on the snake body
- Add a crunch sound effect on eating (using Web Audio API, no external files)

## What NOT to do

- No external dependencies or CDN links
- No TypeScript, no bundlers
- No server — it must work by opening the HTML file directly
