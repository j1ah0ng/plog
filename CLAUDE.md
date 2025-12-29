# CLAUDE.md - Session State

## Status
plog complete. Using canonical Tufte CSS with Computer Modern font.

## Stack
Astro 5 + MDX + Tufte CSS + KaTeX + Computer Modern (CDN) + GitHub Pages

## Commands
- `yarn dev` - local dev server
- `yarn build` - production build to `dist/`
- `yarn preview` - preview production build

## Key Files
- `src/content/posts/*.mdx` - blog posts
- `src/components/Sidenote.astro` - margin footnotes (checkbox toggle, no JS)
- `src/styles/tufte.css` - canonical Tufte CSS adapted for Computer Modern
- `astro.config.mjs` - site/base config for GitHub Pages

## To Deploy
1. Update `site` in `astro.config.mjs` with your GitHub username
2. Push to `master` branch
3. Enable GitHub Pages (Settings > Pages > Source: GitHub Actions)

## Writing Posts
```yaml
---
title: "Post Title"
date: 2025-01-15
description: "Brief description"
draft: false
---
```

Sidenotes: `<Sidenote id="1">content</Sidenote>`
Math: `$...$` inline, `$$...$$` display
Dark mode: automatic via `prefers-color-scheme`
