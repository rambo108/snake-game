# Minecraft Theme Applied

**Date:** 2026-03-29  
**Author:** Data  
**Type:** Visual retheme  

**Decision:** Rethemed entire snake game to Minecraft visual style per Rames's request.

**What changed:**
- All colors, rendering, overlays, buttons, and sound switched to Minecraft palette
- Zero gameplay logic modified — grid size, speed, controls, scoring all identical
- All pixel art is programmatic (canvas fillRect) — no external assets added
- Still a single self-contained `index.html`

**Team notes:**
- The `.death` CSS class on `overlayTitle` toggles the red "You Died!" style; `className = ''` resets it on pause
- If adding new overlay states, remember to manage the `className` on `overlayTitle`
