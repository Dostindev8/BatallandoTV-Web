## 2026-10-24 - Fix broken intro video asset path to bypass 3000ms canplay fallback delay
**Learning:** In `index.html`, when the background video `#bb-vbg` path was set to a non-existent file (`images/SIN_FIN_-_BATALLANDO.mp4`), it failed to fire `canplay`, triggering a mandatory 3000ms fallback timeout in `index.html`'s intro initialization script.
**Action:** Correct media source paths to valid URI-encoded relative assets (`assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`) so `canplay` fires instantly without falling back to the 3-second delay timer.
