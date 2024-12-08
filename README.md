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

To assess the 'predictability' of voters, we trained multiple models with training data split from 
the [American National Election Studies](https://electionstudies.org/) 1948-2020 cumulative time series data. 
We relied on survey data in the time frame 2000-2020 (**JUSTIFY**) and utilized the given ANES sampling weights. 
We cleaned variables for possible MCAR NAs (**JUSTIFY**) and relied on `step_impute_bagged()` in recipes to impute 
for other types of 'missingness'. After splitting the data (~10,000 observations) into training (.75) and testing data (.25),
We trained four models on the training data and validated on the testing data: 

- A decision tree;
- A random forest model with re-sampling;
- A bagged forest model with hyperparameter tuning and resampling; and 
- A LASSO multinominal classification model 

The model uses questions that the ANES asks about a candidate that voter voted for (*e.g., "Which candidate did you vote for in...?"*) as the 
actual outcome($\hat{Y}$). The goal of our model is to have it precisely predict
voter preference by learning about the associated demographic characteristics (race and ethnicity,
religion, socioeconomic status, etc.) and using ~80 survey responses asking about politics. 
(opinion on transgender rights, gun control, reproductive rights, etc.). 

- [Complete list of the survey variables used](https://dangelocfrancis.github.io/ppol6803_final_project/)
- [ANES 1948 - 2020 Cumulative Time Series Data Codebook](https://electionstudies.org/wp-content/uploads/2022/09/anes_timeseries_cdf_codebook_var_20220916.pdf#page=4.76)


We will incorporate variable importance analysis (VIM analysis) to deduce which
survey topics and demographic characteristics are the best indicators of 
candidate preference.

[^1]: A collaboration between Duke University,the University of Michigan,the University of Texas at Austin (UT Austin), 
Stanford University,and the National Science Foundation (NSF).

[^2]: For simplicity, our model will reflect a trinary-choice election: liberal/left-leaning, conservative/right-leaning, or moderate.

