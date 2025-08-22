# Car Price Prediction

This project analyzes a dataset of cars to explore factors that influence selling prices and build a predictive model. The workflow includes:

1. Data Cleaning

2. Models Perfomances
   
3.  Best Performing Model

# Dataset

Includes features such as enginesize, curbweight, horsepower, mileage, fueltype, car_age, etc.

Target variable: Selling Price

# Data Cleaning

Filled missing values in mileage with column mean.

Removed extreme outliers in selling price (< 10,000 or > 5,000,000).

Converted numerical columns stored as strings to numeric.

Created a new feature: price per kilometer

# Models Performances
Linear Regression is still decent, but Lasso balances accuracy + feature selection.

Lasso Regression performed the best in the dataset (highest R², lowest RMSE).

Ridge underperformed slightly possibly because the dataset has features where some should be shrunk (Lasso) rather than just reduced (Ridge).

# Best Performing Model

 # Polynomial Regression (degree=2) is the best.

It explains ~86.6% of the variance vs ~68% for the linear models.

It reduced error by ~35% (195k vs 302k RMSE).

This means car prices depend on nonlinear relationships and feature interactions (e.g., age × mileage, engine², etc.), which Polynomial Regression can capture while simple linear models cannot.
