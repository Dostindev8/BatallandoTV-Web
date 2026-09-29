## 2026-03-30 - Fix Broken Intro Video Path to Bypass 3000ms Initialization Delay
**Learning:** In this codebase, pointing `#bb-vbg` to a missing file triggers a 404 error and relies on a 3000ms fallback timeout in JavaScript before showing the intro content.
**Action:** Always ensure `#bb-vbg` and other critical media elements point to valid, URI-encoded paths in `assets/Batallando/` to allow `canplay` to fire immediately and prevent mandatory timeout delays.
