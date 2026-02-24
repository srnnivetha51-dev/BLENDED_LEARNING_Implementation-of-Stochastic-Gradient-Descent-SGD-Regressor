# BLENDED_LEARNING
# Implementation-of-Stochastic-Gradient-Descent-SGD-Regressor

## AIM:
To write a program to implement Stochastic Gradient Descent (SGD) Regressor for linear regression and evaluate its performance.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Start

2. Import Required Libraries
   Import necessary libraries such as NumPy, Pandas, and Sklearn.
3. Load the Dataset
   Read the dataset and separate it into input features (X) and target variable (y).

4. Preprocess the Data

5. Handle missing values (if any).

6. Perform feature scaling (Standardization is recommended for SGD).

7. Split the Dataset
   Divide the dataset into Training set and Testing set (e.g., 80% training, 20% testing).
   Initialize the SGD Regressor Model
8. Create an instance of SGD Regressor with appropriate   parameters such as
   Learning rate
   Maximum iteration
   Tolerance value
   Train the Model
   Fit the SGD Regressor model using the training dataset.
   Make Predictions
   Use the trained model to predict output values for the test dataset.

9. Evaluate Model Performance
10. Calculate performance metrics such as:
    Mean Squared Error (MSE)
    Root Mean Squared Error (RMSE)
    R² Score

## Program:
```
/*
Program to implement SGD Regressor for linear regression.
import pandas as pd 
import numpy as np

from sklearn.linear_model import SGDRegressor
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import mean_squared_error,r2_score,mean_absolute_error
import matplotlib.pyplot as plt

data=pd.read_csv("CarPrice_Assignment.csv")

print(data.head())
print(data.info())

data=data.drop(['CarName','car_ID'],axis=1)
data=pd.get_dummies(data,drop_first=True)

x=data.drop('price',axis=1)
y=data['price']

scaler=StandardScaler()
x=scaler.fit_transform(x)
y=scaler.fit_transform(np.array(y).reshape(-1,1))
print(x)
print(y)

x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=42)

sgd_model=SGDRegressor(max_iter=1000,tol=1e-3)
sgd_model.fit(x_train,y_train)

y_pred=sgd_model.predict(x_test)
mse=mean_squared_error(y_test,y_pred)
mse=mean_squared_error(y_test,y_pred)

print('Name: SR NIVEDHITHA')
print('Reg NO: 212225240102')

print(f"MSE: {mean_squared_error(y_test,y_pred):.2f}")
print(f"MAE: {mean_absolute_error(y_test,y_pred):.2f}")
print(f"R^2: {r2_score(y_test,y_pred):.4f}")

print("\nModel Coeffient")
print("Coefficient:",sgd_model.coef_)
print("Intercept:",sgd_model.intercept_)

plt.scatter(y_test,y_pred)
plt.xlabel("Actual Price")
plt.ylabel("Predicted Price")
plt.title("Actual vs Predicted Prices using SGD Regressor")
plt.plot([min(y_test),max(y_test)],[min(y_test),max(y_test)],color='red')
plt.show()

Developed by: S R NIVEDHITHA
RegisterNumber:  212225240102
*/
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)
![alt text](<Screenshot 2026-02-24 194024.png>)
![alt text](<Screenshot 2026-02-24 194034.png>)
![alt text](<Screenshot 2026-02-24 194044.png>)
![alt text](<Screenshot 2026-02-24 194102.png>)
![alt text](<Screenshot 2026-02-24 194112.png>)


## Result:
Thus, the implementation of Stochastic Gradient Descent (SGD) Regressor for linear regression has been successfully demonstrated and verified using Python programming.
