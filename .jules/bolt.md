## 2026-03-31 - Intro Video Path 404 Triggers 3s JS Timeout
**Learning:** In `index.html`, a broken media path (`images/SIN_FIN_-_BATALLANDO.mp4`) caused the intro background video to fail loading, triggering a 3000ms `canplay` fallback `setTimeout` in JavaScript that blocked intro hide and site rendering.
**Action:** Ensure intro video paths point to valid assets in `assets/Batallando/` and URIs are encoded (`SIN%20FIN%20-%20BATALLANDO.mp4`) to avoid the mandatory 3s fallback delay.
