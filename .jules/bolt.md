## 2026-05-03 - URI Encoding and Preloading for Critical Media Assets
**Learning:** Hardcoded asset paths containing unencoded spaces (e.g. `SIN FIN - BATALLANDO.mp4` or `Batallando TV 2024.png`) or non-existent directories (`images/` or `video/`) cause silent 404 network failures and resource discovery delays during initial LCP render.
**Action:** Always URI-encode media paths (`%20`), fix non-existent directory references to `assets/Batallando/`, and add `<link rel="preconnect">` and `<link rel="preload">` in `<head>` for critical LCP candidate images and intro video backgrounds.
