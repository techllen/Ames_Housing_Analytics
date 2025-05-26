# Ames Housing Analytics

## Introduction

This repository contains code to perform data analysis on the Ames, Iowa, USA housing dataset, which can be found here: [Ames Housing Dataset](https://www.kaggle.com/datasets/shashanknecrothapa/ames-housing-dataset).

The dataset includes various features and attributes of residential homes in Ames, Iowa, USA. Feature documentation is available here: [AmesHousing.pdf](https://cran.r-project.org/web/packages/AmesHousing/AmesHousing.pdf)

## Problem Statement

* Develop a machine learning model to predict the sale price of residential properties in Ames, Iowa. The model leverages key housing characteristics such as living area, basement size, garage size, overall quality, the number of fireplaces and bathrooms, and age to accurately estimate the sale price.
* Determine different attributes of the house that influence its price using Linear Regression.
* Determine different attributes of the house that influence its price group (High Price or Low Price) using Logistic Regression.

## Setup

This project uses two Google Colab Notebooks:

1.  `ames_housing_LINEAR_REGRESSION.ipynb`: Contains analysis done using a linear regression model.
2.  `ames_housing_LOGISTIC_REGRESSION.ipynb`: Contains analysis done using a logistic regression model.

To set up the project:

1.  Download the dataset from the provided link above.
2.  Load the dataset using your preferred method.
3.  Run either notebook.

## Linear Regression Notebook (`ames_housing_LINEAR_REGRESSION.ipynb`)

This notebook performs Exploratory Data Analysis (EDA), data cleaning, feature engineering, and implements a linear regression model to predict house prices.

### Key Steps:

1.  **EDA:** Explores the dataset to understand its structure and features.
2.  **Data Cleaning and Preprocessing:**
    * Handles missing values by removing columns with >70% missing data and imputing the rest.
    * Converts categorical features to the correct data type.
    * Removes duplicate entries.
    * Detects and handles outliers in the `SalePrice` column using capping.
3.  **Feature Engineering:**
    * Creates a new feature `Age_of_the_house`.
4.  **Model Implementation:**
    * Selects relevant features for linear regression.
    * Scales the features using `StandardScaler`.
    * Splits the data into training and testing sets (80/20 split).
    * Trains a `LinearRegression` model.
    * Evaluates the model using Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R2).
    * Visualizes the model's predictions and residuals.

### Key Features Used:

* `Total Bsmt SF`
* `Fireplaces`
* `Garage Area`
* `TotRms AbvGrd`
* `Gr Liv Area`
* `1st Flr SF`
* `Age_of_the_house`
* `Year Remod/Add`
* `Overall Qual`
* `Mas Vnr Area`
* `Year Built`
* `Full Bath`

## Logistic Regression Notebook (`ames_housing_LOGISTIC_REGRESSION.ipynb`)

This notebook performs EDA, data cleaning, feature engineering, and implements a logistic regression model to classify houses into high-price or low-price groups.

### Key Steps:

1.  **EDA:** Explores the dataset.
2.  **Data Cleaning and Preprocessing:** (Same as Linear Regression Notebook)
    * Handles missing values.
    * Converts data types.
    * Removes duplicates.
    * Handles outliers.
3.  **Feature Engineering:**
    * Creates `Age_of_the_house`.
    * Creates a binary target variable `Is_Price_High` based on the median `SalePrice`.
4.  **Model Implementation:**
    * Selects features based on correlation with `Is_Price_High`.
    * Scales features using `StandardScaler`.
    * Splits data into training and testing sets.
    * Trains a `LogisticRegression` model.
    * Evaluates the model using accuracy, confusion matrix, and classification report.

### Key Features Used:

* `SalePrice`
* `Overall Qual`
* `Full Bath`
* `Year Built`
* `Garage Cars`
* `Gr Liv Area`
* `Year Remod/Add`
* `Garage Yr Blt`
* `Garage Area`

## Observations

* (Refer to the notebooks for specific observations and insights from the EDA and model evaluation.)

## Conclusion

This project demonstrates the application of linear and logistic regression models to predict house prices and classify houses into price groups using the Ames Housing dataset. The notebooks provide a detailed walkthrough of the data analysis, preprocessing, and model building process.
