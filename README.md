# PPOL 6803 - Intro into Data Science Final Project (Fall 2024 )

Contributors: 
- [D'Angelo Francis](https://github.com/DangeloCFrancis)
- [Nathan Su](https://github.com/topnathan) 
- [Su Yeon Seo](https://github.com/ssy0709)

## Overview

The United States 2024 Presidential elections have renewed [debates](https://www.nbcnews.com/politics/2024-election/state-poll-results-show-ties-are-tied-voters-pollsters-rcna177703) about the 
precision of polls in predicting electoral outcomes. The conversation surrounding
the purpose of polls in gauging a presidential candidate's hopes of sitting behind
the Resolute Desk spawned one question: *How 'predictable' is the American voter?*

## Methodology 

To assess the 'predictability' of voters, we trained a Classification and Regression
Tree (CART) model and Principal Component Analysis (PCA) to provide a probability that a survey respondent voted 'conservatively' or 'liberally'[^1]. 
Our primary data for analysis and modeling will be survey data from the 
[American National Election Studies](https://electionstudies.org/), a collaboration 
between Duke University,the University of Michigan,the University of Texas at Austin (UT Austin), 
Stanford University,and the National Science Foundation (NSF). We focused on responses between
2000 and 2020. The list of the survey variables used in the model can be found [here](https://dangelocfrancis.github.io/ppol6803_final_project/).
The codebook provided by ANES for the time series study can be found [here](https://electionstudies.org/wp-content/uploads/2022/09/anes_timeseries_cdf_codebook_var_20220916.pdf#page=4.76).

The model uses questions that the ANES asks about a candidate 
that voter voted for (*e.g., "Which candidate did you vote for in...?"*) as the 
actual outcome($\hat{Y}$). The goal of our model is to have it precisely predict
voter preference by learning about the associated demographic characteristics (race and ethnicity,
religion, socioeconomic status, etc.) and using survey responses asking about relevant policies 
(transgender rights, gun control, reproductive rights, etc.).

We will incorporate variable importance analysis (VIM analysis) to deduce 
which survey topics and demographic characteristics are the best indicators of 
candidate preference.

[^1]: For simplicity, our model will reflect a binary-choice election.
