## 2026-05-18 - Fix broken media paths to eliminate fallback timeouts

**Learning:** Broken media asset paths (e.g., `images/SIN_FIN_-_BATALLANDO.mp4` returning 404) fail `canplay` events and force the JS runtime into a 3000ms fallback timeout before completing page/intro initialization.
**Action:** Ensure all media paths in HTML/JS template literals accurately point to valid asset locations and are properly URI-encoded to avoid network 404 errors and preventable 3-second render delays.
