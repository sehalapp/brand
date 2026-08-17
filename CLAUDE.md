# CLAUDE.md

Guidance for Claude Code (claude.ai/code) when working in this repository.

## What this repo is

`sehalapp/brand` — the home for Sehal's brand: the specification, the logo and icon
masters, and the published guideline site.

**This repository is public**, and [BRAND.md](./BRAND.md) plus the GitHub Pages site are
the customer-facing brand guideline. Anything that discusses unshipped decisions, internal
code paths, the previous identity, or gaps between the spec and the product belongs in
`internal/` (gitignored) — never in `BRAND.md`, `index.html` or this file.

Contents:

- [BRAND.md](./BRAND.md) — the specification. The source of truth.
- [index.html](./index.html) — the visual board, deployed to
  [sehalapp.github.io/brand](https://sehalapp.github.io/brand/). Self-contained: Vend Sans
  and Manrope are embedded as base64 woff2, all logo geometry is inline SVG, no external
  requests.
- [assets/](./assets/) — production logo vectors. The wordmark is **outlined**, not live
  text, so these render without the fonts installed.
- `.github/workflows/deploy-pages.yml` — publishes `index.html` and `assets/` to Pages on
  push to `main`.

There is deliberately no `package.json` and no build step. The brand facts are settled in
`BRAND.md` first; token files and asset exports get generated from it.

## Conventions

- Markdown and self-contained HTML. Keep documents in this directory, flat; logo vectors
  go in `assets/`.
- **Nothing internal goes in `BRAND.md`, `index.html`, `README.md` or this file.** The repo
  is public. Unshipped decisions, product code paths, the previous identity, and any gap
  between the spec and the app live in `internal/`, which is gitignored.
- `BRAND.md` states rules directly — it is a specification, not an audit. Record
  measurements (contrast ratios, sizes) next to the rule they justify, and date them.
- **Never hand-edit `assets/*.svg`.** They are generated from the masters in
  `design/assets/{icon,logo-light,logo-dark}.svg` and recoloured to the brand palette on
  the way out. Change the master, then re-emit.
- The wordmark is **artwork, not type**. It is Vend Sans ~500 with tighter tracking,
  converted to outlines — close enough that re-setting it looks nearly right and is not.
  Never rebuild it by setting the word in a font.
- `index.html` must stay self-contained — fonts base64-inlined, geometry inline SVG, no
  external requests. It is a complete document (doctype, `<head>`, `<body>`) because
  GitHub Pages serves it directly; without the doctype browsers fall into quirks mode,
  where tables stop inheriting `color`. Keep the body all-ASCII (HTML entities for `§`,
  `—`, `×`) so it survives any charset mishap.
- Mockups with a fixed `aspect-ratio` (hero, OG card, banner, slides) size their type in
  `cqw` against a `container-type:inline-size` wrapper, never `vw` — they render side by
  side in the compare view at roughly a third of viewport width, where `vw` overflows.
- The Pages workflow publishes `index.html` and `assets/` only. If you add a file that
  should be public, add it to `.github/workflows/deploy-pages.yml` explicitly.
