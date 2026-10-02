# GitHub Pages Hosting

The production website is published from the public repository:

`https://github.com/nikatsam/FixMyPhotoDates-Website`

The Pages URL follows the project-site format used by the other product website:

`https://nikatsam.github.io/FixMyPhotoDates-Website/`

## Local preview

From the root of this website directory, run:

```powershell
python -m http.server 8000
```

Open `http://localhost:8000/`. In the application repository, serve from the
repository root and open `http://localhost:8000/website/` instead.

## Publishing

The public website repository contains `.github/workflows/deploy-pages.yml`.
It deploys the root-level website and application screenshot to GitHub Pages on
each push to `main`, or when manually run from the Actions tab.

GitHub Pages must use **GitHub Actions** as its build and deployment source.
The sitemap and canonical URLs use the project Pages URL above. If the
repository is renamed, update those URLs in the HTML pages, `robots.txt`, and
`sitemap.xml` before publishing.

After publication, verify the Pages deployment and HTTPS, then submit
`https://nikatsam.github.io/FixMyPhotoDates-Website/sitemap.xml` to Bing
Webmaster Tools, Google Search Console, and Yandex Webmaster.
