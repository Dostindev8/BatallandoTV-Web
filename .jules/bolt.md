## 2026-07-09 - Identifying and fixing critical LCP 404s
**Learning:** In a static repository without automated link checking, broken paths to large media files (like the intro video) not only break the UX but cause significant performance degradation due to failed fetch attempts and console noise during the critical path.
**Action:** Always perform a regex-based scan for asset paths containing spaces and ensure they are URI-encoded and point to the correct 'assets/Batallando/' directory before applying further optimizations.
