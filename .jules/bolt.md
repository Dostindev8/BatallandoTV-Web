## 2026-07-25 - Fixing 404 Media Paths and URI-Encoding Spaces
**Learning:** Hardcoded asset paths with unencoded spaces (e.g., 'SIN FIN - BATALLANDO.mp4' or 'Batallando TV 2024.png') cause browser rendering and loading failures. Moreover, incorrect paths (like 'images/' or 'video/' directories that don't exist) cause silent 404 resource errors that degrade performance metrics such as LCP.
**Action:** Always perform rigorous regex-based scans to identify and URI-encode all spaces in paths to '%20' and verify actual file existence against the directory structure.
