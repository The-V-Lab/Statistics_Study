
# The V Lab Learning & Project Hub

The account-wide learning and project portal for The V Lab GitHub organization (The-V-Lab), and the home of the biostatistics course. The home page indexes 39 standalone HTML pages across eight public repositories and links to the epidemiology, data visualization, R Markdown, synthetic health-data project, Snowflake and ArcGIS material, plus the Alberta Health Data Atlas.

## Live site

Visit [The V Lab Learning & Project Hub](https://the-v-lab.github.io/Statistics_Study/) to browse the projects, search every HTML page, or follow the recommended biostatistics learning path.

## Account directory

The directory was first verified on 2026-08-12 and updated on 2026-10-16 against eight public repositories:

- 39 standalone HTML pages, all published through GitHub Pages;
- the `includes/` header and footer fragments are not counted as standalone pages;
- `HealthcareData_Knowledge` has no repository HTML; the Alberta Health Data Atlas is linked at [vthelab.com/atlas.html](https://vthelab.com/atlas.html);
- the home-page directory is static HTML. Search and filters run in the browser only; they do not call the GitHub API or collect any input.

## Files

- `index.html`: account overview, the searchable directory of HTML pages, and the recommended biostatistics learning path.
- `biostatistics_foundations.html`: biostatistics foundations.
- `medical_statistical_tests_en.html`: common statistical tests in medical research.
- `linear_regression_en.html`: linear regression.
- `logistic_regression_en.html`: logistic regression.
- `design_of_experiments_en.html`: randomization, blocking, factorial designs, randomization inference and power.
- `clinical_trials_en.html`: clinical trial design, estimands, common outcome models, missing data and reporting.
- `poisson_zero_inflated_models_en.html`: Poisson, negative binomial and zero-inflated count models.
- `multilevel_modelling_en.html`: multilevel models for clustered and longitudinal data, variance partitioning, partial pooling, LMMs and GLMMs.
- `longitudinal_data_analysis_en.html`: repeated measures, covariance structures, marginal models and mixed-effects trajectories.
- `causal_inference_en.html`: causal inference.
- `propensity_score_matching_en.html`: design, diagnostics and effect estimation for propensity score matching.
- `survival_analysis_en.html`: survival analysis fundamentals, complex event processes and a complete applied workflow.
- `aft_cox_models_en.html`: AFT and Cox PH survival models.
- `meta_analysis_en.html`: effect sizes, heterogeneity, forest plots and sensitivity analyses in medicine and psychology.
- `includes/vlab-brand.html`: The V Lab brand component shared by the guide pages.
- `og-learning-hub.png`: social preview image for the learning site.
- `og.png`: preview image kept for older links to the foundations module.
- `.nojekyll`: lets GitHub Pages publish the static files as they are.
- `styles.css`: page styles, including mobile and print layouts.
- `render.R`: finds every Rmd file in the project root and renders an HTML file with the same name.

## Re-rendering

The `.Rmd` sources are kept only in local working copies and are excluded by `.gitignore`, so they are not published to GitHub. The rendered HTML shows the teaching code but no longer embeds a downloadable copy of the full Rmd source.

In a working copy that has the local Rmd sources, run:

```bash
Rscript render.R
```

The project uses `.Rlib` as its local R package library. If dependencies are missing, run:

```bash
mkdir -p .Rlib
Rscript -e 'install.packages(c("rmarkdown", "knitr", "survival", "nlme", "MatchIt", "lme4"), lib = ".Rlib", repos = "https://cloud.r-project.org")'
```

All data in these documents are simulated with fixed random seeds and contain no real personal health information.
