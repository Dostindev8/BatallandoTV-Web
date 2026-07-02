# Bolt's Performance Journal

## 2026-05-20 - Static Site Resource Optimization
**Learning:** In a static site without build pipelines, LCP bottlenecks are often caused by unencoded asset paths (leading to 404s) and lack of resource prioritization. Manually injecting performance attributes like `fetchpriority="high"` for above-the-fold assets and `loading="lazy"` for dynamic JS templates provides measurable improvements in load time and main-thread availability.
**Action:** Always verify asset paths via a local server to catch 404s early, and ensure dynamic template literals include lazy-loading attributes for all media.
