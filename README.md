# essays-and-meditations

Personal bilingual (English/Persian) blog powered by **GitHub Pages + Jekyll**.

## Structure

- `index.md` — language chooser
- `en/` — English essay index
- `fa/` — Persian essay index
- `_essays_en/` — English essay markdown files
- `_essays_fa/` — Persian essay markdown files
- `_layouts/` — shared page and essay layouts
- `assets/css/` — site styles

Add new markdown files to `_essays_en` or `_essays_fa`. Each essay should include front matter:

```yaml
---
layout: essay
title: Essay title
date: 2026-06-21
lang: en
text_direction: ltr
---
```

Persian essays should use `lang: fa` and `text_direction: rtl`.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

The site is configured for the GitHub Pages project path `/essays-and-meditations`. If the repository name changes or you publish with a custom domain, update `baseurl` in `_config.yml`.
