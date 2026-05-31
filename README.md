# Xiao Lin Personal Homepage

This repository contains the source code for Xiao Lin's personal academic homepage. The site is a lightweight static page built around a single `index.html` file, with local assets for profile images, logos, documents, and generated thumbnails.

## Overview

The homepage includes:

- Research profile and contact links
- Work experience
- News and selected updates
- Publications with topic filters and a "load more" interaction
- Awards and academic service
- Downloadable resume and related files

## Project Structure

```text
.
├── index.html              # Main homepage
├── CNAME                   # Custom domain for GitHub Pages
├── .nojekyll               # Disable Jekyll processing on GitHub Pages
├── files/                  # Resume and downloadable documents
├── images/                 # Profile images, logos, and visual assets
└── generate_thumbnails.py  # Utility script for image thumbnail generation
```

## Local Preview

Because the site is static, it can be previewed with any local HTTP server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Opening `index.html` directly in a browser also works for most content, but using a local server better matches GitHub Pages behavior.

## Editing Guide

- Update the main site content in `index.html`.
- Add or replace profile and logo assets under `images/`.
- Place resume or other downloadable documents under `files/`.
- Publication filters are controlled by each publication item's `data-tags` attribute and visible tag spans.
- The publication "load more" behavior is implemented in the JavaScript section near the end of `index.html`.

## Deployment

The repository is configured for GitHub Pages-style static hosting:

- `CNAME` stores the custom domain.
- `.nojekyll` ensures GitHub Pages serves the static files directly.

After pushing changes to the hosting branch, the homepage should update automatically according to the GitHub Pages deployment settings.
