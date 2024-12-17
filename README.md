# PPOL 6803 - Intro into Data Science Final Project (Fall 2024 )

Contributors: 
- [D'Angelo Francis](https://github.com/DangeloCFrancis) - Georgetown University
- [Yuxiang Su](https://github.com/topnathan) - Georgetown University
- [Su Yeon Seo](https://github.com/ssy0709) - Georgetown University

## Overview

The United States 2024 Presidential elections have renewed [debates](https://www.nbcnews.com/politics/2024-election/state-poll-results-show-ties-are-tied-voters-pollsters-rcna177703) about the 
precision of polls in predicting electoral outcomes. The conversation surrounding
the purpose of polls in gauging a presidential candidate's hopes of sitting behind
the Resolute Desk spawned three questions: 

1. *How 'predictable' is the American voter?* 
2. *Is the American selectorate as predictable as the South Korean selectorate?* 
3. *Is it possible to predict an individual's political identity if democratic institutions do not exist in their country?*  

**Website**:<https://dangelocfrancis.github.io/ppol6803_final_project/>

## Project Specifics 

This project is written *entirely* in [R](https://www.r-project.org/). 
To run, download the `predicting_voter_politics.qmd` file. Then,
install *all* necessary packages indicated in the **library setup** section.

### Reproducibility

To avoid issues running the code, please make sure that you pull the `/data` 
folder in addition to the `predicting_voter_politics.qmd`file. This file will contain:

- `.RData` for the ANES and KGSS model
- `.sav` (SPSS file) for the Asian Barometer data

The code chunk **ANES data loading and variable selection** can be *skipped*[^1]
if using the .RData file for the ANES. Make sure to load the data using the following:

`load("data/anes_2000_2020.RData")`

This will load the R object directly into the environment.

If you wish to use the raw data that this project worked with, it can be found 
using the links under **Data Sources** below.

## Data Sources

- [ANES 1948 - 2020 Cumulative Time Series Data](https://electionstudies.org/data-center/anes-time-series-cumulative-data-file/)
- [Korean General Society Survey](https://www.icpsr.umich.edu/web/ICPSR/studies/38577/datadocumentation#)
- [Asian Barometer Data Release](https://www.asianbarometer.org/datar?page=d10)

[^1]: Delete the chunk or use the code option `eval: false`


