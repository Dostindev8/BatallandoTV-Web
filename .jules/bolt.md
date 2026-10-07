## 2026-03-28 - Broken Video Path Triggers 3s Fallback Delay
**Learning:** In this application, `#bb-vbg` video element loaded a missing URL (`images/SIN_FIN_-_BATALLANDO.mp4`), triggering a 3000ms `canplay` fallback timeout in JavaScript before intro initialization could complete.
**Action:** Always verify video asset URLs in HTML markup to prevent mandatory fallback timeouts during load.
