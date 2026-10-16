# Budget Planner (installable app)

Plan your budget, see how much is safe to spend today, and log expenses.
Works offline after the first open and installs on a phone like a normal app.

## What is in this folder

- `index.html` - the app (page and logic)
- `styles.css` - all the colors, fonts and layout
- `manifest.webmanifest` - name, colors and icons, so phones can install it
- `sw.js` - makes it work offline
- `icons/` - the app icons

Keep all of these together in one folder.

## 1. Put it online (free, pick one)

The app has to be on a web address that starts with https:// before a phone will install it.

- **Netlify Drop:** go to app.netlify.com/drop and drag this whole folder onto the page. You get a link right away.
- **GitHub Pages:** make a new repository, upload these files, then open Settings > Pages and publish from the main branch.
- **Cloudflare Pages:** create a Pages project and choose "Upload assets", then upload this folder.

## 2. Install it

- **Android (Chrome):** open your link, tap the three-dot menu, then "Install app" (or "Add to Home screen").
- **iPhone (Safari):** open your link, tap Share, then "Add to Home Screen".
- **Computer (Chrome or Edge):** click the install icon in the address bar.

Menu names can differ a little between phone versions.

## Good to know

- Your entries are saved on the device you use. They do not carry over from the claude.ai version, and a second device starts empty.
- Clearing the browser's site data erases your entries.
- **App lock:** open Plan settings, find "App lock" and set a passcode. Your budget is then encrypted on the device and the app asks for the passcode each time it opens (and after it has been away for a minute). If you forget the passcode, the only way back in is "Erase this app's data" on the lock screen, so pick one you will remember.
- The web address itself is public, so anyone can open the empty app. They cannot see your entries, which never leave your device.
- To update the app after editing files, change the number in the `CACHE` name in `sw.js` (for example `v2` to `v3`) (the `CACHE` name) and upload the files again.

## Later: a real Android app file (APK)

Once the app is online, pwabuilder.com can package its link as an Android app. Or wrap this folder with Capacitor in Android Studio.
