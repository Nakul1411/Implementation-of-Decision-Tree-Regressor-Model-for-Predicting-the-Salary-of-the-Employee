# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Import the standard libraries.
2.  Upload the dataset and check for any null values using .isnull()
function.
3.  Import LabelEncoder and encode the dataset.
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
![Screenshot 2024-10-16 145026](https://github.com/user-attachments/assets/1101d406-9d06-4ba3-8b1e-52194aefd87c)
data.info()
![Screenshot 2024-10-16 145059](https://github.com/user-attachments/assets/0e98adc9-c811-4513-a1d7-07049c84d204)
data.isnull().sum()
![Screenshot 2024-10-16 145140](https://github.com/user-attachments/assets/b7b5d202-39a7-408e-8d15-56db6d4eb410)
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
![Screenshot 2024-10-16 145228](https://github.com/user-attachments/assets/409465ac-eeef-41e9-af19-b9d3999df758)
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
![Screenshot 2024-10-16 145315](https://github.com/user-attachments/assets/042a9c7d-a4ba-46b2-9436-ae4ecafcd5b9)
r2=metrics.r2_score(y_test,y_pred)
r2
![Screenshot 2024-10-16 145348](https://github.com/user-attachments/assets/1bf21ca7-bb17-42da-a73c-3d35932281dc)
dt.predict([[5,6]])
## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![Screenshot 2024-10-16 145526](https://github.com/user-attachments/assets/1d8a9620-a23d-4676-a309-8484ea0c7251)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
