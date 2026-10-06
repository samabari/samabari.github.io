# Sama Bari — personal portfolio

A static Jekyll portfolio for GitHub Pages. The site is written in Markdown with YAML front matter, reusable Liquid layouts/includes, semantic HTML, and plain CSS.

## Update the site

- Edit the page content in `index.md`, `about.md`, `experience.md`, and `contact.md`.
- Shared page structure is in `_layouts/` and `_includes/`.
- Update site title, description, public email, and GitHub Pages URL in `_config.yml`.
- Styles live in `assets/css/site.css`; the SVG favicon is in `assets/images/favicon.svg`.
- Keep claims and career details consistent with the supplied résumé. The user's contact email is intentionally public.

## Preview locally

Install Ruby and Bundler, then run:

```sh
bundle install
bundle exec jekyll serve
```

Open `http://127.0.0.1:4000`. The Replit preview workflow uses the same Jekyll source.

## Publish with GitHub Pages

1. Push this repository to the GitHub account `samabari`.
2. In the repository's **Settings → Pages**, set the source to **Deploy from a branch**.
3. Choose the `main` branch and `/` (root) folder, then save.
4. The site will be published at `https://samabari.github.io`; no separate build workflow is required.

## Run Lighthouse

After the site is available locally or on GitHub Pages, open it in Chrome. Open Developer Tools → **Lighthouse**, select Performance, Accessibility, Best Practices, and SEO, and run the report for both desktop and mobile. The target is 90 or higher in every category. Use the report to identify any regressions before publishing.
