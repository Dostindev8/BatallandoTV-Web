## 2026-03-31 - Broken background video path triggers mandatory 3s JS fallback timeout
**Learning:** In this codebase, the intro video element (`#bb-vbg`) has a fallback JS timeout set to 3000ms. When `images/SIN_FIN_-_BATALLANDO.mp4` failed with 404, the video `canplay` event never fired, forcing the browser to wait the full 3000ms delay before transitioning the intro UI.
**Action:** Always verify that critical video asset paths exist in `assets/Batallando/` and are properly URI-encoded to avoid triggering fallback timeouts.
