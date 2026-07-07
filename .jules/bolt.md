## 2026-05-03 - LCP Optimization and URI Robustness
**Learning:** In static sites with manually handled assets, filenames with spaces (e.g., 'SIN FIN - BATALLANDO.mp4') cause silent 404s if not URI-encoded in HTML/JS, severely impacting LCP.
**Action:** Always URI-encode asset paths and use `fetchpriority="high"` with `preload` for hero media to ensure the browser prioritizes critical resources immediately.
