# LiDAR Matrix — website

Custom [Jekyll](https://jekyllrb.com/) static site for **LiDAR Matrix, Inc.**,
served free on GitHub Pages. Brand: Petrol Navy `#143240` + Copper `#C67F3C`,
Libre Franklin type. No third-party theme — the design lives in
`assets/css/style.css` and `_layouts/default.html`.

## Edit & re-publish cheat sheet

```bash
# 1. Preview locally (auto-reloads as you edit)
bundle exec jekyll serve --livereload
#    → open http://127.0.0.1:4000  ·  stop with Ctrl-C

# 2. Publish your changes
git add .
git commit -m "Describe what you changed"
git push
#    → live at the site URL in ~1 minute
```

Edit a page → save → the local preview updates instantly → commit & push when happy.

## What's where

| Path | What it is |
|---|---|
| `index.md` `services.md` `projects.md` `about.md` `contact.md` | The five pages (HTML + placeholder copy inside Markdown). |
| `_layouts/default.html` | Shared shell — header, nav, footer, favicons, SEO. Edit once, applies everywhere. |
| `_includes/thumb.html` | The LiDAR point-cloud graphic used as project thumbnails. |
| `assets/css/style.css` | The whole design system — colors, type, components. |
| `assets/img/logo/` | Logo + favicon files. |
| `_config.yml` | Site title, description, nav order, and the contact email. |
| `DOMAIN-TRANSFER.md` | Steps to move `lidarmatrix.com` over later. |

## Before public launch — replace these placeholders

- **Email:** `INFO@LIDARMATRIX.COM` in `_config.yml` → real inbox.
- **Contact page:** phone and mailing address.
- **About page:** leadership names/bios, founding year, headcount.
- **Home stat band:** confirm the four headline numbers in `index.md`.
- **Projects:** confirm the RTC dashboard details (flagged in the source summaries).

## Local setup (first time only)

Requires Ruby 3.x, then:

```bash
gem install jekyll bundler
bundle install
```
