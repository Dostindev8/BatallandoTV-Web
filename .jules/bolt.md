# Bolt's Performance Journal - Critical Learnings Only

## 2026-06-18 - Manual Asset Encoding and LCP Priority
**Learning:** In static sites lacking a build pipeline, asset paths with spaces (e.g., "Intro Video.mp4") fail to load in many environments unless manually URI-encoded ("Intro%20Video.mp4"). Additionally, for sites using JS template literals for rendering, performance attributes like `loading="lazy"` must be manually included in the strings, and `fetchpriority="high"` is essential for critical video assets to ensure they are prioritized by the browser's preload scanner.
**Action:** Manually URI-encode all asset paths in both HTML and JS files and always apply explicit `fetchpriority` to the main "hero" media (video or image) to optimize LCP.
