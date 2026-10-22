## 2026-03-30 - Fix Intro Video 404 Delay
**Learning:** A missing or invalid background video asset path (`#bb-vbg`) causes a 404 network error and triggers a mandatory 3000ms `setTimeout` fallback in the intro sequence before the site rendered the initial UI/3D canvas.
**Action:** Always ensure background video assets exist and are properly relative and URI-encoded (`assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`) to prevent the 3s fallback delay on intro load.
