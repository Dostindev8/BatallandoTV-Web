## 2026-03-31 - Background Video 404 Resolution
**Learning:** Legacy media asset references pointing to non-existent directories (e.g. `images/SIN_FIN_-_BATALLANDO.mp4`) trigger failed 404 requests on page load, delaying media initialization and causing network resource waste.
**Action:** Always scan HTML media tags and verify URI-encoded asset paths in `assets/Batallando/` before optimization.
