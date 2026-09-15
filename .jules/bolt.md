## 2026-03-30 - Fix broken intro video path to eliminate 3s fallback timeout
**Learning:** Broken media paths in client-side fallback scripts cause silent 3,000ms delay timeouts when `canplay` fails to fire; URI-encoding asset paths and fixing 404 targets eliminates mandatory startup delays.
**Action:** Always inspect JS timeout logic attached to media event listeners like `canplay` and ensure media `src` paths exist and are correctly URI-encoded.
