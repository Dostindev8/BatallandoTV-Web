# Bolt's Performance Journal

## 2026-02-15 - Missing Intro Video Blocks Immediate Startup
**Learning:** In `index.html`, the intro modal `#bb-intro` loads `#bb-vbg`. When `<source src="images/SIN_FIN_-_BATALLANDO.mp4">` fails with 404, `vbg` never fires `canplay`, triggering a mandatory 3000ms fallback timeout before the intro UI (`revealIntro`) becomes visible and interactive.
**Action:** Point `#bb-vbg` to `assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4` to immediately trigger `canplay` / `readyState >= 3`, eliminating the 3000ms wait.
