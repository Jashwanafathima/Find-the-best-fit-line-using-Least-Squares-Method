# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.

**6.** Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by:Jashwana Fathima S
RegisterNumber: 212222040059
*/
```
```
import numpy as np
import matplotlib.pyplot as plt

X=np.array(eval(input()))
Y=np.array(eval(input()))
X_mean=np.mean(X)
print("X_mean =",X_mean)
Y_mean=np.mean(Y)
print("Y_mean =",Y_mean)
num=0
denum=0

for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
m=num/denum

print("Slope =",m)
b=Y_mean - m*X_mean
print("Y-intercept =",b)
Y_pred=m*X+b
print("Predicted Value of Y using X =",Y_pred)
plt.scatter(X,Y,color='blue')
plt.xlabel("X_values")
plt.ylabel("Y_values")
plt.plot(X,Y_pred,color='red') 
plt.show()
```

## Output:
![ml1](https://github.com/user-attachments/assets/0113e883-98a4-41dc-92a9-b304c2ae09be)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
