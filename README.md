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
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()





```
## Output
<img width="595" height="460" alt="{A98D7FF9-A3B8-43D0-8024-B8EAB4E33AE8}" src="https://github.com/user-attachments/assets/aeb6cbbd-c5ee-4536-85f0-6b6c6f24a459" />
<img width="330" height="49" alt="{D4D23962-8C21-4533-BB35-D36AAB615D80}" src="https://github.com/user-attachments/assets/98d0e1d4-1ca0-4204-a0e9-d38fe6440cca" />
<img width="626" height="46" alt="{30C30FF4-271C-4B20-8842-4980797733EB}" src="https://github.com/user-attachments/assets/abbb6804-8eb6-4932-bd29-26cd5c968526" />
<img width="662" height="494" alt="{027D8B6D-137C-4DB9-93C3-B49C865A42B6}" src="https://github.com/user-attachments/assets/7ac061f0-9b91-4f3e-89ed-efad37541675" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
