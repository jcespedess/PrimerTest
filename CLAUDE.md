# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a minimal static web project used as a learning exercise for Git and Vue.js basics. There are no build tools, package managers, or test frameworks — it runs directly in a browser.

## File Structure

- `index.html` — Entry point. Loads Vue.js 2.5.17 via CDN and mounts a Vue instance on `#miApp`.
- `app.js` — Standalone JS file with a console log; currently not linked from `index.html`.
- `style.css` — Empty stylesheet; not yet linked from `index.html`.

## Running the Project

Open `index.html` directly in a browser, or serve it with any static file server:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Architecture Notes

- Vue 2 is loaded from CDN (`vue@2.5.17`), so there is no `npm install` step.
- The Vue instance is defined inline in `index.html` using `new Vue({ el: '#miApp', data: { mensaje: 'Hola Mundo' } })`.
- `app.js` and `style.css` are not referenced by `index.html` and would need `<script src="app.js">` / `<link rel="stylesheet" href="style.css">` tags added to take effect.
