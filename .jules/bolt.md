## 2026-06-11 - Asset Loading and Path Inconsistencies
**Learning:** Large video assets (26MB+) were being preloaded twice due to redundant elements and broken paths, causing significant initial bandwidth waste. Additionally, spaces in asset filenames were inconsistently encoded, leading to potential 404s in some browser environments or during dynamic rendering.
**Action:** Always use `preload="metadata"` or `preload="none"` for non-critical videos. Ensure URI-encoding (`%20`) is used for all asset paths with spaces, especially when rendered via JavaScript templates.
