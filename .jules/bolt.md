# Bolt's Performance Journal

## 2026-06-21 - Initial Repository Audit
**Learning:** Found multiple critical performance issues: 404 on the intro LCP video due to incorrect path (`images/` instead of `assets/Batallando/`), missing URI encoding for assets with spaces causing potential loading failures, and missing resource hints (preconnect, fetchpriority). A 26MB video is used as a background in multiple places, making cache hits critical; however, inconsistent path formatting (spaces vs encoded) prevents efficient caching.
**Action:** Always URI-encode asset paths and maintain consistent relative formatting. Prioritize fixing the LCP asset path and adding `fetchpriority="high"`.
