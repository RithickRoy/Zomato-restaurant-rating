# Zomato Restaurant Rating Prediction

## Project Overview

This project aims to predict restaurant ratings using the Zomato dataset, based on various factors like location, cuisine, cost, online ordering availability, and more. Predicting ratings helps users discover restaurants likely to meet their expectations and aids businesses in understanding key drivers of customer satisfaction.

The model uses **Random Forest Regression** to capture complex relationships between restaurant features and their ratings.

## Dataset

- Source: Zomato Restaurants Dataset (from Kaggle)
- Key features include:
  - Location (city/locality)
  - Cuisine types
  - Approximate cost for two
  - Online ordering and table booking options
  - Number of votes
  - Restaurant type, city, and listing categories
- Target variable: Restaurant rating (`rate`)

## Project Workflow

1. **Data Loading & Cleaning**  
   - Handled missing values (dropped or imputed as appropriate)  
   - Converted ratings to numeric values  
   - Cleaned cost column by removing commas and converting to floats  
   - Dropped columns not useful for modeling (e.g., URLs, reviews text)

2. **Exploratory Data Analysis (EDA)**  
   - Visualized rating distribution, top locations, and relationships between cost and ratings

3. **Feature Engineering**  
   - Encoded categorical variables (e.g., online order, book table, location) using one-hot encoding or label encoding

4. **Model Training & Evaluation**  
   - Split data into training and test sets (80/20)  
   - Trained Random Forest regressor to predict ratings  
   - Evaluated model using RMSE, MAE, and R² metrics

## Results

- **RMSE:** 0.12 (average prediction error in rating points)  
- **MAE:** 0.05 (mean absolute error)  
- **R² Score:** 0.93 (model explains 93% of variance in ratings)

The model performs very well, showing strong predictive power based on available features.
