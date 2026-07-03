# Bolt's Performance Journal - Batallando TV

## 2026-05-03 - Critical LCP Asset Path and Prioritization
**Learning:** The intro video, a critical LCP element, was failing to load due to a 404 error (incorrect directory and unencoded spaces). This caused a significant delay in the "visual complete" state of the application. Additionally, critical assets lacked resource prioritization hints.
**Action:** Always verify asset paths using a local server and Playwright to catch 404s early. Apply 'fetchpriority="high"' to LCP assets and URI-encode paths containing spaces to ensure robustness across different environments.
