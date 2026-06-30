## 2026-05-20 - [LCP Asset Optimization & Path Fixes]
**Learning:** Identifying and fixing 404 errors for critical Largest Contentful Paint (LCP) assets is a primary performance win in static sites. In this repo, URI-encoding asset paths (especially those with spaces) in JavaScript template literals is essential for robustness as there is no build-time processing.
**Action:** Always verify asset paths in both static HTML and dynamic JS templates; prioritize 'fetchpriority="high"' for above-the-fold media elements to minimize LCP.
