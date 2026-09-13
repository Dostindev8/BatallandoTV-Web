## 2026-09-13 - Broken Media Asset Path Causing 404 Delay
**Learning:** Hardcoded asset references in HTML pointing to non-existent directories like `images/` cause browser network request failures (404), blocking parallel asset downloads and degrading load times for critical media assets.
**Action:** Scan for broken media paths in `index.html` and verify that all asset paths point to `assets/Batallando/` with proper URL encoding (`%20` for spaces).
