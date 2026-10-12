## 2026-03-30 - Broken media resource paths trigger intro fallback delay
**Learning:** A broken path to `#bb-vbg` (`images/SIN_FIN_-_BATALLANDO.mp4`) causes a 3000ms `canplay` fallback timeout in JavaScript, significantly delaying initial interactive rendering.
**Action:** Always verify local media paths exist and use URI-encoded spaces (e.g., `assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`) to avoid mandatory timeout fallbacks and 404 errors.
