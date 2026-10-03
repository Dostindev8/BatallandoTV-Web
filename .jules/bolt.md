## 2026-03-29 - Broken Media Source Triggered Mandatory 3s Timeout
**Learning:** In this project's preloader script, failing to load the #bb-vbg video triggers a 3,000ms `canplay` fallback timeout. Validating video asset paths eliminates 3s of loading latency on site launch.
**Action:** Always verify video paths in static HTML when preloader logic uses media event timeouts (`canplay`/`loadeddata`).
