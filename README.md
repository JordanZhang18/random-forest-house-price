# random-forest-house-price
Random forest and gradient boosting were applied to model the house price project on Kaggle

Two linear regression models were trained: simple linear model and Ridge regression model, with alpha=70. 

A random forest model was also trained, setting n_estimators = 500, and max_features = 4 because 19 features were studied. 

A Gradient Boosting Regressor was also trained. CV grid search was used to find proper parameters. Combinations of n_estimators = [100, 200, 300, 400, 500] and learning_rate = [0.0001, 0.001, 0.01, 0.1] were searched, with max_features = 4 set. Using neg_mean_squared_error as scoring method, the GridSearchCV produced best parameters as estimators=200 and learning rate = 0.1.

**Review results, evaluate models**

Cross_val_score in sklearn module was used to evaluate the root mean-squared error, using a 5-fold cross -validation design.Based on the cross validation RMSE, the random forest and gradient boosting regressors outperforms the linear regression models.
