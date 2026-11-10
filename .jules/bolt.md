# Bolt's Performance Journal

## 2026-03-30 - Fix broken intro video path to bypass 3000ms fallback delay
**Learning:** Broken asset paths for media elements with event listeners (e.g. `canplay`) fall back to hardcoded timeout delays (in this case `setTimeout(revealIntro, 3000)`), masking errors while penalizing perceived initial load and intro animation by ~1.6s.
**Action:** When profiling initial load delays, check network logs for 404s on media elements before investigating execution timing; ensure all video paths point to valid assets in `assets/Batallando/` with URI encoding.
