# Jason Barnett — Portfolio Site

A personal portfolio site built to support a job search for strategic leadership roles in Solutions Engineering / Solutions Consulting (presales) and AI enablement — any industry.

**Live site:** _add your deployed URL here once live_

---

## About

This site exists to do one job: give a hiring manager or recruiter a fast, credible, evidence-backed picture of who Jason Barnett is as a leader — not just a list of claims. Every stat links back to something real (a video, a GitHub repo, an actual quote, actual photos), and the whole thing is built around one throughline: *the system behind the win, and the story that sells it.*

## Site Structure

The site is a small multi-page static site. The homepage carries the primary narrative; three deeper case studies live on their own pages, linked from a "Go deeper" section near the bottom of the homepage.

| Page | Purpose |
|---|---|
| `index.html` | Main page — hero, track record, career origin story, AI practical journey, industry impact, executive presence (keynote), customer engagement framework, leadership philosophy, team development, industry breadth, and contact |
| `vpw.html` | Case study — Vision Planning Workshop, evolution from an internal research tool (1.0) to a customer-facing alignment methodology (2.0) |
| `essentials.html` | Case study — Essentials by Adobe, a B2B advisor productivity platform (React/Node.js front end, Adobe Experience Cloud backend) |
| `education.html` | Academic Foundation — M.S., Computer and Information Technology (MCIT), University of Pennsylvania |
| `assets/` | Media (keynote video clip) |

## Tech Stack

Plain HTML5, CSS3, and vanilla JavaScript. No framework, no build step, no dependencies.

- **Fonts:** Space Grotesk (display), IBM Plex Sans (body), IBM Plex Mono (data/labels) — loaded via Google Fonts
- **JS:** IntersectionObserver-based scroll reveal, animated number count-ups on stat tiles, video poster/controls — all vanilla, no libraries
- **Images/video:** the hero photo and video poster frame are embedded as base64 data URIs directly in the HTML; the keynote video clip is a linked file in `assets/`

Each HTML page is fully **self-contained** — CSS and JS are inlined per page rather than pulled from shared external files. This is a deliberate choice: it trades a small amount of duplication for guaranteed portability, so the site renders correctly in any environment (local file preview, any static host) without depending on sibling files loading correctly.

## Running Locally

No build step required. Either:

```bash
# Just open it directly
open index.html

# Or serve it (recommended, avoids any local file:// quirks)
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

This is a static site with no build step, so it deploys cleanly to any static host.

**Vercel (current):**
```bash
npx vercel deploy
```
or drag the project folder onto [vercel.com/drop](https://vercel.com/drop).

**GitHub Pages:**
1. Push this repo to GitHub
2. Repo → Settings → Pages
3. Source: Deploy from a branch → `main` → `/ (root)`
4. Save — your site will be live at `https://<username>.github.io/<repo-name>/`

**Netlify:** drag the project folder onto [app.netlify.com/drop](https://app.netlify.com/drop).

## File Structure

```
.
├── index.html          # Main page
├── vpw.html             # Case study: Vision Planning Workshop
├── essentials.html      # Case study: Essentials by Adobe
├── education.html       # Academic Foundation
├── assets/
│   └── keynote-sizzle.mp4
└── README.md
```

## Important Notes

- **Keep the folder structure intact.** `index.html` and the other pages reference `assets/keynote-sizzle.mp4` by relative path — the `assets/` folder must stay alongside the HTML files, not be moved or renamed.
- **No secrets, no server, no database.** This is a pure static site — safe to host anywhere that serves static files.

## Contact

- Email: barnettmsg@gmail.com
- LinkedIn: [linkedin.com/in/jbarnettconnect](https://linkedin.com/in/jbarnettconnect)

---

© Jason Barnett
