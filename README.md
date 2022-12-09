# Ames Housing Project
---
## Problem Statment
A real estate investment company is drafting a plan for building homes that have a high return on investment. They plan to use a model to guide their purchasing and construction of properties in Ames, Iowa. The goal of this project is to provide a model that gives insights to where new investors should look to purchase high value homes. Additionally, information is needed to know which home features should be prioritized and how.

## Deliverables
1. Creating and iteratively refining a regression model
1. Using [Kaggle](https://www.kaggle.com/) to practice the modeling process
1. Providing business insights through reporting and presentation.

## Workflow
--
Despite the dataset contianed linear relationships, it was tackled in a non-linear fashion. I found myself moving back and forth between notebookd for cleaning and modeling.

### EDA
After reading the data dictionary, it was assumed that many of the features would have a linear relationship to the target variable, sale price. Visualizations, such as scatter and bar plots, were generated and coefficients were evaluated to confirm these assumptions.

Missing values were handled by types: ordinal, nominal, discrete, and continuous. 
- Ordinal features were represented as numbers according to the meaning and order of the original input
- Nominal features had dummy variables created for them during the cleaning process.
- Discrete features were filled with the most frequent value
    - Year columns were represented as number of years since 2010 (the last year data was collected)
- Continuous features were imputed with mean values.

### Pre-processing
- A train/test split was executed prior to the modeling process. 
- Column Transformers included polynomial feature creation and standard scaling.


### Modeling
- A baseline score was established using the a Linear Regression model. Then, six models were produced using variations of Linear Regression, Ridge, Lasso, and Elastic Net.
- GridSearchCV was used for tuning hyperparameters.
- The coefficients, root mean squared error, and $R^2$ score for the second Linear Regression performed the best overall. 
- A production model was used for interpretations and the presentation.


### Business Recommendations
See slides for conclusions and reconmmendations.
