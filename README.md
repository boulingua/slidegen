# slidegen

Beamer (LaTeX) **slide template** in the [boulingua](https://github.com/boulingua)
design language, for generating course presentations that match the sister sites
and the [sheetgen](https://github.com/boulingua/sheetgen) worksheets.

> **Status — draft.** The theme and an example deck are in place; a
> content-to-slides generator will follow.

## Design language

- **Fonts:** Source Sans 3 (headings/body) + JetBrains Mono (code) — bundled in `fonts/`.
- **Accent:** boulingua blue `#1a73e8`; CEFR ramp (A `#4caf50`, B `#1a73e8`, C `#8e24aa`).
- **Watermark:** the boulingua logo + author **S. Le Boulanger** in the **lower-left of every slide**.
- Clean, minimal frames with an accent rule under each frame title.

## Usage

```bash
make example          # or: xelatex slides-template.tex  (run twice)
```

Requires **XeLaTeX** or **LuaLaTeX** (for `fontspec`). In your own deck:

```latex
\documentclass[aspectratio=169]{beamer}
\usetheme{boulingua}
\title{...}\subtitle{...}\author{S. Le Boulanger}
```

## Files

- `beamerthemeboulingua.sty` — the theme
- `slides-template.tex` — worked example
- `fonts/`, `assets/boulingua-logo.png` — bundled assets

## Licence

Code MIT (see `LICENSE`). The boulingua logo and name are used under the project's own terms.

## Use of LLM tools

Portions of this project were prepared with assistance from large language model tooling for narrowly defined, non-authorial tasks: copyediting, prose smoothing, Markdown/LaTeX formatting, scaffolding of boilerplate files (CI configs, build scripts), code refactoring. The tools used were Chat AI, the LLM service of KISSKI (GWDG), and a self-hosted Mistral Small (24B, Apache-2.0) run locally via Ollama and the ollamar R package — local inference only, with no data sent to third parties for the self-hosted model.
