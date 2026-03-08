# 6. Function Analysis: Local Maxima and Minima

## Necessary Definitions and Formulas

### 1. Critical Points
A critical point of a function $f(x)$ occurs where the first derivative is equal to zero ($f'(x) = 0$) or is undefined. These are the candidate points for local maxima or minima.

### 2. First Derivative ($f'(x)$)
The first derivative represents the slope of the tangent line to the function at any given point.
* If $f'(x) > 0$, the function is increasing.
* If $f'(x) < 0$, the function is decreasing.

### 3. Second Derivative Test ($f''(x)$)
The second derivative helps determine the concavity of the function and classifies the critical points:
* If $f''(c) > 0$ at a critical point $c$, the function is concave up, and there is a **local minimum**.
* If $f''(c) < 0$ at a critical point $c$, the function is concave down, and there is a **local maximum**.



### 4. Quadratic Functions (Alternative Method)
For a quadratic function in the form $f(x) = ax^2 + bx + c$, the graph is a parabola. 
* If $a > 0$, it opens upwards (having a global/local minimum).
* The x-coordinate of the vertex (the minimum or maximum) can be found using the formula:

$$
x = -\frac{b}{2a}
$$

---

## Problem Statement

Consider the function $f(x) = 3x^2 - 12x + 7$. Identify any local maxima or minima.

---

## Step-by-Step Solution

We will use calculus (the derivative method) to analyze this function.

### Step 1: Find the first derivative of the function
To find the critical points, we first need to differentiate the function $f(x)$ with respect to $x$ using the power rule.

Given:

$$
f(x) = 3x^2 - 12x + 7
$$

The first derivative is:

$$
f'(x) = 6x - 12
$$

### Step 2: Find the critical points
Set the first derivative equal to zero to find the x-values where the slope is zero.

$$
6x - 12 = 0
$$

Add 12 to both sides:

$$
6x = 12
$$

Divide by 6:

$$
x = 2
$$

So, $x = 2$ is our critical point.

### Step 3: Classify the critical point using the Second Derivative Test
To determine if this point is a maximum or minimum, we find the second derivative $f''(x)$ by differentiating $f'(x)$.

$$
f''(x) = 6
$$

Since $f''(2) = 6$, and $6 > 0$, the function is concave up at $x = 2$. Therefore, a **local minimum** exists at this point. 

*(Note: Because $a = 3$ in our original quadratic equation and $3 > 0$, this confirms the parabola opens upwards.)*

### Step 4: Find the y-coordinate of the local minimum
To find the actual minimum value of the function, substitute $x = 2$ back into the original equation $f(x)$.

$$
f(2) = 3(2)^2 - 12(2) + 7
$$

Calculate the exponent first:

$$
f(2) = 3(4) - 24 + 7
$$

Multiply:

$$
f(2) = 12 - 24 + 7
$$

Add and subtract left to right:

$$
f(2) = -12 + 7
$$

$$
f(2) = -5
$$

---

## Final Result

The function $f(x) = 3x^2 - 12x + 7$ has a **local minimum** at the point **$(2, -5)$**. There are no local maxima.
