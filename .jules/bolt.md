# Bolt's Performance Journal

## 2026-07-20 - Optimizing LCP and Eliminating 404s via Resource Hints and Asset Encoding
**Learning:** In a pure static-site architecture where elements are rendered or modified dynamically via custom JavaScript files, critical assets like background video overlays ('SIN FIN - BATALLANDO.mp4') and main hero images suffer from severe discovery delays. Furthermore, unencoded spaces in local URLs and incorrect directory references (like 'video/') trigger expensive 404 request failures, stalling the browser's main thread and deteriorating Largest Contentful Paint (LCP) performance.
**Action:** Preload critical media and preconnect CDN domains in the HTML head to trigger early resource fetching, select 'loading="eager"' and standardizes 'fetchpriority="high"' for the main LCP images, and audit/URI-encode all local paths across HTML and templates to completely eradicate 404 errors.
