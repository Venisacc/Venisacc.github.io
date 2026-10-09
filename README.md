# Chloe Chan · Personal Website

Static personal site. Drag-and-drop deploy to GitHub Pages.

## Files

```
deploy/
├── index.html              ← main page (single self-contained HTML)
└── assets/
    └── avatar_full.jpg     ← hero portrait
```

That's it. No build step, no node_modules.

## Deploy to GitHub Pages (drag-and-drop, ~2 minutes)

### 1. Create a new repo

Go to <https://github.com/new> and sign in.

- **Repository name**: pick one of:
  - `chloe-chan.github.io` → your site will live at `https://chloe-chan.github.io` (best for a personal site)
  - anything else (e.g. `portfolio`) → your site will live at `https://<your-username>.github.io/portfolio/`
- **Public** (required for free GitHub Pages) or **Private** if you have GitHub Pro
- ✅ Add a README file (optional, helps with the empty-repo state)
- Click **Create repository**

### 2. Upload the files

On the repo page (Code tab), click the **Add file ▾** button → **Upload files**.

Drag **both** of these into the upload area:

```
index.html
assets/    (the whole folder, with avatar_full.jpg inside)
```

> Tip: if GitHub only lets you upload one folder at a time, drag `index.html` first, commit, then drag the `assets/` folder in a second commit.

Click **Commit changes**.

### 3. Turn on GitHub Pages

Go to **Settings** (tab at the top) → **Pages** (left sidebar).

- **Source**: `Deploy from a branch`
- **Branch**: `main` · `/ (root)`
- Click **Save**

Wait 30–60 seconds. Refresh the **Pages** settings page — you'll see:

> ✅ Your site is live at `https://<username>.github.io/<repo>/`

### 4. Done

That's the whole thing. To update later:

1. Open `index.html` on GitHub
2. Click the ✏️ pencil icon
3. Edit, then **Commit changes**
4. Site updates in ~30 seconds

---

## Deploy elsewhere (alternatives)

- **Netlify Drop**: <https://app.netlify.com/drop> — drag the `deploy/` folder onto the page. Done in 10 seconds.
- **Vercel**: `npx vercel` inside the folder.
- **Cloudflare Pages**: drag the folder at <https://dash.cloudflare.com/?to=/:account/pages>.

---

## Customization

Everything is in `index.html`. Common tweaks:

| Change | Where |
|---|---|
| Your name / headline | `<h1>Chloe <em>Chan</em></h1>` |
| Photo | replace `./assets/avatar_full.jpg` |
| Email / phone | search for `chloe.chan.marketing@hku.com` |
| Sticker text | `<div class="sticker top">…</div>` |
| Colors | `:root { --accent … }` at top of `<style>` |
| Fonts | the Google Fonts `<link>` in `<head>` |

© 2026 Chloe Chan · Hong Kong SAR
