# Football-Clubs-Ranking-Prediction

## Overview
This project demonstrates a machine learning model to predict a football club’s end-of-season league performance tier using historical performance, financial indicators, and squad characteristics.

## Problem Statement
Football clubs differ widely in terms of:
- Historical league performance
- Transfer spending
- Squad market value
- Squad age profile

This project aims to classify clubs into league finish tiers:
- Top Four
- Europe
- Mid-Table
- Relegation

## Dataset
The dataset used in this project is synthetic but realistic, designed to resemble football season data.

### Key Features
- `prev_position_1` – League position in the previous season  
- `prev_position_2` – League position two seasons ago  
- `prev_position_3` – League position three seasons ago  
- `transfer_spend_million` – Transfer spending (in millions)  
- `squad_value_million` – Squad market value (in millions)  
- `age_mean` – Average squad age  
- `Club` – Club name  
- `Season_Rank` – Table finish in the latets season (Target Variable)

## Data Cleaning & Preprocessing
The following steps were applied:

- Removal of duplicate rows
- Median imputation for missing numerical values
- Log transformation of skewed financial variables; transfer fees spent and squad value
- Conversion of the target variable into numerical form using label encoding
- One-hot encoding of the `Club` column for machine learning compatibility

## Exploratory Data Analysis (EDA)
Exploratory analysis was performed to understand:
- Distribution of financial variables
- Distribution of squad age
- Relationship between squad value and historical league position
- Transfer spending patterns across clubs with varying ranks

Visualizations included:
- Histograms
- Scatter plots
- Box plots

## Feature Engineering
Final features used for modelling include:
- Historical league positions
- Log-transformed transfer spend
- Log-transformed squad value
- Average squad age
- Club identity 

Raw financial columns were dropped after log transformation to avoid redundancy.
Log-transformed columns were used to avoid poor model fitting by wide range of values in the respective financial variables.

## Machine Learning Models
Two classification models were implemented:

### Logistic Regression
- Serves as a simple and interpretable baseline
- Helps establish a reference performance level

### Random Forest 
- Captures non-linear relationships
- More robust to feature interactions
- Provides feature importance estimates

## Model Evaluation
Models were evaluated using:
- Precision
- Recall
- F1-score
- Overall accuracy

The Random Forest model showed improved performance over Logistic Regression, indicating the presence of non-linear relationships in the data.

## Feature Importance
Feature importance from the Random Forest model highlights:
- Strong influence of historical league performance
- Significant contribution from financial indicators 

This aligns well with real-world football dynamics.

## Conclusion
This project demonstrates a complete machine learning pipeline, including:
- Data cleaning
- Feature engineering
- Exploratory analysis
- Model training
- Model evaluation
- Interpretation of results

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Author
**Shitikshu Vyas**  
