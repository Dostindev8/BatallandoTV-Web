## 2025-05-18 - Optimized LCP and Lazy Loading
**Learning:** Identified that critical Largest Contentful Paint (LCP) assets like the intro video background were broken (404) and lacked performance attributes. Correctly URI-encoding filenames with spaces is essential for robustness in static sites.
**Action:** Always verify asset paths and use `fetchpriority="high"` for LCP candidates while ensuring `loading="lazy"` and `decoding="async"` for below-the-fold content.

## 2025-05-18 - Playwright Verification and Cleanup
**Learning:** `requestfailed` events in Playwright can occur normally for media assets (NS_BINDING_ABORTED) due to browser prefetching strategies. Artifacts like `server.log` must be explicitly removed before submission to avoid leaking local environment data.
**Action:** Filter Playwright error logs for critical failures and always run a final `ls` to ensure no temporary verification artifacts remain in the repo.
