# Data Science Telecom churn prediction: Project Overview
---
* Optimized Lasso, Ridge and Random Forest Regressors using **GridsearchCV** to reach the best model

## Code and Resources Used
---
**Python Version:**3.7
**Packages:** Pandas, numpy, sklearn, matplotlib, seaborn

## Data Cleaning
---
After importing data and reading it found that there are many missing values in the data
* Replacing NaN values in categorical variables with -1 where it become a new category
* Dropped variables with more than a given threshold of missing values
* Imputing missing values using MICE

## EDA
---
Up on univariate analysis find that most of the data is skewed to wards left
