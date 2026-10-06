# Alex's blog

A small Hugo site with a custom layout (no theme dependency). Light and dark mode, posts grouped by year, tag filters, RSS.

## Run it locally

```sh
brew install hugo        # once
hugo server -D           # http://localhost:1313 (-D also shows drafts)
```

## Write a post

```sh
hugo new content posts/my-first-climb.md
```

That creates a draft. Write in Markdown, then set `draft: false` (or delete the line) when it's ready.
Front matter you can use:

```yaml
---
title: "Three weeks on one problem"
date: 2026-10-06
tags: ["bouldering"]
description: "One-line summary for search engines and link previews."
draft: false
---
```

Images go in `static/images/` and are referenced as `/images/name.jpg`.

## Edit your details

Everything personal is in `hugo.toml`: greeting, about text, the "now" line, social links, and an optional photo
(`avatar = "images/me.jpg"` after you drop the file in `static/images/`).

Look and feel live in `static/css/style.css`. Colours are CSS variables at the top of that file.

## Publish on GitHub Pages (free)

1. Create a new **public** repo on GitHub.
   - Name it `YOUR-USERNAME.github.io` to get `https://YOUR-USERNAME.github.io/`.
   - Any other name works too, it just lives at `https://YOUR-USERNAME.github.io/REPO-NAME/`.
2. Push this folder:
   ```sh
   git init -b main
   git add .
   git commit -m "First version of the blog"
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
4. Watch the **Actions** tab. When the run goes green, the site is live.

After that, every `git push` to `main` rebuilds and redeploys automatically.

## Adding a domain later

Buy the domain, then in **Settings → Pages → Custom domain** enter it and follow GitHub's DNS instructions.
No changes to the site are needed; the deploy workflow picks up the new address on its own.

## Layout

```
hugo.toml                  site settings and your personal details
content/posts/             your posts (Markdown)
layouts/                   page templates (home, post, lists, header, footer)
static/css/style.css       styles, light and dark
static/css/syntax.css      code highlighting colours
.github/workflows/hugo.yml build + deploy to GitHub Pages
```
