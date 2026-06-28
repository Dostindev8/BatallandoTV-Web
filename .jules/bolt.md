## 2026-06-28 - LCP Optimization and 404 Resilience
**Learning:** In a static media-heavy site, broken asset paths (404s) for critical above-the-fold content are the most significant LCP bottlenecks. Additionally, using `decoding="async"` on LCP candidate images can be counter-productive as it allows the browser to defer rendering even after data is available.
**Action:** Always prioritize fixing 404s for critical assets, use `fetchpriority="high"` for LCP, and ensure LCP images use default (sync) decoding. Use `preload="metadata"` for background videos to save initial bandwidth.
