# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Zark Incorporated marketing website - a single-page application (SPA) for a custom software solutions company specializing in insurance and financial sector software (Variable Product Administration, LifeCalc Pro, Examiner Pro).

## Tech Stack

- **Single HTML file**: All HTML, CSS, and JavaScript in `index.html`
- **No build system**: No package.json, npm, webpack, or transpilation
- **No dependencies**: Only Google Fonts (Orbitron, Playfair Display, DM Sans)
- **Vanilla JavaScript**: Custom SPA routing via `data-page` attributes

## Development

To view the site, open `index.html` directly in a browser or use a local server:
```bash
npx serve .
# or
python -m http.server 8000
```

## Architecture

**SPA Page Routing**: Pages are `<div class="page">` elements toggled via JavaScript. Navigation uses `data-page` attributes on clickable elements that trigger the `showPage()` function.

**Pages**: home, about, clients (partners), contact

**CSS Variables**: Color scheme defined in `:root` (lines 10-25) - primary blue (#1a3fa8), green (#1a7a4a), backgrounds (#f4f6fb)

**Responsive Breakpoints**: 900px (tablet), 640px (mobile)

## Key Implementation Details

- Contact form is client-side only (shows success message, does not submit to backend)
- Footer copyright year updates dynamically via `document.write(new Date().getFullYear())`
- Logo uses CSS text styling (Orbitron font with text-shadow), not an image
- Animations use CSS `@keyframes fadeUp` triggered when pages become active
