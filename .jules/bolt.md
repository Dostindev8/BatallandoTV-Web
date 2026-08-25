## 2026-03-29 - Critical LCP Asset Path and Preload Optimization
**Learning:** Non-existent paths (such as `video/` or `images/` instead of `assets/Batallando/`) and unencoded spaces in media asset URLs trigger 404 network failures on critical LCP media elements, significantly delaying Largest Contentful Paint.
**Action:** URI-encode space characters (e.g., `%20`) in static HTML asset paths and ensure `fetchpriority="high"` is assigned strictly to the primary LCP candidate image while correcting asset paths.
