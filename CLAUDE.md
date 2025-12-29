# CLAUDE.md - Session State

## Status
plog complete with dark/light mode toggle.

## Stack
Astro 5 + MDX + Tufte CSS + KaTeX + Computer Modern + JetBrains Mono + GitHub Pages

## Commands
- `yarn dev` - local dev server
- `yarn build` - production build to `dist/`
- `yarn preview` - preview production build

## Key Files
- `src/content/posts/*.mdx` - blog posts
- `src/components/Sidenote.astro` - margin footnotes (checkbox toggle)
- `src/components/ThemeToggle.astro` - dark/light mode toggle
- `src/styles/tufte.css` - Tufte CSS + theme support
- `astro.config.mjs` - site/base config

## Fonts
- Body: Computer Modern Serif (CDN)
- Code: JetBrains Mono (Google Fonts)

## Theme
- Toggle button (top right)
- Uses `data-theme` attribute on `<html>`
- Persists to localStorage
- Falls back to system preference

## To Deploy
1. Update `site` in `astro.config.mjs` with your GitHub username
2. Push to `master` branch
3. Enable GitHub Pages (Settings > Pages > Source: GitHub Actions)
