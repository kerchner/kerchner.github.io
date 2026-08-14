# Daniel Kerchner's personal academic website

Quarto website (no executable code cells) published to https://kerchner.github.io.
Source of truth for content is Dan's CV PDF (kept at repo root, untracked).

## Structure

- `_quarto.yml` — site config: navbar, footer, cosmo base theme + `styles/theme.scss` (light) and `styles/theme-dark.scss` (dark)
- `index.qmd` — trestles-style about page (headshot, bio, education, highlights)
- `experience.qmd`, `research.qmd`, `teaching.qmd`, `publications.qmd`, `presentations.qmd` — content pages
- `assets/` — `kerchner-cv.pdf` and `DanHeadshot.jpg` (stable filenames; linked from multiple pages)

## Conventions

- Publications/presentations are hand-authored markdown lists (not Quarto listings or BibTeX). Dan's name bolded (`**Kerchner D.**`), DOIs linked as `https://doi.org/<doi>`, reverse-chronological within sections.
- Never link URL shorteners (bit.ly/tinyurl) — resolve and link the canonical destination; use archive.org if the original is dead.
- When updating the CV, overwrite `assets/kerchner-cv.pdf` in place — do not add dated filenames; the link URL must stay stable.
- Contact email is `kerchner@gwu.edu` (not kerchner@email.gwu.edu).
- Keep the two SCSS themes' typography identical; only colors differ between light and dark.

## Publishing

- Source lives on `main`; the rendered site is force-pushed to `gh-pages` by Quarto. GitHub Pages serves the `gh-pages` branch (do not switch it back to `main` — that serves raw .qmd files).
- To deploy: commit changes to `main` (publish requires a clean working tree), then `quarto publish gh-pages --no-prompt`.
- Preview locally with `quarto preview`; `_site/` and `.quarto/` are generated and git-ignored.
- Dan's pre-2021 Jekyll site lives in the separate `kerchner-old-personal-site` repo — unrelated to this one.
