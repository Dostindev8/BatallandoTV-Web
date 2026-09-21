## 2026-09-21 - Fix broken intro video path to avoid fallback timeout
**Learning:** In this codebase, if `#bb-vbg` video fails to load due to a 404 error (e.g. `images/SIN_FIN_-_BATALLANDO.mp4`), JavaScript waits for a 3000ms `canplay` fallback timeout before triggering `revealIntro()`. Fixing the asset path to point to `assets/Batallando/SIN%20FIN%20-%20BATALLANDO.mp4` allows the video `canplay` event to fire immediately (~1.8s load vs >3s delay).
**Action:** Always verify local media paths against actual file system directories (`assets/Batallando/`) and URI-encode spaces (`%20`).
