# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Local Development

```bash
bundle install              # install Ruby dependencies (delete Gemfile.lock first if errors occur)
bundle exec jekyll liveserve  # serve at localhost:4000 with live reload
bundle exec jekyll serve      # serve without live reload
```

The `_config.yml` is not reloaded automatically — restart the server after changing it. Use `_config.dev.yml` to override settings for local development.

## Architecture

This is a Jekyll academic website based on the [academicpages](https://github.com/academicpages/academicpages.github.io) template (forked from Minimal Mistakes). The site has been trimmed down to the pages actually in use:

- `_pages/about.md` — homepage / bio (permalink `/`)
- `_pages/publications.md` — hand-written list of publications (permalink `/publications/`)
- `_pages/cv.md` — CV (permalink `/cv/`)
- `_pages/404.md` — not-found page

**Site configuration:** `_config.yml` controls author profile, social links, analytics, collections, and permalink structure. Navigation menus are in `_data/navigation.yml`.

**Theming:** Layouts live in `_layouts/`, partials in `_includes/`, and SCSS in `_sass/`. The `assets/` folder holds compiled JS and CSS.

## Adding Content

Publications are maintained directly as markdown in `_pages/publications.md` (not generated from data files). New standalone pages go in `_pages/` with YAML frontmatter and a `permalink`; add a link in `_data/navigation.yml` to surface them in the top menu.
