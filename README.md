# porter

> GPU driver optimisation, program porting, and SteamOS on PS5.

Live at: [https://naveentk1.github.io](https://naveentk1.github.io)

---

## Local Development

### Prerequisites

- Ruby 3.1+
- Bundler

```bash
gem install bundler
```

### Run locally

```bash
bundle install
bundle exec jekyll serve
```

Then open [http://localhost:4000](http://localhost:4000).

---

## Writing a New Post

Create a file in `_posts/` with the format:

```
_posts/YYYY-MM-DD-your-post-title.md
```

With this front matter at the top:

```yaml
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD
categories: gpu mesa steamos  # whatever fits
---
```

Then write your post in Markdown below the `---`.

---

## Deploying to GitHub Pages

1. Push this repo to `github.com/naveentk1/naveentk1.github.io`
2. Go to **Settings → Pages**
3. Set source to **GitHub Actions**
4. Push to `main` — the site builds and deploys automatically

---

## Structure

```
porter/
├── _config.yml          # Site settings
├── _posts/              # Blog posts (YYYY-MM-DD-title.md)
├── about.md             # About page
├── index.md             # Homepage
├── Gemfile              # Ruby dependencies
└── .github/workflows/   # Auto-deploy to GitHub Pages
```
