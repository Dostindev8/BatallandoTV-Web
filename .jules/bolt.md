## 2026-09-18 - Fix missing intro video 404 to eliminate 3s fallback delay
**Learning:** A 404 on the intro video (`#bb-vbg`) causes the `canplay` event to never fire, falling back to a 3000ms `setTimeout` delay in JS before the page intro initializes.
**Action:** Always verify video asset paths exist and are properly URI-encoded to prevent 404 errors and mandatory fallback timeouts.
