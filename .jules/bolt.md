## 2026-05-22 - URI Robustness in Static Assets
**Learning:** In a static site architecture without a build pipeline (like Vite or Webpack), assets with spaces in filenames or invalid leading slashes in relative paths cause silent 404 errors that degrade performance and prevent the browser from correctly prioritizing resources like the LCP.
**Action:** Always URI-encode asset paths (e.g., %20 for spaces) and ensure relative paths do not start with a leading slash unless they are intended to be root-relative, specifically when the application is served via a simple HTTP server.
