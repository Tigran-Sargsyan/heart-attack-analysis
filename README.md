# Heart attack analysis

Kaggle dataset: https://www.kaggle.com/datasets/rashikrahmanpritom/heart-attack-analysis-prediction-dataset

EDA and classification project for detecting whether a patient has a high risk of heart attack or no.

## Steps

1. Problem formulation

Having a set of features about a certain patient classify him/her as having a high/low risk of heart attack.

2. Data preprocessing and preparation

Detecting null values and obvious mistakes, getting rid of duplicates, spliting the dataset into feature matrix and target vector.

3. Encoding, scaling

Encoding categorical features, scaling the dataset to fit it into models like logistic regression, which use gradient descent. Also keeping the old version of the dataset for models like CatBoost who can handle categorical features.

4. Exploratory Data Analysis (EDA)

Exploring feature distributions, finding high correlated features to exclude (if they exist). Used pandas-profiling to get a better sense of the dataset.

5. Model developement

Choosing evaluation metric: AUC, trying out various models in increasing complexity (logistic regression, SVM, catboost), hyperparameter tuning and evaluating models using cross-validation, setting optimal thresholds (we want the model to make as little FN-s as possible) etc.

6. Shap values, feature importances and explainability of the model

Calculating feature importances, to view what features have contributed to decision making process the most. Viewing shap values, to more deeply understand the impact of different features on the decisions made. 

7. Model selection

Selected the logistic regression model, because it had almost the same score on the validation set as catboost. Plus they had very similar shap values, so from these two, a conclusion was made to choose a simpler model, because it is faster, lighter and almost always more interpretable.

8. Final testing

Tested the chosen model (logistic regression) to see the results on the test set.
