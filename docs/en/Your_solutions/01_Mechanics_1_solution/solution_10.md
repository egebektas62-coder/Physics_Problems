# 10. Kinematics: 3D Trajectory and Path Length

## Necessary Definitions and Formulas

### 1. 3D Position, Velocity, and Speed
The position of a particle in three-dimensional space is given by a vector $\vec{r}(t)$ with $x$, $y$, and $z$ components. 

**Velocity Vector:**

$$
\vec{v}(t) = \frac{d\vec{r}}{dt} = \left( \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right)
$$

**Speed (Magnitude of Velocity):**

$$
|\vec{v}(t)| = \sqrt{v_x^2 + v_y^2 + v_z^2}
$$

### 2. Arc Length (Path Length)
The total distance $S$ traveled by a particle from time $t=0$ to $t=t_0$ is the integral of its speed over that time interval:

$$
S = \int_{0}^{t_0} |\vec{v}(t)| \,dt
$$



---

## Problem Statement

Point M moves according to the equation:

$$
\vec{r}(t) = (a \cos(\omega t), b \sin(\omega t), bt)
$$

where $a, b, \omega$ are positive constants.

**a)** Find the equation of the point's trajectory.
**b)** Compute the path length of the point from time $t=0$ to $t=t_0$.
**c)** Draw the trajectory of this point using Python. Discuss special cases.

---

## Step-by-Step Solution

### Part A: Equation of the Trajectory

We are given the parametric equations:

**X-component:**

$$
x = a \cos(\omega t)
$$

**Y-component:**

$$
y = b \sin(\omega t)
$$

**Z-component:**

$$
z = bt
$$

To find the spatial trajectory, we eliminate the time parameter $t$. 
First, let's look at $x$ and $y$. We can isolate the trigonometric functions:

$$
\frac{x}{a} = \cos(\omega t) \quad \text{and} \quad \frac{y}{b} = \sin(\omega t)
$$

Squaring both sides and adding them together uses the identity $\cos^2(\theta) + \sin^2(\theta) = 1$:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

This equation describes an **elliptical cylinder** extending infinitely along the z-axis. 

Next, we solve for $t$ using the z-component:

$$
t = \frac{z}{b}
$$

Substitute this back into the $x$ and $y$ equations:

$$
x = a \cos\left(\frac{\omega}{b} z\right)
$$

$$
y = b \sin\left(\frac{\omega}{b} z\right)
$$

**Trajectory Conclusion:** The path is an **elliptical helix** that wraps around the surface of the elliptical cylinder $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$, moving upwards along the z-axis at a constant rate.

---

### Part B: Compute the Path Length

First, we find the velocity vector by differentiating the position vector with respect to time $t$:

**Velocity components:**

$$
v_x = \frac{d}{dt}(a \cos(\omega t)) = -a\omega \sin(\omega t)
$$

$$
v_y = \frac{d}{dt}(b \sin(\omega t)) = b\omega \cos(\omega t)
$$

$$
v_z = \frac{d}{dt}(bt) = b
$$

Next, we find the speed (magnitude of the velocity):

$$
|\vec{v}(t)| = \sqrt{(-a\omega \sin(\omega t))^2 + (b\omega \cos(\omega t))^2 + (b)^2}
$$

$$
|\vec{v}(t)| = \sqrt{a^2\omega^2 \sin^2(\omega t) + b^2\omega^2 \cos^2(\omega t) + b^2}
$$

The path length $S$ from $t=0$ to $t=t_0$ is the integral of this speed:

$$
S = \int_{0}^{t_0} \sqrt{a^2\omega^2 \sin^2(\omega t) + b^2\omega^2 \cos^2(\omega t) + b^2} \,dt
$$

*Note: Unless $a = b$, this integral does not have a simple elementary antiderivative and is classified as an incomplete elliptic integral of the second kind. It would typically be solved numerically for given values of $a$ and $b$.*

---

### Part C: Python Implementation and Special Cases

#### Special Cases Discussion

1.  **Circular Helix ($a = b$):**
    If $a = b$, the base of the cylinder becomes a perfect circle ($x^2 + y^2 = a^2$). The speed formula simplifies beautifully because $\sin^2 + \cos^2 = 1$:
    
    $$|\vec{v}| = \sqrt{a^2\omega^2 + b^2}$$
    
    Since speed becomes constant, the path length integral becomes a simple multiplication: $S = t_0 \sqrt{a^2\omega^2 + b^2}$.

2.  **No Z-axis motion ($b = 0$ for the z-component):**
    If the $z$ equation was just $z=0$, the particle would simply trace a closed ellipse on the $xy$-plane over and over.

#### Python Code to Draw the Trajectory

You can run this code using standard libraries (`numpy` and `matplotlib`) to visualize the 3D elliptical helix.

```python
import numpy as np
import matplotlib.pyplot as plt

# 1. Define the positive constants
a = 5.0      # Semi-major axis
b = 3.0      # Semi-minor axis (and z-velocity factor)
omega = 2.0  # Angular frequency
t_max = 10.0 # Total time t0

# 2. Generate time values
t = np.linspace(0, t_max, 1000)

# 3. Parametric equations for the kinematic trajectory
x = a * np.cos(omega * t)
y = b * np.sin(omega * t)
z = b * t

# 4. Set up the 3D plot
fig = plt.figure(figsize=(10, 8))
ax = fig.add_subplot(111, projection='3d')

# Plot the trajectory
ax.plot(x, y, z, label='Elliptical Helix Trajectory', color='purple', linewidth=2)

# Formatting the plot
ax.set_xlabel('X axis (a * cos(wt))')
ax.set_ylabel('Y axis (b * sin(wt))')
ax.set_zlabel('Z axis (b * t)')
ax.set_title('3D Kinematics: Trajectory of Point M')
ax.legend()

# Display the interactive plot
plt.show()
