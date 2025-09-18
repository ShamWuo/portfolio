# ShamWuo — Portfolio

This repository contains the public build of my portfolio website. It is intended to host the compiled, static site that is served via GitHub Pages (or any static host). The source code and development artifacts live in a separate private repository.

Live demo
- https://shamwuo.github.io/  (or replace with your published Pages URL)

About
This site showcases my work, case studies, and experiments. The public repository contains only the generated/static files (HTML, CSS, images, and compiled JS) used to serve the live site. Source code, server-side code, and secrets are intentionally not included here.

What's included
- `index.html` — homepage and featured project
- `projects/` — case studies and project pages
- `assets/` — compiled CSS, JS, images, and icons
- `manifest.json`, `robots.txt`, and other site metadata

Run locally
Prerequisites: Node.js (LTS recommended)

1. Clone this repo (or download ZIP):

```powershell
git clone https://github.com/ShamWuo/ShamWuo.github.io.git
cd ShamWuo.github.io
```

2. Preview locally using `live-server` (no build step required):

```powershell
# Uses npx so a global install isn't required
npm run live
```

This runs `npx live-server --open=index.html --port=5500` and opens the site in your browser.

Development vs. Public build
- The public repo contains the built static site only. Development (source, build scripts, test harnesses) is kept in a private repository.
- If you want to work on features or code, request access to the private repo or clone the developer repo instead.

Deployment
- GitHub Pages: set the repository Pages source to the `main` branch. The site will be available at `https://<username>.github.io/<repo>` or via a custom domain if configured.
- CI/CD (recommended): Keep development in a private repo and push build artifacts to this public repo via a CI workflow (GitHub Actions). This keeps source private while publishing the site automatically.

Security & privacy notes
- This repo intentionally excludes secrets and `.env` files. Do NOT add API keys, credentials, or private data to the public repo.
- If you find secrets have been accidentally committed, rotate them immediately and contact the repo owner to remove them from history.

Contact
- Email: replace-with-your-email@example.com
- LinkedIn: https://www.linkedin.com/in/shamwuo

License
- This repository and the public site are released under the MIT License. See `LICENSE` for details.

—
If you'd like tweaks to the README (shorter summary, more contact links, or an included changelog), tell me which parts to change and I will update it.# ShamWuo.github.io

## Interactive Case Study
A new interactive case study page is available at `/projects/data-case-study.html`.
It uses D3 to render an interactive line chart from `/projects/data/sample-data.csv`.

- Open locally with the running live server: `http://127.0.0.1:5500/projects/data-case-study.html`
- Controls: date range, smoothing, add annotations, export PNG/CSV.

## Scaffolding
There's a simple scaffolder script at `tools/scaffold-case-study.js`:

```
node tools/scaffold-case-study.js my-new-case
```

This will create `/projects/my-new-case.html` and a sample CSV at `/projects/data/my-new-case-sample.csv`.
