## 2026-03-31 - Fix 404 Video Paths & URI Encode Assets
**Learning:** Incorrect relative video paths (like `video/batallando.mp4` or `images/SIN_FIN_-_BATALLANDO.mp4`) and unencoded spaces in media asset URLs cause 404 network request failures, blocking LCP/media preloads and stalling resource fetching in static client-rendered sites.
**Action:** Ensure all media resource paths point accurately to valid subdirectories (`assets/Batallando/`), omit leading slashes for relative site deployments, and URI-encode filenames with spaces (e.g., `%20`).
