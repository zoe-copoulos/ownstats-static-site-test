# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Minimal two-page static site for testing an OwnStats analytics tracking script. No build tools, no framework — plain HTML, CSS, and JS only.

## Development

Open locally with any static file server, e.g.:

```bash
npx serve .
# or
python3 -m http.server 8080
```

No build step, no dependencies to install.

## Architecture

| File | Role |
|---|---|
| `index.html` | Home page — navigation, descriptive copy, click-counter button |
| `about.html` | Second page — exists solely to produce a distinct page view |
| `styles.css` | Shared stylesheet, imported by both HTML files |

Both HTML files share the same `<head>` structure, including the placeholder comment:

```html
<!-- OwnStats tracking script goes here -->
```

This is the only place the tracking script should be inserted — once per file, inside `<head>`.

## Key constraint

Do not add build tools, frameworks, or any server-side code. The site must remain deployable as-is to GitHub Pages from the `main` branch root.
