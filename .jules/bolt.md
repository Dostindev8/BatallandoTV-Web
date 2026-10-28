## 2026-03-30 - Broken Intro Video Path Triggers 3s Fallback Delay
**Learning:** In this static application, a broken background video path (`images/SIN_FIN_-_BATALLANDO.mp4`) caused a 404 network error and triggered a 3000ms JavaScript fallback timeout before revealing the main intro sequence.
**Action:** Always verify video asset availability and URI encoding in `index.html` to prevent unnecessary network 404s and fallback delays.
