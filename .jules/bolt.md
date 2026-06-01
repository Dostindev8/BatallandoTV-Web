## 2026-05-03 - Asset Path and Video Preloading Optimization

**Learning:** In projects without a build step or bundle manager, asset paths are prone to becoming stale (e.g., `images/` vs `assets/Batallando/`). A single broken path for a large asset like a 26MB video not only breaks the UI but also wastes significant bandwidth on a 404. Additionally, decorative background videos in list items should always use `preload="none"` to prevent the browser from eagerly downloading megabytes of data that may never be watched.

**Action:** Always verify asset resolution in the target environment. Use relative paths and encoded URIs (`%20` for spaces) for robustness. Implement `preload="none"` on background videos and `loading="lazy"` on non-critical images to minimize initial payload.
