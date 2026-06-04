# Building Bloch's — website

The public website for the Building Bloch's project. A small Jekyll site
(static HTML + one stylesheet) designed to run on GitHub Pages with **no build
configuration**.

## Structure

```
_config.yml          Site settings
index.html           Home
build.html           Build your own (bill of materials, files, firmware)
teach.html           Teach with it (lessons, level guide, troubleshooting)
play.html            Games & outreach (games, scripts, versions)
_layouts/default.html   Page shell: <head>, nav, footer
_includes/nav.html      Top navigation (edit once, applies to every page)
_includes/footer.html   Footer (edit once, applies to every page)
assets/css/style.css    All styling
assets/logo-badge.png   Logo
```

Every page uses **relative links**, so the site works at any URL —
`username.github.io/repo/` or a custom domain — with no `baseurl` changes.

## Host it on GitHub Pages

### Option A — in this repo, from a `/docs` folder (recommended)

1. Copy everything in this folder into a `docs/` folder at the root of your
   repository and push it.
2. On GitHub: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Branch: `main` (or `master`), folder: **/docs**. Save.
5. Wait ~1 minute. Your site appears at
   `https://<username>.github.io/<repo>/`.

Keeping the site in `/docs` means it lives happily alongside the firmware and
CAD folders without Jekyll trying to publish those.

### Option B — a dedicated repository, from the root

1. Create a new repo and put these files at its **root**.
2. **Settings → Pages → Source: Deploy from a branch → main → / (root)**.
3. Save and wait ~1 minute.

> Tip: a repo named `<username>.github.io` is served at the domain root
> (`https://<username>.github.io/`) instead of a sub-path.

## Editing

- Change text/structure in the `.html` pages.
- Change the menu or footer once in `_includes/` and it updates everywhere.
- Change colours, type and spacing in `assets/css/style.css` (design tokens
  live at the top under `:root`).

## Run it locally (optional)

```bash
gem install bundler jekyll
jekyll serve     # then open http://localhost:4000
```

You don't need this to publish — GitHub Pages builds it for you on every push.
