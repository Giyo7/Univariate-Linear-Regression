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
# Simple Linear Regression from Scratch

import numpy as np
import matplotlib.pyplot as plt

# -------------------------------
# 1. Preprocessing Input Data
# -------------------------------
X = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
Y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

# Plot original data
plt.scatter(X, Y)
plt.title("Actual Data Points")
plt.xlabel("X")
plt.ylabel("Y")
plt.show()

# -------------------------------
# 2. Building the Model
# -------------------------------
X_mean = np.mean(X)
Y_mean = np.mean(Y)

num = 0
den = 0

for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean) ** 2

# slope (m) and intercept (c)
m = num / den
c = Y_mean - m * X_mean

print("Slope (m):", m)
print("Intercept (c):", c)

# -------------------------------
# 3. Making Predictions
# -------------------------------
Y_pred = m * X + c
print("Predicted Y values:", Y_pred)

# -------------------------------
# 4. Plotting Regression Line
# -------------------------------
plt.scatter(X, Y)                  # actual values
plt.plot(X, Y_pred, color='red')   # regression line
plt.title("Linear Regression From Scratch")
plt.xlabel("X")
plt.ylabel("Y")
plt.show()
```
## Output
![sc 3](https://github.com/user-attachments/assets/9115fbcf-602c-4cec-ac6a-7481c566ff83)
![sc 3](https://github.com/user-attachments/assets/a3037ba0-8184-4654-840f-fa737ec476bd)
![sc 1](https://github.com/user-attachments/assets/6d54957c-eb3e-47fb-aa11-968b800e8782)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
