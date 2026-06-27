# apm-site

Public **Support + Privacy** page for *Ansha Photo Mosaic*, hosted on GitHub Pages.
Kept in its own repo so the app's internal docs stay private.

| File | What |
|---|---|
| `index.html` | The page — Support (`#support`) and Privacy (`#privacy`) sections. |
| `favicon.svg` | Site icon / header logo. |
| `og-image.png` | 1200×630 social-share preview. |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is (no Jekyll build). |

## Deploy (one time)

From inside this folder:

```sh
git init -b main
git add .
git commit -m "Ansha Photo Mosaic — support & privacy page"
gh repo create apm-site --public --source=. --remote=origin --push
```

Then enable Pages:

```sh
gh api -X POST repos/yu-antonio/apm-site/pages -f source.branch=main -f source.path=/ 2>/dev/null \
  || echo "Enable manually: repo → Settings → Pages → Source: main / root"
```

(Or in the browser: **repo → Settings → Pages → Build and deployment → Source: Deploy from a branch → `main` / `/ (root)` → Save**.) First publish takes ~1 minute.

## URLs for App Store Connect

Once live at `https://yu-antonio.github.io/apm-site/`:

| App Store Connect field | URL |
|---|---|
| **Privacy Policy URL** | `https://yu-antonio.github.io/apm-site/#privacy` |
| **Support URL** | `https://yu-antonio.github.io/apm-site/#support` |

## Updating later
Edit `index.html`, then `git commit -am "update" && git push`. Pages redeploys automatically.
