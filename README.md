# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard libraries.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5.Predict the values of arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7.Predict the values of array.

8.Apply to new unknown values. 

## Program:
```PYTHON
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: VARUN J C
RegisterNumber:  212224240179
import pandas as pd

import matplotlib.pyplot as plt

from sklearn.tree import DecisionTreeClassifier, plot_tree

data = pd.read_csv("/content/Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

data["Position"] = le.fit_transform(data["Position"])

data.head()

x=data[["Position","Level"]]

y=data["Salary"]

from sklearn.model_selection import train_test_split

x_train, x_test, y_train, y_test = train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor,plot_tree

dt=DecisionTreeRegressor()

dt.fit(x_train,y_train)

y_pred=dt.predict(x_test)
from sklearn import metrics

mse = metrics.mean_squared_error(y_test,y_pred)

mse
r2=metrics.r2_score(y_test,y_pred)

r2
dt.predict([[5,6]])

plt.figure(figsize=(20, 8))

plot_tree(dt, feature_names=x.columns, filled=True)

plt.show()
*/
```

## Output:
![435535655-40a9db69-15f1-4c1b-a2e5-c305bf0c224a](https://github.com/user-attachments/assets/904eb213-fe0d-4f1f-aab3-4c56dbc65026)

![Screenshot 2025-04-21 114052](https://github.com/user-attachments/assets/0d8805e7-b622-415f-a781-5c0bd9b02624)

![Screenshot 2025-04-21 114100](https://github.com/user-attachments/assets/c3a9f29a-d7e7-48e5-80f5-1bdaa4abd09d)

![Screenshot 2025-04-21 114142](https://github.com/user-attachments/assets/e92c394f-e7e7-4c56-9d2f-59fa0c7e1ddd)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
