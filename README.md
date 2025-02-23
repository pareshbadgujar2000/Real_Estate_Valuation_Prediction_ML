Model Evaluation and Data Splitting( also we have to use Splitting into Train (70%), Validation (15%), and Test (15%))

Overview

This repository contains an evaluation of different regression models, including Linear Regression, Ridge Regression, Lasso Regression, and Random Forest Regressor.
 The models are assessed using Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R² Score, and Adjusted R² Score on both the Test Set and Validation Set.

**Data Splitting Strategy**

To ensure proper model training and evaluation, the dataset is split as follows:

Train Set: 70% of the data (used for training the model)

Validation Set: 15% of the data (used for hyperparameter tuning)

Test Set: 15% of the data (used for final model evaluation)

**Test Set Evaluation**
Model	MSE	RMSE	R²	Adjusted R²
Linear Regression	40.463	6.361	0.682	0.660
Ridge Regression	39.491	6.284	0.690	0.668
Lasso Regression	40.087	6.331	0.685	0.663
Random Forest Regressor	25.011	5.001	0.804	0.790

**Validation Set Evaluation**
Model	MSE	RMSE	R²	Adjusted R²
Linear Regression	105.057	10.250	0.398	0.356
Ridge Regression	104.333	10.214	0.402	0.360
Lasso Regression	104.486	10.222	0.401	0.359
Random Forest Regressor	72.305	8.503	0.586	0.556

**Interpretation**

**Test Set Performance:**
Random Forest Regressor significantly outperforms all linear models (Linear, Ridge, and Lasso).
It has the lowest MSE (25.011) and lowest RMSE (5.001), indicating better predictive accuracy.
It also has the highest R² (0.804) and Adjusted R² (0.790), meaning it explains around 80% of the variance in the test set.
Among the linear models, Ridge Regression performs slightly better than Linear and Lasso, showing a lower MSE and higher R².

**Validation Set Performance:**
The trend is similar to the test set; Random Forest Regressor remains the best performer.
It has the lowest Validation MSE (72.305) and RMSE (8.503), as well as the highest R² (0.586) and Adjusted R² (0.556).
Ridge and Lasso perform similarly, with slightly better generalization than Linear Regression.
All three linear models have higher error and lower R² on the validation set compared to the test set, indicating some overfitting.

**Key Takeaways:**
Random Forest is the best model in terms of predictive performance, showing lower error and explaining more variance.
Linear models struggle on the validation set, indicating they may not generalize well to unseen data.
Ridge Regression outperforms Lasso and Linear Regression, suggesting that some regularization improves generalization.

