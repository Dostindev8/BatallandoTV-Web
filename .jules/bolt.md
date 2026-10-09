## 2026-03-30 - Fix media asset 404s to eliminate 3s JS fallback delay
**Learning:** Hardcoded asset paths with unencoded spaces or incorrect directories cause 404 network failures on LCP and video assets, triggering a mandatory 3000ms `canplay` timeout fallback in `index.html` during intro initialization.
**Action:** Always URI-encode asset paths containing spaces and use relative `assets/Batallando/` paths for media to ensure immediate playback without falling back to the 3s timeout.
