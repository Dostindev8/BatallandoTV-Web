# Bolt's Performance Journal

## 2026-03-05 - Correcting 404 Video Asset Paths and Optimizing LCP Preloads
**Learning:** In this static-site repository, critical background video assets like the intro video ('SIN FIN - BATALLANDO.mp4') were pointing to non-existent folders ('images/') or unencoded paths, resulting in 404 errors and delaying Largest Contentful Paint (LCP). Additionally, client-side template literals defer discovery of critical assets (e.g., hero image, logos), which can be bypassed via explicit preloads in the HTML `<head>`.
**Action:** Always verify all media paths, ensure they are URI-encoded (e.g. converting spaces to '%20'), point to the correct 'assets/Batallando/' directory, and add resource hints/preloads for critical above-the-fold assets to avoid 404s and reduce page load times.
