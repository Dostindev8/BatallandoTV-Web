## 2026-09-11 - Fix Broken Asset Paths Causing Network 404 Delays
**Learning:** Hardcoded asset paths referencing non-existent directories (like `images/SIN_FIN_-_BATALLANDO.mp4` or `video/batallando.mp4`) cause 404 network errors and trigger 3-second timeout fallbacks during media initialization.
**Action:** Always scan for media/video assets using regex and verify that all video sources point to valid files within `assets/Batallando/` with URI-encoded spaces.
