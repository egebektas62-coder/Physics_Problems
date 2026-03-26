# 4. Vector Calculus: Velocity and Acceleration

## Necessary Definitions and Formulas

### 1. Position Vector
The position vector $\vec{r}(t)$ describes the location of a particle or object in space as a function of time $t$. In two dimensions, it is typically written using the standard unit vectors $\hat{i}$ (x-direction) and $\hat{j}$ (y-direction):

$$
\vec{r}(t) = x(t)\hat{i} + y(t)\hat{j}
$$



### 2. Velocity Vector
Velocity is the rate of change of position with respect to time. It is found by taking the first derivative of the position vector.

$$
\vec{v}(t) = \frac{d\vec{r}}{dt} = x'(t)\hat{i} + y'(t)\hat{j}
$$

### 3. Acceleration Vector
Acceleration is the rate of change of velocity with respect to time. It is found by taking the derivative of the velocity vector, which is equivalent to the second derivative of the position vector.

$$
\vec{a}(t) = \frac{d\vec{v}}{dt} = \frac{d^2\vec{r}}{dt^2} = x''(t)\hat{i} + y''(t)\hat{j}
$$

### 4. The Power Rule for Derivatives
To find the derivatives in this problem, we use the power rule, which states that for $f(t) = at^n$:

$$
f'(t) = a \cdot n \cdot t^{n-1}
$$

---

## Problem Statement

The position of an object is given by $\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$. Find the object's velocity and acceleration vectors as a function of time.

---

## Step-by-Step Solution

### Step 1: Identify the components of the position vector
We are given the position vector:

$$
\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}
$$

From this, we can separate the horizontal ($x$) and vertical ($y$) components:
* $x(t) = 3t^2$
* $y(t) = 5t - 8t^2$

### Step 2: Calculate the velocity vector

To find the velocity vector, we take the first derivative of each component with respect to time $t$.

For the $x$-component:

$$
v_x(t) = \frac{d}{dt}(3t^2) = 6t
$$

For the $y$-component:

$$
v_y(t) = \frac{d}{dt}(5t - 8t^2) = 5 - 16t
$$

Now, combine these components back into vector notation:

$$
\vec{v}(t) = (6t)\hat{i} + (5 - 16t)\hat{j}
$$

### Step 3: Calculate the acceleration vector

To find the acceleration vector, we take the derivative of the velocity vector components with respect to time $t$.

For the $x$-component:

$$
a_x(t) = \frac{d}{dt}(6t) = 6
$$

For the $y$-component:

$$
a_y(t) = \frac{d}{dt}(5 - 16t) = -16
$$

Now, combine these components back into vector notation:

$$
\vec{a}(t) = 6\hat{i} - 16\hat{j}
$$

For the $x$-component:

$$
a_x(t) = \frac{d}{dt}(6t) = 6
$$

For the $y$-component:

$$
a_y(t) = \frac{d}{dt}(5 - 16t) = -16
$$

Combine these constant components into vector notation:

$$
\vec{a}(t) = 6\hat{i} - 16\hat{j}
$$

---

## Final Result

For the given position vector $\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$:

* **Velocity Vector**: 

$$
\vec{v}(t) = (6t)\hat{i} + (5 - 16t)\hat{j}
$$

* **Acceleration Vector**: 

$$
\vec{a}(t) = 6\hat{i} - 16\hat{j}
$$

*(Note that the acceleration vector contains no $t$ terms, meaning the object experiences constant acceleration).*
