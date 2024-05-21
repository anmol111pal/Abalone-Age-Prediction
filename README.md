# Abalone Age Prediction

## Overview
The goal of this project is to predict the age of abalone using various physical measurements. The dataset used for this task is the Abalone dataset from Kaggle. The age of abalone is determined by the number of rings, which is the dependent variable in this study.

## Dataset
The dataset for this competition (both train and test) was generated from a deep learning model trained on the Abalone dataset. Feature distributions are close to, but not exactly the same, as the original. Feel free to use the original dataset as part of this competition, both to explore differences as well as to see whether incorporating the original in training improves model performance.

The training data consists of the following features:

- `Sex`: Categorical variable indicating the sex of the abalone (M, F, I)
- `Length`: Continuous variable indicating the length of the abalone (in mm)
- `Diameter`: Continuous variable indicating the diameter of the abalone (in mm)
- `Height`: Continuous variable indicating the height of the abalone (in mm)
- `Whole weight.1`: Continuous variable indicating the whole weight of the abalone (in grams)
- `Whole weight.2`: Continuous variable indicating another measurement of the whole weight (in grams)
- `Whole weight.3`: Continuous variable indicating yet another measurement of the whole weight (in grams)
- `Shell Weight`: Continuous variable indicating the weight of the shell (in grams)
- `Rings`: Integer variable indicating the number of rings, which is used to determine the age of the abalone

The target variable is `Rings`.

## Model Training
Two regression algorithms were employed to predict the age of abalone:

1. **Random Forest Regressor**
2. **XGBoost Regressor**

### Model Comparison
The dataset was split into training and testing sets to evaluate the performance of these models. The scores achieved on the training and test sets were as follows:

- **Random Forest Regressor**: RMSLE of approximately 0.1561
- **XGBoost Regressor**: RMSLE of approximately 0.1526

Based on these results, the XGBoost Regressor showed slightly better performance compared to the Random Forest Regressor and was therefore selected as the final model.

### Final Model
The XGBoost Regressor was trained on the entire training dataset. This model achieved a metric score (RMSLE) of approximately 0.1574 on (unseen) test data.

## Implementation
### Dependencies
The following Python libraries were used in this project:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

### Training and Evaluation
1. **Data Preprocessing**: The dataset was preprocessed to handle categorical variables and normalize the features.
2. **Model Training**: Both Random Forest and XGBoost models were trained on the training set.
3. **Model Evaluation**: The models were evaluated on the test set, and their performance was compared.
4. **Final Prediction**: The XGBoost model was trained on the entire training dataset and used to predict the test set.

## Conclusion
The XGBoost Regressor model demonstrated better performance compared to the Random Forest Regressor in predicting the age of abalone. This model was used to generate predictions on unseen data. The project showcases the application of advanced regression techniques to solve real-world problems.

## Author
Anmol Pal
