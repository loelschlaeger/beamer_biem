## Aim :pushpin:

This repository contains a template for [LaTeX beamer slides](https://en.wikipedia.org/wiki/Beamer_(LaTeX)) and [Rmarkdown beamer slides](https://bookdown.org/yihui/rmarkdown/beamer-presentation.html) in corporate design of [Bielefeld University](https://www.uni-bielefeld.de/) and serves as a starting point to create a presentation for the Empirical Methods Department.

## Preview :eyes:

See [here](https://github.com/loelschlaeger/slides_template/blob/master/slides.pdf) for a preview of the slides.

## Using this template :pencil2:

1. Either

   - click ["Use this template"](https://github.com/loelschlaeger/slides_template/generate)

   - or download and unzip the repository (e.g., via [DownGit](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/loelschlaeger/slides_template/tree/master)).

2. Either

   - open and modify `slides.Rmd` (e.g., in [RStudio](https://posit.co/download/rstudio-desktop/)) and run `rmarkdown::render("slides.Rmd")`

   - or open and modify `slides.tex` (e.g., in [Overleaf](https://www.overleaf.com/)) and compile.

## Practical notes

- Main files to customize:
  - `slides.Rmd`: your content and examples
  - `theme/template.tex`: pandoc/beamer template logic
  - `theme/packages.tex`: package setup
- Default engine in `slides.Rmd` is `lualatex` (required for local Lelo font via `fontspec`).

### Appendix navigation buttons

The template exposes helper commands in `theme/template.tex`:

- `\appendixbutton{<target-label>}{<button text>}`
- `\returnbutton{<target-label>}{<button text>}`

Typical usage in `slides.Rmd`:

1. Give the source/target slides anchors via `\hypertarget{label_name}{}`.
2. Add a button on a main slide, e.g. `\appendixbutton{backup_model_details}{Details in appendix}`.
3. Add a return button on the appendix slide, e.g. `\returnbutton{main_results_slide}{Back to main slide}`.

A full working example is included in `slides.Rmd` under “Appendix navigation demo”.

## Contributing :construction_worker:

Have a question, found a bug, request a feature, want to contribute? [Please file an issue](https://github.com/loelschlaeger/beamer_biem/issues/new/).
