# abhiraj2.github.io

Personal site of Abhiraj, built with [al-folio](https://github.com/alshedivat/al-folio) (Jekyll) and deployed to GitHub Pages by `.github/workflows/deploy.yml`.

## Where things live

| What                               | Where                                                        |
| ---------------------------------- | ------------------------------------------------------------ |
| Site settings, feature flags       | `_config.yml`                                                |
| Home, About, Experience, etc.      | `_pages/`                                                    |
| Project cards                      | `_projects/` (ordered by `importance`)                       |
| News timeline                      | `_news/` (one file per item; `display_date` overrides a date) |
| Publications                       | `_bibliography/papers.bib` and `_pages/publications.md`      |
| Contact links                      | `_data/socials.yml`                                          |
| Accent colour (burgundy)           | end of `assets/css/main.scss`                                 |
| Local theme overrides              | `_includes/header.liquid`, `_includes/news.liquid`, `_includes/footer.liquid`           |

## Run locally

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

or `docker compose -f docker-compose-slim.yml up` and open <http://localhost:8080>.

## Deploy

Push to `main`. The deploy workflow builds the site and publishes it to the `gh-pages` branch; in the repository settings, set Pages to serve from `gh-pages`.
