## 2025-05-14 - Manual URI Encoding for JS-rendered Assets
**Learning:** In projects without a build pipeline (like Webpack or Vite), spaces in asset paths inside JavaScript template literals are not automatically encoded. This leads to broken images/videos when the browser attempts to fetch the raw URL.
**Action:** Always manually URI-encode asset paths (replace spaces with `%20`) in JavaScript rendering logic to ensure URI robustness.
