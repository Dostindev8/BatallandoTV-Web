## 2026-03-30 - Fix broken intro video path to eliminate 3000ms JS fallback timeout
**Learning:** In this codebase, `index.html` attaches a 3000ms timeout fallback in `revealIntro()` when `#bb-vbg` video fails to trigger `canplay`. A broken media path (`images/SIN_FIN_-_BATALLANDO.mp4` resulting in 404) enforced this full 3s delay on every page load.
**Action:** Ensure all media paths point directly to valid assets under `assets/Batallando/` and are URI-encoded.
