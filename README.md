# Priyanka Kumari — AI/ML Engineer Portfolio

Static portfolio site for `pinkaofc`, with a full build log and walkthrough for every featured project.

**Live:** https://pinkaofc.github.io

## Structure

```
index.html                 Home — hero, work, skills, about, contact
404.html                   Custom not-found page (GitHub Pages picks this up automatically)
style.css                  Site-wide styles and design tokens
case.css                   Styles for the case-study pages
script.js                  Nav toggle, scroll reveals, cursor glow
project/                   One case-study page per featured project
  ai-research-agent.html
  ticket-booking-system.html
  emotiongesture-ai.html
  grammar-spell-checker.html
  resume-screening-app.html
  movie-recommendation-system.html
assets/
  priyanka.jpg             Profile photo
  favicon.svg              Site icon
robots.txt / sitemap.xml   SEO
```

No build step, no dependencies — plain HTML, CSS and JavaScript.

## Case-study pages

Each project page follows the same structure, so the six read as one body of work:

1. **The problem** — what actually breaks, stated concretely
2. **Architecture** — the pipeline or data flow
3. **Build log** — the decisions that shaped the system, and why each was made
4. **Walkthrough** — running it end to end, with real commands
5. **Stack** — the tools, and a link to the source

Every project card on the home page links to all three entry points: `Build Log →`, `Walkthrough`, `Repo ↗`.

## Deploy

This repo is published with **GitHub Pages** from the `main` branch, `/ (root)`.

To set it up on a fresh repository:

1. Create a public repository named `pinkaofc.github.io`.
2. Push this directory to `main`.
3. **Settings → Pages → Deploy from a branch** → `main` / `/ (root)`.
4. Wait ~60 seconds, then visit https://pinkaofc.github.io.

Because the repo is named `<username>.github.io`, the site is served from the domain root — which is why internal links and the sitemap use root-relative paths.

## Local preview

```bash
python -m http.server 8000
```

Then open http://localhost:8000.

## Editing content

Project write-ups live directly in the `project/*.html` files. Each one is self-contained;
copy an existing page as the template when adding a seventh project, and remember to add
the new URL to `sitemap.xml` and a card to the project grid in `index.html`.

## Still to add

- `assets/resume.pdf` — no resume link is shown on the site until this exists.
