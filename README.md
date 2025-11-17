# Sebastian Anema — Personal Website

![License: MIT](https://img.shields.io/badge/License-MIT-lightgrey.svg) *(Code is public but not licensed for reuse without my explicit permission.)*

## Purpose
A simple, hand-coded site that introduces my consulting work, writing, and contact details in a single responsive page.

## Run Locally
```bash
git clone https://github.com/sebanema/personal-website.git
cd personal-website
python -m http.server 8000 # or open index.html directly
```
Visit `http://localhost:8000` to preview.

## Deployment via GitHub Pages
- `main` is the working branch.
- GitHub Actions workflow at `.github/workflows/deploy.yml` publishes the repo to the `gh-pages` branch on every push.
- GitHub Pages serves the content of `gh-pages`, so the live site automatically updates after each successful workflow.

## Updating the Site
1. Edit `index.html` and `styles/main.css` with your changes.
2. Commit and push to `main`.
3. The workflow redeploys; verify the production site at `https://sebanema.xyz` once GitHub Pages finishes.

## Notes
- Entry point: `index.html` at the project root.
- Assets live in the `/styles`, `/images`, and root `favicon.ico` paths to be friendly with GitHub Pages.
- Custom domain `sebanema.xyz` is configured through the `CNAME` file.
