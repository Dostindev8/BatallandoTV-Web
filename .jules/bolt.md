## 2026-03-30 - Intro Background Video Path Fix
**Learning:** Broken video paths in `#bb-vbg` trigger a 3,000ms JavaScript fallback timer in the 3D intro initialization before showing main content.
**Action:** Always verify video paths in `index.html` point to valid assets in `assets/Batallando/` with URI encoding to prevent fallback delay penalties.
