# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the libraries and read the data frame using pandas.
2.Calculate the null values present in the dataset and apply label encoder.
3.Determine test and training data set and apply decison tree regression in dataset.
4.Calculate Mean square error,data prediction and r2.
 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: R.PRIYANGA
RegisterNumber:212223230161

```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
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
## DATA HEAD:
![image](https://github.com/user-attachments/assets/abd65801-77f7-45ee-a5c4-539e517819bb)
## DATA INFO:
![image](https://github.com/user-attachments/assets/1b90d189-4faa-4ed9-b798-64588db712ca)
## ISNULL()ANDSUM():
![image](https://github.com/user-attachments/assets/85d3d658-ca89-4aec-9d1d-1d0b14f85512)
## DATA HEAD FOR SALARY:
![image](https://github.com/user-attachments/assets/0770fcba-1040-4675-b02f-fc0de39c2c1e)

## MEAN SQUARE ERROR:
![image](https://github.com/user-attachments/assets/37fa782e-e4cf-42e7-adc6-d1bf76e65608)
## R2 VALUE:
![image](https://github.com/user-attachments/assets/bc826848-a8e3-4dcb-85a3-5697cb52e91c)
## DATA PREDICTION:
![image](https://github.com/user-attachments/assets/114b199f-0ffe-4f68-a41b-7e0e36f1fe93)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
