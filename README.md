# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Import the standard libraries.
2. Upload the dataset and check for any null values using .isnull()
function.
3. Import LabelEncoder and encode the dataset.
4.  Import DecisionTreeRegressor from sklearn and apply the model on
the dataset.
5. Predict the values of arrays.
6.  Import metrics from sklearn and calculate the MSE and R2 of the
model on the dataset.
7. Predict the values of array.
8.  Apply to new unknown values.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: NAKUL R
RegisterNumber:  212223240102
*/
```
import pandas as pd
data=pd.read_csv("/content/Salary.csv")
data.head()
![Screenshot 2024-10-16 145026](https://github.com/user-attachments/assets/e999974e-08a2-47eb-a21a-66fdb16b8fbe)
data.info()
![Screenshot 2024-10-16 145059](https://github.com/user-attachments/assets/38a127b9-acc3-4516-8a76-e2ebad384681)
data.isnull().sum()
![Screenshot 2024-10-16 145140](https://github.com/user-attachments/assets/cf9dc1d3-19cd-4f8c-a518-5798aa5e224d)
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
![Screenshot 2024-10-16 145228](https://github.com/user-attachments/assets/5b23a3b6-dec2-4276-a471-8352033cb4f5)
x=data[["Position","Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y, test_size=0
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
![Screenshot 2024-10-16 145315](https://github.com/user-attachments/assets/82175555-9220-4d68-a10e-155d96d44594)
r2=metrics.r2_score(y_test,y_pred)
r2
![Screenshot 2024-10-16 145348](https://github.com/user-attachments/assets/a75fc90d-797d-444e-8fd2-27abaa859bf9)
dt.predict([[5,6]])
## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![Screenshot 2024-10-16 145526](https://github.com/user-attachments/assets/f9e6381a-4826-4e74-9e3a-686d5970c835)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
