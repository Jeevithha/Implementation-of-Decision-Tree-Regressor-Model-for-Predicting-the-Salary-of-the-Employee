# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. calculate Mean square error,data prediction and R2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: JEEVITHA S
RegisterNumber:212222100016
/*
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
*/
```
## Output:
### data.head()
![238816638-48e17f09-8429-4ac5-8fe2-ee44d76fb21a](https://github.com/Jeevithha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/123623197/0a9eb72e-66b6-4762-917c-b7ac3098489d)
### data.info()
![238816667-c4648e85-9777-4f19-b846-8b1df6a47967](https://github.com/Jeevithha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/123623197/8bcdda5f-53ee-40a6-8f59-379587084b9a)
### isnull() and sum()
![238816705-3aba0d79-e0d6-41ea-bc5d-2f1bd94f8b87](https://github.com/Jeevithha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/123623197/a4eb84c2-3d9a-474f-a9b0-52bfd92e6526)
### data.head() for salary
![238816792-747bdff3-543f-413f-b005-8d2921f227f1](https://github.com/Jeevithha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/123623197/8d020013-bc00-45a3-ac4e-ed2837573f2c)
### MSE value
![238816891-8499df80-847c-4498-b250-f30050c8b58f](https://github.com/Jeevithha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/123623197/431dbd77-bf7c-4e70-bf1e-f8d7ca44dff1)
### R2 value
![238816935-c932496c-87d7-4794-a4a4-807bc4931939](https://github.com/Jeevithha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/123623197/77a2941a-08d4-4978-a895-dd5c470b64b4)
### data prediction
![238816968-a79326e7-b16b-4cc8-aaf3-229fe12b7537](https://github.com/Jeevithha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/123623197/4f3c5439-4f41-4233-9432-82a3d8c2edab)
## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
