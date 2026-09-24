# Bolt Performance Journal

## 2026-09-24 - Fix Intro Video 404 Delay
**Learning:** In this codebase, pointing `#bb-vbg` to a non-existent video path (`images/SIN_FIN_-_BATALLANDO.mp4`) causes video load failure, which prevents `canplay` from firing and triggers a mandatory 3000ms fallback delay before revealing the intro animation.
**Action:** Always verify media paths exist in `assets/Batallando/` and use proper URL encoding to prevent unnecessary fallback delays on initial load.
