## 2024-06-07 - Initial Performance Audit
**Learning:** Found that the intro video path was broken (`images/` instead of `assets/Batallando/`) and large video assets (26MB) were using `preload="auto"`, leading to massive unnecessary data transfer on initial load. LCP elements like the logo lacked prioritization.
**Action:** Fix video paths, apply URI encoding to all asset paths, switch video preloading to `metadata`, and implement a comprehensive `loading`, `decoding`, and `fetchpriority` strategy across the application.
