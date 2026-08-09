# Bolt's Performance Journal

## 2026-08-09 - Static Media Assets 404 Mitigation and Resource Optimization
**Learning:** Hardcoded non-existent asset paths (like `video/batallando.mp4`) and broken relative paths (like `images/SIN_FIN_-_BATALLANDO.mp4` instead of `assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`) cause significant blocking delay during browser page initialization. Fixing these prevents resource load contention and unnecessary 404 network overhead.
**Action:** Always verify all media file paths in static HTML templates, ensure spaces are properly URI-encoded to `%20`, and use relative formats without leading slashes.
