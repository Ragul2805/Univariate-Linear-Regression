# Implementation of Univariate Linear Regression
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
x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()


x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
den=0
for i in range(len(x)):
num+=(x[i]-x_mean)*(y[i]-y_mean)
den+=(x[i]-x_mean)**2
m=num/den
c=y_mean-m*x_mean
print(m,c) 



y_pred=m*x+c
print(y_pred)
plt.scatter(x,y)
plt.plot([min(x),max(x)],[min(y_pred),max(y_pred)],color='red')
plt.show() 




```
## Output
</br>![WhatsApp Image 2025-12-14 at 09 24 01_e9ed88a8](https://github.com/user-attachments/assets/ff1faa6e-fd92-4ff6-92ce-4da3ad4e70f7)

</br>
![WhatsApp Image 2025-12-14 at 09 24 20_2a911e5c](https://github.com/user-attachments/assets/1dd0fcf2-5a73-4d5e-b718-f6058c373fc7)

</br>
![WhatsApp Image 2025-12-14 at 09 24 53_9642c2d8](https://github.com/user-attachments/assets/da21680a-336f-412f-8b41-f9b28ae7bb33)

</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
