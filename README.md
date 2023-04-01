# Best Model and Params for a Given Dataset
## Description
The objective of this project was to find the best machine learning model and params for a given dataset. To accomplish this task, I used the diamonds dataset from Kaggle competition with my cohort name, i.e. diamonds-datamad1022-part.

## Dataset
The diamonds dataset consists of data related to the prices and attributes of several diamonds. It has 10 variables and 53,940 observations. I worked with two files:

- train.csv: This file contains the data with a target variable.
- test.csv: This file contains the data without a target variable.

## Data Processing
Before applying any model, I had to process and clean the dataset. To simplify the process, I modularized this step into functions that can be found in the data_processing.py file. These functions were used for both train and test datasets.

## Model Training
Once the data was processed, I trained a model using the train dataset. I performed train-test split to evaluate the models and chose the best model based on the lowest Mean Squared Error (MSE) value. I tried different models such as Random Forest Regressor, XGBoost, and Gradient Boosting. The final model I selected was Random Forest Regressor with hyperparameters tuned using RandomizedSearchCV.

## Model Export
After selecting the best model, I exported it using joblib, which allowed me to save the model and load it again in the future without retraining it.

## Model Prediction
With the trained model, I predicted the prices for the test dataset, generating a new column with the predicted values. I then created a submission.csv file with the predicted prices for each diamond ID.

## Deliverables
The deliverables for this project include:

- data_processing.py file with modularized data processing functions.
- Jupyter notebook (diamonds_project.ipynb) with the code and results for each step of the project.
submission.csv file with the predicted prices for the test dataset.
- Summary slide (in diamonds_project_summary.ipynb file) with the metrics obtained and rationale behind the model selection.

## Metrics and Model Selection
I evaluated the models using Mean Squared Error (MSE) and R-squared (R^2) as metrics. I selected the Random Forest Regressor model with hyperparameters tuned using RandomizedSearchCV because it had the lowest MSE and highest R^2 values compared to other models I tried. This model gave me an MSE of 525.27 and an R^2 of 0.98 on the test dataset.

## Conclusion
In conclusion, I was able to find the best model and params for the given diamonds dataset using a Random Forest Regressor model with hyperparameters tuned using RandomizedSearchCV. The model achieved an MSE of 525.27 and an R^2 of 0.98 on the test dataset, which shows that it is a good fit for the data.