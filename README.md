# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. start the program
2. import pandas and read the csv file.
3. print the data head,info(),isnull().
4. import labelencoder and fit transform data"position"
5. Assign a value for x and y.
6. import train_test_split.
7. import decision treeregressor and predict y value.
8. import metrics and calculate mse , then predict data.
9. stop the program.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Srivarshan S
RegisterNumber:  212221040163
*/
import pandas as pd
data=pd.read_csv("/content/sample_data/Salary.csv")
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
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](https://github.com/srivarshan123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/blob/main/data%20head.jpeg)
![Decision Tree Regressor Model for Predicting the Salary of the Employee](https://github.com/srivarshan123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/blob/main/info.jpeg)
![Decision Tree Regressor Model for Predicting the Salary of the Employee](https://github.com/srivarshan123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/blob/main/datainfo.jpeg)
![Decision Tree Regressor Model for Predicting the Salary of the Employee](https://github.com/srivarshan123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/blob/main/predict.jpeg)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
