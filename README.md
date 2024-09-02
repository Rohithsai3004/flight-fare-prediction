# Flight Fare Prediction
This repository contains a machine learning project aimed at predicting flight fares using a dataset of historical flight information. The project also includes data visualization performed using Power BI.

## Project Overview
### Data
The dataset used for this project is Data_Train.xlsx, which includes information such as:

Airline
Date of Journey
Source and Destination
Dep_Time and Arrival_Time
Duration
Total Stops
Price (target variable)

### Steps Involved
1. Data Preprocessing:

Dropped null values.
Extracted day and month from the Date_of_Journey.
Extracted hour and minute from Dep_Time and Arrival_Time.
Refined the Duration by extracting hours and minutes.
Applied one-hot encoding on categorical features like Airline, Source, and Destination.
Converted the Total_Stops feature to numerical values.
Dropped irrelevant columns such as Route and Additional_Info.

2. Exploratory Data Analysis (EDA):

Visualized the variation of flight prices with respect to Airline, Source, and Destination using Seaborn's catplot.
Used a heatmap to identify the correlation between various features.
Feature Selection:

Used ExtraTreesRegressor to determine feature importance and selected the top features influencing the fare.

3. Model Training:

Applied several machine learning models to predict flight fares:
Random Forest Regressor
AdaBoost Regressor
Support Vector Regressor (SVR)
XGBoost Regressor
Evaluated model performance using metrics like R² score and RMSE.
Performed log transformation on the target variable (Price) to normalize the distribution.

4. Model Evaluation:

Visualized the distribution of residuals using Seaborn's displot.
Performed statistical tests to assess the normality of the predicted prices.

### Results
The models were trained and evaluated using the following metrics:

R² Score: Indicates how well the model explains the variance in the target variable.
RMSE (Root Mean Squared Error): Measures the average error in the predictions.
Train/Test Performance: Compared the model's performance on training and test datasets.

### Visualization
Power BI was used for advanced data visualization and further insights into the dataset.

## Dependencies
Python 3.x
Pandas
NumPy
Matplotlib
Seaborn
scikit-learn
XGBoost
Scipy
Power BI for visualization