# Introduction to R

Course materials for the R lab sessions of the Quantitative Methods I class in the research master's programme in political science at Sciences Po Paris (Fall 2024). The sessions complement Jan Rovny's lectures and take students from their first lines of R code to multiple regression.

The course is a Quarto book, available online at **[malojan.github.io/2024_intro_r](https://malojan.github.io/2024_intro_r/)**. Each session has its own folder with the chapter, its data and the exercise.

## Sessions

| Session | Topic | Chapter | Data | Exercise |
|---|---|---|---|---|
| 1 | Getting started with R and RStudio: projects, Quarto, objects, vectors, functions, reading errors | `session01/workflow.qmd`, `basics.qmd`, `help.qmd`, `slides.qmd` | French candidates (`session01/data/`) | `01_exercice` |
| 2 | Manipulating and describing data: `dplyr` verbs, grouped summaries, reshaping with `tidyr` | `session02/0201_manipulate.qmd`, `0202_reshape.qmd`, `further.qmd` | QoG environmental indicators, German and Spanish polls, UK general election results (`session02/data/`) | `02_exercice` |
| 3 | Visualizing data with `ggplot2`: histograms, boxplots, scatter plots, good and bad charts | `session03/03_dataviz.qmd`, `03_slides.qmd` | Chapel Hill Expert Survey 1999–2019 (`session03/`) | `exo_3` |
| 4 | Testing relationships: joining datasets, recoding, missing values, χ² test, t-test | `session04/04_relationships.qmd` | French Election Study 2022 and ELIPSS annual survey (not included, see below) | |
| 5 | Correlation and simple linear regression: OLS, interpreting coefficients, `broom`, regression tables | `session05/correlation_regression.qmd` | US presidential elections 1948–2012 (`session05/data/`); European Social Survey round 9 (not included) | `05_exercice` |
| 6 | Multivariate analysis: multiple regression, interactions, predicted values, models by country with `purrr`, diagnostics | `session06/06_modelling.qmd` | European Social Survey round 8 (not included) | |
| Final | Graded group homework | `final_homework/homework.qmd` | Toshkov et al. table (`final_homework/data/`); European Social Survey round 9 (not included) | |

Exercise solutions are not included in this repository.

## Data not included

Some datasets cannot be redistributed under their providers' terms of use. To run sessions 4 to 6 and the final homework, download them yourself (free, registration required) and save them under the names below:

| Dataset | Where to get it | Save as |
|---|---|---|
| French Election Study 2022 (FES 2022) | [data.sciencespo.fr](https://data.sciencespo.fr/) (CDSP) | `session04/fes2022v4bis.dta` |
| ELIPSS annual survey | [data.sciencespo.fr](https://data.sciencespo.fr/) (CDSP) | `session04/elipss_annual.dta` |
| European Social Survey, round 8 | [ess.sikt.no](https://ess.sikt.no/) | `session06/data/ess8.dta` |
| European Social Survey, round 9 (edition 3.1) | [ess.sikt.no](https://ess.sikt.no/) | `session05/data/ESS9e03_1.dta`, `final_homework/data/ESS9e03_1.dta` |

## Rendering the book

Install [R](https://cloud.r-project.org/), [RStudio](https://posit.co/download/rstudio-desktop/) and [Quarto](https://quarto.org/), then the packages used in the course:

```r
install.packages(c("tidyverse", "haven", "labelled", "janitor", "broom", "infer",
                   "stargazer", "ggrepel", "ggeffects", "performance", "rvest", "here"))
```

With the data above in place, render the website from the project folder with `quarto render --to html`.
