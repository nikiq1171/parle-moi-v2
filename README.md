# Parle-moi

Pronunciation and DELF B1 oral practice app. It runs entirely in your browser: no server, no account.

## 1. Put it on GitHub

1. Sign in at github.com and create a new **public** repository, for example `parle-moi`.
2. Click **Add file → Upload files** and upload every file in this folder:
   `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png`, `README.md`.
3. Click **Commit changes**.

## 2. Turn on GitHub Pages

1. In the repository, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to *Deploy from a branch*, branch `main`, folder `/ (root)`, then **Save**.
3. Wait 1–2 minutes. Your app will be at `https://YOUR-USERNAME.github.io/parle-moi/`.

## 3. Add it to your phone

- **iPhone:** open the address in **Safari** → Share button → **Add to Home Screen**.
- **Android:** open the address in **Chrome** → ⋮ menu → **Add to Home screen** (or **Install app**).

Allow the microphone when the app asks.

## 4. Add your DeepSeek key

Open the app → **Réglages** → paste your DeepSeek API key → **Tester la clé**.

- The key is saved only in your phone's browser. **Never put it in any file on GitHub**: the repository is public.
- Anyone who gets your key can spend your DeepSeek credit, so keep only a small balance on it.
- Without a key, Bilan, Sons and the built-in Écoute documents still work. The key is needed for the Oral exam simulation and for creating new listening documents.

## Why the app opens in the browser, not full screen

On iPhone, speech recognition doesn't work in full-screen home-screen web apps, so the manifest uses `"display": "browser"`. The home screen icon opens the app in Safari/Chrome where the microphone works.
If you're on Android and want full screen, change `"display": "browser"` to `"display": "standalone"` in `manifest.webmanifest`, then test that the microphone still works.

## Updating the app

1. Upload the changed files to the repository again (Add file → Upload files).
2. In `sw.js`, raise the number in `parle-moi-v4` (to `v5`, and so on) so phones fetch the new version.
3. In `index.html`, raise `APP_VERSION` and add a new entry at the top of `CHANGELOG`. Everyone who opens the app then sees a "What's new" pop-up once.
