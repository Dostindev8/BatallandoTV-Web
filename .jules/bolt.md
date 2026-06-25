## 2026-05-03 - Resource Prioritization & Path Fixes
**Learning:** Identifying and fixing 404 errors for critical LCP assets is a primary performance optimization in this codebase. Resource hints like preconnect and preload significantly improve the discovery of critical assets.
**Action:** Always verify asset paths and use URI encoding for filenames with spaces. Prioritize above-the-fold content with fetchpriority and preload.
