# House Price Prediction

## Objective

The objective of this project is to build a Machine Learning model using Linear Regression to predict house prices based on different house features.

## Dataset

The dataset contains information about houses along with their sale prices.

The dataset used in this project contains 2919 rows and 13 columns.

For the first model, the 1460 rows containing `SalePrice` were used because the remaining rows do not have target values.

## Features Used

The numerical features used as input variables are:

- MSSubClass
- LotArea
- OverallCond
- YearBuilt
- YearRemodAdd
- BsmtFinSF2
- TotalBsmtSF

Categorical features used in the improved model:

- MSZoning
- LotConfig
- BldgType
- Exterior1st

The `Id` column was removed because it is only an identifier.

## Approach

The project was completed in the following steps:

1. Loaded the dataset using Pandas.
2. Inspected the dataset structure and data types.
3. Checked for missing values.
4. Selected `SalePrice` as the target variable.
5. Removed the `Id` column.
6. Created a baseline Linear Regression model using numerical features.
7. Split the data into training and testing sets using an 80:20 ratio.
8. Trained the Linear Regression model.
9. Generated predictions on the test data.
10. Evaluated the model using MAE, MSE, RMSE and R².
11. Added categorical features using one-hot encoding.
12. Trained an improved Linear Regression model.
13. Compared the baseline and improved models.

## Models

### Model 1 - Baseline

The baseline model used only numerical features.

**R² Score:** 0.5751

### Model 2 - Improved

The second model included categorical features using one-hot encoding.

**R² Score:** 0.6195

The improved model performed better than the baseline model.

## Model Evaluation

| Metric | Baseline Model | Improved Model |
|--------|----------------|----------------|
| R² | 0.5751 | 0.6195 |
| MAE | 37871.43 | 34122.85 |
| MSE | 3259194958.46 | 2918458029.59 |
| RMSE | 57089.36 | 54022.75 |

## Conclusion

A Linear Regression model was successfully developed to predict house prices.

The improved model achieved an R² score of 0.6195 compared to 0.5751 for the baseline model. It also achieved lower MAE, MSE and RMSE values.

Therefore, including categorical features using one-hot encoding improved the performance of the Linear Regression model.

## Tools & Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- JupyterLab

## Project Structure

```text
House-Price-Prediction/
│
├── data/
│   └── HousePricePrediction (1).csv
│
└── notebooks/
    └── house_price_prediction.ipynb
