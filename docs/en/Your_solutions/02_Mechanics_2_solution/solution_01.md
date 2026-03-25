# 1. Gravitational Dependence: Pendulum on the Moon

## Necessary Definitions and Formulas

### 1. Period of a Simple Pendulum
The time it takes for a simple pendulum to complete one full swing (its period) depends only on its length and the acceleration due to gravity. It is independent of the mass of the bob.



**Formula:**

$$
T = 2\pi \sqrt{\frac{L}{g}}
$$

Where:
* **$T$**: Period (time for one oscillation)
* **$L$**: Length of the pendulum
* **$g$**: Acceleration due to gravity

### 2. Proportionality
From the formula, the period $T$ is inversely proportional to the square root of gravity ($\sqrt{g}$). This means if gravity decreases, the period increases (the pendulum swings slower).

---

## Problem Statement

A simple pendulum has a period of $4$ seconds on Earth. What would its period be on the Moon, where the gravitational acceleration is about $1/6$th of Earth's?

---

## Step-by-Step Solution

### Step 1: Define the period on Earth ($T_E$)
Let $g_E$ be the acceleration due to gravity on Earth. The period on Earth is given as 4 seconds:

$$
T_E = 2\pi \sqrt{\frac{L}{g_E}} = 4
$$

### Step 2: Define the gravity on the Moon ($g_M$)
The problem states that the Moon's gravity is one-sixth of the Earth's gravity:

$$
g_M = \frac{g_E}{6}
$$

### Step 3: Set up the equation for the period on the Moon ($T_M$)
Using the exact same pendulum length $L$, the period on the Moon is:

$$
T_M = 2\pi \sqrt{\frac{L}{g_M}}
$$

### Step 4: Substitute the Moon's gravity into the equation
Replace $g_M$ with $\frac{g_E}{6}$:

$$
T_M = 2\pi \sqrt{\frac{L}{\frac{g_E}{6}}}
$$

To divide by a fraction, we multiply by its reciprocal. This brings the 6 up to the numerator inside the square root:

$$
T_M = 2\pi \sqrt{\frac{6L}{g_E}}
$$

### Step 5: Separate the constant to find the relationship
We can pull the $\sqrt{6}$ out of the main square root to see how it relates to the Earth's period:

$$
T_M = \sqrt{6} \cdot \left( 2\pi \sqrt{\frac{L}{g_E}} \right)
$$

Notice that the expression in the parentheses is exactly our formula for $T_E$. So, we can substitute $T_E$ back in:

$$
T_M = \sqrt{6} \cdot T_E
$$

### Step 6: Calculate the final numerical value
Substitute $T_E = 4$ seconds into our new proportional equation:

$$
T_M = 4\sqrt{6}
$$

Using the decimal approximation $\sqrt{6} \approx 2.449$:

$$
T_M \approx 4 \times 2.449 \approx 9.796 \text{ seconds}
$$

---

## Final Results Summary

**Period on Earth:**

$$
T_E = 4 \text{ s}
$$

**Gravity Relationship:**

$$
g_M = \frac{g_E}{6}
$$

**Period on the Moon (Exact):**

$$
T_M = 4\sqrt{6} \text{ s}
$$

**Period on the Moon (Approximate):**

$$
T_M \approx 9.796 \text{ s}
$$
