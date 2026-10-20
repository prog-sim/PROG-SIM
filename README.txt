PROG SIM (Programming Simulator) — PWA and Offline Distribution Package

FILES
- index.html: the PROG SIM website
- manifest.json: app name, display settings, and icons
- service-worker.js: caches the app shell for offline use
- icons/: app icons for installation

IMPORTANT
The service worker and installable PWA features require HTTPS (for example, a hosted GitHub Pages site). Opening index.html directly from a ZIP may still allow basic website features, but it does not install the service worker for offline caching.

HOSTING STEPS (GitHub Pages)
1. Sign in to GitHub and create a new public repository, e.g. prog-sim.
2. Upload all files and folders in this package to the repository root (not the ZIP file itself).
3. In the repository, open Settings > Pages.
4. Under Build and deployment, select Deploy from a branch, choose the main branch and /(root), then Save.
5. Wait for deployment and open the HTTPS URL shown on the Pages settings screen.
6. On Android Chrome, visit the URL while online, wait for the page to load, then use the browser menu and choose Install app or Add to Home screen if offered.
7. Test offline: close the tab, enable airplane mode, then launch the installed app. Confirm lessons, quiz, and editor work.

If you update the website later, update CACHE_NAME in service-worker.js (for example, v2) so devices can fetch the new cached files.
