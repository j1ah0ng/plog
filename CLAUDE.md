# CLAUDE.md

## Project

plog - Tufte-style static blog built with Astro.

## Commands

```bash
yarn dev      # dev server at localhost:4321
yarn build    # build to dist/
yarn preview  # preview production build
```

## Architecture

```
src/
├── content/posts/*.mdx    # blog posts
├── components/
│   ├── Sidenote.astro     # margin footnotes (label/checkbox pattern)
│   ├── ThemeToggle.astro  # dark/light toggle
│   └── interactive/
│       └── PlotlyChart.astro
├── layouts/
│   ├── BaseLayout.astro   # HTML shell, theme init
│   └── PostLayout.astro   # post wrapper
├── pages/
│   ├── index.astro        # post listing
│   └── posts/[...slug].astro
└── styles/
    └── tufte.css          # all styles
```

## Key Implementation Details

**Fonts**: Latin Modern Roman (CDNFonts), JetBrains Mono (Google Fonts)

**Theme toggle**: Uses `data-theme` attribute on `<html>`, persists to localStorage, falls back to system preference. Inline script in `<head>` prevents flash.

**Sidenotes**: Canonical Tufte CSS pattern - `<label>` + hidden `<input type="checkbox">` + `<span class="sidenote">`. Pure CSS toggle on mobile (≤760px). Styled with accent color + dotted underline when collapsed.

**Code blocks**: github-light Shiki theme, inverted via CSS filter in dark mode. Transparent background matches page.

**Print**: `@media print` forces all sidenotes visible in margins, hides toggle, ensures contrast.

## Deployment

GitHub Actions workflow at `.github/workflows/deploy.yml`. Update `site` in `astro.config.mjs` before deploying.
