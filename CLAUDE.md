# CLAUDE.md - Session State

## Status
plog MVP complete and building successfully.

## Stack
Astro 5 + MDX + KaTeX + Computer Modern (CDN) + GitHub Pages

## Commands
- `yarn dev` - local dev server
- `yarn build` - production build to `dist/`
- `yarn preview` - preview production build

## Key Files
- `src/content/posts/*.mdx` - blog posts
- `src/components/Sidenote.astro` - margin footnotes
- `src/components/TOC.astro` - scroll-synced table of contents
- `src/components/interactive/PlotlyChart.astro` - interactive charts
- `astro.config.mjs` - site/base config for GitHub Pages

## To Deploy
1. Update `site` in `astro.config.mjs` with your GitHub username
2. Push to `master` branch
3. Enable GitHub Pages (Settings > Pages > Source: GitHub Actions)

## Writing Posts
Create `.mdx` files in `src/content/posts/` with frontmatter:
```yaml
---
title: "Post Title"
date: 2025-01-15
description: "Brief description"
draft: false
---
```

Use `<Sidenote id="1">content</Sidenote>` for margin notes.
Use `$...$` for inline math, `$$...$$` for display math.
