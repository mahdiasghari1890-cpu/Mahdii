# Base44 Dev Environment

## Project Overview
A static personal portfolio website (Persian/Farsi, RTL layout) built with plain HTML, CSS, and JavaScript. Uses Tailwind CSS and Feather Icons via CDN. No build step, no backend, no database.

## Running the App
```bash
docker compose -f docker-compose.base44.yml up -d
```
Serves static files via nginx:alpine on port 3000.

## Notes
- The HTML references `components/navbar.js`, `components/footer.js`, and `components/scroll-to-top.js` which do not exist in the repo — these 404 silently and don't break the page.
- No external credentials or secrets are required.
- No live-reload dev server; edits to static files require a `reload_preview` call to reflect in the preview.
