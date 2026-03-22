# Numerical ODE Solvers

This repository contains a JavaScript implementation of standard numerical methods for solving **Ordinary Differential Equations (ODEs)**. It provides a structured way to compare the accuracy of different approximation techniques for initial value problems of the form $y' = f(x, y)$ with $y(x_0) = y_0$. 

---

## 🚀 Implemented Methods

Compute approximations using three distinct techniques:

### 1. Euler's Method
A basic first-order method that uses the tangent line at the current point to step forward.
* **Formula:** $y_{n+1} = y_n + h \cdot f(x_n, y_n)$

### 2. Improved Euler (Heun's Method)
A second-order predictor-corrector method. It improves accuracy by averaging the slopes at the beginning and the predicted end of the interval.
* **Predictor:** $k_1 = f(x_n, y_n)$
* **Corrector:** $k_2 = f(x_n + h, y_n + h \cdot k_1)$
* **Update:** $y_{n+1} = y_n + \frac{h}{2}(k_1 + k_2)$

### 3. Runge-Kutta (RK4)
A high-precision fourth-order method that takes four weighted samples of the slope across the step interval $h$.
* $k_1 = f(x_n, y_n)$
* $k_2 = f(x_n + \frac{h}{2}, y_n + \frac{h}{2}k_1)$
* $k_3 = f(x_n + \frac{h}{2}, y_n + \frac{h}{2}k_2)$
* $k_4 = f(x_n + h, y_n + h \cdot k_3)$
* **Update:** $y_{n+1} = y_n + \frac{h}{6}(k_1 + 2k_2 + 2k_3 + k_4)$

 
 