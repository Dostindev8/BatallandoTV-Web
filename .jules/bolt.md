## 2026-10-21 - Eliminate 3s Intro Video Fallback Delay via Correct Pathing
**Learning:** Failing to load the `#bb-vbg` intro video caused a 3000ms JavaScript fallback timeout before revealing the intro sequence. Fixing the path from `images/SIN_FIN_-_BATALLANDO.mp4` to `assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4` allows the `canplay` event listener to fire immediately, eliminating a mandatory 3-second initialization delay.
**Action:** Always check JavaScript fallback timeout logic when diagnosing media loading bottlenecks to quantify time saved by fixing broken asset paths.
