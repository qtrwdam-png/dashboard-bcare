# Preview Findings

- After restarting the development server, the preview endpoint is available on port 5000.
- The captured preview currently shows the Arabic loading state (`جاري التحميل...`) rather than the dashboard.
- The server health report indicates dependencies, LSP, and TypeScript are healthy.
- The production build succeeds when the build script explicitly sets `NODE_ENV=production`.
- The dashboard selection reconciliation helper was added to clear a selected visitor when the latest Firestore snapshot no longer contains that record.

- After the clean restart, `/login` renders correctly in the preview, while `/` remains on the expected authentication loading state because no authenticated session is present in the preview.
- The preview server reports HTTP 200 for both routes; the earlier runtime errors were caused by rebuilding/removing `.next` while the dev server was still running and were cleared by restarting it.
