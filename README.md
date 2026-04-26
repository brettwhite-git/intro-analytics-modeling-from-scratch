# Analytics Modeling From Scratch

Formula-first walkthroughs for core analytics modeling ideas. Each page pairs
the modeling question, the math, the R code, and the judgment calls that matter
when the method meets real data.

This is an independent educational resource. It is designed for learners who
want to understand how analytics models work rather than only call a library.

## Topics

- Classification: SVM and KNN
- Validation: train/test splits and cross-validation
- Clustering: k-means
- Change detection: CUSUM
- Time series: exponential smoothing, ARIMA, and GARCH
- Regression: linear and logistic regression
- Transformations: PCA and Box-Cox
- Trees: CART
- Variable selection, design of experiments, simulation, missing data,
  optimization, and selected advanced topics

## Local Preview

Install Quarto and R, then restore package dependencies:

```sh
Rscript -e "renv::restore()"
```

Preview the site:

```sh
quarto preview
```

Render the static site:

```sh
quarto render
```

Rendered output is written to `_site/`, which is intentionally ignored by Git.

## Publishing

This repo is configured for GitHub Pages through GitHub Actions. On each push
to `main`, the workflow restores the R environment with `renv`, renders the
Quarto site, uploads `_site/`, and deploys it to Pages.

After creating the GitHub repository, configure Pages to use **GitHub Actions**
as the source.

Expected project-site URL:

```text
https://<github-user>.github.io/intro-analytics-modeling-from-scratch/
```

## Repository Layout

- `_quarto.yml` - Quarto website configuration
- `*.qmd` - source pages
- `styles.css` - site styling
- `.github/workflows/publish.yml` - GitHub Pages deployment workflow
- `renv.lock` - reproducible R package environment

Generated folders such as `_site/`, `.quarto/`, and `scratch-files/` are not
part of the public source repository.

## License

This repository uses a dual-license model:

- Educational prose, explanations, tables, and generated figures are licensed
  under Creative Commons Attribution-NonCommercial 4.0 International.
- Code, configuration, CSS, and workflow files are licensed under MIT.

See [LICENSE.md](LICENSE.md) for details.
