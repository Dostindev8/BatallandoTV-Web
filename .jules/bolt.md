## 2026-07-06 - Critical Path Resource Prioritization
**Learning:** Identifying and fixing 404 errors for LCP assets while simultaneously using fetchpriority and preconnect hints can yield significant LCP improvements (~28% reduction in this case). URI-encoding asset paths with spaces is crucial for robust resource loading in static environments.
**Action:** Always profile network requests first to identify broken critical paths, then apply resource hints and encoding fixes to ensure the browser prioritizes the most important content.
