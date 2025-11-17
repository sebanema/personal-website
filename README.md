# Sebastian Anema – Personal Website

This is the source for my personal website.  
It is a simple static site built with HTML and CSS and deployed with GitHub Pages.

## Features

- Clean, serif typography inspired by classic personal sites.
- Sidebar navigation for About, Consulting, Projects, and Writing.
- Responsive layout that works on desktop and mobile.
- Contact call to action for booking a 30 minute call.
- Social links in the footer.

## Tech Stack

- HTML
- CSS
- GitHub Pages for hosting
- GitHub Actions for automatic deployment (`deploy.yml` in `.github/workflows`)

## Project Structure

```text
.
├── index.html          # Main page
├── styles/
│   └── main.css        # Global styles
├── images/             # Profile photo, icons etc
├── favicon.ico         # Site icon
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Pages deployment workflow
```

## Running the site locally

You do not need any build tools.

1. Clone the repository:

   ```bash
   git clone https://github.com/sebanema/personal-website.git
   cd personal-website
   ```

2. Open `index.html` directly in your browser, or run a simple local server, for example:

   ```bash
   python -m http.server 8000
   ```

   Then visit `http://localhost:8000`.

## Deployment (GitHub Pages)

Deployment is handled by GitHub Actions.

* Any push to the `main` branch triggers the `Deploy Website` workflow.
* The workflow publishes the contents of the repository to the `gh-pages` branch.
* GitHub Pages is configured in the repo settings to serve from the `gh-pages` branch.
* The live site is available at:

  ```text
  https://sebanema.github.io/personal-website
  ```

If you fork this repo, update the URL above to match your GitHub username and repo name.

## Using this as a template

If you want to reuse this layout:

1. Click **Use this template** on GitHub or fork the repository.
2. Update the content in `index.html` with your own name, copy, and links.
3. Replace the profile image and favicon in the `images` folder if desired.
4. Keep the `deploy.yml` workflow if you want automatic GitHub Pages deployment.
5. Enable GitHub Pages in your repository settings and point it to the `gh-pages` branch.

This gives you a minimal, easy to maintain personal site without any build tools.
