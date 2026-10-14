## 2026-03-30 - Fix Broken Video Assets to Avoid Mandatory JS Fallback Timeout
**Learning:** In this codebase, failing to load the background video (`#bb-vbg`) causes a 404 error, preventing the `canplay` DOM event from firing. The intro script relies on `canplay` to initialize page animations and falls back to a hardcoded 3000ms delay (`setTimeout`) when `canplay` fails to fire within 3 seconds.
**Action:** Always verify video asset URLs in HTML/JS templates first; fixing broken media paths eliminates mandatory multi-second initial render delays without touching core UI timing logic.
