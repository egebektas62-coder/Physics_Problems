# 3. Path Intersection and Collision

## Necessary Definitions and Formulas

### 1. Parametric Equations
Parametric equations define the coordinates of a moving object as functions of a single variable, typically time ($t$). For a 2D path, the position is given by a vector $P(t) = (x(t), y(t))$.

### 2. Path Intersection vs. Collision
* **Path Intersection:** Two paths cross if there is a point in space that both objects visit, even if they arrive at different times. We solve $A(t_1) = B(t_2)$ where $t_1$ and $t_2$ can be different.
* **Collision:** Two objects collide if they occupy the same exact point in space at the *exact same time*. We solve $A(t) = B(t)$.



### 3. Distance Formula and Optimization
The distance $D$ between two points $(x_1, y_1)$ and $(x_2, y_2)$ is:

$$
D = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}
$$

To find the minimum distance between two moving objects, it is mathematically easier to minimize the *square* of the distance, $S(t) = D^2(t)$, using the first derivative test ($S'(t) = 0$). The time $t$ that minimizes $S(t)$ will also minimize $D(t)$.

---

## Problem Statement

Alice is moving along a path described by $A(t) = (2+t, 8-3t)$ and Bob is moving along a path $B(t) = (2t-1, 2t+2)$. Determine if their paths intersect. If yes, determine when and where they will collide. If not, determine the minimum distance between them and when it occurs.

---

## Step-by-Step Solution

### Step 1: Check if the paths intersect
To find if the physical paths cross, we check if Alice and Bob ever visit the same $(x, y)$ coordinate, allowing for different times $t_1$ (Alice's time) and $t_2$ (Bob's time). 

Set the $x$-coordinates equal:

$$
2 + t_1 = 2t_2 - 1
$$

Isolate $t_1$:

$$
t_1 = 2t_2 - 3
$$

Set the $y$-coordinates equal, and substitute $t_1$:

$$
8 - 3t_1 = 2t_2 + 2
$$

$$
8 - 3(2t_2 - 3) = 2t_2 + 2
$$

$$
8 - 6t_2 + 9 = 2t_2 + 2
$$

$$
17 - 6t_2 = 2t_2 + 2
$$

$$
15 = 8t_2
$$

$$
t_2 = \frac{15}{8} = 1.875
$$

Now find $t_1$:

$$
t_1 = 2(1.875) - 3 = 3.75 - 3 = 0.75
$$

**Conclusion for Intersection:** Yes, the paths *do* intersect. They intersect at the coordinate $(2.75, 5.75)$. However, Alice reaches this point at $t = 0.75$ and Bob reaches it later at $t = 1.875$. 

### Step 2: Check for a collision
Because they reach the intersection point at different times ($t_1 \neq t_2$), **they do not collide**. 

*(You can also prove this by trying to solve $A(t) = B(t)$ for a single time $t$. The $x$-coordinates match at $t=3$, but at $t=3$, Alice's $y$ is $-1$ and Bob's $y$ is $8$.)*

### Step 3: Set up the distance squared function
Since they do not collide, we must find the minimum distance between them. Let $S(t)$ be the square of the distance between Alice and Bob at any given time $t$.

$$
S(t) = (x_B(t) - x_A(t))^2 + (y_B(t) - y_A(t))^2
$$

Substitute their parametric equations:

$$
S(t) = ((2t - 1) - (2 + t))^2 + ((2t + 2) - (8 - 3t))^2
$$

Simplify the terms inside the parentheses:

$$
S(t) = (t - 3)^2 + (5t - 6)^2
$$

Expand the binomials:

$$
S(t) = (t^2 - 6t + 9) + (25t^2 - 60t + 36)
$$

Combine like terms to get our optimization function:

$$
S(t) = 26t^2 - 66t + 45
$$

### Step 4: Minimize the distance function
To find the time $t$ when the distance is minimized, we take the first derivative of $S(t)$ and set it to zero.

$$
S'(t) = 52t - 66
$$

$$
52t - 66 = 0
$$

$$
52t = 66
$$

$$
t = \frac{66}{52} = \frac{33}{26} \approx 1.269
$$

*(Since $S''(t) = 52$, which is positive, this is confirmed to be a minimum).*

### Step 5: Calculate the minimum distance
Now plug $t = \frac{33}{26}$ back into the $S(t)$ equation to find the minimum distance squared. 

$$
S\left(\frac{33}{26}\right) = 26\left(\frac{33}{26}\right)^2 - 66\left(\frac{33}{26}\right) + 45
$$

$$
S\left(\frac{33}{26}\right) = \frac{1089}{26} - \frac{2178}{26} + \frac{1170}{26}
$$

$$
S\left(\frac{33}{26}\right) = \frac{1089 - 2178 + 1170}{26} = \frac{81}{26}
$$

The actual minimum distance $D_{min}$ is the square root of $S(t)$:

$$
D_{min} = \sqrt{\frac{81}{26}} = \frac{9}{\sqrt{26}}
$$

To rationalize the denominator:

$$
D_{min} = \frac{9\sqrt{26}}{26} \approx 1.765
$$

---

## Final Result

* **Do the paths intersect?** Yes, the paths cross at $(2.75, 5.75)$.
* **Do they collide?** No, because they arrive at the intersection point at different times.
* **When is the minimum distance?** It occurs at exactly $t = \frac{33}{26}$ (approx. $1.269$).
* **What is the minimum distance?** The minimum distance is $\frac{9}{\sqrt{26}}$ units (approx. $1.765$ units).
