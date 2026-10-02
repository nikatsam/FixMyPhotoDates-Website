# Fix My Photo Dates Website

Public website repository: <https://github.com/nikatsam/FixMyPhotoDates-Website>

GitHub Pages site: <https://nikatsam.github.io/FixMyPhotoDates-Website/>

This static website explains how Fix My Photo Dates diagnoses and repairs
incorrect dates on exported or copied photo files. It directs visitors to the
Microsoft Store listing and does not include the private Windows application
source code.

## Preview locally

From the root of the repository:

```powershell
python -m http.server 8000
```

Open <http://localhost:8000/>. Python is only needed for this optional local
preview; GitHub Pages serves the site without a build tool.

## Publish

`.github/workflows/deploy-pages.yml` deploys the root-level static site to
GitHub Pages on pushes to `main` and supports manual runs. The workflow copies
the app preview screenshot to the published artifact. In repository settings,
set Pages to **GitHub Actions** as the deployment source.

## Site files

- `index.html` - product overview, workflow, and Microsoft Store calls to action
- `product.html` - detailed repair workflow
- `faq.html` - user questions and FAQ structured data
- `google-takeout-photo-dates.html` - Google Takeout guide
- `photo-dates-after-moving-files.html` - file timestamp guide
- `mixed-photo-sources.html` - mixed photo library guide
- `privacy.html`, `terms.html`, `404.html` - policy and site pages
- `robots.txt`, `sitemap.xml` - crawler and indexing support
- `styles.css`, `subpages.css`, `app-preview.css`, `motion.css`, `site.js` - design and behavior
- `.github/workflows/deploy-pages.yml` - GitHub Pages deployment

The Store CTA uses `https://apps.microsoft.com/detail/9NFKQ1MV9399`. Canonical
URLs and sitemap entries use the GitHub Pages project URL. Keep those URLs
consistent if the repository name changes.
