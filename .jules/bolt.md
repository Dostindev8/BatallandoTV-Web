## 2026-09-22 - Fix Broken Intro Video Source Path
**Learning:** A broken media path (`images/SIN_FIN_-_BATALLANDO.mp4`) in static HTML causes `vbg.addEventListener('canplay', ...)` to never trigger, forcing JavaScript to hit a mandatory 3000ms `canplay` fallback timeout that delays intro initialization.
**Action:** Always verify that background video sources in static HTML point to valid, URI-encoded asset paths (`assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`) to avoid triggering mandatory fallback delays in JS.
