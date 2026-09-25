## 2026-03-30 - Broken media URL causing 3-second JS intro initialization delay
**Learning:** In `index.html`, a broken media path for `#bb-vbg` (`images/SIN_FIN_-_BATALLANDO.mp4`) resulted in a 404 response, forcing the JavaScript video preloader to wait for its 3000ms fallback timeout before initializing the 3D intro sequence.
**Action:** Always verify that critical video asset paths are valid and URI-encoded (`assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`) to ensure instant load and avoid 3s fallback delays.
