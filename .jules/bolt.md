## 2026-03-31 - Eliminate 3-second timeout delay from invalid intro video path
**Learning:** Broken video background paths in the intro element (`#bb-vbg`) fail quietly on media load, forcing the 3D intro overlay to hang for a full 3000ms fallback timeout before making the site interactive.
**Action:** Always verify background video paths point directly to valid assets in `assets/Batallando/` and use properly URI-encoded filenames to avoid fallback timeouts during initial paint.
