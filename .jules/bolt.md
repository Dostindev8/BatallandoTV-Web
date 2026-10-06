## 2026-10-06 - Fixing 404 intro video path prevents 3000ms JS delay
**Learning:** In this codebase, the background video element `#bb-vbg` had a broken source `images/SIN_FIN_-_BATALLANDO.mp4` resulting in a 404 response. When `canplay` failed to fire, a 3000ms timeout fallback in JavaScript ran before initializing the intro overlay.
**Action:** Always URI-encode and check media paths under `assets/Batallando/` to ensure zero HTTP 404 errors and eliminate fallback delays during critical intro sequences.
