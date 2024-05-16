# Load_forecasting

This project was conducted as part of the ECE 563 course, focusing on the predictive analysis of electricity load values based on temperature data. The study aimed to explore and model the relationships between hourly load values in 20 different zones and temperature data from 11 stations. Two machine learning algorithms, RandomForestRegressor and GradientBoostingRegressor, were employed to predict the load values for the first week of June 2008.

# Data Preprocessing
The data preprocessing phase involved the following steps:

<br />Loading and Cleaning Data: The load and temperature data were loaded into Pandas DataFrames. Datetime columns were created for uniformity and ease of manipulation.
<br />Excluding Data from June 2008: Data from June 2008 was excluded to prevent leakage during the modeling process.
Melting Data: The hourly data columns were converted into rows for easier analysis.
Merging Datasets: The melted load and temperature data were merged to create a combined dataset.

# Mapping Temperature Stations to Load Zones
The correlation between load values and temperature data was calculated for each zone-station pair. The station with the highest correlation coefficient was chosen as the representative station for predicting load values in each zone.

# Machine Learning Models

# Random Forest Regressor
Hyperparameters Tuned:
n_estimators: 150
max_depth: 10
min_samples_split: 6

# Model Performance:
Training Score: 0.7248
Validation Score: 0.6969
Test Score: 0.7024

# Gradient Boosting Regressor
Hyperparameters Tuned:
learning_rate: 0.2
max_depth: 3
n_estimators: 150

# Model Performance:
Training Score: 0.7178
Validation Score: 0.7047
Test Score: 0.7095

# Results and Analysis
Both models were evaluated based on their performance on training, validation, and test datasets. The RandomForestRegressor provided robust initial predictions, while the GradientBoostingRegressor offered improved accuracy with a slight increase in computational cost. The mapping of temperature stations to load zones significantly enhanced the predictive capability of both models.

# Future Work
Feature Engineering: Introduce additional temporal and historical features to capture more complex load patterns.
Model Ensembling: Explore ensemble techniques to combine predictions from multiple models for improved accuracy.
External Data Integration: Incorporate external data sources like weather forecasts and economic indicators to enhance model robustness.

# Contributors
Furkan Mohamed
