# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import pandas module as pd

### Step2
From sklearn module import linear_model

### Step3
Using pd.read_csv function read the cars.csv file

### Step4
Make a list of the independent values(Weight&Volume) and call this variable x and put the
dependent values(CO2) in a variable called y

### Step5
From the sklearn module use the LinearRegression() method to create a linear regression
object.This object has a method called fit() that takes the independent and dependent values as
parameters and fills the regression object with data that describes the relationship.

Step6
Use .coef_ and .intercept_ function to find the coefficient and intercept

Step7
Predict the Linear Regression using regr.predict() method and print it

Step8
End of program

## Program:
```
##Developed by:S.Aishwarya
##reference no:22008635
import pandas as pd
from sklearn import linear_model
df=pd.read_csv("cars.csv")
X=df[['Weight', 'Volume']]
y=df['CO2']
regr=linear_model.LinearRegression()
regr.fit(X,y)
print('Coefficients',regr.coef_)
print('Intercept',regr.intercept_)
predictedCO2=regr.predict([[3300,1300]])
print('Predicted CO2 emission based on weight and volume:',predictedCO2)

```
## Output:

![Screenshot (89) 1](https://user-images.githubusercontent.com/121418444/215153951-5b9c1b7e-dfd3-4769-a852-a8c809ee084b.png)

### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
