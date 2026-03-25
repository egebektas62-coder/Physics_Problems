# 3. Conservation of Energy: Pendulum Speed

## Necessary Definitions and Formulas

### 1. Conservation of Mechanical Energy
In the absence of non-conservative forces like air resistance or friction, the total mechanical energy of a system remains constant. The initial energy equals the final energy:

$$
E_i = E_f \implies K_i + U_i = K_f + U_f
$$

### 2. Kinetic and Potential Energy
* **Kinetic Energy ($K$)**: The energy of motion. Formula: $K = \frac{1}{2}mv^2$
* **Gravitational Potential Energy ($U$)**: Energy based on height. Formula: $U = mgh$

### 3. Pendulum Geometry
When a pendulum of length $L$ is pulled back by an angle $\theta$, it rises by a height $h$ relative to its lowest, resting point. 



The geometric relationship to find this exact height is:

$$
h = L - L\cos(\theta) = L(1 - \cos(\theta))
$$

---

## Problem Statement

A pendulum with a length of 1.0 meter is released from an initial angle of $15^\circ$. What is the speed of the pendulum bob at the bottom of its swing?

---

## Step-by-Step Solution

### Step 1: Define the initial and final energy states
* **Initial State (at angle $\theta = 15^\circ$)**: The pendulum is released from rest, meaning its initial velocity is zero. Therefore, initial kinetic energy $K_i = 0$. It has maximum potential energy $U_i = mgh$.
* **Final State (at the bottom of the swing)**: We set the bottom of the swing as our baseline reference level for height, so $h_f = 0$ and final potential energy $U_f = 0$. The kinetic energy is at its maximum, $K_f = \frac{1}{2}mv^2$.

### Step 2: Set up the conservation of energy equation
Equating the initial and final energies gives us:

$$
mgh = \frac{1}{2}mv^2
$$

Notice that the mass ($m$) is on both sides of the equation. We can divide both sides by $m$ to cancel it out. This proves that the speed of the pendulum at the bottom is completely independent of its mass:

$$
gh = \frac{1}{2}v^2
$$

Solving for velocity $v$:

$$
v = \sqrt{2gh}
$$

### Step 3: Calculate the change in height ($h$)
Using the pendulum geometry formula from our definitions, we find the vertical height the bob was raised before being dropped.

$$
h = L(1 - \cos(\theta))
$$

Substitute the given values ($L = 1.0 \text{ m}$ and $\theta = 15^\circ$):

$$
h = 1.0 \cdot (1 - \cos(15^\circ))
$$

Using the trigonometric value $\cos(15^\circ) \approx 0.9659$:

$$
h = 1.0 \cdot (1 - 0.9659)
$$

$$
h = 0.0341 \text{ m}
$$

### Step 4: Calculate the final speed ($v$)
Now substitute the calculated height $h$ and the standard acceleration due to gravity ($g \approx 9.8 \text{ m/s}^2$) into the isolated velocity equation:

$$
v = \sqrt{2 \cdot 9.8 \cdot 0.0341}
$$

Multiply the terms inside the square root:

$$
v = \sqrt{0.66836}
$$

Calculate the square root:

$$
v \approx 0.818 \text{ m/s}
$$

---

## Final Results Summary

**Height raised ($h$):**

$$
h \approx 0.0341 \text{ m}
$$

**Speed at the bottom of the swing ($v$):**

$$
v = \sqrt{2gh} \approx 0.818 \text{ m/s}
$$
