## 2026-06-12 - Background Video Preloading Anti-pattern
**Learning:** Using `preload="auto"` on multiple background or secondary video assets causes the browser to aggressively download large files during the critical initial load, leading to bandwidth waste and potential main-thread contention.
**Action:** Use `preload="metadata"` for all non-critical background videos to ensure only the necessary headers are fetched, deferring the full download until playback is actually required.
