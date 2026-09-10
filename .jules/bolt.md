## 2026-03-30 - Fix Broken Intro Video URL and URI-Encode Space-Containing Asset Paths

**Learning:** Broken 404 video URLs like `images/SIN_FIN_-_BATALLANDO.mp4` cause unnecessary failed HTTP requests and prevent key background assets from rendering. Additionally, unencoded asset paths containing spaces (e.g., `assets/Batallando/SIN FIN - BATALLANDO.mp4` or `Batallando TV 2024.png`) lead to URI parsing issues depending on browser/server request handling.

**Action:** Ensure all background video paths point to verified files under `assets/Batallando/` and URI-encode all asset URLs with spaces (`%20`) across static HTML files.
