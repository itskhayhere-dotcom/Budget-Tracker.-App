# Moss / Line – files to upload to GitHub

## 1. app-repo  (your existing app repo, the one Vercel deploys at budget-tracker-app-teal.vercel.app)
- Upload `index.html` and replace the old one (Add file > Upload files > commit).
- Keep your existing manifest, sw.js and icons as they are.
- Vercel redeploys automatically. Hard-refresh once, because the service worker may cache the old page.

## 2. website-repo  (the landing page, a NEW repo)
- Create a new GitHub repo, for example `moss-line-website`, and upload `index.html` to its root.
- Deploy it: import the repo into Vercel (Framework: Other), or use GitHub Pages (Settings > Pages > Deploy from branch > main / root).
- Set the iPhone & iPad and Android buttons to your store or APK links (search the file for `data-store`).

## 3. Android APK: do NOT upload the current one yet
The APK and AAB you built open https://github.com, not your Vercel app.
Rebuild in PWABuilder:
- URL: https://budget-tracker-app-teal.vercel.app/  (not a GitHub address)
- Choose a package ID such as com.mossline.app
- Create a new signing key and back up the keystore and its password.
Then:
- Put the signed `.apk` in the app repo, next to index.html.
- Put the `assetlinks.json` from PWABuilder's zip at `.well-known/assetlinks.json` in the app repo.
- Upload the `.aab` to Google Play Console if you publish there.
The landing page's Android button expects:
https://budget-tracker-app-teal.vercel.app/Moss_Line_Budget_Tracker.apk
Keep that file name, or tell me the new one and I will update the button.
