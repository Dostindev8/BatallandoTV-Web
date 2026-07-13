## 2026-03-24 - [LCP Optimization and Asset Robustness]
**Learning:** Identifying and fixing 404 errors for critical LCP candidates (like background videos and hero images) is the most impactful first step in a legacy static codebase. Additionally, using `fetchpriority="high"` and removing `decoding="async"` on the primary hero image significantly improves the LCP metric.
**Action:** Always verify asset paths for URI encoding (especially spaces) and selectively apply `fetchpriority="high"` to the single most critical LCP candidate to avoid resource contention.
