# German Credit Data Analysis

## Overview
This project involves the analysis of the German Credit Data dataset, aiming to identify patterns and insights related to credit risk. The challenge is to apply machine learning techniques, specifically AdaBoost, to improve predictions and perform both classification and regression tasks.

## Project Structure

The project is organized into the following directories:

- `notebook`: This directory contains Jupyter notebooks with the complete analysis, including data preprocessing, model training, and evaluation.
- `repository`: The directory where the `german_credit_data.csv` file is stored.

## Data Dictionary

| Variable           | Description                                      | Type        |
|--------------------|--------------------------------------------------|-------------|
| Age                | Age of the individual in years                   | Numerical   |
| Sex                | Gender of the individual                         | Categorical |
| Job                | Job category                                     | Categorical |
| Housing            | Housing status                                   | Categorical |
| Saving accounts    | Savings account balance                          | Categorical |
| Checking account   | Checking account balance                         | Categorical |
| Credit amount      | Credit amount in Deutsche Mark                   | Numerical   |
| Duration           | Duration of the credit in months                 | Numerical   |
| Purpose            | Purpose for the credit                           | Categorical |
| Risk               | Risk associated with the credit ('good' or 'bad')| Categorical |

## Challenge

### Classification with AdaBoost
- Perform a grid search to optimize the AdaBoostClassifier.
- Evaluate the model's performance and interpret the results.

### Regression with AdaBoost
- Apply AdaBoostRegressor to predict the 'Credit amount' based on other features.
- Determine the model's efficacy using regression metrics.

## Results

### AdaBoostClassifier Grid Search
- Best Parameters: `Learning Rate: 0.1`, `Number of Estimators: 200`
- Test Set Accuracy: `71%`

#### Training Set Evaluation Metrics

| Metric      | Score |
|-------------|-------|
| Precision 0 | 0.73  |
| Precision 1 | 0.75  |
| Recall 0    | 0.27  |
| Recall 1    | 0.96  |
| F1-Score 0  | 0.39  |
| F1-Score 1  | 0.84  |
| Accuracy    | 0.75  |

#### Testing Set Evaluation Metrics

| Metric      | Score |
|-------------|-------|
| Precision 0 | 0.53  |
| Precision 1 | 0.73  |
| Recall 0    | 0.15  |
| Recall 1    | 0.94  |
| F1-Score 0  | 0.24  |
| F1-Score 1  | 0.82  |
| Accuracy    | 0.71  |


#### Regression Challenge
The AdaBoost regressor was used to predict the `Credit amount` with a grid search to optimize its hyperparameters.

- Fitting 5 folds for each of 27 candidates, totalling 135 fits
- Best Parameters: 
  - Learning Rate: `0.1`
  - Loss: `exponential`
  - Number of Estimators: `50`
- Regression Metrics on Test Set:
  - Mean Squared Error (MSE): `3978140.86`
  - Mean Absolute Error (MAE): `1466.01`
  - R-squared: `0.346`


## Open Collaborations

Contributions to the project are welcome! If you have suggestions for improving the models, or if you have performed additional analyses that could provide further insights, please feel free to open an issue or submit a pull request.


## Getting Started

To get started with this project, clone the repository and navigate to the respective directories to access the Jupyter notebooks and the dataset:

```bash
git clone https://github.com/julioclerio/adaboost
# Run the Jupyter notebooks
cd adaboost/notebooks

# Access the dataset for your analyses
repository/german_credit_data.csv





