## 2026-08-20 - Fix 404 Video Asset Paths in Intro Overlay
**Learning:** Hardcoded 404 media asset paths (e.g. `images/SIN_FIN_-_BATALLANDO.mp4` and `video/batallando.mp4`) prevent video readiness events (`canplay`) from firing, forcing preloader overlays to hit fallback timeout delays (3000ms).
**Action:** Audit and verify all static media asset paths in HTML and JS against actual filesystem locations in `assets/Batallando/`, ensuring proper URI encoding (`%20` for spaces) to prevent fallback timeouts and 404 errors.
