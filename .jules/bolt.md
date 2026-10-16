## 2026-10-16 - Fix Intro Video 404 & 3s Delay
**Learning:** A broken path for `#bb-vbg` (`images/SIN_FIN_-_BATALLANDO.mp4`) causes a 404 error and forces JS to wait out a full 3000ms `canplay` fallback timeout before triggering `revealIntro()`.
**Action:** Point `#bb-vbg` directly to `assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4` to eliminate the 404 error and allow immediate `canplay` intro initialization.
