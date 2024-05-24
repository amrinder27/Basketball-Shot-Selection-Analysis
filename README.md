# Exploring the Interplay Between Shot Outcomes and Shot Selection for the Denver Nuggets in the 2022-2023 NBA Season

## Date

April 2024

## Project Summary

### Background
The Denver Nuggets' 2023 NBA championship win highlights their resilience, skill, and strategic prowess. This study examines their shot selection and outcomes to provide insights into player development, play style refinement, and strategic decision-making.

### Purpose
Shot selection is critical in basketball, influencing points scored and winning chances. This analysis uses statistical methods to assess various factors affecting shot outcomes for the Nuggets.

### Literature Review
Fichman and O’Brien (2019): Winning teams favor 3-point shots over 2-point shots.
Erculj and Strumbelj (2015): Dunk shots are common; hook shots are rare; situational variables affect shot selection.
Gomez, Gasperi, and Lupo (2016): Home court advantage varies in close games.

### Methods
#### Data Set and Features
The dataset is the "NBA play-by-play and shot details data (1996-2022)" from Kaggle, focusing on the Denver Nuggets' 2022-2023 season. Variables were selected based on relevance to the literature.

### Model
A logistic generalized linear mixed model (GLMM) was used to analyze binary outcome data, accounting for fixed and random effects. Variable selection was done through a backward stepwise approach, and model diagnostics included measures like DFBETAS and Cook’s distance.

### Results
#### Data Description
EVENT_TYPE: Distribution of shots made vs. missed is balanced.
SHOT_ZONE_BASIC: Different shot zones have varying success rates, with the restricted area showing notable patterns.
PLAYER_NAME and ACTION_TYPE: Shot success depends on these categorical variables.

### Analysis Process and Results
#### Variable Selection
Initial Model: Included all relevant variables; showed an AUC of 0.7102.
Final Model: Excluded non-significant variables (MINUTES_REMAINING, HOME_AWAY, SHOT_DISTANCE, PERIOD) to maintain a stable AUC around 0.71.
#### Diagnostics Results
Influential categories (e.g., “Jump Shot”) were considered but removing them distorted the model due to data loss.

### Discussion
#### Final Model Interpretation
Shots from the right corner 3 have higher success odds compared to other zones.
Insights can help develop offensive strategies and inform defensive positioning for opponents.
#### Limitations
Reliance on AUC for variable selection may risk overfitting.
Inclusion of influential observations might bias results due to imbalance.

### Conclusion
This study provides valuable insights into shot selection and success for the Denver Nuggets, contributing to strategic enhancements and competitive understanding in professional basketball.

## File Description

README.md: Project description

Analysis.Rmd: R code of the analysis conducted for the project

RMD Output.pdf: Output of the Analysis.Rmd file

Final Report.pdf: Final reasearch paper including resultsand implications of the analysis

## Tools and Technologies

R(programming language), Rstudio, ggplot2, lme4, influence.ME, pROC, lattice, mlmhelpr

## Author

Amrinder Sehmbi

amrindersehmbi@outlook.com
