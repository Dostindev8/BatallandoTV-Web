## 2026-03-30 - Fix broken background video path to avoid 3s intro fallback delay
**Learning:** In `index.html`, a missing background video asset (`#bb-vbg`) causes a 404 network error and prevents the `canplay` event listener from firing, forcing the application to wait for a 3000ms `setTimeout` fallback delay before showing the main page content.
**Action:** Always verify video background source paths exist and are properly URL-encoded so the `canplay` event fires immediately, bypassing fallback timeouts.
