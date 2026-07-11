## 2026-05-21 - LCP Optimization and URI Encoding
**Learning:** In this static repository, 404 errors on critical assets (intro video and hero image) were significantly inflating LCP. Fixing these through URI encoding and applying `fetchpriority="high"` only to the most critical LCP candidate (the hero image) reduced LCP from ~6.2s to ~0.5s.
**Action:** Manually verify that all asset paths in HTML/JS template literals are URI-encoded and that `fetchpriority` is not over-applied, which can lead to resource contention in Chromium.
