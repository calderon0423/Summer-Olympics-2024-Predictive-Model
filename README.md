# [PROJECT 2 - GROUP 1]

## EXECUTIVE SUMMARY: Overview and Objectives

The Summer Olympic Games represent the pinnacle of international sports competition, where athletes from around the world compete for glory and national pride. Our goal with this project is to develop predictive models that can estimate the 2024 medal counts for the top five medal-winning countries, namely the United States of America (USA), Soviet Union (URS), Great Britain (GBR), France (FRA), and Germany (GER), based on past data (1896-2012). By leveraging machine learning algorithms, specifically **Linear Regression**, **Random Forest Regressor**, **XGBoost Regressor**, and **SVR**. , we aim to achieve precise predictions.



## OVERVIEW OF THE DATA COLLECTION, CLEAN UP AND EXPLORATION PROCESS 

* The dataset used for this project is sourced from [Kaggle](https://www.kaggle.com/datasets/the-guardian/olympic-games?select=summer.csv)

### Preprocessing Steps

#### Data Cleaning
- Handling missing values by imputing relevant statistics (e.g., mean or median) for numerical columns.
- Dropping non-relevant columns such as 'Athlete', 'Sport', and 'Discipline'.

#### Data Encoding
- Encoding categorical variables using One Hot Encoding for features like event type and athlete nationality.

#### Data Splitting
- Splitting the dataset into training and testing sets using the `train_test_split` function.

#### Exploratory Data Analysis
- Aggregated medal counts by country, year, and type.
- Identified and removed outliers due to historical events, such as the 1904 and 1984 Olympics.

#### Data Visualization
- Plotted USA medal counts over the years.
- Computed and visualized the correlation between year and medal counts.


## Model Training and Evaluation

#### Pipeline for Model Training
A custom pipeline was created to preprocess data, split the dataset, and train various models. The models used include Linear Regression, Random Forest Regressor, XGBoost Regressor, and SVR. The pipeline includes the following steps:

#### Data Preprocessing:
- Drop non-relevant columns.
- Split the dataset into features (X) and target (y).
Model Training:

#### Create pipelines for each model.
- Fit each model on the training data.
- Evaluate each model using Mean Squared Error (MSE), R-squared (R²), and Adjusted R-squared.

#### Model Evaluation:
- Calculate and compare the performance metrics for each model.
- Select the best-performing model based on adjusted R-squared values.


## Observations and Results

### Linear Regression
- Provided a solid baseline with reasonable R-squared values.

### Random Forest Regressor
- Showed improved performance with a lower Mean Squared Error.

### XGBoost Regressor
- Achieved the highest accuracy among the evaluated models with the best R-squared value.

### SVR Regressor
- Also performed well, with comparable results to the other models.

Each model was evaluated using metrics such as Mean Squared Error (MSE), R-squared (R²), and Adjusted R-squared.


## Observations and Results

### Linear Regression
- Provided a solid baseline with reasonable R-squared values.

### Random Forest Regressor
- Showed improved performance with a lower Mean Squared Error.

### XGBoost Regressor
- Achieved the highest accuracy among the evaluated models with the best R-squared value.


## Results and Conclusions
- **Linear Regression** provided a solid baseline with an adjusted R-squared value of 0.32.
- **Random Forest Regression** improved the prediction accuracy with an adjusted R-squared value of 0.41.
- **XGBoost Regression** achieved the highest accuracy with an adjusted R-squared value of 0.80, making it the best model for predicting the 2024 Olympic medal counts.
- **SVR Regressor** was included for comparison but did not outperform XGBoost.