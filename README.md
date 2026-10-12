# FuRuF-11.github.io

My personal website: https://furuf-11.github.io

Built with [Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) theme.

## Structure

| Page    | Source                         | Content                                     |
| ------- | ------------------------------ | ------------------------------------------- |
| About   | `_pages/about.md`              | Home page / biography                       |
| Blog    | `_pages/blog.md`, `_posts/`    | Blog posts (`YYYY-MM-DD-title.md`)          |
| Thought | `_pages/thoughts.md`, `_thoughts/` | Essays and ideas (`YYYY-MM-DD-title.md`) |
| Project | `_pages/projects.md`, `_projects/` | Project cards                            |

A new thought or blog post only needs front matter like:

```yaml
---
title: "My title"
date: 2025-01-01
description: "One-line summary"
---
```

## Local preview

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

Or with Docker: `docker compose up` (http://localhost:8080).

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site and publishes it to the `gh-pages` branch.
In the repository settings, **Pages → Build and deployment → Source** must be "Deploy from a branch", branch `gh-pages` / `(root)`.
