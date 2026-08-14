# PDF Scraper Test Site

A tiny static site for testing PDF-scraping tools. Includes 7 dummy PDFs
across different link patterns: direct links, nested folders, query strings,
a meta-refresh redirect, and a deliberately broken link.

## Deploy to GitHub Pages (no local hosting, ~2 minutes)

1. Go to https://github.com/new and create a new **public** repository
   (e.g. `pdf-scraper-test`).
2. Upload every file in this folder to the repo, preserving the folder
   structure (`docs/`, `reports/2024/`, `reports/2025/`, `archive/`).
   Easiest way: on the repo page, click **Add file → Upload files**, then
   drag the whole `pdf-test-site` folder contents in.
3. Go to **Settings → Pages**.
4. Under "Build and deployment", set **Source: Deploy from a branch**,
   branch: `main`, folder: `/ (root)`. Save.
5. Wait ~1 minute. Your site will be live at:
   `https://<your-username>.github.io/pdf-scraper-test/`

## What's in here

| Path | Purpose |
|---|---|
| `index.html` | Homepage with direct, nested, query-string, redirect, and broken links |
| `docs/*.pdf` | Two small PDFs linked directly and via relative path |
| `reports/index.html` | A nested section linking into two year subfolders |
| `reports/2024/`, `reports/2025/` | PDFs two folders deep |
| `archive/index.html` + `archive/legacy-notice.pdf` | Tests whether your scraper follows links only reachable from a secondary page |
| `redirect.html` | Meta-refresh redirect to a PDF, to test redirect handling |
| `docs/missing.pdf` (link only, file doesn't exist) | Tests 404 handling |

Feel free to add more PDFs or pages the same way — just drop files in and
link to them from an `.html` page.
