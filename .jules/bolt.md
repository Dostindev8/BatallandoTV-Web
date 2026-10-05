## 2026-10-05 - 404 Video Asset Path Delay
**Learning:** In this codebase, if `#bb-vbg` fails to load due to a 404 path error, `vbg.addEventListener('canplay', revealIntro)` never fires, triggering a mandatory 3000ms `setTimeout` fallback delay before intro initialization.
**Action:** Always verify video paths point to valid URI-encoded assets under `assets/Batallando/` to eliminate network 404s and remove the 3-second delay.
