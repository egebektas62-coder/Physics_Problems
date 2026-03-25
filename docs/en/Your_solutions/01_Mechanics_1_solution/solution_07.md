# 7. Elimination of Time and Interpretation of Acceleration

## Necessary Definitions and Formulas

### 1. Parametric Equations and Cartesian Trajectories
When the coordinates of a moving particle are given as functions of time, $x(t)$ and $y(t)$, these are called **parametric equations**. To find the Cartesian equation of the trajectory (the actual path in the $xy$-plane), we must eliminate the parameter $t$ by solving for $t$ in one equation and substituting it into the other, or by finding a common algebraic relationship.



### 2. Velocity and Acceleration Vectors
In 2D kinematics, position is the vector $\vec{r}(t) = x(t)\hat{i} + y(t)\hat{j}$.
* **Velocity** is the first derivative of position:

$$
\vec{v}(t) = \frac{dx}{dt}\hat{i} + \frac{dy}{dt}\hat{j}
$$

* **Acceleration** is the derivative of velocity:

$$
\vec{a}(t) = \frac{d\vec{v}}{dt} = \frac{d^2x}{dt^2}\hat{i} + \frac{d^2y}{dt^2}\hat{j}
$$

### 3. Magnitude of a Vector
The magnitude (or length/speed) of any vector $\vec{A} = A_x\hat{i} + A_y\hat{j}$ is found using the Pythagorean theorem:

$$
|\vec{A}| = \sqrt{A_x^2 + A_y^2}
$$

---

## Problem Statement

The path equation is given in parametric form:

$$
x(t) = 2t^2, \qquad y(t) = 3t^3
$$

* Eliminate the parameter $t$.
* Draw the trajectory.
* Calculate $\vec{v}(t)$, $|\vec{v}(t)|$, $\vec{a}(t)$ and $|\vec{a}(t)|$.
* Is the acceleration constant?

---

## Step-by-Step Solution

### Step 1: Eliminate the parameter $t$
We are given:
1. $x = 2t^2$
2. $y = 3t^3$

To eliminate $t$, let's manipulate both equations so they have the same power of $t$. The least common multiple of 2 and 3 is 6. 

Let's cube the first equation:

$$
x^3 = (2t^2)^3 = 8t^6
$$

Let's square the second equation:

$$
y^2 = (3t^3)^2 = 9t^6
$$

Now, solve both for $t^6$:

$$
t^6 = \frac{x^3}{8} \qquad \text{and} \qquad t^6 = \frac{y^2}{9}
$$

Set them equal to each other to completely eliminate $t$:

$$
\frac{y^2}{9} = \frac{x^3}{8}
$$

$$
y^2 = \frac{9}{8}x^3
$$

*(This defines a Cartesian curve known as a semicubical parabola).*

### Step 2: Draw the trajectory
Since this is a text-based format, we analyze the curve to understand its shape:
* Because $x = 2t^2$, $x$ must always be $\ge 0$. The graph only exists in the right half of the Cartesian plane.
* When $t > 0$, $y > 0$ (first quadrant).
* When $t < 0$, $y < 0$ (fourth quadrant).
* At $t = 0$, the particle is at $(0,0)$.
* The curve forms a sharp point (a cusp) at the origin and opens outward to the right, growing faster in the $y$-direction than the $x$-direction.



### Step 3: Calculate velocity $\vec{v}(t)$ and its magnitude $|\vec{v}(t)|$
Take the derivative of $x(t)$ and $y(t)$ with respect to $t$.

$$
v_x(t) = \frac{d}{dt}(2t^2) = 4t
$$

$$
v_y(t) = \frac{d}{dt}(3t^3) = 9t^2
$$

The velocity vector is:

$$
\vec{v}(t) = 4t\hat{i} + 9t^2\hat{j}
$$

Now, find the magnitude (speed):

$$
|\vec{v}(t)| = \sqrt{(4t)^2 + (9t^2)^2}
$$

$$
|\vec{v}(t)| = \sqrt{16t^2 + 81t^4}
$$

Factor out $t^2$ from inside the square root:

$$
|\vec{v}(t)| = \sqrt{t^2(16 + 81t^2)} = |t|\sqrt{16 + 81t^2}
$$

### Step 4: Calculate acceleration $\vec{a}(t)$ and its magnitude $|\vec{a}(t)|$
Take the derivative of the velocity components with respect to $t$.

$$
a_x(t) = \frac{d}{dt}(4t) = 4
$$

$$
a_y(t) = \frac{d}{dt}(9t^2) = 18t
$$

The acceleration vector is:

$$
\vec{a}(t) = 4\hat{i} + 18t\hat{j}
$$

Now, find its magnitude:

$$
|\vec{a}(t)| = \sqrt{(4)^2 + (18t)^2}
$$

$$
|\vec{a}(t)| = \sqrt{16 + 324t^2}
$$

Factor out $4$ to simplify:

$$
|\vec{a}(t)| = \sqrt{4(4 + 81t^2)} = 2\sqrt{4 + 81t^2}
$$

### Step 5: Is the acceleration constant?
To determine if acceleration is constant, we look at the acceleration vector $\vec{a}(t) = 4\hat{i} + 18t\hat{j}$.

While the horizontal component ($4\hat{i}$) is constant, the vertical component ($18t\hat{j}$) explicitly depends on time $t$. As time changes, the acceleration vector changes in both magnitude and direction.

---

## Final Results Summary

**Cartesian Equation:**

$$
y^2 = \frac{9}{8}x^3
$$

**Velocity Vector:**

$$
\vec{v}(t) = 4t\hat{i} + 9t^2\hat{j}
$$

**Speed (Magnitude of Velocity):**

$$
|\vec{v}(t)| = |t|\sqrt{16 + 81t^2}
$$

**Acceleration Vector:**

$$
\vec{a}(t) = 4\hat{i} + 18t\hat{j}
$$

**Magnitude of Acceleration:**

$$
|\vec{a}(t)| = 2\sqrt{4 + 81t^2}
$$

**Is acceleration constant?** **No**, because it depends on time $t$.
