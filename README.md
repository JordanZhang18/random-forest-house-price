# random-forest-house-price
Random forest and gradient boosting were applied to model the house price project on Kaggle

The appropriate hyper-parameters for fitting the random forest were found using randomized search CV. 
The criterion of ‘entropy’ and ‘gini’, as well as number of estimators ranging from 100 to 200 were explored. 
Using cv=5 and 2 iterations, the randomized search suggests 200 estimators and Gini as classification criterion.

Then a Random Forest Classifier was trained using all training set. The fitting took 71 seconds. 
Prediction was made using this classifier and will later be compared to other model’s predictions.

A second approach combined the training and testing set for a principal components analysis. 
The combined data set was scaled using standard scaler before fitting. The PCA was fitted to account for 95% of variability. 
The result PCA contains 332 features (comparing to 784 in raw data), and the fitting took 8 seconds.
A second random forest was trained based on the PCA transformed training set. The new model fitting took 44 seconds.
