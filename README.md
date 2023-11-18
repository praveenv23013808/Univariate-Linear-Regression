# Implementation of Univariate Linear Regression
EX 09 Implementation of Univariate Linear Regression
Date: 27.10.2023
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
xmean=np.mean(x)
ymean=np.mean(y)
num,den=0,0
for i in range(len(x)):
  num +=(x[i]-xmean)*(y[i]-ymean)
  den +=(x[i]-xmean)**2
m=num/den
c=ymean-m*xmean
print(m,c)
y_pred=m*x+c
print(y_pred)
plt.scatter(x,y)
plt.plot(x,y_pred,color='orange')
plt.show()
```
## Output
![282996186-a0e1bed8-18cc-401b-aab6-4d26ab881e34](https://github.com/praveenv23013808/Univariate-Linear-Regression/assets/145824728/6b694616-ad85-4c86-bd98-273e3f6e6d11)
## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
