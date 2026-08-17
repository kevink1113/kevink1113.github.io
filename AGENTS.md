# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **static personal profile page** (the source for the GitHub Pages site `kevink1113.com`). It is plain HTML/CSS/JavaScript with no build system, no package manager, no dependencies, and no automated tests.

- **Structure**: `index.html` is the whole page (semantic sections: `#about`, `#career`, `#contacts`, `#tmi`). Styling is in `style.css` (Apple.com-inspired tiles, tokens, and responsive layout). Images/icons live in `files/`. `CNAME` sets the custom domain for GitHub Pages.
- **Third-party JS/CSS** (AOS scroll animations + Google Fonts Noto Sans KR) is loaded from CDNs at runtime. The days counter and mobile nav toggle are vanilla JS in `index.html` — no jQuery.
- **Run (development)**: serve the repo root with any static file server, e.g. `python3 -m http.server 8000`, then open `http://localhost:8000/`. There is no hot reload — refresh the browser after editing files.
- **Build**: none. GitHub Pages serves the files as-is; there is no build/compile step.
- **Lint**: no linter is configured. There is nothing to run.
- **Test**: no automated tests exist. Verify changes manually in the browser (check desktop and ~390px mobile widths, including the header menu toggle).
- **Notable behavior**: `#progress_long` updates via `requestAnimationFrame` with days since birth to one decimal place (changes slowly). The hero title (`.hero-title__svg text`) uses SVG stroke-draw (`titleStroke`, 5s) plus fill (`titleFill`, 4s). Body class `nav-open` expands the mobile global nav.
