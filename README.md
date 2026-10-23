# MA LAXMI PRO — prototype starter

Responsive web/PWA prototype for the MA LAXMI PRO DJ video and sound app.

## Run locally
1. Unzip the project.
2. Open a terminal in this folder.
3. Run a local web server (recommended):
   - Python: `python -m http.server 8000`
4. Open `http://localhost:8000` in your browser.

Opening `index.html` directly also shows the UI, but PWA install/offline features require localhost or HTTPS.

## Android
For a quick demo, open the hosted HTTPS version in Chrome on Android and choose **Install app** / **Add to Home screen**. This creates an installable web app, not a Play Store APK.
For a signed Android APK, wrap the web app using Capacitor or build a native Android client, then configure and sign it with Android Studio.

## Demo features
- Responsive home page and navigation
- Select and play local video/audio files
- Audio playback volume slider
- Local demo profile form
- Local mock admin panel passcode: `LAXMI-DEMO`
- Basic PWA manifest and service worker

## Important limitations
This is a **front-end prototype**, not a production monetization platform:
- Video URLs use browser object URLs and are temporary; videos are not uploaded to a server or shared with other users.
- Login is a UI demo only. It does not securely authenticate users or persist accounts.
- Admin passcode is visible in source and must never be used in production.
- Earnings are informational only. No ads are served and no money is collected or paid.
- A production release needs backend APIs, database, secure authentication, cloud video storage, upload moderation/reporting, privacy policy, terms, copyright handling, and an approved ad provider such as AdMob (for Android) or an approved web ad network.
- Do not embed secret keys in frontend code. Enforce admin permissions and upload validation server-side.

## Suggested production architecture
- Frontend: React/Next.js or Flutter
- Authentication and database: Firebase Authentication + Firestore, or a trusted backend
- Video storage: Firebase Storage or another secure object-storage service
- Ads: AdMob for Android; web ads configured separately and subject to approval
- Admin: server-verified role-based access, moderation queue and audit log
