# plog

A static blog with Tufte-style typography, margin sidenotes, LaTeX math, and interactive visualizations.

## Stack

- **Framework**: Astro 5 + MDX
- **Styling**: Tufte CSS (adapted)
- **Fonts**: Latin Modern Roman (body), JetBrains Mono (code)
- **Math**: KaTeX
- **Charts**: Plotly.js
- **Deployment**: GitHub Pages via Actions

## Development

```bash
yarn install
yarn dev      # local dev server
yarn build    # production build
yarn preview  # preview build
```

## Writing Posts

Create `.mdx` files in `src/content/posts/`:

```mdx
---
title: "Post Title"
date: 2025-01-15
description: "Brief description"
draft: false
---

import Sidenote from '../../components/Sidenote.astro';

Body text with a sidenote.<Sidenote id="1">Appears in margin on desktop, expands on tap on mobile.</Sidenote>

Inline math: $e^{i\pi} + 1 = 0$

Display math:
$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$
```

## Features

- **Sidenotes**: Margin notes on desktop, tap-to-expand on mobile
- **Scroll timeline**: Progress indicator with section markers, hover to reveal titles
- **Dark/light mode**: Toggle button, persists preference, respects system default
- **Responsive**: Wide margins on desktop, full-width on mobile
- **Print styles**: All sidenotes expanded, good contrast
- **LaTeX**: Full KaTeX support for math
- **Interactive charts**: Plotly.js integration

## Deployment

1. Update `site` in `astro.config.mjs` with your GitHub username
2. Push to `master` branch
3. Enable GitHub Pages (Settings → Pages → Source: GitHub Actions)
