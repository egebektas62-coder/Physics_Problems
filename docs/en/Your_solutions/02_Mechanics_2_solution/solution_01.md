# 1. Gravitational Dependence & Pendulum Length

## Necessary Definitions and Formulas

### 1. Period of a Simple Pendulum
The time it takes for a simple pendulum to complete one full swing (its period) depends only on its length and the acceleration due to gravity. 



**Formula:**

$$
T = 2\pi \sqrt{\frac{L}{g}}
$$

Where:
* **$T$**: Period (time for one full oscillation)
* **$L$**: Length of the pendulum
* **$g$**: Acceleration due to gravity (On Earth, $g \approx 9.8 \text{ m/s}^2$)

### 2. Rearranging for Length
To find the required length for a specific period, we must isolate $L$ by squaring both sides of the period formula:

$$
L = \frac{T^2 g}{4\pi^2}
$$

---

## Problem Statement

**Part A:** A simple pendulum has a period of **4 seconds** on Earth. What would its period be on the Moon, where the gravitational acceleration is about **1/6th** of Earth's?

**Part B:** What is the required length of a simple pendulum to have a period of exactly **1 second** on Earth?

---

## Step-by-Step Solution

### Part A: Period on the Moon

**Step 1: Set up the period on Earth ($T_E$)**
Let $g_E$ be the acceleration due to gravity on Earth. We are given $T_E = 4$:

$$
T_E = 2\pi \sqrt{\frac{L}{g_E}} = 4
$$

**Step 2: Define gravity on the Moon ($g_M$)**

$$
g_M = \frac{g_E}{6}
$$

**Step 3: Calculate the period on the Moon ($T_M$)**
Substitute $g_M$ into the period formula:

$$
T_M = 2\pi \sqrt{\frac{L}{\frac{g_E}{6}}}
$$

Multiply by the reciprocal to bring the 6 to the numerator:

$$
T_M = 2\pi \sqrt{\frac{6L}{g_E}}
$$

Pull the $\sqrt{6}$ out to the front:

$$
T_M = \sqrt{6} \cdot \left( 2\pi \sqrt{\frac{L}{g_E}} \right)
$$

Since the term in the parentheses is exactly $T_E$, we substitute our known value of **4**:

$$
T_M = 4\sqrt{6}
$$

$$
T_M \approx 9.798 \text{ seconds}
$$

---

### Part B: Length for a 1-Second Period on Earth

**Step 1: Identify the known variables**
* Target period ($T$): **1 second**
* Earth's gravity ($g$): **9.8 m/s²**
* Mathematical constant ($\pi$): **$\approx 3.14159$**

**Step 2: Use the rearranged length formula**

$$
L = \frac{T^2 g}{4\pi^2}
$$

**Step 3: Substitute the values and calculate**

$$
L = \frac{(1)^2 \cdot 9.8}{4\pi^2}
$$

$$
L = \frac{9.8}{4(9.8696)}
$$

$$
L = \frac{9.8}{39.478}
$$

$$
L \approx 0.248 \text{ meters}
$$

*(Note: $0.248 \text{ meters}$ is equal to **24.8 cm**. Interestingly, if you want a pendulum that takes exactly 1 second to swing from left to right—which is a half-period, making the full period $T = 2$ seconds—the required length is nearly exactly **1 meter**. Such a pendulum is historically called a "seconds pendulum".)*

---

## Final Results Summary

**Part A: Period on the Moon**

$$
T_M = 4\sqrt{6} \approx 9.798 \text{ s}
$$

**Part B: Required Length on Earth**

$$
L \approx 0.248 \text{ m} \quad (\text{or } 24.8 \text{ cm})
$$
