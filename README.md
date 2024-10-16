![Screenshot 2024-10-16 145526](https://github.com/user-attachments/assets/4327a4b0-0d4d-4038-a236-a32f5817fc9a)# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard liberaries.
2. Upload the dataset and check for any null values using .isnull()
3. Import Label Encoder and encode the dataset.
4. Import Decision Tree Regressor from sklearn and apply the model on the dataset.
5. Predic the values of arrays
6. Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset .
7. Predict the values of arrays .
8. Apply to new unknown values .

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
![Screenshot 2024-10-16 145026](https://github.com/user-attachments/assets/dff567f9-817a-462b-8daf-1156ca441b00)
data.info()
![Screenshot 2024-10-16 145059](https://github.com/user-attachments/assets/1847cd9a-6115-49f2-8df7-1de033431922)
data.isnull().sum()
![Screenshot 2024-10-16 145140](https://github.com/user-attachments/assets/1234db82-1d52-4172-8d11-245f6c2a21ba)
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
![Screenshot 2024-10-16 145228](https://github.com/user-attachments/assets/4e185447-3a80-4ff9-836a-88ca776d97b4)
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
![Screenshot 2024-10-16 145315](https://github.com/user-attachments/assets/cbf878cd-70c2-4444-a67c-ff84ab943b8e)
r2=metrics.r2_score(y_test,y_pred)
r2
![Screenshot 2024-10-16 145348](https://github.com/user-attachments/assets/488b46b1-a568-4a3e-9e33-419d46c9a3aa)
dt.predict([[5,6]])
## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![Screenshot 2024-10-16 145526](https://github.com/user-attachments/assets/cb13a918-3e5a-4bde-997a-d823ad345de4)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
