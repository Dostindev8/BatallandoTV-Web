## 2026-05-03 - [Fix 404s and optimize critical asset loading]
**Learning:** Broken asset paths (404s) on critical LCP candidates and primary media (video) significantly degrade perceived performance and resource scheduling. Static sites without build pipelines are prone to URI encoding issues with filenames containing spaces.
**Action:** Always URI-encode asset paths and use automated recursive scans to identify and optimize all asset loading strategies (fetchpriority/lazy-loading) across the codebase.
