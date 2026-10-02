# Daily Organizer (Android app)

Tasks, notes, calendar and expense tracking. Plain HTML/CSS/JS wrapped with Capacitor. Data stays on the phone.

## Get the APK (no computer setup needed)

1. Create a new repository on github.com.
2. Upload everything in this folder, keeping the structure (the `.github` folder must be included).
   Easiest: unzip, then drag all files into "Add file > Upload files".
3. Open the **Actions** tab. The "Build Android APK" workflow starts automatically
   (or click it, then "Run workflow").
4. After about 5 minutes, open the finished run and download **daily-organizer-apk** from "Artifacts".
5. Unzip it, copy `app-debug.apk` to your phone, open it, and allow "Install unknown apps" when asked.

## Change the app

Edit `www/index.html`, commit, and the workflow builds a new APK.
The name and package id are in `capacitor.config.json`.

## Notes

- Fonts load from Google Fonts when online and fall back to the system font offline.
  To bundle a font, add the font files to `www/` and reference them with `@font-face`.
- This is a debug-signed APK, fine for personal use. Publishing on Google Play needs a signed release build.
- Needs Android 7+ with an up-to-date Android System WebView.
- CSV export opens the Android share sheet.
