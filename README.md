# Data Science Telecom churn prediction: Project Overview
---
* Recommend strategies to manage customer churn
* Handling **Multi-collinearity** in logistic regression
* Optimized PCA and Logistic Regression, Random Forest Regressors using **GridsearchCV** to reach the best model

## Code and Resources Used
---
**Python Version:**3.7
**Packages:** Pandas, numpy, sklearn, matplotlib, seaborn

## Data Cleaning
---
After importing data and reading it found that there are many missing values in the data
* Replacing **NaN** values in categorical variables with -1 where it become a new category
* Dropped variables with more than a given threshold of missing values
* Imputing missing values using **MICE**

## EDA
---
* Up on univariate analysis find that most of the data is skewed to wards left
<br>![univariate telecom churn git hub](https://user-images.githubusercontent.com/69252134/130794057-08b31d3c-63a4-4b42-8f20-7d4ca2ca9298.png)
* Bivariate EDA
<br>![bivariate telecom churn git hub](https://user-images.githubusercontent.com/69252134/130794309-84cad2d4-ddd6-4bf5-a8f2-04a4ef6c38f3.png)
* Capped outliers in all numeric variables with K-sigma technique

## Model Building
---
First I divided the data into `traintestsplit` and then aggregated the categorical columns

I have used PCA to look at the variance explained by components about **60 componenets explain 90% variance** and **80 components explain 95% variance**

I tried two models:

* **PCA and Logistic Regression** - Because of sparse data from many categorical variables, I thought a normalized regression would be effective.
* OPtimised hyerparameters and resulted the hyperparameter using **Gridsearchcv** and built model on the tuned hyperparameters
* **Random Forest** - Again with the sparsity associated with the data, I thought that this would be a good fit

## Model Performance
---
### PCA and Logistic Regression: 
* **Sensitivity:** 0.82
* **Specifisity:** 0.85
* **AUC:** 0.91

### Random Forest:
* **Sensitivity:** 0.46
* **Specifisity:** 0.98
* **AUC:** 0.89

with poor sensitivity on Random Forest we choose `PCA with Logistic Regression`

