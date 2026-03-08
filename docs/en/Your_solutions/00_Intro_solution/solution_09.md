# 9. Optimization Problem: Maximizing Area Under a Curve

## Necessary Definitions and Formulas

### 1. Optimization in Calculus
Optimization involves finding the absolute maximum or minimum value of a function within a given domain. In geometry problems, this often means maximizing area or volume, or minimizing cost or distance.

### 2. Area of a Rectangle
The fundamental formula for the area of a rectangle is:

$$
A = \text{width} \times \text{height}
$$

### 3. First and Second Derivative Tests for Extrema
To find the maximum of a function $A(x)$:
* **First Derivative**: Find the critical points by setting $A'(x) = 0$.
* **Second Derivative Test**: Evaluate $A''(x)$ at the critical points. If $A''(x) < 0$, the function is concave down at that point, indicating a **local maximum**.



---

## Problem Statement

A rectangle is under the curve $y = 3 - x^2$ in the first quadrant. What are the dimensions of the rectangle with the maximum area?

---

## Step-by-Step Solution

### Step 1: Define the variables and the objective function
The rectangle is in the first quadrant (where $x \ge 0$ and $y \ge 0$). 
* Its bottom-left corner is at the origin $(0,0)$.
* Its bottom-right corner is at $(x, 0)$ on the x-axis.
* Its top-right corner touches the curve at $(x, y)$.
* Its top-left corner is at $(0, y)$ on the y-axis.

The width of the rectangle is $x$ and the height is $y$. The objective function we want to maximize is the area $A$:

$$
A = x \cdot y
$$

### Step 2: Express the area as a function of a single variable
Since the top-right corner of the rectangle touches the curve, we know that $y = 3 - x^2$. We can substitute this expression into our area formula so that it only depends on $x$:

$$
A(x) = x(3 - x^2)
$$

Distribute the $x$:

$$
A(x) = 3x - x^3
$$

### Step 3: Find the first derivative of the area function
To find the maximum area, we need to find the critical points. We do this by taking the first derivative of $A(x)$ with respect to $x$:

$$
A'(x) = 3 - 3x^2
$$

### Step 4: Find the critical points
Set the first derivative equal to zero to find the critical points:

$$
3 - 3x^2 = 0
$$

Divide by 3:

$$
1 - x^2 = 0
$$

$$
x^2 = 1
$$

Taking the square root gives $x = 1$ or $x = -1$. Since the rectangle is in the first quadrant, $x$ must be positive. Therefore, our critical point is:

$$
x = 1
$$

### Step 5: Verify the maximum using the Second Derivative Test
To ensure this critical point gives a maximum (and not a minimum), we find the second derivative $A''(x)$:

$$
A''(x) = -6x
$$

Evaluate the second derivative at our critical point $x = 1$:

$$
A''(1) = -6(1) = -6
$$

Since $-6 < 0$, the function is concave down at $x = 1$, confirming that this point yields a **maximum** area.

### Step 6: Calculate the corresponding y-value (height)
Now that we have the optimal width ($x = 1$), we substitute it back into the equation of the curve to find the optimal height ($y$):

$$
y = 3 - (1)^2
$$

$$
y = 3 - 1
$$

$$
y = 2
$$

---

## Final Result

The dimensions of the rectangle with the maximum area under the curve $y = 3 - x^2$ in the first quadrant are:
* **Width ($x$)**: $1$
* **Height ($y$)**: $2$

*(The maximum area itself is $1 \times 2 = 2$ square units).*
