# 12. Work and Energy with a Constant Force

## Necessary Definitions and Formulas

### 1. Constant Acceleration Kinematics (Vector Form)
When a constant force acts on a mass, the acceleration is constant. We can find the velocity and position vectors by integrating with respect to time $t$.

**Velocity:**

$$
\vec{v}(t) = \int \vec{a} \,dt = \vec{a}t + \vec{v}(0)
$$

**Position:**

$$
\vec{r}(t) = \int \vec{v}(t) \,dt = \frac{1}{2}\vec{a}t^2 + \vec{v}(0)t + \vec{r}(0)
$$

### 2. Work Done by a Constant Force
If the force is constant, the work done ($W$) over a displacement ($\Delta\vec{r}$) is the dot product (scalar product) of the force vector and the displacement vector.

$$
W = \vec{F} \cdot \Delta\vec{r} = F_x \Delta x + F_y \Delta y
$$



### 3. The Work-Energy Theorem
The net work done on an object equals its change in kinetic energy ($\Delta K$). 

$$
W = \Delta K = K_f - K_i
$$

Where Kinetic Energy is:

$$
K = \frac{1}{2}m|\vec{v}|^2 = \frac{1}{2}m(v_x^2 + v_y^2)
$$

---

## Problem Statement

A constant force acts on a body of mass $m = 2 \text{ kg}$:

$$
\vec{F} = [6, 2] \text{ N}
$$

The body starts with an initial velocity $\vec{v}(0) = (1, -1) \text{ m/s}$ from the point $\vec{r}(0) = (0, 0) \text{ m}$.
* Determine $\vec{a}(t)$.
* Determine $\vec{v}(t)$.
* Determine $\vec{r}(t)$.
* Draw the trajectory of the motion.
* Calculate the work done by the force at time $t=3 \text{ s}$.
* Check the consistency with the work-energy theorem.

---

## Step-by-Step Solution

### Part A: Determine Acceleration $\vec{a}(t)$
Using Newton's Second Law ($\vec{F} = m\vec{a}$):

$$
\vec{a}(t) = \frac{\vec{F}}{m} = \left[ \frac{6}{2}, \frac{2}{2} \right]
$$

$$
\vec{a}(t) = [3, 1] \text{ m/s}^2
$$

Since the force is constant, the acceleration is also constant.

### Part B: Determine Velocity $\vec{v}(t)$
Integrate the acceleration vector and add the initial velocity $\vec{v}(0) = [1, -1]$:

$$
\vec{v}(t) = \int [3, 1] \,dt + [1, -1]
$$

$$
\vec{v}(t) = [3t, t] + [1, -1]
$$

Combine the components:

$$
\vec{v}(t) = [3t + 1, \, t - 1] \text{ m/s}
$$

### Part C: Determine Position $\vec{r}(t)$
Integrate the velocity vector and add the initial position $\vec{r}(0) = [0, 0]$:

$$
\vec{r}(t) = \int [3t + 1, \, t - 1] \,dt + [0, 0]
$$

Integrate component by component:

$$
x(t) = \frac{3}{2}t^2 + t
$$

$$
y(t) = \frac{1}{2}t^2 - t
$$

Combine into vector form:

$$
\vec{r}(t) = [1.5t^2 + t, \, 0.5t^2 - t] \text{ m}
$$

### Part D: Draw the Trajectory
The parametric equations $x(t) = 1.5t^2 + t$ and $y(t) = 0.5t^2 - t$ define a **parabola** in the 2D plane. Below is the Python code using `matplotlib` to visualize this trajectory from $t=0$ to $t=3$.

```python
import numpy as np
import matplotlib.pyplot as plt

# Generate time values from 0 to 3 seconds
t = np.linspace(0, 3, 100)

# Parametric equations for position
x = 1.5 * t**2 + t
y = 0.5 * t**2 - t

# Create the plot
plt.figure(figsize=(8, 6))
plt.plot(x, y, label='Trajectory of the body', color='purple', linewidth=2)
plt.scatter(x[0], y[0], color='green', zorder=5, label='Start (t=0)')
plt.scatter(x[-1], y[-1], color='red', zorder=5, label='End (t=3)')

# Formatting
plt.title('2D Trajectory of the Motion')
plt.xlabel('Position X (m)')
plt.ylabel('Position Y (m)')
plt.axhline(0, color='black', linewidth=0.5)
plt.axvline(0, color='black', linewidth=0.5)
plt.grid(True, linestyle='--')
plt.legend()
plt.show()
