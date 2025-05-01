# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
import the required libraries: pandas for data manipulation and linear_model from sklearn for regression.

### Step2
Load the dataset using pd.read_csv() and store it in a DataFrame.

### Step3
Separate the features (independent variables) and the target (dependent variable):

Assign the relevant columns to X (features).
Assign the target column to y (output).

### Step4
Create a linear regression model using linear_model.LinearRegression() and fit it to the data using regr.fit(X, y).

### Step5
Print the regression coefficients (regr.coef_) and intercept (regr.intercept_).

## Program:
```
# Developed by: Deepika.V
# Reg no: 24000724

import pandas as pd
from sklearn import linear_model

df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']

regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:',regr.intercept_)

predictedCO2 = regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume',predictedCO2)





```
## Output:
![image](https://github.com/user-attachments/assets/8c539a86-15d2-42e2-8f92-4b53b989b041)

### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
