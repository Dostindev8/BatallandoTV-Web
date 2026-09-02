## 2026-03-31 - Unencoded media asset paths cause hidden 404 failures and JS fallback delays
**Learning:** In static single-page apps without a build tool, broken or unencoded media URLs in `index.html` (e.g., `images/SIN_FIN_-_BATALLANDO.mp4` or paths with unencoded spaces) silently fail, delaying background media initialization until JS timeout fallbacks trigger.
**Action:** Always URI-encode asset paths containing spaces (`%20`), verify local media file existence against DOM source elements, and test all media URLs against local server response codes.
