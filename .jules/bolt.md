# Bolt's Performance Journal

This is a journal of performance optimizations made in the Batallando codebase.

## 2026-03-31 - Initial Setup
**Learning:** This repository is a static site where assets are primarily located in the 'assets/Batallando/' directory and the UI is rendered via static HTML and client-side JavaScript.
**Action:** Always verify assets exist in 'assets/Batallando/' and use correct path mappings. Ensure relative URLs are used.

## 2026-07-29 - Fixed 404 Media Paths and Optimized Critical LCP Priorities
**Learning:** Hardcoded asset directories like `images/` or `video/` often do not exist in the repository structure (which stores resources under `assets/Batallando/`), leading to expensive, redundant 404 network requests during preloading or background video play attempts. Additionally, setting `preload="auto"` on full-length background videos blocks critical LCP image downloads on slow networks, and DOM queries without null guards can easily trigger uncaught JS crashes.
**Action:** Audit all asset paths recursively to ensure correctness, URI-encode media paths with spaces, set `preload="metadata"` for background/autoplay videos to conserve client bandwidth, use preloads with `fetchpriority="high"` strictly for the above-the-fold LCP image, and always guard element class/style manipulations with null checks.
