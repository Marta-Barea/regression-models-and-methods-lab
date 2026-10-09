[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)
[![R](https://img.shields.io/badge/R-Regression_Models-276DC3?logo=r&logoColor=white)](https://www.r-project.org/)
[![R Markdown](https://img.shields.io/badge/R%20Markdown-Reports-0B4F6C?logo=rstudioide&logoColor=white)](https://rmarkdown.rstudio.com/)
[![Activity A1 PDF](https://img.shields.io/badge/Activity_A1-PDF-1b5e20)](reports/activity-a1.pdf)

# Regression Models and Methods Lab

## Overview

This repository contains R-based coursework for **Regresión, Modelos y Métodos** (M0.156), part of the Interuniversity Master's Degree in Bioinformatics and Biostatistics at the Universitat Oberta de Catalunya and the Universitat de Barcelona.

The reports combine statistical reasoning, mathematical development, data analysis, and interpretation of regression models. They are written in R Markdown, with PDF output and a custom LaTeX layout. The report content is in Spanish.

The current material covers:

- exploratory data analysis and numerical and graphical summaries;
- simple linear regression and least-squares estimation;
- quadratic regression and transformations of variables;
- residual analysis and assessment of model fit;
- comparison of models using residual sums of squares and the coefficient of determination;
- interpretation and prediction in biological, biomedical, socioeconomic, traffic, and sports examples.

## Repository Components

### Statistical report

The repository currently contains **Activity A1: Introduction to the linear model** (*Actividad A1. Introducción al modelo lineal*).

- [reports/activity-a1.Rmd](reports/activity-a1.Rmd): source document containing the exercises, R code, figures, and interpretations.
- [reports/activity-a1.pdf](reports/activity-a1.pdf): rendered report.

The report includes the compulsory introductory exercises and selected exercises from Faraway and Carmona. It examines heart rate and metabolic rate in griffon vultures, age and systolic blood pressure, the `teengamb` and `uswages` datasets, traffic density and speed, and running times by distance.

### Report support files

- [reports/preamble.tex](reports/preamble.tex): LaTeX customizations for the cover, headers, colors, and figure captions.
- [assets/images/](assets/images/): institutional logos and supporting image assets.

## Project Structure

```text
.
├── assets/
│   └── images/
│       ├── pec2_ex2_table2.png
│       ├── ub_logo.png
│       └── uoc_logo.png
├── reports/
│   ├── activity-a1.Rmd
│   ├── activity-a1.pdf
│   └── preamble.tex
├── .gitignore
├── LICENSE
└── README.md
```

## Analytical Scope

Activity A1 develops the foundations of regression through:

- scatter plots, histograms, and descriptive summaries;
- fitting and interpreting regression lines with `lm()` and `lsfit()`;
- adding quadratic terms to represent curved relationships;
- examining residuals against fitted values and explanatory variables;
- calculating and comparing residual sums of squares;
- applying logarithmic transformations and assessing fit with R²;
- deriving predictions and interpreting fitted relationships in context.

## Requirements

- R.
- The `rmarkdown` and `knitr` packages for report generation.
- The `faraway` package for the `teengamb` and `uswages` datasets.
- Pandoc, available with RStudio or through a separate installation.
- A LaTeX distribution with `pdflatex` and the packages used by [preamble.tex](reports/preamble.tex) for PDF output.

## Setup

Clone the repository and open it in your preferred R environment:

```bash
git clone git@github.com:Marta-Barea/regression-models-and-methods-lab.git
cd regression-models-and-methods-lab
```

Install the required R packages:

```r
install.packages(c("rmarkdown", "knitr", "faraway"))
```

If you need a LaTeX distribution for PDF generation, you can install TinyTeX:

```r
install.packages("tinytex")
tinytex::install_tinytex()
```

## Reproducible Workflow

From the repository root, render Activity A1:

```bash
Rscript -e "rmarkdown::render('reports/activity-a1.Rmd', output_format = 'pdf_document')"
```

The generated PDF is written to `reports/activity-a1.pdf`. Keep the repository structure intact: the report uses `reports/preamble.tex`, which references the institutional logos in `assets/images/` through relative paths.

The source also declares Word and HTML output formats. The custom cover and LaTeX formatting are designed for the PDF output.

## Academic Context

This coursework was developed for **Regresión, Modelos y Métodos** within the Interuniversity Master's Degree in Bioinformatics and Biostatistics offered by the Universitat Oberta de Catalunya and the Universitat de Barcelona.

## Access

- Activity A1 report: [PDF](reports/activity-a1.pdf).
- Activity A1 source: [R Markdown](reports/activity-a1.Rmd).

## Author

Marta Barea Sepúlveda\
Interuniversity Master's Degree in Bioinformatics and Biostatistics\
Universitat Oberta de Catalunya - Universitat de Barcelona

## License

This project is distributed under the GNU General Public License v3.0. See [LICENSE](LICENSE) for the full license text.
