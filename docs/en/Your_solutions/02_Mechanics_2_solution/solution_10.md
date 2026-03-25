# 10. Force Field and Power: 3D Kinematics and Dynamics

## Necessary Definitions and Formulas

### 1. Kinematic Vectors
The position of a particle in 3D space is given by its position vector $\vec{r}(t)$. The velocity $\vec{v}(t)$ and acceleration $\vec{a}(t)$ are its first and second time derivatives, respectively:

$$
\vec{v}(t) = \frac{d\vec{r}}{dt} = \left( \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right)
$$

$$
\vec{a}(t) = \frac{d\vec{v}}{dt} = \left( \frac{d^2x}{dt^2}, \frac{d^2y}{dt^2}, \frac{d^2z}{dt^2} \right)
$$

### 2. Momentum and Force
* **Momentum ($\vec{p}$):** The product of mass and velocity.

$$
\vec{p}(t) = m\vec{v}(t)
$$

* **Force ($\vec{F}$):** According to Newton's Second Law, force is mass times acceleration (or the time derivative of momentum).

$$
\vec{F}(t) = m\vec{a}(t)
$$

### 3. Power ($P$)
Power is the rate at which work is done or energy is transferred. In a force field, the instantaneous power transferred to a particle is the dot product of the force vector and the velocity vector.



$$
P(t) = \vec{F}(t) \cdot \vec{v}(t) = F_x v_x + F_y v_y + F_z v_z
$$

---

## Problem Statement

In a certain force field, the equations of motion of a particle with mass $m = 0.5$ kg are as follows:

$$
x = 5t^2 - t, \quad y = 2t^3, \quad z = -3t + 2
$$

Find the time dependence of: the particle's velocity, the particle's momentum, the particle's acceleration, the force acting on the particle, and the power transferred by the field to the particle.

---

## Step-by-Step Solution

### Step 1: Find the Velocity Vector ($\vec{v}(t)$)
Take the first time derivative of each position component:

$$
v_x = \frac{d}{dt}(5t^2 - t) = 10t - 1
$$

$$
v_y = \frac{d}{dt}(2t^3) = 6t^2
$$

$$
v_z = \frac{d}{dt}(-3t + 2) = -3
$$

So, the velocity vector is:

$$
\vec{v}(t) = (10t - 1)\hat{i} + (6t^2)\hat{j} - 3\hat{k}
$$

### Step 2: Find the Momentum Vector ($\vec{p}(t)$)
Multiply the velocity vector by the mass ($m = 0.5$ kg):

$$
\vec{p}(t) = 0.5 \cdot \vec{v}(t)
$$

$$
\vec{p}(t) = 0.5(10t - 1)\hat{i} + 0.5(6t^2)\hat{j} + 0.5(-3)\hat{k}
$$

$$
\vec{p}(t) = (5t - 0.5)\hat{i} + (3t^2)\hat{j} - 1.5\hat{k}
$$

### Step 3: Find the Acceleration Vector ($\vec{a}(t)$)
Take the time derivative of the velocity components:

$$
a_x = \frac{d}{dt}(10t - 1) = 10
$$

$$
a_y = \frac{d}{dt}(6t^2) = 12t
$$

$$
a_z = \frac{d}{dt}(-3) = 0
$$

So, the acceleration vector is:

$$
\vec{a}(t) = 10\hat{i} + 12t\hat{j} + 0\hat{k}
$$

### Step 4: Find the Force Vector ($\vec{F}(t)$)
Multiply the acceleration vector by the mass ($m = 0.5$ kg):

$$
\vec{F}(t) = 0.5 \cdot \vec{a}(t)
$$

$$
\vec{F}(t) = 0.5(10)\hat{i} + 0.5(12t)\hat{j}
$$

$$
\vec{F}(t) = 5\hat{i} + 6t\hat{j} + 0\hat{k}
$$

### Step 5: Find the Power Transferred ($P(t)$)
Calculate the dot product of Force and Velocity: $P = \vec{F} \cdot \vec{v} = F_x v_x + F_y v_y + F_z v_z$.

$$
P(t) = (5)(10t - 1) + (6t)(6t^2) + (0)(-3)
$$

Distribute and simplify:

$$
P(t) = 50t - 5 + 36t^3 + 0
$$

Rearranging in descending order of powers:

$$
P(t) = 36t^3 + 50t - 5 \text{ Watts}
$$

---

## Final Results Summary

**Velocity:**

$$
\vec{v}(t) = (10t - 1)\hat{i} + 6t^2\hat{j} - 3\hat{k} \text{ m/s}
$$

**Momentum:**

$$
\vec{p}(t) = (5t - 0.5)\hat{i} + 3t^2\hat{j} - 1.5\hat{k} \text{ kg}\cdot\text{m/s}
$$

**Acceleration:**

$$
\vec{a}(t) = 10\hat{i} + 12t\hat{j} \text{ m/s}^2
$$

**Force:**

$$
\vec{F}(t) = 5\hat{i} + 6t\hat{j} \text{ N}
$$

**Power:**

$$
P(t) = 36t^3 + 50t - 5 \text{ W}
$$
