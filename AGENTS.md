# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **static personal profile page** (the source for the GitHub Pages site `kevink1113.com`). It is plain HTML/CSS/JavaScript with no build system, no package manager, no dependencies, and no automated tests.

- **Structure**: `index.html` is the whole page. Styling is in `style.css` (`style 2.css` appears to be an unused backup). Images/icons live in `files/`. `CNAME` sets the custom domain for GitHub Pages.
- **Third-party JS/CSS** (AOS animations, jQuery, prognroll progress bar, Google Fonts) is loaded from CDNs at runtime, so an internet connection is needed for the page to look/behave exactly like production. Core content still renders without it.
- **Run (development)**: serve the repo root with any static file server, e.g. `python3 -m http.server 8000`, then open `http://localhost:8000/`. There is no hot reload — refresh the browser after editing files.
- **Build**: none. GitHub Pages serves the files as-is; there is no build/compile step.
- **Lint**: no linter is configured. There is nothing to run.
- **Test**: no automated tests exist. Verify changes manually in the browser.
- **Notable behavior**: `index.html` runs a small inline script that live-updates a "days breathing" counter (`#progress_long`). It ticks every 30ms but is displayed in days to one decimal, so the visible value changes very slowly.
