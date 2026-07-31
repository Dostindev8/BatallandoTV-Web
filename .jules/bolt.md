# Bolt's Performance Journal

## 2026-07-31 - Correcting Broken Video Paths and Optimizing LCP Discovery
**Learning:** Hardcoded asset references in template literals or raw markup that use wrong paths (such as `images/SIN_FIN_-_BATALLANDO.mp4` instead of the actual file location `assets/Batallando/SIN FIN - BATALLANDO.mp4` and absolute paths like `/assets/...`) cause major 404 network bottlenecks and block rendering paths. Furthermore, because static files aren't run through a compilation step, preloading these LCP assets (video and hero image) manually in the `<head>` bypassing JS discovery delays yields a massive improvement in loading speeds.
**Action:** Always scan for resource path mismatches, use relative paths, perform proper URI-encoding, preload above-the-fold assets, and preconnect to critical CDNs.
