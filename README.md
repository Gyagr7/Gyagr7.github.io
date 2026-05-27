# Gyaneshwar Agrahari — Personal Website

Multi-page static site, no build step. Deploys to GitHub Pages.

## Files

```
deploy/
├─ index.html       About / home
├─ research.html    Papers, preprints, talks
├─ teaching.html    Courses
├─ blog.html        Notebook
├─ contact.html     Contact + links
├─ styles.css       Shared styles
├─ CV.pdf           ← drop your CV here, name it CV.pdf
└─ photo.jpg        ← (optional) your portrait, 4:5 ratio looks best
```

## How to deploy to GitHub Pages

1. **Copy every file in `deploy/` to the root of your repo** `Gyagr7/Gyagr7.github.io`.
   (Don't copy the folder itself — copy the contents.)
2. Add your **CV as `CV.pdf`** at the repo root.
3. (Optional) Replace the embedded portrait placeholder with your own photo —
   see "Your photo" below.
4. Commit and push.
5. In **Settings → Pages**, confirm the source is `main` branch, `/ (root)`.
6. The site goes live at **https://gyagr7.github.io** within ~60 seconds.

## Your photo

The hero portrait on the About page ships with a "GA" monogram placeholder
embedded directly in `index.html` as a data URL, so the site looks complete
out of the box. To swap in your real photo:

1. Save a 4:5 portrait JPG as `photo.jpg` at the repo root.
2. In `index.html`, find the line that starts `<img src="data:image/png;base64,...`
   inside the `.ma-portrait` block, and replace the whole `src="..."` with
   `src="photo.jpg"`. That's it.

## What to edit before launch

Look for the comments marked `EDIT` in each HTML file — they call out
placeholder content to replace with your real information:

- **`research.html`** — replace placeholder paper titles, authors, venues, and tags.
  The "See all on Google Scholar" link is already wired to your profile.
- **`teaching.html`** — adjust the course list and the teaching statement.
- **`blog.html`** — replace the four placeholder post cards with real entries
  (or delete them — leaving "Coming soon" placeholders is also fine).
- **`index.html`** — tighten the four bio paragraphs in your own voice.
  The math marginalia ($\mathrm{sat}(n, P_k)$) is easy to swap for any
  research question you want on display.
- **`contact.html`** — confirm office address and add more links if you want
  (Twitter/X, arXiv author page, ORCID, Mastodon, etc).

## Dark mode

The site respects your OS-level dark/light preference automatically
(`prefers-color-scheme`). Remove `class="auto-theme"` from `<html>` in each
page if you want to lock to light mode.

## Math typesetting

KaTeX is loaded via CDN with auto-render. Write inline math with `$...$`
and display math with `$$...$$` anywhere in the body content.

## Local preview

Just open `index.html` in a browser. KaTeX and Google Fonts require
internet to render, but everything else works offline.
