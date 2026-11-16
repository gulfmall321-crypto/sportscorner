# Sports Corner app – setup (about 10 minutes, one time only)

## 1. Allow the app to show your script (in Apps Script)
In `doGet`, add `.setXFrameOptionsMode(...)`:

```javascript
function doGet() {
  return HtmlService.createHtmlOutputFromFile('Index')   // keep your own file name
    .setTitle('Sports Corner')
    .setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)
    .addMetaTag('viewport', 'width=device-width, initial-scale=1');
}
```
Deploy → Manage deployments → ✏️ Edit → Version: **New version** → Deploy.
(The /exec link stays the same.)

## 2. Host the app for free (GitHub Pages)
1. Sign in at github.com → **New repository** → name it `sportscorner` → Public → Create.
2. **Add file → Upload files** → drag in every file from this zip → Commit.
3. **Settings → Pages** → Branch: `main`, folder `/ (root)` → Save.
4. After about a minute your app is at: `https://YOUR-USERNAME.github.io/sportscorner/`

## 3. Install it on each phone or PC
- **Android (Chrome):** open the link → ⋮ → **Install app**
- **iPhone (Safari):** open the link → Share → **Add to Home Screen**
- **PC (Chrome/Edge):** open the link → click the install icon in the address bar

## Notes
- Sign in to Google in the same browser first. If the screen stays blank, tap **⤢** to open the app directly.
- On iPhone, Safari can block Google sign-in inside apps. If that happens, use ⤢, or set the deployment's
  "Who has access" to **Anyone** (only if the data is fine to be reachable by anyone who has the link).
- To change the link later, edit `APP_URL` near the bottom of `index.html`.
