# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. calculate Mean square error,data prediction and r2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Jasim Ahamed A
RegisterNumber:  212225040143
*/
```
```
/*
import pandas as pd
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor
from sklearn import metrics

data = pd.read_csv("Salary.csv")
print(data.head(), "\n")
print(data.info(), "\n")
print(data.isnull().sum(), "\n")

le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
print(data.head(), "\n")

x = data[["Position", "Level"]]
y = data["Salary"]

x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=2)

dt = DecisionTreeRegressor(random_state=2)
dt.fit(x_train, y_train)

y_pred = dt.predict(x_test)

mse = metrics.mean_squared_error(y_test, y_pred)
r2 = metrics.r2_score(y_test, y_pred)

print(mse)
print(r2)

print(dt.predict([[5, 6]])[0])
*\

## Output:
### data.head():
<img width="392" height="147" alt="image" src="https://github.com/user-attachments/assets/0adc1975-a7df-4d84-b62b-f827d8d22d1c" />

### data.isnull().sum():

<img width="297" height="100" alt="image" src="https://github.com/user-attachments/assets/82dfeccd-c014-4d96-a337-48837e3ca562" />

### data.head() for salary
<img width="452" height="50" alt="image" src="https://github.com/user-attachments/assets/d8219678-60ca-47c8-a2ab-5b9a77ddc36b" />

### MSE and r2 value:
<img width="262" height="31" alt="image" src="https://github.com/user-attachments/assets/dab17573-3305-433f-ad10-084d05a445a4" />


### data prediction:


<img width="242" height="25" alt="image" src="https://github.com/user-attachments/assets/51badce2-1e95-433a-8853-9bca2776f99a" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
