# Bolt Performance Journal

## 2026-11-01 - Fix 404 Video Source Triggering 3000ms Fallback Timeout
**Learning:** In `index.html`, the intro background video `#bb-vbg` was referencing a non-existent path `images/SIN_FIN_-_BATALLANDO.mp4` instead of `assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`. Because the video failed to load with a 404 error, the `canplay` event was never fired, forcing the intro reveal sequence to wait for the 3000ms JavaScript fallback timeout (`setTimeout(revealIntro, 3000)`).
**Action:** Always ensure media assets point to existing relative URI-encoded paths in `assets/Batallando/`. This eliminates 404 requests and prevents execution delays caused by fallback timeouts awaiting media readiness events.
