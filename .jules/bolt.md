## 2026-05-03 - Correct Media Paths Prevent Mandatory 3000ms Fallback Delay

**Learning:** In this application, failing to load the `#bb-vbg` intro video (`images/SIN_FIN_-_BATALLANDO.mp4` returning 404) prevents the `canplay` event from firing. The JS engine waits for a mandatory 3000ms fallback timeout before revealing the 3D intro overlay and allowing the user to enter the app.

**Action:** Always verify media asset paths in static HTML and JS template strings. URI-encode spaces (e.g. `%20`) and point to valid files in `assets/Batallando/` to allow native `canplay` events to trigger immediately.
