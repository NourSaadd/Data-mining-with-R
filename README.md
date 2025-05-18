# Forecasting Forest Fires: The Role of Fire Weather Indices
# Forest Fires Prediction using R

This project focuses on predicting forest fire occurrences based on environmental and meteorological data. By leveraging multiple classification algorithms, we aim to evaluate the predictive strength of fire weather indices in two Canadian regions: Cordillera and Hudson Bay.

## Overview

Forest fires are a significant threat to ecosystems and human life. Accurate prediction of fire occurrence based on fire weather indices and climate conditions can support early warning systems. This project involves data preprocessing, exploratory analysis, and comparative modeling using various supervised learning techniques.

## Dataset

The dataset includes measurements from two distinct geographical areas:

- **Cordillera**
- **Hudson Bay**

Each record includes:

- **Meteorological Variables**: Temperature, Relative Humidity (RH), Wind Speed, Rainfall
- **Fire Weather Indices**: FFMC, DMC, DC, ISI, BUI, FWI
- **Target Variable**: Classes (Fire or Not Fire)

The raw dataset is provided in `data/forest_fires_dataset.csv`.

## Preprocessing

Key preprocessing steps:

- Merged two location-based datasets into one unified table
- Created new variables: `Location`, `ClassesN` (numeric version of Classes), and `day_group`
- Converted categorical variables to factors
- Winsorized outliers to reduce skewness (applied 5th–95th percentile capping)
- Removed low-variance columns such as `year`

## Exploratory Data Analysis (EDA)

The dataset was explored through:

- Distribution plots (histograms, boxplots)
- Class imbalance analysis
- Correlation analysis between features
- Location-specific trends in feature values

## Modeling

The following classification models were trained and evaluated:

- Logistic Regression
- Linear Discriminant Analysis (LDA)
- Quadratic Discriminant Analysis (QDA)
- k-Nearest Neighbors (KNN)
- Decision Trees (`rpart`)
- Random Forests (`randomForest`)
- Gradient Boosting Machines (`gbm`)
- Support Vector Machines (`e1071`)

All models were trained on normalized datasets, using a 70-30 train-test split. Model performance was assessed using accuracy and confusion matrices.

## Tools and Packages

All analyses were performed in R. The main packages used include:

- `dplyr`, `tidyr`, `ggplot2`
- `caret` for preprocessing and model training
- `rpart`, `randomForest`, `gbm`, `class`, `e1071`, `MASS`, `pROC`

## Report

The complete project report, including methodology, visualizations, and model evaluation, is provided in `docs/report.html`.

## Team

This project was completed as part of an academic data mining course by:

- Nour Saad
- Joudy Allam
- Haya Mazyad
