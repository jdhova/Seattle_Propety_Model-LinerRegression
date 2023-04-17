

## Introduction And Overview:

***

This project aims at creating two Machine Learning models with the kaggle data set below. The first model is build with scikit learn and file name seaptle_pro_EDA and second model
is built with Pycaret and file name is pycaretVerion

Models were built and model perfomance were compared using the R2




### CSV Dataset :

  [PROPERTY_CSVFILE](https://www.kaggle.com/datasets/samuelcortinhas/house-price-prediction-seattle)



### Steps for EDA

1. CHECKS FOR NULLS AND REPLACE 
2. CHECK FOR MEANS AND REPLACE THE NULLS WITH THE MEAN 
3. USE THE LAMBDA FUNCTION IN CALCULATING THE FROM ARCE TO SQFT 
4. PLOT AND START CHECKING OUTLIARS 
5. REMOVE OUTLIARS (DETMINE RANGE TO WORK WITH)
6. CONCATED DATASET TO BECOME ONE THIS WAY ITS EASIET TO DO THE TEST TRAIN SPLIT

### Preparing data for modeling

1. ONE HOT ENDCONG OF THE TEXT FIELDS 
2. SET ASIDE THE UNSEEN DATA FOR THE FINAL TEST OF OUR MODEL (10%)
3. SPLIT DATA INTO X AND y and convart to Numpy array so it can be read by model
4. TRAIN TEST SPLIT  X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25, shuffle=True)
THIS WAY WE HAVE OUR X_train and X_test which is 75% and y_train and y_test which is 25%

### Creating model with Scikit learn 

1. WE CREATE A model Variable and assign to linerReg as it shows model = LinearRegression() 
2. We fit our model model.fit()  model.fit(X_train, y_train) Now we can use our model variable on test and train easily. since its been fit (WE MUST FIT ON THE TRAIN)
3.  PRINT print(model.intercept_) and print(model.coef_) 
 
### Model Validation with Absolute error and R2 Scikit learn 

1. WE GET THE MEAN ERROR BY RUNNING TRAIN ON PREDICTING THE MODEL 
mae_train = mean_absolute_error(y_train, model.predict(X_train))   
2. model.predict(X_train) now becomes the new Prediction of the Dependent Variable y because we run the model.predict method on it
3. we compare the y_train and the model.predict(X_train) which is the preiction from the model.predict
4. Analyse the diff and the mean absolute error
5. USE abs in Analyzing the residuals
6. COMPARE R2 AND MAE 

### Finally I trained Model with unseen data.



### Comparison and Results

---
### R2 : 0.411 For initial model with scikit learn  
    File: seaptle_pro_EDA

### R2 IS 0.4908 for improved model with pycaret.
    File pycaretVerion

### Conclusion:
 In summary The pycaret model with file pycaretVerion has a relatively better model perfomance and a higher R2. Although model R2 can be improved I decided to work witht the initial r2 value without any tunning or overfitting.



