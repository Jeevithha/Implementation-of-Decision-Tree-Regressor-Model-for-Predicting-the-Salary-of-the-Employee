# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1. Import the libraries and read the data frame using pandas.
2.Calculate the null values present in the dataset and apply label encoder.
3.Determine test and training data set and apply decison tree regression in dataset.
4.calculate Mean square error,data prediction and r2.
```

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: jeevitha S
RegisterNumber:  212222100016

import pandas as pd
data=pd.read_csv('/content/Salary_EX7.csv')
from sklearn.tree import DecisionTreeRegressor,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train , y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
plt.figure(figsize=(20,8))
plot_tree(dt, feature_names=x.columns,filled=True)
plt.show()
*/
```

## Output:

## HEAD:
![Screenshot 2024-04-02 193024](https://github.com/sakthipriyadhanusu/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393194/c5637683-ec58-4738-bf8c-c0598ea5e364)

## MSE:
![Screenshot 2024-04-02 193123](https://github.com/sakthipriyadhanusu/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393194/89af8160-53d6-4274-b3bf-dca17bb9429c)

## r2:
![Screenshot 2024-04-02 193415](https://github.com/sakthipriyadhanusu/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393194/10f5f2e7-c755-49e3-9348-1ac121c737af)

![Screenshot 2024-04-02 193511](https://github.com/sakthipriyadhanusu/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393194/375af8d4-30a0-4cec-8312-2ca3d23e7948)

![Screenshot 2024-04-02 193602](https://github.com/sakthipriyadhanusu/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393194/13e3ba1a-0025-4896-959b-6054c445028e)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
