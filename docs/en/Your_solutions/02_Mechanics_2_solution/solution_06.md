# 6. Energy Dissipation: Bouncing Ball

## Necessary Definitions and Formulas

### 1. Gravitational Potential Energy
At the highest point of its bounce, the ball momentarily stops. At this exact moment, all of its mechanical energy is in the form of gravitational potential energy.

**Formula:**

$$
U = mgh
$$

Where:
* **$U$**: Potential energy
* **$m$**: Mass of the object
* **$g$**: Acceleration due to gravity
* **$h$**: Height above the ground



### 2. Energy Dissipation (Loss)
When the ball hits the ground, it deforms, generates sound, and creates heat. This means the collision is inelastic, and a percentage of its total mechanical energy is "lost" to the environment. 

If a system loses a certain percentage of energy, the remaining energy $E_{new}$ is:

$$
E_{new} = E_{old} \cdot (1 - \text{loss fraction})
$$

---

## Problem Statement

A tennis ball is dropped from a height of 2.0 m. After each bounce, it loses 30% of its mechanical energy. To what height does it rise after the second bounce?

---

## Step-by-Step Solution

### Step 1: Define the initial state
Let $h_0$ be the initial drop height (2.0 m). The initial mechanical energy $E_0$ is entirely potential energy:

$$
E_0 = mgh_0
$$

### Step 2: Determine the energy remaining after each bounce
The problem states the ball loses 30% (or 0.30) of its energy upon bouncing. Therefore, it retains 70% (or 0.70) of its energy after each bounce.

**Energy after the 1st bounce ($E_1$):**

$$
E_1 = 0.70 \cdot E_0
$$

**Energy after the 2nd bounce ($E_2$):**

$$
E_2 = 0.70 \cdot E_1 = 0.70 \cdot (0.70 \cdot E_0) = 0.70^2 \cdot E_0
$$

### Step 3: Relate the remaining energy to height
At the peak of any bounce, the kinetic energy is zero, and the remaining mechanical energy is purely potential ($E = mgh$). 

For the second bounce, the energy is $E_2$ and the peak height is $h_2$:

$$
E_2 = mgh_2
$$

We also know from Step 2 that:

$$
E_2 = 0.70^2 \cdot (mgh_0)
$$

Set these two equations equal to each other:

$$
mgh_2 = 0.70^2 \cdot mgh_0
$$

### Step 4: Solve for the height after the second bounce ($h_2$)
Notice that the mass ($m$) and gravity ($g$) are on both sides of the equation. We can cancel them out. This proves that the bounce height is independent of the ball's mass or the local gravity.

$$
h_2 = 0.70^2 \cdot h_0
$$

Substitute the initial height $h_0 = 2.0$ m:

$$
h_2 = (0.49) \cdot 2.0
$$

Multiply to find the final height:

$$
h_2 = 0.98 \text{ m}
$$

---

## Final Results Summary

**Initial Height ($h_0$):** 2.0 m

**Energy retained per bounce:** 70%

**Height after 1st bounce ($h_1$):** $$
h_1 = 0.70 \cdot 2.0 = 1.4 \text{ m}
$$

**Height after 2nd bounce ($h_2$):** $$
h_2 = 0.49 \cdot 2.0 = 0.98 \text{ m}
$$
