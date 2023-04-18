

## Introduction And Overview:

***

This project aims at creating two Machine Learning models with the Seattle Property kaggle data set below. The first model is built with scikit learn and file name seaptle_pro_EDA and second model is built with Pycaret and file name is pycaretVerion

Models were built and model perfomance were compared using the R2




### CSV Dataset :

  [PROPERTY_CSVFILE](https://www.kaggle.com/datasets/samuelcortinhas/house-price-prediction-seattle)


## Scikit Learn Pipeline
***

### Steps for EDA

1. Check for Nulls and Replace 
2. Replace the Null Value with the Mean
3. Convart from Arce to Sqft with Lamda Function
4. Plot and check for Outliars
5. Remove Outliars and determine the range we are working with
6. Concatnate dataset to become one dataset, this way its easier to do the test and train split

### Preparing data for modeling

1. One hot encoding for the text fields
2. Set Aside the unseen data for the final test of our model (10%)
3. Split data into X and y and convart to Numpy Array so it can be rad by model 
4. Train Test Split X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25, shuffle=True)
This way we have our X_train and X_test which is 75% and y_train and y_test which is 25%

### Creating model with Scikit learn 

1. We Create a  model Variable and assign to linerReg as it shows model = LinearRegression() 
2. We fit our model model.fit()  model.fit(X_train, y_train) Now we can use our model variable on test and train easily. since its been fit (WE MUST FIT ON THE TRAIN)
3. Print(model.intercept_) and print(model.coef_) 
 
### Model Validation with Absolute error and R2 Scikit learn 

1. We get the Mean Error by running Train and predicting the model mae_train = mean_absolute_error(y_train, model.predict(X_train))   
mae_train = mean_absolute_error(y_train, model.predict(X_train))   
2. model.predict(X_train) now becomes the new Prediction of the Dependent Variable y because we run the model.predict method on it
3. we compare the y_train and the model.predict(X_train) which is the preiction from the model.predict
4. Analyse the diff and the mean absolute error
5. Use SE abs in Analyzing the residuals
6. Compare R2 AND MAE 

### Finally I trained Model with unseen data.


***




## Pycaret Pipeline  
***

file: pycaretVersion.ipynb

### Initial EDA

1.  We started by importing the cleaned data CSV file 
2.  Checking for nulls and EDA to make sure data is in the right format and cleaned.
3.  Setting Aside Unseen data 

### Data Prep

1. Creating Data Prep with pycaret.
2. Comparing the best 2 models which are gbr and ridge.
3. Create the gbr model and assigning to a variable.
4. Then we arrived at the r2 for the pycaret pipeline which we used for the comparison.







### Comparison and Results

---
### R2 : 0.411 For initial model with scikit learn  
    File: seaptle_pro_EDA

### R2 IS 0.4908 for improved model with pycaret.
    File pycaretVerion

### Conclusion:
 In summary The pycaret model with file pycaretVerion has a relatively better model perfomance and a higher R2. Although model R2 can be improved I decided to work witht the initial r2 value without any tunning or overfitting.



