# Predicting Graduate Admissions with Linear Regression

- [Project Overview](#overview)
- [Dataset](#dataset)
- [Key Features](#key-features)
- [Model Performance](#model-performance)
- [Technologies Used](#technologies-used)

## Overview
This project explores the chances of a student’s admission into graduate programs. Using linear regression, we aim to predict admission probabilities based on factors like GRE score, TOEFL score, CGPA, research experience, etc.

## Dataset
The data for this analysis is available on Kaggle. You can access it at the following link: [Data for Admission in the University](https://www.kaggle.com/datasets/akshaydattatraykhare/data-for-admission-in-the-university).

The dataset contains 400 records with the following columns:
- GRE Score (out of 340)
- TOEFL Score (out of 120)
- University Rating (out of 5)
- SOP Rating (out of 5)
- LOR Rating (out of 5)
- CGPA (out of 10)
- Research (0 = No, 1 = Yes)
- Chance of Admit (ranging from 0 to 1) (Target Variable)

## Key Features
- Predict graduate admission chances based on student profiles.
- Perform exploratory data analysis (EDA).
- Compare training and testing performance using 10-fold cross-validation.
- Calculate model performance metrics like RMSE and R².

## Model Performance

**Cross-Validation Results:**  
The Linear Regression model was trained on 322 samples with 7 predictors and evaluated using 10-fold cross-validation. The model demonstrated strong performance with a Root Mean Squared Error (RMSE) of 0.0626, indicating low prediction error. The R-squared value of 0.813 suggests that the model explains 81.3% of the variance in the admission probability, indicating good predictive power. 

**Performance on the Test Set:**  
When evaluated on the test set, the model achieved an RMSE of 0.0662, indicating that the model makes small errors in its predictions of unseen data. The R-squared value on the test set was 0.803, meaning the model explains 80.3% of the variance in the test data. A multicollinearity check using the Variance Inflation Factor (VIF) revealed moderate correlations among some predictors, such as GRE Score and CGPA, with VIF values above 4. Despite these moderate correlations, the model maintained strong performance and demonstrated its ability to generalize well to new data.

## Technologies Used
- **RStudio**: An integrated development environment (IDE) for R, providing tools for writing, debugging, and running R code.
- **tidyverse**: A collection of R packages for data manipulation, visualization, and analysis, including tools like ggplot2, dplyr, and tidyr.
- **caret**: A comprehensive package for building, training, and evaluating machine learning models in R.
- **GGally**: An extension of ggplot2 for creating complex visualizations like pair plots and correlation matrices.
- **car**: A package for regression diagnostics and analysis, providing tools for model evaluation and multicollinearity checks.
