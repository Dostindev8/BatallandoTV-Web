## 2026-03-30 - Fix background video 404 path to prevent 3s fallback delay
**Learning:** Broken background video paths (`404`) prevent the `canplay` DOM event from firing, triggering a 3000ms JavaScript fallback timeout before revealing the main interface.
**Action:** Always verify video asset URLs exist and are correctly URI-encoded to ensure instant `canplay` initialization without delay.
