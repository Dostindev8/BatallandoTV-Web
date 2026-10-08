## 2026-03-31 - Fix critical intro video 404 and preconnect optimization
**Learning:** Hardcoded video paths pointing to non-existent folders (`images/` or `video/`) cause 404 network errors and trigger mandatory JS fallback timeouts (e.g. 3000ms `canplay` fallback delay), significantly degrading perceived load performance.
**Action:** Always verify local media file paths in static projects and add `preconnect` resource hints with `crossorigin` for external CDN dependencies.
