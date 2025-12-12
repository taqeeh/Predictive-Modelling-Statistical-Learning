📊 Predictive Modeling and Statistical Learning

A supervised learning project focused on model comparison, evaluation, and selection using a large structured dataset.

🔍 Overview

This project compares multiple statistical and machine learning models to predict a continuous response variable using a large dataset. The objective was to evaluate predictive performance, understand bias variance tradeoffs, and select a final model based on out of sample accuracy.

The work emphasizes rigorous validation, model interpretability, and practical decision making, rather than black box optimization.

🗂️ Dataset
- ~20,000 observations
- 19 predictor variables
- Continuous target variable
- The data was divided into:
- Training dataset for model development and validation
- Test predictor dataset used for final prediction generation

🧠 Modeling Approach
1. Baseline Model
- Least Squares Regression
- Used as a benchmark for comparison
- Evaluated using 10 fold cross validation and MSPE

3. Regularized Regression
- Ridge Regression
- LASSO Regression
- Penalty parameters selected using cross validation
- These models were tested to determine whether regularization improved performance in a low dimensional, high signal setting.

3. Tree Based Models

- Regression Tree with cost complexity pruning
- Random Forest with hyperparameter tuning using out of bag error
- Gradient Boosting using XGBoost
- Tree based methods were applied to capture nonlinear relationships not addressed by linear models.

📈 Model Evaluation

- 10 fold cross validation applied consistently across models
- Mean Squared Prediction Error (MSPE) used as the primary evaluation metric
- Random Forest achieved the lowest MSPE after tuning mtry and ntree
- Final model selected based on predictive accuracy and stability

✅ Key Findings

- Regularization did not outperform least squares due to strong signal across predictors
- Single regression trees reduced error but exhibited high variance
- Ensemble methods significantly improved predictive accuracy through variance reduction
- A tuned Random Forest best captured complex nonlinear relationships

🛠️ Tools and Technologies
- Language: R
- Libraries: tidyverse, glmnet, rpart, randomForest, xgboost
