# Sam: Paint & Glass website

A single-page site for Sam (painting, gypsum ceilings, feature walls, glass installation).
Most photos and clips are embedded in `site/index.html`. Mirror and window inspiration
photos are stored locally in `site/assets/`.

## Run with Docker

    docker compose up --build -d
    # open http://localhost:8080

Stop it with `docker compose down`.

Without compose:

    docker build -t sam-paint-glass .
    docker run -d -p 8080:80 --name sam-paint-glass sam-paint-glass

## Deploy on a server

Copy this folder to the server, then run `docker compose up --build -d`.
Change `8080:80` to `80:80` in `docker-compose.yml` to serve on port 80,
and put a TLS proxy (Caddy, Traefik or Cloudflare) in front for HTTPS.

## Deploy with Vercel

The Vercel project deploys the static site from `site/` whenever a commit is
pushed to `main`. The public site is available at
`https://sam-paint-glass.vercel.app/`.

## Editing

Edit `site/index.html`, then rebuild: `docker compose up --build -d`.
The listed service area is Kenya; confirm town availability with Sam before requesting a visit.

## Notes

- The 3D hero loads three.js from cdnjs and fonts from Google Fonts, so visitors need internet access.
- The "Glass finishes" clip is used with permission from @fineariton. Keep that credit.
- The mirror and window inspiration photos are from Unsplash and are labeled as examples, not Sam's completed work. Their source links and creator credits are shown on the page.
- WhatsApp number used by the forms: +254 714 771606.
