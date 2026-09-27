## 2026-05-03 - Eliminate 3s intro delay by resolving 404 video asset path
**Learning:** In `index.html`, `#bb-vbg` video loading failure triggers a mandatory 3000ms `canplay` fallback timeout that delays intro initialization; correcting broken video source paths prevents 404 errors and saves 3000ms on first load.
**Action:** Always verify local media file paths exist under `assets/Batallando/` with URI-encoded spaces before using them in video tags or JS handlers.
