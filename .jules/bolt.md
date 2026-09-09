## 2026-03-31 - Fix 404s and asset load failures caused by unencoded path spaces
**Learning:** In static HTML sites, unencoded spaces and non-existent legacy directory references (`video/`, `images/`) in media asset paths cause 404 network errors, preventing critical LCP background video and hero image rendering.
**Action:** Always URI-encode asset paths containing spaces (`%20`) and verify path targets against existing assets in `assets/Batallando/` to ensure 0% asset 404 network failures.
