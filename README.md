# Building Blochs — website

The public website for the **Building Blochs** project: an open-source, motorised
Bloch-sphere demonstrator for teaching and outreach in quantum computing.

It's a small [Jekyll](https://jekyllrb.com/) site — static HTML + one stylesheet
for the main pages, plus a handful of Markdown manuals — that builds on GitHub
Pages with **no configuration**. The only runtime dependencies are Google Fonts
and (on the manual pages only) MathJax, both loaded from a CDN.

## Structure

```
.
├── _config.yml          # site title, description, Markdown + math build settings
├── _layouts/
│   ├── default.html      # shared <head>, nav + footer wrapper
│   └── manual.html       # wrapper for the Markdown manuals (meta cards + MathJax)
├── _includes/
│   ├── nav.html          # top navigation
│   └── footer.html       # site footer
├── index.html            # Home
├── build.html            # Build your own (placeholder — "coming soon")
├── teach.html            # Teach with it — lesson plans
├── play.html             # Games & laptop troubleshooting
├── styleguide.html       # internal design-system catalogue (not linked from the site)
├── MANUAL-*.md           # lesson plans & game manuals (Markdown, layout: manual)
└── assets/
    ├── css/style.css     # the entire design system
    ├── building-bloch.gif
    └── logo-*.png
```

The top-level pages are plain HTML with Jekyll front matter (`layout`, `title`,
`nav`, `description`). To add one, copy any of the `.html` pages, change the front
matter, and link to it from `_includes/nav.html`.

## House style

See [`styleguide.html`](styleguide.html) for all house style elements — a live
catalogue of every reusable component, rendered with the markup to copy. This page can in principle be found by anyone on the internet, but that won't normally happen for regular site visitors because no other page links to it. 

## Manuals

Lesson plans and game manuals live in `MANUAL-*.md` as plain **Markdown**, so they
stay easy to edit. Each carries `layout: manual` front matter, which renders it
through `_layouts/manual.html`: a page header, a row of "basic info" stat cards and
a "you need" checklist (both from a `meta:` list in the front matter), the rendered
body styled to match the design system, and `related:` cross-link buttons.

A few conventions:

- `permalink:` gives each manual a clean URL (e.g. `/manual-qx-orb.html`).
- In a `meta:` row, use `v:` for a stat card or `items:` for a checklist.
- Maths is written in LaTeX and typeset by **MathJax**. Use single `$…$` for inline
  and `$$…$$` for display, and write kets as `\lvert 0\rangle` — a literal `|`
  makes Kramdown try to parse a table. (`_config.yml` sets `math_engine: null` so
  Kramdown leaves the maths for MathJax.)
- Raw HTML blocks (e.g. a `.note` callout) work inside the Markdown as long as
  there's a blank line before and after.

## Run it locally

```bash
bundle install
bundle exec jekyll serve
# → http://127.0.0.1:4000
```

(Requires Ruby + Bundler. The `Gemfile` pins the `github-pages` gem so your local
build matches GitHub's.)

## Publish on GitHub Pages

Upon upload, Github will automatically update the website. For more information, search for 'GitHub Pages'.

## Theming

The look is driven entirely by CSS custom properties in `assets/css/style.css`.
The `<body>` carries `data-vibe` (`playful` / `editorial` / `bold`) and
`data-surface` (`warm` / `bright` / `slate`) attributes — set in
`_layouts/default.html` — which swap the radii, borders, shadows and paper tone.
Change those two attributes to re-skin the whole site.
