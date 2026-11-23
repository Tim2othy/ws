# ws

Source for my personal Jekyll site.
This file is for development only: it's in `exclude` in `_config.yml`, so it is never built or published.

## Preview the site in a browser

Needs Ruby and Jekyll (`gem install jekyll webrick`).

From the repo root:

```sh
jekyll serve --livereload
```

Then open <http://127.0.0.1:4000>.

## Paper PDFs

Not committed (`assets/papers/*.pdf` is gitignored).
On deploy, `.github/workflows/pages.yml` downloads the latest release PDF from the paper repo.
For a local preview, put a copy at `assets/papers/ai-risk-in-race.pdf`.
