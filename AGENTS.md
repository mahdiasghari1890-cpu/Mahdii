# AGENTS.md

## Project Overview
Static personal portfolio website (Persian/Farsi, RTL layout) built with plain HTML, CSS, and JavaScript.
Uses Tailwind CSS via CDN (`https://cdn.tailwindcss.com`) and Feather Icons via CDN.
No build step, no backend, no database.

## Dev Environment
- Served by Vite dev server on port 3000 (configured in `vite.config.js` and `docker-compose.base44.yml`).
- `package.json` contains only Vite as a dev dependency for live reload.
- Start: `docker compose -f docker-compose.base44.yml up -d --build`
- Health check: `curl http://localhost:3000/`

## Known Issues
- `index.html` references `components/navbar.js`, `components/footer.js`, `components/scroll-to-top.js` — these files do not exist in the repo. They 404 on load but do not prevent the page from rendering.
- Some asset paths in `index.html` use backslashes (`assets\Picture6.png`) which may not resolve on Linux.
