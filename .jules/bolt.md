## 2026-10-26 - Eliminate 3s intro fallback delay by fixing broken media asset path
**Learning:** In `index.html`, `#bb-vbg` video attempted to load from non-existent `images/SIN_FIN_-_BATALLANDO.mp4`. When media fail to load, the script triggers a 3000ms `canplay` fallback timeout (`setTimeout(revealIntro, 3000)`), causing a forced 3-second delay before the intro transition triggers.
**Action:** Always verify that critical video elements point to existing paths with proper URI encoding (`assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4`), preventing mandatory network fallback timeouts.
