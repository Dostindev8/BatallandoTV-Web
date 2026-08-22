## 2026-03-30 - Fix 404 asset path and space-containing media URLs
**Learning:** Hardcoded video asset paths pointing to non-existent directories (e.g. `images/SIN_FIN_-_BATALLANDO.mp4`) and unencoded space characters in asset URLs in static HTML and JS template literals cause HTTP 404 errors and block the critical asset rendering pipeline.
**Action:** Always verify media paths exist under `assets/` and ensure space characters in static and dynamic URL paths are percent-encoded (`%20`).
