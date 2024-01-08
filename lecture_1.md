# Lecture 1

Based on [Lecture 1 Course Notes](https://pages.github.ubc.ca/MDS-2023-24/DSCI_524_collab-sw-dev_book/materials/lectures/01_lecture-intro-to-r-and-python-pkgs.html)

## Video Analysis: RMarkdown Driven Development by

- literate programming: code and documentation in one place
- RMarkdown: markdown + R code

- Steps:
  1. Removing troublesome components
     - Good coding practicies: hard coding, magic numbers, etc.
     - use `here::here()` to avoid hard coding file paths
     - remove unsuccesful coding experiments
  2. Rearranging the code chunks
     - all computations first (infrastructure)
     - then visualizations and data wrangling (narrative)
  3. Reducing duplication using functions
     - to show difference in code using function params
     - document functions using roxygen2
  4. Migrating to a project
     - file structure:
       - `/analysis`: final reports
       - `/src`: source code/ scripts
       - `/data`: raw data
       - `/results`: intermediate data
  5. Convert project to a package

## Packages in R and Python

| Description                        | Pytoon                                                                                                                     | R                            |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ---------------------------- |
| Online package repo or index       | PyPI or Conda                                                                                                              | CRAN or Conda                |
| Directory for user-facing packages | src or folder related to package name (flexible) </br></br> (any named dir as long as it has `__init__.py` and `.py` file) | `R` directory (not flexible) |
| Directory for test packages        | tests                                                                                                                      | `tests/testthat`             |
| Directory for documentation        | docs                                                                                                                       | `man` and `vignettes`        |
| Package metadata                   | pyproject.toml                                                                                                             | `DESCRIPTION`                |
| Files that define the namespace    | `__init__.py`                                                                                                              | `NAMESPACE`                  |
| Tools for easy package creation    | `poetry` or `cookiecutter`                                                                                                 | `devtools` and `usethis`     |
