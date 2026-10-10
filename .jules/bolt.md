## 2026-03-29 - Fix broken intro video path to eliminate 3s fallback timeout
**Learning:** In this codebase, a 404 error on the `#bb-vbg` background video source triggers a 3000ms JS fallback timeout during initialization, stalling intro presentation and user interactivity.
**Action:** Always verify background video paths point to valid URI-encoded assets in `assets/Batallando/` instead of legacy or missing directories.
