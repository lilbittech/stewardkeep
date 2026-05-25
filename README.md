# StewardKeep

A personal media collection tracker — books, vinyl, DVDs — built as a single-page PWA. Data lives in `localStorage`; no backend, no account required.

## Features

- Track books, vinyl records, DVDs, and CDs
- Log location, intent (keepsake, to-read, sell, lend), and notes
- Fetch book covers automatically via Open Library ISBN lookup
- Installable on iOS and Android home screens
- Works offline after first load

## GitHub Pages Setup

### First time

```bash
git init
git add .
git commit -m "Initial commit"
gh repo create stewardkeep --public --source=. --remote=origin --push
```

Then in your GitHub repo: **Settings → Pages → Branch: main → /(root) → Save**.

Your site will be live at `https://<your-username>.github.io/stewardkeep/` within a minute or two.

### Subsequent deploys

```bash
git add .
git commit -m "your message"
git push
```

GitHub Pages redeploys automatically on every push to `main`.

## Icons (optional but recommended)

The manifest references two icon files for home screen install:

```
icons/icon-192.png   — 192×192 px
icons/icon-512.png   — 512×512 px
```

Create an `icons/` folder and drop your PNG icons there. Without them the app still installs, but the home screen icon will be a generic browser placeholder.

## Local development

No build step. Just open `index.html` in a browser, or serve it locally:

```bash
npx serve .
# or
python3 -m http.server 8080
```

The service worker requires a real HTTP server (not `file://`), so use one of the above when testing offline behavior.
