# 11. Dynamics with a Time-Dependent Force

## Necessary Definitions and Formulas

### 1. Newton's Second Law (Vector Form)
The net force acting on a particle is equal to its mass multiplied by its acceleration vector. If the force changes with time, the acceleration will also change with time.

$$
\vec{F}(t) = m\vec{a}(t) \implies \vec{a}(t) = \frac{\vec{F}(t)}{m}
$$



### 2. Kinematic Integrals
To find velocity and position from a time-dependent acceleration, we must integrate with respect to time ($t$). The initial velocity ($\vec{v}_0$) and initial position ($\vec{r}_0$) act as our constants of integration.

**Velocity:**

$$
\vec{v}(t) = \int \vec{a}(t) \,dt + \vec{v}_0
$$

**Position:**

$$
\vec{r}(t) = \int \vec{v}(t) \,dt + \vec{r}_0
$$

---

## Problem Statement

A particle of mass $m=3$ kg moves in a force field $F$ dependent on time in the following way:

$$
F = (15t, 3t-12, -6t^2) \text{ N}
$$

Assuming initial conditions $r_0=(5,2,-3)$ m, $v_0=(2,0,1)$ m/s, find the dependence of the particle's position and velocity on time.

---

## Step-by-Step Solution

### Step 1: Find the Acceleration Vector ($\vec{a}(t)$)
Divide the force vector by the mass ($m = 3$ kg).

$$
\vec{a}(t) = \frac{1}{3} (15t, 3t - 12, -6t^2)
$$

$$
\vec{a}(t) = (5t, t - 4, -2t^2) \text{ m/s}^2
$$

### Step 2: Find the Velocity Vector ($\vec{v}(t)$)
Integrate each component of the acceleration vector with respect to time, and add the initial velocity components $\vec{v}_0 = (2, 0, 1)$.

**X-component ($v_x$):**

$$
v_x(t) = \int 5t \,dt = \frac{5}{2}t^2 + C_x
$$

Since $v_x(0) = 2$, then $C_x = 2$.

$$
v_x(t) = 2.5t^2 + 2
$$

**Y-component ($v_y$):**

$$
v_y(t) = \int (t - 4) \,dt = \frac{1}{2}t^2 - 4t + C_y
$$

Since $v_y(0) = 0$, then $C_y = 0$.

$$
v_y(t) = 0.5t^2 - 4t
$$

**Z-component ($v_z$):**

$$
v_z(t) = \int -2t^2 \,dt = -\frac{2}{3}t^3 + C_z
$$

Since $v_z(0) = 1$, then $C_z = 1$.

$$
v_z(t) = -\frac{2}{3}t^3 + 1
$$

**Full Velocity Vector:**

$$
\vec{v}(t) = \left( 2.5t^2 + 2, \, 0.5t^2 - 4t, \, -\frac{2}{3}t^3 + 1 \right) \text{ m/s}
$$

### Step 3: Find the Position Vector ($\vec{r}(t)$)
Integrate each component of the velocity vector with respect to time, and add the initial position components $\vec{r}_0 = (5, 2, -3)$.

**X-component ($x$):**

$$
x(t) = \int (2.5t^2 + 2) \,dt = \frac{2.5}{3}t^3 + 2t + C_{rx}
$$

Since $x(0) = 5$, then $C_{rx} = 5$. (Note: $\frac{2.5}{3} = \frac{5}{6}$).

$$
x(t) = \frac{5}{6}t^3 + 2t + 5
$$

**Y-component ($y$):**

$$
y(t) = \int (0.5t^2 - 4t) \,dt = \frac{0.5}{3}t^3 - 2t^2 + C_{ry}
$$

Since $y(0) = 2$, then $C_{ry} = 2$. (Note: $\frac{0.5}{3} = \frac{1}{6}$).

$$
y(t) = \frac{1}{6}t^3 - 2t^2 + 2
$$

**Z-component ($z$):**

$$
z(t) = \int \left(-\frac{2}{3}t^3 + 1\right) \,dt = -\frac{2}{12}t^4 + t + C_{rz}
$$

Since $z(0) = -3$, then $C_{rz} = -3$. (Note: $-\frac{2}{12} = -\frac{1}{6}$).

$$
z(t) = -\frac{1}{6}t^4 + t - 3
$$

**Full Position Vector:**

$$
\vec{r}(t) = \left( \frac{5}{6}t^3 + 2t + 5, \, \frac{1}{6}t^3 - 2t^2 + 2, \, -\frac{1}{6}t^4 + t - 3 \right) \text{ m}
$$

---

## Final Results Summary

**Time-dependent Velocity:**

$$
\vec{v}(t) = \left( \frac{5}{2}t^2 + 2, \quad \frac{1}{2}t^2 - 4t, \quad -\frac{2}{3}t^3 + 1 \right) \text{ m/s}
$$

**Time-dependent Position:**

$$
\vec{r}(t) = \left( \frac{5}{6}t^3 + 2t + 5, \quad \frac{1}{6}t^3 - 2t^2 + 2, \quad -\frac{1}{6}t^4 + t - 3 \right) \text{ m}
$$
