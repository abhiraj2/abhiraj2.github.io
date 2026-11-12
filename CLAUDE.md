# CLAUDE.md

Personal portfolio site built on the al-folio v1.x Jekyll starter. Layouts, includes and Sass come from the `al_folio_core` gem; this repo holds config, content and three deliberate local overrides.

- Content: `_pages/`, `_projects/`, `_news/`, `_bibliography/papers.bib`, `_data/socials.yml`.
- Local overrides of gem files (keep them minimal; re-check after gem upgrades with `bundle exec al-folio upgrade overrides audit`):
  - `assets/css/main.scss`: copy of the gem entry stylesheet with a burgundy accent block appended at the end.
  - `_includes/header.liquid`: navbar shows `site.first_name` instead of the long SEO `site.title`.
  - `_includes/news.liquid`: month-level dates and the `display_date` front matter field.
- `Gemfile` and `_config.yml` `plugins:` must list the same plugins.
- `baseurl` is empty: the site is served from the root of the custom domain `theabhiraj.com` (set by the `CNAME` file; DNS is on Cloudflare).
- Build: `bundle exec jekyll build`. Format: `npx prettier . --write`.

Content rules: no resume/CV, no quant or trading content, Goldman Sachs is one line only ("Listed Derivatives, Distributed Systems."), and unpublished work carries a status badge and never appears under Publications.
