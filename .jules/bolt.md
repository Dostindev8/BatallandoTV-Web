# Bolt's Performance Journal

## 2026-05-04 - Intro Video Path Fix & Fallback Timeout Bypass
**Learning:** In this codebase, the intro screen (`#bb-intro`) waits for the background video (`#bb-vbg`) to fire the `canplay` event before calling `revealIntro()`. When the video source points to a broken path (e.g. `images/SIN_FIN_-_BATALLANDO.mp4` returning 404), playback fails and the reveal relies on a hardcoded 3000ms `setTimeout` fallback.
**Action:** Always verify that critical media assets point to existing files in `assets/Batallando/` with proper URI encoding (`%20`), eliminating 404s and bypassing the 3s fallback delay.
