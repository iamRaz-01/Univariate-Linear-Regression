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
```python
##Developed By Abdul Razak N 24002896

import numpy as np
import matplotlib.pyplot as plt

# Input data points
x = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

# Scatter plot of the data
plt.scatter(x, y, color='red', label='Data points')
plt.title("Scatter Plot of Input Data")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.legend()
plt.show()

# Calculate the mean of x and y
xmean = np.mean(x)
ymean = np.mean(y)

# Initialize numerator and denominator for slope calculation
num = 0  # Numerator for slope formula
den = 0  # Denominator for slope formula

# Calculate slope (m) using the formula
for i in range(len(x)):
    num += (x[i] - xmean) * (y[i] - ymean)
    den += (x[i] - xmean) ** 2

m = num / den  # Slope of the regression line
b = ymean - m * xmean  # Intercept of the regression line

# Print the slope and intercept
print("Slope (m):", m)
print("Intercept (b):", b)

# Predict y values using the regression line equation
ypred = m * x + b
print("Predicted y values:", ypred)

# Plot the original data points and the regression line
plt.scatter(x, y, color='red', label='Data points')
plt.plot(x, ypred, color='blue', label='Regression line')
plt.title("Linear Regression")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.legend()
plt.show()




```
## Output
![image](https://github.com/user-attachments/assets/5bb2e797-6f4b-458b-b2ec-948fbf4d07b7)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
