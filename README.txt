MY MONEY — PWA DEPLOYMENT

Files:
- index.html: expense tracker with localStorage, backup/restore, and saved dark mode
- manifest.webmanifest: PWA metadata
- service-worker.js: offline app-shell caching and update handling
- icons/: app icons

NETLIFY:
1. Upload/deploy the contents of this folder (not the folder wrapper) so index.html is at the site root.
2. Open the HTTPS Netlify URL once while online.
3. In Chrome on Android, use the browser menu and choose "Install app" or "Add to Home screen".
4. Use Backup & restore in the app to export JSON backups regularly.

DATA NOTES:
- Expense data and theme preference are stored in localStorage on that browser/device.
- Service worker caches the app shell so the page can reopen offline after first successful load.
- Browser storage can be cleared by the user or browser. The JSON backup is the durable copy.
- If you update the app and an old version persists, bump CACHE_NAME in service-worker.js (e.g. my-money-pwa-v2).
