## 2026-06-06 - URI Encoding and LCP Prioritization
**Learning:** This repository uses a static file structure where assets (especially those in `assets/Batallando/`) often contain spaces in their filenames. Browsers in this environment can struggle or fail to resolve these if not explicitly URI-encoded (e.g., `%20`). Additionally, critical branding assets like the Preloader Logo and 3D Cube Logo are essential for the first paint and should always have high fetch priority.

**Action:** Always URI-encode asset paths in HTML/JS and apply `fetchpriority="high"` / `loading="eager"` to critical brand/LCP elements. For background videos, default to `preload="metadata"` to save bandwidth unless immediate playback of the entire file is absolutely critical.
