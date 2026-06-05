# Bolt's Performance Journal

## 2025-05-15 - URI Encoding in Static Projects
**Learning:** In projects without a build pipeline (like Webpack or Vite), browsers and certain environments might fail to resolve asset paths containing spaces (e.g., `Batallando TV.png`) if they aren't manually URI-encoded to `%20`. This is especially critical in JavaScript template literals used for rendering UI components.
**Action:** Always manually URI-encode asset paths and verify them with visual checks (screenshots) to ensure they resolve correctly after optimization.
