## 2026-03-31 - Fix Missing Background Video Path & URL Space Encoding

**Learning:** Missing video assets (e.g. `images/SIN_FIN_-_BATALLANDO.mp4`) in HTML video elements cause network 404 delays and block intro reveal animations until a 3-second script fallback timer expires. Additionally, unencoded spaces in media path URLs cause resource fetch failures depending on browser URL parser strictness.

**Action:** Always verify local asset existence in `assets/Batallando/` and explicitly URL-encode space characters as `%20` in HTML/JS source paths to guarantee immediate 200 OK responses and instant video playback.
