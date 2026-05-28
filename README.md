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
import numpy as np
import matplotlib.pyplot as plt

X = np.array(eval(input()))
Y = np.array(eval(input()))

Xmean = np.mean(X)
Ymean = np.mean(Y)


num = np.sum((X - Xmean) * (Y - Ymean))
den = np.sum((X - Xmean) ** 2)

m = num / den
c = Ymean - m * Xmean

print(f"Slope: {m}, Intercept: {c}")

Y_pred = m * X + c
print(Y_pred)

plt.scatter(X, Y, label="Data")
plt.plot(X, Y_pred, color="red", label="Regression line")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.show()
## Output
<img width="1906" height="1023" alt="Screenshot 2026-05-28 101002" src="https://github.com/user-attachments/assets/a435f7e5-74c4-4e0f-a0df-dd9cdd9b7178" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
