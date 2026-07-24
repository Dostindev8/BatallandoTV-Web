# Bolt Performance Journal

## 2026-05-03 - URI Encoding and Asset Prioritization
**Learning:** Hardcoded asset references with unencoded spaces or incorrect path prefixes (e.g. `images/SIN_FIN_-_BATALLANDO.mp4` instead of `assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`) trigger immediate 404 network errors, completely breaking critical media loading and degrading the Largest Contentful Paint (LCP) performance. Preloading key LCP images and background videos while setting their correct resource scheduling attributes (like `fetchpriority="high"`, `loading="eager"`, and using `preload="metadata"` for autoplay background videos) is the most impactful speed optimization for this client-side rendered codebase.
**Action:** Always URI-encode spaces in filenames as `%20` in HTML/JS, replace wrong folders like `images/` or `video/` with `assets/Batallando/`, and load critical above-the-fold assets eagerly using `fetchpriority="high"`.
