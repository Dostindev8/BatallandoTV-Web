# Bolt's Performance Journal

## 2026-05-03 - Initial Profiling
**Learning:** Found a broken asset path for the intro video (`images/SIN_FIN_-_BATALLANDO.mp4` instead of `assets/Batallando/SIN FIN - BATALLANDO.mp4`). This causes a 404 and delays the intro reveal. Also, multiple images lack lazy loading.
**Action:** Fix the broken path and implement `fetchpriority="high"` for the critical intro video to improve LCP.
