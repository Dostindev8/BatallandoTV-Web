## 2026-03-30 - Fixing broken media asset paths to eliminate fallback timeouts

**Learning:** Broken relative paths for background hero videos (such as `video/batallando.mp4` or non-URI encoded paths) result in 404 network errors and trigger fallback delays, stalling LCP media loading.
**Action:** Always verify relative media paths match `assets/Batallando/` and URI-encode filenames with spaces to ensure zero-delay resource fetching.
