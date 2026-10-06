# Portfolio Site Plan

## Goal

Build a static, personal portfolio for Sama Bari at `samabari.github.io`, aimed at recruiting in product marketing, growth marketing, go-to-market strategy, and technology/AI. The presentation should feel minimal, modern, polished, and tech-forward, with some personality. Use a light theme, clear sans-serif typography, generous whitespace, and simple navigation, drawing on the user's stated preferences for Apple and Notion.

## Pages and content

- **Home (`index.md`)** — Introduce Sama Bari using only accurate details supported by the résumé and link visitors to the other pages.
- **About (`about.md`)** — Summarize the résumé-supported professional focus and education. List UCLA only as an institution because the résumé does not state a degree there; include the Haas MBA and expected May 2027 completion as listed.
- **Work Experience (`experience.md`)** — Present the supplied Microsoft, Meta, Amazon, and Walmart eCommerce roles in reverse chronological order, preserving the résumé's employers, titles, dates, and accomplishments without adding claims.
- **Contact (`contact.md`)** — Show the email address the user approved for public display as a `mailto:` link. Do not add a contact form or backend.

All four pages will use YAML front matter, shared Jekyll layouts/includes, site navigation, and a consistent footer. Content will remain in Markdown, separate from the HTML and CSS presentation.

## Visual and accessibility direction

- Light theme only; clean, modern sans-serif typography with a professional, polished feel.
- Responsive single-column content and straightforward navigation, checked at 375px and 1280px widths.
- Semantic HTML, keyboard-accessible navigation, visible focus states, and accessible text/background contrast.
- Keep motion and JavaScript unnecessary; do not add third-party trackers or external services.

## Jekyll and publishing

- Make the repository root itself the complete GitHub Pages site: `index.md`, `_config.yml`, `_layouts/`, `_includes/`, `assets/`, the remaining Markdown pages, and `README.md` all live directly at the root.
- Configure a GitHub user site for `samabari.github.io` with an empty `baseurl`; use Jekyll URL filters for internal links and assets.
- Use GitHub Pages-compatible Jekyll features, SEO metadata, a sitemap, and a simple SVG favicon.
- Include a README with content-editing guidance, local preview instructions, and Lighthouse instructions.
- Aim for Lighthouse scores of at least 90 in Performance, Accessibility, Best Practices, and SEO. Verify the final source tree is publishable from the `main` branch and `/` (root), and verify internal navigation and the requested viewport widths.

## Content rules

- Use the supplied résumé as the source of truth for About and Work Experience.
- Do not invent or infer achievements, metrics, employers, clients, projects, degrees, or dates.
- Do not publish the résumé's phone number or location; the user explicitly approved the email address for public display.
- The résumé does not provide project descriptions or a full UCLA education credential, so do not create project content or infer a UCLA degree.

## Technical choices

- Use Jekyll with Markdown, YAML front matter, reusable Liquid layouts/includes, semantic HTML, and plain CSS.
- Use the GitHub Pages root publishing flow rather than a separate app, backend, database, CMS, or manual deployment build.
- Prefer a native system sans-serif font stack so the site stays fast and does not depend on a remote font service.
- Keep client-side JavaScript to none unless an essential, accessible interaction is identified.

## Assumptions

- The approved public contact method is the supplied `samabari@berkeley.edu` mailto link; no phone number or location will be shown.
- The homepage introduction will be limited to the professional focus and verified résumé details rather than adding an unsourced personal biography.
- A plain text-based favicon derived from the user's initials is acceptable because no logo or other brand assets were supplied.
- The current repository contains a starter API server, reusable libraries, and canvas mockup. Satisfying the root-only, Jekyll-only requirement means removing those starter files and replacing them with the Jekyll site; their contents will not be part of the published portfolio.
