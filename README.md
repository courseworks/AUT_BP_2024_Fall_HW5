<h1 align="center">
<strong>AUT_BP_2024_Fall Homework 5</strong>
</h1>

<p align="center">
<strong> Deadline: 16th of Azar - Friday - 23:59 o'clock</strong>
</p>

---

## **Question 1: Implementing Newton-Raphson Method for Root Finding**

### **Objective**

In this question, you will implement the Newton-Raphson method for finding the root of a function. The function should accept a pointer to the function whose root is to be found, along with the initial guess. The algorithm must continue iterating until the difference between two consecutive iterations is less than `1e-6`.

### **Explanation of Newton-Raphson Method**

The Newton-Raphson method is an iterative technique used to find the root of a real-valued function. The algorithm begins with an initial guess \( x_0 \), and then iteratively refines this guess to get closer to the actual root.

The formula used in each iteration is:

<p align="center">
<img src="https://latex.codecogs.com/svg.latex?x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}" alt="Newton-Raphson formula" style="width: 20%;">
</p>

In this implementation, the algorithm will continue iterating until the absolute difference between two consecutive approximations is smaller than a tolerance of \( 1e-6 \), indicating that the solution has converged.

**_For simplicity, You may assume that the function passed to `newtonRaphson` has exactly one real root._**

### **Function Prototype**

```c
double newtonRaphson(double (*func)(double), double initial);

double derivative(double (*func)(double), double x);
```

### **Detailed Description**

1. **`newtonRaphson`**: This function takes a function pointer `func` (to the function whose root we are trying to find) and an initial guess `initial`. It applies the Newton-Raphson method iteratively until the difference between two consecutive approximations is less than \( 1e-6 \). The function will return the estimated root.

2. **`derivative`**: This function computes the derivative of the given function `func` at a point `x`. The derivative is approximated using the difference quotient:

<p align="center">
<img src="https://latex.codecogs.com/svg.latex?f'(x)%20%5Capprox%20%5Cfrac%7Bf(x+h)%20-%20f(x)%7D%7Bh%7D" alt="Derivative approximation formula" style="width: 20%;">
</p>

Where \( h \) is a small value (e.g., \( h = 0.0001 \)).

The Newton-Raphson method is stopped when the difference between two consecutive approximations is smaller than \( 1e-6 \), which ensures that the algorithm has converged to a solution.

<p align="center">
  <img src="./resource/NewtonIteration_Ani.gif" alt="Newton Raphson Animation" style="width: 80%;">
</p>

### **Example**

#### **Input**

```c
double func(double x) {
    return x*x - 4;  // Example function f(x) = x^2 - 4
}
```

#### **Function Call**

```c
double root = newtonRaphson(func, -1.0);
```

#### **Expected Output**

For the example function \( f(x) = x^2 - 4 \), the root should be approximately \( 2.0 \), since the exact root is \( x = 2 \). The function `newtonRaphson` should return a value close to \( 2.0 \) after running the algorithm.

### **Notes**

-   The `newtonRaphson` function should stop when the absolute difference between two consecutive guesses is less than \( 1e-6 \).
-   You may assume that the function passed to `newtonRaphson` has exactly one real root.

---

If you have any questions regarding the homework, feel free to reach out:

-   **Teaching Assistant**: Seyyed Mohammad Hamidi
-   **Telegram Group**: [t.me/AUT_BP_Fall_2024](https://t.me/AUT_BP_Fall_2024)
-   **Github**: [github.com/smhamidi](https://github.com/smhamidi)

---

<p align="center">
  <img src="./resource/NoWarInBaSingSe.webp" alt="No War in ba sing se" style="width: 40%;">
</p>

**Best Regards, [Hamidi](https://github.com/smhamidi)**
