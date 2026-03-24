# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal portfolio/resume website for Harsh Wadhawe, hosted on GitHub Pages at `harsh3173.github.io`. It is a static site (no build step, no framework) based on the CEEVEE template (Creative Commons Attribution 3.0).

## Development

No build tools, package managers, or test runners are used. To preview locally, open `index.html` in a browser or use any static file server (e.g., `python3 -m http.server`).

Deployment is automatic via GitHub Pages on push to `main`.

## Architecture

- **`index.html`** — Single-page site with all content. Sections: Home/header, About, Certifications, Projects, Footer. Navigation uses smooth-scroll anchors.
- **`css/`** — `default.css` (base/reset styles), `layout.css` (main layout), `media-queries.css` (responsive breakpoints), `magnific-popup.css` (lightbox plugin). Also includes vendored Font Awesome and Fontello icon fonts, plus self-hosted Open Sans and Libre Baskerville web fonts.
- **`js/`** — `init.js` (site initialization, smooth scroll, fittext, waypoints setup). Remaining files are vendored jQuery 1.10.2 and plugins (FlexSlider, Waypoints, FitText, Magnific Popup, Modernizr).
- **`images/`** — All site images: profile photo, education logos, certification badges, project screenshots, favicon set.
- **`inc/sendEmail.php`** — Server-side email handler (currently unused since contact form was removed).
- **`try.css`** — Appears to be an experimental/scratch stylesheet.

## Key Details

- Inline `<script>` blocks at the bottom of `index.html` handle scroll-triggered animations for `.cert-card` and `.projects-card` elements using IntersectionObserver.
- Google Tag Manager (`GTM-5J5KGXZ`) and Google Analytics are loaded in the `<head>`.
- jQuery is loaded from Google CDN with a local fallback (`js/jquery-1.10.2.min.js`).
- The template license requires a credit link to styleshout.com (see `readme.txt`).
