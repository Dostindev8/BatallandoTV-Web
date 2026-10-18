## 2026-10-18 - Intro Video Path Failure & 3-Second Delay
**Learning:** In this codebase, if `#bb-vbg` video src fails (e.g., `images/SIN_FIN_-_BATALLANDO.mp4` returning 404), the JavaScript fallback timer imposes a mandatory 3000ms delay before triggering `revealIntro()`. Fixing 404 video paths eliminates this mandatory 3s startup block and restores instant intro rendering upon `canplay`.
**Action:** Always verify that `#bb-vbg` video path is relative, URI-encoded, and returns 200 OK to prevent mandatory intro startup timeouts.
