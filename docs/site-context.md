# Personal Website Context

Last updated: 2026-03-06

## Purpose
- Static personal website for Sebastian Anema.
- Primary goals: introduce profile, show work, publish writing, and provide contact/social links.

## Stack and deployment
- Stack: plain HTML + CSS + tiny inline JavaScript (no framework/build step).
- Entry points:
  - `/index.html` (About/home)
  - `/work/index.html`
  - `/writing/index.html`
  - `/writing/*.html` (individual posts)
- Styling: `/styles/main.css`
- Assets: `/images`, `/favicons`
- Feed: `/rss.xml`
- Hosting/deploy: GitHub Pages via `.github/workflows/deploy.yml` (push to `main` deploys to `gh-pages`).

## Site-wide layout conventions
- Reused structure on all pages:
  - `.page-layout` wrapper
  - left `.sidebar` with `SA` logo + nav links
  - `.content > .content-inner`
  - shared footer with social SVG icons + dynamic year script
- Active nav item uses class `active`.
- Paths are root-relative (example: `/styles/main.css`, `/writing/`).

## Design and style conventions
- Visual direction: minimal editorial look, serif-forward typography.
- Main font stack: `"PT Serif", Georgia, ui-serif, Cambria, "Times New Roman", Times, serif`.
- Core colors:
  - `--brand-color: #0b1f3e`
  - `--brand-muted: #0f284c`
  - body text near-black (`#111111`)
- Spacing/layout:
  - desktop split layout with fixed-width sidebar
  - progressively collapses to stacked layout on tablet/mobile breakpoints
- Link behavior:
  - default links understated
  - links in `.content` are underlined with subtle offset/thickness

## Content conventions
- Writing index (`/writing/index.html`):
  - list entries in reverse chronological order
  - each item uses title link + human-readable date
- Post pages:
  - `article.post` containing `.post-header` and `.post-body`
  - hero image generally uses `<figure class="post-image post-hero">`
  - inline images use `<figure class="post-image">`
  - image alt text should be descriptive
- External links usually use `target="_blank"` with `rel="noreferrer"`.

## Reusable snippets
- Footer year script:
```html
<script>
  const y = new Date().getFullYear();
  const yearEl = document.getElementById('current-year');
  if (yearEl) {
    yearEl.textContent = y;
  }
</script>
```

## Working rules for future edits
- Keep the existing design language unless explicitly changing branding.
- Prefer reusing existing CSS classes over creating new one-off patterns.
- Maintain semantic HTML (`header`, `main`, `section`, `article`, `figure`).
- Preserve accessibility basics: alt text, readable heading hierarchy, clear link labels.
- Keep pages fully static and GitHub Pages friendly unless a conscious architecture change is requested.

## Content and voice notes
- Tone is personal, thoughtful, direct, and human (not corporate).
- Writing style favors narrative + concrete examples over abstract claims.
- Professional copy is concise and evidence-based.

## Session memory log
Use this section to preserve decisions across Codex conversations.

### 2026-03-05
- Created this file as the persistent context source of truth for future edits.
- Captured current architecture, layout conventions, styling patterns, and content rules.
- Personal Projects are grouped under `Financial Modelling` and `Software Development`.
- Qualifications currently use icon-as-bullet styling (`SU.jpg`, `CFA.png`), and key project rows use icons (`excel.jpg`, `debug.png`, favicon for personal site).
- Security review done: functionality passed; Cloudflare security headers recommended for later implementation.

### 2026-03-06
- Work page still collapses top-level sections on load, but inner professional experience and project entries are now rendered as readable blocks instead of deeply nested per-item toggles.
- Professional Experience is role-first; repeated-company roles can be bundled under one company block (example: Invictus Capital).
- Project titles are the primary links; extra CTA links under project cards were removed to keep the page simpler.
