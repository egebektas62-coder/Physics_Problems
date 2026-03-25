# 6. Variable Velocity: Position and Acceleration

## Necessary Definitions and Formulas

### 1. Kinematic Relationships (Calculus)
In physics, the position $x(t)$, velocity $v(t)$, and acceleration $a(t)$ of an object moving in one dimension are directly linked through calculus.

* **Acceleration** is the derivative of velocity with respect to time:

$$
a(t) = \frac{dv}{dt}
$$

* **Position** is the antiderivative (indefinite integral) of velocity with respect to time:

$$
x(t) = \int v(t) \,dt
$$



### 2. The Power Rule for Integrals
When integrating a polynomial term $t^n$ (where $n \neq -1$), the rule is to add 1 to the exponent and divide by the new exponent, plus a constant of integration $C$:

$$
\int t^n \,dt = \frac{t^{n+1}}{n+1} + C
$$

### 3. Initial Value Problem
When you integrate velocity to find position, you generate an unknown constant $C$. To find the exact position function, you must use an initial condition (a known position at a specific time) to solve for $C$.

---

## Problem Statement

An object's velocity is given by $v(t) = t^2 + 2t - 5$. If the object was at $x=4$ at $t=0$, what is its position and acceleration at time $t=3$?

---

## Step-by-Step Solution

### Part A: Determine the Acceleration at $t=3$

**Step 1: Find the acceleration function $a(t)$**
We take the first derivative of the velocity function $v(t)$ using the power rule.

Given:

$$
v(t) = t^2 + 2t - 5
$$

Differentiating with respect to time $t$:

$$
a(t) = \frac{d}{dt}(t^2 + 2t - 5)
$$

$$
a(t) = 2t + 2
$$

**Step 2: Evaluate acceleration at $t=3$**
Substitute $t=3$ into our new acceleration function.

$$
a(3) = 2(3) + 2
$$

$$
a(3) = 6 + 2 = 8
$$

The acceleration at $t=3$ is **8**.

---

### Part B: Determine the Position at $t=3$

**Step 1: Find the general position function $x(t)$**
We integrate the velocity function $v(t)$ with respect to time $t$ to find the position.

$$
x(t) = \int (t^2 + 2t - 5) \,dt
$$

Apply the power rule for integration to each term:

$$
x(t) = \frac{t^3}{3} + \frac{2t^2}{2} - 5t + C
$$

Simplify the equation:

$$
x(t) = \frac{1}{3}t^3 + t^2 - 5t + C
$$

**Step 2: Solve for the constant of integration ($C$)**
We are given the initial condition that at $t=0$, the position $x=4$. We plug these values into our general position function to find $C$.

$$
4 = \frac{1}{3}(0)^3 + (0)^2 - 5(0) + C
$$

$$
4 = 0 + 0 - 0 + C
$$

$$
C = 4
$$

Now we can write the exact position function for this object:

$$
x(t) = \frac{1}{3}t^3 + t^2 - 5t + 4
$$

**Step 3: Evaluate position at $t=3$**
Substitute $t=3$ into the exact position function.

$$
x(3) = \frac{1}{3}(3)^3 + (3)^2 - 5(3) + 4
$$

Calculate the exponents and multiplications:

$$
x(3) = \frac{1}{3}(27) + 9 - 15 + 4
$$

$$
x(3) = 9 + 9 - 15 + 4
$$

Add and subtract left to right:

$$
x(3) = 18 - 15 + 4
$$

$$
x(3) = 3 + 4 = 7
$$

The position at $t=3$ is **7**.

---

## Final Result

For the given object at time $t=3$:
* **Acceleration**: **8** (units/s²)
* **Position**: **7** (units)
