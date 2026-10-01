## 2026-10-01 - Intro Video 404 Fallback Timeout Bottleneck
**Learning:** In this codebase, failing to load the `#bb-vbg` intro video triggers a 3000ms `canplay` fallback timeout in JavaScript that delays intro initialization.
**Action:** Always verify video asset paths are relative and URI-encoded to prevent 404 errors and eliminate the mandatory 3s initial load delay.
