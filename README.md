# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1

Import the necessary Python libraries for data handling, modeling, and evaluation.

### Step2

Load the dataset containing multiple predictor variables and the target variable.

### Step3

Separate the dataset into predictor variables (features) and the target variable (output).

### Step4

Split the dataset into training and testing sets for model training and evaluation.

### Step5

Create and train the multivariate linear regression model using the training data.

## Program:
```


import matplotlib.pyplot as plt
import numpy as np
from sklearn import datasets,linear_model,metrics
boston=datasets.load_diabetes(return_X_y=False)
#defining feature matrix(X) and response vector (y)
x=boston.data
y=boston.target
#splitting x and y into training and testing sets
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.4,random_stat
#create linear regression object
reg=linear_model.LinearRegression()
#train the model using the training sets
reg.fit(x_train,y_train)
#regression coefficients
print("Coefficients",reg.coef_)
#variance score: 1means perfect prediction
print("Variance score: {}".format(reg.score(x_test,y_test)))
#plot for residual error
#setting plot style
plt.style.use("fivethirtyeight")
#plotting residual errors in training data
plt.scatter(reg.predict(x_train),reg.predict(x_train)-y_train,color='green'
#plotting residual errors in test data
plt.scatter(reg.predict(x_test),reg.predict(x_test)-y_test,color='blue',s=10
#plotting line for zero residual error
plt.hlines(y=0,xmin=0,xmax=50,linewidth=2)
#plotting legend
plt.legend(loc='upper right')
#plot title
plt.title('Residual errors')
##method call for showing the plot
plt.show()

Developed by: LAL RHIDHISHAN R
Register No.:212225100022

```
## Output:

### Insert your output

<img width="1037" height="609" alt="image" src="https://github.com/user-attachments/assets/81a60af1-3c18-458b-abad-5803bc5fa4e1" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
