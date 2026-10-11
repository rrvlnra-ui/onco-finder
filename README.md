# Oncology Research Finder — install guide

This folder is a complete web app. You put it online once (free), then add it to your iPhone Home Screen and your Mac Dock, where it opens in its own window like any other app.

## What's in the folder

| File | What it is |
|---|---|
| `index.html` | The app: all sources, live results, Open all, source directory |
| `manifest.webmanifest` | App name and icons for iPhone and Mac |
| `sw.js` | Lets the app open without an internet connection |
| `icons/` | App icons |

## Step 1: Put it online with GitHub Pages (about 10 minutes, free)

1. Unzip the download on your Mac. You'll get a folder called `orf-app`.
2. Create a free account at **github.com** (skip this if you have one).
3. Click **+** (top right) → **New repository**. Name it `onco-finder`, choose **Public**, then **Create repository**.
4. On the new repository page, click **uploading an existing file**.
5. Open the `orf-app` folder in Finder, select **everything inside it** (including the `icons` folder) and drag it onto the upload area. Click **Commit changes**.
6. Go to **Settings** → **Pages**. Under *Build and deployment*, set **Source** to *Deploy from a branch*, **Branch** to *main* and folder */ (root)*, then **Save**.
7. Wait a minute or two and refresh. The page shows your app's address, for example `https://yourname.github.io/onco-finder/`. Open it to check it works.

The address is public, but the app holds no personal data: your saved searches and your own sources are stored only on your devices.

## Step 2: Install on iPhone

1. Open your app's address in **Safari**.
2. Tap **Share** → **Add to Home Screen**. If you see an **Open as Web App** switch, leave it on.
3. Tap **Add**. The "Onco Finder" icon appears on your Home Screen.

## Step 3: Install on Mac

- **Safari** (macOS Sonoma or later): open the address, then choose **File → Add to Dock**.
- **Chrome**: open the address, then click the install icon at the right of the address bar (or ⋮ → **Cast, save and share → Install page as app**).

## Using it

- **Search** loads the top 10 results from PubMed, Europe PMC preprints and ClinicalTrials.gov inside the app, and updates every source link below them.
- **Open all** opens your search on every source. Browsers block a single click from opening many tabs:
  - On Mac Safari: **Safari → Settings → Websites → Pop-up Windows**, and set your app's address to **Allow**. In Chrome, click the blocked pop-up icon in the address bar and choose **Always allow**.
  - On iPhone, use **Open next**: each tap opens the next source and ticks it off.
- **Saved searches** run as soon as you tap them.

## Moving saved searches between iPhone and Mac

1. On the first device, tap **Export backup**. On iPhone, choose **Save to Files** (iCloud Drive) or **AirDrop** to your Mac.
2. On the other device, tap **Import backup** and pick that file. Imports are added to what's already there; nothing is overwritten.

## Updating the app later

1. In your GitHub repository, click **Add file → Upload files** and drag in the changed files. Uploading a file with the same name replaces it.
2. If you changed anything, also open `sw.js`, change `orf-v1` to `orf-v2` (then `orf-v3`, and so on) and upload it too. This tells installed copies to fetch the new version.
3. Close and reopen the app on each device. It may take one extra reopen to update.

## If something doesn't work

- **A results column says it couldn't load**: check your connection, then use the "Open this search on…" link in that column. The other columns and all source links still work.
- **Icon or name looks wrong after installing**: delete the Home Screen icon and add it again; iPhone saves the icon at the moment you add it.
