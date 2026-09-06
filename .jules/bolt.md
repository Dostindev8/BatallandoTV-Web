## 2026-03-30 - Fix video background path 404 to eliminate intro delay
**Learning:** In `index.html`, a missing or invalid video background source (`images/SIN_FIN_-_BATALLANDO.mp4`) caused a 404 error on initial load, forcing `revealIntro()` to wait for a 3-second timeout fallback before displaying the main content.
**Action:** Ensure critical intro video paths point directly to valid assets (`assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`) with proper URL encoding to allow immediate playback and avoid render-blocking timeouts.
